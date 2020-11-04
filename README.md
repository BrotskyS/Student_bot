# Requirements

	- support ONLY Android OS
	- nodejs > 12
	- yarn
	- Android studio
	- Android emulator nexus_4_API_22 Android v5.1.1
	- Java v8

## Java Development Kit
React Native requires version 8 of the Java SE Development Kit (JDK). You may download and install OpenJDK from AdoptOpenJDK or your system packager. You may also Download and install Oracle JDK 8 if desired.

# Build and run instructions

1. Open the project directory into terminal.
2. Run `npm install`. This should download and create the directory with dependencies.
3. Run `Android Studio` and open `./android` folder. Studio will sync and download all dependencies.
4. Run `yarn start` to start the server to deliver the bundle url. Make sure this is running before you start your application.
5. Into the other terminal run `yarn android` to start app.
6. For first start app will need add device id to a staging. Please send device id to admin from console log on the terminal.

# other instructions

reset metro bundler cache: `yarn start --reset-cache --verbose`

If Android Studio report `Unsupported Modules Detected` or don't found modules
 - delete the `./android/.idea` directory

# Build and run instructions for Mac os
1. Open the project directory into terminal.
2. Run `npm install`. This should download and create the directory with dependencies.
3. Install [brew](https://brew.sh/index_ru) `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"`
4. Install yarn `brew install yarn`
5. Install watchman `brew install watchman`
6. Instal adb `brew cask install android-platform-tools`
7. Install java v8 `brew cask install adoptopenjdk/openjdk/adoptopenjdk8`
8. Open Android Studio open Appearance & Behavior → System Settings → Android SDK. Select: Android SDK Platform 29, Intel x86 Atom_64 System Image or Google APIs Intel x86 Atom System Image
9. Open file `$HOME/.bash_profile` and past this code 

		export ANDROID_HOME=$HOME/Library/Android/sdk
		export PATH=$PATH:$ANDROID_HOME/emulator
		export PATH=$PATH:$ANDROID_HOME/tools
		export PATH=$PATH:$ANDROID_HOME/tools/bin
		export PATH=$PATH:$ANDROID_HOME/platform-tools
		
10. Run `Android Studio` and open `./android` folder. Studio will sync and download all dependencies.
11. Run `yarn start` to start the server to deliver the bundle url. Make sure this is running before you start your application.
12. Into the other terminal run `yarn android` to start app.
13. For first start app will need add device id to a staging. Please send device id to admin from console log on the terminal.
