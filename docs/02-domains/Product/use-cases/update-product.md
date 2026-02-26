---
title: "Update Product"
sidebar_label: "Update Product"
---

# Update Product

## Overview
Updates an existing product in the system.

## Request Payload

| Field       | Type   | Required | Description                     |
|-------------|--------|----------|---------------------------------|
| id          | string | Yes      | The ID of the product to update |
| name        | string | Yes      | Product name (max length 50)    |
| description | string | No       | Product description               |

## Response Payload

| Field | Type    | Description               |
|-------|---------|---------------------------|
| id    | string  | The ID of the product     |

## Business Rules

1.  Only `name` and `description` can be updated.

## Validation Rules

1.  `name` must be between 1 and 50 characters.

## Workflow

1.  User provides the product ID, new `name`, and new `description`.
2.  The system validates the input.
3.  The system updates the product with the given information.
4.  The system returns a success message and redirects the user to the product list page.


## Error Scenarios

| Scenario         | HTTP Status | Error Code |
|------------------|-------------|------------|
| Invalid input    | 400         | INVALID_INPUT |
| Product not found| 404         | NOT_FOUND     |
