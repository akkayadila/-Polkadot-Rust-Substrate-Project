# Polkadot-Rust-Substrate-Project

## Overview

- **Building a blockchain:** Simulation of a transaction on Substrate node using front end
- **Simulating a substrate network:** Simulation a substrate network by with two nodes
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
1. Purged the old chain data for Alice and Bob and starting new nodes
2. Observed the nodes discovering each other on the network and starting consensus mechanism

<img width="800" alt="polkadot7" src="https://github.com/akkayadila/-Polkadot-Rust-Substrate-Project/assets/133990573/ac687586-eb95-4032-a2b2-f15408a8a7a3">

Shown above is Alice node discovering Bob node and switching from 0 peers to 1 peer and Bob node producing a block that is imported to Alice node.

### 3. Adding trusted nodes to a network
1. Opened up two terminals with different sudo users.
2. Cloned and ran substrate node template on both terminals.
3. Generated aura key using Sr25519 signature and grandpa key using Ed25519 signature
  - Command used to get aura keys for respective users: `./target/release/node-template key generate --scheme Sr25519 --password-interactive`
  - Command used to get grandpa key for the first user: `./target/release/node-template key inspect --password-interactive --scheme Ed25519 "clay also afford asthma burden swallow enable rebuild duck range champion habit"`
  - Command used to get grandpa key for the first user: `./target/release/node-template key inspect --password-interactive --scheme Ed25519 "digital lunar lyrics brush witness funny rebuild master love stable hair gas"`
4. Exported the local chain specifications into `customSpec.json` using the command `./target/release/node-template build-spec --disable-default-bootnode --chain local > customSpec.json`
5. Opened `customSpec.json` and edited in aura and granpa keys generated earlier to obtain custom chain specifications with validators.
6. Converted .json file to raw format with command `./target/release/node-template build-spec --chain=customSpec.json --raw --disable-default-bootnode > customSpecRaw.json` so that the chain can be used
7. Ran the first node using the command:
 `./target/release/node-template  
  --base-path /tmp/node01  
  --chain ./customSpecRaw.json  
  --port 30333  
  --rpc-port 9933  
  --telemetry-url "wss://telemetry.polkadot.io/submit/ 0"  
  --validator  
  --rpc-methods Unsafe  
  --name MyNode01  
  --password-interactive`
   
