---
title: "Delete Product"
sidebar_label: "Delete Product"
---

# Delete Product

## Overview
Deletes a product from the system (soft delete).

## Request Payload

| Field | Type   | Required | Description                |
|-------|--------|----------|----------------------------|
| id    | string | Yes      | The ID of the product      |

## Response Payload

| Field | Type    | Description               |
|-------|---------|---------------------------|
| id    | string  | The ID of the product     |

## Business Rules

1.  The product is soft-deleted (the `deleted` flag is set to true).

## Validation Rules

- None

## Workflow

1.  User requests to delete a product by ID.
2.  The system updates the `deleted` flag to true.
3.  The system returns a success message.

## Error Scenarios

| Scenario         | HTTP Status | Error Code |
|------------------|-------------|------------|
| Product not found| 404         | NOT_FOUND     |
