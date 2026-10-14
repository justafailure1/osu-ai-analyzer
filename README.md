<p align="center">
  <img src="assets/banner.png" alt="osu! AI Analyzer, tu entrenador personal de osu!" width="100%">
</p>

<p align="center">
  <a href="https://github.com/justafailure1/osu-ai-analyzer/releases/latest"><img src="https://img.shields.io/github/v/release/justafailure1/osu-ai-analyzer?label=versi%C3%B3n&color=ff66aa&style=for-the-badge" alt="Versión"></a>
  <img src="https://img.shields.io/badge/Windows-10%20%7C%2011-7c4dff?style=for-the-badge&logo=windows&logoColor=white" alt="Windows 10 y 11">
  <img src="https://img.shields.io/badge/osu!-stable-ff66aa?style=for-the-badge" alt="osu! stable">
  <img src="https://img.shields.io/badge/estado-beta%20cerrada-e2489f?style=for-the-badge" alt="Beta cerrada">
</p>

<p align="center">
  <b>Español</b> · <a href="README.en.md">English</a>
</p>

---

**osu! AI Analyzer** tiene una IA que aprende **solo de tus partidas**, nota por nota. Antes de jugar un mapa te dice cuántos misses espera de ti y en qué partes. Después de jugarlo te muestra dónde fallaste más o menos de lo esperado y por qué. Con eso elige qué entrenar y con qué mapas.

<p align="center">
  <img src="assets/live.png" alt="En vivo: lo que tu IA espera de ti en el mapa seleccionado" width="92%">
</p>

## Qué hace

### Tu IA antes de jugar
Al seleccionar un mapa en osu!, la app te dice cuántos misses espera tu IA, en qué segundos del mapa y por qué (el salto, el ritmo, el stream, el cansancio...). También te dice si el mapa te queda cómodo, en tu límite o muy por encima de lo que sueles terminar.

### Cada partida, contra lo que se esperaba de ti
En **Partidas** está cada mapa que jugaste, también los fails, con:
- lo esperado contra lo real, nota por nota;
- la replay dentro de la app, con el cursor, las teclas y los misses marcados;
- los misses que no se esperaban (concentración o cansancio);
- dónde haces clic en los saltos: si te quedas corto o te pasas, y tu timing.

<p align="center">
  <img src="assets/replay.png" alt="Visor de replays" width="80%">
</p>

### Tus habilidades, medidas por tu propia IA
Velocidad de streams, resistencia, velocidad y alcance de salto y precisión (UR), medidos con patrones de prueba en tu forma y con tus ajustes habituales. También ves tu progreso por habilidad semana a semana.

<p align="center">
  <img src="assets/skills.png" alt="Habilidades" width="80%">
</p>

### Qué entrenar hoy
La app elige la habilidad que más te cuesta (o eliges tú entre 10: saltos, flow aim, streams, resistencia, velocidad, tech, sliders, lectura, círculos chicos y precisión) y te propone:
- **mapas de tu carpeta** que más te enseñan de esa habilidad por minuto y que puedes terminar, para los mods que elijas (NM, HD, HR, DT...); un clic los abre en osu!;
- **un mapa hecho para ti**, con el patrón que más te cuesta y la dificultad subiendo hasta tu límite.

<p align="center">
  <img src="assets/train.png" alt="Entrenar" width="80%">
</p>

### Overlays para stream
Además de los overlays de tosu, la app instala los suyos en el panel de tosu, cada uno con su enlace para OBS: mapa y tiempo, PP, teclas, 100/50/miss, combo y precisión, barra de hit error con UR, y lo que tu IA espera en el mapa.

<p align="center">
  <img src="assets/ov-full.png" alt="Overlay completo" width="46%">
  <img src="assets/ov-map.png" alt="Overlay del mapa" width="40%">
</p>

### Y además
- 13 idiomas: español, inglés, portugués, francés, alemán, ruso, polaco, turco, indonesio, japonés, coreano y chino (simplificado y tradicional).
- Leaderboard global y de tu país del mapa seleccionado, con PP en vivo.
- Se actualiza sola cuando sale una versión nueva.

## Liviana mientras juegas
El trabajo pesado (leer replays, entrenar la IA, puntuar tu carpeta) **se pausa mientras juegas** un mapa, corre con prioridad baja y usa como máximo 2 núcleos. En reposo casi no usa CPU.

## Privacidad
- Tus replays y tus datos **se quedan en tu PC**. La IA se entrena en tu propio equipo, solo con tus partidas.
- La app **no modifica osu!** ni juega por ti: lee los datos del juego con [tosu](https://github.com/tosuapp/tosu) (el mismo lector que usan los overlays de stream) y las replays que osu! ya guarda.
- Solo se conecta a internet para pedir a la API de osu! los leaderboards y los mapas, para comprobar tu licencia y para buscar actualizaciones.

## Instalar

> **Beta cerrada:** la app necesita una licencia ligada a tu cuenta de osu!. Si quieres probarla, escríbele a **[Kenzo R en osu!](https://osu.ppy.sh/users/10338561)**.

1. Descarga **`osu-AI-Analyzer-Setup-x.y.z.exe`** desde [**Releases**](https://github.com/justafailure1/osu-ai-analyzer/releases/latest).
2. Ábrelo. Windows puede mostrar *"Windows protegió su PC"* porque el instalador no está firmado: haz clic en **Más información** y luego en **Ejecutar de todas formas**.
3. Pega tu licencia cuando la app te la pida.
4. Abre osu! con la cuenta de la licencia. La primera vez, la app lee tus replays guardadas y entrena tu IA (unos 2 minutos).

**Requisitos:** Windows 10 u 11 (64 bits), osu! stable y 1 GB de espacio libre.

## Preguntas frecuentes

<details>
<summary><b>¿Funciona con osu!lazer?</b></summary>
Está pensada para osu! stable. El soporte de osu!lazer está en pruebas.
</details>

<details>
<summary><b>¿Cuánto tarda en conocerme la IA?</b></summary>
Las replays que ya tienes en osu! cuentan desde el primer día: con unas 200 partidas tarda un par de minutos en entrenarse. Después se vuelve a entrenar sola cada 10 partidas.
</details>

<details>
<summary><b>¿Y los fails? osu! no guarda replay de ellos.</b></summary>
La app graba tus intentos mientras juegas: los fails, los retries y los mapas que dejas a medias también cuentan para tu IA, y puedes ver la replay de cada fail.
</details>

<details>
<summary><b>¿Por qué no aparece el leaderboard de mi país?</b></summary>
osu! solo entrega leaderboards por país a cuentas con osu!supporter.
</details>

<details>
<summary><b>¿Pierdo mis datos si reinstalo o actualizo?</b></summary>
No. Desinstalar o actualizar conserva tus partidas, tu IA y tu licencia.
</details>

---

<p align="center">
  <img src="assets/logo.png" width="56" alt=""><br>
  <sub>osu! AI Analyzer no está afiliado a osu! ni a ppy Pty Ltd. · Software propietario, todos los derechos reservados.<br>
  Usa componentes de terceros bajo sus propias licencias (incluye tosu y lazer-calculator, LGPL-3.0); el detalle va en la carpeta <code>licencias</code> de la instalación.</sub>
</p>
