<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/0xDarkSeidBull/daotask16/main/dao-logo-on-dark.png">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/0xDarkSeidBull/daotask16/main/dao-logo-on-light.png">
  <img alt="Redbelly DAO" src="https://raw.githubusercontent.com/0xDarkSeidBull/daotask16/main/dao-logo-on-dark.png" width="220">
</picture>

# Unstick Your RBNT
### A Cross Chain Recovery Playbook

[![Read PDF](https://img.shields.io/badge/Read-PDF-EF5350?style=for-the-badge&logo=adobeacrobatreader&logoColor=white)](https://github.com/0xDarkSeidBull/daotask16/blob/main/rbnt_recovery.pdf)
[![Read Docs](https://img.shields.io/badge/Read-Docs-2B579A?style=for-the-badge&logo=microsoftword&logoColor=white)](https://github.com/0xDarkSeidBull/daotask16/blob/main/rbnt_recovery.docx)
[![Live Site](https://img.shields.io/badge/Live-daotask16.test--hub.xyz-10B981?style=for-the-badge&logo=vercel&logoColor=white)](https://daotask16.test-hub.xyz)
[![View Evidence](https://img.shields.io/badge/View-Evidence-1F2937?style=for-the-badge&logo=github&logoColor=white)](https://github.com/0xDarkSeidBull/daotask16/tree/main/evidence)

A community support guide for the four most common ways RBNT gets stuck: wrong network CEX deposits, wrapped RBNT showing zero value, quote unavailable errors bridging back to Redbelly Network, and stranded stablecoin transfers.

![Verified](https://img.shields.io/badge/Verified-August%202026-EF5350?style=flat-square)
![Checked against](https://img.shields.io/badge/Checked%20against-Lucid%20Labs%20%2B%20Oku-1F2937?style=flat-square)
![Sources](https://img.shields.io/badge/Sources-Cited%20inline-1F2937?style=flat-square)

</div>

<br>

---

## Verified live, not just documented

Every number in this guide, contract addresses, pool liquidity, price impact, bridge fees and timing, was checked live in August 2026, cross-checked across two independent bridge interfaces where possible. Where something could not be verified, that is stated directly rather than filled in with a guess.

<p align="center">
<img src="https://raw.githubusercontent.com/0xDarkSeidBull/daotask16/main/evidence/connect%20wallet.jpg" width="700" alt="Lucid Labs Bridge before connecting a wallet">
<br>
<i>Lucid Labs Bridge before connecting a wallet. Total Bridged Value $149.7M and 112,152 transactions confirm this is a live, active bridge, checked directly rather than assumed from documentation.</i>
</p>

<p align="center">
<img src="https://raw.githubusercontent.com/0xDarkSeidBull/daotask16/main/evidence2/wallet_connect.png" width="700" alt="Oku wallet connect screen showing oku.trade in the browser URL bar">
<br>
<i>Oku (oku.trade), the second bridge interface used to cross check every fee and time in this guide. The browser URL bar confirms this is the real site, not a lookalike.</i>
</p>

<p align="center">
<img src="https://raw.githubusercontent.com/0xDarkSeidBull/daotask16/main/evidence/solana%20to%20redbelly.png" width="700" alt="Solana selected as source chain, Recommended Bridge shows no route found">
<br>
<i>Solana selected as the source chain on Lucid Labs Bridge. Recommended Bridge shows "No route found for selected parameters", this is expected behaviour, not a bug, see Failure Mode 2 for the two hop route that actually works.</i>
</p>

<p align="center">
<img src="https://raw.githubusercontent.com/0xDarkSeidBull/daotask16/main/evidence/appie.jpg" width="700" alt="Redbelly team confirming in Discord that RBNT on BSC is fake">
<br>
<i>Redbelly's own team, in their official Discord support channel: "We never had rbnt on bsc. All RBNT on bsc is fake." This is the source behind the BNB Chain warning in Table A below.</i>
</p>

<p align="center"><i>Full screenshot sets: <a href="https://github.com/0xDarkSeidBull/daotask16/tree/main/evidence">Lucid Labs Bridge (14 screenshots)</a> &middot; <a href="https://github.com/0xDarkSeidBull/daotask16/tree/main/evidence2">Oku (9 screenshots)</a></i></p>

---

## What is in this repo

| File | What it is |
|---|---|
| [`rbnt_recovery.pdf`](https://github.com/0xDarkSeidBull/daotask16/blob/main/rbnt_recovery.pdf) | The full playbook, ready to read or print |
| [`rbnt_recovery.docx`](https://github.com/0xDarkSeidBull/daotask16/blob/main/rbnt_recovery.docx) | The same playbook, editable |
| [`evidence/`](https://github.com/0xDarkSeidBull/daotask16/tree/main/evidence) | Lucid Labs Bridge screenshots, every chain tested |
| [`evidence2/`](https://github.com/0xDarkSeidBull/daotask16/tree/main/evidence2) | Oku screenshots, used to cross check Lucid Labs |

## What is inside the playbook

🌉 &nbsp; **Before You Bridge** - how to avoid a wrong network deposit in the first place

📋 &nbsp; **Reference Tables** - verified wrapped RBNT contract addresses on every chain, plus live swap liquidity depth

🪙 &nbsp; **Failure Mode 1** - wrapped RBNT showing zero value or a swap that will not complete

🔁 &nbsp; **Failure Mode 2** - quote unavailable when bridging RBNT back to Redbelly Network

💵 &nbsp; **Failure Mode 3** - USDC or USDT that appears stranded on Ethereum

🏦 &nbsp; **Failure Mode 4** - RBNT sent directly to an exchange on the wrong network

---

## Quick answers

<details>
<summary>My wrapped RBNT shows zero value, is it fake?</summary>
<br>
Compare the contract address in your wallet against Table A in the playbook, character by character. If it does not match, you are holding an unverified or impersonator token, most commonly on BNB Chain, where Redbelly's own team has confirmed no official token was ever issued.
</details>

<details>
<summary>Why does bridging from Solana show no route?</summary>
<br>
Redbelly's team confirmed directly that there is no single step bridge between Solana and Redbelly Network. The route is two hops: Redbelly Network to a supported EVM chain via Lucid Labs Bridge or Oku, then that EVM chain to Solana via Stargate. Same path in reverse.
</details>

<details>
<summary>Is RBNT really on BSC?</summary>
<br>
No. See the evidence image above, Redbelly's team stated this directly in their official Discord: "We never had rbnt on bsc. All RBNT on bsc is fake."
</details>

<details>
<summary>I sent funds to the wrong exchange deposit address, what now?</summary>
<br>
Failure Mode 4 covers the exact recovery process, fees, and odds for each of the four exchanges that list RBNT: Gate, MEXC, BYDFi, and WhiteBIT. Do not resend funds, and do not click any link offering to expedite recovery for a fee.
</details>

---

## Sources this guide relies on

- Redbelly developer docs, `vine.redbelly.network`
- Redbelly official X announcements
- Redbelly official Discord, team confirmations cited by date
- Live quotes from Lucid Labs Bridge (`bridge.lucidlabs.fi`) and Oku (`oku.trade`)
- Redbelly explorer, `redbelly.routescan.io`

Full citation list with links is in the playbook's Sources section.

## A note on how to use this

This guide describes what was true at the time it was checked. Bridge routes, pool depth, and exchange recovery processes change. Treat the step by step instructions as durable and the specific numbers (fees, price impact, liquidity) as a snapshot, confirm current figures before acting on anything that matters to you.

---

<div align="center">

**Redbelly DAO** · Task Board, TASK-16

[Read PDF](https://github.com/0xDarkSeidBull/daotask16/blob/main/rbnt_recovery.pdf) · [Read Docs](https://github.com/0xDarkSeidBull/daotask16/blob/main/rbnt_recovery.docx) · [Live Site](https://daotask16.test-hub.xyz) · [Evidence](https://github.com/0xDarkSeidBull/daotask16/tree/main/evidence)

</div>
