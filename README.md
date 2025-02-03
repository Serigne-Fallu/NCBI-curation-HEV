# Curation des données NCBI - Hepatitis E Virus (HEV)
Ce projet permet de récupérer et de curer les séquences complètes du génome du virus de l'hépatite E (HEV) ainsi que leurs métadonnées associées depuis la base de données NCBI.

## Objectif
Rechercher et télécharger les séquences complètes du génome du virus de l'hépatite E.
Récupérer et extraire les métadonnées associées à ces séquences.
Nettoyer et filtrer les données pour conserver les séquences pertinentes.
Sauvegarder les résultats sous forme de fichiers .fasta et .csv.

## Dépendances
- rentrez: Pour interagir avec la base de données NCBI.
- dplyr, stringr: Pour le nettoyage et la manipulation des données.
- seqinr: Pour la gestion des fichiers FASTA.

## Étapes du projet
### Téléchargement des séquences :
- Recherche des séquences de HEV avec "complete genome" sur NCBI.
- Téléchargement des séquences au format FASTA.

### Extraction des métadonnées :
- Récupération des métadonnées associées à chaque séquence HEV.
- Nettoyage des métadonnées pour extraire des informations utiles (ex. : accession, pays, technologie de séquençage).

### Nettoyage des données :
- Suppression des séquences sans pays ou date de soumission.
- Modification des colonnes pour obtenir des informations claires sur les dates et pays.

### Filtrage des séquences FASTA :
Filtrage des séquences FASTA pour ne conserver que celles correspondant aux métadonnées filtrées.

## Fichiers générés 
HEV_Genomes.fasta : Fichier contenant toutes les séquences FASTA téléchargées.
HEV_Metadonnees.csv : Fichier CSV avec les métadonnées brutes.
HEV_metadonneesFiltrees.csv : Fichier CSV avec les métadonnées nettoyées.
HEV_Genomes_Filtres.fasta : Fichier FASTA contenant les séquences filtrées.
