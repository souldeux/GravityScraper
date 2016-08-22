GravityForms is a popular WordPress form plugin. Sometimes, people would like to POST the data they receive through their GravityForms to other websites. The easiest way to do this is with a custom WP plugin. This small command-line application generates that plugin for you.

Dependencies:

requests
BeautifulSoup

(pip install x for x in dependencies)


Usage:

Save gravityscraper.py to a location on your computer. In a terminal/shell, navigate to the directory containing the script and run it with python gravityscraper.py. Enter the FQDN of the page containing the forms for which you’d like to create a plugin. Then, enter the FQDN of the page/endpoint where you want to POST your data.

The generated .php file will need some editing. The script tries to detect what names it should use to POST what values, but you’ll want to make sure they’re correct. For instance, maybe it thinks a field should be sent as “First Name” but you want it sent as “first_name” - just use your favorite text editor to edit those values. You may also want to remove some values, like “Confirm Email” fields.

When you are satisfied with the plugin, right click and zip/compress it then upload it to your site via the plugin upload interface.


Known Issues:

This works best with simpler forms, and has not been tested with many edge cases. File uploading, multi-page forms, form with heavy reliance on conditional logic and/or ajax, and forms which make use of the “Other” field on checkboxes and/or radio buttons all need further testing. 