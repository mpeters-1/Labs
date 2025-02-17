```mermaid
erDiagram
TITLE {
    string book_title The_Catcher_in_the_Rye
    string ISBN PK S9780316769488
    string genre Adult_Fiction
    string author JD_Salinger
    string media_type eBook
    int copy 2
}
PATRON ||--|{ ORDER : checks_out
PATRON {
    string name John_Doe
    string librarycardNumber PK 000123456
}
ORDER ||--|{ TITLE : contains
ORDER {
    string book_title FK The_Catcher_in_the_Rye
    int number_of_items 1}
COLLECTION ||--|{ TITLE : holds
COLLECTION {
    string book_titles FK 
    string genre FK
    string media_types FK
    int copies_available FK
}
```

This is a note