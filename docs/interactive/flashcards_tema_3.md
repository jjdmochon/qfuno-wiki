---
tags:
  - interactivo
  - flashcards
  - tema-3
  - CADD
  - serendipia
hide:
  - toc
---

# :material-cards: Flashcards — Tema 3: Búsqueda del Prototipo

<div style="text-align:center; margin-bottom: 1rem;">
  <span style="background: rgba(255,127,80,0.1); color: #FF7F50; padding: 0.5rem 1rem; border-radius: 20px; font-weight: 600; font-size: 0.9rem;">
    40 tarjetas · Prototipos, Screening, SOSA, Serendipia, CADD, IA
  </span>
</div>

!!! info "Controles"
    - **Clic** en la tarjeta para voltear (pregunta ↔ respuesta)
    - **← →** teclas de flecha para navegar
    - **Enter** para voltear con teclado
    - Algunas respuestas incluyen fórmulas LaTeX

<div id="flashcard-app">
  <div style="display:flex; justify-content:space-between; align-items:center; margin-bottom:1rem;">
    <span id="counter3" style="background:rgba(255,127,80,0.1); color:#FF7F50; padding:0.5rem 1rem; border-radius:20px; font-weight:600;">1 / 40</span>
    <div style="display:flex; gap:0.5rem;">
      <button onclick="prevCard3()" id="btnPrev3" disabled style="width:44px;height:44px;border-radius:50%;border:2px solid #FF7F50;background:white;color:#FF7F50;cursor:pointer;font-size:1.1rem;display:flex;align-items:center;justify-content:center;">◀</button>
      <button onclick="nextCard3()" id="btnNext3" style="width:44px;height:44px;border-radius:50%;border:2px solid #FF7F50;background:white;color:#FF7F50;cursor:pointer;font-size:1.1rem;display:flex;align-items:center;justify-content:center;">▶</button>
    </div>
  </div>

  <div onclick="flipCard3()" style="perspective:1500px;width:100%;height:420px;cursor:pointer;margin-bottom:1rem;">
    <div id="flashcard3" style="width:100%;height:100%;position:relative;transition:transform 0.6s cubic-bezier(0.4,0.2,0.2,1);transform-style:preserve-3d;">
      <div id="card-front3" style="position:absolute;width:100%;height:100%;backface-visibility:hidden;background:white;border-radius:20px;box-shadow:0 10px 25px -5px rgba(0,0,0,0.1);padding:2rem;display:flex;flex-direction:column;border-top:6px solid #FF7F50;overflow-y:auto;">
        <span style="align-self:flex-start;font-size:0.75rem;font-weight:700;text-transform:uppercase;letter-spacing:0.05em;padding:0.4rem 0.8rem;border-radius:4px;background:rgba(255,127,80,0.1);color:#FF7F50;margin-bottom:1rem;">Pregunta</span>
        <div id="frontText3" style="font-size:1.15rem;font-weight:500;color:#36454F;flex-grow:1;line-height:1.7;"></div>
        <div style="text-align:center;color:#94a3b8;font-size:0.85rem;margin-top:auto;padding-top:1rem;">🔄 Clic para ver la respuesta</div>
      </div>
      <div style="position:absolute;width:100%;height:100%;backface-visibility:hidden;background:white;border-radius:20px;box-shadow:0 10px 25px -5px rgba(0,0,0,0.1);padding:2rem;display:flex;flex-direction:column;border-top:6px solid #3EB489;transform:rotateY(180deg);overflow-y:auto;">
        <span style="align-self:flex-start;font-size:0.75rem;font-weight:700;text-transform:uppercase;letter-spacing:0.05em;padding:0.4rem 0.8rem;border-radius:4px;background:rgba(62,180,137,0.1);color:#3EB489;margin-bottom:1rem;">Respuesta</span>
        <div id="backText3" style="font-size:1.15rem;font-weight:500;color:#36454F;flex-grow:1;line-height:1.7;"></div>
        <div style="text-align:center;color:#94a3b8;font-size:0.85rem;margin-top:auto;padding-top:1rem;">🔄 Clic para volver</div>
      </div>
    </div>
  </div>

  <div style="width:100%;height:6px;background:#e2e8f0;border-radius:3px;overflow:hidden;">
    <div id="progressBar3" style="height:100%;background:linear-gradient(90deg,#FF7F50,#3EB489);width:0%;transition:width 0.3s ease;"></div>
  </div>
</div>

<script>
const d3=[
{q:"¿Cuál es el objetivo principal de la Química Farmacéutica respecto a la potencia de los compuestos?",a:"Desarrollar moléculas que sean activas a dosis muy bajas (más potentes)."},
{q:"¿Qué concepto busca reducir los efectos secundarios mediante la medicina de precisión?",a:"La selectividad."},
{q:"¿Por qué el paracetamol probablemente no obtendría aprobación bajo estándares actuales?",a:"Debido a su elevada hepatotoxicidad."},
{q:"¿Qué es un Prototipo (Cabeza de serie)?",a:"Molécula con actividad farmacológica interesante que sirve como punto de partida para optimizaciones estructurales."},
{q:"¿A qué tipo de sustancias deben su actividad biológica los productos naturales?",a:"A los metabolitos secundarios."},
{q:"¿Qué modificación estructural diferencia la morfina de la codeína?",a:"La metilación de un grupo -OH fenólico."},
{q:"¿Qué son los fármacos 'gemelos' (me-too products)?",a:"Fármacos diseñados usando productos líderes como prototipos para evitar restricciones de patentes."},
{q:"¿Qué fármaco inhibidor de la ECA sirvió de prototipo para el Enalapril?",a:"El Captopril (sintetizado en 1977)."},
{q:"¿En qué consiste el cribado farmacológico (screening)?",a:"En someter un gran número de compuestos a ensayos biológicos para encontrar una acción biológica desconocida."},
{q:"¿Qué familia de psicofármacos descubrió L.H. Sternbach mediante ensayos extensivos?",a:"Las benzodiazepinas."},
{q:"¿Qué es el HTS (High Throughput Screening)?",a:"Uso de robótica y automatización para someter miles de compuestos a ensayos biológicos de forma rápida y masiva."},
{q:"¿Qué agente hipocolesterolémico fue descubierto mediante HTS?",a:"La lovastatina (inhibidor de la HMG-CoA reductasa)."},
{q:"¿Qué fármaco antiviral contra SARS-CoV-2 se desarrolló mediante docking computacional?",a:"El Ensitrelvir (S-217622)."},
{q:"¿Qué significa el enfoque SOSA?",a:"Selective Optimization of Side Activities: optimización selectiva de una actividad lateral de un fármaco conocido para un nuevo uso clínico."},
{q:"¿Qué aplicaciones terapéuticas surgieron de los efectos laterales de las sulfonamidas?",a:"Diuréticos e hipoglucemiantes orales."},
{q:"¿Para qué indicación original se investigaba el sildenafilo?",a:"Angina de pecho (antianginoso). El efecto secundario inesperado fue la erección peneana."},
{q:"¿Qué antihistamínico fue el punto de partida para los neurolépticos (clorpromazina)?",a:"La prometazina."},
{q:"¿Qué compuesto de la industria del caucho se convirtió en tratamiento del alcoholismo?",a:"El disulfiram (Antabus®)."},
{q:"¿Cuál es la base fundamental del Diseño Racional de Fármacos?",a:"El conocimiento detallado de los procesos bioquímicos alterados en una enfermedad específica."},
{q:"¿Por qué se administra L-dopa en lugar de dopamina para el Parkinson?",a:"Porque la dopamina no atraviesa la barrera hematoencefálica, mientras que la L-dopa sí puede cruzarla."},
{q:"¿Qué enzima transforma la L-dopa en dopamina en el cerebro?",a:"La dopa-descarboxilasa."},
{q:"¿Qué característica de la enzima ECA fue clave para diseñar el Captopril?",a:"Es una metaloproteasa que contiene un ion de Zinc (Zn²⁺)."},
{q:"¿Cuál fue el 'salto de genialidad' químico del Captopril?",a:"La incorporación de un grupo tiol (-SH) capaz de quelar el átomo de Zinc."},
{q:"¿Qué es el CADD (Computer-Aided Drug Design)?",a:"Uso de herramientas informáticas para comprender requisitos estructurales, diseñar nuevas moléculas y predecir actividad biológica."},
{q:"¿Qué base de datos internacional almacena las estructuras 3D de las proteínas?",a:"El Protein Data Bank (PDB)."},
{q:"¿Qué es un Farmacóforo?",a:"Conjunto de grupos químicos y su disposición espacial esenciales para que una molécula sea reconocida por un receptor específico."},
{q:"¿Qué técnica computacional consiste en ajustar un ligando en el centro activo de una proteína?",a:"Docking (diseño directo)."},
{q:"¿Qué fármaco inhibidor de COX-2 fue retirado por efectos cardiovasculares?",a:"El Vioxx (Rofecoxib). Detectado en Fase IV post-marketing."},
{q:"¿Qué avance de IA permite predecir la estructura 3D de proteínas desde su secuencia?",a:"AlphaFold (Google DeepMind). Nobel de Química 2024: Demis Hassabis y John Jumper."},
{q:"¿Bajo qué condición se usa el Diseño Indirecto de fármacos?",a:"Cuando NO se conoce la estructura 3D de la diana."},
{q:"¿Cuál es la principal diferencia entre COX-1 y COX-2?",a:"COX-1 protege la mucosa estomacal; COX-2 está implicada en procesos inflamatorios."},
{q:"¿Qué importancia tiene el grupo tiol (-SH) en el Captopril?",a:"Actúa como agente quelante del ion Zn²⁺ en el centro activo de la enzima ECA."},
{q:"¿Qué analogía utiliza el profesor para el concepto de prototipo?",a:"El coche de Fórmula 1 al inicio de la temporada."},
{q:"¿Qué componente del farmacóforo de las penicilinas es esencial?",a:"El anillo betalactámico."},
{q:"¿Qué ocurrió con la talidomida que cambió la regulación de fármacos quirales?",a:"Se administró como mezcla racémica y un enantiómero causó efectos teratogénicos graves."},
{q:"¿Cuál es la diana del Ensitrelvir en el tratamiento del COVID-19?",a:"La proteasa 3CL del SARS-CoV-2."},
{q:"¿Cuál es el objetivo del diseño indirecto al superponer moléculas activas?",a:"Encontrar características estructurales comunes (el farmacóforo) a pesar de sus diferencias químicas."},
{q:"¿Qué papel juega el Zinc en el mecanismo catalítico de la ECA?",a:"Actúa como cofactor metálico necesario para la hidrólisis de la angiotensina."},
{q:"¿Qué limitación ética impulsa el cribado in vitro e in silico?",a:"Las leyes de bienestar animal que limitan los ensayos in vivo."},
{q:"¿Qué método obtiene la estructura 3D de proteínas para diseño directo?",a:"Difracción de rayos X (cristalografía)."}
];
let ci3=0;const t3=d3.length;
function u3(i){document.getElementById("frontText3").innerHTML=d3[i].q;document.getElementById("backText3").innerHTML=d3[i].a;document.getElementById("counter3").textContent=(i+1)+" / "+t3;document.getElementById("btnPrev3").disabled=i===0;document.getElementById("btnNext3").disabled=i===t3-1;document.getElementById("progressBar3").style.width=((i+1)/t3*100)+"%";if(typeof MathJax!=="undefined"){MathJax.typesetPromise();}}
function flipCard3(){const s=window.getSelection();if(s&&s.toString().length>0)return;const f=document.getElementById("flashcard3");f.style.transform=f.style.transform==="rotateY(180deg)"?"rotateY(0deg)":"rotateY(180deg)";}
function r3(){document.getElementById("flashcard3").style.transform="rotateY(0deg)";}
function prevCard3(){if(ci3>0){ci3--;r3();setTimeout(()=>u3(ci3),150);}}
function nextCard3(){if(ci3<t3-1){ci3++;r3();setTimeout(()=>u3(ci3),150);}}
document.addEventListener("keydown",e=>{if(e.key==="ArrowRight")nextCard3();else if(e.key==="ArrowLeft")prevCard3();else if(e.key==="Enter")flipCard3();});
u3(0);
</script>
