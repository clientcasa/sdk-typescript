# ChangeTodoOccurrenceRequestBody


## Supported Types

### `operations.CreateSeries`

```typescript
const value: operations.CreateSeries = {
  intent: "create-series",
  commandId: "5dc0df39-f2b0-44fe-9fad-7133acbe5818",
  seriesId: "09182150-fb8c-48a4-a1ab-2149a5283fc6",
  businessId: "4d97f589-ee8e-41d1-8660-30960bcdca0b",
  title: "<value>",
  rrule: "<value>",
  day: "<value>",
  fields: {},
};
```

### `operations.Occurrence`

```typescript
const value: operations.Occurrence = {
  intent: "occurrence",
  commandId: "17d94d11-461e-46da-90c3-210da736b88a",
  seriesId: "528b3a49-5134-4cab-b79a-0d49212793e5",
  nominalKey: "<value>",
  expectedRevision: 503043,
  todoId: "3298f793-8e32-4103-91cd-ae98c199fc89",
};
```

### `operations.EditSeries`

```typescript
const value: operations.EditSeries = {
  intent: "edit-series",
  commandId: "728f0b47-f39c-4086-94a8-6003f1bd811f",
  seriesId: "886648fc-826d-46be-8eb1-6e37e65b015b",
  newSeriesId: "3857c0d3-ecd5-4770-91ba-594a3993c8e3",
  nominalKey: "<value>",
  expectedUpdatedAt: "<value>",
  expectedLineageVersion: "<value>",
  scope: "future",
  reviewed: true,
  fields: {},
};
```

