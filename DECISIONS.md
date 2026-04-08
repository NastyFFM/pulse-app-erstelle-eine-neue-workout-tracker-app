# Decisions: Workout Tracker

## D-001: Single-Page mit Tab-Navigation
date: 2026-04-08
context: App soll in einem PulseOS-Fenster laufen, kompakte Navigation nötig
decision: 3 Tabs — Workout (aktiv), Historie, Stats
alternatives: Separate Seiten verworfen (zu viel URL-Routing in Single-File-App)

## D-002: Daten in state.json (flache Struktur)
date: 2026-04-08
context: PulseOS Data-API nutzt einzelne JSON-Dateien
decision: Alle Daten in data/state.json: { workouts: [], templates: [] }
alternatives: Separate workouts.json + templates.json — zu komplex für einfache App

## D-003: Chart.js via CDN für Statistiken
date: 2026-04-08
context: Vanilla JS, kein npm — Visualisierung nötig für Fortschritts-Charts
decision: Chart.js über cdnjs.cloudflare.com einbinden
alternatives: Eigene Canvas-Charts — zu aufwändig; keine Charts — schlechte UX

## D-004: Muskelgruppen als Tags
date: 2026-04-08
context: User soll schnell nach Muskelgruppe filtern können
decision: Feste Liste: Brust, Rücken, Beine, Schultern, Arme, Core
alternatives: Freie Eingabe — zu unstrukturiert für Statistiken
