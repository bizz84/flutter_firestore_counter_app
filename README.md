# flutter_firestore_counter_app

Minimal demo showing how to use Firestore as a backend for the Flutter counter app.

![Counter App Preview](/.github/images/firebase-emulator-flutter-web-counter.png)

## Firebase setup

Open the [Firebase console](https://console.firebase.google.com/) and follow these steps:

- Create a new Firebase app
- Go to Cloud Firestore and create the database, enabling security rules in **test mode**
- Go to Firebase project settings and copy the Firebase project ID

From the terminal:

- Clone this repo and `cd` into it
- Run `firebase init` and go through the setup steps (choose **Firestore** and **Emulators** only)
- Select the Firebase project ID from above
- When setting up the emulator, only the Firestore emulator is needed

Example log:

```

     ######## #### ########  ######## ########     ###     ######  ########
     ##        ##  ##     ## ##       ##     ##  ##   ##  ##       ##
     ######    ##  ########  ######   ########  #########  ######  ######
     ##        ##  ##    ##  ##       ##     ## ##     ##       ## ##
     ##       #### ##     ## ######## ########  ##     ##  ######  ########

You're about to initialize a Firebase project in this directory:

  /Users/andrea/work/codewithandrea/github/flutter-scratch/flutter_firestore_counter_app

Before we get started, keep in mind:

  * You are initializing within an existing Firebase project directory

? Which Firebase features do you want to set up for this directory? Press Space to select features, then Enter to confirm your 
choices. Firestore: Configure security rules and indexes files for Firestore, Emulators: Set up local emulators for Firebase 
products

=== Project Setup

First, let's associate this project directory with a Firebase project.
You can create multiple project aliases by running firebase use --add, 
but for now we'll just set up a default project.

? Please select an option: Use an existing project
i  Don't want to scroll through all your projects? If you know your project ID, you can initialize it directly using firebase init --project <project_id>.

? Select a default Firebase project for this directory: flutter-firestore-counter-app (flutter-firestore-counter-app)
i  Using project flutter-firestore-counter-app (flutter-firestore-counter-app)

=== Firestore Setup

Firestore Security Rules allow you to define how and when to allow
requests. You can keep these rules in your project directory
and publish them with firebase deploy.

? What file should be used for Firestore Rules? firestore.rules
? File firestore.rules already exists. Do you want to overwrite it with the Firestore Rules from the Firebase Console? No

Firestore indexes allow you to perform complex queries while
maintaining performance that scales with the size of the result
set. You can keep index definitions in your project directory
and publish them with firebase deploy.

? What file should be used for Firestore indexes? firestore.indexes.json
? File firestore.indexes.json already exists. Do you want to overwrite it with the Firestore Indexes from the Firebase Console?
 No

=== Emulators Setup
? Which Firebase emulators do you want to set up? Press Space to select emulators, then Enter to confirm your choices. 
Firestore Emulator
i  Port for firestore already configured: 8080
i  Emulator UI already enabled with port: (automatic)
? Would you like to download the emulators now? Yes

i  Writing configuration info to firebase.json...
i  Writing project information to .firebaserc...

✔  Firebase initialization complete!
```

## FlutterFire Setup

From the terminal, run `flutterfire configure`

If needed, install flutterfire:

```
dart pub global activate flutterfire_cli
```

Then configure the project, selecting the Firebase project created before:

```
flutterfire configure
```

Finally, install the Flutter packages:

```
flutter pub get
```


## Running the app

- Start the Firebase emulator: `firebase emulators:start`
- Run the Flutter app on web: `flutter run -d chrome`

### [LICENSE: MIT](LICENSE.md)
