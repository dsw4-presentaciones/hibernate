---
layout: default
hideInToc: true
---

# ¿Por Qué Utilizar un ORM?

### Object Relational Mapping (ORM)

Puente entre el mundo orientado a objetos y las bases de datos relacionales.

---
hideInToc: true
---

# Problema: Objetos vs. Tablas

Las aplicaciones trabajan con objetos:

```java
User user = new User();
user.setUsername("juan");
```

Las bases de datos trabajan con tablas:

```sql
INSERT INTO USERS (USERNAME)
VALUES ('juan');
```

### El ORM se encarga de:

- Convertir objetos en registros.
- Convertir registros en objetos.
- Reducir código SQL repetitivo.
- Mantener sincronizados ambos modelos.

> El desarrollador(a) trabaja principalmente con objetos y el ORM gestiona la persistencia.

---
hideInToc: true
---

# Beneficios de Utilizar ORM

✅ Mayor productividad del desarrollador

✅ Menos código SQL manual

✅ Código más limpio y mantenible

✅ Independencia parcial de la base de datos

✅ Manejo automático de relaciones entre entidades

```java
User user = userRepository.findById(1L);

user.setEmail("nuevo@email.com");

userRepository.save(user);
```

Sin necesidad de escribir explícitamente:

```sql
SELECT ...
UPDATE ...
```

---
hideInToc: true
---

# Herramientas populares:

- Hibernate
- JPA
- Spring Data JPA
- Entity Framework (.NET)

---
layout: default
hideInToc: true
---

# ORM: Object Relational Mapping

## La técnica que conecta objetos y tablas

### ¿Qué hace?

Convierte automáticamente:

```java
User user = new User("Juan");
```

en operaciones sobre la base de datos:

```sql
INSERT INTO USERS ...
```

### Beneficios

✅ Menos SQL manual

✅ Código orientado a objetos

✅ Mayor productividad

✅ Mejor mantenibilidad

> ORM es un concepto o técnica, no una herramienta específica.

---
hideInToc: true
layout: two-cols
---

# JPA y Hibernate

## Estándar + Implementación

### JPA (Java Persistence API)

Es la especificación oficial de Java para persistencia.

Define:

- `@Entity`
- `@Id`
- `@OneToMany`
- `EntityManager`
- JPQL

::right::
```java
@Entity
public class User {
    @Id
    private Long id;
}
```

### Hibernate

Es la implementación más popular de JPA.

Responsabilidades:

- Generar SQL
- Gestionar entidades
- Manejar relaciones
- Administrar el contexto de persistencia

> JPA define las reglas; Hibernate realiza el trabajo.

---
hideInToc: true
layout: two-cols
---

# Spring Data JPA

## Simplificando el acceso a datos

Sin Spring Data:

```java
entityManager.createQuery(...)
```

Con Spring Data:

```java
public interface UserRepository
        extends JpaRepository<User, Long> {

    User findByUsername(String username);
}
```
::right::

- **ORM** → Técnica de mapeo objeto-relacional.
- **JPA** → Especificación estándar.
- **Hibernate** → Implementación de JPA.
- **Spring Data JPA** → Capa que simplifica el uso de JPA/Hibernate.