SortableGridField
=================

Adds drag and drop functionality to SilverStripe 3.0's GridField

## Requirments
* SilverStripe 3.0 RC1

## Installation
* Download the module from here https://github.com/UndefinedOffset/SortableGridField/downloads
* Extract the downloaded archive into your site root so that the destination folder is called SortableGridField, opening the extracted folder should contain _config.php in the root along with other files/folders
* Run dev/build?flush=all to re-gernate the manifest
* Upon entering the cms and using GridFieldSortableRows component for the first time you make need to add ?flush=all to the end of the address to force the templates to regenerate

## Usage
To enable sorting on a has_many relationship set up an interger field on your data object.

To enable drag and drop sorting on the grid field add the following to your grid field's config
*Grid Field Config*

    :::php
    $myGridConfig->addComponent(new GridFieldSortableRows('{Column to store sort}'));

To move an item to another page drag the row over the respective page button and release.

## @TODO
* Optimize re-ordering of a has_many relationship when sorting on a single page
