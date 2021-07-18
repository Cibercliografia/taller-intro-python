---
title: Taller Introducción a Python para el análisis de datos históricos
author: Víctor Gayol
date: 2021-07-15
---

## Introducción

El taller *Introducción a Python para el análisis de datos históricos* está diseñado como una puerta de entrada al uso de un lenguaje de programación de alto nivel, como Python, para crear herramientas de análisis de datos digitales de investigación en historia, ciencias sociales y humanidades.

Está dirigido a aquellas personas que no tienen experiencia alguna en el uso de lenguajes de programación.

El taller comienza desde 0 con un repaso del uso de la interfaz de línea de comandos (CLI, *command-line-interface*), para después adentrarse en las nociones mínimas del funcionamiento del lenguaje de programación.

Con las nociones básicas aprendidas, el taller tiene como objetivo desarrollar un par de módulos de código que sean útiles para el análisis de un texto histórico. Básicamente, se mostrará: 1) cómo extraer la frecuencia de palabras del texto, lo cual sirve como indicador de los temas que trata el documento; y 2) hacer un listado de palabras clave en contexto (KWC), lo cual es útil para saber de qué manera se utilizaron ciertos términos en relación con otros en el documento. 

### Requisitos previos

**Línea de comandos**

Usuaria/os Windows: instalar el CLI [GitBash](https://gitforwindows.org/) para homologar el uso de comandos UNIX con el resto de usuaria/os (macOS, Linux). Si ya se tiene experiencia en el manejo de [PowerShell](https://es.wikipedia.org/wiki/PowerShell), no es necesario.

**Editor de texto y código**

Para poder escribir archivos en texto plano y también correr módulos con fragmentos de código necesitamos un [editor de texto](https://es.wikipedia.org/wiki/Editor_de_texto) que sea a la vez [editor de código fuente](https://es.wikipedia.org/wiki/Editor_de_c%C3%B3digo_fuente). Hay muchos disponibles. Particularmente recomiendo [Atom](https://atom.io/) y [Visual Studio Code](https://code.visualstudio.com/), ambos con licencia MIT; o [Sublime Text](https://www.sublimetext.com/), que es propietario (licencia = $99.00 US), pero la versión de prueba tiene casi completa funcionalidad. Komodo Edit era una opción gratuita de [Komodo IDE](https://www.activestate.com/products/komodo-ide/), pero actualmente está muy descuidada.

**Nota:** Para habilitar Atom como editor de código es necesario descargar el paquete `script`. Para ello abrir el menú `--> Packages --> Command Palet --> Toogle`, y elegir `install packages and themes`; buscar `script`e instalar.

**Python**

Usuaria/os Windows y macOS: pueden descargar Python directamente de [https://www.python.org/](https://www.python.org/) procurando que sea la versión 3.8 y no la última (3.9). Una buena estrategia para obtener Python es recurriendo a la distribución de [Anaconda](https://www.anaconda.com/products/individual) que permite tener, además, muchas de las librerías que se utilizan en el análisis de datos en historia y humanidades digitales. Esto evita sufrir con la instalación de `cartopy`, `scikit-learn`o `geos proj`que requerirían tener preinstalado [Homebrew](https://brew.sh/index_es).

**Nota:** usuaria/os macOS. **Python 2.7** está instalado por defecto en las Mac para llevar a cabo algunas operaciones del sistema. Pero Python 2.7 ya no es utilizada para programación en general, pues el código ya no tiene mantenimiento y puede causar problemas de seguridad en los equipos. Por lo tanto, cuando se abre o se corre un programa en Python 3.x desde la CLI (Terminal), es necesario indicar la versión:

```
~$ python3
>>>
```

**Data**

Para este taller solamente revisaremos dos ejemplos de minería de texto (conteo de fecuencia y palabras clave en contexto, o KWC), a partir de un texto único. Trabajaremos con un libro del siglo XVII: el *Tratado de confirmaciones reales de encomiendas...* de Antonio de León Pinelo (1630). Para obtener los datos:

* Ir al sitio del proyecto de la Escuela de Salamanca donde se encuentra el libro: [https://www.salamanca.school/es/work.html?wid=W0061](https://www.salamanca.school/es/work.html?wid=W0061)
* En el menú de la parte superior, donde dice `exportar`, elegir `texto simple (TXT)`y descargar las dos versiones ('constituido' y 'diplomático').
* Guardar en una carpeta de trabajo llamada `python-data` en el escritorio de la computadora.

#### Ejemplo:

Windows
```
C:\users\user\escritorio\python-data\
```

macOS, UNIX:
```
/users/user/desktop/python-data/
```

### comprobar

Una vez instalado Python 3.8.x en la computadora, abrir el CLI y escribir en el cursor lo siguiente:

Windows cmd o PowerShell:
```
C:\user>python --version
```

macOS o Linux
```
~ $ python3 --version
```

Si Python está bien instalado aparecerá por respuesta algo así como: `python 3.8.x`

### Referencias

Baker, James. "Preservar tus datos de investigación", traducido por Víctor Gayol, *The Programming Historian en español 1* (2017), https://doi.org/10.46430/phes0023.

Dawson, Ted. "Introducción a la línea de comandos de Windows con PowerShell", traducido por Victor Gayol, *The Programming Historian en español 2* (2018), https://doi.org/10.46430/phes0037.

Gibbs, Fred. "Instalar módulos de Python con pip", traducido por Víctor Gayol, *The Programming Historian en español 1* (2017), https://doi.org/10.46430/phes0012.

Lutz, Mark. *Learning Python: Powerful Object-Oriented Programming*. Beijing: O'Reilly, 2013.

———. *Programming Python: Powerful Object-Oriented Programming*. Beijing: O'Reilly, 2011.

———. *Python Pocket Reference: Python in Your Pocket*. Beijing: O'Reilly, 2014.


Matthes, Eric. *Python Crash Course, 2Nd Edition: A Hands-On, Project-Based Introduction To Programming*. 2da edición. San Francisco, CA: No Starch Press, 2019.

Milligan, Ian  y James Baker, "Introducción a la línea de comandos en Bash", traducido por Víctor Gayol, *The Programming Historian en español 1* (2017), https://doi.org/10.46430/phes0013.

Turkel, William J. y Adam Crymble. "Introducción a Python e Instalación", traducido por Víctor Gayol, *The Programming Historian en español 1* (2017), https://doi.org/10.46430/phes0016. (14 lecciones)
