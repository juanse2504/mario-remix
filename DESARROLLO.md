# Ruta de Desarrollo - Mario Remix (Versión Simple)

## Stack Tecnológico
- HTML5 
- CSS3
- JavaScript (ES6+)
- p5.js para renderizado y lógica de juego
- p5.serialport para comunicación con Arduino

## Integración con Arduino Esplora
1. Lectura de Sensores
   - Acelerómetro (X, Y, Z)
     * X: Control movimiento horizontal (-1023 a 1023)
     * Y: Control de velocidad
     * Z: No utilizado
   - Cruz direccional (alternativa al acelerómetro)
     * LEFT: Movimiento izquierda
     * RIGHT: Movimiento derecha
   - Sensor de luz (control ambiental)
   - Temperatura (efectos visuales)
   - Slider (control de volumen)
   - Micrófono (efectos especiales)
   - 4 switches (acciones del personaje)

2. Comunicación Serial
   - Puerto serie: /dev/ttyACM0 (Linux)
   - Velocidad: 9600 baudios
   - Formato de datos: CSV
   - Estructura: `accelX,accelY,accelZ,light,temp,slider,mic,sw1,sw2,sw3,sw4`

// ...existing code...

3. Comunicación Web-Arduino
   - Implementación de p5.serialport para Web
   - Protocolo de comunicación CSV
   - Estructura de datos serial:
     ```text
     accelX,accelY,accelZ,button1,button2,button3,button4
     ```
   - Mapeo de controles desde datos seriales:
     * Acelerómetro X: Movimiento izquierda/derecha (inclinación)
     * Acelerómetro Y: Control de velocidad
     * Switch 1: Salto
     * Switch 2: Agacharse
     * Switch 3: Correr
     * Switch 4: Pausa

   - Rangos de control:
     * Acelerómetro X: -1023 a 1023
       - < -100: Movimiento izquierda
       - > 100: Movimiento derecha
       - Entre -100 y 100: Personaje quieto

## Estructura de Archivos Simplificada
```
mario-remix/
│
├── index.html
├── css/
│   └── styles.css
├── js/
│   ├── game.js
│   ├── player.js
│   └── serial-handler.js
├── assets/
│   ├── images/
│   └── sounds/
└── README.md
```

## Notas Técnicas
- Usar p5.js para el loop del juego y renderizado
- Física simple basada en gravedad básica
- Comunicación serial directa mediante p5.serialport
- Sin necesidad de servidor backend
- Requisitos mínimos:
  * Navegador moderno con soporte WebSerial
  * Drivers Arduino instalados
  * p5.js y p5.serialport

## Ejemplo de Implementación Base
```html
<!-- index.html -->
<!DOCTYPE html>
<html>
<head>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/p5.js/1.4.0/p5.js"></script>
    <script src="path/to/p5.serialport.js"></script>
    <script src="js/serial-handler.js"></script>
    <script src="js/game.js"></script>
    <script src="js/player.js"></script>
</head>
<body>
    <main></main>
</body>
</html>
```

// ...resto del código existente...

