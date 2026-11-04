# Flyerss Signal — Android starter project

A native Android WebView shell with a responsive dashboard inspired by the supplied reference image.

## Included
- Dark dashboard UI for XAUUSD
- Live spot-price fetch from the existing Flyerss Signal Worker `/price` endpoint
- Connection / stale-data status and 30-second refresh
- Screener-style M1 / M5 / M15 panel
- Android Studio project and GitHub Actions cloud-build workflow

## Important
The BUY/SELL badge, reference entry/TP figures, running pips and screener rows are demo placeholders. They are **not** calculated trading signals and must not be used to place trades. This starter app does not connect to a broker or execute orders.

## Build APK using GitHub Actions
1. Create a new GitHub repository.
2. Upload the contents of this folder to the repository root.
3. Open the **Actions** tab and enable workflows if GitHub asks.
4. Run **Build Flyerss Signal APK**.
5. When it finishes, open the workflow run and download the `FlyerssSignal-debug-apk` artifact.
6. Extract the ZIP and install `app-debug.apk` on your Android phone. Android may ask you to allow installation from that source.

## Build locally
Open this folder in Android Studio (JDK 17), wait for Gradle sync, then select **Build > Build Bundle(s) / APK(s) > Build APK(s)**.

## API
The app currently reads:
`https://flyerss-signal-api.prohunterkhil08.workers.dev/price`

If the Worker URL changes, update the `API` constant in `app/src/main/assets/index.html`.
