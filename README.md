# Cashu NUTs (Notation, Usage, and Terminology)

These documents each specify parts of the Cashu Ecash protocol. Read the specifications for the legacy API [here](https://github.com/cashubtc/nuts/tree/74f26b81b6617db710fa1081eebc0c7203711213).

## Cashu v1 (Single Signature) Specifications
Wallets & mints `MUST` implement all mandatory specs and `CAN` implement optional specs.

### Mandatory
| # | Description | Wallets | Mints |
|--- | --- | --- | --- |
| [00][00] | Cryptography and Models | [Nutshell][py], [Feni][feni], [Moksha][cashume], [Nutstash][ns], [cashu-ts][ts], [cashu-crab][cashu-crab] | [Nutshell][py], [Feni][feni], [LNbits], [Moksha][moksha], [cashu-rs-mint][cashu-rs-mint]
| [01][01] | Mint public keys | [Nutshell][py], [Feni][feni], [Moksha][cashume], [Nutstash][ns], [cashu-ts][ts], [cashu-crab][cashu-crab] | [Nutshell][py], [Feni][feni], [LNbits], [Moksha][moksha], [cashu-rs-mint][cashu-rs-mint]
| [02][02] | Keysets and keyset IDs | [Nutshell][py], [Feni][feni], [Moksha][cashume], [Nutstash][ns], [cashu-ts][ts], [cashu-crab][cashu-crab] | [Nutshell][py], [Feni][feni], [LNbits], [Moksha][moksha], [cashu-rs-mint][cashu-rs-mint]
| [03][03] | Swapping tokens | [Nutshell][py], [Feni][feni], [Moksha][cashume], [Nutstash][ns], [cashu-ts][ts], [cashu-crab][cashu-crab] | [Nutshell][py], [Feni][feni], [LNbits], [Moksha][moksha], [cashu-rs-mint][cashu-rs-mint]
| [04][04] | Minting tokens | [Nutshell][py], [Feni][feni], [Moksha][cashume], [Nutstash][ns], [cashu-ts][ts], [cashu-crab][cashu-crab] | [Nutshell][py], [Feni][feni], [LNbits], [Moksha][moksha], [cashu-rs-mint][cashu-rs-mint]
| [05][05] | Melting tokens | [Nutshell][py], [Feni][feni], [Moksha][cashume], [Nutstash][ns], [cashu-ts][ts], [cashu-crab][cashu-crab] | [Nutshell][py], [Feni][feni], [LNbits], [Moksha][moksha], [cashu-rs-mint][cashu-rs-mint]
| [06][06] | Mint info | [Nutshell][py], [eNuts][enuts] | [Nutshell][py], [cashu-rs-mint][cashu-rs-mint]

### Optional
| # | Description | Wallets | Mints |
| --- | --- | --- | --- |
| [07][07] | Token state check | [Nutshell][py], [Feni][feni], [Moksha][cashume], [Nutstash][ns], [cashu-ts][ts], [cashu-crab][cashu-crab] | [Nutshell][py], [Feni][feni], [LNbits], [Moksha][moksha], [cashu-rs-mint][cashu-rs-mint]
| [08][08] | Overpaid Lightning fees | [Nutshell][py], [Feni][feni], [Moksha][cashume], [Nutstash][ns], [cashu-ts][ts], [cashu-crab][cashu-crab] | [Nutshell][py], [LNbits], [Moksha][moksha], [cashu-rs-mint][cashu-rs-mint]
| [09][09] | Deterministic backup and restore | - | -
| [10][10] | Spending conditions | [Nutshell][py] | [Nutshell][py]
| [11][11] | Pay-To-Pubkey (P2PK) | [Nutshell][py] | [Nutshell][py]
| [12][12] | DLEQ proofs | [Nutshell][py] | [Nutshell][py]

## Cashu vF (Federated Threshold Signatures) Specifications

FedNuts are corresponding threshold signature specifications for the cashu vF (`cashuF`) ecash scheme as applied in the [Fedimint protocol](https://github.com/fedimint/fedimint).

The FedNuts are organized to mirror the single-sig NUTS (with the addition of `FedNut F-X` which specifies the `Fedimint Consensus Mechanism` and `Transaction Primitive` which do not appear in single-sig Cashu and are used to prevent malicious federation members from modifying ecash transactions after broadcast.

### FedNUTs: Federated NUTs
| # | Description | Wallets | Mints |
| ---- | --- | --- | --- |
| [F-X](/fedNuts/F-X.md)   | Fedimint Consensus and Transaction Primitive | - | - |
| [F-00](/fedNuts/F-00.md) | Cryptography and Models | [Fedi](https://fedi.xyz), [Mutiny](https://mutinywallet.com) | [Fedimint](https://fedimint.com) |
| [F-01](/fedNuts/F-01.md) | Mint public keys | [Fedi](https://fedi.xyz), [Mutiny](https://mutinywallet.com) | [Fedimint](https://fedimint.com) |
| [F-02](/fedNuts/F-02.md) | Keysets and keyset IDs | [Fedi](https://fedi.xyz), [Mutiny](https://mutinywallet.com) | [Fedimint](https://fedimint.com) |
| [F-03](/fedNuts/F-03.md) | Swapping tokens | [Fedi](https://fedi.xyz), [Mutiny](https://mutinywallet.com) | [Fedimint](https://fedimint.com) |
| [F-04](/fedNuts/F-04.md) | Minting tokens (Pegging-In) | [Fedi](https://fedi.xyz), [Mutiny](https://mutinywallet.com) | [Fedimint](https://fedimint.com) |
| [F-05](/fedNuts/F-05.md) | Melting tokens (Pegging-Out) | [Fedi](https://fedi.xyz), [Mutiny](https://mutinywallet.com) | [Fedimint](https://fedimint.com) |
| [F-06](/fedNuts/F-06.md) | Mint info | [Fedi](https://fedi.xyz), [Mutiny](https://mutinywallet.com) | [Fedimint](https://fedimint.com) |
| [F-07](/fedNuts/F-07.md) | Token state check | [Fedi](https://fedi.xyz), [Mutiny](https://mutinywallet.com) | [Fedimint](https://fedimint.com) |
| [F-08](/fedNuts/F-08.md) | Overpaid Fees | [Fedi](https://fedi.xyz), [Mutiny](https://mutinywallet.com) | [Fedimint](https://fedimint.com) |
| [F-09](/fedNuts/F-09.md) | Deterministic backup and restore | - | - |
| [F-10](/fedNuts/F-10.md) | Spending conditions | [Fedi](https://fedi.xyz) | [Fedimint](https://fedimint.com) |

[py]: https://github.com/cashubtc/cashu
[feni]: https://github.com/cashubtc/cashu-feni
[lnbits]: https://github.com/lnbits/cashu
[cashume]: https://cashu.me
[ns]: https://nutstash.app/
[ts]: https://github.com/cashubtc/cashu-ts
[enuts]: https://github.com/cashubtc/eNuts
[moksha]: https://github.com/ngutech21/moksha
[cashu-crab]: https://github.com/thesimplekid/cashu-crab
[cashu-rs-mint]: https://github.com/thesimplekid/cashu-rs-mint

[00]: 00.md
[01]: 01.md
[02]: 02.md
[03]: 03.md
[04]: 04.md
[05]: 05.md
[06]: 06.md
[07]: 07.md
[08]: 08.md
[09]: 09.md
[10]: 10.md
[11]: 11.md
[12]: 12.md
