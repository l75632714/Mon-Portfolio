<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mon Portfolio - Paramètres Juridiques</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            max-width: 600px;
            margin: 40px auto;
            padding: 20px;
            background-color: #f9f9f9;
            color: #333;
        }
        .form-group {
            background: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 2px 4px rgba(0,0,0,0.1);
        }
        label {
            display: block;
            margin-bottom: 8px;
            font-weight: bold;
        }
        select {
            width: 100%;
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 4px;
            font-size: 14px;
            margin-bottom: 15px;
        }
        #legal-description {
            font-size: 13px;
            color: #666;
            font-style: italic;
            background: #f1f1f1;
            padding: 10px;
            border-radius: 4px;
            min-height: 40px;
        }
    </style>
</head>
<body>

    <div class="form-group">
        <h2>Configuration des options juridiques</h2>
        
        <label for="legal-options-select">Sélectionnez le régime de protection :</label>
        <select id="legal-options-select" name="legal_option">
            <option value="aucun-copyright">Aucun copyright (Libre de droits ou contenu tiers / lien posté)</option>
            <option value="tous-droits-reserves">© Tous droits réservés</option>
            <option value="tous-droits-reserves-2026">© 2026 Tous droits réservés / All rights reserved</option>
            <option value="all-rights-reserved">© All rights reserved</option>
            <option value="copyright-all-rights-reserved">Copyright © All rights reserved</option>
            <option value="propriete-intellectuelle-lda">Propriété intellectuelle — Droit d'auteur global (LDA / Berne)</option>
            <option value="droits-moraux">Droits moraux (Paternité, Divulgation & Intégrité)</option>
            <option value="droits-patrimoniaux">Droits patrimoniaux (Exploitation économique & Diffusion)</option>
            <option value="concurrence-deloyale">Protection contre la concurrence déloyale (Lutte contre le parasitisme)</option>
            <option value="propriete-industrielle-suisse">Propriété industrielle — Brevets, Marques & Designs (Suisse - IPI)</option>
            <option value="propriete-industrielle-europe">Propriété industrielle — Marques & Designs unitaires (Europe - EUIPO)</option>
            <option value="propriete-industrielle-international">Propriété industrielle — Systèmes internationaux (Madrid, PCT, La Haye)</option>
            <option value="domaine-public-cc0">Domaine public / CC0 (International)</option>
            <option value="cc-by">CC BY (Attribution)</option>
            <option value="cc-by-sa">CC BY-SA (Attribution + Partage dans les mêmes conditions)</option>
            <option value="cc-by-nd">CC BY-ND (Attribution + Pas de modification)</option>
            <option value="cc-by-nc">CC BY-NC (Attribution + Non-commercial)</option>
            <option value="cc-by-nc-sa">CC BY-NC-SA (Attribution + Non-commercial + Partage dans les mêmes conditions)</option>
            <option value="cc-by-nc-nd">CC BY-NC-ND (Attribution + Non-commercial + Pas de modification)</option>
        </select>

        <label>Description de l'option :</label>
        <p id="legal-description">Contenu totalement libre sans restriction, ou contenu soumis au droit d'auteur d'un tiers / provenant d'un lien externe.</p>
    </div>

    <script>
        const descriptions = {
            "aucun-copyright": "Contenu totalement libre sans restriction, ou contenu soumis au droit d'auteur d'un tiers / provenant d'un lien externe.",
            "tous-droits-reserves": "Le choix par défaut à privilégier pour ton portfolio artistique.",
            "tous-droits-reserves-2026": "Version bilingue actualisée avec l'année en cours, idéale pour un public suisse et européen.",
            "all-rights-reserved": "Standard international en anglais couramment utilisé pour les sites web à portée mondiale.",
            "copyright-all-rights-reserved": "Formule universelle complète combinant le terme 'Copyright' et le symbole ©.",
            "propriete-intellectuelle-lda": "Protection automatique de l'œuvre dès sa création (régie en Suisse par la LDA et mondialement par la Convention de Berne).",
            "droits-moraux": "Garantit le droit de revendiquer son nom, de décider de la publication et de protéger l'œuvre contre toute modification dénaturée.",
            "droits-patrimoniaux": "Confère le droit exclusif d'autoriser ou d'interdire la reproduction, la vente et la diffusion de l'œuvre.",
            "concurrence-deloyale": "Recours légal (en Suisse via la LCD) contre le vol de réputation, le plagiat parasitaire ou l'imitation trompeuse.",
            "propriete-industrielle-suisse": "Protection officielle des inventions techniques, des noms/logos et de l'esthétique des produits auprès de l'IPI.",
            "propriete-industrielle-europe": "Titres de protection valables de manière uniforme dans toute l'Union européenne via l'EUIPO.",
            "propriete-industrielle-international": "Procédures centralisées permettant d'étendre la protection des marques, brevets et designs à l'international.",
            "domaine-public-cc0": "Abandon volontaire de tous les droits d'auteur, permettant à quiconque de réutiliser l'œuvre librement.",
            "cc-by": "Permet toute réutilisation, modification et exploitation commerciale, à condition de citer le nom de l'auteur.",
            "cc-by-sa": "Permet l'usage commercial et les modifications, à condition de repartager les créations dérivées sous la même licence.",
            "cc-by-nd": "Permet la diffusion de l'œuvre originale (même commerciale), mais interdit d'y apporter des modifications ou des remixes.",
            "cc-by-nc": "Permet de modifier et de remixer l'œuvre, mais exclusivement pour des utilisations non commerciales.",
            "cc-by-nc-sa": "Permet le remix et l'usage non commercial, avec obligation de repartager sous la même licence.",
            "cc-by-nc-nd": "La plus restrictive des licences CC ; autorise uniquement le téléchargement et le partage à l'identique, sans modification et sans usage commercial."
        };

        const selectElement = document.getElementById('legal-options-select');
        const descriptionElement = document.getElementById('legal-description');

        selectElement.addEventListener('change', (event) => {
            const selectedKey = event.target.value;
            if (descriptionElement) {
                descriptionElement.textContent = descriptions[selectedKey] || '';
            }
        });
    </script>

</body>
</html>
