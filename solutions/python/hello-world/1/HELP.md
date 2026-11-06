# Help

## Ejecutar las pruebas

Usamos [pytest][pytest: Getting Started Guide] como ejecutor de pruebas de nuestro sitio web.
Tendrás que instalar `pytest` en tu máquina de desarrollo si quieres ejecutar las pruebas del track de Python en local.
También deberías instalar los siguientes plugins de `pytest`:

- [pytest-cache][pytest-cache]
- [pytest-subtests][pytest-subtests]

Encontrarás información ampliada en la [guía de pruebas de Python][Python track tests page] de nuestro sitio web.


### Ejecutar las pruebas

Para ejecutar las pruebas incluidas, ve a la carpeta donde está guardado el ejercicio con `cd` en tu terminal (_sustituye `<exercise-folder-location>` de abajo por tu ruta_).
Los archivos de prueba normalmente terminan en `_test.py` y son las mismas pruebas que se ejecutan en el sitio web cuando se sube una solución.

Linux/MacOS
```bash
$ cd <path/to/exercise-folder-location>
```

Windows
```powershell
PS C:\Users\foobar> cd <path\to\exercise-folder-location>
```

<br>

A continuación, ejecuta el comando `pytest` en tu terminal, sustituyendo `<exercise_test.py>` por el nombre del archivo de prueba:

Linux/MacOS
```bash
$ python3 -m pytest -o markers=task <exercise_test.py>
==================== 7 passed in 0.08s ====================
```

Windows
```powershell
PS C:\Users\foobar> py -m pytest -o markers=task <exercise_test.py>
==================== 7 passed in 0.08s ====================
```


### Opciones comunes
- `-o` : anula el `pytest.ini` predeterminado (_puedes usarlo para evitar los avisos de marcadores_)
- `-v` : activa la salida detallada.
- `-x` : detiene la ejecución de las pruebas en el primer fallo.
- `--ff` : ejecuta los fallos de la prueba anterior antes de ejecutar los demás casos de prueba.

Para ver opciones adicionales, usa `python3 -m pytest -h` o `py -m pytest -h`.


### Solucionar los avisos

Si no usas `pytest -o markers=task` al invocar `pytest`, es posible que recibas un `PytestUnknownMarkWarning` en las pruebas que usan nuestra nueva sintaxis:

```bash
PytestUnknownMarkWarning: Unknown pytest.mark.task - is this a typo?  You can register custom marks to avoid this warning - for details, see https://docs.pytest.org/en/stable/mark.html
```

Para no tener que escribir `pytest -o markers=task` en cada prueba que ejecutes, puedes usar un archivo de configuración `pytest.ini`.
Hemos creado uno que puedes descargar desde el nivel superior del directorio del track de Python: [pytest.ini][pytest.ini].

También puedes crear tu propio archivo `pytest.ini` con el siguiente contenido:

```ini
[pytest]
markers =
    task: A concept exercise task.
```

Si colocas el archivo `pytest.ini` en el directorio _raíz_ o _de trabajo_ de tus ejercicios del track de Python, se registrarán los marcadores y se detendrán los avisos.
Puedes encontrar más información sobre los marcadores de pytest en la documentación de `pytest` sobre [cómo marcar funciones de prueba][pytest: marking test functions with attributes] y en la documentación de `pytest` sobre [cómo trabajar con marcadores personalizados][pytest: working with custom markers].

Puedes encontrar información sobre cómo personalizar las configuraciones de pytest en la documentación de `pytest` sobre [formatos de archivo de configuración][pytest: configuration file formats].


### Ampliar tu IDE o editor de código

Muchos IDE y editores de código tienen soporte integrado para usar `pytest` y otras herramientas de calidad del código.
Puedes encontrar algunas opciones creadas por la comunidad en nuestra [página de herramientas del track de Python][Python track tools page].

[Pytest: Getting Started Guide]: https://docs.pytest.org/en/latest/getting-started.html
[Python track tools page]: https://exercism.org/docs/tracks/python/tools
[Python track tests page]: https://exercism.org/docs/tracks/python/tests
[pytest-cache]:http://pythonhosted.org/pytest-cache/
[pytest-subtests]:https://github.com/pytest-dev/pytest-subtests
[pytest.ini]: https://github.com/exercism/python/blob/main/pytest.ini
[pytest: configuration file formats]: https://docs.pytest.org/en/6.2.x/customize.html#configuration-file-formats
[pytest: marking test functions with attributes]: https://docs.pytest.org/en/6.2.x/mark.html#raising-errors-on-unknown-marks
[pytest: working with custom markers]: https://docs.pytest.org/en/6.2.x/example/markers.html#working-with-custom-markers

## Enviar tu solución

Puedes enviar tu solución con el comando `exercism submit hello_world.py`.
Este comando subirá tu solución al sitio web de Exercism e imprimirá la URL de la página de la solución.

Es posible enviar una solución incompleta, lo que te permite:

- Ver cómo otras personas han completado el ejercicio
- Pedir ayuda a un mentor

## ¿Necesitas ayuda?

Si quieres ayuda para resolver el ejercicio, consulta las siguientes páginas:

- La [documentación de la pista Python](https://exercism.org/docs/tracks/python)
- La [categoría de programación de la pista Python en el foro](https://forum.exercism.org/c/programming/python)
- La [categoría de programación de Exercism en el foro](https://forum.exercism.org/c/programming/5)
- Las [preguntas frecuentes](https://exercism.org/docs/using/faqs)

Si esos recursos no te bastan, puedes enviar tu solución (incompleta) para solicitar mentoría.

A continuación tienes algunos recursos para obtener ayuda si te encuentras con algún problema:

- [La PSF](https://www.python.org) aloja las descargas de Python, la documentación y recursos de la comunidad.
- [Foros de la comunidad de Python](https://discuss.python.org/) ayuda, debate de PEP, committers principales de Python y mucho más.
- [La comunidad de Exercism en Discord](https://exercism.org/r/discord)
- [Foros de debate de la comunidad de Exercism](https://forum.exercsim.org)
- [Comunidad de Python en Discord](https://pythondiscord.com/) es una comunidad muy útil y activa.
- [/r/learnpython/](https://www.reddit.com/r/learnpython/) es un subreddit pensado para quienes aprenden Python.
- [#python en Libera.chat](https://www.python.org/community/irc/) aquí es donde los desarrolladores principales del lenguaje se reúnen y trabajan.
- [Foros de la comunidad de Free Code Camp](https://forum.freecodecamp.org/)
- [Pythontutor](http://pythontutor.com/) para recorrer pequeños fragmentos de código de forma visual.

Además, [StackOverflow](http://stackoverflow.com/questions/tagged/python) es un buen lugar para buscar tu problema o pregunta y ver si ya se ha respondido. Si no es así, siempre puedes [preguntar](https://stackoverflow.com/help/how-to-ask) o [responder](https://stackoverflow.com/help/how-to-answer) a la pregunta de otra persona.