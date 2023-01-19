# OMS-API

## Modules
- Job
- Order
- Product
- Shipment
- Stock
- User

### Job [WIP]
---

### Order [WIP]
---

### Product [WIP]
---

### Shipment [WIP]
---

### Stock [WIP]

*Perform operations related to product(s) stock.*

The main purpose of this module is to provide information regarding stock of product(s). The transformation rules for the module are defined in mappings/stock, and the typings for stock are available in types/stock.

> **Warning:**
For fetching the stock we are using *`checkInventory`* api that has a constraint of processing maximum 100 records at once, thus make sure to not exceed the viewSize by 100 and if needed, use pagination for the same.

**Use Cases:**
- fetch total stock for product(s) on all facilities
- fetch stock for product(s) on single/multiple/0(zero) facilities

**Methods:**
- fetchProductsStock

  Finds the total stock of product(s) based on productId(s) on all the facilities. This method makes use of `checkInventory` api.

  **IN:**
  <table>
    <tr><th>Property</th><th>Type</th><th>Description</th><th>Default Value</th></tr>
    <tr><td>productId*</td><td>string[] / string</td><td>Array of productIds or a single productId for which the stock needs to be fetched</td><td>-</td></tr>
  </table>

  **OUT:**

  In case of success it returns a resolved promise as `Stock[]` and in case of error/failure, rejected promise is returned as `Response` having a code, message, and serverResponse.

- fetchProductsStockAtFacility

  Fetches the product(s) stock by facility. This method makes use of `checkInventory` api.

  **IN:**
  <table>
    <tr><th>Property</th><th>Type</th><th>Description</th><th>Default Value</th></tr>
    <tr><td>productId*</td><td>string[] / string</td><td>Array of productIds or a single productId for which the stock needs to be fetched</td><td>-</td></tr>
    <tr><td>facilityId</td><td>string[] / string</td><td>Array of facilityIds or a single facilityId on which the stock needs to be fetched. If no facilityId is passed then stock for the products are fetched by facility.</td><td>-</td></tr>
  </table>

  **OUT:**

  In case of success it returns a resolved promise as `Stock[]` and in case of error/failure, rejected promise is returned as `Response` having a code, message, and serverResponse.

---
### User [WIP]
---