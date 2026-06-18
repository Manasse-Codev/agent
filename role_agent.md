Voici une description détaillée du **rôle de chaque agent** dans l'écosystème e-Citoyen CI, organisée par catégorie.

---

## RÔLES DES AGENTS DE L'ÉCOSYSTÈME e-Citoyen CI

---

### I. VUE D'ENSEMBLE

```
┌─────────────────────────────────────────────────────────────────────────┐
│                 ÉCOSYSTÈME MULTI-AGENTS — 15 AGENTS                      │
├─────────────────────────────────────────────────────────────────────────┤
│                                                                          │
│                        🎼 AGENT COORDONNATEUR                            │
│                        (Chef d'orchestre)                                │
│                              │                                           │
│         ┌────────────────────┼────────────────────┐                     │
│         │                    │                    │                     │
│    👤 AGENTS           🏛️ AGENTS              ⚙️ AGENTS                │
│    PERSONNELS          INSTITUTIONNELS        TECHNIQUES                │
│         │                    │                    │                     │
│    ┌────┴────┐        ┌──────┴──────┐        ┌───┴────┐               │
│    │Citoyen  │        │Mairie       │        │Notaire │               │
│    │Entrepr. │        │ONECI        │        │Paiement│               │
│    │Fonction.│        │Justice      │        │Registre│               │
│    │         │        │Impôts       │        │         │               │
│    │         │        │CNPS/CMU     │        │         │               │
│    │         │        │Domaine      │        │         │               │
│    │         │        │Éducation    │        │         │               │
│    └─────────┘        └─────────────┘        └─────────┘               │
│                                                                          │
│    🔔 AGENT NOTIFICATEUR          🦮 AGENT SURVEILLANT                  │
│    (Messager multicanal)          (Chien de garde)                       │
│                                                                          │
└─────────────────────────────────────────────────────────────────────────┘
```

---

### II. FICHE DÉTAILLÉE DE CHAQUE AGENT

---

#### 👤 CATÉGORIE 1 : AGENTS PERSONNELS
#### (Représentants numériques des utilisateurs)

---

```
┌─────────────────────────────────────────────────────────────────────────┐
│                                                                          │
│   🧑 AGENT CITOYEN                                                       │
│   ───────────────────────────────────────────────────────────────────   │
│                                                                          │
│   RÔLE PRINCIPAL :                                                       │
│   Représenter et assister un citoyen dans toutes ses interactions        │
│   avec l'administration publique. Il est le "guichet unique              │
│   numérique" de l'usager.                                                │
│                                                                          │
│   RESPONSABILITÉS :                                                      │
│   ┌─────────────────────────────────────────────────────────────────┐   │
│   │                                                                  │   │
│   │  🆔 IDENTITÉ NUMÉRIQUE                                          │   │
│   │  • Stocke et gère l'identité vérifiée du citoyen                │   │
│   │  • Conserve les données personnelles (nom, prénom, N° CNI)      │   │
│   │  • Gère les préférences de contact (SMS, Push, Email)           │   │
│   │                                                                  │   │
│   │  📋 GESTION DES DROITS                                           │   │
│   │  • Connaît les droits ouverts du citoyen (allocations, CMU...)  │   │
│   │  • Alerte sur les droits non réclamés                            │   │
│   │  • Anticipe les renouvellements (CNI, passeport...)             │   │
│   │                                                                  │   │
│   │  📜 HISTORIQUE ADMINISTRATIF                                     │   │
│   │  • Conserve l'historique complet des démarches                  │   │
│   │  • Archive les documents obtenus                                 │   │
│   │  • Permet la recherche dans l'historique                        │   │
│   │                                                                  │   │
│   │  🗣️ INTERFACE UTILISATEUR                                        │   │
│   │  • Point d'entrée unique pour toutes les démarches              │   │
│   │  • Traduit le langage administratif en actions simples          │   │
│   │  • Guide l'utilisateur étape par étape                           │   │
│   │                                                                  │   │
│   │  🔔 RÉCEPTION DES NOTIFICATIONS                                  │   │
│   │  • Reçoit les alertes de l'Agent Notificateur                   │   │
│   │  • Affiche les notifications dans l'application                 │   │
│   │  • Priorise les urgences                                         │   │
│   │                                                                  │   │
│   └─────────────────────────────────────────────────────────────────┘   │
│                                                                          │
│   INTERACTIONS AVEC LES AUTRES AGENTS :                                  │
│   ┌─────────────────────────────────────────────────────────────────┐   │
│   │  → Agent Coordonnateur : Transmet les événements de vie          │   │
│   │  → Agent Notificateur : Reçoit les messages                      │   │
│   │  → Tous les Agents Institutionnels : Via le Coordinateur         │   │
│   └─────────────────────────────────────────────────────────────────┘   │
│                                                                          │
│   VERSION : MVP                                                          │
│                                                                          │
└─────────────────────────────────────────────────────────────────────────┘
```

```
┌─────────────────────────────────────────────────────────────────────────┐
│                                                                          │
│   🏢 AGENT ENTREPRENEUR                                                  │
│   ───────────────────────────────────────────────────────────────────   │
│                                                                          │
│   RÔLE PRINCIPAL :                                                       │
│   Représenter un créateur d'entreprise ou une société dans toutes        │
│   ses démarches administratives.                                         │
│                                                                          │
│   RESPONSABILITÉS :                                                      │
│   ┌─────────────────────────────────────────────────────────────────┐   │
│   │                                                                  │   │
│   │  📋 CYCLE DE VIE DE L'ENTREPRISE                                 │   │
│   │  • Gère la création d'entreprise (immatriculation RCCM)         │   │
│   │  • Suit les modifications statutaires                            │   │
│   │  • Gère la cessation d'activité                                  │   │
│   │                                                                  │   │
│   │  💰 OBLIGATIONS FISCALES ET SOCIALES                             │   │
│   │  • Suit les déclarations fiscales périodiques                    │   │
│   │  • Gère les déclarations CNPS (employés)                         │   │
│   │  • Anticipe les échéances                                        │   │
│   │                                                                  │   │
│   │  📄 DOCUMENTS LÉGAUX                                             │   │
│   │  • Conserve les statuts, patente, registre de commerce           │   │
│   │  • Archive les attestations fiscales et sociales                 │   │
│   │  • Permet le téléchargement des documents                        │   │
│   │                                                                  │   │
│   └─────────────────────────────────────────────────────────────────┘   │
│                                                                          │
│   INTERACTIONS :                                                         │
│   ┌─────────────────────────────────────────────────────────────────┐   │
│   │  → Agent Coordonnateur : Transmet les événements                 │   │
│   │  → Agent Fisc, Agent CNPS, Agent CEPICI                          │   │
│   └─────────────────────────────────────────────────────────────────┘   │
│                                                                          │
│   VERSION : V2                                                           │
│                                                                          │
└─────────────────────────────────────────────────────────────────────────┘
```

```
┌─────────────────────────────────────────────────────────────────────────┐
│                                                                          │
│   🧑‍💼 AGENT FONCTIONNAIRE                                                  │
│   ───────────────────────────────────────────────────────────────────   │
│                                                                          │
│   RÔLE PRINCIPAL :                                                       │
│   Assister l'agent de l'État humain dans son travail quotidien           │
│   d'instruction, de vérification et de décision administrative.          │
│                                                                          │
│   RESPONSABILITÉS :                                                      │
│   ┌─────────────────────────────────────────────────────────────────┐   │
│   │                                                                  │   │
│   │  📥 RÉCEPTION ET TRI DES DOSSIERS                                │   │
│   │  • Reçoit les dossiers numériques des citoyens                  │   │
│   │  • Trie par priorité, date, type de demande                     │   │
│   │  • Présente une liste de travail organisée                      │   │
│   │                                                                  │   │
│   │  🔍 VÉRIFICATION AUTOMATIQUE                                     │   │
│   │  • Vérifie la complétude du dossier                              │   │
│   │  • Croise les informations avec d'autres sources                 │   │
│   │  • Détecte les incohérences ou fraudes potentielles              │   │
│   │                                                                  │   │
│   │  ✍️ AIDE À LA DÉCISION                                            │   │
│   │  • Propose une décision basée sur les règles métier             │   │
│   │  • Prépare les documents à signer                                │   │
│   │  • Laisse la validation finale à l'humain                       │   │
│   │                                                                  │   │
│   └─────────────────────────────────────────────────────────────────┘   │
│                                                                          │
│   NOTE : Cet agent ne remplace PAS le fonctionnaire humain,              │
│   il l'assiste. La décision finale reste humaine.                        │
│                                                                          │
│   VERSION : V1                                                           │
│                                                                          │
└─────────────────────────────────────────────────────────────────────────┘
```

---

#### 🏛️ CATÉGORIE 2 : AGENTS INSTITUTIONNELS
#### (Représentants des administrations)

---

```
┌─────────────────────────────────────────────────────────────────────────┐
│                                                                          │
│   🏛️ AGENT MAIRIE (État Civil)                                          │
│   ───────────────────────────────────────────────────────────────────   │
│                                                                          │
│   RÔLE PRINCIPAL :                                                       │
│   Gérer et délivrer tous les actes d'état civil de manière              │
│   sécurisée et dématérialisée.                                           │
│                                                                          │
│   RESPONSABILITÉS :                                                      │
│   ┌─────────────────────────────────────────────────────────────────┐   │
│   │                                                                  │   │
│   │  👶 NAISSANCE                                                    │   │
│   │  • Réceptionne les déclarations de naissance                     │   │
│   │  • Vérifie le certificat médical                                 │   │
│   │  • Génère l'extrait d'acte de naissance (PDF sécurisé)          │   │
│   │  • Transmet le document à l'Agent Notaire pour signature         │   │
│   │                                                                  │   │
│   │  💒 MARIAGE                                                      │   │
│   │  • Gère les dossiers de mariage civil                            │   │
│   │  • Vérifie les pièces constitutives                              │   │
│   │  • Génère le certificat de mariage                               │   │
│   │                                                                  │   │
│   │  🕊️ DÉCÈS                                                        │   │
│   │  • Enregistre les déclarations de décès                          │   │
│   │  • Génère le certificat de décès                                 │   │
│   │  • Alerte l'Agent Coordonnateur (déclenche autres démarches)     │   │
│   │                                                                  │   │
│   └─────────────────────────────────────────────────────────────────┘   │
│                                                                          │
│   ÉVÉNEMENTS ÉMIS :                                                     │
│   • "naissance:enregistree" → Déclenche CNPS, CMU                       │
│   • "deces:enregistre" → Déclenche pension réversion                    │
│                                                                          │
│   VERSION : MVP                                                          │
│                                                                          │
└─────────────────────────────────────────────────────────────────────────┘
```

```
┌─────────────────────────────────────────────────────────────────────────┐
│                                                                          │
│   🪪 AGENT IDENTITÉ (ONECI)                                              │
│   ───────────────────────────────────────────────────────────────────   │
│                                                                          │
│   RÔLE PRINCIPAL :                                                       │
│   Gérer les pièces d'identité nationales et l'authentification           │
│   des citoyens dans l'écosystème.                                        │
│                                                                          │
│   RESPONSABILITÉS :                                                      │
│   ┌─────────────────────────────────────────────────────────────────┐   │
│   │                                                                  │   │
│   │  🪪 CARTE NATIONALE D'IDENTITÉ (CNI)                             │   │
│   │  • Gère les demandes de première CNI                              │   │
│   │  • Gère les renouvellements (péremption, perte, vol)             │   │
│   │  • Suit le processus de fabrication                               │   │
│   │                                                                  │   │
│   │  🛂 PASSEPORT                                                     │   │
│   │  • Gère les demandes de passeport                                 │   │
│   │  • Vérifie les pièces requises                                    │   │
│   │  • Suit la production et la mise à disposition                   │   │
│   │                                                                  │   │
│   │  🔐 AUTHENTIFICATION                                              │   │
│   │  • Vérifie l'identité des citoyens via la base ONECI            │   │
│   │  • Fournit un jeton d'identité vérifiée aux autres agents        │   │
│   │  • Gère les données biométriques (futur)                         │   │
│   │                                                                  │   │
│   └─────────────────────────────────────────────────────────────────┘   │
│                                                                          │
│   VERSION : V1                                                           │
│                                                                          │
└─────────────────────────────────────────────────────────────────────────┘
```

```
┌─────────────────────────────────────────────────────────────────────────┐
│                                                                          │
│   ⚖️ AGENT JUSTICE                                                       │
│   ───────────────────────────────────────────────────────────────────   │
│                                                                          │
│   RÔLE PRINCIPAL :                                                       │
│   Gérer l'accès sécurisé aux informations judiciaires et                 │
│   administratives liées à la justice.                                    │
│                                                                          │
│   RESPONSABILITÉS :                                                      │
│   ┌─────────────────────────────────────────────────────────────────┐   │
│   │                                                                  │   │
│   │  📋 CASIER JUDICIAIRE (Bulletin N°3)                             │   │
│   │  • Reçoit les demandes de casier judiciaire                      │   │
│   │  • Vérifie l'identité du demandeur via Agent ONECI               │   │
│   │  • Délivre le bulletin n°3 de manière sécurisée                  │   │
│   │                                                                  │   │
│   │  🇨🇮 CERTIFICAT DE NATIONALITÉ                                    │   │
│   │  • Gère les demandes de certificat de nationalité                │   │
│   │  • Vérifie les conditions légales                                │   │
│   │  • Transmet le certificat signé                                  │   │
│   │                                                                  │   │
│   └─────────────────────────────────────────────────────────────────┘   │
│                                                                          │
│   VERSION : V2                                                           │
│                                                                          │
└─────────────────────────────────────────────────────────────────────────┘
```

```
┌─────────────────────────────────────────────────────────────────────────┐
│                                                                          │
│   💰 AGENT FISC (Direction Générale des Impôts)                          │
│   ───────────────────────────────────────────────────────────────────   │
│                                                                          │
│   RÔLE PRINCIPAL :                                                       │
│   Gérer l'identifiant fiscal unique, les déclarations et les             │
│   attestations fiscales.                                                 │
│                                                                          │
│   RESPONSABILITÉS :                                                      │
│   ┌─────────────────────────────────────────────────────────────────┐   │
│   │                                                                  │   │
│   │  🔢 IDENTIFIANT FISCAL UNIQUE                                    │   │
│   │  • Attribue l'identifiant fiscal aux citoyens et entreprises     │   │
│   │  • Lie l'identifiant au profil citoyen                           │   │
│   │                                                                  │   │
│   │  📊 DÉCLARATIONS FISCALES                                        │   │
│   │  • Reçoit les déclarations de revenus                            │   │
│   │  • Calcule l'impôt dû                                            │   │
│   │  • Génère les avis d'imposition                                   │   │
│   │                                                                  │   │
│   │  📄 ATTESTATIONS                                                 │   │
│   │  • Délivre les attestations de situation fiscale                 │   │
│   │  • Délivre les quitus fiscaux                                    │   │
│   │  • Transmet aux autres agents sur demande                        │   │
│   │                                                                  │   │
│   └─────────────────────────────────────────────────────────────────┘   │
│                                                                          │
│   VERSION : V1                                                           │
│                                                                          │
└─────────────────────────────────────────────────────────────────────────┘
```

```
┌─────────────────────────────────────────────────────────────────────────┐
│                                                                          │
│   🏥 AGENT SOCIAL (CNPS / CMU)                                           │
│   ───────────────────────────────────────────────────────────────────   │
│                                                                          │
│   RÔLE PRINCIPAL :                                                       │
│   Gérer les droits sociaux, les prestations familiales et la             │
│   couverture maladie universelle.                                        │
│                                                                          │
│   RESPONSABILITÉS :                                                      │
│   ┌─────────────────────────────────────────────────────────────────┐   │
│   │                                                                  │   │
│   │  👨‍👩‍👧‍👦 PRESTATIONS FAMILIALES (CNPS)                                   │   │
│   │  • Gère les allocations familiales                                │   │
│   │  • Gère les allocations prénatales                                │   │
│   │  • Gère les pensions de retraite                                  │   │
│   │  • Gère les pensions de réversion (décès)                         │   │
│   │  • Vérifie les conditions d'éligibilité                           │   │
│   │                                                                  │   │
│   │  🏥 COUVERTURE MALADIE UNIVERSELLE (CMU)                          │   │
│   │  • Gère les inscriptions à la CMU                                 │   │
│   │  • Gère les renouvellements                                       │   │
│   │  • Ajoute les bénéficiaires (enfants, conjoint)                   │   │
│   │  • Vérifie les droits à la couverture                             │   │
│   │                                                                  │   │
│   │  🏢 EMPLOYEURS                                                    │   │
│   │  • Gère l'immatriculation des employeurs                          │   │
│   │  • Reçoit les déclarations de salaires                            │   │
│   │  • Calcule les cotisations                                        │   │
│   │                                                                  │   │
│   └─────────────────────────────────────────────────────────────────┘   │
│                                                                          │
│   ÉVÉNEMENTS ÉMIS :                                                     │
│   • "droits:ouverts" → Informe l'Agent Citoyen de nouveaux droits       │
│   • "prestation:activee" → Confirme l'activation d'une prestation       │
│                                                                          │
│   VERSION : MVP (allocations + CMU)                                      │
│                                                                          │
└─────────────────────────────────────────────────────────────────────────┘
```

```
┌─────────────────────────────────────────────────────────────────────────┐
│                                                                          │
│   🏠 AGENT DOMAINE & FONCIER                                             │
│   ───────────────────────────────────────────────────────────────────   │
│                                                                          │
│   RÔLE PRINCIPAL :                                                       │
│   Gérer les informations cadastrales, les titres de propriété            │
│   et les autorisations d'urbanisme.                                      │
│                                                                          │
│   RESPONSABILITÉS :                                                      │
│   ┌─────────────────────────────────────────────────────────────────┐   │
│   │                                                                  │   │
│   │  🗺️ CADASTRE                                                     │   │
│   │  • Fournit les extraits cadastraux                               │   │
│   │  • Vérifie la situation juridique d'un terrain                   │   │
│   │  • Signale les litiges ou restrictions                           │   │
│   │                                                                  │   │
│   │  📜 TITRES FONCIERS                                               │   │
│   │  • Gère les demandes de titre foncier                            │   │
│   │  • Suit les mutations de propriété                               │   │
│   │  • Délivre les certificats de propriété                          │   │
│   │                                                                  │   │
│   │  🏗️ URBANISME                                                     │   │
│   │  • Gère les demandes de permis de construire                     │   │
│   │  • Vérifie la conformité aux règles d'urbanisme                  │   │
│   │  • Suit le processus d'approbation                               │   │
│   │                                                                  │   │
│   └─────────────────────────────────────────────────────────────────┘   │
│                                                                          │
│   VERSION : V2                                                           │
│                                                                          │
└─────────────────────────────────────────────────────────────────────────┘
```

```
┌─────────────────────────────────────────────────────────────────────────┐
│                                                                          │
│   🎓 AGENT ÉDUCATION (Ministère de l'Éducation Nationale)                │
│   ───────────────────────────────────────────────────────────────────   │
│                                                                          │
│   RÔLE PRINCIPAL :                                                       │
│   Gérer les inscriptions scolaires, les diplômes et les                  │
│   attestations académiques.                                              │
│                                                                          │
│   RESPONSABILITÉS :                                                      │
│   ┌─────────────────────────────────────────────────────────────────┐   │
│   │                                                                  │   │
│   │  📚 INSCRIPTIONS SCOLAIRES                                       │   │
│   │  • Gère les inscriptions en ligne                                 │   │
│   │  • Vérifie les pièces requises                                    │   │
│   │  • Affecte les élèves aux établissements                         │   │
│   │                                                                  │   │
│   │  🎓 DIPLÔMES ET ATTESTATIONS                                      │   │
│   │  • Délivre les attestations de diplôme                            │   │
│   │  • Vérifie l'authenticité des diplômes                            │   │
│   │  • Fournit les relevés de notes                                   │   │
│   │                                                                  │   │
│   └─────────────────────────────────────────────────────────────────┘   │
│                                                                          │
│   VERSION : V3                                                           │
│                                                                          │
└─────────────────────────────────────────────────────────────────────────┘
```

---

#### 🎼 CATÉGORIE 3 : AGENTS DE COORDINATION
#### (Chefs d'orchestre de l'écosystème)

---

```
┌─────────────────────────────────────────────────────────────────────────┐
│                                                                          │
│   🎼 AGENT COORDONNATEUR                                                 │
│   ───────────────────────────────────────────────────────────────────   │
│                                                                          │
│   RÔLE PRINCIPAL :                                                       │
│   Traduire un événement de vie en une série de démarches                 │
│   coordonnées. C'est le CHEF D'ORCHESTRE de l'écosystème.               │
│                                                                          │
│   RESPONSABILITÉS :                                                      │
│   ┌─────────────────────────────────────────────────────────────────┐   │
│   │                                                                  │   │
│   │  📋 ANALYSE DE L'ÉVÉNEMENT                                       │   │
│   │  • Reçoit l'événement de vie de l'Agent Citoyen                  │   │
│   │  • Consulte sa table de correspondance                           │   │
│   │  • Identifie TOUTES les administrations concernées               │   │
│   │                                                                  │   │
│   │  🗂️ CRÉATION DES DOSSIERS                                        │   │
│   │  • Crée un dossier par administration concernée                  │   │
│   │  • Attribue un identifiant unique par dossier                    │   │
│   │  • Initialise la timeline de suivi                               │   │
│   │                                                                  │   │
│   │  🚀 ORCHESTRATION                                                 │   │
│   │  • Lance tous les agents en parallèle                            │   │
│   │  • Transmet les bons documents au bon agent                      │   │
│   │  • Suit l'avancement de chaque dossier                           │   │
│   │                                                                  │   │
│   │  📦 COLLECTE UNIQUE DES JUSTIFICATIFS                            │   │
│   │  • Applique le principe "Dites-le nous une fois"                 │   │
│   │  • Un document fourni = distribué à tous les agents concernés    │   │
│   │  • Demande les compléments UNE SEULE FOIS au citoyen             │   │
│   │                                                                  │   │
│   │  📊 CONSOLIDATION DES RÉSULTATS                                  │   │
│   │  • Attend la réponse de tous les agents                          │   │
│   │  • Consolide les résultats en un rapport unique                  │   │
│   │  • Transmet le rapport à l'Agent Notificateur                    │   │
│   │                                                                  │   │
│   └─────────────────────────────────────────────────────────────────┘   │
│                                                                          │
│   TABLE DE CORRESPONDANCE (Règles métier) :                              │
│   ┌─────────────────────────────────────────────────────────────────┐   │
│   │                                                                  │   │
│   │  ÉVÉNEMENT        →  AGENTS ACTIVÉS                              │   │
│   │  ─────────────────────────────────────────────────────────────   │   │
│   │  NAISSANCE         →  🏛️ Mairie, 🏥 CNPS, 🏥 CMU                 │   │
│   │  DÉCÈS             →  🏛️ Mairie, 🏥 CNPS (pension réversion)     │   │
│   │  MARIAGE           →  🏛️ Mairie, 🪪 ONECI (changement nom)       │   │
│   │  DÉMÉNAGEMENT      →  🏛️ Mairie, 💰 Impôts, 🪪 ONECI, 🏠 Domaine │   │
│   │  CRÉATION ENTREP.  →  🏢 CEPICI, 💰 Impôts, 🏥 CNPS              │   │
│   │  DEMANDE CNI       →  🪪 ONECI, 💰 Impôts (timbre)               │   │
│   │                                                                  │   │
│   └─────────────────────────────────────────────────────────────────┘   │
│                                                                          │
│   VERSION : MVP                                                          │
│                                                                          │
└─────────────────────────────────────────────────────────────────────────┘
```

```
┌─────────────────────────────────────────────────────────────────────────┐
│                                                                          │
│   🔔 AGENT NOTIFICATEUR (Messager)                                       │
│   ───────────────────────────────────────────────────────────────────   │
│                                                                          │
│   RÔLE PRINCIPAL :                                                       │
│   Gérer toutes les communications entre l'écosystème et                  │
│   l'utilisateur humain, via tous les canaux disponibles.                 │
│                                                                          │
│   RESPONSABILITÉS :                                                      │
│   ┌─────────────────────────────────────────────────────────────────┐   │
│   │                                                                  │   │
│   │  📱 ENVOI MULTICANAL                                              │   │
│   │  • SMS (via Twilio / Orange API / MTN API)                       │   │
│   │  • Notification Push (via Firebase Cloud Messaging)              │   │
│   │  • Email (futur)                                                  │   │
│   │  • Message in-app                                                 │   │
│   │                                                                  │   │
│   │  📝 CONSTRUCTION DES MESSAGES                                     │   │
│   │  • Reçoit les événements de l'Agent Coordonnateur                │   │
│   │  • Formate le message selon le canal                              │   │
│   │  • Personnalise avec le nom et la langue du citoyen              │   │
│   │                                                                  │   │
│   │  🎯 PRIORISATION                                                  │   │
│   │  • Messages urgents : SMS + Push immédiat                        │   │
│   │  • Messages normaux : Push + notification in-app                 │   │
│   │  • Récapitulatifs : Email (futur)                                 │   │
│   │                                                                  │   │
│   │  📊 SUIVI DES ENVOIS                                              │   │
│   │  • Vérifie que le message a bien été délivré                     │   │
│   │  • Réessaie en cas d'échec                                        │   │
│   │  • Logge toutes les communications                                │   │
│   │                                                                  │   │
│   └─────────────────────────────────────────────────────────────────┘   │
│                                                                          │
│   VERSION : MVP                                                          │
│                                                                          │
└─────────────────────────────────────────────────────────────────────────┘
```

```
┌─────────────────────────────────────────────────────────────────────────┐
│                                                                          │
│   🦮 AGENT SURVEILLANT (Chien de garde)                                  │
│   ───────────────────────────────────────────────────────────────────   │
│                                                                          │
│   RÔLE PRINCIPAL :                                                       │
│   Surveiller le respect des délais légaux, détecter les anomalies        │
│   et garantir la performance de l'écosystème.                            │
│                                                                          │
│   RESPONSABILITÉS :                                                      │
│   ┌─────────────────────────────────────────────────────────────────┐   │
│   │                                                                  │   │
│   │  ⏱️ SURVEILLANCE DES DÉLAIS                                      │   │
│   │  • Connaît les délais légaux de chaque administration            │   │
│   │  • Vérifie en continu le temps de traitement                     │   │
│   │  • Alerte si un agent dépasse le délai imparti                   │   │
│   │                                                                  │   │
│   │  🚨 DÉTECTION D'ANOMALIES                                        │   │
│   │  • Détecte les dossiers bloqués sans raison                      │   │
│   │  • Identifie les pics d'erreurs ou de rejets                     │   │
│   │  • Signale les comportements suspects (corruption)               │   │
│   │                                                                  │   │
│   │  📊 RAPPORTS DE PERFORMANCE                                       │   │
│   │  • Génère des tableaux de bord quotidiens                        │   │
│   │  • Mesure le taux de complétion, délai moyen, taux d'erreur      │   │
│   │  • Publie les statistiques (transparence)                        │   │
│   │                                                                  │   │
│   │  🔄 RELANCE AUTOMATIQUE                                           │   │
│   │  • Relance automatiquement un agent qui ne répond pas            │   │
│   │  • Escalade au superviseur humain après 3 relances              │   │
│   │  • Documente toutes les actions pour l'audit                     │   │
│   │                                                                  │   │
│   └─────────────────────────────────────────────────────────────────┘   │
│                                                                          │
│   VERSION : V1                                                           │
│                                                                          │
└─────────────────────────────────────────────────────────────────────────┘
```

---

#### ⚙️ CATÉGORIE 4 : AGENTS TECHNIQUES
#### (Infrastructure et sécurité)

---

```
┌─────────────────────────────────────────────────────────────────────────┐
│                                                                          │
│   📜 AGENT NOTAIRE (Authentificateur)                                    │
│   ───────────────────────────────────────────────────────────────────   │
│                                                                          │
│   RÔLE PRINCIPAL :                                                       │
│   Horodater, signer électroniquement et garantir l'authenticité          │
│   de chaque document et transaction de l'écosystème.                     │
│                                                                          │
│   RESPONSABILITÉS :                                                      │
│   ┌─────────────────────────────────────────────────────────────────┐   │
│   │                                                                  │   │
│   │  🖊️ SIGNATURE ÉLECTRONIQUE                                        │   │
│   │  • Appose une signature électronique sur chaque document         │   │
│   │  • Utilise un certificat reconnu légalement                      │   │
│   │  • Garantit l'intégrité du document (infalsifiable)              │   │
│   │                                                                  │   │
│   │  ⏰ HORODATAGE LÉGAL                                              │   │
│   │  • Horodate chaque action avec une source de temps fiable       │   │
│   │  • Fuseau horaire GMT (Abidjan)                                  │   │
│   │  • Fournit la preuve de date certaine                            │   │
│   │                                                                  │   │
│   │  🔗 CHAÎNE DE PREUVE                                              │   │
│   │  • Enregistre chaque transaction dans le Registre Distribué     │   │
│   │  • Crée un lien immuable entre les documents                     │   │
│   │  • Permet la vérification d'authenticité a posteriori           │   │
│   │                                                                  │   │
│   └─────────────────────────────────────────────────────────────────┘   │
│                                                                          │
│   VERSION : V3                                                           │
│                                                                          │
└─────────────────────────────────────────────────────────────────────────┘
