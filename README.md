# www.rondeau-cameira.fr

Page d’accueil statique donnant accès au site personnel de Sébastien
Rondeau-Cameira : https://sebastien.rondeau-cameira.fr/.

## Fichiers

- `index.html` : contenu et métadonnées de la page.
- `contact/index.html` : formulaire de contact HTML envoyé à Formspree.
- `styles.css` : styles de la page, avec affichage mobile et mode sombre.
- `sitemap.xml` : URL publique de la page d’accueil.
- `robots.txt` : accès des robots et emplacement du sitemap.
- `LICENSE` : licence du dépôt.

## Aperçu local

Depuis la racine du dépôt, avec Python 3 installé :

```sh
python3 -m http.server 8000
```

Ouvrir http://localhost:8000. Arrêter le serveur avec `Ctrl+C`.

## Publication et domaine

Aucune compilation n’est nécessaire. Publier `index.html`, `styles.css`, `sitemap.xml` et
`robots.txt` à la racine du site auprès de l’hébergeur utilisé. Publier également
le dossier `contact/` et les icônes référencées par les pages et le manifeste.

Le formulaire utilise `POST https://formspree.io/f/xnppzkpk`, sans JavaScript ni
serveur applicatif. Le navigateur vérifie les champs obligatoires et le format
de l’adresse e-mail. Formspree gère la réponse après soumission. Pour vérifier
la réception, effectuer un envoi manuel avec ses propres coordonnées et contrôler
le tableau de bord Formspree ; aucun message de test n’est envoyé automatiquement.

L’URL publique retenue est `https://www.rondeau-cameira.fr/`, conformément au nom
de ce dépôt. Si le domaine principal change, mettre à jour le lien canonique dans
`index.html`, l’URL dans `sitemap.xml` et la déclaration dans `robots.txt`.

La configuration de l’hébergement et du DNS n’est pas décrite dans ce dépôt.
Vérifier auprès de l’hébergeur que le domaine est associé au site et que HTTPS
fonctionne. Configurer une redirection permanente des variantes HTTP et du domaine
sans `www` vers l’URL principale.

La page conserve une navigation par lien vers le site personnel. Si une
redirection automatique devient souhaitée, la configurer au niveau HTTP chez
l’hébergeur.

## Vérifications avant publication

- Contrôler la page sur mobile et ordinateur, ainsi qu’en mode sombre.
- Vérifier que le lien est accessible au clavier avec `Tab` puis `Entrée`.
- Vérifier que `/sitemap.xml` et `/robots.txt` sont accessibles après publication.
- Ajouter au sitemap uniquement les pages publiques de ce site ; le site personnel
  sur le sous-domaine doit disposer de son propre sitemap.
