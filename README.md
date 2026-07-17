# Interfaze Migration Calculator

A tiny proof-of-concept: paste code that calls OpenAI for extraction/OCR/structured
output, and see exactly what changes to run it on [Interfaze](https://interfaze.ai)
instead — a live diff plus a cost/latency estimate.

**[Live demo →](#)** *(add your GitHub Pages link here once deployed)*

## Why

Interfaze is OpenAI SDK-compatible — switching is a `baseURL` + `model` change,
not a rewrite. That's a stronger claim than "better OCR," but it's buried in docs.
This tool makes it a felt experience instead of a claim.

## What it does

- Paste (or load the example) OpenAI client code — JS/TS or Python
- Auto-detects the `baseURL` / `base_url` and `model` lines
- Renders a real +/- diff swapping in `https://api.interfaze.ai/v1` and `interfaze-beta`
- One-click copy of the migrated code
- Editable calculator for monthly/annual $ savings and latency reduction based on your own request volume

Everything runs client-side — no backend, nothing is sent anywhere.

## Running it

It's a single static HTML file. Either:

- Open `index.html` directly in a browser, or
- Serve it locally:
  ```bash
  python3 -m http.server 8000
  ```
  then visit `http://localhost:8000`

## Notes

The default cost/latency numbers in the calculator are placeholders, not official
Interfaze pricing — they're editable so you can plug in real numbers.

## License

MIT
