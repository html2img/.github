<div align="center">

<a href="https://html2img.com">
  <img src="https://html2img.com/og-image.png" alt="HTML to Image" width="640">
</a>

# HTML to Image API

**Convert HTML, CSS or any URL into a PNG with a single API call.**

<a href="https://html2img.com">Website</a> ·
<a href="https://html2img.com/docs">Docs</a> ·
<a href="https://html2img.com/templates">Templates</a> ·
<a href="https://html2img.com/tools">Tools</a> ·
<a href="https://html2img.com/pricing">Pricing</a> ·
<a href="https://html2img.com/compare">Compare</a>

<a href="https://html2img.com"><img src="https://img.shields.io/badge/Free_tier-25_renders_a_month-2563EB" alt="Free tier, 25 renders a month"></a>
<a href="https://html2img.com/docs/getting-started"><img src="https://img.shields.io/badge/Docs-Getting_started-0F172A" alt="Getting started docs"></a>
<a href="https://app.html2img.com/register"><img src="https://img.shields.io/badge/Sign_up-No_card_required-0F172A" alt="Sign up, no card required"></a>

</div>

---

[HTML to Image](https://html2img.com) is a REST API that turns raw HTML and CSS, a live URL, or a named JSON template into a PNG in seconds. Every render runs in real Chrome, so flexbox, grid, custom properties, web fonts and inline JavaScript behave exactly as they do in the browser. The first 25 renders each month are free, with no card required.

This organisation hosts the official client libraries for the API. Watch or star it to get notified when they ship.

## Quick start

Send some HTML, get back a hosted PNG.

```bash
curl -X POST https://app.html2img.com/api/html \
  -H "X-API-Key: YOUR_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{"html": "<h1>Hello world</h1>"}'
```

```json
{
  "success": true,
  "credits_remaining": 95,
  "id": "abc123",
  "url": "https://i.html2img.com/abc123.png"
}
```

Grab a key from your [dashboard](https://app.html2img.com/register), then read the [getting started guide](https://html2img.com/docs/getting-started) and the [authentication docs](https://html2img.com/docs/authentication).

## Three ways to render

| Endpoint | Use it for | Docs |
| --- | --- | --- |
| `POST /api/html` | Your own markup and CSS, full design control | [html parameter](https://html2img.com/docs/parameters/html) |
| `POST /api/screenshot` | Capturing a public URL you already host | [url parameter](https://html2img.com/docs/parameters/url) |
| `POST /api/v1/templates/[slug]` | A tested design, JSON in, PNG out | [browse templates](https://html2img.com/templates) |

The base URL for every endpoint is `https://app.html2img.com`. Full parameter reference is in the [docs](https://html2img.com/docs/parameters).

## What you can build

- **Social media images** such as [Open Graph cards](https://html2img.com/templates/open-graph-image), [Twitter/X posts](https://html2img.com/templates/twitter-post), Instagram squares and stories. [See social templates](https://html2img.com/templates#social)
- **Business documents** such as [invoices](https://html2img.com/templates/invoice-image), [receipts](https://html2img.com/templates/receipt-image), [event tickets](https://html2img.com/templates/event-ticket) and [certificates](https://html2img.com/templates/certificate-of-completion). [See business templates](https://html2img.com/templates#business)
- **Developer assets** such as [code screenshots](https://html2img.com/templates/code-screenshot), [GitHub social previews](https://html2img.com/templates/github-social-preview) and [project showcase cards](https://html2img.com/templates/project-showcase). [See developer templates](https://html2img.com/templates#developer)
- **URL screenshots**, full page or selector cropped, with CSS injection to remove cookie banners and sticky headers before capture. [See screenshot examples](https://html2img.com/docs/examples)

There are [25 named templates](https://html2img.com/templates) in total, covering social, commerce, content and marketing.

## Free browser tools

No sign-up needed. Build an image in the browser, then move to the API when you want to automate it.

- [Open Graph Image Generator](https://html2img.com/tools/open-graph-image)
- [Code Screenshot Generator](https://html2img.com/tools/code-screenshot)
- [Invoice Image Generator](https://html2img.com/tools/invoice-image)
- [Certificate Generator](https://html2img.com/tools/certificate)
- [Twitter Card Generator](https://html2img.com/tools/twitter-card)
- [YouTube Thumbnail Generator](https://html2img.com/tools/youtube-thumbnail)
- [Pinterest Pin Generator](https://html2img.com/tools/pinterest-pin)
- [Quote Card Generator](https://html2img.com/tools/quote-card)

See the full [image generation tools](https://html2img.com/tools) hub.

## Language guides

Worked examples for the seven languages developers reach for most. Anything that can make an HTTP request will work.

[PHP](https://html2img.com/docs/usage/php) ·
[Laravel](https://html2img.com/docs/usage/laravel) ·
[Ruby on Rails](https://html2img.com/docs/usage/rails) ·
[Python](https://html2img.com/docs/usage/python) ·
[JavaScript and Node.js](https://html2img.com/docs/usage/javascript) ·
[React](https://html2img.com/docs/usage/react) ·
[Vue](https://html2img.com/docs/usage/vue)

## Built for production

- **Real Chrome rendering** so your output matches the browser. [Features](https://html2img.com/features)
- **Webhook delivery** for renders that run past the 30 second sync window. [webhook_url docs](https://html2img.com/docs/parameters/webhook-url)
- **DPI control** from 1x to 4x for retina output when you need it. [dpi docs](https://html2img.com/docs/parameters/dpi)
- **Custom fonts** from Google Fonts, Adobe Fonts and self-hosted `@font-face`, all server-side.
- **Global CDN**, with images served from `i.html2img.com`.

## How it compares

Honest, side-by-side notes against the common alternatives, covering pricing, features and migration effort.

- [htmlcsstoimage alternative](https://html2img.com/compare/htmlcsstoimage)
- [Bannerbear alternative](https://html2img.com/compare/bannerbear)
- [Urlbox alternative](https://html2img.com/compare/urlbox)
- [ApiFlash alternative](https://html2img.com/compare/apiflash)
- [All comparisons](https://html2img.com/compare)

## Guides and articles

- [How to generate signed digital certificates at scale](https://html2img.com/articles/how-to-generate-signed-digital-certificates-at-scale/)
- [Dynamic OG images in Astro, Hugo and Eleventy](https://html2img.com/articles/dynamic-og-images-in-astro-hugo-and-eleventy/)
- [How to generate dynamic Open Graph images in Laravel](https://html2img.com/articles/how-to-generate-dynamic-open-graph-images-in-laravel/)
- [Why `@vercel/og` fails on emoji and how to fix it](https://html2img.com/articles/why-vercel-og-fails-on-emoji-and-how-to-fix-it/)
- [All articles](https://html2img.com/articles)

## Official packages

Client libraries are in development and will live here under this organisation.

| Language | Package | Status |
| --- | --- | --- |
| PHP | Composer | In development |
| Laravel | Composer | In development |
| JavaScript and Node.js | npm | In development |
| Python, Ruby and more | | Planned |

Until they land, the API works from any language over HTTP. Start with the [language guides](https://html2img.com/docs/usage).

## Pricing

Start free with 25 renders a month and no card. Paid plans raise the render volume as you grow. See [pricing](https://html2img.com/pricing).

## Links

[Website](https://html2img.com) ·
[Features](https://html2img.com/features) ·
[Templates](https://html2img.com/templates) ·
[Tools](https://html2img.com/tools) ·
[Docs](https://html2img.com/docs) ·
[Compare](https://html2img.com/compare) ·
[Articles](https://html2img.com/articles) ·
[Pricing](https://html2img.com/pricing) ·
[About](https://html2img.com/about) ·
[Contact](https://html2img.com/contact)

---

<div align="center">

Built by the team behind [HTML to Image](https://html2img.com).

<a href="https://app.html2img.com/register">Create a free account</a> ·
<a href="https://app.html2img.com/login">Login</a>

© 2026 HTML to Image

</div>
