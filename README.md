# Anansi Arcade — Verified High-Score Challenge & Public Payout Log

🎮 **Play Free in the Farcaster Arcade:** [anansidata-miniapp.vercel.app](https://anansidata-miniapp.vercel.app)  
🧩 **Daily Live-Data Riddle:** [anansidata.xyz/r](https://anansidata.xyz/r)  
📜 **Live On-Chain Proof Page:** [anansidata.xyz/payouts.html](https://anansidata.xyz/payouts.html)

## How the High-Score Challenge Works

Play **Star Blaster**, **Bug Hunt**, **Blackjack**, **Slots**, and the **60-Second Speed Quiz** free every UTC day at **[anansidata-miniapp.vercel.app](https://anansidata-miniapp.vercel.app)** (no purchase, fee, or deposit ever required):

- **Server-Verified Anti-Cheat:** Every skill game session (`Star Blaster` and `Bug Hunt`) issues an HMAC-signed seed at start and deterministically replays the player's frame-by-frame input log on the server before recording a score on the leaderboard.
- **Rank #1 High-Score Prizes (starting soon — see [Official Rules](https://anansidata.xyz/r/rules.html)):**
  - **Daily #1 High Score:** **$1 USDC + 1,000 ANANSI** on Base (minimum 3 distinct players per day; rolls into the weekly pot if fewer than 3 play).
  - **Weekly #1 High Score:** **$5 USDC (+ any daily rollover) + 10,000 ANANSI** on Base.
- **Team Exclusion:** Sponsor and team accounts (`@anansidata` and team wallets) are automatically excluded from prize eligibility so 100% of prizes go to outside players.

---

## Public Payout Feed (`payouts-extra.json`)

[`payouts-extra.json`](payouts-extra.json) lists every prize paid on Base, one object per confirmed transfer. It is regenerated and pushed automatically after each payout run, and the proof page at [anansidata.xyz/payouts.html](https://anansidata.xyz/payouts.html) reads it from:

https://raw.githubusercontent.com/kburrus64-max/anansi-prize-proof/main/payouts-extra.json

### Row format

```json
{"source":"arcade","period":"2026-10-04","game":"Star Blaster","rank":1,"who":"anansidata","address":"0x4B08d9E0C0e0DB53F456Cc72aa46a69584d3f17C","amount":100,"tx":"0x6137fc8e5e2e030409c88bc1432f5f200807f429456e9d72bce8b7e364d41a67"}
```

| Field | Meaning |
|---|---|
| `source` | `arcade` |
| `period` | the game day the prize was won (YYYY-MM-DD) |
| `game` | game name (`Star Blaster`, `Bug Hunt`, `Quiz`, etc.) |
| `rank` | leaderboard rank (`1` = #1 daily high score) |
| `who` | the winner's Farcaster username |
| `address` | the winner's Farcaster-verified address the prize was sent to |
| `amount` | whole ANANSI (not wei) |
| `tx` | Base transaction hash; verify at `https://basescan.org/tx/<tx>` |

- **Active Prize Wallet (v2):** [`0x134d3A5BEE3D57dcDE2F7Ff6b0526f0442bbdf55`](https://basescan.org/address/0x134d3A5BEE3D57dcDE2F7Ff6b0526f0442bbdf55)
- **Retired v1 Wallet (Oct 4–5 test payouts):** [`0xd6389597bEF5C4d18D9069Bf280164bD2A483c7c`](https://basescan.org/address/0xd6389597bEF5C4d18D9069Bf280164bD2A483c7c#tokentxns)
- **Token:** ANANSI [`0x4e50a097b37Fb3949733Ce9f7356500b9cc9A702`](https://basescan.org/token/0x4e50a097b37Fb3949733Ce9f7356500b9cc9A702) · Base USDC [`0x833589fCD6eDb6E08f4c7C32D4f71b54bdA02913`](https://basescan.org/token/0x833589fCD6eDb6E08f4c7C32D4f71b54bdA02913)

Only confirmed on-chain transfers are listed. Every row can be checked independently on BaseScan.
