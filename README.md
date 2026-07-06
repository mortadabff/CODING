# Coding Interview Roadmap

📚 Une collection complète de problèmes algorithmes à résoudre, organisée par thème et niveau de difficulté.

---

## 📋 TABLEAUX / ARRAYS

### Facile
- Two Sum
- Contains Duplicate
- Remove Duplicates from Sorted Array
- Move Zeroes
- Best Time to Buy and Sell Stock
- Maximum Subarray (Kadane's Algorithm)
- Missing Number
- Duplicate Number

### Moyen
- Product of Array Except Self
- Rotate Array
- Merge Sorted Array
- Search in Rotated Sorted Array
- 3Sum
- Container With Most Water
- First Missing Positive
- Majority Element

### Difficile
- Trapping Rain Water
- Median of Two Sorted Arrays
- Sliding Window Maximum
- LRU Cache

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