# DeadlineRuleUnion1


## Supported Types

### `operations.DeadlineRuleNone1`

```typescript
const value: operations.DeadlineRuleNone1 = {
  kind: "none",
};
```

### `operations.DeadlineRuleFixed1`

```typescript
const value: operations.DeadlineRuleFixed1 = {
  kind: "fixed",
  day: "<value>",
};
```

### `operations.DeadlineRuleEventRelative1`

```typescript
const value: operations.DeadlineRuleEventRelative1 = {
  kind: "event-relative",
  anchor: {
    kind: "bound",
    eventDayId: "e62cb379-d340-4fad-becb-2d59156b6e73",
  },
  offsetDays: 452406,
};
```

