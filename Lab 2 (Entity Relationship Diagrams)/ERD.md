```mermaid
erDiagram
TITLE {
    string book_title
    string ISBN PK
    string genre
    string author
    string media_type
    int copy
}
PATRON ||--|{ ORDER : checks_out
PATRON {
    string name
    string librarycardNumber PK
}
ORDER ||--|{ TITLE : contains
ORDER {
    string book_title FK
    int number_of_items}
COLLECTION ||--|{ TITLE : holds
COLLECTION {
    string book_titles FK
    string genre FK
    string media_types FK
    int copies_available FK
}

Here is some more information