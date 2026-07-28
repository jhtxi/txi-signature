# TXI Email Signature Generator

Static page that generates a TXI email signature and copies it ready to paste into Gmail.

**Live: https://jhtxi.github.io/txi-signature/**

Single self-contained `index.html`. No build step, no dependencies, no external requests.
Deploys on push to `master` via GitHub Pages.

## The signature

```
Name                      bold 15px  #070b18
Title                     14px       #595959
TXI | Traffic By Intent   17px       #432cf3
email                     13px       #595959  (mailto link)
phone (optional)          13px mono  #595959
trafficbyintent.com       bold 13px  #432cf3
```

## House rules

These are email-client survival rules, not style preferences. Do not "modernize" them.

- **Table layout.** Outlook ignores flexbox and grid.
- **Every style inline.** Gmail strips `<style>` blocks on receive.
- **Arial only.** No web font survives an email client.
- **No images.** Logo files get blocked, break, or attach themselves to every send.
- **Six lines.** No banners, quotes, social icons, or confidentiality boilerplate.
- **ASCII punctuation.** Em-dashes and curly quotes mojibake in older clients.

The signature markup hardcodes `#432cf3`; it renders in the recipient's mail client, so it
never follows this page's theme. The page chrome lightens the indigo in dark mode for contrast.

## Source of truth

The same template, plus a Node batch builder and roster, lives in the TXI repo at
`TXI-Data/outputs/email_signatures/`. Change the markup in both, or this page and the repo drift.
