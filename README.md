# Hi, I'm Mehdi

I'm a Rust engineer. I work on the parts of a system where a bug costs someone money: exchanges, custody, smart contracts, zero-knowledge verifiers. More recently that includes AI agents, and making them prove what they did.

I trained as an engineer (statistics and signal processing), then did a Master in Finance at ESSEC and a stint on the exotic equity derivatives desk at Natixis. So I can sit down with a trading or compliance team, work out what they actually need, and build it myself. I speak French, English and Arabic.

Open to forward deployed, AI engineering and blockchain roles.

## Right now

**An exchange for tokenised real-world assets, settled on Solana.** Rust from top to bottom: Axum and Leptos on the web side, Postgres through SQLx, Anchor programs on-chain. I work on the exchange core: the order book and its settlement, token issuance under Token-2022, custody with a separate signing service, and the vault and escrow programs. The code is private, but I'm happy to talk through the design.

**[Triffin](https://triffin.app), on the side.** You photograph your meal. A model names the dish, counts the calories and protein, and tells you what to eat next. I built it on my own, from the app to the backend to the billing, and it is on the App Store.

## Things I've built

**[Execution Kernel](https://github.com/Defiesta/execution-kernel)** · Rust, RISC Zero, Solidity  
An autonomous trading agent runs inside a zkVM and comes out with a proof that it stayed within its limits. Solidity contracts verify that proof on-chain. I designed and wrote it, and the same kernel is now the base of [Tokamak's agent layer](https://github.com/tokamak-network/Tokamak-AI-Layer).

**[A cheaper verifier for the Tokamak zk-EVM](https://eprint.iacr.org/2025/1390)** · Solidity, BLS12-381  
First author of the paper. We took on-chain proof verification from 857,200 gas to 748,450, mostly by bringing the G1 exponentiations down from 40 to 31. I also wrote a large part of the rollup's [Layer 1 contracts](https://github.com/tokamak-network/Tokamak-zk-EVM-contracts).

**[GemSTON](https://github.com/tokamak-network/gem-nft-contract)** · Solidity  
NFTs whose value is backed by staked TON, with a marketplace, mining and forging, and the wrapped staked TON token underneath. I wrote nearly all of it.

**[Poseidon for BLS12-381 on the EVM](https://github.com/Mehd1b/Poseidon-bls12381-EVM)** · Solidity, Yul  
Poseidon hashing over the BLS12-381 scalar field. The Yul version costs about 33K gas per hash, against 440K for plain Solidity. It has not been audited, so read it before you rely on it.

**Security reviews**  
I review contracts before they ship. Some of what I found is public: [staking v2](https://github.com/tokamak-network/ton-staking-v2/issues?q=is%3Aissue+author%3AMehd1b), the [Thanos bridge](https://github.com/tokamak-network/tokamak-thanos/issues?q=is%3Aissue+author%3AMehd1b) and [Commit-Reveal²](https://github.com/tokamak-network/Commit-Reveal2/issues?q=is%3Aissue+author%3AMehd1b).

## What I work with

- **Rust:** Tokio, Axum, SQLx and Postgres, Leptos, Anchor and Solana programs, RISC Zero guests
- **Smart contracts:** Solidity, Yul, Foundry, Hardhat
- **Zero-knowledge:** Groth16, circom and snarkjs, verifier design, the BLS12-381 precompiles
- **AI:** model features in a shipped product, agent runtimes, agents whose actions can be verified
- **Also:** TypeScript, Next.js, and Go when the job calls for it

## Get in touch

mehdiberiane@gmail.com · [mehd1b.github.io](https://mehd1b.github.io)

If the role means sitting next to the customer and shipping what they need that week, I'd like to hear about it.
