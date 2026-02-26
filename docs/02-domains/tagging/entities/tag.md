---
title: "Tag"
sidebar_label: "Tag"
---

# Tag

## Fields

| Field | Type | Required | Description |
|---|---|---|---|
| id | UUID | Yes | Unique identifier for the tag |
| name | string | Yes | Name of the tag |

## Relationships

*   Many-to-many relationship with Product.

## Invariants

*   Tag names must be unique.
