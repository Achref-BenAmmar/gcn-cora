# GCN sur Cora

Réimplémentation d'un Graph Convolutional Network à partir de la règle de propagation de
Kipf & Welling (ICLR 2017), sur le jeu de données Cora (2 708 articles, 140 nœuds étiquetés).

## Résultats (10 graines)

| Modèle | Précision en test |
|---|---|
| MLP (sans le graphe) | 57,9 % |
| GCN implémenté à la main | 81,7 % |
| GCN (PyTorch Geometric) | 82,3 % |

La précision s'effondre de 82 % à 17 % entre 2 et 16 couches, un effet d'over-smoothing.

## Lancer le notebook

    pip install torch torch_geometric scikit-learn matplotlib

Puis lancer `gcn_cora.ipynb`.