```mermaid
    sequenceDiagram
    actor Tutor as Tutor
    participant Sist as Sistema de Tutorias

    Tutor->>Sist: 1. Accede a 'Asistencias', selecciona grupo y sesión/actividad
    Sist-->>Tutor: 2. Despliega lista de tutorados del grupo
    Tutor->>Sist: 3. Marca estatus (Presente/Ausente/Justificado) y agrega notas/observaciones
    Tutor->>Sist: 4. Confirma el registro ('Guardar asistencia')
    Sist->>Sist: 5. Actualiza porcentaje de asistencia acumulado por tutorado
    Sist-->>Tutor: 6. Despliega resumen del registro confirmado
