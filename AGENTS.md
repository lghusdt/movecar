# Repository Guidelines

This repository contains a Cloudflare Workers app for the MoveCar notification flow.

## Project Layout

- `movecar.js`: Cloudflare Worker entrypoint, API routes, and rendered pages.
- `preview-requester.html`: static requester-page preview.
- `preview-owner.html`: static owner-confirmation preview.
- `README.md`: setup, deployment, and usage documentation.

## Development And Verification

There is currently no package manager or automated test suite in this repository.

Before proposing changes:

- Run `node --check movecar.js` when JavaScript syntax changes.
- Review the preview HTML files when changing visible UI, CSS, or copy.
- Keep the preview files and the Worker-rendered UI aligned when possible.
- Do not add generated build artifacts unless the task explicitly introduces a build step.

## Cloudflare Notes

- Do not commit secrets, Bark tokens, phone numbers, or Cloudflare credentials.
- Expected runtime configuration includes the `MOVE_CAR_STATUS` KV namespace.
- Optional runtime variables include `BARK_URL` and `PHONE_NUMBER`.
- Keep existing API routes compatible with printed QR-code links unless the task explicitly requests a breaking change.

## Style

- Preserve UTF-8 Chinese copy.
- Keep changes small and focused.
- In final responses, include what was changed and how it was verified.
