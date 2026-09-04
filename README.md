# 🛡️ Strip AI Labels & Metadata Stripper (Images & Videos)

<p align="center">
  <img src="https://img.shields.io/badge/Privacy-100%25_Client--Side-4ade80?style=for-the-badge&logo=shield" alt="100% Client-Side" />
  <img src="https://img.shields.io/badge/Hosted_on-Cloudflare_Pages-f38020?style=for-the-badge&logo=cloudflarepages&logoColor=white" alt="Cloudflare Pages" />
  <img src="https://img.shields.io/badge/Supports-Images_%26_Videos-c084fc?style=for-the-badge" alt="Images and Videos" />
  <img src="https://img.shields.io/badge/Offline-Ready-38bdf8?style=for-the-badge&logo=offline" alt="Offline Ready" />
  <img src="https://img.shields.io/badge/License-MIT-a855f7?style=for-the-badge" alt="MIT License" />
</p>

<p align="center">
  <strong>Strip C2PA Content Credentials, EXIF Camera/GPS tags, Adobe XMP, UDTA atoms, and AI generator labels from Images &amp; Videos entirely inside your browser. No server uploads. Instant, lossless, and 100% private.</strong>
</p>

---

## 🌐 Live Web Application

🚀 **[https://remove-ai-labels.pages.dev/](https://remove-ai-labels.pages.dev/)**

---

## ✨ Features

- 🔒 **100% Client-Side & Private**: All scrubbing runs locally in your browser’s memory. Your images and videos never leave your device.
- 🎬 **Full Image & Video Support**: Sanitizes both static images (JPG, PNG, WebP) and videos (MP4, MOV, WebM).
- ⚡ **Zero-Loss Video Surgery**: Strips C2PA manifests, QuickTime `udta` atoms, and metadata boxes without re-encoding, preserving 100% video/audio quality and frame synchronization.
- 🖼️ **Lossless Image Canvas**: Preserves full pixel fidelity, color profiles, and native resolution ($W \times H$).
- 🏷️ **Bypasses Social AI Tags**: Removes C2PA manifests and XMP metadata tags used by Instagram, Facebook, Threads, and TikTok to mark media with "AI Info" tags.
- 📋 **Multiple Input & Output Options**:
  - **Drag & Drop**: Drag images or videos anywhere onto the screen.
  - **Clipboard Paste (`Ctrl + V`)**: Copy any image and paste it directly on the webpage.
  - **1-Click Demo Samples**: Test metadata stripping instantly with sample image and video generators.
  - **Copy to Clipboard**: Copy cleaned images directly to your clipboard for quick sharing.
  - **Direct Download**: Download sanitized files with original format preserved (`clean_filename.mp4/png/jpg/mov/webm`).
- 📱 **Mobile & Desktop First**: Fully responsive dark mode UI optimized for touch gestures, mobile browsers, tablets, and desktop displays.
- 📊 **Real-Time Metadata Stats**: Displays file size, pixel dimensions, format, and processing speed benchmark in milliseconds.

---

## 🧹 What Metadata Gets Stripped?

| Metadata / Tag Type | Description | Media | Status |
|---|---|:---:|:---:|
| **C2PA Manifests & Boxes** | Cryptographic digital signatures & Content Credentials used by AI models (Midjourney, DALL-E 3, Sora, Runway, Adobe Firefly, etc.) | Images & Videos | ✅ **Stripped** |
| **MP4 / MOV `udta` & `uuid`** | QuickTime / MP4 user data atoms, GPS coordinates, camera specs, and creation software tags | Videos | ✅ **Stripped** |
| **Adobe XMP & Metadata** | Photoshop & Premiere edit history, AI generation tags, metadata trees, and custom headers | Images & Videos | ✅ **Stripped** |
| **EXIF & Camera Specs** | Camera model, lens, shutter speed, timestamp, serial numbers, and device specifications | Images | ✅ **Stripped** |
| **GPS Geolocation** | Geotagging coordinates, altitude, and location timestamps embedded in media headers | Images & Videos | ✅ **Stripped** |
| **IPTC & Comments** | Author/copyright text chunks, software tags, and non-pixel payload comments | Images & Videos | ✅ **Stripped** |

---

## ⚙️ How It Works

1. **Images (Canvas Extraction)**: Images are drawn onto a hardware-accelerated 2D canvas buffer, discarding all non-pixel metadata headers while preserving raw RGB/RGBA pixels.
2. **Videos (ISO BMFF Stream Surgery)**: For MP4 and MOV files, an in-memory binary parser walks the atom/box hierarchy, strips `uuid` C2PA manifests, `udta` atoms, and metadata trees, while adjusting `stco` / `co64` chunk offset tables to ensure instantaneous, lossless playback without video re-encoding.
3. **Memory-Safe Zero-Uploads**: Operates completely in-memory using `Blob` and `URL.createObjectURL()`, keeping your data 100% secure and offline-capable.

---

## 🚀 Quick Start / Local Setup

You can run this project locally without installing any web servers or dependencies:

1. **Clone the repository:**
   ```bash
   git clone https://github.com/HasanImamShanto/Strip-AI-Labels-Metadata.git
   cd Strip-AI-Labels-Metadata
   ```

2. **Open the web app:**
   Simply double-click `index.html` or open it in any modern browser:
   - Chrome / Brave / Edge
   - Safari (iOS & macOS)
   - Firefox
   - Opera

---

## 🛠️ Supported Formats

- **Images**: JPEG / JPG (`.jpg`, `.jpeg`), PNG (`.png`), WebP (`.webp`)
- **Videos**: MP4 (`.mp4`), QuickTime MOV (`.mov`), WebM (`.webm`)

---

## 🌟 Support & Star

If this tool helped you protect your privacy or remove AI tags from your images and videos, please consider giving this project a **⭐ Star** on GitHub!

---

## 📄 License

This project is licensed under the [MIT License](LICENSE). Feel free to use, modify, and distribute it freely.

