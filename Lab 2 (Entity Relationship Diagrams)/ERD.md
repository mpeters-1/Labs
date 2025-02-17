```mermaid
erDiagram
    PRODUCT {Books
}
    CUSTOMER ||--o{ SALE : checks out
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