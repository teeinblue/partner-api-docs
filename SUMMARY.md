# Table of contents

* [Overview](README.md)
* [API Reference](api-reference/README.md)
  * ```yaml
    props:
      models: false
    type: builtin:openapi
    dependencies:
      spec:
        ref:
          kind: openapi
          spec: openai
    ```
  * ```yaml
    props:
      models: true
    type: builtin:openapi
    dependencies:
      spec:
        ref:
          kind: openapi
          spec: partner-api
    ```
* [Shipment notification](shipment-notification.md)
