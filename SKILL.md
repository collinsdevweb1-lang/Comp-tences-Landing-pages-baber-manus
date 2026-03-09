# Barbershop Site Generator (React/Vite)

Cette compétence permet de transformer une fiche Google Maps de barbershop en un site web professionnel complet et responsive, basé sur **React (avec Vite) et Tailwind CSS**.

## Workflow d'utilisation

### 1. Analyse des données (Entrée)
Lorsqu'un utilisateur fournit un lien Google Maps, effectuez les actions suivantes :
- **Extraction des données** : Utilisez le navigateur pour récupérer le nom du salon, l'adresse, le téléphone, les horaires, la description et les avis clients (3 à 5 avis récents).
- **Analyse visuelle** : Identifiez le style du salon (moderne, vintage, industriel) et les couleurs dominantes à partir des photos de la façade et du logo.
- **Sélection d'images** : Identifiez les meilleures photos pour la section Hero (façade ou intérieur) et la galerie.

### 2. Initialisation du Projet
- **Scaffold** : Utilisez l'outil `webdev_init_project` avec le scaffold `web-static` pour créer un nouveau projet React + TypeScript + Tailwind CSS.
- **Nom du projet** : Utilisez une version simplifiée du nom du salon (ex: `new-land-barber-house`).

### 3. Génération des Composants
- **Structure** : Créez des composants React distincts pour chaque section de la page (`Hero.tsx`, `Services.tsx`, `Gallery.tsx`, `Reviews.tsx`, `Contact.tsx`, `Map.tsx`, `Footer.tsx`).
- **Props** : Passez les données extraites de Google Maps (nom, adresse, etc.) aux composants via les props.
- **Styling** : Utilisez les classes Tailwind CSS directement dans le JSX pour styler les composants. La palette de couleurs doit être configurable.

### 4. Intégration et Finalisation
- **Assemblage** : Importez et assemblez tous les composants dans le fichier principal `App.tsx`.
- **SEO** : Utilisez `react-helmet` ou une technique similaire pour gérer les balises `<title>` et `<meta description>` de manière dynamique.
- **Accessibilité** : Assurez-vous que tous les éléments interactifs sont accessibles et que les images ont des attributs `alt` descriptifs.

## Directives de contenu

| Composant | Contenu requis |
| :--- | :--- |
| **Hero.tsx** | Nom du salon, phrase d'accroche, bouton CTA "Réserver". |
| **Services.tsx** | Liste des services et prix extraits de l'image ou de la description. |
| **Reviews.tsx** | Intégration des avis Google (nom, note, texte). |
| **Contact.tsx** | Boutons pour WhatsApp/Appel, formulaire de contact simple. |
| **Map.tsx** | Carte interactive (iframe) et lien d'itinéraire. |

## Contraintes

- **Fidélité** : Ne jamais inventer d'informations. Si une donnée manque, demandez à l'utilisateur ou utilisez un placeholder évident.
- **Dépendances** : Limitez l'ajout de nouvelles dépendances. Privilégiez les solutions natives de React et Tailwind CSS.
- **Export** : Le résultat final doit être un projet React complet, prêt à être zippé et envoyé à l'utilisateur, avec des instructions claires pour l'installation (`pnpm install`) et le lancement (`pnpm dev`).
