# PDB Protein Structure Viewer

Un notebook Jupyter pour visualiser et analyser des structures protéiques à partir de fichiers PDB (Protein Data Bank).

## 🔧 Installation

Installez les dépendances nécessaires :

```bash
pip install biopython numpy matplotlib
```

## 📁 Préparation

1. Téléchargez un fichier PDB depuis [RCSB Protein Data Bank](https://www.rcsb.org/)
2. Placez le fichier `.pdb` dans le même répertoire que le notebook


##  Utilisation

### 1. Ouvrir le notebook

```bash
jupyter notebook pdb-1.ipynb
```

### 2. Modifier le fichier PDB

Dans la cellule 3, modifiez le nom du fichier :

```python
structure = parser.get_structure("test", "VOTRE_FICHIER.pdb")
```

### 3. Exécuter les cellules

Le notebook effectue trois analyses :

#### 📊 Cellule 4 : Angles dièdres Phi/Psi
- Affiche un tableau des angles Phi (φ) et Psi (ψ) pour chaque résidu
- Utile pour analyser la conformation de la chaîne polypeptidique

#### 📈 Cellule 5 : Diagramme de Ramachandran
- Génère un graphique Phi vs Psi
- Permet de valider la qualité de la structure
- Les régions autorisées correspondent aux structures secondaires (hélices α, feuillets β)

#### 🌐 Cellule 6 : Structure 3D
- Visualise la structure tridimensionnelle de la protéine
- Trace le squelette carboné (atomes Cα)
- Affiche les coordonnées en Angströms (Å)

## 📖 Exemple

```python
# Charger une structure
structure = parser.get_structure("test", "9LG6.pdb")

# Les résultats incluent :
# - Tableau des angles dièdres
# - Plot de Ramachandran interactif
# - Visualisation 3D de la structure
```

## 🔍 Ressources

- [RCSB Protein Data Bank](https://www.rcsb.org/) - Télécharger des fichiers PDB
- [Biopython Documentation](https://biopython.org/docs/latest/) - Documentation de Biopython


