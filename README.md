My Life in Weeks: Complete Setup Guide

This guide will show you how to host your "Life in Weeks" application publicly so you can view it from anywhere, while keeping all of your actual life events 100% private and secure on your GitHub account.

Step 1: Set up the Public App (The Visual Grid)

Go to your GitHub account and create a new Public repository (e.g., name it life-in-weeks).

Upload the liw.html file (provided in this chat) directly into this repository. (You can rename it to index.html if you want it to be the main page).

Go to Settings > Pages inside the repository.

Under "Build and deployment", set the source to Deploy from a branch, select the main branch, and click Save.

In a few minutes, your app will be live at your-username.github.io/life-in-weeks/.

Right now, anyone can visit this link. But it will just say "Not Connected" and load an empty placeholder grid. Your life events are safe!

Step 2: Set up the Private Database (The Vault)

Now, we need a secret place for the website to save your events.

Go to your GitHub account and click New Repository.

Name it something like: liw-data

CRITICAL: Select Private. (If you don't do this, people can read your milestones).

Check the box that says "Add a README file". (This initializes the repository so the app can start saving to it).

Click Create repository.

Step 3: Get Your Secret Key (Personal Access Token)

The website needs your permission to push data into your Private repository.

In GitHub, click your profile picture in the top right -> Settings.

Scroll down the left sidebar to the very bottom and click Developer settings.

Click Personal access tokens -> Tokens (classic).

Click Generate new token -> Generate new token (classic).

In the "Note" field, type "Life In Weeks App".

Change the "Expiration" to No expiration.

Under "Select scopes", check the box for repo (This gives it control of private repositories).

Scroll to the bottom and click Generate token.

COPY THIS TOKEN NOW. It starts with ghp_. You will never be able to see it again after leaving the page.

Step 4: Connect the Website to the Vault

Go to your public website on your browser.

At the bottom right of the screen, click "Not Connected" (the sync status button).

Enter your Date of Birth (This is required to calculate your weeks correctly).

Under Private Data Repository, type your repo name exactly like this:
your-username/liw-data

Under Personal Access Token, paste the ghp_... token you just copied.

Click Connect & Load.

🎉 You are done!

Whenever you want to add a memory or event to a specific week, just click on that box in the grid. Type your event in English or Bangla, click "Commit Event," and it will automatically generate a liw_data.json file in your private repository!
