ROUTINE MAJOR — mise en ligne (5 minutes)

1. Sur GitHub, crée un nouveau dépôt (ex. "Routine"), public.
2. Dépose À PLAT à la racine tous les fichiers de ce zip (index.html, manifest.json,
   service-worker.js, icon.svg, icon-192.png, icon-512.png). Pas de sous-dossier.
3. Settings > Pages > Deploy from a branch > main / (root). Attends 1-2 minutes.
4. Ouvre https://nawanem812-boop.github.io/<nom-du-dépôt>/ dans Chrome, puis
   menu ⋮ > "Installer l'application" / "Ajouter à l'écran d'accueil".

POURQUOI LE LIEN AVEC PROGRAMME MAJOR MARCHE
Ton site Programme Major et cette appli seront sur le même domaine (nawanem812-boop.github.io).
Le navigateur partage donc leurs données : la routine lit tes cours (J+0/J+3/J+7/J+30), tes TD,
tes stages et tes QCM en direct, et cocher une révision ou un TD dans la routine le valide dans
Programme Major. Le choix de DA est partagé aussi. Il faut ouvrir les deux depuis le même
navigateur (Chrome). Une appli installée garde en général les mêmes données que Chrome.

SAUVEGARDE (à faire chaque semaine)
Réglages > Exporter : télécharge un fichier .json (et affiche le texte à copier).
- Sur le même domaine que Programme Major, le fichier contient tout (routine + cours + TD + stages
  + QCM). Il peut être réimporté dans Programme Major (Importer) comme dans la routine.
- Importer (routine) : restaure seulement la routine. "Restaurer tout" remet aussi Programme Major.
- Les données sont aussi demandées en stockage "persistant" au navigateur pour limiter les pertes,
  mais seul un export fichier te protège vraiment (cache vidé, nouveau téléphone, désinstallation).

MISE À JOUR : remplace index.html dans le dépôt. Tes données ne sont pas touchées.

NOUVEAUTÉS v2 (d'après ton export Major de promo)
- Rattrapage compressé : un cours resté 3 points de révision en retard ou plus devient UNE tâche « Rattrapage complet » (40 min). La cocher valide les points J+ déjà échus dans Programme Major et ajoute une révision « Rattrapage (Routine Major) » dans le cours.
- Routine recherche & langues (07h15, 30 min, 20 en rattrapage) reprise de ton planning type.
- Journal de stage : le bloc est coché automatiquement s'il existe une entrée à cette date dans Programme Major.
- Sommeil (LIFE-PROJECT-) : si la moyenne des 3 derniers relevés (7 derniers jours) est sous 6 h, le mode Minimal s'active en Auto.
- Suivi > Revue du dimanche : bilan de la semaine (révisions, TD, journal, sommeil, dépenses, retard) avec bouton Copier.
- Importer une sauvegarde sur une autre adresse récupère aussi sommeil et dépenses de LIFE-PROJECT-.
Remplace index.html ET service-worker.js dans le dépôt.

NOTIFICATIONS (v3) + NOUVELLE ICÔNE
- Réglages > Notifications : « Activer les rappels », choix de l'avance (à l'heure, 5, 10, 15, 30 min), sujet ntfy, « Programmer 2 jours », « Tester ».
- Sans ntfy : rappels locaux, seulement si la routine est ouverte ou récemment active (limite des navigateurs).
- Avec ntfy : installe l'appli ntfy, abonne-toi au même sujet (nom long et secret). La routine programme chaque bloc non coché pour aujourd'hui et demain, et se reprogramme à chaque ouverture.
- Remplace TOUS les fichiers du dépôt (icônes comprises). Pour voir la nouvelle icône sur l'écran d'accueil, désinstalle puis réinstalle l'appli (tes données restent dans Chrome).

VERSION 4 — NOUVELLE ORGANISATION + RAPPELS SANS NOTIFICATIONS
- Barre du bas : Jour · Rappels · Semaine · Suivi · Réglages (l'ancien onglet Programme est dans Suivi). En-tête fixe avec anneau d'avancement de la journée. Carte « Maintenant / Ensuite » avec bouton Fait, frise verticale des blocs, réglage du jour replié.
- Onglet Rappels (sans autorisation de notification) : bandeau + son + vibration à l'heure de chaque bloc quand l'appli est ouverte (+10 min / Fait / ✕), pastille sur l'icône si le navigateur le permet.
- Fichier agenda .ics : exporte 1, 2, 7 ou 14 jours de blocs avec une alarme (0 à 30 min avant) dans l'agenda du téléphone : c'est ce qui sonne appli fermée. Réexporter met à jour les mêmes blocs. Google Agenda ignore parfois les alarmes du fichier : règle ses notifications par défaut.
- ntfy reste disponible dans Rappels > Avancé.
- Réglages > Calendrier d'alternance : les semaines après le 22/02/2027 sont en « Cours » par défaut ; corrige-les (Cours / Stage / Vacances).
Remplace TOUS les fichiers du dépôt Routine (index.html, service-worker.js, manifest.json, icônes).

VERSION 5 — FIABILITÉ (phases 1 à 4 du cahier des charges)
- Les mêmes fichiers servent pour Routine et TEST-ROUTINE-TEST : si l'adresse contient « test », l'appli passe en mode TEST (bandeau rouge, clés « test:… », aucune lecture/écriture des cours de Multi-DA).
- Dates : tout est calculé en date locale (le décalage d'un jour vers minuit et sur les jalons J+ est corrigé).
- Restauration : confirmation avec la version/date du fichier, sauvegarde automatique téléchargée avant, clés TEST jamais mélangées à la production.
- Service worker : cache propre à Routine, ne supprime plus les caches des autres applis. Version affichée dans Réglages.

VERSION 6 — ÉCOSYSTÈME
- Bouton 🧭 « Mon écosystème » : accès aux trois applications avec statut (Synchronisé, Données anciennes, Non connecté).
- Suivi > Sommeil et énergie : saisie unique qui alimente LIFE-PROJECT (source officielle des données santé) ; conflit signalé si une valeur différente existe déjà.
