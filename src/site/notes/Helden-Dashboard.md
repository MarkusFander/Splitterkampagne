---
{"dg-publish":true,"permalink":"/Helden-Dashboard/","hideInGraph":"true","tags":["gardenEntry"],"dg-note-properties":{}}
---


# 📜 Helden Dashboard

Willkommen im Kampagnen-Kompendium unserer DSA-Gruppe. Hier findet ihr alles, was ihr über eure Abenteuer in Aranien nachlesen könnt.

## NPC

```base
properties:
  file.name:
    displayName: Name
  note.kurzbeschreibung:
    displayName: Beschreibung
views:
  - type: table
    name: NPC
    filters:
      and:
        - file.hasTag("NPC")
        - file.hasProperty("dg-publish")
        - '!file.hasTag("#Lehrmeister")'
    order:
      - file.name
      - Ort
      - kurzbeschreibung
    sort:
      - property: file.name
        direction: ASC
    columnSize:
      note.kurzbeschreibung: 322

```

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
        - file.hasTag("NPC")
        - file.hasProperty("dg-publish")
        - file.hasTag("#Lehrmeister")
    order:
      - file.name
      - Ort
      - kurzbeschreibung
    sort:
      - property: file.name
        direction: ASC
    columnSize:
      note.kurzbeschreibung: 322

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
        - Type == ["Stadt"]
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
        - Type != ["Stadt"]
    order:
      - file.name

```