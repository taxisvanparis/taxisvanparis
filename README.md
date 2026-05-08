<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Taxi Van Paris | Réservation de Prestige</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        .hero-bg {
            background: linear-gradient(rgba(0,0,0,0.6), rgba(0,0,0,0.6)), 
                        url('https://images.unsplash.com/photo-1544620347-c4fd4a3d5957?auto=format&fit=crop&q=80&w=1000');
            background-size: cover;
            background-position: center;
        }
    </style>
</head>
<body class="bg-gray-50 font-sans">

    <!-- Navigation -->
    <nav class="bg-black text-white p-4 sticky top-0 z-50">
        <div class="container mx-auto flex justify-between items-center">
            <div class="text-2xl font-bold tracking-tighter">
                <span class="text-yellow-500">VAN</span> PARIS <i class="fa-solid fa-van-shuttle"></i>
            </div>
            <a href="tel:+33600000000" class="bg-yellow-500 text-black px-4 py-2 rounded-full font-bold text-sm">
                <i class="fa-solid fa-phone"></i> Appeler
            </a>
        </div>
    </nav>

    <!-- Hero Section -->
    <header class="hero-bg h-[60vh] flex items-center justify-center text-center text-white px-4">
        <div>
            <h1 class="text-4xl md:text-6xl font-extrabold mb-4">Votre Van Privé sur Paris</h1>
            <p class="text-xl mb-6 text-gray-200">Spécialiste familles : Sièges bébé et réhausseurs gratuits.</p>
            <a href="#reserve" class="bg-yellow-500 text-black px-8 py-4 rounded-lg font-bold text-lg hover:bg-yellow-400 transition">Réserver maintenant</a>
        </div>
    </header>

    <!-- Calculateur -->
    <section id="reserve" class="container mx-auto px-4 py-12">
        <div class="max-w-2xl mx-auto bg-white rounded-2xl shadow-xl p-8 border border-gray-100">
            <h2 class="text-2xl font-bold mb-6 text-center text-gray-800 italic">Estimez le prix de votre course</h2>
            
            <div class="space-y-4">
                <div>
                    <label class="block text-sm font-medium text-gray-700">Distance estimée (km)</label>
                    <input type="number" id="distance" placeholder="Ex: 25" class="w-full p-3 border border-gray-300 rounded-lg mt-1 focus:ring-2 focus:ring-yellow-500 outline-none">
                </div>

                <div class="grid grid-cols-2 gap-4">
                    <div class="flex items-center p-3 border rounded-lg bg-gray-50">
                        <input type="checkbox" id="babySeat" class="w-5 h-5 text-yellow-500">
                        <label for="babySeat" class="ml-3 text-sm font-medium">Siège Bébé (Gratuit)</label>
                    </div>
                    <div class="flex items-center p-3 border rounded-lg bg-gray-50">
                        <input type="checkbox" id="boosterSeat" class="w-5 h-5 text-yellow-500">
                        <label for="boosterSeat" class="ml-3 text-sm font-medium">Réhausseur (Gratuit)</label>
                    </div>
                </div>

                <div class="bg-black text-white p-6 rounded-xl text-center">
                    <p class="text-gray-400 text-sm uppercase font-bold">Prix Estimé</p>
                    <div class="text-4xl font-bold text-yellow-500"><span id="totalPrice">0</span> €</div>
                </div>

                <button onclick="calculatePrice()" class="w-full bg-gray-200 text-black font-bold py-3 rounded-lg hover:bg-gray-300 transition mb-4">Recalculer</button>
                
                <a href="https://wa.me/33600000000" class="flex items-center justify-center w-full bg-green-500 text-white font-bold py-4 rounded-lg hover:bg-green-600 transition">
                    <i class="fa-brands fa-whatsapp mr-2 text-xl"></i> Confirmer via WhatsApp
                </a>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 text-gray-400 py-8 text-center text-sm">
        <p>&copy; 2026 Taxis Van Paris. Service disponible 24h/7j.</p>
        <p>Aéroports CDG / Orly / Gares Parisiennes</p>
    </footer>

    <!-- Logique de Calcul -->
    <script>
        function calculatePrice() {
            const distance = document.getElementById('distance').value;
            const baseFare = 15; // Prise en charge
            const pricePerKm = 2.5; // Tarif Van par km
            
            if(distance > 0) {
                let total = baseFare + (distance * pricePerKm);
                document.getElementById('totalPrice').innerText = total.toFixed(2);
            } else {
                document.getElementById('totalPrice').innerText = "0";
            }
        }
        
        // Calcul automatique lors de la saisie
        document.getElementById('distance').addEventListener('input', calculatePrice);
    </script>
</body>
</html>

