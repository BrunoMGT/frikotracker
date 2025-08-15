# Frikotracker
Registro y análisis de resusltados de partidas de juegos de mesa entre amigos.

## Objetivo
Registrar resultados de las partidas y generar un tablero de posiciones actualizado y un contador de victorias.

## Funcionalidades actuales
- Carga de datos mediante un Google Forms conectado a un Google Sheets, los datos registrados son:
    - Jornada (número)
    - Fecha (de la jornada)
    - Juego
    - Posición de cada jugador.
        ![Datos registrados hasta jornada 5](/images/Master - Jor5.png)
- Conteo de victorias por jugador.
- Cálculo de puntos, por jugador, segun el sistema mencionado en las **notas de desarrollo**.
    ![Puntos y victorias hasta jornada 5](/images/Master 2 - Jor5.png)
- Visualización de una tabla de resultados sencilla en Google Sheets.
    ![Tablero hasta jornada 5](/images/Tablero de pos. - Jor5.png)

## Herramientas
- Google Forms (subida de datos)
- Google Sheets (base de datos y visualizacion simple)

## Estructura
- 'data/raw': datos originales de Google Sheets
- 'data/processed': datos limpios para un analisis completo
- 'notebooks': documentación del proceso
- 'images': campturas de dashboard y gráficas

## Fuente de datos
Datos privados recopilados a través de Google Forms.

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

## Próximos pasos
- Limpieza de datos para posterior análisis en Power BI
- Dashboard interactivo en Power BI