<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset=".github/assets/hero-dark.png">
    <img src=".github/assets/hero.png" alt="run.me.at landing page" width="880">
  </picture>
</p>

<h1 align="center">run.me.at</h1>

<p align="center"><strong>Toolchain benchmarks by me.</strong></p>

<p align="center">
  <img src="https://img.shields.io/badge/status-live-171717?style=flat-square" alt="Status: live">
  <img src="https://img.shields.io/badge/license-source--available-404040?style=flat-square" alt="License: source-available">
  <img src="https://img.shields.io/badge/part%20of-me.at-737373?style=flat-square" alt="Part of me.at">
</p>

<p align="center">
  <a href="https://run.me.at">Website</a> ·
  <a href="#features">Features</a> ·
  <a href="#how-it-works">How it works</a> ·
  <a href="#screenshots">Screenshots</a> ·
  <a href="#built-with">Built with</a>
</p>

Most benchmark charts give you one number with no machine, no versions and no way to check it. I built run.me.at as a first-party bench: I run the suites on hardware I own and disclose, then publish each number with the machine, the toolchain versions, the cache state and the command that produced it, so a run can be repeated rather than believed. The front page is the toolchain ladders: every TypeScript minor from 5.0 to 7.0, Node 18 to 26 (and Bun), and Next.js 13.5 to 16.4 with webpack and Turbopack, each timed on the same pinned public project with the raw hyperfine output beside every chart. It is not a leaderboard, nothing on it is vendor-attested, and nothing is for sale.

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset=".github/assets/overview-dark.svg">
    <img src=".github/assets/overview.svg" alt="run.me.at at a glance: every version in order, repeatable not believed, never merged, spread on the surface" width="880">
  </picture>
</p>

## Why run.me.at

| The usual benchmark chart | run.me.at |
| --- | --- |
| One number, no context | The machine, versions, cache state and command with every value |
| Different hardware mixed into one ranking | Results partitioned by hardware, cache state and toolchain |
| A single figure that hides the spread | Iteration count and spread next to every value |
| Run or sponsored by a vendor | First-party, on hardware I own, with nothing for sale |

## Features

- **Toolchain ladders**: TypeScript 5.0 to 7.0, Node 18 to 26 and Bun, and Next.js 13.5 to 16.4 with webpack and Turbopack, drawn in version order on one pinned project, with the raw hyperfine output published.
- **The bench index**: corpus counts plus every published measurement and comparison.
- **Methodology**: each honesty rule is paired with the function in the code that enforces it.
- **Machines and versions**: the hardware, environments and what a comparable run needs, treated as a fingerprint.
- **Partitioned results**: numbers from different hardware, cache states or toolchain versions are never merged into one ranking.
- **Spread on the surface**: every value carries its iteration count and spread next to the number, and single runs are labeled as such.
- **Publishing gates**: provenance, distribution and stored-value checks refuse a value before it can reach a page.
- **The fleet dashboard**: `/fleet` is the monorepo behind these apps measuring its own builds.
- **Open corpus**: `/corpus.json` exposes the whole corpus in the shapes the pages render from.

## How it works

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset=".github/assets/flow-dark.svg">
    <img src=".github/assets/flow.svg" alt="How run.me.at works: pin, time, gate, publish" width="880">
  </picture>
</p>

Every rung of a ladder does the same job on the same pinned public project, so the only thing that changes is the version. hyperfine times each version on one disclosed machine, and the run is recorded with its machine fingerprint, versions, cache state and command. Publishing gates check provenance, distribution and stored values before anything reaches a page, which renders the charts, the raw output and the open corpus.

## Screenshots

<table>
  <tr>
    <td width="50%"><picture><source media="(prefers-color-scheme: dark)" srcset=".github/assets/methodology-dark.png"><img src=".github/assets/methodology.png" alt="Methodology"></picture><br><sub>Methodology: each promise and the code that enforces it.</sub></td>
    <td width="50%"><picture><source media="(prefers-color-scheme: dark)" srcset=".github/assets/machines-dark.png"><img src=".github/assets/machines.png" alt="Machines and versions"></picture><br><sub>Machines and versions: what a comparable run needs.</sub></td>
  </tr>
  <tr>
    <td width="50%"><picture><source media="(prefers-color-scheme: dark)" srcset=".github/assets/fleet-dark.png"><img src=".github/assets/fleet.png" alt="Fleet dashboard"></picture><br><sub>Fleet: the monorepo measuring its own builds.</sub></td>
  </tr>
</table>

## Built with

<p>
  <img src="https://img.shields.io/badge/Next.js-16-000000?style=flat-square&logo=nextdotjs&logoColor=white" alt="Next.js 16">
  <img src="https://img.shields.io/badge/React-19-171717?style=flat-square&logo=react&logoColor=white" alt="React 19">
  <img src="https://img.shields.io/badge/TypeScript-5-262626?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript">
  <img src="https://img.shields.io/badge/Tailwind%20CSS-4-404040?style=flat-square&logo=tailwindcss&logoColor=white" alt="Tailwind CSS 4">
</p>

- Next.js 16 (App Router) and React 19
- TypeScript
- Tailwind CSS 4
- hyperfine for the toolchain ladders
- A typed benchmark corpus committed alongside the code, also served as `/corpus.json`

## Part of the me.at family

run.me.at is one of my [`*.me.at`](https://me.at) apps. They share one design system, account, and app shell. Development happens in a private monorepo; this repository is the project's public-facing home.

## License

Source-available. See [LICENSE](LICENSE).
