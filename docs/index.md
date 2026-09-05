# Platform Portal

This is the Gurujix Internal Developer Platform portal (Backstage).

## What this component is

- Software Catalog front door for Gurujix
- Ownership and system map for platform capabilities
- Future home for golden paths, CI status, and deploy visibility

## Local development

```sh
yarn install
yarn start
```

Open `http://localhost:3000`.

## Catalog model

```text
Domain: gurujix
  └── System: developer-platform
        └── Component: platform-portal
              owner: platform-team
```

Entity YAML lives in:

- `catalog-info.yaml` — this portal component
- `catalog/org.yaml` — ownership
- `catalog/platform.yaml` — domain and system

## Related links

- Hub site: [gurujix.com](https://gurujix.com/)
- Future portal hostname: `platform.gurujix.com`
