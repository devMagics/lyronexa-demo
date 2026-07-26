# Lyronexa demo bundle

Upload this whole directory to a public HTTPS host, then paste a plugin URL into the app.

Serving requirements, because the host is strict:

- HTTPS on port 443 with a publicly valid certificate. Loopback and private address
  space are rejected, so a local or LAN server cannot be used.
- Media responses need a strong `ETag` and `Accept-Ranges: bytes`.
- Serve `.wav` as `audio/wav`.

## Plugin links

- player: `https://media.example/plugins/player.lyx`
- downloader: `https://media.example/plugins/downloader.lyx`
- tracker: `https://media.example/plugins/tracker.lyx`
- player-v2: `https://media.example/plugins/player-v2.lyx`

## Media links

- `https://media.example/media/tone-stereo.wav`
- `https://media.example/media/tone-mono.wav`

## Note on the player-v2 stream link

Its `playMedia.v1` URL is baked into the signed document, so changing the host means
rebuilding the package. Pass the real origin as the second argument to this script and
update `examples/plugins/player-v2/ui/home.json` and its `media.play.v1` scope to match.
