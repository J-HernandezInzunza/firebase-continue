# Firebase Continue Samples - "Continote" iOS App

This directory contains a sample iOS app titled "Continote" which uses the
Firebase Continue for iOS library.

Users can begin writing a note in this app and then continue writing in Chrome
from exactly where they are using the
[sample Chrome extension](../chrome-extension) and [sample web app](../web).

For users with a macOS computer that is paired with their iOS device to be
[Apple Handoff](https://developer.apple.com/handoff/) enabled,
this app also leverages that technology (via Firebase Continue) to provide users with
the option to continue writing directly within Safari.

## Table of Contents

1. [Prerequisites](#prerequisites)
2. [Setup](#setup)
3. [Usage](#usage)
4. [Compatibility](#compatibility)
5. [Dependencies](#dependencies)
6. [Disclaimer](#disclaimer)

## Prerequisites

Before proceeding to the [Setup section](#setup) below, you must
first follow the [main `samples` README](../) so that you have a properly
configured Firebase project for this and any other "Continote" samples
you run.

## Setup

After completing the following steps, you will have a properly configured instance of
this sample to build and install to try out:

1.  First, make sure you followed the [Prerequisites section](#prerequisites) above.

2.  Go to the
    [Firebase console for your Firebase project](https://console.firebase.google.com/)

3.  Click to "Add Firebase to your iOS app":

    1.  In the dialog that opens, when asked for an iOS bundle ID, choose one for your
        sample app (ex. `com.my-unique-name.firebase.continue.sample.continote`).

        **Make note of this bundle ID as you will need it later.**

    2.  Leave everything else in this dialog as is, and click the
        **Register App** button.

    3.  Click the "Download GoogleService-info.plist" button, then close the dialog
        as we do not need to perform the dialog's remaining steps to set up
        this sample.

    4.  Copy the `GoogleService-info.plist` file you just downloaded to
        the [`Continote/Continote/`](Continote/Continote) directory.

4.  Copy the `sample-project.pbxproj` file from
    [`Continote/Continote.xcodeproj`](Continote/Continote.xcodeproj)
    file by first right-clicking `Continote/Continote.xcodeproj` and then
    clicking "Show Package Contents".

    Then, paste a copy of it also in
    [`Continote/Continote.xcodeproj`](Continote/Continote.xcodeproj).

5.  Rename the `sample-project.pbxproj` copy to `project.pbxproj`.

6.  Open `project.pbxproj` in a text editor and fill out the clearly marked
    *[TODO: YOUR-VALUE-HERE]* details:

    1.  Replace the two instances of *[TODO: YOUR-IOS-BUNDLE-ID-HERE]* with your
        iOS bundle ID from above (without any quotes).

7.  Copy the `sample-Info.plist` file from the
    [`Continote/Continote/`](Continote/Continote)
    directory and paste a copy of it also in
    [`Continote/Continote/`](Continote/Continote).

8.  Rename the `sample-Info.plist` copy to `Info.plist`.

9.  Open `Info.plist` in a text editor and fill out the clearly marked
    *[TODO: YOUR-VALUE-HERE]* details:

    1.  Replace the two instances of *[TODO: YOUR-FACEBOOK-APP-ID-HERE]* with your
        Facebook app's ID from the [Prerequisites section](#prerequisites) above.

    2.  Replace *[TODO: YOUR-FACEBOOK-APP-NAME-HERE]* with your Facebook app's name
        from the [Prerequisites section](#prerequisites) above.

    3.  Replace *[TODO: YOUR-GOOGLESERVICE-INFO.PLIST-RESERVED_CLIENT_ID-HERE]*
        with the `RESERVED_CLIENT_ID` value in your `GoogleService-Info.plist` file.

10. Copy the `Sample-Constants.swift` file from the
    [`Continote/Continote/`](Continote/Continote)
    directory and paste a copy of it also in
    [`Continote/Continote/`](Continote/Continote).

11. Rename the `Sample-Constants.swift` copy to `Constants.swift`.

12. Open `Constants.swift` in a text editor and fill out the clearly marked
    *[TODO: YOUR-VALUE-HERE]* details:

    1.  Replace *[TODO: YOUR-FIREBASE-HOSTING-URL-FOR-CONTINOTE-WEB-HERE]* with the
        Firebase Hosting URL of the Continote sample web app your project from the
        [Prerequisites section](#prerequisites) above.

        For example: `https://SomeDeployedFirebaseProjectName.firebaseapp.com`

13. Copy the `FCNContinue.h` and `FCNContinue.m` Firebase Continue for iOS library files from the
    [`../../ios/FirebaseContinue/FirebaseContinue/Classes/`](../../ios/FirebaseContinue/FirebaseContinue/Classes)
    directory, and paste a copy of them in the
    [`Continote/Continote/`](Continote/Continote) directory.

14. If you have not already done so, [install CocoaPods](https://cocoapods.org/).

    CocoaPods is used for dependency management for this sample.

15. Use CocoaPods to install all remaining dependencies by using the `pod install` command
    in the [`Continote/`](Continote) directory.

16. Open [`Continote/Continote.xcworkspace`](Continote/Continote.xcworkspace) in Xcode.

17. Done!

    You should now be able to build and then install the sample on any compatible iOS
    device or simulator.

## Usage

After this sample is properly set up and installed on your iOS device or simulator,
open it.

From there, you will be asked to sign in to be able to add notes, delete notes, or
open to edit a note.

When editing a note, you will also have the option of "continuing" to write/edit the
note elsewhere (i.e. within Chrome). To make use of this, be sure to also install the
[sample Chrome extension](../chrome-extension).

## Compatibility

This sample app is compatible with the
[same versions of iOS as the Firebase Continue library itself](../../ios/#compatibility).

In order to build and install this sample on an iOS device or simulator,
you must be using a macOS computer with Xcode 8+.

## Dependencies

This sample is dependent on the following libraries/SDKs:

### Firebase
- [Firebase/Auth v4.0+](https://firebase.google.com/docs/auth/ios/start#add_firebase_auth_to_your_xcode_project)
- [Firebase/Database v4.0+](https://firebase.google.com/docs/database/ios/start#add_firebase_database_to_your_app)

### Firebase Continue
- [Firebase Continue for iOS v0.1+](../../ios)

### FirebaseUI
- [FirebaseUI iOS v4.0+](https://github.com/firebase/FirebaseUI-iOS)

### Material Components
- [Material Components iOS v31.0+](https://material.io/components/ios/)

## Disclaimer

The focus of this sample is to demonstrate Firebase Continue usage in a
somewhat realistic scenario. This sample can also act as a simple model of how
to use Firebase and FirebaseUI in an iOS app.

The focus is *not*, however, to have a perfect user interface or user
experience. Please keep that in mind when trying out this sample.
