# Priority Filter Specification

## Goal

Help managers quickly focus on equipment requests with a selected priority.

## User Need

As a manager, I want to filter the existing equipment request list by its priority so I can review requests with a particular priority without losing sight of the rest of the list.

## Functional Rules

- Provide a priority filter with an `All` choice and one choice for each priority value already used by the application.
- Initially select `All`; all existing requests are visible in their current order.
- Selecting a priority shows only requests whose existing priority value exactly matches the selection.
- Selecting `All` clears the filter and restores every request in its existing order.
- If no requests match a selected priority, show a clear empty state identifying that no requests match the selected priority.
- Filtering changes only which requests are shown. It does not edit, delete, reorder, or replace request data.

## Constraints

- Use the application's existing priority information and request data.
- Work without login, a database, or a network connection.
- Preserve all existing requests and existing behavior outside the priority filter.
- Use the application's existing priority labels verbatim.

## Acceptance Criteria

1. On initial load, the filter shows `All` and every existing request appears in its prior order.
2. For each priority value present in the existing requests, selecting that value displays all and only requests whose priority exactly equals it.
3. After selecting a priority, selecting `All` displays every original request in its prior order.
4. When the selected priority has no matching requests, the request list is replaced by a visible message that no requests match that priority.
5. After filtering and clearing the filter, the underlying set and values of requests are unchanged.
6. The filter renders and functions without login, database access, or network access.

## Out of Scope

- Combining multiple priority values or including higher priorities in a selection.
- Saving a filter choice between sessions.
- Changing request priorities, sorting requests, or editing request data.
- Adding authentication, a database, or server-side filtering.
