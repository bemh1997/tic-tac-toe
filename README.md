# Juego de Tres en Raya con React

Un clásico juego de Tres en Raya (Tic-Tac-Toe) construido con React, que demuestra conceptos fundamentales de React como la gestión del estado, la composición de componentes y la elevación del estado.

![Captura de pantalla del juego Tres en Raya](https://res.cloudinary.com/dnvln2exo/image/upload/v1745523052/imagen_2025-04-24_133050792_u2hkx7.png)

## Características

- 🎮 Tablero de juego interactivo
- 🕹️ Seguimiento de turnos de jugadores ("X" o "O")
- 🏆 Detección del ganador
- ⏪ Viaje en el tiempo: Volver a cualquier movimiento anterior
- 📱 Diseño responsive

## Tecnologías Utilizadas

- React 18
- JavaScript (ES6+)
- CSS para el estilo

## Estructura del Proyecto

```
tic-tac-toe/
├── public/
│   ├── index.html
│   └── favicon.ico
├── src/
│   ├── components/
│   │   ├── Board.jsx
│   │   ├── Square.jsx
│   │   └── CalculateWinner.jsx
│   ├── App.jsx
│   ├── main.jsx
│   └── styles.css
├── package.json
└── README.md
```

## Arquitectura de Componentes

La aplicación está construida utilizando una arquitectura basada en componentes:

- **App**: El componente principal que gestiona el historial del juego y renderiza el tablero
- **Board**: Gestiona el estado actual del tablero y renderiza los componentes Square
- **Square**: Una celda individual en el tablero de juego que puede ser clicada para colocar una "X" o una "O"
- **CalculateWinner**: Una función utilitaria que determina si un jugador ha ganado

## Gestión del Estado

El juego utiliza el hook useState de React para gestionar varias piezas del estado:

- **history**: Un array de estados del tablero, donde cada estado es un array de 9 casillas
- **currentMove**: Realiza un seguimiento del número de movimiento actual para mostrar el estado correcto del tablero
- **xIsNext**: Booleano para determinar de quién es el turno (X o O)

El estado se "eleva" al componente App, permitiendo características como el historial de movimientos y el viaje en el tiempo.

## Cómo Funciona

1. Los jugadores se turnan para hacer clic en las casillas y colocar su marca (X u O)
2. El juego registra cada movimiento en el array de historial
3. Después de cada movimiento, el juego comprueba si hay un ganador
4. Los jugadores pueden volver a cualquier movimiento anterior en el historial del juego

## Primeros Pasos

### Requisitos Previos

- Node.js (v16.0 o posterior recomendado)
- npm o yarn

### Instalación

1. Clona el repositorio:
   ```
   git clone https://github.com/tuusuario/tic-tac-toe.git
   ```

2. Navega al directorio del proyecto:
   ```
   cd tic-tac-toe
   ```

3. Instala las dependencias:
   ```
   npm install
   ```
   o
   ```
   yarn install
   ```

4. Inicia el servidor de desarrollo:
   ```
   npm run dev
   ```
   o
   ```
   yarn dev
   ```

5. Abre tu navegador y visita `http://localhost:5173`

## Conceptos de Aprendizaje

Este proyecto demuestra varios conceptos importantes de React:

- **Composición de Componentes**: División de la interfaz en componentes reutilizables
- **Props**: Paso de datos de componentes padre a componentes hijo
- **Gestión del Estado**: Uso de useState para rastrear el estado de la aplicación
- **Inmutabilidad**: Creación de nuevas copias de datos en lugar de mutar el estado existente
- **Elevación del Estado**: Mover el estado a ancestros comunes para compartirlo entre c