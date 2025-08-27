# Ruta de Desarrollo - Mario Remix (Versión Simple)

## Objetivo
Desarrollar una versión simplificada pero funcional de Mario Remix utilizando tecnologías web básicas.

## Fases de Desarrollo

### Fase 1: Configuración Inicial (1 semana)
- [x] Crear repositorio del proyecto
- [ ] Configurar entorno básico
  - HTML5 Canvas para el juego
  - Archivos JavaScript básicos
  - CSS para estilos simples
  - Estructura de carpetas del proyecto

### Fase 2: Mecánicas Básicas (2 semanas)
1. Implementación del personaje
   - Dibujo básico del personaje (rectángulo/sprite simple)
   - Movimiento izquierda/derecha
   - Salto básico
   - Gravedad simple

2. Creación del nivel básico
   - Plataformas simples (rectángulos)
   - Detección de colisiones básica
   - Fondo estático

### Fase 3: Elementos del Juego (2 semanas)
1. Elementos básicos
   - Monedas simples para recolectar
   - Obstáculos básicos
   - Enemigos simples (movimiento horizontal)

2. Sistema de juego básico
   - Contador de puntos
   - Vidas (3 intentos)
   - Pantalla de inicio y fin

### Fase 4: Mejoras y Pulido (1 semana)
1. Mejoras visuales simples
   - Sprites básicos
   - Colores definidos
   - Mensajes al jugador

2. Audio básico
   - Efecto de salto
   - Efecto de moneda
   - Música de fondo simple

## Tecnologías a Utilizar
- HTML5
- JavaScript vanilla (sin frameworks complejos)
- CSS básico
- Canvas para el renderizado
- Sprites simples (imágenes PNG)
- Arduino Esplora
- Comunicación Serial Web (Web Serial API)

## Integración con Arduino Esplora
1. Configuración del Hardware
   - Programación básica del Arduino Esplora
   - Configuración de la cruz direccional
   - Configuración de los 4 switches
   - Lectura de entradas digitales

2. Comunicación Web-Arduino
   - Implementación de Web Serial API
   - Protocolo de comunicación simple
   - Mapeo de controles:
     * Cruz direccional: Movimiento izquierda/derecha
     * Switch 1: Salto
     * Switch 2: Agacharse
     * Switch 3: Correr
     * Switch 4: Pausa

3. Características del Control
   - Respuesta inmediata a las pulsaciones
   - Detección de múltiples botones simultáneos
   - Estado de pausa

## Estructura de Archivos
```
mario-remix/
│
├── index.html
├── css/
│   └── styles.css
├── js/
│   ├── game.js
│   ├── player.js
│   ├── levels.js
│   └── arduino-controller.js
├── arduino/
│   └── mario_controller.ino
├── assets/
│   ├── images/
│   └── sounds/
└── README.md
```

## Funcionalidades Mínimas
1. Movimiento del personaje (izquierda, derecha, salto)
2. Plataformas para saltar
3. Colección de monedas
4. Sistema de puntuación
5. Condición de victoria/derrota

## Controles
### Controles Arduino Esplora
- Cruz direccional: Mover izquierda/derecha
- Switch 1: Saltar
- Switch 2: Agacharse
- Switch 3: Correr
- Switch 4: Pausar juego

## Siguientes Pasos
1. Crear estructura básica de archivos
2. Implementar el canvas y el loop principal del juego
3. Agregar movimiento básico del personaje
4. Desarrollar sistema de colisiones simple

## Notas Técnicas
- Usar requestAnimationFrame para el loop del juego
- Mantener la física simple (gravedad básica)
- Utilizar objetos JavaScript simples para la lógica del juego
- Priorizar la funcionalidad sobre la estética en esta primera versión
