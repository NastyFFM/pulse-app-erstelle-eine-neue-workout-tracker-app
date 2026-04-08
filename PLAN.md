# Plan: Workout Tracker

created: 2026-04-08T17:45:00Z
status: active
app_id: erstelle-eine-neue-workout-tracker-app
app_dir: /Users/chris.pohl/Documents/GitHub/pulse-app-erstelle-eine-neue-workout-tracker-app
standalone: true

## Ziel
Eine vollständige Workout-Tracker App für PulseOS. Der User kann Trainingseinheiten loggen, Übungen mit Sets/Reps/Gewicht erfassen, den Verlauf einsehen und Fortschritte verfolgen.

## Stack
- PulseOS Vanilla HTML/CSS/JS (Single-File App)
- PulseOS SDK (saveState, loadState, onInput, emit, onDataChanged)
- CSS-Variablen (var(--bg), var(--text), var(--teal), etc.)
- Chart.js via CDN (Fortschritts-Graphen)

## Features
- Workout starten (Datum, Name der Einheit)
- Übungen hinzufügen (Name, Muskelgruppe, Sets × Reps × Gewicht)
- Workout-Historie anzeigen (Liste der vergangenen Einheiten)
- Statistiken: Gesamtvolumen, Trainingstage, Lieblingsübungen
- Muskelgruppen-Tags (Brust, Rücken, Beine, Schultern, Arme, Core)
- Quick-Add: häufige Übungen als Vorlagen

## Aufgaben

### Phase 1 — Grundgerüst
- [ ] TASK-001: PLAN.md, PROGRESS.md, DECISIONS.md anlegen
      assigned_to: orchestrator
      depends_on: -
      files: [PLAN.md, PROGRESS.md, DECISIONS.md]
      complexity: low

### Phase 2 — Implementierung
- [ ] TASK-002: manifest.json aktualisieren (Name, Icon, Color, Ports)
      assigned_to: code-generator
      depends_on: TASK-001
      files: [manifest.json]
      complexity: low

- [ ] TASK-003: data/state.json mit Beispieldaten anlegen
      assigned_to: code-generator
      depends_on: TASK-001
      files: [data/state.json]
      complexity: low

- [ ] TASK-004: index.html — vollständige Workout-Tracker App
      assigned_to: code-generator
      depends_on: [TASK-002, TASK-003]
      files: [index.html]
      complexity: high

### Phase 3 — Qualität
- [ ] TASK-005: Code Review
      assigned_to: code-reviewer
      depends_on: TASK-004
      files: []
      complexity: low

### Phase 4 — Abschluss
- [ ] TASK-006: Git commit + GitHub Deploy
      assigned_to: orchestrator
      depends_on: TASK-005
      files: []
      complexity: low

## Offene Fragen an User
Keine offenen Fragen — Plan ist bereit.
