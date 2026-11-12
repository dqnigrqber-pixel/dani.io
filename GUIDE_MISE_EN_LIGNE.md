# Mettre ton site en ligne gratuitement

Ton site, c'est ce dossier `site_web` : le fichier `index.html` et les photos `.jpg`. Il n'y a pas de sous-dossier, tout est au même niveau. C'est fait exprès pour que tu puisses tout envoyer d'un coup.

Il y a deux étapes : activer le formulaire, puis mettre le site en ligne. Compte 20 minutes en tout.

---

## Étape 1 : activer le formulaire de contact (Web3Forms, gratuit)

Le formulaire envoie chaque message directement dans ta boîte Gmail, avec le nom, l'entreprise, l'e-mail, le téléphone, le type de soutien et le message. Quand tu cliques sur « Répondre » dans Gmail, ta réponse part directement au sponsor.

1. Va sur **https://web3forms.com**.
2. Clique sur **Create your Access Key**.
3. Entre ton adresse : `danigrabereduvaud@gmail.com`, puis valide.
4. Tu reçois un e-mail avec ta **clé** (une longue suite de lettres et de chiffres, du genre `a1b2c3d4-...`).
5. Ouvre `index.html` et cherche cette ligne :

   ```html
   <input type="hidden" name="access_key" value="COLLE_TA_CLE_WEB3FORMS_ICI">
   ```

   Remplace `COLLE_TA_CLE_WEB3FORMS_ICI` par ta clé, en gardant les guillemets.

C'est gratuit jusqu'à 250 messages par mois, largement assez.

**Tant que la clé n'est pas collée,** le formulaire ne casse pas : il propose au visiteur d'envoyer son message par e-mail.

> Tu peux aussi faire l'étape 1 **après** l'étape 2, directement sur GitHub (voir « Modifier le site » plus bas). C'est le plus simple depuis un téléphone.

---

## Étape 2 : mettre le site en ligne (GitHub Pages, gratuit)

### A. Créer le dépôt

1. Connecte-toi sur **https://github.com**.
2. En haut à droite, appuie sur **+** puis **New repository**.
3. **Repository name** : écris `TONNOM.github.io`, en remplaçant `TONNOM` par ton nom d'utilisateur GitHub exact.
   Comme ça, ton site aura l'adresse courte `https://TONNOM.github.io`.
   (Si tu préfères un autre nom, par exemple `14x8000`, l'adresse sera `https://TONNOM.github.io/14x8000/`.)
4. Choisis **Public**. GitHub Pages gratuit demande un dépôt public.
5. Appuie sur **Create repository**.

### B. Envoyer les fichiers

Le plus simple, c'est depuis un ordinateur (par exemple à l'école) :

1. Sur la page du dépôt, clique sur **uploading an existing file**.
2. Glisse **tous les fichiers** du dossier `site_web` (`index.html` et toutes les photos `.jpg`).
   Tu peux laisser ce guide de côté, il n'a pas besoin d'être en ligne.
3. En bas, clique sur **Commit changes**.

Depuis ton téléphone, c'est possible aussi :

1. Dans l'app OneDrive, ouvre `montages / sponsor / site_web`, sélectionne tous les fichiers et enregistre-les dans l'app **Fichiers**.
2. Dans Safari (ou Chrome), ouvre ton dépôt sur github.com, demande la **version ordinateur** du site (menu « aA » dans Safari), puis **Add file → Upload files** et choisis les fichiers.
3. Appuie sur **Commit changes**.

### C. Allumer le site

1. Dans ton dépôt, va dans **Settings** puis **Pages** (menu de gauche).
2. Sous **Build and deployment**, choisis **Source : Deploy from a branch**.
3. **Branch** : `main`, dossier `/ (root)`, puis **Save**.
4. Attends 1 à 3 minutes, puis recharge la page : l'adresse de ton site s'affiche en haut (« Your site is live at… »).

---

## Modifier le site plus tard

Tout se fait sur github.com, même depuis ton téléphone :

- **Changer un texte ou coller la clé Web3Forms** : ouvre `index.html` dans ton dépôt, appuie sur le **crayon** (Edit), fais ta modification, puis **Commit changes**. Le site se met à jour tout seul en 1 à 2 minutes.
- **Chiffres TikTok** : rien à faire. Le site affiche la carte officielle de ton compte TikTok, avec tes abonnés et tes j'aime en direct. Si un visiteur est sur un réseau qui bloque TikTok (certaines écoles ou entreprises), la carte est cachée et il reste le bouton vers ton compte.
- **Ajouter une photo au carnet de route** : envoie le fichier `.jpg` dans le dépôt, puis ajoute une ligne dans la liste `const carnet = [...]` vers la fin de `index.html`, par exemple :
  `["nom-de-la-photo","Légende de la photo"],` (sans `.jpg` dans le nom).

Les animations utilisent GSAP, un outil gratuit chargé depuis Internet : tu n'as rien à installer.

---

## Vérifier que tout marche

1. Ouvre ton site sur ton téléphone et sur un ordinateur.
2. Envoie-toi un message de test avec le formulaire.
3. Regarde dans Gmail. La première fois, regarde aussi dans **Spam** ; si le message y est, marque-le « Non spam ».

---

## Ensuite

- Mets l'adresse du site dans ta **bio TikTok** et dans ta **signature d'e-mail**.
- Ajoute le lien dans tes prochains messages aux sponsors, à côté du PDF.
- Un nom de domaine à toi (par exemple `danigraber.ch`) coûte environ CHF 10 à 20 par an. Ce n'est pas obligatoire : l'adresse GitHub suffit.

## Bon à savoir

- Le dépôt est public : n'y mets jamais de mot de passe, d'adresse ou de numéro de téléphone personnel.
- La clé Web3Forms peut être visible dans le code, c'est normal : elle sert seulement à envoyer les messages vers ta boîte.
- Les photos du site ont été réduites et leurs données cachées (GPS, date, modèle du téléphone) ont été enlevées.
