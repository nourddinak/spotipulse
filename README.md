# 🎵 SpotiPulse

<p align="center">
  <a href="https://spotify.openapisfree.dpdns.org/">
    <img src="https://img.shields.io/badge/Live%20App-spotify.openapisfree.dpdns.org-1DB954?style=for-the-badge&logo=spotify&logoColor=white" alt="Live Web App" />
  </a>
  <img src="https://img.shields.io/badge/Live%20Spotify%20Broadcast-1DB954?style=for-the-badge&logo=spotify&logoColor=white" alt="Live Spotify Broadcast" />
  <img src="https://img.shields.io/badge/Karaoke%20Lyrics-Real--Time-25c2a0?style=for-the-badge" alt="Karaoke Lyrics" />
  <img src="https://img.shields.io/badge/Zero%20Code%20Setup-000000?style=for-the-badge" alt="Zero Code Setup" />
  <img src="https://img.shields.io/badge/License-MIT-green?style=for-the-badge" alt="MIT License" />
</p>

> **Turn your Spotify listening activity into a living, real-time digital identity.** Broadcast your currently playing tracks, animated vinyl visuals, and synchronized karaoke lyrics across personal portfolios, GitHub READMEs, Twitch/YouTube streams, and Discord bots with zero developer friction.

---

## ⚡ The 10-Second Elevator Pitch

Imagine you are listening to music on your headphones. Anywhere in the world—on your personal website, your GitHub profile, your Twitch stream, or your digital resume—people can see what track you are playing right now, watch the vinyl record spin, and read the **synchronized karaoke lyrics** as the song plays in real time.

**SpotiPulse** is an ultra-fast, live music bridge. It takes whatever you play on Spotify and transforms it into interactive glassmorphic cards, stream overlays, dynamic SVG badges, and high-speed JSON/WebSocket streams—all without requiring visitors to log in and without making you write a single line of code.

---

## 🛑 The Problem SpotiPulse Solves

If an ordinary person, creator, or developer tries to display their live Spotify playback on the web, they immediately run into a massive technical and financial barrier:

```
❌ The Traditional Way (Painful & Blocked):
You ➔ Apply for Spotify Developer Portal ➔ Must Pay for Spotify Premium ➔ 
Write Server Code ➔ Handle Expiring Access Tokens Hourly ➔ 
Manually Whitelist Friends' Emails (25-user cap) ➔ No Lyrics Available

✅ The SpotiPulse Way (Instant & Frictionless):
You ➔ Click "Connect Spotify" ➔ Copy 1 Universal Link ➔ Live Everywhere in Real Time!
```

### The March 2026 Spotify Developer Barrier

In **March 2026**, Spotify introduced strict developer policy changes that locked most personal projects and hobbyist creators out of the official API:

1. **Mandatory Spotify Premium for Developers**: Spotify now strictly requires that the creator of any application in "Development Mode" on the Spotify Developer Portal **must have an active, paid Spotify Premium subscription**. If a developer's subscription lapses or they use a free account, their API tokens and widgets immediately stop working.
2. **Playback Endpoint Lockdown (`403 PREMIUM_REQUIRED`)**: Endpoints that query or read currently playing tracks (`GET /v1/me/player/currently-playing`) throw `403 Forbidden: PREMIUM_REQUIRED` if accessed without an active Premium subscription.
3. **The 25-User Development Mode Trap**: By default, custom Spotify developer apps are trapped in sandbox mode, requiring you to manually whitelist every single visitor or friend by their Spotify email address (maximum 25 accounts). Expanding this quota requires commercial business verification that Spotify routinely denies for personal portfolios.
4. **Zero Public Lyrics Support**: Even developers who pay for Premium and configure an official app cannot display synchronized lyrics because **Spotify does not provide a public lyrics API**.

### How SpotiPulse Fixes This
* **Zero Developer Setup**: No developer portal registration, no client secrets, and no OAuth redirect configurations.
* **1-Click Authentication**: Users authenticate once via standard Spotify OAuth. SpotiPulse acts as the secure, multi-tenant proxy.
* **Persistent Token Management**: Background token refresh engines ensure your widgets never disconnect or expire.
* **Automated Synchronized Lyrics**: Real-time karaoke lyrics parsed and cached with zero configuration.

---

## 🌟 Core Features

| Feature | What It Is | How It Works |
| :--- | :--- | :--- |
| **Interactive Live Card**<br>`/embed/{username}` | A glassmorphic now-playing player card for portfolios and websites. | Displays dynamic album art, spinning vinyl animations, live seek/progress bars, real-time equalizer bars, and direct deep links to open the track in Spotify. |
| **Synchronized Live Lyrics** | Line-by-line karaoke lyrics that scroll in real time with the music. | Cleans track titles automatically, matches exact audio duration, parses timecoded LRC files, and highlights each line on screen as the artist sings. |
| **OBS Streaming Overlay**<br>`/overlay/{username}` | A clean, transparent browser source overlay for streamers. | Drops into OBS, Streamlabs, or Prism Studio with a transparent background. Smoothly animates in when a song changes, then docks neatly so it never obstructs gameplay. |
| **Dynamic GitHub SVG Badge**<br>`/badge/{username}` | Animated vector badge for GitHub profile READMEs and markdown docs. | Generates an animated SVG with pulsing status dots, track metadata, and real-time audio wave bars that renders instantly on GitHub without JavaScript. |
| **Real-Time WebSocket Engine** | Instant, zero-polling live updates. | Whenever you press skip, pause, or play on your phone or desktop, the change propagates to all connected embeds in sub-second latency via open WebSocket pipes. |
| **Creator Telemetry Dashboard** | A personal analytics hub for tracking visibility. | Live metrics for total embed views, unique visitors, API requests, top played songs, and hourly telemetry charts with built-in preview deduplication. |
| **Privacy & Safety Shield** | Granular privacy settings to protect your listening activity. | One-click toggles to hide album art, blur track names, filter out explicit content, or toggle your profile from Public to Private. |
| **Developer API & WebSockets**<br>`/api/v1/now-playing/{username}` | Clean REST endpoints and live WebSocket feeds for developers. | Connect custom Discord bots, desktop widgets, Raspberry Pi smart clocks, or CLI status bars to your live music stream with standard JSON payloads. |

---

## 🌐 Live Web Application

SpotiPulse is live and fully hosted as a cloud web application:

👉 **[SpotiPulse - Real-Time Spotify Telemetry & Embed Infrastructure](https://spotify.openapisfree.dpdns.org/)**

### Instant 1-Click Setup (Zero Coding Required)

1. **Sign Up & Log In**: Visit [spotify.openapisfree.dpdns.org](https://spotify.openapisfree.dpdns.org/) and create your free account.
2. **Connect Spotify**: Click **"Connect Spotify"** to securely authorize your listening activity via official Spotify OAuth.
3. **Copy Your Links**: Your dashboard instantly generates your personalized **Interactive Embed Player**, **OBS Streaming Overlay**, and **GitHub Animated Badge**.
4. **Broadcast Everywhere**: Drop the link into your website, stream, or GitHub profile. Whenever you put on your headphones, your listeners will see your live track updates and can follow along with synchronized karaoke lyrics in real time!

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.
