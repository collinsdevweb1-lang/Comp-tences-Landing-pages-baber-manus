---
name: barbershop-site-generator
description: Création automatique de landing pages modernes pour barbershops à partir d'un lien Google Maps. Analyse les données du salon (nom, photos, avis, horaires) et génère un site web responsive, optimisé pour le SEO et prêt à l'exportation.
---

# Générateur de site Barbershop depuis Google Maps

Cette compétence permet de transformer une fiche Google Maps de barbershop en un site web professionnel complet.

## Workflow d'utilisation

### 1. Analyse des données (Entrée)
Lorsqu'un utilisateur fournit un lien Google Maps, effectuez les actions suivantes :
- **Extraction des données** : Utilisez le navigateur pour récupérer le nom du salon, l'adresse, le téléphone, les horaires, la description et les avis clients (3 à 5 avis récents).
- **Analyse visuelle** : Identifiez le style du salon (moderne, vintage, industriel) et les couleurs dominantes à partir des photos de la façade et du logo.
- **Sélection d'images** : Identifiez les meilleures photos pour la section Hero (façade ou intérieur) et la galerie.

### 2. Conception et Design
- **Palette de couleurs** : Si aucune couleur n'est évidente, utilisez une palette classique : Noir (#1a1a1a), Blanc (#f5f5f5), et Or (#c5a059) ou Rouge/Bleu Barber Pole.
- **Structure** : Utilisez le template situé dans `templates/landing_page_template.html` comme base.
- **Placeholders** : Laissez des sections claires pour les services et la galerie que l'utilisateur pourra personnaliser.

### 3. Génération du Code
- **SEO** : Générez des balises `<title>` et `<meta description>` optimisées localement (ex: "Meilleur Barbershop à [Ville] - [Nom du Salon]").
- **Accessibilité** : Ajoutez des attributs `alt` descriptifs à toutes les images extraites.
- **Performance** : Structurez le code pour un chargement rapide (Tailwind CSS via CDN, lazy-loading des images).

## Directives de contenu

| Section | Contenu requis |
| :--- | :--- |
| **Hero** | Nom du salon, phrase d'accroche percutante, bouton CTA "Réserver". |
| **Services** | Liste de services génériques (Coupe, Barbe) avec prix à compléter. |
| **Avis** | Intégration fidèle des avis Google (nom, note, texte). |
| **Contact** | Boutons directs pour WhatsApp et Appel, formulaire de contact simple. |
| **Localisation** | Carte interactive (iframe) et lien d'itinéraire. |

## Ressources de la compétence

- `templates/landing_page_template.html` : Structure HTML/Tailwind de base.

## Contraintes
- **Fidélité** : Ne jamais inventer d'informations (horaires, téléphone). Si une donnée manque, demandez à l'utilisateur.
- **Images** : Utilisez uniquement les URLs d'images provenant de Google Maps ou des placeholders de haute qualité si nécessaire.
- **Export** : Le résultat final doit être un fichier HTML unique ou un projet React prêt à être déployé sur GitHub/Vercel.
