# AquaLens

AquaLens is a citizen-science prototype for **Track 1: Citizen Science UX** of the OneAquaHealth IEEE Global Hackathon.

It helps people with little or no environmental-science background record stream observations through a simple guided workflow. The goal is to make stream assessment easier to understand, more consistent, and easier to repeat.

## Problem

Citizen-science stream assessments can be difficult for new participants because ecological terminology and field-observation steps may be unfamiliar. This can reduce participation and lead to incomplete observations.

## Solution

AquaLens guides the user through four simple steps:

1. **Learn a clue** — a short visual exercise introduces an observable sign such as bank erosion.
2. **Observe the stream** — record water clarity, bank cover, litter, flow condition, and approximate flow speed.
3. **Add evidence** — attach a stream photo. The browser performs simple checks such as image resolution, brightness, and rough green-area cues.
4. **Review and save** — review the observation, see an evidence-completeness score, save it locally, and export the record as JSON.

The completeness score measures how well the observation was documented. It is **not** a water-quality, pollution, safety, or scientific-confidence score.

## Track alignment

**Track 1: Citizen Science UX** — AquaLens focuses on guided workflows, simpler ecological language, better evidence capture, and repeat observations.

The prototype supports the OneAquaHealth goal of improving citizen participation in freshwater monitoring while keeping human observation central.

## How it works

- Single-page HTML, CSS, and JavaScript application
- No backend or account required
- Current assessment stored in browser `localStorage`
- Uploaded photos processed locally using the browser Canvas API
- Structured JSON export for saved observations
- Responsive layout for desktop and mobile

The current image checks are simple browser-based heuristics, not a trained machine-learning model.

## Run the prototype

Open `index.html` directly in a browser.

Alternatively, run a local server:

```bash
python -m http.server 8000
```

Then open `http://localhost:8000`.

## Current limitations and future work

This is a hackathon prototype and does not diagnose whether a stream is healthy, polluted, or safe.

Future versions could add properly trained and validated ML assistance for erosion recognition, vegetation-cover estimation, visible litter detection, and repeat-visit change detection. Other extensions could include maps, GPS-based sites, offline collection, multilingual support, weather or sensor context, and researcher review tools.

## Demo data

`Willow Beck` and site `WB-014` are illustrative demo data used inside the prototype and are not presented as a real OneAquaHealth monitoring site.
