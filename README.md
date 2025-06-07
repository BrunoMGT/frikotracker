# FrikoTracker

**FrikoTracker** es una herramienta para registrar, visualizar y analizar el progreso de partidas informales de juegos de mesa entre amigos.


## Objetivo del proyecto

Documentar y profesionalizar el registro de datos de partidas, posiciones y jornadas, con visualizaciones claras y automatizadas.


## Estructura del repositorio

```
frikotracker/
├── data/         ← Exportaciones de datos
├── docs/         ← Capturas, referencias, ideas
├── powerbi/      ← Archivos .pbix y elementos del dashboard
├── scripts/      ← Códigos (JS, Python, Apps Script, etc.)
├── sheets/       ← Planillas o exportaciones (Google Sheets)
├── README.md     ← Este archivo
└── .gitignore    ← Archivos a excluir
```


## Tecnologías utilizadas

- Google Sheets + Forms
- GitHub
- Power BI
- (posiblemente) Python / Apps Script
- (posiblemente) SQL o base de datos futura


## Funcionalidades actuales

- [ ] Registro de partidas desde Formulario
- [ ] Carga automática a Google Sheets
- [ ] Visualización de ranking por jornada, jugador, etc.


## Próximos pasos

- [ ] Exportación de Sheets a Power BI
- [ ] Conectar base de datos externa
- [ ] Publicar versión web (con HTML/CSS o framework)
- [ ] Permitir a otros usar la herramienta


## Notas de desarrollo

- En el formulario se registrarán la fecha y las posiciones de cuatro jugadores fijos. Luego, estos datos se exportarán a una hoja de cálculo (Google Sheets), donde se aplicarán dos sistemas de puntaje diferentes para analizarlos:

    **Sistema A:** 
    Se otorga un (1) punto solo al ganador. Los otros tres jugadores reciben cero (0). Es básicamente un sistema de conteo de victorias.
        
    Resolución de empates: Si dos o mas jugadores empatan en la primer posición, se les da un punto a cada uno.


    **Sistema B:** 
    Se asignan puntos en el orden: 
    - 1º → 4 puntos
    - 2º → 2 puntos
    - 3º → 1 punto
    - 4º → 0 puntos 
        
    Resolución de empates: Si dos o más jugadores empatan en una misma posición, todos ellos reciben los puntos correspondientes a esa posición. Las posiciones siguientes se omiten según la cantidad de empatados.

    Por ejemplo:
    - Entre 1º y 2º         →   4|4|1|0
    - Entre 2º y 3º         →   4|2|2|0
    - Entre 3º y 4º         →   4|2|1|1
    - Doble empate          →   4|4|1|1
    - Entre 1º, 2º y 3º     →   4|4|4|0
    - Entre 2º, 3º y 4º     →   4|2|2|2


## Capturas

...


## Inspiración

Este proyecto nace del deseo de convertir un registro casual entre amigos en una herramienta profesionalizable y visual.
Tambien de mis ganas de entrenar mis habilidades en el uso de las herramientas antes mencionadas.


## Licencia

...