 # BluRoll Privacy Policy

  _Last updated: 2026-05-23_

  BluRoll is a Chrome extension that detects Blu-ray and 4K UHD listings on
  supported retailer websites and tells you whether the title is already in
  your BluRoll library. This policy describes what data the extension
  handles, why, and what we do (and don't do) with it.

  ## What we collect
  
  The extension collects only the data needed to log you in and match
  products against your library:

  - **Account information (PII):** the email address and display name
    associated with your BluRoll account.
  - **Authentication credentials:** your password is sent to the BluRoll
    backend at sign-in to obtain a long-lived extension API token. The
    password itself is never stored by the extension. The extension token
    (prefixed `blx_`) is stored locally in your browser via
    `chrome.storage.local` and is sent as a bearer token with each API
    request.
  - **Product page data (website content + web history):** when you visit
    a product page on a supported retailer (currently Amazon, Walmart, and
    Gruv), the extension reads the product title, UPC/barcode (when
    present), format/edition labels, cover image URL, and the page URL,
    and sends them to the BluRoll backend at `api.bluroll.com` so the
    backend can determine whether the title is already in your library.
    The extension does not read pages on any other websites and does not
    build a browsing history.

  The extension does not collect health information, financial or payment
  information, personal communications, precise location, or behavioral
  analytics (keystrokes, mouse movements, scroll position, etc.).

  ## What we do with it

  - Authenticate you to the BluRoll API.
  - Compare the product on the page against your saved library and return
    an ownership result (owned / owned in a different edition / not
    owned).
  - Cache match results locally in your browser for up to 24 hours to
    reduce repeated API calls while you browse.
  - Periodically (every ~12 hours) refresh a local copy of your library
    index so ownership lookups are fast and work briefly offline.

  ## What we do not do

  - We do not sell or transfer your data to third parties.
  - We do not use your data for advertising, profiling, or
    creditworthiness decisions.
  - We do not use your data for any purpose unrelated to telling you
    whether you already own a given Blu-ray or 4K title.
  - We do not share your library or browsing data with retailers.

  ## Where the data goes

  All network requests from the extension go to `api.bluroll.com`, which
  is operated by the BluRoll service. The BluRoll backend stores your
  account, library, and match history under the privacy terms of the
  BluRoll service itself.

  The extension does not send data to any other third-party services,
  analytics providers, or advertising networks.

  ## Storage and retention

  - Locally in your browser (`chrome.storage.local`): your extension API
    token, a cached copy of your library index, and a short-lived cache
    of recent match results.
  - On the BluRoll backend: your account and library, plus standard
    request logs.

  Signing out of the extension revokes the extension token on the server
  and clears the locally stored token, user info, and cached library.

  ## Your choices

  - You can sign out at any time from the extension popup. This removes
    the locally stored credentials and revokes the extension token on the
    server.
  - You can uninstall the extension from `chrome://extensions`, which
    clears all locally stored data.
  - To delete your BluRoll account and library data on the server,
    contact us at the address below.

  ## Changes
  
  If this policy changes in a material way, we will update the "Last
  updated" date above and, where appropriate, prompt you in the extension
  on next sign-in.
