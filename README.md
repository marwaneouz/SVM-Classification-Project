# SVM-Classification-Project
Implémentation et analyse des SVM sur les datasets Iris et LFW 
# Support Vector Machine (SVM) - Master IMSD  
![License](https://img.shields.io/badge/license-MIT-blue.svg) ![Python](https://img.shields.io/badge/Python-3.8%2B-green.svg) ![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.0%2B-orange.svg)

> **Réalisé par :** Marwane Ouzaina  
> **Encadrant :** Rapport SVM  
> **Master IMSD - Université Ibn Zohr, Faculté de Ouarzazate**  
> **Année Universitaire : 2024–2025**

---

## 📘 Présentation

Ce projet présente une implémentation complète des **Support Vector Machines (SVM)** dans le cadre d’un TP académique. Il couvre :
- Les **fondements théoriques** des SVM
- L’implémentation avec `scikit-learn`
- Des expériences sur deux datasets : **Iris** et **Labeled Faces in the Wild (LFW)**
- L’analyse des noyaux (linéaire, polynomial, RBF), du paramètre `C`, de l’impact du bruit, et de l’utilisation de PCA

🎯 Objectif : Comprendre comment les SVM maximisent la marge entre classes, gèrent les données non linéaires, et résistent (ou non) au sur-apprentissage.

📄 Le rapport complet est disponible ici : [TP_SVM.pdf](reports/TP_SVM.pdf)

---

## 🧪 Résultats Clés

### 1. SVM sur le dataset Iris
- **Précision (noyau linéaire)** : 70%
- **Précision (noyau polynomial)** : 54%
- ✅ Le noyau linéaire est plus efficace ici : les classes sont presque linéairement séparables.

 

---

### 2. SVM sur le dataset LFW (Blair vs Powell)
- **Précision (données équilibrées)** : 96.8%
- **Précision (données déséquilibrées)** : 93.6%
- ✅ L’équilibrage des classes améliore la performance.

 

---

### 3. Impact du paramètre C
- Un `C` faible → sous-apprentissage (marge large)
- Un `C` élevé → sur-apprentissage possible
- **Optimum autour de C = 1**

 

---

### 4. Robustesse au bruit et avec PCA
| Condition | Précision |
|---------|----------|
| Données bruitées (+300 features aléatoires) | 94.7% |
| Après PCA (50 composantes) | 87.2% |
| Avec noyau RBF | 87.2% |

📉 Curieusement, PCA n’améliore pas les performances ici : les composantes principales ne capturent pas toute l’information discriminante.

---

 
