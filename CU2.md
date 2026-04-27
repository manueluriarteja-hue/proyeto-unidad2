```mermaid
    sequenceDiagram
    actor Coord as Coordinador del PT
    participant Sist as Sistema SGPT
    actor Tutor as Tutores Asignados

    Coord->>Sist: 1. Accede a 'Planificación del PT', selecciona periodo y 'Nueva actividad'
    Sist-->>Coord: 2. Despliega formulario de registro de actividad
    Coord->>Sist: 3. Ingresa datos (nombre, fase, tipo) y define si requiere evidencia
    Coord->>Sist: 4. Asigna la actividad (a todos, por carrera o específico)
    Coord->>Sist: 5. Guarda actividad presionando 'Registrar actividad'
    Sist->>Sist: 6. Valida datos y registra la actividad en el semestre
    Sist-->>Coord: 7. Confirma el registro exitoso
    Sist-->>Tutor: 8. Notifica sobre la nueva actividad asignada
