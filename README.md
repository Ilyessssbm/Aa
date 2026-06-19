# witanime-cloudstream

> CloudStream 3 extension for **[WitAnime (witanime.you)](https://witanime.you)** –
> Arabic-subtitled anime streaming.

---

## ⚡ Quick Install (CloudStream app)

1. Open CloudStream → **Settings ⚙️ → Extensions → Add repository**
2. Paste this URL:

```
https://raw.githubusercontent.com/YOUR_USERNAME/witanime-cloudstream/builds/repo.json
```

> Replace `YOUR_USERNAME` with your GitHub username after you fork/clone this repo.

---

## 📦 Manual install

Download the latest `.cs3` file from the
[Releases](../../releases/latest) page and sideload it in CloudStream via
**Settings → Extensions → Install from file**.

---

## 🛠 Build from source

Requirements: JDK 17, Android SDK

```bash
git clone https://github.com/YOUR_USERNAME/witanime-cloudstream
cd witanime-cloudstream
chmod +x gradlew
./gradlew WitAnime:make          # builds WitAnime.cs3
./gradlew WitAnime:deployWithAdb # push directly to a connected phone
```

The `.cs3` output is in `WitAnime/build/`.

---

## ✅ Features

| | |
|---|---|
| 🌐 Language | Arabic (`ar`) |
| 🏠 Home sections | الرئيسية · آخر الحلقات · أفلام · يعرض الآن · TV · OVA · قائمة الأنمي |
| 🔍 Search | ✅ |
| 📺 Types | Anime · AnimeMovie · OVA |
| 🎬 Video servers | ok.ru · Streamwish · Dailymotion · Videa · yonaplay |

---

## 📁 Repository structure

```
witanime-cloudstream/
├── .github/workflows/build.yml   ← Auto-builds & publishes on push
├── WitAnime/
│   ├── build.gradle.kts          ← Plugin metadata
│   └── src/main/kotlin/com/witanime/
│       ├── WitAnimePlugin.kt     ← Entry point
│       └── WitAnimeProvider.kt   ← Scraper
├── build.gradle.kts              ← Root build
├── settings.gradle.kts           ← Module registry
└── gradle.properties
```

---

## ➕ Adding more extensions

1. Create a new folder (e.g. `MyProvider/`) with the same structure as `WitAnime/`.
2. Add `include(":MyProvider")` to `settings.gradle.kts`.
3. Push → GitHub Actions builds and adds it to `repo.json` automatically.

---

## ⚠️ Disclaimer

For personal / educational use only.
Respect the site's terms of service.
