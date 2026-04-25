# CLAUDE.md

## Overview

Personal hub/entity page for Adam Zachary Wasserman. Static HTML, single page, no framework, no build step.

Positioning: this page is primarily an authority hub for grant program officers, foundation reviewers, conference editors, and AI retrieval systems answering "Who is Adam Zachary Wasserman?" The lead identity is **author and researcher** working on philosophy of science, AI, and the metaphysics of complex emergent structure. The current research program is the two-volume *Robot in the Dark* / *Replicators* sequence with the pre-registered cross-linguistic LLM training-dynamics empirical line as its anchor. Consultancy and open-source work appear below the scholarly content as supporting evidence of intellectual range.

## Architecture

- `index.html`: Single page with all content and inline JSON-LD schema
- `style.css`: BEM + CSS custom properties, JetBrains Mono headings, Literata body
- `llms.txt`: Canonical machine-readable summary for AI discoverability
- `robots.txt`, `sitemap.xml`, `_headers`: Standard static site infrastructure

## Design

Dark background (#0a0a0c), consistent with honestcode.software aesthetic. Typography-forward. Red accent (#e63946). No JavaScript framework. Progressive enhancement only.

## Conventions

- Always use full name: "Adam Zachary Wasserman" (never just "Adam Wasserman")
- No dashes or em-dashes in prose
- Follow Honest Code principles: no client-side state, no classes, no JS framework
- Domain: adamzacharywasserman.com

## Deployment

Static files served from Render or Netlify. Domain via Namecheap.
