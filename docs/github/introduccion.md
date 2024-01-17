!!! note

    I've led this short workshop as part of Summer School of [UDD CICS](https://complejidadsocial.udd.cl/). I will soon compile the material here.

# [Workshop] Orbitar Jupyter y Aterrizar en la Tierra: un viaje en Github hacia la Ciencia de Datos Práctica y Colaborativa.

<img src="https://github.com/aastroza/aastroza.github.io/blob/main/docs/github/introduccion.png?raw=true" alt="portada" width="600"/>

## Resumen

El curso es una intensiva sesión de trabajo diseñada para transformar la manera en que los estudiantes abordan la Ciencia de Datos: pasando de proyectos solitarios en Jupyter Notebook a un enfoque más colaborativo y práctico, listo para integrarse en entornos de software reales.

Se comienza con una introducción rápida a la Ciencia de Datos, enfatizando la importancia de estructuras de proyectos estandarizadas. Se explorará cómo Jupyter puede ser la puerta de entrada para análisis complejos, experimentación y desarrollo de productos de datos. 

Luego se aborda cómo estructurar proyectos de Ciencia de Datos con metodologías estandarizadas como Cookiecutter para asegurar que sean mantenibles, replicables y escalables, adecuados para colaboración y uso en entornos de software real. No sólo se pondrá foco en el código, sino también en como trabajar con datos y modelos de machine learning.

A continuación, se exploran las tecnologías Git/GitHub, herramientas cruciales para el trabajo colaborativo. Los estudiantes aprenden sobre control de versiones (crear, clonar, commit, push, pull, branches), colaboración efectiva y la automatización de flujos de trabajo (github actions).

También se introducen temas clave para generar proyectos estructurados y listos para ser compartidos o desplegados, tales como entornos virtuales, devops, integración continua, colaboración open source, templates y contenedores, con el objetivo de establecer un camino de aprendizaje sugerido para el futuro.

## Requisitos

* Conocimiento básico de [Python](https://realpython.com/tutorials/basics/).
* Instalación funcional del software [Anaconda](https://www.anaconda.com/download).
* Una cuenta de [GitHub](https://github.com/).

## Material

* [Github Repositories List](https://github.com/stars/aastroza/lists/curso-navegar-jupyter-y-github)
* [Template: Introduccion a Github](https://github.com/aastroza/introduccion-a-github)
* [Template: IDS Cookiecutter](https://github.com/aastroza/cookiecutter-ids)
* [Hands-On ML](https://github.com/aastroza/handson-ml3-cookiecutter)

## Introduccion

<iframe width="560" height="315" src="https://www.youtube.com/embed/pBy1zgt0XPc?si=TDJQufznmZ8EQ48R" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

## Profesor

* Subdirector de Alianzas con la Industria @  [Instituto de Ciencia de Datos, Universidad del Desarrollo](https://ingenieria.udd.cl/persona/alonso-astroza-tagle/).
* Consultor Independiente: [GeoVictoria](https://www.geovictoria.com) - [Defontana](https://www.defontana.com) - [Discolab](https://www.discolab.cl) - [Subconscious.ai](https://www.subconscious.ai/).
* Profesor en el [Magíster de Data Science @ Universidad del Desarrollo](https://ingenieria.udd.cl/postgrado/magister-en-data-science/profesores/).
* Ingeniero Eléctrico @ Universidad de Chile.

<img src="https://github.com/aastroza/aastroza.github.io/blob/main/docs/github/companies.PNG?raw=true" alt="companies" width="600"/>

## Ciencia de Datos


<img src="https://github.com/aastroza/aastroza.github.io/blob/main/docs/github/piramidePNG.PNG?raw=true" alt="piramide" width="600"/>

*[The AI Hierarchy of Needs (Mónica Rogati, Hackernoon)​](https://hackernoon.com/the-ai-hierarchy-of-needs-18f111fcc007)*

> La triste realidad es que la mayoría de los proyectos de IA fracasan. Según una investigación de Gartner, solo el 15% de las soluciones de IA implementadas para 2022 serán exitosas, y serán muchas menos las que crearán un valor positivo en términos de ROI.

*[Why most AI implementations fail, and what enterprises can do to beat the odds​.](https://venturebeat.com/ai/why-most-ai-implementations-fail-and-what-enterprises-can-do-to-beat-the-odds/)*

<img src="https://github.com/aastroza/aastroza.github.io/blob/main/docs/github/mlops.PNG?raw=true" alt="mlops" width="600"/>

*[MLOps: Why you Might Want to use Machine Learning](https://ml-ops.org/content/motivation)*

## Necesidad de 

## Por qué es necesario esta metodología

## Git/Github

<img src="https://github.com/aastroza/aastroza.github.io/blob/main/docs/github/repos.PNG?raw=true" alt="mlops" width="600"/>

*[Norman Perrin, Introducción a Git y Github](https://github.com/NormanPerrin/introduccion-a-git-y-github)*

<img src="https://github.com/aastroza/aastroza.github.io/blob/main/docs/github/git.PNG?raw=true" alt="mlops" width="600"/>

*[Understanding the GitHub flow](https://docs.github.com/en/get-started/quickstart/github-flow)*

Algunos tips de [Git for Data Science](https://valohai.com/blog/git-for-data-science/):

### No agregues los datasets

Git es un sistema de control de versiones diseñado para servir a los desarrolladores de software. Cuenta con excelentes herramientas para manejar el código fuente y otros contenidos relacionados como configuración, dependencias, documentación. No está pensado para datos de entrenamiento. Punto. Git es solo para código.

En el desarrollo de software, el código es rey y todo lo demás sirve al código. En la ciencia de datos, esto ya no es el caso y existe una dualidad entre datos y código. No tiene sentido que el código dependa de los datos tanto como no tiene sentido que los datos dependan del código. Deben estar desacoplados y aquí es donde el modelo de desarrollo de software centrado en el código te falla. Git no debería ser el punto central de verdad para un proyecto de ciencia de datos.

Hay extensiones como LFS que se refieren a conjuntos de datos externos desde un repositorio git. Aunque cumplen un propósito y resuelven algunos de los límites técnicos (tamaño, velocidad), no resuelven el problema central de una mentalidad de desarrollo de software centrada en el código arraigada en git.

Siempre tendrás conjuntos de datos flotando en tu directorio local, sin embargo. Es bastante fácil agregarlos accidentalmente al escenario y hacer un commit de ellos si no tienes cuidado. La forma correcta de asegurarte de que no necesitas preocuparte por los conjuntos de datos con git es usar el archivo de configuración .gitignore. Agrega tus conjuntos de datos o la carpeta de datos a la configuración y no mires atrás.

Ejemplo:

```
# ignore archives
*.zip
*.tar
*.tar.gz
*.rar

# ignore dataset folder and subfolders
data/
```

### No agregues tus passwords/keys

Esto debería ser obvio, pero los constantes errores en el mundo real nos demuestran que no lo es. No importa si el repositorio es privado. En ninguna circunstancia se debe hacer un commit de ningún nombre de usuario, contraseña, token de API, código clave, certificados TLS, o cualquier otro dato sensible en git.

Incluso los repositorios privados son accesibles por múltiples cuentas y también se clonan en múltiples máquinas locales. Esto le da al hipotético atacante exponencialmente más objetivos. Recuerda que los repositorios privados también pueden volverse públicos en algún momento.

Desacopla tus secretos de tu código y pásalos usando el entorno en su lugar. Para Python, puedes usar el común archivo .env, que contiene las variables de entorno, y el archivo .gitignore, que asegura que el archivo .env no se envíe al repositorio remoto de git. Es una buena idea también proporcionar el .env.template para que otros sepan qué tipo de variables de entorno espera el sistema.

**.env:**

`API_TOKEN=98789fsda789a89sdafsa9f87sda98f7sda89f7`

**.env.template:**

`API_TOKEN=`

**.gitignore:**

```
.env
```

**hello.py:**

```python
from dotenv import load_dotenv
load_dotenv()
api_token = os.getenv('API_TOKEN')
```

Esto todavía requiere algo de copiar y pegar manualmente para cualquiera que clone el repositorio por primera vez. Para una configuración más avanzada, hay herramientas encriptadas y con acceso restringido que pueden compartir secretos a través del entorno, como Doppler

!!! note

    Si ya has enviado tus secretos al repositorio remoto, no intentes arreglar la situación simplemente borrándolos. Es demasiado tarde ya que git está diseñado para ser inmutable. Una vez que el gato está fuera de la bolsa, la única estrategia válida es cambiar las contraseñas o desactivar los tokens.

### Realiza commits pequeños con descripciones claras

### No le tengas miedo a las ramas y pull requests

### [Opcional] No agregues los outputs de los Jupyter Notebooks

## Cookiecutter

## Los futuros destinos de este viaje

### Data Drift / Concepto Drift

### Devops/MLOps/LLMOps

### Contenedores

### Otras formas de contar esta historia

## Bibliografía

- [Github Skills](https://skills.github.com/)
- [Cookiecutter Data Science](https://drivendata.github.io/cookiecutter-data-science/)
- [Git for Data Science](https://valohai.com/blog/git-for-data-science/)
- [Hands-On Machine Learning with Scikit-Learn, Keras & TensorFlow](https://www.oreilly.com/library/view/hands-on-machine-learning/9781098125967/)
