```mermaid
    sequenceDiagram
    actor Tutor as Tutor
    participant Sist as Sistema de Tutorías

    Tutor->>Sist: 1. Accede a 'Evidencias pendientes', selecciona grupo y actividad
    Sist-->>Tutor: 2. Muestra listado de tutorados con estatus de entrega
    Tutor->>Sist: 3. Selecciona tutorado y revisa evidencia cargada
    Tutor->>Sist: 4. Asigna resultado (Aceptada/Requiere corrección/Rechazada) y retroalimentación
    Tutor->>Sist: 5. Guarda la evaluación
    Sist->>Sist: 6. Actualiza estado de la actividad del tutorado
