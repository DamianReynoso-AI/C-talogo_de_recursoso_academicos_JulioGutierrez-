## Pregunta de control (Punto 6)

**¿Qué ventaja tiene registrar las dependencias del proyecto en requirements.txt en lugar de compartir la carpeta .venv?**

Registrar las dependencias en `requirements.txt` es mucho más eficiente que compartir la carpeta `.venv`, ya que este archivo solo contiene una lista de texto con los nombres y versiones de las bibliotecas necesarias, mientras que `.venv` puede pesar varios cientos de megabytes al incluir todos los binarios e instalaciones completas del intérprete y los paquetes. Además, `.venv` depende del sistema operativo en el que fue creado, por lo que compartirla podría causar errores en otras máquinas o plataformas distintas. Con `requirements.txt`, cualquier persona puede recrear exactamente el mismo entorno ejecutando `pip install -r requirements.txt`, sin importar su sistema operativo, manteniendo el repositorio ligero y evitando subir archivos innecesarios a Git.

79. ¿Cómo identificaron el comando necesario cuando la práctica no lo proporcionó?

Pensamos en qué queríamos hacer y buscamos cómo hacerlo. Por ejemplo, si necesitábamos crear un entorno virtual, buscamos "cómo crear entorno virtual Python". Experimentamos con comandos seguros y leímos los errores para entender qué estaba mal.

80. ¿Qué diferencia existe entre preparar un archivo para un commit y crear el commit?

git add prepara el archivo (lo pone listo). git commit lo guarda en el historial. Es como hacer una foto: primero alinjas (add), luego aprietas el botón (commit).

81. ¿Cómo pueden comprobar en qué rama están trabajando?

Con git branch. Aparece un asterisco (*) en la rama donde estamos. También lo vemos en VS Code abajo a la izquierda.

82. ¿Cómo pueden determinar qué archivos fueron modificados antes de registrarlos?

Con git status. Nos muestra qué archivos cambiamos y cuáles están listos para commit.

83. ¿Cómo pueden observar exactamente qué cambió dentro de un archivo?

Con git diff nombre_archivo.md. Nos muestra línea por línea qué agregamos (verde) y qué borramos (rojo).

84. ¿Por qué debe reconstruirse .venv después de obtener un repositorio?

Porque .venv no está en GitHub (está ignorado). Cuando clonamos el proyecto no lo bajamos, así que tenemos que crearlo nuevo. Además, las dependencias pueden no ser compatibles entre sistemas operativos diferentes.

85. ¿Qué relación existe entre requirements.txt y .gitignore?

requirements.txt lista qué librerías necesitamos. .gitignore excluye .venv de Git. Compartimos la lista (pequeña) pero no la carpeta (pesada).

86. ¿Por qué la colaboración se realiza desde una rama y no directamente desde main?

Porque main debe estar siempre estable. En una rama podemos experimentar sin romper nada. Otros pueden revisar nuestros cambios antes de mezclarlos.

87. ¿Por qué una solicitud de cambios no requiere crear un Pull Request nuevo?

Porque el Pull Request está conectado a la rama. Si hacemos más cambios en la misma rama y hacemos push, GitHub actualiza automáticamente el PR. No necesitamos hacer otro.

88. Después de realizar el merge en GitHub, ¿por qué todavía es necesario actualizar el repositorio local?

Porque el merge pasó en GitHub, no en nuestras computadoras. Hacemos git pull para descargar los cambios y estar sincronizados.