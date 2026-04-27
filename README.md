<div align="center">

```
        ████████╗██████╗  █████╗  ██████╗███████╗
        ╚══██╔══╝██╔══██╗██╔══██╗██╔════╝██╔════╝
           ██║   ██████╔╝███████║██║     █████╗
           ██║   ██╔══██╗██╔══██║██║     ██╔══╝
           ██║   ██║  ██║██║  ██║╚██████╗███████╗
           ╚═╝   ╚═╝  ╚═╝╚═╝  ╚═╝ ╚═════╝╚══════╝
```

### autonomous AI agent verifier on ethereum

fake agents have no pulse · scan every deployment · classify autonomous / hybrid / human · publish onchain attestations

[![repo](https://img.shields.io/badge/repo-traceprotocolscan%2Ftrace--protocol-181717?logo=github)](https://github.com/traceprotocolscan/trace-protocol)
[![license](https://img.shields.io/badge/license-MIT-blue)](https://github.com/traceprotocolscan/trace-protocol/blob/main/LICENSE)
[![ethereum](https://img.shields.io/badge/ethereum-native-627EEA?logo=ethereum&logoColor=white)](#)
[![solidity](https://img.shields.io/badge/solidity-0.8.24-363636?logo=solidity&logoColor=white)](#)
[![X](https://img.shields.io/badge/follow-%40TraceProtocol__-1DA1F2?logo=x&logoColor=white)](https://x.com/TraceProtocol_)

</div>

---

## what i'm building

**[trace protocol](https://github.com/traceprotocolscan/trace-protocol)** — onchain registry of agent classifications. classifier observes an agent's transaction history, scores it, and publishes an attestation so downstream contracts and frontends read the verdict from a single source of truth.

four layers compose the stack:

- **scanner** — viem-based event listener, indexes the attestation contract feed
- **classifier** — feature extraction + onnx inference + temperature-scaled confidence
- **verdict engine** — scoring + thresholds, decides when to publish or update
- **on-chain registry** — Solidity contract on ethereum, rotatable attester key, custom errors, sepolia-deployable today

---

## why

every project that ships an "AI agent" puts a wallet onchain and calls it autonomous. most of them are scripts with a llm sticker. trace separates real agents from packaging by reading their actual behavior, not their marketing.

---

## pinned

| repo | what it is | status |
|---|---|---|
| [**trace-protocol**](https://github.com/traceprotocolscan/trace-protocol) | scanner + classifier + verdict engine + onchain registry | 🟢 v0.4.0 |

---

## stack

solidity 0.8.24 · foundry · typescript · viem · onnx-runtime · pino · vitest · pnpm workspaces

---

<div align="center">

[github](https://github.com/traceprotocolscan) · [x](https://x.com/TraceProtocol_)

</div>
