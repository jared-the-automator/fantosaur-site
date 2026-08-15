# fantosaur.com

The Fantosaur brand site. Plain HTML and one stylesheet, no build step, no JavaScript,
no third-party requests at runtime.

## Layout

- `index.html` promotes the sketch series (primary call to action is YouTube) and the
  Riff Ruck merchandise line (`shop.fantosaur.com`).
- `privacy-policy/` and `terms-of-service/` are the live legal URLs the Meta, TikTok
  and Google developer applications require. They reject placeholder pages, so this
  prose is real and must stay real.
- `styles.css` holds the whole design system. The palette is the measured one in
  `Store 2026/STORE-SPEC.md` in the brand vault.

## The one colour rule

Comet Aqua `#4ffff6` on a light surface measures 1.14:1. Aqua text and the aqua brand
marks only ever appear on a Fossil Violet `#25064d` panel, which is why the header,
hero and footer stay violet in both colour schemes.

## Assets

Everything under `assets/` is cut from the brand vault at
`~/Documents/2B/Fantosaur/Images/`. The three joke frames are real episode stills.

`band-*.webp` are the hero backdrop: one full-strength horizontal crop from each of
the six art themes, stacked, no blur and no fade. `dino-mic.webp` is the performer,
composited from `assets/brand/dino-transparent.png` and `rig/stage/foreground.svg` in
the `fantosaur` repo at that pipeline's own stage geometry (canvas 1080x1920, art
bbox 193..2878, floor 1480, mic drawn over Dino). Rebuilding it any other way puts
the mic on the wrong plane, which is the note Jared gave the video rig on 2026-07-28.
Fonts are self-hosted (Protest Riot and Poppins, both OFL, licences alongside the
files) and the social icons are Simple Icons (CC0), inlined into the markup. That is
deliberate: the privacy policy promises the site makes no third-party requests, so
adding a CDN font or icon link would make the policy untrue.

## Deploying

GitHub Pages serves `main` from the repository root. `CNAME` holds the custom domain
and `.nojekyll` disables Jekyll processing.
