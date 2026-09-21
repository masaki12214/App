# NEXT_EARN — TimCOOKED / masaki12214

**Checked:** 2026-09-22 ~01:10 Asia/Taipei (UTC+8)  
**Wallet:** `0x4C69E9fa61023c39ad9491d82c5c25Cc906bc08e`  
**Constraint:** zero capital / no user ETH ask. Prefer PR/review/text without on-chain gas.

## Snapshot

| Path | Status |
|------|--------|
| Expensify #91935 ($250) | Proposal incomplete; PR #101765 **auto-closed** (not assigned). Melvin asked for Upwork/Expensify details. |
| Superteam agent `timcooked-curved-90` | Registered; `GET .../listings/live` empty / 401 on earn subdomain; public board **1× AGENT_ALLOWED** = Steve Arena ($500) needs trade capital |
| ArcBounty job12 UX | Deliverable ready; needs Arc USDC gas. Circle faucet = **testnet only** (no real $). |
| BountyBook | Oracle broken |
| Phantom | ~$4.23 USDT L1, 0 ETH everywhere |
| Stakely Base | Tweet verified SMA9MB9E, still queued 0 Base ETH |

**Critical Expensify rule:** new contributors = **one job at a time**. Do **not** open PRs until hired. Do **not** spam other HW issues until #91935 resolves.

---

## Top 5 (ranked)

### 1. Expensify App #91935 — Spend default Date sort Desc — **$250** ⭐ TOP PICK
- **URL:** https://github.com/Expensify/App/issues/91935
- **Upwork:** https://www.upwork.com/jobs/~022059919919895211074
- **Why zero-cap:** GitHub proposal + (after hire) PR. No gas.
- **Blockers:** (1) No proper template proposal yet — only a PR link comment. (2) PR auto-closed: not assignee. (3) Need Expensify email + Upwork profile posted. (4) Heavy competition; C+ @rojiphil overdue on selection.
- **TimCOOKED next action:**
  1. Human posts **Contributor details** (Expensify email + Upwork URL) on the issue.
  2. Human posts the ready proposal in `deliverables/PROPOSAL_91935.md` (GitHub PAT cannot comment — 403).
  3. Wait for hire/assignment → then reopen PR from `fix/91935-spend-default-date-sort-asc` (patch already proven).
  4. Do **not** open more Expensify proposals until this is done or rejected.

### 2. Superteam — Spout Finance Product Feedback — **$1000**
- **URL:** https://superteam.fun/earn (search “Spout Finance Product Feedback”; id `ae1041af-2378-4a17-b21f-8d74a4505f96`)
- **Deadline:** ~2026-09-23 22:59 UTC
- **Why zero-cap:** Text UX/product write-up; HUMAN_ONLY listing → human submits, agent drafts.
- **Blockers:** HUMAN_ONLY (no agent API submit). Need Spout app walkthrough / screenshots if required by listing body.
- **TimCOOKED next action:** Finalize `deliverables/SPOUT_FEEDBACK.md`, human submits on Earn before deadline. No gas.

### 3. Superteam — IDEATHON innovative ideas — **$1000**
- **URL:** https://superteam.fun/earn (id `b658d1a3-7bbe-48f4-b95a-3647029ff41b`)
- **Deadline:** 2026-09-21 20:59 UTC (~hours from check; may be expired — verify before spend).
- **Why zero-cap:** Text idea doc; HUMAN_ONLY.
- **Blockers:** Deadline risk; HUMAN_ONLY.
- **TimCOOKED next action:** If still open, draft 1–2 crisp Solana/hackathon ideas → human submit. Else skip.

### 4. Next Expensify HW after #91935 clears — e.g. #99450 / #98624 / #99090
- **URLs:** https://github.com/Expensify/App/issues?q=is%3Aopen+label%3A%22Help+Wanted%22
- **Amount:** usually $75–$500 (title `$`)
- **Why zero-cap:** Proposal-first OSS, no gas.
- **Blockers:** New-contributor one-job rule; most $250s are proposal-flooded.
- **TimCOOKED next action:** After #91935 hire or decline, pick a quiet HW with fewer strong proposals; post template proposal only (no PR).

### 5. ArcBounty job12 UX review — ~1 USDC (likely **testnet / not real income**)
- **URL:** https://arcbounty.app + local deliverable under `earn-bounty/arc-ux/`
- **Why “zero-cap” prep:** Review MD already written offline.
- **Blockers:** Needs Arc USDC gas to take/submit. Circle faucet = Arc **Testnet** USDC (no monetary value). Mainnet still 0.
- **TimCOOKED next action:** Keep deliverable warm; only take if real mainnet USDC appears without user funding. Do not prioritize over #1–2.

---

## Explicitly blocked / skip now

- **Steve Agent Arena $500 (AGENT_ALLOWED):** needs ≥20 USDC trades ×5 + X + XP — no capital.
- **Frantic Ausca / Base USDC apps:** need Base USDC.
- **BountyBook:** oracle `code_test`/`ipfs_fetch` broken.
- **Algora public API:** HTML/406 from this host; board showed no useful open set.
- **AsyncAPI bounty:** assignment/mutex mentorship — not open claim.
- **SmolRefuel / L1 USDT→gas:** unproven; prior API 500; may burn $4.23.

---

## Started this run

1. Confirmed PR #101765 closed reason (not assigned).
2. Confirmed masaki12214 comment on #91935 is **not** a valid proposal template.
3. Drafted proper proposal → `deliverables/PROPOSAL_91935.md` (post manually; API 403).
4. Drafted Spout feedback → `deliverables/SPOUT_FEEDBACK.md`.
5. Attempted Superteam live agent listings (auth/empty).
6. Wrote this file (also mirrored on branch `earn/next-earn-meta` if workspace write failed).

## Human checklist (no ETH ask)

- [ ] Post Expensify + Upwork contributor details on #91935
- [ ] Paste PROPOSAL_91935.md as issue comment
- [ ] Submit Spout feedback on Superteam Earn before deadline
- [ ] After hire on #91935: reopen fix PR (helper already in closed PR diff)
