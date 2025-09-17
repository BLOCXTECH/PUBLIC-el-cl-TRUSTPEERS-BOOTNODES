# PR Guidelines: Add your Bootnodes & Trust Peers (`script.sh`)

## 📌 Scope

This repository holds **public bootnodes and trust peers** for the BLOCX ecosystem.
All entries live in **`./script.sh`** inside these variables:

- `STATIC_EL_BOOTNODES` (`enode://…`)
- `STATIC_CL_BOOTNODES` (`enr:-…`)
- `STATIC_CL_TRUSTPEERS` (`16Uiu2H…`)

---

## 🚀 How to Contribute

### 1. Fork & clone

```bash
git clone https://github.com/<your-username>/PUBLIC-el-cl-TRUSTPEERS-BOOTNODES.git
cd PUBLIC-el-cl-TRUSTPEERS-BOOTNODES
git checkout -b add-my-node
```

### 2. Edit `script.sh`

- Place your new entry in the correct variable section.
- Keep **one entry per line**, inside quotes.
- Follow ordering (alphabetical or grouped by region if noted).

### 3. Validate

- ✅ **Format:**

  - `enode://<128-hex>@<IP>:<port>`
  - `enr:-…` (full, not truncated)
  - `16Uiu2H…` (peer IDs only)

- ✅ **Reachability:** confirm your node is online.
- ✅ **No duplicates:** check that your entry isn’t already listed.

### 4. Commit & push

```bash
git add script.sh
git commit -m "net: add bootnode/trust peer <short-description>"
git push origin add-my-node
```

### 5. Open PR on GitHub

- Go to [Pull Requests](../../pulls) → **New pull request**.
- Target branch: `main`.
- Use the template below.

---

## 📝 PR Template

**Title**

```
net: add/update bootnodes/trust peers (YYYY-MM-DD)
```

**Description**

```
## Summary
- [ ] Added/updated EL bootnodes (`enode://…`)
- [ ] Added/updated CL bootnodes (`enr:-…`)
- [ ] Added/updated trust peers (`16Uiu2H…`)

---

## Validation
- [ ] My entries follow the correct format
- [ ] My node is online and reachable
- [ ] I confirmed there are no duplicates
- [ ] I edited only `./script.sh`
```

---

## ⚠️ Notes

- These values are **public identifiers only**. They are safe to publish.
- Do not include private keys, secrets, or internal-only IPs.
- Only stable, long-lived nodes should be added.

---
