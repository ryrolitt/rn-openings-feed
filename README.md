# rn-openings-feed

A postings-only feed of San Francisco Bay Area RN job openings, regenerated about hourly
from one person's job-hunt tooling. It carries facts about postings and nothing about any
applicant: employer, title, location, URL, when it was found, the employer's own experience
sentence and a model's read of whether a new grad is eligible, and for tracked entries the
close date as read on the employer's page plus its source.

- `openings.json`: the machine-readable feed (`schema_version`, `generated_at`, `postings[]`,
  each with a stable `id`).
- `index.html`: the same rows as a filterable page.

Consumer: [rn-apply-kit](https://github.com/ryrolitt/rn-apply-kit) (`scripts/fetch_feed.py`).

A row here is a pointer. Every date and requirement is verified on the employer's own page
before anyone acts on it; a model's "new grad" read is a hint, not a ruling.
