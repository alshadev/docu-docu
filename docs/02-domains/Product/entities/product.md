---
title: "Product"
sidebar_label: "Product"
---

# Product

## Overview
Represents a product in the system.

## Fields

| Field       | Type    | Required | Description                                 |
|-------------|---------|----------|---------------------------------------------|
| code        | string  | Yes      | Unique product code (max length 20)         |
| name        | string  | Yes      | Product name (max length 50)                |
| description | string  | No       | Product description                           |
| deleted     | boolean | Yes      | Flag indicating if the product is deleted (soft delete) |

## Relationships
- None

## Invariants
- `code` must be unique.
