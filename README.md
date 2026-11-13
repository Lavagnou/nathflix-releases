<h1 align="center">Nathflix</h1>

<p align="center">
  <b>A Netflix-style Stremio app for Windows, macOS, Linux and TVs.</b><br>
  Download, sign in, done. Works with your existing addons. Nothing to configure.<br>
  <sub>Also available as a plugin for Stremio Enhanced.</sub>
</p>

<p align="center">
  <a href="https://github.com/lavagnou/nathflix-releases/releases/latest"><img alt="Latest release" src="https://img.shields.io/github/v/release/lavagnou/nathflix-releases?label=release&color=e50914&style=flat-square"></a>
  <img alt="Windows · macOS · Linux · Android TV · Fire TV" src="https://img.shields.io/badge/Windows%20·%20macOS%20·%20Linux%20·%20Android%20TV%20·%20Fire%20TV-222?style=flat-square">
  <a href="LICENSE"><img alt="GPL-3.0" src="https://img.shields.io/badge/license-GPL--3.0-222?style=flat-square"></a>
</p>

> [!NOTE]
> This repository holds Nathflix's releases and its Stremio Enhanced plugin, and nothing else: the apps, the plugin, its installers, and the source code of each version (attached to its release). Nathflix is a personal project based on [dx.bi](https://github.com/notdxbi/dxbi-stremio), built with the help of [Claude Code](https://www.anthropic.com/claude-code), Anthropic's AI coding assistant. It isn't affiliated with Netflix, Stremio or dx.bi.

<br>

## Install

Pick your device below. It takes about two minutes.

| Device | Download |
|---|---|
| Windows 10 and 11 | [**Download for Windows**](https://github.com/lavagnou/nathflix-releases/releases/latest/download/nathflix-Setup-x64.exe) |
| Mac with an Apple chip (M1, M2, M3, M4…) | [**Download for Mac (Apple chip)**](https://github.com/lavagnou/nathflix-releases/releases/latest/download/nathflix-mac-arm64.dmg) |
| Mac with an Intel chip | [**Download for Mac (Intel)**](https://github.com/lavagnou/nathflix-releases/releases/latest/download/nathflix-mac-x64.dmg) |
| Linux | [**Download for Linux**](https://github.com/lavagnou/nathflix-releases/releases/latest/download/nathflix-linux-x86_64.AppImage) |
| Android TV, Google TV, Fire TV | [**See the TV steps**](#on-a-tv) |

Not sure which Mac you have? Click the Apple menu  → *About This Mac*. "Chip: Apple M…" means an Apple chip; "Processor: Intel" means Intel.

> [!TIP]
> You'll sign in with a Stremio account. If you don't have one yet, it's free: create it in the app when it asks, or at [stremio.com](https://www.stremio.com).

### On Windows

1. Open the file you downloaded (`nathflix-Setup-x64.exe`).
2. Windows may show *"Windows protected your PC"*, because Nathflix is a small free project without a paid publisher certificate. Click **More info**, then **Run anyway**.
3. Nathflix installs and opens by itself. It's then in your Start menu.
4. Sign in with your Stremio account.

Nathflix sets up Stremio's streaming server by itself (it's what plays torrents), and plays videos with its built-in mpv player, so every format plays as it is: HEVC, 10-bit, Dolby Vision, DTS and TrueHD sound, MKV.

<details>
<summary>Prefer not to install anything?</summary>
<br>

Download [`nathflix-portable-x64.exe`](https://github.com/lavagnou/nathflix-releases/releases/latest/download/nathflix-portable-x64.exe) instead: it runs straight away, without installing.
</details>

### On a Mac

1. Open the file you downloaded (`.dmg`) and drag **Nathflix** into **Applications**.
2. Open Nathflix from Applications. macOS will say it can't check the app (Nathflix is a free project without a paid Apple certificate). Click **Done**.
3. Open **System Settings → Privacy & Security**, scroll down to *"Nathflix" was blocked*, and click **Open Anyway**. Confirm with your password.
4. Nathflix opens. Sign in with your Stremio account.

You only need steps 2 and 3 once.

<details>
<summary>macOS says Nathflix "is damaged and can't be opened"?</summary>
<br>

That's macOS being extra careful with apps downloaded from the internet. Open *Terminal* (in Applications → Utilities), paste this, press Enter, and open Nathflix again:

```bash
xattr -dr com.apple.quarantine /Applications/Nathflix.app
```
</details>

### On Linux

1. Right-click the downloaded `nathflix-linux-x86_64.AppImage` → *Properties* → *Permissions*, and tick **Allow executing file as program** (or run `chmod +x nathflix-linux-x86_64.AppImage`).
2. Double-click it to open Nathflix, and sign in with your Stremio account.

<details>
<summary>It doesn't open?</summary>
<br>

Some distributions need *FUSE* for AppImages. On Ubuntu and Debian: `sudo apt install libfuse2`. On a Raspberry Pi or another ARM computer, download [`nathflix-linux-arm64.AppImage`](https://github.com/lavagnou/nathflix-releases/releases/latest/download/nathflix-linux-arm64.AppImage) instead.
</details>

### On a TV

Nathflix TV runs on Android TV, Google TV and Fire TV (Fire TV Sticks, Cubes and Fire TV televisions), and on TCL, Sony, Hisense and other TVs that run Google TV or Android TV. Everything works with the remote: the arrows move around, OK opens, Back goes back.

**1. Install Downloader.** On the TV, search for *Downloader* (by AFTVnews) in the Play Store or Amazon's Appstore, and install it.

**2. Let Downloader install apps.**
- Fire TV: *Settings → My Fire TV → Developer options → Install unknown apps* → turn **Downloader** on. (No *Developer options*? Go to *Settings → My Fire TV → About*, click your device's name 7 times, then go back.)
- Android TV and Google TV: Downloader asks for permission the first time you install something. Choose **Settings**, turn it on, and go back.

**3. Download Nathflix.** Open Downloader, select the address box and type:

```
github.com/lavagnou/nathflix-releases/releases/latest/download/nathflix-tv.apk
```

Select **Go**. When the download finishes, choose **Install**, then **Open**.

**4. Sign in** with your Stremio account. Nathflix is now in your TV's apps.

Good to know:

- Your watch progress is shared with every other Stremio app, so you can start something on the TV and finish it on your computer.

- Debrid streams and torrents both play straight away: Nathflix TV downloads torrents itself, so no computer or streaming server is needed. On a slow stick you can hand torrents to the Nathflix app (or Stremio) on a computer instead: keep it running on the same network, then on the TV open *Settings → Streaming server for torrents → Find*. If Windows asks whether to let Nathflix use private networks, allow it.

- Not supported: LG (webOS), Samsung (Tizen), Roku and Apple TV can't install Android apps. A cheap Google TV or Fire TV stick plugged into one of them works. The 2025 *Fire TV Stick 4K Select* runs Amazon's Vega OS instead of Fire OS and can't install Nathflix either.

- If Nathflix says the TV needs an update, update *Android System WebView* from the Play Store (on Fire TV: *Settings → My Fire TV → About → Check for Updates*).

### After installing

Nathflix keeps itself up to date. On Windows and Linux it downloads new versions in the background and offers to restart; on a Mac it tells you and you download the new version; on a TV it offers the update when it starts.

- **Already used Stremio Enhanced?** The first time the computer app opens, it offers to copy your sign-in, library, settings and plugins over. Stremio Enhanced itself isn't changed.

- **New to Stremio?** Nathflix shows films and series from your *catalog addons*, and plays them from your *stream addons*. On a new account it offers to add free catalogs for a full Home. For streams, open *Addons* and add one you like from the community list; many people use them with a debrid service such as [Real-Debrid](https://real-debrid.com/). What you watch and where it comes from is your responsibility, so please follow the laws where you live.

<br>

## Read this first

> [!IMPORTANT]
> Nathflix is a Stremio app: it uses your Stremio account and addons. It doesn't add any movies, shows or streams of its own, and it doesn't make anything play on its own.
>
> Titles play the way they do in Stremio. If nothing plays in your Stremio today, nothing will play in Nathflix either.

<br>

## Already using Stremio Enhanced? Use the plugin

You can add Nathflix to [Stremio Enhanced](https://github.com/REVENGE977/stremio-enhanced/releases) as a plugin instead of installing the app. You get the same Nathflix. The plugin is made and tested on Stremio Enhanced's latest full release, currently 1.2.0; preview and test builds (such as 1.3.0-preview) aren't supported and can break the player.

1. Run one command. On Windows, open *PowerShell* and paste:

   ```powershell
   irm https://raw.githubusercontent.com/lavagnou/nathflix-releases/main/install.ps1 | iex
   ```

   On macOS or Linux, open *Terminal* and paste:

   ```bash
   curl -fsSL https://raw.githubusercontent.com/lavagnou/nathflix-releases/main/install.sh | bash
   ```

2. Restart Stremio Enhanced.

3. Go to *Settings → Enhanced* and switch the Nathflix plugin on. The theme is built into the plugin, so that's all you need.

Updates are offered automatically inside Stremio Enhanced.

<details>
<summary>Prefer to install the plugin by hand?</summary>
<br>

1. Download [`nathflix.plugin.js`](https://raw.githubusercontent.com/lavagnou/nathflix-releases/main/nathflix.plugin.js) (your browser may open it as text: save the page as `nathflix.plugin.js`).
2. In Stremio Enhanced, go to *Settings → Enhanced*, open *Open Plugins Folder* and put the file there.
3. Restart and switch the plugin on.

The look is built into the plugin, so no theme file is needed. Applying any other theme switches the built-in one off.
</details>

<br>

## Source code and licence

Nathflix is free and open source under the [GNU GPL, version 3 or later](LICENSE). The complete source code of each version is attached to its release, as `nathflix-source-<version>.tar.gz` ([latest release](https://github.com/lavagnou/nathflix-releases/releases/latest)): you can use, study, change and share it, and anything you share that's based on it must keep the credit and publish its full source under the same licence. Nathflix is based on [dx.bi](https://github.com/notdxbi/dxbi-stremio), whose versions up to 2.15.9 were MIT. The "Nathflix" name and logo aren't part of the licence: please give forks their own name. Details, and the parts by others that keep their own licences, are in [NOTICE.md](NOTICE.md) and [LICENSE-ANIME4K](LICENSE-ANIME4K).

<br>

## Credits

- [dx.bi](https://github.com/notdxbi/dxbi-stremio) — the project Nathflix is based on (GPL-3.0-or-later): the plugin, the theme, the desktop app and the TV app all started there.
- [Stremio](https://www.stremio.com/) ([stremio-web](https://github.com/Stremio/stremio-web)) — the app underneath everything.
- [Stremio Enhanced](https://github.com/REVENGE977/stremio-enhanced) by REVENGE977 — the open-source desktop client the Nathflix app is built on (MIT, [app/LICENSE.md](app/LICENSE.md)), and the home of the Nathflix plugin.
- The plugin authors whose work showed what Stremio users want — TheIntroDB, Sul-404 (Addon Manager), Fxy and MrBlu03.
- [Anime4K](https://github.com/bloc97/Anime4K) by bloc97 — the shaders behind Picture enhancement, included unmodified under the MIT licence ([LICENSE-ANIME4K](LICENSE-ANIME4K)).
- Cinemeta and MetaHub for metadata and artwork; [Kitsu](https://kitsu.app) and [AniList](https://anilist.co) for anime scores; [TheIntroDB](https://theintrodb.org) and [AniSkip](https://aniskip.com) for skip times; [animefillerlist.com](https://www.animefillerlist.com) for the filler guide; [Wikidata](https://www.wikidata.org) (CC0) and [Wikipedia](https://en.wikipedia.org) (CC BY-SA) for review scores and critics' summaries; [MDBList](https://mdblist.com) for extra scores. Audience reviews come from [TMDB](https://www.themoviedb.org): this product uses the TMDB API but is not endorsed or certified by TMDB.
- Fonts: [Bebas Neue](https://github.com/dharmatype/Bebas-Neue) and [Inter](https://rsms.me/inter/) (SIL Open Font License).
- Country flags: [Twemoji](https://github.com/jdecked/twemoji) graphics (CC-BY 4.0) via the [Twemoji Country Flags](https://github.com/talkjs/country-flag-emoji-polyfill) font by TalkJS (MIT).
- Built with the help of [Claude Code](https://www.anthropic.com/claude-code).

<sub>Inspired by the Netflix interface; no Netflix logos, fonts, images or sounds are used. The intro and all sounds are original. Not affiliated with Netflix, Inc., Stremio, Stremio Enhanced, dx.bi or any plugin author.</sub>
