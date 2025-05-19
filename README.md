# Panduan Instalasi Flutter Tanpa Android Studio (Windows)
- [Instalasi](#instalasi)
- [Konfigurasi](#konfigurasi)
- [Setting Flutter](#setting-flutter)
- [Install Emulator](#install-emulator)

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
   setx JAVA_HOME C:\Program Files\Eclipse Adoptium\jdk-21.0.7.6-hotspot
   ```
   ```
   java -version
   ```
   untuk melihat versi java yang terinstall<br><br>
   untuk step 3-9 pastikan PC/Laptop terkoneksi ke <b>Internet</b><br>
4. Ketik
   ```
   sdkmanager "platform-tools"
   ```
5. Ketik
   ```
   sdkmanager “platforms;android-30”
   ```
6. Ketik
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

## Install Emulator
Lihat device yang bisa diinstall
```
sdkmanager --list
```
Pilih device yang diinginkan, kemudian install
```
sdkmanager "system-images;android-30;google_apis;x86_64"
```
Tambahkan Lisensi
```
sdkmanager --licenses
```
Membuat virtual device
```
avdmanager create avd -n google_api_30 -k "system-images;android-30;google_apis;x86_64"
```
Arahkan ke path emulator
```
cd %ANDROID_HOME%\sdk\emulator
```
Jalankan emulator
```
emulator -avd google_api_30
```
jika muncul error. Pergi ke control panel->program and feature->turn windows feature on or off->Ceklis `virtual machine platform` dan `windows hypervisor platform`

Cek apakah device terdeteksi di flutter
```
flutter devices
```
