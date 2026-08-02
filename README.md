# Tugas Mengubah Ikon Aplikasi (Change the App Icon)

| | |
|---|---|
| **Nama** | Faiz Zaki |
| **Kelas** | TI5A1 |
| **NIM** | 452024611006 |
| **Teknologi** | Kotlin, Jetpack Compose |

## Deskripsi Tugas

Menyelesaikan materi Codelab dari Google Developer Codelab: **"Mengubah Ikon Aplikasi"** (*Change the App Icon*).

Pada codelab ini dipelajari cara menggunakan **Image Asset Studio** di Android Studio untuk memperbarui ikon peluncur (*launcher icon*) aplikasi — baik versi **adaptive icon** maupun **legacy icon** — sehingga aplikasi terlihat lebih profesional dan sesuai dengan identitas desain yang diinginkan.

- Referensi codelab: <https://developer.android.com/codelabs/basic-android-kotlin-compose-training-change-app-icon>
- Starter code: [basic-android-kotlin-compose-training-affirmations](https://github.com/google-developer-training/basic-android-kotlin-compose-training-affirmations) (branch `intermediate`)

## Yang Dilakukan

1. Mengunduh *starter code* aplikasi **Affirmations** (branch `intermediate`).
2. Mengganti launcher icon bawaan (Android robot) dengan ikon kustom aplikasi Affirmations melalui Image Asset Studio:
   - **Adaptive icon** (API 26+): `res/mipmap-anydpi-v26/ic_launcher.xml` dan `ic_launcher_round.xml`, terdiri dari dua lapisan:
     - *Foreground layer*: `res/drawable/ic_launcher_foreground.xml` (vector drawable)
     - *Background layer*: `res/drawable/ic_launcher_background.xml` (vector drawable)
   - **Legacy icon** (perangkat di bawah API 26): `res/mipmap-{mdpi,hdpi,xhdpi,xxhdpi,xxxhdpi}/ic_launcher.webp` dan `ic_launcher_round.webp`
3. Build dan verifikasi ikon di emulator.

## Cara Build & Jalankan

Buka project ini di Android Studio lalu tekan **Run**, atau build melalui CLI:

```bash
./gradlew assembleDebug
```

Hasil APK: `app/build/outputs/apk/debug/app-debug.apk`

## Struktur Resource Ikon

```
app/src/main/res/
├── drawable/
│   ├── ic_launcher_background.xml   # background layer (vector)
│   └── ic_launcher_foreground.xml   # foreground layer (vector)
├── mipmap-anydpi-v26/               # adaptive icon (API 26+)
│   ├── ic_launcher.xml
│   └── ic_launcher_round.xml
└── mipmap-{mdpi,hdpi,xhdpi,xxhdpi,xxxhdpi}/
    ├── ic_launcher.webp             # legacy icon (raster)
    └── ic_launcher_round.webp       # legacy icon round (raster)
```
