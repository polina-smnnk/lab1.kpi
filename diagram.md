erDiagram
    User { Int id PK }
    Course { Int id PK }
    User_Course { Int user_id FK, Int course_id FK }
    Module { Int id PK, Int course FK }
    User ||--o{ User_Course : ""
    Course ||--o{ User_Course : ""