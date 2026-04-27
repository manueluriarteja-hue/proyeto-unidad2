```mermaid
    sequenceDiagram
    actor Tutor as Tutor
    participant Sist as Sistema de Tutorías

    Tutor->>Sist: 1. Accede a 'Evaluación de tutorados', selecciona grupo y periodo parcial
    Sist-->>Tutor: 2. Muestra resumen del tutorado (asistencias, notas, reprobación)
    Tutor->>Sist: 3. Evalúa con rúbrica
    Tutor->>Sist: 4. Registra observaciones y define si requiere canalización
    Tutor->>Sist: 5. Guarda la evaluación parcial
    Sist->>Sist: 6. Actualiza estatus del tutorado (Al corriente / En riesgo)
