# ReccoBeats (reccobeats)

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
