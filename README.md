# Brilliantpala Search

Self-hosted SearXNG metasearch service.

## API

`GET /search?q=your+query&format=json`

Optional parameters include `language`, `categories`, `safesearch`, and `pageno`.

Example:

```bash
curl "https://YOUR-SERVICE.onrender.com/search?q=latest+AI+news&format=json"
```

The service aggregates results from configured public search engines. Availability and result counts depend on upstream engines and their rate limits.

## Deployment

Runs the official `searxng/searxng` container on Render. Configure `SEARXNG_SECRET`, `SEARXNG_PORT`, and `SEARXNG_BIND_ADDRESS` as runtime environment variables.
