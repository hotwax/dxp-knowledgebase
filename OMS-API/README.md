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

The main purpose of this module is to provide information regarding stock of product(s). The transformation rules for the module are defined in mappings/stock, and the typings for stock are availble in types/stock.

Also for fetching the stock we are using *`checkInventory`* api that has a constraint of processing maximum 100 records at once, thus make sure to not exceed the viewSize by 100 and if needed, use pagination for the same.

**Use Cases:**
- fetch total stock for product(s) on all facilities
- fetch stock for product(s) on single/multiple/0(zero) facilities

Methods:
- fetchProductsStock
- fetchProductsStockAtFacility

---
### User [WIP]
---