---
name: analyze-business-plan
description: Analyze startup and company business plans, pitch decks, financing decks, and BP PDFs from a venture-capital perspective. Use when Codex needs to verify the exact BP version, identify internal contradictions, investigate founders and legal entities, validate market size or technology leadership, compare competitors separately across each target market, reconstruct competitor timelines, model unit economics or TCO for device sales, leasing, per-use, or RaaS, stress-test commercialization forecasts, assess financing, create a Markdown investment report, or generate company-specific due-diligence questions.
---

# Analyze Business Plan

Turn a BP into an evidence-aware investment report. Separate company disclosure, external fact, analytical inference, contradiction, and unresolved diligence.

## Core Workflow

1. **Lock the source version before analysis.**
   - Record filename, page count, cover date, PDF creation/modification date, and visible version label.
   - If multiple decks or prior reports exist, compare their dates and page counts. Use the newest user-designated source as primary; treat older versions as historical evidence.
   - Flag changed market figures, shipment targets, financing terms, product status, and management claims. Never merge versions silently.

2. **Read the complete source.**
   - For PDF or slide-like documents, use the PDF skill.
   - Extract text from every page. Visually review every page at low resolution, then inspect material charts, tables, product images, team slides, roadmaps, customer logos, financials, and financing pages at readable resolution.
   - Record page references for material claims.
   - Distinguish historical actuals, current status, targets, forecasts, aspirations, and illustrative examples.

3. **Build a claim and contradiction inventory.**
   Capture identity, product, customer, market, technology, competition, traction, team, business model, financing, and use of funds. Mark each claim as:
   - `BP disclosed`
   - `externally verified`
   - `partially supported / qualified`
   - `contradicted`
   - `analytical inference`
   - `not disclosed / requires diligence`

   Run an internal consistency scan before browsing:
   - same metric on different pages;
   - text versus chart;
   - currency conversions and units;
   - current revenue versus theoretical TAM;
   - pilot, order, shipment, revenue, collection, and profit;
   - product status versus roadmap;
   - shipment targets versus stated capacity and channel;
   - financing amount versus use-of-funds arithmetic.

4. **Research consequential claims with a source ladder.**
   Browse for current market size, competitors, product releases, shipments, financing, regulation, technical leadership, team credentials, and legal entities.
   - Prefer primary sources: official company product pages, regulatory filings, prospectuses, standards, patents, peer-reviewed papers, official university/employer pages, official competition results, government registries, and official datasets.
   - Use broker reports and market research as secondary context; identify when they merely re-cite another provider.
   - Cite external facts near the claim with clickable links when the format supports them.
   - For market size, use at least two external sources when available and explain scope differences.
   - For exclusivity or technology leadership, check at least one primary paper/filing and two relevant competitor official sources when available.
   - For founder credentials, verify material degrees, positions, awards, competition results, and prior companies through primary institutional sources when available.
   - For legal identity, distinguish company names, jurisdictions, registration dates, shareholders, related entities, and similarly named entities. Do not merge entities based only on a shared person or brand.
   - Record research cutoff date and say explicitly when no confirming evidence is found.

5. **Reconstruct the competitive timeline.**
   - First split competition by each market, customer segment, or use case the company actually enters. Do not mix residential, commercial, industrial, healthcare, or other materially different markets in one undifferentiated ranking.
   - For every segment, identify direct competitors, adjacent entrants, substitutes or legacy workflows, and financial comparables separately.
   - State the company product, customer buying criteria, and relative position for each segment. Compare only metrics that matter to that buyer.
   - Separate direct, adjacent, substitute, and financial comparables.
   - Identify the narrowest direct competitor set for each superiority claim, not only broad category leaders.
   - Record representative product, launch date, navigation/technology route, price, shipment/deployment scale, channel, and service model where available.
   - Use the timeline to test “first,” “only,” “leading,” and claimed market-window narratives.
   - Compare company targets with how long credible peers took to reach similar shipment, revenue, certification, channel, or service milestones. State differences in starting resources.

6. **Analyze rather than restate.**
   - Recompute or challenge market assumptions and identify the most sensitive variables.
   - Separate theoretical TAM, observed market revenue, SAM, and attainable SOM.
   - Test whether product differentiation creates measurable customer value.
   - Separate academic novelty from production readiness.
   - Evaluate traction through paid deployment, repeat orders, collections, revenue quality, reliability, and unit economics.
   - Rebuild unit economics separately for each material business model: device sale, lease, per-task or per-unit pricing, RaaS, software, and component sales as applicable.
   - Distinguish energy or other marginal input cost from full lifecycle cost. Include ASP/service price, BOM, manufacturing, channel, deployment, operator labor, consumables, batteries, maintenance, warranty, field support, depreciation, utilization, downtime, financing, collection, and bad debt.
   - When actual inputs are missing, do not invent company performance. Provide a transparent low/base/high sensitivity model, label every analyst assumption, show formulas and units, and identify the variables that reverse customer ROI or company contribution margin.
   - Separate customer savings/payback from company gross margin, contribution margin, cash payback, and corporate profitability.
   - Stress-test forecast jumps against capacity, certification, channel, working capital, support network, and peer ramp history.
   - Use strong wording only when evidence warrants it. Prefer “inconsistent,” “unsupported,” or “not comparable” over an exact overstatement multiple when definitions differ.

7. **Draft the report answer-first.**
   Default to Markdown. Use `assets/bp-report-template.md`, adapting it to available evidence.
   - Keep the company summary to one or two sentences.
   - Put market and competition second.
   - Include material internal contradictions, market-specific competition, team/entity verification, technology validation, commercialization stress test, unit economics, financing, conditional decision, and specific diligence questions.
   - Keep a clean reader-facing report; do not expose search logs or private temporary paths.

8. **Generate decision-reversing diligence questions.**
   Read `references/due-diligence-questions.md` when a diligence section is requested. Derive questions from contradictions, missing denominators, unsupported superiority claims, identity/IP uncertainty, forecast jumps, and operating risks. Request evidence and explain the tested decision. Do not output a generic checklist.

9. **Validate the output.**
   - Confirm the report names the exact BP version used.
   - Check every important number for unit, period, geography, definition, and source.
   - Ensure external validation does not mix incompatible scopes.
   - Check that founder, award, customer, financing, and legal-entity claims are not attributed across different people or entities.
   - Confirm external citations are clickable and directly support nearby claims.
   - Label subjective judgments and calibrated uncertainty.
   - Remove unsupported superlatives, duplicated sections, and conclusions based on superseded deck versions.

## Required Reference Routing

- Read `references/analysis-framework.md` for market, competition, technology, commercialization, team, entity, or financing validation.
- Read `references/due-diligence-questions.md` when producing diligence questions.
- Use `assets/bp-report-template.md` for the default report structure.

## Default Report Rules

- Do not place KPI cards before the one- or two-sentence summary.
- Do not treat customer logos as paid customers, cooperation as revenue, pilots as deployments, framework agreements as orders, shipments as collections, papers as production performance, or roadmaps as released products.
- Treat product photos as optional; add them only when they improve understanding.
- Prefer compact tables for comparisons and Mermaid only for a useful system or business flow.
- Structure competition by target market or use case whenever the company spans materially different customer segments. Do not compare products with different buyers and jobs as though they were interchangeable.
- Include a dedicated unit-economics section when the BP makes cost, ROI, gross-margin, payback, productivity, RaaS, leasing, or scale claims. Clearly separate disclosed data, analyst assumptions, and calculated outputs.
- Never present electricity, fuel, cloud, or another single marginal input as full operating cost. Never compare a partial robot cost with an all-in labor or outsourced-service price without reconciliation.
- Do not invent scores, rankings, or risk values unless requested. If used, label method and analyst judgment.
- Keep the investment conclusion conditional when financial, customer, reliability, ownership, or identity evidence is missing.
- If another report analyzed a different BP version, compare process quality separately from factual conclusions.

## Evidence Language

Use explicit labels:

- **公司披露：** “BP第X页称……”
- **外部验证：** “官方文件/论文/产品页显示……”
- **有限支持：** “方向成立，但适用范围仅为……”
- **矛盾或反证：** “该主张与……不一致/被……反驳。”
- **分析推断：** “若假设……，这意味着……”
- **未解决：** “现有材料不足以证明……”

## Source Handling and Degraded Mode

- Read text files as UTF-8 and preserve Chinese filenames.
- Temporary PDF renders are allowed under the workspace temp directory unless prohibited; keep them out of the visible report.
- If the source cannot be parsed or rendered, report the concrete blocker and do not invent company-specific claims.
- When only partial pages are readable, label the report partial and identify unread pages.
- If multiple versions conflict and the intended primary version cannot be determined, state the conflict and avoid version-sensitive conclusions.

## Deliverables

Return one primary artifact and a concise handoff:

- `report.md` for standard BP analysis;
- another surface only when explicitly requested;
- supporting source notes only when needed.
