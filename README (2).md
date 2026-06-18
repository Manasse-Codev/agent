# e-Citoyen CI

**Assistant administratif intelligent pour les citoyens ivoiriens**

Projet réalisé par l'équipe **IA Force CI (Team 17)** dans le cadre du **Challenge IA 2026** — Leading Change Africa & Intro Group.

Thème : *Écosystème multi-agents pour automatiser les services administratifs publics*

---

## Le problème

En Côte d'Ivoire, accomplir une démarche administrative simple (acte de naissance, CNI, allocations CNPS, inscription CMU) prend souvent plusieurs jours et plusieurs déplacements, car :

- le citoyen ne sait pas quels documents rassembler
- les procédures changent selon les situations (acte perdu, naissance hors mariage, etc.)
- l'information est dispersée entre administrations qui ne communiquent pas entre elles
- chaque guichet demande des justificatifs que l'État possède déjà ailleurs

Un événement de vie simple, comme la naissance d'un enfant, déclenche en réalité **trois démarches séparées** (Mairie, CNPS, CMU), que le citoyen doit aujourd'hui gérer seul, guichet par guichet.

## La solution

e-Citoyen CI est un assistant conversationnel qui comprend la situation d'un citoyen en langage naturel, identifie automatiquement les démarches concernées, et produit un plan d'action complet et personnalisé — y compris pour des cas particuliers que des règles fixes ne couvriraient pas (document perdu, situation familiale atypique, etc.).

Le système repose sur une **architecture multi-agents** : plusieurs agents IA spécialisés collaborent, chacun avec un rôle précis, plutôt qu'un seul modèle généraliste qui répond de façon approximative à tout.

### Exemple

```
Citoyen : "Mon enfant est né hier à Anyama, mais je n'ai pas
           encore d'acte de mariage avec le père"

→ Agent Accueil      : identifie un cas complexe (naissance + 
                        reconnaissance paternelle à traiter séparément)
→ Agent Documentaliste : récupère les procédures exactes pour 
                        chaque démarche concernée
→ Agent Rédacteur     : génère un plan clair, les délais, les lieux,
                        et une lettre de déclaration prête à imprimer
```

## Architecture

```
┌──────────────┐     ┌──────────────┐
│   Web App    │     │  Mobile App  │
│ (FastShorts) │     │ (FastShorts) │
└──────┬───────┘     └──────┬───────┘
       │                    │
       └─────────┬──────────┘
                  │  API REST
                  ▼
       ┌─────────────────────┐
       │   Backend FastAPI    │
       └──────────┬───────────┘
                  │
                  ▼
   ┌──────────────────────────────┐
   │   Orchestration CrewAI        │
   │                                │
   │  Agent Accueil                │
   │       │                       │
   │       ▼                       │
   │  Agent Documentaliste         │
   │       │                       │
   │       ▼                       │
   │  Agent Rédacteur              │
   └──────────────┬─────────────────┘
                  │
                  ▼
       ┌─────────────────────┐
       │  Base de connaissances│
       │  (procédures CI -     │
       │   JSON / SQLite)       │
       └─────────────────────┘
                  │
                  ▼
       ┌─────────────────────┐
       │   Groq (llama-3.3-     │
       │   70b-versatile)        │
       └─────────────────────┘
```

### Les 3 agents

| Agent | Rôle |
|---|---|
| **Agent Accueil** | Comprend la demande du citoyen, même formulée de façon imprécise ou avec des complications imprévues, et identifie l'événement de vie concerné |
| **Agent Documentaliste** | Interroge la base de connaissances des procédures administratives ivoiriennes et détermine les documents, délais et bureaux compétents pour chaque démarche identifiée |
| **Agent Rédacteur** | Compile une réponse claire et personnalisée pour le citoyen, et génère si besoin un courrier ou une liste prête à utiliser |

## Stack technique

| Composant | Technologie | Notes |
|---|---|---|
| Backend & agents IA | Python 3.12, CrewAI, FastAPI | Code écrit et maîtrisé par l'équipe |
| LLM | Groq — llama-3.3-70b-versatile | Gratuit, rapide, adapté à une démo live |
| Base de connaissances | JSON / SQLite | Procédures administratives ivoiriennes réelles |
| Interface Web | FastShorts (vibe coding) | Consomme l'API backend |
| Application mobile | FastShorts — React Native / Expo | Imposé par les organisateurs du Challenge |
| Gestion de version | GitHub | Dépôt partagé avec le mentor, commits réguliers |

## Périmètre du MVP

Le MVP se concentre sur **un scénario de vie traité de bout en bout** plutôt que sur une couverture large et superficielle :

- **Scénario principal** : naissance d'un enfant (Mairie, CNPS, CMU)
- **Scénario secondaire** (si le temps le permet) : demande de carte nationale d'identité

Volontairement exclus du MVP : connexions à de vraies API gouvernementales, paiement Mobile Money, signature électronique, blockchain/traçabilité, authentification biométrique. Ces éléments relèvent d'une vision long terme du projet, pas d'une démonstration en 2 semaines.

## Équipe — IA Force CI (Team 17)

| Membre | Rôle |
|---|---|
| Morel Assamoi | Chef d'équipe — architecture, coordination, lien mentor |
| Manassé | Responsable technique — agents CrewAI, backend FastAPI |
| Fahisol | Responsable communication — interfaces FastShorts (web & mobile), daily updates |
| Béni | Responsable projet — GitHub, base de connaissances, organisation des tâches |
| Joran | Responsable recherche — collecte des procédures administratives réelles |

## Calendrier

- **Développement** : 2 semaines (15–28 juin 2026)
- **Pitch final & évaluation** : 29 juin – 12 juillet 2026

## Critères d'évaluation visés

Solution proposée · Usage pertinent de l'IA · Innovation · Faisabilité SMART · Impact potentiel · Qualité du pitch

---

*Challenge IA 2026 — Leading Change Africa & Intro Group*
