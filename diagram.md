erDiagram
    User { UUID id PK, String email }
    Course { UUID id PK, String title, UUID author_id FK }
    Module { UUID id PK, String title, UUID course_id FK }
    User }o--o{ Course : "enrolled_in"
    Course ||--|{ Module : "contains"