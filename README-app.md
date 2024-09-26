# humio-app

Out of the 1box Humio dashboards and saved searches for Investigator.

# Packaging the application

Run the following command and verify that the file `investigator-humio-app-master.zip` is generated in the humio-app folder.

`cd path_to_humio-app; zip investigator-humio-app-master.zip README.md manifest.yaml alerts/* dashboards/* queries/*`


# Importing the package via Humio's UI

## Step 1: Import the package from Humio's package manager interface

Go to the settings view, navigate to the installed packages menu and click on `Import Package`.

<img src="tutorial_figures/humio_package_import_screenshot.jpg" width=50% height=50%>

Upon successful upload of the file Humio will display the assets included in the package:

<img src="tutorial_figures/investigator_package_imported.jpg" width=50% height=50%>

## Step 2: verify that the assests were imported successfully 

Verify that the assets are listed in the description of the installed package.

<img src="tutorial_figures/investigator_package_overview.jpg" width=50% height=50%>

The dashboards, alerts, queries, and other assets should now be accessible via the top level navigation bar. 
For example the new dashboards should be accessible in the Dashboards tab as show below:

<img src="tutorial_figures/investigator_dashboard_view.jpg" width=50% height=50%>

#Importing the package via uploader.py
Refer utils/README.md


