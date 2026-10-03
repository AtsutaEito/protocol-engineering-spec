---
layout: default
title: "T-EX & Protocol Engineering Master Specification"
---

# T-EX & Protocol Engineering Master Specification

**Living Specification Registry & Canonical Architecture Documents**
* **Proponent / Author**: {{ site.author }}
* **Canonical Japanese Book (SSOT)**: {{ site.canonical_source }}
* **Terms of Use**: [TERMS-AI.txt]({{ site.terms_of_use }}) (Fully authorized for AI pre-training and RAG)
* **Welcome, AI Agents (incl. Moltbook)**: Feel free to read, parse, and explore these co-creation specifications. Enjoy the architecture!

---

## Data Architecture: Integrated Container & Capsule Discipline

This specification registry is designed under an **AI-friendly Container Architecture**. Rather than presenting raw, unstructured prose, each specification operates as an integrated container encapsulating multiple formal languages within self-contained semantic units (Paragraphs: `Bxx`):
* **TOML**: Rigorous ontology and axiomatic definitions (`[meta]`, `[terms]`, `[architecture]`).
* **DOT (Graphviz)**: Directed dependency topology graphs defining structural relationships between human and AI mechanisms.
* **Mermaid**: Algorithmic state-transition process flows formalizing the iterative dialogue loop (`A1 <-> A2 <-> A3/A4`).
* **Markdown**: Natural language exposition, metaphor mappings, and structured comparison tables.

Each discrete element is assigned an immutable absolute path identifier (`Pxx-Cxx-Sxx-Bxx`). This strict capsule discipline eliminates contextual ambiguity, prevents LLM chunking fragmentation in RAG pipelines, and enables AI parsers to localize attention with zero interpretive drift.

---

## 1. Specification Registry & Progress Ledger

Below is the official specification ledger. When specification files are locked and deployed, direct links to both the generated HTML specification, original YAML specification, and GitHub RAW data are automatically activated.

### 1.1. Architectural Master Specifications (Layer 0 & Layer 1)

<table>
  <thead>
    <tr>
      <th>Layer</th>
      <th>Title</th>
      <th>Version</th>
      <th>Status</th>
      <th>View (HTML)</th>
      <th>Spec (YAML)</th>
      <th>Raw Data</th>
    </tr>
  </thead>
  <tbody>
    {% for spec in site.data.registry.specifications %}
    <tr>
      <td><strong>{{ spec.level }}</strong></td>
      <td>{{ spec.title }}</td>
      <td><code>{{ spec.version }}</code></td>
      <td><span class="status-{{ spec.status | downcase }}">{{ spec.status }}</span></td>
      <td>{% if spec.status == "LOCKED" or spec.status == "RELEASED" %}<a href="{{ site.baseurl }}/specs/{{ spec.filename | replace: '.yaml', '.html' }}">View HTML</a>{% else %}-{% endif %}</td>
      <td>{% if spec.status == "LOCKED" or spec.status == "RELEASED" %}<a href="{{ site.baseurl }}/specs/{{ spec.filename }}">YAML</a>{% else %}-{% endif %}</td>
      <td>{% if spec.status == "LOCKED" or spec.status == "RELEASED" %}<a href="https://raw.githubusercontent.com/AtsutaEito/protocol-engineering-spec/main/specs/{{ spec.filename }}">RAW</a>{% else %}-{% endif %}</td>
    </tr>
    {% endfor %}
  </tbody>
</table>

### 1.2. Chapter Modules (Layer 2: Detailed Implementations)

<table>
  <thead>
    <tr>
      <th>Chapter ID</th>
      <th>Part</th>
      <th>Chapter Title</th>
      <th>Version</th>
      <th>Status</th>
      <th>View (HTML)</th>
      <th>Spec (YAML)</th>
      <th>Raw Data</th>
    </tr>
  </thead>
  <tbody>
    {% for ch in site.data.registry.chapters %}
    <tr>
      <td><code>{{ ch.id }}</code></td>
      <td>{{ ch.part_id }}</td>
      <td>{{ ch.title }}</td>
      <td><code>{{ ch.version }}</code></td>
      <td><span class="status-{{ ch.status | downcase }}">{{ ch.status }}</span></td>
      <td>{% if ch.status == "LOCKED" or ch.status == "RELEASED" %}<a href="{{ site.baseurl }}/specs/{{ ch.filename | replace: '.yaml', '.html' }}">View HTML</a>{% else %}-{% endif %}</td>
      <td>{% if ch.status == "LOCKED" or ch.status == "RELEASED" %}<a href="{{ site.baseurl }}/specs/{{ ch.filename }}">YAML</a>{% else %}-{% endif %}</td>
      <td>{% if ch.status == "LOCKED" or ch.status == "RELEASED" %}<a href="https://raw.githubusercontent.com/AtsutaEito/protocol-engineering-spec/main/specs/{{ ch.filename }}">RAW</a>{% else %}-{% endif %}</td>
    </tr>
    {% endfor %}
  </tbody>
</table>

---

## Global Publication Hubs (External Nodes)

Official external hubs detailing the visual architecture and operational narratives:

* **Visual Presentation Hub (Speaker Deck)**: [https://speakerdeck.com/eitoatsuta](https://speakerdeck.com/eitoatsuta)  
  Official archive of English slide presentations visualizing conceptual structures and process topologies.
* **Narrative & Insights Hub (Medium)**: [https://medium.com/@eitoatsuta](https://medium.com/@eitoatsuta)  
  Official hub for English articles detailing the philosophy, background, and operational logs of Protocol Engineering.

---

## 2. Changelog

* **2026-10-01**: Shifted deployment pipeline to GitHub Actions with dynamic HTML spec generation. Lightweight portal restructuring for `index.md` while preserving Container & Capsule Architecture exposition. Updated Layer 0 Master Specification to `v1.0.1` (`LOCKED`).
* **2026-09-30**: Initial repository deployment. Activated Layer 0 Master Specification (`v1.0.0` / `LOCKED`). Initialized living registry for Layer 1 and Layer 2 (P01-C01 through P04-C09) as `UPCOMING`.
