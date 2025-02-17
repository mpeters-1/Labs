```mermaid
erDiagram
    PRODUCT {
}
    CUSTOMER ||--o{ SALE : places
    CUSTOMER {
       string name
       int librarycardnumber
    }
}
    SALE ||--|{ PRODUCT : contains
    SALE {
        string bookTitle
        string ISBN
    }
    }
    INVENTORY {Media Collection
    }