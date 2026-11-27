<div align="center">

<a href="https://doimus.com/"><img src="https://doimus.com/logo.png" alt="Doimus" width="100%"></a>

<h3>Your home, your rules.</h3>

<p>
  A local-first smart home platform that runs on a Raspberry&nbsp;Pi or Orange&nbsp;Pi in your house.
  Your devices talk to your hub, there is no subscription, and your data stays home.
</p>

<p>
  <a href="https://doimus.com/"><b>▶&nbsp; Get started</b></a>
  &nbsp;·&nbsp;
  <a href="https://doimus.com/getting-started"><b>Setup guide</b></a>
  &nbsp;·&nbsp;
  <a href="https://github.com/doimushome/doimus-core"><b>Source code</b></a>
  &nbsp;·&nbsp;
  <a href="https://github.com/doimushome/doimus-core/releases"><b>Releases</b></a>
</p>

<p>
  <a href="https://img.shields.io/github/stars/doimushome/doimus-core?style=flat&label=stars&color=F5F7FA&labelColor=08090D&logo=github&logoColor=white"><img alt="GitHub stars" src="https://img.shields.io/github/stars/doimushome/doimus-core?style=flat&label=stars&color=F5F7FA&labelColor=08090D&logo=github&logoColor=white"></a>
  <a href="https://img.shields.io/badge/license-Apache_2.0-blue.svg"><img alt="License: Apache-2.0" src="https://img.shields.io/badge/license-Apache_2.0-blue.svg"></a>
</p>

</div>

<img src="https://doimus.com/mascot/mascot_happy.png" alt="Doimus mascot" width="360">

**Doimus** is a local-first smart home platform. The hub is one Go binary with a SQLite file for state; the app (iOS and Android, one Kotlin codebase) talks to it directly over your LAN. No cloud account, no subscription, no telemetry — the optional push-notification relay (`push.doimus.com`) is off by default, and the built-in AI downloads its model once from Hugging Face with prompts and device data staying on the hub.

<table>
  <tr>
    <td align="center" valign="top" width="25%"><h1>45</h1><b>plugins</b><br><sub>in the public registry</sub></td>
    <td align="center" valign="top" width="25%"><h1>1</h1><b>hub</b><br><sub>Go + SQLite on your own hardware</sub></td>
    <td align="center" valign="top" width="25%"><h1>0</h1><b>accounts</b><br><sub>to create, subscribe or pay</sub></td>
    <td align="center" valign="top" width="25%"><h1>2</h1><b>platforms</b><br><sub>iOS + Android from one codebase</sub></td>
  </tr>
</table>

## What you can do

<table>
  <tr>
    <td width="50%" valign="top">
      <b>Feel your home.</b> Lights, plugs, thermostats, locks, cameras and sensors are driven by the hub over your own network. The hub itself never calls a vendor cloud, and whichever plugins talk to a cloud do it on their own terms.
    </td>
    <td width="50%" valign="top">
      <b>Automate on the hub.</b> Triggers, conditions and actions run on the hub itself — nested AND/OR logic, per-action delays and an ELSE branch, with a dry run before anything touches a real device. State moves over WebSocket, so a tap reaches the device fast.
    </td>
  </tr>
  <tr>
    <td valign="top">
      <b>Ask the local AI.</b> The built-in assistant runs on the hub on a model it downloads once from Hugging Face. Prompts and device data stay on the hub, behind the same sensitive-control and device-type gates the rest of the platform runs with.
    </td>
    <td valign="top">
      <b>Get told what changed.</b> Optional push notifications through the relay; a privacy-mode camera suppresses motion alerts, and battery cameras carry a cooldown so a sleeping doorbell does not wake the world for one motion event.
    </td>
  </tr>
</table>

## How it works

Your phone talks to your hub. Your hub talks to your things. Nobody else is in the room.

1. **Mobile app** — iOS and Android from one Kotlin codebase. Talks straight to the hub.
2. **Doimus hub** — Go + SQLite on a Raspberry&nbsp;Pi or Orange&nbsp;Pi, listening on `:8765`. Each integration runs in its own sandboxed process.
3. **Your devices** — Wi-Fi, Bluetooth LE, Zigbee, Z-Wave. The gear you already own.

A vendor cloud is not on this path. A light still turns on when your broadband is down.

## Where it runs

| Where | How |
| :-- | :-- |
| **Your LAN** | Raspberry&nbsp;Pi 3B+/4/5 or Orange&nbsp;Pi Zero&nbsp;2W/3&nbsp;LTS, flashed with the ready-to-run `.img.zst` — flash the whole card, power on, hand over Wi-Fi over the app. |
| **Away from home** | Over a WireGuard VPN into your own network. Remote control goes straight to your hub — there is no cloud in the middle. |

## Repositories

| Repository | What's in it |
| :-- | :-- |
| [**doimus-core**](https://github.com/doimushome/doimus-core) | The hub, its plugin sandbox, the IoT image builder and the docs. |
| [**doimus-mobile**](https://github.com/doimushome/doimus-mobile) | The iOS and Android app. |
| [**doimus-plugins**](https://github.com/doimushome/doimus-plugins) | The plugin registry and catalogue. |
| [**doimus-website**](https://github.com/doimushome/doimus-website) | The landing page and documentation site. |
| [**.github**](https://github.com/doimushome/.github) | This page. |

## Get involved

- **Found a bug?** [Open an issue](https://github.com/doimushome/doimus-core/issues).
- **Have an idea?** Start a [discussion](https://github.com/doimushome/doimus-core/discussions).
- **Write a plugin?** The [plugin authoring skill](https://github.com/doimushome/doimus-skill) walks through adding a device to the hub.
- **Found a security problem?** Please [report it privately](https://github.com/doimushome/doimus-core/security/advisories/new).

## Support and licence

Doimus is free. If you'd like to help with hosting, you can [buy me a coffee](https://buymeacoffee.com/alpyalayg); it never unlocks anything.

The code is released under the [Apache License 2.0](https://github.com/doimushome/doimus-core/blob/main/LICENSE.md). The Doimus name and logo are trademarks and are not licensed under this license.

<br>

<div align="center">
<sub>
Made by Matteo Crippa · <a href="https://www.youtube.com/@KhazAlp">YouTube</a> · <a href="https://x.com/alpyalay">X</a>
<br>
Doimus is an independent open-source project. It isn't affiliated with any vendor whose devices it talks to.
</sub>
</div>
