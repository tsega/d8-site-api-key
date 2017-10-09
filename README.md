## Background Information

When logged in as the administrator, the **"Site Information"** form can be found at the path `/admin/config/system/site-information`.

## Requirements

This module needs to alter the existing Drupal "Site Information" form. Specifics:

  - [x] A new form text field named "Site API Key" needs to be added to the "Site Information" form with the default value of “No API Key yet”.
  - [x] When this form is submitted, the value that the user entered for this field should be saved as the system variable named "siteapikey".
  - [x] A Drupal message should inform the user that the Site API Key has been saved with that value.
  - [x] When this form is visited after the "Site API Key" is saved, the field should be populated with the correct value.
  - [x] The text of the "Save configuration" button should change to "Update Configuration".
  - [x] This module also provides a URL that responds with a JSON representation of a given node with the content type "page" only if the previously submitted API Key and a node id (nid) of an appropriate node are present, otherwise it will respond with **"access denied"**.

## Example URL

```http://localhost/page_json/FOOBAR12345/17```

## Resources

  - [Creating custom modules](https://www.drupal.org/docs/8/creating-custom-modules)
  - [A practical guide to building basic Drupal 8 modules](https://www.drupal.org/docs/8/creating-custom-modules/a-practical-guide-to-building-basic-drupal-8-modules)
  - [Drupal coding standards](https://www.drupal.org/node/318)
  - [Acquia Drupal 8 Module Development](https://community.acquiacademy.com)
  - [Drupal Exchange - How can I add a textbox in Site Information configuration](https://drupal.stackexchange.com/questions/156703/how-can-i-add-a-textbox-in-site-information-configuration)
  - [Drupal 8 node serialization to JSON](https://drupal.stackexchange.com/questions/191419/drupal-8-node-serialization-to-json)
  - [Using parameters in routes](https://www.drupal.org/docs/8/api/routing-system/using-parameters-in-routes)
  
## Time Taken
The approximate time taken to implement this module was **5 hours**. *Note: It was my first time to build a Drupal 8 module.*