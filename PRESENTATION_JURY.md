# DOSSIER DE PRESENTATION - JURY MIABE HACKATHON 2026

---

## DIASPORACONNECT

### Plateforme de transfert d'argent blockchain pour la diaspora africaine vers le Benin

**Equipe**: LumniX  
**Hackathon**: MIABE 2026  
**Date**: Mai 2026

---

## 1. PROBLEME IDENTIFIE

### Le cout exorbitant des transferts d'argent vers l'Afrique

- **7 a 15%** de frais preleves par les operateurs traditionnels (Western Union, MoneyGram, etc.)
- La diaspora africaine envoie **plus de 90 milliards USD/an** vers l'Afrique
- **Perte estimee** : 6 a 14 milliards USD/an en frais excessifs
- **Delais** : 1 a 5 jours pour un transfert classique
- **Accessibilite** : Necessite souvent un deplacement physique dans une agence

### Impact au Benin
- La diaspora beninoise envoie environ **500 millions USD/an** vers le pays
- Les frais representent un frein majeur pour les familles beneficiaires
- Les populations rurales n'ont pas acces aux agences de transfert

---

## 2. NOTRE SOLUTION : DIASPORACONNECT

### Transferts instantanes a 0.8% de frais via la blockchain Polygon

DiasporaConnect est une **Progressive Web App (PWA)** qui permet a la diaspora d'envoyer de l'argent vers le Benin avec :

| Critere | Traditionnel | DiasporaConnect |
|---------|-------------|-----------------|
| **Frais** | 7-15% | **0.8%** |
| **Delai** | 1-5 jours | **< 30 min** |
| **Accessibilite** | Agence physique | **Smartphone** |
| **Retrait** | Agence | **Mobile Money** |
| **Securite** | Variable | **Blockchain + AES-256** |

---

## 3. FONCTIONNALITES CLES

### Portail Diaspora (Expediteur)
- **Authentification sans mot de passe** par OTP SMS (securise, simple)
- **Calculateur en temps reel** des frais et du taux de change EUR/XOF
- **Transfert via smart contract** Polygon (transparent, traçable)
- **Suivi en temps reel** avec ID de transaction unique
- **Historique complet** des transactions

### Portail Benin (Beneficiaire)
- **Recherche de transfert** par numero de telephone ou ID transaction
- **Retrait en Mobile Money** : MTN MoMo et Moov Money
- **Paiement de factures** : SBEE (electricite), SONEB (eau), MTN, Canal+
- **Paiement marchand** par QR Code

### Innovation PWA
- **Installation** sur l'ecran d'accueil comme une app native
- **Fonctionne hors ligne** grace au Service Worker
- **Pas besoin du Play Store/App Store** : accessible via un simple lien
- **Mise a jour automatique** sans reinstallation

---

## 4. ARCHITECTURE TECHNIQUE

### Stack Technologique

```
Frontend (PWA)          Backend (API)           Blockchain
+------------------+   +------------------+   +------------------+
| HTML5/CSS3/JS    |   | Node.js          |   | Solidity         |
| Service Worker   |-->| Express.js       |-->| Polygon Amoy     |
| Lucide Icons     |   | Prisma ORM       |   | Hardhat          |
| Responsive       |   | JWT Auth         |   | ethers.js        |
+------------------+   | PostgreSQL       |   +------------------+
                        +------------------+
```

### Flux de transfert

```
1. Expediteur s'authentifie via OTP SMS
2. Saisit le montant et le numero du beneficiaire
3. Le smart contract Polygon execute le transfert
4. Le beneficiaire recoit une notification
5. Retrait en Mobile Money (MTN MoMo / Moov Money)
```

### Securite
- **Chiffrement AES-256** pour les donnees sensibles
- **JWT (JSON Web Tokens)** pour l'authentification
- **OTP cryptographique** (crypto.randomInt, pas de code en dur)
- **Blockchain Polygon** : transactions immutables et traçables
- **CORS configure** pour la securite des requetes cross-origin

---

## 5. DEMO EN LIGNE

### Liens d'acces (prototype fonctionnel)

| Service | URL | Description |
|---------|-----|-------------|
| **Landing Page** | https://deploy-landing-xwspoghs.devinapps.com | Page d'accueil, tarifs, FAQ |
| **Application PWA** | https://deploy-pwa-jidihhbo.devinapps.com | App complete (2 portails) |
| **Backend API** | /api/health | API REST avec PostgreSQL |

### Tester l'application

1. **Ouvrir l'App PWA** sur un smartphone
2. **Choisir un portail** : "Je suis dans la Diaspora" ou "Je suis au Benin"
3. **Explorer les fonctionnalites** : transfert, retrait, paiement factures
4. **Installer la PWA** : Cliquer "Ajouter a l'ecran d'accueil" (Chrome)

---

## 6. MODELE ECONOMIQUE

### Sources de revenus
1. **Commission sur transferts** : 0.8% par transaction (bien en dessous de la concurrence)
2. **Paiement de factures** : Commission des fournisseurs (SBEE, SONEB, MTN)
3. **Paiement marchand** : 0.5% par transaction QR Code
4. **Services premium** : Transferts prioritaires, alertes personnalisees

### Projections financieres (Annee 1)

| Metrique | Valeur |
|----------|--------|
| Utilisateurs cibles | 10 000 |
| Volume transferts mensuel | 500 000 EUR |
| Commission moyenne | 0.8% |
| Revenu mensuel estime | 4 000 EUR |
| Revenu annuel estime | 48 000 EUR |

### Avantage concurrentiel
- **10x moins cher** que Western Union/MoneyGram
- **Integration Mobile Money** directe (pas d'intermediaire)
- **Pas d'agence physique** necessaire (cout operationnel minimal)
- **Blockchain = confiance** : transactions verifiables publiquement

---

## 7. IMPACT SOCIAL ET ODD

### Objectifs de Developpement Durable vises

| ODD | Contribution |
|-----|-------------|
| **ODD 1** - Fin de la pauvrete | Reduire les frais = plus d'argent pour les familles |
| **ODD 8** - Travail decent et croissance | Faciliter les investissements de la diaspora |
| **ODD 9** - Industrie et innovation | Blockchain + PWA pour l'inclusion financiere |
| **ODD 10** - Inegalites reduites | Frais 0.8% vs objectif ONU de 3% d'ici 2030 |
| **ODD 17** - Partenariats | Collaboration operateurs Mobile Money |

### Impact mesurable
- **Economie par transaction** : Un transfert de 200 EUR coute 1.60 EUR (vs 14-30 EUR traditionnellement)
- **Economie annuelle par famille** : Si une famille recoit 200 EUR/mois, elle economise **150 a 340 EUR/an**
- **Accessibilite** : Toute personne avec un smartphone peut utiliser le service

---

## 8. ROADMAP

### Phase 1 - Prototype (Hackathon MIABE 2026) -- FAIT
- Landing page et PWA fonctionnelle
- Backend API avec PostgreSQL
- Smart contracts sur Polygon Amoy Testnet
- Demo deployee en ligne

### Phase 2 - Beta (Q3 2026)
- Integration reelle avec Twilio SMS
- Partenariat MTN MoMo / Moov Money API
- Tests utilisateurs avec 50 membres de la diaspora
- KYC/AML (verification d'identite)

### Phase 3 - Lancement (Q4 2026)
- Deploiement sur Polygon Mainnet
- Integration avec les banques beninois (UBA, BOA)
- Lancement commercial Benin + France
- Application mobile native (React Native)

### Phase 4 - Expansion (2027)
- Extension vers d'autres pays (Togo, Cote d'Ivoire, Senegal)
- Ajout de nouvelles devises (USD, GBP)
- Marketplace de services (assurance, epargne)

---

## 9. EQUIPE

**LumniX** - Equipe du MIABE Hackathon 2026

Technologies maîtrisees :
- Developpement Web Full-Stack (Node.js, Express, HTML/CSS/JS)
- Blockchain (Solidity, Polygon, Hardhat)
- Base de donnees (PostgreSQL, Prisma)
- DevOps (Docker, CI/CD)
- Design UX/UI

---

## 10. POURQUOI DIASPORACONNECT VA GAGNER

1. **Probleme reel et urgent** : Les frais de transfert sont un fardeau pour des millions de familles
2. **Solution technique solide** : Blockchain + PWA = securite + accessibilite
3. **Prototype fonctionnel** : Pas juste une idee, une application deployee et testable
4. **Impact mesurable** : Economies directes et quantifiables pour les utilisateurs
5. **Modele economique viable** : 0.8% de commission reste rentable a grande echelle
6. **Scalabilite** : Polygon traite 65 000 transactions/seconde
7. **Alignement ODD** : Contribution directe a 5 Objectifs de Developpement Durable

---

## CONTACTS & LIENS

- **Code source** : https://github.com/jauressciti-design/ss
- **Landing Page** : https://deploy-landing-xwspoghs.devinapps.com
- **Application PWA** : https://deploy-pwa-jidihhbo.devinapps.com
- **Email** : sourakahamida@gmail.com

---

*DiasporaConnect - Fait avec passion pour la diaspora africaine*
