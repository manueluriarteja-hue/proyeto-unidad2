```mermaid
    sequenceDiagram
    actor Coord as Jefe Departamento Academico
    participant Sist as Sistema de Tutorías

    Coord->>Sist: 1. Accede a 'Asignación de grupos', selecciona periodo y busca tutor
    Sist-->>Coord: 2. Muestra perfil del tutor y asignaciones actuales
    Coord->>Sist: 3. Selecciona grupo, define horario (día/horas) y asigna salón
    Coord->>Sist: 4. Confirma asignación ('Guardar asignación')
    Sist->>Sist: 5. Valida que no exista conflicto de horario ni sobrecarga
    Sist->>Sist: 6. Registra la asignación
    Sist-->>Coord: 7. Muestra confirmación de asignación
