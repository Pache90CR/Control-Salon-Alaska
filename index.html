<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Bar Restaurante Alaska - Control Total</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        .hide-scrollbar::-webkit-scrollbar { display: none; }
        .hide-scrollbar { -ms-overflow-style: none; scrollbar-width: none; }
        .pro-scroll::-webkit-scrollbar { width: 6px; }
        .pro-scroll::-webkit-scrollbar-track { background: #0f172a; border-radius: 8px; }
        .pro-scroll::-webkit-scrollbar-thumb { background: #334155; border-radius: 8px; }
        .pro-scroll::-webkit-scrollbar-thumb:hover { background: #475569; }
    </style>
</head>
<body class="bg-slate-900 text-white font-sans antialiased h-screen flex flex-col overflow-hidden w-full max-w-[100vw] selection:bg-amber-500 selection:text-slate-900">

    <!-- MODAL DE INGRESO -->
    <div id="modal-login" class="fixed inset-0 bg-slate-950 z-50 flex items-center justify-center p-4">
        <div class="bg-slate-900 border border-slate-700 p-8 rounded-3xl w-full max-w-sm shadow-2xl shadow-black/50 text-center">
            <img src="179967.png" alt="Logo Alaska" class="w-32 h-32 mx-auto mb-6 rounded-full shadow-lg shadow-black/40 border-4 border-slate-800 object-cover" onerror="this.src='https://via.placeholder.com/150/1e293b/fbbf24?text=Alaska'">
            <h2 class="text-2xl font-black mb-8 text-slate-100 tracking-tight">Restaurante Alaska</h2>
            <div class="space-y-4">
                <button onclick="seleccionarRol('salonero')" class="w-full bg-slate-800 hover:bg-slate-700 border border-slate-600 text-white font-bold py-4 rounded-xl transition shadow-lg flex items-center justify-center gap-3">
                    <i class="fa-solid fa-bell-concierge"></i> Ingreso Salonero
                </button>
                <button onclick="seleccionarRol('admin')" class="w-full bg-gradient-to-r from-amber-500 to-amber-600 hover:from-amber-400 hover:to-amber-500 text-slate-900 font-bold py-4 rounded-xl transition shadow-lg flex items-center justify-center gap-3">
                    <i class="fa-solid fa-lock"></i> Ingreso Administrador
                </button>
            </div>
            <p id="firebase-status" class="mt-6 text-xs text-slate-500 animate-pulse">Conectando a la nube...</p>
        </div>
    </div>

    <!-- MODAL DE APERTURA DE CAJA -->
    <div id="modal-caja" class="fixed inset-0 bg-slate-950/90 z-50 flex items-center justify-center p-4 hidden backdrop-blur-sm">
        <div class="bg-slate-900 border border-slate-700 p-8 rounded-3xl w-full max-w-md shadow-2xl">
            <h3 class="text-2xl font-black text-amber-400 mb-2"><i class="fa-solid fa-cash-register mr-2"></i> Apertura de Caja</h3>
            <p class="text-sm text-slate-400 mb-6">Fondo inicial (Base de efectivo):</p>
            <div class="relative mb-6">
                <span class="absolute left-4 top-3 text-slate-400 font-bold text-lg">₡</span>
                <input type="number" id="input-monto-caja" class="w-full bg-slate-950 border border-slate-700 rounded-xl pl-10 pr-4 py-3 text-xl font-bold text-emerald-400 focus:outline-none focus:border-amber-500" value="25000">
            </div>
            <button onclick="abrirCaja()" class="w-full bg-amber-500 hover:bg-amber-400 text-slate-900 font-bold py-4 rounded-xl transition text-lg">Abrir Turno</button>
        </div>
    </div>

    <!-- HEADER -->
    <header class="bg-slate-900 border-b border-slate-800 px-4 py-3 flex flex-col sm:flex-row justify-between sm:items-center shadow-lg gap-3 relative z-10 w-full overflow-hidden">
        <div class="flex items-center space-x-3">
            <img src="179967.png" alt="Logo Alaska" class="w-12 h-12 rounded-full border border-slate-700 object-cover" onerror="this.src='https://via.placeholder.com/48/1e293b/fbbf24?text=A'">
            <div>
                <h1 class="text-base font-bold tracking-wide text-slate-100">Bar Restaurante Alaska</h1>
                <p id="info-caja-header" class="text-xs text-emerald-500 font-bold hidden bg-emerald-500/10 inline-block px-2 py-0.5 rounded-full mt-1 border border-emerald-500/20">Caja abierta</p>
            </div>
        </div>
        <div class="flex overflow-x-auto bg-slate-950 p-1 rounded-xl border border-slate-800 hide-scrollbar shrink-0 w-full sm:w-auto">
            <button onclick="cambiarVista('barra')" id="btn-tab-barra" class="px-5 py-2 rounded-lg font-semibold transition bg-amber-500 text-slate-900 text-sm whitespace-nowrap">Barra</button>
            <button onclick="cambiarVista('mesas')" id="btn-tab-mesas" class="px-5 py-2 rounded-lg font-semibold transition text-slate-400 hover:text-white text-sm whitespace-nowrap">Mesas</button>
            <button onclick="cambiarVista('vip')" id="btn-tab-vip" class="px-5 py-2 rounded-lg font-semibold transition text-slate-400 hover:text-white text-sm whitespace-nowrap">VIP</button>
            <button onclick="cambiarVista('admin')" id="btn-tab-admin" class="px-5 py-2 rounded-lg font-semibold transition text-slate-400 hover:text-amber-400 text-sm whitespace-nowrap hidden"><i class="fa-solid fa-chart-line mr-1"></i> Admin</button>
        </div>
    </header>

    <!-- CONTENIDO PRINCIPAL -->
    <main class="flex-1 flex overflow-hidden relative bg-slate-950 w-full">
        <!-- SECCIÓN DE OPERACIÓN -->
        <section class="flex-1 p-4 md:p-6 overflow-y-auto pro-scroll w-full" id="area-operacion">
            <div class="flex flex-col sm:flex-row justify-between sm:items-center mb-6 gap-3">
                <h2 id="titulo-vista" class="text-2xl font-black text-slate-100">Control de Barra</h2>
                <div class="flex items-center gap-4 flex-wrap">
                    <button id="btn-agregar-barra" onclick="agregarClienteExtraBarra()" class="bg-emerald-600 hover:bg-emerald-500 text-white font-bold py-2 px-4 rounded-xl shadow-lg text-sm flex items-center gap-2">
                        <i class="fa-solid fa-user-plus"></i> Cliente Extra
                    </button>
                    <div class="flex gap-4 text-xs font-bold text-slate-400 bg-slate-900 px-4 py-2 rounded-xl border border-slate-800 shrink-0">
                        <span class="flex items-center gap-2"><span class="w-3 h-3 rounded-full bg-emerald-500"></span> Libre</span>
                        <span class="flex items-center gap-2"><span class="w-3 h-3 rounded-full bg-rose-500"></span> Ocupada</span>
                    </div>
                </div>
            </div>
            <div id="grid-elementos" class="grid grid-cols-2 md:grid-cols-3 xl:grid-cols-4 gap-4 md:gap-5 pb-20 w-full"></div>
        </section>

        <!-- SECCIÓN ADMIN -->
        <section class="flex-1 overflow-hidden hidden flex-col w-full bg-slate-950" id="area-admin">
            <div class="border-b border-slate-800 bg-slate-900 px-4 py-3 flex gap-6 overflow-x-auto hide-scrollbar w-full">
                <button onclick="cambiarSubVistaAdmin('caja')" id="btn-admin-caja" class="pb-2 text-amber-500 border-b-2 border-amber-500 font-bold whitespace-nowrap">Resumen de Caja</button>
                <button onclick="cambiarSubVistaAdmin('menu')" id="btn-admin-menu" class="pb-2 text-slate-400 border-b-2 border-transparent hover:text-slate-200 font-bold whitespace-nowrap">Gestión de Menú</button>
                <button onclick="cambiarSubVistaAdmin('espacios')" id="btn-admin-espacios" class="pb-2 text-slate-400 border-b-2 border-transparent hover:text-slate-200 font-bold whitespace-nowrap">Mesas y Zonas</button>
            </div>
            <div id="contenedor-admin" class="flex-1 p-4 md:p-6 overflow-y-auto pro-scroll w-full"></div>
        </section>

        <!-- PANEL LATERAL DE CUENTA -->
        <aside id="panel-cuenta" class="fixed inset-y-0 right-0 w-full md:w-96 bg-slate-900 border-l border-slate-800 flex-col justify-between shadow-2xl z-40 hidden transition-all">
            <div class="p-5 border-b border-slate-800 flex justify-between items-center bg-slate-900">
                <div class="w-full overflow-hidden pr-4">
                    <h3 id="panel-cliente" class="text-xl font-black text-amber-400 truncate">Nombre Cliente</h3>
                    <p id="panel-titulo" class="text-xs text-slate-400 font-medium bg-slate-800 inline-block px-2 py-1 rounded-md mt-1">Ubicación</p>
                </div>
                <button onclick="cerrarPanel()" class="text-slate-400 hover:text-white p-2 text-2xl shrink-0"><i class="fa-solid fa-xmark"></i></button>
            </div>
            <div class="flex-1 p-4 overflow-y-auto pro-scroll bg-slate-900/50">
                <div id="lista-items-cuenta" class="space-y-2"></div>
            </div>
            <div class="p-5 border-t border-slate-800 bg-slate-900">
                <div class="flex justify-between items-center mb-4 text-xl font-black">
                    <span class="text-slate-300">Total:</span>
                    <span id="panel-total" class="text-emerald-400">₡0</span>
                </div>
                <div class="grid grid-cols-2 gap-3">
                    <button onclick="abrirModalAgregar()" class="bg-slate-800 hover:bg-slate-700 text-amber-400 font-bold py-4 rounded-xl border border-slate-700 transition flex items-center justify-center gap-2">
                        <i class="fa-solid fa-cart-plus"></i> Agregar
                    </button>
                    <button onclick="cobrarCuenta()" class="bg-gradient-to-r from-emerald-500 to-emerald-600 hover:from-emerald-400 text-white font-bold py-4 rounded-xl transition flex items-center justify-center gap-2">
                        <i class="fa-solid fa-check-double"></i> Cobrar
                    </button>
                </div>
            </div>
        </aside>
    </main>

    <!-- SCRIPT FIREBASE -->
    <script type="module">
        import { initializeApp } from "https://www.gstatic.com/firebasejs/10.8.0/firebase-app.js";
        import { getFirestore, collection, onSnapshot, doc, updateDoc, addDoc, deleteDoc, setDoc } from "https://www.gstatic.com/firebasejs/10.8.0/firebase-firestore.js";

        // CREDENCIALES DEL PROYECTO BAR ALASKA
        const firebaseConfig = {
            apiKey: "AIzaSyBrVAO_tc3pU7wehVEX9q-JUMkSOkTAdG8",
            authDomain: "bar-alaska.firebaseapp.com",
            projectId: "bar-alaska",
            storageBucket: "bar-alaska.firebasestorage.app",
            messagingSenderId: "634346870517",
            appId: "1:634346870517:web:82d806af82d04d8c3297bc",
            measurementId: "G-WB0G1KFX6K"
        };

        const app = initializeApp(firebaseConfig);
        const db = getFirestore(app);

        let vistaActual = 'barra';
        let adminSubVista = 'caja';
        let elementoSeleccionado = null;
        let rolUsuario = '';
        let montoCajaInicial = 0;
        let ventasTotalesTurno = 0; 
        let busquedaMenu = '';

        let datosRestaurante = { barra: [], mesas: [], vip: [], productos: [] };

        // Confirmar Conexión
        document.getElementById('firebase-status').innerText = "Conectado a bar-alaska ✅";
        document.getElementById('firebase-status').classList.remove('animate-pulse');
        document.getElementById('firebase-status').classList.add('text-emerald-500');

        // Escuchar Espacios
        onSnapshot(collection(db, "espacios"), (snapshot) => {
            datosRestaurante.barra = [];
            datosRestaurante.mesas = [];
            datosRestaurante.vip = [];
            
            snapshot.forEach((doc) => {
                const data = doc.data();
                data.id = doc.id;
                if(data.categoria === 'barra') datosRestaurante.barra.push(data);
                else if(data.categoria === 'mesas') datosRestaurante.mesas.push(data);
                else if(data.categoria === 'vip') datosRestaurante.vip.push(data);
            });
            if(rolUsuario) {
                if(vistaActual === 'admin') renderizarModuloAdmin();
                else renderizarGridOperacion();
            }
        });

        // Escuchar Productos
        onSnapshot(collection(db, "productos"), (snapshot) => {
            datosRestaurante.productos = [];
            snapshot.forEach((doc) => {
                const data = doc.data();
                data.id = doc.id;
                datosRestaurante.productos.push(data);
            });
            if(vistaActual === 'admin' && adminSubVista === 'menu') renderizarModuloAdmin();
        });

        // Escuchar Caja
        onSnapshot(doc(db, "config", "cajaActual"), (doc) => {
            if(doc.exists()) {
                montoCajaInicial = doc.data().fondoInicial || 0;
                ventasTotalesTurno = doc.data().ventasTurno || 0;
                document.getElementById('info-caja-header').innerText = `Caja: ₡${montoCajaInicial.toLocaleString()}`;
                if(vistaActual === 'admin' && adminSubVista === 'caja') renderizarModuloAdmin();
            }
        });

        window.seleccionarRol = function(rol) {
            rolUsuario = rol;
            document.getElementById('modal-login').classList.add('hidden');
            if(rol === 'admin') {
                const pin = prompt("Ingrese PIN:");
                if(pin !== '1234') return window.location.reload();
                document.getElementById('modal-caja').classList.remove('hidden'); 
                document.getElementById('btn-tab-admin').classList.remove('hidden'); 
                document.getElementById('info-caja-header').classList.remove('hidden');
            } else {
                document.getElementById('btn-tab-admin').classList.add('hidden');
                window.cambiarVista('barra'); 
            }
        };

        window.abrirCaja = async function() {
            const val = document.getElementById('input-monto-caja').value;
            if(!val) return;
            montoCajaInicial = parseFloat(val);
            await setDoc(doc(db, "config", "cajaActual"), {
                fondoInicial: montoCajaInicial,
                ventasTurno: 0,
                fechaApertura: new Date().toISOString()
            });
            document.getElementById('modal-caja').classList.add('hidden');
            window.cambiarVista('barra');
        };

        window.cambiarVista = function(tipo) {
            if(tipo === 'admin' && rolUsuario !== 'admin') return;
            vistaActual = tipo;
            
            ['barra', 'mesas', 'vip', 'admin'].forEach(t => {
                const btn = document.getElementById(`btn-tab-${t}`);
                if(btn) btn.className = t === tipo 
                    ? (tipo==='admin' ? "px-5 py-2 rounded-lg font-bold bg-amber-500 text-slate-900 shadow-lg text-sm" : "px-5 py-2 rounded-lg font-bold bg-amber-500 text-slate-900 shadow text-sm") 
                    : "px-5 py-2 rounded-lg font-semibold text-slate-400 hover:text-white hover:bg-slate-800 text-sm";
            });

            window.cerrarPanel();
            if(tipo === 'admin') {
                document.getElementById('area-operacion').classList.add('hidden');
                document.getElementById('area-admin').classList.remove('hidden');
                document.getElementById('area-admin').classList.add('flex');
                renderizarModuloAdmin();
            } else {
                const titulos = { barra: 'Control de Barra', mesas: 'Salón Principal', vip: 'Área Reservada' };
                document.getElementById('titulo-vista').innerText = titulos[tipo];
                document.getElementById('btn-agregar-barra').style.display = tipo === 'barra' ? 'flex' : 'none';
                document.getElementById('area-operacion').classList.remove('hidden');
                document.getElementById('area-admin').classList.add('hidden');
                document.getElementById('area-admin').classList.remove('flex');
                renderizarGridOperacion();
            }
        };

        function renderizarGridOperacion() {
            const grid = document.getElementById('grid-elementos');
            grid.innerHTML = '';
            
            if(datosRestaurante[vistaActual].length === 0) {
                grid.innerHTML = `<p class="col-span-full text-slate-500 mt-10">No hay espacios configurados en ${vistaActual}. Aguarde o créelos desde Admin.</p>`;
                return;
            }

            datosRestaurante[vistaActual].forEach(el => {
                const ocupada = el.estado === 'ocupada';
                const tarjeta = document.createElement('div');
                tarjeta.className = `p-4 rounded-2xl border-2 flex flex-col justify-between h-32 md:h-36 cursor-pointer transition-all transform active:scale-95 shadow-lg relative overflow-hidden ${
                    ocupada ? 'bg-rose-950/20 border-rose-600/50 hover:border-rose-400' : 'bg-slate-900 border-slate-800 hover:border-amber-500/50'
                }`;
                tarjeta.onclick = () => window.seleccionarElemento(el.id);

                const brillo = ocupada ? `<div class="absolute -top-10 -right-10 w-24 h-24 bg-rose-500/10 rounded-full blur-xl"></div>` : '';
                tarjeta.innerHTML = `
                    ${brillo}
                    <div class="flex justify-between items-start mb-2 relative z-10 gap-2">
                        <span class="font-black text-lg md:text-xl text-slate-100 truncate flex-1">${ocupada ? el.cliente : 'Libre'}</span>
                        <span class="w-3 h-3 md:w-3.5 md:h-3.5 rounded-full shrink-0 mt-1 ${ocupada ? 'bg-rose-500 animate-pulse' : 'bg-emerald-500'}"></span>
                    </div>
                    <div class="relative z-10 mt-auto">
                        <div class="flex items-center gap-1.5 mb-1">
                            <i class="fa-solid fa-location-dot text-[10px] ${ocupada ? 'text-rose-400/70' : 'text-slate-500'}"></i>
                            <p class="text-[11px] md:text-xs font-semibold uppercase tracking-wider ${ocupada ? 'text-rose-200/70' : 'text-slate-500'} truncate">${el.nombre}</p>
                        </div>
                        <p class="text-base md:text-lg font-black ${ocupada ? 'text-emerald-400' : 'text-slate-600'}">${ocupada ? '₡' + el.total.toLocaleString() : '---'}</p>
                    </div>`;
                grid.appendChild(tarjeta);
            });
        }

        window.cambiarSubVistaAdmin = function(vista) {
            adminSubVista = vista;
            ['caja', 'menu', 'espacios'].forEach(v => {
                const btn = document.getElementById(`btn-admin-${v}`);
                if(v === vista) btn.className = "pb-2 text-amber-500 border-b-2 border-amber-500 font-bold whitespace-nowrap";
                else btn.className = "pb-2 text-slate-400 border-b-2 border-transparent hover:text-slate-200 font-bold whitespace-nowrap";
            });
            renderizarModuloAdmin();
        };

        function renderizarModuloAdmin() {
            const cont = document.getElementById('contenedor-admin');
            if(adminSubVista === 'caja') {
                const totalEsperado = montoCajaInicial + ventasTotalesTurno;
                cont.innerHTML = `
                    <div class="max-w-4xl mx-auto w-full">
                        <h2 class="text-2xl md:text-3xl font-black mb-6 text-slate-100">Resumen Financiero</h2>
                        <div class="grid grid-cols-1 md:grid-cols-3 gap-4 md:gap-6 mb-8 w-full">
                            <div class="bg-slate-900 p-5 rounded-2xl border border-slate-800 shadow-xl relative overflow-hidden">
                                <p class="text-xs text-slate-400 font-bold uppercase tracking-wider mb-2">Fondo Base</p>
                                <p class="text-2xl font-black text-slate-200 relative z-10">₡${montoCajaInicial.toLocaleString()}</p>
                            </div>
                            <div class="bg-slate-900 p-5 rounded-2xl border border-slate-800 shadow-xl relative overflow-hidden">
                                <p class="text-xs text-slate-400 font-bold uppercase tracking-wider mb-2">Ventas del Turno</p>
                                <p class="text-2xl font-black text-emerald-400 relative z-10">+ ₡${ventasTotalesTurno.toLocaleString()}</p>
                            </div>
                            <div class="bg-gradient-to-br from-amber-500 to-amber-600 p-5 rounded-2xl shadow-xl shadow-amber-500/20 relative overflow-hidden text-slate-900">
                                <p class="text-xs font-black uppercase tracking-wider mb-2 opacity-90">Total en Caja</p>
                                <p class="text-3xl font-black relative z-10">₡${totalEsperado.toLocaleString()}</p>
                            </div>
                        </div>
                        <button onclick="window.ejecutarCierreCaja()" class="w-full bg-rose-600 hover:bg-rose-500 text-white font-bold py-4 rounded-xl shadow-lg transition flex justify-center gap-2">
                            <i class="fa-solid fa-lock mt-1"></i> Cerrar Turno Definitivo
                        </button>
                    </div>`;
            } 
            else if(adminSubVista === 'menu') {
                const prodsFiltrados = datosRestaurante.productos.filter(p => p.nombre.toLowerCase().includes(busquedaMenu.toLowerCase()));
                let html = `
                    <div class="max-w-6xl mx-auto w-full">
                        <div class="flex flex-col md:flex-row justify-between mb-6 gap-4">
                            <h2 class="text-2xl font-black text-slate-100">Menú</h2>
                            <div class="flex flex-col lg:flex-row gap-3">
                                <input type="text" value="${busquedaMenu}" onkeyup="window.filtrarMenu(this.value)" placeholder="Buscar..." class="w-full lg:w-48 bg-slate-900 border border-slate-700 rounded-xl px-3 py-2 text-sm focus:outline-none">
                                <div class="flex gap-2">
                                    <input type="text" id="add-prod-nombre" placeholder="Producto" class="flex-1 bg-slate-900 border border-slate-700 px-3 py-2 rounded-xl text-sm focus:outline-none">
                                    <input type="number" id="add-prod-precio" placeholder="Precio" class="w-20 bg-slate-900 border border-slate-700 px-2 py-2 rounded-xl text-sm focus:outline-none">
                                    <button onclick="window.adminAgregarProducto()" class="bg-emerald-600 text-white px-4 py-2 rounded-xl font-bold"><i class="fa-solid fa-plus"></i></button>
                                </div>
                            </div>
                        </div>
                        <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-3 md:gap-4 pb-10">
                `;
                if(prodsFiltrados.length === 0) html += `<div class="col-span-full text-slate-500">No hay productos. Usa el formulario de arriba para agregar uno.</div>`;
                prodsFiltrados.forEach(p => {
                    html += `
                        <div class="bg-slate-900 border border-slate-800 rounded-xl p-4 flex flex-col justify-between">
                            <div class="mb-3">
                                <h4 class="font-bold text-slate-200 truncate">${p.nombre}</h4>
                                <p class="text-lg font-black text-amber-400">₡${p.precio.toLocaleString()}</p>
                            </div>
                            <div class="flex gap-2 border-t border-slate-800/60 pt-3">
                                <button onclick="window.adminEditarPrecio('${p.id}', '${p.nombre}', ${p.precio})" class="flex-1 bg-slate-800 text-slate-300 py-1.5 rounded-lg text-xs"><i class="fa-solid fa-pen"></i></button>
                                <button onclick="window.adminEliminarProducto('${p.id}')" class="flex-1 bg-rose-950/30 text-rose-500 py-1.5 rounded-lg text-xs border border-rose-900/30"><i class="fa-solid fa-trash"></i></button>
                            </div>
                        </div>`;
                });
                html += `</div></div>`;
                cont.innerHTML = html;
            }
            else if(adminSubVista === 'espacios') {
                let html = `
                    <div class="max-w-6xl mx-auto w-full">
                        <div class="flex flex-col md:flex-row justify-between mb-6 gap-4">
                            <h2 class="text-2xl font-black text-slate-100">Zonas</h2>
                            <div class="flex gap-2">
                                <select id="add-esp-tipo" class="bg-slate-900 border border-slate-700 px-3 py-2 rounded-xl text-sm focus:outline-none w-28">
                                    <option value="barra">Barra</option><option value="mesas">Salón</option><option value="vip">VIP</option>
                                </select>
                                <input type="text" id="add-esp-nombre" placeholder="Nombre" class="flex-1 bg-slate-900 border border-slate-700 px-3 py-2 rounded-xl text-sm focus:outline-none">
                                <button onclick="window.adminAgregarEspacio()" class="bg-amber-500 text-slate-900 px-4 py-2 rounded-xl font-bold">+</button>
                            </div>
                        </div>
                        <div class="grid grid-cols-1 md:grid-cols-3 gap-4 pb-10">
                `;
                const zonas = [
                    { key: 'barra', icon: 'fa-martini-glass-citrus', title: 'Barra', color: 'text-blue-400' },
                    { key: 'mesas', icon: 'fa-utensils', title: 'Mesas', color: 'text-amber-400' },
                    { key: 'vip', icon: 'fa-crown', title: 'VIP', color: 'text-fuchsia-400' }
                ];
                zonas.forEach(z => {
                    html += `<div class="bg-slate-900 border border-slate-800 rounded-2xl p-4 shadow-lg">
                                <h3 class="text-base font-black mb-4 flex items-center gap-2 border-b border-slate-800 pb-3"><i class="fa-solid ${z.icon} ${z.color}"></i> ${z.title}</h3>
                                <div class="space-y-2">`;
                    if(datosRestaurante[z.key].length === 0) html += `<p class="text-xs text-slate-500">Sin espacios agregados</p>`;
                    datosRestaurante[z.key].forEach(esp => {
                        html += `
                                <div class="flex justify-between items-center bg-slate-950 p-2 rounded-xl border border-slate-800/60">
                                    <span class="font-bold text-slate-300 text-sm truncate pr-2">${esp.nombre}</span>
                                    <div class="flex gap-1 shrink-0">
                                        <button onclick="window.adminEditarEspacio('${esp.id}', '${esp.nombre}')" class="w-7 h-7 rounded-lg text-slate-400 hover:bg-slate-800"><i class="fa-solid fa-pen text-xs"></i></button>
                                        <button onclick="window.adminEliminarEspacio('${esp.id}', '${esp.estado}')" class="w-7 h-7 rounded-lg text-rose-500/70 hover:bg-rose-950"><i class="fa-solid fa-trash text-xs"></i></button>
                                    </div>
                                </div>`;
                    });
                    html += `</div></div>`;
                });
                html += `</div></div>`;
                cont.innerHTML = html;
            }
        }

        window.filtrarMenu = function(val) { busquedaMenu = val; renderizarModuloAdmin(); };
        window.adminAgregarProducto = async function() {
            const nom = document.getElementById('add-prod-nombre').value;
            const pre = parseFloat(document.getElementById('add-prod-precio').value);
            if(!nom || !pre) return;
            await addDoc(collection(db, "productos"), { nombre: nom, precio: pre });
            document.getElementById('add-prod-nombre').value = '';
            document.getElementById('add-prod-precio').value = '';
        };
        window.adminEliminarProducto = async function(id) {
            if(confirm('¿Eliminar producto?')) await deleteDoc(doc(db, "productos", id));
        };
        window.adminEditarPrecio = async function(id, nombre, precioActual) {
            const nv = prompt(`Precio para ${nombre}:`, precioActual);
            if(nv && !isNaN(nv)) await updateDoc(doc(db, "productos", id), { precio: parseFloat(nv) });
        };

        window.adminAgregarEspacio = async function() {
            const cat = document.getElementById('add-esp-tipo').value;
            const nom = document.getElementById('add-esp-nombre').value;
            if(!nom) return;
            await addDoc(collection(db, "espacios"), { categoria: cat, nombre: nom, estado: 'libre', cliente: '', total: 0, items: [] });
            document.getElementById('add-esp-nombre').value = '';
        };
        window.adminEliminarEspacio = async function(id, estado) {
            if(estado === 'ocupada') return alert('Mesa ocupada. Ciérrela primero.');
            if(confirm(`¿Eliminar este espacio?`)) await deleteDoc(doc(db, "espacios", id));
        };
        window.adminEditarEspacio = async function(id, nombreActual) {
            const nv = prompt("Modificar nombre:", nombreActual);
            if(nv) await updateDoc(doc(db, "espacios", id), { nombre: nv });
        };

        window.agregarClienteExtraBarra = async function() {
            const nom = prompt("Nombre del cliente:");
            if(nom) {
                await addDoc(collection(db, "espacios"), { categoria: 'barra', nombre: 'Extra', estado: 'ocupada', cliente: nom, total: 0, items: [] });
            }
        };

        window.seleccionarElemento = async function(id) {
            const espacio = [...datosRestaurante.barra, ...datosRestaurante.mesas, ...datosRestaurante.vip].find(e => e.id === id);
            
            if (espacio.estado === 'libre') {
                const nom = prompt(`Apertura de cuenta. Cliente:`);
                if (!nom) return;
                await updateDoc(doc(db, "espacios", id), { estado: 'ocupada', cliente: nom });
                espacio.estado = 'ocupada';
                espacio.cliente = nom;
            }
            
            elementoSeleccionado = espacio;
            const panel = document.getElementById('panel-cuenta');
            panel.classList.remove('hidden');
            panel.classList.add('flex');
            document.getElementById('panel-cliente').innerText = espacio.cliente;
            document.getElementById('panel-titulo').innerText = espacio.nombre;
            window.actualizarListaPanel();
        };

        window.actualizarListaPanel = function() {
            const cont = document.getElementById('lista-items-cuenta');
            cont.innerHTML = '';
            if (!elementoSeleccionado.items || elementoSeleccionado.items.length === 0) {
                cont.innerHTML = `<p class="text-slate-500 text-sm text-center italic mt-10">Sin productos aún</p>`;
            } else {
                elementoSeleccionado.items.forEach((item, index) => {
                    cont.innerHTML += `
                        <div class="flex justify-between items-center bg-slate-950 p-3 rounded-xl border border-slate-800 shadow-sm mb-2">
                            <span class="font-bold text-slate-200 text-sm truncate pr-2">${item.nombre}</span> 
                            <div class="flex items-center gap-3 shrink-0">
                                <span class="font-black text-amber-400">₡${item.precio.toLocaleString()}</span>
                                <button onclick="window.eliminarItemCuenta(${index})" class="text-rose-500 hover:text-rose-400"><i class="fa-solid fa-xmark"></i></button>
                            </div>
                        </div>`;
                });
            }
            document.getElementById('panel-total').innerText = `₡${(elementoSeleccionado.total || 0).toLocaleString()}`;
        };

        window.cerrarPanel = function() {
            document.getElementById('panel-cuenta').classList.add('hidden');
            document.getElementById('panel-cuenta').classList.remove('flex');
            elementoSeleccionado = null;
        };

        window.abrirModalAgregar = async function() {
            if (!elementoSeleccionado) return;
            if(datosRestaurante.productos.length === 0) return alert('No hay productos creados en el menú. Ingrese como Admin y créelos primero.');
            
            const prod = datosRestaurante.productos[Math.floor(Math.random() * datosRestaurante.productos.length)];
            const itemsActuales = elementoSeleccionado.items || [];
            const nuevosItems = [...itemsActuales, { nombre: prod.nombre, precio: prod.precio }];
            const nuevoTotal = (elementoSeleccionado.total || 0) + prod.precio;
            
            await updateDoc(doc(db, "espacios", elementoSeleccionado.id), { items: nuevosItems, total: nuevoTotal });
            elementoSeleccionado.items = nuevosItems;
            elementoSeleccionado.total = nuevoTotal;
            window.actualizarListaPanel();
        };

        window.eliminarItemCuenta = async function(index) {
            if (!elementoSeleccionado) return;
            const itemEliminado = elementoSeleccionado.items[index];
            const nuevosItems = [...elementoSeleccionado.items];
            nuevosItems.splice(index, 1);
            const nuevoTotal = elementoSeleccionado.total - itemEliminado.precio;

            await updateDoc(doc(db, "espacios", elementoSeleccionado.id), { items: nuevosItems, total: nuevoTotal });
            elementoSeleccionado.items = nuevosItems;
            elementoSeleccionado.total = nuevoTotal;
            window.actualizarListaPanel();
        };

        window.cobrarCuenta = async function() {
            if (!elementoSeleccionado || !elementoSeleccionado.total) return window.cerrarPanel();
            
            alert(`Pago procesado: ₡${elementoSeleccionado.total.toLocaleString()}`);
            
            ventasTotalesTurno += elementoSeleccionado.total;
            await updateDoc(doc(db, "config", "cajaActual"), { ventasTurno: ventasTotalesTurno });

            if(elementoSeleccionado.nombre === 'Extra') {
                await deleteDoc(doc(db, "espacios", elementoSeleccionado.id));
            } else {
                await updateDoc(doc(db, "espacios", elementoSeleccionado.id), { estado: 'libre', cliente: '', total: 0, items: [] });
            }
            window.cerrarPanel();
        };

        window.ejecutarCierreCaja = async function() {
            alert('Turno cerrado en Firebase.');
            await setDoc(doc(db, "config", "cajaActual"), { fondoInicial: 0, ventasTurno: 0, fechaCierre: new Date().toISOString() });
            window.location.reload();
        };

    </script>
</body>
</html>
