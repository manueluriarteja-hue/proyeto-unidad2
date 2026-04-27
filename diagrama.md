```mermaid
    sequenceDiagram
    actor Coord as Coordinador Institucional
    participant Sist as Sistema SGPT

    Coord->>Sist: 1. Accede a Gestión de Usuarios y selecciona 'Registrar nuevo usuario'
    Sist-->>Coord: 2. Despliega el formulario de alta
    Coord->>Sist: 3. Ingresa datos generales y selecciona rol (Tutor, Tutorado, etc.)
    Coord->>Sist: 4. Confirma registro presionando 'Guardar'
    Sist->>Sist: 5. Valida que no exista duplicado de matrícula/número de control
    Sist->>Sist: 6. Genera credenciales temporales y envía al correo institucional
    Sist-->>Coord: 7. Muestra mensaje "Usuario registrado exitosamente" y resumen
