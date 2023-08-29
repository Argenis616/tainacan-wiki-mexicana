# Understanding Tainacan

The typical workflow when you create a Digital Repository with Tainacan is:

* Create a collection
* Choose which metadata the item in this collections will have
* Choose which filters will be used when browsing the collection
* Insert items to the collection or import them from an external source

## Collections

A collection is a group of items, that share the same set of metadata. Every item uploaded to your digital repository will be part of a collection - and only one collection. For instance, you could have a "paintings" collections, with metadata such as Title, Author, Country, Technique, etc and another collection for "films", with Title, Director, Country, and Genre.

For each collection, you can set a different set of metadata and they can share common taxonomies, which means you could browse for items in a specific Country, and get both paintings and films in your results. 

Collections can also have child collections, which will inherit the parent's collection metadata and can add their own set of additional information.

## Items

Items are the actual content of your repository. The painting, the film, the book and so on. They belong to a collection and have all the metadata configured in the collection it belongs to.

In WordPress language, each item is a post and its post type represents its collection.

### Document 

The document is the main information of the item. It is the object which all metadata refer to. Tainacan accepts 3 different document types:

* File: A file attached to the item. An image, video, pdf, audio or other media file.
* URL: An URL pointing to an external website or file. It can be a general website, a specific file, or media services. In the case of media services, Tainacan recognizes addresses and displays the appropriate player, using [oEmbed](https://oembed.com/). A list of services automatically converted to embeds by WordPress can be found [here](https://codex.wordpress.org/Embeds).
* Text: A plain text, stored directly in the database, the user can type upon creating or editing an item

## Metadata

Data about the Document. 

Every collection declares a set of metadata to describe its documents. This means that the collection the item belongs to will determine the metadata it will have.

Each metadata has a set of settings. Is it required? Is it supposed to be unique (an ID number for example)? Does it accept multiple values? Which is its Metadata Type? (TODO: see the complete list of metadata attributes).

You may have repository-level metadata, that will be inherited by all collections of your repository. In the same way, collections inherit metadata from their parent collection.

(Note: you can use and import/export presets of metadata)

## Metadata Types

Metadata types are the objects that represent the types of metadata that can be used. Examples of Metadata Types are "Text", "Long text", "Date", "Relationship with another item", etc (TODO: see full list).

Each metadata type object has its settings and web component that will be used to render the interface. 

Metadata Types can be created via plugins and extend the default set of types shipped with Tainacan.

## Filters

For every collection, you may choose which metadata will be used to filter the results in a faceted search interface. These are the filters.

Filters give the ability to the user to filter items in a collection using a Filter Type.

## Filter Types

Filter types are the different types of interfaces to filter items in a collection based on one specific Metadatum. Examples of Filter Types are "input text", "datepicker", "date range picker", "number range slider", "list of checkboxes", etc.

Each Filter Type object has its settings and web component that will be used to render the interface.

Filter Types can be created via plugins and extend the default set of types shipped with Tainacan. 

## Taxonomies

Taxonomies can be created and used to classify items. Typical Taxonomies are Genre, Country, etc.

In WordPress language, they are Custom Taxonomies, and they can be shared among many collections.

Each Taxonomy has a set of terms. For example, the taxonomy Genre may have terms like "drama" and "comedy".

Terms can have a hierarchy, which means that when you browse for items that have a parent term (for instance, "Rock"), the results will include items that have any of the child terms (for instance, "Progressive Rock" and "Classic Rock").

Terms also have a description, may have an icon or image that represents it and may also be linked to an existing concept of an ontology. They can have their URL in your site, with a page listing all items that are related to them, despite their collection. In that way, they behave as if they were a collection themselves.

## Under discussion

### Item types

Item types give you the ability to specialize in the description of an item based on its nature. So, inside the same collection, you may have items that vary in its nature and, therefore, have a different set of metadata.

For each item type, you can choose a group of Metadata, as you do for a collection. When you create an item inside a collection, it will have all the metadata chosen for that collection plus the metadata related to its type.

An item type can be anything. For example, LPs, Books and paintings are õbvious distinct item types that may have specific metadata. But it could also more abstract concepts, such as "financial transactions".

### Desktop

Desktop holds items that are not part of any collections yet. You might want to use it when you want to upload a bunch of items and organize them afterward, instead of having to think and prepare all the collections beforehand.

Items in Desktop are not publicly visible and have only the metadata configured at the repository level.

### Thematic Collections

Thematic Collections is another way to organize the items in your repository. In essence, each thematic collection is a term inside a taxonomy called "Thematic Collections", that can hold items from any collections, and an item can be part of many Thematic Collections.

It works in the same way as any other taxonomy, the only difference is that you have another way to manage it...

Another idea here is, instead of having a "fixed taxonomy" called thematic collections, we could just have a menu item "Taxonomies" or "Organize by taxonomies" that lets you browse the items by taxonomy, instead of by collections, and manipulate them.
