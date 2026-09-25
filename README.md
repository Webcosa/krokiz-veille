# Krokiz — veille

Appelle toutes les 10 minutes la route `/api/veille` du serveur Krokiz, qui :

- compare les paiements Stripe et les commandes Shopify, et recrée une commande
  manquante depuis la copie complète gardée dans Stripe ;
- rafraîchit le suivi des colis et envoie les notifications d'étape ;
- alerte sur le téléphone des gérants en cas d'anomalie.

La clé d'accès est dans les secrets du dépôt (`CRON_SECRET`), jamais dans le code.
