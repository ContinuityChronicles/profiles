# ContinuityChronicles Profiles

This public repository contains investigative timeline data for documenting and fact-checking the narratives of individuals whose stories contain contradictions, inconsistencies, or disputed claims.

---

## Purpose

ContinuityChronicles is designed to:

- **Track multiple versions** of the same story as told over time
- **Document contradictions** between different accounts or statements
- **Compare claims vs. records** — what someone says happened vs. documented evidence
- **Preserve sources** with links, screenshots, and archived references
- **Highlight inconsistencies** that emerge when events are viewed chronologically

### What This Is NOT

- A platform for harassment or personal attacks
- A place for unverified accusations or rumors
- A tool for doxxing or exposing private information

All documented events must be based on **verifiable, cited sources** and presented **neutrally without editorializing**.

---

## Repository Structure

```
/profiles
├── /_schema                    # Schema documentation and templates
│   ├── EVENT_TEMPLATE.md       # Template for event README files
│   ├── event.schema.yaml       # YAML schema documentation
│   └── CONVENTIONS.md          # Naming conventions and guidelines
│
└── /{profile-slug}             # Individual subject profiles
    ├── profile.yaml            # Profile metadata (optional)
    ├── README.md               # Subject overview and context
    └── /events
        └── /{event-id}         # Event folder (e.g., 2024-03-15-interview-claim)
            ├── event.yaml      # Structured event metadata
            ├── README.md       # Human-readable documentation
            └── /assets         # Screenshots, archives, supporting files
                ├── screenshot-tweet.png
                └── archived-interview.pdf
```

---

## Quick Start

### Creating a New Profile (Subject)

1. Create a folder with a kebab-case slug: `/profiles/subject-name/`
2. Add a `README.md` with context about who the subject is and why they're being documented
3. Create an `/events` subfolder for timeline entries

### Adding an Event

1. Create an event folder: `/profiles/{subject}/events/YYYY-MM-DD-event-slug/`
2. Copy the template from `/_schema/EVENT_TEMPLATE.md` to `README.md`
3. Create `event.yaml` with structured metadata
4. Add supporting evidence to `/assets` (screenshots, archives, etc.)

---

## Event Types

| Type | Description | When to Use |
|------|-------------|-------------|
| `statement` | Public statement, interview, or claim | Press conferences, podcasts, interviews |
| `document` | Official record or filing | Court docs, financial filings, contracts |
| `social-media` | Posts, tweets, or online content | Tweets, Instagram, TikTok, blog posts |
| `contradiction` | Direct conflict between accounts | Documenting Story A vs Story B |
| `evidence` | Supporting documentation | Screenshots, receipts, archives |
| `timeline-gap` | Notable absence or unexplained period | Missing time, deleted content |
| `third-party` | Account from someone else | Witness statements, other interviews |

---

## The Claims vs. Records Framework

The most important section of any event is **Claims vs. Records**. Use this whenever:

- The subject's account differs from documented evidence
- Multiple versions of the same story exist
- Third-party accounts contradict the subject's narrative
- Official records don't match public statements

### Example Structure

```markdown
### Claim A
- **Claim:** "I graduated from Harvard in 2010"
- **Attributed to:** Interview on Podcast X, Episode 42
- **Date asserted:** 2023-05-15
- **Notes:** Subject made this claim unprompted

### Record A
- **Record:** Harvard has no graduation record for this individual
- **Source:** FOIA request response (see assets/harvard-foia.pdf)
- **Why it conflicts:** No record exists; subject later changed claim to "attended"
```

---

## Evidence Standards

### Required for All Events

- [ ] At least one primary source link or archived reference
- [ ] Date of the event or claim
- [ ] Clear attribution (who said it, where, when)

### Best Practices

- **Archive everything** — Use archive.org, archive.today, or screenshots
- **Capture metadata** — Note timestamps, URLs, platform context
- **Multiple sources** — Corroborate claims when possible
- **Original context** — Don't cherry-pick; include surrounding context

### Asset Naming

```
screenshot-{platform}-{date}.png     → screenshot-twitter-2024-03-15.png
archive-{source}-{description}.pdf   → archive-interview-podcast-name.pdf
document-{type}-{date}.pdf           → document-court-filing-2023-11-01.pdf
```

---

## Tags

Use consistent tags across events for filtering and analysis:

| Category | Tags |
|----------|------|
| **Source Type** | `statement`, `interview`, `document`, `social-media`, `legal-filing`, `financial` |
| **Analysis** | `contradiction`, `inconsistency`, `version-change`, `retraction`, `pattern` |
| **Evidence** | `screenshot`, `archived`, `video`, `audio`, `receipts` |
| **Verification** | `verified`, `unverified`, `disputed`, `debunked`, `confirmed` |
| **Severity** | `minor-inconsistency`, `major-contradiction`, `pattern-of-deception` |

---

## Contributing

### Before You Contribute

1. **Verify sources** — Don't add unverified claims
2. **Stay neutral** — Document facts, not opinions
3. **Cite everything** — Every claim needs a source
4. **Archive proactively** — Links die; screenshots don't

### Contribution Process

1. **Fork** this repository
2. Create or update profile/event following the schema
3. Ensure all files follow templates and conventions
4. Submit a **Pull Request** with clear description
5. Be prepared to provide additional sources if requested

### What Will Be Rejected

- Unverified accusations without sources
- Editorialized or biased language
- Personal attacks or harassment
- Private information (addresses, phone numbers, non-public data)
- Content that could constitute defamation

---

## Legal & Ethical Guidelines

### Do

- Document public statements and actions
- Use publicly available records
- Present information neutrally
- Distinguish between facts and analysis
- Acknowledge uncertainty when it exists

### Don't

- Publish private/non-public information
- Make claims you can't source
- Editorialize or inject personal opinions
- Coordinate harassment
- Ignore context that contradicts your narrative

---

## Schema Documentation

Detailed schema documentation is available in the `/_schema` folder:

- **[EVENT_TEMPLATE.md](./_schema/EVENT_TEMPLATE.md)** — Copy this when creating new events
- **[event.schema.yaml](./_schema/event.schema.yaml)** — Complete YAML field definitions
- **[CONVENTIONS.md](./_schema/CONVENTIONS.md)** — Naming and style guidelines

---

## Related

- **Profiles Repository**: https://github.com/ContinuityChronicles/profiles
- **Frontend Application**: Private repository for the ContinuityChronicles web interface
- **Documentation**: See `/_schema` for detailed schema and template documentation

---

*Remember: The goal is truth and accountability through rigorous documentation, not harassment or defamation. Every entry should be something you'd be comfortable defending with evidence.*