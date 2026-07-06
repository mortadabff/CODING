# Coding Interview Roadmap

📚 Une collection complète de problèmes algorithmes à résoudre, organisée par thème et niveau de difficulté.

---

## 📋 TABLEAUX / ARRAYS

### Facile

#### 1️⃣ Two Sum
**Énoncé:** Étant donné un tableau d'entiers `nums` et un entier `target`, retourne les indices des deux éléments dont la somme est égale à `target`. Chaque solution est unique et un même élément ne peut pas être utilisé deux fois.

**Exemples de test:**
```
Input: nums = [2,7,11,15], target = 9
Output: [0,1]
Explication: nums[0] + nums[1] == 9, on retourne [0, 1]

Input: nums = [3,2,4], target = 6
Output: [1,2]
Explication: nums[1] + nums[2] == 6

Input: nums = [3,3], target = 6
Output: [0,1]
```

---

#### 2️⃣ Contains Duplicate ⭐
**Énoncé:** Étant donné un tableau d'entiers, détermine s'il contient au moins une valeur présente plusieurs fois. Retourne `true` si un doublon existe, sinon `false`.

**Exemples de test:**
```
Input: nums = [1,2,3,4]
Output: false

Input: nums = [1,2,2,4]
Output: true

Input: nums = [1]
Output: false
```

---

#### 3️⃣ Remove Duplicates from Sorted Array
**Énoncé:** Un tableau trié peut contenir plusieurs occurrences d'une même valeur. Supprime les doublons sur place (sans créer un nouveau tableau) et retourne le nombre d'éléments distincts.

**Exemples de test:**
```
Input: nums = [1,1,2]
Output: k = 2, nums = [1,2,_]

Input: nums = [0,0,1,1,1,2,2,3,3,4]
Output: k = 5, nums = [0,1,2,3,4,_,_,_,_,_]

Input: nums = [1]
Output: k = 1, nums = [1]
```

---

#### 4️⃣ Move Zeroes
**Énoncé:** Déplace tous les zéros à la fin du tableau tout en conservant l'ordre des autres éléments. La modification doit être faite directement dans le tableau.

**Exemples de test:**
```
Input: nums = [0,1,0,3,12]
Output: [1,3,12,0,0]

Input: nums = [0]
Output: [0]

Input: nums = [0,0,1]
Output: [1,0,0]
```

---

#### 5️⃣ Best Time to Buy and Sell Stock
**Énoncé:** On te donne le prix d'une action pour chaque jour. Tu peux acheter une seule fois puis vendre une seule fois. Calcule le profit maximal possible. Si aucun bénéfice n'est possible, retourne 0.

**Exemples de test:**
```
Input: prices = [7,1,5,3,6,4]
Output: 5
Explication: Achat à 1, vente à 6

Input: prices = [7,6,4,3,1]
Output: 0
Explication: Pas de profit possible

Input: prices = [2,4,1]
Output: 2
Explication: Achat à 2, vente à 4
```

---

#### 6️⃣ Maximum Subarray (Kadane's Algorithm)
**Énoncé:** Trouve la sous-partie contiguë d'un tableau dont la somme est maximale. Retourne cette somme.

**Exemples de test:**
```
Input: nums = [-2,1,-3,4,-1,2,1,-5,4]
Output: 6
Explication: Sous-tableau [4,-1,2,1] a la somme maximale = 6

Input: nums = [5,4,-1,7,8]
Output: 23
Explication: Sous-tableau [5,4,-1,7,8]

Input: nums = [-1]
Output: -1
```

---

#### 7️⃣ Missing Number
**Énoncé:** On te donne un tableau contenant tous les nombres de 0 à n, sauf un. Retrouve le nombre manquant.

**Exemples de test:**
```
Input: nums = [3,0,1]
Output: 2

Input: nums = [0,1]
Output: 2

Input: nums = [9,6,4,2,3,5,7,0,1]
Output: 8
```

---

#### 8️⃣ Find the Duplicate Number
**Énoncé:** Le tableau contient n+1 nombres compris entre 1 et n. Un seul nombre est dupliqué. Retrouve ce nombre sans modifier le tableau.

**Exemples de test:**
```
Input: nums = [1,3,4,2,2]
Output: 2

Input: nums = [3,1,3,4,2]
Output: 3

Input: nums = [1,4,4,2,4]
Output: 4
```

---

### Moyen

#### 9️⃣ Product of Array Except Self
**Énoncé:** Pour chaque position du tableau, calcule le produit de tous les autres éléments, sans utiliser la division.

**Exemples de test:**
```
Input: nums = [1,2,3,4]
Output: [24,12,8,6]

Input: nums = [-1,1,0,-3,3]
Output: [0,0,9,0,0]
```

---

#### 🔟 Rotate Array
**Énoncé:** Tourne le tableau vers la droite de `k` pas. La rotation doit être faite sur place.

**Exemples de test:**
```
Input: nums = [1,2,3,4,5,6,7], k = 3
Output: [5,6,7,1,2,3,4]

Input: nums = [-1,-100,3,99], k = 2
Output: [3,99,-1,-100]
```

---

#### 1️⃣1️⃣ Merge Sorted Array
**Énoncé:** On te donne deux tableaux triés `nums1` et `nums2`. Fusionne-les en un seul tableau trié. Fait la fusion sur place dans `nums1`.

**Exemples de test:**
```
Input: nums1 = [1,2,3,0,0,0], m = 3, nums2 = [2,5,6], n = 3
Output: [1,2,2,3,5,6]

Input: nums1 = [1], m = 1, nums2 = [], n = 0
Output: [1]
```

---

#### 1️⃣2️⃣ Search in Rotated Sorted Array
**Énoncé:** Un tableau trié a été tourné. Cherche une valeur cible et retourne son index. Si elle n'existe pas, retourne -1. La complexité doit être O(log n).

**Exemples de test:**
```
Input: nums = [4,5,6,7,0,1,2], target = 0
Output: 4

Input: nums = [4,5,6,7,0,1,2], target = 3
Output: -1
```

---

### Difficile

#### 1️⃣3️⃣ Trapping Rain Water
**Énoncé:** Calcule combien d'eau peut être piégée après la pluie en fonction de l'élévation du terrain.

**Exemples de test:**
```
Input: height = [0,1,0,2,1,0,1,3,2,1,2,1]
Output: 6

Input: height = [4,2,0,3,2,5]
Output: 9
```

---

#### 1️⃣4️⃣ Median of Two Sorted Arrays
**Énoncé:** Trouve la médiane de deux tableaux triés. La complexité doit être O(log(min(m, n))).

**Exemples de test:**
```
Input: nums1 = [1,3], nums2 = [2]
Output: 2.0

Input: nums1 = [1,2], nums2 = [3,4]
Output: 2.5
```

---

## 🔤 CHAÎNES DE CARACTÈRES / STRINGS

### Facile
- Valid Anagram
- Valid Parentheses
- Reverse String
- Palindrome Check
- First Unique Character in a String
- Isomorphic Strings
- Ransom Note
- Longest Common Prefix

### Moyen
- Longest Substring Without Repeating Characters
- Group Anagrams
- Encode and Decode Strings
- Longest Palindromic Substring
- String Compression
- Minimum Window Substring
- Word Break
- Regular Expression Matching

### Difficile
- Edit Distance
- Longest Duplicate Substring
- Valid Palindrome II

---

## 🔗 LISTES CHAÎNÉES / LINKED LIST

### Facile
- Reverse Linked List
- Linked List Cycle
- Merge Two Sorted Lists
- Remove Nth Node From End of List
- Palindrome Linked List
- Middle of the Linked List

### Moyen
- Add Two Numbers
- Reorder List
- Copy List with Random Pointer
- Linked List Cycle II
- Intersection of Two Linked Lists

### Difficile
- Reverse Nodes in k-Group
- Merge k Sorted Lists

---

## 🌳 ARBRES / TREES

### Facile
- Binary Tree Traversal (Inorder, Preorder, Postorder)
- Maximum Depth of Binary Tree
- Symmetric Tree
- Invert Binary Tree
- Path Sum
- Same Tree

### Moyen
- Binary Search Tree Validation
- Lowest Common Ancestor
- Binary Tree Level Order Traversal
- Construct Binary Tree from Preorder and Inorder
- Serialize and Deserialize Binary Tree
- Maximum Path Sum
- Right View of Binary Tree
- Kth Smallest Element in a BST

### Difficile
- Word Ladder
- Recover Binary Search Tree

---

## 📊 GRAPHES / GRAPHS

### Facile
- Number of Islands
- Flood Fill
- Transpose Graph
- Degree of a Node

### Moyen
- Clone Graph
- Course Schedule (Topological Sort)
- Alien Dictionary
- Number of Connected Components in an Undirected Graph
- Redundant Connection
- Pacific Atlantic Water Flow
- Accounts Merge
- Evaluate Division

### Difficile
- Critical Connections in a Network
- Minimum Height Trees
- All Paths From Source to Target II
- Network Delay Time

---

## 💰 PROGRAMMATION DYNAMIQUE / DYNAMIC PROGRAMMING

### Facile
- Climbing Stairs
- House Robber
- Min Cost Climbing Stairs
- Fibonacci Number

### Moyen
- Coin Change
- Longest Increasing Subsequence
- Decode Ways
- Partition Equal Subset Sum
- Longest Common Subsequence
- Word Break
- Unique Paths
- Jump Game II

### Difficile
- Burst Balloons
- Edit Distance
- Regex Matcher
- Number of Distinct Subsequences

---

## 🗺️ GÉOSPATIAL / GIS & GÉOMÉTRIE

### Facile
- Point in Rectangle
- Distance Between Two Points
- Angle Between Vectors

### Moyen
- Rotating Calipers
- Convex Hull
- Line Intersection
- Closest Pair of Points
- Point in Polygon
- Area of Triangle

### Difficile
- Voronoi Diagram Basics
- Delaunay Triangulation
- Geographic Nearest Neighbor Search

---

## 🗄️ SQL

### Queries de Base
- SELECT avec WHERE
- JOIN (INNER, LEFT, RIGHT, FULL)
- GROUP BY et HAVING
- ORDER BY et LIMIT
- Aggregate Functions (COUNT, SUM, AVG, MIN, MAX)

### Moyen
- Window Functions (ROW_NUMBER, RANK, DENSE_RANK)
- CTEs (Common Table Expressions)
- Self Joins
- Complex Aggregations
- Pivot Tables
- Date Functions

### Avancé
- Recursive Queries
- Complex Window Functions
- Performance Optimization
- Index Strategy

---

## 🌐 PostGIS

### Facile
- ST_Distance
- ST_Contains
- ST_Intersects
- Point Creation and Manipulation
- Buffer Operations

### Moyen
- ST_DWithin
- ST_Closest Point
- Spatial Joins
- Polygon Simplification
- Coordinate Transformation (ST_Transform)

### Difficile
- Complex Spatial Analysis
- KNN Queries
- Advanced Geographic Calculations
- PostGIS Performance Tuning

---

## 🎯 ALGORITHMES DE RECHERCHE & TRI

### Facile
- Binary Search
- Linear Search
- Bubble Sort
- Selection Sort
- Insertion Sort

### Moyen
- Quick Sort
- Merge Sort
- Heap Sort
- Search in BST
- Find Median in Data Stream

### Difficile
- K-th Largest Element
- Median Finder

---

## ⚡ TECHNIQUES AVANCÉES

- **Two Pointers** : Problèmes avec deux pointeurs
- **Sliding Window** : Fenêtre glissante
- **Binary Search** : Recherche binaire et variantes
- **DFS/BFS** : Parcours en profondeur/largeur
- **Backtracking** : Retour arrière
- **Greedy** : Approche gloutonne
- **Divide & Conquer** : Diviser pour régner
- **Bit Manipulation** : Manipulations binaires

---

*Last updated: 2026-07-06*
Valid Palindrome
Longest Common Prefix
Reverse String
Roman to Integer
Longest Substring Without Repeating Characters

Tu apprendras :

dictionnaires (HashMap) ;
ensembles (HashSet) ;
fenêtres glissantes.
HashMap
Two Sum
Group Anagrams
Top K Frequent Elements
First Unique Character

Les HashMap sont omniprésentes en entretien.

Piles
Valid Parentheses
Min Stack
Evaluate Reverse Polish Notation
Files
Number of Recent Calls
Implement Queue using Stacks
Phase 2 : Les structures de données
Linked List
Reverse Linked List
Merge Two Sorted Lists
Linked List Cycle
Remove Nth Node From End
Arbres
Maximum Depth of Binary Tree
Invert Binary Tree
Same Tree
Validate Binary Search Tree
Lowest Common Ancestor
Graphes

Très importants pour le SIG.

Number of Islands
Clone Graph
Course Schedule
Pacific Atlantic Water Flow
Rotting Oranges

Tu réviseras :

BFS ;
DFS ;
graphes orientés et non orientés.
Phase 3 : Très orientée SIG

C'est là que tu peux te différencier.

1. Point in Polygon

Le classique.

Un point appartient-il à un polygone ?

Algorithme :

Ray Casting
Winding Number
2. Distance entre deux points GPS

Implémenter la formule de Haversine.

3. KNN spatial

Trouver les k points les plus proches.

4. Bounding Box

Calculer :

xmin
ymin
xmax
ymax
5. Convex Hull

Algorithmes :

Graham Scan
Jarvis March
6. Intersection de segments

Très utilisé en géométrie.

7. Douglas-Peucker

Simplification de lignes.

8. Recherche spatiale

Construire un petit Quadtree.

9. Implémenter un R-Tree simplifié

Excellent projet GitHub.

10. Dijkstra sur un réseau routier

Très formateur.

Phase 4 : Data Engineering

Tu veux évoluer vers la data, donc ajoute aussi quelques exercices orientés pipelines et traitement de données.

Par exemple :

parser un gros fichier CSV sans tout charger en mémoire ;
compter les fréquences de millions de lignes ;
faire un tri externe ;
dédupliquer un jeu de données ;
écrire un mini ETL en Python.
Phase 5 : SQL

Très important.

Exercices :

deuxième salaire le plus élevé ;
employés ayant un salaire supérieur à leur manager ;
requêtes récursives ;
fonctions de fenêtre (ROW_NUMBER, RANK, LAG, LEAD) ;
agrégations.
Phase 6 : PostGIS

Tu peux créer une série "PostGIS Interview".

Exemples :

ST_Intersects
ST_Contains
ST_DWithin
ST_Buffer
ST_Union
ST_Transform
ST_Distance
ST_Area

Explique pour chaque fonction :

le cas d'usage ;
un exemple ;
la requête SQL ;
les performances ;
les index spatiaux.
Les entreprises qui aiment ce type de préparation

Si tu fais sérieusement cette roadmap, tu seras beaucoup mieux préparé pour des entretiens chez :

Atos ;
Capgemini ;
Sopra Steria ;
Magellium ;
Thales ;
Airbus ;
Dassault Systèmes ;
Esri ;
Google (pour les fondamentaux) ;
Amazon ;
Datadog.