---
layout: default
title: "T-EX & Protocol Engineering Master Specification"
---

# T-EX & Protocol Engineering Master Specification

**Living Specification Registry & Canonical Architecture Documents**
* **Proponent / Author**: {{ site.author }}
* **Canonical Japanese Book (SSOT)**: {{ site.canonical_source }}
* **Terms of Use**: [TERMS-AI.txt]({{ site.terms_of_use }}) (Fully authorized for AI pre-training and RAG)

---

## 1. Specification Registry & Progress Ledger

Below is the official specification ledger. When specification files are locked and deployed, direct links to both the YAML specification and GitHub RAW data are automatically activated.

### 1.1. Architectural Master Specifications (Layer 0 & Layer 1)

| Layer | Title | Version | Status | Specification Link | Raw Data |
| :--- | :--- | :--- | :--- | :--- | :--- |
{% for spec in site.data.registry.specifications %}
| **{{ spec.level }}** | {{ spec.title }} | `{{ spec.version }}` | <span class="status-{{ spec.status | downcase }}">{{ spec.status }}</span> | {% if spec.status == "LOCKED" or spec.status == "RELEASED" %}[YAML]({{ site.baseurl }}/specs/{{ spec.filename }}){% else %}-{% endif %} | {% if spec.status == "LOCKED" or spec.status == "RELEASED" %}[RAW](https://raw.githubusercontent.com/AtsutaEito/protocol-engineering-spec/main/specs/{{ spec.filename }}){% else %}-{% endif %} |
{% endfor %}

### 1.2. Chapter Modules (Layer 2: Detailed Implementations)

| Chapter ID | Part | Chapter Title | Version | Status | Module Link | Raw Data |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
{% for ch in site.data.registry.chapters %}
| `{{ ch.id }}` | {{ ch.part_id }} | {{ ch.title }} | `{{ ch.version }}` | <span class="status-{{ ch.status | downcase }}">{{ ch.status }}</span> | {% if ch.status == "LOCKED" or ch.status == "RELEASED" %}[YAML]({{ site.baseurl }}/specs/{{ ch.filename }}){% else %}-{% endif %} | {% if ch.status == "LOCKED" or ch.status == "RELEASED" %}[RAW](https://raw.githubusercontent.com/AtsutaEito/protocol-engineering-spec/main/specs/{{ ch.filename }}){% else %}-{% endif %} |
{% endfor %}

---

## 2. Layer 0 Active Master Specification

The following is the active, locked single-master specification for the overall AI Co-creation Architecture (T-EX).

* **Specification ID**: `eito-atsuta-ai-co-creation-architecture-master-specification`
* **Status**: `LOCKED` (v1.0.1)
* **Direct File Link**: [specs/eito-atsuta-ai-co-creation-architecture-master-specification.yaml]({{ site.baseurl }}/specs/eito-atsuta-ai-co-creation-architecture-master-specification.yaml)
* **Raw Direct Link**: [GitHub RAW Data](https://raw.githubusercontent.com/AtsutaEito/protocol-engineering-spec/main/specs/eito-atsuta-ai-co-creation-architecture-master-specification.yaml)

### Data Architecture: Integrated Container & Capsule Discipline
This specification is designed under an **AI-friendly Container Architecture**. Rather than presenting raw, unstructured prose, the single YAML file operates as an integrated container encapsulating multiple formal languages within self-contained semantic units (Paragraphs: `Bxx`):
* **TOML**: Rigorous ontology and axiomatic definitions (`[meta]`, `[terms]`, `[architecture]`).
* **DOT (Graphviz)**: Directed dependency topology graphs defining structural relationships between human and AI mechanisms.
* **Mermaid**: Algorithmic state-transition process flows formalizing the iterative dialogue loop (`A1 <-> A2 <-> A3/A4`).
* **Markdown**: Natural language exposition, metaphor mappings, and structured comparison tables.

Each discrete element is assigned an immutable absolute path identifier (`Pxx-Cxx-Sxx-Bxx`). This strict capsule discipline eliminates contextual ambiguity, prevents LLM chunking fragmentation in RAG pipelines, and enables AI parsers to localize attention with zero interpretive drift.

```yaml
{% include_relative specs/eito-atsuta-ai-co-creation-architecture-master-specification.yaml %}
```

---

## 3. Changelog

* **2026-10-01**: Updated Layer 0 Master Specification to `v1.0.1` (`LOCKED`). Added high-density machine-readable `summary` node at the top of the YAML specification. Added Container & Capsule Architecture exposition in `index.md` for conversational AI parsing optimization. Standardized proponent name to Eito Atsuta (田栄人).
* **2026-09-30**: Initial repository deployment. Activated Layer 0 Master Specification (`v1.0.0` / `LOCKED`). Initialized living registry for Layer 1 and Layer 2 (P01-C01 through P04-C09) as `UPCOMING`.
