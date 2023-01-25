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

When fetching the stock, the module does not handle the case of product(s) those were not found on server. If all the product(s) for which inventory needs to be fetched is/are not found on server then module simply returns an error response and when some of the products are not found when fetching stock for multiple products, then only those products were returned whose stock is found on server and other products are not returned in response.

**Use Cases:**
- fetch total stock for product(s) on all facilities
- fetch stock for product(s) on single/multiple/0(zero) facilities

**Methods:**
- fetchProductsStock

  Finds the sum of product(s) stock based on productId(s) on all the facilities. This method makes use of `checkInventory` api.

  **IN:**
  <table>
    <tr><th>Property</th><th>Type</th><th>Description</th><th>Default Value</th></tr>
    <tr><td>productId*</td><td>string[] / string</td><td>Array of productIds or a single productId for which the stock needs to be fetched</td><td>-</td></tr>
  </table>

  **OUT:**

  In case of success it returns a resolved promise as `Stock[]` having a productId for which the stock is fetched, and sum of product stock(availableToPromiseTotal) on all the facilities and in case of error/failure, rejected promise is returned as `Response` having a code, message, and serverResponse.

  **Sample Response:**

  - Success
    ```ts
    [{
      productId: "00001",
      availableToPromiseTotal: 4
    },{
      productId: "00002",
      availableToPromiseTotal: 5
    }]
    ```

  - Error
    ```ts
    {
      code: 'error',
      message: 'Unable to find the stock for product(s)',
      serverResponse: err
    }
    ```

- fetchProductsStockByFacility

  Fetches the product(s) stock by facility. This method can be useful when we want to fetch the stock of product(s) on single/multiple/all facilities. When want to fetch the stock for all facilities don't pass value for facilityId(s) in the method call. This method makes use of `checkInventory` api.

  **IN:**
  <table>
    <tr><th>Property</th><th>Type</th><th>Description</th><th>Default Value</th></tr>
    <tr><td>productId*</td><td>string[] / string</td><td>Array of productIds or a single productId for which the stock needs to be fetched</td><td>-</td></tr>
    <tr><td>facilityId</td><td>string[] / string</td><td>Array of facilityIds or a single facilityId on which the stock needs to be fetched. If no facilityId is passed then stock for the products are fetched by facility on all facilities.</td><td>-</td></tr>
  </table>

  **OUT:**

  In case of success it returns a resolved promise as `Stock[]` and in case of error/failure, rejected promise is returned as `Response` having a code, message, and serverResponse.

  **Sample Response:**

  - Success
    ```ts
    [{
      productId: "00001",
      availableToPromiseTotal: 4,
      facilityId: 'STORE_1'
    },{
      productId: "00002",
      availableToPromiseTotal: 5,
      facilityId: 'STORE_2'
    }]
    ```

  - Error
    ```ts
    {
      code: 'error',
      message: 'Unable to find the stock for product(s)',
      serverResponse: err
    }
    ```


> **Warning:**
For fetching the stock we are using `checkInventory` api that has a constraint of processing maximum 100 records at once, thus make sure to not exceed the viewSize by 100 and if needed, use pagination for the same.

---
### User [WIP]
---

> **Note:** \* after the parameter names means required.
