# pointmadecraps.com

The website for **Point Made: Learn & Play Craps**, the iPhone and iPad app. App Store Connect
needs its privacy policy and support pages, and AdMob reads its `app-ads.txt`.

Plain HTML and one stylesheet: no build step, no JavaScript, no web fonts, nothing loaded from
another site. GitHub Pages serves `main` as it is.

| Path | What it is |
|---|---|
| `/` | Home: what the app is |
| `/support/` | Contact, restoring Pro, the daily allowance, questions |
| `/privacy/` | The privacy policy |
| `/404.html` | Any address that isn't a page |
| `/app-ads.txt` | Tells ad networks which sellers may sell this app's ads: AdMob, publisher `pub-7644660963454743` |
| `CNAME` | The custom domain, for GitHub Pages |
| `.nojekyll` | Serve the files as they are |

## Keeping it true

The privacy policy describes what the app actually does, and has to stay in step with the app's
App Privacy answers in App Store Connect. When the app starts using information in a new way,
change the policy, its "Last updated" date, and those answers together, before that version ships.

The support page quotes the app's numbers (1 free game and 3 free runs a day; 2 credits or 7 runs
per ad). If `AdTuning` changes in the app, change them here too.

## Looking at it locally

```
python3 -m http.server 8123
```

then open http://localhost:8123. The pages link with paths from the root (`/styles.css`), so open
them through a server rather than as files.

## Hosting

GitHub Pages, from `main`, at the root. The domain is on Cloudflare, with DNS records for GitHub
Pages set to "DNS only".
