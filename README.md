# Polkadot-Rust-Substrate-Project

## Overview

- **Building a blockchain:** Simulation of a transaction on Substrate node using front end.
- **Simulating a substrate network:**
- **Adding trusted nodes to a network:**

### 1. Building a blockchain
1. Cloned the the substrate node template to start a substrate node from `https://github.com/substrate-developer-hub/substrate-node-template`
2. Started a new branch with `git switch -c my-new-branch`
3. Compiled with `cargo build --release` and started the node with `./target/release/node-template --dev`
4. Cloned the template for front end from `https://github.com/substrate-developer-hub/substrate-front-end-template`
5. Installed the front end using `yarn install` and started it with `yarn start`
6. Front end available at `http://localhost:8000/substrate-front-end-template` to make a transaction

Transaction simulated here is from Alice to Dave and the amount is 1 unit.
<img width="709" alt="polkadot1" src="https://github.com/akkayadila/-Polkadot-Rust-Substrate-Project/assets/133990573/f8968183-d7c9-4e1c-9d6b-81edd54a7a1b">
<img width="454" alt="polkadot2" src="https://github.com/akkayadila/-Polkadot-Rust-Substrate-Project/assets/133990573/9b3575e1-b1db-4b1c-a5c3-91d8e0c9f103">

### 2. Simulating a substrate network


### 3. Adding trusted nodes to a network
1. Opened up two terminals with different Linux users.
2. Cloned and ran substrate node template on both terminals.
3. Generated aura key using Sr25519 signature and grandpa key using Ed25519 signature
4. 
   
