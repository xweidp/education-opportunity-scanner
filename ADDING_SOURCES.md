# Adding Private Foundation or State Funding Sources

The Monday scanner now supports two kinds of sources:

1. **Structured federal search**
   - Grants.gov API
   - Good deadlines and metadata

2. **Private/state source watchlist**
   - Foundation and state funding pages
   - Best-effort link extraction
   - Often no clean deadline, so these appear as monitored source leads

## Add a Source

Edit:

```text
data/source-watchlist.json
```

Add a new object to the `sources` list:

```json
{
  "name": "Example Foundation",
  "type": "Private foundation",
  "url": "https://example.org/grants",
  "keywords": ["education", "research", "postsecondary", "student success", "grant"]
}
```

Use `"type": "State funding"` for state pages.

## Good Keywords

Use words likely to appear on the funder's page:

- `education`
- `research`
- `grant`
- `rfp`
- `rfa`
- `postsecondary`
- `student success`
- `stem`
- `teacher`
- `assessment`
- `secondary data`
- `evaluation`
- `workforce`

## Current Watchlist

The starter watchlist includes:

- Spencer Foundation
- William T. Grant Foundation
- IES Funding Opportunities
- Lumina Foundation
- Gates Foundation committed grants page
- Walton Family Foundation grants page
- California Department of Education funding
- New York State Education Department funding
- Texas Education Agency grants

These pages do not all expose clean application deadlines. The scanner therefore treats them as monitored source pages and extracts likely funding links when possible.
