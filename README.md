# Edge Decision Graph

**Open it:** https://christophergoodale.github.io/edge_decision_graph/

A 3D simulation of how businesses could combine **edge machine learning** (small models running on phones, card terminals, cars, shelf sensors and trucks) with **knowledge graphs** to make fast AI decisions they can explain afterwards.

Five businesses run side by side: credit, sports betting, insurance, retail and logistics. Each one builds its own knowledge graph from the same six node types (entity, event, signal, edge model, rule, decision), so one design serves them all while their data and models stay separate.

> **Concept mockup.** All data is mock and every scenario is made up. It shows a design pattern, not a production system.

## Start with "Walk me through"

The button in the header starts an 8-step guided tour. It plays by itself; press Next or an arrow key to take over, and Space to resume.

1. **One pattern, five businesses:** the three tiers and the shared node types.
2. **A shared vocabulary, not a shared model:** the ontology at the top holds node types only, no data and no model.
3. **A card swipe, decided on the device:** fraud screening in milliseconds without leaving the terminal.
4. **A credit line goes to the approved model:** lending is regulated, so the phone only does pre-checks and Credit's own validated underwriting model decides. The graph stores the reason codes for decline notices.
5. **Same pattern, different words:** sports betting uses the same node types, with safer-gambling scoring and geofence rules on the device.
6. **When the device isn't sure:** a borderline insurance claim goes to that business's own cloud model. Only the score and signals cross the privacy boundary.
7. **Learning stays inside each business:** federated learning per business. Nothing is pooled across businesses and raw data never moves.
8. **Every decision leaves a trail:** click any decision cube to see the event, signals, score, escalation and rule behind it.

## How to read the scene

| Tier | What it shows |
|---|---|
| Ground | Edge devices for each business. A device glows when it senses an event and when its model scores it. |
| Middle | Each business's knowledge graph. Particles travel event → signals → edge model → rule → decision, then back to the device. |
| Above the dashed privacy boundary | Each business's own cloud model (violet cylinder), and the shared ontology at the top centre (node types only). |

Decision colours show the score band: green for low, amber for the middle band, red for high.

Outside the walkthrough the simulation runs on its own. The chips at the top focus one business, the rail along the bottom counts decisions in each stage, and the right-hand panel shows the latest decision, live counts and an event log.

## Keys

`W` walk me through · `←` / `→` step · `Space` pause or resume (auto-advance during the tour) · `Esc` end the tour

Link to a step with `#walkthrough-N`, for example `…/edge_decision_graph/#walkthrough-4`.

## Run it locally

It's a single `index.html` with no build step. three.js r147 and the fonts load from public CDNs.

```bash
python -m http.server 8000
# then open http://localhost:8000
```

Opening `index.html` straight from disk also works in most browsers.
