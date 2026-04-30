  README.md 
 Web AHP - Application d'aide à la décision multicritère
Description
Cette application implémente la méthode *Analytic Hierarchy Process (AHP)* de Saaty.  
Elle permet de prendre une décision lorsqu'on doit choisir entre plusieurs alternatives évaluées sur plusieurs critères.
Comment utiliser l'application
 1. Configuration initiale
- Choisissez le nombre de critères (2 à 7) et le *nombre d'alternatives (2 à 7)
- Cliquez sur "Initialiser les formulaires"
2. Nommez vos éléments
- Saisissez les noms des critères (ex: Prix, Confort, Sécurité)
- Saisissez les noms des alternatives (ex: Voiture A, Voiture B, Voiture C)
3. Évaluez les alternatives pour chaque critère
Pour chaque critère, vous avez deux options :
 Option A : Valeurs numériques
- Saisissez des nombres (ex: prix en euros, kilométrage)
- Cochez "Coût"* si la valeur la plus basse est la meilleure (prix, distance, temps)
- Laissez décoché si la valeur la plus haute est la meilleure (note, performance)
 Option B : Valeurs catégorielles
- Sélectionnez *"Catégoriel" dans le menu déroulant
- Pour chaque alternative, choisissez une catégorie (ex: Mauvais, Moyen, Bon, Excellent)
- Attribuez une note de 1 à 9 à chaque catégorie (1 = très mauvais, 9 = excellent)
4. Comparez les critères entre eux
Remplissez la matrice de comparaison par paires (échelle de Saaty) :
 Valeur et Signification :
| 1 | Aussi important |
| 3 | Modérément plus important |
| 5 | Fortement plus important |
| 7 | Très fortement plus important |
| 9 | Extrêmement plus important |
| 1/3, 1/5, etc. | Inverse (moins important) |
Exemple pour 3 critères (Prix > Confort > Sécurité) :
| Paire | Valeur |
|-------|--------|
| Prix vs Confort | 3 |
| Prix vs Sécurité | 2 |
| Confort vs Sécurité | 1/2 (ou 0.5) |
Les valeurs inverses sont automatiquement remplies.
5. Lancez le calcul
Cliquez sur *"Lancer le calcul AHP"
 6. Interprétez les résultats
 Si la matrice est cohérente (RC < 0,1) :
- Vous verrez les *poids des critères (leur importance relative)
- Vous verrez les *scores globaux des alternatives (en %)
- L'alternative avec le score le plus élevé est proposée comme meilleure
 Si la matrice est incohérente (RC ≥ 0,1) :
- Un message d'erreur s'affiche
- Vous devez revoir vos comparaisons dans la matrice des critères
- Vérifiez qu'il n'y a pas de cycle illogique (ex: A > B, B > C mais C > A)
Exemple concret
 Problème : Choisir une voiture
Critères : Prix, Confort, Sécurité  
Alternatives : Voiture A, Voiture B, Voiture C
Matrice des critères :
| | Prix | Confort | Sécurité |
|--|------|---------|----------|
| Prix | 1 | 3 | 2 |
| Confort | 1/3 | 1 | 1/2 |
| Sécurité | 1/2 | 2 | 1 |
Évaluations numériques (Prix - coût) :
| Alternative | Prix (€) |
|-------------|----------|
| Voiture A | 10000 |
| Voiture B | 12000 |
| Voiture C | 15000 |
Évaluations catégorielles (Confort) :
| Alternative | Catégorie | Note (1-9) |
|-------------|-----------|-------------|
| Voiture A | Moyen | 5 |
| Voiture B | Bon | 7 |
| Voiture C | Très bon | 9 |
Cliquez sur Lancer le calcul pour voir la meilleure alternative.

 Installation locale

Aucune installation requise. Ouvrez simplement le fichier index.html dans un navigateur.


Utilisation en ligne
Cliquez ici pour utiliser l'application : 
https://mmxavier-app.github.io/web-ahp
