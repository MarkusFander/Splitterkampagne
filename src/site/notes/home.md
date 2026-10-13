---
{"dg-publish":true,"permalink":"/home/","tags":["gardenEntry"],"dg-note-properties":{}}
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
    order:
      - file.name
      - Ort
      - kurzbeschreibung
    sort:
      - property: kurzbeschreibung
        direction: ASC

```
