# YouTube Adblocker Enhancements 🚫🎥

This repository contains a collection of user scripts designed to enhance the YouTube experience by removing unwanted ads and warnings. These scripts are specifically for users who want to skip preroll ads and bypass the "Adblocker detected" warning that appears on YouTube. 

## Features ✨

- **Remove YouTube Adblock Warnings** 🚫
  - Automatically dismisses the warning banner that tells users to disable ad blockers.
  - Prevents the banner from interfering with video playback.
  
- **No Preroll Ads (Beta)** ⏩
  - Skips YouTube's preroll ads before the video starts.
  - Allows uninterrupted video viewing, bypassing the ads YouTube serves.

## Installation Instructions 🔧

### Prerequisites

To use these user scripts, you need a browser extension that supports user scripts, such as [Tampermonkey](https://www.tampermonkey.net/) or [Greasemonkey](https://www.greasespot.net/).

### Step-by-Step Guide

1. **Install Tampermonkey (or Greasemonkey)** 🧰:
   - Go to the official website: 
     - [Tampermonkey](https://www.tampermonkey.net/) 
     - [Greasemonkey](https://www.greasespot.net/)
   - Install the extension in your browser.
   
2. **Install the Scripts** 📥:
   - Click on the script links below to install the user scripts directly:
     - **[Remove YouTube Adblock Warnings](https://greasyfork.org/en/scripts/477390-remove-youtube-adblock-warnings)** 🛠
     - **[YouTube No Preroll Ads (Beta)](https://greasyfork.org/en/scripts/477464-beta-youtube-no-preroll-ads-bypass-new-restrictions)** ⏩
   
3. **Enable the Scripts** 🔄:
   - After installing the scripts, they will automatically be enabled in Tampermonkey or Greasemonkey. You should see them active when visiting YouTube.
   
4. **Enjoy an Ad-Free YouTube Experience!** 🎉

## Script Breakdown 🔍

### 1. **Remove YouTube Adblock Warnings**

- **What It Does**: 
  - This script **automatically dismisses** the "Adblocker Detected" warning that YouTube displays when it detects that you're using an ad blocker.
  - It automatically clicks the "Dismiss" button for you, allowing you to continue watching videos without interruption.

- **How It Works**:
  - The script constantly checks for the presence of the warning banner on YouTube. 
  - Once the banner is detected, it clicks the dismiss button and automatically resumes playback.

```javascript
(function() {
    'use strict';
    var player = document.getElementById("movie_player");
    var closeit = setInterval(function() {
        if(document.getElementsByClassName("style-scope ytd-popup-container").length > 0 && document.getElementById("dismiss-button") && document.getElementById("divider")) {
            setTimeout(function(){
                document.getElementById("dismiss-button").click();
                document.getElementsByClassName("ytp-play-button ytp-button")[0].click();
                console.log("banner closed");
                clearInterval(closeit);
            }, 4000);
        }
    }, 300);
})();

```
# YouTube No Preroll Ads (Beta)
- What It Does:

   - This bypasses the preroll ads that appear before YouTube videos.
  - It prevents YouTube from showing the ad entirely, allowing you to jump straight into the video.
### How It Works:

- The script automatically detects when a preroll ad is about to play and skips it before it starts.
- As this is still in beta, it might not work perfectly on all videos or for all users.
  ``` javascript
  (function() {
    'use strict';
    // Preroll ad bypass logic here
  })();

# Compatibility 💻
- The scripts are designed to work across all major browsers that support Tampermonkey or Greasemonkey, including:
> Google Chrome
> Mozilla Firefox
> Microsoft Edge
> Safari (with userscript support)
## Notes 📝
- Beta Limitations: The "No Preroll Ads" feature is still in development and may not work with all YouTube videos or may break after YouTube updates its platform.
- Adblock Detection: YouTube might occasionally change its method of detecting adblockers, which could break the functionality of these scripts. Please check for script updates regularly.
- Legal Disclaimer: These scripts bypass ads that YouTube uses to monetize its platform. Use them responsibly and understand that such usage may violate YouTube's Terms of Service.
## Contributing 🤝
> If you have suggestions for improvements, bug fixes, or additional features, feel free to open an issue or submit a pull request! Contributions are welcome.

## License 📄
> This project is licensed under the MIT License - see the LICENSE file for details.

## Support 💬
- If you encounter any issues or need help with the scripts, feel free to open an issue in this repository. We will try our best to assist you!

## Acknowledgments 🙏
- Thanks to GreasyFork for hosting the user scripts.
- Thanks to Tampermonkey and Greasemonkey for enabling the use of custom scripts in browsers.
- Enjoy your improved YouTube experience! 🚀


### Explanation of Sections:

1. **Title and Description**: An overview of what the repository and scripts are meant to do with a touch of style.
2. **Features**: Clearly highlights the primary functions of the scripts with emojis to make it visually appealing.
3. **Installation Instructions**: Walks the user through setting up the scripts step by step, ensuring clarity with helpful emojis.
4. **Script Breakdown**: Explains the logic behind each script, including snippets of the code so users can understand how it works.
5. **Compatibility**: Informs users about browser compatibility.
6. **Notes**: Gives some important disclaimers and information about script limitations.
7. **Contributing**: Encourages open-source collaboration with instructions on how users can contribute.
8. **License**: Mentions the license type to ensure clarity on usage rights.
9. **Support**: Provides a channel for users to ask questions or report issues.








### live at [https://sk16er.github.io/youtube_adblocker_adblocker/](https://sk16er.github.io/youtube_adblocker_adblocker/)
