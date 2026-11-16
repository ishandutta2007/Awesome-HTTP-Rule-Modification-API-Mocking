# Awesome-HTTP-Rule-Modification-API-Mocking

## Top HTTP Rule Modification & API Mocking Ecosystem

**Curated List of SaaS Platforms & Open-Source GitHub Projects**  
*Focused on Request Interception, Response Mocking & Self-Hosted Debugging Proxies*  
**Last updated: March 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **HTTP Rule Modification & API Mocking**. These tools help developers and QA engineers intercept live traffic and rewrite it on the fly—covering everything from browser extensions that redirect URLs without proxy setup to full MITM proxies that script arbitrary request and response transformations.

**Examples** include Requestly (BrowserStack), mitmproxy, Whistle, HTTP Toolkit, Mockoon, Charles Proxy, and Fiddler Everywhere (the category leaders).

**Open-source emphasis**: This section highlights every major active project for self-hosted traffic modification, open-source API mocking, and community-driven interception—ideal for teams seeking data sovereignty and avoiding per-seat proxy licensing. The open-source landscape is genuinely functional: **mitmproxy** is the scriptable standard for automated interception , **Whistle** is a Node.js-based cross-platform debugging proxy with 14.7k+ stars , and **HTTP Toolkit** offers a polished GUI with a powerful mock server library .

Contributions welcome! Open an PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-products)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

| Product | Description | Pricing (Starting) | Free Tier / Trial Limits |
|---------|-------------|-------------------|--------------------------|
| **[Requestly (BrowserStack)](https://requestly.com/)** | **Browser-native HTTP interception and API mocking without proxy setup.** Trusted by **300,000+ developers**; acquired by BrowserStack in May 2025 . **Core features**: mock REST/GraphQL APIs, modify request/response headers and bodies, redirect URLs, inject scripts, block requests, and simulate delays . **No system proxy or SSL certificates required**—works through corporate VPNs . **Open-source core** available on GitHub. | Free: **$0**; paid plans via Requestly | **Free**: core interception and mocking features; **open-source** version available |
| **[Charles Proxy](https://www.charlesproxy.com/)** | Desktop MITM proxy with per-host SSL proxying and rewrite rules. Charles 5 adds Apple Silicon support and MSIX installer . | Upgrade: **$20/license** (40% of new); Site License: **$160** | Free trial with 30-minute session limits |
| **[Fiddler Everywhere](https://www.telerik.com/fiddler)** | Cross-platform debugging proxy with visual Rules builder. **Lite ($7/user/mo annual) does not include traffic manipulation through Rules**—that requires **Pro ($13/user/mo)** . | Pro: **$13/user/month** (annual); Lite: **$7** | Lite plan available; Rules require Pro |
| **[Proxyman](https://proxyman.com/)** | Native macOS/Windows/Linux HTTPS debugging proxy with mock, script, and reverse-proxy capabilities. | Pro: **~$99/year** (starting) | Free tier: core capture and inspect; Pro features locked |

## Open-Source GitHub Projects

| Project | Star Badge | Description |
|---------|------------|-------------|
| **[mitmproxy](https://github.com/mitmproxy/mitmproxy)** | [![Stars](https://img.shields.io/github/stars/mitmproxy/mitmproxy?style=social&color=white)](https://github.com/mitmproxy/mitmproxy/stargazers) | **The standard open-source scriptable MITM proxy for automated rule modification and mocking.** **MIT licensed**, Python. **Three interfaces**: `mitmproxy` (interactive console for HTTP/1, HTTP/2, WebSockets), `mitmweb` (browser UI), and `mitmdump` (headless for CI/scripts) . **Python addons** receive each flow as a mutable object—rewrite responses, mock endpoints, or log traffic programmatically . **TLS interception** via generated CA; per-host decryption control . **Certificate pinning defeats it**—test only against your own apps . **Best for teams wanting programmatic, scriptable interception** in CI pipelines. |
| **[Whistle](https://github.com/avwo/whistle)** | [![Stars](https://img.shields.io/github/stars/avwo/whistle?style=social&color=white)](https://github.com/avwo/whistle/stargazers) | **Node.js-based cross-platform debugging proxy with a web UI for rule modification.** **MIT licensed**, **14,760+ GitHub stars**, actively maintained (releases ~19 days ago) . **HTTP, HTTP2, HTTPS, and WebSocket** support . **Rule-based interception**: rewrite requests, mock responses, redirect URLs, modify headers—configured via a browser-based interface . **Keywords**: charles, fiddler, hosts, proxy, weinre . **Best for teams wanting a Node.js-native proxy** with a visual rule editor and no desktop install. |
| **[HTTP Toolkit](https://github.com/httptoolkit/httptoolkit)** | [![Stars](https://img.shields.io/github/stars/httptoolkit/httptoolkit?style=social&color=white)](https://github.com/httptoolkit/httptoolkit/stargazers) | **Polished open-source HTTP(S) debugging proxy, analyzer, and client.** **AGPL-3.0** for UI and desktop wrapper . **Backend uses Mockttp** (`mockttp` library, Apache-2.0) for powerful HTTP mocking and proxying . **Cross-platform** (Electron desktop app) . **One-click interception** for browsers, mobile apps, and backend processes . **Best for teams wanting a modern GUI** with built-in mocking without commercial licensing. |
| **[Mockoon](https://github.com/mockoon/mockoon)** | [![Stars](https://img.shields.io/github/stars/mockoon/mockoon?style=social&color=white)](https://github.com/mockoon/mockoon/stargazers) | **Open-source API mocking desktop application.** **Create unlimited mock APIs** locally with no remote deployment or account. **CLI available** (`mockoon/cli`) for deploying mocks anywhere . **Best for teams wanting dedicated API mocking** without a full interception proxy—mock endpoints before backend exists. |

### Additional Strong Open-Source Options

| Project | Star Badge | Description |
|---------|------------|-------------|
| **[ModHeader](https://addons.mozilla.org/en-GB/android/addon/modheader-by-modheader-app/)** | — | **Browser extension for HTTP header modification.** Modify, add, edit, remove, and override **request and response headers** without changing application code . **Reusable header profiles** and URL-pattern-based rules . **Best for quick header-only testing** (User-Agent, Authorization, CORS) without a proxy. |

**Frameworks for building custom systems**: Choose **mitmproxy** for scriptable interception in CI , **Whistle** for a Node.js proxy with a web UI rule editor , or **Requestly** for browser-native mocking without proxy setup  —all without per-seat proxy licensing.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- HTTP rule modification tools intercept traffic containing credentials, session tokens, and sensitive data; **only intercept and modify traffic you own or have explicit authorization to test**. Remove CA certificates from test devices when finished.
- **Tool choice depends on whether you need browser-native mocking, scripted automation, or a full MITM proxy.** **Requestly is the most accessible for frontend mocking**—no proxy setup, works through corporate VPNs, and is now backed by BrowserStack while remaining open-source . **mitmproxy is built for automation**: `mitmdump` runs headless in CI, and Python addons let you rewrite flows programmatically . **Whistle offers a Node.js-native alternative** with a web UI for rule configuration . **Fiddler Everywhere's Lite tier does not include traffic manipulation through Rules**—you need Pro ($13/user/month) for that capability . **Charles and Proxyman are polished desktop proxies** but require system-level proxy configuration and SSL certificate installation, which can conflict with corporate VPNs . **Validate whether you need browser-native interception (Requestly), scriptable automation (mitmproxy), or a visual desktop proxy (Charles, Proxyman)** before committing.

---

**Made for developers, QA engineers, and security teams modifying HTTP traffic.**  
Let's make HTTP rule modification and API mocking more open, accessible, and proxy-free.
