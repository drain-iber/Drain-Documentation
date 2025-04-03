[![Read the documentation](https://img.shields.io/badge/Read-the%20docs-green.svg)](https://docs.drain.org/testing/)

Este repositorio está destinado a escribir y gestionar la Documentación Oficial del plugin de QGIS [Drain](https://www.drain.org),
que es un sistema de información geográfica para el desarrollo de proyectos de ingeniería hidráulica y sanitaria.

## Tabla de contenidos

- [Documentación](#documentación)
- [Construir la documentación](#construir-la-documentación)
  - [En Linux o macOS](#en-linux-o-macos)
  - [En Windows](#en-windows)
- [Traducción de la documentación](#traducción-de-la-documentación)

## Documentación

La documentación se encuentra en el directorio `docs` y está escrita usando [Sphinx](https://www.sphinx-doc.org/en/master/) con archivos fuente en formato reStructuredText.

La última documentación de Drain se encuentra disponible en el siguiente enlace: [Documentación de Drain](https://docs.drain.org/testing/)

## Construir la documentación

1. Instala los paquetes necesarios en tu sistema operativo.

Debes de tener en tu sistema operativo instalado los siguientes paquetes:

- git
- python (>= 3.9)

Puedes instalarlos usando el gestor de paquetes de tu sistema operativo.

2. Clona el repositorio en tu máquina local.

```bash
git clone https://github.com/drain-iber/Drain-Documentation.git
```

3. Accede al directorio del repositorio.

```bash
cd Drain-Documentation
```

La mejor forma de construir la documentación es usando el entorno virtual de Python que viene incluido en el repositorio. Para ello sigue los siguientes pasos según tu sistema operativo.

### En Linux o macOS

Para crear el entorno virtual y activarlo, ejecuta los siguientes comandos:

> Nota: Si no tienes instalado Python 3.9 o superior, puedes instalarlo usando el gestor de paquetes de tu sistema operativo.

```bash
python3 -m venv venv
```

Ahora activa el entorno virtual.

```bash
source venv/bin/activate
```

Ejecuta el siguiente comando para instalar las dependencias necesarias.

```bash
pip install -r REQUIREMENTS.txt
```

Ahora puedes construir la documentación usando el siguiente comando.

```bash
make html
```

La documentación se construirá en el directorio `docs/build/html/en/`.

Si quieres ver la documentación en tu navegador, ejecuta el siguiente comando.

```bash
make open
```

### En Windows

Para crear el entorno virtual y activarlo, ejecuta los siguientes comandos:

```bash
python -m venv venv
```

Ahora activa el entorno virtual.

```bash
venv\Scripts\activate
```

Ejecuta el siguiente comando para instalar las dependencias necesarias.

```bash
pip install -r REQUIREMENTS.txt
```

Ahora puedes construir la documentación usando el siguiente comando.

```bash
./make.bat html
```

La documentación se construirá en el directorio `docs\build\html\en\`.

Si quieres ver la documentación en tu navegador, ejecuta el siguiente comando.

```bash
./make.bat open
```

## Traducción de la documentación

Para traducir la documentación a otros idiomas, revisa la lista de idiomas disponibles en el archivo `docs_conf.yml`.

Actualmente estamos usando Weblate para gestionar las traducciones de la documentación. Si quieres colaborar en las traducciones, puedes hacerlo en el siguiente enlace: [Traducciones de la documentación](https://translate.docs.drain.org/projects/drain/drain-documentation/).

El proceso esta automatizado con workflows de GitHub Actions y scripts personalizados.
