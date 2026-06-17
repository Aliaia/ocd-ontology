# OCD Ontology

A comprehensive ontology for Obsessive-Compulsive Disorder (OCD) developed at Cardiff University.

**Permanent URI:** https://w3id.org/ocd  
**BioPortal:** https://bioportal.bioontology.org/ontologies/OCD  
**Version:** 1.0 (2026)  
**Licence:** [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)

---

## Description

The OCD Ontology provides a formal, comprehensive representation of Obsessive-Compulsive Disorder and its related constructs, developed from authoritative clinical sources (DSM-5, Y-BOCS) and validated by domain experts. It is the first OCD-specific ontology to model the obsession–compulsion relational structure in Description Logic terms.

**Key statistics:**
- 80 OCD-specific named classes
- 14 object properties
- 9 external biomedical ontologies integrated (BFO, DOID, GSSO, ADL, MFOEM, MFOMD, GO, SYMP, SNOMED-CT)
- 576 OntoLex-Lemon lexical entries (concept and property enrichment)
- 12,878 triples total

---

## Repository contents

| File | Description |
|---|---|
| `ocd.owl` | Full enriched ontology — OWL/XML format (BioPortal submission) |
| `ocd.ttl` | Full enriched ontology — Turtle format (SPARQL-ready) |
| `ocd-base.owl` | Base ontology — formal definitions and reuse axioms only, without lexical enrichment |

---

## Ontology structure

The ontology is organised into three layers:

**Base layer** — 80 OCD-specific classes with formal Description Logic definitions, covering: the disorder and its classification within OCRDs; the core concepts of Obsession and Compulsion; three constituent intrusive experience types (Intrusive Thought, Image, Urge); eight thematic obsession subtypes; typed intrusive concepts (24 classes); compulsive behaviour types; risk factors; functional impairment types; severity assessment dimensions; treatments; and comorbid OCRD-spectrum disorders.

**Reuse layer** — integration of nine external biomedical ontologies through five documented reuse strategies, including equivalence linking to MFOMD, DOID, GSSO, and MFOEM, direct import from ADL, GO, and SYMP, referential linking to SNOMED-CT, and BFO upper-ontology alignment.

**Enrichment layer** — systematic lexical enrichment using OntoLex-Lemon and the FrAC extension, providing curated WordNet-derived synonyms for all 80 concepts and alternative surface expressions for seven OCD-specific object properties.

---

## Methodology

Developed using a two-stage human–machine methodology:

- **Stage 1:** Formal concept definitions validated through expert survey (n=34 clinicians, 84–97% agreement)
- **Stage 2:** Object property enrichment validated by independent clinical adjudication and benchmarked against two frontier LLMs

Full methodology described in the journal paper (see Citation below).

---

## Usage

### Loading in Protégé
Open `ocd.owl` directly in Protégé 5.x. The HermiT reasoner can be used for DL classification.

### SPARQL queries
The Turtle file (`ocd.ttl`) can be loaded into any SPARQL endpoint. Example query to retrieve all obsession subtypes:

```sparql
PREFIX ocd: <https://w3id.org/ocd#>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>

SELECT ?subtype WHERE {
  ?subtype rdfs:subClassOf ocd:Obsession .
}
```

### BioPortal
Browse classes, properties, and mappings interactively at https://bioportal.bioontology.org/ontologies/OCD

---

## Citation

If you use this ontology, please cite:

```
Muhajab, A., Abdelmoty, A. I., and Hassoulas, A. (2026). Development, Evaluation, 
and Enrichment of an OCD Ontology: A Two-Stage Human–Machine Methodology. 
```

The preliminary version of this work was presented at:
```
Muhajab, A., Abdelmoty, A. I., and Hassoulas, A. (2023). Reuse and Enrichment 
for Building an Ontology for Obsessive-Compulsive Disorder. 
ICBO 2023, CEUR Workshop Proceedings, Vol. 3637.
```

---

## Contact

- **Alia I. Abdelmoty** (PI) — AbdelmotyA@cardiff.ac.uk
- **Areej Muhajab** — MuhajabA@cardiff.ac.uk
- School of Computer Science & Informatics, Cardiff University, Wales, UK

---

## Acknowledgements

The doctoral thesis underpinning this work is available via the Cardiff University ORCA open-access repository.
