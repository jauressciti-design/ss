# LumniX - DiasporaConnect

<p align="center">
  <img src="https://img.shields.io/badge/MIABE-Hackathon%202026-orange" alt="MIABE 2026">
  <img src="https://img.shields.io/badge/Blockchain-Polygon-blue" alt="Polygon">
  <img src="https://img.shields.io/badge/Status-En%20ligne-brightgreen" alt="En ligne">
  <img src="https://img.shields.io/badge/License-MIT-green" alt="License">
</p>

<p align="center">
  <strong>Plateforme de transfert d'argent blockchain pour la diaspora africaine vers le Benin</strong><br/>
  Frais reduits a 0.8% | Reception en moins de 30 minutes | PWA installable
</p>

---

## Liens de deploiement (Production)

| Service | URL | Status |
|---------|-----|--------|
| **Landing Page** | [deploy-landing-xwspoghs.devinapps.com](https://deploy-landing-xwspoghs.devinapps.com) | En ligne |
| **Application PWA** | [deploy-pwa-jidihhbo.devinapps.com](https://deploy-pwa-jidihhbo.devinapps.com) | En ligne |
| **Backend API** | [0c643afbf900-tunnel-yamugwtu.devinapps.com](https://user:d10b00d279fa413f36617173530f37dd@0c643afbf900-tunnel-yamugwtu.devinapps.com/api/health) | En ligne |
| **Presentation Jury** | [presentation-yxgdjfmm.devinapps.com](https://presentation-yxgdjfmm.devinapps.com) | En ligne |
| **Base de donnees** | Neon.tech PostgreSQL | Connectee |
| **Repo GitHub** | [github.com/jauressciti-design/ss](https://github.com/jauressciti-design/ss) | Actif |
| **PR principale** | [Pull Request #2](https://github.com/jauressciti-design/ss/pull/2) | Ouverte |

---

## Description

**DiasporaConnect** est une plateforme innovante de transfert de fonds internationaux construite sur la blockchain Polygon, permettant a la diaspora africaine d'envoyer de l'argent vers le Benin avec des frais reduits a **0.8%** et une reception en Mobile Money (MTN MoMo, Moov Money) en moins de 30 minutes.

Le projet est developpe par l'equipe **LumniX** dans le cadre du **MIABE Hackathon 2026**.

---

## Fonctionnalites Principales

### Portail Diaspora (Expediteurs)
- **Authentification sans mot de passe** par OTP SMS cryptographique
- **Calcul automatique des frais** et conversion en temps reel (USD, EUR, GBP, CAD vers XOF)
- **Transfert securise** via smart contract Polygon
- **Suivi en temps reel** avec ID de transaction unique
- **Historique des transferts** avec details complets

### Portail Benin (Beneficiaires)
- **Recherche de transfert** par telephone ou ID de transaction
- **Retrait en Mobile Money** (MTN MoMo / Moov Money)
- **Paiement de factures** : SBEE (electricite), SONEB (eau), MTN (mobile), Canal+ (TV)
- **Paiement marchand** par QR Code sans frais
- **Solde disponible** et historique des operations

### Points Forts
- **Frais quasi nuls** : 0.8% contre 7-15% chez Western Union / MoneyGram
- **Rapidite** : Moins de 30 minutes de bout en bout
- **Securite** : Chiffrement AES-256 + blockchain Polygon + OTP cryptographique
- **PWA** : Installable sur mobile, fonctionne hors ligne via Service Worker
- **Pas de compte requis** : Authentification par numero de telephone uniquement

---

## Architecture Technique

### Frontend
| Technologie | Usage |
|-------------|-------|
| HTML5 / CSS3 / JavaScript | Interface utilisateur |
| Lucide Icons | Iconographie |
| GSAP + ScrollTrigger | Animations landing page |
| Service Worker | Mode hors ligne PWA |
| Design responsive | Mobile-first |

### Backend
| Technologie | Usage |
|-------------|-------|
| Node.js + Express.js | Serveur API REST |
| Prisma ORM | Acces base de donnees |
| PostgreSQL (Neon.tech) | Base de donnees production |
| JSON Web Tokens (JWT) | Authentification |
| crypto (Node.js) | Generation OTP securise |

### Blockchain
| Technologie | Usage |
|-------------|-------|
| Solidity | Smart Contracts |
| Polygon Amoy Testnet | Reseau blockchain |
| Hardhat | Dev, test, deploiement |
| ethers.js | Interaction blockchain |

### Infrastructure
| Service | Plateforme |
|---------|-----------|
| Landing Page | Devin Apps (CDN statique) |
| Application PWA | Devin Apps (CDN statique) |
| Backend API | Devin Apps (tunnel Node.js) |
| Base de donnees | Neon.tech (PostgreSQL cloud) |
| Presentation | Devin Apps (CDN statique) |

---

## Endpoints API

| Methode | Route | Description |
|---------|-------|-------------|
| GET | `/api/health` | Health check du serveur |
| GET | `/api/rates` | Taux de change en temps reel (EUR/USD/GBP/CAD vers XOF) |
| POST | `/api/auth/register` | Inscription / Connexion par OTP |
| POST | `/api/auth/verify-otp` | Verification du code OTP et generation JWT |
| POST | `/api/transfer` | Initier un transfert d'argent |
| POST | `/api/withdraw` | Retirer des fonds en Mobile Money |
| GET | `/api/transactions` | Historique des transferts |

### Exemples d'appels API

```bash
# Health check
curl https://user:d10b00d279fa413f36617173530f37dd@0c643afbf900-tunnel-yamugwtu.devinapps.com/api/health

# Taux de change
curl https://user:d10b00d279fa413f36617173530f37dd@0c643afbf900-tunnel-yamugwtu.devinapps.com/api/rates

# Inscription OTP
curl -X POST https://user:d10b00d279fa413f36617173530f37dd@0c643afbf900-tunnel-yamugwtu.devinapps.com/api/auth/register \
  -H "Content-Type: application/json" \
  -d '{"phone":"+22997000000","name":"Aminata Diallo"}'
```

### Reponses API

```json
// GET /api/health
{"status":"ok","service":"DiasporaConnect API","version":"1.0.0","timestamp":"2026-05-14T17:55:19.757Z"}

// GET /api/rates
{"eurToUsdc":1.08,"usdcToXof":605,"eurToXof":655.95,"updatedAt":"2026-05-14T17:55:26.976Z"}

// POST /api/auth/register
{"message":"OTP envoye","phone":"+22997000000"}
```

---

## Structure du Projet

```
ss/
├── index.html                  # Landing page principale
├── styles.css                  # Styles CSS landing page
├── script.js                   # Logique JavaScript landing page
├── app.html                    # Application PWA (2 portails)
├── app-styles.css              # Styles CSS application
├── app-script.js               # Logique JavaScript application
├── manifest.json               # Manifeste PWA
├── sw.js                       # Service Worker PWA
├── presentation.html           # Slides de presentation jury (12 slides)
├── PRESENTATION_JURY.md        # Dossier ecrit pour le jury
├── API_FRONTEND_DOCS.md        # Documentation API frontend
├── README.md                   # Ce fichier
│
├── backend/                    # Serveur Node.js
│   ├── src/
│   │   ├── index.js            # Point d'entree serveur
│   │   ├── prismaClient.js     # Client Prisma
│   │   ├── middleware/
│   │   │   └── auth.js         # Middleware JWT
│   │   ├── routes/
│   │   │   ├── auth.js         # Routes inscription/OTP
│   │   │   ├── transfer.js     # Routes transferts
│   │   │   ├── withdraw.js     # Routes retraits
│   │   │   ├── rates.js        # Routes taux de change
│   │   │   └── transactions.js # Routes historique
│   │   └── services/
│   │       ├── blockchain.js   # Interactions Polygon
│   │       ├── coingecko.js    # API taux de change
│   │       └── twilio.js       # Envoi SMS OTP
│   ├── prisma/
│   │   └── schema.prisma       # Schema base de donnees
│   ├── Dockerfile              # Image Docker backend
│   ├── package.json            # Dependances Node.js
│   └── .env.example            # Variables d'environnement exemple
│
├── contracts/                  # Smart Contracts Blockchain
│   ├── contracts/
│   │   ├── DiasporaTransfer.sol    # Contrat principal de transfert
│   │   └── MockUSDC.sol            # Stablecoin USDC pour tests
│   ├── scripts/
│   │   ├── deploy.js               # Script de deploiement
│   │   ├── faucet.js               # Faucet testnet
│   │   ├── fund-alice-local.js     # Financement compte test local
│   │   └── fund-alice.js           # Financement compte test
│   ├── test/
│   │   └── DiasporaTransfer.test.js # Tests smart contracts
│   └── hardhat.config.js           # Configuration Hardhat
│
├── assets/                     # Ressources statiques
│   ├── favicon.svg             # Icone du site
│   ├── icon-192.png            # Icone PWA 192x192
│   ├── icon-512.png            # Icone PWA 512x512
│   └── screens/                # Captures d'ecran
│       ├── diaspora-home.png
│       ├── diaspora-transfer.png
│       ├── diaspora-summary.png
│       └── benin-home.png
│
├── render.yaml                 # Configuration Render (Blueprint)
├── Dockerfile                  # Docker pour le backend
└── vercel.json                 # Configuration Vercel
```

---

## Installation locale

### Prerequisites
- Node.js v22+
- npm

### 1. Cloner le depot

```bash
git clone https://github.com/jauressciti-design/ss.git
cd ss
```

### 2. Installer et lancer le backend

```bash
cd backend
npm install

# Configurer les variables d'environnement
cp .env.example .env
# Editez .env avec vos propres valeurs (voir section Variables d'environnement)

# Synchroniser la base de donnees
npx prisma db push
npx prisma generate

# Lancer le serveur
npm start
# Backend disponible sur http://localhost:3000
```

### 3. Lancer le frontend

```bash
# Depuis la racine du projet
npx serve .
# Ou ouvrir index.html directement dans le navigateur
```

### 4. Blockchain locale (Optionnel)

```bash
cd contracts
npm install
npx hardhat node
npx hardhat run scripts/deploy.js --network localhost
```

---

## Variables d'environnement

Creez un fichier `.env` dans `backend/` :

```env
# Base de donnees
DATABASE_URL="postgresql://user:password@host:5432/dbname?sslmode=require"

# Securite
ENCRYPTION_KEY="cle_hex_64_caracteres"
JWT_SECRET="votre_secret_jwt"

# Blockchain
RELAYER_PRIVATE_KEY="cle_privee_wallet_relayer"
AMOY_RPC_URL="https://rpc-amoy.polygon.technology"

# SMS (optionnel, mode mock par defaut)
USE_REAL_TWILIO="false"
TWILIO_ACCOUNT_SID=""
TWILIO_AUTH_TOKEN=""
TWILIO_PHONE_NUMBER=""
```

---

## Presentation Jury

Le dossier de presentation complet est disponible en deux formats :

1. **Slides interactives (HTML)** : [presentation-yxgdjfmm.devinapps.com](https://presentation-yxgdjfmm.devinapps.com)
   - 12 slides couvrant : probleme, solution, fonctionnalites, architecture, demo, comparaison, business model, ODD, roadmap
   - Navigation par scroll
   - Liens directs vers les demos en ligne

2. **Dossier ecrit (Markdown)** : [PRESENTATION_JURY.md](./PRESENTATION_JURY.md)
   - Document complet de 10 sections
   - Donnees chiffrees et comparaisons
   - Roadmap detaillee

---

## Comparaison avec la concurrence

| Critere | Western Union | MoneyGram | DiasporaConnect |
|---------|--------------|-----------|-----------------|
| **Frais** | 8-15% | 7-12% | **0.8%** |
| **Delai** | 1-3 jours | 1-5 jours | **< 30 min** |
| **Retrait** | Agence physique | Agence physique | **Mobile Money** |
| **Securite** | Standard | Standard | **Blockchain AES-256** |
| **Hors ligne** | Non | Non | **Oui (PWA)** |
| **Installation** | App Store | App Store | **Aucune (PWA)** |

---

## Impact Social & ODD

DiasporaConnect contribue a 4 Objectifs de Developpement Durable :

| ODD | Objectif | Contribution |
|-----|----------|-------------|
| **ODD 1** | Fin de la pauvrete | Plus d'argent pour les familles (economie de 150-340 EUR/an) |
| **ODD 8** | Croissance economique | Faciliter les investissements de la diaspora |
| **ODD 9** | Innovation | Blockchain + PWA pour l'inclusion financiere |
| **ODD 10** | Inegalites reduites | Frais 0.8% vs 3% objectif ONU 2030 |

---

## Modele Economique

| Source de revenus | Taux | Details |
|-------------------|------|---------|
| Commission transferts | 0.8% | Par transaction (10x moins que la concurrence) |
| Paiement factures | Variable | Commission des fournisseurs (SBEE, SONEB, MTN, Canal+) |
| Paiement marchand | 0.5% | Par paiement QR Code |

**Projection Annee 1** : 10 000 utilisateurs | 500K EUR/mois de volume | ~48K EUR de revenus annuels

---

## Roadmap

| Phase | Periode | Objectifs |
|-------|---------|-----------|
| **Phase 1 - Hackathon** | Mai 2026 | PWA fonctionnelle, backend API, smart contracts, demo en ligne |
| **Phase 2 - Beta** | Q3 2026 | Integration Twilio, partenariat MTN MoMo/Moov, tests 50 utilisateurs, KYC/AML |
| **Phase 3 - Lancement** | Q4 2026 | Polygon Mainnet, integration banques beninois, lancement Benin + France |
| **Phase 4 - Expansion** | 2027 | Togo, Cote d'Ivoire, Senegal, nouvelles devises, marketplace services |

---

## Equipe

Projet developpe par l'equipe **LumniX** pour le **MIABE Hackathon 2026**.

- **Email** : sourakahamida@gmail.com
- **GitHub** : [github.com/jauressciti-design/ss](https://github.com/jauressciti-design/ss)

---

## Licence

MIT License

---

## Liens utiles

| Ressource | Lien |
|-----------|------|
| Landing Page | [deploy-landing-xwspoghs.devinapps.com](https://deploy-landing-xwspoghs.devinapps.com) |
| Application PWA | [deploy-pwa-jidihhbo.devinapps.com](https://deploy-pwa-jidihhbo.devinapps.com) |
| Backend API (Health) | [API Health Check](https://user:d10b00d279fa413f36617173530f37dd@0c643afbf900-tunnel-yamugwtu.devinapps.com/api/health) |
| Presentation Jury | [presentation-yxgdjfmm.devinapps.com](https://presentation-yxgdjfmm.devinapps.com) |
| Documentation API | [API_FRONTEND_DOCS.md](./API_FRONTEND_DOCS.md) |
| Doc Blockchain | [DiasporaConnect_Technique_Blockchain.docx](./DiasporaConnect_Technique_Blockchain.docx) |
| Dossier Jury | [PRESENTATION_JURY.md](./PRESENTATION_JURY.md) |

---

<p align="center">Fait avec amour pour la diaspora africaine | Equipe LumniX | MIABE 2026</p>
