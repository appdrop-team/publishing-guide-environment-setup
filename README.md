# Publishing Guide {#get-started}

## App Store Initial Steps {#app-store}

Here are easy steps to get started developing for iOS. All you need is a laptop or desktop computer to get started. Before your launch, we highly recommend testing your app on a physical iOS device such as an iPhone or iPad.

### 1. Create an Apple ID and an Apple Developer Account.

In order to publish apps to the App Store, you must create an Apple Developer account for yourself or your business. Developer accounts require you to log in using a traditional Apple ID, such as ones you may be familiar with from iCloud. Visit [Apple's Developer Website](https://developer.apple.com) to complete all the required steps.

Note – If publishing your app under a business account, Apple requires a tax ID number, such as an EIN, and additional verification from Dun & Bradstreet. This process can take a week or longer after your incorporation steps are complete, so make sure to budget the necessary time into your project timeline.

### 2. Visit your [Apple Devloper Team Dashboard](https://developer.apple.com/account) to create an Apple Distribution Signing Certificate for your account.

After creating your Developer Account, you will need register a **Apple Distribution** Signing Certificate which ensures that only you and members of your team can publish apps to your account. Later, you will attach that certificate to the machine where you plan to use Xcode.

Once you complete everything, you should see the Distribution Signing Certificate appear in your list of certificates.

### 2. From the same Developer Dashboard, create a Bundle Identifier for your app.

All apps on the app store have a unique bundle id to help iPhones, iPads, and so on differentiate between each installed app. 

In order to create a bundle id, visit Certificates, IDs, & Profiles Section of your Dashboard.

Navigate the the Identifiers section and select the plus (+). 

When prompted, select App ID from the list of identifier types. Next, select that you are creating an App, not an App-Clip.

Create an id and optional description. It is recommended to reverse your domain name when you set this id. For instance, the bundle id for Appdrop's companion app is `com.appdrop`.

### 3. Visit your [App Store Connect Dashboard](https://appstoreconnect.apple.com) and create your app.

In order to publish your app, you will need to provide a name for your app and select the bundle identifier you just created for your app. Afterwards, you will receive an App ID and be able to manage this app from your *My Apps* page within App Store Connect.

After this step, you are ready to start testing and publishing your app using Xcode.

### Next Steps

That's it! You're ready to start iOS development. 

If you're supporting Android as well, head over to our [Play Store guide](#play-store). 

Afterwards, head over to our [Appdrop setup guide](#appdrop-setup) to start testing your app.

## Google Play Store Initial Steps {#play-store}

Here are easy steps to get started developing for Android. All you need is a laptop or desktop computer to get started. Before your launch, we highly recommend testing your app on a physical Android device such as an Samsung, Google Pixel or Android Tablet.

### 1. Create a Google Play Store Developer Account.

In order to publish apps to the Play Store, you must create a Google Play Store Developer account for yourself or your business. Visit [Google's Play Store Developer Website](https://developer.android.com/distribute) to complete all the required steps.

Note – If publishing your app under a business account, Google requires a tax ID number such as an EIN. This process can take a week or longer to complete, so make sure to budget the necessary time into your project timeline.

### 2. Visit your [Play Store Console](https://play.google.com/apps/publish) and create your app.

In order to publish your app, you will create your app from the Play Store Console and provide all of the appropriate metadata. Unlike the App Store publishing process, you will define your app's package name within Android studio and upload this within your code base. Afterwards, you should see your app appear in your *Pinned Apps* list within the Play Store Console.

After this step, you are ready to start testing and publishing your app using Android Studio. You will learn how to install and configure Android Studio in the next step.

### Next Steps

That's it! You're ready to start Android development. 

If you're supporting iOS as well, head over to our [App Store guide](#app-store). 

Afterwards, head over to our [Appdrop setup guide](#appdrop-setup) to start testing your app.

## Appdrop Setup Guide

Your end-product will be a vanilla [React Native](https://reactnative.dev) app built with Typescript. That's just a fancy way of saying you'll be using one of the most robust, well-tested mobile app frameworks on the planet. React Native was originally created by Facebook to power the largest, most mission-critical apps that exist. In other words, you're in great company.

React Native development with Typescript requires the use of a command-line interface such as Terminal for Mac or Git Bash for PC. At points, this will feel like coding, but trust us that we've made this guide incredibly streamlined and you will primarily be pasting our commands or dropping our files into the correct places in your computer. If you ever feel overwhelmed or frustrated, then we recommend our getting help from our Appdrop Experts for a [Fast Track App Submission](https://appdrop.com/pricing).

### 1. Create a dedicated `@appdrop` folder on your computer.

You will need a dedicated space on your computer to house your app's files. Start by creating a folder called `@appdrop` inside your downloads folder so that you can house everything inside one place.

### 2. Launch Your Command Line at this Folder.

Next, Ctrl- Click this folder and select `New Terminal at Folder`.

Once your Command Line is up, type the command `pwd` (short for present-working-director) and press Enter on your keyboard. Your command line should print something like `/Users/yourname/Downloads/@appdrop` to verify that you are inside of your `@appdrop` folder. Leave this window open and run the command line steps from the next step inside this Folder.

Tip – You can organize your Downloads folder alphabetically to place @appdrop at or near the top.

### 3. Prepare Your Computer to run React Native Apps

Your next big milestone will be successfully creating a React Native test project on your device to ensure that your environment setup is correctly. At the end, you should see screens on your iOS and Android devices that look like these photos.

Head over to the React Native Environment Setup guide and follow the instructions for the `React Native CLI Quickstart` option with the `yarn` package manager.

Note – Be absolutely certain that React Native 0.63 is selected in the top left corner of the website so that you follow the correct setup steps.

Select your development OS `Mac`, `Windows`, or `Linux` and go through the setup steps for each type of app you plan to support.

When you reach the *Creating a New Application* step, you will be specifying React Native version 0.63.0 and using the Typescript template. This is the specific command:

```
npx react-native init AwesomeTSProject --version 0.63.0 --template react-native-template-typescript
```

Note for iOS – Make sure to select the .xcworkspace file, not the .xcodeproj file when you launch Xcode.

If everything was done correctly, you will see a new folder inside of @appdrop called AwesomeTSProject.

Note – if you don't have both an iOS and Android device, that is OK! Simulators will help you test your app on the device(s) that you are missing.

Note for Windows Users – In order to install Xcode and publish iOS apps from your PC, you may need to install virtual MacOS software, such as [VirtualBox](https://www.virtualbox.org/) which is free from Oracle.


