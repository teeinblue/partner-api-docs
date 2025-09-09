---
description: Teeinblue Print Partner API
---

# Overview

## Introduction

The **Teeinblue Print Partner API** enables **print partners** to seamlessly integrate their systems with the **Teeinblue platform**.\
Through this API, partners can synchronize **product catalogs**, **receive and fulfill orders**, and **send shipment tracking updates** back to Teeinblue.

## Integration Workflow

The typical integration flow looks like this:

1. **Catalog Synchronization**
   * Teeinblue retrieves your product data using `GET /catalogs` and `GET /catalogs/{id}`.
   * This information (mockups, print areas, variants, prices,...) is shown to sellers on Teeinblue.
2. **Order Submission**
   * When a seller places an order, Teeinblue calls `POST /orders` on your API with all order details (variant, shipping address, designs,...).
   * The order payload includes a **`shipment_notification_url`** — You must store this URL for each order.
3. **Shipment Notification**
   * Once the order is shipped, you send a **`POST`** request to the `shipment_notification_url` provided by Teeinblue.
   * Include tracking details (tracking number, tracking URL, carrier).
   * Teeinblue automatically updates the seller.
