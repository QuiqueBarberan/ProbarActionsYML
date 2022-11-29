# ProbarActionsYML
Probar posibilidades matriz eventos, yml, ramas

Este repositorio es para probar el boton de RUN con distintas posibilidades.
Lanzar desde la rama por defecto sobre otras ramas... ¿qué ocurre?


## Estructura del repositorio

├── .github
│   └── workflows
│       └── YAML1.yml
│       └── YAML2.yml
├── Lectura.txt
└── README.md

Donde:
Lectura.txt
 - Su contenido ha sido modificido en cada rama para que al leerlo se obtenga resultado distinto.

YAML1.yml
 - Contiene un pipeline que se repite en todas las ramas. Todas las ramas se comportan igual.
 - Excepcion: una condicion de IF en cada job unicamente en la rama master. Por lo que el comportamiento en la rama master difiere del resto de ramas.

YAML2.yml
 - Contiene un job donde unicamente se ejecutará en la propia rama.


## Objetivo del repositorio
Acudir a Pestaña ACTIONS, y observar que YAML2.yml no se puede lanzar desde la rama master (rama por defecto).
 - Este archivo no se encuentra en rama master pero si en otras ramas. ¿cómo lanzarlo? Con otros eventos que no sean workflow_dispatch.

Acudir a Pestaña ACTIONS, y ejecutar el pipeline YAML1.yml con todas las posibilidades de ramas.
 - Se podrá observar que se ejecuta el YAML1.yml contenido en la propia rama, no el archivo de la rama por defecto.
