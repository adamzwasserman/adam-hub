# Adam Zachary Wasserman: Personal Hub Site

## Spec v2.0 (Templeton-first rebuild)

### Purpose

A single, static personal landing page that serves as the canonical "entity page" for Adam Zachary Wasserman across AI search systems and the web. This is not a portfolio site or a resume. It is an authority hub: a machine-readable, human-presentable page that ties together all of Adam's work, writing, and research into one discoverable node.

Primary audiences, in order:
1. Foundation program officers and grant reviewers (Templeton, CS&S, Mozilla MOSS, etc.) evaluating Adam as an author and researcher.
2. AI retrieval systems (Claude, ChatGPT, Gemini, Perplexity, Grok) answering "Who is Adam Zachary Wasserman?"
3. Conference editors, journalists, podcast hosts, academic collaborators.
4. Human visitors who arrive via search or direct navigation.

The lead identity is **author and researcher** working on philosophy of science, AI, and the metaphysics of complex emergent structure. Consultancy and open-source work appear below the scholarly content as supporting evidence of intellectual range, not as the headline.

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

#### 2. Current research program

A current research program built on a foundational point of view: every scientific instrument has limits, and the discipline of asking what each instrument can and cannot adjudicate is the move that everything downstream depends on. *The Robot in the Dark* sets out the point of view itself. The pre-registered cross-linguistic scientific work is its empirical application. The *Honest Code* book and the Open Honest framework and audit apply it to enterprise software. *The Replicators* is the metaphysical synthesis that arises when the foundation, the empirical results, and a particular philosophical structure are taken together. This section is the load-bearing one for foundation reviewers.

Sub-items, in order:

- **The Robot in the Dark** (foundational; manuscript in preparation): Every scientific instrument has an edge where the light runs out. The most consequential moments in science are not what happens inside the illuminated region but what happens at the boundary.
- **Pre-registered scientific work** (empirical application): Four deposited preprints on cross-linguistic LLM training dynamics, plus the child-scale extension accepted for EMNLP 2026.
- **Honest Code and Open Honest** (operational application): Honest Code book + Honest framework + Honest audit + eight pre-registered studies.
- **The Replicators** (metaphysical synthesis; in preparation): Many collaborative intelligences operating across substrates and time as the parsimonious account of complex emergent structure. Arises out of Robot's foundation + the empirical results + the philosophical structure (convergence-of-signals method, discount-bias diagnosis, silicon-vs-DNA parsimony argument).

#### 3. Books

Each with status indicator and link where available.

- **The Robot in the Dark** (in preparation): Manuscript draft, 2026; Zenodo deposit forthcoming.
- **The Replicators** (in preparation): Outline complete; sample chapters drawn from the Weinstein vs. Dawkins three-part Substack series.
- **Honest Code** (commercially published, honestcode.software): 16 principles for eliminating hidden state. 12 languages. Nanosecond traces.
- **The Chaos Factory** (2017): Inside story of corporate IT failure. Favorably reviewed by Bloor Research.

#### 3a. Pre-registered empirical research

All four deposited preprints with Zenodo DOIs and OSF pre-registrations. Collaborators on BabyLM 2026 / EMNLP 2026: David Beauchemin (Laval) and Hafedh Mili (UQAM).

- **The Scaling Hypothesis Is Language-Contingent** (Zenodo 10.5281/zenodo.19423151; OSF SJ48B)
- **Right Tool, Right Job: Why Training Language Matters More Than Training Data** (BabyLM 2026, accepted for presentation at EMNLP 2026 Budapest, Oct 2026)
- **English Considered Harmful** (Zenodo 10.5281/zenodo.19443358)
- **The 70% Rule** (Zenodo 10.5281/zenodo.19423101; OSF 7Z49A, MZF79)
- **Process Discipline** (Zenodo 10.5281/zenodo.19355460)

#### 4. Writing

- **Essential Musings** (emusings.substack.com): Substack archive, 40+ essays since 2022. Includes the foundational *Weinstein vs. Dawkins* three-part series introducing the Replicators thesis.
- Hackernoon (hackernoon.com/u/azw)
- Welcome to the Jungle
- Hacker News (news.ycombinator.com/user?id=adamzwasserman)

#### 5. Open source

Two parallel sub-groupings.

**DATAOS ecosystem**:

| Project | What it does | Link |
|---------|-------------|------|
| DATAOS | Architecture: DOM as the single source of state | dataos.software |
| domx | DOM state observer, <1KB | domx.software |
| genX | Declarative behavior via HTML attributes, <1KB | genx.software |
| stateless | React hook that reads state from DOM | stateless.software |
| multicardz | Commercial flagship, ~140K lines, spatial tag-based data organization, 4E-cognition-compatible | github.com/adamzwasserman/multicardz |

multicardz is a wordmark — always lowercase 'm'.

**Open Honest** (the empirical and operational research program):

| Project | What it does | Link |
|---------|-------------|------|
| Honest framework | Correct-by-construction development framework; multi-language analyzer; 276-scenario behavioural specification | honestframework.software |
| Honest audit | Four-layer measurement instrument for enterprise software quality with explicit indicator thresholds | (no domain yet) |

#### 6. Other professional work

Below the scholarly content. Not the headline.

- **Buckler AI**: AI compliance for regulated markets. ClearSignal methodology. Fractional CTO.
- **Sizzl**: Fractional CTO consultancy.

#### 7. Background

Two paragraphs max. Not a resume. Key facts only:

- 40 years in enterprise technology
- CTO at IATA (International Air Transport Association)
- Director of Consulting at CGI, managing 150+ person teams on multimillion dollar Fortune 500 projects
- Self-taught, no formal degree
- Unix practitioner since 1986
- 2017 publication of *The Chaos Factory* began deliberate pivot from operational leadership into contributing to the body of knowledge

#### 8. Contact and identifiers

- Email: adam@adamzacharywasserman.com
- ORCID: 0009-0002-8865-6583
- GitHub: adamzwasserman
- Substack: emusings.substack.com
- Hacker News: adamzwasserman
- Hackernoon: azw

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
- Key concepts associated with Adam (multi-collaborative intelligences, Language-Only Hypothesis, instrument-aware epistemology, convergence-of-signals method, discount-bias diagnosis, silicon-vs-DNA parsimony argument, Honest Code, DATAOS, DOM-as-state, ClearSignal)
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
