# TimelineItemCreateAnchorType

How the item is timed. 'none' floats (the cascade solves its time from order + duration). 'fixed' pins the item's START to requestedStartTime (HH:MM). 'fixed-end' pins the item's END to requestedStartTime — a hard stop / curfew / 'must be done by'; the schedule back-solves the items before it to fit (pin = end − duration). 'custom-event' pins to a named Key Moment via anchorKey. 'sunset'/'sunrise' pin to the venue's golden hour. 'ceremony'/'event-start' are legacy named anchors.

## Example Usage

```typescript
import { TimelineItemCreateAnchorType } from "@clientcasa/sdk/models";

let value: TimelineItemCreateAnchorType = "custom-event";
```

## Values

```typescript
"none" | "fixed" | "fixed-end" | "ceremony" | "event-start" | "sunset" | "sunrise" | "custom-event"
```