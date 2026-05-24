<!-- Start SDK Example Usage [usage] -->
```typescript
import { ClientCasa } from "@clientcasa/sdk";

const clientCasa = new ClientCasa();

async function run() {
  const result = await clientCasa.clients.list({
    apiKey: process.env["CLIENTCASA_API_KEY"] ?? "",
  }, {});

  for await (const page of result) {
    console.log(page);
  }
}

run();

```
<!-- End SDK Example Usage [usage] -->