# FlowDeck

> **Note: This project is currently under active development.**

### Table of Contents

- [Project Details](#project-details)
- [Quickstart](#quickstart)

---

## Project Details

### Objective

FlowDeck is a method for using a Stream Deck profile to enhance the Webflow build experience. The primary objective is to create a comprehensive profile to automate some of the more complex tasks required when building with Webflow frameworks like Client-First. This will allow you to streamline your workflow and stay organized throughout your build, while providing intuitive control over various build actions and object creation.

### Project Status

FlowDeck is still a work in progress. We are actively developing and refining the Stream Deck profile to ensure it meets the needs of Webflow developers.

### Features (planned)

- Intuitive control of Webflow build actions
- Real-time visual feedback for seamless workflows
- Enhanced productivity and speed for Webflow development
- Profiles for Stream Deck, Stream Deck XL, and Stream Deck Mini (iOS Free Tier)
- Profiles tailored to Client-First Framework (other frameworks to follow)

### Disclaimer

Please note that while we strive to provide a stable and reliable solution, FlowDeck is currently a work in progress. Use it at your own risk, and we appreciate your understanding and patience during the development process.

We are in no way affiliated with Webflow or {Finsweet.

---

## Quickstart

### Requirements

Some of the more advanced automations regarding specific frameworks require some Applescript to work, these profiles will be marked as MacOS only. Don't forget the Webflow step below, it's very important to how the automations work.

- Tested on MacOS 10.11 or later
- Stream Deck App/Software
- Stream Deck Plugin for Applescript: [OSA Script](https://apps.elgato.com/plugins/com.gabrielperales.osascript)
- Google Chrome (can be used with other Chromium based browsers with [minor changes to select actions](#browser-migration))
- Allow JavaScript from Apple Events in the developer tab of your browser
- **In Webflow** bring up the **Quick Find** bar with cmd or ctrl + k or e, and click on the settings icon on the right end of the bar, make sure all actions are enabled **except** for 'Add asset'
- *Some client first related actions will require the [Finsweet Extension](https://chrome.google.com/webstore/detail/finsweet-extension-for-we/mjfibgdpclkaemogkfadpbdfoinnejep)*


### Installation

After choosing the profiles you'd like to use on your Stream Deck and downloading them, follow these instructions to import them:

1. Open the **Stream Deck** software and open the **Settings**
2. In the **Settings** click on the **Profiles** tab
3. Click on the down arrow at the bottom right of the **Profiles** window and click **Import...**
4. Navigate to your downloaded profiles and click to add them.
5. The imported profiles will be add to your profile list for that device.


### Post-Install

The profiles are setup with a variety of tools ready to be used, but to take full advantage of the idea behind this concept, explore the actions and modify them or the layout to best suit your workflow!

---

## Browser Migration

For some actions involving Applescript, a browser is specified. To use other browsers instead, you'll have to modify the Applescript in those actions to point at your new browser. 

To make the changes, click into the stream deck action (if it is a multi action, double click and look through the list for any "Custom: Run OSA script" actions where the first line says 'tell application "Google Chrome"'). Change the browser listed to the browser of your choice (Arc, Brave, etc.).

`tell application "Arc" activate`

The following actions have/are an Applescript (Run OSA script) action which requires updating:

- Add Attribute
- Add Heading H(1-6)
- H(1-6) w/ Folder
