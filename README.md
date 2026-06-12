# Linear Raw

Linear Raw is a high-performance Android application designed for photographers and enthusiasts who need to convert RAW image files directly on their mobile devices. Built with a focus on image quality and technical precision, it leverages the powerful **LibRaw** C++ library via JNI to provide professional-grade RAW decoding and conversion to 16-bit Linear DNG.

## ✨ New in v1.3.0 (v7)

- **Universal RAW Support:** Now supports a wide range of RAW formats from major manufacturers including **Sony (.ARW), Nikon (.NEF), Canon (.CR2, .CR3), Fujifilm (.RAF), Olympus (.ORF), Panasonic (.RW2), Pentax (.PEF)**, and more. Featuring specialized black level handling for **Fujifilm RAF** files to ensure color accuracy across all sensor types.
- **Improved Metadata Extraction:** Enhanced support for multi-brand EXIF and MakerNote data.
- **DNG and JPEG Filtering:** Improved import logic to exclude DNG and JPEG files, focusing strictly on high-quality RAW source conversion.
- **Refined UI:** Updated branding and interface to reflect universal RAW support and improved clarity.

## ✨ Features

- **Batch Conversion:** Process multiple RAW files simultaneously with an efficient background queue.
- **Compressed & Uncompressed Support:** Choose between maximum quality uncompressed DNGs or space-saving Lossless ZIP DNGs (Adobe DNG 1.4).
- **Professional Metadata:** Extracts and displays detailed EXIF and MakerNote data, including ISO, Shutter Speed, Aperture, Focal Length, Lens Model, and Body Serial Number.
- **Native RAW Engine:** High-speed decoding using a custom C++ layer powered by `LibRaw`, supporting hundreds of camera models.
- **Calibration Precision:** Access to technical RAW data including Black/White levels, Camera Multipliers, and CFA (Bayer) patterns, with model-specific color matrices.
- **HEVC Thumbnail Support:** Integrated `libde265` for decoding high-resolution HEVC previews embedded in modern RAW files.
- **Diagnostic Pipeline:** Includes a "Core Trace" view for real-time telemetry and diagnostic log outputs during the conversion process.
- **Modern UI:** A beautiful, responsive interface built with **Jetpack Compose**, featuring glassmorphism elements and full support for Dark Mode.
- **History Tracking:** Keep track of previous conversions with a built-in history screen powered by Room Database.

## 🛠 Tech Stack

- **UI:** Jetpack Compose, Material 3
- **Language:** Kotlin & C++
- **Native Layer:** JNI, LibRaw, libde265
- **Database:** Room (for conversion history)
- **Architecture:** MVVM with Coroutines and Flow

## 📁 Project Structure

- `:app`: The main Android application module containing the UI and business logic.
- `:raw-engine`: A dedicated Android Library module housing the native C++ code, LibRaw integration, and DNG generation logic.

## 🚀 Getting Started

### Prerequisites
- Android Studio Ladybug (or newer)
- Android SDK 24+
- NDK (for compiling the `raw-engine`)

### Installation
1. Clone the repository.
2. Open the project in Android Studio.
3. Sync Gradle and ensure all dependencies are resolved.
4. Connect an Android device or start an emulator.
5. Build and Run.

## 📄 Licenses & Privacy

Linear Raw utilizes several open-source libraries:
- **LibRaw:** Copyright (C) 2008-2025 LibRaw LLC. Licensed under CDDL 1.0 or LGPL 2.1.
- **libde265:** Copyright (C) 2013-2024 struktur AG. Licensed under LGPL 2.1.
- **Android Jetpack & Material Components:** Apache 2.0.
- **Room, DataStore, & Lifecycle:** Apache 2.0.
- **Coil:** Apache 2.0.

For more information on how we handle your data, please see our [Privacy Policy](PRIVACY_POLICY.md).

---
*Developed by Scott Loucks*
