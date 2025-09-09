# Shipment notification

When you (print partner) fulfill an order, you need to notify **Teeinblue** about the shipment details.

After the order is shipped, your system sends a **POST** request to the **Shipment Notification URL** that **Teeinblue provided to you** when the order was created.\
This allows Teeinblue to update the seller with the tracking details automatically.\


***

### Notification Payload Format

The request body should be JSON and include the following fields:

```json
{​
  "id": "text",
  "reference_order_id": "text",
  "order_id": "text",
  "tracking_number": "text",
  "tracking_url": "https://example.com",
  "tracking_company": "text"​
​}
```
