```mermaid
erDiagram
TITLE {
    string book_title
    string ISBN
    string genre
    string author
    int copies
}
PATRON ||--|{ ORDER : checks_out
PATRON {
    string name
    string librarycardNumber
}
ORDER ||--|{ TITLE : contains
ORDER {
    string book_titles
    int quantity}
COLLECTION ||--|{ TITLE : holds
COLLECTION {
    string book_titles
    string genre
    string media_types
    int copies_available
}