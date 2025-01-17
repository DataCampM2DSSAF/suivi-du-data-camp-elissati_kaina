## Semaine 1:
- Importation du jeu de données
- Description des données pour avoir des idées sur la structure et détecter les failles de notre jeu de données
- Début de traitement des valeurs manquantes dans les dataframe
- Concaténer identity et transaction, puis faire extraire la variable cible et variables explicatives.

## L'objective de la semaine prochaine:
- Réduction de la mémoire
- Traitement des valeur manquantes Mean-Mode
- Observation IsFraud (Imbalanced Data)
- Codage des variables nominatives

## Semaine 2:
- D'apès la visualisation de nos données on remarque que 97,19% des transaction sont non frauduleuses et juste 2,81% des transactions frauduleuses alors si on utilise cette base de données pour nos études avec les modèles prédictifs classiques nous allons obtenir des fausses prédictions.
- Le traitement des valeurs manquantes dans les dataframe et les doublons:
 * Supprimer les doublons de train et test
 * Supprimer les colonnes qui ont plus de 90% des valeurs manquantes
 - Imputation des valeurs manquantes par la moyenne : nous allons remplir les valeurs manquantes en utilisant la technique du mode mais il faut faire attention au varaible qualitative qui sont inimputable par la moyenne
 -  Mapping de E-mail et P-mail (pipline)
 - Aggregation la modalité des certaines varaibles qualitaives afin de réduire la dimension aprés leur décodage :"DeviceInfos", "Id31" et "id33"

## L'objective de la semaine prochaine:
- Imputaion des valeurs manquantes par KNN 
- Commencer la rédaction du rapport

## Semaine 3
- Imputaion des valeurs manquantes par KNN:

*step0 : Décodage de varaible qualitatives en varaible discrétes par label encoder : programmé manuellement
* Step1: Scaling des varaibles continues par Min_Max: programmé manuellement
* Step2: Imputation par KNN pour K==5 
* Step3: l'application da la fonction inverse de scaling  : programmé manuellement
* Step4: l'application de la fonction inverse de Décodage : programmé manuellement 
* step5 :  enregistrement cette base imputée par KNN sous nom base_KNN

## L'objective de la semaine prochaine:
- Data exploration et visualisation : analyse bi-variée
- Décodage des données qualitatives
- Etude de corrélation  
- Continuer la rédaction du rapport 
 
## Semaine 4
- Data exploration et visualisation: estimation des distributions des variables continues pour isfraud = 0 et y 001, et réalisation de statistique bivariés
- Décodage des données qualitatives: transformation qualitatives en des variables binaire en eevitant la multicolinéarité.
- Etude de corrélation entre les variables de la base imputée par KNN et celles imputées par mode-mean

## L'objective de la semaine prochaine:
- Split de jeu de donné (stratifié)
- Implémentation LGBM (without ACP)
- XGboost (on ne le implémentera plus car il se focalise presque sur le meme principe de fonctionnement de LGBM)

## Semaine 5 : High-powered Machine Learning model for unbalanced datasets
- Implémentation lgbm sur la base mean_mode et LGBM sur la base KNN, avec des paraètre par défaut

- Implémentation lgbm sur la base mean_mode et LGBM sur la base KNN  ( LGBM avec spécification de number of leaves==5 , num_boost_round=100 : corresponds to the number of boosting rounds or trees to build )

- Implémentation LGBM with Hyper Parametres optimized via scikit-learn's GridSearchCV or Baysian Optimizer 

- LGBM classifier with cross validation via API avec des hyper-paramétres optimisés (seuelemnt sur la base imputée par KNN)+ programation de la fonction de Full prédiction de probababilité et de Full prédiction des classes d'appartenance.

- LGBM classifier with cross validation programmé manuellement avec des hyper-paramétres optimisés (seuelemnt sur la base imputée par KNN) + programation de la fonction de Full prédiction de probababilité et de Full prédiction des classes d'appartenance

## Semaine 6: Implémentation d'autre méthode de Machine learning ( KNN avec RandomUnderSempler):
 - clibrage de la varaible 'isFRaud' par la méthode undersampling
 
 - normalisation et standardisation des variables continues
 
 - split de jeu de données
 
 - implémentation de KNN pour différentes K afin de choisir celui qui maximise accuracy de validation en tenant compte le sur    apprentissage 
 
 - implémentation KNN pour le meilleur K ( sélectionné visuellement  à partir de la courbe de la sensibilité de k en fonction de accuracy).
 - report classification et coubre de roc
 
 - submission
 
 - optimisation de tuninig paramètres par Cross Validation
 
 - sélection du meilleur paramètre optimisé par cross validation 
 
 - implémentation KNN pour r K ( optimisé par cross validation).
 
 - report classification et coubre de roc
 
 - submission
 
 
 ##  Semaine 7 + 8: Implémentation d'autre méthode de Machine learning ( KNN avec RandomOverSempler):
 - on applique la même méthode de la semaine 6 mais avec jeu de donnée calibrée par over sampler.
 
 - clibrage de la varaible 'isFRaud' par la méthode undersampling
 
 - normalisation et standardisation des variables continues.
 
 - split de jeu de données
 
 - implémentation de KNN pour différentes valeurs de K afin de choisir la valeur qui maximise l'accuracy de la validation en tenant compte le sur apprentissage.
 
 - sélection du meilleur paramètre optimisé , visuellement, par étude de la sensibilité.
 
 - implémentation KNN pour le K chosi ( sélectionné visuellement).
 
 - report classification et coubre de roc
 
 - submission
 
 ***optimisation de truning paramètres par Cross Validation ( étape dépassée)  
 ***sélection du meilleur paramètre ( c'est le même paramètre selectioné visuellement) ( étape dépassée)
