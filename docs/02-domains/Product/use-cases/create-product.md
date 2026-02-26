---
title: "Create Product"
sidebar_label: "Create Product"
---

# Create Product

## Overview
Creates a new product in the system.

## Request Payload

| Field       | Type   | Required | Description                                 |
|-------------|--------|----------|---------------------------------------------|
| code        | string | Yes      | Unique product code (max length 20)         |
| name        | string | Yes      | Product name (max length 50)                |
| description | string | No       | Product description                           |

## Response Payload

| Field | Type   | Description        |
|-------|--------|--------------------|
| id    | string | The ID of product |

## Business Rules
1.  The `code` must be unique.

## Validation Rules

1.  `code` must be between 1 and 20 characters.
2.  `name` must be between 1 and 50 characters.

## Workflow

1.  User provides the product `code`, `name`, and `description`.
2.  The system validates the input.
3.  The system creates a new product with the given information.
4.  The system returns a success message and redirects the user to the product list page.

## Error Scenarios

| Scenario                     | HTTP Status | Error Code |
|------------------------------|-------------|------------|
| `code` is not unique         | 400         | CODE_EXISTS |
| Validation fails             | 400         | INVALID_INPUT |
