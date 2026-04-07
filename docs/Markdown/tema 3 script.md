Listen to this tab

Hoy vamos a adentrarnos en una de las partes más fascinantes del Bloque II: Diseño y  Desarrollo de Fármacos. Si recordáis, en clases anteriores estuvimos viendo cómo  históricamente muchos fármacos se descubrían por serendipia o a partir de productos  naturales sin conocer muy bien su diana. Sin embargo, hoy vamos a cambiar el chip. Vamos  a hablar de cómo la química se encuentra con la tecnología. 

En los próximos 45 minutos, vamos a cubrir la Sección 2.4: Diseño racional basado en la  diana (SBDD, por sus siglas en inglés) y la Sección 3: Diseño de fármacos asistido por  Inteligencia Artificial. 

Si queréis profundizar después de clase, os recomiendo que le echéis un vistazo al capítulo  correspondiente en el Patrick (An Introduction to Medicinal Chemistry) o en el Foye, que lo  explican con una claridad meridiana. 

¿Listos? Empezamos. 

### Minutos 0 - 15: Sección 2.4 - Diseño racional basado en la diana (SBDD) 

Profesor (hablando a la clase): 

El diseño racional basado en la diana parte de una premisa lógica: si conocemos la  cerradura en detalle, podemos diseñar la llave perfecta para abrirla o bloquearla. No  probamos moléculas a ciegas; usamos la estructura tridimensional de nuestra diana  biológica (una enzima, un receptor, un canal iónico) obtenida mediante cristalografía de  rayos X, RMN o criomicroscopía electrónica. 

Shutterstock 

(Instrucción visual para tu presentación: Aquí debes mostrar en la diapositiva la estructura  de una proteína con un ligando en su centro activo). 

Para que lo entendáis bien, os voy a poner un ejemplo clínico y químico histórico: el  desarrollo del Captopril, el primer inhibidor de la Enzima Convertidora de Angiotensina  (ECA) para tratar la hipertensión. 

Estructura a añadir en la pizarra/diapositiva: * Captopril (Pequeña molécula): Muestra  su estructura destacando el grupo sulfhidrilo (-SH), el grupo amida y el ácido carboxílico  de la prolina. 

Profesor: 

Fijaos en la estructura del Captopril. Los investigadores no conocían la estructura exacta de  la ECA en ese momento, pero sabían que era una metaloproteasa de zinc, muy parecida a  la carboxipeptidasa A, cuya estructura sí se conocía. Usando un razonamiento lógico  impecable, diseñaron el Captopril para que su grupo carboxilato interaccionara con residuos  básicos del centro activo, y aquí viene la magia: introdujeron un grupo sulfhidrilo (-SH) específicamente para que coordinara fuertemente con el ion Zinc ($Zn^{2+}$) catalítico de la  enzima. ¡Esto es diseño racional puro! Entender la química de la diana para modelar tu  molécula. 

### Minutos 15 - 30: Subsecciones del Diseño Racional (Molecular Docking y  Diseño De Novo) 

Profesor: 

Dentro de esta sección 2.4, tenemos varias herramientas computacionales. Vamos a  centrarnos en dos subsecciones clave: el Docking Molecular (o acoplamiento molecular) y el  Diseño De Novo. 

El Docking es básicamente un programa informático que coge una quimioteca de miles de  moléculas pequeñas y prueba computacionalmente cómo encajarían en el bolsillo de  nuestra proteína. Evalúa interacciones puente de hidrógeno, fuerzas de Van der Waals y  repulsiones estéricas, dándonos un "score" o puntuación de energía de unión. 

Estructura a añadir en la pizarra/diapositiva: 

- ●  Zanamivir y Oseltamivir (Tamiflu): Muestra ambas estructuras comparadas con el  ácido siálico (el sustrato natural). 

Profesor: 

Un ejemplo brillante de éxito del Docking molecular y la cristalografía es el diseño del  Oseltamivir (Tamiflu), usado para la gripe. Mirad las estructuras. Los químicos cristalizaron  la enzima neuraminidasa del virus de la gripe. Vieron que el sustrato natural (el ácido  siálico) dejaba unos "bolsillos" hidrofóbicos y básicos vacíos en la enzima durante el estado  de transición. Mediante docking, diseñaron el Oseltamivir cambiando el grupo hidroxilo del  sustrato natural por un grupo amino y añadiendo cadenas hidrofóbicas para rellenar esos  huecos. El resultado fue una afinidad miles de veces mayor que el sustrato natural. Relación  estructura-actividad (SAR) aplicada directamente sobre la pantalla del ordenador. 

La otra estrategia es el Diseño De Novo. Aquí no partimos de una base conocida; el  programa informático construye la molécula átomo a átomo o fragmento a fragmento  directamente dentro del centro activo vacío, creando andamiajes (scaffolds) químicos  completamente nuevos y patentables. 

- 1.  Predicción de propiedades ADMET: La IA puede predecir si una molécula que  acabas de dibujar será tóxica, si se absorberá bien por vía oral o si cruzará la  barrera hematoencefálica, antes incluso de sintetizarla en el laboratorio. 
- 2.  Modelos Generativos: Al igual que ChatGPT genera texto, existen IAs generativas  que "imaginan" nuevas moléculas con las propiedades químicas exactas que le  pidamos. 

### Minutos 30 - 40: Sección 3 - Diseño de fármacos asistido por IA 

Profesor: 

Y esto nos lleva al futuro que ya es presente: la Sección 3, el Diseño de Fármacos  asistido por Inteligencia Artificial. 

Hoy en día ya no dependemos solo de la intuición del químico farmacéutico. Las redes  neuronales y el Machine Learning han revolucionado nuestro campo. ¿Cómo lo hace? 

Estructura a añadir en la pizarra/diapositiva: 

- ●  Halicina (Halicin): Muestra la estructura de este compuesto (un derivado de  nitro-tiazol). 

Profesor: 

Dejadme que os dé un ejemplo clínico revolucionario. Mirad la estructura de la Halicina.  Fue descubierta recientemente en el MIT usando Inteligencia Artificial. Los investigadores  entrenaron a una red neuronal con miles de moléculas indicándole cuáles tenían actividad  antibacteriana y cuáles no. Luego, le pidieron a la IA que buscara en una base de datos de  fármacos ya existentes (SOSA, que lo vimos en el Tema 3) aquellos que pudieran matar  bacterias pero que no se parecieran en nada a los antibióticos clásicos (como las penicilinas  que veíamos en formulación). 

La IA identificó la Halicina, que originalmente se investigaba para la diabetes. Resultó ser un  potente antibiótico contra cepas multirresistentes, con un mecanismo de acción totalmente  novedoso (altera el gradiente electroquímico en la membrana celular bacteriana). Un  descubrimiento que a un humano le habría llevado décadas, la IA lo filtró en días. 

### Minutos 40 - 45: Conclusiones, Resumen y Dudas 

Profesor: 

Para resumir los puntos clave de hoy, quedaos con esto: 

- 1.  SBDD (Diseño basado en la diana): Requiere conocer la estructura tridimensional  del objetivo biológico para modelar fármacos como llaves perfectas (ej. Captopril). 
- 2.  Docking Molecular: Herramienta que predice la orientación y afinidad de un  fármaco en su diana (ej. Oseltamivir). 
- 3.  Inteligencia Artificial: Acelera drásticamente el descubrimiento identificando  patrones ocultos, generando nuevas estructuras y prediciendo perfiles  farmacocinéticos (ADMET) de forma ultra rápida (ej. Halicina). 

Recordad que para el examen parcial, como siempre os digo, no quiero que memoricéis  estructuras complejas como un dibujo sin sentido. Quiero que sepáis identificar el  farmacóforo y explicar por qué ese grupo funcional está ahí interactuando con la diana. 

¿Alguna duda con los mecanismos de interacción que hemos visto hoy? ¿O sobre cómo la  IA define los parámetros de afinidad? 


