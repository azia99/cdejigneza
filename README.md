<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CDEJ IGNEZA TG0682 - Centre de Développement des Enfants et Jeunes</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #333;
            background: #f5f5f5;
            overflow-x: hidden;
            width: 100%;
            margin: 0 auto;
        }

        header {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 2rem 1rem;
            text-align: center;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }

        h1 {
            font-size: clamp(1.5rem, 5vw, 2.5rem);
            margin-bottom: 0.5rem;
        }

        header p {
            font-size: clamp(0.9rem, 3vw, 1.1rem);
        }

        nav {
            background: #2c3e50;
            padding: 0.5rem;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 2px 5px rgba(0,0,0,0.2);
        }

        nav ul {
            list-style: none;
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 0.5rem;
            padding: 0.5rem;
        }

        nav button {
            background: none;
            border: none;
            color: white;
            font-size: clamp(0.85rem, 2.5vw, 1rem);
            cursor: pointer;
            padding: 0.6rem 1rem;
            transition: all 0.3s;
            border-radius: 5px;
            white-space: nowrap;
        }

        nav button:hover {
            background: #34495e;
        }

        nav button.active {
            background: #667eea;
        }

        .container {
            max-width: 1200px;
            margin: 1rem auto;
            padding: 0 1rem;
            width: 100%;
            overflow-x: hidden;
        }

        .section {
            display: none;
            animation: fadeIn 0.5s;
        }

        .section.active {
            display: block;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .card {
            background: white;
            padding: 1.5rem;
            margin: 1rem 0;
            border-radius: 10px;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
        }

        .team-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 1rem;
            margin-top: 1.5rem;
        }

        .member-card {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 1.5rem;
            border-radius: 10px;
            text-align: center;
            cursor: pointer;
            transition: transform 0.3s;
        }

        .member-card:hover {
            transform: scale(1.05);
        }

        .member-card h3 {
            margin-bottom: 0.5rem;
            font-size: clamp(1rem, 3vw, 1.2rem);
        }

        .back-btn {
            background: #667eea;
            color: white;
            border: none;
            padding: 0.7rem 1.5rem;
            border-radius: 5px;
            cursor: pointer;
            margin-bottom: 1rem;
            font-size: 1rem;
            transition: background 0.3s;
        }

        .back-btn:hover {
            background: #5568d3;
        }

        .participant-list {
            background: #f8f9fa;
            padding: 1rem;
            border-radius: 8px;
            margin-top: 1rem;
        }

        .participant-item {
            padding: 0.8rem;
            background: white;
            margin: 0.5rem 0;
            border-radius: 5px;
            border-left: 4px solid #667eea;
            font-size: clamp(0.85rem, 2.5vw, 1rem);
        }

        .event-card {
            background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
            color: white;
            padding: 1.5rem;
            border-radius: 10px;
            margin: 1rem 0;
        }

        .event-card h3 {
            font-size: clamp(1.1rem, 3vw, 1.3rem);
        }

        .vision-box {
            background: linear-gradient(135deg, #4facfe 0%, #00f2fe 100%);
            color: white;
            padding: 2rem;
            border-radius: 15px;
            font-size: clamp(1rem, 2.5vw, 1.2rem);
            text-align: center;
            line-height: 1.8;
        }

        h2 {
            color: #667eea;
            margin-bottom: 1.5rem;
            font-size: clamp(1.5rem, 4vw, 2rem);
            text-align: center;
        }

        h3 {
            font-size: clamp(1rem, 3vw, 1.2rem);
        }

        @media (max-width: 768px) {
            .container {
                padding: 0 0.5rem;
            }
            
            nav ul {
                gap: 0.3rem;
            }
            
            nav button {
                padding: 0.5rem 0.7rem;
                font-size: 0.85rem;
            }
            
            .team-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <header>
        <h1>CDEJ IGNEZA TG0682</h1>
        <p>Centre de Développement des Enfants et des Jeunes</p>
    </header>

    <nav>
        <ul>
            <li><button class="nav-btn active" data-section="accueil">Accueil</button></li>
            <li><button class="nav-btn" data-section="equipe">Équipe</button></li>
            <li><button class="nav-btn" data-section="classes">Classes</button></li>
            <li><button class="nav-btn" data-section="participants">Participants</button></li>
            <li><button class="nav-btn" data-section="evenements">Événements</button></li>
        </ul>
    </nav>

    <div class="container">
        <!-- Section Accueil -->
        <div id="accueil" class="section active">
            <h2>Bienvenue au CDEJ IGNEZA TG0682</h2>
            <div class="vision-box">
                <h3 style="margin-bottom: 1rem;">Notre Vision</h3>
                <p>Contribuer au développement intégral des enfants et des jeunes en leur offrant un environnement sûr, stimulant et enrichissant. Nous visons à former des citoyens responsables, épanouis et engagés dans la construction d'un avenir meilleur pour leur communauté.</p>
            </div>
        </div>

        <!-- Section Équipe -->
        <div id="equipe" class="section">
            <h2>Équipe Dirigeante</h2>
            <div class="team-grid">
                <div class="member-card" onclick="showCPC()">
                    <h3>👥 CPC</h3>
                    <p>Comité de Protection</p>
                </div>
                <div class="member-card" onclick="showAnimateurs()">
                    <h3>🎯 Animateurs</h3>
                    <p>Équipe d'Animation</p>
                </div>
                <div class="member-card" onclick="showVolontaires()">
                    <h3>🤝 Volontaires</h3>
                    <p>Équipe de Volontaires</p>
                </div>
            </div>
        </div>

        <!-- Section CPC -->
        <div id="cpc" class="section">
            <button class="back-btn" onclick="showSection('equipe')">← Retour</button>
            <h2>Comité de Protection (CPC)</h2>
            <div class="team-grid">
                <div class="member-card" onclick="showMemberDetail('president-cpc')">
                    <h3>🏆 Président</h3>
                    <p>Voir les détails</p>
                </div>
                <div class="member-card" onclick="showMemberDetail('secretaire-cpc')">
                    <h3>📝 Secrétaire</h3>
                    <p>Voir les détails</p>
                </div>
                <div class="member-card" onclick="showMemberDetail('tresorier-cpc')">
                    <h3>💰 Trésorier</h3>
                    <p>Voir les détails</p>
                </div>
            </div>
        </div>

        <!-- Détails Membres CPC -->
        <div id="president-cpc" class="section">
            <button class="back-btn" onclick="showSection('cpc')">← Retour</button>
            <div class="card">
                <h2>Président du CPC</h2>
                <p style="font-size: 1.3rem; color: #667eea; margin-top: 1rem;"><strong>ALEMOU Awoutmare</strong></p>
                <div style="margin-top: 2rem; padding: 1.5rem; background: #f8f9fa; border-radius: 8px;">
                    <h3 style="color: #333; margin-bottom: 1rem;">📞 Contact</h3>
                    <p style="color: #666;"><strong>Téléphone:</strong> [Numéro à ajouter]</p>
                    <p style="color: #666;"><strong>Email:</strong> [Email à ajouter]</p>
                </div>
            </div>
        </div>

        <div id="secretaire-cpc" class="section">
            <button class="back-btn" onclick="showSection('cpc')">← Retour</button>
            <div class="card">
                <h2>Secrétaire du CPC</h2>
                <p style="font-size: 1.3rem; color: #667eea; margin-top: 1rem;"><strong>DJIDJONOU Yawavi Boèdi</strong></p>
                <div style="margin-top: 2rem; padding: 1.5rem; background: #f8f9fa; border-radius: 8px;">
                    <h3 style="color: #333; margin-bottom: 1rem;">📞 Contact</h3>
                    <p style="color: #666;"><strong>Téléphone:</strong> [Numéro à ajouter]</p>
                    <p style="color: #666;"><strong>Email:</strong> [Email à ajouter]</p>
                </div>
            </div>
        </div>

        <div id="tresorier-cpc" class="section">
            <button class="back-btn" onclick="showSection('cpc')">← Retour</button>
            <div class="card">
                <h2>Trésorier du CPC</h2>
                <p style="font-size: 1.3rem; color: #667eea; margin-top: 1rem;"><strong>DOGO David</strong></p>
                <div style="margin-top: 2rem; padding: 1.5rem; background: #f8f9fa; border-radius: 8px;">
                    <h3 style="color: #333; margin-bottom: 1rem;">📞 Contact</h3>
                    <p style="color: #666;"><strong>Téléphone:</strong> [Numéro à ajouter]</p>
                    <p style="color: #666;"><strong>Email:</strong> [Email à ajouter]</p>
                </div>
            </div>
        </div>

        <!-- Section Animateurs -->
        <div id="animateurs" class="section">
            <button class="back-btn" onclick="showSection('equipe')">← Retour</button>
            <h2>Équipe d'Animation</h2>
            <div class="team-grid">
                <div class="member-card" onclick="showMemberDetail('coordinateur')">
                    <h3>🎯 Coordinateur</h3>
                    <p>Voir les détails</p>
                </div>
                <div class="member-card" onclick="showMemberDetail('assistance-sociale')">
                    <h3>🤝 Assistance Sociale</h3>
                    <p>Voir les détails</p>
                </div>
                <div class="member-card" onclick="showMemberDetail('comptable')">
                    <h3>💼 Comptable</h3>
                    <p>Voir les détails</p>
                </div>
            </div>
        </div>

        <!-- Section Volontaires -->
        <div id="volontaires" class="section">
            <button class="back-btn" onclick="showSection('equipe')">← Retour</button>
            <h2>Équipe de Volontaires</h2>
            <div class="participant-list">
                <div class="participant-item"><strong>1.</strong> [Nom du volontaire 1]</div>
                <div class="participant-item"><strong>2.</strong> [Nom du volontaire 2]</div>
                <div class="participant-item"><strong>3.</strong> [Nom du volontaire 3]</div>
                <div class="participant-item"><strong>4.</strong> [Nom du volontaire 4]</div>
                <div class="participant-item"><strong>5.</strong> [Nom du volontaire 5]</div>
                <p style="margin-top: 1rem; color: #666; font-style: italic;">
                    Note : Ajoutez les noms des volontaires
                </p>
            </div>
        </div>

        <!-- Détails Animateurs -->
        <div id="coordinateur" class="section">
            <button class="back-btn" onclick="showSection('animateurs')">← Retour</button>
            <div class="card">
                <h2>Coordinateur</h2>
                <p style="font-size: 1.3rem; color: #667eea; margin-top: 1rem;"><strong>AZIABLE Kodjovi Charles</strong></p>
                <div style="margin-top: 2rem; padding: 1.5rem; background: #f8f9fa; border-radius: 8px;">
                    <h3 style="color: #333; margin-bottom: 1rem;">📞 Contact</h3>
                    <p style="color: #666;"><strong>Téléphone:</strong> [Numéro à ajouter]</p>
                    <p style="color: #666;"><strong>Email:</strong> [Email à ajouter]</p>
                </div>
            </div>
        </div>

        <div id="assistance-sociale" class="section">
            <button class="back-btn" onclick="showSection('animateurs')">← Retour</button>
            <div class="card">
                <h2>Assistance Sociale</h2>
                <p style="font-size: 1.3rem; color: #667eea; margin-top: 1rem;"><strong>TCHORO Tchapo</strong></p>
                <div style="margin-top: 2rem; padding: 1.5rem; background: #f8f9fa; border-radius: 8px;">
                    <h3 style="color: #333; margin-bottom: 1rem;">📞 Contact</h3>
                    <p style="color: #666;"><strong>Téléphone:</strong> [Numéro à ajouter]</p>
                    <p style="color: #666;"><strong>Email:</strong> [Email à ajouter]</p>
                </div>
            </div>
        </div>

        <div id="comptable" class="section">
            <button class="back-btn" onclick="showSection('animateurs')">← Retour</button>
            <div class="card">
                <h2>Comptable</h2>
                <p style="font-size: 1.3rem; color: #667eea; margin-top: 1rem;"><strong>EDAH Yawa Justine</strong></p>
                <div style="margin-top: 2rem; padding: 1.5rem; background: #f8f9fa; border-radius: 8px;">
                    <h3 style="color: #333; margin-bottom: 1rem;">📞 Contact</h3>
                    <p style="color: #666;"><strong>Téléphone:</strong> [Numéro à ajouter]</p>
                    <p style="color: #666;"><strong>Email:</strong> [Email à ajouter]</p>
                </div>
            </div>
        </div>

        <!-- Section Classes -->
        <div id="classes" class="section">
            <h2>Les Classes</h2>
            <div class="team-grid">
                <div class="member-card" onclick="showClasse('classe-peniel')">
                    <h3>📚 Péniel</h3>
                    <p>Voir les détails</p>
                </div>
                <div class="member-card" onclick="showClasse('classe-winners')">
                    <h3>🏆 Winners</h3>
                    <p>Voir les détails</p>
                </div>
                <div class="member-card" onclick="showClasse('classe-elus')">
                    <h3>⭐ Les Élus</h3>
                    <p>Voir les détails</p>
                </div>
                <div class="member-card" onclick="showClasse('classe-providence')">
                    <h3>🌟 La Providence</h3>
                    <p>Voir les détails</p>
                </div>
                <div class="member-card" onclick="showClasse('classe-5')">
                    <h3>📖 Classe 5</h3>
                    <p>Voir les détails</p>
                </div>
                <div class="member-card" onclick="showClasse('classe-6')">
                    <h3>📘 Classe 6</h3>
                    <p>Voir les détails</p>
                </div>
            </div>
        </div>

        <!-- Détails Classes (exemple pour une classe) -->
        <div id="classe-peniel" class="section">
            <button class="back-btn" onclick="showSection('classes')">← Retour</button>
            <div class="card">
                <h2>Classe Péniel</h2>
                <div style="background: #667eea; color: white; padding: 1.5rem; border-radius: 8px; margin: 1.5rem 0;">
                    <h3 style="margin-bottom: 0.5rem;">👨‍🏫 Enseignant(e)</h3>
                    <p style="font-size: 1.2rem;"><strong>[Nom de l'enseignant]</strong></p>
                </div>
                <h3 style="margin-top: 2rem; margin-bottom: 1rem;">📋 Liste des enfants</h3>
                <div class="participant-list">
                    <div class="participant-item">1. [Nom de l'enfant]</div>
                    <div class="participant-item">2. [Nom de l'enfant]</div>
                    <div class="participant-item">3. [Nom de l'enfant]</div>
                    <!-- ... jusqu'à 30 -->
                </div>
            </div>
        </div>

        <!-- Section Participants -->
        <div id="participants" class="section">
            <h2>Participants Enrôlés</h2>
            <div class="card">
                <p style="font-size: 1.1rem; color: #666; margin-bottom: 2rem;">
                    Téléchargez la liste complète des participants avec toutes leurs informations.
                </p>
                <div style="text-align: center;">
                    <a href="#" onclick="alert('Veuillez ajouter le lien vers le fichier PDF'); return false;" 
                       style="display: inline-block; background: linear-gradient(135deg, #667eea 0%, #764ba2 100%); 
                              color: white; padding: 1.2rem 2rem; text-decoration: none; border-radius: 10px; 
                              font-size: 1rem; font-weight: bold;">
                        📄 Télécharger la liste (PDF)
                    </a>
                </div>
            </div>
        </div>

        <!-- Section Événements -->
        <div id="evenements" class="section">
            <h2>Événements</h2>
            <div class="event-card">
                <h3>📅 Activités Hebdomadaires</h3>
                <p style="margin-top: 1rem;">
                    <strong>Tous les samedis</strong><br>
                    Rejoignez-nous pour des activités enrichissantes et éducatives.
                </p>
            </div>
            
            <h3 style="margin-top: 2rem; margin-bottom: 1rem; text-align: center; color: #667eea;">Événements Spéciaux</h3>
            
            <div class="event-card" style="background: linear-gradient(135deg, #fa709a 0%, #fee140 100%);">
                <h3>🎄 Célébration de Noël</h3>
                <p style="margin-top: 0.5rem;">Journée festive pour célébrer Noël avec les enfants.</p>
            </div>

            <div class="event-card" style="background: linear-gradient(135deg, #30cfd0 0%, #330867 100%);">
                <h3>👶 Journée Internationale des Enfants</h3>
                <p style="margin-top: 0.5rem;">Célébration des droits et du bien-être des enfants.</p>
            </div>

            <div class="event-card" style="background: linear-gradient(135deg, #a8edea 0%, #fed6e3 100%); color: #333;">
                <h3>💧 Journée Mondiale de l'Eau</h3>
                <p style="margin-top: 0.5rem;">Sensibilisation à l'importance de l'eau.</p>
            </div>

            <div class="event-card" style="background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);">
                <h3>⚖️ Journée des Droits des Enfants</h3>
                <p style="margin-top: 0.5rem;">Promotion des droits fondamentaux de chaque enfant.</p>
            </div>
        </div>
    </div>

    <script>
        const navBtns = document.querySelectorAll('.nav-btn');
        
        navBtns.forEach(btn => {
            btn.addEventListener('click', () => {
                const section = btn.dataset.section;
                showSection(section);
                
                navBtns.forEach(b => b.classList.remove('active'));
                btn.classList.add('active');
            });
        });

        function showSection(sectionId) {
            const sections = document.querySelectorAll('.section');
            sections.forEach(s => s.classList.remove('active'));
            
            const targetSection = document.getElementById(sectionId);
            if (targetSection) {
                targetSection.classList.add('active');
                window.scrollTo(0, 0);
            }
        }

        function showCPC() {
            showSection('cpc');
        }

        function showAnimateurs() {
            showSection('animateurs');
        }

        function showVolontaires() {
            showSection('volontaires');
        }

        function showClasse(classeId) {
            showSection(classeId);
        }

        function showMemberDetail(memberId) {
            showSection(memberId);
        }
    </script>
</body>
</html>
