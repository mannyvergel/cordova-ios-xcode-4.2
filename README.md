cordova-ios-xcode-4.2
=====================

Phonegap / Cordova 2.9 and XCode 4.2 Sample Project

Summary:

This is a Phonegap / Cordova Sample Project that works with XCode 4.2.

Fixed all link and compile errors, undefined variables that's only available with SDK >= 5.1.

Tried with XCode 4.2 with 5.0 Simulator iOS SDK.


Background:

When you download Cordova / Phonegap and create an iOS project using the create command, the resulting project has many compile errors if you do not use XCode 4.5. It is also written in their documentation and at least XCode 4.5 is needed to run their project. 

The first error you will encounter is CDVInvokedUrlCommand for instance message does not declare a method with selector... on line 62 of CDVInvokedUrlCommand.m with the code: [self massageArguments];


Found out that the compatibility issue was just due to declarations, position of methods, and use of new syntax (The "at" syntax of new iOS @{} for NSDictionary). So I just changed the code to be compatible with older version of compiler / SDK.