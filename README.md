# OpenGothic 0.6.8 — Direct Folder (Android)

Separate Android ARM64 build of [Solessfir/OpenGothic](https://github.com/Solessfir/OpenGothic), pinned to `launcher-0.6.8` (`98e8ef73993fe0700fabdbb898c4504a090d7860`).

Adds a **Select game folder / Выбрать папку игры** action to the upstream launcher. Allows a legitimate already-installed Gothic I, Gothic II / Night of the Raven, or Archolos directory on Android shared storage to be used directly, without ZIP import or copying game archives. Uses Android 11+ All Files Access because the native engine requires an ordinary absolute filesystem path. Saves and settings stay in the app's own `User/<game>` directory. The stock import and Steam download flows remain present.

Build workflow: [Build 0.6.8 Direct Folder](.github/workflows/build-068.yml). APK and checksums are uploaded to the workflow run's artifacts and to GitHub Releases if CI passes.

Unlike the experimental `Erken22/Gothic-Open-Android` 0.6.7 FIX series, this repository includes upstream OpenGothic 0.6.8 graphics and performance improvements **without** the experimental Turnip/FIX36 renderer patches. Phone stability and performance are not yet verified.

Signing uses this repository's independent key; updating an APK signed by another project may require uninstalling the old package, which may remove app-managed saves. Back up saves first.
