# ContinuityChronicles Naming & Style Conventions

This document establishes consistent naming conventions and style guidelines for all contributors to the ContinuityChronicles profiles repository.

---

## Table of Contents

1. [File & Folder Naming](#file--folder-naming)
2. [Event ID Format](#event-id-format)
3. [Date Formats](#date-formats)
4. [Tags](#tags)
5. [People References](#people-references)
6. [Systems & Services](#systems--services)
7. [Writing Style](#writing-style)
8. [Markdown Formatting](#markdown-formatting)
9. [Asset Files](#asset-files)
10. [Status Definitions](#status-definitions)
11. [Severity Levels](#severity-levels)

---

## File & Folder Naming

### General Rules

| Element | Convention | Example |
|---------|------------|---------|
| Profile folders | `lowercase-kebab-case` | `project-alpha/` |
| Event folders | `YYYY-MM-DD-descriptive-slug` | `2026-01-31-server-outage/` |
| Asset files | `lowercase-with-hyphens.ext` | `error-screenshot.png` |
| Schema files | `lowercase-with-hyphens.ext` | `event.schema.yaml` |

### Do's and Don'ts

```
✅ DO
───────────────────────────────
my-profile-name/
2024-03-15-database-migration/
screenshot-error-log.png
meeting-notes-draft.pdf

❌ DON'T
───────────────────────────────
My_Profile_Name/
DatabaseMigration/
Screenshot Error Log.png
Meeting Notes (Draft).pdf
```

### Character Restrictions

- Use only lowercase letters (`a-z`), numbers (`0-9`), and hyphens (`-`)
- No spaces, underscores, or special characters in folder/file names
- No leading or trailing hyphens
- No consecutive hyphens (`--`)

---

## Event ID Format

Event IDs serve as unique identifiers and MUST match their folder name.

### Format

```
YYYY-MM-DD-descriptive-slug
```

### Components

| Part | Description | Example |
|------|-------------|---------|
| `YYYY` | Four-digit year | `2026` |
| `MM` | Two-digit month (zero-padded) | `01` |
| `DD` | Two-digit day (zero-padded) | `31` |
| `descriptive-slug` | Kebab-case description | `server-outage` |

### Slug Guidelines

- Keep slugs concise but meaningful (2-5 words ideal)
- Use present tense verbs when describing actions
- Avoid articles (a, an, the) unless necessary for clarity
- Be specific enough to distinguish from similar events

### Examples

```
✅ Good Event IDs
───────────────────────────────
2024-03-15-production-db-outage
2023-11-01-v2-api-launch
2025-06-30-security-audit-findings
2024-01-15-ceo-resignation-announced

❌ Bad Event IDs
───────────────────────────────
2024-3-15-outage            # Month not zero-padded
march-15-2024-outage        # Wrong date format
2024-03-15-the-big-outage   # Unnecessary article
2024-03-15                   # No description
outage-march-2024           # Missing proper date prefix
```

---

## Date Formats

### Standard Format

Always use **ISO-8601** format: `YYYY-MM-DD`

| Field | Format | Example |
|-------|--------|---------|
| Single date | `YYYY-MM-DD` | `2026-01-31` |
| Date range (YAML) | `date` + `end_date` | `2026-01-31` to `2026-02-02` |
| Date range (text) | `YYYY-MM-DD to YYYY-MM-DD` | `2026-01-31 to 2026-02-02` |

### Time Formats (When Needed)

If time precision is required in narrative text:

- Use 24-hour format with timezone: `14:32 UTC`
- Include timezone abbreviation always
- For timestamps: `YYYY-MM-DDTHH:MM:SSZ` (ISO-8601)

### Examples in Text

```markdown
✅ Good
───────────────────────────────
The incident occurred on 2024-03-15.
Service was restored at 16:32 UTC.
The outage lasted from 2024-03-15 to 2024-03-17.

❌ Bad
───────────────────────────────
The incident occurred on March 15, 2024.
The incident occurred on 03/15/24.
Service was restored at 4:32 PM.
```

---

## Tags

Tags enable filtering and categorization across the timeline.

### Format Rules

- All lowercase
- Use hyphens for multi-word tags: `data-breach`
- No spaces, underscores, or special characters
- Singular form preferred: `incident` not `incidents`

### Standard Tag Categories

Use these established tags when applicable before creating new ones:

#### Event Type
- `incident`
- `announcement`
- `launch`
- `acquisition`
- `legal`
- `policy-change`

#### Domain
- `security`
- `operations`
- `financial`
- `communications`
- `personnel`
- `technical`
- `legal`

#### Impact
- `data-loss`
- `service-outage`
- `user-impact`
- `regulatory`

#### Priority/Attention
- `high-priority`
- `disputed`
- `unverified`
- `needs-review`

### Creating New Tags

Before creating a new tag:
1. Check if an existing tag covers the concept
2. Use the most general applicable term
3. Document profile-specific tags in the profile's README

---

## People References

### Format Options

| Format | When to Use | Example |
|--------|-------------|---------|
| Full Name | Public figures, official records | `John Smith` |
| Handle | Online identities, pseudonyms | `@johndoe` |
| Role | When name is unknown/irrelevant | `Lead Engineer` |
| Pseudonym | Privacy protection | `Employee A` |

### Guidelines

- Be consistent within a profile
- Document your convention in the profile README
- Use handles with `@` prefix for online identities
- For privacy-sensitive profiles, prefer roles or pseudonyms
- When using real names, ensure there's a legitimate reason

### Example Conventions

```yaml
# For a corporate timeline (use roles)
people:
  - "CEO"
  - "Engineering Lead"
  - "External Auditor"

# For a public figure timeline (use names)
people:
  - "Jane Doe"
  - "@janedoe"
  - "John Smith (CFO)"

# For privacy-conscious documentation
people:
  - "Employee A"
  - "Witness 1"
  - "Anonymous Source"
```

---

## Systems & Services

### Naming Guidelines

- Use the official product/service name when known
- Use lowercase-kebab-case for internal systems: `auth-service`
- Be specific: `production-database` not just `database`
- Include version if relevant: `api-v2`

### Examples

```yaml
systems:
  # External services (official names)
  - "AWS S3"
  - "Cloudflare"
  - "GitHub Actions"
  
  # Internal systems (kebab-case)
  - "production-db"
  - "api-gateway"
  - "auth-service"
  - "internal-dashboard"
```

---

## Writing Style

### Tone

- **Neutral and factual**: Avoid editorializing
- **Clear and concise**: Prefer short sentences
- **Chronological**: Present events in time order
- **Source-attributed**: Cite where information comes from

### Voice

- Use **past tense** for describing events: "The server crashed at 14:00."
- Use **present tense** for facts that remain true: "The API uses OAuth 2.0."
- Use **active voice** when possible: "The team deployed a fix" not "A fix was deployed"

### Objectivity

When documenting disputed events:

```markdown
✅ Good (neutral)
───────────────────────────────
According to the press release, the company stated that no user data was accessed.
However, security researcher @example reported finding exposed credentials.

❌ Bad (editorialized)
───────────────────────────────
The company lied about the breach. They obviously knew about it for months.
```

### Abbreviations

- Define abbreviations on first use: "The Application Programming Interface (API) was..."
- Common tech abbreviations (API, URL, HTTP) don't need definition
- Create a glossary in the profile README for domain-specific terms

---

## Markdown Formatting

### Headings

- Use ATX-style headings (`#`, `##`, etc.)
- Include a blank line before and after headings
- Don't skip heading levels (e.g., `#` to `###`)

### Lists

- Use `-` for unordered lists
- Use `1.` for ordered lists (let markdown handle numbering)
- Indent nested items with 2 spaces

### Links

```markdown
# Inline links (preferred for short references)
See the [official documentation](https://example.com).

# Reference links (for repeated or long URLs)
See the [official documentation][docs].

[docs]: https://example.com/very/long/documentation/path
```

### Code and Commands

- Inline code: `` `variable_name` ``
- Code blocks: Use fenced blocks with language identifier

```markdown
```yaml
id: "example"
```
```

### Tables

- Use for structured data comparisons
- Align columns for readability in source

```markdown
| Column 1 | Column 2 | Column 3 |
|----------|----------|----------|
| Data A   | Data B   | Data C   |
```

---

## Asset Files

### Supported Formats

| Type | Preferred Formats | Notes |
|------|-------------------|-------|
| Images | `.png`, `.jpg`, `.webp` | PNG for screenshots, JPG for photos |
| Documents | `.pdf`, `.md` | PDF for official docs, MD for notes |
| Data | `.json`, `.csv`, `.yaml` | Use appropriate format for data type |

### File Size Guidelines

- Images: Optimize to < 500KB when possible
- Documents: Keep under 10MB
- Consider linking to external hosting for large files

### Naming Convention

```
[type]-[description]-[date-if-relevant].[ext]

Examples:
───────────────────────────────
screenshot-error-dashboard.png
document-press-release-2024-03-15.pdf
graph-user-growth-q1-2024.png
archive-email-thread.pdf
```

### Alt Text and Captions

Always provide meaningful captions in `event.yaml`:

```yaml
images:
  - path: "assets/error-rate-graph.png"
    caption: "Error rate spike showing 500% increase during outage window"
```

---

## Status Definitions

| Status | Definition | When to Use |
|--------|------------|-------------|
| `draft` | Work in progress | Initial documentation, incomplete research |
| `final` | Complete and verified | Fully documented, sources cited |
| `archived` | Historical, possibly outdated | Superseded events, old versions |

### Transitioning Status

1. Start all new events as `draft`
2. Move to `final` only when:
   - All sections are complete
   - Sources are cited
   - Key points are verified
3. Move to `archived` when:
   - Information is superseded
   - Event is no longer relevant
   - Significant updates would require a new event

---

## Severity Levels

### Text Scale

| Level | Definition | Example |
|-------|------------|---------|
| `low` | Minor impact, easily resolved | Brief service degradation |
| `medium` | Moderate impact, notable but contained | Partial outage, data delay |
| `high` | Major impact, widespread effects | Complete outage, data breach |

### Numeric Scale (1-5)

| Level | Severity | Definition |
|-------|----------|------------|
| `1` | Minimal | Cosmetic or minor issue |
| `2` | Low | Limited impact, workaround available |
| `3` | Medium | Significant but contained impact |
| `4` | High | Major impact on operations |
| `5` | Critical | Severe, organization-wide impact |

### Usage

- Choose ONE scale (text or numeric) per profile
- Document the chosen scale in the profile README
- Use `null` for events where severity doesn't apply

---

## Quick Reference Card

```
PROFILES
────────────────────────────────────────
Folder:     lowercase-kebab-case/
Example:    project-timeline/

EVENTS
────────────────────────────────────────
Folder:     YYYY-MM-DD-slug/
Example:    2024-03-15-server-outage/
Required:   event.yaml, README.md

ASSETS
────────────────────────────────────────
Location:   events/{id}/assets/
Naming:     lowercase-with-hyphens.ext
Example:    screenshot-error-log.png

DATES
────────────────────────────────────────
Format:     YYYY-MM-DD (ISO-8601)
Example:    2026-01-31

TAGS
────────────────────────────────────────
Format:     lowercase, kebab-case
Example:    security, data-breach

STATUS
────────────────────────────────────────
Options:    draft | final | archived
```

---

*Last Updated: 2025*