<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Taxi Van Paris - Réservation Officielle</title>
    <style>
        :root { --gold: #c9a24a; --dark: #0b0b0b; --white: #f4f4f4; --grey: #1a1a1a; }
        body { font-family: 'Segoe UI', sans-serif; background-color: var(--dark); color: var(--white); margin: 0; padding: 15px; }
        .container { background: var(--grey); padding: 20px; border-radius: 15px; border: 1px solid var(--gold); max-width: 450px; margin: auto; text-align: center; }
        h1 { color: var(--gold); text-transform: uppercase; margin-bottom: 5px; font-size: 1.5rem; }
        .subtitle { margin-bottom: 20px; font-size: 0.9rem; opacity: 0.8; }
        .input-group { text-align: left; margin-bottom: 15px; }
        label { display: block; margin-bottom: 5px; color: var(--gold); font-size: 0.9rem; font-weight: bold; }
        input { width: 100%; padding: 12px; border-radius: 5px; border: 1px solid #444; background: #333; color: white; box-sizing: border-box; font-size: 1rem; }
        .result-box { background: var(--gold); color: var(--dark); padding: 15px; border-radius: 10px; margin: 20px 0; display: none; border-left: 5px solid #000; }
        .price { font-size: 2.5rem; font-weight: bold; display: block; }
        .btn { display: block; width: 100%; padding: 15px; border-radius: 5px; font-weight: bold; text-decoration: none; border: none; cursor: pointer; font-size: 1.1rem; margin-top: 10px; }
        .btn-wa { background: var(--gold); color: var(--dark); }
        .btn-call { background: transparent; border: 1px solid var(--gold); color: var(--gold); }
    </style>
</head>
<body>

<div class="container">
    <h1>Taxi Van Paris</h1>
    <p class="subtitle">Transport de Prestige - Van 1-8 Passagers</p>

    <div class="input-group">
        <label>📍 Lieu de prise en charge</label>
        <input type="text" id="dep" placeholder="Ex: Gare du Nord, Paris...">
    </div>

    <div class="input-group">
        <label>🏁 Destination</label>
        <input type="text" id="arr" placeholder="Ex: Roissy CDG, Orly...">
    </div>

    <div class="input-group">
        <label>📱 Votre numéro de téléphone</label>
        <input type="tel" id="tel_client" placeholder="06 00 00 00 00">
    </div>

    <button class="btn btn-wa" onclick="calculer()">Calculer mon tarif</button>

    <div id="resultat" class="result-box">
        <span id="type-trajet">Tarif Estimé</span>
        <span class="price" id="prix-final">0 €</span>
        <small>Service Van Premium</small>
    </div>

    <button id="btn-reserver" class="btn btn-wa" style="display:none;" onclick="envoyerWhatsApp()">✅ Confirmer & Envoyer à Taxi Van</button>
    <a href="tel:+33649553640" class="btn btn-call">📞 Appeler le 06 49 55 36 40</a>
</div>

<script>
function calculer() {
    const dep = document.getElementById('dep').value.toLowerCase();
    const arr = document.getElementById('arr').value.toLowerCase();
    const tel = document.getElementById('tel_client').value;
    const resBox = document.getElementById('resultat');
    const prixSpan = document.getElementById('prix-final');
    const typeTrajet = document.getElementById('type-trajet');
    const btnRes = document.getElementById('btn-reserver');

    if (dep.length > 2 && arr.length > 2 && tel.length > 5) {
        let prix = 0;
        let label = "Estimation du trajet";

        // LOGIQUE FORFAITS AÉROPORTS
        if (arr.includes("roissy") || arr.includes("cdg") || dep.includes("roissy") || dep.includes("cdg")) {
            prix = 90;
            label = "Forfait Paris ↔ Roissy CDG";
        } 
        else if (arr.includes("orly") || dep.includes("orly")) {
            prix = 80;
            label = "Forfait Paris ↔ Orly";
        }
        else {
            // Simulation : 15€ base + 2.90€/km (base 15km par défaut)
            prix = 15 + (15 * 2.90);
            label = "Tarif Estimé (Base + Km)";
        }

        prixSpan.innerText = Math.round(prix) + " €";
        typeTrajet.innerText = label;
        resBox.style.display = "block";
        btnRes.style.display = "block";
    } else {
        alert("Veuillez remplir les adresses et votre numéro de téléphone.");
    }
}

function envoyerWhatsApp() {
    const dep = document.getElementById('dep').value;
    const arr = document.getElementById('arr').value;
    const tel = document.getElementById('tel_client').value;
    const prix = document.getElementById('prix-final').innerText;
    
    // Construction du message détaillé
    const texte = `NOUVELLE RÉSERVATION TAXI VAN\n\n` +
                  `📍 DÉPART : ${dep}\n` +
                  `🏁 ARRIVÉE : ${arr}\n` +
                  `💰 MONTANT : ${prix}\n` +
                  `📱 CLIENT : ${tel}\n\n` +
                  `Merci de me confirmer la prise en charge.`;
                  
    window.location.href = "https://wa.me/33649553640?text=" + encodeURIComponent(texte);
}
</script>

</body>
</html>


