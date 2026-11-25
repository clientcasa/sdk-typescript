# ListTodosResponse

## Example Usage

```typescript
import { ListTodosResponse } from "@clientcasa/sdk/models/operations";

let value: ListTodosResponse = {
  result: {
    data: [
      {
        id: "550e8400-e29b-41d4-a716-446655440000",
        persisted: true,
        mutationPath: "<value>",
        businessId: "550e8400-e29b-41d4-a716-446655440000",
        projectId: "550e8400-e29b-41d4-a716-446655440000",
        clientId: "550e8400-e29b-41d4-a716-446655440000",
        title: "<value>",
        details: "<value>",
        kind: "milestone",
        status: "done",
        revision: 999282,
        doRule: {
          kind: "fixed",
          day: "<value>",
        },
        deadlineRule: {
          kind: "event-relative",
          anchor: {
            kind: "bound",
            eventDayId: "4d5aff57-f4fb-4395-b1d4-54258eb35620",
          },
          offsetDays: 204773,
        },
        localStart: "<value>",
        durationMinutes: 8586.28,
        scheduleZone: null,
        location: "<value>",
        assigneeId: "550e8400-e29b-41d4-a716-446655440000",
        seriesId: "550e8400-e29b-41d4-a716-446655440000",
        nominalOccurrenceKey: "<value>",
        doDate: new Date("2024-02-19"),
        deadlineDay: new Date("2026-02-21"),
        completedAt: new Date("2026-09-30T02:34:26.016Z"),
        completedOn: new Date("2024-07-18"),
        completionPrecision: "instant",
        createdAt: new Date("2025-05-23T12:25:27.725Z"),
        updatedAt: new Date("2024-01-02T12:08:38.241Z"),
      },
    ],
    items: [
      {
        "key": "<value>",
      },
      {
        "key": "<value>",
        "key1": "<value>",
        "key2": "<value>",
      },
    ],
    complete: false,
    pagination: {
      nextCursor: "<value>",
    },
    coverage: {
      after: "<value>",
      next: "<value>",
      stopped: false,
    },
    sources: {
      "key": "<value>",
      "key1": "<value>",
    },
    evaluatedAt: new Date("2024-04-10T18:46:06.922Z"),
    revisions: {
      "key": 3545.96,
      "key1": 6124.64,
      "key2": 2358.81,
    },
    nextAction: {
      "key": "<value>",
    },
    notice: "<value>",
  },
};
```

## Fields

| Field                                        | Type                                         | Required                                     | Description                                  |
| -------------------------------------------- | -------------------------------------------- | -------------------------------------------- | -------------------------------------------- |
| `result`                                     | [models.TodoList](../../models/todo-list.md) | :heavy_check_mark:                           | N/A                                          |