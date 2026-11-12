# Chaos HQ public link

Permanent entry point: https://jim-starace.github.io/chaos-hq-redirect/

The Ubuntu host runs one Cloudflare Quick Tunnel and commits the current tunnel
URL into `index.html` and `404.html`. The GitHub Actions workflow publishes those
two static pages to GitHub Pages after each update. `404.html` handles direct
visits to deep links. The pages use an inline script to preserve the path,
query, and fragment, with a timed redirect and clickable link as fallbacks.

The host-side source and operations guide live in the local `ai-server` and
`chaos-hq` workspaces. This repository contains only public redirect files.
