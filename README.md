![Appdrop Logo](/images/logo.png)
# Appdrop Publishing Guide

## Section 1 – Environment Setup

Welcome to Section 1 of Appdrop's Publishing Guide. Here marks the first step to publishing your apps to the App Store, Play Store or both.

In this section of our Publishing Guide, you will create your developer accounts with Apple and Google and prepare your laptop or desktop for publishing apps using React Native. We've divided Section 1 into the following parts:

1. [Initial Steps for the App Store](#initial-steps-for-the-app-store)
2. [Initial Steps for the Play Store](#initial-steps-for-the-play-store)
3. [Appdrop Environment Setup](#appdrop-environment-setup)
4. [Next Steps](#next-steps)

In [Section 2 of our Publishing Guide](https://github.com/appdrop-team/publishing-guide-app-setup), you'll complete the process of testing your app on a device and publishing it.

<hr>

## Initial Steps for the App Store

Here are easy steps to get started developing for iOS. All you need is a laptop or desktop computer to get started. Before your launch, we highly recommend testing your app on a physical iOS device such as an iPhone or iPad.

### 1. Create an Apple ID and an Apple Developer Account.

In order to publish apps to the App Store, you must create an Apple Developer account for yourself or your business. Developer accounts require you to log in using a traditional Apple ID, such as ones you may be familiar with from iCloud. Visit [Apple's Developer Website](https://developer.apple.com) to complete all the required steps.

> <br>**_Note for Business Accounts:_** <br>
If you plan to publish your app under a business account, Apple requires a tax ID number, such as an EIN, and additional verification from Dun & Bradstreet. Incorporation and verification can take a week or longer, so make sure to budget the necessary time into your project timeline.
<br>

### 2. Visit your [Apple Devloper Team Dashboard](https://developer.apple.com/account) to create an Apple Distribution Signing Certificate for your account.

After creating your Developer Account, you will need register a **Apple Distribution** Signing Certificate which ensures that only you and members of your team can publish apps to your account. Later, you will attach that certificate to the machine where you plan to use Xcode.

![iOS Certificate Selection](/images/01.png)

![iOS Certificate Plus](/images/02.png)

![iOS Certificate Distribution](/images/02@.png)


Once you complete everything, you should see the Distribution Signing Certificate appear in your list of certificates.

### 2. From the same Developer Dashboard, create a Bundle Identifier for your app.

All apps on the app store have a unique bundle id to help iPhones, iPads, and so on differentiate between each installed app. 

In order to create a bundle id, visit Certificates, IDs, & Profiles Section of your Dashboard.

Navigate the the Identifiers section and select the plus (+). 

![iOS Bundle ID Addition](/images/02a.png)

When prompted, select App ID from the list of identifier types. Next, select that you are creating an App, not an App-Clip.

Lastly, input an id and optional description for your app. It is recommended to reverse your domain name when you set this id. For instance, the bundle id for Appdrop's companion app is `com.appdrop`.

### 3. Visit your [App Store Connect Dashboard](https://appstoreconnect.apple.com) and create your app.

Next, you will create your iOS app from App Store Connect. During this process you will receive an App ID.

Navigate to your [My Apps](https://appstoreconnect.apple.com/apps) page within App Store Connect.

![Select My Apps](/images/02b.png)

Once you've entered your App Dashboard, select the plus (+). 

![Create an App](/images/02c.png)

Enter the name of your app as it will appear on the App Store and select the bundle identifier you just created.

![Describe App](/images/02d.png)

### Congrats! 🚀 

After this step, you are ready to start testing and publishing your app using Xcode.

![Prepared App](/images/02e.png)

### Next Steps

That's it! You're ready to start iOS development. 

If you're supporting Android as well, head over to our [Play Store guide](#initial-steps-for-the-play-store). 

Afterwards, head over to our [Appdrop setup guide](#appdrop-environment-setup) to start testing your app.

<br>
<hr>
<br>

## Initial Steps for the Play Store

Here are easy steps to get started developing for Android. All you need is a laptop or desktop computer to get started. Before your launch, we highly recommend testing your app on a physical Android device such as an Samsung, Google Pixel or Android Tablet whenever possible.

### 1. Create a Google Play Store Developer Account.

In order to publish apps to the Play Store, you must create a Google Play Store Developer account for yourself or your business. Visit [Google's Play Store Developer Website](https://developer.android.com/distribute) to complete all the required steps.

> <br>**_Note for Business Accounts:_** <br>
If you plan to publish your app under a business account, Google requires a tax ID number such as an EIN and a valid business address. Incorporation can take a week or longer after your company incorporation steps are complete, so make sure to budget the necessary time into your project timeline.
<br>

### 2. Visit your [Play Store Console](https://play.google.com/apps/publish) and create your app.

In order to publish your app, you will create your app from the Play Store Console and provide all of the appropriate metadata. Unlike the App Store publishing process, you will define your app's package name within Android studio and upload this within your code base. Afterwards, you should see your app appear in your *Pinned Apps* list within the Play Store Console.

![Pinned App](/images/03.png)

### Congrats! 🚀 

After this step, you are ready to start testing and publishing your app using Android Studio. You will learn how to install and configure Android Studio in the next step.

### Next Steps

That's it! You're ready to start Android development. 

If you're supporting iOS as well, head over to our [App Store guide](#initial-steps-for-the-app-store). 

Afterwards, head over to our [Appdrop setup guide](#appdrop-environment-setup) to start testing your app.

<br>
<hr>
<br>

## Appdrop Environment Setup

Your end-product will be a vanilla [React Native](https://reactnative.dev) app built with Typescript. That's just a fancy way of saying you'll be using one of the most robust, well-tested mobile app frameworks on the planet. React Native was originally created by Facebook to power the largest, most mission-critical apps that exist including Appdrop's portfolio apps.

React Native development with Typescript requires the use of a command-line interface such as Terminal for Mac or Git Bash for PC. At points, this will feel like coding, but trust us that we've made this guide incredibly streamlined and you will primarily be pasting our commands or dropping our files into the correct places in your computer. If you ever feel overwhelmed or frustrated, then we recommend our getting help from our Appdrop Experts for a [Fast Track App Submission](https://appdrop.com/pricing).

Let's get started!

### 1. Create a dedicated `@appdrop` folder on your computer.

You will need a dedicated space on your computer to house your app's files. Start by creating a folder called `@appdrop` inside your downloads folder so that you can house everything inside one place.

![Appdrop folder](/images/04.png)

### 2. Launch Your Command Line at this Folder.

Next, Ctrl- Click this folder and select `New Terminal at Folder`.

![Launch Terminal](/images/05.png)

Once your Command Line is up, paste in the command:

`pwd` 

Press Enter on your keyboard to run this command (short for "present working directory").

![Verify Terminal](/images/06.png)

Your command line should print something like `/Users/yourname/Downloads/@appdrop` to verify that you are working inside of your `@appdrop` folder. You should also be able to see this at the top of your Command Line Interface on most computers.

Leave this window open because you will run the command line prompts from the next step inside this same location.

> <br>**_Tip:_**
You can organize your Downloads folder alphabetically which will place @appdrop at or near the top.
<br>

### 3. Prepare Your Computer to run React Native Apps

Your next big milestone will be successfully creating a React Native test project on your device to ensure that your environment setup is correctly. At the end, you should see screens on your iOS and Android devices that look like these photos.

![Successful milestone](/images/07.png)

Head over to the [React Native Environment Setup guide linked here](https://reactnative.dev/docs/environment-setup) and __carefully__ follow the instructions for the `React Native CLI Quickstart` option with the `yarn` package manager.

![RN Environment Setup](/images/08.png)

> <br>**_Important:_**
Be absolutely certain that React Native 0.63 is selected in the top left corner of the website so that you follow the correct setup steps.
<br>

Select your development OS `Mac`, `Windows`, or `Linux` and go through the setup steps for each type of app you plan to support.

When you reach the *Creating a New Application* step, you will be specifying React Native version 0.63.0 and using the Typescript template. This is the specific command:

```
npx react-native init AwesomeTSProject --version 0.63.0 --template react-native-template-typescript
```

If everything was done correctly up to this point, you will see a new folder inside of @appdrop called AwesomeTSProject. You will run your app using the code inside the `iOS` and `android` folders. If you don't have both an iOS and Android device, that is OK! Simulators will help you test your app on the device(s) that you are missing.

![RN Create](/images/09.png)

<br>
<br>
<hr>
<br>

## Additional Steps to Run the Test App on iOS

### 4. Launch Xcode

> <br>**_Important:_** 
Make sure to select the .xcworkspace file, not the .xcodeproj file when you launch Xcode.
<br>

![Select .xcworkspace](/images/10.png)

> <br>**_Note for Windows Computers:_** <br>
In order to install Xcode and publish iOS apps from your PC, you may need to install virtual MacOS software, such as [VirtualBox](https://www.virtualbox.org/) which is free from Oracle.
<br>

### 5. Configure Xcode with your Developer Credentials

From Xcode, you will need to sign in to your Apple Developer Account and attach the Distribution Signing Certificate you created during the [Initial Steps for App Store](#initial-steps-for-the-app-store).

Select your project on the left side of Xcode and navigate to the Signing & Capabilities tab.

![Navigate to Signing & Capabilities](/images/11.png)

Enter the Apple ID credentials attached to your Apple Developer Account.

![Sign in to Apple](/images/12.png)

Next, you will select the appropriate Team from this list. In some cases, you may have multiple Apple Developer Accounts on your device separated for personal and business use or separated for 1st party work and external client work.

![Select Team](/images/13.png)

Double-click your Distribution Signing Certificate to select it.

![Select your Distribution Signing Certificate](/images/14.png)

Xcode will now provide you with a dropdown list where you can select your Team from the Signing & Capabilities tab. Choose your Team name and your Distribution Signing Certificate will automatically be attached to this app.

![Select Team](/images/15.png)


<br>
<hr>
<br>

## Next Steps

With that, you're one step closer to launching your app! Feeling excited yet? We hope so!

Next, head on over [Section 2 of our Publishing Guide](https://github.com/appdrop-team/publishing-guide-app-setup) which walks you through the process of testing your app on a device and publishing it.
