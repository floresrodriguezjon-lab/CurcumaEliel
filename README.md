<!DOCTYPE html>
<html lang="es" class="scroll-smooth">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Curcu-Eliel | Cúrcuma Pura & Bienestar Natural</title>
  
  <!-- Google Fonts: Inter & Outfit -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Outfit:wght@400;500;600;700;800&family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
  
  <!-- FontAwesome Icons -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" />

  <!-- Tailwind CSS -->
  <script src="https://cdn.tailwindcss.com"></script>
  <script>
    tailwind.config = {
      theme: {
        extend: {
          fontFamily: {
            sans: ['Inter', 'sans-serif'],
            heading: ['Outfit', 'sans-serif']
          },
          colors: {
            amberGold: {
              50: '#fffbeb',
              100: '#fef3c7',
              200: '#fde68a',
              300: '#fcd34d',
              400: '#fbbf24',
              500: '#f59e0b',
              600: '#d97706',
              700: '#b45309',
              800: '#92400e',
              900: '#78350f',
            },
            herbGreen: {
              50: '#f0fdf4',
              100: '#dcfce7',
              500: '#22c55e',
              600: '#16a34a',
              700: '#15803d',
              800: '#166534',
              900: '#14532d',
            }
          }
        }
      }
    }
  </script>

  <style>
    .gold-gradient-bg {
      background: linear-gradient(135deg, #fffbeb 0%, #fef3c7 40%, #fef9c3 100%);
    }
    .text-gradient {
      background: linear-gradient(90deg, #b45309 0%, #d97706 60%, #15803d 100%);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
    }
    .badge-glow {
      box-shadow: 0 0 15px rgba(245, 158, 11, 0.4);
    }
    /* Hide scrollbar for tabs on mobile */
    .no-scrollbar::-webkit-scrollbar {
      display: none;
    }
    .no-scrollbar {
      -ms-overflow-style: none;
      scrollbar-width: none;
    }
  </style>
</head>
<body class="bg-amber-50/30 text-stone-800 font-sans antialiased">

  <aside aria-label="Anuncio promocional" class="bg-amberGold-600 text-white text-xs sm:text-sm font-medium py-2 px-4 text-center tracking-wide flex items-center justify-center gap-2">
    <span class="animate-pulse">✨</span>
    <span><strong>¡OFERTA DE LANZAMIENTO!</strong> Envío gratis en combos Curcu-Eliel a todo el país + Asesoría nutricional gratuita.</span>
  </aside>

  <header class="sticky top-0 z-40 bg-white/90 backdrop-blur-md border-b border-amber-100 shadow-sm transition-all duration-200">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex items-center justify-between h-20">
        
        <!-- Logo -->
        <a href="#inicio" class="flex items-center gap-3 group">
          <div class="w-12 h-12 rounded-2xl bg-gradient-to-tr from-amberGold-500 to-amberGold-400 flex items-center justify-center text-white shadow-md group-hover:scale-105 transition-transform duration-200">
            <i class="fa-solid fa-mortar-pestle text-2xl"></i>
          </div>
          <div>
            <span class="font-heading font-extrabold text-2xl tracking-tight text-stone-900 block leading-none">
              CURCU<span class="text-amberGold-600">-ELIEL</span>
            </span>
            <span class="text-[11px] uppercase tracking-widest text-herbGreen-700 font-semibold">Elixir de Salud Natural</span>
          </div>
        </a>

        <!-- Desktop Navigation Links -->
        <nav class="hidden md:flex items-center space-x-8 font-medium text-stone-600">
          <a href="#inicio" class="hover:text-amberGold-600 transition-colors">Inicio</a>
          <a href="#beneficios" class="hover:text-amberGold-600 transition-colors">Beneficios</a>
          <a href="#formula" class="hover:text-amberGold-600 transition-colors">Curcu-Eliel Forte</a>
          <a href="#productos" class="hover:text-amberGold-600 transition-colors">Productos</a>
          <a href="#testimonios" class="hover:text-amberGold-600 transition-colors">Testimonios</a>
          <a href="#faq" class="hover:text-amberGold-600 transition-colors">Preguntas</a>
        </nav>

        <!-- Cart Button & Quick CTA -->
        <div class="flex items-center gap-3">
          <button id="cartBtn" onclick="toggleCartModal()" class="relative p-2.5 rounded-full text-stone-700 bg-amberGold-100/60 hover:bg-amberGold-200 transition-colors" aria-label="Abrir carrito de compras">
            <i class="fa-solid fa-cart-shopping text-lg text-amberGold-800"></i>
            <span id="cartCountBadge" class="absolute -top-1 -right-1 bg-herbGreen-600 text-white text-xs font-bold rounded-full h-5 w-5 flex items-center justify-center shadow-sm">0</span>
          </button>

          <a href="#productos" class="hidden sm:inline-flex items-center gap-2 bg-gradient-to-r from-amberGold-500 to-amberGold-600 hover:from-amberGold-600 hover:to-amberGold-700 text-white font-semibold px-5 py-2.5 rounded-full shadow-md hover:shadow-lg transition-all transform hover:-translate-y-0.5">
            <span>Comprar Ahora</span>
            <i class="fa-solid fa-arrow-right text-xs"></i>
          </a>

          <!-- Mobile Hamburger -->
          <button id="mobileMenuBtn" onclick="toggleMobileMenu()" class="md:hidden p-2 rounded-xl text-stone-700 hover:bg-amber-100/50" aria-label="Abrir menú de navegación">
            <i class="fa-solid fa-bars text-2xl"></i>
          </button>
        </div>

      </div>
    </div>

    <!-- Mobile Dropdown Menu -->
    <div id="mobileMenu" class="hidden md:hidden bg-white border-b border-amber-100 px-6 py-4 space-y-3">
      <a href="#inicio" onclick="toggleMobileMenu()" class="block font-medium text-stone-700 hover:text-amberGold-600 py-1">Inicio</a>
      <a href="#beneficios" onclick="toggleMobileMenu()" class="block font-medium text-stone-700 hover:text-amberGold-600 py-1">Beneficios</a>
      <a href="#formula" onclick="toggleMobileMenu()" class="block font-medium text-stone-700 hover:text-amberGold-600 py-1">Curcu-Eliel Forte</a>
      <a href="#productos" onclick="toggleMobileMenu()" class="block font-medium text-stone-700 hover:text-amberGold-600 py-1">Productos</a>
      <a href="#testimonios" onclick="toggleMobileMenu()" class="block font-medium text-stone-700 hover:text-amberGold-600 py-1">Testimonios</a>
      <a href="#faq" onclick="toggleMobileMenu()" class="block font-medium text-stone-700 hover:text-amberGold-600 py-1">Preguntas</a>
      <a href="#productos" onclick="toggleMobileMenu()" class="block text-center bg-amberGold-500 text-white font-semibold py-2.5 rounded-xl shadow mt-3">Comprar Ahora</a>
    </div>
  </header>

  <main id="main-content">
  <section id="inicio" class="relative overflow-hidden pt-8 pb-16 lg:py-24 gold-gradient-bg border-b border-amber-100">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="grid grid-cols-1 lg:grid-cols-12 gap-12 items-center">
        
        <!-- Hero Text -->
        <div class="lg:col-span-7 space-y-6 text-center lg:text-left">
          
          <div class="inline-flex items-center gap-2 bg-amber-200/70 border border-amber-300 text-amberGold-900 px-4 py-1.5 rounded-full text-xs sm:text-sm font-semibold tracking-wide">
            <i class="fa-solid fa-certificate text-amberGold-600"></i>
            <span>Cúrcuma Orgánica Certificada 100% Pura</span>
          </div>

          <h1 class="font-heading text-4xl sm:text-5xl lg:text-6xl font-extrabold text-stone-900 leading-[1.15]">
            Revive tu vitalidad con el poder dorado de <br class="hidden sm:inline">
            <span class="text-gradient">Curcu-Eliel</span>
          </h1>

          <p class="text-stone-600 text-base sm:text-lg max-w-2xl mx-auto lg:mx-0 leading-relaxed">
            La fórmula bioactiva más avanzada: extracto puro de raíz de cúrcuma potenciado con <strong>piperina (pimienta negra)</strong> y jengibre para una absorción <span class="text-herbGreen-800 font-bold">20 veces superior</span>. Alivio articular, desinflamación profunda y energía sin químicos.
          </p>

          <!-- Badges Mini -->
          <div class="flex flex-wrap justify-center lg:justify-start gap-4 text-xs font-semibold text-stone-700 pt-2">
            <div class="flex items-center gap-2 bg-white/80 backdrop-blur px-3.5 py-2 rounded-xl border border-amber-200 shadow-sm">
              <i class="fa-solid fa-shield-heart text-herbGreen-600 text-base"></i>
              <span>Antiinflamatorio Activo</span>
            </div>
            <div class="flex items-center gap-2 bg-white/80 backdrop-blur px-3.5 py-2 rounded-xl border border-amber-200 shadow-sm">
              <i class="fa-solid fa-leaf text-amberGold-600 text-base"></i>
              <span>100% Vegano & Sin TACC</span>
            </div>
            <div class="flex items-center gap-2 bg-white/80 backdrop-blur px-3.5 py-2 rounded-xl border border-amber-200 shadow-sm">
              <i class="fa-solid fa-bolt text-amberGold-500 text-base"></i>
              <span>Máxima Biodisponibilidad</span>
            </div>
          </div>

          <!-- CTA Buttons -->
          <div class="flex flex-col sm:flex-row justify-center lg:justify-start gap-4 pt-4">
            <a href="#productos" class="inline-flex items-center justify-center gap-3 bg-amberGold-500 hover:bg-amberGold-600 text-white font-bold text-base px-8 py-4 rounded-2xl shadow-xl shadow-amberGold-500/20 hover:shadow-amberGold-600/30 transition-all transform hover:-translate-y-0.5">
              <i class="fa-solid fa-bag-shopping"></i>
              <span>Ver Ofertas de Cúrcuma</span>
            </a>
            <a href="https://wa.me/?text=Hola%20Curcu-Eliel,%20deseo%20m%C3%A1s%20informaci%C3%B3n%20y%20ofertas%20de%20sus%20productos" target="_blank" rel="noopener noreferrer" class="inline-flex items-center justify-center gap-3 bg-white hover:bg-stone-50 text-herbGreen-700 border-2 border-herbGreen-600 font-bold text-base px-7 py-4 rounded-2xl shadow-sm hover:shadow transition-all">
              <i class="fa-brands fa-whatsapp text-xl text-herbGreen-600"></i>
              <span>Consultar por WhatsApp</span>
            </a>
          </div>

          <!-- Social Proof Stars -->
          <div class="flex items-center justify-center lg:justify-start gap-3 pt-2 text-stone-600 text-sm">
            <div class="flex text-amber-400">
              <i class="fa-solid fa-star"></i>
              <i class="fa-solid fa-star"></i>
              <i class="fa-solid fa-star"></i>
              <i class="fa-solid fa-star"></i>
              <i class="fa-solid fa-star"></i>
            </div>
            <span><strong>4.9/5</strong> basado en más de 2,400 clientes en todo el país</span>
          </div>

        </div>

        <!-- Hero Graphic / Showcase Card -->
        <div class="lg:col-span-5 relative">
          <div class="relative mx-auto max-w-md">
            
            <!-- Glow background decor -->
            <div class="absolute -top-6 -left-6 w-64 h-64 bg-amberGold-300 rounded-full filter blur-3xl opacity-50 animate-pulse"></div>
            <div class="absolute -bottom-6 -right-6 w-64 h-64 bg-herbGreen-200 rounded-full filter blur-3xl opacity-40"></div>

            <div class="relative bg-white rounded-3xl p-6 sm:p-8 shadow-2xl border border-amber-200/80">
              <div class="relative rounded-2xl overflow-hidden mb-6 bg-amber-50 group">
                <img 
                  src="https://images.unsplash.com/photo-1615485290382-441e4d049cb5?auto=format&fit=crop&w=800&q=80" 
                  alt="Cúrcuma fresca y producto Curcu-Eliel" 
                  class="w-full h-72 object-cover rounded-2xl group-hover:scale-105 transition-transform duration-500"
                  onerror="this.src='https://placehold.co/600x400/d97706/ffffff?text=Curcu-Eliel+Premium'"
                />
                <span class="absolute top-3 left-3 bg-amberGold-500 text-white font-bold text-xs uppercase px-3 py-1.5 rounded-full shadow-md">
                  ⭐ Producto Estrella
                </span>
                <span class="absolute bottom-3 right-3 bg-stone-900/80 backdrop-blur-md text-white font-mono text-xs px-3 py-1 rounded-full">
                  Fórmula 95% Curcuminoides
                </span>
              </div>

              <div class="space-y-3">
                <div class="flex items-center justify-between">
                  <h2 class="font-heading font-bold text-2xl text-stone-900">Curcu-Eliel Forte Plus</h2>
                  <span class="text-2xl font-black text-amberGold-600">$24.99</span>
                </div>
                <p class="text-stone-500 text-sm">Frasco con 60 cápsulas vegetales concentradas de cúrcuma estandarizada con extracto de Bioperine®.</p>
                <div class="pt-2">
                  <button onclick="quickAddToCart(2)" class="w-full bg-herbGreen-700 hover:bg-herbGreen-800 text-white font-bold py-3 px-4 rounded-xl flex items-center justify-center gap-2 shadow-md transition-all">
                    <i class="fa-solid fa-cart-plus"></i>
                    <span>Añadir al Carrito Directo</span>
                  </button>
                </div>
              </div>
            </div>

          </div>
        </div>

      </div>
    </div>
  </section>

  <section id="beneficios" class="py-20 bg-white">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      
      <div class="text-center max-w-3xl mx-auto mb-16 space-y-4">
        <span class="text-herbGreen-700 font-bold uppercase tracking-wider text-xs sm:text-sm bg-herbGreen-50 border border-herbGreen-100 px-4 py-1 rounded-full">
          Medicina Milenaria respaldada por la Ciencia
        </span>
        <h2 class="font-heading text-3xl sm:text-4xl font-extrabold text-stone-900">
          ¿Por qué tu cuerpo agradecerá la Cúrcuma y Curcu-Eliel?
        </h2>
        <p class="text-stone-600 text-base sm:text-lg">
          La curcumina es uno de los antiinflamatorios naturales más investigados del planeta. Descubre cómo transforma tu bienestar integral cada día.
        </p>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
        
        <!-- Benefit Card 1 -->
        <div class="bg-amber-50/40 rounded-3xl p-8 border border-amber-100 hover:border-amber-300 hover:shadow-xl transition-all duration-300 group">
          <div class="w-14 h-14 rounded-2xl bg-amber-100 text-amberGold-600 flex items-center justify-center text-2xl mb-6 group-hover:scale-110 group-hover:bg-amberGold-500 group-hover:text-white transition-all">
            <i class="fa-solid fa-bone"></i>
          </div>
          <h3 class="font-heading font-bold text-xl text-stone-900 mb-3">Alivio y Flexibilidad Articular</h3>
          <p class="text-stone-600 text-sm leading-relaxed">
            Reduce la rigidez y las molestias en rodillas, manos y columna. Ideal para adultos mayores, deportistas y personas con molestias articulares recurrentes.
          </p>
        </div>

        <!-- Benefit Card 2 -->
        <div class="bg-amber-50/40 rounded-3xl p-8 border border-amber-100 hover:border-amber-300 hover:shadow-xl transition-all duration-300 group">
          <div class="w-14 h-14 rounded-2xl bg-herbGreen-100 text-herbGreen-600 flex items-center justify-center text-2xl mb-6 group-hover:scale-110 group-hover:bg-herbGreen-600 group-hover:text-white transition-all">
            <i class="fa-solid fa-shield-virus"></i>
          </div>
          <h3 class="font-heading font-bold text-xl text-stone-900 mb-3">Poderoso Antioxidante</h3>
          <p class="text-stone-600 text-sm leading-relaxed">
            Neutraliza los radicales libres y estimula las defensas enzimáticas del organismo, protegiendo las células frente al envejecimiento prematuro.
          </p>
        </div>

        <!-- Benefit Card 3 -->
        <div class="bg-amber-50/40 rounded-3xl p-8 border border-amber-100 hover:border-amber-300 hover:shadow-xl transition-all duration-300 group">
          <div class="w-14 h-14 rounded-2xl bg-amber-100 text-amberGold-600 flex items-center justify-center text-2xl mb-6 group-hover:scale-110 group-hover:bg-amberGold-500 group-hover:text-white transition-all">
            <i class="fa-solid fa-heart-pulse"></i>
          </div>
          <h3 class="font-heading font-bold text-xl text-stone-900 mb-3">Salud Cardiovascular & Celular</h3>
          <p class="text-stone-600 text-sm leading-relaxed">
            Favorece la función endotelial y la regulación del colesterol, manteniendo arterias más flexibles y una circulación sanguínea más eficiente.
          </p>
        </div>

        <!-- Benefit Card 4 -->
        <div class="bg-amber-50/40 rounded-3xl p-8 border border-amber-100 hover:border-amber-300 hover:shadow-xl transition-all duration-300 group">
          <div class="w-14 h-14 rounded-2xl bg-amber-100 text-amberGold-600 flex items-center justify-center text-2xl mb-6 group-hover:scale-110 group-hover:bg-amberGold-500 group-hover:text-white transition-all">
            <i class="fa-solid fa-apple-whole"></i>
          </div>
          <h3 class="font-heading font-bold text-xl text-stone-900 mb-3">Digestión Liviana y Deshinchazón</h3>
          <p class="text-stone-600 text-sm leading-relaxed">
            Estimula suavemente la secreción biliar facilitando la digestión de grasas, calmando la pesadez estomacal y los gases recurrentes.
          </p>
        </div>

        <!-- Benefit Card 5 -->
        <div class="bg-amber-50/40 rounded-3xl p-8 border border-amber-100 hover:border-amber-300 hover:shadow-xl transition-all duration-300 group">
          <div class="w-14 h-14 rounded-2xl bg-herbGreen-100 text-herbGreen-600 flex items-center justify-center text-2xl mb-6 group-hover:scale-110 group-hover:bg-herbGreen-600 group-hover:text-white transition-all">
            <i class="fa-solid fa-brain"></i>
          </div>
          <h3 class="font-heading font-bold text-xl text-stone-900 mb-3">Enfoque y Memoria Ágil</h3>
          <p class="text-stone-600 text-sm leading-relaxed">
            La curcumina eleva los niveles del factor neurotrófico cerebral (BDNF), estimulando la claridad mental, el estado de ánimo y la memoria.
          </p>
        </div>

        <!-- Benefit Card 6 -->
        <div class="bg-amber-50/40 rounded-3xl p-8 border border-amber-100 hover:border-amber-300 hover:shadow-xl transition-all duration-300 group">
          <div class="w-14 h-14 rounded-2xl bg-amber-100 text-amberGold-600 flex items-center justify-center text-2xl mb-6 group-hover:scale-110 group-hover:bg-amberGold-500 group-hover:text-white transition-all">
            <i class="fa-solid fa-sun"></i>
          </div>
          <h3 class="font-heading font-bold text-xl text-stone-900 mb-3">Energía y Desintoxicación Diaria</h3>
          <p class="text-stone-600 text-sm leading-relaxed">
            Favorece el trabajo de depuración del hígado y acelera la eliminación de toxinas metabólicas, brindándote mayor vitalidad desde la primera semana.
          </p>
        </div>

      </div>
    </div>
  </section>

  <section id="formula" class="py-20 bg-stone-900 text-white relative overflow-hidden">
    <!-- Ambient glowing light -->
    <div class="absolute -top-32 left-1/2 -translate-x-1/2 w-96 h-96 bg-amber-500/20 rounded-full blur-3xl pointer-events-none"></div>

    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 relative">
      <div class="grid grid-cols-1 lg:grid-cols-12 gap-12 items-center">
        
        <div class="lg:col-span-6 space-y-6">
          <div class="inline-flex items-center gap-2 bg-amber-500/20 border border-amber-500/40 text-amber-300 px-4 py-1.5 rounded-full text-xs font-semibold">
            <i class="fa-solid fa-dna"></i>
            <span>La Diferencia Científica de Curcu-Eliel</span>
          </div>

          <h2 class="font-heading text-3xl sm:text-4xl lg:text-5xl font-extrabold text-white leading-tight">
            ¿Por qué la cúrcuma común no es suficiente?
          </h2>

          <p class="text-stone-300 leading-relaxed text-base">
            El mayor desafío de la cúrcuma pura es su <strong>baja biodisponibilidad</strong>: el cuerpo apenas absorbe una pequeña fracción por sí solo. Por eso nació <span class="text-amber-400 font-bold">Curcu-Eliel</span>.
          </p>

          <div class="space-y-4 pt-2">
            <div class="flex items-start gap-4 p-4 rounded-2xl bg-stone-800/80 border border-stone-700">
              <div class="w-10 h-10 rounded-xl bg-amber-500/20 text-amber-400 flex items-center justify-center shrink-0 mt-1">
                <i class="fa-solid fa-pepper-hot text-lg"></i>
              </div>
              <div>
                <h3 class="font-bold text-white text-lg">Extracto de Piperina (Pimienta Negra)</h3>
                <p class="text-stone-400 text-sm">Incrementa la absorción gastrointestinal de los curcuminoides hasta en un <span class="text-amber-400 font-semibold">2,000%</span> sin irritar el estómago.</p>
              </div>
            </div>

            <div class="flex items-start gap-4 p-4 rounded-2xl bg-stone-800/80 border border-stone-700">
              <div class="w-10 h-10 rounded-xl bg-herbGreen-500/20 text-herbGreen-400 flex items-center justify-center shrink-0 mt-1">
                <i class="fa-solid fa-leaf text-lg"></i>
              </div>
              <div>
                <h3 class="font-bold text-white text-lg">Estandarización al 95% de Curcuminoides</h3>
                <p class="text-stone-400 text-sm">Cada cápsula equivale a más de 12 cucharadas de cúrcuma común, garantizando una dosis terapéutica efectiva y constante.</p>
              </div>
            </div>

            <div class="flex items-start gap-4 p-4 rounded-2xl bg-stone-800/80 border border-stone-700">
              <div class="w-10 h-10 rounded-xl bg-amber-500/20 text-amber-400 flex items-center justify-center shrink-0 mt-1">
                <i class="fa-solid fa-seedling text-lg"></i>
              </div>
              <div>
                <h3 class="font-bold text-white text-lg">Cápsulas 100% Vegetales (HPMC)</h3>
                <p class="text-stone-400 text-sm">Libres de estearato de magnesio sintético, gelatina animal, conservantes y gluten. Apto para dietas veganas y celíacos.</p>
              </div>
            </div>
          </div>

          <div class="pt-2">
            <a href="#productos" class="inline-flex items-center gap-2 bg-amber-500 hover:bg-amber-400 text-stone-900 font-bold px-7 py-3.5 rounded-xl shadow-lg transition-colors">
              <span>Descubrir la gama Curcu-Eliel</span>
              <i class="fa-solid fa-arrow-down text-sm"></i>
            </a>
          </div>
        </div>

        <!-- Comparative Interactive Card -->
        <div class="lg:col-span-6">
          <div class="bg-gradient-to-b from-stone-800 to-stone-850 rounded-3xl p-6 sm:p-8 border border-stone-700 shadow-2xl">
            <h3 class="font-heading font-bold text-xl text-center text-white mb-6">Comparativa de Absorción</h3>
            
            <div class="space-y-6">
              <div>
                <div class="flex justify-between text-sm mb-2">
                  <span class="text-stone-400 font-medium">Cúrcuma en polvo convencional</span>
                  <span class="text-red-400 font-bold">Aprox. 2% a 5%</span>
                </div>
                <div class="w-full bg-stone-700 h-3.5 rounded-full overflow-hidden">
                  <div class="bg-red-400 h-full rounded-full" style="width: 5%"></div>
                </div>
                <span class="text-xs text-stone-500 mt-1 block">El hígado la metaboliza y expulsa rápidamente.</span>
              </div>

              <div>
                <div class="flex justify-between text-sm mb-2">
                  <span class="text-amber-300 font-bold flex items-center gap-2">
                    <i class="fa-solid fa-crown text-xs text-amber-400"></i> Fórmula Curcu-Eliel Forte Plus
                  </span>
                  <span class="text-herbGreen-400 font-black">Hasta 95% de Asimilación</span>
                </div>
                <div class="w-full bg-stone-700 h-3.5 rounded-full overflow-hidden">
                  <div class="bg-gradient-to-r from-amberGold-500 to-herbGreen-500 h-full rounded-full shadow-lg" style="width: 95%"></div>
                </div>
                <span class="text-xs text-herbGreen-300/80 mt-1 block">La sinergia con piperina asegura la entrada al torrente sanguíneo.</span>
              </div>
            </div>

            <!-- Guarantee Seal Box -->
            <div class="mt-8 pt-6 border-t border-stone-700 flex items-center gap-4">
              <div class="w-12 h-12 rounded-full bg-amber-500/10 border border-amber-500/30 flex items-center justify-center text-amber-400 shrink-0">
                <i class="fa-solid fa-award text-2xl"></i>
              </div>
              <p class="text-xs text-stone-300 leading-relaxed">
                <strong>Garantía de Satisfacción Total:</strong> Si en 30 días no sientes la diferencia en tus articulaciones y energía, te devolvemos el 100% de tu dinero sin preguntas.
              </p>
            </div>
          </div>
        </div>

      </div>
    </div>
  </section>

  <section id="productos" class="py-20 bg-amber-50/50">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      
      <div class="text-center max-w-3xl mx-auto mb-12 space-y-3">
        <span class="text-amberGold-700 font-bold uppercase tracking-wider text-xs sm:text-sm bg-amber-100 border border-amber-200 px-4 py-1 rounded-full">
          Tienda Oficial
        </span>
        <h2 class="font-heading text-3xl sm:text-4xl font-extrabold text-stone-900">
          Nuestras Presentaciones y Combos Especiales
        </h2>
        <p class="text-stone-600 text-base">
          Selecciona tu producto favorito o aprovecha los combos con descuentos exclusivos y envíos bonificados.
        </p>
      </div>

      <!-- Filter Buttons -->
      <div class="flex justify-center gap-2 sm:gap-4 mb-10 overflow-x-auto pb-2 no-scrollbar">
        <button onclick="filterProducts('todos')" class="filter-btn active bg-stone-900 text-white text-xs sm:text-sm font-semibold px-5 py-2.5 rounded-full transition-all shadow" data-cat="todos">Todos</button>
        <button onclick="filterProducts('capsulas')" class="filter-btn bg-white hover:bg-amber-100 text-stone-700 text-xs sm:text-sm font-semibold px-5 py-2.5 rounded-full border border-amber-200 transition-all shadow-sm" data-cat="capsulas">Cápsulas Curcu-Eliel</button>
        <button onclick="filterProducts('polvo')" class="filter-btn bg-white hover:bg-amber-100 text-stone-700 text-xs sm:text-sm font-semibold px-5 py-2.5 rounded-full border border-amber-200 transition-all shadow-sm" data-cat="polvo">Cúrcuma en Polvo Pura</button>
        <button onclick="filterProducts('combos')" class="filter-btn bg-white hover:bg-amber-100 text-stone-700 text-xs sm:text-sm font-semibold px-5 py-2.5 rounded-full border border-amber-200 transition-all shadow-sm" data-cat="combos">Packs & Combos</button>
      </div>

      <!-- Product Grid -->
      <div id="productGrid" class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-8">
        <!-- Products dynamically injected by JavaScript -->
      </div>

      <!-- Bottom Order Assurance banner -->
      <div class="mt-14 bg-white rounded-2xl p-6 border border-amber-200 shadow-sm flex flex-col md:flex-row items-center justify-between gap-6">
        <div class="flex items-center gap-4">
          <div class="w-12 h-12 rounded-xl bg-herbGreen-100 text-herbGreen-700 flex items-center justify-center text-2xl shrink-0">
            <i class="fa-solid fa-truck-fast"></i>
          </div>
          <div>
            <h4 class="font-bold text-stone-900 text-base">Envíos Rápidos y Seguros</h4>
            <p class="text-xs text-stone-500">Despachamos en 24/48 horas con número de seguimiento y pago contra entrega disponible en zonas seleccionadas.</p>
          </div>
        </div>
        <div class="flex items-center gap-3">
          <button onclick="toggleCartModal()" class="inline-flex items-center gap-2 bg-amberGold-500 hover:bg-amberGold-600 text-white font-bold text-sm px-6 py-3 rounded-xl shadow transition-colors">
            <i class="fa-solid fa-shopping-bag"></i>
            <span>Ver mi Pedido</span>
          </button>
        </div>
      </div>

    </div>
  </section>

  <section id="testimonios" class="py-20 bg-white border-t border-amber-100">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      
      <div class="text-center max-w-3xl mx-auto mb-16 space-y-3">
        <span class="text-herbGreen-700 font-bold uppercase tracking-wider text-xs sm:text-sm bg-herbGreen-50 border border-herbGreen-100 px-4 py-1 rounded-full">
          Casos Reales
        </span>
        <h2 class="font-heading text-3xl sm:text-4xl font-extrabold text-stone-900">
          Lo que dicen quienes ya toman Curcu-Eliel
        </h2>
        <p class="text-stone-600">Historias de personas que recuperaron su movilidad y vitalidad cotidiana.</p>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
        
        <!-- Review 1 -->
        <div class="bg-amber-50/30 rounded-3xl p-8 border border-amber-100 flex flex-col justify-between shadow-sm hover:shadow-md transition-shadow">
          <div class="space-y-4">
            <div class="flex text-amber-400 text-sm">
              <i class="fa-solid fa-star"></i>
              <i class="fa-solid fa-star"></i>
              <i class="fa-solid fa-star"></i>
              <i class="fa-solid fa-star"></i>
              <i class="fa-solid fa-star"></i>
            </div>
            <p class="text-stone-700 text-sm italic leading-relaxed">
              "Llevaba dos años sufriendo dolor en la rodilla derecha al bajar escaleras. A las tres semanas de tomar dos cápsulas de Curcu-Eliel al día, la inflamación cedió notablemente. Ahora camino sin molestias."
            </p>
          </div>
          <div class="flex items-center gap-3 pt-6 border-t border-amber-100 mt-6">
            <div class="w-11 h-11 rounded-full bg-amberGold-200 text-amberGold-800 font-bold flex items-center justify-center text-sm shadow-inner">
              MC
            </div>
            <div>
              <h4 class="font-bold text-stone-900 text-sm">Marta Calderón, 58 años</h4>
              <span class="text-xs text-stone-500 flex items-center gap-1">
                <i class="fa-solid fa-circle-check text-herbGreen-600"></i> Comprador verificado
              </span>
            </div>
          </div>
        </div>

        <!-- Review 2 -->
        <div class="bg-amber-50/30 rounded-3xl p-8 border border-amber-100 flex flex-col justify-between shadow-sm hover:shadow-md transition-shadow">
          <div class="space-y-4">
            <div class="flex text-amber-400 text-sm">
              <i class="fa-solid fa-star"></i>
              <i class="fa-solid fa-star"></i>
              <i class="fa-solid fa-star"></i>
              <i class="fa-solid fa-star"></i>
              <i class="fa-solid fa-star"></i>
            </div>
            <p class="text-stone-700 text-sm italic leading-relaxed">
              "El combo familiar es fabuloso. Yo uso las cápsulas para mis entrenamientos de crossfit (recuperación articular inmediata) y mi esposa usa la cúrcuma en polvo pura en batidos matutinos y leche dorada. Súper aromática."
            </p>
          </div>
          <div class="flex items-center gap-3 pt-6 border-t border-amber-100 mt-6">
            <div class="w-11 h-11 rounded-full bg-herbGreen-200 text-herbGreen-800 font-bold flex items-center justify-center text-sm shadow-inner">
              DR
            </div>
            <div>
              <h4 class="font-bold text-stone-900 text-sm">David Ramírez, 39 años</h4>
              <span class="text-xs text-stone-500 flex items-center gap-1">
                <i class="fa-solid fa-circle-check text-herbGreen-600"></i> Comprador verificado
              </span>
            </div>
          </div>
        </div>

        <!-- Review 3 -->
        <div class="bg-amber-50/30 rounded-3xl p-8 border border-amber-100 flex flex-col justify-between shadow-sm hover:shadow-md transition-shadow">
          <div class="space-y-4">
            <div class="flex text-amber-400 text-sm">
              <i class="fa-solid fa-star"></i>
              <i class="fa-solid fa-star"></i>
              <i class="fa-solid fa-star"></i>
              <i class="fa-solid fa-star"></i>
              <i class="fa-solid fa-star"></i>
            </div>
            <p class="text-stone-700 text-sm italic leading-relaxed">
              "Padecía de digestiones lentas y vientre hinchado todas las noches. Desde que tomo Curcu-Eliel después del almuerzo me siento liviana, con la digestión impecable y más energía por las tardes."
            </p>
          </div>
          <div class="flex items-center gap-3 pt-6 border-t border-amber-100 mt-6">
            <div class="w-11 h-11 rounded-full bg-amberGold-200 text-amberGold-800 font-bold flex items-center justify-center text-sm shadow-inner">
              LP
            </div>
            <div>
              <h4 class="font-bold text-stone-900 text-sm">Laura Paredes, 46 años</h4>
              <span class="text-xs text-stone-500 flex items-center gap-1">
                <i class="fa-solid fa-circle-check text-herbGreen-600"></i> Comprador verificado
              </span>
            </div>
          </div>
        </div>

      </div>
    </div>
  </section>

  <section id="faq" class="py-20 bg-amber-50/40">
    <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
      
      <div class="text-center max-w-2xl mx-auto mb-12 space-y-3">
        <h2 class="font-heading text-3xl sm:text-4xl font-extrabold text-stone-900">
          Preguntas Frecuentes
        </h2>
        <p class="text-stone-600 text-sm sm:text-base">
          Todo lo que necesitas saber antes de comenzar a tomar Curcu-Eliel y cúrcuma pura.
        </p>
      </div>

      <div class="space-y-4">
        
        <!-- FAQ 1 -->
        <div class="bg-white rounded-2xl border border-amber-200 overflow-hidden transition-all">
          <button onclick="toggleFaq(1)" class="w-full text-left px-6 py-5 flex items-center justify-between font-heading font-bold text-base sm:text-lg text-stone-900 focus:outline-none">
            <span>¿Cómo se debe tomar Curcu-Eliel Forte?</span>
            <i id="faq-icon-1" class="fa-solid fa-chevron-down text-amberGold-600 transition-transform duration-300"></i>
          </button>
          <div id="faq-ans-1" class="hidden px-6 pb-5 text-sm text-stone-600 leading-relaxed border-t border-amber-100 pt-3">
            Se recomienda tomar 2 cápsulas al día: una con el desayuno y otra con el almuerzo o cena, preferiblemente acompañadas de algún alimento que contenga grasas saludables (como aceite de oliva, palta/aguacate o frutos secos) para optimizar la biodisponibilidad de los curcuminoides.
          </div>
        </div>

        <!-- FAQ 2 -->
        <div class="bg-white rounded-2xl border border-amber-200 overflow-hidden transition-all">
          <button onclick="toggleFaq(2)" class="w-full text-left px-6 py-5 flex items-center justify-between font-heading font-bold text-base sm:text-lg text-stone-900 focus:outline-none">
            <span>¿En cuánto tiempo comenzaré a notar los resultados?</span>
            <i id="faq-icon-2" class="fa-solid fa-chevron-down text-amberGold-600 transition-transform duration-300"></i>
          </button>
          <div id="faq-ans-2" class="hidden px-6 pb-5 text-sm text-stone-600 leading-relaxed border-t border-amber-100 pt-3">
            La mayoría de personas reporta mejoras en la digestión y menor pesadez en los primeros 5 a 7 días. En molestias articulares o musculares acumuladas, los efectos antiinflamatorios más evidentes se perciben entre la segunda y tercera semana de consumo diario ininterrumpido.
          </div>
        </div>

        <!-- FAQ 3 -->
        <div class="bg-white rounded-2xl border border-amber-200 overflow-hidden transition-all">
          <button onclick="toggleFaq(3)" class="w-full text-left px-6 py-5 flex items-center justify-between font-heading font-bold text-base sm:text-lg text-stone-900 focus:outline-none">
            <span>¿Tiene alguna contraindicación o efecto secundario?</span>
            <i id="faq-icon-3" class="fa-solid fa-chevron-down text-amberGold-600 transition-transform duration-300"></i>
          </button>
          <div id="faq-ans-3" class="hidden px-6 pb-5 text-sm text-stone-600 leading-relaxed border-t border-amber-100 pt-3">
            Curcu-Eliel es un suplemento natural seguro. Sin embargo, no se aconseja en personas con cálculos biliares obstructivos ni en personas bajo tratamiento anticoagulante intenso sin supervisión médica previa. Tampoco está recomendado durante el embarazo y lactancia sin autorización de su obstetra.
          </div>
        </div>

        <!-- FAQ 4 -->
        <div class="bg-white rounded-2xl border border-amber-200 overflow-hidden transition-all">
          <button onclick="toggleFaq(4)" class="w-full text-left px-6 py-5 flex items-center justify-between font-heading font-bold text-base sm:text-lg text-stone-900 focus:outline-none">
            <span>¿Cómo se realiza el pago y la entrega?</span>
            <i id="faq-icon-4" class="fa-solid fa-chevron-down text-amberGold-600 transition-transform duration-300"></i>
          </button>
          <div id="faq-ans-4" class="hidden px-6 pb-5 text-sm text-stone-600 leading-relaxed border-t border-amber-100 pt-3">
            Aceptamos transferencias bancarias, tarjetas de débito/crédito y billeteras móviles. También ofrecemos servicio contra entrega en las principales ciudades. Puedes realizar tu pedido mediante el carrito web o directamente por WhatsApp con atención personalizada.
          </div>
        </div>

      </div>
    </div>
  </section>

  <section id="contacto" class="py-20 bg-white">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="bg-gradient-to-br from-amberGold-600 via-amberGold-700 to-stone-900 rounded-3xl p-8 sm:p-12 text-white shadow-2xl relative overflow-hidden">
        
        <div class="grid grid-cols-1 lg:grid-cols-12 gap-10 items-center">
          
          <div class="lg:col-span-7 space-y-6">
            <span class="bg-white/20 text-amber-100 text-xs font-bold uppercase tracking-wider px-3.5 py-1.5 rounded-full inline-block backdrop-blur-sm">
              Atención Directa y Personalizada
            </span>
            <h2 class="font-heading text-3xl sm:text-4xl lg:text-5xl font-extrabold text-white leading-tight">
              ¿Dudas sobre cuál presentación es la ideal para ti?
            </h2>
            <p class="text-amber-100/90 text-base max-w-lg leading-relaxed">
              Escríbenos directamente. Un asesor especialista en nutrición natural resolverá tus consultas sobre dosis, compatibilidad y envíos sin ningún compromiso.
            </p>
            
            <div class="flex flex-wrap gap-6 pt-2 text-sm">
              <div class="flex items-center gap-3">
                <i class="fa-brands fa-whatsapp text-2xl text-herbGreen-400"></i>
                <div>
                  <span class="block text-xs text-amber-200">WhatsApp de Ventas</span>
                  <span class="font-bold">+51 987 654 321</span>
                </div>
              </div>
              <div class="flex items-center gap-3">
                <i class="fa-solid fa-envelope text-xl text-amber-300"></i>
                <div>
                  <span class="block text-xs text-amber-200">Correo Oficial</span>
                  <span class="font-bold">contacto@curcu-eliel.com</span>
                </div>
              </div>
            </div>
          </div>

          <!-- Fast Contact Card -->
          <div class="lg:col-span-5 bg-white text-stone-800 rounded-2xl p-6 sm:p-8 shadow-xl">
            <h3 class="font-heading font-bold text-xl text-stone-900 mb-2">Solicitar Asesoría Inmediata</h3>
            <p class="text-stone-500 text-xs mb-5">Déjanos tu mensaje y te contactaremos por WhatsApp en minutos.</p>
            
            <form id="leadForm" onsubmit="handleLeadSubmit(event)" class="space-y-4">
              <div>
                <label for="leadName" class="block text-xs font-semibold text-stone-700 uppercase mb-1">Nombre Completo</label>
                <input type="text" id="leadName" required placeholder="Ej. Roberto Gómez" class="w-full px-4 py-2.5 rounded-xl border border-stone-300 focus:outline-none focus:ring-2 focus:ring-amberGold-500 text-sm">
              </div>

              <div>
                <label for="leadPhone" class="block text-xs font-semibold text-stone-700 uppercase mb-1">WhatsApp / Teléfono</label>
                <input type="tel" id="leadPhone" required placeholder="Ej. +51 987 123 456" class="w-full px-4 py-2.5 rounded-xl border border-stone-300 focus:outline-none focus:ring-2 focus:ring-amberGold-500 text-sm">
              </div>

              <div>
                <label for="leadInterest" class="block text-xs font-semibold text-stone-700 uppercase mb-1">Interés Principal</label>
                <select id="leadInterest" class="w-full px-4 py-2.5 rounded-xl border border-stone-300 focus:outline-none focus:ring-2 focus:ring-amberGold-500 text-sm bg-white">
                  <option value="Curcu-Eliel Forte (Cápsulas)">Curcu-Eliel Forte (Cápsulas)</option>
                  <option value="Cúrcuma en Polvo Pura">Cúrcuma Orgánica en Polvo</option>
                  <option value="Combo Familiar o Promoción">Combos Promocionales</option>
                  <option value="Consulta sobre Dolores Articulares">Dolores Articulares / Inflamación</option>
                </select>
              </div>

              <button type="submit" class="w-full bg-herbGreen-600 hover:bg-herbGreen-700 text-white font-bold py-3 px-4 rounded-xl shadow-md transition-all flex items-center justify-center gap-2">
                <i class="fa-brands fa-whatsapp text-lg"></i>
                <span>Enviar Consulta por WhatsApp</span>
              </button>
            </form>
          </div>

        </div>

      </div>
    </div>
  </section>
  </main>

  <footer class="bg-stone-900 text-stone-400 text-sm pt-16 pb-12 border-t border-stone-800">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-10 mb-12">
        
        <!-- Brand summary -->
        <div class="space-y-4">
          <div class="flex items-center gap-3">
            <div class="w-10 h-10 rounded-xl bg-amberGold-500 flex items-center justify-center text-white">
              <i class="fa-solid fa-mortar-pestle"></i>
            </div>
            <span class="font-heading font-extrabold text-xl text-white tracking-tight">
              CURCU<span class="text-amberGold-500">-ELIEL</span>
            </span>
          </div>
          <p class="text-xs text-stone-400 leading-relaxed">
            Comprometidos con llevar a tu mesa la cúrcuma más pura, potente y biológicamente activa para nutrir tu salud de forma 100% natural.
          </p>
          <div class="flex items-center gap-3 pt-2">
            <a href="#" class="w-8 h-8 rounded-full bg-stone-800 flex items-center justify-center text-stone-300 hover:text-amberGold-400 hover:bg-stone-700 transition-colors" aria-label="Facebook"><i class="fa-brands fa-facebook-f text-xs"></i></a>
            <a href="#" class="w-8 h-8 rounded-full bg-stone-800 flex items-center justify-center text-stone-300 hover:text-amberGold-400 hover:bg-stone-700 transition-colors" aria-label="Instagram"><i class="fa-brands fa-instagram text-xs"></i></a>
            <a href="#" class="w-8 h-8 rounded-full bg-stone-800 flex items-center justify-center text-stone-300 hover:text-amberGold-400 hover:bg-stone-700 transition-colors" aria-label="YouTube"><i class="fa-brands fa-youtube text-xs"></i></a>
            <a href="#" class="w-8 h-8 rounded-full bg-stone-800 flex items-center justify-center text-stone-300 hover:text-amberGold-400 hover:bg-stone-700 transition-colors" aria-label="TikTok"><i class="fa-brands fa-tiktok text-xs"></i></a>
          </div>
        </div>

        <!-- Quick Links -->
        <div>
          <h4 class="font-heading font-bold text-white text-base mb-4">Navegación</h4>
          <ul class="space-y-2 text-xs">
            <li><a href="#inicio" class="hover:text-amberGold-400 transition-colors">Inicio</a></li>
            <li><a href="#beneficios" class="hover:text-amberGold-400 transition-colors">Beneficios Clínicos</a></li>
            <li><a href="#formula" class="hover:text-amberGold-400 transition-colors">Fórmula Curcu-Eliel</a></li>
            <li><a href="#productos" class="hover:text-amberGold-400 transition-colors">Catálogo y Precios</a></li>
            <li><a href="#testimonios" class="hover:text-amberGold-400 transition-colors">Opiniones de Clientes</a></li>
          </ul>
        </div>

        <!-- Legal and Quality -->
        <div>
          <h4 class="font-heading font-bold text-white text-base mb-4">Calidad & Seguridad</h4>
          <ul class="space-y-2 text-xs">
            <li>Registro Sanitario Vigente</li>
            <li>Cúrcuma 100% Orgánica certificada</li>
            <li>Sin aditivos artificiales ni GMO</li>
            <li>Política de Devolución de 30 días</li>
            <li>Términos y Condiciones</li>
          </ul>
        </div>

        <!-- Contact Box -->
        <div>
          <h4 class="font-heading font-bold text-white text-base mb-4">Contacto</h4>
          <ul class="space-y-2 text-xs">
            <li class="flex items-center gap-2"><i class="fa-solid fa-location-dot text-amberGold-500"></i> Distribución a nivel nacional</li>
            <li class="flex items-center gap-2"><i class="fa-brands fa-whatsapp text-herbGreen-500"></i> WhatsApp: +51 987 654 321</li>
            <li class="flex items-center gap-2"><i class="fa-solid fa-clock text-amberGold-500"></i> Lun - Sáb: 8:00 AM - 8:00 PM</li>
            <li class="flex items-center gap-2"><i class="fa-solid fa-shield text-herbGreen-500"></i> Compra 100% Protegida</li>
          </ul>
        </div>

      </div>

      <div class="pt-8 border-t border-stone-800 text-center text-xs text-stone-500">
        <p>© 2026 Curcu-Eliel Natural Labs. Todos los derechos reservados. Este producto es un suplemento alimentario natural y no sustituye el tratamiento prescrito por un médico especialista.</p>
      </div>
    </div>
  </footer>

  <div id="cartModal" class="fixed inset-0 z-50 bg-stone-900/60 backdrop-blur-sm hidden flex justify-end">
    <div class="w-full max-w-md bg-white h-full shadow-2xl flex flex-col justify-between overflow-hidden animate-in slide-in-from-right duration-300">
      
      <!-- Cart Header -->
      <div class="p-5 border-b border-amber-100 flex items-center justify-between bg-amber-50/50">
        <div class="flex items-center gap-2">
          <i class="fa-solid fa-cart-shopping text-amberGold-600 text-xl"></i>
          <h3 class="font-heading font-bold text-lg text-stone-900">Tu Carrito de Bienestar</h3>
        </div>
        <button onclick="toggleCartModal()" class="w-8 h-8 rounded-full bg-stone-100 hover:bg-stone-200 text-stone-600 flex items-center justify-center transition-colors" aria-label="Cerrar carrito">
          <i class="fa-solid fa-xmark text-lg"></i>
        </button>
      </div>

      <!-- Cart Items Container -->
      <div id="cartItemsList" class="flex-1 overflow-y-auto p-5 space-y-4">
        <!-- Injected dynamically -->
      </div>

      <!-- Cart Footer / Summary -->
      <div class="p-5 border-t border-amber-100 bg-amber-50/30 space-y-4">
        <div class="space-y-1.5 text-sm">
          <div class="flex justify-between text-stone-500">
            <span>Subtotal</span>
            <span id="cartSubtotal" class="font-medium">$0.00</span>
          </div>
          <div class="flex justify-between text-stone-500">
            <span>Envío</span>
            <span id="cartShipping" class="font-medium text-herbGreen-600">Gratis por tiempo limitado</span>
          </div>
          <div class="flex justify-between text-stone-900 font-bold text-lg pt-2 border-t border-amber-200">
            <span>Total a Pagar</span>
            <span id="cartTotal" class="text-amberGold-700 font-black">$0.00</span>
          </div>
        </div>

        <div class="space-y-2">
          <button onclick="checkoutWhatsApp()" class="w-full bg-herbGreen-600 hover:bg-herbGreen-700 text-white font-bold py-3.5 px-4 rounded-xl shadow-lg transition-all flex items-center justify-center gap-2">
            <i class="fa-brands fa-whatsapp text-xl"></i>
            <span>Confirmar Pedido por WhatsApp</span>
          </button>
          <button onclick="toggleCartModal()" class="w-full bg-white hover:bg-stone-100 text-stone-700 border border-stone-300 font-semibold py-2.5 px-4 rounded-xl text-xs transition-colors">
            Seguir explorando
          </button>
        </div>
        
        <p class="text-[11px] text-center text-stone-400">
          <i class="fa-solid fa-lock text-stone-400"></i> No cobramos por adelantado. Acuerdas el pago directamente con el asesor.
        </p>
      </div>

    </div>
  </div>

  <div id="toastNotification" class="fixed bottom-6 left-6 z-50 bg-stone-900 text-white px-5 py-3.5 rounded-2xl shadow-2xl flex items-center gap-3 transform transition-all duration-300 translate-y-24 opacity-0 pointer-events-none">
    <div class="w-8 h-8 rounded-full bg-herbGreen-600 flex items-center justify-center text-white text-sm shrink-0">
      <i class="fa-solid fa-check"></i>
    </div>
    <div>
      <h4 class="font-bold text-xs" id="toastTitle">Producto añadido</h4>
      <p class="text-[11px] text-stone-300" id="toastDesc">Se sumó correctamente al carrito.</p>
    </div>
  </div>

  <script>
    // Product Catalog Database
    const products = [
      {
        id: 1,
        title: "Cúrcuma en Polvo Orgánica 250g",
        category: "polvo",
        price: 11.99,
        originalPrice: 15.00,
        badge: "Pura & Aromática",
        rating: 4.8,
        description: "Raíz de cúrcuma seleccionada finamente molida. Ideal para leche dorada (Golden Milk), jugos, guisos e infusiones digestivas.",
        image: "https://images.unsplash.com/photo-1615485290382-441e4d049cb5?auto=format&fit=crop&w=600&q=80"
      },
      {
        id: 2,
        title: "Curcu-Eliel Forte (60 Cápsulas)",
        category: "capsulas",
        price: 24.99,
        originalPrice: 32.00,
        badge: "⭐ El Más Vendido",
        rating: 5.0,
        description: "Fórmula de alta potencia: 95% curcuminoides enriquecida con Piperina (Bioperine) para absorción multiplicada x20. Alivio articular profundo.",
        image: "https://images.unsplash.com/photo-1584308666744-24d5c474f2ae?auto=format&fit=crop&w=600&q=80"
      },
      {
        id: 3,
        title: "Curcu-Eliel + Jengibre & Vitamina C",
        category: "capsulas",
        price: 27.50,
        originalPrice: 35.00,
        badge: "Inmunidad Total",
        rating: 4.9,
        description: "Triple acción desinflamatoria y escudo inmunológico. Diseñada para proteger las vías respiratorias y la salud celular diaria.",
        image: "https://images.unsplash.com/photo-1550572017-edd951aa8f72?auto=format&fit=crop&w=600&q=80"
      },
      {
        id: 4,
        title: "Pack Dúo Curcu-Eliel (120 Cápsulas)",
        category: "combos",
        price: 44.99,
        originalPrice: 59.99,
        badge: "Ahorra 25%",
        rating: 5.0,
        description: "Tratamiento completo para 2 meses de desinflamación y cuidado de cartílagos. Incluye guía nutricional antiinflamatoria en PDF.",
        image: "https://images.unsplash.com/photo-1628771065518-0d82f1938462?auto=format&fit=crop&w=600&q=80"
      },
      {
        id: 5,
        title: "Cúrcuma Orgánica a Granel 1 Kg",
        category: "polvo",
        price: 29.00,
        originalPrice: 38.00,
        badge: "Formato Económico",
        rating: 4.8,
        description: "Empaque hermético aluminizado con cierre ziploc para conservar sus aceites esenciales y poder curcuminoide por meses.",
        image: "https://images.unsplash.com/photo-1615485500704-8e990f9900f7?auto=format&fit=crop&w=600&q=80"
      },
      {
        id: 6,
        title: "Combo Familiar 'Salud & Vigor'",
        category: "combos",
        price: 52.00,
        originalPrice: 72.00,
        badge: "Envío Gratis",
        rating: 5.0,
        description: "Contiene: 1 Curcu-Eliel Forte (60 cap) + 1 Cúrcuma Pura 500g + 1 Recetario impreso para Golden Milk y batidos desintoxicantes.",
        image: "https://images.unsplash.com/photo-1546069901-ba9599a7e63c?auto=format&fit=crop&w=600&q=80"
      }
    ];

    // State
    let cart = [];

    // Initialize Page
    document.addEventListener('DOMContentLoaded', () => {
      renderProducts(products);
      updateCartUI();
    });

    function renderProducts(items) {
      const grid = document.getElementById('productGrid');
      grid.innerHTML = '';

      if (items.length === 0) {
        grid.innerHTML = `<div class="col-span-3 text-center py-12 text-stone-500">No se encontraron productos en esta categoría.</div>`;
        return;
      }

      items.forEach(prod => {
        const card = document.createElement('div');
        card.className = "bg-white rounded-3xl overflow-hidden border border-amber-100 hover:border-amber-300 shadow-sm hover:shadow-xl transition-all duration-300 flex flex-col justify-between group";
        
        card.innerHTML = `
          <div>
            <div class="relative overflow-hidden bg-amber-50 h-56">
              <img 
                src="${prod.image}" 
                alt="${prod.title}" 
                class="w-full h-full object-cover group-hover:scale-105 transition-transform duration-500"
                onerror="this.src='https://placehold.co/600x400/d97706/ffffff?text=${encodeURIComponent(prod.title)}'"
              />
              <span class="absolute top-3 left-3 bg-amberGold-600 text-white font-bold text-[11px] uppercase px-3 py-1 rounded-full shadow">
                ${prod.badge}
              </span>
              <div class="absolute bottom-3 right-3 bg-stone-900/80 backdrop-blur-sm text-white px-2.5 py-0.5 rounded-full text-xs font-semibold flex items-center gap-1">
                <i class="fa-solid fa-star text-amber-400 text-[10px]"></i>
                <span>${prod.rating}</span>
              </div>
            </div>

            <div class="p-6">
              <h3 class="font-heading font-bold text-xl text-stone-900 mb-2 group-hover:text-amberGold-700 transition-colors">
                ${prod.title}
              </h3>
              <p class="text-stone-500 text-xs leading-relaxed mb-4">
                ${prod.description}
              </p>
            </div>
          </div>

          <div class="p-6 pt-0 border-t border-amber-50 mt-auto">
            <div class="flex items-baseline gap-2 mb-4">
              <span class="text-2xl font-black text-stone-900">$${prod.price.toFixed(2)}</span>
              ${prod.originalPrice ? `<span class="text-xs text-stone-400 line-through">$${prod.originalPrice.toFixed(2)}</span>` : ''}
              <span class="ml-auto text-[11px] font-semibold text-herbGreen-700 bg-herbGreen-50 px-2 py-0.5 rounded-md">En Stock</span>
            </div>

            <button onclick="quickAddToCart(${prod.id})" class="w-full bg-amberGold-500 hover:bg-amberGold-600 text-white font-bold py-3 px-4 rounded-xl shadow-md hover:shadow-lg transition-all flex items-center justify-center gap-2">
              <i class="fa-solid fa-cart-plus"></i>
              <span>Agregar al Carrito</span>
            </button>
          </div>
        `;
        grid.appendChild(card);
      });
    }

    function filterProducts(category) {
      document.querySelectorAll('.filter-btn').forEach(btn => {
        if (btn.dataset.cat === category) {
          btn.classList.add('bg-stone-900', 'text-white');
          btn.classList.remove('bg-white', 'text-stone-700');
        } else {
          btn.classList.remove('bg-stone-900', 'text-white');
          btn.classList.add('bg-white', 'text-stone-700');
        }
      });

      if (category === 'todos') {
        renderProducts(products);
      } else {
        const filtered = products.filter(p => p.category === category);
        renderProducts(filtered);
      }
    }

    function quickAddToCart(productId) {
      const product = products.find(p => p.id === productId);
      if (!product) return;

      const existing = cart.find(item => item.id === productId);
      if (existing) {
        existing.quantity += 1;
      } else {
        cart.push({
          id: product.id,
          title: product.title,
          price: product.price,
          image: product.image,
          quantity: 1
        });
      }

      updateCartUI();
      showToast(`¡Añadido!`, `${product.title} se sumó a tu carrito.`);
    }

    function updateCartQuantity(productId, change) {
      const itemIndex = cart.findIndex(item => item.id === productId);
      if (itemIndex > -1) {
        cart[itemIndex].quantity += change;
        if (cart[itemIndex].quantity <= 0) {
          cart.splice(itemIndex, 1);
        }
      }
      updateCartUI();
    }

    function removeCartItem(productId) {
      cart = cart.filter(item => item.id !== productId);
      updateCartUI();
    }

    function updateCartUI() {
      const countBadge = document.getElementById('cartCountBadge');
      const list = document.getElementById('cartItemsList');
      const subtotalEl = document.getElementById('cartSubtotal');
      const totalEl = document.getElementById('cartTotal');

      const totalItems = cart.reduce((acc, item) => acc + item.quantity, 0);
      countBadge.textContent = totalItems;

      if (cart.length === 0) {
        list.innerHTML = `
          <div class="text-center py-16 space-y-3">
            <div class="w-16 h-16 bg-amber-100 text-amberGold-600 rounded-full flex items-center justify-center mx-auto text-2xl">
              <i class="fa-solid fa-basket-shopping"></i>
            </div>
            <h4 class="font-bold text-stone-800">Tu carrito está vacío</h4>
            <p class="text-stone-500 text-xs max-w-xs mx-auto">Selecciona tus productos de cúrcuma o Curcu-Eliel para comenzar a mejorar tu salud.</p>
          </div>
        `;
        subtotalEl.textContent = "$0.00";
        totalEl.textContent = "$0.00";
        return;
      }

      let subtotal = 0;
      list.innerHTML = '';

      cart.forEach(item => {
        const itemTotal = item.price * item.quantity;
        subtotal += itemTotal;

        const row = document.createElement('div');
        row.className = "flex items-center gap-4 bg-stone-50 p-3 rounded-2xl border border-stone-200/70";
        row.innerHTML = `
          <img src="${item.image}" alt="${item.title}" class="w-14 h-14 object-cover rounded-xl shrink-0" onerror="this.src='https://placehold.co/100x100/d97706/ffffff?text=Cúrcuma'">
          <div class="flex-1 min-w-0">
            <h4 class="text-xs font-bold text-stone-900 truncate">${item.title}</h4>
            <span class="text-xs font-semibold text-amberGold-700">$${item.price.toFixed(2)} c/u</span>
            <div class="flex items-center gap-2 mt-1.5">
              <button onclick="updateCartQuantity(${item.id}, -1)" class="w-6 h-6 rounded-md bg-white border border-stone-300 text-stone-600 flex items-center justify-center text-xs hover:bg-stone-100">-</button>
              <span class="text-xs font-bold w-4 text-center">${item.quantity}</span>
              <button onclick="updateCartQuantity(${item.id}, 1)" class="w-6 h-6 rounded-md bg-white border border-stone-300 text-stone-600 flex items-center justify-center text-xs hover:bg-stone-100">+</button>
            </div>
          </div>
          <div class="text-right">
            <span class="block text-xs font-bold text-stone-900 mb-2">$${itemTotal.toFixed(2)}</span>
            <button onclick="removeCartItem(${item.id})" class="text-stone-400 hover:text-red-500 text-xs" title="Eliminar"><i class="fa-regular fa-trash-can"></i></button>
          </div>
        `;
        list.appendChild(row);
      });

      subtotalEl.textContent = `$${subtotal.toFixed(2)}`;
      totalEl.textContent = `$${subtotal.toFixed(2)}`;
    }

    function checkoutWhatsApp() {
      if (cart.length === 0) {
        showToast("Carrito Vacío", "Por favor añade al menos un producto.");
        return;
      }

      let message = "🌿 *¡Hola Curcu-Eliel! Deseo realizar este pedido:*\n\n";
      let total = 0;

      cart.forEach((item, index) => {
        const itemTotal = item.price * item.quantity;
        total += itemTotal;
        message += `${index + 1}. ${item.title} (x${item.quantity}) - $${itemTotal.toFixed(2)}\n`;
      });

      message += `\n💰 *Total Estimado:* $${total.toFixed(2)}`;
      message += `\n🚚 *Envío:* Solicito información y coordinación de entrega.`;

      const encoded = encodeURIComponent(message);
      const whatsappUrl = `https://wa.me/?text=${encoded}`;
      window.open(whatsappUrl, '_blank');
    }

    function handleLeadSubmit(event) {
      event.preventDefault();
      const name = document.getElementById('leadName').value;
      const phone = document.getElementById('leadPhone').value;
      const interest = document.getElementById('leadInterest').value;

      const message = `🌿 *Consulta sobre Cúrcuma & Curcu-Eliel*\n\n` +
                      `👤 *Nombre:* ${name}\n` +
                      `📱 *Teléfono:* ${phone}\n` +
                      `✨ *Interés:* ${interest}\n\n` +
                      `_Deseo recibir más detalles y promociones vigentes._`;

      const encoded = encodeURIComponent(message);
      window.open(`https://wa.me/?text=${encoded}`, '_blank');
      showToast("Mensaje Preparado", "Te estamos redirigiendo a WhatsApp...");
      document.getElementById('leadForm').reset();
    }

    function toggleCartModal() {
      const modal = document.getElementById('cartModal');
      modal.classList.toggle('hidden');
    }

    function toggleMobileMenu() {
      const menu = document.getElementById('mobileMenu');
      menu.classList.toggle('hidden');
    }

    function toggleFaq(index) {
      const ans = document.getElementById(`faq-ans-${index}`);
      const icon = document.getElementById(`faq-icon-${index}`);
      
      const isHidden = ans.classList.contains('hidden');
      if (isHidden) {
        ans.classList.remove('hidden');
        icon.classList.add('rotate-180');
      } else {
        ans.classList.add('hidden');
        icon.classList.remove('rotate-180');
      }
    }

    function showToast(title, desc) {
      const toast = document.getElementById('toastNotification');
      document.getElementById('toastTitle').textContent = title;
      document.getElementById('toastDesc').textContent = desc;

      toast.classList.remove('translate-y-24', 'opacity-0', 'pointer-events-none');
      toast.classList.add('translate-y-0', 'opacity-100');

      setTimeout(() => {
        toast.classList.add('translate-y-24', 'opacity-0', 'pointer-events-none');
        toast.classList.remove('translate-y-0', 'opacity-100');
      }, 3200);
    }
  </script>
</body>
</html>
