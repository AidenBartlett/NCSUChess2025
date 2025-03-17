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
It is best to automatically have the entries being updated. This is trickier than you might think. Here is how I've done it in the past:


