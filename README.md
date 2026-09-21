# Reanimated Dead × Neo X Reference Integration

This repository is the planned public home for the Neo X integration components proposed for **Reanimated Dead**, a live browser-based trading card game.

**Project:** Reanimated Dead  
**Live game:** https://www.reanimateddead.com  
**Network:** Neo X  
**Status:** Proposed / pre-development  
**Grant track:** Neo X Elevate — Genesis

## About Reanimated Dead

Reanimated Dead is a free-to-play browser trading card game built around gameplay first and optional digital ownership.

Players can play without cryptocurrency, a wallet, or an NFT.

The live game currently supports:

- Solo and multiplayer gameplay
- Optional Ethereum NFT utility
- Optional Solana NFT utility
- Stripe and Ethereum purchases
- Player profile badges
- Digital and physical collectible development

Additional cosmetics, emoji/reactions, owner-driven lore, tournaments, and spectator functionality are in development or testing.

## Proposed Neo X Integration

The proposed Neo X work will add an optional Neo X commerce and ownership layer to the existing game.

The planned integration includes:

- Neo X purchase flows for selected game products
- Secure wallet-to-account linking
- Server-side transaction verification
- Retry-safe and idempotent game fulfillment
- Selected player-owned badges and cosmetics
- Earned competitive collectibles
- An approved owner-driven lore/version path
- Ownership reconciliation
- Production instrumentation and reporting
- A public competitive activation using Neo X-enabled awards

Existing Ethereum and Solana functionality will remain supported.

Core gameplay will remain off-chain and wallet-optional.

## Planned Public Components

Subject to final grant scope and development, this repository is intended to contain the separable Neo X components created through the proposed integration, including:

- Grant-specific Neo X smart contracts
- Reference commerce and fulfillment adapter
- Wallet/account verification interfaces
- Event and entitlement interfaces
- Example integration code
- Automated tests
- Deployment examples
- Recovery and operational documentation
- Technical implementation notes
- Production case-study findings

The goal is to provide other developers with a practical reference for connecting Neo X commerce and ownership to a conventional game backend.

## Proposed Architecture

At a high level:

Player / Wallet
        |
        v
Neo X Transaction or Asset
        |
        v
Neo X Verification Layer
        |
        v
Reanimated Dead Ownership / Fulfillment Adapter
        |
        v
Game Account Entitlement
        |
        v
Player-Usable Item, Cosmetic, Achievement, or Reward

The integration is intended to keep blockchain verification separate from core game execution.

A blockchain transaction or owned asset can establish an eligible entitlement, while Reanimated Dead remains responsible for gameplay rules, authorization, moderation, and the player experience.

## Commerce Design Goals

The proposed commerce implementation is intended to demonstrate the complete path from a blockchain payment to usable game content.

Planned safeguards include:

- Order-specific payment authorization
- Chain and contract validation
- Amount verification
- Replay protection
- Duplicate-event protection
- Idempotent entitlement issuance
- Durable recovery after interrupted processing
- Transaction and fulfillment status tracking

Production measurements are expected to distinguish blockchain confirmation from backend verification and game-item fulfillment.

## Player Ownership

The initial proposed release is expected to include a limited set of Neo X-enabled player assets rather than moving the entire Reanimated Dead collection to Neo X.

The proposed scope includes:

- Four selected badge/cosmetic templates
- Two competitive award templates
- One approved owner-driven lore/version path

These quantities describe the proposed grant scope and may be refined through technical review and final milestone agreement.

## Owner-Driven Lore

Reanimated Dead is developing a system in which owners of supported assets can contribute approved lore associated with those assets.

For the proposed Neo X implementation:

1. An eligible owner proves control of a supported asset.
2. Lore follows defined submission and approval rules.
3. An approved version can be associated with the asset.
4. Reanimated Dead can recognize that approved state.
5. Any resulting in-game effect remains bounded by the game's rules.

Arbitrary owner-authored text will not execute directly as game logic.

## Competitive Integration

Reanimated Dead is actively testing tournament and spectator functionality.

The proposed Neo X integration is intended to support selected competitive achievements and awards, culminating in a public competitive activation.

Blockchain ownership will not be required to participate in ordinary gameplay.

## Open-Source Boundary

This repository is intended for the **separable Neo X integration components** developed under the proposed project.

It is **not** the source repository for the Reanimated Dead game.

The following remain proprietary and are not intended to be published here:

- Reanimated Dead game source code
- Characters and artwork
- Card designs and game content
- Proprietary gameplay systems
- Private backend systems
- Player/account data
- Commercial infrastructure
- Reanimated Dead brand and other intellectual property

Any final open-source scope and license will follow the applicable grant agreement and third-party license requirements.

## Current Status

This repository was created in preparation for the proposed Neo X integration.

**No Neo X production deployment is claimed at this time.**

Development artifacts, contracts, tests, documentation, and release information will be added here if and as the proposed work proceeds.

## Team

### Joshua Kassabian
Technical Lead

Software architecture, game development, blockchain and payment integrations, production systems, and technical delivery.

### Jeff Vongore
Creative & Product Lead

Game/product development, art, collectibles, physical-product direction, player experience, and distribution.

The team has worked together for approximately four years across cryptocurrency, NFTs, digital products, and Reanimated Dead.

## Links

**Play Reanimated Dead:**  
https://reanimateddead.com

**Neo X:**  
https://x.neo.org/

---

Reanimated Dead is an independent project. References to Neo X in this repository describe a proposed integration and should not be interpreted as an endorsement, partnership, or grant award unless explicitly announced by the relevant parties.
