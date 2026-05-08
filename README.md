<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <!-- SEO : Mots-clés pour le référencement 95, 92, 78 et Gares/Aéroports -->
    <title>Taxi Van Paris | Réservation 95, 92, 78 | Aéroports & Gares</title>
    <meta name="description" content="Réservez votre Van taxi dans le 95, 92, 78. Transferts Aéroports (CDG, Orly) et Gares Parisiennes. Sièges bébé et réhausseurs inclus. Van 7-8 places.">
    <meta name="keywords" content="Van Paris, Taxi 95, Taxi 92, Taxi 78, Réservation Van Aéroport, Van Gare du Nord, Van Gare de Lyon, Siège bébé taxi, Van 8 places Val d'Oise, Van Yvelines, Van Hauts-de-Seine">
    
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        .hero-bg {
            background: linear-gradient(rgba(0,0,0,0.7), rgba(0,0,0,0.7)), 
                        url('https://images.unsplash.com/photo-1559297434-2d8a1e929ff7?auto=format&fit=crop&q=80&w=1000');
            background-size: cover;
            background-position: center;
        }
    </style>
</head>
<body class="bg-gray-50 font-sans text-gray-900">

    <!-- Header / Navigation -->
    <nav class="bg-black text-white p-4 sticky top-0 z-50 border-b-2 border-yellow-500">
        <div class="container mx-auto flex justify-between items-center">
            <div class="leading-tight">
                <span class="text-2xl font-black text-yellow-500 italic uppercase">Van Paris Prestige</span>
                <p class="text-xs text-gray-400">Services 95 • 92 • 78 • Aéroports</p>
            </div>
            <a href="tel:+33600000000" class="bg-yellow-500 text-black px-5 py-2 rounded-md font-bold hover:bg-yellow-400">
                <i class="fa-solid fa-phone"></i> Appeler
            </a>
        </div>
    </nav>

    <!-- Hero -->
    <header class="hero-bg py-20 text-center text-white px-4">
        <h1 class="text-3xl md:text-5xl font-extrabold mb-4 uppercase">Réservation Van Île-de-France</h1>
        <p class="text-lg md:text-xl mb-6 text-yellow-400 font-semibold">Spécialiste Famille : Sièges Bébé & Réhausseurs Gratuits</p>
        <div class="flex flex-wrap justify-center gap-2 text-sm">
            <span class="bg-white/20 px-3 py-1 rounded-full border border-white/30">Val-d'Oise (95)</span>
            <span class="bg-white/20 px-3 py-1 rounded-full border border-white/30">Hauts-de-Seine (92)</span>
            <span class="bg-white/20 px-3 py-1 rounded-full border border-white/30">Yvelines (78)</span>
        </div>
    </header>

    <!-- Calculateur de Prix -->
    <section id="devis" class="container mx-auto px-4 -mt-10 mb-12">
        <div class="max-w-xl mx-auto bg-white rounded-xl shadow-2xl p-6 border-t-4 border-yellow-500">
            <h2 class="text-xl font-bold mb-6 text-center uppercase tracking-wide">Calculateur de prix immédiat</h2>
            
            <div class="space-y-5">
                <div>
                    <label class="block text-sm font-bold text-gray-600 mb-1">Nombre de kilomètres estimés :</label>
                    <input type="number" id="distance" placeholder="Entrez la distance (ex: 30)" 
                           class="w-full p-4 border-2 border-gray-100 rounded-xl bg-gray-50 focus:border-yellow-500 outline-none text-lg">
                </div>

                <div class="grid grid-cols-1 md:grid-cols-2 gap-3">
                    <div class="flex items-center p-3 border rounded-xl bg-yellow-50 border-yellow-100">
                        <i class="fa-solid fa-baby text-yellow-600 mr-3 text-xl"></i>
                        <span class="text-sm font-bold">Siège Bébé (Offert)</span>
                    </div>
                    <div class="flex items-center p-3 border rounded-xl bg-yellow-50 border-yellow-100">
                        <i class="fa-solid fa-child text-yellow-600 mr-3 text-xl"></i>
                        <span class="text-sm font-bold">Réhausseur (Offert)</span>
                    </div>
                </div>

                <div class="bg-black text-white p-5 rounded-xl text-center shadow-inner">
                    <p class="text-yellow-500 text-xs font-bold uppercase mb-1">Estimation du tarif TTC</p>
                    <div class="text-5xl font-black"><span id="totalPrice">15.00</span> €</div>
                    <p class="text-[10px] text-gray-400 mt-2">*Base 15€ + 2.80€/km (Tarif indicatif)</p>
                </div>

                <a href="https://wa.me/33600000000?text=Bonjour, je souhaite réserver un van pour une course de..." 
                   class="flex items-center justify-center w-full bg-green-600 text-white font-black py-4 rounded-xl text-lg shadow-lg hover:bg-green-700 transition">
                    <i class="fa-brands fa-whatsapp mr-3 text-2xl"></i> RÉSERVER VIA WHATSAPP
                </a>
            </div>
        </div>
    </section>

    <!-- Services Section -->
    <section class="container mx-auto px-4 py-8 bg-white rounded-3xl mb-12">
        <h3 class="text-2xl font-black text-center mb-10 uppercase">Nos Trajets Fréquents</h3>
        <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
            <div class="p-6 border rounded-2xl text-center">
                <i class="fa-solid fa-plane-departure text-3xl text-yellow-500 mb-4"></i>
                <h4 class="font-bold mb-2">Aéroports</h4>
                <p class="text-sm text-gray-600">Transferts vers Roissy CDG, Orly et Beauvais depuis tout le 95, 92 et 78.</p>
            </div>
            <div class="p-6 border rounded-2xl text-center">
                <i class="fa-solid fa-train text-3xl text-yellow-500 mb-4"></i>
                <h4 class="font-bold mb-2">Gares Parisiennes</h4>
                <p class="text-sm text-gray-600">Gare du Nord, Gare de Lyon, Montparnasse et Gare de l'Est en Van 8 places.</p>
            </div>
            <div class="p-6 border rounded-2xl text-center">
                <i class="fa-solid fa-users text-3xl text-yellow-500 mb-4"></i>
                <h4 class="font-bold mb-2">Famille</h4>
                <p class="text-sm text-gray-600">Équipements complets bébé et enfants disponibles sur simple demande.</p>
            </div>
        </div>
    </section>

    <footer class="bg-black text-white py-10 text-center">
        <p class="font-bold uppercase tracking-widest text-yellow-500">Van Paris Prestige</p>
        <p class="text-xs text-gray-500 mt-2">Zone de couverture : Val d'Oise, Hauts-de-Seine, Yvelines, Paris.</p>
    </footer>

    <script>
        const distanceInput = document.getElementById('distance');
        const priceDisplay = document.getElementById('totalPrice');

        function calculate() {
            const dist = parseFloat(distanceInput.value);
            const base = 15; // Ton prix d'approche
            const rate = 2.80; // Ton prix au km
            
            if (!isNaN(dist) && dist > 0) {
                const total = base + (dist * rate);
                priceDisplay.innerText = total.toFixed(2);
            } else {
                priceDisplay.innerText = "15.00";
            }
        }

        distanceInput.addEventListener('input', calculate);
    </script>
</body>
</html>

