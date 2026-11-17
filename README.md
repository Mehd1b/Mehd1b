<p align="center">
  <img width="100%" alt="Mehdi Beriane: Rust, exchanges, zero-knowledge, AI agents" src="assets/header.svg" />
</p>

<p align="center">
  <img alt="I build exchanges in Rust. Zero-knowledge verifiers on the EVM. AI agents that prove what they did." src="assets/tagline.svg" />
</p>

<p align="center">
  <a href="https://eprint.iacr.org/2025/1390"><img alt="IACR ePrint 2025/1390" src="https://img.shields.io/badge/IACR_ePrint-2025%2F1390-b31b1b?style=for-the-badge" /></a>
  <img alt="Open to FDE, AI and blockchain roles" src="https://img.shields.io/badge/open_to-FDE_%C2%B7_AI_%C2%B7_blockchain-1f6feb?style=for-the-badge" />
  <a href="mailto:mehdiberiane@gmail.com"><img alt="Email me" src="https://img.shields.io/badge/Email_me-0b1220?style=for-the-badge&logo=gmail&logoColor=white" /></a>
  <a href="https://mehd1b.github.io"><img alt="CV and site" src="https://img.shields.io/badge/CV_and_site-0b1220?style=for-the-badge&logo=googlechrome&logoColor=white" /></a>
</p>

I'm a lead engineer at @mantiq-technologies. I work on the parts of a system where a bug costs someone money: exchanges, custody, smart contracts, zero-knowledge proofs. More recently that includes AI agents, and making them prove what they did.

I trained as an engineer (statistics and signal processing), then did a Master in Finance at ESSEC and a stint on the exotic equity derivatives desk at Natixis. So I can sit down with a trading or compliance team, work out what they actually need, and build it myself. I speak French, English and Arabic.

## Right now

**An exchange for tokenised real-world assets, settled on Solana.** Rust from top to bottom: Axum and Leptos on the web side, Postgres through SQLx, Anchor programs on-chain. I work on the exchange core: the order book and its settlement, token issuance under Token-2022, custody with a separate signing service, and the vault and escrow programs. The code is private, but I'm happy to talk through the design.

**[Triffin](https://triffin.app), on the side.** You photograph your meal. A model names the dish, counts the calories and protein, and tells you what to eat next. I built it on my own, from the app to the backend to the billing, and it is on the App Store.

## Things I've built

<table>
  <tr>
    <td width="50%" valign="top">
      <h3><a href="https://github.com/Defiesta/execution-kernel">Execution Kernel</a></h3>
      <p>An autonomous trading agent runs inside a zkVM and comes out with a proof that it stayed within its limits. I designed and wrote it, and the same kernel is now the base of <a href="https://github.com/tokamak-network/Tokamak-AI-Layer">Tokamak's agent layer</a>.</p>
      <img alt="Rust" src="https://img.shields.io/badge/Rust-0b1220?style=flat-square&logo=rust&logoColor=white" />
      <img alt="RISC Zero" src="https://img.shields.io/badge/RISC_Zero-0b1220?style=flat-square" />
      <img alt="Solidity" src="https://img.shields.io/badge/Solidity-0b1220?style=flat-square&logo=solidity&logoColor=white" />
    </td>
    <td width="50%" valign="top">
      <h3><a href="https://eprint.iacr.org/2025/1390">zk-EVM verifier</a></h3>
      <p>First author of the paper. On-chain proof verification went from 857,200 gas to 748,450. I also wrote a large part of the rollup's <a href="https://github.com/tokamak-network/Tokamak-zk-EVM-contracts">Layer 1 contracts</a>.</p>
      <img alt="Solidity" src="https://img.shields.io/badge/Solidity-0b1220?style=flat-square&logo=solidity&logoColor=white" />
      <img alt="BLS12-381" src="https://img.shields.io/badge/BLS12--381-0b1220?style=flat-square" />
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <h3><a href="https://github.com/tokamak-network/gem-nft-contract">GemSTON</a></h3>
      <p>NFTs backed by staked TON, with a marketplace and the liquid staking token underneath. I wrote nearly all of it.</p>
      <img alt="Solidity" src="https://img.shields.io/badge/Solidity-0b1220?style=flat-square&logo=solidity&logoColor=white" />
      <img alt="Stars" src="https://img.shields.io/github/stars/tokamak-network/gem-nft-contract?style=flat-square&label=stars&color=0b1220" />
    </td>
    <td width="50%" valign="top">
      <h3><a href="https://github.com/Mehd1b/Poseidon-bls12381-EVM">Poseidon for BLS12-381</a></h3>
      <p>Poseidon hashing for the EVM. About 33K gas per hash in Yul, against 440K in plain Solidity. Not audited, so read it before you rely on it.</p>
      <img alt="Solidity" src="https://img.shields.io/badge/Solidity-0b1220?style=flat-square&logo=solidity&logoColor=white" />
      <img alt="Yul" src="https://img.shields.io/badge/Yul-0b1220?style=flat-square" />
    </td>
  </tr>
</table>

How the Execution Kernel fits together:

```mermaid
flowchart LR
    A["Agent code<br/>Rust"] --> B["Execution Kernel<br/>RISC Zero zkVM"]
    B --> C["Proof of the run"]
    C --> D["Verifier contract<br/>Solidity, on-chain"]
```

**Security reviews**  
I review contracts before they ship. Some of what I found is public: [staking v2](https://github.com/tokamak-network/ton-staking-v2/issues?q=is%3Aissue+author%3AMehd1b), the [Thanos bridge](https://github.com/tokamak-network/tokamak-thanos/issues?q=is%3Aissue+author%3AMehd1b) and [Commit-Reveal²](https://github.com/tokamak-network/Commit-Reveal2/issues?q=is%3Aissue+author%3AMehd1b).

## What I work with

![Rust](https://img.shields.io/badge/Rust-0b1220?style=for-the-badge&logo=rust&logoColor=white)
![Tokio](https://img.shields.io/badge/Tokio-0b1220?style=for-the-badge&logo=tokio&logoColor=white)
![Axum](https://img.shields.io/badge/Axum-0b1220?style=for-the-badge)
![Leptos](https://img.shields.io/badge/Leptos-0b1220?style=for-the-badge&logo=leptos&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-0b1220?style=for-the-badge&logo=postgresql&logoColor=white)
![Solana](https://img.shields.io/badge/Solana-0b1220?style=for-the-badge&logo=solana&logoColor=white)
![Anchor](https://img.shields.io/badge/Anchor-0b1220?style=for-the-badge)
![RISC Zero](https://img.shields.io/badge/RISC_Zero-0b1220?style=for-the-badge)
![Solidity](https://img.shields.io/badge/Solidity-0b1220?style=for-the-badge&logo=solidity&logoColor=white)
![Ethereum](https://img.shields.io/badge/Ethereum-0b1220?style=for-the-badge&logo=ethereum&logoColor=white)
![Foundry](https://img.shields.io/badge/Foundry-0b1220?style=for-the-badge)
![TypeScript](https://img.shields.io/badge/TypeScript-0b1220?style=for-the-badge&logo=typescript&logoColor=white)
![Next.js](https://img.shields.io/badge/Next.js-0b1220?style=for-the-badge&logo=nextdotjs&logoColor=white)
![Go](https://img.shields.io/badge/Go-0b1220?style=for-the-badge&logo=go&logoColor=white)

**Zero-knowledge:** Groth16, circom and snarkjs, verifier design, the BLS12-381 precompiles.  
**AI:** model features in a shipped product, agent runtimes, agents whose actions can be verified.

## Activity

<p align="center">
  <img alt="Contribution totals and chart" src="https://github-profile-summary-cards.vercel.app/api/cards/profile-details?username=Mehd1b&theme=github_dark" />
</p>

<p align="center">
  <img alt="Activity over the last month" src="https://github-readme-activity-graph.vercel.app/graph?username=Mehd1b&theme=github-compact&hide_border=true" />
</p>

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Mehd1b/Mehd1b/output/github-contribution-grid-snake-dark.svg" />
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Mehd1b/Mehd1b/output/github-contribution-grid-snake.svg" />
    <img alt="Contribution graph" src="https://raw.githubusercontent.com/Mehd1b/Mehd1b/output/github-contribution-grid-snake.svg" />
  </picture>
</p>

## Get in touch

mehdiberiane@gmail.com · [mehd1b.github.io](https://mehd1b.github.io)

If the role means sitting next to the customer and shipping what they need that week, I'd like to hear about it.
