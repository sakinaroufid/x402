---
"@x402/core": patch
---

Fixed `x402Facilitator.settle()` running `onAfterSettle` hooks when a scheme returns `success: false`. Failed settlements now run `onSettleFailure` hooks (which can recover), matching how `verify()` handles `isValid: false` and how the Python facilitator handles failed settlements.
