# Cloud storage

We are giving you a ready-made cloud storage support for your app.

## Which cloud storage are supported?

- We are supporting **Firebase** and **Supabase** cloud storage.
- You can choose any of the above cloud storage and follow the instructions to use it in your app.

## Firebase cloud storage usage

- Supported file types are: 
    - Images
    - Videos
    - Audio
    - Documents
    - Archives

- You can select the file and upload it using this  function:

```dart
uploadFile(String filePath) // You'll get the url in return to access the file
```

- Get the url of any uploaded file:

```dart
getDownloadUrl(String filePath)
```
- Download the file in your local storage:

```dart
downloadFile(String filePath)
```

- Delete the file:

```dart
deleteFile(String filePath)
```
- If you encounter any error, please check the **[usage section](https://firebase.google.com/docs/storage/flutter/start)**

## Supabase cloud storage usage

- Supported file types are: 
    - Images
    - Videos
    - Audio
    - Documents
    - Archives

- We're using 'users' bucket for storing files.
- You can select the file and upload it using this  function:

```dart
uploadToStorage(String id, io.File file)
```

- Update the file:

``` dart
updateFileOfStorage(String id, io.File file)
```

- Delete the file:

```dart
deleteFileFromStorage(String id)
```


## Next step

Go to **[Push notifications setup](push_notifications.md)** section.
