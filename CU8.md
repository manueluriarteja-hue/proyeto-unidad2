```mermaid
    sequenceDiagram
    actor Tutor as Tutor
    participant Sist as Sistema de Tutorías

    Tutor->>Sist: 1. Accede a 'Mis actividades', selecciona grupo y actividad a modificar
    Sist-->>Tutor: 2. Muestra formulario con campos editables
    Tutor->>Sist: 3. Adapta descripción, fecha o requisitos e ingresa justificación obligatoria
    Tutor->>Sist: 4. Guarda cambios ('Actualizar actividad')
    Sist->>Sist: 5. Registra modificación, justificación y fecha
