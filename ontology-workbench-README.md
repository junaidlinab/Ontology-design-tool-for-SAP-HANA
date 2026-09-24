# SAP Ontology Workbench

A design-time tool for building SAP-aware ontologies for the SAP HANA Cloud Knowledge Graph Engine. It reads SAP metadata (CSN / ODM), helps you shape an ontology around the questions you actually need answered, and exports it in standard formats.

## What it does

The workbench follows a competency-question-driven method: you decide what the graph must answer first, then model only what serves those questions, instead of modelling the whole domain up front.

Workflow:

1. Load a CSN or ODM metadata file. The tool shows you what it contains.
2. State the business questions you want the ontology to answer (competency questions).
3. The tool proposes an ontology (classes, relationships, constraints) scoped to those questions.
4. Review and adjust the proposal.
5. Test it against sample data.
6. Export OWL and SHACL, with Turtle and SPARQL, ready for the SAP HANA Cloud Knowledge Graph Engine.

## Why

SAP metadata (CSN and ODM) carries real meaning: annotations, associations and cardinality. A generic relational-to-graph mapping loses that. This tool reads the SAP semantics and turns them into an SAP-aware ontology, scoped to what the business needs rather than a boil-the-ocean model.

## Running it

It is a single self-contained HTML file. You can either:

* Open it directly: download `ontology-workbench.html` and double-click it. It runs in your browser and loads React and Tailwind from a CDN.
* Or use the hosted version via GitHub Pages: (add your Pages URL here once enabled)

You will need:

* A modern browser
* An Anthropic API key, entered in the app at runtime
* A CSN or ODM metadata file to work from

## About the API key

The app calls the Anthropic API to help propose the ontology. You supply your own key at runtime. The key is held in tab memory only for the session, and is not stored, saved or transmitted anywhere else. Closing the tab clears it. No key is bundled in the file.

## Output formats

OWL, SHACL, Turtle, SPARQL.

## Status

This is a working prototype and reference implementation, shared to show the approach. Treat a generated ontology as a starting point for review, not a finished model.

## Author

Junaid Ahmed, 
Contact: junaid.linab@gmail.com
