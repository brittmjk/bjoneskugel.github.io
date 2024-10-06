
```mermaid
erDiagram
    PRODUCTS {
        int ProductID
        string ProductName
        string Category
        float Price
    }
    
    CUSTOMERS {
        int CustomerID
        string FirstName
        string LastName
        string Email
        string Phone
    }
    
    SALES {
        int SaleID
        date SaleDate
        int Quantity
        float TotalPrice
    }
    
    INVENTORY {
        int InventoryID
        int StockLevel
        int ReorderLevel
        string Location
    }
    
    PRODUCTS ||--|{ SALES : "contains"
    CUSTOMERS ||--o{ SALES : "purchases"
    PRODUCTS ||--|{ INVENTORY : "tracked by"
‘’’
