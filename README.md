# VANIA BAR LOUNGE — gestion du stock

Application web statique en français pour saisir les ventes et les entrées de stock, gérer les produits, calculer le rapport journalier et imprimer ou sauvegarder les données.

## Utilisation

- Ouvrir `index.html`, puis cliquer sur **Ouvrir l’administration**, ou ouvrir directement `admin.html`.
- Les quantités initiales et les prix communiqués sont préchargés. Les produits sans prix sont affichés avec un prix de 0 FC et doivent être complétés.
- Saisir les entrées, les ventes et, si nécessaire, corriger le stock initial. Les totaux et la valeur du stock restant sont calculés automatiquement.
- Le solde du dernier rapport antérieur est proposé comme stock initial lors de la création d’un nouveau rapport.
- Utiliser **Imprimer le rapport** pour l’impression et **Sauvegarder les données** pour exporter un fichier JSON. Le fichier peut être restauré dans l’application.

## Stockage et synchronisation

Cette version sauvegarde les données dans `localStorage` du navigateur : les changements ne se synchronisent pas entre téléphones et peuvent être effacés si les données du navigateur sont supprimées. Les sauvegardes JSON doivent être conservées en lieu sûr. L’application n’est pas encore reliée à iCloud, Firebase ou Supabase. Une base de données cloud et une authentification doivent être configurées pour permettre une synchronisation fiable entre plusieurs appareils ; ne mettez jamais une clé secrète de service dans le code HTML public.

## Publication

Les fichiers `index.html` et `admin.html` peuvent être publiés avec GitHub Pages ou hébergés sur votre service web actuel. Un hébergement statique seul ne fournit pas la synchronisation cloud.
