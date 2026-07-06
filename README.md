# shadow-peace-solitaire

A groovy version of Klondike solitaire for the hippies and homies.

**Play it:** open `index.html` in any browser — the whole game is one file, no build step, no server needed.

## Features

- Classic Klondike (draw 3) with drag & drop and double-click/double-tap to send cards to foundations
- Daily challenge — everyone gets the same seeded deal each day
- Score, timer, moves, undo (3 free), hints (3 free), auto-complete
- Stats tracking (wins, streaks, best score) saved in the browser
- 11 card back designs, dark/light theme, draw-pile side toggle, sound effects and ambient music
- Fully responsive — works on phones (all 7 columns fit) and desktop
- Premium shop UI (demo mode — purchases are simulated; wire up Stripe/PayPal to charge real money)

## Putting it online

Any static host works. Two free options:

**GitHub Pages** (this repo): Settings → Pages → deploy from the `main` branch, root folder. Your game will be live at `https://<username>.github.io/shadow-peace-solitaire/`.

**Netlify Drop:** drag `index.html` and `manifest.json` onto https://app.netlify.com/drop and get an instant URL.

## Making money from it

The shop (`purchaseItem` in `index.html`) currently just shows a demo confirmation. To take real payments you need a payment provider — the simplest options for a static site are [Stripe Payment Links](https://stripe.com/payments/payment-links) or [PayPal buttons](https://www.paypal.com/buttons/). Another route that needs no payment integration at all is ads (e.g. Google AdSense).
