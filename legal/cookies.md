---
layout: default
title: Cookie Notice
description: "Cookie Notice for Bracket Control by Dev Dyl NZ explaining essential Discord authentication session cookies, OAuth state protection and browser session storage."
permalink: /legal/cookies/
---
# Cookie Notice

**Effective: 22 October 2026**

Bracket Control / Dev Dyl NZ (NZBN **9429054041851**) uses browser cookies and session storage for Discord sign-in, account security and tournament navigation.

## Essential application cookies

| Cookie | Purpose | Typical expiry |
| --- | --- | --- |
| `bc_session` | Keeps an authenticated session active after Discord sign-in. | Up to **24 hours** |
| `bc_oauth_state` | Protects and links an OAuth sign-in attempt to the correct browser. | Up to **10 minutes** |

In the reviewed application source both cookies are `HttpOnly` and `SameSite=Lax`, with the `Secure` attribute when running in production mode. The session cookie has path `/`; the OAuth state cookie has path `/api/auth` and is cleared on callback. Signing out ends the application session.

These cookies are for **authentication and security**, not advertising. Preventing them from working can stop Discord login or protected tournament features.

## Other browser storage

The app uses an in-memory CSRF token for signed-in requests, not a separate CSRF cookie. Browser `sessionStorage` can remember a chosen server, tournament or certain older interface preferences; it is not an ordinary cookie.

## Optional analytics

Google Analytics is currently off in production. If enabled after acceptance, the purpose is to understand which public Bracket Control pages people use. You can allow or decline it in **Analytics preferences** on the app home page or under **Privacy Settings**. Your browser stores that choice. You can disable analytics there at any time to stop future collection from that browser.

If you opt in after activation, Google may use analytics cookies or similar browser identifiers to distinguish visits and process measurement requests outside New Zealand. Bracket Control's page-view data uses general route labels and does not include Discord identifiers, account details, private tournament or team information, sign-in tokens or sensitive URL parameters. We do not use this feature for advertising. Withdrawal stops future collection but does not delete events already sent to Google. Browser controls also let you clear site data and cookies.

See the [Privacy Policy]({{ '/legal/privacy/' | relative_url }}) for information about providers, overseas handling and how to contact us about your rights.

## Discord and hosting providers

Opening the Discord login page means Discord's own cookie and privacy practices apply. Cloudflare and other providers can use security or delivery technologies according to their settings. Their cookie names and lifetimes can vary.

This inventory reflects the reviewed application source; **a full independent inspection of every live browser and third-party cookie has not been completed**.

## Your choices and contact

Your browser can show, block or delete cookies and site storage. Blocking essential storage may prevent login. Use **Sign out** to end your session.

For more information contact **privacy@devdylnz.com** or read the [Privacy Policy]({{ '/legal/privacy/' | relative_url }}) and [Terms of Service]({{ '/legal/terms/' | relative_url }}).
