# Force update

Force update is a feature that allows users to update your app to the latest version and prevent user to use the old version.

## How to implement force update?

- We've already implemented this feature in the project.
- You just need to do the following:

- Go to your firebase project folder
- Set these 3 values in **Remote config**

```
// make it true when you want to force your user to update the app
force_update: false 

// Android version which you want your user to use
force_update_android_version: "1.0.0" 

// iOS version which you want your user to use
force_update_ios_version: "1.0.0" 
```

- Once done, update these values in remote config, whenever you want to **force** your user to update the app.


## Next step

Go to **[Onboarding](onboarding.md)** section.
