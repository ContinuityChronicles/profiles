# Example Profile

This is a demonstration profile showing the proper structure for ContinuityChronicles investigative timelines.

---

## Subject Overview

**Profile ID:** `example-profile`  
**Created:** 2026-01-31  
**Maintainer:** ContinuityChronicles Team  
**Status:** Active (Example/Template)  

---

## About This Profile

This profile serves as a **reference implementation** demonstrating how to properly document and fact-check an individual's narrative over time. It shows:

- Proper folder structure for profiles and events
- Correct usage of `event.yaml` metadata files
- Well-formatted `README.md` documentation
- The Claims vs. Records framework
- Asset organization and archiving best practices

**Note:** This is a fictional example profile. Use it as a template when creating real investigative profiles.

---

## Subject Background

[In a real profile, this section would contain:]

- Who the subject is (public figure, organization, etc.)
- Why their narrative is being documented
- Brief summary of the contradictions or inconsistencies that prompted investigation
- Any relevant public context

**Example:**

> John Doe is a public figure who has made numerous claims about their educational background, business history, and personal achievements. Multiple versions of key life events have been documented across interviews, social media, and official filings, with significant contradictions emerging when compared chronologically.

---

## Key Contradictions Summary

| Topic | Versions Found | Severity | Key Events |
|-------|----------------|----------|------------|
| Example Topic | 2+ | Medium | `2026-01-31-example-event` |

[This table provides a quick overview of the main areas of inconsistency being tracked.]

---

## Timeline Events

| Date | Event ID | Title | Type | Status |
|------|----------|-------|------|--------|
| 2026-01-31 | `2026-01-31-example-event` | Example Event Title | statement | final |

---

## Profile Conventions

### Severity Scale

This profile uses the **text scale** for rating the significance of contradictions:

| Level | Definition | Example |
|-------|------------|---------|
| `low` | Minor inconsistency, could be memory error | Date off by a few months |
| `medium` | Notable contradiction worth documenting | Different versions of same story |
| `high` | Major contradiction, pattern of deception | Fabricated credentials |

### Verification Status

| Status | Meaning |
|--------|---------|
| `verified` | Confirmed true with documentation |
| `unverified` | Cannot confirm or deny |
| `disputed` | Conflicting evidence exists |
| `debunked` | Proven false with documentation |
| `partially-true` | Some elements verified, others not |

### People References

This profile uses the following conventions for referencing people:

- **Subject:** Referred to by name or "the subject"
- **Third parties:** Full names when public figures, initials or roles when private individuals
- **Handles:** Include @ symbol for social media handles

### Source Standards

All events in this profile must include:

- [ ] At least one primary source (direct quote, document, or screenshot)
- [ ] Archive links for any URLs that could disappear
- [ ] Timestamps for video/audio sources
- [ ] Capture dates for screenshots

---

## Tags Used

| Category | Tags |
|----------|------|
| **Source Type** | `statement`, `interview`, `document`, `social-media` |
| **Analysis** | `contradiction`, `version-change`, `example` |
| **Topic** | `operations`, `security` |
| **Status** | `verified`, `unverified` |

---

## Contributing to This Profile

### Before Adding Events

1. Search existing events to avoid duplicates
2. Verify your sources are legitimate
3. Archive all URLs before they disappear
4. Follow the event template exactly

### Event Naming

Events should be named: `YYYY-MM-DD-brief-description`

Examples:
- `2024-03-15-podcast-interview-claim`
- `2024-01-10-twitter-education-statement`
- `2023-11-01-court-filing-contradiction`

### Pull Request Requirements

- [ ] `event.yaml` follows the schema
- [ ] `README.md` follows the template
- [ ] All sources are cited and archived
- [ ] Screenshots include capture dates
- [ ] No private/non-public information included

---

## Related Resources

- [Event Schema Documentation](../_schema/event.schema.yaml)
- [Event Template](../_schema/EVENT_TEMPLATE.md)
- [Naming Conventions](../_schema/CONVENTIONS.md)

---

## Disclaimer

This profile documents publicly available statements and records for research and accountability purposes. All information is sourced from public records, interviews, social media posts, and other publicly accessible materials.

This is not a platform for harassment. Contributors must:
- Present facts neutrally without editorializing
- Cite verifiable sources for all claims
- Distinguish between documented facts and analysis
- Respect legal boundaries

---

*Last Updated: 2026-01-31*