# SkinTally Privacy Policy

[Türkçe](gizlilik-politikasi) · [About SkinTally](./)

*Last updated: November 23, 2026*

## The short version

**Your inventory data never leaves your browser.** SkinTally has no server. We cannot see your inventory, your Steam account, your costs, or anything else — the extension stores everything locally on your device.

## What SkinTally stores (locally, on your device only)

- A cached copy of your CS2 inventory (so repeat visits don't re-request Steam)
- A cached market price catalog (Skinport sales/listings, CSFloat price list)
- Your daily inventory value history
- Cost amounts you enter ("Paid") for your P&L ledger
- Preferences (language, currency, value basis, Steam mode)
- Steam Market prices you looked up (12 hours) and English names of applied stickers/charms
- Your trade partner's public CS2 inventory while a trade offer is open (30 minutes)

All of this lives in your browser's extension storage. You can export it (popup → Export data) or delete it by removing the extension.

## Network requests the extension makes

SkinTally makes **anonymous** requests (no account data, no cookies, no identifiers) to:

| Endpoint | Purpose |
|---|---|
| `steamcommunity.com/inventory/...` | Reads the inventory you are viewing, using your own browser session — the same request the Steam page itself makes |
| Trade offer pages | Reads the items both sides have in the offer and in the trade window from what the Steam page has already loaded. Because that data has no float, pattern or stickers, it also asks Steam once for your trade partner's public CS2 inventory (the same request as opening their inventory page; from your browser, to Steam only). The result is kept on your device for 30 minutes, nothing is requested while Steam is rate-limiting, and a private inventory is simply skipped. |
| Trade offers list (incoming and sent) | Reads which items each offer contains from the page and shows each side's total and the difference. Read-only: it never accepts, declines or checks for new offers in the background. |
| Steam Market item pages (CS2) | On a case or capsule page, shows the price of each possible item and its price range across wears next to Steam's "Possible contents" list. Names come from the data the page already contains; no extra request. Read-only: it never buys, sells or places orders. |
| `steamcommunity.com/market/priceoverview` | Live Steam Market price for the item you open; for the items on the page you are looking at only if you turn on "Steam" mode; and for up to 40 items that no cash market (Skinport/CSFloat) prices, so they are not shown as worthless. Paced one at a time, paused if Steam asks us to slow down, remembered locally for 12 hours |
| `steamcommunity.com/economy/itemclasshover` | Only for names SkinTally can't read from the page. That happens when an applied sticker or charm name can't be matched to a price (for example because Steam shows it in your language), or for items on your trade offers list, where Steam shows only an item's class number. It asks Steam for that item's English market name: at most 30 per inventory visit, 10 per trade offer, 40 per visit to your trade offers list and 6 per opened item, one every 1.5 s, without cookies, and never while Steam is rate-limiting. Names are remembered locally, so later visits need no request. |
| `steamcommunity.com/market/sellitem` | **Only when you click** "List on Steam" (in the item panel or the sell list): lists the items you picked on the Steam Market, exactly like Steam's own Sell button. Sent to Steam with your Steam session and Steam's `sessionid` token, because Steam requires them. Nothing is sent anywhere else. |
| `api.skinport.com/v1/items`, `/v1/sales/history` | Bulk anonymous price catalog |
| `csfloat.com/api/v1/listings/price-list` | Bulk anonymous price list for cross-checking |
| `tcmb.gov.tr/kurlar/today.xml` | Daily exchange rates for showing prices in your currency |

Apart from the Steam requests above (which go only to Steam, with your own session, just as the Steam page does), no request contains your Steam ID, inventory contents, or any personal data.

## Selling helpers

On your own inventory, SkinTally can list one item from the item panel or up to 20 items from your sell list after you tick Steam's Subscriber Agreement box, or open Steam's own sell window. Every listing starts with your click, and Steam still asks you to confirm each one in the Steam Mobile app. SkinTally never sells, relists or reprices anything on its own.

## What SkinTally does NOT do

- No analytics, no telemetry, no tracking of any kind
- No data sent to any SkinTally server (none exists)
- No affiliate redirection or link modification
- No reading of your browsing activity — the extension only runs on Steam inventory, trade offer, trade offers list and CS2 Market item pages
- The Steam Web API key security check reads Steam's key page in your browser and shows you the result; the key itself is never stored or transmitted

## Permissions explained

- **storage** — local caches and your ledger, as listed above
- **steamcommunity.com** (inventory, trade offer, trade offers list and CS2 Market item pages; declared as content scripts, not as a host permission) — to draw the value layer and the selling helpers
- **api.skinport.com / csfloat.com / tcmb.gov.tr** — anonymous price and rate data

## Contact

Questions: [aslantnh@gmail.com](mailto:aslantnh@gmail.com) or the Support tab on SkinTally's Chrome Web Store page. The extension's code is shipped unminified, so you can read the package and verify all of the above yourself.
