```mermaid
    sequenceDiagram
    actor Coordinador as Coordinador Institucional
    participant Sistema as Sistema de Tutorías (SGPT)

    Coordinador->>Sistema: 1. Accede a Gestión de Usuarios y selecciona 'Registrar nuevo usuario'
    Sistema-->>Coordinador: 2. Despliega el formulario de alta
    Coordinador->>Sistema: 3. Ingresa datos generales y selecciona el rol
    Coordinador->>Sistema: 4. Presiona el botón 'Guardar'
    Sistema->>Sistema: 5. Valida datos correctos y no duplicidad
    Sistema->>Sistema: 6. Genera credenciales y envía correo
    Sistema-->>Coordinador: 7. Muestra mensaje "Usuario registrado exitosamente"
