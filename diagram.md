erDiagram
    User {
        UUID id PK
        String email
        String full_name
        Timestamp created_at
    }

    Course {
        UUID id PK
        String title
        String description
        UUID author_id FK
    }

    Module {
        UUID id PK
        String title
        Int order_index
        UUID course_id FK
    }

    User }o--o{ Course : "enrolled_in"
    Course ||--|{ Module : "contains"
    User ||--o{ Course : "created_by"