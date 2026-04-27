```mermaid
    sequenceDiagram
    actor Alumno as Tutorado
    participant Sist as Sistema de Tutorías

    Alumno->>Sist: 1. Accede a 'Mis actividades' y selecciona actividad 'Pendiente'
    Sist-->>Alumno: 2. Muestra requisitos de evidencia y fecha límite
    Alumno->>Sist: 3. Sube archivo, agrega comentario opcional y da clic en 'Entregar evidencia'
    Sist->>Sist: 4. Valida formato y tamaño del archivo (Máx 10MB)
    Sist->>Sist: 5. Registra evidencia, fecha y cambia estatus a 'Entregada'
    Sist-->>Alumno: 6. Muestra confirmación de entrega
