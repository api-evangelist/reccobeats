# ReccoBeats (reccobeats)

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
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

ReccoBeats is a free music recommendation and database API service. It exposes a REST API over a database of millions of tracks, artists, and albums, and a machine-learning recommendation engine that suggests tracks from seed tracks, artists, or albums. ReccoBeats also extracts Spotify-style audio features - acousticness, danceability, energy, instrumentalness, liveness, loudness, speechiness, tempo, and valence - either for a catalog track by ID or directly from an uploaded audio file. Resources can be addressed by ReccoBeats UUID or by Spotify ID, and the API requires no API key or authentication.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/reccobeats/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/reccobeats/refs/heads/main/apis.yml)

## Tags

- Music
- Recommendations
- Audio Features
- Audio Analysis
- Music Database
- Spotify Alternative

## Timestamps

- **Created:** 2026-07-03
- **Modified:** 2026-07-03

## APIs

### ReccoBeats Track API

Retrieve track metadata from the ReccoBeats music database - fetch a single track by its ReccoBeats UUID, or look up multiple tracks in one request by ReccoBeats or Spotify IDs. Tracks are the primary resource used as seeds for recommendations and as the subject of audio-feature lookups.

- **Human URL:** [https://reccobeats.com/docs/apis/get-track-by-id](https://reccobeats.com/docs/apis/get-track-by-id)
- **Base URL:** `https://api.reccobeats.com/v1`

#### Tags

- Tracks
- Metadata
- Music Database

#### Properties

- [Documentation](https://reccobeats.com/docs/documentation/introduction)
- [API Reference](https://reccobeats.com/docs/apis/get-track-by-id)
- [OpenAPI](openapi/reccobeats-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/reccobeats.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/reccobeats.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### ReccoBeats Audio Features API

Get the Spotify-style audio features for a catalog track by ID - acousticness, danceability, energy, instrumentalness, liveness, loudness, speechiness, tempo, and valence - as numeric characteristics describing the track's sound and mood. A drop-in alternative to Spotify's deprecated audio features endpoint.

- **Human URL:** [https://reccobeats.com/docs/apis/get-track-audio-features](https://reccobeats.com/docs/apis/get-track-audio-features)
- **Base URL:** `https://api.reccobeats.com/v1`

#### Tags

- Audio Features
- Danceability
- Energy
- Valence

#### Properties

- [API Reference](https://reccobeats.com/docs/apis/get-track-audio-features)
- [OpenAPI](openapi/reccobeats-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/reccobeats.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/reccobeats.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### ReccoBeats Audio Analysis API

Extract audio features directly from an uploaded audio file (MP3, OGG, WAV, AIFF; up to 5 MB, first 30 seconds analyzed) via a multipart POST. Returns the same nine-dimension feature vector as the catalog audio-features endpoint, for tracks that are not in the ReccoBeats database.

- **Human URL:** [https://reccobeats.com/docs/documentation/Analysis/audio-features-extraction](https://reccobeats.com/docs/documentation/Analysis/audio-features-extraction)
- **Base URL:** `https://api.reccobeats.com/v1`

#### Tags

- Audio Analysis
- Feature Extraction
- File Upload

#### Properties

- [Documentation](https://reccobeats.com/docs/documentation/Analysis/audio-features-extraction)
- [API Reference](https://reccobeats.com/docs/apis/extract-audio-features)
- [OpenAPI](openapi/reccobeats-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/reccobeats.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/reccobeats.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### ReccoBeats Recommendation API

Generate track recommendations from seed tracks, artists, or albums. The engine clusters a large dataset of songs, artists, and audio features and returns tracks whose characteristics best match the seeds, with the result set size controlled by the size parameter. Seeds accept ReccoBeats or Spotify IDs.

- **Human URL:** [https://reccobeats.com/docs/apis/get-recommendation](https://reccobeats.com/docs/apis/get-recommendation)
- **Base URL:** `https://api.reccobeats.com/v1`

#### Tags

- Recommendations
- Seeds
- Discovery

#### Properties

- [API Reference](https://reccobeats.com/docs/apis/get-recommendation)
- [OpenAPI](openapi/reccobeats-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/reccobeats.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/reccobeats.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### ReccoBeats Artist API

Retrieve artist metadata and discography - get a single artist by ID, fetch multiple artists in one request, and list an artist's albums or tracks. Artist IDs can seed recommendations and resolve to the artist's catalog for further browsing.

- **Human URL:** [https://reccobeats.com/docs/apis/get-artist-by-id](https://reccobeats.com/docs/apis/get-artist-by-id)
- **Base URL:** `https://api.reccobeats.com/v1`

#### Tags

- Artists
- Discography
- Music Database

#### Properties

- [API Reference](https://reccobeats.com/docs/apis/get-artist-by-id)
- [OpenAPI](openapi/reccobeats-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/reccobeats.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/reccobeats.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### ReccoBeats Album API

Retrieve album metadata and tracklists - get a single album by ID, fetch multiple albums in one request, and list the tracks on an album. Album IDs can seed recommendations and resolve to their constituent tracks for audio-feature analysis.

- **Human URL:** [https://reccobeats.com/docs/apis/get-albums](https://reccobeats.com/docs/apis/get-albums)
- **Base URL:** `https://api.reccobeats.com/v1`

#### Tags

- Albums
- Tracklists
- Music Database

#### Properties

- [API Reference](https://reccobeats.com/docs/apis/get-albums)
- [OpenAPI](openapi/reccobeats-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/reccobeats.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/reccobeats.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Website](https://reccobeats.com)
- [Documentation](https://reccobeats.com/docs/documentation/introduction)
- [Plans](plans/reccobeats-plans-pricing.yml)
- [Rate Limits](rate-limits/reccobeats-rate-limits.yml)
- [Fin Ops](finops/reccobeats-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
