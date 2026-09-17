---  
layout: full
class: bg-[#858778] text-white flex flex-col items-center justify-center
bibFile: references.bib
hideInToc: false
highlighter: shiki
---

# Mapeos avanzados en Hibernate: Many-to-Many bidireccional

---
layout: two-cols

---

# 🧩 ¿Qué es una relación Many-to-Many?

- Un **Curso** (`Course`) puede tener **muchos estudiantes** matriculados.
- Un **Estudiante** (`Student`) puede inscribirse en **muchos cursos**.
- Para relacionarlos a nivel de base de datos relacional, necesitamos obligatoriamente una **tabla Intermedia** (`course_student`).

::right::
```mermaid
erDiagram 
    INSTRUCTOR ||--o{ COURSE : "enseña (1:N)"
    COURSE ||--o{ COURSE_STUDENT : "contiene"
    STUDENT ||--o{ COURSE_STUDENT : "inscribe"
    INSTRUCTOR ||--|| INSTRUCTOR_DETAIL : has
    INSTRUCTOR {
        int id PK
        string first_name
        string last_name
        string email
        int instructor_detail_id FK
    }

    COURSE {
        int id PK
        string title
        int instructor_id FK
    }

    INSTRUCTOR_DETAIL {
        int id PK
        string youtube_channel
        string hobby
    }
    STUDENT {
        int id PK
        string first_name
        string last_name
        string email
    }
    COURSE_STUDENT {
        int course_id PK, FK
        int student_id PK, FK
    }
```
