# Tres en Raya vs IA - TensorFlow.js

## 🌐 Demo en Vivo
Puedes ver el sitio funcionando en tiempo real [aquí][(TU_ENLACE_DE_GITHUB_PAGES](https://ramirorn.github.io/tres-en-raya-seminario/))
Este proyecto es una implementación interactiva del clásico juego del Tres en Raya (Tic-Tac-Toe), donde un jugador humano se enfrenta a un modelo de inteligencia artificial pre-entrenado utilizando TensorFlow.js en el navegador.

## Información Académica
- **Asignatura**: Seminario De Actualización II
- **Autor**: Pereyra Roman, Ramiro Nicolás

## Descripción del Proyecto

El objetivo principal del trabajo fue adaptar un proyecto base que contenía únicamente la carga de un modelo neuronal y la evaluación de estados predefinidos, para convertirlo en una aplicación web interactiva y completamente jugable. 

### Características Principales:

1. **Interfaz Gráfica Moderna (UI/UX)**:
   - Se diseñó un tablero interactivo y responsivo utilizando CSS Grid.
   - La interfaz implementa un estilo "Glassmorphism" con un tema oscuro (Dark Mode), tipografía moderna (Inter) y efectos visuales atractivos (brillos, transiciones suaves y sombras).
   
2. **Integración Estricta con TensorFlow.js**:
   - El juego se comunica con el modelo pre-entrenado (`model/ttt_model.json`) utilizando exclusivamente los métodos base indicados para la evaluación neuronal: `tf.loadLayersModel`, `tf.tidy`, `tf.tensor` y `model.predict`.
   - Se maneja de forma eficiente la memoria de los tensores generados durante el juego gracias a la función `tf.tidy()`.

3. **Historial de Probabilidades de la IA**:
   - Al finalizar cada partida (ya sea por victoria, derrota o empate), el sistema despliega un historial detallado de los movimientos realizados por la Inteligencia Artificial.
   - Este historial muestra un mini-tablero de 3x3 por cada turno, visualizando las probabilidades matemáticas (con 3 decimales) que el modelo asignó a cada una de las 9 casillas posibles antes de tomar su decisión final. La jugada que la IA finalmente seleccionó aparece resaltada.

## Tecnologías Utilizadas

- **HTML5 & CSS3**: Estructuración y estilización moderna usando variables CSS, Flexbox, Grid, gradientes y pseudo-elementos.
- **Vanilla JavaScript**: Lógica central del juego, detección algorítmica de victorias/empates y manipulación dinámica del DOM sin depender de frameworks adicionales.
- **TensorFlow.js**: Carga e inferencia del modelo de Machine Learning de manera nativa en el navegador web del usuario.

## Cómo Ejecutar el Proyecto

1. Clona o descarga este repositorio en tu máquina local.
2. Dado que el proyecto carga los archivos del modelo neuronal (`.json` y `.bin`) de manera asíncrona, es necesario servir el directorio a través de un servidor web local por políticas de CORS. (Ejemplos: *Live Server* en VSCode, `python -m http.server`, o `npx serve`).
3. Abre el archivo `index.html` desde la URL proporcionada por tu servidor local (por ejemplo: `http://localhost:5500` o `http://localhost:8000`).
4. ¡Empieza a jugar seleccionando una casilla vacía! (El jugador humano inicia siempre como "X" y la IA responde como "O").
