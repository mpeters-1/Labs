```mermaid
erDiagram
TITLE {
    string book_title
    string ISBN
    string genre
}
PATRON ||--|{ ORDER : checks_out
PATRON {
    string name
    string librarycardNumber
    string address
}}