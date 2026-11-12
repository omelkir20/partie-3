# Partie-3 (TP7 + TP8)
## TP7
### Partie 1 : Couches et cache
![](cap-partie3/tp7-cap1.PNG)
![](cap-partie3/tp7-cap2.PNG)
![](cap-partie3/tp7-cap3.PNG)
![](cap-partie3/tp7-cap4.PNG)
![](cap-partie3/tp7-cap5.PNG)
![](cap-partie3/tp7-cap6.PNG)
![](cap-partie3/tp7-cap7.PNG)
### Partie 2 : Mesurer l’image naïve
![](cap-partie3/tp7-cap8.PNG)
![](cap-partie3/tp7-cap9.PNG)
### Partie 3 : Dockerfile multi-stage
![](cap-partie3/tp7-cap10.PNG)
![](cap-partie3/tp7-cap11.PNG)
![](cap-partie3/tp7-cap12.PNG)
![](cap-partie3/tp7-cap13.PNG)
![](cap-partie3/tp7-cap14.PNG)
### Partie 4 : Pile Docker Compose
![](cap-partie3/tp7-cap15.PNG)
![](cap-partie3/tp7-cap16.PNG)
![](cap-partie3/tp7-cap17.PNG)
![](cap-partie3/tp7-cap18.PNG)
![](cap-partie3/tp7-cap19.PNG)
![](cap-partie3/tp7-cap20.PNG)
![](cap-partie3/tp7-cap21.PNG)
![](cap-partie3/tp7-cap22.PNG)
### Partie 5 : Buildx et images multi-architecture
![](cap-partie3/tp7-cap23.PNG)
![](cap-partie3/tp7-cap24.PNG)
![](cap-partie3/tp7-cap25.PNG)
![](cap-partie3/tp7-cap26.PNG)
## TP8
### Étape 0 :
![](cap-partie3/tp8-cap1.PNG)
![](cap-partie3/tp8-cap2.PNG)
![](cap-partie3/tp8-cap3.PNG)
### Partie 1 : OWASP API Security Top 10
| Risque | Concerne l’API ? | Mesure |
|---|---|---|
| API1 BOLA | Non pour l’instant : pas d’accès à un objet par ID. Oui si vous ajoutez `GET /api/contact/:id` | Contrôle d’accès par objet |
| API2 Broken Authentication | Oui : aucune authentification | Hors périmètre du TP. Il faudrait JWT ou clé d’API pour `GET /api/contact` |
| API3 Property Level | Oui : mass assignment possible | `.strict()` refuse les champs en trop |
| API4 Resource Consumption | Oui | Rate limit, `limit: "10kb"`, pagination max 50 |
| API5 Function Level Authorization | Oui pour la future route de liste (accessible à tous) | Rôles / authentification |
| API6 Sensitive Business Flows | Oui : spam du formulaire | Rate limit, captcha |
| API7 SSRF | Non : l’API n’appelle pas d’URL fournie par l’utilisateur | N/A |
| API8 Security Misconfiguration | Oui : stack trace, `x-powered-by` | Helmet, errorHandler, `disable("x-powered-by")` |
| API9 Improper Inventory | Peu : une seule version, pas de doc | Documenter les routes, versionner |
| API10 Unsafe Consumption of APIs | Non : pas d’API tierce | N/A |
#### Trois attaques que la version de départ laisse passer

1. **JSON invalide ou champs manquants :** provoquent une erreur 500 avec la stack trace visible (fuite d’information).

2. **Déni de service (DoS) :** une rafale de requêtes ou un corps énorme permet un déni de service, car il n’y a ni limite de débit (Rate Limiting) ni limite de taille du corps (Body Size Limit).

3. **Absence de validation des données :** des champs supplémentaires (`isAdmin`) ou des données sans contrôle (chaîne de 10 Mo, `<script>`) sont acceptés.

Vous pouvez le vérifier avec :
![](cap-partie3/tp8-cap4.PNG)
### Partie 2 : Validation et gestion des erreurs
![](cap-partie3/tp8-cap5.PNG)
![](cap-partie3/tp8-cap6.PNG)
![](cap-partie3/tp8-cap7.PNG)
![](cap-partie3/tp8-cap8.PNG)
### Partie 3 : Durcissement HTTP
![](cap-partie3/tp8-cap9.PNG)
![](cap-partie3/tp8-cap10.PNG)
![](cap-partie3/tp8-cap11.PNG)
![](cap-partie3/tp8-cap12.PNG)
![](cap-partie3/tp8-cap13.PNG)
![](cap-partie3/tp8-cap14.PNG)
### Partie 4 : Tests de routes et cas négatifs
![](cap-partie3/tp8-cap15.PNG)
![](cap-partie3/tp8-cap16.PNG)
![](cap-partie3/tp8-cap17.PNG)
### Partie 5 : Intégration avec PostgreSQL et migrations
![](cap-partie3/tp8-cap18.PNG)
![](cap-partie3/tp8-cap19.PNG)
![](cap-partie3/tp8-cap20.PNG)
![](cap-partie3/tp8-cap21.PNG)
![](cap-partie3/tp8-cap22.PNG)
![](cap-partie3/tp8-cap23.PNG)
![](cap-partie3/tp8-cap24.PNG)
![](cap-partie3/tp8-cap25.PNG)
![](cap-partie3/tp8-cap26.PNG)
![](cap-partie3/tp8-cap27.PNG)
### Partie 6 : Défi
![](cap-partie3/tp8-cap28.PNG)
![](cap-partie3/tp8-cap29.PNG)
![](cap-partie3/tp8-cap30.PNG)
![](cap-partie3/tp8-cap31.PNG)
![](cap-partie3/tp8-cap32.PNG)
![](cap-partie3/tp8-cap33.PNG)
![](cap-partie3/tp8-cap34.PNG)


