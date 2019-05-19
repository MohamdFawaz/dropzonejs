# Dropzonejs Drupal 8

Dropzonejs is a Drupal 8 module that provides drag and drop file uplaods with image previews and the following are the required files for the library:

  - [Download the library](https://github.com/enyo/dropzone) and to be added in  /libraries/dropzone/dist/dropzone.js
  - [Inline Entity Form](https://www.drupal.org/project/inline_entity_form)




### Installation

Install the module after adding the required library files from Extend both Dropzonejs and DropzoneJS entity browser widget


### Examples

The following example in Form API 
```php
$form['image'] = [
      '#title' => $this->t('Documents'),
      '#type' => 'dropzonejs',
      '#required' => TRUE,
      '#dropzone_description' => 'Drag and drop file',
      '#max_filesize' => '1M',
      '#extensions' => 'jpg png pdf',
      '#max_files' => 1,
      '#attributes' => array('class' => array('form-control')),
    ];
```

To use it as entity browser in content types:

first you have to install the following
Entity Browser Module

and go to Configuration->Entity Browsers->Add Entity browser
and choose these options
Display plugin: Modal
Widget selector plugin: Tabs
Selection display plugin: No selection display

Save this configuration
and on the entity page select the Widget Settings tab 
and choose DropzoneJs from the Widgets list and save your selections

now go to content type and select a contnet type and choose Manage form display
and in the file/image field select entity browser in the widget 
and with the cog icon on the right select the entity browser that you created
