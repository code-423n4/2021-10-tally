# Tally Contest 🐕

Meet [Tally](https://tally.cash), the community owned and operated Web3 wallet.
In this contest, we're looking at Tally Swap, the 0x-based DEX aggregator
embedded in the wallet.

![Tally Swap](./public/swap.gif)

## Tally contest details
- $28,500 worth of ETH award pot
- $1,500 worth of ETH gas optimization award pot
- Join [C4 Discord](https://discord.gg/EY5dvm3evD) to register
- Submit findings [using the C4 form](https://code423n4.com/2021-10-tally-contest/submit)
- [Read our guidelines for more details](https://docs.code4rena.com/roles/wardens)
- Starts October 20, 2021 00:00 UTC
- Ends October 22, 2021 23:59 UTC
---

# Useful links ⭐️

🐕 [tally.cash](https://tally.cash) — 🐦 [@tallycash](https://twitter.com/tallycash) — 🤖 [Discord](https://chat.tally.cash)

# Quickstart

To build the contracts, run

```bash
yarn install
yarn build
```

## Contract overview

| Contract Name              | Lines of Code |
| -------------------------- | ------------- |
| `Swap.sol`                 | 263           |
| `Math.sol`                 | 20            |
| `EmergencyGovernable.sol`  | 64            |
| `EmergencyPausable.sol`    | 26            |
| `MockZrxExchangeProxy.sol` | 73            |
| `MockToken.sol`            | 9             |
| **Total**                  | **455**       |

### Dependencies

The main contract is `Swap.sol`, which executes quotes provided off-chain by the
[0x API](https://0x.org/docs/api) in the Tally wallet, taking swap fees for the
DAO. It relies on `SafeMath.sol`, `SafeERC20.sol`, and `ReentrancyGuard.sol`
from the OpenZeppelin contracts library.

## System overview

The Tally wallet is an EOA wallet that runs as a browser extension. Though Tally
isn't a "smart contract wallet", preferring to custody user funds outside smart
contracts to save on gas, a number of features in the wallet require paired
smart contracts. Tally Swap is one of those features.

## ⭐️ Sponsor: Provide contest details

Under "SPONSORS ADD INFO HERE" heading below, include the following:

- [X] Name of each contract and:
  - [X] lines of code in each
  - [ ] external contracts called in each
  - [ ] libraries used in each
- [X] Describe any novel or unique curve logic or mathematical models implemented in the contracts
- [X] Does the token conform to the ERC-20 standard? In what specific ways does it differ?
- [ ] Describe anything else that adds any special logic that makes your approach unique
- [ ] Identify any areas of specific concern in reviewing the code
- [ ] Add all of the code to this repo that you want reviewed
- [ ] Create a PR to this repo with the above changes.

---

# ⭐️ Sponsor: Provide marketing details

- [ ] Your logo (URL or add file to this repo - SVG or other vector format preferred)
- [X] Your primary Twitter handle
- [ ] Any other Twitter handles we can/should tag in (e.g. organizers' personal accounts, etc.)
- [X] Your Discord URI
- [X] Your website
- [ ] Optional: Do you have any quirks, recurring themes, iconic tweets, community "secret handshake" stuff we could work in? How do your people recognize each other, for example?
- [X] Optional: your logo in Discord emoji format

---

# Contest prep

## 🐺 C4: Contest prep
- [X] Rename this repo to reflect contest date (if applicable)
- [X] Rename contest H1 below
- [X] Add link to report form in contest details below
- [X] Update pot sizes
- [X] Fill in start and end times in contest bullets below.
- [X] Move any relevant information in "contest scope information" above to the bottom of this readme.
- [ ] Delete this checklist.

## ⭐️ Sponsor: Contest prep
- [X] Make sure your code is thoroughly commented using the [NatSpec format](https://docs.soliditylang.org/en/v0.5.10/natspec-format.html#natspec-format).
- [ ] Modify the bottom of this `README.md` file to describe how your code is supposed to work with links to any relevent documentation and any other criteria/details that the C4 Wardens should keep in mind when reviewing. ([Here's a well-constructed example.](https://github.com/code-423n4/2021-06-gro/blob/main/README.md))
- [ ] Please have final versions of contracts and documentation added/updated in this repo **no less than 8 hours prior to contest start time.**
- [X] Ensure that you have access to the _findings_ repo where issues will be submitted.
- [ ] Promote the contest on Twitter (optional: tag in relevant protocols, etc.)
- [ ] Share it with your own communities (blog, Discord, Telegram, email newsletters, etc.)
- [ ] Optional: pre-record a high-level overview of your protocol (not just specific smart contract functions). This saves wardens a lot of time wading through documentation.
- [X] Designate someone (or a team of people) to monitor DMs & questions in the C4 Discord (**#questions** channel) daily (Note: please *don't* discuss issues submitted by wardens in an open channel, as this could give hints to other wardens.)
- [ ] Delete this checklist and all text above the line below when you're ready.

---

This repo will be made public before the start of the contest. (C4 delete this line when made public)

[ ⭐️ SPONSORS ADD INFO HERE ]
