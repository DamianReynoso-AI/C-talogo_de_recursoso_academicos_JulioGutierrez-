# Catálogo de Recursos Académicos

## Descripción
Aplicación que representa la estructura inicial de un sistema para registrar y consultar recursos académicos como libros, sitios web, videos, artículos y herramientas de software.

## Objetivo
Sentar las bases de un catálogo digital que permita organizar y clasificar recursos académicos de distintos tipos, facilitando su búsqueda y consulta.

## Estructura general
catalogo_recursos/
├── app/
│ ├── main.py
│ └── configuracion.py
├── data/
│ └── recursos.json
├── docs/
│ ├── alcance.md
│ ├── criterios.md
│ ├── respuestas.md
│ └── evidencias/
├── tests/
│ └── test_basico.py
├── .gitignore
├── README.md
├── requirements.txt
└── CHANGELOG.md


## Tecnologías utilizadas
- Python 3
- Git y GitHub
- Visual Studio Code

## Preparación del entorno
1. Clona el repositorio.
2. Crea un entorno virtual: `python -m venv .venv`
3. Actívalo.
4. Instala las dependencias: `pip install -r requirements.txt`

## Dependencias
- requests
- rich

## Próximas mejoras

- Implementar búsqueda y filtrado de recursos por tipo, tema y nivel.
- Agregar validación de datos al registrar nuevos recursos.
- Incluir pruebas automatizadas más completas.
- Conectar el catálogo con una interfaz de usuario sencilla.