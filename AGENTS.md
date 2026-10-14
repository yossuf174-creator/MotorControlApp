# Base44 Dev Environment

## What this app is

An Android (Kotlin) WebView app that wraps a single self-contained HTML file (`app/src/main/assets/index.html`) — an Arabic motor simulator. No backend, no database, no external services.

## How it runs in the sandbox

The Android app itself can't run in the preview. Instead, `docker-compose.base44.yml` serves the HTML asset via nginx:alpine on host port 3000, so the preview shows the same content the WebView would display.

## Verification

- `docker compose -f docker-compose.base44.yml up -d --build`
- `curl http://localhost:3000/` should return the HTML page
- The preview at port 3000 shows the motor simulator UI
