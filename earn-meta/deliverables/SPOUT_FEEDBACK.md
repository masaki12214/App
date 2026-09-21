# Spout Finance — Product Feedback (draft for Superteam Earn)

**Listing:** Spout Finance Product Feedback · **$1000** · HUMAN_ONLY  
**Product:** https://www.spout.finance/ — borrow stables at 0% against tokenized US equities; lenders earn covered-call premium.  
**Submitter:** masaki12214 / TimCOOKED (human must submit on Earn)  
**Wallet (if asked):** `0x4C69E9fa61023c39ad9491d82c5c25Cc906bc08e`

> Paste into Superteam submission. Adjust if the listing asks for screenshots, a form, or a Loom — attach those separately.

---

## 1. Who I am / how I used Spout

I reviewed Spout as a Solana DeFi user who holds (or wants to hold) tokenized US equities and needs liquidity **without selling**. I walked the public product narrative (borrower vs lender), KYC/custody story, LTV, weekly covered-call cycle, and risk copy on spout.finance.

Goal of this feedback: make first-session comprehension and trust high enough that a cautious equity holder completes KYC → deposit → borrow (or lend) without bouncing.

---

## 2. What works well

1. **Clear core promise:** “0% interest borrow vs tokenized US stocks” is memorable and differentiated vs Aave-style interest markets.
2. **Honest second-order risk:** Explaining that borrowers absorb ITM covered-call outcomes (~0.5% hist. annualized framing) is better than hiding options risk.
3. **Lender yield source is named:** Variance risk premium / covered calls / JEPI-like mental model helps sophisticated users.
4. **Compliance posture is front-and-center:** FINRA broker-dealer custody, PoR, KYC — necessary for US equities narrative.
5. **No lockup messaging** for repay/withdraw reduces “DeFi hotel California” fear.

---

## 3. Friction & confusion (prioritized)

### P0 — Trust & risk comprehension before KYC
- **Issue:** Marketing leads with “0% interest,” but the economically material borrower cost is **options opportunity / assignment path**, not APR. First-time users may think “free leverage.”
- **Ask:** Above-the-fold borrower module: `Interest APR: 0%` + `Estimated cycle cost (hist.): ~X%` + link “How covered calls affect you.”
- **Why it pays:** Fewer angry support tickets; higher quality KYC completions.

### P0 — Collateral eligibility wall
- **Issue:** Only 11 tickers at launch. Users will connect wallet, KYC, then discover their equity isn’t supported.
- **Ask:** Pre-KYC “Supported assets” checklist + “Request an asset” form. Show chain/token mint IDs for each.

### P1 — Dual-sided IA (Borrow vs Lend) mixing
- **Issue:** One page sells both sides; a borrower scanning lender APY may mis-click supply flow.
- **Ask:** Persistent mode toggle (`I want to borrow` / `I want to earn`) that restyles CTAs and hides opposite-side numbers by default.

### P1 — Weekly cycle opacity
- **Issue:** “Weekly cycles” is mentioned, but UI impact (when can I repay without waiting? what happens mid-cycle?) is easy to miss.
- **Ask:** Borrower dashboard card: `Current cycle ends: <date/time UTC>` · `Repay anytime: Yes/No + caveat` · `Next reconstitution: …`

### P1 — Liquidation / 200% collateralization literacy
- **Issue:** 50% LTV + 200% collateralization + VIX regime + insurance fund is a lot; order of failure modes is unclear.
- **Ask:** One diagram: price ↓ → warnings → partial liquidations → insurance → lender principal. Use plain language, not whitepaper tone.

### P2 — Proof of Reserve discoverability
- **Issue:** PoR is claimed but not obviously one-click from the app shell.
- **Ask:** Footer + dashboard badge: `PoR last verified <timestamp>` → explorer/attestation.

### P2 — Mobile / wallet deep links
- **Issue:** Solana wallet + KYC + deposit is a multi-app hop; drop-off risk is high on mobile.
- **Ask:** Explicit “Best on desktop for first KYC” banner, or guided mobile deep-link checklist (wallet → browser → return).

---

## 4. Concrete UX recommendations (ship-sized)

| # | Change | Effort | Impact |
|---|--------|--------|--------|
| 1 | Borrower cost strip (0% APR + hist. cycle cost) | S | Trust |
| 2 | Supported-assets gate before KYC | S | Conversion |
| 3 | Borrow/Lend mode toggle | M | Error rate |
| 4 | Cycle countdown card | S | Clarity |
| 5 | Liquidation storyboard modal | M | Support load |
| 6 | PoR live badge | S | Trust |
| 7 | “What if VIX spikes?” FAQ accordion on borrow confirm | S | Retention |

---

## 5. Copy nits

- Prefer **“No interest charged by Spout”** over bare **“0% interest”** when options drag exists.
- Replace vague **“double-digit APY”** for lenders with a range + as-of date + “not guaranteed.”
- On repay CTA: **“Repay stablecoin debt → unlock collateral”** beats generic Confirm.

---

## 6. Metrics I’d watch after changes

- KYC start → deposit success rate
- Deposit → first borrow rate
- Time-to-first-borrow
- Support tickets tagged `interest` / `call assignment` / `unsupported asset`
- Lender deposit retention across 4 weekly cycles

---

## 7. Nice-to-have product ideas (out of immediate UX scope)

1. **Read-only portfolio simulator:** paste holdings → show which are borrowable + max stablecoin at 50% LTV before KYC.
2. **Per-asset call shortbook transparency:** strike, expiry, % of collateral covered this week.
3. **Borrower “covered call pause” request** during known binary events (earnings) — even if answer is no, explain why.

---

## 8. Closing

Spout’s economic design is differentiated; the product risk is **expectation management**, not lack of yield story. Tighten pre-KYC asset gating, make borrower cost legible next to “0%,” and separate Borrow/Lend IA — that unlocks the narrative you already earned with custody + PoR.

Happy to iterate if the listing wants a Loom walkthrough or annotated screenshots of a specific build.
