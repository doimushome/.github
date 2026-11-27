<div align="center">

<a href="https://doimus.com/"><img src="https://doimus.com/logo.png" alt="Doimus" width="320"></a>

<h3>Your home, your rules.</h3>

<p>
  A local-first smart home platform that runs on a Raspberry&nbsp;Pi or Orange&nbsp;Pi in your house.
  Your devices talk to your hub, there is no subscription, and your data stays home.
</p>

<p>
  <a href="https://doimus.com/"><b>Website</b></a>
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

<img src="https://doimus.com/mascot/mascot_happy.png" alt="Doimus mascot" width="140">

**Doimus** is a local-first smart home platform. The hub is one Go binary with a SQLite file for state; the app talks to it directly over your LAN. No cloud account, no subscription, no telemetry.

## How it works

1. **Mobile app** — iOS and Android, talks straight to the hub.
2. **Doimus hub** — Go + SQLite on a Raspberry&nbsp;Pi or Orange&nbsp;Pi, listening on `:8765`. Each integration runs in its own sandboxed process.
3. **Your devices** — Wi-Fi, Bluetooth LE, Zigbee, Z-Wave.

A vendor cloud is not on this path. A light still turns on when your broadband is down.

## Get involved

- **Found a bug?** [Open an issue](https://github.com/doimushome/doimus-core/issues).
- **Have an idea?** Start a [discussion](https://github.com/doimushome/doimus-core/discussions).
- **Write a plugin?** The [plugin authoring skill](https://github.com/doimushome/doimus-skill) walks through adding a device to the hub.
- **Found a security problem?** Please [report it privately](https://github.com/doimushome/doimus-core/security/advisories/new).

