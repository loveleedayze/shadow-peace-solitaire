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

**Netlify Drop:** drag the whole folder (`index.html`, `manifest.json`, `sw.js`, `icons/`) onto https://app.netlify.com/drop and get an instant URL.

## Offline / installable (PWA)

Once hosted, the game can be installed to a phone or desktop and plays with no connection. `sw.js` caches the game files, and the shop shows a "connect to the internet to purchase" note while offline. **When you change any file, bump `CACHE_VERSION` in `sw.js`** so players get the update. Service workers don't run from a double-clicked `index.html`, so to test locally run `python -m http.server 8123` in this folder and open http://localhost:8123.

## Making money from it

The shop (`purchaseItem` in `index.html`) currently just shows a demo confirmation. To take real payments you need a payment provider — the simplest options for a static site are [Stripe Payment Links](https://stripe.com/payments/payment-links) or [PayPal buttons](https://www.paypal.com/buttons/). Another route that needs no payment integration at all is ads (e.g. Google AdSense).
