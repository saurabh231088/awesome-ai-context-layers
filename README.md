# Awesome AI Context Layers

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
- [Genie Ontology vs Palantir Ontology: what's the difference?](https://medium.com/@saurabhanilagrawal/genie-ontology-vs-palantir-ontology-whats-the-difference-e64f06746ad2) — docs-linked comparison with notes on the platforms above (updated Nov 23, 2026). _Maintainer's own guide._

- # Databricks Genie Ontology — 30 How-To Quick Reference

[Full guide](https://medium.com/@saurabhanilagrawal/genie-ontology-vs-palantir-ontology-whats-the-difference-e64f06746ad2) | Updated Nov 25, 2026

## MCP & integrations https://medium.com/@saurabhanilagrawal/genie-ontology-vs-palantir-ontology-whats-the-difference-e64f06746ad2
- **Expose to ChatGPT/Claude via MCP** → EXECUTE on system.ai.genie_one_mcp + ai-gateway scope
- **Connect MCP to Genie Agents** → Sources tab → Add → MCP Services (Beta)
- **MCP permission enforcement** → per-user auth; write tools need approval

## Domains & governance https://medium.com/@saurabhanilagrawal/genie-ontology-vs-palantir-ontology-whats-the-difference-e64f06746ad2
- **Structure domains** → one top-level per business area, up to 5 levels
- **Permission boundaries** → UC grants per team; external knowledge sources visible to all (Beta)
- **Create Pages** → Discover → Pages → Create; attach to one domain
- **Bulk import Pages** → Genie Code "Bulk import" starter; creates drafts
- **Stewardship workflow** → consumers draft, managers publish, curators certify

## Metrics & validation https://medium.com/@saurabhanilagrawal/genie-ontology-vs-palantir-ontology-whats-the-difference-e64f06746ad2
- **Validate Genie uses your metrics** → check snippet source under each response
- **Test against ground truth** → benchmark SQL in Chat mode; Good = match within 4 sig digits
- **Evaluate inferred context** → inspect authority scores and source citations
- **How Genie infers metrics** → extracts snippets from queries, dashboards, metric views
- **Help Genie discover metrics** → define metric views, organize domains, write Pages
- **Override inferred metrics** → define as metric view or Page; modeled wins
- **Inferred as starting point** → treat snippets as drafts, formalize as modeled
- **Compare inferred vs certified** → view snippets alongside metric views
- **Correct wrong inferences** → fix source asset or publish authoritative metric view
- **Resolve team conflicts** → separate domains, certify the winner
- **Configure Agent metrics** → add up to 50 tables/views/metric views
- **Define semantic objects** → CREATE VIEW WITH METRICS using MEASURE()

## Metric views & dashboards https://medium.com/@saurabhanilagrawal/genie-ontology-vs-palantir-ontology-whats-the-difference-e64f06746ad2
- **Metrics for Agents + dashboards** → one metric view, shared everywhere
- **Metric views in dashboards** → same view in both; MEASURE() auto-applied
- **Agent as dashboard source of truth** → back both with certified metric views
- **Lineage tracking** → UC lineage + Genie provenance citations
- **Temporal patterns** → fiscal calendars and time-window rules in metric views

## Migration & discovery https://medium.com/@saurabhanilagrawal/genie-ontology-vs-palantir-ontology-whats-the-difference-e64f06746ad2
- **Snowflake → metric views** → logical tables → source; dimensions → fields; metrics → measures
- **Snowflake layering** → metric view composability with MEASURE()
- **Genie One search** → Discover page + chat; domain filter includes subdomains
- **External knowledge sources** → Beta for BI models; Preview for volumes
- **Data product strategy** → domain-aligned certified metric views + dedicated Agents

## Contributing
Add a platform with a one-line description and a link to official docs. Mark preview features as preview.
