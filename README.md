# Hotel HMS Mobile

Flutter mobile application for the Hotel Management System.

## Backend

Default API base URL:

`https://hotel.kemmytech.com/api`

Change it in:

`lib/core/api_config.dart`

## Expected Laravel API endpoints

The app is ready to consume:

- POST `/api/login`
- POST `/api/logout`
- GET `/api/me`
- GET `/api/dashboard`
- GET `/api/rooms`
- GET `/api/bookings`
- GET `/api/guests`
- GET `/api/tasks`
- GET `/api/pos/orders`
- GET `/api/inventory/items`
- GET `/api/notifications`

Login should return a token as either `token` or `access_token`, plus a `user` object.

Use Laravel Sanctum for mobile token authentication.

## Create missing Flutter platform files

If you extracted this source into a new folder, run once:

```powershell
& "D:\development\flutter\bin\flutter.bat" create . --platforms=android,ios
```

Flutter may regenerate standard platform boilerplate while keeping `lib/` and `pubspec.yaml`.

## Run in VS Code / PowerShell

```powershell
cd D:\projects\hotel_hms

& "D:\development\flutter\bin\flutter.bat" clean
& "D:\development\flutter\bin\flutter.bat" pub get
& "D:\development\flutter\bin\flutter.bat" analyze
& "D:\development\flutter\bin\flutter.bat" devices
& "D:\development\flutter\bin\flutter.bat" run
```

## Production next steps

The frontend is structured so detailed CRUD screens can be expanded without changing authentication or networking architecture. If an endpoint is not yet available on the Laravel backend, that page will show a controlled server/error state rather than crashing.
