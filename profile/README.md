<p align="center">
  <a href="https://openmasjidsolutions.org">
    <img src="https://avatars.githubusercontent.com/u/296720769?s=200&v=4" width="120" alt="OpenMasjid Solutions">
  </a>
</p>

<h1 align="center">OpenMasjid Solutions</h1>

<p align="center">
  <strong>Your masjid's software. Free, forever.</strong><br>
  Prayer displays, donations, a giving kiosk and a madrasa fee desk — running on one computer at the masjid.
</p>

<p align="center">
  <a href="https://openmasjidsolutions.org"><img src="https://img.shields.io/badge/Website-openmasjidsolutions.org-blue?style=flat-square" alt="Website"></a>
  <a href="https://discord.gg/MpPDbyQfaF"><img src="https://img.shields.io/badge/Discord-Join-blue?style=flat-square&logo=discord" alt="Discord"></a>
  <a href="https://github.com/OpenMasjid-Solutions/OpenMasjidOS/blob/master/LICENSE"><img src="https://img.shields.io/badge/License-AGPL--3.0-blue?style=flat-square" alt="AGPL-3.0"></a>
</p>

---

Every masjid ends up paying somebody a monthly fee for a prayer screen, a donation page and a card
reader — and the donor records live in that somebody's cloud. We think that's backwards. So we build
the same software and give it away: **no tiers, no licence per screen, no card on file, nothing held
back in a paid version.** It runs on hardware the masjid already owns, and the data never leaves the
building, because there is no server of ours for it to leave to.

Install the platform with one command:

```bash
bash -c "$(curl -fsSL https://raw.githubusercontent.com/OpenMasjid-Solutions/OpenMasjidOS/master/install.sh || wget -qO- https://raw.githubusercontent.com/OpenMasjid-Solutions/OpenMasjidOS/master/install.sh)"
```

Then open `http://<your-server-ip>` on the same network and create your admin account. Everything
else installs from the App Store inside the dashboard, with one click.

## The same donation, two routes

| Through somebody else's cloud | Straight through your own machine |
| --- | --- |
| Donor taps a card | Donor taps a card |
| The supplier's cloud | Your computer, in the masjid |
| **Their monthly fee** — busy month or quiet one | **Your own Stripe account** |
| The gift, less the processor's fee | **No monthly fee, in any month** |
| | The gift, less the processor's fee |
| Donor records live in their system. If you leave, you ask for them back. | Donor records stay on your machine. There is no middle to leave. |

## One platform, and the apps that run on it

**OpenMasjidOS** is the base. Everything else is an app you install onto it from the App Store — its
own repo, its own Docker container, its own data. Updating the platform never touches your apps.

| Repository | What it is |
| --- | --- |
| **[OpenMasjidOS](https://github.com/OpenMasjid-Solutions/OpenMasjidOS)** | The platform. One-line install, a login-protected dashboard with live system status, a one-click App Store, file manager, terminals and backups. Think umbrelOS, built for masjids. |
| **[OpenMasjidAPPS](https://github.com/OpenMasjid-Solutions/OpenMasjidAPPS)** | The app catalog OpenMasjidOS reads to populate the App Store. Start here if you want to build an app or list one. |
| **[OpenMasjidDisplay](https://github.com/OpenMasjid-Solutions/OpenMasjidDisplay)** | Every TV in the masjid, driven from one small computer over RTSP — prayer timetables designed in a live editor, IP and imam cameras, HDMI sources, schedules, and a PIN-protected page so a volunteer can switch a screen from their phone. |
| **[OpenMasjidDonations](https://github.com/OpenMasjid-Solutions/OpenMasjidDonations)** | Your own branded donation website on your own Stripe account. Campaigns with clean links, one-time or monthly giving, QR codes, a full ledger with CSV export, and an optional Cloudflare Tunnel for public access. |
| **[OpenMasjidKiosk](https://github.com/OpenMasjid-Solutions/OpenMasjidKiosk)** | A wall-mounted Android tablet and a Stripe Reader M2 become a tap-to-give station at the door. Pair a tablet with a 6-digit code; it locks into full screen and only a PIN gets out. |
| **[OpenMasjidStudents](https://github.com/OpenMasjid-Solutions/OpenMasjidStudents)** | The madrasa's tuition desk. Households, fee plans, invoicing and an append-only ledger, with a phone-first parent portal, saved cards and autopay — and a Student ID that lets a parent pay at the kiosk or on the donation site without an account. |

Browse the whole catalog at **[openmasjidsolutions.org/apps](https://openmasjidsolutions.org/apps)**.

## Why it's different

- **Free, forever.** Every masjid gets every part of it. There is no upsell, because there is nothing to sell.
- **Open source.** [AGPL-3.0](https://github.com/OpenMasjid-Solutions/OpenMasjidOS/blob/master/LICENSE) — anyone can read the code and improve it, and those improvements come back to every masjid.
- **Your hardware, your data.** A Raspberry Pi, a mini-PC or a Proxmox container at the masjid. Nothing is uploaded to us.
- **One-click App Store.** Browse the catalog from the dashboard, install, and the app asks for what it needs.

## Getting started

**Running a masjid?** Start at **[openmasjidsolutions.org/get-started](https://openmasjidsolutions.org/get-started)** — it walks through the hardware, the install and the first app. The
[docs](https://openmasjidsolutions.org/docs) cover the rest, and there's [help](https://openmasjidsolutions.org/help) if you get stuck.

**Building on it?** Every repo is a TypeScript monorepo that runs as one Docker container. Start with
[OpenMasjidAPPS](https://github.com/OpenMasjid-Solutions/OpenMasjidAPPS) (`docs/BUILDING_AN_APP.md`) for the app contract, and
[`docs/APP_MANIFEST_SPEC.md`](https://github.com/OpenMasjid-Solutions/OpenMasjidOS/blob/master/docs/APP_MANIFEST_SPEC.md) for the platform side.

## Come and build it with us

Volunteers, imams and developers are in the [**Discord**](https://discord.gg/MpPDbyQfaF) every day — asking questions, testing releases,
and deciding what gets built next. Come and say salaam.

You don't have to write code to help. Testing a release in a real masjid, writing docs, translating
the interface, or telling us what your committee actually needs are all worth a great deal. See
[how to help](https://openmasjidsolutions.org/community) and the
[contributing guide](https://github.com/OpenMasjid-Solutions/OpenMasjidOS/blob/master/CONTRIBUTING.md).

Contributions are made under AGPL-3.0 plus a [Contributor License Agreement](https://github.com/OpenMasjid-Solutions/OpenMasjidOS/blob/master/CLA.md), signed automatically on
your first pull request. It lets the project offer commercial licenses to organisations that can't
accept AGPL — the public tree always stays AGPL-3.0.

## Who builds and funds this

Created by **Hasan Ismail**, with immense help from **Qari Ijaz** and **Osman Sayed**.

<div align="center">
  <table>
    <tr>
      <td align="center">
        <a href="https://github.com/hasan-ismail">
          <img src="https://github.com/hasan-ismail.png?size=100" width="100px;" alt="Hasan Ismail"/><br />
          <sub><b>Hasan Ismail</b></sub>
        </a>
      </td>
      <td align="center">
        <a href="https://github.com/ijazshare">
          <img src="https://github.com/ijazshare.png?size=100" width="100px;" alt="Qari Ijaz"/><br />
          <sub><b>Qari Ijaz</b></sub>
        </a>
      </td>
      <td align="center">
        <a href="https://github.com/osayed0001">
          <img src="https://github.com/osayed0001.png?size=100" width="100px;" alt="Osman Sayed"/><br />
          <sub><b>Osman Sayed</b></sub>
        </a>
      </td>
    </tr>
  </table>
</div>

Resources for this project were generously sponsored by **[An-Noor Institute](https://www.annoorusa.org/)**, **[Rihlatul Ilm Foundation](https://rifusa.org/)**, and **[AsmaTec Inc.](https://asmatec.com/)**.

<div align="center">
  <table>
    <tr>
      <td align="center">
        <a href="https://www.annoorusa.org/">
          <img src="https://raw.githubusercontent.com/OpenMasjid-Solutions/OpenMasjidOS/master/assets/An-noor2.png" width="120px;" alt="An-Noor Institute"/><br />
          <sub><b>An-Noor Institute</b></sub>
        </a>
      </td>
      <td align="center">
        <a href="https://rifusa.org/">
          <img src="https://raw.githubusercontent.com/OpenMasjid-Solutions/OpenMasjidOS/master/assets/RIFbetter.png" width="120px;" alt="Rihlatul Ilm Foundation"/><br />
          <sub><b>Rihlatul Ilm Foundation</b></sub>
        </a>
      </td>
      <td align="center">
        <a href="https://asmatec.com/">
          <img src="https://raw.githubusercontent.com/OpenMasjid-Solutions/OpenMasjidOS/master/assets/Asmatec.png" width="120px;" alt="AsmaTec Inc."/><br />
          <sub><b>AsmaTec Inc.</b></sub>
        </a>
      </td>
    </tr>
  </table>
</div>

*May Allah reward everyone who made it possible.*

---
<p align="center">
  <a href="https://openmasjidsolutions.org">Website</a> ·
  <a href="https://discord.gg/MpPDbyQfaF">Discord</a> ·
  <a href="https://openmasjidsolutions.org/docs">Docs</a> ·
  <a href="https://openmasjidsolutions.org/support-us">Support us</a>
</p>

<p align="center"><sub>Free, forever, for every masjid. · The software is <a href="https://github.com/OpenMasjid-Solutions/OpenMasjidOS/blob/master/LICENSE">AGPL-3.0</a></sub></p>
