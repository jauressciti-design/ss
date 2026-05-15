# LumniX - DiasporaConnect

<p align="center">
  <img src="https://img.shields.io/badge/MIABE-Hackathon%202026-orange" alt="MIABE 2026">
  <img src="https://img.shields.io/badge/Blockchain-Polygon-blue" alt="Polygon">
  <img src="https://img.shields.io/badge/Status-En%20ligne-brightgreen" alt="En ligne">
  <img src="https://img.shields.io/badge/PWA-Installable-blueviolet" alt="PWA">
  <img src="https://img.shields.io/badge/License-MIT-green" alt="License">
</p>

<p align="center">
  <strong>Plateforme de transfert d'argent blockchain pour la diaspora africaine vers le Benin</strong><br/>
  Frais reduits a 0.8% | Reception en moins de 30 minutes | PWA installable sur telephone
</p>

---

## Tous les liens du projet

### Deploiements principaux (Vercel - Production permanente)

| Service | URL | Description |
|---------|-----|-------------|
| **Landing Page** | [ss-tan-two.vercel.app](https://ss-tan-two.vercel.app) | Page d'accueil avec presentation, tarifs, FAQ, mockups iPhone |
| **Application PWA** | [ss-tan-two.vercel.app/app.html](https://ss-tan-two.vercel.app/app.html) | App complete avec connexion OTP, 2 portails |

### Deploiements Devin Apps (Backup)

| Service | URL | Description |
|---------|-----|-------------|
| **Landing Page** | [deploy-landing-xwspoghs.devinapps.com](https://deploy-landing-xwspoghs.devinapps.com) | Landing page de backup |
| **Application PWA** | [deploy-pwa-jidihhbo.devinapps.com](https://deploy-pwa-jidihhbo.devinapps.com) | PWA de backup |
| **Backend API** | [0c643afbf900-tunnel-yamugwtu.devinapps.com](https://user:d10b00d279fa413f36617173530f37dd@0c643afbf900-tunnel-yamugwtu.devinapps.com/api/health) | API REST Node.js + PostgreSQL |
| **Presentation Jury** | [presentation-yxgdjfmm.devinapps.com](https://presentation-yxgdjfmm.devinapps.com) | 12 slides pour le jury |

### Code source et documentation

| Ressource | URL |
|-----------|-----|
| **Repo GitHub** | [github.com/jauressciti-design/ss](https://github.com/jauressciti-design/ss) |
| **PR #2 - Deploiement complet** | [Pull Request #2](https://github.com/jauressciti-design/ss/pull/2) |
| **PR #3 - Nav fix + mockups** | [Pull Request #3](https://github.com/jauressciti-design/ss/pull/3) |
| **Dossier jury (Markdown)** | [PRESENTATION_JURY.md](./PRESENTATION_JURY.md) |
| **Documentation API** | [API_FRONTEND_DOCS.md](./API_FRONTEND_DOCS.md) |

### Base de donnees

| Service | Plateforme | Details |
|---------|-----------|---------|
| **PostgreSQL** | Neon.tech (cloud gratuit) | Base de donnees production, toutes tables creees et synchronisees |

---

## Ce qui a ete fait (resume complet)

### 1. Frontend - Landing Page
- Page d'accueil responsive avec hero section, animations GSAP + ScrollTrigger
- Calculateur de frais en temps reel (USD/EUR/GBP/CAD vers XOF)
- Section tarifs avec comparaison Western Union / MoneyGram
- FAQ interactive avec accordeons
- Section "Comment ca marche" en 3 etapes
- Section securite et blockchain
- Mockups iPhone avec les vraies captures d'ecran de l'app (9 screenshots)
- Footer avec liens et informations equipe

### 2. Frontend - Application PWA
- **Ecran de connexion OTP** : numero de telephone +229, nom complet, code OTP a 6 chiffres (code demo: **123456**)
- **Selecteur de portail** : Diaspora (envoyer) ou Benin (recevoir)
- **Portail Diaspora** :
  - Accueil avec solde, quick actions, derniers transferts
  - Envoi de transfert avec calcul automatique des frais et conversion XOF
  - Historique des transferts
  - Profil utilisateur avec parametres
- **Portail Benin** :
  - Accueil avec solde disponible et derniers transferts recus
  - Reception de transferts par telephone ou ID
  - Paiement de factures (SBEE, SONEB, MTN, Canal+)
  - Profil utilisateur
- **Navigation amélioree** : barre de navigation visible, icones larges, fond colore sur l'onglet actif, safe-area pour iOS
- **PWA installable** sur telephone :
  - Manifeste PWA (`manifest.json`) avec icones PNG 192x192 et 512x512
  - Service Worker (`sw.js`) pour le mode hors ligne
  - Banniere d'installation en bas de page
  - Meta tags Apple (apple-mobile-web-app-capable, viewport-fit=cover)
- **Design** : mobile-first, dark mode login, animations fluides, Lucide Icons

### 3. Backend API
- Serveur **Node.js + Express.js** avec 7 endpoints REST
- **PostgreSQL** sur Neon.tech (gratuit, cloud) avec Prisma ORM
- **Authentification OTP** cryptographique (plus de code en dur)
- **JWT** pour la gestion de session
- **CORS** configure pour autoriser tous les frontends
- **Health check** et taux de change en temps reel

### 4. Blockchain (Smart Contracts)
- Contrat **DiasporaTransfer.sol** en Solidity pour les transferts
- Contrat **MockUSDC.sol** pour simuler le stablecoin
- Configuration **Hardhat** pour Polygon Amoy Testnet
- Scripts de deploiement et de test

### 5. Presentation Jury
- **12 slides interactives** (HTML) couvrant :
  1. Page de titre
  2. Le probleme (frais 7-15%, delais 1-5 jours)
  3. Notre solution (blockchain Polygon, 0.8%)
  4. Fonctionnalites cles
  5. Architecture technique
  6. Demo en direct (liens vers l'app)
  7. Comparaison concurrents
  8. Modele economique
  9. Impact ODD (4 objectifs)
  10. Roadmap (4 phases)
  11. Securite et conformite
  12. Conclusion et appel a l'action
- **Dossier ecrit** (PRESENTATION_JURY.md) : 10 sections detaillees

### 6. Deploiements
- **Vercel** : Landing page + PWA sur [ss-tan-two.vercel.app](https://ss-tan-two.vercel.app) avec auto-deploy a chaque push GitHub
- **Devin Apps** : Landing, PWA, Backend API, Presentation (4 services separes)
- **Neon.tech** : Base de donnees PostgreSQL en cloud
- **GitHub** : Code source sur [jauressciti-design/ss](https://github.com/jauressciti-design/ss)

### 7. Mockups iPhone (Landing Page)
- 9 captures d'ecran reelles de l'app en format iPhone (375x812 @2x) :
  - `diaspora-home.png` - Accueil Diaspora
  - `diaspora-transfer.png` - Ecran d'envoi
  - `diaspora-summary.png` - Historique
  - `diaspora-profile.png` - Profil
  - `diaspora-sent.png` - Confirmation
  - `benin-home.png` - Accueil Benin
  - `benin-receive.png` - Reception
  - `benin-bills.png` - Factures
  - `benin-withdraw.png` - Retrait

### 8. Documentation
- `README.md` : Ce fichier, avec tous les liens et instructions
- `PRESENTATION_JURY.md` : Dossier complet pour le jury
- `API_FRONTEND_DOCS.md` : Documentation de l'API frontend
- `.env.example` : Variables d'environnement necessaires
- `render.yaml` : Configuration Render (Blueprint)
- `vercel.json` : Configuration Vercel avec headers de securite
- `Dockerfile` : Image Docker pour le backend

---

## Description du projet

**DiasporaConnect** est une plateforme innovante de transfert de fonds internationaux construite sur la blockchain Polygon, permettant a la diaspora africaine d'envoyer de l'argent vers le Benin avec des frais reduits a **0.8%** et une reception en Mobile Money (MTN MoMo, Moov Money) en moins de 30 minutes.

Le projet est developpe par l'equipe **LumniX** dans le cadre du **MIABE Hackathon 2026**.

---

## Fonctionnalites detaillees

### Portail Diaspora (Expediteurs)
- Authentification sans mot de passe par OTP SMS cryptographique
- Calcul automatique des frais et conversion en temps reel (USD, EUR, GBP, CAD vers XOF)
- Transfert securise via smart contract Polygon
- Suivi en temps reel avec ID de transaction unique
- Historique des transferts avec details complets
- Profil utilisateur avec parametres de securite

### Portail Benin (Beneficiaires)
- Recherche de transfert par telephone ou ID de transaction
- Retrait en Mobile Money (MTN MoMo / Moov Money)
- Paiement de factures : SBEE (electricite), SONEB (eau), MTN (mobile), Canal+ (TV)
- Paiement marchand par QR Code sans frais
- Solde disponible et historique des operations

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
| CSS Custom Properties | Theming (variables CSS) |
| Safe Area Insets | Support iPhone X+ (encoche) |

### Backend
| Technologie | Usage |
|-------------|-------|
| Node.js + Express.js | Serveur API REST |
| Prisma ORM | Acces base de donnees |
| PostgreSQL (Neon.tech) | Base de donnees production |
| JSON Web Tokens (JWT) | Authentification |
| crypto (Node.js) | Generation OTP securise |
| CORS | Securite cross-origin |

### Blockchain
| Technologie | Usage |
|-------------|-------|
| Solidity | Smart Contracts |
| Polygon Amoy Testnet | Reseau blockchain |
| Hardhat | Dev, test, deploiement |
| ethers.js | Interaction blockchain |

### Infrastructure
| Service | Plateforme | URL |
|---------|-----------|-----|
| Landing Page (prod) | Vercel | [ss-tan-two.vercel.app](https://ss-tan-two.vercel.app) |
| PWA (prod) | Vercel | [ss-tan-two.vercel.app/app.html](https://ss-tan-two.vercel.app/app.html) |
| Landing Page (backup) | Devin Apps | [deploy-landing-xwspoghs.devinapps.com](https://deploy-landing-xwspoghs.devinapps.com) |
| PWA (backup) | Devin Apps | [deploy-pwa-jidihhbo.devinapps.com](https://deploy-pwa-jidihhbo.devinapps.com) |
| Backend API | Devin Apps | [API Health](https://user:d10b00d279fa413f36617173530f37dd@0c643afbf900-tunnel-yamugwtu.devinapps.com/api/health) |
| Base de donnees | Neon.tech | PostgreSQL cloud |
| Presentation Jury | Devin Apps | [presentation-yxgdjfmm.devinapps.com](https://presentation-yxgdjfmm.devinapps.com) |

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
├── styles.css                  # Styles CSS landing page (animations, hero, responsive)
├── script.js                   # Logique JavaScript landing page (GSAP, FAQ, calculateur)
├── app.html                    # Application PWA (connexion OTP + 2 portails)
├── app-styles.css              # Styles CSS application (dark login, nav, portails)
├── app-script.js               # Logique JavaScript application (auth OTP, transferts)
├── manifest.json               # Manifeste PWA (icones, theme, start_url)
├── sw.js                       # Service Worker PWA (cache v2, mode hors ligne)
├── presentation.html           # Slides de presentation jury (12 slides)
├── PRESENTATION_JURY.md        # Dossier ecrit pour le jury
├── API_FRONTEND_DOCS.md        # Documentation API frontend
├── README.md                   # Ce fichier
│
├── backend/                    # Serveur Node.js
│   ├── src/
│   │   ├── index.js            # Point d'entree serveur (Express, CORS, routes)
│   │   ├── prismaClient.js     # Client Prisma (connexion PostgreSQL)
│   │   ├── middleware/
│   │   │   └── auth.js         # Middleware JWT (verification token)
│   │   ├── routes/
│   │   │   ├── auth.js         # Routes inscription/OTP (crypto)
│   │   │   ├── transfer.js     # Routes transferts (Polygon)
│   │   │   ├── withdraw.js     # Routes retraits (Mobile Money)
│   │   │   ├── rates.js        # Routes taux de change (CoinGecko)
│   │   │   └── transactions.js # Routes historique
│   │   └── services/
│   │       ├── blockchain.js   # Interactions Polygon (ethers.js)
│   │       ├── coingecko.js    # API taux de change
│   │       └── twilio.js       # Envoi SMS OTP (mock/reel)
│   ├── prisma/
│   │   └── schema.prisma       # Schema base de donnees (User, Transfer, OTP)
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
│   ├── favicon.svg             # Icone du site (SVG)
│   ├── icon-192.png            # Icone PWA 192x192
│   ├── icon-512.png            # Icone PWA 512x512
│   └── screens/                # Captures d'ecran pour les mockups iPhone
│       ├── diaspora-home.png       # Accueil portail Diaspora
│       ├── diaspora-transfer.png   # Ecran d'envoi de transfert
│       ├── diaspora-summary.png    # Historique des transferts
│       ├── diaspora-profile.png    # Profil utilisateur Diaspora
│       ├── diaspora-sent.png       # Confirmation d'envoi
│       ├── benin-home.png          # Accueil portail Benin
│       ├── benin-receive.png       # Ecran de reception
│       ├── benin-bills.png         # Paiement de factures
│       └── benin-withdraw.png      # Ecran de retrait
│
├── render.yaml                 # Configuration Render (Blueprint auto-deploy)
├── Dockerfile                  # Docker pour le backend
└── vercel.json                 # Configuration Vercel (headers securite)
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
   - 12 slides : probleme, solution, fonctionnalites, architecture, demo, comparaison, business model, ODD, roadmap, securite, conclusion
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
| **Transparence** | Opaque | Opaque | **100% transparent** |

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

## Comment tester l'application

### Tester la PWA (connexion + portails)
1. Aller sur [ss-tan-two.vercel.app/app.html](https://ss-tan-two.vercel.app/app.html) (ou [deploy-pwa-jidihhbo.devinapps.com](https://deploy-pwa-jidihhbo.devinapps.com))
2. Entrer un numero de telephone (ex: `97123456`) et un nom
3. Cliquer "Recevoir le code OTP"
4. Entrer le code demo : **123456**
5. Choisir le **Portail Diaspora** (envoyer) ou **Portail Beninois** (recevoir)
6. Explorer les fonctionnalites de chaque portail

### Installer la PWA sur telephone
1. Ouvrir le lien PWA sur Chrome mobile
2. Une banniere "Installer DiasporaConnect" apparait en bas
3. Cliquer "Installer" pour ajouter l'app a l'ecran d'accueil
4. L'app s'ouvre comme une app native (plein ecran, pas de barre URL)

### Tester l'API
```bash
# Health check
curl https://user:d10b00d279fa413f36617173530f37dd@0c643afbf900-tunnel-yamugwtu.devinapps.com/api/health

# Taux de change
curl https://user:d10b00d279fa413f36617173530f37dd@0c643afbf900-tunnel-yamugwtu.devinapps.com/api/rates
```

---

## Equipe

Projet developpe par l'equipe **LumniX** pour le **MIABE Hackathon 2026**.

- **Email** : sourakahamida@gmail.com
- **GitHub** : [github.com/jauressciti-design/ss](https://github.com/jauressciti-design/ss)

---

## Licence

MIT License

---

## Recapitulatif de tous les liens

| Ressource | Lien |
|-----------|------|
| **Landing Page (Vercel)** | [ss-tan-two.vercel.app](https://ss-tan-two.vercel.app) |
| **PWA (Vercel)** | [ss-tan-two.vercel.app/app.html](https://ss-tan-two.vercel.app/app.html) |
| **Landing Page (Devin Apps)** | [deploy-landing-xwspoghs.devinapps.com](https://deploy-landing-xwspoghs.devinapps.com) |
| **PWA (Devin Apps)** | [deploy-pwa-jidihhbo.devinapps.com](https://deploy-pwa-jidihhbo.devinapps.com) |
| **Backend API (Health)** | [API Health Check](https://user:d10b00d279fa413f36617173530f37dd@0c643afbf900-tunnel-yamugwtu.devinapps.com/api/health) |
| **Backend API (Rates)** | [API Taux de change](https://user:d10b00d279fa413f36617173530f37dd@0c643afbf900-tunnel-yamugwtu.devinapps.com/api/rates) |
| **Presentation Jury (Slides)** | [presentation-yxgdjfmm.devinapps.com](https://presentation-yxgdjfmm.devinapps.com) |
| **Dossier Jury (Markdown)** | [PRESENTATION_JURY.md](./PRESENTATION_JURY.md) |
| **Documentation API** | [API_FRONTEND_DOCS.md](./API_FRONTEND_DOCS.md) |
| **Repo GitHub** | [github.com/jauressciti-design/ss](https://github.com/jauressciti-design/ss) |
| **PR #2** | [Pull Request #2](https://github.com/jauressciti-design/ss/pull/2) |
| **PR #3** | [Pull Request #3](https://github.com/jauressciti-design/ss/pull/3) |

---

<p align="center">Fait avec amour pour la diaspora africaine | Equipe LumniX | MIABE 2026</p>
