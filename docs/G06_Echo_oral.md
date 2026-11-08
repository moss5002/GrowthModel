# Echo — préparation de l’oral

Les notes de chaque slide contiennent une proposition de présentation. Les durées prévues totalisent huit minutes : 40, 45, 45, 55, 55, 45, 60, 55, 45 et 35 secondes. Répartir les slides entre vous, puis répéter avec un chronomètre.

## Les idées à savoir expliquer

- **Activation** : vingt minutes cumulées pendant la semaine d’inscription. C’est une convention de première utilisation, pas une preuve de fidélité. Les comparaisons avec dix minutes, deux sessions et leur combinaison ne montrent pas de meilleur retour S4.
- **Cohorte** : les personnes inscrites pendant la même semaine. S4 est la quatrième semaine après leur semaine d’inscription ; chaque utilisateur compte une seule fois dans le taux de retour de sa cohorte.
- **Retour S4 ajusté** : on compare les canaux avec une même répartition de mois d’inscription et de plateformes. Cela réduit certaines différences de composition sans prouver un effet causal du canal.
- **North Star** : les minutes totales d’écoute par semaine. Elles mesurent l’usage audio ; on les accompagne du nombre d’actifs et de la rétention pour éviter qu’une poignée de gros auditeurs masque une perte d’utilisateurs.
- **Le +30 % annoncé** : notre reconstruction calendaire trouve +31,5 % de sessions totales. La méthode exacte de l’équipe reste inconnue. Sur douze semaines comparables par assigné, les sessions gagnent 8,71 %, mais l’écoute perd 5,25 % et le retour S12 perd 11,71 points.
- **Deux mois ou douze semaines ?** Les inscriptions au test ont lieu du 15 janvier au 15 mars 2026. Les données jusqu’à juin permettent ensuite douze semaines complètes de suivi pour chaque participant.
- **CAC et revenu** : pour les inscrits paid de janvier à juin 2025, environ 2,61 € de CAC contre 1,62 € de revenu publicitaire à 52 semaines. Le remboursement moyen n’est pas atteint à cet horizon. Cela ne donne ni une LTV à vie ni un délai certain de remboursement.
- **Modèle** : actifs suivants = anciens actifs × maintien + nouveaux inscrits, par canal. Paid dépend du budget et du CAC ; les deux autres canaux suivent leurs inscriptions passées. L’effet éventuel de paid sur les autres canaux n’est pas mesuré.
- **Pourquoi simple ?** Sur la validation interne, le modèle simple donne 1,57 % d’erreur d’écoute contre 2,54 % pour le découpage par ancienneté testé. Sur le backtest final, l’erreur est de 3,85 %. Le modèle sous-estime la fin de période.
- **Scénarios** : mêmes notifications normales et budget de 1 630 €/mois. Le CAC et la probabilité de départ varient de ±5 %. Ce sont des hypothèses, pas des gains acquis ni des intervalles de confiance.

## Utiliser le modèle pour la question du jury

Avant l’oral, ouvrir `G06_Echo_model.ipynb` depuis la racine du projet et exécuter toutes les cellules avec les dépendances de `requirements.txt`. Vérifier que les graphiques apparaissent. Garder une copie inchangée pour retrouver les résultats du rendu.

La section des scénarios contient trois réglages :

| Réglage | Valeur du rendu | Utilité |
| --- | --- | --- |
| `BUDGET_PAID_MONTHLY` | 1630 | Budget paid mensuel en euros |
| `SCENARIO_CHANGE` | 0.05 | Variation relative du CAC et des départs |
| `FORECAST_WEEKS` | 26 | Nombre de semaines projetées |

Modifier un réglage puis relancer les cellules des paramètres, des résultats et du graphique des scénarios. Exemple : pour +20 % de budget, remplacer 1630 par 1956. Les inscriptions paid augmentent dans le modèle ; cela ne prouve pas qu’un budget plus élevé conserverait le même CAC dans la réalité. Les autres canaux ne reçoivent pas de hausse automatique.

Lire les actifs de dernière semaine, les minutes cumulées, le revenu publicitaire et la dépense paid. Ne pas appeler « bénéfice » le revenu moins la seule dépense paid : les autres coûts manquent. Revenir aux réglages du rendu après la démonstration.

## Ce qui reste avant le dépôt

Relire les trois rendus en groupe, vérifier les éventuelles exigences de langue et ajouter vos noms si nécessaire. Répéter les huit minutes et la modification d’un paramètre. Déposer le notebook, le rapport PDF et les slides avec les données nécessaires à l’exécution, selon le canal demandé par l’enseignante.
