# CryptoAI Jedi

Reliability monitoring, wallet operations tooling, and AI-assisted automation for crypto infrastructure. Currently running ops for a 2,000-unit ASIC fleet at ~98% uptime across multiple sites.

Background runs in an unusual order: eight years as a futures broker (NFA Series 3, expired) → 2.5 years in enterprise endpoint security at ESET → mining infrastructure operations. Crypto-native since 2018; building AI agent systems on VPS since 2024.

## What I work with

**Languages:** Python, Bash, PowerShell. SQL at working level.

**Infrastructure:** Linux (Debian / Arch / RHEL), Windows Server, Docker, systemd, networking (TCP/IP, DNS, DHCP, firewalls), Tailscale, WireGuard.

**Observability:** Prometheus, Grafana, structured logging, metric-driven alerting, incident escalation patterns.

**APIs:** Postman, cURL, REST/JSON, OAuth/JWT, webhook signing, HTTP debugging.

**Web3:** Bitcoin, EVM, and Solana —> node ops, multi-signature wallet operations, onchain investigation with Etherscan, Solscan, Mempool, Tenderly, and Blockstream.

**AI / agents:** OpenRouter, LiteLLM proxy, multi-agent orchestration on VPS, Docker backend, prompt engineering, RAG fundamentals.

**Support tooling:** Zendesk, Jira, Bomgar, NetSuite.

## Projects

### [wallet-ops-sentinel](https://github.com/CryptoAI-Jedi/wallet-ops-sentinel)

Multi-chain wallet monitoring with sanctioned-address screening and structured alert envelopes designed to feed ticketing, SIEM, or LLM-assisted incident summaries.

**Tech:** Python, PyYAML, Etherscan API, Blockstream API.

**Built for:** Detecting large outflows from monitored addresses; flagging interactions with sanctioned wallets and known mixer contracts; producing JSON alert records that downstream systems can consume without further parsing.

**What I learned:** Bitcoin's UTXO model and EVM's account model need genuinely different "what just happened" logic — you can't fake one with the other. Structuring alert events for consumers I don't control (some hypothetical SIEM, some hypothetical LLM summarizer) was harder than the detection itself; the schema is the contract.

### [node-health-monitor](https://github.com/CryptoAI-Jedi/node-health-monitor)

Production-style observability stack for Bitcoin and Monero node uptime, peer connectivity, and infrastructure health.

**Tech:** Prometheus, Grafana, Docker, systemd, Linux.

**Built for:** Replacing manual SSH-and-check workflows with dashboards and metric-based alerting. Real-time visibility into node operations with escalation-grade data, not just "is this thing reachable."

### [mining-ops-toolkit](https://github.com/CryptoAI-Jedi/mining-ops-toolkit)

Daily-driver scripts for ASIC fleet monitoring: miner health, pool connectivity, thermal status.

**Tech:** Python, Bash, JSON-RPC.

**Built for:** Standardizing fleet checks across thousands of units where 5% offline at any given moment is the steady state, not an emergency. Structured output feeds log aggregation; degraded-miner detection runs against historical baselines instead of arbitrary thresholds.

**What I learned:** "Is this thing okay?" logic at fleet scale has to handle missing data as a normal case, not an error case. Otherwise your alerts page you for the network, not the miners.

### [base-escrow](https://github.com/CryptoAI-Jedi/base-escrow)

Marketplace escrow MVP on Base Sepolia. Explores Chainlink CRE for dispute resolution events and transparent settlement logic.

**Tech:** Solidity, Python, Chainlink CRE, Base Sepolia.

**Status:** Work in progress — current focus has shifted to other projects.

### [dev-cheatsheets](https://github.com/CryptoAI-Jedi/dev-cheatsheets)

Field-ready CLI / DevOps / Web3 reference. Personal notes that became shareable.

## Currently building

Most of my active work lives in private repositories — AI agent infrastructure on VPS (multi-agent orchestration with shared memory, tool routing, and persistent execution), prediction-market trading automation, and a SaaS product in the operations-tooling space. The public projects above are extracted utilities and reference work from this broader stack.

## Certifications

| Certification | Issuer | Year |
|---|---|---|
| Postman API Fundamentals Student Expert | Postman | 2026 |
| API Security Fundamentals | APISEC University | 2026 |
| Blockchain Basics | Cyfrin Updraft | 2026 |
| Web3 Wallet Security Basics & Advanced | Cyfrin Updraft | 2026 |
| CompTIA A+, Network+, Security+ | CompTIA | 2018 (expired, knowledge current) |

## Contact

[cryptoaijedi@proton.me](mailto:cryptoaijedi@proton.me)

USA · US Eastern · Open to global remote and relocation
