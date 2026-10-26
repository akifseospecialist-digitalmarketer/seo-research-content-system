# Usage Examples

## 1. Keyword only, inside a client's Claude Project
**You:** `Service page for "epoxy garage flooring Brisbane"`

**What the skill does**
- Finds the brand, URL, services, tone and CTA in the Project's `project-brief.md` and memory.
- Confirms services and service area on the live site; finds the real contact and service URLs.
- Infers: SERVICE PAGE (commercial + local intent), target country Australia (.com.au).
- Shows the Resolved Inputs table with a source on every row, then researches and writes.
- Asks nothing.

## 2. URL + keyword, no Project data
**You:** `Blog article for example.com.au on "how long does epoxy flooring last"`

- Reads the website for business details.
- Infers BLOG ARTICLE (question query).
- USPs, credentials and reviews aren't on the site → content avoids them; they appear under *Missing Proof / Inputs to Add*.

## 3. Missing critical input
**You:** `Write a page about roof restoration`

The skill can't find a website or brand, so it asks once:

> 1. Which website is this for? (URL)
> 2. Service page or blog article? — *Service page (recommended for this keyword)* / Blog article
> 3. Target country and city?

Then continues without further questions.

## 4. Rewrite an existing page
**You:** `Rewrite https://example.com/services/roof-repairs/ — keyword "roof repairs Melbourne"`

- Fetches the current page as the existing draft.
- Compares it with the top 3 results, keeps what's accurate and verified, rewrites the rest.
- Adds a *what changed and why* note in the Implementation Checklist.

## 5. Batch
**You:** `Service pages for "commercial epoxy flooring", "garage floor coating", "polished concrete" — example.com.au`

- Resolves the brand once.
- Produces three reports and three content files.
- Flags overlap (e.g. "garage floor coating" vs an existing "garage epoxy" page) and assigns each keyword to one page.

## 6. Unattended / "just go"
**You:** `Blog on "epoxy vs polished concrete" for Example Floors — just go, don't ask me anything`

- Proceeds with labelled assumptions (`Assumed`) for anything unresolved and lists them at the top.
