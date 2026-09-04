# BentoPDF for LazyCat

This repository packages [BentoPDF](https://github.com/alam00000/bentopdf) as a LazyCat LPK v2 application using the upstream self-hosted Simple image.

BentoPDF is the privacy-first PDF toolkit. It provides browser-based tools for editing, converting, merging, splitting, compressing, signing, and organizing PDF documents.

## Automatic publishing

The scheduled workflow discovers stable semantic-version tags from `ghcr.io/alam00000/bentopdf-simple`, verifies the `linux/amd64` image through `ghcr.nju.edu.cn`, creates a versioned GitHub Release asset, and publishes it only to the MiaoMiao private store.

Required GitHub Actions secrets:

- `APPSTORE_URL`
- `APPSTORE_TOKEN`
- `APP_ID` (optional)
- `PRIVATE_STORE_GROUP_CODES` (optional)

## Local build

```bash
lzc-cli project release -o dist/bentopdf.lpk
lzc-cli lpk info dist/bentopdf.lpk
```

## License and attribution

BentoPDF and its branding are provided by the upstream project under AGPL-3.0-only. This packaging repository does not modify the upstream application image.
