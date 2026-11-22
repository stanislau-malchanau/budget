---
title: Politique de confidentialité de Budget
lang: fr
---

# Politique de confidentialité de Savings Challenge & Budget

*Ceci est une traduction. En cas de divergence avec la [version anglaise](../privacy), la version anglaise prévaut.*

Date d’entrée en vigueur : 2026-11-22

Cette politique explique comment Savings Challenge & Budget (affichée « Budget » sur votre écran d’accueil, l’« App »), développée par Stanislau Malchanau (« nous »), traite vos informations. En bref : **nous ne collectons, ne vendons ni ne partageons vos données personnelles. Votre budget reste sur votre appareil et dans votre propre compte iCloud. L’App ne détient ni ne transfère d’argent, n’est reliée à aucune banque et ne donne pas de conseils financiers.**

## 1. Données conservées par l’App

L’App conserve sur votre appareil : vos dépenses, revenus et remboursements (le montant, sa devise et le taux de change utilisé, la catégorie, une note, la date, l’heure et le fuseau horaire, et la façon dont l’opération a été ajoutée, par exemple saisie à la main, depuis un ticket de caisse ou depuis Apple Pay), vos catégories et leurs plafonds, votre budget mensuel et ses réglages (le jour où commence votre mois, le report ou non de ce qui reste), vos paiements récurrents, vos objectifs d’épargne avec ce que vous y avez versé et ce que vous en avez retiré, vos défis d’épargne, les taux de change que vous avez saisis vous-même, le budget partagé que vous tenez avec une personne que vous invitez (section 3), vos réponses aux questions du premier lancement et vos réglages (l’heure du rappel, le verrou Face ID, les sons et les vibrations). Les opérations supprimées restent 30 jours dans « Supprimés récemment » pour que vous puissiez les récupérer.

Ces données décrivent la façon dont vous dépensez et épargnez, et certaines lois les considèrent comme des informations financières ou sensibles. Elles ne quittent jamais votre appareil et votre compte iCloud (sections 2 et 3). Nous n’exploitons aucun serveur qui reçoit vos données, nous n’y avons pas accès, et l’App n’envoie jamais vos opérations à un service d’IA en ligne ni à qui que ce soit. Le seul petit serveur que nous exploitons (section 6) fournit des taux de change et signe des offres de réduction ; il ne reçoit jamais vos données.

## 2. Synchronisation iCloud

Si vous êtes connecté à iCloud, l’App synchronise votre budget via CloudKit d’Apple, dans la base de données privée de votre propre compte iCloud, afin qu’il soit là sur un nouveau téléphone et après une réinstallation. Ces données sont stockées et protégées par Apple conformément à la Politique de confidentialité d’Apple (https://www.apple.com/legal/privacy/). Nous ne pouvons ni les voir, ni les lire, ni les exporter. Lorsque quelque chose change dans iCloud, le service push d’Apple peut réveiller l’App pour qu’elle récupère la modification ; cette notification ne contient aucune de vos données. Vous pouvez désactiver la synchronisation dans Réglages iOS > [votre nom] > iCloud ; votre budget reste alors uniquement sur cet iPhone.

## 3. Le budget partagé

Vous pouvez inviter une personne à un budget que vous tenez ensemble. L’invitation est un lien iCloud que vous envoyez vous-même, et le budget partagé est stocké par Apple dans une zone partagée CloudKit que vous êtes tous les deux seuls à pouvoir ouvrir. Ce que l’un de vous y ajoute est vu par l’autre, et chaque opération indique qui l’a ajoutée ; votre propre budget n’est jamais partagé. Si vous saisissez un nom pour le budget partagé, l’autre personne le voit avec vos opérations ; il est stocké avec votre budget dans votre compte iCloud et dans la zone partagée. L’App indique à la personne invitée si votre abonnement est actif, afin qu’elle puisse ajouter gratuitement des opérations au budget partagé (section 2 des Conditions d’utilisation). Chacun de vous peut quitter ou fermer le budget partagé dans l’App à tout moment. Si vous cessez le partage, l’autre personne peut conserver une copie en lecture seule de ce que contenait le budget partagé jusque-là. Lorsqu’Apple signale à l’App que l’autre personne a ajouté quelque chose, la notification passe par le service push d’Apple.

## 4. Scanner de tickets et appareil photo

L’App n’utilise l’appareil photo que lorsque vous ouvrez le scanner de tickets, et iOS vous demande votre autorisation la première fois. La photo du ticket est lue sur votre iPhone : le framework Vision d’Apple y trouve le texte et un éventuel code QR et, sur les iPhone dotés d’Apple Intelligence, le modèle de langage d’Apple qui fonctionne sur l’appareil aide à trouver le total, la devise et le nom du magasin. La photo et le texte reconnu ne restent dans la mémoire du téléphone que le temps de leur lecture et sont effacés juste après. Ils ne sont jamais enregistrés, jamais mis en ligne et jamais envoyés, ni à nous ni à aucun service en ligne. Seule la dépense que vous enregistrez ensuite (son montant, sa devise, sa date et le nom du magasin dans la note) est conservée, comme toute autre opération.

## 5. Apple Pay via Raccourcis

L’App ne lit ni l’app Cartes (Wallet), ni vos cartes, ni votre banque. Si vous choisissez de configurer une automatisation personnelle dans l’app Raccourcis d’Apple avec son déclencheur « Transaction », chaque fois que vous payez avec Apple Pay dans un magasin, Raccourcis transmet le montant et le nom du commerçant à l’action de l’App qui ajoute une dépense, sur le même iPhone, et l’App en fait une dépense. Rien de tout cela ne nous est envoyé ; l’opération est conservée et synchronisée comme toute autre (sections 1 et 2). Rien ne se passe tant que vous n’avez pas configuré l’automatisation vous-même, et vous pouvez la modifier ou la supprimer dans Raccourcis à tout moment.

## 6. Taux de change et offres de réduction (notre serveur)

Nous exploitons un seul petit serveur, sur Cloudflare Workers, pour deux tâches. Pour aucune des deux, il ne reçoit vos données.

- **Taux de change.** Lorsqu’une dépense est dans une autre devise que votre devise principale, ou que vous changez de devise principale, l’App demande au serveur les taux de ce jour-là. La requête ne contient que la date : aucun montant, aucune devise et rien sur vous. Le serveur prend les taux de référence du jour publiés par la Banque centrale européenne et, pour les devises que la banque ne publie pas, des taux de banques centrales rassemblés par le service ouvert Frankfurter, puis renvoie le tableau complet de ce jour ; votre iPhone y choisit le taux dont il a besoin. Les dépenses dans votre devise principale n’ont jamais besoin du serveur.
- **Offres de réduction.** Si vous désactivez le renouvellement, l’App peut vous proposer un prix plus bas pour votre prochaine période (section 2 des Conditions d’utilisation). Apple exige qu’une telle offre soit signée par nous ; juste avant l’achat, l’App n’envoie donc au serveur que l’identifiant de l’App elle-même, les identifiants de la formule et de l’offre et, lorsqu’Apple le demande, le numéro attribué par l’App Store à votre achat d’abonnement en cours. Le serveur y ajoute un nombre aléatoire à usage unique, signe le tout, répond et ne conserve rien. Il n’apprend rien sur votre identité : ni nom, ni compte Apple, ni aucune de vos données.

Comme tout serveur, le nôtre voit l’adresse IP d’une requête pour pouvoir y répondre. Il n’enregistre cette adresse nulle part dans ce qu’il conserve et ne relie pas les requêtes à une personne. Cloudflare, qui fait fonctionner le serveur, peut conserver des journaux techniques de courte durée des requêtes, pour la sécurité et la fiabilité, selon sa propre politique de confidentialité (https://www.cloudflare.com/privacypolicy/).

## 7. Notifications et widgets

Le rappel du soir est programmé sur votre iPhone, et seulement si vous autorisez les notifications. Aucune donnée ne nous est envoyée pour le délivrer. Les widgets lisent votre budget sur votre appareil.

## 8. Verrou Face ID

Si vous activez le verrou, l’App demande à iOS de vérifier votre Face ID, ou votre code. Face ID est entièrement géré par iOS : l’App ne voit jamais les données de votre visage et apprend seulement si la vérification a réussi.

## 9. Achats

Les abonnements sont vendus et traités par Apple via l’App Store. Nous ne recevons pas vos informations de paiement. Apple indique à l’App si votre abonnement est actif, quelle formule vous avez choisie et son prix, si le renouvellement est activé et si une offre est disponible pour votre compte Apple ; la section 10 précise ce qui en est transmis à nos statistiques d’utilisation.

## 10. Statistiques d’utilisation et rapports de plantage

Pour savoir quelles fonctions aident et où l’App gêne, l’App envoie des signaux d’utilisation anonymes à TelemetryDeck, un service d’analyse de TelemetryDeck GmbH (Augsbourg, Allemagne) dont les serveurs sont dans l’UE. Son code est le seul code de l’App qui ne vient ni d’Apple ni de nous. Un signal désigne une action dans l’App : par exemple, qu’une étape du premier lancement a été terminée et laquelle de ses réponses à choix multiple a été choisie (ce qui vous gênait auparavant, si vous avez fixé un budget mensuel, le jour où commence votre mois, le type de votre premier objectif choisi dans la liste et dans combien de mois), combien de temps a pris la première dépense, qu’une dépense ou un revenu a été ajouté et comment (saisi à la main, depuis un widget, un ticket de caisse, Apple Pay ou un fichier) et s’il était dans votre devise principale, qu’un objectif a été créé (son type choisi dans la liste et s’il a une date), que de l’argent a été mis de côté, qu’un défi a été lancé ou qu’une case a été cochée, qu’une fenêtre a été ouverte ou qu’un fichier a été importé (avec un nombre approximatif de ses lignes), que l’écran d’abonnement ou une offre a été affiché, qu’une formule a été choisie ou qu’un abonnement a commencé, a été renouvelé ou restauré, que l’App a demandé une note, ou, sous forme de code d’erreur court, que quelque chose n’a pas fonctionné, par exemple que l’App Store n’a pas répondu. Il est accompagné d’un horodatage arrondi à l’heure et de détails techniques généraux : les versions de l’App et d’iOS, le modèle de l’appareil, la langue, la région et le fuseau horaire, et des réglages d’affichage et d’accessibilité comme le mode sombre ou la taille du texte. Lorsqu’un abonnement commence ou est renouvelé, son signal comporte aussi la formule, son prix converti en dollars américains, la devise et le pays de votre App Store, afin que nous voyions quelles formules les gens choisissent.

Un signal ne contient jamais vos montants, vos soldes ou les chiffres de votre budget, vos catégories, vos notes ou les noms de vos objectifs, les noms des magasins ou des commerçants, les photos de tickets ou leur texte, les taux de change que vous avez saisis, ni votre nom, votre adresse e-mail, votre compte Apple ou votre position, ni quoi que ce soit sur la personne avec qui vous partagez un budget. Votre installation n’est identifiée que par un identifiant aléatoire que l’App sale et hache avant l’envoi, de sorte que les signaux ne peuvent pas remonter jusqu’à vous ni vous suivre d’une app à l’autre. TelemetryDeck ne conserve aucune adresse IP et n’utilise pas de cookies. Nous n’utilisons ces signaux que comme statistiques pour améliorer l’App ; nous ne les vendons pas, ne les partageons pas avec des annonceurs et ne les utilisons pas pour vous suivre. L’App ne contient aucun code publicitaire ou de suivi et ne vous suit pas à travers d’autres apps ou sites web.

Par ailleurs, si vous choisissez de partager des analyses avec les développeurs d’apps dans Réglages iOS > Confidentialité et sécurité > Analyses et améliorations, Apple peut nous fournir des statistiques d’utilisation et des rapports de plantage agrégés et anonymes. Ils ne vous identifient pas.

## 11. Game Center

Si vous êtes connecté à Game Center, les succès liés à vos paliers d’épargne sont transmis à Game Center d’Apple sous votre compte Game Center et traités conformément à la Politique de confidentialité d’Apple. Un succès indique seulement qu’un palier a été franchi ; vos opérations, vos notes et les noms de vos objectifs ne sont pas envoyés. Nous ne recevons pas votre identité Game Center.

## 12. Import et export

L’export de vos dépenses et revenus dans un fichier CSV, et l’import d’un fichier CSV venant d’une autre app de budget, se font sur votre appareil. L’App ne lit que le fichier que vous choisissez, et un fichier exporté ne va que là où vous l’envoyez avec la feuille de partage.

## 13. Ce que l’App ne fait pas

L’App ne détient, ne transfère, n’investit ni ne prête d’argent. Elle n’est reliée à aucune banque, carte ou compte de paiement, et elle ne donne pas de conseils financiers, fiscaux ou en investissement. Elle ne lit ni l’app Cartes (Wallet), ni votre position, ni vos contacts, ni votre photothèque, ni votre micro, et elle n’a ni compte, ni connexion, ni publicité, ni messagerie, ni fil public.

## 14. Enfants

L’App convient à tous les âges (classée 4+) et ne collecte sciemment aucune information personnelle auprès de quiconque, y compris les enfants de moins de 13 ans (ou l’âge équivalent dans votre pays).

## 15. Conservation et suppression des données

Les données restent tant que vous les gardez. Vous pouvez supprimer une opération dans l’App à tout moment ; elle attend 30 jours dans « Supprimés récemment », puis disparaît. Vous pouvez tout supprimer en supprimant l’App et, pour les données synchronisées, dans Réglages iOS > [votre nom] > iCloud > Gérer le stockage du compte > Budget. Ce que vous avez ajouté à un budget partagé y reste pour l’autre personne jusqu’à ce que l’un de vous le supprime ou que le budget partagé soit fermé. Comme nous ne détenons aucune copie, il n’y a rien d’autre à supprimer de notre côté. Les signaux d’utilisation sont anonymes et ne peuvent pas vous être associés, et notre serveur ne conserve rien sur vous ; il n’existe donc, ni d’un côté ni de l’autre, aucun dossier personnel à consulter ou à supprimer.

## 16. Vos droits

Selon l’endroit où vous vivez (par exemple en vertu du RGPD dans l’UE, du UK GDPR, du CCPA/CPRA en Californie, de l’APPI au Japon, de la PIPA en Corée ou de la LGPD au Brésil), vous pouvez avoir le droit d’accéder à vos données personnelles, de les rectifier, de les supprimer ou d’en obtenir la portabilité, ainsi que de vous opposer à leur traitement ou de le limiter. Comme nous ne détenons pas vos données, vous pouvez exercer ces droits directement sur votre appareil et dans iCloud comme décrit ci-dessus ; l’export CSV dans les Réglages vous donne toutes vos dépenses et tous vos revenus en un seul fichier. Vous pouvez aussi nous contacter pour toute demande ou question, et vous pouvez déposer une plainte auprès de votre autorité locale de protection des données.

Nous ne vendons ni ne partageons d’informations personnelles au sens du CCPA/CPRA.

## 17. Modifications

Si cette politique change, nous mettrons à jour la date d’entrée en vigueur ci-dessus et, pour les changements importants, nous vous en informerons dans l’App.

## 18. Contact

Stanislau Malchanau, Biélorussie
E-mail : 7tam.official@gmail.com
