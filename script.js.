/* =========================================================
   NAVEGACIÓN GENERAL (sin recargar la página)
   ========================================================= */
function mostrarSeccion(id) {
  document.querySelectorAll('.pantalla').forEach(p => p.classList.remove('activa'));
  const destino = document.getElementById(id);
  if (destino) destino.classList.add('activa');

  document.body.classList.toggle('dentro', id !== 'portada');

  const menuLista = document.getElementById('menu-lista');
  if (menuLista) menuLista.classList.remove('abierto');

  window.scrollTo({ top: 0, behavior: 'smooth' });
}

function toggleMenu() {
  document.getElementById('menu-lista').classList.toggle('abierto');
}

/* Ver un tema específico dentro de una unidad */
function verTema(unidadKey, temaIndex) {
  const unidad = DATOS_UNIDADES[unidadKey];
  const tema = unidad.temas[temaIndex];
  const cont = document.getElementById('contenido-tema');

  cont.innerHTML = `
    <div class="tema-header">
      <span class="tema-icono-grande">${tema.icono}</span>
      <h2 class="titulo-seccion" style="font-size:1.8rem;">${tema.titulo}</h2>
    </div>

    <div class="bloque-tema">
      <h4>🌱 Introducción</h4>
      <p>${tema.introduccion}</p>
    </div>

    <div class="bloque-tema">
      <h4>📖 Definición</h4>
      <p>${tema.definicion}</p>
    </div>

    <div class="bloque-tema">
      <h4>🔎 Explicación detallada</h4>
      <p>${tema.explicacion}</p>
      <div class="emoji-ilustracion">${tema.imagen}</div>
    </div>

    <div class="bloque-tema">
      <h4>💡 Ejemplos</h4>
      ${tema.ejemplos}
    </div>

    <div class="bloque-tema actividad">
      <h4>✏️ Actividad</h4>
      <p>${tema.actividad}</p>
    </div>

    <div class="bloque-tema ejercicio">
      <h4>🧩 Ejercicio propuesto</h4>
      <p>${tema.ejercicio}</p>
    </div>

    <div class="bloque-tema conclusion">
      <h4>🌷 Conclusión</h4>
      <p>${tema.conclusion}</p>
    </div>

    <div class="botones-tema">
      <button class="btn-volver" onclick="mostrarSeccion('${unidadKey}')">← Volver a la Unidad</button>
      <button class="btn-volver" onclick="mostrarSeccion('inicio')">🏠 Menú principal</button>
    </div>
  `;
  mostrarSeccion('vista-tema');
}

/* =========================================================
   DATOS · UNIDADES Y TEMAS
   ========================================================= */
const DATOS_UNIDADES = {
  unidad1: {
    temas: [
      {
        icono: '🖥️',
        titulo: 'Modelo de Von Neumann y Hardware',
        introduccion: 'Toda computadora moderna, desde un celular hasta un servidor, sigue un mismo esquema básico de funcionamiento propuesto hace más de 70 años.',
        definicion: 'El Modelo de Von Neumann es una arquitectura de computadora que propone almacenar tanto los datos como las instrucciones del programa en la misma memoria, y procesarlos de forma secuencial.',
        explicacion: 'Este modelo se compone de cuatro elementos principales: la Unidad Central de Proceso (CPU), que ejecuta las instrucciones; la Memoria, que guarda datos e instrucciones; las Unidades de Entrada/Salida, que permiten la comunicación con el exterior; y el Bus de datos, que transporta la información entre estos componentes. El hardware es el conjunto de elementos físicos y tangibles de la computadora que hacen posible este modelo.',
        imagen: '🧠💾🖱️',
        ejemplos: `<ul>
          <li>Un teclado envía datos (entrada) que el CPU procesa y muestra en pantalla (salida).</li>
          <li>La memoria RAM guarda temporalmente las instrucciones que la CPU va ejecutando.</li>
          <li>El disco duro almacena de forma permanente programas y archivos.</li>
        </ul>`,
        actividad: 'Dibuja en tu cuaderno el esquema del Modelo de Von Neumann señalando la CPU, la memoria y las unidades de entrada/salida.',
        ejercicio: 'Clasifica los siguientes componentes como entrada, salida o almacenamiento: mouse, impresora, disco SSD, micrófono, monitor.',
        conclusion: 'Comprender el Modelo de Von Neumann permite entender por qué las computadoras procesan la información de forma ordenada y cómo se relacionan sus partes físicas.'
      },
      {
        icono: '🗂️',
        titulo: 'Sistemas Operativos',
        introduccion: 'Sin un sistema operativo, el hardware de una computadora sería inútil para el usuario común, ya que no existiría una forma sencilla de interactuar con él.',
        definicion: 'Un Sistema Operativo (SO) es el software principal que administra los recursos de hardware y software de una computadora, y sirve de intermediario entre el usuario y la máquina.',
        explicacion: 'El sistema operativo gestiona la memoria, los procesos, los dispositivos de entrada/salida y el almacenamiento. Además, ofrece una interfaz (gráfica o de texto) para que el usuario pueda ejecutar programas, gestionar archivos y controlar el equipo sin necesidad de conocer el lenguaje de la máquina.',
        imagen: '🪟🐧🍎',
        ejemplos: `<ul>
          <li>Windows, Linux y macOS son sistemas operativos de escritorio.</li>
          <li>Android e iOS son sistemas operativos para dispositivos móviles.</li>
          <li>El SO permite abrir varios programas a la vez (multitarea).</li>
        </ul>`,
        actividad: 'Investiga qué sistema operativo utiliza tu computadora o celular y anota tres funciones que realiza sin que te des cuenta.',
        ejercicio: 'Menciona tres tareas que realiza el sistema operativo cada vez que enciendes tu computadora.',
        conclusion: 'El sistema operativo es el puente esencial entre el hardware y el usuario, permitiendo que la tecnología sea accesible y funcional.'
      },
      {
        icono: '🔢',
        titulo: 'Sistemas de Numeración y Conversiones',
        introduccion: 'Las computadoras no entienden números como los humanos; internamente todo se representa mediante distintos sistemas de numeración.',
        definicion: 'Un sistema de numeración es un conjunto de símbolos y reglas que permiten representar cantidades. Los más usados en computación son el binario (base 2), octal (base 8), decimal (base 10) y hexadecimal (base 16).',
        explicacion: 'Cada sistema utiliza una cantidad distinta de símbolos: el binario usa 0 y 1; el octal usa del 0 al 7; el decimal del 0 al 9; y el hexadecimal usa del 0 al 9 más las letras A-F. Para convertir entre ellos se utilizan métodos como las divisiones sucesivas (de decimal a otra base) o la multiplicación por potencias (de otra base a decimal).',
        imagen: '0️⃣1️⃣🔟',
        ejemplos: `<ul>
          <li>El número decimal 10 equivale a 1010 en binario.</li>
          <li>El número binario 1111 equivale a 15 en decimal y a F en hexadecimal.</li>
          <li>El número octal 17 equivale a 15 en decimal.</li>
        </ul>`,
        actividad: 'Convierte tu edad (en decimal) a binario, octal y hexadecimal usando el método de divisiones sucesivas.',
        ejercicio: 'Convierte el número decimal 45 a binario, octal y hexadecimal.',
        conclusion: 'Dominar los sistemas de numeración es la base para comprender cómo la computadora almacena y procesa toda la información internamente.'
      },
      {
        icono: '➕',
        titulo: 'Aritmética Binaria',
        introduccion: 'Así como realizamos sumas y restas en el sistema decimal, las computadoras realizan operaciones aritméticas utilizando el sistema binario.',
        definicion: 'La aritmética binaria es el conjunto de operaciones matemáticas (suma, resta, multiplicación y división) realizadas utilizando únicamente los dígitos 0 y 1.',
        explicacion: 'Las reglas básicas de la suma binaria son: 0+0=0, 0+1=1, 1+0=1 y 1+1=10 (se lleva 1). La resta utiliza el concepto de "préstamo" similar al sistema decimal. Estas operaciones son la base del funcionamiento interno de la Unidad Aritmético-Lógica (ALU) del procesador.',
        imagen: '🧮',
        ejemplos: `<ul>
          <li>1011 + 0110 = 10001 en binario.</li>
          <li>101 - 011 = 010 en binario.</li>
          <li>La ALU del procesador usa estas reglas millones de veces por segundo.</li>
        </ul>`,
        actividad: 'Practica sumando dos números binarios de 4 bits que tú elijas, verificando el resultado en decimal.',
        ejercicio: 'Realiza la suma binaria de 1101 + 1011 y comprueba el resultado convirtiendo ambos números a decimal.',
        conclusion: 'La aritmética binaria es el lenguaje matemático fundamental que permite a los procesadores realizar cálculos a gran velocidad.'
      },
      {
        icono: '🔀',
        titulo: 'Álgebra de Boole',
        introduccion: 'Toda decisión lógica que toma una computadora, desde encender un led hasta ejecutar una condición en un programa, se basa en una rama especial de las matemáticas.',
        definicion: 'El Álgebra de Boole es una rama de las matemáticas que trabaja con valores lógicos (verdadero/falso o 1/0) y operadores como AND, OR y NOT para construir expresiones lógicas.',
        explicacion: 'Las compuertas lógicas AND, OR y NOT son la base física de los circuitos digitales. AND retorna verdadero solo si ambas entradas son verdaderas; OR retorna verdadero si al menos una entrada lo es; y NOT invierte el valor de la entrada. Estas operaciones permiten construir desde simples circuitos hasta procesadores completos.',
        imagen: '🔲🔳',
        ejemplos: `<ul>
          <li>1 AND 0 = 0 · 1 AND 1 = 1</li>
          <li>0 OR 1 = 1 · 0 OR 0 = 0</li>
          <li>NOT 1 = 0 · NOT 0 = 1</li>
        </ul>`,
        actividad: 'Construye una tabla de verdad para la expresión (A AND B) OR NOT C.',
        ejercicio: 'Evalúa la expresión lógica: (1 OR 0) AND (NOT 0).',
        conclusion: 'El Álgebra de Boole es el fundamento matemático que hace posible el diseño de circuitos digitales y la lógica de programación.'
      }
    ]
  },
  unidad2: {
    temas: [
      {
        icono: '🧭',
        titulo: 'Algoritmos y sus características',
        introduccion: 'Antes de escribir una sola línea de código, todo programador debe aprender a pensar de forma ordenada y lógica.',
        definicion: 'Un algoritmo es una secuencia finita, ordenada y bien definida de pasos que permite resolver un problema o realizar una tarea específica.',
        explicacion: 'Todo algoritmo debe cumplir ciertas características: ser preciso (indicar claramente el orden de cada paso), finito (tener un número limitado de pasos), definido (producir siempre el mismo resultado con las mismas entradas) y tener entradas y salidas claramente identificadas.',
        imagen: '🧭📋',
        ejemplos: `<ul>
          <li>Una receta de cocina es un algoritmo de la vida cotidiana.</li>
          <li>Los pasos para cambiar un neumático también son un algoritmo.</li>
          <li>En programación, un algoritmo para sumar dos números: leer A, leer B, calcular A+B, mostrar resultado.</li>
        </ul>`,
        actividad: 'Escribe, en tus propias palabras, el algoritmo para preparar tu bebida favorita, numerando cada paso.',
        ejercicio: 'Diseña un algoritmo (en pasos numerados) para determinar si un número ingresado es par o impar.',
        conclusion: 'Los algoritmos son la base del pensamiento computacional: aprender a diseñarlos bien es el primer paso para programar correctamente.'
      },
      {
        icono: '🔷',
        titulo: 'Diagramas de flujo',
        introduccion: 'Los diagramas de flujo permiten visualizar gráficamente la lógica de un algoritmo antes de convertirlo en código.',
        definicion: 'Un diagrama de flujo es una representación gráfica de un algoritmo, que utiliza figuras geométricas estandarizadas para mostrar el orden y tipo de cada instrucción.',
        explicacion: 'Cada figura tiene un significado específico: el óvalo representa inicio o fin, el rectángulo representa un proceso, el rombo representa una decisión, el paralelogramo representa entrada o salida de datos, y las flechas indican el flujo o secuencia entre pasos.',
        imagen: '⬭➡️🔷➡️▭',
        ejemplos: `<ul>
          <li>Diagrama para saber si un número es positivo o negativo, usando un rombo de decisión.</li>
          <li>Diagrama para calcular el promedio de tres notas usando rectángulos de proceso.</li>
        </ul>`,
        actividad: 'Dibuja el diagrama de flujo correspondiente al algoritmo que escribiste sobre pares e impares.',
        ejercicio: 'Elabora el diagrama de flujo para determinar si una persona es mayor de edad, dado su edad como entrada.',
        conclusion: 'Los diagramas de flujo facilitan la comprensión visual de la lógica de un programa antes de escribir el código, reduciendo errores.'
      },
      {
        icono: '📝',
        titulo: 'Pseudocódigo',
        introduccion: 'Entre la idea de un algoritmo y el código real de un lenguaje de programación existe un paso intermedio muy útil.',
        definicion: 'El pseudocódigo es una forma de describir un algoritmo utilizando palabras y estructuras similares a un lenguaje de programación, pero sin la sintaxis estricta de ningún lenguaje en particular.',
        explicacion: 'El pseudocódigo utiliza palabras clave como Inicio, Fin, Leer, Escribir, Si...Entonces, Mientras, Para, que describen las acciones de forma clara y comprensible para cualquier persona, sin importar el lenguaje de programación que use después.',
        imagen: '📝✅',
        ejemplos: `<pre class="codigo">Inicio
  Leer numero
  Si numero % 2 == 0 Entonces
      Escribir "Es par"
  Sino
      Escribir "Es impar"
  FinSi
Fin</pre>`,
        actividad: 'Convierte el diagrama de flujo de mayoría de edad en pseudocódigo, usando las palabras clave vistas en clase.',
        ejercicio: 'Escribe en pseudocódigo un algoritmo que calcule el área de un triángulo dados su base y su altura.',
        conclusion: 'El pseudocódigo es el puente ideal entre la idea de un algoritmo y su implementación real en un lenguaje de programación como Python.'
      }
    ]
  },
  unidad3: {
    temas: [
      {
        icono: '🌐',
        titulo: 'Lenguajes y paradigmas de programación',
        introduccion: 'Existen muchas formas de decirle a una computadora qué hacer, y cada una responde a una filosofía distinta de resolver problemas.',
        definicion: 'Un lenguaje de programación es un conjunto de reglas y símbolos que permite escribir instrucciones que la computadora puede ejecutar. Un paradigma de programación es el enfoque o estilo utilizado para estructurar esas instrucciones.',
        explicacion: 'Entre los principales paradigmas están el estructurado (secuencia de instrucciones paso a paso), el orientado a objetos (organiza el código en clases y objetos) y el funcional (basado en funciones matemáticas puras). Python es un lenguaje multiparadigma, ya que permite programar de forma estructurada, orientada a objetos o funcional.',
        imagen: '🐍💻',
        ejemplos: `<ul>
          <li>C es un lenguaje principalmente estructurado.</li>
          <li>Java es un lenguaje orientado a objetos.</li>
          <li>Python permite combinar varios paradigmas en un mismo programa.</li>
        </ul>`,
        actividad: 'Investiga y menciona dos lenguajes de programación adicionales, indicando a qué paradigma pertenecen.',
        ejercicio: 'Explica con tus propias palabras la diferencia entre el paradigma estructurado y el orientado a objetos.',
        conclusion: 'Conocer los paradigmas de programación ayuda a elegir la mejor forma de estructurar la solución a un problema.'
      },
      {
        icono: '🐍',
        titulo: 'Introducción a Python',
        introduccion: 'Python se ha convertido en uno de los lenguajes más utilizados en el mundo por su sencillez y versatilidad.',
        definicion: 'Python es un lenguaje de programación de alto nivel, interpretado y de sintaxis sencilla, ampliamente usado en desarrollo web, ciencia de datos, inteligencia artificial y automatización.',
        explicacion: 'Una de las principales ventajas de Python es que su sintaxis es muy cercana al lenguaje natural, lo que facilita el aprendizaje de la programación. Además cuenta con una enorme cantidad de librerías que amplían sus funcionalidades.',
        imagen: '🐍✨',
        ejemplos: `<pre class="codigo">print("¡Hola, mundo!")

nombre = "Sandy"
print("Bienvenida", nombre)</pre>`,
        actividad: 'Instala Python en tu computadora (o usa un entorno en línea) y ejecuta el clásico programa "Hola, mundo".',
        ejercicio: 'Escribe un programa en Python que pida tu nombre y edad, y muestre un mensaje de bienvenida personalizado.',
        conclusion: 'Python es una excelente puerta de entrada al mundo de la programación gracias a su claridad y a la enorme comunidad que lo respalda.'
      },
      {
        icono: '➗',
        titulo: 'Operadores algebraicos, relacionales y lógicos',
        introduccion: 'Para que un programa pueda calcular, comparar y tomar decisiones, necesita de operadores que manipulen los datos.',
        definicion: 'Los operadores son símbolos que permiten realizar operaciones sobre uno o más valores. Los algebraicos realizan cálculos matemáticos, los relacionales comparan valores, y los lógicos combinan condiciones.',
        explicacion: 'Los operadores algebraicos incluyen suma (+), resta (-), multiplicación (*), división (/) y módulo (%). Los relacionales incluyen igual (==), diferente (!=), mayor (>), menor (<). Los lógicos incluyen and, or y not, y se usan para combinar condiciones en estructuras de decisión.',
        imagen: '➕➖✖️➗',
        ejemplos: `<pre class="codigo">a = 10
b = 3
print(a % b)          # resultado: 1
print(a > b and b > 0) # resultado: True</pre>`,
        actividad: 'Escribe cinco expresiones en Python usando distintos operadores algebraicos y relacionales, y predice su resultado antes de ejecutarlas.',
        ejercicio: 'Dado a = 15 y b = 4, calcula en Python: a // b, a % b y (a > b) and (b != 0).',
        conclusion: 'Los operadores son las herramientas básicas que permiten a un programa calcular, comparar y tomar decisiones inteligentes.'
      },
      {
        icono: '🔀',
        titulo: 'Estructuras de control condicionales',
        introduccion: 'Los programas rara vez siguen un único camino: normalmente deben decidir qué hacer según ciertas condiciones.',
        definicion: 'Las estructuras condicionales permiten ejecutar distintos bloques de código dependiendo de si una condición se cumple o no.',
        explicacion: 'En Python la estructura principal es if, que puede combinarse con elif (para más condiciones) y else (para el caso contrario). La condición se evalúa como verdadera o falsa, y según el resultado se ejecuta un bloque de código u otro.',
        imagen: '🔀✅❌',
        ejemplos: `<pre class="codigo">edad = 20
if edad >= 18:
    print("Eres mayor de edad")
else:
    print("Eres menor de edad")</pre>`,
        actividad: 'Modifica el ejemplo anterior para que además indique si la persona es adulta mayor (65 años o más).',
        ejercicio: 'Escribe un programa en Python que reciba una nota (0-10) e indique si el estudiante aprobó (>=7), está en recuperación (5-6.9) o reprobó (<5).',
        conclusion: 'Las estructuras condicionales dotan a los programas de la capacidad de tomar decisiones, algo esencial en cualquier aplicación real.'
      },
      {
        icono: '🔁',
        titulo: 'Estructuras de control repetitivas',
        introduccion: 'Muchas tareas requieren repetir una acción varias veces, y hacerlo manualmente sería poco práctico.',
        definicion: 'Las estructuras repetitivas (o bucles) permiten ejecutar un bloque de código varias veces mientras se cumpla una condición o durante un número determinado de repeticiones.',
        explicacion: 'En Python existen principalmente dos tipos de bucles: for, que se usa cuando se conoce el número de repeticiones o se recorre una secuencia; y while, que se repite mientras una condición se mantenga verdadera.',
        imagen: '🔁🔂',
        ejemplos: `<pre class="codigo">for i in range(1, 6):
    print("Número:", i)

contador = 0
while contador < 3:
    print("Repetición", contador)
    contador += 1</pre>`,
        actividad: 'Escribe un programa con un bucle for que muestre la tabla de multiplicar del 5.',
        ejercicio: 'Escribe un programa en Python con un bucle while que sume los números del 1 al 10 y muestre el resultado final.',
        conclusion: 'Las estructuras repetitivas permiten automatizar tareas que se realizan varias veces, ahorrando tiempo y líneas de código.'
      }
    ]
  }
};

/* Genera las tarjetas de cada unidad */
function generarListasUnidades() {
  Object.keys(DATOS_UNIDADES).forEach(unidadKey => {
    const contenedor = document.getElementById(`lista-${unidadKey}`);
    if (!contenedor) return;
    contenedor.innerHTML = DATOS_UNIDADES[unidadKey].temas.map((tema, i) => `
      <button class="tarjeta-tema" onclick="verTema('${unidadKey}', ${i})">
        <span class="tema-icono">${tema.icono}</span>${tema.titulo}
      </button>
    `).join('');
  });
}

/* =========================================================
   JUEGO 1 · CUESTIONARIO
   ========================================================= */
const PREGUNTAS_QUIZ = [
  { pregunta: '¿Qué componente ejecuta las instrucciones en el Modelo de Von Neumann?', opciones: ['La CPU', 'El teclado', 'La impresora', 'El monitor'], correcta: 0 },
  { pregunta: '¿Cuál es el resultado de 1 AND 0 en Álgebra de Boole?', opciones: ['1', '0', '10', 'Indefinido'], correcta: 1 },
  { pregunta: '¿Qué símbolo del diagrama de flujo representa una decisión?', opciones: ['Óvalo', 'Rectángulo', 'Rombo', 'Círculo'], correcta: 2 },
  { pregunta: '¿Qué palabra clave de Python se usa para repetir un bloque un número conocido de veces?', opciones: ['while', 'for', 'if', 'def'], correcta: 1 },
  { pregunta: '¿Cuál es el equivalente en decimal del número binario 1010?', opciones: ['8', '9', '10', '12'], correcta: 2 },
  { pregunta: '¿Qué software administra los recursos de hardware de una computadora?', opciones: ['El sistema operativo', 'El navegador', 'El antivirus', 'El procesador de texto'], correcta: 0 },
  { pregunta: '¿Qué estructura permite ejecutar un bloque solo si una condición es verdadera?', opciones: ['Bucle for', 'Estructura condicional', 'Variable', 'Función'], correcta: 1 },
  { pregunta: '¿Qué es un algoritmo?', opciones: ['Un lenguaje de programación', 'Una secuencia ordenada de pasos para resolver un problema', 'Un tipo de computadora', 'Un componente de hardware'], correcta: 1 }
];
let quizIndice = 0, quizPuntaje = 0;
function iniciarQuiz() {
  quizIndice = 0; quizPuntaje = 0;
  mostrarPreguntaQuiz();
}
function mostrarPreguntaQuiz() {
  const cont = document.getElementById('quiz-contenedor');
  if (quizIndice >= PREGUNTAS_QUIZ.length) {
    cont.innerHTML = `
      <div class="quiz-resultado">🌸 Obtuviste ${quizPuntaje} de ${PREGUNTAS_QUIZ.length} 🌸</div>
      <div style="text-align:center;"><button class="btn-rosa" onclick="iniciarQuiz()">Volver a intentar</button></div>
    `;
    return;
  }
  const p = PREGUNTAS_QUIZ[quizIndice];
  cont.innerHTML = `
    <p style="color:var(--texto-suave); font-weight:600;">Pregunta ${quizIndice + 1} de ${PREGUNTAS_QUIZ.length} · Puntaje: ${quizPuntaje}</p>
    <div class="pregunta-quiz">
      <p class="enunciado">${p.pregunta}</p>
      <div class="opciones-quiz">
        ${p.opciones.map((op, i) => `<button class="opcion-quiz" onclick="responderQuiz(${i})">${op}</button>`).join('')}
      </div>
    </div>
  `;
}
function responderQuiz(seleccion) {
  const p = PREGUNTAS_QUIZ[quizIndice];
  const botones = document.querySelectorAll('.opcion-quiz');
  botones.forEach((b, i) => {
    b.disabled = true;
    if (i === p.correcta) b.classList.add('correcta');
    else if (i === seleccion) b.classList.add('incorrecta');
  });
  if (seleccion === p.correcta) quizPuntaje++;
  setTimeout(() => { quizIndice++; mostrarPreguntaQuiz(); }, 900);
}

/* =========================================================
   JUEGO 2 · SOPA DE LETRAS
   ========================================================= */
const PALABRAS_SOPA = ['HARDWARE', 'SOFTWARE', 'PYTHON', 'ALGORITMO', 'VARIABLES', 'BOOLE', 'BINARIO', 'OCTAL', 'HEXADECIMAL', 'CONDICIONAL', 'CICLO', 'OPERADOR'];
const TAMANO_SOPA = 14;
let sopaGrid = [];
let sopaEncontradas = new Set();
let sopaUbicaciones = {}; // palabra -> array de [f,c]

function generarSopa() {
  sopaGrid = Array.from({ length: TAMANO_SOPA }, () => Array(TAMANO_SOPA).fill(''));
  sopaUbicaciones = {};
  sopaEncontradas = new Set();
  const direcciones = [
    [0, 1],  // horizontal derecha
    [1, 0],  // vertical abajo
    [1, 1],  // diagonal abajo-derecha
  ];

  PALABRAS_SOPA.forEach(palabra => {
    let colocada = false;
    let intentos = 0;
    while (!colocada && intentos < 200) {
      intentos++;
      const dir = direcciones[Math.floor(Math.random() * direcciones.length)];
      const maxFila = dir[0] === 1 ? TAMANO_SOPA - palabra.length : TAMANO_SOPA - 1;
      const maxCol = dir[1] === 1 ? TAMANO_SOPA - palabra.length : TAMANO_SOPA - 1;
      const fila = Math.floor(Math.random() * (maxFila + 1));
      const col = Math.floor(Math.random() * (maxCol + 1));

      let cabe = true;
      const celdas = [];
      for (let i = 0; i < palabra.length; i++) {
        const f = fila + dir[0] * i;
        const c = col + dir[1] * i;
        const actual = sopaGrid[f][c];
        if (actual !== '' && actual !== palabra[i]) { cabe = false; break; }
        celdas.push([f, c]);
      }
      if (cabe) {
        celdas.forEach(([f, c], i) => sopaGrid[f][c] = palabra[i]);
        sopaUbicaciones[palabra] = celdas;
        colocada = true;
      }
    }
  });

  // Rellenar espacios vacíos con letras aleatorias
  const letras = 'ABCDEFGHIJKLMNOPQRSTUVWXYZ';
  for (let f = 0; f < TAMANO_SOPA; f++) {
    for (let c = 0; c < TAMANO_SOPA; c++) {
      if (sopaGrid[f][c] === '') sopaGrid[f][c] = letras[Math.floor(Math.random() * letras.length)];
    }
  }
}

let sopaSeleccion = [];
let sopaArrastrando = false;

function renderSopa() {
  const tablero = document.getElementById('sopa-tablero');
  tablero.style.gridTemplateColumns = `repeat(${TAMANO_SOPA}, 30px)`;
  tablero.innerHTML = '';
  for (let f = 0; f < TAMANO_SOPA; f++) {
    for (let c = 0; c < TAMANO_SOPA; c++) {
      const celda = document.createElement('div');
      celda.className = 'sopa-celda';
      celda.textContent = sopaGrid[f][c];
      celda.dataset.f = f; celda.dataset.c = c;
      celda.addEventListener('mousedown', () => { sopaArrastrando = true; sopaSeleccion = [[f, c]]; pintarSeleccion(); });
      celda.addEventListener('mouseenter', () => { if (sopaArrastrando) { agregarSeleccion(f, c); } });
      celda.addEventListener('mouseup', () => { sopaArrastrando = false; validarSeleccionSopa(); });
      celda.addEventListener('touchstart', (e) => { sopaArrastrando = true; sopaSeleccion = [[f, c]]; pintarSeleccion(); }, { passive: true });
      tablero.appendChild(celda);
    }
  }
  document.addEventListener('touchmove', manejarTouchMoveSopa, { passive: true });
  document.addEventListener('touchend', () => { if (sopaArrastrando) { sopaArrastrando = false; validarSeleccionSopa(); } });

  document.getElementById('sopa-total').textContent = PALABRAS_SOPA.length;
  document.getElementById('sopa-contador').textContent = sopaEncontradas.size;

  const listaEl = document.getElementById('sopa-palabras');
  listaEl.innerHTML = '<ul>' + PALABRAS_SOPA.map(p => `<li id="palabra-${p}">${p}</li>`).join('') + '</ul>';
}

function manejarTouchMoveSopa(e) {
  if (!sopaArrastrando) return;
  const touch = e.touches[0];
  const el = document.elementFromPoint(touch.clientX, touch.clientY);
  if (el && el.classList.contains('sopa-celda')) {
    agregarSeleccion(parseInt(el.dataset.f), parseInt(el.dataset.c));
  }
}

function agregarSeleccion(f, c) {
  const inicio = sopaSeleccion[0];
  if (!inicio) return;
  const df = f - inicio[0], dc = c - inicio[1];
  // Solo permitir líneas rectas: horizontal, vertical o diagonal
  let pasos = Math.max(Math.abs(df), Math.abs(dc));
  if (pasos === 0) { sopaSeleccion = [inicio]; pintarSeleccion(); return; }
  const dirF = df === 0 ? 0 : df / Math.abs(df);
  const dirC = dc === 0 ? 0 : dc / Math.abs(dc);
  if (!(df === 0 || dc === 0 || Math.abs(df) === Math.abs(dc))) return;
  const nueva = [];
  for (let i = 0; i <= pasos; i++) nueva.push([inicio[0] + dirF * i, inicio[1] + dirC * i]);
  sopaSeleccion = nueva;
  pintarSeleccion();
}

function pintarSeleccion() {
  document.querySelectorAll('.sopa-celda').forEach(cel => {
    if (!cel.classList.contains('encontrada')) cel.classList.remove('seleccionando');
  });
  sopaSeleccion.forEach(([f, c]) => {
    const cel = document.querySelector(`.sopa-celda[data-f="${f}"][data-c="${c}"]`);
    if (cel && !cel.classList.contains('encontrada')) cel.classList.add('seleccionando');
  });
}

function validarSeleccionSopa() {
  const letrasSeleccion = sopaSeleccion.map(([f, c]) => sopaGrid[f][c]).join('');
  const letrasInvertidas = letrasSeleccion.split('').reverse().join('');

  let palabraEncontrada = PALABRAS_SOPA.find(p => (p === letrasSeleccion || p === letrasInvertidas) && !sopaEncontradas.has(p));

  if (palabraEncontrada) {
    sopaEncontradas.add(palabraEncontrada);
    sopaSeleccion.forEach(([f, c]) => {
      const cel = document.querySelector(`.sopa-celda[data-f="${f}"][data-c="${c}"]`);
      if (cel) { cel.classList.remove('seleccionando'); cel.classList.add('encontrada'); }
    });
    const li = document.getElementById(`palabra-${palabraEncontrada}`);
    if (li) li.classList.add('encontrada');
    document.getElementById('sopa-contador').textContent = sopaEncontradas.size;
  } else {
    document.querySelectorAll('.sopa-celda.seleccionando').forEach(cel => cel.classList.remove('seleccionando'));
  }
  sopaSeleccion = [];
}

function reiniciarSopa() {
  generarSopa();
  renderSopa();
}

/* =========================================================
   JUEGO 3 · VERDADERO O FALSO
   ========================================================= */
const PREGUNTAS_VF = [
  { texto: 'El sistema binario utiliza únicamente los dígitos 0 y 1.', respuesta: true },
  { texto: 'La CPU es la encargada de almacenar permanentemente los archivos del usuario.', respuesta: false },
  { texto: 'Un algoritmo debe ser finito, es decir, tener un número limitado de pasos.', respuesta: true },
  { texto: 'En Python, la palabra clave "while" se usa para repetir un bloque de código.', respuesta: true },
  { texto: 'El operador lógico AND retorna verdadero si al menos una de las condiciones es verdadera.', respuesta: false },
  { texto: 'Un diagrama de flujo usa un rombo para representar una decisión.', respuesta: true },
];
function generarVF() {
  const cont = document.getElementById('vf-contenedor');
  cont.innerHTML = PREGUNTAS_VF.map((p, i) => `
    <div class="vf-item" id="vf-${i}">
      <p>${p.texto}</p>
      <div class="vf-botones">
        <button class="vf-btn v" onclick="responderVF(${i}, true)">Verdadero</button>
        <button class="vf-btn f" onclick="responderVF(${i}, false)">Falso</button>
      </div>
    </div>
  `).join('');
}
function responderVF(indice, seleccion) {
  const item = document.getElementById(`vf-${indice}`);
  const correcto = PREGUNTAS_VF[indice].respuesta === seleccion;
  const botones = item.querySelectorAll('.vf-btn');
  botones.forEach(b => b.disabled = true);
  const boton = seleccion ? botones[0] : botones[1];
  boton.classList.add(correcto ? 'correcto' : 'incorrecto');
}

/* =========================================================
   JUEGO 4 · MEMORIA DE CONCEPTOS
   ========================================================= */
const PARES_MEMORIA = [
  { concepto: 'CPU', definicion: 'Ejecuta las instrucciones del programa' },
  { concepto: 'Algoritmo', definicion: 'Secuencia ordenada de pasos para resolver un problema' },
  { concepto: 'Binario', definicion: 'Sistema numérico basado en 0 y 1' },
  { concepto: 'Python', definicion: 'Lenguaje de programación de alto nivel' },
  { concepto: 'Bucle for', definicion: 'Repite un bloque un número conocido de veces' },
  { concepto: 'AND', definicion: 'Operador lógico verdadero solo si ambas condiciones lo son' },
  { concepto: 'Sistema Operativo', definicion: 'Administra los recursos de hardware y software' },
  { concepto: 'Diagrama de flujo', definicion: 'Representación gráfica de un algoritmo' },
];
let memoriaCartas = [], memoriaVolteadas = [], memoriaBloqueado = false;
let memoriaIntentos = 0, memoriaAciertos = 0;

function iniciarMemoria() {
  memoriaIntentos = 0; memoriaAciertos = 0; memoriaVolteadas = []; memoriaBloqueado = false;
  document.getElementById('memoria-intentos').textContent = 0;
  document.getElementById('memoria-pares').textContent = 0;

  let cartas = [];
  PARES_MEMORIA.forEach((par, i) => {
    cartas.push({ id: i, texto: par.concepto, tipo: 'concepto' });
    cartas.push({ id: i, texto: par.definicion, tipo: 'definicion' });
  });
  // Mezclar
  cartas.sort(() => Math.random() - 0.5);
  memoriaCartas = cartas;

  const tablero = document.getElementById('memoria-tablero');
  tablero.innerHTML = cartas.map((c, idx) => `
    <div class="memoria-carta" data-idx="${idx}" onclick="voltearCarta(${idx})">🌸</div>
  `).join('');
}

function voltearCarta(idx) {
  if (memoriaBloqueado) return;
  const el = document.querySelector(`.memoria-carta[data-idx="${idx}"]`);
  if (el.classList.contains('volteada') || el.classList.contains('acertada')) return;

  el.classList.add('volteada');
  el.textContent = memoriaCartas[idx].texto;
  memoriaVolteadas.push(idx);

  if (memoriaVolteadas.length === 2) {
    memoriaIntentos++;
    document.getElementById('memoria-intentos').textContent = memoriaIntentos;
    const [a, b] = memoriaVolteadas;
    if (memoriaCartas[a].id === memoriaCartas[b].id) {
      document.querySelector(`.memoria-carta[data-idx="${a}"]`).classList.add('acertada');
      document.querySelector(`.memoria-carta[data-idx="${b}"]`).classList.add('acertada');
      memoriaAciertos++;
      document.getElementById('memoria-pares').textContent = memoriaAciertos;
      memoriaVolteadas = [];
    } else {
      memoriaBloqueado = true;
      setTimeout(() => {
        [a, b].forEach(i => {
          const c = document.querySelector(`.memoria-carta[data-idx="${i}"]`);
          c.classList.remove('volteada');
          c.textContent = '🌸';
        });
        memoriaVolteadas = [];
        memoriaBloqueado = false;
      }, 900);
    }
  }
}

/* =========================================================
   INICIALIZACIÓN
   ========================================================= */
document.addEventListener('DOMContentLoaded', () => {
  generarListasUnidades();
  iniciarQuiz();
  generarSopa();
  renderSopa();
  generarVF();
  iniciarMemoria();
  mostrarSeccion('portada');
});