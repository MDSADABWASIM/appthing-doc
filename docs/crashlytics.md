# Crashlytics

## What is crashlytics?

Crashlytics is a feature that allows you to track and analyze crashes and exceptions in your app.

## How to implement crashlytics?

- It's already configured in the project.
- But if you want to manually log any crashes or exceptions, you can use the the existing **crashlytics** service methods:

```dart
recordError(exception, stackTrace, exceptionReason);
```
```dart
errorLog(error);
```
