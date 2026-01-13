1. Supprimer la base de données locale
    - `symfony console doctrine:database:drop --force`
2. Recréer la base de données locale
    - `symfony console doctrine:database:create`
3. Supprimer les fichiers du dossier `/migrations`
    - `symfony console doctrine:database:create`
4. Rajouter la configuration nécessaire à `/config/packages/doctrine.yaml`
5. Refaire la migration
    - `symfony console make:migration`
6. Vérifier le code sql généré afin d'être sûr qu'InnoDB a été rajouté en tant que moteur de stockage
5. Migrer les données
    - `symfony console doctrine:migrations:migrate`