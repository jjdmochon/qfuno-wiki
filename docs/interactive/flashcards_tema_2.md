---
tags:
  - interactivo
  - flashcards
  - tema-2
  - nomenclatura
hide:
  - toc
---

# :material-cards: Flashcards — Tema 2: Nomenclatura

<div style="text-align:center; margin-bottom: 1rem;">
  <span style="background: rgba(139,92,246,0.1); color: #8b5cf6; padding: 0.5rem 1rem; border-radius: 20px; font-weight: 600; font-size: 0.9rem;">
    13 tarjetas · Nomenclatura IUPAC, Heterociclos, Betalactámicos
  </span>
</div>

!!! info "Controles"
    - **Clic** en la tarjeta para voltear (pregunta ↔ respuesta)
    - **← →** teclas de flecha para navegar
    - **Enter** para voltear con teclado

<div id="flashcard-app">
  <div style="display:flex; justify-content:space-between; align-items:center; margin-bottom:1rem;">
    <span id="counter" style="background:rgba(0,128,128,0.1); color:#008080; padding:0.5rem 1rem; border-radius:20px; font-weight:600;">1 / 13</span>
    <div style="display:flex; gap:0.5rem;">
      <button onclick="prevCard()" id="btnPrev" disabled style="width:44px;height:44px;border-radius:50%;border:2px solid #008080;background:white;color:#008080;cursor:pointer;font-size:1.1rem;display:flex;align-items:center;justify-content:center;">◀</button>
      <button onclick="nextCard()" id="btnNext" style="width:44px;height:44px;border-radius:50%;border:2px solid #008080;background:white;color:#008080;cursor:pointer;font-size:1.1rem;display:flex;align-items:center;justify-content:center;">▶</button>
    </div>
  </div>

  <div id="flashcard-container" onclick="flipCard()" style="perspective:1500px;width:100%;height:550px;cursor:pointer;margin-bottom:1rem;">
    <div id="flashcard" style="width:100%;height:100%;position:relative;transition:transform 0.6s cubic-bezier(0.4,0.2,0.2,1);transform-style:preserve-3d;">
      <div id="card-front" style="position:absolute;width:100%;height:100%;backface-visibility:hidden;background:white;border-radius:20px;box-shadow:0 10px 25px -5px rgba(0,0,0,0.1);padding:2rem;display:flex;flex-direction:column;border-top:6px solid #008080;overflow-y:auto;">
        <span style="align-self:flex-start;font-size:0.75rem;font-weight:700;text-transform:uppercase;letter-spacing:0.05em;padding:0.4rem 0.8rem;border-radius:4px;background:rgba(0,128,128,0.1);color:#008080;margin-bottom:1rem;">Pregunta / Reto</span>
        <div id="frontConcept" style="font-size:0.85rem;color:#64748b;font-weight:600;text-transform:uppercase;letter-spacing:0.05em;margin-bottom:0.75rem;"></div>
        <div id="frontText" style="font-size:1.15rem;font-weight:500;color:#36454F;flex-grow:1;line-height:1.6;"></div>
        <div id="frontImg" style="text-align:center;margin:1rem 0;"></div>
        <div style="text-align:center;color:#94a3b8;font-size:0.85rem;margin-top:auto;">🔄 Clic para ver la respuesta</div>
      </div>
      <div id="card-back" style="position:absolute;width:100%;height:100%;backface-visibility:hidden;background:white;border-radius:20px;box-shadow:0 10px 25px -5px rgba(0,0,0,0.1);padding:2rem;display:flex;flex-direction:column;border-top:6px solid #3EB489;transform:rotateY(180deg);overflow-y:auto;">
        <span style="align-self:flex-start;font-size:0.75rem;font-weight:700;text-transform:uppercase;letter-spacing:0.05em;padding:0.4rem 0.8rem;border-radius:4px;background:rgba(62,180,137,0.1);color:#3EB489;margin-bottom:1rem;">Explicación</span>
        <div id="backConcept" style="font-size:0.85rem;color:#64748b;font-weight:600;text-transform:uppercase;letter-spacing:0.05em;margin-bottom:0.75rem;"></div>
        <div id="backText" style="font-size:1.15rem;font-weight:500;color:#36454F;flex-grow:1;line-height:1.6;"></div>
        <div id="backImg" style="text-align:center;margin:1rem 0;"></div>
        <div style="text-align:center;color:#94a3b8;font-size:0.85rem;margin-top:auto;">🔄 Clic para volver a la pregunta</div>
      </div>
    </div>
  </div>

  <div style="width:100%;height:6px;background:#e2e8f0;border-radius:3px;overflow:hidden;">
    <div id="progressBar" style="height:100%;background:#008080;width:0%;transition:width 0.3s ease;"></div>
  </div>
</div>

<script>
const data=[{concepto:"Jerarquía IUPAC (Ej. Metadona)",pregunta:"La Metadona contiene un grupo amina y un grupo cetona. ¿Qué grupo define el sufijo IUPAC y cómo afecta a la numeración?",explicacion:"La <strong>cetona</strong> tiene prioridad sobre la amina. El nombre base termina en \"-ona\" y la cadena se numera otorgando al carbono carbonílico el localizador más bajo. La amina se nombra como sustituyente (\"amino\").",imgP:"https://i.ibb.co/VYBpRykT/metadona.png",imgE:"https://i.ibb.co/pBwPTsJm/metadona-respuesta.png"},{concepto:"Prefijos deductivos Hantzsch-Widman",pregunta:"Un heterociclo de 5 miembros contiene O y N. ¿Por qué átomo empiezas a numerar y cómo se ensamblan los prefijos?",explicacion:"Prioridad: Oxígeno (Oxa-) > Azufre (Tia-) > Nitrógeno (Aza-). Se numera desde el O. Uniendo prefijos + sufijo 5 miembros (-ol), se forma <strong>Oxazol</strong>.",imgP:"https://i.ibb.co/23p3ntQY/oxazol-pregunta.png",imgE:"https://i.ibb.co/Lz5xSrhx/oxazol-respuesta.png"},{concepto:"Deducción del esqueleto: -epina",pregunta:"'Benzodiacepina': benzo=benceno, di-aza=2N. ¿Qué revela '-epina' sobre el esqueleto base?",explicacion:"Hantzsch-Widman: 5 miembros→-ol, 6→-ina, <strong>7 miembros→-epina</strong>. El heterociclo base es un anillo de 7 miembros.",imgP:"https://i.ibb.co/TqNkNt7W/benzodiazepina-pregunta.png",imgE:"https://i.ibb.co/qMDhJPGV/benzodiazepina-respuesta.png"},{concepto:"Fórmula [x.y.z] (Cocaína/Atropina)",pregunta:"¿Cómo deduces los números del corchete [x.y.z] en un biciclo y por qué el total es superior a x+y+z?",explicacion:"[x.y.z] cuentan los átomos en las tres rutas entre ambas cabezas de puente (mayor→menor). Total = x+y+z + <strong>2</strong> (las propias cabezas de puente).",imgP:"https://i.ibb.co/VYBFP1rk/cocaina-pregunta.png",imgE:"https://i.ibb.co/QF6wjgg3/cocaina-respuesta.png"},{concepto:"Cefalosporinas: sufijo -eno",pregunta:"Penicilina: 'heptano'. Cefalosporina: 'oct-2-eno'. ¿Qué revela '-2-eno' sobre el anillo de 6?",explicacion:"'-eno' indica un <strong>doble enlace en posición 2</strong> del anillo dihidrotiazina. Es fundamental para la estructura 3D del núcleo Cephem.",imgP:"https://i.ibb.co/tMqH6DHQ/penicilina-cefalosporina-pregunta.png",imgE:"https://i.ibb.co/84269Dmw/penicilina-cefalosporina-respuesta.png"},{concepto:"Ácido Clavulánico: cambio heteroátomo",pregunta:"El ácido clavulánico no es un penam clásico. ¿Qué cambio tiene su anillo de 5 y cómo afecta al prefijo?",explicacion:"Sustituye el <strong>azufre (tia-)</strong> de las penicilinas por <strong>oxígeno (oxa-)</strong>. El prefijo cambia obligatoriamente.",imgP:"https://i.ibb.co/bMwq8Gjn/clavulanico-pregunta.png",imgE:"https://i.ibb.co/nN3vq63x/clavulanico-respuesta.png"},{concepto:"Numeración periférica: salto en fusión",pregunta:"Al numerar la periferia de una benzodiacepina, ¿qué ocurre con los carbonos de fusión?",explicacion:"Los carbonos de fusión se <strong>saltan</strong> con números enteros. Reciben el número del átomo precedente + una letra (5a, 9a).",imgP:"https://i.ibb.co/YShxHhD/benzodiazepina-pregunta2.png",imgE:"https://i.ibb.co/TBSBKGXg/benzodiazepina-respuesta2.png"},{concepto:"Regla histórica del N para la 'base'",pregunta:"Furano (O) + Piridina (N). El O tiene mayor prioridad de numeración. ¿Cuál es la base?",explicacion:"Regla de oro: el ciclo con <strong>Nitrógeno siempre es la base</strong>. La piridina es base y el furano se contrae a 'furo'.",imgP:"https://i.ibb.co/3YyKCWqd/furano-piridina-pregunta.png",imgE:"https://i.ibb.co/d1bMj1B/furano-piridina-respuesta.png"},{concepto:"Orientación X-Y de policíclicos",pregunta:"Un policíclico sin nombre común: ¿cuáles son las dos reglas de orientación antes de numerar?",explicacion:"1. Mayor número de anillos en horizontal (eje X). 2. Mayor número restante en cuadrante superior derecho. Solo entonces se numera desde arriba-derecha.",imgP:"https://i.ibb.co/ymvWX5LM/cuadrante-pregunta.png",imgE:"https://i.ibb.co/FLf4yC6y/cuadrante-respuesta.png"},{concepto:"Desempate: tamaño y heteroátomos",pregunta:"Imidazol (5, 2N) + Pirimidina (6, 2N). Empate en N. ¿Cómo eliges la base?",explicacion:"Criterios en orden: 1. <strong>Mayor tamaño</strong> (pirimidina 6 > imidazol 5). 2. Mayor número/variedad de heteroátomos.",imgP:"https://i.ibb.co/HLx6TSd0/imidazol-piridina-pregunta.png",imgE:"https://i.ibb.co/R4Dbtyd1/imidazol-piridina-respuesta.png"},{concepto:"Formato del corchete [nº,nº-letra]",pregunta:"En [2,3-b], ¿a qué componente pertenecen los números y a qué la letra?",explicacion:"<strong>Letra</strong> → base (enlace 1-2=a, 2-3=b...). <strong>Números</strong> → no-base (átomos que participan en la fusión).",imgP:"https://i.ibb.co/yFwT1zcw/corchetes-pregunta.png",imgE:"https://i.ibb.co/SDySwxDx/corchetes-respuesta.png"},{concepto:"Orden inverso en el no-base",pregunta:"En [3,2-c], ¿por qué los números van 3,2 en vez de 2,3?",explicacion:"El orden respeta la <strong>dirección del enlace del anillo base</strong>. Se escriben según como se encuentran al recorrer esa dirección geométrica.",imgP:"https://i.ibb.co/MkfdCHZQ/corechetes-inverso-pregunta.png",imgE:"https://i.ibb.co/QFGRBShM/corechetes-inverso-respuesta.png"},{concepto:"Prefijos contraídos del no-base",pregunta:"Si el componente no-base es furano, tiofeno o piridina, ¿cuáles son sus prefijos?",explicacion:"Furano → <strong>furo</strong>, Tiofeno → <strong>tieno</strong>, Piridina → <strong>pirido</strong>. Ej: tieno[3,2-b]furano.",imgP:"https://i.ibb.co/99PM2bnz/furo-pregunta.png",imgE:"https://i.ibb.co/zHsHsTkG/furo-respuesta.png"}];
let ci=0;const t=data.length;
function u(i){const d=data[i];document.getElementById("frontConcept").textContent=d.concepto;document.getElementById("frontText").innerHTML=d.pregunta;document.getElementById("backConcept").textContent=d.concepto;document.getElementById("backText").innerHTML=d.explicacion;document.getElementById("counter").textContent=(i+1)+" / "+t;document.getElementById("btnPrev").disabled=i===0;document.getElementById("btnNext").disabled=i===t-1;document.getElementById("progressBar").style.width=((i+1)/t*100)+"%";document.getElementById("frontImg").innerHTML=d.imgP?'<img src="'+d.imgP+'" style="max-height:160px;border-radius:12px;">':'';document.getElementById("backImg").innerHTML=d.imgE?'<img src="'+d.imgE+'" style="max-height:160px;border-radius:12px;">':'';}
function flipCard(){const s=window.getSelection();if(s&&s.toString().length>0)return;const f=document.getElementById("flashcard");f.style.transform=f.style.transform==="rotateY(180deg)"?"rotateY(0deg)":"rotateY(180deg)";}
function reset(){document.getElementById("flashcard").style.transform="rotateY(0deg)";}
function prevCard(){if(ci>0){ci--;reset();setTimeout(()=>u(ci),150);}}
function nextCard(){if(ci<t-1){ci++;reset();setTimeout(()=>u(ci),150);}}
document.addEventListener("keydown",e=>{if(e.key==="ArrowRight")nextCard();else if(e.key==="ArrowLeft")prevCard();else if(e.key==="Enter")flipCard();});
document.addEventListener("DOMContentLoaded",()=>u(0));
u(0);
</script>
