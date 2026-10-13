---
{"dg-publish":true,"permalink":"/Helden-Dashboard/","tags":["gardenEntry"],"dg-note-properties":{}}
---


# 📜 Chronik von "Hinter dem Schleier"

Willkommen im Kampagnen-Kompendium unserer DSA-Gruppe. Hier findet ihr alles, was ihr über eure Abenteuer in Aranien nachlesen könnt.

## Lehrmeister

```base
properties:
  file.name:
    displayName: Name
  note.kurzbeschreibung:
    displayName: Beschreibung
views:
  - type: table
    name: Lehrmeister
    filters:
      and:
        - file.hasTag("Lehrmeister")
        - file.hasProperty("dg-publish")
    order:
      - file.name
      - Ort
      - kurzbeschreibung
    sort:
      - property: file.name
        direction: DESC
      - property: kurzbeschreibung
        direction: ASC

```

## Orte

```base
properties:
  file.name:
    displayName: Name
  note.kurzbeschreibung:
    displayName: Beschreibung
views:
  - type: list
    name: Orte
    filters:
      and:
        - file.hasTag("Stadt")
        - file.hasProperty("dg-publish")
    order:
      - file.name
    sort: []

```

## Divers

```base
views:
  - type: list
    name: Divers
    filters:
      and:
        - file.hasProperty("dg-publish")
        - '!file.hasProperty("dg-home")'
        - '!file.hasTag("NPC")'
        - '!file.hasTag("Stadt")'
    order:
      - file.name

```