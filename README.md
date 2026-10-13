# Azure Cost Visibility — learning project

An early Azure learning project by Abdullah Alhammoud, a business information systems student. The aim is to understand cloud costs and show month-to-date actual costs grouped by resource group.

## Available work

- `cost-visibility.workbook`: export of the existing Azure Monitor workbook. The subscription ID has been replaced with a placeholder.
- `cost-query-request.json`: the Cost Management request extracted from that workbook, formatted for readability.
- Existing Azure resources inspected on 13 October 2026: a project resource group, storage account, Key Vault and the workbook. Private account identifiers and credentials are excluded from this repository.

## Current status and limitations

This is work in progress, not a completed or production-ready solution. At export time, the workbook displayed `obj needs to be an object` and a missing Log Analytics workspace warning. The first item contains an endpoint definition encoded inside its query; the second item is an empty Log Analytics query. Those issues are retained transparently in the exported sample rather than hidden.

The request uses ActualCost, MonthToDate, sum of Cost and grouping by ResourceGroup. No claim is made that this exported workbook currently runs successfully. The JSON files were parsed locally and checked for private Azure GUIDs. No live Azure execution or deployment was performed during preparation of this portfolio.

This repository contains the workbook export and its extracted API request only. Python Function source and automated budget alerts are not included in this export. The full end-to-end integration has not been verified.

## Learning goals

Understand the Azure Cost Management API, correct the workbook configuration, and validate the result against Azure Cost Analysis. Any future automation should use secure authentication and keep credentials outside version control.
