```mermaid
    classDiagram
    class TECNM {
        -String claveInstitucional
    }
    class ITCuliacan {
        -Int idCampus
        -String nombreCampus
    }
    class Programa_Tutorias {
        -Int idPrograma
        -String periodoEscolar
        -String objetivoGeneral
    }
    class Usuario {
        -Int idUsuario
        -String nombreCompleto
        -String correoInstitucional
        -String estatus
        +iniciarSesion()
    }
    class Director {
        +consultarReportesEstadisticos()
        +consultarDistribucionTutoria()
    }
    class Subdirector {
        +consultarReportesEstadisticos()
        +consultarDistribucionTutoria()
    }
    class Jefe_Desarrollo_Academico {
        +consultarActividades()
    }
    class Coordinadora_Institucional {
        +programarActividadesPT()
        +capturarPlanAccion()
        +gestionarUsuarios()
        +exportarReportesEstadisticos()
    }
    class Jefe_Departamento_Academico {
        +consultarAsignaciones()
        +consultarReportesEstadisticos()
    }
    class Coordinadora_Departamental {
        +asignarTutores()
        +asignarTutorados()
        +consultarReportesEstadisticos()
    }
    class Tutor {
        -String noEmpleado
        +capturarFechaSesion()
        +pasarAsistencia()
        +revisarEvidencias()
        +registrarCalificaciones()
    }
    class Tutorado {
        -String noControl
        +subirEvidenciaActividad()
    }
    class Actividad {
        -Int idActividad
        -String nombreActividad
        -String descripcion
        -Date fechaProgramada
        -String fasePT
        -boolean requiereEvidencia
    }
    class Asignacion {
        -Int idAsignacion
        -String grupo
        -String horario
    }
    class Sesion {
        -Int idSesion
        -Date fechaRealizada
        -String observaciones
    }
    class Evidencia {
        -Int idEvidencia
        -String urlArchivo
        -Date fechaCarga
    }
    class Evaluacion {
        -Int idEvaluacion
        -float calificacionFinal
    }

    %% Jerarquía de Herencia
    Usuario <|-- Director
    Usuario <|-- Subdirector
    Usuario <|-- Jefe_Desarrollo_Academico
    Usuario <|-- Coordinadora_Institucional
    Usuario <|-- Jefe_Departamento_Academico
    Usuario <|-- Coordinadora_Departamental
    Usuario <|-- Tutor
    Usuario <|-- Tutorado

    %% Relaciones y Cardinalidades
    TECNM "1" *-- "1" ITCuliacan
    ITCuliacan "1" *-- "1" Programa_Tutorias
    Programa_Tutorias "1" *-- "1..*" Actividad : se_compone_de
    Director ..> Programa_Tutorias : consulta
    Subdirector ..> Programa_Tutorias : consulta
    Tutor "1" -- "1..*" Asignacion : imparte
    Tutorado "1..25" -- "1" Asignacion : pertenece_a
    Asignacion "1" -- "1..*" Sesion : registra
    Actividad "1" -- "0..*" Evidencia : genera
    Tutorado "1" -- "0..*" Evidencia : entrega
    Tutor "1" -- "0..*" Evidencia : valida
    Tutorado "1" -- "1" Evaluacion : recibe
    Tutor "1" -- "1..*" Evaluacion : califica
