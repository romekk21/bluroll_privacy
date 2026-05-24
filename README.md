  # BluRoll Privacy Policy

  _Last updated: 2026-05-24_

  BluRoll is a service for tracking your Blu-ray and 4K UHD library. It
  consists of a mobile app (the primary way to build and manage your
  library) and a Chrome extension (which detects listings on supported
  retailer websites and tells you whether the title is already in your
  library). This policy describes what data each surface handles, why,
  and what we do (and don't do) with it.

  ## What we collect

  Across both the mobile app and the Chrome extension, we collect only
  the data needed to run your account and the ownership-detection
  features:

  - **Account information (PII):** the email address and display name
    associated with your BluRoll account.
  - **Authentication credentials:** your password is sent to the BluRoll
    backend at sign-in to obtain a session or extension API token. The
    password itself is never stored on your device. Tokens are stored
    locally (in `chrome.storage.local` on the extension, in
    `expo-secure-store` / the OS keychain on mobile) and sent as bearer
    tokens with each API request.
  - **Your Blu-ray / 4K library:** titles, release years, formats,
    editions, UPCs/barcodes, and cover images you add to your library —
    whether by scanning a barcode, importing from a CLZ export, or adding
    manually.
  - **Product page data (Chrome extension only):** when you visit a
    product page on a supported retailer, the extension reads the product
    title, UPC/barcode (when present), format/edition labels, cover image
    URL, and the page URL, and sends them to the BluRoll backend so it
    can determine whether the title is already in your library.

  We do not collect health information, financial or payment information,
  personal communications, precise location, or behavioral analytics
  (keystrokes, mouse movements, scroll position, etc.).

  ## Chrome extension

  The extension runs only on supported retailer domains (currently
  Amazon, Walmart, and Gruv) and does not read pages on any other
  websites. On those pages it:

  - Authenticates you to the BluRoll API.
  - Compares the product on the page against your saved library and
    returns an ownership result (owned / owned in a different edition /
    not owned).
  - Caches match results locally in your browser for up to 24 hours to
    reduce repeated API calls while you browse.
  - Periodically (every ~12 hours) refreshes a local copy of your library
    index so ownership lookups are fast and work briefly offline.

  The extension does not build a browsing history; it only sends the URL
  and product details of pages where it actively performs an ownership
  lookup.

  ## Mobile app
  
  The mobile app (iOS and Android, built with Expo / React Native) is the
  primary way to build and manage your BluRoll library. It:

  - Authenticates you to the BluRoll API and stores a session token in
    the OS keychain (via `expo-secure-store`).
  - Lets you add titles to your library manually, by scanning a barcode
    with your device camera, or by importing a CLZ Movies export file
    you select from your device.
  - Syncs your library with the BluRoll backend so it is available on
    every device where you sign in (and to the Chrome extension).
  - Caches your library, cover images, and recently viewed details
    locally so the app is fast and partially usable offline.

  A few specifics worth being explicit about:

  - **Camera:** the camera is requested only when you open the barcode
    scanner. Frames are processed on-device to decode the barcode; the
    raw camera image is not stored on your device and is not sent to
    BluRoll or any third party. Only the decoded UPC is used for the
    lookup.
  - **Photos / files:** if you choose to import a CLZ Movies export via
    the document picker, only the file you select is read; the app does
    not browse or upload any other files from your device.
  - **Push notifications and background tracking:** the app does not send
    push notifications and does not track your location or activity in
    the background.

  ## What we do not do

  - We do not sell or transfer your data to third parties.
  - We do not use your data for advertising, profiling, or
    creditworthiness decisions.
  - We do not use your data for any purpose unrelated to managing your
    Blu-ray / 4K library and telling you whether you already own a given
    title.
  - We do not share your library or browsing data with retailers.

  ## Where the data goes

  All network requests from both the extension and the mobile app go to
  `api.bluroll.com`, which is operated by the BluRoll service. The
  BluRoll backend stores your account, library, and match history.

  Neither surface sends data to any other third-party services,
  analytics providers, or advertising networks.

  ## Storage and retention

  - **Locally in your browser** (extension): your extension API token, a
    cached copy of your library index, and a short-lived cache of recent
    match results.
  - **Locally on your phone** (mobile app): your session token (in the OS
    keychain), a cached copy of your library, cover images, and recently
    viewed details.
  - **On the BluRoll backend:** your account and library, plus standard
    request logs.
  
  Signing out clears the locally stored token and cached data on that
  device and, where applicable, revokes the token on the server.

  ## Your choices

  - You can sign out at any time from the extension popup or the mobile
    app. This removes the locally stored credentials and, for the
    extension, revokes the extension token on the server.
  - You can uninstall the extension from `chrome://extensions` or
    uninstall the mobile app from your device, either of which clears
    all locally stored data on that surface.
  - To delete your BluRoll account and library data on the server,
    contact us at the address below.

  ## Changes

  If this policy changes in a material way, we will update the "Last
  updated" date above and, where appropriate, prompt you on next
  sign-in.

