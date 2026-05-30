# BOMOHSAHN
BOMOHSAHN
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>BOMOHSA | El Poder de la Experiencia desde 1974</title>
    
    <meta name="description" content="Líder en Honduras en soluciones de bombeo, motores, generadores y equipos industriales. Certificación ISO 9001.">
    
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;600;700;800&family=Roboto:wght@300;400;500&display=swap" rel="stylesheet">
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://unpkg.com/aos@2.3.1/dist/aos.css" rel="stylesheet">

    <style>
        :root {
            --bomo-blue: #003876;
            --bomo-blue-dark: #002650;
            --bomo-accent: #f37021; /* Naranja Industrial */
            --steel-gray: #f8f9fa;
            --industrial-gray: #495057;
            --glass: rgba(255, 255, 255, 0.9);
        }

        body {
            font-family: 'Roboto', sans-serif;
            overflow-x: hidden;
            background-color: #fff;
        }

        h1, h2, h3, .navbar-brand {
            font-family: 'Montserrat', sans-serif;
            font-weight: 700;
        }

        /* --- NAVBAR --- */
        .navbar {
            background: var(--glass) !important;
            backdrop-filter: blur(15px);
            border-bottom: 3px solid var(--bomo-blue);
            transition: all 0.3s ease;
        }

        .nav-link {
            color: var(--bomo-blue-dark) !important;
            font-weight: 600;
            text-transform: uppercase;
            font-size: 0.85rem;
            letter-spacing: 1px;
        }

        .nav-link:hover {
            color: var(--bomo-accent) !important;
        }

        /* --- HERO SECTION --- */
        .hero {
            height: 90vh;
            background: linear-gradient(rgba(0, 56, 118, 0.7), rgba(0, 38, 80, 0.85)), 
                        url('https://images.unsplash.com/photo-1581091226825-a6a2a5aee158?auto=format&fit=crop&w=1920&q=80');
            background-size: cover;
            background-position: center;
            display: flex;
            align-items: center;
            color: white;
            clip-path: polygon(0 0, 100% 0, 100% 90%, 0% 100%);
        }

        .hero h1 { font-size: 4rem; text-shadow: 2px 2px 10px rgba(0,0,0,0.5); }

        /* --- CATALOGO DINAMICO --- */
        .filter-btn {
            border: 2px solid var(--bomo-blue);
            background: transparent;
            color: var(--bomo-blue);
            padding: 8px 20px;
            border-radius: 50px;
            margin: 5px;
            font-weight: 600;
            transition: 0.3s;
        }

        .filter-btn.active, .filter-btn:hover {
            background: var(--bomo-blue);
            color: white;
        }

        .product-card {
            border: none;
            border-radius: 15px;
            overflow: hidden;
            background: var(--steel-gray);
            transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
            height: 100%;
        }

        .product-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0,56,118,0.15);
        }

        .product-img {
            height: 220px;
            object-fit: contain;
            background: white;
            padding: 20px;
        }

        .badge-category {
            background: var(--bomo-blue);
            color: white;
            font-size: 0.7rem;
            padding: 5px 12px;
            border-radius: 50px;
            position: absolute;
            top: 15px;
            right: 15px;
        }

        /* --- BOLETIN TECNICO CLUB PRO --- */
        .newsletter-section {
            background: linear-gradient(135deg, var(--bomo-blue-dark) 0%, #004a99 100%);
            color: white;
            padding: 80px 0;
            position: relative;
            overflow: hidden;
        }

        .newsletter-card {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255,255,255,0.2);
            border-radius: 20px;
            padding: 40px;
        }

        .coupon-box {
            display: none;
            border: 2px dashed var(--bomo-accent);
            padding: 20px;
            background: rgba(243, 112, 33, 0.1);
            border-radius: 10px;
            margin-top: 20px;
        }

        /* --- WHATSAPP & FLOATING --- */
        .float-wa {
            position: fixed;
            bottom: 30px;
            right: 30px;
            background: #25d366;
            color: white;
            width: 65px;
            height: 65px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 35px;
            box-shadow: 0 10px 25px rgba(37,211,102,0.4);
            z-index: 1000;
            text-decoration: none;
            transition: 0.3s;
        }

        .float-wa:hover { transform: scale(1.1) rotate(10deg); color: white; }

        /* --- CART DRAWER --- */
        #cartDrawer {
            position: fixed;
            right: -400px;
            top: 0;
            width: 400px;
            height: 100vh;
            background: white;
            box-shadow: -10px 0 30px rgba(0,0,0,0.1);
            z-index: 2000;
            transition: 0.4s;
            padding: 30px;
            display: flex;
            flex-direction: column;
        }

        #cartDrawer.open { right: 0; }

        .cart-item {
            display: flex;
            align-items: center;
            gap: 15px;
            padding: 10px 0;
            border-bottom: 1px solid #eee;
        }

        .brand-logo {
            filter: grayscale(100%);
            opacity: 0.6;
            transition: 0.3s;
            max-width: 120px;
        }

        .brand-logo:hover { filter: grayscale(0%); opacity: 1; }
    </style>
</head>
<body>

    <nav class="navbar navbar-expand-lg fixed-top shadow-sm">
        <div class="container">
            <a class="navbar-brand d-flex align-items-center" href="#">
                <img src="https://i.imgur.com/Kz8pXmB.png" alt="BOMOHSA" height="50" class="me-2">
            </a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#mainNav">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="mainNav">
                <ul class="navbar-nav mx-auto">
                    <li class="nav-item"><a class="nav-link" href="#inicio">Inicio</a></li>
                    <li class="nav-item"><a class="nav-link" href="#nosotros">Historia</a></li>
                    <li class="nav-item"><a class="nav-link" href="#catalogo">Catálogo</a></li>
                    <li class="nav-item"><a class="nav-link" href="#servicios">Servicios</a></li>
                    <li class="nav-item"><a class="nav-link" href="#contacto">Contacto</a></li>
                </ul>
                <div class="d-flex align-items-center">
                    <span class="me-3 d-none d-xl-block"><i class="fas fa-phone me-2 text-primary"></i>+504 556-6614</span>
                    <button class="btn btn-primary rounded-pill px-4" onclick="toggleCart()">
                        <i class="fas fa-file-invoice me-2"></i>Cotización <span id="cartCount" class="badge bg-danger">0</span>
                    </button>
                </div>
            </div>
        </div>
    </nav>

    <section id="inicio" class="hero">
        <div class="container text-center text-md-start">
            <div class="row">
                <div class="col-lg-8" data-aos="fade-right">
                    <span class="badge bg-warning text-dark mb-3 px-3 py-2 fw-bold">DESDE 1974 EN HONDURAS</span>
                    <h1 class="display-2 fw-extrabold mb-4">El Poder de la <br><span class="text-warning">Experiencia</span></h1>
                    <p class="lead mb-5 fs-4">Líderes en soluciones integrales de AGUA, ENERGÍA, AIRE y AGRICULTURA. Ingeniería de alto nivel con respaldo profesional garantizado.</p>
                    <div class="d-flex flex-wrap gap-3">
                        <a href="#catalogo" class="btn btn-warning btn-lg px-5 py-3 fw-bold shadow">Explorar Catálogo</a>
                        <a href="#contacto" class="btn btn-outline-light btn-lg px-5 py-3">Asesoría Técnica</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section class="py-5 bg-light">
        <div class="container">
            <div class="row align-items-center text-center g-4">
                <div class="col-6 col-md-2"><img src="https://i.imgur.com/uR6oQ3n.png" class="brand-logo img-fluid" alt="Goulds"></div>
                <div class="col-6 col-md-2"><img src="https://i.imgur.com/8f8Z0S0.png" class="brand-logo img-fluid" alt="Grundfos"></div>
                <div class="col-6 col-md-2"><img src="https://i.imgur.com/u6Q6Q3n.png" class="brand-logo img-fluid" alt="Toshiba"></div>
                <div class="col-6 col-md-2"><img src="https://i.imgur.com/oR6oQ3n.png" class="brand-logo img-fluid" alt="Gardner Denver"></div>
                <div class="col-6 col-md-2"><img src="https://i.imgur.com/9R6oQ3n.png" class="brand-logo img-fluid" alt="Honda"></div>
                <div class="col-6 col-md-2"><img src="https://i.imgur.com/2R6oQ3n.png" class="brand-logo img-fluid" alt="Spirax Sarco"></div>
            </div>
        </div>
    </section>

    <section id="catalogo" class="py-5">
        <div class="container">
            <div class="text-center mb-5" data-aos="fade-up">
                <h2 class="display-4 mb-3">Catálogo Industrial <span class="text-primary">BOMOHSA</span></h2>
                <p class="text-muted">Filtra por división tecnológica y encuentra el equipo ideal para tu proyecto.</p>
                
                <div class="d-flex flex-wrap justify-content-center mt-4">
                    <button class="filter-btn active" onclick="filterProducts('all')">Todos</button>
                    <button class="filter-btn" onclick="filterProducts('Agua')">División Agua</button>
                    <button class="filter-btn" onclick="filterProducts('Energía')">Energía</button>
                    <button class="filter-btn" onclick="filterProducts('Aire')">Aire Comprimido</button>
                    <button class="filter-btn" onclick="filterProducts('Vapor')">Sistemas de Vapor</button>
                </div>
                <div class="mt-4 mx-auto" style="max-width: 500px;">
                    <div class="input-group">
                        <span class="input-group-text bg-white border-end-0"><i class="fas fa-search text-muted"></i></span>
                        <input type="text" id="productSearch" class="form-control border-start-0" placeholder="Buscar bomba, motor, marca..." onkeyup="searchProducts()">
                    </div>
                </div>
            </div>

            <div class="row g-4" id="productsGrid">
                </div>
        </div>
    </section>

    <section class="newsletter-section">
        <div class="container">
            <div class="row justify-content-center text-center">
                <div class="col-lg-8" data-aos="zoom-in">
                    <div class="newsletter-card">
                        <i class="fas fa-cog fa-spin fa-3x text-warning mb-4"></i>
                        <h2 class="display-5 fw-bold mb-3">¡Únete al Club BOMOHSA Pro!</h2>
                        <p class="lead mb-4">Regístrate para recibir asesoría técnica exclusiva y obtén un <strong>10% de DESCUENTO</strong> en tu primera cotización de equipos industriales.</p>
                        
                        <form id="newsletterForm" class="row g-3 justify-content-center">
                            <div class="col-md-5">
                                <input type="text" id="subName" class="form-control form-control-lg rounded-pill border-0" placeholder="Nombre completo" required>
                            </div>
                            <div class="col-md-5">
                                <input type="email" id="subEmail" class="form-control form-control-lg rounded-pill border-0" placeholder="Correo corporativo" required>
                            </div>
                            <div class="col-md-10">
                                <select id="subInterest" class="form-select form-select-lg rounded-pill border-0">
                                    <option value="">¿En qué área te especializas?</option>
                                    <option value="Industrial">Planta Industrial</option>
                                    <option value="Agrícola">Producción Agrícola</option>
                                    <option value="Constructor">Ingeniería / Construcción</option>
                                    <option value="Residencial">Soluciones Hogar</option>
                                </select>
                            </div>
                            <div class="col-md-4 mt-4">
                                <button type="submit" class="btn btn-warning btn-lg rounded-pill w-100 fw-bold">OBTENER MI 10% OFF</button>
                            </div>
                        </form>

                        <div id="couponResult" class="coupon-box mt-4">
                            <h4 class="text-warning mb-2">¡BIENVENIDO PRO! 🎉</h4>
                            <p class="mb-2 text-white">Usa el siguiente código en tu cotización por WhatsApp:</p>
                            <div class="bg-white text-dark py-2 px-4 d-inline-block rounded fw-bold fs-3">BOMOHSA10PRO</div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <div id="cartDrawer">
        <div class="d-flex justify-content-between align-items-center mb-4">
            <h4 class="m-0"><i class="fas fa-list-check me-2"></i>Tu Cotización</h4>
            <button class="btn-close" onclick="toggleCart()"></button>
        </div>
        <div id="cartItems" class="flex-grow-1 overflow-auto">
            </div>
        <div class="border-top pt-3 mt-3">
            <p class="text-muted small">* Los precios son referenciales. Un ingeniero validará tu solicitud.</p>
            <button class="btn btn-success btn-lg w-100 py-3 rounded-pill fw-bold" onclick="sendQuote()">
                <i class="fab fa-whatsapp me-2"></i>SOLICITAR POR WHATSAPP
            </button>
        </div>
    </div>

    <a href="https://wa.me/50497223433?text=Hola%20BOMOHSA,%20necesito%20asesoría%20técnica%20para%20mi%20proyecto." class="float-wa shadow-lg" target="_blank">
        <i class="fab fa-whatsapp"></i>
    </a>

    <footer id="contacto" class="bg-dark text-white pt-5 pb-3">
        <div class="container">
            <div class="row g-4">
                <div class="col-lg-4">
                    <img src="https://i.imgur.com/Kz8pXmB.png" height="60" class="mb-3" style="filter: brightness(0) invert(1);">
                    <p class="text-secondary small">"El Poder de la Experiencia" - Desde 1974 brindando soluciones de ingeniería para el desarrollo de Honduras.</p>
                    <div class="d-flex gap-3 fs-5 mt-4">
                        <a href="#" class="text-white"><i class="fab fa-facebook"></i></a>
                        <a href="#" class="text-white"><i class="fab fa-linkedin"></i></a>
                        <a href="#" class="text-white"><i class="fab fa-instagram"></i></a>
                    </div>
                </div>
                <div class="col-md-4 col-lg-2">
                    <h5>Enlaces</h5>
                    <ul class="list-unstyled text-secondary small mt-3">
                        <li class="mb-2"><a href="#" class="text-decoration-none text-secondary">Catálogo Digital</a></li>
                        <li class="mb-2"><a href="#" class="text-decoration-none text-secondary">Marcas Aliadas</a></li>
                        <li class="mb-2"><a href="#" class="text-decoration-none text-secondary">Sucursales</a></li>
                        <li class="mb-2"><a href="#" class="text-decoration-none text-secondary">Servicio Técnico</a></li>
                    </ul>
                </div>
                <div class="col-md-8 col-lg-6">
                    <h5>Nuestras Sucursales</h5>
                    <div class="row mt-3 text-secondary small">
                        <div class="col-md-6 mb-3">
                            <h6 class="text-white">San Pedro Sula (Matriz)</h6>
                            <p><i class="fas fa-map-marker-alt me-2 text-warning"></i>Barrio La Guardia, 3 Ave, 26-27 Calle.</p>
                            <p><i class="fas fa-phone me-2 text-warning"></i>+504 556-6614</p>
                        </div>
                        <div class="col-md-6 mb-3">
                            <h6 class="text-white">Tegucigalpa</h6>
                            <p><i class="fas fa-map-marker-alt me-2 text-warning"></i>Centro-Sur, Francisco Morazán.</p>
                        </div>
                    </div>
                </div>
            </div>
            <hr class="border-secondary mt-5">
            <div class="row text-center small text-secondary">
                <div class="col-md-6 text-md-start">© 2024 BOMOHSA. Todos los derechos reservados.</div>
                <div class="col-md-6 text-md-end">Certificación ISO 9001:2009 | El Poder de la Experiencia</div>
            </div>
        </div>
    </footer>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
    <script src="https://unpkg.com/aos@2.3.1/dist/aos.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/sweetalert2@11"></script>

    <script>
        AOS.init({ duration: 800, once: true });

        // --- DATA DE PRODUCTOS BASADA EN EL CATÁLOGO COMPARTIDO ---
        const products = [
            { id: 1, name: "Bomba ANSI Proceso 3196", brand: "Goulds ITT", category: "Agua", app: "Industrial / Azucarera", img: "https://i.imgur.com/uG2Z4Sj.png", desc: "Bombas para procesos químicos y salmueras." },
            { id: 2, name: "Bomba Sumergible Flygt N", brand: "Xylem Flygt", category: "Agua", app: "Aguas Residuales", img: "https://i.imgur.com/8Y0Z4Hj.png", desc: "Impulsor inatascable para drenaje municipal." },
            { id: 3, name: "Bomba Autocebante Super T", brand: "Gorman-Rupp", category: "Agua", app: "Efluentes / Minería", img: "https://i.imgur.com/vH0Z4Yj.png", desc: "Líder mundial en bombas de fácil limpieza." },
            { id: 4, name: "Bomba Sanitaria QTS", brand: "Q-Pumps", category: "Agua", app: "Alimentos / Sanitaria", img: "https://i.imgur.com/xR0Z4Nj.png", desc: "Trasiego de lácteos y chocolate con acabado 3A." },
            { id: 5, name: "Generador Diésel 250kVA", brand: "Grupel", category: "Energía", app: "Industrial / Emergencia", img: "https://i.imgur.com/tR0Z4Nj.png", desc: "Energía europea de alta confiabilidad." },
            { id: 6, name: "Motor NEMA Premium EQP", brand: "Toshiba", category: "Energía", app: "Industrial Pesada", img: "https://i.imgur.com/pG0Z4Nj.png", desc: "Eficiencia energética máxima de vanguardia." },
            { id: 7, name: "Compresor Tornillo Variable", brand: "Gardner Denver", category: "Aire", app: "Aire Comprimido", img: "https://i.imgur.com/zW0Z4Nj.png", desc: "Ahorro energético del 35% en plantas." },
            { id: 8, name: "Trampa de Vapor Spiratol", brand: "Spirax Sarco", category: "Vapor", app: "Calderas / Energía", img: "https://i.imgur.com/yQ0Z4Nj.png", desc: "Control de temperatura preciso en procesos." },
            { id: 9, name: "Válvula Control Bermad", brand: "Bermad", category: "Agua", app: "Riego / Municipios", img: "https://i.imgur.com/aW0Z4Nj.png", desc: "Válvulas reductoras y de alivio de presión." }
        ];

        let cart = JSON.parse(localStorage.getItem('bomoQuote')) || [];

        // Renderizar Catálogo
        function renderProducts(data) {
            const grid = document.getElementById('productsGrid');
            grid.innerHTML = data.map(p => `
                <div class="col-md-6 col-lg-4 product-item" data-aos="fade-up">
                    <div class="product-card position-relative shadow-sm">
                        <span class="badge-category">${p.category}</span>
                        <img src="${p.img}" class="product-img w-100" alt="${p.name}">
                        <div class="p-4">
                            <h6 class="text-primary fw-bold mb-1">${p.brand}</h6>
                            <h4 class="mb-2">${p.name}</h4>
                            <p class="text-muted small mb-3">${p.desc}</p>
                            <div class="d-flex justify-content-between align-items-center">
                                <span class="badge bg-light text-dark border">${p.app}</span>
                                <button onclick="addToCart(${p.id})" class="btn btn-bomo btn-sm btn-primary rounded-pill px-3">
                                    <i class="fas fa-plus me-1"></i> Cotizar
                                </button>
                            </div>
                        </div>
                    </div>
                </div>
            `).join('');
        }

        // Lógica de Filtrado Dinámico
        function filterProducts(cat) {
            const btns = document.querySelectorAll('.filter-btn');
            btns.forEach(b => b.classList.remove('active'));
            event.target.classList.add('active');

            if(cat === 'all') renderProducts(products);
            else renderProducts(products.filter(p => p.category === cat));
        }

        function searchProducts() {
            const term = document.getElementById('productSearch').value.toLowerCase();
            const filtered = products.filter(p => 
                p.name.toLowerCase().includes(term) || 
                p.brand.toLowerCase().includes(term) ||
                p.category.toLowerCase().includes(term)
            );
            renderProducts(filtered);
        }

        // --- LÓGICA DE COTIZACIÓN (CARRITO) ---
        function addToCart(id) {
            const item = products.find(p => p.id === id);
            cart.push(item);
            updateCart();
            Swal.fire({
                icon: 'success',
                title: 'Agregado a Cotización',
                text: `${item.name} se agregó correctamente.`,
                timer: 1500,
                showConfirmButton: false
            });
        }

        function updateCart() {
            localStorage.setItem('bomoQuote', JSON.stringify(cart));
            document.getElementById('cartCount').innerText = cart.length;
            const cartItems = document.getElementById('cartItems');
            cartItems.innerHTML = cart.map((p, index) => `
                <div class="cart-item">
                    <img src="${p.img}" height="50">
                    <div class="flex-grow-1">
                        <h6 class="m-0">${p.name}</h6>
                        <small class="text-muted">${p.brand}</small>
                    </div>
                    <button class="btn btn-sm text-danger" onclick="removeFromCart(${index})"><i class="fas fa-trash"></i></button>
                </div>
            `).join('');
        }

        function removeFromCart(index) {
            cart.splice(index, 1);
            updateCart();
        }

        function toggleCart() {
            document.getElementById('cartDrawer').classList.toggle('open');
        }

        function sendQuote() {
            if(cart.length === 0) return Swal.fire('Error', 'Agrega productos para cotizar', 'error');
            
            let message = "⚙️ ¡SOLICITUD DE COTIZACIÓN BOMOHSA! %0A%0AHola, soy un cliente interesado en los siguientes equipos industriales: %0A%0A";
            cart.forEach((p, i) => {
                message += `${i+1}. *${p.name}* (Marca: ${p.brand})%0A`;
            });
            message += "%0AQuedamos atentos a su asesoría técnica y propuesta comercial. ¡Gracias! 🔧";
            
            window.open(`https://wa.me/50497223433?text=${message}`);
        }

        // --- LÓGICA BOLETÍN PRO ---
        document.getElementById('newsletterForm').addEventListener('submit', function(e) {
            e.preventDefault();
            const name = document.getElementById('subName').value;
            const email = document.getElementById('subEmail').value;
            
            // Simulación de guardado
            console.log(`Nuevo suscriptor Club Pro: ${name} <${email}>`);
            
            document.getElementById('newsletterForm').classList.add('d-none');
            document.getElementById('couponResult').style.display = 'block';
            
            Swal.fire('¡Bienvenido Pro!', 'Tu cupón BOMOHSA10PRO ha sido activado.', 'success');
        });

        // Inicio
        renderProducts(products);
        updateCart();
    </script>
</body>
</html>
