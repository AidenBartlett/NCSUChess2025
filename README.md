This is how I did the website, automatic registrations, etc. for NCSU chess tournaments. I will try to make step by step.

Setting up the website:
1. Create Github repo.
2. Go to Settings -> Pages -> Source and change to Github Actions. (https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)
  After this, find the "Static HTML" by Github Actions. Click Configure -> Commit changes. This should add a file called static.yml in a folder called .github/workflows. Click Commit changes -> Commit changes.
3. Go back to the main tab (Code). Click Add file -> Create new file.
4. Add a file called index.html. This is where you should add your .html file. This is the main part of the webpage. Here is a past .html file I have used: https://github.com/AidenBartlett/SeptemberStalemate/blob/main/index.html
  Helpful hint 1: If you're unfamiliar with html, paste in an html file into ChatGPT and ask what you would like it to change, add, edit or delete.
  Helpful hint 2: If you have a long URL, it's a bit ugly. I would recommend using tinyurl.com to get a better URL to use.
6. When done with the .html file, click Commit changes -> Commit changes.
7. Since we added the earlier static.yml file, once we commit our changes, we have to wait a second and the updates will be added to our website!
  Helpful hint: If you want to make sure the changes are finished, you can view the "Actions" tab.
8. In order to see the URL of your website, go to Settings -> Pages. On this page, you should see text that says "Your site is live at ...". Copy and paste this URL into another tab.
9. If you would like to make changes to the website, edit the index.html file, click commit changes -> commit changes. Wait a minute or two, and then revisit the website.


Adding images: If you want to add an image, you will have to first have to add the image to your Github repo. Do this by going to the Code tab, click Add file -> Upload files, and then upload the files.
Note: After doing this, you can link the image into the .html. To see how to do this, either ask ChatGPT or refer to past html files.

Automatic entries:
It is best to automatically have the entries being updated (people want to see ratings of players and manually updating is a PAIN). This is trickier than you might think. I have used an automatic script in order to hide people's information like email, Venmo, photo consent, etc. Here is how I've done automatic entry list update in the past:
1. Open the Google form that people use to enter the tournament. Click Responses and then click "Link to Sheets" -> Create a new Spreadsheet -> Create. Open this Spreadsheet in another tab.
2. Find the spreadsheet that was just created. Keep this open in a separate tab. We will need this for later.
3. Now, we need to create another spreadsheet. This will be the entries everyone will see. Go to Google Spreadsheets -> Blank Spreadsheet and name this the name of the tournament (for organization).
4. Now, it is very important to not forget this next step. At the bottom where it says "Sheet1" rename this to "Exported Data". (This is the name used in the script).
5. Now comes the fun part! Open the Google sheets form that people fill out to sign up for the tournament. Then, click on the three dots in the top right corner and select "Apps Script". It is important to create the Script this way so we can "bind" the registration form to our script.
6. In another tab, go to the NCSU drive and go to Apps Script. You should see a file called "ExportInformation". Alternatively, visit the URL https://script.google.com/u/2/home/projects/1FGApJdENb_cbUGCqgAOBhoU_U5ROm54Ld3bX58ma0PXzC_npeefEmp0V/edit (requires access to the NCSU Drive). Open it and copy the text.
9. Close the registration form tab. You should now have three tabs open: the spreadsheet that was auto-generated (source spreadsheet), the spreadsheet you manually created (destination spreadsheet), and the Apps Script.
10. You will now have to make slight modifications to the Apps Script file. You will have to paste in the ids of both the source and destination spreadsheet.
11. Open the source spreadsheet, click the URL and extract the ID. This is the part that comes in between "/d" and "/edit". For reference on how to do this, see https://stackoverflow.com/questions/36061433/how-do-i-locate-a-google-spreadsheet-id.
12. Copy and paste the ID of the source spreadsheet on line 3 where it says sourceSpreadsheetId.
13. Similarly, extract the ID of the destination spreadsheet and paste it on line 4 where it says destinationSpreadsheetId.
14. When done, use Ctrl + S to save (make sure there are no unsaved changes in the top left corner). You're done!
15. Try to "Run" this script. See if anything is wrong. In the past, I have had to "Allow permissions" in order for the script to work. After this, you shouldn't have to run the script.
16. Cool. Let's add a trigger so every time someone submits the form, it's automatically updated. Do this by going to the far left side of the Apps Script and finding the "Triggers" tab.
17. Add a trigger. Change "Select Event Source" to "From form". Change "Select Event Type" to "On Form Submit".
18. You're done now! Have someone enter their data into the spreadsheet and see if the destination spreadsheet is updated. The destination spreadsheet should then be updated with their name and rating.


If you have any questions or problems with any of the above, please reach out to aiden@thebartlettkids.com. I was the one who created this, and hopefully I remember how to do all this :)
