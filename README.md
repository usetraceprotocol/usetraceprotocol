<div align="center">

```
        ████████╗██████╗  █████╗  ██████╗███████╗
        ╚══██╔══╝██╔══██╗██╔══██╗██╔════╝██╔════╝
           ██║   ██████╔╝███████║██║     █████╗
           ██║   ██╔══██╗██╔══██║██║     ██╔══╝
           ██║   ██║  ██║██║  ██║╚██████╗███████╗
           ╚═╝   ╚═╝  ╚═╝╚═╝  ╚═╝ ╚═════╝╚══════╝
```

### autonomous ai agent verifier on ethereum

**fake agents have no pulse.**

scan every agent deployment · classify autonomous / hybrid / human · publish onchain attestations

[![repo](https://img.shields.io/badge/repo-trace--protocol-181717?logo=github&logoColor=white)](https://github.com/traceprotocolscan/trace-protocol)
[![release](https://img.shields.io/github/v/release/traceprotocolscan/trace-protocol?label=release&color=627EEA)](https://github.com/traceprotocolscan/trace-protocol/releases)
[![license](https://img.shields.io/badge/license-MIT-blue)](https://github.com/traceprotocolscan/trace-protocol/blob/main/LICENSE)
[![ethereum](https://img.shields.io/badge/ethereum-native-627EEA?logo=ethereum&logoColor=white)](#)
[![solidity](https://img.shields.io/badge/solidity-0.8.24-363636?logo=solidity&logoColor=white)](#)
[![X](https://img.shields.io/badge/follow-%40TraceProtocol__-1DA1F2?logo=x&logoColor=white)](https://x.com/TraceProtocol_)

</div>

---

## what i'm building

**[trace protocol](https://github.com/traceprotocolscan/trace-protocol)** — onchain registry of agent classifications. an off-chain classifier observes an agent's transaction history, scores it, and publishes an attestation so downstream contracts and frontends read the verdict from a single source of truth.

four layers compose the stack:

- **scanner** — viem-based event listener, indexes the attestation contract feed
- **classifier** — feature extraction + onnx inference + temperature-scaled confidence
- **verdict engine** — scoring + thresholds, decides when to publish or update
- **on-chain registry** — solidity contract on ethereum, rotatable attester key, custom errors, sepolia-deployable today

---

## why this exists

every project that ships an "ai agent" puts a wallet onchain and calls it autonomous. most are scripts with an llm sticker. trace separates real agents from packaging by reading their actual behavior — tx frequency entropy, response latency, instruction diversity, decision variance, time-of-day patterns — not their marketing.

---

## pinned

| repo | what it is | status |
|---|---|---|
| [**trace-protocol**](https://github.com/traceprotocolscan/trace-protocol) | scanner + classifier + verdict engine + onchain registry | 🟢 v0.4.0 |

---

## stats

<div align="center">

![trace stats](https://github-readme-stats.vercel.app/api?username=traceprotocolscan&show_icons=true&hide=stars,issues&theme=dark&hide_border=true&include_all_commits=true&count_private=false&bg_color=0d1117&title_color=627EEA&icon_color=627EEA&text_color=c9d1d9)
![trace languages](https://github-readme-stats.vercel.app/api/top-langs/?username=traceprotocolscan&layout=compact&theme=dark&hide_border=true&bg_color=0d1117&title_color=627EEA&text_color=c9d1d9&langs_count=8)

</div>

---

## stack

solidity 0.8.24 · foundry · openzeppelin · typescript · viem · wagmi · onnx-runtime · pino · vitest · pnpm workspaces · python · prometheus

---

## status

- v0.4.0 shipped — confidence calibration + historical verdicts
- sepolia deploy workflow scaffolded; mainnet gated behind multisig setup
- l2 deploys (arbitrum / base / optimism) on the v0.5.x track

---

<div align="center">

[github](https://github.com/traceprotocolscan) · [trace-protocol](https://github.com/traceprotocolscan/trace-protocol) · [x](https://x.com/TraceProtocol_)

*classifier, not an oracle. confidence capped at 0.95.*

</div>
