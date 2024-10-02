# Setup

## Initialize

### Step 1: Clone the appthing github repo

```bash
git clone https://github.com/MDSADABWASIM/appthing <your_repo_name_here>
```
### Step 2: Remove the .git directory
`cd <your_repo_name_here>` and then run this command

```bash
rm -rf .git
```
### Step 3: Initialize a new Git repository
```bash
git init
```
### Step 4: Add your repository url
```bash
git remote add origin <your_repo_url_here>
```

## Tools needed

**Add these four CLI tools that will help you in each step (needed)**

1. ### [Flutter_launcher_icons](https://pub.dev/packages/flutter_launcher_icons)
- add this library in `pubspec.yaml` flutter_launcher_icons: latest-version

2. ### [Flutterfire CLI](https://firebase.flutter.dev/docs/cli/)
- install [Node.js](https://nodejs.org/en/download)
- Run this command `npm install -g firebase-tools`
- ```dart pub global activate flutterfire_cli```

3. ### [Stacked CLI](https://stacked.filledstacks.com/docs/tooling/stacked-cli/)
- ```dart pub global activate stacked_cli```


## Rename app packages and name (needed)

- Go to `package_rename_config.yaml` file and update the app_name, package_name, bundle_name as required.
- Check an example config [here](https://github.com/chandrabezzo/package_rename/blob/main/example/example.md#default-configuration)
- Then run this command ```dart run package_rename_plus```
- Then go to `pubspec.yaml` and change the name from `name: ship_app` to `name: your_app_name`
- Do a global search & replace for `ship_app` to `your_app_name`


## Change your app icons

- Replace your android icon on assets/icons/android_icon.png
- Replace your iOS icon on assets/icons/ios_icon.png
- `flutter pub get`
- `flutter pub run flutter_launcher_icons`

## Add Firebase in app (needed)
- Create a new project in firebase
- ```firebase logout``` and then
- ```firebase login``` (to the same account you used to create the project)
- ```flutterfire configure``` & select the project you created
-   Import the generated file in main.dart  ```import 'firebase_options.dart';```

## If you want to use supabase instead of firebase
- Go to **[supabase](https://supabase.io/)** and create an account
- Create a new project
- Go to supbase dashboard and copy supabase url and public key(anon key) and paste it in your .env file(in codebase)

```
SUPABASE_PUBLIC_KEY = ''
SUPABASE_API_URL = ''
```

## To speed up development use Stacked CLI
-   **[Stacked](https://stacked.filledstacks.com)** is an MVVM based architecture that helps you to build your app faster.
-   You can create new services, views and viewModels with a single command.

?> For more use cases of `stacked-cli`, head over to the [stacked-cli documentation](https://stacked.filledstacks.com/docs/getting-started/overview)

## Setup is done, Let's start configuring your app

Go to **[Force update](force_update.md)** section.

