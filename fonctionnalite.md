
---

## LISTE COMPLÈTE DES FONCTIONNALITÉS
### Projet "e-Citoyen CI" — Écosystème Multi-Agents

---

### I. LÉGENDE DE PRIORITÉ

| Symbole | Signification |
|:-------:|---------------|
| ⭐⭐⭐ | Critique — MVP obligatoire |
| ⭐⭐ | Important — Version 1 |
| ⭐ | Secondaire — Version 2+ |
| 🔮 | Futur — Vision long terme |

---

### II. FONCTIONNALITÉS PAR MODULE

---

#### MODULE 1 : AUTHENTIFICATION & ONBOARDING

```
┌─────────────────────────────────────────────────────────────────────────┐
│                         🔐 AUTHENTIFICATION                              │
├─────────────────────────────────────────────────────────────────────────┤
│                                                                          │
│  ID    │ FONCTIONNALITÉ                              │ PRIORITÉ │ VER.  │
│ ───────┼─────────────────────────────────────────────┼──────────┼───────│
│  A-01  │ Onboarding (3 slides de présentation)       │   ⭐⭐⭐   │  MVP  │
│  A-02  │ Inscription par numéro de téléphone         │   ⭐⭐⭐   │  MVP  │
│  A-03  │ Connexion par OTP SMS (code à 6 chiffres)   │   ⭐⭐⭐   │  MVP  │
│  A-04  │ Persistance de session (JWT + AsyncStorage) │   ⭐⭐⭐   │  MVP  │
│  A-05  │ Déconnexion                                 │   ⭐⭐⭐   │  MVP  │
│  A-06  │ Renvoi du code OTP (après 60 secondes)      │   ⭐⭐    │  V1   │
│  A-07  │ Limitation des tentatives OTP (5 max)       │   ⭐⭐    │  V1   │
│  A-08  │ Connexion biométrique (empreinte / Face ID)  │   ⭐     │  V2   │
│  A-09  │ Connexion via e-Identité ONECI              │   🔮    │  V3   │
│  A-10  │ Profil utilisateur modifiable               │   ⭐⭐    │  V1   │
│  A-11  │ Photo de profil                             │   ⭐     │  V2   │
│  A-12  │ Suppression de compte                       │   ⭐     │  V2   │
│                                                                          │
└─────────────────────────────────────────────────────────────────────────┘
```

---

#### MODULE 2 : ÉVÉNEMENTS DE VIE

```
┌─────────────────────────────────────────────────────────────────────────┐
│                       📋 ÉVÉNEMENTS DE VIE                              │
├─────────────────────────────────────────────────────────────────────────┤
│                                                                          │
│  ID    │ FONCTIONNALITÉ                              │ PRIORITÉ │ VER.  │
│ ───────┼─────────────────────────────────────────────┼──────────┼───────│
│  E-01  │ Déclarer une naissance                      │   ⭐⭐⭐   │  MVP  │
│  E-02  │ Formulaire naissance (nom, date, lieu)      │   ⭐⭐⭐   │  MVP  │
│  E-03  │ Upload certificat médical (photo)           │   ⭐⭐⭐   │  MVP  │
│  E-04  │ Liste des événements disponibles            │   ⭐⭐⭐   │  MVP  │
│  E-05  │ Événements grisés "Bientôt disponible"      │   ⭐⭐⭐   │  MVP  │
│  E-06  │ Déclarer un décès                           │   ⭐⭐    │  V1   │
│  E-07  │ Déclarer un déménagement                    │   ⭐⭐    │  V1   │
│  E-08  │ Déclarer un mariage                         │   ⭐     │  V2   │
│  E-09  │ Création d'entreprise                       │   ⭐     │  V2   │
│  E-10  │ Demande de CNI / Passeport                  │   ⭐     │  V2   │
│  E-11  │ Déclaration de perte de document            │   ⭐     │  V2   │
│  E-12  │ Demande de casier judiciaire                │   🔮    │  V3   │
│  E-13  │ Demande de certificat de nationalité        │   🔮    │  V3   │
│  E-14  │ Inscription scolaire                        │   🔮    │  V3   │
│  E-15  │ Historique des événements déclarés           │   ⭐⭐    │  V1   │
│  E-16  │ Possibilité de reprendre un brouillon       │   ⭐     │  V2   │
│                                                                          │
└─────────────────────────────────────────────────────────────────────────┘
```

---

#### MODULE 3 : SUIVI DE DOSSIERS

```
┌─────────────────────────────────────────────────────────────────────────┐
│                       📊 SUIVI DE DOSSIERS                               │
├─────────────────────────────────────────────────────────────────────────┤
│                                                                          │
│  ID    │ FONCTIONNALITÉ                              │ PRIORITÉ │ VER.  │
│ ───────┼─────────────────────────────────────────────┼──────────┼───────│
│  S-01  │ Vue liste de tous mes dossiers              │   ⭐⭐⭐   │  MVP  │
│  S-02  │ Vue détaillée d'un dossier                  │   ⭐⭐⭐   │  MVP  │
│  S-03  │ Statut en temps réel (PENDING/IN_PROGRESS/  │   ⭐⭐⭐   │  MVP  │
│        │ COMPLETED/REJECTED)                         │          │       │
│  S-04  │ Timeline chronologique du dossier           │   ⭐⭐⭐   │  MVP  │
│  S-05  │ Compteur "En cours" / "Terminées"           │   ⭐⭐⭐   │  MVP  │
│  S-06  │ Code couleur par statut                     │   ⭐⭐⭐   │  MVP  │
│  S-07  │ Téléchargement document final (PDF)         │   ⭐⭐⭐   │  MVP  │
│  S-08  │ Filtrage par statut                         │   ⭐⭐    │  V1   │
│  S-09  │ Recherche dans mes dossiers                 │   ⭐     │  V2   │
│  S-10  │ Tri par date / statut / institution         │   ⭐     │  V2   │
│  S-11  │ Archivage des dossiers terminés             │   ⭐     │  V2   │
│  S-12  │ Export de l'historique (PDF récapitulatif)  │   🔮    │  V3   │
│                                                                          │
└─────────────────────────────────────────────────────────────────────────┘
```

---

#### MODULE 4 : NOTIFICATIONS

```
┌─────────────────────────────────────────────────────────────────────────┐
│                          🔔 NOTIFICATIONS                                │
├─────────────────────────────────────────────────────────────────────────┤
│                                                                          │
│  ID    │ FONCTIONNALITÉ                              │ PRIORITÉ │ VER.  │
│ ───────┼─────────────────────────────────────────────┼──────────┼───────│
│  N-01  │ SMS de confirmation de début de traitement  │   ⭐⭐⭐   │  MVP  │
│  N-02  │ SMS final "Toutes vos démarches sont prêtes"│   ⭐⭐⭐   │  MVP  │
│  N-03  │ Notification Push dans l'application        │   ⭐⭐⭐   │  MVP  │
│  N-04  │ Notification "Document complémentaire requis"│   ⭐⭐   │  V1   │
│  N-05  │ Notification "Délai dépassé, relance auto"  │   ⭐     │  V2   │
│  N-06  │ Paramètres de notifications (activer/désactiver)│ ⭐  │  V2   │
│  N-07  │ Choix du canal (SMS, Push, Email, Tous)     │   ⭐     │  V2   │
│  N-08  │ Email de récapitulatif mensuel              │   🔮    │  V3   │
│  N-09  │ Rappel "Votre document expire dans X jours" │   🔮    │  V3   │
│                                                                          │
└─────────────────────────────────────────────────────────────────────────┘
```

---

#### MODULE 5 : GESTION DES DOCUMENTS

```
┌─────────────────────────────────────────────────────────────────────────┐
│                       📄 GESTION DES DOCUMENTS                           │
├─────────────────────────────────────────────────────────────────────────┤
│                                                                          │
│  ID    │ FONCTIONNALITÉ                              │ PRIORITÉ │ VER.  │
│ ───────┼─────────────────────────────────────────────┼──────────┼───────│
│  D-01  │ Prise de photo via appareil natif           │   ⭐⭐⭐   │  MVP  │
│  D-02  │ Upload depuis la galerie                    │   ⭐⭐⭐   │  MVP  │
│  D-03  │ Aperçu du document avant envoi              │   ⭐⭐⭐   │  MVP  │
│  D-04  │ Suppression et reprise de photo             │   ⭐⭐⭐   │  MVP  │
│  D-05  │ Stockage sécurisé (MinIO / S3)              │   ⭐⭐⭐   │  MVP  │
│  D-06  │ Liste des documents fournis                 │   ⭐⭐    │  V1   │
│  D-07  │ Ajout document complémentaire demandé       │   ⭐⭐    │  V1   │
│  D-08  │ Compression automatique des images          │   ⭐     │  V2   │
│  D-09  │ Scan de document (détection des bords)      │   ⭐     │  V2   │
│  D-10  │ Support PDF en plus des images              │   ⭐     │  V2   │
│  D-11  │ Signature électronique sur document         │   🔮    │  V3   │
│  D-12  │ Vérification automatique de la qualité      │   🔮    │  V3   │
│  D-13  │ OCR (lecture automatique du texte)          │   🔮    │  V3   │
│                                                                          │
└─────────────────────────────────────────────────────────────────────────┘
```

---

#### MODULE 6 : AGENTS IA (Coordination)

```
┌─────────────────────────────────────────────────────────────────────────┐
│                       🤖 AGENTS IA                                       │
├─────────────────────────────────────────────────────────────────────────┤
│                                                                          │
│  ID    │ FONCTIONNALITÉ                              │ PRIORITÉ │ VER.  │
│ ───────┼─────────────────────────────────────────────┼──────────┼───────│
│  AG-01 │ Moteur de coordination (Événement → Démarch.)│  ⭐⭐⭐   │  MVP  │
│  AG-02 │ Agent Mairie (extrait naissance)            │   ⭐⭐⭐   │  MVP  │
│  AG-03 │ Agent CNPS (allocations familiales)         │   ⭐⭐⭐   │  MVP  │
│  AG-04 │ Agent CMU (couverture maladie)              │   ⭐⭐⭐   │  MVP  │
│  AG-05 │ Traitement parallèle des démarches          │   ⭐⭐⭐   │  MVP  │
│  AG-06 │ Agent Notificateur (SMS + Push)             │   ⭐⭐⭐   │  MVP  │
│  AG-07 │ Agent Surveillant (délais)                  │   ⭐⭐    │  V1   │
│  AG-08 │ Agent Impôts (identifiant fiscal)           │   ⭐⭐    │  V1   │
│  AG-09 │ Agent ONECI (CNI, Passeport)                │   ⭐⭐    │  V1   │
│  AG-10 │ Agent Justice (casier judiciaire)           │   ⭐     │  V2   │
│  AG-11 │ Agent Domaine (foncier)                     │   ⭐     │  V2   │
│  AG-12 │ Agent Paiement (timbre fiscal)              │   ⭐     │  V2   │
│  AG-13 │ Agent Notaire (horodatage, signature)       │   🔮    │  V3   │
│  AG-14 │ Registre Blockchain (traçabilité)           │   🔮    │  V3   │
│  AG-15 │ Mode dégradé si agent indisponible          │   ⭐⭐    │  V1   │
│  AG-16 │ Relance automatique si agent ne répond pas  │   ⭐     │  V2   │
│                                                                          │
└─────────────────────────────────────────────────────────────────────────┘
```

---

#### MODULE 7 : TABLEAU DE BORD FONCTIONNAIRE (Interface Admin)

```
┌─────────────────────────────────────────────────────────────────────────┐
│                 🧑‍💼 TABLEAU DE BORD FONCTIONNAIRE                           │
├─────────────────────────────────────────────────────────────────────────┤
│                                                                          │
│  ID    │ FONCTIONNALITÉ                              │ PRIORITÉ │ VER.  │
│ ───────┼─────────────────────────────────────────────┼──────────┼───────│
│  T-01  │ Connexion agent administratif               │   ⭐⭐    │  V1   │
│  T-02  │ Liste des dossiers à traiter                │   ⭐⭐    │  V1   │
│  T-03  │ Vue détaillée d'un dossier citoyen          │   ⭐⭐    │  V1   │
│  T-04  │ Bouton Valider / Rejeter / Demander info    │   ⭐⭐    │  V1   │
│  T-05  │ Compteur de dossiers en attente             │   ⭐⭐    │  V1   │
│  T-06  │ Filtrage par date / type / statut           │   ⭐     │  V2   │
│  T-07  │ Statistiques de traitement                  │   ⭐     │  V2   │
│  T-08  │ Export CSV / Excel des dossiers             │   ⭐     │  V2   │
│  T-09  │ Gestion des utilisateurs (création agent)   │   🔮    │  V3   │
│  T-10  │ Tableau de bord superviseur (vue globale)   │   🔮    │  V3   │
│                                                                          │
└─────────────────────────────────────────────────────────────────────────┘
```

---

#### MODULE 8 : TECHNIQUE & SÉCURITÉ

```
┌─────────────────────────────────────────────────────────────────────────┐
│                       ⚙️ TECHNIQUE & SÉCURITÉ                            │
├─────────────────────────────────────────────────────────────────────────┤
│                                                                          │
│  ID    │ FONCTIONNALITÉ                              │ PRIORITÉ │ VER.  │
│ ───────┼─────────────────────────────────────────────┼──────────┼───────│
│  T-01  │ API RESTful avec JWT                        │   ⭐⭐⭐   │  MVP  │
│  T-02  │ Validation des données côté serveur         │   ⭐⭐⭐   │  MVP  │
│  T-03  │ Stockage chiffré des documents              │   ⭐⭐⭐   │  MVP  │
│  T-04  │ HTTPS obligatoire                           │   ⭐⭐⭐   │  MVP  │
│  T-05  │ Rate limiting (anti-bruteforce)             │   ⭐⭐    │  V1   │
│  T-06  │ Logging des actions (audit trail)           │   ⭐⭐    │  V1   │
│  T-07  │ Monitoring et alertes (Sentry)              │   ⭐⭐    │  V1   │
│  T-08  │ Mode hors-ligne (saisie sans connexion)     │   ⭐     │  V2   │
│  T-09  │ Synchronisation automatique                 │   ⭐     │  V2   │
│  T-10  │ Multi-langue (Français / Anglais / Langues) │   ⭐     │  V2   │
│  T-11  │ Accessibilité (lecteur écran, contraste)    │   🔮    │  V3   │
│  T-12  │ Déploiement CI/CD automatisé                │   ⭐⭐    │  V1   │
│  T-13  │ Tests automatisés (unitaires + E2E)         │   ⭐⭐    │  V1   │
│                                                                          │
└─────────────────────────────────────────────────────────────────────────┘
```

---

#### MODULE 9 : SUPPORT & AIDE

```
┌─────────────────────────────────────────────────────────────────────────┐
│                        🆘 SUPPORT & AIDE                                 │
├─────────────────────────────────────────────────────────────────────────┤
│                                                                          │
│  ID    │ FONCTIONNALITÉ                              │ PRIORITÉ │ VER.  │
│ ───────┼─────────────────────────────────────────────┼──────────┼───────│
│  H-01  │ FAQ intégrée                                │   ⭐⭐    │  V1   │
│  H-02  │ Chatbot assistant (basique)                 │   ⭐     │  V2   │
│  H-03  │ Contact support par WhatsApp                │   ⭐⭐    │  V1   │
│  H-04  │ Tutoriel vidéo intégré                      │   ⭐     │  V2   │
│  H-05  │ Signalement d'un bug                        │   ⭐⭐    │  V1   │
│  H-06  │ Feedback après chaque démarche              │   ⭐     │  V2   │
│  H-07  │ Centre d'aide complet                       │   🔮    │  V3   │
│  H-08  │ Appel direct à un agent humain              │   🔮    │  V3   │
│                                                                          │
└─────────────────────────────────────────────────────────────────────────┘
```

---

### III. RÉSUMÉ PAR VERSION

```
┌─────────────────────────────────────────────────────────────────────────┐
│                    CONTENU DE CHAQUE VERSION                             │
├─────────────────────────────────────────────────────────────────────────┤
│                                                                          │
│  🚀 MVP (3 mois) — 25 fonctionnalités                                   │
│  ┌───────────────────────────────────────────────────────────────────┐  │
│  │ • Onboarding + Connexion OTP + Session JWT                        │  │
│  │ • Déclaration de naissance (formulaire + upload certificat)       │  │
│  │ • Suivi de dossier (statuts, timeline, compteurs)                 │  │
│  │ • 3 Agents IA : Mairie, CNPS, CMU                                │  │
│  │ • Agent Coordonnateur (parallélisation)                           │  │
│  │ • Agent Notificateur (SMS + Push)                                 │  │
│  │ • Téléchargement document final (PDF)                             │  │
│  │ • Liste des événements (avec grisés)                              │  │
│  │ • Photo via appareil natif + galerie                              │  │
│  │ • API REST sécurisée (JWT + HTTPS)                                │  │
│  └───────────────────────────────────────────────────────────────────┘  │
│                                                                          │
│  📦 VERSION 1 (3 mois supplémentaires) — 18 fonctionnalités             │
│  ┌───────────────────────────────────────────────────────────────────┐  │
│  │ • Nouveaux événements : Décès, Déménagement                       │  │
│  │ • Agent Surveillant (alertes délais)                              │  │
│  │ • Agent Impôts + Agent ONECI                                      │  │
│  │ • Tableau de bord Fonctionnaire (simple)                          │  │
│  │ • Renvoi OTP, limitation tentatives                               │  │
│  │ • Profil modifiable                                               │  │
│  │ • Filtrage dossiers                                               │  │
│  │ • Notification "Document complémentaire requis"                   │  │
│  │ • Liste des documents fournis + ajout complémentaire              │  │
│  │ • Mode dégradé, Rate limiting, CI/CD, Tests                       │  │
│  │ • FAQ intégrée, Contact WhatsApp, Signalement bug                 │  │
│  └───────────────────────────────────────────────────────────────────┘  │
│                                                                          │
│  📦 VERSION 2 (6 mois) — 25 fonctionnalités                             │
│  ┌───────────────────────────────────────────────────────────────────┐  │
│  │ • Nouveaux événements : Mariage, Création entreprise, CNI, Perte  │  │
│  │ • Agent Justice + Agent Domaine + Agent Paiement                  │  │
│  │ • Authentification biométrique                                    │  │
│  │ • Mode hors-ligne + synchronisation                               │  │
│  │ • Dashboard fonctionnaire avancé (stats, export)                  │  │
│  │ • Paramètres de notifications                                     │  │
│  │ • Compression auto, scan document                                 │  │
│  │ • Chatbot assistant                                               │  │
│  │ • Multi-langue                                                    │  │
│  │ • Archivage, recherche, tri, brouillon                            │  │
│  │ • Feedback utilisateur                                            │  │
│  └───────────────────────────────────────────────────────────────────┘  │
│                                                                          │
│  🔮 VERSION 3+ (Futur) — 15 fonctionnalités                            │
│  ┌───────────────────────────────────────────────────────────────────┐  │
│  │ • Connexion e-Identité ONECI                                      │  │
│  │ • Tous les événements (scolarité, casier, nationalité)            │  │
│  │ • Agent Notaire + Registre Blockchain                             │  │
│  │ • OCR, signature électronique                                     │  │
│  │ • Export historique PDF                                           │  │
│  │ • Centre d'aide complet, appel humain                             │  │
│  │ • Accessibilité                                                   │  │
│  │ • Dashboard superviseur                                           │  │
│  └───────────────────────────────────────────────────────────────────┘  │
│                                                                          │
└─────────────────────────────────────────────────────────────────────────┘
```

---

### IV. TOTAL DES FONCTIONNALITÉS

| Version | Nombre | Délai |
|---------|:------:|-------|
| **MVP** | 25 | 3 mois |
| **Version 1** | 18 | +3 mois |
| **Version 2** | 25 | +6 mois |
| **Version 3+** | 15 | +12 mois |
| **TOTAL** | **83** | |

---

### V. FONCTIONNALITÉS SPÉCIFIQUES À LA CÔTE D'IVOIRE

```
┌─────────────────────────────────────────────────────────────────────────┐
│           FONCTIONNALITÉS ADAPTÉES AU CONTEXTE IVOIRIEN                  │
├─────────────────────────────────────────────────────────────────────────┤
│                                                                          │
│  CI-01 │ Intégration API Orange CI / MTN / Moov pour SMS               │
│  CI-02 │ Paiement Mobile Money (Orange Money, MTN MoMo, Moov Money)    │
│  CI-03 │ Intégration future avec e-Identité ONECI                      │
│  CI-04 │ Interface en français (langue officielle)                     │
│  CI-05 │ Prochaine version : langues locales (Dioula, Baoulé, Bété)    │
│  CI-06 │ Adapté aux connexions faibles (3G, Edge)                      │
│  CI-07 │ Mode économie de données                                      │
│  CI-08 │ Fonctionne avec les anciens smartphones Android               │
│  CI-09 │ Conforme à la loi ivoirienne sur la protection des données    │
│  CI-10 │ Horodatage légal (fuseau horaire GMT, Abidjan)                │
│  CI-11 │ Formats de documents acceptés par l'administration ivoirienne │
│  CI-12 │ Partenariat avec les mairies pilotes (Plateau, Cocody...)     │
│                                                                          │
└─────────────────────────────────────────────────────────────────────────┘
```

---

