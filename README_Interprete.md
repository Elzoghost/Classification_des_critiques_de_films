Classification binaire de critiques de films avec Keras
Ce projet implémente un modèle de réseau neuronal pour effectuer une classification binaire des critiques de films en utilisant le jeu de données IMDb avec Keras. Le modèle utilise un réseau de neurones récurrent (LSTM) pour l'analyse de texte.

Résultats
Après avoir entraîné le modèle sur le jeu de données IMDb, nous avons obtenu les résultats suivants :

Perte (Loss) sur l'ensemble de test : 0.57
Précision (Accuracy) sur l'ensemble de test : 0.70
Interprétation des résultats
La perte (Loss) est une mesure de l'erreur du modèle pendant l'entraînement. Une valeur de perte plus basse indique une meilleure performance du modèle. Vous pouvez comparer cette valeur à travers différentes exécutions ou modèles pour évaluer leur performance relative.

La précision (Accuracy) est la proportion de critiques de films correctement classées par le modèle sur l'ensemble de test. Une précision plus élevée indique que le modèle est meilleur pour discriminer les critiques positives des critiques négatives.

Prédiction sur de nouvelles données
Nous avons également testé le modèle en lui fournissant une nouvelle critique de film :

Nouvelle critique : "This movie was great! I loved it."
Résultat de la prédiction : Critique positive
La prédiction sur de nouvelles données est un indicateur de la capacité du modèle à généraliser et à faire des prédictions sur des données qu'il n'a jamais vues auparavant.
