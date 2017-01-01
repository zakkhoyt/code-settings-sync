# Settings Sync
### Previously Known as Visual Studio Code Settings Sync

[![Version](https://vsmarketplacebadge.apphb.com/version/Shan.code-settings-sync.svg)](https://marketplace.visualstudio.com/items?itemName=Shan.code-settings-sync)

[![Installs](https://vsmarketplacebadge.apphb.com/installs/Shan.code-settings-sync.svg)](https://marketplace.visualstudio.com/items?itemName=Shan.code-settings-sync)

[![Ratings](https://vsmarketplacebadge.apphb.com/rating/Shan.code-settings-sync.svg)](https://marketplace.visualstudio.com/items?itemName=Shan.code-settings-sync)


**Type Sync in command Palette in order to view all commands.**

**Note :** Latest Update is available for Code Version 1.9+ as currently its in insiders and I want to make sure that it works well to publish in normal release.

## Key Features
```
1. Use your github account token and Gist.
2. Easy to Upload and Download on one click.
3. Upload Key : Shift + Alt + U
4. Download Key : Shift + Alt + D
5. Use Other User's Public Gist to completely sync your settings with them.
6. Show a summary page at the end with details.
7. Auto Download Latest Settings on Startup.
8. Auto upload Settings on file change.
```      

## It Syncs
```
All the extensions and complete User Folder that Contains
    1. Settings File
    2. Keybinding File
    3. Launch File
    4. Snippets Folder
    5. VSCode Extensions Settings
    6. Workspaces
```
   
## Steps To Get the Github Key.

This extension required your GitHub Account Personal Access Token. You can create one simple by looking into the following pictures. Make sure you add **Gist** in scope.

**Goto Settings / Personal Access Tokens / Generate New Token**


![Goto Settings / Personal Access Tokens](http://shanalikhan.github.io/img/github1.PNG)

**Select Gist From Scopes**

![Select Scopes](http://shanalikhan.github.io/img/github2.PNG)

**Get Unique Key**

![Get Unique Key](http://shanalikhan.github.io/img/github3.PNG)


> Save the Key somewhere for future use.


## Upload Your Settings For the first time


**Press Shift + Alt + U it will ask your github account access token.**

> Type ">Sync" In Command Palette into order download / upload

Enter the github account in the window and click enter.

![github account access token](http://shanalikhan.github.io/img/upload1.png)

**Upload your settings automatically and give you Gist ID.**
Copy this Gist ID in order to download the settings in other machines.

![uploaded automatically](http://shanalikhan.github.io/img/upload2.png)


## Download your Settings

**Press Shift + Alt + D it will ask your github account access token.**

> Type ">Sync" In Command Palette into order download / upload

Enter the github account in the window and click enter.

![github account access token](http://shanalikhan.github.io/img/upload1.png)

**Enter Your Gist ID.**
you need to enter your Gist ID in order to get the all files

![Enter Your Gist ID](http://shanalikhan.github.io/img/download2.png)

**Settings Downloaded.**
You are Done! All your files are downloaded

![Enter Your Gist ID](http://shanalikhan.github.io/img/download3.png)

## Reset Token / Gist Settings

> Type ">Sync" In Command Palette and select Reset Token and Gist Settings

## Toggle Auto Download

Auto Download is **disabled by default**. It will sync all the setting by default when the editor starts.
Please make sure you have valid github Token and Gist available to make it work properly.

Select Command **"Sync : Advance Options > Toggle Auto-Download On Startup"** command to Turn ON / OFF the auto download.

## Toggle Force Download

Force Download is **disabled by default**. By default extension wont download the latest settings if you already have latest downloaded version , but sometime when you delete some extension locally and dont upload the settings it will still show you have latest versions by date or time checks, by turning this ON it will always download the cloud settings on startup.

Please make sure you have valid github Token and Gist available to make it work properly.

Select Command **"Sync : Advance Options > Toggle Force Download"** command to Turn ON / OFF the force download.

## Toggle Auto-Upload on change
Auto-upload is **disabled by default**. When the settings are changed and saved this feature will automatic start the upload process and save the settings online.

Please make sure you have valid github Token and Gist available to make it work properly.

Select Command **"Sync : Advance Options > Toggle Auto-Upload on Setting Change"** command to Turn ON / OFF the auto-upload.



## Toggle Summary

Summary is **enabled by default** which shows all the files and extensions that are added or deleted in a single page.
You may turn it off in order to make a upload and download process clean and quiet.  

Select Command **"Sync : Advance Options > Toggle Summary Page On Upload / Download"** command to Turn ON / OFF the auto download.

## Create Public Gist To Share Settings

By default, it creates secret Gist so only you can see it but if you want to share your Gist with other users, you can set it to public.
You can't change the exiting Gist type from secret to public so it will reset the Gist ID so you can create new Gist with all the existing editor settings.

Select Command **"Sync : Advance Options > Share Settings with Public GIST"**

Other users can give your Gist Id to download the Gist, but they cant upload their settings on your Gist.


## Settings

```
    "sync.gist": "",
    "sync.version": 240,
    "sync.lastUpload": "2016-12-27T16:34:19.308Z",
    "sync.firstTime": true,
    "sync.autoDownload": false,
    "sync.autoUpload": true,
    "sync.lastDownload": "2016-12-27T15:58:35.760Z",
    "sync.showSummary": true,
    "sync.forceDownload": true
```



# How To Contribute

If you have any idea, you can open an issue on the Github repository so we can further discuss it or you can send me a pull request.

## Through Code

Download source code and install dependencies

```
git clone https://github.com/shanalikhan/code-settings-sync.git
cd code-settings-sync
npm install
code .
```
Make the respective code changes.

Go to the debugger in VS Code, choose `Launch Extension` and click run. You can test your changes.

Submit a Pull Request.

## Through Donation

If you enjoy this extension. How about donating, Your donation will help me to keep working and supporting this project.

 <form action="https://www.paypal.com/cgi-bin/webscr" method="post" target="_top">
<input type="hidden" name="cmd" value="_s-xclick">
<input type="hidden" name="encrypted" value="-----BEGIN PKCS7-----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-----END PKCS7-----
">
<input type="image" src="https://www.paypalobjects.com/en_US/i/btn/btn_donateCC_LG.gif" border="0" name="submit" alt="PayPal - The safer, easier way to pay online!">
<img alt="" border="0" src="https://www.paypalobjects.com/en_US/i/scr/pixel.gif" width="1" height="1">
</form>
  

    
## [Contributors](https://github.com/shanalikhan/code-settings-sync/graphs/contributors)
# [Release Notes](http://shanalikhan.github.io/2016/05/14/Visual-studio-code-sync-settings-release-notes.html)
    
# License
MIT

[![Version](https://vsmarketplacebadge.apphb.com/version/Shan.code-settings-sync.svg)](https://marketplace.visualstudio.com/items?itemName=Shan.code-settings-sync)

[![Installs](https://vsmarketplacebadge.apphb.com/installs/Shan.code-settings-sync.svg)](https://marketplace.visualstudio.com/items?itemName=Shan.code-settings-sync)

[![Ratings](https://vsmarketplacebadge.apphb.com/rating/Shan.code-settings-sync.svg)](https://marketplace.visualstudio.com/items?itemName=Shan.code-settings-sync)
