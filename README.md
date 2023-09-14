# -Polkadot-Rust-Substrate-Project

### 1. Building a blockchain

We make a transaction using frontend on Substrate node. Transaction simulated here is from Alice to Dave and the amount is 1 unit.

Events
system:ExtrinsicSuccess
{"dispatchInfo":{"weight":{"refTime":"308,980,000","proofSize":"3,593"},"class":"Normal","paysFee":"Yes"}}
transactionPayment:TransactionFeePaid
{"who":"5GrwvaEF5zXb26Fz9rcQpDWS57CtERHpNehXCPcNoHGKutQY","actualFee":"308,980,146","tip":"0"}
balances:Transfer
{"from":"5GrwvaEF5zXb26Fz9rcQpDWS57CtERHpNehXCPcNoHGKutQY","to":"5DAAnrj7VHTznn2AWBemMuyBwZWs6FNFjdyVXUeYum3PTXFy","amount":"1,000,000,000,000"}
balances:Endowed
{"account":"5DAAnrj7VHTznn2AWBemMuyBwZWs6FNFjdyVXUeYum3PTXFy","freeBalance":"1,000,000,000,000"}
system:NewAccount
{"account":"5DAAnrj7VHTznn2AWBemMuyBwZWs6FNFjdyVXUeYum3PTXFy"}
balances:Withdraw
{"who":"5GrwvaEF5zXb26Fz9rcQpDWS57CtERHpNehXCPcNoHGKutQY","amount":"308,980,146"}
