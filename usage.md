Voici une explication concrète de **comment et par qui** la solution "e-Citoyen CI" sera utilisée, dans la vraie vie, une fois le MVP déployé.

---

## UTILISATION DE LA SOLUTION "e-Citoyen CI"

---

### I. LES 3 TYPES D'UTILISATEURS

```
┌─────────────────────────────────────────────────────────────────────────┐
│                    QUI UTILISE L'APPLICATION ?                           │
├─────────────────────────────────────────────────────────────────────────┤
│                                                                          │
│  👤 TYPE 1 : LE CITOYEN (Utilisateur principal)                         │
│  ┌───────────────────────────────────────────────────────────────────┐  │
│  │ • Toute personne ayant un smartphone et un numéro de téléphone    │  │
│  │ • Déclare des événements de vie                                   │  │
│  │ • Suit l'avancement de ses dossiers                               │  │
│  │ • Reçoit des notifications                                        │  │
│  │ • Télécharge ses documents administratifs                         │  │
│  │ • Estimation : 500 utilisateurs pour le pilote                    │  │
│  └───────────────────────────────────────────────────────────────────┘  │
│                                                                          │
│  🧑‍💼 TYPE 2 : L'AGENT ADMINISTRATIF (Utilisateur secondaire - futur)     │
│  ┌───────────────────────────────────────────────────────────────────┐  │
│  │ • Fonctionnaire dans une mairie, CNPS, CMU                        │  │
│  │ • Reçoit les dossiers numériques                                  │  │
│  │ • Valide, rejette ou demande des compléments                      │  │
│  │ • Voit un tableau de bord des dossiers à traiter                  │  │
│  │ • Pas dans le MVP, ajouté en V2                                   │  │
│  └───────────────────────────────────────────────────────────────────┘  │
│                                                                          │
│  🔧 TYPE 3 : L'ADMINISTRATEUR TECHNIQUE                                 │
│  ┌───────────────────────────────────────────────────────────────────┐  │
│  │ • Membre de l'équipe technique                                    │  │
│  │ • Supervise le bon fonctionnement du système                      │  │
│  │ • Ajoute de nouveaux événements de vie                            │  │
│  │ • Connecte de nouvelles administrations                           │  │
│  │ • Gère les incidents                                              │  │
│  └───────────────────────────────────────────────────────────────────┘  │
│                                                                          │
└─────────────────────────────────────────────────────────────────────────┘
```

---

### II. SCÉNARIOS D'UTILISATION RÉELS

#### Scénario 1 : Le Jeune Parent (Cas le plus fréquent)

```
┌─────────────────────────────────────────────────────────────────────────┐
│  SITUATION : Koffi, 32 ans, employé, vit à Abidjan                       │
│  Sa femme vient d'accoucher au CHU de Cocody                            │
│  Il a un smartphone Android, est à l'aise avec les apps                 │
├─────────────────────────────────────────────────────────────────────────┤
│                                                                          │
│  AVANT e-Citoyen CI (Ce qu'il faisait)                                  │
│  ──────────────────────────────────                                      │
│  Jour 1 : Aller à la mairie → Faire la queue → Déclarer naissance       │
│  Jour 3 : Retourner à la mairie → Récupérer extrait de naissance        │
│  Jour 4 : Aller à la CNPS → Déposer dossier allocations                 │
│  Jour 7 : Aller à la CMU → Déposer dossier inscription                  │
│  ⏱️ Temps total : ~15 jours, 4 déplacements, 3 files d'attente          │
│  💰 Coût : Transport + temps de travail perdu                           │
│                                                                          │
│  AVEC e-Citoyen CI (Ce qu'il fait maintenant)                           │
│  ───────────────────────────────────────                                  │
│  1. Assis dans la chambre d'hôpital, il télécharge l'app               │
│  2. Il crée son compte avec son numéro de téléphone                    │
│  3. Il clique sur "Naissance d'un enfant"                              │
│  4. Il remplit : nom, date, lieu                                       │
│  5. Il prend en photo le certificat médical avec son téléphone         │
│  6. Il clique sur "Lancer les démarches"                               │
│  7. Il range son téléphone                                             │
│  8. 2 jours plus tard, il reçoit un SMS : "Tout est prêt !"           │
│  9. Il ouvre l'app, télécharge l'extrait de naissance en PDF           │
│  ⏱️ Temps total : 5 minutes de saisie, 0 déplacement                   │
│  💰 Coût : 0 FCFA                                                      │
│                                                                          │
└─────────────────────────────────────────────────────────────────────────┘
```

---

#### Scénario 2 : La Mère Célibataire en Zone Périurbaine

```
┌─────────────────────────────────────────────────────────────────────────┐
│  SITUATION : Awa, 24 ans, vit à Anyama, travaille au marché             │
│  Vient d'accoucher à l'hôpital général d'Anyama                         │
│  A un smartphone mais connexion internet instable                       │
├─────────────────────────────────────────────────────────────────────────┤
│                                                                          │
│  UTILISATION DE L'APPLICATION                                           │
│  ─────────────────────────                                              │
│                                                                          │
│  1. L'infirmière de l'hôpital lui montre l'app                          │
│  2. Elle télécharge l'app sur le WiFi de l'hôpital                      │
│  3. Elle crée son compte (même sans savoir lire, une aide-soignante     │
│     l'aide 2 minutes)                                                   │
│  4. Elle prend la photo du certificat médical                           │
│  5. Elle clique sur le bouton vert "Lancer"                             │
│  6. Même si elle perd la connexion, le formulaire est déjà envoyé       │
│  7. Elle reçoit un SMS (pas besoin d'internet pour recevoir un SMS)     │
│  8. Elle retourne à l'hôpital la semaine suivante, l'infirmière         │
│     l'aide à télécharger l'extrait de naissance sur le WiFi             │
│                                                                          │
│  POINTS FORTS POUR CE PROFIL :                                          │
│  ✅ Fonctionne avec une connexion faible                                │
│  ✅ L'interface est en français simple, avec icônes                     │
│  ✅ Le SMS informe même sans smartphone récent                          │
│  ✅ Une personne peut aider pour la 1ère utilisation                    │
│                                                                          │
└─────────────────────────────────────────────────────────────────────────┘
```

---

#### Scénario 3 : L'Agent de Mairie (Tableau de bord - Version Future)

```
┌─────────────────────────────────────────────────────────────────────────┐
│  SITUATION : Mme Koné, officier d'état civil à la Mairie de Cocody      │
│  Reçoit 30 déclarations de naissance par jour                           │
│  Actuellement, elle traite des dossiers papier                          │
├─────────────────────────────────────────────────────────────────────────┤
│                                                                          │
│  AVANT (Son quotidien actuel)                                           │
│  ─────────────────────────────                                           │
│  • Des piles de dossiers papiers sur son bureau                         │
│  • Des citoyens qui frappent à sa porte pour savoir où en est le dossier│
│  • Des dossiers perdus ou mal classés                                   │
│  • Impossible de savoir combien de dossiers sont en attente             │
│                                                                          │
│  APRÈS (Avec le tableau de bord - V2)                                   │
│  ─────────────────────────────────────                                    │
│                                                                          │
│  ┌─────────────────────────────────────────────────────────────────┐    │
│  │              TABLEAU DE BORD AGENT MAIRIE                        │    │
│  │              ────────────────────────────                        │    │
│  │                                                                  │    │
│  │  📊 AUJOURD'HUI : 12 nouveaux dossiers                          │    │
│  │                                                                  │    │
│  │  ⏳ EN ATTENTE (5)          ✅ TRAITÉS (25)        ❌ REJETÉS (2) │    │
│  │                                                                  │    │
│  │  ┌─────────────────────────────────────────────────────────┐    │    │
│  │  │ N°     │ NOM ENFANT   │ DATE      │ STATUT    │ ACTION  │    │    │
│  │  ├────────┼──────────────┼───────────┼───────────┼─────────┤    │    │
│  │  │ 001    │ KOFFI Junior │ 15/06/2026│ En attente│ [Voir]  │    │    │
│  │  │ 002    │ TRAORÉ Awa   │ 15/06/2026│ En attente│ [Voir]  │    │    │
│  │  │ 003    │ BAMBA Moussa │ 14/06/2026│ En attente│ [Voir]  │    │    │
│  │  └─────────────────────────────────────────────────────────┘    │    │
│  │                                                                  │    │
│  └─────────────────────────────────────────────────────────────────┘    │
│                                                                          │
│  ELLE CLIQUE SUR "KOFFI Junior" → VOIT LE DOSSIER COMPLET :             │
│  ┌─────────────────────────────────────────────────────────────────┐    │
│  │  • Formulaire de déclaration rempli automatiquement             │    │
│  │  • Certificat médical en pièce jointe (photo)                   │    │
│  │  • Bouton [✅ VALIDER] ou [❌ REJETER] ou [📝 DEMANDER INFOS]   │    │
│  └─────────────────────────────────────────────────────────────────┘    │
│                                                                          │
│  RÉSULTAT :                                                              │
│  ✅ Elle clique "Valider" → L'extrait est généré automatiquement (PDF)  │
│  ✅ Le citoyen reçoit une notification instantanément                    │
│  ✅ Le dossier est archivé numériquement, plus jamais perdu              │
│                                                                          │
└─────────────────────────────────────────────────────────────────────────┘
```

---

### III. COMMENT L'APPLICATION SERA DÉPLOYÉE ET DISTRIBUÉE

```
┌─────────────────────────────────────────────────────────────────────────┐
│                    STRATÉGIE DE DÉPLOIEMENT                              │
├─────────────────────────────────────────────────────────────────────────┤
│                                                                          │
│  PHASE 1 : PILOTE (Mois 1-3 après MVP)                                  │
│  ┌───────────────────────────────────────────────────────────────────┐  │
│  │ OÙ : 1 mairie pilote (ex: Mairie du Plateau ou Cocody)           │  │
│  │ QUI : 200-500 citoyens test                                       │  │
│  │ COMMENT :                                                          │  │
│  │  • L'app n'est pas sur le Play Store                              │  │
│  │  • Distribution par lien direct (APK) via WhatsApp                │  │
│  │  • QR Code affiché dans la mairie et l'hôpital                    │  │
│  │  • Des agents formés aident les citoyens à installer l'app        │  │
│  │  • Collecte de feedback chaque semaine                            │  │
│  └───────────────────────────────────────────────────────────────────┘  │
│                                                                          │
│  PHASE 2 : EXTENSION (Mois 4-6)                                         │
│  ┌───────────────────────────────────────────────────────────────────┐  │
│  │ OÙ : 5 mairies + 3 hôpitaux à Abidjan                            │  │
│  │ QUI : 2000-5000 utilisateurs                                      │  │
│  │ COMMENT :                                                          │  │
│  │  • Publication sur Google Play Store                              │  │
│  │  • Partenariat avec Orange/MTN/Moov pour zéro coût data           │  │
│  │  • Campagne SMS : "Déclarez la naissance de votre enfant          │  │
│  │    depuis votre téléphone. Téléchargez e-Citoyen CI"              │  │
│  │  • Affiches dans les mairies et hôpitaux                          │  │
│  └───────────────────────────────────────────────────────────────────┘  │
│                                                                          │
│  PHASE 3 : NATIONAL (Mois 7-12)                                         │
│  ┌───────────────────────────────────────────────────────────────────┐  │
│  │ OÙ : Toute la Côte d'Ivoire                                       │  │
│  │ QUI : 50 000+ utilisateurs                                        │  │
│  │ COMMENT :                                                          │  │
│  │  • Intégration dans le portail national servicepublic.gouv.ci     │  │
│  │  • Obligation légale pour les administrations d'accepter          │  │
│  │    les dossiers via e-Citoyen CI                                  │  │
│  │  • Campagne nationale TV/Radio                                    │  │
│  │  • Points d'assistance dans chaque sous-préfecture                │  │
│  └───────────────────────────────────────────────────────────────────┘  │
│                                                                          │
└─────────────────────────────────────────────────────────────────────────┘
```

---

### IV. CAS D'USAGE QUOTIDIENS (Quand et comment on ouvre l'app)

```
┌─────────────────────────────────────────────────────────────────────────┐
│            QUAND LE CITOYEN UTILISE L'APPLICATION                       │
├─────────────────────────────────────────────────────────────────────────┤
│                                                                          │
│  📱 USAGE ÉVÉNEMENTIEL (Quelques fois par an)                           │
│  ┌───────────────────────────────────────────────────────────────────┐  │
│  │ • Naissance d'un enfant                                            │  │
│  │ • Décès d'un proche                                                │  │
│  │ • Déménagement                                                     │  │
│  │ • Mariage                                                          │  │
│  │ • Création d'entreprise                                            │  │
│  │ → L'utilisateur ouvre l'app seulement quand un événement survient  │  │
│  └───────────────────────────────────────────────────────────────────┘  │
│                                                                          │
│  📱 USAGE DE SUIVI (Quelques jours après l'événement)                   │
│  ┌───────────────────────────────────────────────────────────────────┐  │
│  │ • Vérifier où en sont ses dossiers                                 │  │
│  │ • Voir si un document complémentaire est demandé                   │  │
│  │ • Télécharger un document final (extrait, attestation)             │  │
│  │ → L'utilisateur ouvre l'app 2-3 fois par dossier                   │  │
│  └───────────────────────────────────────────────────────────────────┘  │
│                                                                          │
│  📱 USAGE PASSIF (Sans ouvrir l'app)                                    │
│  ┌───────────────────────────────────────────────────────────────────┐  │
│  │ • Reçoit un SMS quand un document est prêt                         │  │
│  │ • Reçoit une notification Push quand une action est requise        │  │
│  │ • L'application travaille en arrière-plan                          │  │
│  │ → L'utilisateur n'a rien à faire, il est informé automatiquement   │  │
│  └───────────────────────────────────────────────────────────────────┘  │
│                                                                          │
└─────────────────────────────────────────────────────────────────────────┘
```

---

### V. OÙ ET DANS QUELLES CONDITIONS L'APPLICATION SERA UTILISÉE

```
┌─────────────────────────────────────────────────────────────────────────┐
│                    LIEUX ET CONTEXTES D'UTILISATION                      │
├─────────────────────────────────────────────────────────────────────────┤
│                                                                          │
│  🏥 À L'HÔPITAL (Lieu de déclenchement principal)                       │
│  ┌───────────────────────────────────────────────────────────────────┐  │
│  │ • Juste après l'accouchement                                       │  │
│  │ • La sage-femme ou l'infirmière montre l'app à la mère/père       │  │
│  │ • Connexion WiFi de l'hôpital utilisée pour télécharger l'app     │  │
│  │ • Le certificat médical est photographié immédiatement             │  │
│  │ • Avantage : le document ne peut pas être perdu                    │  │
│  └───────────────────────────────────────────────────────────────────┘  │
│                                                                          │
│  🏠 À LA MAISON                                                         │
│  ┌───────────────────────────────────────────────────────────────────┐  │
│  │ • L'utilisateur déclare l'événement depuis son canapé             │  │
│  │ • Utilise sa connexion mobile ou WiFi domestique                  │  │
│  │ • Peut prendre son temps pour remplir le formulaire               │  │
│  │ • Pas de pression, pas de file d'attente                          │  │
│  └───────────────────────────────────────────────────────────────────┘  │
│                                                                          │
│  🏛️ DANS UN POINT D'ACCÈS NUMÉRIQUE (Futur)                             │
│  ┌───────────────────────────────────────────────────────────────────┐  │
│  │ • Bornes interactives dans les mairies et sous-préfectures        │  │
│  │ • Un agent aide les citoyens sans smartphone                      │  │
│  │ • L'agent utilise l'app sur une tablette pour le compte du citoyen│  │
│  │ • Accessible aux personnes âgées ou non connectées                │  │
│  └───────────────────────────────────────────────────────────────────┘  │
│                                                                          │
│  🚌 EN MOBILITÉ (Dans les transports)                                   │
│  ┌───────────────────────────────────────────────────────────────────┐  │
│  │ • L'utilisateur remplit le formulaire dans le bus ou le taxi      │  │
│  │ • L'application fonctionne avec une connexion 3G faible           │  │
│  │ • Le formulaire est envoyé dès que la connexion revient           │  │
│  └───────────────────────────────────────────────────────────────────┘  │
│                                                                          │
└─────────────────────────────────────────────────────────────────────────┘
```

---

### VI. COMMENT L'APPLICATION SERA MAINTENUE ET ÉVOLUERA

```
┌─────────────────────────────────────────────────────────────────────────┐
│                    CYCLE DE VIE DE LA SOLUTION                           │
├─────────────────────────────────────────────────────────────────────────┤
│                                                                          │
│  🔄 MAINTENANCE HEBDOMADAIRE                                            │
│  ┌───────────────────────────────────────────────────────────────────┐  │
│  │ • Vérification que les simulateurs répondent                       │  │
│  │ • Monitoring des erreurs (Sentry ou équivalent)                    │  │
│  │ • Correction de bugs mineurs                                       │  │
│  │ • Mise à jour du Play Store si nécessaire                          │  │
│  └───────────────────────────────────────────────────────────────────┘  │
│                                                                          │
│  📈 ÉVOLUTION MENSUELLE                                                  │
│  ┌───────────────────────────────────────────────────────────────────┐  │
│  │ • Analyse des feedbacks utilisateurs                               │  │
│  │ • Ajout d'améliorations UI/UX                                      │  │
│  │ • Optimisation des performances                                    │  │
│  │ • Nouveau build APK                                                │  │
│  └───────────────────────────────────────────────────────────────────┘  │
│                                                                          │
│  🚀 ÉVOLUTION TRIMESTRIELLE                                             │
│  ┌───────────────────────────────────────────────────────────────────┐  │
│  │ • Ajout d'un nouvel événement de vie (ex: Déménagement)            │  │
│  │ • Ajout d'un nouveau simulateur (ex: Impôts)                       │  │
│  │ • Remplacement d'un simulateur par une vraie API                   │  │
│  │ • Nouvelle fonctionnalité majeure                                  │  │
│  └───────────────────────────────────────────────────────────────────┘  │
│                                                                          │
│  🏛️ GOUVERNANCE (Qui décide ?)                                          │
│  ┌───────────────────────────────────────────────────────────────────┐  │
│  │ • Comité de pilotage : Équipe technique + ANSUT + Mairie pilote    │  │
│  │ • Réunion mensuelle pour prioriser les évolutions                  │  │
│  │ • Validation des nouvelles règles métier par l'administration      │  │
│  └───────────────────────────────────────────────────────────────────┘  │
│                                                                          │
└─────────────────────────────────────────────────────────────────────────┘
```

---

### VII. MESURES DE SUCCÈS (Comment on saura que ça marche)

```
┌─────────────────────────────────────────────────────────────────────────┐
│                    INDICATEURS CLÉS DE SUCCÈS                            │
├─────────────────────────────────────────────────────────────────────────┤
│                                                                          │
│  📊 INDICATEURS QUANTITATIFS                                            │
│  ┌───────────────────────────────────────────────────────────────────┐  │
│  │                                                                    │  │
│  │  Nombre de téléchargements    ████████░░░░░░░░  500 (objectif)    │  │
│  │                                                                    │  │
│  │  Nombre de dossiers créés     ██████████░░░░░░  300 dossiers      │  │
│  │                                                                    │  │
│  │  Taux de complétion           ██████████████░░  85% (pas d'abandon)│  │
│  │                                                                    │  │
│  │  Temps moyen de complétion    ████████████████  4 min 30s          │  │
│  │                                                                    │  │
│  │  Délai moyen de traitement    ██████████░░░░░░  48h (vs 15 jours)  │  │
│  │                                                                    │  │
│  │  Nombre de bugs critiques     ░░░░░░░░░░░░░░░░  0                  │  │
│  │                                                                    │  │
│  └───────────────────────────────────────────────────────────────────┘  │
│                                                                          │
│  💬 INDICATEURS QUALITATIFS                                             │
│  ┌───────────────────────────────────────────────────────────────────┐  │
│  │ • "Je n'ai pas eu à me déplacer" — Témoignage d'Awa, Anyama       │  │
│  │ • "J'ai tout fait depuis l'hôpital" — Témoignage de Koffi, Cocody │  │
│  │ • "L'app est simple comme WhatsApp" — Témoignage utilisateur      │  │
│  │ • Note moyenne sur le Play Store : 4.2/5 ⭐                        │  │
│  └───────────────────────────────────────────────────────────────────┘  │
│                                                                          │
└─────────────────────────────────────────────────────────────────────────┘
```

---

### VIII. RÉSUMÉ VISUEL : UNE JOURNÉE TYPE AVEC e-Citoyen CI

```
┌─────────────────────────────────────────────────────────────────────────┐
│            UNE JOURNÉE DANS LA VIE D'UN UTILISATEUR                     │
├─────────────────────────────────────────────────────────────────────────┤
│                                                                          │
│  08:00  🏥  Naissance de Koffi Junior au CHU de Cocody                  │
│  09:30  📱  Le père télécharge e-Citoyen CI                             │
│  09:35  📝  Il remplit le formulaire (nom, date, lieu)                  │
│  09:37  📸  Il photographie le certificat médical                       │
│  09:38  🚀  Il clique sur "Lancer les démarches"                        │
│  09:38  ⚙️   L'Agent Coordonnateur crée 3 dossiers automatiquement      │
│  09:50  🏛️  Mairie : dossier reçu                                      │
│  10:00  🏥  CNPS : dossier reçu                                        │
│  10:10  🏥  CMU : dossier reçu                                         │
│                                                                          │
│  ... Le système travaille tout seul ...                                  │
│                                                                          │
│  12:00  ✅  Mairie : extrait de naissance généré                        │
│  14:00  ✅  CMU : inscription validée                                   │
│  16:00  ✅  CNPS : allocations activées                                 │
│                                                                          │
│  16:05  📱  Notification Push : "Toutes vos démarches sont terminées"   │
│  16:05  💬  SMS reçu : "Extrait de naissance prêt, allocations OK..."   │
│                                                                          │
│  16:10  📄  Le père ouvre l'app, télécharge l'extrait de naissance      │
│  16:15  🎉  FIN. Tout est réglé.                                        │
│                                                                          │
│  ⏱️  Temps actif de l'utilisateur : 7 minutes                           │
│  🏛️  Déplacements physiques : 0                                         │
│  📄  Documents fournis : 1 (au lieu de 3)                               │
│                                                                          │
└─────────────────────────────────────────────────────────────────────────┘
```

