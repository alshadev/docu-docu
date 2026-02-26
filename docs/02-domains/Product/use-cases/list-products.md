---
title: "List Products"
sidebar_label: "List Products"
---

# List Products

## Overview
Retrieves a paginated list of products.

## Request Payload

| Field    | Type   | Required | Description                                   |
|----------|--------|----------|-----------------------------------------------|
| page     | number | No       | The page number to retrieve (default: 1)      |
| pageSize | number | No       | The number of products per page (default: 10) |

## Response Payload

| Field      | Type     | Description                                  |
|------------|----------|----------------------------------------------|
| items      | array    | An array of products (code and name)         |
| totalItems | number   | The total number of products in the system    |
| totalPages | number   | The total number of pages                      |
| page       | number   | The current page number                        |
| pageSize   | number   | The number of products per page              |

## Business Rules

1.  Only return products that are not soft-deleted.

## Validation Rules

1.  `page` must be a positive integer.
2.  `pageSize` must be a positive integer.

## Workflow

1.  User requests a list of products with pagination parameters.
2.  The system retrieves the products from the database, applying pagination.
3.  The system returns a paginated list of products containing only the `code` and `name`.

## Error Scenarios

| Scenario         | HTTP Status | Error Code |
|------------------|-------------|------------|
| Invalid input    | 400         | INVALID_INPUT |
