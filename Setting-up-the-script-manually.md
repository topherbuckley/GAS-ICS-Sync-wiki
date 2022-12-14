Recently, we have had a few reports of users seeing the following message:

![](https://i.imgur.com/seoYVDs.png)

Here are some manual instructions to get the code running from GitHub:

## Note that Google has updated the Google Apps Script IDE! Here are the instructions for the new editor (Legacy editor instructions below):

1. Go to Google Drive
2. Click "New" > "More" > "Connect more apps"

![](https://i.imgur.com/SfsJFta.png)

3. Find and install "Google Apps Script"
4. Go back to Google Drive and click "New" > "More" > "Google Apps Script"
5. Now make sure you have the GitHub repo open in a separate window/tab
6. You will need the following files:
  - `Code.gs`
  - `Helpers.gs`
  - `ical.js.gs`
  - `tzid.gs`
  - `appsscript.json` (the manifest file - see special step #8)
7. For each of those files (except `appsscript.json`) you'll want to do the following:
    1. Click the "+" button in the Files section. The select "Script"

    ![](https://i.imgur.com/YlSF7NK.png)
8. For `appsscript.json` you should click the "Project Settings" option in the sidebar, then check the box for `Show "appsscript.json" manifest file in editor` and copy the contents from GitHub to there

   ![](https://i.imgur.com/tydATjG.png)
9. You should be all set up! Open back up the `Code.gs` file and Click "Run" > "Run Function" > "Install"

   ![](https://i.imgur.com/7QktuS0.png)

## Legacy Editor Instructions:

1. Go to Google Drive
2. Click "New" > "More" > "Connect more apps"

![](https://i.imgur.com/SfsJFta.png)

3. Find and install "Google Apps Script"
4. Go back to Google Drive and click "New" > "More" > "Google Apps Script"
5. Now make sure you have the GitHub repo open in a separate window/tab
6. You will need the following files:
  - `Code.gs`
  - `Helpers.gs`
  - `ical.js.gs`
  - `tzid.gs`
  - `appsscript.json` (the manifest file - see special step #8)
7. For each of those files (except `appsscript.json`) you'll want to do the following:
    1. "File" > "New" > "Script file"

    ![](https://i.imgur.com/Bz5G1rb.png)

    2. Name the script file
    3. Copy the contents from GitHub to the file *(Protip: if you select ["Raw"](https://i.imgur.com/J8wgaP4.png) on GitHub it makes the file easier to copy)*
    4. Save the file
8. For `appsscript.json` you should click "View" > "Show manifest file" and copy the contents from GitHub to there

   ![](https://i.imgur.com/vIKPLJ9.png)

9. Add the needed services by clicking "Resources" > "Advanced Google Services" (turn on the "on/off" switches for "Calendar API" and "Tasks API")

   ![](https://i.imgur.com/XAPEpL4.png)
   ![](https://i.imgur.com/toa8yLw.png)

10. You should be all set up! Open back up the `Code.gs` file and Click "Run" > "Run Function" > "Install"

   ![](https://i.imgur.com/ftWhYJ0.png)
