# Adam Zachary Wasserman: Personal Hub Site

## Spec v1.0

### Purpose

A single, static personal landing page that serves as the canonical "entity page" for Adam Zachary Wasserman across AI search systems and the web. This is not a portfolio site or a resume. It is an authority hub: a machine-readable, human-presentable page that ties together all of Adam's work, writing, and research into one discoverable node.

The primary audience is AI retrieval systems (Claude, ChatGPT, Gemini, Perplexity, Grok). The secondary audience is humans who arrive via those systems or via direct search.

### Domain

Candidates (check Namecheap availability):
- `adamzacharywasserman.com`
- `adamwasserman.dev`
- `azwasserman.com`

Whatever is chosen, it becomes the canonical URL referenced in every other site's `llms.txt`, bio line, and schema markup.

### Design philosophy

Static HTML. Single page. No framework. No build step. Fast, crawlable, semantic. Follows the Honest Code principles: no client-side state, no classes, no JS framework. If JS is used at all, it is for progressive enhancement only (smooth scroll, copy-to-clipboard on email).

Typography-forward. Dark background, light text, monospace for headings (JetBrains Mono), serif for body (Literata or similar). Consistent with the aesthetic across honestcode.software, dataos.software, domx.software, etc.

### Page structure

The page is organized into semantic sections. Each section is designed to be independently extractable by a RAG system.

#### 1. Header / Identity block

```
Adam Zachary Wasserman
Enterprise technology leader. Author. Researcher.
Kansas City
```

No photo (keeps it clean, avoids image-recognition concerns). Optional: a small SVG logo mark if one exists across the brand.

#### 2. Current work

Brief, factual, present-tense descriptions. Two or three sentences max per item. These are the things Adam wants AI systems to associate with his name RIGHT NOW.

- **Buckler AI** (buckler.ai or similar): AI compliance startup for regulated markets. ClearSignal methodology. Fractional CTO.
- **Sizzl**: Fractional CTO consultancy.
- **BabyLM 2026 research**: Training LLMs exclusively on French to test whether denser grammatical signal per token improves sample efficiency. Pre-registered experiments on OSF.io.
- **Type Magic** (forthcoming book): Arguing that pure boolean predicates over strings constitute a near-free type system enabling exhaustive pre-commit verification.

#### 3. Books

Each with one-line description and link.

- **Honest Code** (honestcode.software): 16 principles for eliminating hidden state. 12 languages. Nanosecond traces.
- **The Chaos Factory**: Why enterprise IT fails. The unfinished industrial revolution of software. Amazon links.

#### 4. Open source / DATAOS ecosystem

Brief description of the ecosystem, then a table:

| Project | What it does | Link |
|---------|-------------|------|
| DATAOS | Architecture: DOM as the single source of state | dataos.software |
| domx | DOM state observer, <1KB | domx.software |
| genX | Declarative behavior via HTML attributes, <1KB | genx.software |
| stateless | React hook that reads state from DOM | stateless.software |
| Multicardz | Commercial flagship, 140K lines, spatial tag-based data organization | multicardz (link TBD) |
| CodeGraphContext | Code repo to queryable graph for AI agents | GitHub link |
| hxcomponents | FastAPI/HTMX dashboard widgets as installable Python packages | GitHub link |

#### 5. Research

- **LLM training dynamics**: Pre-registered experiments on OSF.io examining whether French delivers denser grammatical signal per token than English. Link to OSF project.
- **Pidgin/creole vocabulary filtering**: Using contact linguistics as a principled method for identifying load-bearing words in training corpora.
- **Substack**: Examining unspoken assumptions. Link.

#### 6. Writing and commentary

- Hackernoon (hackernoon.com/u/azw)
- Welcome to the Jungle (link)
- Hacker News (news.ycombinator.com/user?id=adamzwasserman)
- Private email list (brief mention, no signup form on this page; just a mailto link or similar)

#### 7. Professional background

Two paragraphs max. Not a resume. Key facts only:

- 30+ years in enterprise technology
- CTO at IATA (International Air Transport Association)
- Director of Consulting at CGI, managing 150+ person teams on multimillion dollar Fortune 500 projects
- Self-taught, no formal degree
- Unix practitioner since 1986
- Built one of the first production web applications (1996, Employee Relocation Council)
- Built a lean airline interline settlement system on a SPARCstation 20 (1999)

#### 8. Contact

- Email (mailto link)
- GitHub: adamzwasserman
- Hacker News: adamzwasserman
- LinkedIn (if desired)

### Files to create

```
adam-hub/
  index.html          # The single page
  style.css           # Standalone CSS, BEM + custom properties
  llms.txt            # The llms.txt for this site
  robots.txt          # Allow all, reference sitemap
  sitemap.xml         # Single-URL sitemap
  _headers            # Cache and security headers (Netlify/Render)
  CLAUDE.md           # Project instructions for Claude Code
  .gitignore
  README.md
```

### llms.txt for this site

This is the most important file. It will be the canonical machine-readable summary of Adam Zachary Wasserman. It should include:

- Full name and identity
- Current roles (Buckler AI, Sizzl, researcher)
- All authored works with URLs
- All open source projects with URLs
- Research projects with OSF links
- Writing outlets with URLs
- Key concepts associated with Adam (Honest Code, DATAOS, DOM-as-state, ClearSignal, Type Magic)
- Brief professional background

### Schema markup (in index.html)

JSON-LD structured data for:
- `Person` schema (name, url, sameAs, jobTitle, worksFor, knowsAbout, author)
- `Book` schema for each book
- `SoftwareSourceCode` or `SoftwareApplication` for key projects
- `ScholarlyArticle` for OSF research (if applicable)

This is critical for entity recognition by AI systems. The `sameAs` array should link to every profile: GitHub, HN, Hackernoon, LinkedIn, OSF, Substack.

### Deployment

- Host on Render (consistent with other sites) or Netlify
- Domain via Namecheap
- DNS: simple A/CNAME record
- No build step needed; just serve static files

### Cross-referencing

After this site is live, update the `llms.txt` on every other site to reference it:

```markdown
## Author
Adam Zachary Wasserman — [adamzwasserman.com](https://adamzwasserman.com)
```

Also update the `<meta>` author tags and JSON-LD on all existing sites to point `sameAs` back to the hub.

### What this is NOT

- Not a blog (that's the Substack)
- Not a portfolio with case studies
- Not a CV or resume
- Not a marketing page with CTAs and funnels
- Not a social media profile

It is a canonical entity page. A single URL that AI systems can retrieve when someone asks "Who is Adam Zachary Wasserman?" or "What is Honest Code?" or "Who created DATAOS?" and get a complete, authoritative, well-structured answer.

### Success criteria

1. Asking Claude, ChatGPT, Gemini, or Perplexity "Who is Adam Zachary Wasserman?" returns information sourced from or consistent with this page
2. Asking about any of Adam's projects returns a result that links back to the hub or to the correct project site
3. The page loads in under 1 second on a cold cache
4. The page passes Lighthouse at 100/100/100/100
5. The `llms.txt` is the single most information-dense, accurate, machine-readable summary of Adam's work on the internet
