<h1 align="center">
    <img width="120" height="120" src="https://i.imgur.com/qidPCBf.png" alt=""><br>
    Honkai: Star Rail Check-In Helper
</h1>

<p align="center">
   <img src="https://img.shields.io/github/license/torikushiii/starrail-auto">
   <img src="https://img.shields.io/github/stars/torikushiii/starrail-auto">
</p>

# Daily Check-In

[Daily Check-In](https://act.hoyolab.com/bbs/event/signin/hkrpg/index.html?act_id=e202303301540311)

# Services
If you don't want to use Node.js, you can use one of the following services:
- [Google Apps Script](https://github.com/torikushiii/starrail-auto/tree/master/services/google-script)

# Pre-requisites
- [Node.js](https://nodejs.org/en/)

# Installation
1. Clone the repository.
2. Run `npm install` to install the dependencies.
3. Create a `config.js` or rename `example.config.js` to `config.js`.
4. Follow the instructions in the `config.js` file.

# Usage
1. Go to the Daily Check-In page [here](https://act.hoyolab.com/bbs/event/signin/hkrpg/index.html?act_id=e202303301540311).
2. Log in with your miHoYo account.
3. Open the browser console (F12).
4. Click on the "Console" tab.
5. Type in `document.cookie` in the console and press Enter.
6. Copy the output from the console.
   ![](https://i.imgur.com/hFCL4yN.png)
7. Paste the output into `COOKIE` property in the `config.js` file.
8. Fill in the `DISCORD_WEBHOOK` field if you want to receive a Discord notification when the check-in is successful.
9. Run `index.js` with `node index.js` if you want to run it indefinitely everytime the daily reset occurs.
10. Run `index.js` with `node index.js --sign` if you want to run it once.

# Discord Webhooks
This is an **OPTIONAL** feature. If you want to receive a Discord notification when the check-in is successful, you can create a Discord webhook and add it to the `.env` file.

1. Edit channel settings. (Create your own server if you don't have one.)
   ![](https://i.imgur.com/FWfK3My.png)
2. Go to the "Integrations" tab and click on "Create Webhook".
   ![](https://i.imgur.com/DnELZJl.png)
3. Create a name for your webhook and click on "Copy Webhook URL".
   ![](https://i.imgur.com/AkfTTBB.png)
4. Paste the URL into the `DISCORD_WEBHOOK` field at the `.env` file.
5. Click on "Save Changes".
   ![](https://i.imgur.com/KFYeonU.png)
6. You should receive a Discord notification when the check-in is successful.
   ![](https://i.imgur.com/MOkfwrK.png)
7. And if you enable stamina check, you should receive a Discord notification when your stamina is above your set threshold.
   ![](https://i.imgur.com/XlSdYxC.png)

# Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change. If there's any bugs, please open an issue.
