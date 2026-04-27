```mermaid
    sequenceDiagram
    actor Coord as Coord Dpto Academico
    participant Sist as Sistema de Tutorías

    Coord->>Sist: 1. Accede a 'Asignación de tutorados', selecciona periodo y tutor
    Sist-->>Coord: 2. Muestra grupo del tutor, cupo disponible y lista de alumnos sin tutor
    Coord->>Sist: 3. Selecciona tutorados a asignar (individual o bloque)
    Coord->>Sist: 4. Confirma asignación ('Asignar tutorados')
    Sist->>Sist: 5. Registra la relación tutor-tutorado para el semestre
    Sist-->>Coord: 6. Confirma la asignación exitosa
