# Classification_des_critiques_de_films
Classification binaire de critiques de films avec Keras
Ce projet implémente un modèle de réseau neuronal pour effectuer une classification binaire des critiques de films en utilisant le jeu de données IMDb avec Keras. Le modèle utilise un réseau de neurones récurrent (LSTM) pour l'analyse de texte.

Étapes du code
Étape 1 : Chargement des données
Nous commençons par charger les données du jeu de données IMDb à l'aide de Keras. Le jeu de données IMDb contient des critiques de films étiquetées comme positives (1) ou négatives (0).

Étape 2 : Prétraitement des données
Nous effectuons le prétraitement des données en limitant le nombre de mots du vocabulaire et la longueur des séquences. Nous utilisons également la fonction pad_sequences de Keras pour ajuster la longueur des séquences.

Étape 3 : Création du modèle
Nous créons un modèle de réseau neuronal séquentiel avec une couche d'incorporation (Embedding), une couche LSTM et une couche de sortie avec une activation sigmoid. Cette architecture est couramment utilisée pour l'analyse de texte.

Étape 4 : Compilation du modèle
Nous compilons le modèle en spécifiant une fonction de perte (binary_crossentropy) et un optimiseur (Adam) pour l'entraînement. Nous utilisons également la métrique de précision (accuracy) pour évaluer la performance du modèle.

Étape 5 : Entraînement du modèle
Nous entraînons le modèle sur l'ensemble d'entraînement en spécifiant le nombre d'époques et la taille de lot (batch_size). Les données sont divisées en ensembles d'entraînement et de validation pour surveiller l'apprentissage du modèle.

Étape 6 : Évaluation du modèle
Nous évaluons la performance du modèle sur l'ensemble de test en calculant la perte (loss) et la précision (accuracy).

Étape 7 : Prédiction sur de nouvelles données
Nous effectuons une prédiction sur une nouvelle critique de film pour déterminer si elle est positive ou négative en utilisant le modèle entraîné.

Étape 8 : Tracer les graphes de la perte et de la précision
Nous utilisons la bibliothèque matplotlib pour tracer les graphes de la perte et de la précision au fil de l'entraînement. Ces graphes permettent de visualiser l'évolution de la performance du modèle.
