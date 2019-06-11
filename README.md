# Axelerant

Created a custom module siteinfo for updating site information of Drupal 8 web.

The site has default core modules and contrib module installed.

As per the requirement, created a custom module that does the following tasks:

  A site configuration form with text field named "Site API Key" added to the "Site Information" form with the default value of “No API Key yet”.
* When this form is submitted, the value that the user entered for this field is saved as the system variable named "siteapikey".
* A Drupal message inform the user that the Site API Key has been saved with that value.
* When this form is visited after the "Site API Key" is saved, the field is populated with the correct value.
* The text of the "Save configuration" button is changed to "Update Configuration".
* This module also provides a URL that responds with a JSON representation of a given node with the content type "page" only if the previously submitted API Key and a node id (nid) of an appropriate node are present, otherwise it will respond with "access denied".

created a new menu as /nodevalidate/{key}/{nid} to return json object
* created a controller to match siteapikey and nodeid , 
* if Key doesn't match it will respond access denied 
* if key matches but node id is wrong, it will respond as 'not a node'
* if key and node both matches, it will respond json object of the node.

