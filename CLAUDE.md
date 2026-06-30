# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Purpose

This project produces an information page (and a printable PDF) for friends attending a
boat-fishing outing ("船釣小搞搞") on **7/4**. The deliverables are:

1. A web page presenting event info (meeting point, parking, the boat, fishing spots, meals, a fishing tutorial).
2. A PDF generated from / matching that page, suitable for sharing with attendees.

Content language is **Traditional Chinese (zh-TW)**. There is no code in the repo yet — it is
currently media assets awaiting the page build.

## Asset layout

- `assets/images/` — event photos (`.jpg`). Filenames are descriptive Chinese names; treat them as
  the source of truth for what each photo shows:
  - `集合地點.jpg` — meeting point
  - `停車場入口.jpg` — parking lot entrance
  - `商店大街.jpg` — shop street (on the way in)
  - `往管理室方向走.jpg` — walk toward the management office
  - `當天搭的船.jpg` — the boat we board
  - `船內的樣子.jpg` — interior of the boat
  - `在船頭釣魚的樣子.jpg` / `在走道釣魚的樣子.jpg` / `後甲板也是釣魚區.jpg` — fishing spots (bow / walkway / rear deck)
  - `船的甲板可以躺著看星星.jpg` — deck stargazing
  - `餐點1.jpg` / `餐點2.jpg` — meals
  - `彩虹祝我們順利.jpg` — rainbow (mood/closing shot)
  - `防暈船_提早服藥.jpg` / `防暈船_服藥時機.jpg` / `防暈船_看遠處.jpg` — anti-seasickness infographics
- `assets/video/簡單釣魚教學.mp4` — short fishing tutorial (~95 MB).
- `content/event-info.md` — single source of truth for the page/PDF content. Update this first, then rebuild the page.

## Conventions

- Chinese filenames work in `src`/`href` but must be **URL-encoded** when referenced from HTML/CSS
  (or rename to ASCII slugs if a build step has trouble). Keep the originals as the canonical names.
- The tutorial video is large; for the web page prefer linking/embedding lazily rather than autoplay,
  and do not commit re-encoded copies without reason.
