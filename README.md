# Lyronexa demo bundle

Upload this whole directory to a public HTTPS host, then paste a plugin URL into the app.

Serving requirements, because the host is strict:

- HTTPS on port 443 with a publicly valid certificate. Loopback and private address
  space are rejected, so a local or LAN server cannot be used.
- Media responses need a strong `ETag` and `Accept-Ranges: bytes`.
- Serve `.wav` as `audio/wav`.

## Plugin links

- minimal: `https://raw.githubusercontent.com/devMagics/lyronexa-demo/main/plugins/minimal.lyx`
- player: `https://raw.githubusercontent.com/devMagics/lyronexa-demo/main/plugins/player.lyx`
- downloader: `https://raw.githubusercontent.com/devMagics/lyronexa-demo/main/plugins/downloader.lyx`
- tracker: `https://raw.githubusercontent.com/devMagics/lyronexa-demo/main/plugins/tracker.lyx`

## Media links

- `https://raw.githubusercontent.com/devMagics/lyronexa-demo/main/media/calm.wav`
- `https://raw.githubusercontent.com/devMagics/lyronexa-demo/main/media/pulse.wav`
- `https://raw.githubusercontent.com/devMagics/lyronexa-demo/main/media/chime.wav`

## Note on the player stream links

They are baked into the signed document, so changing the host means rebuilding the
package. Pass the real origin as the second argument to this script and update
`examples/plugins/player/ui/home.json` and its `media.play.v1` scope to match.
