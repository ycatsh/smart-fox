![graphic](https://github.com/ycatsh/firefox-themes/assets/91330011/86523a74-7788-4164-8439-0fe0a207d526)
<br>

![stars](https://img.shields.io/github/stars/ycatsh/firefox-themes?logo=github)
![issues](https://img.shields.io/github/issues-closed/ycatsh/firefox-themes?logo=github)

This is a collection of custom Firefox themes that I designed. These themes are perfect for those who prefer comfortable, minimalistic, elegant, and simple designs. To download and use them please read the following instructions.

## Intructions 
These instructions provide a step-by-step guide for downloading and applying themes to customize your Firefox. The process is divided into two parts: styling the Firefox elements and modifying the new tab and homepage with the custom theme.

### userChrome.css

1. Download the Firefox Color add-on from [here](https://addons.mozilla.org/en-US/firefox/addon/firefox-color/)  

2. After you set up the add-on, click on [this link](https://color.firefox.com/?theme=XQAAAAKEAwAAAAAAAABBKYhm849SCicxcUUSqiuG_ebZUZXOFqqYn_O4akhBDGiaWd0FjBOq31N1Flo2QaWxtQ6soXvQmPL_Upd3YVaTP-QTAEKfKo8_hUfLueZP0k-rmfVo_jfFNFb9HyVOXU-NXjQTv-zSu7Kg9-Tq4byjMV_kXKgDR38tZi2Sj_zhU8Yx8VVEDTHPt_Hrq_c76cKBmBJ7cdswAG8dWDtuxHy-h8_3x4rFOA9xicLWh1BQYBcy6btytJVQesYC7-wijAstUFJCME_7oZf8zWtJwxFNeZWnIlN0udLKf9nEhZ8dGv2LxOyfB9o6IxUESTxlqTIxJd6KXPKluMOGt7dQEEFyS5cdLcpkX0tJ0783fdze03GDAFjNR4SgEdnTOyL2G7UFsfP7SQmn35SPgaMXALaNe85AqRcMUx1yZ2OW8sLmiCDaoXA9kWgKSBae2ugq6SbaAT2Zft0--OQgTJtn8Y9Vonp3a7JRa-8kQBDrF880_ff6Cg) to add the appropriate colors to your tabs, etc.  

3. On the firefox search bar, enter `about:config` and set `toolkit.legacyUserProfileCustomizations.stylesheets` to `true` to enable CSS customization. 

4. In your [profile directory](about:profiles) make 2 folders `startpage` and `chrome`, inside `chrome/`, paste `userChrome.css`, `userContent.css`, and `tabs/` from the `chrome` directory in this repo.

### New tab as custom page

1. Choose a theme and paste the content from its corresponding folder from the repository to the `startpage` folder you just created 

2. Navigate to your firefox directory, under `default/prefs` create a `autoconfig.js` file
    ```javascript
    //
    pref("general.config.filename", "autoconfig.cfg");
    pref("general.config.obscure_value", 0);
    pref("general.config.sandbox_enabled", false); 
    ```
    paste this code in the file and save

3. Navigate one directory back to `defaults/` and create a `autoconfig.cfg` file
    ```javascript
    //  
    var {classes:Cc,interfaces:Ci,utils:Cu} = Components;  
    
    try {  
    Cu.import("resource:///modules/AboutNewTab.jsm");  
    var newTabURL = "file:///PATH_TO_YOUR_START_PAGE.html";  
    AboutNewTab.newTabURL = newTabURL;  
    } catch(e){Cu.reportError(e);} // report errors in the Browser Console  
    ```
    make sure to put the path of the index.html file in your `startpage` folder

4. Change homepage under firefox settings to 'Custom URLs' and paste in the path. 

5. Restart Firefox. 


## Themes 

### Gratuitous
![image](https://user-images.githubusercontent.com/91330011/210130702-6fb82055-fb88-4268-b335-0d04f3fe6817.png)

### Idyllic
![image1](https://user-images.githubusercontent.com/91330011/162780403-f4b27beb-ea1c-4709-a179-bc70b1588140.png)
Check out [cascade](https://github.com/andreasgrafen/cascade) (for the one line look)

### Busy Cat
![image2](https://user-images.githubusercontent.com/91330011/203773014-c2db8c2d-7010-419a-8dae-46dcd79bc996.png)

### F40
![image3](https://user-images.githubusercontent.com/91330011/204031110-fb0b9c54-cded-44b9-a545-66fb73c9c431.png)
