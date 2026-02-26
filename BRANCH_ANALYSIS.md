# Branch Analysis: Does `main` Include `1.6`?

## Summary

**Yes — branch `1.6` has been fully incorporated into `main`.**

---

## Evidence

### 1. Commit Ancestor Check

The tip commit of `1.6` appears directly in `main`'s commit history:

| Branch | Tip Commit SHA | Commit Message |
|--------|---------------|----------------|
| `1.6`  | `16e1373ac320420b31f9fdb2cbe526312ffcab36` | "Assemblies" (2025-07-12) |
| `main` | `06b854ef484b01e19dd7e2b9380b824737db0009` | "Create LICENSE" (2025-07-31) |

Walking `main`'s ancestry, commit `16e1373` ("Assemblies") — which is the **tip of `1.6`** — appears as an ancestor of `main`. This proves that every commit reachable from `1.6` is also reachable from `main`.

### 2. Explicit Merge Commit in `main`

`main` contains a merge commit that explicitly records the incorporation of `1.6`:

```
commit 510d608796e39d3944e2d3b08fa1d131fb938182
Date:   2025-07-23

    Merge pull request #1 from Taranchuk/1.6

    1.6 fix
```

This merge commit was created on **2025-07-23**, after which `main` also received an additional commit (`9bf97d90` — "1.6 fix" from Scorpiopt) and finally `06b854ef` ("Create LICENSE" on 2025-07-31).

### 3. Commit Comparison (`1.6` vs `main`)

All commits unique to `1.6` relative to their common ancestor are present in `main`:

| Commit | Message | In `main`? |
|--------|---------|-----------|
| `16e1373` | Assemblies (2025-07-12) | ✅ Yes |
| `69f1d66` | Version 1.6 (2025-07-12) | ✅ Yes |

There are **zero commits** in `1.6` that are absent from `main`.

---

## Conclusion

Branch `1.6` is an **ancestor** of `main`. All commits from `1.6` are included in `main`'s history, as confirmed by:

1. The `1.6` tip commit (`16e1373`) appearing in `main`'s commit log.
2. An explicit merge commit (`510d608`) in `main` recording the merge of `1.6`.

`1.6` has been **fully incorporated** into `main`.
