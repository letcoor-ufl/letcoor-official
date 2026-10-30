# LETCOOR 1.0.0 — Documentation utilisateur complète

> Documentation établie à partir du code source réel de **LETCOOR 1.0.0** fourni le 30 octobre 2026.
> Cette documentation décrit les fonctions réellement exposées par l'application Android/Windows et l'interface actuelle.

---

## Sommaire

1. [Bien démarrer : connecter les appareils](#1-bien-démarrer--connecter-les-appareils)
2. [Permissions importantes, surtout hors ligne](#2-permissions-importantes-surtout-hors-ligne)
3. [Créer ou rejoindre un groupe](#3-créer-ou-rejoindre-un-groupe)
4. [Comprendre l'écran principal](#4-comprendre-lécran-principal)
5. [La carte tactique](#5-la-carte-tactique)
6. [Créer un signalement](#6-créer-un-signalement)
7. [Créer un objectif](#7-créer-un-objectif)
8. [Créer un ordre](#8-créer-un-ordre)
9. [Créer un rassemblement](#9-créer-un-rassemblement)
10. [Envoyer une alerte de sécurité](#10-envoyer-une-alerte-de-sécurité)
11. [Interagir avec un objet déjà publié](#11-interagir-avec-un-objet-déjà-publié)
12. [Le panneau « Commandement et activité »](#12-le-panneau-commandement-et-activité)
13. [Le menu du groupe ou de l'équipe](#13-le-menu-du-groupe-ou-de-léquipe)
14. [Équipes](#14-équipes)
15. [Participants et rôles](#15-participants-et-rôles)
16. [Inviter un nouveau participant](#16-inviter-un-nouveau-participant)
17. [Opérations](#17-opérations)
18. [Campagnes de rôles](#18-campagnes-de-rôles)
19. [Sessions](#19-sessions)
20. [Partage de données entre équipes](#20-partage-de-données-entre-équipes)
21. [Gestion du groupe et des équipes](#21-gestion-du-groupe-et-des-équipes)
22. [Limites de publication](#22-limites-de-publication)
23. [Localisation](#23-localisation)
24. [Notifications](#24-notifications)
25. [Cartes hors ligne](#25-cartes-hors-ligne)
26. [Connexion réseau et fonctionnement hors ligne](#26-connexion-réseau-et-fonctionnement-hors-ligne)
27. [Confidentialité, verrouillage et récupération](#27-confidentialité-verrouillage-et-récupération)
28. [Rôles disponibles](#28-rôles-disponibles)
29. [Conseils de préparation avant une activité](#29-conseils-de-préparation-avant-une-activité)
30. [Dépannage](#30-dépannage)
31. [Résumé rapide](#31-résumé-rapide)

---

# 1. Bien démarrer : connecter les appareils

LETCOOR utilise un système d'invitation entre appareils. Une invitation peut être transmise par **QR code**, **lien**, partage système ou fichier selon la plateforme.

Pour maximiser les chances de connexion, surtout **sans Internet**, préparez les deux appareils avant l'échange.

## 1.1 Avant de scanner le QR code ou d'ouvrir le lien

Sur les deux appareils :

1. Ouvrez LETCOOR et laissez l'application au premier plan pendant la première connexion.
2. Activez le **Wi‑Fi**.
3. Activez le **Bluetooth**.
4. Acceptez les demandes Android/Windows concernant les **appareils à proximité**, le Bluetooth, le Wi‑Fi Direct ou le réseau local.
5. Si Android propose de rendre le téléphone visible en Bluetooth, acceptez pendant la phase de connexion.
6. Si Android demande d'activer le service de localisation pour permettre la détection radio, il est recommandé de l'activer pour la compatibilité avec les API de proximité du téléphone.
7. La **caméra** n'est nécessaire que pour scanner un QR code. Elle n'est pas nécessaire si vous utilisez un lien.

> **Important :** l'autorisation ou l'activation du service de localisation Android pour la découverte de proximité n'active pas automatiquement le partage de votre position dans LETCOOR. Le partage de localisation est une fonction séparée et reste désactivé tant que vous ne l'activez pas vous-même.

## 1.2 Connexion par QR code

### Sur l'appareil qui invite

1. Ouvrez le menu du groupe ou de l'équipe en touchant son nom en haut à gauche.
2. Ouvrez l'onglet **Inviter**.
3. Si plusieurs destinations sont disponibles, choisissez le **groupe** ou l'**équipe** à rejoindre.
4. Ouvrez **Partager l'invitation**.
5. Sélectionnez **Afficher le QR code**.
6. Laissez le QR affiché à l'écran.

Un QR peut être composé de plusieurs parties. LETCOOR les fait défiler automatiquement. Il est possible de mettre le défilement en pause ou de passer manuellement à la partie précédente/suivante.

### Sur l'appareil invité

1. Sur l'écran d'accueil, choisissez **Rejoindre avec une invitation**.
2. Appuyez sur le bouton de scan QR.
3. Autorisez la caméra si Android/Windows le demande.
4. Visez le QR de l'autre appareil.
5. Si le QR comporte plusieurs parties, gardez la caméra orientée vers l'écran jusqu'à ce que LETCOOR ait lu toutes les parties.
6. LETCOOR importe l'invitation et prépare une **réponse**.
7. L'appareil invité affiche alors un **lien de réponse** ou un **QR de réponse** à renvoyer à l'appareil invitant.

### Retour de la réponse vers l'invitant

Sur l'appareil qui a créé l'invitation :

1. Restez dans **Inviter**.
2. Ouvrez **Recevoir la réponse**.
3. Scannez le QR de réponse, collez le lien de réponse ou utilisez le mécanisme de partage disponible.
4. LETCOOR vérifie la réponse puis commence la connexion directe.

L'application affiche ensuite l'état de la tentative : préparation de proximité, connexion Internet, recherche locale, connexion établie ou délai dépassé.

## 1.3 Connexion par lien

La procédure est identique, mais sans caméra.

### Appareil invitant

Dans **Inviter > Partager l'invitation** :

1. Choisissez **Lien d'invitation**.
2. Appuyez sur **Copier le lien** ou sur le bouton de partage.
3. Envoyez le lien à l'autre participant.

### Appareil invité

1. Ouvrez **Rejoindre avec une invitation**.
2. Collez le lien dans **Invitation à accepter**, ou utilisez le bouton presse-papiers.
3. LETCOOR traite automatiquement un lien valide.
4. Renvoyez ensuite le **lien de réponse** à l'appareil qui vous invite.

### Appareil invitant

Dans **Recevoir la réponse** :

1. Collez le lien de réponse ou scannez le QR de réponse.
2. LETCOOR vérifie la réponse.
3. La connexion commence automatiquement.

## 1.4 Pourquoi y a-t-il une réponse à renvoyer ?

Le flux bidirectionnel permet aux deux appareils de connaître les informations nécessaires à la tentative de connexion. LETCOOR peut alors essayer les chemins disponibles et authentifier le pair avant l'admission au groupe ou à l'équipe.

## 1.5 Admission au groupe et à l'équipe

Une invitation valide est signée et cible une destination déterminée lors de sa création.

- Une invitation de groupe permet de rejoindre le groupe correspondant.
- Une invitation provenant d'une équipe peut inclure l'accès au **groupe parent et à l'équipe de l'invitant**.
- Les clés privées du groupe ou l'historique complet ne sont pas placés dans le QR code.
- L'admission est validée par le protocole LETCOOR après authentification ; il n'existe pas de validation manuelle supplémentaire pour une invitation valide, sauf si la politique d'admission ou les droits de l'espace l'empêchent.

---

# 2. Permissions importantes, surtout hors ligne

LETCOOR utilise plusieurs fonctions système. Pour une utilisation hors Internet, les permissions de proximité sont particulièrement importantes.

## 2.1 Bluetooth et Wi‑Fi Direct

Dans **Paramètres > Autorisations**, LETCOOR propose :

- **Bluetooth et Wi‑Fi Direct — Autoriser**
- **Caméra — Autoriser**
- **Localisation — Vérifier**

Sur Android récent, LETCOOR peut demander notamment les autorisations système liées à :

- appareils à proximité ;
- scan Bluetooth ;
- connexion Bluetooth ;
- annonce Bluetooth ;
- Wi‑Fi Direct / appareils Wi‑Fi à proximité ;
- accès au réseau local sur les versions Android qui l'imposent.

Sur certaines anciennes versions d'Android, la découverte Bluetooth/Wi‑Fi peut dépendre de l'autorisation de localisation Android.

## 2.2 Localisation : deux choses différentes

Il faut distinguer :

1. **La localisation système Android utilisée par certaines API de découverte de proximité.**
2. **Le partage volontaire de votre position dans LETCOOR.**

Vous pouvez utiliser LETCOOR sans publier votre position sur la carte. Le partage de position se règle séparément depuis l'icône **Localisation**.

## 2.3 Caméra

La caméra sert uniquement au scan des QR codes. Le scan ne demande pas le microphone.

Si la caméra est refusée :

- utilisez le lien d'invitation ;
- ou réautorisez la caméra dans les réglages Android/Windows.

## 2.4 Notifications système

Les notifications système peuvent être activées depuis le centre de notifications LETCOOR. Elles permettent de recevoir des alertes natives pour certains événements lorsque la plateforme le permet.

---

# 3. Créer ou rejoindre un groupe

Au premier lancement, si l'appareil ne possède encore aucun groupe, LETCOOR affiche l'écran d'accueil.

Vous disposez de deux choix :

- **Créer un groupe**
- **Rejoindre avec une invitation**

## 3.1 Créer un groupe

1. Appuyez sur **Créer un groupe**.
2. Entrez le **Nom du groupe**.
3. Le nom doit contenir au moins 2 caractères.
4. Appuyez sur **Créer**.

Le créateur obtient le rôle d'administration du groupe et peut ensuite créer des équipes, inviter des participants et gérer l'espace selon les capacités accordées par le Core.

## 3.2 Rejoindre un groupe

1. Appuyez sur **Rejoindre avec une invitation**.
2. Importez le lien ou le QR.
3. Suivez l'échange invitation/réponse décrit au début de cette documentation.

## 3.3 Num Perso

Chaque appareil possède un **Num Perso** affiché dans l'onboarding et dans l'onglet **Contexte**.

Ce numéro sert d'identifiant lisible pour l'utilisateur dans l'interface. L'identité cryptographique réelle repose sur l'identité de l'appareil LETCOOR, pas sur ce code affiché.

---

# 4. Comprendre l'écran principal

LETCOOR utilise une interface **centrée sur la carte** plutôt qu'une succession de pages classiques.

## 4.1 En-tête

En haut de l'écran :

- à gauche : le **nom du groupe ou de l'équipe actuellement sélectionné** ;
- le sous-titre indique **Groupe** ou **Équipe** ;
- l'état **Non synchronisé** peut apparaître si le contexte fonctionne hors synchronisation ;
- une cloche ouvre les **Notifications** ;
- le bouton **Commandement** ouvre le panneau de commandement et d'activité ;
- une pastille affiche l'état réseau : Internet direct, relais, Wi‑Fi Direct, Wi‑Fi local, Bluetooth, LAN, synchronisation ou recherche de connexion.

## 4.2 Carte centrale

La carte affiche les objets autorisés dans le contexte courant :

- ordres ;
- signalements ;
- objectifs ;
- rendez-vous / rassemblements ;
- alertes sécurité ;
- présence d'équipe ;
- présence exacte lorsqu'elle est autorisée ;
- mouvements / trajectoires selon les droits et partages actifs.

## 4.3 Légende

Le bouton `?` affiche la légende, notamment :

- Danger ;
- Objectif ;
- Rassemblement ;
- Équipe.

## 4.4 Pied de page

Le bas de l'écran indique :

- le nombre de membres actifs du contexte ;
- le nombre d'objets actifs ;
- la présence éventuelle d'une session en cours, sinon votre Num Perso.

## 4.5 Ouvrir le menu du groupe ou de l'équipe

Touchez le nom du contexte en haut à gauche.

Le panneau comporte les onglets :

- **Contexte**
- **Équipes**
- **Participants**
- **Inviter**
- **Opérations**
- **Gestion**
- **Paramètres**

Certaines fonctions n'apparaissent que si votre rôle possède la permission correspondante.

---

# 5. La carte tactique

## 5.1 Se déplacer

La carte se manipule comme une carte tactile classique : déplacement et zoom.

## 5.2 Ajouter un objet

Pour publier un objet spatial :

1. Faites un **appui long** à l'emplacement voulu.
2. LETCOOR ouvre **Ajouter ici**.
3. Les actions autorisées pour votre rôle sont proposées.

Les possibilités sont :

- **Signalement**
- **Objectif**
- **Ordre**
- **Rassemblement**
- **Alerte sécurité**

Les actions non autorisées dans votre contexte ne sont pas affichées.

## 5.3 Formes géographiques

Selon le type d'objet, LETCOOR permet :

- **Point** ;
- **Zone circulaire** ;
- **Polygone** ;
- **Tracé**.

Pour une zone circulaire, le rayon est réglable de **10 à 500 m**.

Pour un polygone ou un tracé :

1. choisissez la géométrie ;
2. appuyez sur **Dessiner sur la carte** ;
3. ajoutez les sommets sur la carte ;
4. utilisez **Annuler le dernier**, **Terminer** ou **Abandonner**.

Le nombre de points est borné par l'interface.

## 5.4 Durée / échéance

Les objets spatiaux non-sécurité peuvent recevoir une durée entre **5 et 360 minutes**, par pas de 5 minutes.

---

# 6. Créer un signalement

1. Faites un appui long sur la carte.
2. Choisissez **Signalement**.
3. Sélectionnez le type.
4. Entrez éventuellement un nom et une description.
5. Choisissez la géométrie et la durée.
6. Appuyez sur **Publier**.

## Types de signalement disponibles

- Danger
- Obstacle
- Route bloquée
- Passage impraticable
- Passage ouvert
- Adversaire observé
- Groupe observé
- Mouvement observé
- Problème de matériel
- Personnalisé

Selon votre rôle, un signalement peut être publié dans l'équipe ou au niveau du groupe.

Les éclaireurs et responsables disposant des permissions nécessaires peuvent notamment confirmer, contester, résoudre ou promouvoir certains signalements.

---

# 7. Créer un objectif

1. Appui long sur la carte.
2. Choisissez **Objectif**.
3. Saisissez **Objectif à réaliser**.
4. Choisissez le type.
5. Choisissez la priorité.
6. Sélectionnez la géométrie.
7. Réglez l'échéance.
8. Appuyez sur **Publier**.

## Types d'objectif

- Atteindre un point
- Tenir une zone
- Capturer une zone
- Récupérer un objet
- Rejoindre un rendez-vous
- Observer une zone
- Personnalisé

## Objectif d'équipe ou objectif final du groupe

Lorsque le rôle et le contexte l'autorisent, le formulaire permet de choisir :

- **Tout le groupe — objectif final** ;
- **Cette équipe — objectif d'équipe**.

L'objectif final est visible par les membres du groupe et les équipes conformément aux règles d'autorisation du Core.

## Priorités

L'interface propose :

- P0 — Urgente
- P1 — Haute
- P2 — Normale
- P3 — Faible

---

# 8. Créer un ordre

1. Appui long sur la carte.
2. Choisissez **Ordre**.
3. Entrez la consigne personnalisée si nécessaire.
4. Choisissez le type d'ordre.
5. Choisissez la priorité.
6. Vous pouvez lier l'ordre à un **objectif** existant.
7. Vous pouvez lier l'ordre à un **rendez-vous** existant.
8. Si nécessaire, LETCOOR permet de créer directement un objectif ou un rendez-vous au même emplacement puis de revenir à l'ordre.
9. Choisissez la géométrie et la durée.
10. Appuyez sur **Publier**.

## Types d'ordre

- Se déplacer
- Se regrouper
- Tenir la position
- Avancer
- Se replier
- Défendre
- Observer
- Sécuriser un objectif
- Personnalisé

## Ordre du chef de groupe

Lorsque la publication est un ordre de commandement de groupe, le chef de groupe choisit les **équipes destinataires**. Le code opérationnel prévoit que ce type d'ordre est destiné aux chefs des équipes sélectionnées.

## Ordre d'équipe

Un chef d'équipe peut créer des ordres dans son équipe. Un ordre d'équipe peut également être lié à un ordre de commandement parent lorsque cette relation est disponible.

---

# 9. Créer un rassemblement

1. Appui long sur la carte.
2. Choisissez **Rassemblement**.
3. Donnez un nom court.
4. Choisissez un **Point** ou une **Zone circulaire**.
5. Réglez la durée / échéance.
6. Publiez.

Le rassemblement crée un rendez-vous utilisable également comme référence par un ordre.

---

# 10. Envoyer une alerte de sécurité

L'alerte sécurité est une publication prioritaire.

1. Appui long sur la carte.
2. Choisissez **Alerte sécurité**.
3. Entrez un message si nécessaire.
4. Choisissez le type.
5. Appuyez sur **Envoyer l'alerte**.

## Types disponibles

- Blessure
- Arrêt de l'activité
- Danger
- Personne disparue
- Autre urgence

Une alerte personnalisée exige un message.

LETCOOR rappelle dans l'interface que l'alerte P0 doit être utilisée en cas de danger ou de besoin d'aide.

Selon les permissions, un responsable peut ensuite **Marquer comme résolue**.

---

# 11. Interagir avec un objet déjà publié

Touchez un objet de la carte pour ouvrir sa fiche.

Les actions proposées dépendent du type d'objet et de vos permissions.

## Signalement

Actions possibles :

- Confirmer
- Contester
- Résoudre
- Prolonger de 15 min
- Annuler le signalement
- Promouvoir au groupe, lorsque le signalement provient d'une équipe et que le rôle le permet

Pour certains objets opérationnels, LETCOOR peut aussi proposer :

- **Confirmer sur le terrain** ;
- **Voter pour résoudre** ;
- **Signaler le passage ouvert** ;
- **Retirer l'information**.

## Objectif

Un utilisateur disposant de la permission correspondante peut faire évoluer son état :

- En cours
- Terminé
- Échoué
- Annulé

## Ordre

Des réponses peuvent être proposées selon le type d'ordre :

- Reçu
- Accepté
- Terminé
- Impossible

Le panneau simplifié **Opérations > Ordres** utilise au minimum l'accusé **Reçu** lorsque l'ordre demande une réponse.

## Alerte sécurité

Le responsable autorisé peut choisir **Marquer comme résolue**.

---

# 12. Le panneau « Commandement et activité »

Le bouton **Commandement** en haut de l'écran ouvre un panneau séparé destiné aux opérations non nécessairement liées à un point sur la carte.

Il comporte jusqu'à trois onglets :

- **Notifications**
- **Publier**
- **Historique**

Les onglets n'apparaissent que lorsqu'ils ont du contenu ou qu'une action est autorisée.

## 12.1 Notifications

Affiche les objets opérationnels accessibles :

- ordre de commandement ;
- ordre d'équipe ;
- objectif ;
- objectif final du groupe ;
- annonce ;
- rapport à vérifier ;
- signalement vérifié.

Chaque carte peut indiquer :

- texte ;
- type ;
- état ;
- équipe/groupe ;
- objectif ou rendez-vous lié ;
- équipes ciblées ;
- accusés de réception ;
- votes ;
- progression par équipe.

Selon votre rôle, les boutons peuvent proposer :

- Reçu ;
- Vérifier sur le terrain ;
- Retirer ;
- Marquer comme lu ;
- Déclarer terminé ;
- Voter terminé ;
- Voter impossible ;
- Voter résolu ;
- Résoudre.

## 12.2 Publier

LETCOOR affiche seulement les publications autorisées pour votre rôle et votre contexte.

Les types internes actuellement gérés par l'interface incluent :

- Ordre de commandement
- Ordre d'équipe
- Objectif d'équipe
- Objectif final du groupe
- Annonce
- Rapport à vérifier
- Signalement vérifié

Pour un ordre de commandement, choisissez les équipes destinataires.

Pour un ordre d'équipe, vous pouvez sélectionner un ordre de commandement parent.

Entrez ensuite la description puis appuyez sur **Publier**.

Les publications créées depuis ce panneau utilisent actuellement une durée opérationnelle par défaut d'environ 30 minutes dans le code de l'interface.

## 12.3 Historique

Affiche les événements enregistrés avec leur date, résumé et identifiant d'objet.

---

# 13. Le menu du groupe ou de l'équipe

Touchez le nom du contexte en haut à gauche.

## Onglet Contexte

Affiche :

- le sélecteur **Groupe ou équipe** ;
- le nombre de membres ;
- le nombre d'appareils connectés ;
- l'état de session ;
- vos rôles ;
- le thème Système / Clair / Sombre ;
- la langue ;
- votre **Num Perso**, copiable.

Les langues actuellement exposées par l’interface sont : **Système, Français, English, العربية, Deutsch et Русский**. L’interface passe automatiquement en sens droite-à-gauche pour l’arabe.

## Onglet Équipes

Voir [Équipes](#14-équipes).

## Onglet Participants

Voir [Participants et rôles](#15-participants-et-rôles).

## Onglet Inviter

Voir [Inviter un nouveau participant](#16-inviter-un-nouveau-participant).

## Onglet Opérations

Voir [Opérations](#17-opérations).

## Onglet Gestion

Voir [Gestion du groupe et des équipes](#21-gestion-du-groupe-et-des-équipes).

## Onglet Paramètres

Contient actuellement :

- les cartes hors ligne ;
- la gestion des permissions Bluetooth/Wi‑Fi Direct ;
- l'autorisation caméra ;
- la vérification de localisation.

---

# 14. Équipes

L'onglet **Équipes** affiche les équipes du groupe.

Pour chaque équipe, LETCOOR montre notamment :

- nom ;
- nombre de membres ;
- chef d'équipe ;
- liste des participants ;
- votre état d'accès à l'équipe.

## États d'accès

- **Vous êtes membre · accès prêt**
- **Adhésion enregistrée · réception des clés en cours**
- **Vous ne faites pas partie de cette équipe**

Si vous êtes membre et que l'accès est prêt, appuyez sur **Ouvrir mon équipe**.

## 14.1 Créer une équipe

Cette fonction apparaît au chef de groupe disposant de la permission correspondante.

1. Entrez le **Nom de l'équipe**.
2. Choisissez le **Chef d'équipe** parmi les membres du groupe.
3. Sélectionnez éventuellement les membres initiaux.
4. Vous pouvez utiliser :
   - Tout sélectionner ;
   - 10 personnes ;
   - 15 personnes ;
   - Tout désélectionner.
5. Appuyez sur **Créer l'équipe et nommer son chef**.

Une équipe accepte au maximum 200 membres initiaux dans le formulaire, chef inclus.

Les membres sélectionnés quittent leur éventuelle ancienne équipe du même groupe pour rejoindre la nouvelle.

Lorsque le groupe possède déjà dix équipes ou plus, le code impose des règles supplémentaires de taille minimale : les équipes actives doivent compter au moins quatre membres pour poursuivre l'expansion.

## 14.2 Remplacer le chef d'équipe

Si l'action est autorisée :

1. ouvrez l'équipe ;
2. utilisez **Remplacer le chef d'équipe** ;
3. choisissez un membre du groupe.

## 14.3 Seuils de validation

Les responsables autorisés peuvent régler :

- votes d'éclaireurs nécessaires pour terminer ;
- votes d'éclaireurs nécessaires pour déclarer impossible ;
- votes nécessaires pour résoudre un signalement.

---

# 15. Participants et rôles

L'onglet **Participants** affiche les membres du contexte sélectionné.

Vous pouvez rechercher un participant par son Num Perso ou son identifiant.

Touchez un participant pour ouvrir les actions disponibles.

## 15.1 Rôles permanents et rôles de session

Lorsqu'une session est disponible, le gestionnaire peut choisir :

- **Permanent** ;
- **Session**.

Un rôle permanent reste attaché au membre selon les règles du groupe/équipe.

Un rôle de session s'applique à la session sélectionnée.

## 15.2 Attribuer ou retirer un rôle

Les rôles que vous pouvez attribuer apparaissent sous forme de boutons.

Un bouton actif indique que le rôle est déjà présent. Appuyer dessus permet de le retirer lorsque vous en avez l'autorité.

Il existe également une section **Administrer un rôle dans une équipe** permettant de choisir :

1. l'équipe cible ;
2. le rôle ;
3. **Attribuer le rôle d'équipe** ou **Retirer le rôle d'équipe**.

## 15.3 Affectation de session

Un administrateur de session peut affecter le participant :

- Actif ;
- En pause ;
- Parti ;
- Retiré.

Il peut également choisir son équipe de session ou **Sans équipe**.

Appuyez sur **Appliquer l'affectation**.

## 15.4 Retirer un membre

Lorsque la permission est disponible, le bouton **Retirer de ce groupe ou de cette équipe** apparaît.

## 15.5 Transférer l'administration du groupe

Le responsable autorisé peut sélectionner un autre participant puis utiliser **Transférer l'administration**.

Le destinataire devra ensuite accepter le transfert depuis la section **Gestion**.

## 15.6 Bannir un appareil

La section **Modération** permet, lorsque votre rôle le permet :

- **Bannir cet appareil** ;
- afficher les appareils bannis ;
- **Lever le bannissement**.

Un appareil banni reste refusé lors de nouvelles invitations jusqu'à la levée du bannissement.

---

# 16. Inviter un nouveau participant

Ouvrez **Inviter**.

## 16.1 Choisir la destination

Selon votre rôle, le menu **Destination** permet de choisir :

- le groupe ;
- une équipe.

Un administrateur du groupe peut disposer de plusieurs destinations dans le menu.

## 16.2 Admissions ouvertes / fermées

L'interface peut indiquer :

- **Admissions ouvertes** ;
- **Admissions fermées**.

Si votre rôle le permet :

- **Ouvrir l'accès** ;
- **Fermer l'accès**.

Une équipe peut également hériter de la fermeture générale du groupe.

## 16.3 Partager l'invitation

LETCOOR permet :

- lien ;
- QR ;
- copie ;
- partage système ;
- fichier `.letcoor` sur les plateformes où le bouton est proposé.

## 16.4 Recevoir la réponse

Après import de l'invitation par l'autre appareil :

1. ouvrez **Recevoir la réponse** ;
2. scannez ou collez le lien de réponse ;
3. LETCOOR lance la connexion.

Si les tentatives Internet et proximité expirent, le bouton **Réessayer** permet de recommencer.

## 16.5 Réinitialiser une invitation

Le bouton de réinitialisation permet d'invalider/régénérer l'échange courant lorsque votre rôle le permet.

---

# 17. Opérations

L'onglet **Opérations** permet de choisir un groupe ou une équipe puis affiche plusieurs sous-onglets selon les droits et le contenu :

- **Ordres**
- **Annonces**
- **Rôles**
- **Partage entre équipes**
- **Sessions**
- **Historique**

## 17.1 Ordres

Affiche les ordres actifs avec :

- type ;
- priorité ;
- texte ;
- état de réponse.

Lorsqu'un accusé est requis, le bouton **Reçu** permet d'accuser réception depuis cette vue.

## 17.2 Annonces

Affiche les annonces actives.

Chaque annonce peut comporter :

- type ;
- texte ;
- état épinglé ;
- bouton **Accuser réception**.

Un membre autorisé peut créer une annonce en choisissant :

### Types

- Information
- Important
- Information du groupe
- Information de session
- Règle de l'activité
- Coordination

### Expiration

- 15 min
- 1 h
- 4 h
- 24 h
- Sans expiration

Une case permet d'**Épingler l'annonce**.

---

# 18. Campagnes de rôles

Les campagnes de rôles permettent d'ouvrir temporairement des places pour un rôle donné.

Elles se trouvent dans :

**Menu du groupe/équipe > Opérations > Rôles**

## 18.1 Rejoindre une campagne

Une campagne ouverte affiche :

- le rôle ;
- son état ;
- le mode ;
- le nombre de places déjà attribuées / capacité.

Appuyez sur **Rejoindre** pour demander le rôle.

## 18.2 Modes de campagne

### Premières demandes valides — `FIRST_VALID`

Les premières demandes éligibles sont attribuées automatiquement jusqu'à la capacité disponible.

Le code n'autorise ce mode que pour les rôles considérés comme non privilégiés.

### Validation par un responsable — `ADMIN_APPROVAL`

Les demandes restent en attente jusqu'à validation par un responsable.

Le gestionnaire voit **Demandes en attente** et peut appuyer sur **Approuver** pour chaque participant.

## 18.3 Créer une campagne

Si votre rôle autorise la gestion des campagnes :

1. choisissez le **Rôle** ;
2. choisissez le **Mode** proposé pour ce rôle ;
3. choisissez le nombre de **Places** de 1 à 64 ;
4. choisissez la **Durée** :
   - 15 min ;
   - 1 h ;
   - 4 h ;
   - 24 h ;
5. appuyez sur **Ouvrir une campagne**.

## 18.4 Fermer une campagne

Un gestionnaire autorisé peut appuyer sur **Fermer**.

## 18.5 Retirer sa demande

Dans **Historique**, une demande encore en attente peut afficher **Retirer ma demande**.

## 18.6 Rôles disponibles pour les campagnes

Le code expose aux campagnes, selon le contexte et vos droits :

- Éclaireur du groupe ;
- Éclaireur d'équipe ;
- Relais ;
- Couverture ;
- Assaut.

Le rôle de Chef de groupe n'est jamais attribué par campagne.

---

# 19. Sessions

Une session représente une période opérationnelle limitée dans le groupe.

## 19.1 Créer une session

Depuis **Gestion**, si vous disposez de la permission :

1. ouvrez la section **Session** ;
2. entrez la durée en minutes ;
3. la durée maximale affichée est de **56 jours** ;
4. appuyez sur **Créer une session**.

## 19.2 Consulter les sessions

Dans **Opérations > Sessions**, LETCOOR affiche :

- date de création ;
- état : ouverte/terminée ou état d'affectation ;
- votre équipe éventuelle ;
- fin prévue.

## 19.3 Gérer une session

Le responsable autorisé peut :

- ajouter **+ 1 h** ;
- **Terminer** la session.

## 19.4 Rôles et affectations pendant une session

Dans **Participants**, vous pouvez choisir une session administrée, attribuer des rôles limités à cette session et affecter les participants à une équipe/état.

---

# 20. Partage de données entre équipes

Cette fonction est disponible depuis une **équipe** dans :

**Opérations > Partage entre équipes**

Elle ne donne pas automatiquement accès au contenu privé d'une autre équipe. Elle utilise une offre de partage explicitement créée et acceptée.

## 20.1 Proposer un partage

1. Choisissez l'**Équipe cible**.
2. Choisissez les **Données partagées**.
3. Choisissez la précision.
4. Réglez la cadence.
5. Réglez l'expiration.
6. Appuyez sur **Proposer le partage**.

## 20.2 Classes de données disponibles

- Présence générale de l'équipe
- Signal
- État de l'équipe
- Position précise
- Historique des déplacements

## 20.3 Précision

- Vue d'ensemble / agrégée
- Approximative
- Précise

Si **Position précise** est sélectionnée, la précision devient nécessairement précise dans l'interface.

## 20.4 Cadence

Réglable entre **5 et 300 secondes**, par pas de 5 secondes.

## 20.5 Expiration

- 15 min
- 1 h
- 4 h
- 24 h

## 20.6 Accepter ou révoquer

L'équipe destinataire autorisée peut appuyer sur **Accepter**.

Une offre ou un partage peut être **Révoqué** par le côté disposant de la permission correspondante.

---

# 21. Gestion du groupe et des équipes

L'onglet **Gestion** centralise les fonctions administratives.

## 21.1 Sélectionner un espace

Le sélecteur **Groupe ou équipe** permet de choisir l'espace à administrer.

## 21.2 Rejoindre une équipe existante

Lorsque l'action est autorisée, une équipe peut proposer :

- **Rejoindre** ;
- **Récupérer l'accès** lorsque l'adhésion existe mais que les clés doivent être récupérées.

## 21.3 Quitter une équipe

Appuyez sur **Quitter l'équipe** puis vérifiez le résumé avant de confirmer.

## 21.4 Dissoudre une équipe

Un responsable autorisé voit **Dissoudre l'équipe**.

La confirmation indique que :

- l'équipe sera dissoute pour ses membres ;
- les membres restent dans le groupe ;
- les autres appareils appliquent la dissolution lorsqu'ils la reçoivent.

## 21.5 Quitter un groupe

Un membre ordinaire peut préparer un plan de départ puis confirmer.

Si le participant dirige des équipes, LETCOOR peut devoir dissoudre ces équipes avant son départ selon le plan calculé par le Core.

## 21.6 Dissoudre un groupe

Le chef de groupe autorisé peut utiliser **Dissoudre le groupe**.

La confirmation avertit que le groupe et ses équipes seront dissous. Les appareils hors ligne devront se reconnecter pour recevoir la dissolution.

## 21.7 Rejoindre un nouveau groupe ou une nouvelle équipe

La page **Gestion** contient aussi un bloc **Rejoindre un groupe ou une équipe** avec le même système d'invitation que l'onboarding.

## 21.8 Invitations en attente

Lorsque le Core expose des invitations à accepter, elles apparaissent avec un bouton **Accepter** jusqu'à expiration.

## 21.9 Statut d'équipe

Le responsable autorisé peut publier :

- Prêt
- En déplacement
- En position
- En rassemblement
- Besoin d'aide
- Déconnecté

## 21.10 Politique de position exacte

Dans une équipe, un responsable autorisé peut choisir :

- **Autoriser** ;
- **Refuser**

pour la politique de position exacte de l'équipe.

## 21.11 Transfert d'administration

Si un transfert d'administration est en attente pour vous, la section affiche **Accepter le transfert d'administration**.

---

# 22. Limites de publication

Dans **Gestion**, les responsables autorisés peuvent régler les limites de publication du groupe ou de l'équipe.

Les limites peuvent être définies :

- par défaut ;
- pour un membre précis.

Paramètres actuellement exposés :

- nombre d'alertes de sécurité actives ;
- signalements par minute ;
- signalements par 4 minutes.

Les valeurs du formulaire vont de 1 à 1000.

---

# 23. Localisation

L'icône **Localisation** apparaît sur la carte lorsque la plateforme fournit la localisation native.

## 23.1 Activer le partage

1. Ouvrez **Localisation**.
2. Sélectionnez **Partager ma localisation**.
3. Réglez la précision.

LETCOOR republie la présence périodiquement pendant que le partage est actif et que l'application peut obtenir la position.

## 23.2 Précision

Le curseur va de **0 m à 1 km**.

- **0 m** : précision disponible sur l'appareil, sans décalage ajouté par LETCOOR.
- valeur supérieure : la position partagée est décalée aléatoirement dans le rayon choisi.

## 23.3 Arrêter le partage

Sélectionnez **Ne pas partager ma localisation**.

Le partage est également arrêté lorsque le contexte change ou lorsque l'application interrompt la présence selon son cycle de vie.

## 23.4 États affichés

- Localisation en cours…
- Partage actif avec votre groupe
- Partage en attente de reprise
- Localisation non partagée

> Le partage de localisation n'est pas obligatoire pour rejoindre un groupe, utiliser la carte, envoyer des ordres ou utiliser le mesh.

---

# 24. Notifications

Touchez la **cloche** en haut de l'écran.

Le centre de notifications rassemble :

- événements du groupe ;
- changements de connexion/transport ;
- notices système LETCOOR.

Le badge indique le nombre de notifications non lues.

## 24.1 Lecture

Les notifications sont marquées comme lues lorsqu'elles deviennent suffisamment visibles dans la liste ou lorsque la section correspondante est consultée.

## 24.2 Navigation

Toucher une notification peut ouvrir :

- la section Participants ;
- Équipes ;
- Opérations ;
- un objet de carte ;
- le panneau Commandement.

## 24.3 Notifications système

Les réglages de la cloche permettent d'activer/désactiver les notifications système natives lorsque la plateforme le permet.

---

# 25. Cartes hors ligne

Ouvrez :

**Menu du groupe/équipe > Paramètres > Cartes hors ligne**

## 25.1 Sélectionner une zone

1. Appuyez sur **Sélectionner les tuiles sur la carte**.
2. LETCOOR ferme le panneau et affiche une grille sur la carte.
3. Touchez les cellules à conserver.
4. Le compteur indique le nombre de cellules sélectionnées sur un maximum de 20.
5. Appuyez sur **Valider** pour revenir aux paramètres ou **Annuler**.

## 25.2 Niveau de détail

Le menu **Détail** permet de sélectionner un zoom de 3 à 14.

Une zone trop grande à un niveau de détail élevé peut être refusée. L'interface demande alors de réduire le détail ou de choisir des cellules plus petites.

## 25.3 Installer

Une fois les cellules choisies :

1. appuyez sur **Installer les cellules sélectionnées** ;
2. suivez la progression ;
3. vous pouvez **Annuler le téléchargement**.

## 25.4 Supprimer une carte

Les cartes installées sont listées avec leur zoom et leur taille. Appuyez sur **Supprimer** pour libérer de l'espace.

---

# 26. Connexion réseau et fonctionnement hors ligne

LETCOOR peut utiliser plusieurs transports pour un même réseau logique.

L'interface connaît notamment :

- **Internet direct** ;
- **Internet via relais** ;
- **Réseau local (LAN)** ;
- **Wi‑Fi local** ;
- **Wi‑Fi Direct** ;
- **Bluetooth**.

## 26.1 Mesh logique

LETCOOR n'exige pas que chaque membre soit directement connecté à tous les autres.

Exemple :

```text
Téléphone A ↔ Téléphone B ↔ Téléphone C ↔ Téléphone D
```

Un événement autorisé peut être relayé entre pairs selon la topologie et les règles de portée du groupe/équipe.

Le transport physique et l'identité LETCOOR sont séparés : un pair reste identifié par son identité LETCOOR même si le chemin réseau change.

## 26.2 Hors Internet

Pour maximiser les chances de fonctionner hors Internet :

- activez le Wi‑Fi ;
- activez le Bluetooth ;
- autorisez les appareils à proximité ;
- autorisez le réseau local si Android le demande ;
- acceptez la visibilité/appairage système lorsque LETCOOR le demande ;
- gardez LETCOOR au premier plan lors de la première connexion ;
- rapprochez les appareils pendant le bootstrap initial ;
- ne refusez pas les dialogues système nécessaires à la radio de proximité.

## 26.3 État des transports de proximité

LETCOOR peut afficher séparément :

- Wi‑Fi local ;
- Wi‑Fi Direct ;
- Bluetooth ;

avec des états tels que :

- autorisation requise ;
- activation requise ;
- initialisation ;
- prêt ;
- recherche ;
- pair trouvé ;
- connexion ;
- groupe formé ;
- authentification LETCOOR ;
- connecté ;
- récupération ;
- indisponible.

## 26.4 Wi‑Fi Direct occupé

Si Android indique que Wi‑Fi Direct est occupé, LETCOOR peut tenter une récupération. L'écran d'information Wi‑Fi Direct conseille notamment de vérifier :

- que le Wi‑Fi est actif ;
- que le partage de connexion n'entre pas en conflit avec Wi‑Fi Direct ;
- qu'une autre recherche/connexion Wi‑Fi Direct n'est pas déjà en cours.

## 26.5 Le réseau peut changer de transport

Le statut en haut de l'écran peut afficher différents transports au cours de la session. LETCOOR peut disposer de routes alternatives vers un pair et utiliser la route disponible selon l'état réseau.

---

# 27. Confidentialité, verrouillage et récupération

LETCOOR applique plusieurs comportements de protection lorsque les données privées d'un groupe ne peuvent plus être vérifiées auprès d'autres membres.

## 27.1 Verrouillage après absence

Le code de l'interface prévoit un écran :

**Session verrouillée après une minute d'absence.**

Appuyez sur **Se reconnecter** pour reprendre l'accès.

## 27.2 Vérification de connexion aux membres

Lorsqu'une récupération de confidentialité est nécessaire, LETCOOR affiche :

**Vérification de la connexion aux membres…**

Il tente de retrouver un membre joignable et peut afficher le détail des transports de proximité.

## 27.3 Suppression automatique locale

Pour certains groupes configurés avec récupération automatique, si aucune reconnexion n'est possible pendant la période prévue, les données locales du groupe peuvent être supprimées **après vérification**.

L'interface actuelle annonce une échéance de vingt minutes pour les groupes concernés.

Vous pouvez, lorsqu'elle est proposée :

- supprimer/réinitialiser les données locales ;
- ou choisir **Conserver les données à mes risques**, ce qui désactive la suppression automatique pour ce contexte.

LETCOOR avertit que conserver ces données peut augmenter le risque en cas de compromission physique de l'appareil.

## 27.4 Protection desktop

Sur desktop, la vue privée peut être masquée/floutée lorsque la fenêtre perd le focus puis rafraîchie avant réaffichage.

---

# 28. Rôles disponibles

Le modèle de domaine LETCOOR définit neuf rôles.

| Rôle | Fonction générale dans le code actuel |
|---|---|
| **Chef de groupe** (`GROUP_ADMIN`) | Administration du groupe, création d'équipes et sessions, gestion des membres/rôles, campagnes, dissolution, transfert d'administration, annonces. |
| **Coordinateur du groupe** (`GROUP_LEADER`) | Coordination au niveau groupe, ordres/objectifs/signalements de groupe, campagnes et annonces selon permissions. |
| **Chef d'équipe** (`TEAM_LEADER`) | Ordres/objectifs/rendez-vous/statut de son équipe, partage inter-équipe, annonces, campagnes d'équipe. |
| **Éclaireur du groupe** (`GROUP_SCOUT`) | Signalement et confirmation/promotion au niveau groupe selon permissions. |
| **Éclaireur d'équipe** (`TEAM_SCOUT`) | Rapport/signalement d'équipe, confirmation et promotion selon permissions. |
| **Relais** (`TRANSMITTER`) | Capacité de relais prévue par le domaine et publication de certaines présences résumées selon politique ; ce rôle n'accorde pas l'accès aux données privées d'autres équipes. |
| **Couverture** (`COVER`) | Étiquette opérationnelle avec les capacités de base du membre. |
| **Assaut** (`ATTACKER`) | Étiquette opérationnelle avec les capacités de base du membre. |
| **Membre** (`MEMBER`) | Capacités de base : signalement normal dans son équipe lorsque permis, alerte sécurité, réponse aux ordres, présence autorisée et participation aux campagnes. |

> Les permissions sont calculées par le Core et sont additives. L'interface n'affiche que les actions réellement autorisées. Appartenir à un groupe ne donne pas automatiquement accès aux données privées de toutes ses équipes.

---

# 29. Conseils de préparation avant une activité

Pour une utilisation réelle, en particulier dans une zone où Internet peut être mauvais :

1. Installez la même version de LETCOOR sur les appareils.
2. Créez le groupe avant le début de l'activité.
3. Faites rejoindre les participants tant qu'ils sont physiquement proches.
4. Acceptez les permissions de proximité sur chaque Android.
5. Activez Bluetooth et Wi‑Fi.
6. Testez au moins une connexion sans données mobiles si le fonctionnement hors ligne est important.
7. Créez les équipes et attribuez les chefs avant de vous disperser.
8. Ouvrez une session si vous souhaitez des rôles/affectations de session et l'historique correspondant.
9. Téléchargez les cartes hors ligne nécessaires avant de perdre Internet.
10. Vérifiez que les participants savent ouvrir :
    - Notifications ;
    - Commandement ;
    - leur équipe ;
    - la fonction Alerte sécurité.
11. N'activez le partage de localisation que si vous souhaitez réellement le publier.

---

# 30. Dépannage

## Les deux appareils ne se voient pas hors ligne

Vérifiez sur les deux appareils :

- Wi‑Fi activé ;
- Bluetooth activé ;
- permissions **Appareils à proximité** accordées ;
- permission réseau local accordée si Android la demande ;
- app visible/détectable si le système demande une confirmation ;
- LETCOOR au premier plan pendant la recherche initiale.

Si Android ouvre les réglages de localisation, activez le service de localisation pour maximiser la compatibilité de découverte. Cela n'active pas le partage de position LETCOOR.

## « Wi‑Fi Direct indisponible » ou « occupé »

- désactivez temporairement un partage de connexion/hotspot manuel ;
- attendez quelques secondes ;
- relancez la tentative ;
- vérifiez qu'une autre application ou connexion Wi‑Fi Direct n'est pas active.

## Le QR ne fonctionne pas

- attendez que toutes les parties du QR aient été lues ;
- rapprochez les écrans ;
- augmentez la luminosité de l'écran affichant le QR ;
- utilisez le curseur de zoom de la caméra ;
- utilisez le lien à la place du QR si nécessaire.

## La caméra est refusée

- utilisez le lien ;
- ou ouvrez les réglages caméra de Windows/Android depuis LETCOOR quand le bouton est proposé.

## Le lien est accepté mais la connexion expire

- vérifiez Internet ou la proximité ;
- rapprochez les appareils ;
- activez Wi‑Fi et Bluetooth ;
- acceptez les dialogues système ;
- appuyez sur **Réessayer** lorsque le bouton apparaît.

## Je suis dans le groupe mais pas dans une équipe

Ouvrez :

**Contexte > Équipes** ou **Gestion**.

Si l'équipe autorise l'adhésion, utilisez **Rejoindre**. Une invitation d'équipe peut également admettre directement le participant dans le groupe parent et l'équipe ciblée selon le ticket reçu.

## « Adhésion enregistrée · réception des clés en cours »

La membership est connue, mais l'accès cryptographique de l'équipe n'est pas encore prêt. Laissez les appareils connectés pour permettre la récupération/synchronisation des clés. Si le bouton **Récupérer l'accès** apparaît dans Gestion, utilisez-le.

## Un objet n'est pas visible

Vérifiez :

- le groupe/équipe sélectionné ;
- vos permissions ;
- l'expiration de l'objet ;
- la synchronisation réseau ;
- le fait qu'un objet privé d'équipe n'est pas automatiquement visible par les autres équipes.

## La localisation ne s'affiche pas

- vérifiez l'autorisation de localisation ;
- vérifiez que **Partager ma localisation** est sélectionné ;
- vérifiez le groupe courant ;
- attendez la prochaine publication périodique ;
- vérifiez que la politique de l'équipe autorise la précision nécessaire.

---

# 31. Résumé rapide

## Pour rejoindre LETCOOR

```text
Invitant
  ↓
Inviter
  ↓
QR ou lien
  ↓
Appareil invité importe
  ↓
Appareil invité produit une réponse
  ↓
L'invitant scanne/colle la réponse
  ↓
Connexion + authentification + admission
```

## Pour créer quelque chose sur la carte

```text
Appui long sur la carte
  ↓
Signalement / Objectif / Ordre / Rassemblement / Alerte sécurité
  ↓
Remplir le formulaire
  ↓
Choisir zone / durée si disponible
  ↓
Publier
```

## Pour gérer un groupe

```text
Nom du groupe en haut à gauche
  ↓
Contexte | Équipes | Participants | Inviter | Opérations | Gestion | Paramètres
```

## Pour une campagne de rôle

```text
Opérations
  ↓
Rôles
  ↓
Choisir rôle + mode + places + durée
  ↓
Ouvrir une campagne
  ↓
Les membres rejoignent
  ↓
Attribution automatique ou validation responsable selon le mode
```

## Pour fonctionner sans Internet

```text
Wi‑Fi ON
Bluetooth ON
Permissions de proximité autorisées
Réseau local autorisé si demandé
Appairage/visibilité accepté si demandé
Appareils proches au premier contact
LETCOOR ouvert au premier plan
```

LETCOOR peut ensuite utiliser les transports disponibles et relayer les informations autorisées entre pairs selon la topologie du mesh.

---

**LETCOOR 1.0.0 — Documentation utilisateur**
