# kefigen.com

The Kefigen studio site: one static page (plain HTML and CSS, no build step, no scripts, no third-party requests), published with GitHub Pages at `kefigen.com`.

## Preview locally

```bash
python3 -m http.server 8788
```

Then open http://localhost:8788/.

## Publish

GitHub Pages serves the `main` branch root. `CNAME` holds the custom domain, so every push to `main` deploys.

DNS (Cloudflare, zone `kefigen.com`), **DNS only** (grey cloud) so GitHub can issue the certificate:

| Type | Name | Content |
| --- | --- | --- |
| A | `@` | `185.199.108.153` |
| A | `@` | `185.199.109.153` |
| A | `@` | `185.199.110.153` |
| A | `@` | `185.199.111.153` |
| CNAME | `www` | `danreyes.github.io` |

Then in the repository: Settings → Pages → confirm the custom domain shows a green tick and turn on **Enforce HTTPS**. The orange-cloud proxy can be turned on afterwards if wanted.

## Art

The hero and screenshots are Rig King's own key art and Mac-build captures, copied from the `rig-king` repository's `site/assets/`.
