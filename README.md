# Decentralized Voting System using Ethereum Blockchain

## Technologies or Frameworks or Languages Used

1. Smart Contract
2. React
3. Truffle
4. Ganache
5. Metamask
6. Web3
7. Ethers

## Project Preview

Voting is one of the most popular example to illustrate the potentials of Blockchain and Smart Contracts. Voting is a use case that is well aligned to the unique propositions of Blockchain technology.

### Basic Principle of Voting

According to the Equal Justice Foundation, the 6 principles of voting are as follows.

- **Secret Ballot**: Your vote is secret. Nobody should be able to link your vote back to your race, gender, age and personal profile.
- **One man, one vote**: Every voter votes once and the voting system must be able to reconcile the total number of votes to the total number of voters and those who did not vote.
- **Voter eligibility**: Only eligible voters are allowed to vote.
- **Transparency**: The vote counting process is fixed, rules are well established,known to voters and withstands public scrutiny.
- **Votes accurately recorded and counted**: Vote counting is consistent. Rules are cast in stone. Vote counts are audit-able.
- **Reliability**: Voting system must be accurate and verifiable. Safeguards are in place to prevent frauds, accidents and security breeches.

This application is covers all these principles. It is fully a Web3.0 Application where anyone can create a Poll or Voting and share `contract address` with others.

## How does the Ballot contract implement the principles of voting?

### Secret Ballot

In the ballot contract, only wallet addresses and names are recorded. Every voter is identified by their MetaMask wallet address. Other than the manager who was the person who created the new instance of the ballot contract, no one else can tell who voted yes or no. For the technical folks among us, I meant to say that the votes array is declared private so no one can read the contents of the votes array.

### One man one vote

The voters array stores a list of voters who have voted. It ensures that no one can vote the second time. Once a voter votes, his status changes to “voted” and the ballot contract checks to ensure that he does not vote again.

### Voter eligibility

Voter eligibility is determined by assembling a voters’ array of wallet address before voting begins. You need to vote with your MetaMask Wallet whose address matches the one that the manager registers before voting begins.

### Transparency

This is one of the things that Blockchain does extremely well. Every action taken and every record etched on the Blockchain is immutable. On a public Blockchain, collusion is close to impossible as described here.

### Votes accurately recorded and counted

In the ballot smart contract, the ballot goes through several states, from the point it is created, open for voting to the point where ballot is closed and votes are counted.

### Reliability

There is no single point of failure on a Blockchain as every node in the chain participates in keeping the Blockchain running.
