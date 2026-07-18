# n8n-portfolio

Workflows N8N construits dans le cadre de ma formation pratique en automatisation. Chaque fichier est exporté directement depuis N8N et documenté ci-dessous.

## Workflows

### 01 — Notification Discord conditionnelle
`01-discord-notification.json`

Reçoit des données via un webhook, les formate, et envoie une notification automatique dans un salon Discord via son API webhook.

**Concepts démontrés** : trigger webhook, requête HTTP vers une API externe, formatage dynamique de message avec expressions N8N.

### 02 — Traitement de données et écriture Google Sheets
`02-google-sheets.json`

Reçoit des données via webhook, les transforme (concaténation de champs, horodatage), les écrit dans une ligne d'un Google Sheet, puis renvoie une réponse HTTP.

**Concepts démontrés** : intégration OAuth2 (Google Sheets), écriture de données structurées, gestion des expressions et du fuseau horaire, réponse webhook personnalisée.

### 03 — Gestion d'erreur
`03-error-handling.json`

Simule un appel API défaillant (URL invalide) et capture l'erreur via la sortie dédiée du node, pour déclencher automatiquement une alerte Discord — sans interrompre l'exécution du workflow.

**Concepts démontrés** : gestion d'erreur native (`onError: continueErrorOutput`), branches conditionnelles de sortie, notification automatisée en cas d'échec.

### 04 — Automatisation de boîte mail avec agent IA
`04-email-automation.json`

Surveille une boîte Gmail, analyse chaque email entrant avec un agent IA (Claude), génère une réponse professionnelle contextualisée, et peut consulter/créer des événements dans Google Calendar selon la demande du client.

**Concepts démontrés** : trigger Gmail, agent IA avec prompt système structuré, output parser, mémoire de conversation, outils connectés (Google Calendar), envoi de réponse automatisé.

## Notes

Les identifiants de connexion (credentials) et URLs de webhooks ont été retirés ou remplacés par des placeholders avant publication. Pour réutiliser ces workflows, importez le JSON dans une instance N8N et reconfigurez vos propres accès (Google, Discord, Gmail, Anthropic).

## À propos

Workflows réalisés dans le cadre d'un parcours de formation en automatisation N8N, en vue d'une activité freelance en tant que technicien N8N.
