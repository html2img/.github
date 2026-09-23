<div align="center">

<a href="https://html2img.com">
  <img src="https://html2img.com/og-image.png" alt="HTML to Image API" width="640">
</a>


<h1><a href="https://html2img.com">HTML to Image API</a></h1>

**Convert HTML, CSS or any URL into a PNG or PDF with a single API call.**

<a href="https://html2img.com">Website</a> ·
<a href="https://html2img.com/docs">Docs</a> ·
<a href="https://html2img.com/integrations">Integrations</a> ·
<a href="https://html2img.com/templates">Templates</a> ·
<a href="https://html2img.com/tools">Tools</a> ·
<a href="https://html2img.com/pricing">Pricing</a> ·
<a href="https://html2img.com/compare">Compare</a>

<a href="https://html2img.com/pricing"><img src="https://img.shields.io/badge/Free_tier-50_credits_on_sign_up-2563EB" alt="Free tier, 50 credits on sign up"></a>
<a href="https://html2img.com/docs/getting-started"><img src="https://img.shields.io/badge/Docs-Getting_started-0F172A" alt="Getting started docs"></a>
<a href="https://app.html2img.com/register"><img src="https://img.shields.io/badge/Sign_up-No_card_required-0F172A" alt="Sign up, no card required"></a>

</div>

---

[HTML to Image](https://html2img.com) is a REST API that turns raw HTML and CSS, a live URL, or a named JSON template into a PNG or an A4 PDF in seconds. Every render runs in real Chrome, so flexbox, grid, custom properties, web fonts and inline JavaScript behave exactly as they do in the browser. Every new account gets 50 free credits up front, with no card required.

This organisation hosts the official libraries for the API: SDKs for [PHP](https://github.com/html2img/html2img-php), [JavaScript and TypeScript](https://github.com/html2img/html2img-js), [Python](https://github.com/html2img/html2img-python) and [Ruby](https://github.com/html2img/html2img-ruby), framework packages for [Laravel](https://github.com/html2img/html2img-laravel) and [Django](https://github.com/html2img/html2img-django), Open Graph image plugins for [WordPress](https://github.com/html2img/wordpress), [Statamic](https://github.com/html2img/statamic-og-images) and [Craft CMS](https://github.com/html2img/html2img-craft), and a [GitHub Action](https://github.com/html2img/action). All of them are available now.

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
  "id": "abc123",
  "url": "https://i.html2img.com/abc123.png",
  "credits_remaining": 49,
  "expires_at": "2026-09-30T10:00:00+00:00"
}
```

`expires_at` is set on free-tier renders, which are hosted for 7 days. On any paid plan it is `null` and the render is kept permanently.

Grab a key from your [dashboard](https://app.html2img.com/register), then read the [getting started guide](https://html2img.com/docs/getting-started) and the [authentication docs](https://html2img.com/docs/authentication).

## Three ways to render

| Endpoint | Use it for | Docs |
| --- | --- | --- |
| `POST /api/html` | Your own markup and CSS, full design control | [html parameter](https://html2img.com/docs/parameters/html) |
| `POST /api/screenshot` | Capturing a public URL you already host | [url parameter](https://html2img.com/docs/parameters/url) |
| `POST /api/v1/templates/[slug]` | A tested design, JSON in, PNG out | [browse templates](https://html2img.com/templates) |

The base URL for every endpoint is `https://app.html2img.com`. Full parameter reference is in the [docs](https://html2img.com/docs/parameters).

Need a PDF instead? Set `"format": "pdf"` on an HTML or screenshot render and you get back an A4 vector PDF with selectable text, embedded web fonts and automatic pagination. It costs one credit, the same as an image. See the [HTML to PDF API](https://html2img.com/html-to-pdf/) and the [format parameter](https://html2img.com/docs/parameters/format).

## What you can build

- **Social media images** such as [Open Graph cards](https://html2img.com/templates/open-graph-image), [Twitter/X posts](https://html2img.com/templates/twitter-post), Instagram squares and stories. [See social templates](https://html2img.com/templates#social)
- **Business documents** such as [invoices](https://html2img.com/templates/invoice-image), [receipts](https://html2img.com/templates/receipt-image), [event tickets](https://html2img.com/templates/event-ticket) and [certificates](https://html2img.com/templates/certificate-of-completion), as PNGs or as PDFs. [See business templates](https://html2img.com/templates#business)
- **Developer assets** such as [code screenshots](https://html2img.com/templates/code-screenshot), [GitHub social previews](https://html2img.com/templates/github-social-preview) and [project showcase cards](https://html2img.com/templates/project-showcase). [See developer templates](https://html2img.com/templates#developer)
- **URL screenshots**, full page or selector cropped, with CSS injection to remove cookie banners and sticky headers before capture. [See the Screenshot API](https://html2img.com/screenshot-api/)
- **PDFs** of reports, invoices and any live web page. [See the HTML to PDF API](https://html2img.com/html-to-pdf/)

There are [25 named templates](https://html2img.com/templates) in total, covering social, business, content, developer and real estate.

## Official packages

Every package below is published and maintained here. Anything else works over plain HTTP.

### SDKs

| Language | Install | Repo | Registry |
| --- | --- | --- | --- |
| PHP | `composer require html2img/html2img-php` | [html2img-php](https://github.com/html2img/html2img-php) | [Packagist](https://packagist.org/packages/html2img/html2img-php) |
| JavaScript and TypeScript | `npm install @html2img/client` | [html2img-js](https://github.com/html2img/html2img-js) | [npm](https://www.npmjs.com/package/@html2img/client) |
| Python | `pip install html2img-client` | [html2img-python](https://github.com/html2img/html2img-python) | [PyPI](https://pypi.org/project/html2img-client/) |
| Ruby | `bundle add html2img-client` | [html2img-ruby](https://github.com/html2img/html2img-ruby) | [RubyGems](https://rubygems.org/gems/html2img-client) |

### Frameworks

| Framework | Install | Repo | Registry |
| --- | --- | --- | --- |
| Laravel | `composer require html2img/html2img-laravel` | [html2img-laravel](https://github.com/html2img/html2img-laravel) | [Packagist](https://packagist.org/packages/html2img/html2img-laravel) |
| Django | `pip install html2img-django` | [html2img-django](https://github.com/html2img/html2img-django) | [PyPI](https://pypi.org/project/html2img-django/) |

### CMS plugins

Automatic Open Graph images for every post or entry, regenerated only when something on the card changes.

| CMS | Install | Repo | Listing |
| --- | --- | --- | --- |
| WordPress | Install from [wordpress.org/plugins/html2img](https://wordpress.org/plugins/html2img/) | [wordpress](https://github.com/html2img/wordpress) | [WordPress.org](https://wordpress.org/plugins/html2img/) |
| Statamic | `composer require html2img/statamic-og-images` | [statamic-og-images](https://github.com/html2img/statamic-og-images) | [Packagist](https://packagist.org/packages/html2img/statamic-og-images) |
| Craft CMS | `composer require html2img/craft-og-images` | [html2img-craft](https://github.com/html2img/html2img-craft) | [Craft Plugin Store](https://plugins.craftcms.com/og-images) |

### Automation and AI

| Integration | Use it | Repo | Listing |
| --- | --- | --- | --- |
| GitHub Action | `uses: html2img/action@v1` | [action](https://github.com/html2img/action) | [GitHub Marketplace](https://github.com/marketplace/actions/html-to-image) |
| MCP server | Render images from Claude, Cursor and other MCP clients (paid plans) | | [Setup guide](https://html2img.com/mcp/) · [Smithery](https://smithery.ai/servers/html2img/html2img) |

See every integration, with setup guides, on the [integrations hub](https://html2img.com/integrations).

## Quick examples

### PHP

Framework-agnostic, built on Guzzle, returns a typed response object. Requires PHP 8.3+.

```php
use Html2img\Html2imgClient;
use Html2img\Request\HtmlRequest;

$client = new Html2imgClient('your-api-key');

$response = $client->html(new HtmlRequest(
    html: '<!doctype html><html><body><h1>Hello</h1></body></html>',
    width: 1200,
    height: 630,
));

echo $response->url; // https://i.html2img.com/abc123def456.png
```

See the [PHP SDK readme](https://github.com/html2img/html2img-php) and the [PHP guide](https://html2img.com/integrations/php/).

### JavaScript and TypeScript

Fully typed, built on the global `fetch`. Requires Node.js 18+, and runs on Bun, Deno and edge runtimes too.

```js
import { Html2img } from '@html2img/client';

const client = new Html2img('your-api-key');

const response = await client.html({
  html: '<!doctype html><html><body><h1>Hello</h1></body></html>',
  width: 1200,
  height: 630,
});

console.log(response.url); // https://i.html2img.com/abc123def456.png
```

See the [JavaScript SDK readme](https://github.com/html2img/html2img-js) and the [JavaScript guide](https://html2img.com/integrations/javascript/).

### Python

Zero runtime dependencies, full type hints, sync and async clients. Requires Python 3.9+.

```python
from html2img import Html2img

client = Html2img()  # reads HTML2IMG_API_KEY from the environment

response = client.html(
    "<h1 style='font: 700 64px system-ui'>Hello from Python</h1>",
    width=1200,
    height=630,
)

print(response.url)  # https://i.html2img.com/abc123def456.png
```

See the [Python SDK readme](https://github.com/html2img/html2img-python) and the [Python guide](https://html2img.com/integrations/python/).

### Ruby

Zero runtime dependencies, built on Net::HTTP. Requires Ruby 3.1+.

```ruby
require "html2img/client"

client = Html2img::Client.new # reads HTML2IMG_API_KEY from the environment

response = client.html(
  "<h1 style='font: 700 64px system-ui'>Hello from Ruby</h1>",
  width: 1200,
  height: 630
)

puts response.url # https://i.html2img.com/abc123def456.png
```

See the [Ruby SDK readme](https://github.com/html2img/html2img-ruby) and the [Ruby guide](https://html2img.com/integrations/ruby/).

### Laravel

Zero-config auto-discovery, a `Html2img` facade, a published config file, one-line saving to any filesystem disk, and an `html2img:test` artisan health check. Requires Laravel 11, 12 or 13.

```php
use Html2img\Laravel\Facades\Html2img;
use Html2img\Request\HtmlRequest;

$response = Html2img::html(new HtmlRequest(
    html: view('og.post', ['post' => $post])->render(),
    width: 1200,
    height: 630,
    dpi: 2,
));

$path = Html2img::store($response, "og/{$post->id}.png");
```

See the [Laravel integration readme](https://github.com/html2img/html2img-laravel) and the [Laravel guide](https://html2img.com/integrations/laravel/).

### GitHub Actions

Render Open Graph images for new posts, screenshot pull request previews or produce a card for each release.

```yaml
- uses: html2img/action@v1
  with:
    api-key: ${{ secrets.HTML2IMG_API_KEY }}
    html: '<div style="font: 700 72px system-ui; padding: 80px">Hello</div>'
    width: 1200
    height: 630
    output-path: og/hello.png
```

See the [action readme](https://github.com/html2img/action) and the [GitHub Actions guide](https://html2img.com/integrations/github-actions/).

## Free browser tools

No sign-up needed. Build an image or PDF in the browser, then move to the API when you want to automate it.

- [Open Graph Image Generator](https://html2img.com/tools/open-graph-image)
- [Code Screenshot Generator](https://html2img.com/tools/code-screenshot)
- [Invoice Image Generator](https://html2img.com/tools/invoice-image)
- [Certificate Generator](https://html2img.com/tools/certificate)
- [Twitter Card Generator](https://html2img.com/tools/twitter-card)
- [YouTube Thumbnail Generator](https://html2img.com/tools/youtube-thumbnail)
- [Pinterest Pin Generator](https://html2img.com/tools/pinterest-pin)
- [Quote Card Generator](https://html2img.com/tools/quote-card)
- [HTML to PDF Converter](https://html2img.com/tools/html-to-pdf)
- [URL to PDF Converter](https://html2img.com/tools/url-to-pdf)

See the full [image generation tools](https://html2img.com/tools) hub.

## Integration guides

Worked examples for every official package, plus guides for React and Vue. Anything that can make an HTTP request will work.

[PHP](https://html2img.com/integrations/php/) ·
[Laravel](https://html2img.com/integrations/laravel/) ·
[JavaScript and Node.js](https://html2img.com/integrations/javascript/) ·
[React](https://html2img.com/integrations/javascript/#react-and-nextjs) ·
[Vue](https://html2img.com/integrations/javascript/#vue-and-nuxt) ·
[Python](https://html2img.com/integrations/python/) ·
[Django](https://html2img.com/integrations/django/) ·
[Ruby and Rails](https://html2img.com/integrations/ruby/) ·
[WordPress](https://html2img.com/integrations/wordpress/) ·
[Statamic](https://html2img.com/integrations/statamic/) ·
[Craft CMS](https://html2img.com/integrations/craft/) ·
[GitHub Actions](https://html2img.com/integrations/github-actions/) ·
[MCP server](https://html2img.com/mcp/)

## Built for production

- **Real Chrome rendering** so your output matches the browser. [Features](https://html2img.com/features)
- **PNG or PDF** from the same request, one credit either way. [format docs](https://html2img.com/docs/parameters/format)
- **Webhook delivery** for renders that run past the 30 second sync window. [webhook_url docs](https://html2img.com/docs/parameters/webhook-url)
- **DPI control** from 1x to 4x for retina output when you need it. [dpi docs](https://html2img.com/docs/parameters/dpi)
- **Custom fonts** from Google Fonts, Adobe Fonts and self-hosted `@font-face`, all server-side.
- **Global CDN**, with images served from `i.html2img.com` and kept permanently on paid plans.

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

## Pricing

Every new account starts with 50 free credits, a one-off allowance rather than a monthly one, and no card is needed. One credit renders one image or one PDF. Free-tier renders are hosted on the CDN for 7 days.

Paid plans start at $9 a month for 1,000 credits. Renders on a paid plan are hosted permanently, and upgrading makes everything you have already rendered permanent too. The MCP server is included on paid plans. See [pricing](https://html2img.com/pricing).

## Links

[Website](https://html2img.com) ·
[Features](https://html2img.com/features) ·
[Integrations](https://html2img.com/integrations) ·
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
