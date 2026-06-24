# Módulo SIMA7670SA - Hardware y PCB 🚀

Este repositorio contiene el diseño completo de la placa de circuito impreso (PCB) desarrollado en **KiCad**, optimizado para el módulo de telemetría GPRS/LTE Cat-1 **SIMA7670SA** y el microcontrolador **STM32F401CCU6** (o STM32F411CCU6).

---

## 📌 Características del Diseño
* **Microcontrolador Central:** STM32F401CCU6 (Soporte pin a pin con STM32F411CCU6).
* **Módulo de Comunicaciones:** SIMCom A7670SA (LTE Cat-1, GSM/GPRS, conectividad optimizada para Sudamérica).
* **Alimentación:** Entrada de voltaje regulada para soportar los picos de corriente del módem (hasta 2A en transmisión).
* **Interfaz de Comunicación:** Líneas UART con adaptación de niveles de voltaje (Level Shifting) entre el STM32 (3.3V) y el A7670SA (1.8V).
* **Periféricos Integrados:** Ranura NanoSIM, conector de antena de red externa, pines de depuración SWD y puertos de expansión GPIO.

---

## 📂 Estructura de Archivos del Proyecto

El repositorio se organiza de la siguiente manera:
* `Gerber Files/` -> Archivos Gerber y de perforación listos para enviar a fabricar (JLCPCB, PCBWay, etc.).
* `PrototipoCasero/` -> Variaciones o esquemas adaptados para pruebas iniciales de taller.
* `Modulo_SIMA7670SA.kicad_sch` -> Diagrama esquemático principal del circuito.
* `Modulo_SIMA7670SA.kicad_pcb` -> Diseño físico y ruteado de la placa.
* `BOM_Modulo_SIMA7670SA.xlsx` -> Lista completa de materiales (Bill of Materials) con referencias de componentes.
* `Esquema eléctrico Modem EYSE v1.pdf` -> Diagrama del circuito exportado en formato PDF para lectura rápida.

---

## 🛠️ Especificaciones Técnicas de Fabricación
Si deseas mandar a producir esta PCB en una casa de fabricación masiva, te sugerimos utilizar la siguiente configuración basada en las reglas de diseño (DRC) aplicadas en KiCad:

| Parámetro | Configuración Sugerida |
| :--- | :--- |
| **Capas (Layers)** | 2 Capas |
| **Grosor de la Placa** | 1.6 mm |
| **Ancho mínimo de pistas** | 0.25 mm (Señales) / 0.8 mm (Líneas de alimentación) |
| **Acabado Superficial** | HASL (with lead) o ENIG (Inmersión en Oro para mejor soldadura del A7670SA) |
| **Color de Máscara** | Verde / Azul / Negro (A elección) |

---

## 💾 Instrucciones para Visualización y Clonado

1. **Clonar este repositorio específico de Hardware:**
   ```bash
   git clone https://github.com
   ```
2. **Abrir el proyecto:** 
   Instalar **KiCad (versión 8.0 o superior)**, abrir el gestor de proyectos y seleccionar el archivo `Modulo_SIMA7670SA.kicad_pro`.

---

## 🔗 Proyectos Relacionados
* **Firmware Oficial:** El código fuente en C desarrollado en STM32CubeIDE para el control de este hardware (UDP, SMS, RTC, comandos AT) se encuentra en el repositorio independiente: **[STM32_SIMA7670SA_Firmware](https://github.com)**.

---

## 👥 Desarrollado por
* **Damian Granzella** - *Ingeniería de Hardware* - [edgranzella](https://github.com)
