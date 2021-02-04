# Extra View Modes

Extra View Modes are a way of creating your own templates for items list visualization. By default, Tainacan offers the following view modes:

- Table
- Cards
- Records
- Masonry
- Thumbnails
- Slideshow
- List

Each has it's specificities, but in case you're not satisfied with them, a developer can easily create a plugin to offer a custom template for displaying items list.

## Creating your extra view mode

As shown in [our post for extra view modes](http://tainacan.org/2018/06/13/custom-view-modes-how-will-the-world-see-your-collection/), we've created [a sample plugin](https://wordpress.org/plugins/tainacan-extra-view-modes/) with some inspirational ideas for custom view modes, such as this one:

![Image with an example of an extra view mode, showing borders around items thumbnail.](/_assets/images/Example_of_an_Extra_View_Mode.jpeg)

We here describe the process to create such a plugin. You will need three files:

1. The _.php_ file for registering the plugin and view mode;
2. The _.php_ file with the items list template;
3. The _.css_ file with the styling for your template;

### Registering your plugin

As in any WordPress Plugin, you'll first need to create a php header as follows:

```php
<?php
/*
Plugin Name: Name of Your Extra View Mode Plugin
Plugin URI: A URL for a related link
Description: An extra view modes plugin for Tainacan
Author: Your Name Here
Version: 0.1
License: GPLv2 or later
License URI: http://www.gnu.org/licenses/gpl-3.0.html
*/

defined( 'ABSPATH' ) or die( 'No script kiddies please!' );
```

Only Plugin Name is obligatory. Save the file with a name unique to your plugin (a good practice is to use the plugin name, such as `name-of-your-extra-view-mode-plugin.php`).

The rest of the file will contain the register function for your view mode. We discuss it in details ahead:

```php
add_action( 'after_setup_theme', function() {

	tainacan_register_view_mode('MyViewMode', [
		'label' => 'My View Mode',
		'icon' => '<span class="icon"><i class="mdi mdi-view-quilt mdi-24px"></i></span>',
		'description' => 'This is my view mode. It looks great the way it is.',
		'dynamic_metadata' => false,
		'template' => __DIR__ . './my-view-mode.php',
	]);

} );

?> /* End of file */
```

The function `tainacan_register_view_mode` is part of Tainacan's plugin. Its first parameter is a unique _slug_ that will be used to identify your view mode. Then follows an array of parameters:

| Type   | Name                | Description                                                                                                                                                                               | Default                                     |
| ------ | ------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------- |
| string | label               | Label, visible to users on the view modes dropdown.                                                                                                                                       | Same of the variable `$slug`                |
| string | icon                | HTML that outputs an icon that represents the view mode. Visible to users on view modes dropdown.                                                                                         | None                                        |
| string | description         | Description, visible only to editors in the admin.                                                                                                                                        | None                                        |
| string | type                | Type. Accepted values are 'template' or 'component'.                                                                                                                                      | _template_                                  |
| string | template            | Full path to the template file to be used. Required if $type is set to template.                                                                                                          | _theme-path/tainacan/view-mode-`$slug`.php_ |
| string | component           | Component tag name. The web component js must be included and must accept two props: 1) items: the list of items to be rendered; 2) displayed-metadata: list of metadata to be displayed; | _view-mode-`$slug`_                         |
| string | thumbnail           | Full URL to a thumbnail that represents the view mode. Displayed only in Admin.                                                                                                           | None                                        |
| string | skeleton_template   | HTML that outputs a preview of the items to be loaded, such as gray blocks, mimicking the shape of the items.                                                                             | None                                        |
| bool   | show_pagination     | Whether to display or not pagination controls.                                                                                                                                            | `true`                                      |
| bool   | full_screen         | Whether the view mode will display full screen or not.                                                                                                                                    | `false`                                     |
| bool   | dynamic_metadata    | Whether to display or not (and use or not) the "displayed metadata" selector.                                                                                                             | `false`                                     |
| bool   | implements_skeleton | Whether the view modes take care of showing it's own Skeleton/Ghost css classes for loading items.                                                                                        | `false`                                     |

The `type` parameter is one of the most relevant here. When registering view modes, you can either create a simple PHP `template` using WordPress functions (as the ones in our sample plugin) or more complex Vue.js `component`. When passing a template, the file path should be provided, while for components the name of previously loaded .vue component must be provided. Vue components must also have two props, one for receiving the items list as a parsed JSON Object and other for an array of metadata that will be displayed.

<div style="float: right; margin-left: 1rem;">
	<img 
		alt="Enabled Metadata Dropdown.png" 
		src="/dev/_assets/images/Enabled_Metadata_Dropdown.png"
		width="300"
		height="256">
</div>

View modes as Cards and Grid do not allow users to choose which metadata should be displayed, but rather decide that only certain will be visible. For this kind of view mode, it is used the `dynamic_metadata` parameter as `false`.

By default, a spinning circle loading animation is shown when items are being fetched. Most of our official view modes override this by implementing a so-called skeleton/ghost list, that mimics a list of gray blocks in the shape of items before they arrived. If your view mode does that, you should set `implements_skeleton` to true and provide an HTML template with such skeleton to `skeleton_template`. Tainacan will take care of rendering this skeleton while items are being loaded.

## Making an extra view mode template

The file path indicated on the register above should point to the .php file where your template lives. It will probably have some structure similar to the following sample:

```php
<?php if ( have_posts() ) : ?>

	<div class="my-view-mode-container">

		<?php while ( have_posts() ) : the_post(); ?>

			<a class="my-view-mode-item" href="<?php the_permalink(); ?>">
				<div class="media">

					<?php if ( tainacan_current_view_displays('thumbnail') ): ?>
						<a href="<?php the_permalink(); ?>">
							<?php if ( has_post_thumbnail() ): ?>
								<?php the_post_thumbnail('tainacan-medium', array('class' => 'mr-4')); ?>
							<?php else: ?>
								<?php echo '<div class="mr-4"><img alt="Thumbnail placeholder" src="'.get_stylesheet_directory_uri().'/assets/images/thumbnail_placeholder.png"></div>'?>
							<?php endif; ?>

						</a>
					<?php endif; ?>

					<div class="list-metadata media-body">
						<?php if ( tainacan_current_view_displays('title') ): ?>
							<p class="metadata-title">
								<a href="<?php the_permalink(); ?>">
									<?php the_title(); ?>
								</a>
							</p>
						<?php endif; ?>
						<?php tainacan_the_metadata(array('metadata__in' => $view_mode_displayed_metadata['meta'], 'exclude_title' => true, 'before_title' => '<h3 class="metadata-label">', 'before_value' => '<p class="metadata-value">')); ?>
					</div>
				</div>
			</a>

		<?php endwhile; ?>

	</div>

<?php else : ?>

	<div class="my-view-mode-container">
		<section class="section">
			<div class="content has-text-gray4 has-text-centered">
				<p>
					<span class="icon is-large">
						<i class="mdi mdi-48px mdi-file-multiple"></i>
					</span>
				</p>
				<p>'No item was found.','tainacan-interface'</p>
			</div>
		</section>
	</div>

<?php endif; ?>
```

The classes `my-view-mode-container` and `my-view-mode-item`, and so forth should be implemented by you on your style file. Other classes as the `skeleton`, `section` are part of Tainacan's plugin CSS, and can be used if you wish to keep a standard.

Thumbnail is obtained via the function `the_post_thumbnail()`, which accepts as first parameter any of the following:

- `tainacan-small` (40px width, 40px height, cropped);
- `tainacan-medium` (275px width, 275 height, cropped);
- `tainacan-medium-full`, (max. 205px width, max. 1500px height, not cropped );

You can see that this view mode displays the array of metadata obtained from `tainacan_the_metadata()` function.
