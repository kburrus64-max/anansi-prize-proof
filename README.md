# anansi-prize-proof

Public prize payout log for the Anansi arcade games (AnansiData Daily: Star Blaster, Bug Hunt, Slots, Blackjack,
Raffle, Quiz).

[`payouts-extra.json`](payouts-extra.json) lists every prize that has been paid in ANANSI on Base, one object per
paid prize. It is regenerated and pushed automatically after each payout run, and the proof page at
https://anansidata.xyz/payouts.html reads it from:

https://raw.githubusercontent.com/kburrus64-max/anansi-prize-proof/main/payouts-extra.json

## Row format

```json
{"source":"arcade","period":"2026-10-04","game":"Star Blaster","rank":1,"who":"anansidata","address":"0x4B08d9E0C0e0DB53F456Cc72aa46a69584d3f17C","amount":100,"tx":"0x6137fc8e5e2e030409c88bc1432f5f200807f429456e9d72bce8b7e364d41a67"}
```

| Field | Meaning |
|---|---|
| `source` | `arcade` |
| `period` | the game day the prize was won (YYYY-MM-DD) |
| `game` | game name |
| `rank` | leaderboard rank (null if the game has no rank) |
| `who` | the winner's Farcaster username |
| `address` | the winner's Farcaster-verified address the prize was sent to |
| `amount` | whole ANANSI (not wei) |
| `tx` | Base transaction hash; check it at `https://basescan.org/tx/<tx>` |

- Prize wallet: [`0xd6389597bEF5C4d18D9069Bf280164bD2A483c7c`](https://basescan.org/address/0xd6389597bEF5C4d18D9069Bf280164bD2A483c7c#tokentxns)
- Token: ANANSI [`0x4e50a097b37Fb3949733Ce9f7356500b9cc9A702`](https://basescan.org/token/0x4e50a097b37Fb3949733Ce9f7356500b9cc9A702)

Only confirmed on-chain transfers are listed. Every row can be checked independently on BaseScan.
