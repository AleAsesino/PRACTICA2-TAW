# 📘 Endpoints – API de Docentes

Estos son los endpoints disponibles para la gestión de docentes en el sistema de Registro Universitario.

---

### 🔹 `GET /api/docentes`

- Obtiene la lista de todos los docentes registrados.

---

### 🔹 `POST /api/docentes`

- Crea un nuevo docente en el sistema.

---

### 🔹 `PUT /api/docentes/{id}`

- Actualiza los datos de un docente según su ID.

---

### 🔹 `DELETE /api/docentes/{id}`

- Elimina un docente por su ID.

---

### 🔹 `PUT /api/docentes/inscribirse/{id_docente}/{id_materia}`

- Asigna un docente a una materia específica.

---
# 📘 Endpoints – API de Estudiantes

Estos son los endpoints disponibles para la gestión de estudiantes en el sistema de Registro Universitario.

---

### 🔹 `GET /api/estudiantes`
- Obtiene la lista de todos los estudiantes registrados.

### 🔹 `GET /api/estudiantes/inscripcion/{numeroInscripcion}`
- Obtiene un estudiante específico mediante su número de inscripción.

### 🔹 `GET /api/estudiantes/{id}/materias`
- Lista todas las materias a las que está inscrito un estudiante por su ID.

### 🔹 `GET /api/estudiantes/{id}/lock`
- Obtiene los datos del estudiante aplicando bloqueo de concurrencia (lock).

### 🔹 `POST /api/estudiantes`
- Registra un nuevo estudiante en el sistema.

### 🔹 `PUT /api/estudiantes/{id}`
- Actualiza los datos de un estudiante según su ID.

### 🔹 `PUT /api/estudiantes/{id}/baja`
- Marca a un estudiante como dado de baja en el sistema.

### 🔹 `GET /api/estudiantes/activos`
- Obtiene la lista de estudiantes activos.

---

## 📚 Gestión de Inscripciones

### 🔹 `PUT /api/estudiantes/inscribirse/{id_estudiante}/{id_materia}`
- Inscribe a un estudiante en una materia.

### 🔹 `PUT /api/estudiantes/inscribirse/{id_estudiante}/{id_retiro}/{id_inscribirse}`
- Modifica una inscripción reemplazando una materia por otra.

### 🔹 `PUT /api/estudiantes/retirar/{id_estudiante}/{id_retiro}`
- Retira a un estudiante de una materia inscrita.

---

---

# 🧾 Endpoints – Evaluación Docente

Estos endpoints permiten gestionar las evaluaciones realizadas a docentes.

---

### 🔹 `POST /api/evaluaciones-docente`
- Crea una nueva evaluación docente.

### 🔹 `GET /api/evaluaciones-docente/docente/{docenteId}`
- Obtiene todas las evaluaciones asociadas a un docente específico.

### 🔹 `GET /api/evaluaciones-docente/{id}`
- Obtiene una evaluación docente específica por su ID.

### 🔹 `DELETE /api/evaluaciones-docente/{id}`
- Elimina una evaluación docente por su ID.

---

---

# 📚 Endpoints – Materias

Estos endpoints permiten gestionar las materias en el sistema universitario.

---

### 🔹 `GET /api/materias`
- Obtiene la lista de todas las materias disponibles.
- 📌 Acceso: Público (`permitAll`)

### 🔹 `GET /api/materias/{id}`
- Obtiene una materia específica por su ID.
- 🔐 Acceso: Roles `ESTUDIANTE`, `DOCENTE`, `ADMIN`

### 🔹 `GET /api/materias/codigo/{codigoUnico}`
- Obtiene una materia por su código único.
- 🔐 Acceso: Roles `ESTUDIANTE`, `DOCENTE`, `ADMIN`

### 🔹 `POST /api/materias`
- Crea una nueva materia.
- 🔐 Acceso: Roles `ESTUDIANTE`, `DOCENTE`, `ADMIN`

### 🔹 `PUT /api/materias/{id}`
- Actualiza una materia existente por su ID.
- 🔐 Acceso: Roles `ESTUDIANTE`, `DOCENTE`, `ADMIN`

### 🔹 `DELETE /api/materias/{id}`
- Elimina una materia por su ID.
- 🔐 Acceso: Roles `ESTUDIANTE`, `DOCENTE`, `ADMIN`

### 🔹 `GET /api/materias/formaria-circulo/{materiaId}/{prerequisitoId}`
- Verifica si agregar un prerequisito a una materia generaría un ciclo de dependencias.
- 🔐 Acceso: Roles `ESTUDIANTE`, `DOCENTE`, `ADMIN`
