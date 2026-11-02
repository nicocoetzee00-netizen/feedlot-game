FEEDLOT MANAGER: installable web app package

WHAT IS IN HERE
  index.html            the whole game
  manifest.webmanifest  app name, icons, colours (makes it installable)
  sw.js                 service worker (lets it work offline after the first visit)
  icons/                192, 512, maskable and Apple icons

HOW TO PUT IT ONLINE
1. Upload the contents of this folder to any static web host, keeping the icons folder.
   It can sit at the root of a site or in a subfolder (all paths are relative).
   Examples: GitHub Pages, Netlify Drop (drag the folder onto app.netlify.com/drop),
   Cloudflare Pages, or a folder on your own web server.
2. The address must be HTTPS. Phones will not install it from plain http.
3. Make sure the server sends .webmanifest as application/manifest+json (most hosts do;
   text/plain or application/json also works in Chrome).

HOW TO INSTALL ON ANDROID
1. Open the address in Chrome and let it load once.
2. Chrome menu (three dots), then "Install app" (or "Add to Home screen").
3. Open it from the home screen: it runs full-screen and works offline.

UPDATING
  When you upload a new index.html, also change VERSION in sw.js (for example feedlot-v2).
  Phones fetch the new version on the next open, and clean out the old one.

GOOD TO KNOW
  - Saves are stored on the phone, in that browser, for that web address. A different address,
    or clearing Chrome's site data, starts a new game. Saves from the claude.ai link do not
    carry over.
  - Prices, costs and biology are simplified for play; they are not market quotes.
