# OpenAgriX — Crypto World's Fair track

**Proof of Agriculture on Solana**

This repository is the submission. It is the two-page pitch. The working prototype is the live app below.

| | |
|---|---|
| Live prototype | https://openagrix.com |
| Product code | https://github.com/openagrix/OpenAgri-Living-Matrix |
| Colosseum project | https://colosseum.com/arena/projects/openagri |
| Devnet program | https://explorer.solana.com/address/2pcucTtxUGkNidFi48ioK8oLaUSCcMH3QEabA8QasGsL?cluster=devnet |
| X | https://x.com/OpenAgriX |
| Contact | Telegram `lieulieunft` · hello@openagrix.com |

**Founder:** Nguyen Thi Lieu, Ho Chi Minh City, Vietnam.  
**Eligibility:** Vietnam-based. ID or residence proof can be shown before any prize is paid.  
**Product:** Vietnamese and English. **Network:** Solana Devnet only.

---

## Page 1 — The business today, and why onchain

### The business today

OpenAgriX is the onchain version of the lot dossier Vietnamese farms and exporters already keep in Excel, PDF, and email.

The break is not a missing token. A buyer outside Vietnam will not trust a file the sender can still edit. Organic and origin paperwork can cost a lot and still be disputed at the border. For a small farm or cooperative, the failure mode is a lost order.

We record evidence for farms, cooperatives, exporters, and the buyer who has to check one lot. We do not turn crops into tradable assets.

In September 2026 we sat with Agricultural Cooperative in Chau Duc Commune, and with the Director of the Center for Sustainable Economic Development. The subject was a customer path for agricultural digital transformation and export, built with local cooperatives. That was a working session. It is not a signed pilot, not a paid customer, and not revenue.

### Why onchain

A private database still asks the buyer to trust OpenAgriX. Solana does not.

The farm submits a standardized JSON dossier. The chain stores the SHA-256 hash and a short summary, not the raw file. After that write, the farm, OpenAgriX, and a middleman cannot quietly change the record. The buyer recomputes the hash from the file they received and compares it with the account on Devnet. No wallet is required to read public evidence. The evidence account belongs to the farm account, not to a row only we can edit.

Solana fits because one season produces many small writes, fees stay low, and Phantom is already familiar to builders in Vietnam. A subscription quote on the pricing page can be paid in Devnet USDC, or in SOL using the Chainlink SOL/USD feed.

If a database were enough, we would not enter. The part that needs a chain is cross-border verification without a trusted intermediary.

**Limits, on purpose**

- Devnet only. This is not Mainnet and not a legal certification.
- The raw dossier stays off-chain. Only the hash and summary fields are public.
- Payments can settle onchain. Some subscription state is still kept in the browser.
- The honey lab feed used by the Chainlink CRE demo is our fixture, not an independent laboratory.
- Nothing has been sold.

---

## Page 2 — How it works, and what is next

### How it works

1. Connect Phantom on Devnet.
2. Register a farm account (PDA: farm, owner, farm id).
3. Submit evidence. Types include harvest, soil, carbon, biodiversity, honey quality, and produce quality. `dataHash` is SHA-256 of the standardized JSON. Optional fields cover quantity, unit, event time, and an IPFS CID.
4. A buyer opens https://openagrix.com/explore, a verify link, or Solana Explorer. No account is required to read public evidence.

**Already clickable:** home, farm registration, evidence submit, public explorer, evidence guides (including an agarwood / CITES-shaped sample), pricing, and Devnet USDC or SOL payment.

**Program:** `openagri_evidence` · `2pcucTtxUGkNidFi48ioK8oLaUSCcMH3QEabA8QasGsL`  
**Stack:** Next.js 14 · Anchor 0.30 · Phantom · Chainlink SOL/USD on Devnet

A separate Chainlink CRE workflow can score one stingless-bee honey fixture and publish a hash plus a verdict. That broadcast is a simulated CRE run, not proof of a production enclave. Our own attestation program is in the product repository. The Phase 1 public write used the CRE docs receiver because the local BPF toolchain could not build that program.

### What is next

With a working session and a small team, the next steps are:

1. Keep this Devnet demo public. Record a real lot only when a cooperative agrees to a scoped trial.
2. Move subscription entitlements out of browser storage into a durable registry.
3. Review the hash schema with one exporter, then take counsel on personal data and payments. Mainnet comes after that, not before.
4. Replace the mock honey lab with a source the buyer does not have to take from us.
5. Use a Country Lead session to test whether the verify step actually shortens a buyer's questions.

The business can grow as grower subscriptions and buyer-side verify packs. The prices are on https://openagrix.com so the flow can be tried on Devnet. No invoice has been paid.

### Who is behind it

Nguyen Thi Lieu builds this in Ho Chi Minh City, from Vietnam's export paperwork, not as a generic chain demo. The product is public. The chain accounts are public. The claims above stop where the evidence stops.

**Proof of Agriculture on Solana. Written once. Checked by the buyer.**
