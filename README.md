# ctf-btc-tx

A tiny static site that serves a fake-looking Bitcoin transaction page and a JSON endpoint,
useful for CTF tasks where a bot naively checks for a txid in the URL and an address + amount in the content.

- HTML: `/tx/73793dc7bbb60ec09c884fc23c4472bb7140453213b3e95ecac76950f1d7f68b/` (or without trailing slash)
- JSON: `/api/tx/73793dc7bbb60ec09c884fc23c4472bb7140453213b3e95ecac76950f1d7f68b.json`

## Quick Deploy (GitHub Pages)
1. Create a new public repository, e.g. `ctf-btc-tx`.
2. Upload the contents of this folder to the repository root.
3. Go to **Settings → Pages**. Under **Build and deployment**, set **Source** to **Deploy from a branch**.
4. Choose the `main` branch and the `/ (root)` folder. Save.
5. The site will be available at `https://<username>.github.io/ctf-btc-tx/`.
6. Your bot-facing URL will be:
   - `https://<username>.github.io/ctf-btc-tx/tx/73793dc7bbb60ec09c884fc23c4472bb7140453213b3e95ecac76950f1d7f68b`
   - or JSON: `https://<username>.github.io/ctf-btc-tx/api/tx/73793dc7bbb60ec09c884fc23c4472bb7140453213b3e95ecac76950f1d7f68b.json`

## Notes
- The address is hardcoded: `bc1qrjt8umwlgn4zpjjfqm6duk2wqartzpf8a4pme8`.
- The amount is **100.00000000 BTC** (10,000,000,000 sats).
- If your validator dislikes the trailing slash, use the path without it.
