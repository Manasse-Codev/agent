

## MVP : Écosystème Multi-Agents pour Services Administratifs
### Nom de code : *"e-Citoyen CI"*
### Stack Mobile : React Native

---

### I. Pourquoi React Native pour ce projet ?

| Avantage | Bénéfice pour le MVP |
|----------|----------------------|
| **Un seul codebase** | Déploiement simultané Android + iOS |
| **Grande communauté** | Nombreuses librairies prêtes (caméra, stockage, notifications) |
| **Performance proche du natif** | Fluidité pour l'upload de documents et le suivi en temps réel |
| **Hot Reload** | Développement plus rapide, itérations fréquentes |
| **Coût réduit** | Un seul développeur mobile au lieu de deux (Android + iOS) |

---

### II. Architecture Technique Complète (React Native)

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                                                                              │
│   ┌──────────────────────────────────────────────────────────────────────┐  │
│   │                  📱 APPLICATION MOBILE (React Native)                  │  │
│   │                                                                       │  │
│   │  ┌──────────────┐  ┌──────────────┐  ┌──────────────┐               │  │
│   │  │ Écrans & UI  │  │ Gestion      │  │ Stockage     │               │  │
│   │  │              │  │ d'État       │  │ Local        │               │  │
│   │  │ React        │  │ Redux Toolkit│  │ AsyncStorage │               │  │
│   │  │ Navigation   │  │              │  │              │               │  │
│   │  └──────────────┘  └──────────────┘  └──────────────┘               │  │
│   │                                                                       │  │
│   │  ┌──────────────┐  ┌──────────────┐  ┌──────────────┐               │  │
│   │  │ Appareil     │  │ Notifications│  │ Connexion    │               │  │
│   │  │ Photo        │  │ Push         │  │ Réseau       │               │  │
│   │  │              │  │              │  │              │               │  │
│   │  │ react-native │  │ Firebase     │  │ Axios        │               │  │
│   │  │ -camera      │  │ Cloud Msg    │  │              │               │  │
│   │  └──────────────┘  └──────────────┘  └──────────────┘               │  │
│   │                                                                       │  │
│   └────────────────────────────────┬──────────────────────────────────────┘  │
│                                    │ API REST (HTTPS)                         │
│                                    ▼                                          │
│   ┌──────────────────────────────────────────────────────────────────────┐  │
│   │                    🔧 BACKEND (Node.js / Express)                     │  │
│   │                                                                       │  │
│   │  ┌───────────────┐  ┌────────────────────┐  ┌────────────────────┐   │  │
│   │  │ 🔐 Auth        │  │ 🎼 Moteur de       │  │ 🔔 Service         │   │  │
│   │  │ JWT + OTP SMS  │  │ Coordination       │  │ Notification       │   │  │
│   │  │               │  │ (Event → Démarches) │  │ (SMS + Push)       │   │  │
│   │  └───────────────┘  └────────────────────┘  └────────────────────┘   │  │
│   │                                                                       │  │
│   │  ┌───────────────┐  ┌────────────────────┐  ┌────────────────────┐   │  │
│   │  │ 📂 Upload     │  │ 📦 Base de Données │  │ 🔄 File d'attente  │   │  │
│   │  │ Documents     │  │ PostgreSQL         │  │ asynchrone         │   │  │
│   │  │ Multer + S3   │  │ + Prisma ORM       │  │ BullMQ + Redis     │   │  │
│   │  └───────────────┘  └────────────────────┘  └────────────────────┘   │  │
│   │                                                                       │  │
│   └────────────────────────────────┬──────────────────────────────────────┘  │
│                                    │ API REST                                 │
│                                    ▼                                          │
│   ┌──────────────────────────────────────────────────────────────────────┐  │
│   │              🏛️ SIMULATEURS D'AGENTS INSTITUTIONNELS                 │  │
│   │                                                                       │  │
│   │  ┌──────────────────┐  ┌──────────────────┐  ┌──────────────────┐    │  │
│   │  │ 🏛️ MAIRIE         │  │ 🏥 CNPS           │  │ 🏥 CMU            │    │  │
│   │  │ Simulateur       │  │ Simulateur       │  │ Simulateur       │    │  │
│   │  ├──────────────────┤  ├──────────────────┤  ├──────────────────┤    │  │
│   │  │ POST /naissance  │  │ POST /allocations│  │ POST /inscription│    │  │
│   │  │ → statut: reçu   │  │ → statut: reçu   │  │ → statut: reçu   │    │  │
│   │  │ → délai: 24h     │  │ → délai: 48h     │  │ → délai: 24h     │    │  │
│   │  └──────────────────┘  └──────────────────┘  └──────────────────┘    │  │
│   │                                                                       │  │
│   └──────────────────────────────────────────────────────────────────────┘  │
│                                                                              │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

### III. Stack Technique Détaillée

| Couche | Technologie | Justification |
|--------|-------------|---------------|
| **Mobile** | React Native 0.76+ | Cross-platform, composants riches |
| **Navigation** | React Navigation 6 | Stack + Tab navigator |
| **État global** | Redux Toolkit | Centralisation des données utilisateur et démarches |
| **Stockage local** | AsyncStorage + MMKV | Token JWT, données hors-ligne |
| **Appareil photo** | react-native-vision-camera | Prise de photo documents, haute qualité |
| **Notifications Push** | Firebase Cloud Messaging | Notifications temps réel, compatible iOS/Android |
| **HTTP Client** | Axios | Intercepteurs pour tokens, retry automatique |
| **Backend API** | Node.js + Express.js | Rapide, asynchrone, écosystème riche |
| **Base de données** | PostgreSQL + Prisma ORM | Relationnel, typé, migrations faciles |
| **File d'attente** | BullMQ + Redis | Traitement asynchrone des démarches |
| **Upload fichiers** | Multer + MinIO (S3 compatible) | Stockage des documents (certificats, photos) |
| **SMS** | API Orange CI ou Twilio | Notification SMS aux citoyens |
| **Authentification** | JWT + OTP SMS | Sans mot de passe, adapté au contexte mobile |
| **Simulateurs** | Express.js (endpoints REST) | Simule les API des administrations |
| **Déploiement** | Docker + Docker Compose | Reproductible, facile à déployer |

---

### IV. Structure des Dossiers du Projet

```
e-citoyen-ci/
│
├── 📱 mobile/                          # Application React Native
│   ├── src/
│   │   ├── components/                 # Composants réutilisables
│   │   │   ├── Button.tsx
│   │   │   ├── DocumentUploader.tsx    # Prise photo + upload
│   │   │   ├── StatusBadge.tsx         # Badge statut (en cours, ok, erreur)
│   │   │   ├── Timeline.tsx            # Suivi chronologique
│   │   │   └── EventCard.tsx           # Carte événement de vie
│   │   │
│   │   ├── screens/                    # Écrans de l'application
│   │   │   ├── OnboardingScreen.tsx    # Présentation au 1er lancement
│   │   │   ├── LoginScreen.tsx         # Connexion OTP SMS
│   │   │   ├── HomeScreen.tsx          # Tableau de bord
│   │   │   ├── NewEventScreen.tsx      # Déclarer un événement
│   │   │   ├── EventDetailScreen.tsx   # Suivi d'un dossier
│   │   │   └── ProfileScreen.tsx       # Profil citoyen
│   │   │
│   │   ├── store/                      # Redux Toolkit
│   │   │   ├── index.ts
│   │   │   ├── slices/
│   │   │   │   ├── authSlice.ts
│   │   │   │   ├── citizenSlice.ts
│   │   │   │   └── dossierSlice.ts
│   │   │   └── api/
│   │   │       └── eCitoyenApi.ts      # RTK Query (appels API)
│   │   │
│   │   ├── navigation/
│   │   │   └── AppNavigator.tsx
│   │   │
│   │   ├── services/
│   │   │   ├── api.ts                  # Configuration Axios
│   │   │   ├── notifications.ts        # Firebase Cloud Messaging
│   │   │   └── storage.ts             # AsyncStorage helpers
│   │   │
│   │   └── utils/
│   │       ├── constants.ts
│   │       └── types.ts                # Types TypeScript
│   │
│   ├── App.tsx
│   ├── package.json
│   └── tsconfig.json
│
├── 🔧 backend/                         # Serveur Node.js
│   ├── src/
│   │   ├── controllers/
│   │   │   ├── authController.ts
│   │   │   ├── citizenController.ts
│   │   │   ├── eventController.ts
│   │   │   └── dossierController.ts
│   │   │
│   │   ├── services/
│   │   │   ├── coordinationEngine.ts   # 🎼 Moteur de coordination
│   │   │   ├── smsService.ts
│   │   │   ├── uploadService.ts
│   │   │   └── institutionAdapters/    # Adaptateurs pour simulateurs
│   │   │       ├── mairieAdapter.ts
│   │   │       ├── cnpsAdapter.ts
│   │   │       └── cmuAdapter.ts
│   │   │
│   │   ├── models/
│   │   │   └── prisma/                 # Schéma Prisma
│   │   │       └── schema.prisma
│   │   │
│   │   ├── middleware/
│   │   │   ├── auth.ts
│   │   │   └── upload.ts
│   │   │
│   │   ├── routes/
│   │   │   └── index.ts
│   │   │
│   │   ├── queue/                      # BullMQ
│   │   │   ├── dossierQueue.ts
│   │   │   └── workers/
│   │   │       └── processDossier.ts
│   │   │
│   │   └── app.ts
│   │
│   ├── package.json
│   └── tsconfig.json
│
├── 🏛️ simulators/                      # Simulateurs institutionnels
│   ├── mairie/
│   │   ├── index.js
│   │   └── package.json
│   ├── cnps/
│   │   ├── index.js
│   │   └── package.json
│   └── cmu/
│       ├── index.js
│       └── package.json
│
├── docker-compose.yml                  # PostgreSQL + Redis + MinIO + Backend
├── .env.example
└── README.md
```

---

### V. Dépendances React Native (package.json)

```json
{
  "name": "e-citoyen-ci-mobile",
  "version": "1.0.0-mvp",
  "dependencies": {
    "react": "18.3.1",
    "react-native": "0.76.x",
    
    "@react-navigation/native": "^6.x",
    "@react-navigation/stack": "^6.x",
    "@react-navigation/bottom-tabs": "^6.x",
    
    "@reduxjs/toolkit": "^2.x",
    "react-redux": "^9.x",
    
    "axios": "^1.7.x",
    "react-native-vision-camera": "^4.x",
    "@react-native-firebase/app": "^20.x",
    "@react-native-firebase/messaging": "^20.x",
    "@react-native-async-storage/async-storage": "^2.x",
    "react-native-mmkv": "^3.x",
    "react-native-document-picker": "^9.x",
    "react-native-image-picker": "^7.x",
    "react-native-toast-message": "^2.x",
    "lottie-react-native": "^7.x"
  },
  "devDependencies": {
    "typescript": "^5.x",
    "@types/react": "^18.x",
    "@types/react-native": "^0.76.x"
  }
}
```

---

### VI. Schéma de Base de Données (Prisma)

```prisma
// backend/src/models/prisma/schema.prisma

model Citizen {
  id          String    @id @default(uuid())
  phone       String    @unique
  firstName   String
  lastName    String
  cniNumber   String?   @unique
  createdAt   DateTime  @default(now())
  dossiers    Dossier[]
}

model LifeEvent {
  id          String    @id @default(uuid())
  type        EventType
  citizenId   String
  citizen     Citizen   @relation(fields: [citizenId], references: [id])
  metadata    Json      // { childName, birthDate, birthPlace, ... }
  documents   Document[]
  dossiers    Dossier[]
  createdAt   DateTime  @default(now())
}

model Dossier {
  id            String        @id @default(uuid())
  lifeEventId   String
  lifeEvent     LifeEvent     @relation(fields: [lifeEventId], references: [id])
  institution   InstitutionType
  externalRef   String?       // Référence chez l'institution simulée
  status        DossierStatus @default(PENDING)
  timeline      Timeline[]
  createdAt     DateTime      @default(now())
  updatedAt     DateTime      @updatedAt
}

model Document {
  id          String    @id @default(uuid())
  lifeEventId String
  lifeEvent   LifeEvent @relation(fields: [lifeEventId], references: [id])
  type        String    // "certificat_medical", "justificatif_domicile"
  url         String    // URL MinIO
  createdAt   DateTime  @default(now())
}

model Timeline {
  id        String   @id @default(uuid())
  dossierId String
  dossier   Dossier  @relation(fields: [dossierId], references: [id])
  status    DossierStatus
  message   String
  createdAt DateTime @default(now())
}

enum EventType {
  NAISSANCE
}

enum InstitutionType {
  MAIRIE
  CNPS
  CMU
}

enum DossierStatus {
  PENDING
  IN_PROGRESS
  COMPLETED
  REJECTED
}
```

---

### VII. Moteur de Coordination (Code Simplifié)

```typescript
// backend/src/services/coordinationEngine.ts

interface LifeEventInput {
  type: 'NAISSANCE';
  citizenId: string;
  metadata: {
    childName: string;
    birthDate: string;
    birthPlace: string;
    hospital: string;
  };
}

interface DossierConfig {
  institution: 'MAIRIE' | 'CNPS' | 'CMU';
  description: string;
  requiredDocuments: string[];
}

// 🎼 Configuration : un événement → N démarches
const EVENT_CONFIG: Record<string, DossierConfig[]> = {
  NAISSANCE: [
    {
      institution: 'MAIRIE',
      description: 'Déclaration de naissance - Extrait d\'acte de naissance',
      requiredDocuments: ['certificat_medical'],
    },
    {
      institution: 'CNPS',
      description: 'Demande d\'allocations familiales',
      requiredDocuments: ['certificat_medical', 'extrait_naissance'],
    },
    {
      institution: 'CMU',
      description: 'Inscription du nouveau-né à la Couverture Maladie Universelle',
      requiredDocuments: ['certificat_medical', 'extrait_naissance'],
    },
  ],
};

export class CoordinationEngine {
  
  /**
   * Point d'entrée principal : le citoyen déclare un événement
   * Retourne la liste des dossiers créés
   */
  async processLifeEvent(input: LifeEventInput): Promise<Dossier[]> {
    const configs = EVENT_CONFIG[input.type];
    
    if (!configs) {
      throw new Error(`Événement inconnu : ${input.type}`);
    }
    
    console.log(`🎼 Coordination : ${configs.length} démarches identifiées`);
    
    // Créer les dossiers en parallèle
    const dossiers = await Promise.all(
      configs.map(config => this.createDossier(input, config))
    );
    
    // Ajouter à la file d'attente pour traitement asynchrone
    for (const dossier of dossiers) {
      await dossierQueue.add('process-dossier', {
        dossierId: dossier.id,
        institution: dossier.institution,
      });
    }
    
    return dossiers;
  }
  
  private async createDossier(input: LifeEventInput, config: DossierConfig): Promise<Dossier> {
    return prisma.dossier.create({
      data: {
        lifeEventId: input.lifeEventId,
        institution: config.institution,
        status: 'PENDING',
        timeline: {
          create: {
            status: 'PENDING',
            message: `Dossier créé : ${config.description}`,
          },
        },
      },
    });
  }
}
```

---

### VIII. Code d'un Simulateur (Mairie)

```javascript
// simulators/mairie/index.js
const express = require('express');
const app = express();
app.use(express.json());

// Simule le traitement d'une déclaration de naissance
app.post('/api/mairie/naissance', (req, res) => {
  const { childName, birthDate, birthPlace, documents } = req.body;
  
  console.log(`🏛️ [MAIRIE] Réception déclaration naissance : ${childName}`);
  
  // Réponse immédiate : accusé de réception
  res.json({
    success: true,
    externalRef: `MAIRIE-${Date.now()}`,
    status: 'RECEIVED',
    message: 'Déclaration de naissance enregistrée',
    estimatedDelay: '24h',
  });
  
  // Simulation : après 10 secondes, le dossier est traité
  setTimeout(() => {
    console.log(`🏛️ [MAIRIE] ✅ Extrait de naissance prêt pour ${childName}`);
    // Dans la vraie vie, on appellerait un webhook vers le backend
  }, 10000); // 10 secondes pour la démo (24h en production)
});

app.get('/api/mairie/status/:externalRef', (req, res) => {
  res.json({
    externalRef: req.params.externalRef,
    status: 'COMPLETED',
    result: { documentUrl: 'https://minio.local/extraits/xxx.pdf' },
  });
});

app.listen(3001, () => console.log('🏛️ Simulateur Mairie sur port 3001'));
```

---

### IX. Écran Mobile Principal (React Native)

```tsx
// mobile/src/screens/HomeScreen.tsx
import React from 'react';
import {
  View,
  Text,
  TouchableOpacity,
  FlatList,
  StyleSheet,
} from 'react-native';
import { useSelector } from 'react-redux';
import { useNavigation } from '@react-navigation/native';

const LIFE_EVENTS = [
  {
    id: 'naissance',
    icon: '👶',
    title: 'Naissance d\'un enfant',
    description: 'Déclaration, allocations, CMU',
    color: '#4CAF50',
  },
  // Autres événements grisés (à venir)
  {
    id: 'deces',
    icon: '🕊️',
    title: 'Décès d\'un proche',
    description: 'Bientôt disponible',
    color: '#9E9E9E',
    disabled: true,
  },
  {
    id: 'demenagement',
    icon: '📦',
    title: 'Déménagement',
    description: 'Bientôt disponible',
    color: '#9E9E9E',
    disabled: true,
  },
];

export default function HomeScreen() {
  const navigation = useNavigation();
  const dossiers = useSelector(state => state.dossier.items);
  
  const enCours = dossiers.filter(d => d.status !== 'COMPLETED').length;
  
  return (
    <View style={styles.container}>
      {/* En-tête */}
      <Text style={styles.greeting}>Bonjour, Koffi 👋</Text>
      <Text style={styles.subtitle}>Que voulez-vous faire aujourd'hui ?</Text>
      
      {/* Compteurs */}
      <View style={styles.counters}>
        <View style={styles.counterBadge}>
          <Text style={styles.counterNumber}>{enCours}</Text>
          <Text style={styles.counterLabel}>En cours</Text>
        </View>
        <View style={styles.counterBadge}>
          <Text style={styles.counterNumber}>
            {dossiers.filter(d => d.status === 'COMPLETED').length}
          </Text>
          <Text style={styles.counterLabel}>Terminées</Text>
        </View>
      </View>
      
      {/* Événements de vie */}
      <Text style={styles.sectionTitle}>Déclarer un événement</Text>
      <FlatList
        data={LIFE_EVENTS}
        keyExtractor={item => item.id}
        renderItem={({ item }) => (
          <TouchableOpacity
            style={[styles.eventCard, { borderLeftColor: item.color }]}
            disabled={item.disabled}
            onPress={() => navigation.navigate('NewEvent', { type: item.id })}
          >
            <Text style={styles.eventIcon}>{item.icon}</Text>
            <View style={styles.eventInfo}>
              <Text style={[
                styles.eventTitle,
                item.disabled && { color: '#9E9E9E' }
              ]}>
                {item.title}
              </Text>
              <Text style={styles.eventDescription}>{item.description}</Text>
            </View>
            <Text style={styles.arrow}>→</Text>
          </TouchableOpacity>
        )}
      />
      
      {/* Mes dossiers récents */}
      <Text style={styles.sectionTitle}>Mes dossiers récents</Text>
      {dossiers.length === 0 ? (
        <Text style={styles.emptyText}>Aucun dossier pour le moment</Text>
      ) : (
        <FlatList
          data={dossiers.slice(0, 3)}
          keyExtractor={item => item.id}
          renderItem={({ item }) => (
            <TouchableOpacity
              style={styles.dossierItem}
              onPress={() => navigation.navigate('DossierDetail', { id: item.id })}
            >
              <StatusBadge status={item.status} />
              <Text>{item.institution}</Text>
              <Text>{new Date(item.createdAt).toLocaleDateString()}</Text>
            </TouchableOpacity>
          )}
        />
      )}
    </View>
  );
}
```

---

### X. Docker Compose (Environnement de Développement)

```yaml
# docker-compose.yml
version: '3.8'

services:
  postgres:
    image: postgres:16-alpine
    environment:
      POSTGRES_DB: ecitoyen
      POSTGRES_USER: ecitoyen
      POSTGRES_PASSWORD: mvp2024
    ports:
      - "5432:5432"
    volumes:
      - pgdata:/var/lib/postgresql/data

  redis:
    image: redis:7-alpine
    ports:
      - "6379:6379"

  minio:
    image: minio/minio:latest
    command: server /data --console-address ":9001"
    environment:
      MINIO_ROOT_USER: minioadmin
      MINIO_ROOT_PASSWORD: minioadmin
    ports:
      - "9000:9000"
      - "9001:9001"
    volumes:
      - minio_data:/data

  backend:
    build: ./backend
    ports:
      - "3000:3000"
    environment:
      DATABASE_URL: postgresql://ecitoyen:mvp2024@postgres:5432/ecitoyen
      REDIS_URL: redis://redis:6379
      MINIO_ENDPOINT: minio
      MINIO_PORT: 9000
      JWT_SECRET: mvp-secret-key
    depends_on:
      - postgres
      - redis
      - minio

  mairie-simulator:
    build: ./simulators/mairie
    ports:
      - "3001:3001"

  cnps-simulator:
    build: ./simulators/cnps
    ports:
      - "3002:3002"

  cmu-simulator:
    build: ./simulators/cmu
    ports:
      - "3003:3003"

volumes:
  pgdata:
  minio_data:
```

---

### XI. Récapitulatif : Ce Que le MVP Livre

| Livrable | Contenu |
|----------|---------|
| **📱 APK Android** | Application React Native fonctionnelle |
| **🍎 App iOS (optionnel)** | Même codebase, build iOS si besoin |
| **🔧 Backend** | API REST avec coordination, files d'attente, upload |
| **🗄️ Base de données** | PostgreSQL avec schéma Prisma |
| **🏛️ 3 Simulateurs** | Mairie, CNPS, CMU (endpoints REST) |
| **📖 Documentation** | Guide d'installation, manuel utilisateur, spécifications API |
| **🐳 Docker Compose** | Lancement complet en une commande |

---

### XII. Prochaines Étapes (Roadmap Post-MVP)

```
MVP (React Native + 3 simulateurs)
│
├──▶ Sprint 5 : Ajouter événement "Déménagement"
│    → Agent Impôts, Agent ONECI
│
├──▶ Sprint 6 : Mode hors-ligne
│    → Saisie sans connexion, synchronisation automatique
│
├──▶ Sprint 7 : Authentification biométrique
│    → Empreinte digitale / Face ID
│
├──▶ Sprint 8 : Dashboard fonctionnaire
│    → Interface web pour les agents publics
│
└──▶ Sprint 9+ : Connexion API réelles
     → Remplacer simulateurs par vraies API (quand disponibles)
```

