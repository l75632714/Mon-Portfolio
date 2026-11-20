<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mon Portfolio Atelier Mixed Media</title>
    <style>
        :root {
            --bg-color: #f4f5f7;
            --card-bg: #ffffff;
            --text-color: #2c3e50;
            --border-color: #dcdde1;
            --accent-color: #0066cc;
            --desc-bg: #f8f9fa;
            --desc-color: #495057;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Helvetica, Arial, sans-serif;
            max-width: 900px;
            margin: 0 auto;
            padding: 20px;
            background-color: var(--bg-color);
            color: var(--text-color);
            line-height: 1.6;
        }

        /* Navigation */
        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            background: var(--card-bg);
            padding: 15px 30px;
            border-radius: 12px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.04);
            margin-bottom: 30px;
        }

        .logo {
            font-weight: bold;
            font-size: 1.2rem;
            color: var(--accent-color);
        }

        .nav-links {
            list-style: none;
            display: flex;
            gap: 20px;
            margin: 0;
            padding: 0;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--text-color);
            font-weight: 500;
        }

        .nav-links a:hover {
            color: var(--accent-color);
        }

        /* En-tête */
        header {
            text-align: center;
            padding: 50px 20px;
            background: var(--card-bg);
            border-radius: 12px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.04);
            margin-bottom: 30px;
        }

        header h1 {
            margin: 0 0 10px 0;
            font-size: 2.2rem;
        }

        header p {
            margin: 0;
            color: #718096;
            font-size: 1.1rem;
        }

        /* Sections générales */
        .section-container {
            background: var(--card-bg);
            padding: 30px;
            border-radius: 12px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.04);
            margin-bottom: 30px;
        }

        h2 {
            margin-top: 0;
            font-size: 1.4rem;
            margin-bottom: 20px;
            color: var(--text-color);
            border-bottom: 2px solid var(--bg-color);
            padding-bottom: 10px;
        }

        /* Grille de projets du portfolio */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
        }

        .project-card {
            background: var(--bg-color);
            padding: 20px;
            border-radius: 8px;
            border: 1px solid var(--border-color);
        }

        .project-card h3 {
            margin-top: 0;
            font-size: 1.1rem;
        }

        .project-card p {
            font-size: 0.9rem;
            color: #666;
            margin-bottom: 0;
        }

        /* Formulaire & Options juridiques */
        label {
            display: block;
            margin-bottom: 8px;
            font-weight: 600;
            font-size: 0.95rem;
        }

        select {
            width: 100%;
            padding: 12px;
            border: 1px solid var(--border-color);
            border-radius: 6px;
            font-size: 0.95rem;
            background-color: #fff;
            color: var(--text-color);
            margin-bottom: 20px;
            cursor: pointer;
            transition: border-color 0.2s;
        }

        select:focus {
            outline: none;
            border-color: var(--accent-color);
            box-shadow: 0 0 0 3px rgba(0, 102, 204, 0.1);
        }

        .description-label {
            font-size: 0.85rem;
            text-transform: uppercase;
            letter-spacing: 0.5px;
            color: #718096;
            margin-bottom: 6px;
            font-weight: 700;
        }

        #legal-description {
            font-size: 0.95rem;
            color: var(--desc-color);
            background: var(--desc-bg);
            padding: 14px 18px;
            border-radius: 6px;
            min-height: 40px;
            margin: 0;
            border-left: 4px solid var(--accent-color);
        }

        /* Pied de page */
        footer {
            text-align: center;
            font-size: 0.9rem;
            color: #718096;
            padding: 20px 0;
            margin-top: 40px;
            border-top: 1px solid var(--border-color);
        }
    </style>
</head>
<body>

    <!-- Barre de navigation -->
    <nav>
        <div class="logo">Mon Portfolio</div>
        <ul class="nav-links">
            <li><a href="#accueil">Accueil</a></li>
            <li><a href="#projets">Projets</a></li>
            <li><a href="#juridique">Paramètres juridiques</a></li>
        </ul>
    </nav>

    <!-- En-tête / Accueil -->
    <header id="accueil">
        <h1>Bienvenue sur mon Portfolio</h1>
        <p>Espace de présentation de mes créations artistiques et multimédias</p>
    </header>

    <!-- Section Projets -->
    <div id="projets" class="section-container">
        <h2>Mes Projets Récents</h2>
        <div class="projects-grid">
            <div class="project-card">
                <h3>Projet 01</h3>
                <p>Création graphique originale et illustrations numériques.</p>
            </div>
            <div class="project-card">
                <h3>Projet 02</h3>
                <p>Photographies artistiques et retouches de paysages.</p>
            </div>
            <div class="project-card">
                <h3>Projet 03</h3>
                <p>Design d'interface web et intégration front-end.</p>
            </div>
        </div>
    </div>

    <!-- Section de Configuration Juridique (19 options + année dynamique) -->
    <div id="juridique" class="section-container">
        <h2>Configuration des options juridiques</h2>
        
        <label for="legal-options-select">Sélectionnez le régime de protection :</label>
        <select id="legal-options-select" name="legal_option">
            <option value="aucun-copyright">Aucun copyright (Libre de droits ou contenu tiers / lien posté)</option>
            <option value="tous-droits-reserves">© Tous droits réservés</option>
            <!-- L'option dynamique avec l'année en cours sera injectée ici par JavaScript -->
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

        <div class="description-label">Description de l'option :</div>
        <p id="legal-description">Contenu totalement libre sans restriction, ou contenu soumis au droit d'auteur d'un tiers / provenant d'un lien externe.</p>
    </div>

    <!-- Pied de page global du site avec année automatique -->
    <footer>
        <p>&copy; <span id="current-year"></span> Mon Portfolio - Tous droits réservés</p>
    </footer>

    <!-- Script JavaScript global pour le site -->
    <script>
        // Récupération automatique de l'année en cours
        const currentYear = new Date().getFullYear();

        // 1. Injection dynamique de l'option avec l'année en cours dans le menu déroulant (en 3ème position)
        const selectElement = document.getElementById('legal-options-select');
        const dynamicOption = document.createElement('option');
        dynamicOption.value = "tous-droits-reserves-annee";
        dynamicOption.textContent = `© ${currentYear} Tous droits réservés / All rights reserved`;
        selectElement.insertBefore(dynamicOption, selectElement.children[2]);

        // 2. Dictionnaire complet des descriptions associées aux 19 options
        const legalDescriptions = {
            "aucun-copyright": "Contenu totalement libre sans restriction, ou contenu soumis au droit d'auteur d'un tiers / provenant d'un lien externe.",
            "tous-droits-reserves": "Le choix par défaut à privilégier pour ton portfolio artistique.",
            "tous-droits-reserves-annee": `Version bilingue actualisée avec l'année en cours (${currentYear}), idéale pour un public suisse et européen.`,
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

        const descriptionElement = document.getElementById('legal-description');

        // 3. Gestionnaire d'événement pour changer la description dynamiquement au changement de sélection
        selectElement.addEventListener('change', (event) => {
            const selectedKey = event.target.value;
            if (descriptionElement) {
                descriptionElement.textContent = legalDescriptions[selectedKey] || '';
            }
        });

        // 4. Mise à jour automatique de l'année dans le pied de page du portfolio
        document.getElementById('current-year').textContent = currentYear;
    </script>

</body>
</html>
