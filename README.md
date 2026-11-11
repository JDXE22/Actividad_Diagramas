# Actividad_Diagramas

La base de datos está diseñada en Tercera Forma Normal (3FN) para evitar la duplicidad de datos y garantizar la integridad referencial. Consta de 3 tablas principales con las siguientes relaciones:

```text
[Autores] 1 ----- N [Libros] N ----- 1 [Editores]

```

### Detalle de las Relaciones:

1. **Tabla `Autores`:**

- **Clave Primaria (PK):** `ID_Autor`

- **Relación con `Libros`:** Uno a Muchos (**1:N**).
- _Descripción:_ Un autor puede haber escrito uno o varios libros, pero cada libro registrado pertenece a un único autor principal.

2. **Tabla `Editores`:**

- **Clave Primaria (PK):** `ID_Editor`

- **Relación con `Libros`:** Uno a Muchos (**1:N**).
- _Descripción:_ Una editorial puede publicar múltiples libros, pero cada libro en el sistema está asociado a una única editorial editora.

3. **Tabla `Libros` (Tabla Intermedia / Entidad Principal):**

- **Clave Primaria (PK):** `ID_Libro`

- **Claves Foráneas (FK):** `ID_Autor` y `ID_Editor`

- _Descripción:_ Centraliza la información del título de la obra y actúa como puente al almacenar las referencias (`ID_Autor` e `ID_Editor`) que conectan cada libro con su respectivo creador y casa editorial.

---
