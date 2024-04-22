# Panduan Instalasi Flutter Tanpa Android Studio (Windows)
- [Instalasi](#instalasi)
- [Konfigurasi](#konfigurasi)
- [Setting Flutter](#setting-flutter)

## Instalasi
1. Download [SDK Flutter](https://docs.flutter.dev/get-started/install)
3. Download [Command Line Tools](https://developer.android.com/studio)
4. Download [Open JDK](https://adoptium.net/)

## Konfigurasi
1. Buat folder <b>`Android`</b> di partisi <b>`c:/`</b>
2. Buat folder <b>`sdk`</b> di dalam folder <b>`Android`</b>
3. Buat folder <b>`cmdline-tools/latest`</b> didalam folder <b>`sdk`</b>
4. Ekstrak SDK Flutter ke folder <b>`Android`</b>
5. Ekstrak Command Line Tools ke dalam folder <b>`latest`</b>

## Setting flutter
1. Set environtment variable<br><br>
   Buka CMD lalu ketik :
   ```
   setx ANDROID_HOME C:\Android
   ```
   ```
   setx Path C:\Android\flutter\bin;C:\Android\sdk\cmdline-tools\latest\bin
   ```
   Close CMD<br><br>
2. Install Open JDK<br><br>
   Buka CMD. Ketik:
   ```
   java -version
   ```
   untuk melihat versi java yang terinstall<br><br>
   untuk step 3-9 pastikan PC/Laptop terkoneksi ke <b>Internet</b><br>
3. Ketik
   ```
   sdkmanager platform-tools
   ```
4. Ketik
   ```
   sdkmanager “platforms;android-30”
   ```
5. Ketik
   ```
   sdkmanager “build-tools;30.0.0”
   ```
7. Ketik
   ```
   sdkmanager --licenses
   ```
9. Ketik
    ```
    flutter doctor --android-licenses
    ```
11. Ketik
    ```
    flutter doctor
    ```
12. Selesai
