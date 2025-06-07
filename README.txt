# 🎲 Sistema de puntuación para juegos de mesa

Proyecto personal para llevar el registro de partidas jugadas con amigos, calcular rankings y visualizar estadísticas de desempeño. El sistema está diseñado para escalar desde una solución rápida con Google Forms y Sheets hasta una aplicación web o tablero profesional en Power BI.

---

## 📅 ¿Qué resuelve?

- Registro de partidas jugadas con:  
  - Fecha (ej. "26/05/25")  
  - Jornada (ej. "Fecha 1")  
  - Juego (ej. "7 Wonders", "Bunny Kingdom")  
  - Posiciones finales de cada jugador  

- Dos sistemas de puntuación:  
  - **Sistema A**: 1 punto para el ganador, 0 para el resto.  
  - **Sistema B**: 4 puntos al 1°, 2 al 2°, 1 al 3°, 0 al 4°. Empates promedian el puntaje.

---

## 🧠 Lógica del sistema de puntuación

### Sistema A - "Gana todo"
- Solo se suma 1 punto al ganador. Todos los demás reciben 0.
- En caso de empate en el primer lugar, cada uno recibe 1 punto.

### Sistema B - "Escalonado"
- Reparto estándar:  
  - 1°: 4 pts  
  - 2°: 2 pts  
  - 3°: 1 pt  
  - 4°: 0 pts

- **Empates**:  
  - Si hay empate entre dos jugadores, se promedian los puntos de las posiciones empatadas.  
  - Ejemplo:  
    - 1° Bruno, Mau (empate) → (4 + 2)/2 = 3 puntos cada uno  
    - Luego: 3° Leo → 1 punto, 4° Panchi → 0 puntos

---

## 🛠 Tecnologías usadas

- Google Sheets
- Google Forms
- Power BI (para visualizaciones)
- Git + GitHub (para documentación y versión del proyecto)
- (Futuro) HTML/CSS/JavaScript para una app web

---

## 📊 Visualizaciones previstas

- Ranking general por jugador
- Ranking por juego
- Evolución de puntajes a lo largo de las jornadas
- Partidas ganadas y puntos acumulados
- Filtros por fecha, jugador y juego

---

## 📁 Estructura del proyecto

