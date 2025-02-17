```mermaid
erDiagram
TITLE {
    string Catcher_in_the_Rye
    string 9780316769488 PK
    string youngadult_fiction
    string JD_salinger
    string eBook
    int 1_of_12
}
PATRON ||--|{ ORDER : checks_out
PATRON {
    string John_Doe
    string 000123456 PK
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
```

This is a note.