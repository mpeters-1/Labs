```mermaid
erDiagram
TITLE {
    string book_title
    string ISBN
    string genre
    string author
    string media_type
    int copy
}
PATRON ||--|{ ORDER : checks_out
PATRON {
    string name
    string librarycardNumber
}
ORDER ||--|{ TITLE : contains
ORDER {
    string book_titles
    int number_of_items}
COLLECTION ||--|{ TITLE : holds
COLLECTION {
    string all_titles
    string genre
    string media_types
    int copies_available
}