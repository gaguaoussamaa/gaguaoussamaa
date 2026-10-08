Je développe surtout des applications web métier, des API et des intégrations entre systèmes (ERP Odoo, e-commerce, outils internes).

## Projets

### [Passerelle](https://github.com/gaguaoussamaa/passerelle-ecoles-entreprises)

Application web qui gère le cycle complet d'un stage ou d'une alternance entre une école, ses étudiants et des entreprises : offres, candidatures, conventions, suivi et évaluation.

- **Stack** : PHP 8.4, Laravel 13, MySQL 8, Blade, dompdf, Docker
- **Architecture** : monolithe MVC, services métier pour les workflows, cinq rôles cloisonnés par établissement (middlewares et contrôles côté serveur)
- **Points techniques** : conventions PDF versionnées et immuables (empreinte SHA-256), circuit d'approbation séquentiel, états de suivi calculés, import CSV avec rapport ligne à ligne, journal d'audit
- **Données** : 28 tables ; les règles importantes sont portées par la base (contraintes `CHECK`, unicités, clés étrangères)
- **Tests** : 89 tests PHPUnit sur MySQL, exécutés par GitHub Actions à chaque push

### [Validation des remises sur devis](https://github.com/gaguaoussamaa/odoo19-sale-discount-approval)

Module Odoo 19 Community : au-delà d'un seuil, une remise doit être validée par un responsable avant la confirmation du devis.

- **Stack** : Python, Odoo 19 (ORM, vues XML héritées, sécurité), PostgreSQL 16, Docker
- **Points techniques** : héritage de `sale.order`, blocage par le point d'extension de la confirmation, contrôle des droits côté serveur, assistant de refus avec motif obligatoire, activités pour les valideurs
- **Tests** : 8 tests `TransactionCase`, exécutés par GitHub Actions sur Odoo 19 et PostgreSQL 16

## En production (code non publié)

Pendant dix-huit mois chez EN PLACE, comme seul développeur de l'entreprise :

- applications PHP et JavaScript en production, avec leurs évolutions, leurs corrections et le suivi des incidents ;
- échanges en Python entre Odoo, une boutique WooCommerce et le configurateur de produits Prodboard, par leurs API ;
- paramétrage d'Odoo au fil des besoins des équipes.

Ce code appartient à l'entreprise.
