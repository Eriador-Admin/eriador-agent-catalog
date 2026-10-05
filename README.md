# eriador-agent-catalog

Public first-party **curated agent** catalog. Browse files here; install copies a listing into the tenant.

> **Repo home:** [`Eriador-Admin/eriador-agent-catalog`](https://github.com/Eriador-Admin/eriador-agent-catalog) — public. Clone without credentials:
>
> ```bash
> git clone https://github.com/Eriador-Admin/eriador-agent-catalog.git
> ```

## Layout

```
agents/v1/catalog.json   agent listings + categories
agents/v1/schema.json    shape of catalog.json
tools/v1/catalog.json    agent tool listings + categories
tools/v1/schema.json     shape of catalog.json
```

Each listing is `install: tenant-record` and `artifactStore: eriador`. Tenant-published agents and tools, and review queues, stay in the tenant database.

A tool listing is a declarative tool definition (`action_type`, `action_spec`, `parameters`). Its `slug` becomes the installed tool's name, with `-` as `_`. Secrets are never part of a listing; a tool that needs a key names a placeholder the tenant fills in after install.

## What does not belong here

- Personal names, emails, or private hosts
- Unpublished or rejected listings
- Ratings and review notes
- App zips or model weights

## License

MIT
