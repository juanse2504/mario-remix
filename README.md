# mario-remix
el super mario word con arduino esplora

---

# 📄 Product Requirements Document (PRD)

### Proyecto: **Mario Remix Controls**

**Plataforma:** Arduino Esplora + Emulador SNES

---

## Visión General
![Boceto](boceto.jpeg)

**Mario Remix Controls** es un sistema de control alternativo que reemplaza el mando clásico de *Super Mario World* por los sensores integrados en el **Arduino Esplora**. Su objetivo es ofrecer una experiencia de juego innovadora y experimental al usar entradas físicas poco convencionales como el potenciómetro y el sensor de luz.

---

## Controles y Entradas

* **Botón físico del Esplora (switch):** Salto (tecla A).
* **Potenciómetro deslizable:** Movimiento horizontal (izquierda/derecha).
* **Sensor de luz (LDR):** Acción de correr/disparar (tecla Y).
* *(Opcional)* Joystick analógico → control adicional para versiones futuras.

---

## Requerimientos del Prototipo

* **Hardware:**

  * Arduino Esplora.
  * Cable USB para conexión a PC.
* **Software:**

  * Sketch en Arduino IDE con librerías `Esplora.h` y `Keyboard.h`.
  * Emulador de SNES (ZSNES, Snes9x, RetroArch).
* **Compatibilidad:**

  * El Esplora debe ser reconocido como teclado USB.

---

## Mecánica del Juego

* **Switch → Salto:** Mario brinca sobre obstáculos o enemigos.
* **Potenciómetro → Movimiento:** regula dirección izquierda/derecha.
* **Sensor de luz → Correr/Disparar:** activa velocidad extra o lanza bolas de fuego.
* El control responde con baja latencia (<100 ms), garantizando jugabilidad fluida.

---

## Forma de Juego y Diagrama

El jugador interactúa con los sensores del Esplora, que envían señales como teclas al emulador. Esto reemplaza los controles originales del mando SNES.

**Diagrama simplificado:**

```
 [Botón Esplora] ----\
                      \
 [Potenciómetro] -------> [Arduino Esplora] --> [USB] --> [PC/Emulador SNES] --> [Super Mario World]
                      /
     [Sensor de luz]-/
```

---


