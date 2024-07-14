# Analytics

Analytics is a feature that allows you to track user behavior and measure the effectiveness of your app.

## How to implement analytics?

- Go to your firebase project folder.
- Make sure you have **analytics** enabled.
- Go to **firebase_analytics_service** and use the added methods to log the analytics events.

```dart
logEvent(name, {Map<String, dynamic> params});
```
```dart
logLogin();
```
```dart
logSignUp();
```
```dart
setUserProperty(userId, userEmail);
```
```dart
setAppVersion();
```


## Next step

Go to **[Crashlytics setup](crashlytics.md)** section.
