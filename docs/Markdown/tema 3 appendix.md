2.4. Diseño racional basado en la diana (Structure  Based Drug Discovery - SBDD) 

Si conocemos la cerradura en detalle, podemos diseñar la llave perfecta para  abrirla o bloquearla.

No probamos moléculas a ciegas; usamos la estructura tridimensionalde nuestra diana biológica (una enzima, un receptor, un canal iónico) obtenidamediante:

• Cristalografía de rayos X - https://www.rcsb.org/ PDF Database

• RMN (Resonancia Magnética Nuclear)

• Criomicroscopía electronica

- • Alphafold (asistida por IA)

https://alphafold.ebi.ac.uk/

https://alphafoldserver.com/welcome

2.4. Diseño racional basado en la diana (Structure  Based Drug Discovery - SBDD) 

Differencias entre X-Ray y Criomicroscopia

|Característica|Cristalografía de Rayos X|Crio-Microscopía Electrónica (CrioEM)|
|---|---|---|
|Preparación de la  Muestra|Requiere cristalización (el  mayor cuello de botella; puede  tardar meses o años).|No requiere cristales. La muestra se  congela rápidamente en su estado  nativo.|
|Tamaño de la Proteína|Ideal para proteínas pequeñas  (<100 kDa) y muy estables.|Ideal para complejos grandes,  proteínas de membrana y  ensamblajes.|
|Resolución y Detalle|Generalmente mayor resolución  atómica (inferior a 2 Å).|2 -4 Å|
|Dinámica y Flexibilidad|Lla estructura está "rígida"|Permite identificar múltiples estados  conformacionales y flexibilidad.|
|Cantidad de Muestra|Necesita grandes cantidades de  proteína pura.|Requiere mucha menos muestra,  ideal para proteínas difíciles de  producir.|

SBDD – Ejemplo: Captopril (iECA)

Primer inhibidor de la Enzima Convertidora de Angiotensina (ECA) para tratar la  hipertensión.

Diseño racional

Los investigadores no conocían la estructura exacta  de la ECA, pero sabían que era una metaloproteasa  de zinc muy parecida a la carboxipeptidasa A, cuya  estructura sí se conocía.

Grupos funcionales clave

• Grupo sulfhidrilo (-SH): coordina con el Zn²⁺ catalítico de la enzima.

• Grupo carboxilato: interactúa con residuos básicos  del centro activo.

• Grupo amida + Prolina

![image 8](images/imageFile8.png)

Esto es diseño racional puro: entender la química de la diana para modelar tu  molécula.

2.4. Diseño racional basado en la diana (Structure  Based Drug Discovery - SBDD)

Si conocemos la cerradura en detalle, podemos diseñar la llave perfecta para  abrirla o bloquearla.

![image 12](images/imageFile12.png)

![image 13](images/imageFile13.png)

https://www.rcsb.org/3d-view/1UZF

Zn+2

Docking Molecular (Acoplamiento Molecular)

Programa informático que prueba computacionalmente cómo miles de moléculas  pequeñas (quimioteca) encajarían en el bolsillo de unión de una proteína diana.

Puentes de H

Evalúa interacciones por  puente de hidrógeno entre  ligando y diana.

Van der Waals

Calcula fuerzas de Van der  Waals complementarias.

Score energético

Genera una puntuación de  energía de unión (binding score).

Ejemplo: Oseltamivir (Tamiflu®) – Antigripal

Los químicos cristalizaronla neuraminidasa del virus de la gripe. Observaron que el sustrato natural (ácidosiálico) dejaba bolsillos hidrofóbicosy básicos vacíos en el estado de  transición. Mediante docking, diseñaron el Oseltamivir cambiando el grupo hidroxilo por un  amino y añadiendo cadenas hidrofóbicas → afinidad miles de veces mayor que el sustrato natural. SAR sobre la pantalla del ordenador.

https://www.rcsb.org/3d-view/3CL0/1

Docking Molecular (Acoplamiento Molecular)

Ejemplo de éxito: Oseltamivir (Tamiflu®) – Antigripal

https://www.rcsb.org/3d-view/3CL0/1

ácido siálico

Oseltamivir

Diseño De Novo

A diferencia del Docking, en el Diseño De Novo no se parte de una molécula conocida.

El programa informático construye la molécula átomo a átomo o fragmento a  fragmento directamente dentro del centro activo vacío, creando andamiajes (scaffolds) químicos completamente nuevos y patentables.

Ventaja

Genera estructuras totalmente novedosas  sin sesgo hacia compuestos conocidos.

Aplicación

Especialmente útil cuando se dispone de  la estructura cristalina de la diana pero no  hay ligandos conocidos.

3. Diseño de fármacos asistido por IA

El futuro que ya es presente: las redes neuronales y el Machine Learning han  revolucionado el descubrimiento de fármacos.

Predicción ADMET

La IA predice si una molécula será tóxica, si se  absorberá bien por vía oral o si cruzará la  barrera hematoencefálica, ANTES de  sintetizarla en el laboratorio.

Modelos Generativos

Al igual que ChatGPT genera texto, existen IAs  generativas que "imaginan" nuevas moléculas  con las propiedades químicas exactas que le  pidamos.

![image 29](images/imageFile29.png)

Ya no dependemos solo de la intuición del químico farmacéutico.

IA – Caso de éxito: Halicina

Descubierta en el MIT usando Inteligencia Artificial.

Los investigadores entrenaron a una red neuronal con miles de moléculas indicándole cuáles tenían actividad antibacteriana y cuáles no. Luego le pidieron a  la IA que buscara en una base de datos de fármacos existentes (enfoque SOSA)  aquellos que pudieran matar bacterias pero que no se parecieran a los antibióticos clásicos.

![image 33](images/imageFile33.png)

IA – Caso de éxito: Halicina

Descubierta en el MIT usando Inteligencia Artificial.

Resultado

La IA identificó la Halicina (derivado de nitro-tiazol),  investigada originalmente para la diabetes. Resultó  ser un potente antibiótico contra cepas  multirresistentes.

Mecanismo novedoso

Altera el gradiente electroquímico en la membrana  celular bacteriana. Un mecanismo de acción  totalmente distinto a los antibióticos clásicos.

![image 39](images/imageFile39.png)

Un descubrimiento que habría llevado décadas → la IA lo filtró en días.

Conclusiones y Puntos Clave

SBDD

Requiereconocer la estructura 3D del objetivo biológico para  modelarfármacoscomo llaves perfectas.

Ej. Captopril

Docking

Herramientaque predice la  orientacióny afinidad de un  fármacoen su diana computacionalmente.

Ej. Oseltamivir

IA

Acelera drásticamente el  descubrimiento identificando  patrones ocultos y prediciendo  ADMET de forma ultra rápida.

Ej. Halicina

Para el examen: No memoricéis estructuras complejas como un dibujo sin  sentido. Debéis saber identificar el farmacóforo y explicar por qué ese grupo  funcional está ahí interactuando con la diana.

BIBLIOGRAFÍA:

• Patrick, G. (2023) An Introduction to Medicinal Chemistry, Oxford University Press.

• Foye, W.O. et al. Foye's Principles of Medicinal Chemistry.

• Galbis Pérez, J.A. (2004) Panorama Actual de la Química Farmacéutica, 2ª ed., Univ. de Sevilla.

• Campos Rosa, J.M. et al. (2013) Química Farmacéutica I, 1ª ed., Univ. de Granada.


