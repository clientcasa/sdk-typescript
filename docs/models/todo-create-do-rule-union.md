# TodoCreateDoRuleUnion


## Supported Types

### `models.TodoCreateDoRuleNone`

```typescript
const value: models.TodoCreateDoRuleNone = {
  kind: "none",
};
```

### `models.TodoCreateDoRuleFixed`

```typescript
const value: models.TodoCreateDoRuleFixed = {
  kind: "fixed",
  day: "<value>",
};
```

### `models.TodoCreateDoRuleEventRelative`

```typescript
const value: models.TodoCreateDoRuleEventRelative = {
  kind: "event-relative",
  anchor: {
    kind: "bound",
    eventDayId: "1cf81fd4-2414-45bc-975f-c819d864562a",
  },
  offsetDays: 727984,
};
```

