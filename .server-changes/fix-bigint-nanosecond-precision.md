---
area: webapp
type: fix
---

Fix nanosecond timestamps losing precision in retry event records. Previously, converting milliseconds to nanoseconds via float multiplication silently dropped precision above Number.MAX_SAFE_INTEGER; timestamps are now computed with BigInt arithmetic throughout.
