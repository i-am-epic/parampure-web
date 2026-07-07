# parampure-web

Public marketing site for **ParamPure** — a B2B ordering app that connects
tea stalls, cafes, and restaurants with verified wholesale beverage
suppliers (tea, coffee, dairy, sugar, disposables), with bulk-tier
pricing, GST-compliant invoicing, and next-day delivery.

This site exists primarily so ParamPure's app-store and OAuth/Firebase
branding review has a real, ownable homepage that explains what the app
does and links to its Privacy Policy and Terms of Service.

## Structure

Plain static HTML/CSS — no build step, no framework, deployable as-is.

```
index.html     Homepage — what ParamPure is, features, buyer/seller roles
privacy.html   Privacy Policy (mirrors the in-app copy)
terms.html     Terms of Service (mirrors the in-app copy)
assets/        Logo, favicon, shared stylesheet
```

## Local preview

```bash
python3 -m http.server 8080
# open http://localhost:8080
```

## Deploying

Deployed via Vercel (zero-config static site). To point a custom domain
at it and satisfy Google's home-page-ownership check, add the domain in
the Vercel project's Domains settings and verify it via the DNS TXT
record Vercel provides, or verify the URL directly in
[Google Search Console](https://search.google.com/search-console).

## Editing legal copy

`privacy.html` and `terms.html` are kept in sync with
`lib/features/legal/presentation/legal_screen.dart` in the main
[parampure](https://github.com/i-am-epic/parampure) app repo — update
both places together.
