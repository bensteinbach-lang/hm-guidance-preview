# Client Preview

A password-protected preview, hosted on GitHub Pages.

The page itself is encrypted (AES-256-GCM, key derived with PBKDF2-SHA256 at 600,000 iterations). Only the ciphertext (`payload.enc.json`) and a small password page (`index.html`) are published. The password is not stored in this repo.

## Rebuild

```
node encrypt.mjs source.html '<password>'
```

Then commit `payload.enc.json`. `source.html` is the plaintext and is never committed.
