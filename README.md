Classification binaire de critiques de films avec Keras
Ce projet implémente un modèle de réseau neuronal pour effectuer une classification binaire des critiques de films en utilisant le jeu de données IMDb avec Keras. Le modèle utilise un réseau de neurones récurrent (LSTM) pour l'analyse de texte.

Détails du Code
1. Chargement des données
Les données sont chargées à partir du jeu de données IMDb en utilisant la bibliothèque Keras. Les critiques de films sont encodées en séquences de nombres, et les étiquettes correspondent à des critiques positives (1) ou négatives (0).

2. Création du Modèle
Le modèle de réseau neuronal est créé à l'aide de Keras Sequential API. Il se compose des couches suivantes :

Une couche d'incorporation (Embedding) pour convertir les mots en vecteurs.
Une couche LSTM avec 128 unités pour l'analyse de séquence.
Une couche de sortie avec une activation sigmoid pour la classification binaire.
3. Compilation du Modèle
Le modèle est compilé avec une fonction de perte binaire_crossentropy, un optimiseur Adam et la métrique de précision (accuracy) pour évaluer la performance.

4. Utilisation de Callbacks
Trois callbacks sont utilisés pour améliorer l'entraînement du modèle :

EarlyStopping : Arrête l'entraînement prématurément si la perte sur l'ensemble de validation ne s'améliore pas pendant un certain nombre d'époques.
ModelCheckpoint : Sauvegarde le meilleur modèle basé sur la perte sur l'ensemble de validation.
ReduceLROnPlateau : Réduit le taux d'apprentissage si la performance stagne.
5. Entraînement du Modèle
Le modèle est entraîné sur l'ensemble d'entraînement avec un batch size de 64 pendant 10 époques. Les callbacks sont utilisés pour améliorer la performance et éviter le surapprentissage.

6. Évaluation du Modèle
Le modèle est évalué sur l'ensemble de test pour calculer la perte (loss), la précision (accuracy) et le F1-score. La matrice de confusion et le rapport de classification sont également générés pour évaluer la performance du modèle de manière plus détaillée.

7. Tracer les Graphes
Des graphes de la perte et de la précision au fil de l'entraînement sont tracés à l'aide de la bibliothèque matplotlib pour visualiser l'évolution de la performance du modèle.
