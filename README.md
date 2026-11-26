# Awesome AI Context Layers

# Databricks Genie Ontology — Architecture Guide

A practitioner's comparison of how 10 platforms approach giving AI systems
business context: Palantir Foundry Ontology, Databricks Genie Ontology,
Stardog, Neo4j, Glean Context Graph, Tableau Semantics, Snowflake Semantic
Views, AWS Context, and Microsoft Foundry IQ.

## Read the full comparison

[Genie Ontology vs Palantir Ontology — What's the Difference?](https://saurabhanilagrawal.medium.com/genie-ontology-vs-palantir-ontology-whats-the-difference-e64f06746ad2)

Updated November 26, 2026. Product details checked against each vendor's
public documentation.

## About

Written by Saurabh Agrawal, a Delivery Solutions Architect with 15+ years
in data platforms.

A curated list of platforms and official documentation for giving AI agents business context: definitions, metrics, relationships and rules. Links point to vendor docs where possible. Pull requests welcome.

_Last reviewed: November 2026. Check vendor release notes for current status._

## Platforms

### Context layers and ontologies
- **Databricks Genie Ontology** — modeled Unity Catalog semantics plus context learned from existing assets; GA since Nov 9, 2026. [Docs](https://docs.databricks.com/aws/en/genie/genie-ontology/)
- **Palantir Ontology** — explicitly modeled objects, properties, links and actions for operational workflows. [Docs](https://www.palantir.com/docs/foundry/ontology/overview/)
- **Microsoft Fabric IQ** — business entities and ontology built around OneLake and Power BI semantic models. [Docs](https://learn.microsoft.com/fabric/iq/overview)
- **Google Knowledge Catalog** — metadata, glossary, lineage and verified queries exposed to agents. [Docs](https://docs.cloud.google.com/knowledge-catalog/docs)

### Semantic layers
- **Snowflake Semantic Views** — logical tables, relationships, dimensions and metrics for Cortex. [Docs](https://docs.snowflake.com/en/user-guide/views-semantic/overview)
- **Databricks metric views** — governed metrics in Unity Catalog, shared by dashboards and agents. [Docs](https://docs.databricks.com/aws/en/uc-semantics/metric-views/)
- **Tableau Semantics** — semantic models and metrics in Salesforce Data 360. [Product page](https://www.tableau.com/products/tableau-semantics)

### Retrieval and knowledge
- **Microsoft Foundry IQ** — reusable knowledge bases with agentic retrieval. [Docs](https://learn.microsoft.com/en-us/azure/foundry/agents/concepts/what-is-foundry-iq)
- **Glean** — enterprise search and context graph across workplace apps. [Blog](https://www.glean.com/blog/how-do-you-build-a-context-graph)

### Graph databases and knowledge graphs
- **Neo4j** — property graph database queried with Cypher. [Docs](https://neo4j.com/docs/getting-started/graph-database/)
- **Stardog** — RDF/OWL knowledge graph with SPARQL and virtual graphs. [Docs](https://docs.stardog.com/virtual-graphs/)

### Connecting AI tools
- **Genie One MCP** — expose Databricks business context to external AI agents. [Docs](https://docs.databricks.com/aws/en/agents/mcp-tools/genie-mcp)

## Comparisons and guides
- [Genie Ontology vs Palantir Ontology: what's the difference?](https://saurabhanilagrawal.medium.com/genie-ontology-vs-palantir-ontology-whats-the-difference-e64f06746ad2) — docs-linked comparison with notes on the platforms above (updated Nov 26, 2026). _Maintainer's own guide._

## Contributing
Add a platform with a one-line description and a link to official docs. Mark preview features as preview.
