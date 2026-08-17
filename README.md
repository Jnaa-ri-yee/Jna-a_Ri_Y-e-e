<div align="center">

<img src="https://api.iconify.design/mdi:hand-back-right-outline.svg?color=%2300C2FF&height=72" />

# Jña'a Ri Y'ë'ë

### *"La mano que habla"*

**Plataforma de inclusión que reconoce el abecedario de la Lengua de Señas Mexicana (LSM) en tiempo real, directo desde tu cámara — sin internet, sin servidores, 100&nbsp;% en tu teléfono.**

<br/>

[![Web](https://img.shields.io/badge/Web-jnaa--ri--yee.com-4285F4?style=for-the-badge&logo=googlechrome&logoColor=white)](https://www.jnaa-ri-yee.com)
[![Instagram](https://img.shields.io/badge/Instagram-jnaa__ri__yee-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](https://www.instagram.com/jnaa_ri_yee/)
[![Email](https://img.shields.io/badge/Email-jnaariyee@gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:jnaariyee@gmail.com)

[![Platform](https://img.shields.io/badge/Plataforma-Android-3DDC84?style=flat-square&logo=android&logoColor=white)](#)
[![Status](https://img.shields.io/badge/Estado-Beta-orange?style=flat-square)](#)
[![License](https://img.shields.io/badge/Licencia-Uso%20No%20Comercial-lightgrey?style=flat-square)](./LICENSE.md)
[![Offline](https://img.shields.io/badge/Funciona-100%25%20offline-2ea44f?style=flat-square&logo=cloud&logoColor=white)](#)

</div>

<br/>

> Cada seña reconocida correctamente es una barrera menos para alguien que depende de la Lengua de Señas Mexicana para comunicarse.

---

## <img src="https://api.iconify.design/mdi:sparkles-outline.svg?color=%2300C2FF&height=24" valign="middle"/> ¿Qué hace la app?

Apuntas la cámara a tu mano y **Jña'a Ri Y'ë'ë** reconoce, letra por letra, la seña que estás formando en el abecedario de la LSM — todo el procesamiento ocurre **dentro del teléfono**, sin enviar ninguna imagen ni video a internet.

<table>
<tr>
<td width="33%" valign="top" align="center">
<img src="https://api.iconify.design/mdi:camera-outline.svg?color=%2300C2FF&height=40"/><br/>
<b>Traductor en vivo</b><br/>
<sub>Reconocimiento de señas en tiempo real mediante la cámara, con nivel de confianza en pantalla.</sub>
</td>
<td width="33%" valign="top" align="center">
<img src="https://api.iconify.design/mdi:gesture-tap.svg?color=%2300C2FF&height=40"/><br/>
<b>Deletreo manual</b><br/>
<sub>Tú decides cuándo confirmar cada letra y armar tu palabra, sin temporizador.</sub>
</td>
<td width="33%" valign="top" align="center">
<img src="https://api.iconify.design/mdi:volume-high.svg?color=%2300C2FF&height=40"/><br/>
<b>Lectura en voz alta</b><br/>
<sub>Escucha la palabra que acabas de deletrear con un solo toque.</sub>
</td>
</tr>
<tr>
<td width="33%" valign="top" align="center">
<img src="https://api.iconify.design/mdi:school-outline.svg?color=%2300C2FF&height=40"/><br/>
<b>Academia LSM</b><br/>
<sub>Repasa el abecedario completo a tu ritmo, sin conexión a internet.</sub>
</td>
<td width="33%" valign="top" align="center">
<img src="https://api.iconify.design/mdi:shield-lock-outline.svg?color=%2300C2FF&height=40"/><br/>
<b>Privacidad total</b><br/>
<sub>Ninguna imagen sale de tu dispositivo. Nada se sube a un servidor.</sub>
</td>
<td width="33%" valign="top" align="center">
<img src="https://api.iconify.design/mdi:tune-vertical.svg?color=%2300C2FF&height=40"/><br/>
<b>Ajustes finos</b><br/>
<sub>Controla umbrales de detección, aceleración por GPU y más, según tu equipo.</sub>
</td>
</tr>
</table>

---

## <img src="https://api.iconify.design/mdi:cellphone-screenshot.svg?color=%2300C2FF&height=24" valign="middle"/> Pantallas de la app

<div align="center">

| <img src="https://api.iconify.design/mdi:home-variant-outline.svg?height=28"/><br/>**Inicio** | <img src="https://api.iconify.design/mdi:school-outline.svg?height=28"/><br/>**Academia** | <img src="https://api.iconify.design/mdi:camera-outline.svg?height=28"/><br/>**Traductor** | <img src="https://api.iconify.design/mdi:account-group-outline.svg?height=28"/><br/>**Comunidad** | <img src="https://api.iconify.design/mdi:cog-outline.svg?height=28"/><br/>**Ajustes** |
|:---:|:---:|:---:|:---:|:---:|
| Acceso directo al traductor | Lecciones del abecedario LSM | Reconocimiento en tiempo real | Retroalimentación de la comunidad | Modelo, cámara y preferencias |

</div>

---

## <img src="https://api.iconify.design/mdi:brain.svg?color=%2300C2FF&height=24" valign="middle"/> ¿Cómo funciona por dentro?

Cada cuadro de cámara pasa por un pipeline de 4 modelos encadenados, ejecutado localmente en el teléfono:

<div align="center">

`📷 Cámara` → **YOLO-Pose** *(21 puntos clave de la mano)* → **KP-Embedding** + **CNN-Embedding** *(forma y textura)* → **Fusion Gating** *(decide la letra)* → `🔤 Letra + confianza`

</div>

<br/>

<div align="center">

| Métrica | Resultado |
|:---|:---:|
| Accuracy del modelo de fusión | **99.9 %** |
| Velocidad de inferencia | **~30 fps**, local |
| Tamaño del modelo en el dispositivo | **~13.76 MB** |
| Conexión a internet requerida | **Ninguna** |

</div>

---

## <img src="https://api.iconify.design/mdi:layers-triple-outline.svg?color=%2300C2FF&height=24" valign="middle"/> Stack tecnológico

<div align="center">

![Flutter](https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white)
![Dart](https://img.shields.io/badge/Dart-0175C2?style=for-the-badge&logo=dart&logoColor=white)
![TensorFlow Lite](https://img.shields.io/badge/TensorFlow%20Lite-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=black)
![Android](https://img.shields.io/badge/Android-3DDC84?style=for-the-badge&logo=android&logoColor=white)
![Figma](https://img.shields.io/badge/Figma-F24E1E?style=for-the-badge&logo=figma&logoColor=white)

</div>

<div align="center">
<sub>

| Capa | Tecnología |
|---|---|
| 📱 App móvil | Flutter + Dart, un solo código base para Android e iOS |
| 🧠 Detección de mano y puntos clave | YOLO-Pose |
| 🧠 Clasificación de señas | Modelo de fusión (KP-Embedding + CNN-Embedding) exportado a **TensorFlow Lite** |
| 🐍 Entrenamiento de modelos | Python |
| 👁️ Visión por computadora | OpenCV |
| 📦 Distribución de pruebas cerradas | Firebase App Distribution |
| 🎨 Diseño de interfaz | Figma |

</sub>
</div>

---

## <img src="https://api.iconify.design/mdi:flask-outline.svg?color=%2300C2FF&height=24" valign="middle"/> Estado del proyecto

- ✅ Reconocimiento en tiempo real de señas **estáticas** del abecedario (21 letras).
- ✅ Deletreo manual, lectura en voz alta y módulo Academia LSM.
- ✅ Funcionamiento **100&nbsp;% offline**.
- 🚧 En camino: letras con movimiento (**J · K · Ñ · Q · X · Z**), números, saludos, frases y comunidad in-app.

---

## <img src="https://api.iconify.design/mdi:package-variant-closed.svg?color=%2300C2FF&height=24" valign="middle"/> Contenido de este repositorio

Este repositorio contiene únicamente material de difusión — no incluye código fuente, modelos editables ni el dataset:

- 📄 Documento de presentación del proyecto (PDF)
- 📄 Cuadernillo de bienvenida para pruebas cerradas (PDF)
- 📱 Instalador de la aplicación móvil (APK)

Uso personal y no comercial, mensión de creditos obligatorio, sin modificaciones y sin publicación en tiendas de aplicaciones por terceros. Términos completos en [`LICENSE.md`](./LICENSE.md) y [`NOTICE.md`](./NOTICE.md).

---

<div align="center">

### <img src="https://api.iconify.design/mdi:email-fast-outline.svg?color=%2300C2FF&height=22" valign="middle"/> ¿Preguntas, ideas o retroalimentación?

📧 [jnaariyee@gmail.com](mailto:jnaariyee@gmail.com) · 🌐 [www.jnaa-ri-yee.com](https://www.jnaa-ri-yee.com) · 📷 [@jnaa_ri_yee](https://www.instagram.com/jnaa_ri_yee/)

`#HablaConTusManos` · `#JñaaRiYee`

<sub>Copyright © 2026 Equipo Jña'a Ri Y'ë'ë. Todos los derechos reservados.</sub>

</div>
