<p align="center">
  <img src="assets/banner-en.png" alt="osu! AI Analyzer, your personal osu! coach" width="100%">
</p>

<p align="center">
  <a href="https://github.com/justafailure1/osu-ai-analyzer/releases/latest"><img src="https://img.shields.io/github/v/release/justafailure1/osu-ai-analyzer?label=version&color=ff66aa&style=for-the-badge" alt="Version"></a>
  <img src="https://img.shields.io/badge/Windows-10%20%7C%2011-7c4dff?style=for-the-badge&logo=windows&logoColor=white" alt="Windows 10 and 11">
  <img src="https://img.shields.io/badge/osu!-stable-ff66aa?style=for-the-badge" alt="osu! stable">
  <img src="https://img.shields.io/badge/status-closed%20beta-e2489f?style=for-the-badge" alt="Closed beta">
</p>

<p align="center">
  <a href="README.md">Español</a> · <b>English</b>
</p>

---

**osu! AI Analyzer** has an AI that learns **only from your own plays**, note by note. Before you play a map, it tells you how many misses it expects from you and where. After you play it, it shows where you missed more or less than expected and why. From that it picks what to train and which maps to train it on.

<p align="center">
  <img src="assets/live.png" alt="Live: what your AI expects from you on the selected map" width="92%">
</p>

## What it does

### Your AI before you play
When you select a map in osu!, the app tells you how many misses your AI expects, at which seconds of the map, and why (the jump, the rhythm, the stream, fatigue...). It also tells you whether the map is comfortable for you, at your limit, or well above what you usually finish.

### Every play, against what was expected from you
**Plays** lists every map you played, fails included, with:
- expected vs actual, note by note;
- the replay inside the app, with the cursor, the keys and the misses marked;
- the misses nobody expected (focus or fatigue);
- where you click on jumps: whether you fall short or overshoot, and your timing.

<p align="center">
  <img src="assets/replay.png" alt="Replay viewer" width="80%">
</p>

### Your skills, measured by your own AI
Stream speed, stamina, jump speed and reach, and accuracy (UR), measured on test patterns in your usual form and with your usual settings. You also see your progress per skill, week by week.

<p align="center">
  <img src="assets/skills.png" alt="Skills" width="80%">
</p>

### What to train today
The app picks the skill you struggle with most (or you choose among 10: jumps, flow aim, streams, stamina, speed, tech, sliders, reading, small circles and accuracy) and suggests:
- **maps from your folder** that teach you the most of that skill per minute and that you can finish, for the mods you pick (NM, HD, HR, DT...); one click opens them in osu!;
- **a map made for you**, with the pattern that is hardest for you and the difficulty rising up to your limit.

<p align="center">
  <img src="assets/train.png" alt="Train" width="80%">
</p>

### Stream overlays
Besides tosu's own overlays, the app adds its own to the tosu dashboard, each with its link for OBS: map and time, PP, keys, 100/50/miss, combo and accuracy, hit error bar with UR, and what your AI expects on the map.

<p align="center">
  <img src="assets/ov-full.png" alt="Full overlay" width="46%">
  <img src="assets/ov-map.png" alt="Map overlay" width="40%">
</p>

### And also
- 13 languages: Spanish, English, Portuguese, French, German, Russian, Polish, Turkish, Indonesian, Japanese, Korean and Chinese (Simplified and Traditional).
- Global and country leaderboard of the selected map, with live PP.
- Updates itself when a new version is out.

## Light while you play
The heavy work (reading replays, training the AI, scoring your folder) **pauses while you play** a map, runs at low priority and uses at most 2 cores. At rest it barely uses any CPU.

## Privacy
- Your replays and your data **stay on your PC**. The AI is trained on your own computer, only with your plays.
- The app **doesn't modify osu!** or play for you: it reads the game's data with [tosu](https://github.com/tosuapp/tosu) (the same reader stream overlays use) and the replays osu! already saves.
- It only goes online to get leaderboards and maps from the osu! API, to check your license and to look for updates.

## Install

> **Closed beta:** the app needs a license tied to your osu! account. If you want to try it, message **[Kenzo R on osu!](https://osu.ppy.sh/users/10338561)**.

1. Download **`osu-AI-Analyzer-Setup-x.y.z.exe`** from [**Releases**](https://github.com/justafailure1/osu-ai-analyzer/releases/latest).
2. Open it. Windows may show *"Windows protected your PC"* because the installer isn't signed: click **More info**, then **Run anyway**.
3. Paste your license when the app asks for it.
4. Open osu! with the license's account. The first time, the app reads your saved replays and trains your AI (about 2 minutes).

**Requirements:** Windows 10 or 11 (64-bit), osu! stable and 1 GB of free space.

## FAQ

<details>
<summary><b>Does it work with osu!lazer?</b></summary>
It's made for osu! stable. osu!lazer support is being tested.
</details>

<details>
<summary><b>How long until the AI knows me?</b></summary>
The replays you already have in osu! count from day one: with about 200 plays it trains in a couple of minutes. After that it retrains by itself every 10 plays.
</details>

<details>
<summary><b>What about fails? osu! doesn't save replays of them.</b></summary>
The app records your attempts while you play: fails, retries and maps you leave halfway also count for your AI, and you can watch the replay of every fail.
</details>

<details>
<summary><b>Why can't I see my country leaderboard?</b></summary>
osu! only gives country leaderboards to accounts with osu!supporter.
</details>

<details>
<summary><b>Do I lose my data if I reinstall or update?</b></summary>
No. Uninstalling or updating keeps your plays, your AI and your license.
</details>

---

<p align="center">
  <img src="assets/logo.png" width="56" alt=""><br>
  <sub>osu! AI Analyzer is not affiliated with osu! or ppy Pty Ltd. · Proprietary software, all rights reserved.<br>
  Uses third-party components under their own licenses (including tosu and lazer-calculator, LGPL-3.0); details are in the <code>licencias</code> folder of the installation.</sub>
</p>
