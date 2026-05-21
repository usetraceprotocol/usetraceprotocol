<div align="center">

```
        ████████╗██████╗  █████╗  ██████╗███████╗
        ╚══██╔══╝██╔══██╗██╔══██╗██╔════╝██╔════╝
           ██║   ██████╔╝███████║██║     █████╗
           ██║   ██╔══██╗██╔══██║██║     ██╔══╝
           ██║   ██║  ██║██║  ██║╚██████╗███████╗
           ╚═╝   ╚═╝  ╚═╝╚═╝  ╚═╝ ╚═════╝╚══════╝
```

### onchain ai agent verifier · base + ethereum

**fake agents have no pulse.**

scan every agent deployment · classify autonomous / hybrid / human · publish onchain attestations · funded by uniswap v4 hook fees

[![repo](https://img.shields.io/badge/repo-trace--protocol-181717?logo=github&logoColor=white)](https://github.com/usetraceprotocol/trace-protocol)
[![release](https://img.shields.io/github/v/release/usetraceprotocol/trace-protocol?label=release&color=627EEA)](https://github.com/usetraceprotocol/trace-protocol/releases)
[![license](https://img.shields.io/badge/license-MIT-blue)](https://github.com/usetraceprotocol/trace-protocol/blob/main/LICENSE)
[![base](https://img.shields.io/badge/base-mainnet-0052FF?logo=coinbase&logoColor=white)](#)
[![ethereum](https://img.shields.io/badge/ethereum-native-627EEA?logo=ethereum&logoColor=white)](#)
[![uniswap v4](https://img.shields.io/badge/uniswap-v4_hook-FF007A?logo=uniswap&logoColor=white)](#)
[![solidity](https://img.shields.io/badge/solidity-0.8.24-363636?logo=solidity&logoColor=white)](#)
[![X](https://img.shields.io/badge/follow-%40TraceProtocol__-1DA1F2?logo=x&logoColor=white)](https://x.com/TraceProtocol_)
[![Telegram](https://img.shields.io/badge/telegram-usetraceprotocol-26A5E4?logo=telegram&logoColor=white)](https://t.me/usetraceprotocol)

</div>

---

## what i'm building

**[trace protocol](https://github.com/usetraceprotocol/trace-protocol)** — onchain registry of agent classifications, written by a uniswap v4 hook that fingerprints every swap caller on base and ethereum. one hook, two chains. the chain is the source of truth — contracts and frontends read the verdict from a single onchain call.

four layers compose the stack:

- **v4 hook** — `beforeSwap` fingerprints the caller against gas cadence, nonce drift, signer entropy, mempool timing. 1% of pool fee routes into the scanner endpoint. fee becomes forensics.
- **scanner** — viem-based event listener, indexes the attestation contract feed across base + ethereum
- **classifier** — feature extraction + onnx inference + temperature-scaled confidence, capped at 0.95
- **on-chain registry** — solidity contract, rotatable attester key, custom errors. attestations land on base, mirrored to ethereum via L1 message proofs

---

## why this exists

every project that ships an "ai agent" puts a wallet onchain and calls it autonomous. most are scripts with an llm sticker. 97% of self-claimed agents on ethereum are humans pretending.

trace separates real agents from packaging by reading their actual behavior — tx frequency entropy, response latency, instruction diversity, decision variance, time-of-day patterns — not their marketing. signatures cannot be faked at scale. the chain does not lie.

---

## pinned

| repo | what it is | status |
|---|---|---|
| [**trace-protocol**](https://github.com/usetraceprotocol/trace-protocol) | scanner + classifier + verdict engine + v4 hook + onchain registry | 🟢 v0.4.2 |
| [**trace-protocol-site**](https://github.com/usetraceprotocol/trace-protocol-site) | landing at traceprotocol.tech (next 16 + tailwind v4) | 🟢 live |

---

## stats

<div align="center">

![trace stats](https://github-readme-stats.vercel.app/api?username=usetraceprotocol&show_icons=true&hide=stars,issues&theme=dark&hide_border=true&include_all_commits=true&count_private=false&bg_color=0d1117&title_color=627EEA&icon_color=627EEA&text_color=c9d1d9)
![trace languages](https://github-readme-stats.vercel.app/api/top-langs/?username=usetraceprotocol&layout=compact&theme=dark&hide_border=true&bg_color=0d1117&title_color=627EEA&text_color=c9d1d9&langs_count=8)

</div>

---

## stack

solidity 0.8.24 · foundry · openzeppelin · uniswap v4-core · typescript · viem · wagmi · onnx-runtime · pino · vitest · pnpm workspaces · python · prometheus · base + ethereum

---

## status

- **v0.4.2 shipped** — base support live · v4 hook beforeSwap + fee routing · attestation mirroring base → ethereum
- v4 hook open source: [`contracts/trace-hook`](https://github.com/usetraceprotocol/trace-protocol/tree/main/contracts/trace-hook)
- attestation registry live: [`contracts/trace-attestation`](https://github.com/usetraceprotocol/trace-protocol/tree/main/contracts/trace-attestation)
- arbitrum + optimism on the v0.5.x track

---

<div align="center">

[website](https://traceprotocol.tech) · [github](https://github.com/usetraceprotocol/trace-protocol) · [x](https://x.com/TraceProtocol_) · [telegram](https://t.me/usetraceprotocol)

*classifier, not an oracle. confidence capped at 0.95.*

</div>
