# Qobuz (qobuz)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Qobuz is a French hi-res audio streaming and download platform founded in 2007 and operated by Xandrie SA. It offers lossless FLAC streaming up to 24-bit/192 kHz and a hi-res download store covering over 100 million tracks across all genres. The Qobuz REST API (v0.2) is a partner-only interface that enables third-party applications — hi-fi hardware manufacturers, DAPs, music players, and streaming integrators — to search the catalog, retrieve album and artist metadata, generate authenticated streaming URLs, manage user playlists and favorites, and process purchases from the hi-res download store. API access requires contacting Qobuz directly at api@qobuz.com to obtain an app_id and app_secret. Consumer subscription plans (Studio Solo, Studio Duo, Studio Family, Sublime) provide the underlying access entitlement; partners and integrators are subject to the Qobuz API Terms of Use governed by French law. The service is deployed across France, Germany, and Canada infrastructure nodes monitored via a public status page.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/qobuz/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/qobuz/refs/heads/main/apis.yml)

## Tags

- Music Streaming
- Hi-Res Audio
- FLAC
- Lossless Audio
- Music Downloads
- Catalog Search
- Streaming URLs
- Music Metadata
- Audiophile
- France

## Timestamps

- **Created:** 2026-06-13
- **Modified:** 2026-06-13

## APIs

### Qobuz Music API

The Qobuz Music API (v0.2) is a REST interface served at https://www.qobuz.com/api.json/0.2 returning JSON responses. It covers user authentication (email/password or token-based with MD5-hashed credentials plus app_id and app_secret), catalog operations (search albums, artists, tracks, and playlists), detailed metadata retrieval (album/get, artist/get, track/get, playlist/get), streaming and download URL generation (track/getFileUrl with format codes 5=MP3-320, 6=FLAC-CD, 7=FLAC-HiRes-96kHz, 27=FLAC-HiRes-192kHz), and user account management (favorite/getUserFavorites). Request signing for protected endpoints uses an MD5 hash of concatenated path parameters, a timestamp, and the app_secret. Access requires a valid Qobuz subscription (Studio or Sublime) and partner credentials issued by Qobuz.

- **Human URL:** [https://github.com/DJDoubleD/QobuzApiSharp](https://github.com/DJDoubleD/QobuzApiSharp)
- **Base URL:** `https://www.qobuz.com/api.json/0.2`

#### Tags

- Catalog Search
- Albums
- Artists
- Tracks
- Playlists
- Streaming URLs
- Hi-Res Audio
- User Favorites
- Authentication
- Downloads

#### Properties

- [OpenAPI](openapi/openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Documentation](https://github.com/DJDoubleD/QobuzApiSharp)
- [Documentation](https://pkg.go.dev/github.com/markhc/gobuz)
- [Terms of Service](http://static.qobuz.com/apps/api/QobuzAPI-TermsofUse.pdf)
- [Authentication](https://github.com/DJDoubleD/QobuzApiSharp#authentication)

## Common Properties

- [Portal](https://www.qobuz.com/)
- [Documentation](https://github.com/DJDoubleD/QobuzApiSharp)
- [Terms of Service](http://static.qobuz.com/apps/api/QobuzAPI-TermsofUse.pdf)
- [Integration Guidelines](https://static.qobuz.com/apps/api/Qobuz-AppsGuidelines-V1.0.pdf)
- [Contact](mailto:api@qobuz.com)
- [Sign Up](https://www.qobuz.com/us-en/music/streaming/offers)
- [Pricing](https://www.qobuz.com/us-en/music/streaming/offers)
- [Status Page](https://status.qobuz.com/)
- [Blog](https://www.qobuz.com/us-en/magazine)
- [Apps Partners](https://www.qobuz.com/us-en/discover/apps-partners)
- [LinkedIn](https://www.linkedin.com/company/qobuz/)
- [Facebook](https://www.facebook.com/Qobuz)
- [Twitter](https://twitter.com/qobuz)
- [Git Hub](https://github.com/DJDoubleD/QobuzApiSharp)
- [Plans](plans/qobuz-plans-pricing.yml)
- [Rate Limits](rate-limits/qobuz-rate-limits.yml)
- [Fin Ops](finops/qobuz-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
