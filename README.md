# Loadspreader_Unity_Checker
A mobile‑friendly web application designed to help engineers, planners, and site supervisors quickly calculate ground bearing pressures when using load spreaders, mats, or crawler tracks under cranes and heavy equipment. 

---

## 🛠 Requirements

* **Android Studio Hedgehog** (or newer)  
* **Java 17 JDK** (bundled with recent Android Studio)  
* A connected Android device or emulator running **API 21+** (Android 5.0 Lollipop or higher)

---

## 🚀 Build & run

1. **Clone / unzip** this repo.  
2. In Android Studio, **File ▸ Open** and select the project folder.  
3. Let **Gradle sync** finish (first run downloads Android SDK components).  
4. Click **Run ▶︎** to install the debug build on a device/emulator.  
   *—or* **Build ▸ Build APK(s)** to get a release or debug APK for sideloading.

---

## 🔄 Updating the calculator

1. Replace `app/src/main/assets/index.html` (and any images/scripts) with your new version.  
2. Increment `versionCode`/`versionName` in `app/build.gradle` if you’re distributing updates.  
3. Re-build; the WebView will load the updated files.

---

## 🚧 Troubleshooting

| Symptom | Fix |
|---------|-----|
| **“Namespace not specified”** | Make sure `namespace 'com.example.loadspreader'` is present in the `android {}` block of `app/build.gradle`. |
| **Gradle warning: ‘prefer settings repositories’** | We already use `repositoriesMode.set(RepositoriesMode.PREFER_SETTINGS)` in `settings.gradle`. If you add new modules, stick to that pattern. |
| **White screen in release build** | Verify that `index.html` and all referenced assets (images, JS, CSS) are under `assets/`. Relative paths only—no `file:///` or absolute URLs unless they’re online resources. |

---

## 📄 License

This wrapper code is released under the **MIT License** (see `LICENSE`).  
Your original Loadspreader Calculator HTML/JS remains under its existing license.
