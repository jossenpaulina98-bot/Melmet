<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>MELMET 🍌</title>

<style>

:root{
--rosa:#ffd9e8;
--marron:#7b4f34;
--amarillo:#ffd84d;
--verde:#28a745;
}

*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:Segoe UI,sans-serif;
}

body{
background:#fff7fb;
overflow-x:hidden;
padding-bottom:100px;
}

/* HEADER */

header{
background:white;
display:flex;
justify-content:center;
align-items:center;
padding:15px 20px;
box-shadow:0 2px 15px rgba(0,0,0,.1);
}

.logo{
display:block;
margin:0 auto;
width:320px;
max-width:90%;
height:180px;
object-fit:cover;
object-position:center;
border-radius:20px;
}

/* HERO */

.hero{
height:520px;
position:relative;
overflow:hidden;
display:flex;
flex-direction:column;
justify-content:center;
align-items:center;
text-align:center;
background:linear-gradient(135deg,#ffbfd8,#ffd9e8,#fff2bb,#ffd84d);
}

.hero h1{
font-size:60px;
color:var(--marron);
}

.hero p{
font-size:20px;
max-width:600px;
padding:20px;
}

.hero button{
padding:15px 25px;
font-size:18px;
border:none;
border-radius:12px;
background:var(--marron);
color:white;
cursor:pointer;
}

/* BANANAS */

.banana{
position:absolute;
font-size:80px;
animation:subir 12s linear infinite;
}

.b1{ left:10%; bottom:-100px; }
.b2{ left:50%; bottom:-120px; animation-delay:3s; }
.b3{ right:10%; bottom:-100px; animation-delay:6s; }

@keyframes subir{
0%{ transform:translateY(0) rotate(0deg); }
100%{ transform:translateY(-900px) rotate(360deg); }
}

/* BANNER */

.banner{
background:var(--amarillo);
padding:15px;
text-align:center;
font-size:20px;
font-weight:bold;
color:var(--marron);
}

/* SECCIONES */

.container{
width:95%;
max-width:1200px;
margin:auto;
padding:20px;
}

.seccion{
background:white;
padding:25px;
margin-top:20px;
border-radius:20px;
box-shadow:0 5px 20px rgba(0,0,0,.1);
}

h2{
color:var(--marron);
margin-bottom:15px;
}

/* PRODUCTOS Y COMBOS */

.productos{
display:flex;
gap:20px;
flex-wrap:wrap;
justify-content:center;
}

.card{
width:290px;
background:white;
border-radius:20px;
overflow:hidden;
box-shadow:0 2px 15px rgba(0,0,0,.15);
position:relative;
display:flex;
flex-direction:column;
justify-content:space-between;
}

.etiqueta-promo{
position:absolute;
top:12px;
left:12px;
background:#e53935;
color:white;
font-size:12px;
font-weight:bold;
padding:5px 10px;
border-radius:20px;
box-shadow:0 2px 8px rgba(0,0,0,.2);
}

.card img{
width:100%;
height:180px;
object-fit:cover;
}

.card-content{
padding:15px;
}

.descripcion-prod{
font-size:14px;
color:#666;
margin-top:6px;
}

.info-nutri{
font-size:12px;
background:#fff7fb;
color:var(--marron);
padding:6px 10px;
border-radius:8px;
margin-top:8px;
border:1px solid #ffd9e8;
}

.select-ingrediente{
font-size:13px;
padding:8px;
margin-top:8px;
background:#fafafa;
}

.precio-tachado{
font-size:15px;
color:#999;
text-decoration:line-through;
margin-top:8px;
}

.precio{
font-size:25px;
font-weight:bold;
color:#ff9800;
margin:4px 0 12px 0;
}

/* INPUTS Y BOTONES */

input,
textarea,
select{
width:100%;
padding:12px;
margin:8px 0;
border-radius:10px;
border:1px solid #ddd;
font-size:15px;
}

button{
background:var(--marron);
color:white;
border:none;
padding:12px 18px;
border-radius:10px;
cursor:pointer;
font-weight:bold;
transition:0.2s;
}

button:hover{
opacity:0.9;
}

/* MÉTODOS DE PAGO */

.promo-pagos-info{
display:flex;
gap:10px;
flex-wrap:wrap;
margin-bottom:12px;
}

.pill-descuento{
background:#e8f5e9;
color:#1b5e20;
border:1px solid #a5d6a7;
padding:8px 14px;
border-radius:12px;
font-size:14px;
font-weight:bold;
}

.pago-box{
display:none;
background:#fff9fc;
border:2px dashed #ffb6d5;
padding:18px;
border-radius:15px;
margin-top:12px;
}

.dato-banco{
background:white;
padding:10px 14px;
border-radius:8px;
margin:8px 0;
border:1px solid #eee;
display:flex;
justify-content:space-between;
align-items:center;
flex-wrap:wrap;
gap:10px;
}

.btn-copiar{
background:#ff9800;
padding:6px 12px;
font-size:13px;
}

.fila-tarjeta{
display:flex;
gap:10px;
}

/* CARRITO Y TOTALES */

#carrito{
list-style:none;
margin-bottom:15px;
}

#carrito li{
padding:10px 14px;
background:#f8f8f8;
border-radius:8px;
margin:6px 0;
display:flex;
justify-content:space-between;
align-items:center;
gap:10px;
}

.btn-eliminar{
background:#e53935;
padding:5px 10px;
font-size:12px;
}

.resumen-totales{
background:#fff9f0;
padding:15px;
border-radius:12px;
margin:15px 0;
border:1px solid #ffe0b2;
}

.linea-subtotal{
font-size:16px;
color:#555;
margin-bottom:5px;
}

.linea-descuento{
font-size:17px;
color:var(--verde);
font-weight:bold;
margin-bottom:8px;
display:none;
}

.total{
font-size:28px;
font-weight:bold;
color:var(--marron);
}

.btn-confirmar{
width:100%;
padding:16px;
font-size:18px;
background:var(--verde);
margin-top:10px;
}

/* SEGUIMIENTO DEL PEDIDO */

#seccionSeguimiento{
display:none;
border:2px solid var(--marron);
background:#fffdf9;
}

.header-seguimiento{
display:flex;
justify-content:space-between;
align-items:center;
flex-wrap:wrap;
gap:10px;
margin-bottom:15px;
}

.codigo-pedido{
background:var(--amarillo);
color:var(--marron);
padding:6px 14px;
border-radius:20px;
font-weight:bold;
font-size:15px;
}

.barra-progreso-contenedor{
width:100%;
height:12px;
background:#eee;
border-radius:10px;
overflow:hidden;
margin:15px 0 25px 0;
}

.barra-progreso{
height:100%;
width:25%;
background:linear-gradient(90deg, #ff9800, #28a745);
transition:width 0.6s ease;
}

.pasos-seguimiento{
display:grid;
grid-template-columns:repeat(auto-fit, minmax(200px, 1fr));
gap:15px;
margin-bottom:20px;
}

.paso{
padding:15px;
border-radius:14px;
background:#f4f4f4;
color:#888;
border:2px solid transparent;
transition:0.3s;
}

.paso.activo{
background:#e8f5e9;
color:#1b5e20;
border-color:var(--verde);
font-weight:bold;
}

.paso.completado{
background:#fff7fb;
color:var(--marron);
border-color:#ffb6d5;
}

.paso-icono{
font-size:26px;
display:block;
margin-bottom:6px;
}

.detalle-entrega-box{
background:white;
padding:15px;
border-radius:12px;
border:1px solid #eee;
font-size:14px;
line-height:1.6;
}

.btn-simular{
background:#ff9800;
font-size:13px;
padding:8px 14px;
margin-top:12px;
}

/* NOTIFICACIÓN FLOTANTE DE PEDIDO */

#notificacion{
display:none;
position:fixed;
top:20px;
right:20px;
max-width:360px;
background:white;
border-left:6px solid var(--verde);
padding:18px;
border-radius:15px;
box-shadow:0 10px 30px rgba(0,0,0,.25);
z-index:9999;
animation:deslizar 0.4s ease;
}

@keyframes deslizar{
from{ transform:translateX(120%); opacity:0; }
to{ transform:translateX(0); opacity:1; }
}

#notificacion h3{
color:var(--verde);
margin-bottom:6px;
}

#notificacion p{
font-size:14px;
color:#333;
line-height:1.4;
}

.btn-wsp{
display:inline-block;
margin-top:10px;
background:#25D366;
color:white;
text-decoration:none;
padding:8px 14px;
border-radius:8px;
font-size:13px;
font-weight:bold;
}

/* COQUITO */

#coquito{
position:fixed;
right:20px;
bottom:20px;
width:80px;
height:80px;
border-radius:50%;
overflow:hidden;
cursor:pointer;
box-shadow:0 5px 20px rgba(0,0,0,.25);
background:white;
z-index:1000;
border:3px solid var(--marron);
}

#coquito img{
width:100%;
height:100%;
object-fit:cover;
object-position:center;
transform:scale(1.4);
}

.badge-coquito{
position:fixed;
right:18px;
bottom:85px;
background:#e53935;
color:white;
font-size:12px;
font-weight:bold;
width:24px;
height:24px;
border-radius:50%;
display:flex;
justify-content:center;
align-items:center;
z-index:1001;
box-shadow:0 2px 6px rgba(0,0,0,.3);
}

#chat{
display:none;
position:fixed;
right:20px;
bottom:115px;
width:330px;
background:white;
border-radius:20px;
overflow:hidden;
box-shadow:0 8px 25px rgba(0,0,0,.25);
z-index:1000;
}

.chat-header{
background:var(--marron);
color:white;
padding:15px;
display:flex;
justify-content:space-between;
align-items:center;
font-weight:bold;
}

.chat-body{
height:260px;
overflow-y:auto;
padding:12px;
background:#fffafc;
}

.chat-msg{
padding:9px 12px;
background:#efefef;
border-radius:12px;
margin-bottom:8px;
font-size:14px;
line-height:1.4;
}

.bot{
background:#ffe7f1;
color:#4a2c18;
}

.sugerencias{
display:flex;
gap:5px;
flex-wrap:wrap;
padding:6px 10px;
background:#fff;
border-top:1px solid #eee;
}

.sugerencias button{
background:#ffd9e8;
color:var(--marron);
font-size:11px;
padding:5px 8px;
border-radius:15px;
}

.chat-input-area{
display:flex;
padding:8px;
gap:6px;
background:white;
border-top:1px solid #eee;
}

.chat-input-area input{
margin:0;
padding:9px;
}

</style>
</head>

<body>

<!-- NOTIFICACIÓN DE PEDIDO -->
<div id="notificacion">
  <h3>🔔 ¡Nuevo Pedido Confirmado!</h3>
  <p id="notifTexto"></p>
  <a id="linkWsp" class="btn-wsp" href="#" target="_blank">📲 Enviar por WhatsApp</a>
  <button onclick="cerrarNotif()" style="background:#ccc;color:#333;padding:6px 10px;font-size:12px;margin-left:5px;">Cerrar</button>
</div>

<header>
  <img src="imagenes/logo.png.png" alt="Logo MELMET" class="logo">
</header>

<section class="hero">
  <div class="banana b1">🍌</div>
  <div class="banana b2">🍌</div>
  <div class="banana b3">🍌</div>

  <h1>MELMET</h1>

  <p>
    Shots saludables personalizados.
    Sabor, energía y nutrición.
  </p>

  <button onclick="document.getElementById('combos').scrollIntoView({behavior:'smooth'})">
    Pedir Ahora
  </button>
</section>

<div class="banner">
  🎉 15% OFF EN EFECTIVO CONTADO 💵 | 10% OFF POR TRANSFERENCIA 🏦
</div>

<div class="container">

  <!-- SEGUIMIENTO DEL PEDIDO EN VIVO (Aparece al confirmar compra) -->
  <div class="seccion" id="seccionSeguimiento">
    <div class="header-seguimiento">
      <h2>🛵 Estado y Seguimiento de tu Pedido</h2>
      <span class="codigo-pedido" id="codigoPedidoTexto">Pedido #MLM-000</span>
    </div>

    <p id="textoEstadoActual" style="font-size:17px;color:var(--verde);font-weight:bold;">
      ✅ ¡Recibimos tu pedido! En breve comenzamos a prepararlo.
    </p>

    <div class="barra-progreso-contenedor">
      <div class="barra-progreso" id="barraProgreso"></div>
    </div>

    <div class="pasos-seguimiento">
      <div class="paso activo" id="paso1">
        <span class="paso-icono">📋</span>
        1. Pedido Recibido<br>
        <small>Orden ingresada en sistema</small>
      </div>
      <div class="paso" id="paso2">
        <span class="paso-icono">🥤</span>
        2. Preparando Shots<br>
        <small>Licuando ingredientes frescos</small>
      </div>
      <div class="paso" id="paso3">
        <span class="paso-icono">🛵</span>
        3. En Camino<br>
        <small id="subtextoPaso3">Yendo hacia tu ubicación</small>
      </div>
      <div class="paso" id="paso4">
        <span class="paso-icono">🎉</span>
        4. ¡Entregado!<br>
        <small>¡A disfrutar tu MELMET!</small>
      </div>
    </div>

    <div class="detalle-entrega-box" id="resumenSeguimiento"></div>

    <button type="button" class="btn-simular" onclick="avanzarEstadoManual()">
      ⏩ Avanzar estado (Demo en vivo)
    </button>
  </div>

  <!-- DATOS DEL CLIENTE Y PUNTO DE ENTREGA -->
  <div class="seccion">
    <h2>👤 Tus Datos y Distribución</h2>
    <input id="nombre" placeholder="Tu Nombre y Apellido">
    <input id="telefono" placeholder="Teléfono / WhatsApp">

    <label><strong>📍 Modalidad de Entrega:</strong></label>
    <select id="tipoEntrega" onchange="cambiarTipoEntrega()">
      <option value="domicilio">🏠 Envío a Domicilio</option>
      <option value="encuentro">🤝 Punto de Encuentro</option>
    </select>

    <div id="boxDomicilio">
      <input id="direccion" placeholder="Dirección exacta de entrega (Calle, número, piso)">
    </div>

    <div id="boxEncuentro" style="display:none;">
      <select id="puntoEncuentroSelect" onchange="verificarOtroPunto()">
        <option value="Plaza San Martín">📍 Plaza San Martín</option>
        <option value="Costanera / Puente Colgante">📍 Costanera / Puente Colgante</option>
        <option value="Peatonal San Martín">📍 Peatonal San Martín</option>
        <option value="Ciudad Universitaria / Facultad">📍 Ciudad Universitaria / Facultad</option>
        <option value="otro">✏️ Otro punto de encuentro...</option>
      </select>
      <input id="otroPuntoInput" style="display:none;" placeholder="Escribí el punto de encuentro y horario sugerido">
    </div>
  </div>

  <!-- COMBOS Y PROMOCIONES -->
  <div class="seccion" id="combos">
    <h2>🔥 Combos y Promociones</h2>

    <div class="productos">
      <div class="card">
        <span class="etiqueta-promo">2x1 IMPERDIBLE</span>
        <img src="https://images.unsplash.com/photo-1499636136210-6f4ee915583e?w=800">
        <div class="card-content">
          <h3>🍌 Promo 2x1 Shot Banana</h3>
          <p class="descripcion-prod">Llevás 2 Shots Banana naturales al precio de 1.</p>
          <div class="info-nutri">🌱 Banana, avena, miel pura y canela.</div>
          <select id="ing-promo2x1" class="select-ingrediente">
            <option value="Receta estándar">✨ Ingredientes: Estándar</option>
            <option value="Extra Banana y Canela">🍌 Extra Banana y Canela</option>
            <option value="Sin Miel (100% Vegano)">🌿 Sin Miel (Vegano)</option>
            <option value="Extra Avena proteica">💪 Extra Avena</option>
          </select>
          <div class="precio-tachado">$3000</div>
          <div class="precio">$1500</div>
          <button onclick="agregar('Promo 2x1 Shot Banana',1500,'ing-promo2x1')">Agregar Promo</button>
        </div>
      </div>

      <div class="card">
        <span class="etiqueta-promo">AHORRÁ $500</span>
        <img src="https://images.unsplash.com/photo-1553530666-ba11a7da3888?w=800">
        <div class="card-content">
          <h3>⚡ Combo Dúo Energía</h3>
          <p class="descripcion-prod">1 Shot Banana + 1 Shot Energético para arrancar con todo.</p>
          <div class="info-nutri">⚡ Potasio + Jengibre, naranja y cúrcuma.</div>
          <select id="ing-duo" class="select-ingrediente">
            <option value="Receta estándar">✨ Ingredientes: Estándar</option>
            <option value="Extra Jengibre intenso">🔥 Extra Jengibre intenso</option>
            <option value="Suave (poco jengibre)">🍯 Suave (poco jengibre)</option>
          </select>
          <div class="precio-tachado">$3300</div>
          <div class="precio">$2800</div>
          <button onclick="agregar('Combo Dúo Energía',2800,'ing-duo')">Agregar Combo</button>
        </div>
      </div>

      <div class="card">
        <span class="etiqueta-promo">PACK SEMANAL</span>
        <img src="https://images.unsplash.com/photo-1505252585461-04db1eb84625?w=800">
        <div class="card-content">
          <h3>📦 Pack x5 Shots Surtidos</h3>
          <p class="descripcion-prod">3 Shot Banana + 2 Shot Energético listos para tu semana.</p>
          <div class="info-nutri">❄️ Conservación en heladera hasta 5 días.</div>
          <select id="ing-pack5" class="select-ingrediente">
            <option value="3 Banana + 2 Energético">✨ Mix: 3 Banana + 2 Energético</option>
            <option value="5 Shot Banana">🍌 Todos Shot Banana (x5)</option>
            <option value="5 Shot Energético">⚡ Todos Shot Energético (x5)</option>
          </select>
          <div class="precio-tachado">$8100</div>
          <div class="precio">$6500</div>
          <button onclick="agregar('Pack x5 Shots Surtidos',6500,'ing-pack5')">Agregar Pack</button>
        </div>
      </div>
    </div>
  </div>

  <!-- PRODUCTOS INDIVIDUALES -->
  <div class="seccion" id="catalogo">
    <h2>🥤 Shots Individuales (Personalizables)</h2>

    <div class="productos">
      <div class="card">
        <img src="https://images.unsplash.com/photo-1499636136210-6f4ee915583e?w=800">
        <div class="card-content">
          <h3>🍌 Shot Banana</h3>
          <p class="descripcion-prod">Cremoso, dulce natural y lleno de potasio.</p>
          <div class="info-nutri">📊 110 kcal | 100% fruta natural</div>
          <select id="ing-banana" class="select-ingrediente">
            <option value="Receta estándar">✨ Ingredientes: Estándar</option>
            <option value="Extra Banana">🍌 Extra Banana</option>
            <option value="Extra Canela y Avena">🌾 Extra Canela y Avena</option>
            <option value="Sin Miel">🌿 Sin Miel</option>
          </select>
          <div class="precio">$1500</div>
          <button onclick="agregar('Shot Banana',1500,'ing-banana')">Agregar</button>
        </div>
      </div>

      <div class="card">
        <img src="https://images.unsplash.com/photo-1464306076886-da185f6a9d05?w=800">
        <div class="card-content">
          <h3>⚡ Shot Energético</h3>
          <p class="descripcion-prod">Mix natural revitalizante para entrenar o estudiar.</p>
          <div class="info-nutri">📊 85 kcal | Naranja, jengibre, cúrcuma y miel</div>
          <select id="ing-energetico" class="select-ingrediente">
            <option value="Receta estándar">✨ Ingredientes: Estándar</option>
            <option value="Doble Jengibre y Cúrcuma">🔥 Doble Jengibre y Cúrcuma</option>
            <option value="Más Naranja (más dulce)">🍊 Más Naranja (suave)</option>
            <option value="Sin Miel">🌿 Sin Miel</option>
          </select>
          <div class="precio">$1800</div>
          <button onclick="agregar('Shot Energético',1800,'ing-energetico')">Agregar</button>
        </div>
      </div>
    </div>
  </div>

  <!-- CARRITO Y PAGO -->
  <div class="seccion">
    <h2>🛒 Mi Carrito y Beneficios de Pago</h2>

    <ul id="carrito"></ul>

    <div class="promo-pagos-info">
      <div class="pill-descuento">💵 Efectivo Contado: 15% OFF</div>
      <div class="pill-descuento">🏦 Transferencia: 10% OFF</div>
    </div>

    <label><strong>💳 Elegí cómo querés pagar para aplicar tu descuento:</strong></label>
    <select id="metodoPago" onchange="actualizarTotalesYForm()">
      <option value="">-- Seleccionar medio de pago --</option>
      <option value="efectivo">💵 Efectivo Contado (15% de descuento)</option>
      <option value="transferencia">🏦 Transferencia Bancaria / Mercado Pago (10% de descuento)</option>
      <option value="tarjeta">💳 Tarjeta de Débito / Crédito (Precio de lista)</option>
    </select>

    <!-- DATOS DE EFECTIVO -->
    <div id="boxEfectivo" class="pago-box">
      <h3 style="color:var(--marron);margin-bottom:8px;">💵 Pago en Efectivo Contado (15% OFF aplicado):</h3>
      <p style="font-size:14px;color:#444;margin-bottom:8px;">Pagás al recibir tu pedido o en el punto de encuentro.</p>
      <input id="pagaCon" type="number" placeholder="¿Con cuánto abonás? (Ej: 5000 - para llevarte cambio exacto)">
    </div>

    <!-- DATOS DE TRANSFERENCIA (CBU / ALIAS) -->
    <div id="boxTransferencia" class="pago-box">
      <h3 style="color:var(--marron);margin-bottom:8px;">🏦 Datos para transferir (10% OFF aplicado):</h3>
      <div class="dato-banco">
        <span><strong>Titular:</strong> MELMET Shots Saludables</span>
      </div>
      <div class="dato-banco">
        <span><strong>Banco / Billetera:</strong> Mercado Pago</span>
      </div>
      <div class="dato-banco">
        <span><strong>Alias:</strong> <span id="aliasTexto">MELMET.SHOTS.MP</span></span>
        <button type="button" class="btn-copiar" onclick="copiarTexto('aliasTexto')">Copiar Alias</button>
      </div>
      <div class="dato-banco">
        <span><strong>CBU / CVU:</strong> <span id="cbuTexto">0000003100084592014728</span></span>
        <button type="button" class="btn-copiar" onclick="copiarTexto('cbuTexto')">Copiar CBU</button>
      </div>
      <input id="comprobanteNombre" placeholder="Nombre del titular desde donde transferís (opcional)">
    </div>

    <!-- DATOS DE TARJETA -->
    <div id="boxTarjeta" class="pago-box">
      <h3 style="color:var(--marron);margin-bottom:8px;">💳 Ingresá los datos de tu tarjeta:</h3>
      <input id="numTarjeta" maxlength="19" placeholder="Número de tarjeta (Ej: 4509 1234 5678 9010)">
      <input id="titularTarjeta" placeholder="Nombre como figura en la tarjeta">
      <div class="fila-tarjeta">
        <input id="vencTarjeta" maxlength="5" placeholder="Vencimiento (MM/AA)">
        <input id="cvvTarjeta" maxlength="4" type="password" placeholder="CVV (3 dígitos)">
      </div>
    </div>

    <!-- RESUMEN DE PRECIO CON DESCUENTO -->
    <div class="resumen-totales">
      <div class="linea-subtotal">Subtotal: $<span id="subtotal">0</span></div>
      <div class="linea-descuento" id="lineaDescuento">🎉 Descuento aplicado: -$<span id="montoDescuento">0</span></div>
      <div class="total">Total a pagar: $<span id="totalFinal">0</span></div>
    </div>

    <button class="btn-confirmar" onclick="confirmarPedido()">
      ✅ Confirmar Pedido y Ver Seguimiento
    </button>
  </div>

</div>

<!-- CHAT DE COQUITO -->
<div id="chat">
  <div class="chat-header">
    <span>🐵 Coquito - Asistente MELMET</span>
    <span style="cursor:pointer;" onclick="toggleChat()">✖</span>
  </div>

  <div class="chat-body" id="chatBody">
    <div class="chat-msg bot">
      ¡Hola! Soy Coquito 🍌 Preguntame por nuestros <b>combos</b>, <b>puntos de encuentro</b>, el <b>estado de tu pedido</b> o los descuentos en <b>efectivo/transferencia</b>.
    </div>
  </div>

  <!-- BOTONES RÁPIDOS -->
  <div class="sugerencias">
    <button onclick="preguntaRapida('¿Cómo va mi pedido?')">🛵 Estado Pedido</button>
    <button onclick="preguntaRapida('¿Cuáles son los puntos de encuentro?')">📍 Puntos Encuentro</button>
    <button onclick="preguntaRapida('¿Qué promo hay en efectivo?')">💵 Efectivo 15%</button>
    <button onclick="preguntaRapida('¿Cómo pago con transferencia?')">🏦 Transf. 10%</button>
  </div>

  <div class="chat-input-area">
    <input id="pregunta" placeholder="Escribí tu pregunta..." onkeypress="if(event.key==='Enter') preguntar()">
    <button onclick="preguntar()">Enviar</button>
  </div>
</div>

<!-- BURBUJA FLOTANTE -->
<div class="badge-coquito" id="badgeCoquito">1</div>
<div id="coquito" onclick="toggleChat()">
  <img src="imagenes/logo.png.png" alt="Coquito">
</div>

<script>

let subtotal = 0;
let totalFinal = 0;
let descuentoAplicado = 0;
let itemsPedido = [];

// Variables de seguimiento
let pedidoConfirmado = false;
let pasoActual = 0;
let codigoOrden = "";
let intervaloSeguimiento = null;

function toggleChat(){
  let chat = document.getElementById("chat");
  let badge = document.getElementById("badgeCoquito");
  if(chat.style.display === "block"){
    chat.style.display = "none";
  } else {
    chat.style.display = "block";
    badge.style.display = "none";
  }
}

/* TIPO DE ENTREGA: DOMICILIO O PUNTO DE ENCUENTRO */

function cambiarTipoEntrega(){
  let tipo = document.getElementById("tipoEntrega").value;
  if(tipo === "domicilio"){
    document.getElementById("boxDomicilio").style.display = "block";
    document.getElementById("boxEncuentro").style.display = "none";
  } else {
    document.getElementById("boxDomicilio").style.display = "none";
    document.getElementById("boxEncuentro").style.display = "block";
  }
}

function verificarOtroPunto(){
  let sel = document.getElementById("puntoEncuentroSelect").value;
  document.getElementById("otroPuntoInput").style.display = (sel === "otro") ? "block" : "none";
}

/* CARRITO CON PERSONALIZACIÓN DE INGREDIENTES */

function agregar(nombre, precio, idSelectIng){
  let detalleIng = "Receta estándar";
  if(idSelectIng && document.getElementById(idSelectIng)){
    detalleIng = document.getElementById(idSelectIng).value;
  }
  itemsPedido.push({nombre, precio, detalleIng});
  actualizarCarrito();
}

function eliminarItem(index){
  itemsPedido.splice(index, 1);
  actualizarCarrito();
}

function actualizarCarrito(){
  let lista = document.getElementById("carrito");
  lista.innerHTML = "";
  subtotal = 0;

  itemsPedido.forEach((item, index) => {
    subtotal += item.precio;
    lista.innerHTML += `
      <li>
        <div>
          <strong>${item.nombre}</strong> - <strong>$${item.precio}</strong><br>
          <small style="color:#666;">🌿 ${item.detalleIng}</small>
        </div>
        <button class="btn-eliminar" onclick="eliminarItem(${index})">Quitar</button>
      </li>
    `;
  });

  actualizarTotalesYForm();
}

/* CALCULAR DESCUENTOS Y MOSTRAR FORMULARIO DE PAGO */

function actualizarTotalesYForm(){
  let metodo = document.getElementById("metodoPago").value;

  document.getElementById("boxEfectivo").style.display = "none";
  document.getElementById("boxTransferencia").style.display = "none";
  document.getElementById("boxTarjeta").style.display = "none";

  let porcentajeDesc = 0;

  if(metodo === "efectivo"){
    document.getElementById("boxEfectivo").style.display = "block";
    porcentajeDesc = 0.15; // 15% OFF
  } else if(metodo === "transferencia"){
    document.getElementById("boxTransferencia").style.display = "block";
    porcentajeDesc = 0.10; // 10% OFF
  } else if(metodo === "tarjeta"){
    document.getElementById("boxTarjeta").style.display = "block";
    porcentajeDesc = 0;
  }

  descuentoAplicado = Math.round(subtotal * porcentajeDesc);
  totalFinal = subtotal - descuentoAplicado;

  document.getElementById("subtotal").innerText = subtotal;
  document.getElementById("totalFinal").innerText = totalFinal;

  let lineaDesc = document.getElementById("lineaDescuento");
  if(descuentoAplicado > 0){
    lineaDesc.style.display = "block";
    document.getElementById("montoDescuento").innerText = descuentoAplicado;
  } else {
    lineaDesc.style.display = "none";
  }
}

function copiarTexto(idElemento){
  let texto = document.getElementById(idElemento).innerText;
  navigator.clipboard.writeText(texto);
  alert("✅ Copiado: " + texto);
}

/* CONFIRMAR PEDIDO, NOTIFICACIÓN Y SEGUIMIENTO */

function confirmarPedido(){
  let nombre = document.getElementById("nombre").value.trim();
  let telefono = document.getElementById("telefono").value.trim();
  let tipoEntrega = document.getElementById("tipoEntrega").value;
  let metodo = document.getElementById("metodoPago").value;

  let lugarEntrega = "";
  if(tipoEntrega === "domicilio"){
    lugarEntrega = document.getElementById("direccion").value.trim();
  } else {
    let selPunto = document.getElementById("puntoEncuentroSelect").value;
    if(selPunto === "otro"){
      lugarEntrega = "Punto de encuentro: " + document.getElementById("otroPuntoInput").value.trim();
    } else {
      lugarEntrega = "Punto de encuentro: " + selPunto;
    }
  }

  if(itemsPedido.length === 0){
    alert("🍌 ¡Agregá al menos un combo o shot al carrito antes de confirmar!");
    return;
  }

  if(!nombre || !lugarEntrega || lugarEntrega === "Punto de encuentro: "){
    alert("👤 Por favor completá tu nombre y la dirección o punto de encuentro.");
    return;
  }

  if(!metodo){
    alert("💳 Por favor seleccioná un medio de pago (Efectivo, Transferencia o Tarjeta).");
    return;
  }

  if(metodo === "tarjeta"){
    let num = document.getElementById("numTarjeta").value.trim();
    let tit = document.getElementById("titularTarjeta").value.trim();
    let venc = document.getElementById("vencTarjeta").value.trim();
    let cvv = document.getElementById("cvvTarjeta").value.trim();
    if(!num || !tit || !venc || !cvv){
      alert("💳 Completá todos los datos de tu tarjeta para continuar.");
      return;
    }
  }

  let detalleProductos = itemsPedido.map(i => `${i.nombre} [${i.detalleIng}] ($${i.precio})`).join(", ");
  let textoPago = "";
  let infoExtra = "";

  if(metodo === "efectivo"){
    textoPago = "Efectivo Contado (15% OFF)";
    let pagaCon = document.getElementById("pagaCon").value;
    if(pagaCon && Number(pagaCon) >= totalFinal){
      let vuelto = Number(pagaCon) - totalFinal;
      infoExtra = ` (Abona con $${pagaCon} - Vuelto: $${vuelto})`;
    }
  } else if(metodo === "transferencia"){
    textoPago = "Transferencia Bancaria (10% OFF)";
  } else {
    textoPago = "Tarjeta Débito/Crédito";
  }

  // Generar código de orden único
  let numRandom = Math.floor(100 + Math.random() * 900);
  codigoOrden = `MLM-${numRandom}`;
  pedidoConfirmado = true;

  // 1. Mostrar notificación visual arriba a la derecha
  let notif = document.getElementById("notificacion");
  let notifTexto = document.getElementById("notifTexto");
  notifTexto.innerHTML = `
    <strong>Orden:</strong> #${codigoOrden}<br>
    <strong>Cliente:</strong> ${nombre}<br>
    <strong>Pedido:</strong> ${detalleProductos}<br>
    <strong>Total Final:</strong> $${totalFinal}<br>
    <strong>Pago:</strong> ${textoPago}${infoExtra}<br>
    <strong>Entrega:</strong> ${lugarEntrega}
  `;

  let mensajeWsp = encodeURIComponent(
    `¡Hola MELMET! 🍌 Hice el pedido #${codigoOrden}:\n• Nombre: ${nombre}\n• Pedido: ${detalleProductos}\n• Descuento: -$${descuentoAplicado}\n• Total Final: $${totalFinal}\n• Pago: ${textoPago}${infoExtra}\n• Entrega: ${lugarEntrega}`
  );
  document.getElementById("linkWsp").href = `https://wa.me/5493420000000?text=${mensajeWsp}`;
  notif.style.display = "block";

  // 2. Activar panel de Seguimiento en vivo
  iniciarSeguimiento(nombre, detalleProductos, totalFinal, textoPago, lugarEntrega, tipoEntrega);

  // 3. Coquito también avisa en el chat
  let chatBody = document.getElementById("chatBody");
  chatBody.innerHTML += `
    <div class="chat-msg bot">
      🔔 <strong>¡Pedido #${codigoOrden} confirmado, ${nombre}!</strong><br>
      Ya activamos el seguimiento en pantalla. Entrega en: <strong>${lugarEntrega}</strong>. 🍌🥤
    </div>
  `;
  document.getElementById("chat").style.display = "block";
  chatBody.scrollTop = chatBody.scrollHeight;
}

/* LÓGICA DEL SEGUIMIENTO DEL ENVÍO */

function iniciarSeguimiento(nombre, detalle, total, pago, entrega, tipoEntrega){
  let secSeg = document.getElementById("seccionSeguimiento");
  secSeg.style.display = "block";
  document.getElementById("codigoPedidoTexto").innerText = `Orden #${codigoOrden}`;

  document.getElementById("subtextoPaso3").innerText =
    tipoEntrega === "encuentro" ? "Yendo al punto de encuentro" : "Repartidor en camino a tu domicilio";

  document.getElementById("resumenSeguimiento").innerHTML = `
    <strong>👤 Cliente:</strong> ${nombre}<br>
    <strong>📍 Destino:</strong> ${entrega}<br>
    <strong>🥤 Detalle:</strong> ${detalle}<br>
    <strong>💳 Pago:</strong> ${pago} — <strong>Total: $${total}</strong>
  `;

  pasoActual = 1;
  actualizarVistaPasos();
  secSeg.scrollIntoView({behavior: "smooth"});

  // Avanza automáticamente cada 8 segundos para simular el seguimiento real
  if(intervaloSeguimiento) clearInterval(intervaloSeguimiento);
  intervaloSeguimiento = setInterval(() => {
    if(pasoActual < 4){
      pasoActual++;
      actualizarVistaPasos();
    } else {
      clearInterval(intervaloSeguimiento);
    }
  }, 8000);
}

function avanzarEstadoManual(){
  if(pasoActual < 4){
    pasoActual++;
    actualizarVistaPasos();
  }
}

function actualizarVistaPasos(){
  let barra = document.getElementById("barraProgreso");
  let textoEstado = document.getElementById("textoEstadoActual");

  for(let i = 1; i <= 4; i++){
    let el = document.getElementById("paso" + i);
    el.classList.remove("activo", "completado");
    if(i < pasoActual){
      el.classList.add("completado");
    } else if(i === pasoActual){
      el.classList.add("activo");
    }
  }

  if(pasoActual === 1){
    barra.style.width = "25%";
    textoEstado.innerText = "📋 Estado: Pedido recibido. En breve comenzamos a prepararlo.";
  } else if(pasoActual === 2){
    barra.style.width = "50%";
    textoEstado.innerText = "🥤 Estado: ¡Estamos preparando tus shots frescos con tus ingredientes elegidos!";
  } else if(pasoActual === 3){
    barra.style.width = "75%";
    textoEstado.innerText = "🛵 Estado: ¡Tu pedido salió! Está en camino hacia el punto de entrega.";
  } else if(pasoActual === 4){
    barra.style.width = "100%";
    textoEstado.innerText = "🎉 Estado: ¡Pedido entregado! Gracias por elegir MELMET 🍌.";
  }
}

function cerrarNotif(){
  document.getElementById("notificacion").style.display = "none";
}

/* CHAT INTELIGENTE DE COQUITO */

function preguntaRapida(texto){
  document.getElementById("pregunta").value = texto;
  preguntar();
}

function preguntar(){
  let input = document.getElementById("pregunta");
  let textoOriginal = input.value.trim();
  if(!textoOriginal) return;

  let pregunta = textoOriginal.toLowerCase();
  let respuesta = "";

  if(pregunta.includes("hola") || pregunta.includes("buenas")){
    respuesta = "¡Hola! Soy Coquito 🐵🍌 ¿Querés conocer nuestros combos, los puntos de encuentro o el estado de tu pedido?";
  }
  else if(pregunta.includes("estado") || pregunta.includes("seguimiento") || pregunta.includes("mi pedido") || pregunta.includes("donde")){
    if(!pedidoConfirmado){
      respuesta = "Todavía no confirmaste ningún pedido 🍌. Agregá tus shots al carrito, elegí cómo pagar y tocá <b>Confirmar Pedido</b> para ver el seguimiento en vivo.";
    } else {
      let estadosTexto = [
        "",
        "📋 Tu orden <b>#" + codigoOrden + "</b> fue <b>recibida</b> y está en cola.",
        "🥤 ¡Estamos <b>preparando</b> tus shots frescos ahora mismo!",
        "🛵 ¡Tu orden <b>#" + codigoOrden + "</b> ya está <b>en camino</b>!",
        "🎉 ¡Tu pedido <b>#" + codigoOrden + "</b> ya fue <b>entregado</b>!"
      ];
      respuesta = estadosTexto[pasoActual];
    }
  }
  else if(pregunta.includes("punto") || pregunta.includes("encuentro") || pregunta.includes("retiro")){
    respuesta = "🤝 ¡Sí! Podés elegir <b>Punto de Encuentro</b> en <i>Tus Datos y Distribución</i> (Plaza San Martín, Costanera, Peatonal, Ciudad Universitaria o el que vos nos indiques).";
  }
  else if(pregunta.includes("ingrediente") || pregunta.includes("personaliz")){
    respuesta = "🌿 ¡Podés personalizar tus shots! Antes de agregar cada producto al carrito elegí en el menú desplegable si querés extra banana, doble jengibre, sin miel o extra avena.";
  }
  else if(pregunta.includes("combo") || pregunta.includes("pack") || pregunta.includes("promo")){
    respuesta = "🔥 Tenemos 3 promos activas:<br>• <b>Promo 2x1 Shot Banana:</b> $1500<br>• <b>Combo Dúo Energía:</b> $2800<br>• <b>Pack x5 Shots Surtidos:</b> $6500<br>¡Y además sumás descuento por pago!";
  }
  else if(pregunta.includes("efectivo") || pregunta.includes("contado")){
    respuesta = "💵 ¡Pagando en <b>Efectivo Contado</b> tenés un <b>15% de descuento</b> automático en todo tu carrito!";
  }
  else if(pregunta.includes("transferencia") || pregunta.includes("cbu") || pregunta.includes("alias")){
    respuesta = "🏦 ¡Pagando por <b>Transferencia</b> tenés un <b>10% de descuento</b>! Elegila en el carrito y te aparecen nuestro Alias (<b>MELMET.SHOTS.MP</b>) y CBU.";
  }
  else if(pregunta.includes("tarjeta") || pregunta.includes("credito") || pregunta.includes("debito")){
    respuesta = "💳 Aceptamos tarjeta de débito y crédito a precio de lista. Podés cargar los datos directo en el carrito.";
  }
  else if(pregunta.includes("envio") || pregunta.includes("delivery") || pregunta.includes("entregan")){
    respuesta = "🛵 Hacemos envíos a domicilio o entregas en puntos de encuentro. ¡Y podés seguir el estado de tu envío en tiempo real desde la app!";
  }
  else {
    respuesta = "🐵 Preguntame por el <b>estado de tu pedido</b>, <b>puntos de encuentro</b>, <b>ingredientes</b>, <b>efectivo (15% OFF)</b> o <b>transferencia (10% OFF)</b> 🍌.";
  }

  let chatBody = document.getElementById("chatBody");
  chatBody.innerHTML += `<div class="chat-msg">🧑 ${textoOriginal}</div>`;
  chatBody.innerHTML += `<div class="chat-msg bot">${respuesta}</div>`;

  input.value = "";
  chatBody.scrollTop = chatBody.scrollHeight;
}

</script>

</body>
</html>
