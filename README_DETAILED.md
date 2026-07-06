# 🚀 CODING INTERVIEW ROADMAP - GUIDE COMPLET

📚 **Une collection exhaustive de problèmes algorithmiques avec énoncés détaillés, exemples de test et explications.**

---

# 📋 TABLEAUX / ARRAYS

## Facile ⭐

### 1. Two Sum
**Énoncé:** Étant donné un tableau d'entiers `nums` et un entier `target`, retourne les indices des deux éléments dont la somme est égale à `target`. Chaque solution est unique et un même élément ne peut pas être utilisé deux fois.

**Complexité:** O(n) en temps, O(n) en espace  
**Approche:** Hash Map pour stocker les valeurs et trouver le complément

**Exemples de test:**
```python
Input: nums = [2,7,11,15], target = 9
Output: [0,1]
Explication: nums[0] + nums[1] == 9, retourne [0, 1]

Input: nums = [3,2,4], target = 6
Output: [1,2]
Explication: nums[1] + nums[2] == 6

Input: nums = [3,3], target = 6
Output: [0,1]
Cas limite: même nombre deux fois
```

---

### 2. Contains Duplicate
**Énoncé:** Détermine si un tableau contient au moins une valeur dupliquée. Retourne `True` si oui, `False` sinon.

**Complexité:** O(n) en temps, O(n) en espace  
**Approche:** Set pour tracker les valeurs vues

**Exemples de test:**
```python
Input: nums = [1,2,3,1]
Output: True

Input: nums = [1,2,3,4]
Output: False

Input: nums = [99,99]
Output: True
Cas limite: deux éléments identiques
```

---

### 3. Remove Duplicates from Sorted Array
**Énoncé:** Un tableau TRIÉ contient des doublons. Supprime-les sur place et retourne le nombre d'éléments distincts `k`. Le premier `k` élément du tableau doivent être uniques.

**Complexité:** O(n) en temps, O(1) en espace  
**Approche:** Two pointers - lent pour écrire, rapide pour lire

**Exemples de test:**
```python
Input: nums = [1,1,2]
Output: k = 2, nums = [1,2,_]

Input: nums = [0,0,1,1,1,2,2,3,3,4]
Output: k = 5, nums = [0,1,2,3,4,_,_,_,_,_]

Input: nums = [1,2,2,3,3,3]
Output: k = 3, nums = [1,2,3,_,_,_]
```

---

### 4. Move Zeroes
**Énoncé:** Déplace tous les zéros à la fin du tableau tout en conservant l'ordre relatif des éléments non-zéro. Doit être fait sur place.

**Complexité:** O(n) en temps, O(1) en espace  
**Approche:** Two pointers - position pour zéro, index pour parcours

**Exemples de test:**
```python
Input: nums = [0,1,0,3,12]
Output: [1,3,12,0,0]

Input: nums = [0]
Output: [0]

Input: nums = [0,0,1]
Output: [1,0,0]

Input: nums = [1,2,3]
Output: [1,2,3]
Cas limite: pas de zéros
```

---

### 5. Best Time to Buy and Sell Stock
**Énoncé:** Reçois les prix d'une action par jour. Tu peux acheter puis vendre UNE SEULE FOIS. Calcule le profit maximal. Si aucun profit, retourne 0.

**Complexité:** O(n) en temps, O(1) en espace  
**Approche:** Une passe, track min prix vu et max profit

**Exemples de test:**
```python
Input: prices = [7,1,5,3,6,4]
Output: 5
Explication: Achat à 1, vente à 6 = profit 5

Input: prices = [7,6,4,3,1]
Output: 0
Explication: Prix décroissants, pas de profit

Input: prices = [2,4,1]
Output: 2
Explication: Achat à 2, vente à 4

Input: prices = [1,1,1,1,1]
Output: 0
Cas limite: tous les prix sont identiques
```

---

### 6. Maximum Subarray (Kadane's Algorithm) ⭐⭐
**Énoncé:** Trouve la sous-partie CONTIGUË d'un tableau dont la somme est maximale. Retourne cette somme maximale.

**Complexité:** O(n) en temps, O(1) en espace  
**Approche:** Programmation dynamique - Kadane's Algorithm

**Exemples de test:**
```python
Input: nums = [-2,1,-3,4,-1,2,1,-5,4]
Output: 6
Explication: Sous-tableau [4,-1,2,1] = 6

Input: nums = [5,4,-1,7,8]
Output: 23
Explication: Tout le tableau

Input: nums = [-2,-1,-3]
Output: -1
Explication: Tous négatifs, retourne le max

Input: nums = [1]
Output: 1
Cas limite: seul élément
```

---

### 7. Missing Number
**Énoncé:** Reçois un tableau contenant tous les nombres de 0 à n, SAUF UN. Retrouve celui qui manque.

**Complexité:** O(n) en temps, O(1) en espace  
**Approche:** Math - formule de somme n*(n+1)/2 ou XOR

**Exemples de test:**
```python
Input: nums = [3,0,1]
Output: 2

Input: nums = [0,1]
Output: 2

Input: nums = [9,6,4,2,3,5,7,0,1]
Output: 8

Input: nums = [0]
Output: 1
Cas limite: manque le dernier
```

---

### 8. Find the Duplicate Number ⭐⭐
**Énoncé:** Le tableau contient n+1 nombres entre 1 et n. UN SEUL est dupliqué. Trouve-le SANS modifier le tableau. Ne peut pas utiliser d'espace supplémentaire (ou O(1) seulement).

**Complexité:** O(n) en temps, O(1) en espace (Floyd's cycle detection)  
**Approche:** Détection de cycle (utilise la liste comme graphe)

**Exemples de test:**
```python
Input: nums = [1,3,4,2,2]
Output: 2

Input: nums = [3,1,3,4,2]
Output: 3

Input: nums = [1,4,4,2,4]
Output: 4

Input: nums = [2,5,9,6,4,3,8,5,7,1]
Output: 5
Cas limite: dupliqué caché
```

---

## Moyen 🟡

### 9. Product of Array Except Self ⭐⭐
**Énoncé:** Pour chaque index i, calcule le produit de TOUS les autres éléments (sauf nums[i]). Interdit d'utiliser la division.

**Complexité:** O(n) en temps, O(n) en espace (output array non compté)  
**Approche:** Prefix et suffix products

**Exemples de test:**
```python
Input: nums = [1,2,3,4]
Output: [24,12,8,6]
Explication:
  - Index 0: 2*3*4 = 24
  - Index 1: 1*3*4 = 12
  - Index 2: 1*2*4 = 8
  - Index 3: 1*2*3 = 6

Input: nums = [-1,1,0,-3,3]
Output: [0,0,9,0,0]

Input: nums = [2,3,4,5]
Output: [60,40,30,24]
```

---

### 10. Rotate Array
**Énoncé:** Tourne le tableau vers la DROITE de `k` pas. Doit être fait sur place et en O(1) espace supplémentaire.

**Complexité:** O(n) en temps, O(1) en espace  
**Approche:** Reverse-Reverse-Reverse technique

**Exemples de test:**
```python
Input: nums = [1,2,3,4,5,6,7], k = 3
Output: [5,6,7,1,2,3,4]
Explication: Rotate right 3 fois

Input: nums = [-1,-100,3,99], k = 2
Output: [3,99,-1,-100]

Input: nums = [1], k = 1
Output: [1]
Cas limite: tableau d'un élément

Input: nums = [1,2,3], k = 6
Output: [1,2,3]
Cas limite: k > n (modulo)
```

---

### 11. Merge Sorted Array
**Énoncé:** Fusionne deux tableaux TRIÉS. Fait la fusion sur place dans nums1 (qui a assez de place à la fin).

**Complexité:** O(m+n) en temps, O(1) en espace  
**Approche:** Two pointers depuis la fin

**Exemples de test:**
```python
Input: nums1 = [1,2,3,0,0,0], m = 3, nums2 = [2,5,6], n = 3
Output: [1,2,2,3,5,6]

Input: nums1 = [4,5,6,0,0,0], m = 3, nums2 = [1,2,3], n = 3
Output: [1,2,3,4,5,6]

Input: nums1 = [1], m = 1, nums2 = [], n = 0
Output: [1]
```

---

### 12. Search in Rotated Sorted Array ⭐⭐
**Énoncé:** Un tableau TRIÉ a été tourné une fois. Cherche la cible et retourne son index (-1 si absent). Complexité doit être O(log n).

**Complexité:** O(log n) en temps, O(1) en espace  
**Approche:** Binary search modifié - détermine quel côté est "normal"

**Exemples de test:**
```python
Input: nums = [4,5,6,7,0,1,2], target = 0
Output: 4

Input: nums = [4,5,6,7,0,1,2], target = 3
Output: -1

Input: nums = [1], target = 1
Output: 0

Input: nums = [1,3], target = 3
Output: 1
```

---

### 13. 3Sum
**Énoncé:** Trouve TOUS les triplets uniques du tableau dont la somme = 0. Pas de doublons dans le résultat.

**Complexité:** O(n²) en temps, O(1) en espace (excluant output)  
**Approche:** Trier + Two pointers

**Exemples de test:**
```python
Input: nums = [-1,0,1,2,-1,-4]
Output: [[-1,-1,2],[-1,0,1]]

Input: nums = [0]
Output: []

Input: nums = [-2,0,1,1,2]
Output: [[-2,0,2],[-2,1,1]]
```

---

### 14. Container With Most Water ⭐
**Énoncé:** Deux pointeurs verticaux à différentes hauteurs. Trouve le container (formé par deux lignes) avec la plus grande area.

**Complexité:** O(n) en temps, O(1) en espace  
**Approche:** Two pointers converging

**Exemples de test:**
```python
Input: height = [1,8,6,2,5,4,8,3,7]
Output: 49
Explication: Entre index 1 et 8, width=7, height=min(8,7)=7, area=49

Input: height = [1,1]
Output: 1

Input: height = [4,3,2,1,4]
Output: 16
Explication: Entre index 0 et 4, width=4, height=min(4,4)=4, area=16
```

---

## Difficile 🔴

### 15. Trapping Rain Water ⭐⭐⭐
**Énoncé:** Après la pluie, l'eau est piégée entre les barres. Calcule le volume total d'eau piégée.

**Complexité:** O(n) en temps, O(n) en espace  
**Approche:** Pre-compute max à gauche et max à droite

**Exemples de test:**
```python
Input: height = [0,1,0,2,1,0,1,3,2,1,2,1]
Output: 6
Explication:
  [0,1,0,2,1,0,1,3,2,1,2,1]
  Au-dessus des barres, l'eau remplie représente 6 unités

Input: height = [4,2,0,3,2,5]
Output: 9

Input: height = [0,1,2]
Output: 0
Cas limite: pente ascendante, pas d'eau
```

---

### 16. Median of Two Sorted Arrays ⭐⭐⭐
**Énoncé:** Trouve la MÉDIANE de deux tableaux TRIÉS. Complexité doit être O(log(min(m,n))).

**Complexité:** O(log(min(m,n))) en temps, O(1) en espace  
**Approche:** Binary search sur le plus petit array

**Exemples de test:**
```python
Input: nums1 = [1,3], nums2 = [2]
Output: 2.0

Input: nums1 = [1,2], nums2 = [3,4]
Output: 2.5

Input: nums1 = [], nums2 = [1]
Output: 1.0

Input: nums1 = [0,0], nums2 = [0,0]
Output: 0.0
```

---

### 17. Sliding Window Maximum ⭐⭐
**Énoncé:** Glisse une fenêtre de taille k sur le tableau. Pour chaque position, retourne le maximum dans la fenêtre.

**Complexité:** O(n) en temps, O(k) en espace  
**Approche:** Deque pour maintenir les maximums

**Exemples de test:**
```python
Input: nums = [1,3,-1,-3,5,3,6,7], k = 3
Output: [3,3,5,5,6,7]
Explication:
  [1,3,-1] -> 3
  [3,-1,-3] -> 3
  [-1,-3,5] -> 5
  ...

Input: nums = [1], k = 1
Output: [1]

Input: nums = [1,-1], k = 1
Output: [1,-1]
```

---

# 🔤 CHAÎNES DE CARACTÈRES / STRINGS

## Facile ⭐

### 1. Valid Anagram
**Énoncé:** Deux strings sont des anagrams si elles contiennent les mêmes caractères avec les mêmes fréquences.

**Complexité:** O(n) en temps, O(1) en espace (26 lettres max)  
**Approche:** Hash map ou sorted

**Exemples de test:**
```python
Input: s = "anagram", t = "nagaram"
Output: True

Input: s = "rat", t = "car"
Output: False

Input: s = "a", t = "a"
Output: True

Input: s = "ab", t = "a"
Output: False
```

---

### 2. Valid Parentheses ⭐
**Énoncé:** Vérifie que les parenthèses `()`, accolades `{}`, crochets `[]` sont valides et correctement imbriquées.

**Complexité:** O(n) en temps, O(n) en espace  
**Approche:** Stack

**Exemples de test:**
```python
Input: s = "()"
Output: True

Input: s = "()[]{}"
Output: True

Input: s = "([{}])"
Output: True

Input: s = "(]"
Output: False

Input: s = "([)]"
Output: False
Cas important: imbrication correcte
```

---

### 3. Reverse String
**Énoncé:** Inverse une string. Doit être fait sur place si c'est une liste.

**Complexité:** O(n) en temps, O(1) en espace  
**Approche:** Two pointers

**Exemples de test:**
```python
Input: s = ["h","e","l","l","o"]
Output: ["o","l","l","e","h"]

Input: s = ["H","a","n","n","a","h"]
Output: ["h","a","n","n","a","H"]

Input: s = ["a"]
Output: ["a"]
```

---

### 4. Palindrome Check
**Énoncé:** Vérifie si une string est un palindrome (lit pareil en avant et arrière). Ignore les espacements et la casse.

**Complexité:** O(n) en temps, O(1) en espace  
**Approche:** Two pointers

**Exemples de test:**
```python
Input: s = "A man, a plan, a canal: Panama"
Output: True

Input: s = "race a car"
Output: False

Input: s = "0P"
Output: False

Input: s = "a"
Output: True
```

---

### 5. First Unique Character in a String
**Énoncé:** Trouve l'index du PREMIER caractère qui n'apparaît qu'une seule fois. Retourne -1 si aucun.

**Complexité:** O(n) en temps, O(26) en espace  
**Approche:** Hash map des fréquences

**Exemples de test:**
```python
Input: s = "leetcode"
Output: 0
Explication: 'l' n'apparaît qu'une fois

Input: s = "loveleetcode"
Output: 2
Explication: 'v' est le premier unique

Input: s = "aabb"
Output: -1

Input: s = "abcabcbb"
Output: -1
```

---

## Moyen 🟡

### 6. Longest Substring Without Repeating Characters ⭐⭐
**Énoncé:** Trouve la LONGUEUR du plus long substring SANS caractères dupliquées.

**Complexité:** O(n) en temps, O(min(m,n)) en espace  
**Approche:** Sliding window avec hash map

**Exemples de test:**
```python
Input: s = "abcabcbb"
Output: 3
Explication: "abc"

Input: s = "bbbbb"
Output: 1
Explication: "b"

Input: s = "pwwkew"
Output: 3
Explication: "wke"

Input: s = "au"
Output: 2

Input: s = " "
Output: 1
```

---

### 7. Group Anagrams ⭐
**Énoncé:** Groupe tous les anagrams ensemble. Retourne une liste de listes.

**Complexité:** O(n*k log k) en temps, O(n*k) en espace (n mots, k longueur max)  
**Approche:** Sorted key as hash

**Exemples de test:**
```python
Input: strs = ["eat","tea","ate","nat","bat"]
Output: [["eat","tea","ate"],["nat"],["bat"]]

Input: strs = [""]
Output: [[""]]

Input: strs = ["a"]
Output: [["a"]]
```

---

### 8. Longest Palindromic Substring ⭐⭐
**Énoncé:** Trouve le PLUS LONG substring qui est un palindrome.

**Complexité:** O(n²) expand around center, O(n) Manacher's algorithm  
**Approche:** Expand around center ou Manacher's

**Exemples de test:**
```python
Input: s = "babad"
Output: "bab" ou "aba"

Input: s = "cbbd"
Output: "bb"

Input: s = "a"
Output: "a"

Input: s = "ac"
Output: "a" ou "c"
```

---

### 9. Edit Distance (Levenshtein Distance) ⭐⭐
**Énoncé:** Nombre minimum d'opérations (insert, delete, replace) pour transformer word1 en word2.

**Complexité:** O(m*n) en temps, O(m*n) en espace  
**Approche:** Dynamic Programming 2D

**Exemples de test:**
```python
Input: word1 = "horse", word2 = "ros"
Output: 3
Explication: 
  - horse -> rorse (replace 'h' with 'r')
  - rorse -> rose (delete 'r')
  - rose -> ros (delete 'e')

Input: word1 = "intention", word2 = "execution"
Output: 5

Input: word1 = "a", word2 = "b"
Output: 1
```

---

### 10. Minimum Window Substring ⭐⭐⭐
**Énoncé:** Trouve le PLUS COURT substring de s qui contient TOUS les caractères de t (avec mêmes fréquences).

**Complexité:** O(n+m) en temps, O(m) en espace  
**Approche:** Sliding window avec tracking de fréquences

**Exemples de test:**
```python
Input: s = "ADOBECODEBANC", t = "ABC"
Output: "BANC"

Input: s = "a", t = "a"
Output: "a"

Input: s = "a", t = "aa"
Output: ""

Input: s = "ab", t = "b"
Output: "b"
```

---

## Difficile 🔴

### 11. Regular Expression Matching ⭐⭐⭐
**Énoncé:** Implémente un matcher regex avec support de '.' (n'importe quel caractère) et '*' (0 ou plus de précédent).

**Complexité:** O(m*n) en temps, O(m*n) en espace  
**Approche:** Dynamic Programming 2D

**Exemples de test:**
```python
Input: s = "aa", p = "a"
Output: False

Input: s = "aa", p = "a*"
Output: True

Input: s = "ab", p = ".*"
Output: True

Input: s = "aab", p = "c*a*b"
Output: True
```

---

# 🔗 LISTES CHAÎNÉES / LINKED LIST

## Facile ⭐

### 1. Reverse Linked List
**Énoncé:** Inverse complètement une liste chaînée. Peut être itératif ou récursif.

**Complexité:** O(n) en temps, O(1) itératif / O(n) récursif en espace  
**Approche:** Three pointers (prev, curr, next)

**Exemples de test:**
```python
Input: head = [1,2,3,4,5]
Output: [5,4,3,2,1]

Input: head = [1,2]
Output: [2,1]

Input: head = []
Output: []

Input: head = [1]
Output: [1]
```

---

### 2. Linked List Cycle ⭐
**Énoncé:** Vérifie s'il y a un cycle dans la liste chaînée.

**Complexité:** O(n) en temps, O(1) en espace  
**Approche:** Floyd's cycle detection (slow & fast pointers)

**Exemples de test:**
```python
Input: head = [3,2,0,-4], pos = 1
Output: True
Explication: Le 2ème nœud pointe vers le 2ème

Input: head = [1,2], pos = 0
Output: True

Input: head = [1], pos = -1
Output: False
```

---

### 3. Merge Two Sorted Lists
**Énoncé:** Fusionne deux listes TRIÉES en une seule liste triée.

**Complexité:** O(n+m) en temps, O(1) en espace  
**Approche:** Parcours simultané

**Exemples de test:**
```python
Input: list1 = [1,2,4], list2 = [1,3,4]
Output: [1,1,2,3,4,4]

Input: list1 = [], list2 = []
Output: []

Input: list1 = [], list2 = [0]
Output: [0]
```

---

### 4. Remove Nth Node From End of List ⭐
**Énoncé:** Supprime le n-ième nœud à partir de la fin. Une passe uniquement.

**Complexité:** O(n) en temps, O(1) en espace  
**Approche:** Two pointers avec distance n

**Exemples de test:**
```python
Input: head = [1,2,3,4,5], n = 2
Output: [1,2,3,5]

Input: head = [1], n = 1
Output: []

Input: head = [1,2], n = 1
Output: [1]

Input: head = [1,2], n = 2
Output: [2]
```

---

### 5. Palindrome Linked List ⭐⭐
**Énoncé:** Vérifie si une liste chaînée est un palindrome.

**Complexité:** O(n) en temps, O(1) en espace  
**Approche:** Trouve le milieu, inverse la 2ème moitié, compare

**Exemples de test:**
```python
Input: head = [1,2,2,1]
Output: True

Input: head = [1,2]
Output: False

Input: head = [9,9,9,9]
Output: True
```

---

### 6. Middle of the Linked List
**Énoncé:** Trouve le nœud du MILIEU de la liste. Si paire, retourne le 2ème milieu.

**Complexité:** O(n) en temps, O(1) en espace  
**Approche:** Slow & fast pointers

**Exemples de test:**
```python
Input: head = [1,2,3,4,5]
Output: [3,4,5]

Input: head = [1,2,3,4,5,6]
Output: [4,5,6]
```

---

## Moyen 🟡

### 7. Add Two Numbers ⭐⭐
**Énoncé:** Deux nombres sont stockés en ordre INVERSE dans des listes. Additionne-les et retourne le résultat en liste.

**Complexité:** O(max(m,n)) en temps, O(max(m,n)) en espace  
**Approche:** Parcours avec carry

**Exemples de test:**
```python
Input: l1 = [2,4,3], l2 = [5,6,4]
Output: [7,0,8]
Explication: 342 + 465 = 807

Input: l1 = [0], l2 = [0]
Output: [0]

Input: l1 = [9,9,9,9,9,9,9], l2 = [9,9,9,9]
Output: [8,9,9,9,0,0,0,1]
```

---

### 8. Copy List with Random Pointer ⭐⭐
**Énoncé:** Copie une liste chaînée spéciale où chaque nœud a un pointeur `random` vers n'importe quel nœud (ou null).

**Complexité:** O(n) en temps, O(n) en espace  
**Approche:** Hash map pour mapper old -> new

**Exemples de test:**
```python
Input: head = [[7,null],[13,0],[11,4],[10,2],[1,0]]
Output: [[7,null],[13,0],[11,4],[10,2],[1,0]]
Explication: Une copie profonde
```

---

### 9. Linked List Cycle II ⭐⭐
**Énoncé:** S'il y a un cycle, retourne le nœud où le cycle COMMENCE. Sinon null.

**Complexité:** O(n) en temps, O(1) en espace  
**Approche:** Floyd's + trouver point d'intersection

**Exemples de test:**
```python
Input: head = [3,2,0,-4], pos = 1
Output: Node with value 2
Explication: Le cycle commence au 2ème nœud

Input: head = [1,2], pos = 0
Output: Node with value 1

Input: head = [1], pos = -1
Output: None
```

---

### 10. Reorder List ⭐
**Énoncé:** Réorganise la liste en alternant le début et la fin:
L0 → L1 → … → Ln-1 → Ln
devient
L0 → Ln → L1 → Ln-1 → L2 → Ln-2 → …

**Complexité:** O(n) en temps, O(1) en espace  
**Approche:** Trouve milieu, inverse la 2ème moitié, merge

**Exemples de test:**
```python
Input: head = [1,2,3,4]
Output: [1,4,2,3]

Input: head = [1,2,3,4,5]
Output: [1,5,2,4,3]
```

---

## Difficile 🔴

### 11. Reverse Nodes in k-Group ⭐⭐⭐
**Énoncé:** Inverse les nœuds d'une liste par groupes de k. Si < k nœuds à la fin, les laisser en place.

**Complexité:** O(n) en temps, O(1) en espace  
**Approche:** Reverse chaque groupe récursivement

**Exemples de test:**
```python
Input: head = [1,2,3,4,5], k = 2
Output: [2,1,4,3,5]

Input: head = [1,2,3,4,5], k = 3
Output: [3,2,1,4,5]

Input: head = [1,2], k = 2
Output: [2,1]
```

---

### 12. Merge k Sorted Lists ⭐⭐⭐
**Énoncé:** Fusionne k listes chaînées TRIÉES en une seule liste triée.

**Complexité:** O(n log k) en temps avec heap, O(n) en espace  
**Approche:** Min-heap ou divide & conquer

**Exemples de test:**
```python
Input: lists = [[1,4,5],[1,3,4],[2,6]]
Output: [1,1,2,3,4,4,5,6]

Input: lists = []
Output: []

Input: lists = [[]]
Output: []
```

---

# 🌳 ARBRES / TREES

## Facile ⭐

### 1. Binary Tree Traversals (Inorder, Preorder, Postorder) ⭐
**Énoncé:** Traverse un arbre binaire dans les trois ordres DFS (depth-first search).

**Complexité:** O(n) en temps, O(h) en espace (h = hauteur)

#### Inorder (Left-Root-Right):
```python
Input: root = [1,null,2,3]
Output: [1,3,2]

Input: root = []
Output: []
```

#### Preorder (Root-Left-Right):
```python
Input: root = [1,null,2,3]
Output: [1,2,3]
```

#### Postorder (Left-Right-Root):
```python
Input: root = [1,null,2,3]
Output: [3,2,1]
```

---

### 2. Maximum Depth of Binary Tree
**Énoncé:** Trouve la PROFONDEUR MAXIMALE (nombre de nœuds dans le chemin le plus long).

**Complexité:** O(n) en temps, O(h) en espace  
**Approche:** DFS récursif

**Exemples de test:**
```python
Input: root = [3,9,20,null,null,15,7]
Output: 3

Input: root = [1,null,2]
Output: 2

Input: root = []
Output: 0
```

---

### 3. Symmetric Tree
**Énoncé:** Vérifie si un arbre binaire est symétrique (miroir).

**Complexité:** O(n) en temps, O(h) en espace  
**Approche:** DFS récursif, compare mirrored subtrees

**Exemples de test:**
```python
Input: root = [1,2,2,3,4,4,3]
Output: True

Input: root = [1,2,2,null,3,null,3]
Output: False
```

---

### 4. Invert Binary Tree
**Énoncé:** Inverse complètement l'arbre (échange gauche/droite pour chaque nœud).

**Complexité:** O(n) en temps, O(h) en espace  
**Approche:** DFS récursif

**Exemples de test:**
```python
Input: root = [4,2,7,1,3,6,9]
Output: [4,7,2,9,6,3,1]

Input: root = [2,1,3]
Output: [2,3,1]
```

---

### 5. Path Sum
**Énoncé:** Vérifie s'il existe un chemin racine-feuille dont la somme = target.

**Complexité:** O(n) en temps, O(h) en espace  
**Approche:** DFS avec tracking de la somme

**Exemples de test:**
```python
Input: root = [5,4,8,11,null,13,4,7,2,null,1], targetSum = 22
Output: True
Explication: Path 5->4->11->2 = 22

Input: root = [1,2,3], targetSum = 5
Output: False
```

---

### 6. Same Tree
**Énoncé:** Vérifie si deux arbres binaires sont IDENTIQUES.

**Complexité:** O(min(m,n)) en temps, O(min(h1,h2)) en espace  
**Approche:** DFS récursif

**Exemples de test:**
```python
Input: p = [1,2,3], q = [1,2,3]
Output: True

Input: p = [1,2], q = [1,null,2]
Output: False
```

---

## Moyen 🟡

### 7. Validate Binary Search Tree ⭐⭐
**Énoncé:** Vérifie qu'un arbre binaire est un BST valide.

**Complexité:** O(n) en temps, O(h) en espace  
**Approche:** DFS avec min/max bounds

**Exemples de test:**
```python
Input: root = [2,1,3]
Output: True

Input: root = [5,1,4,null,null,3,6]
Output: False
Explication: 4 et 6 sous 5 mais 6 > 5 donc invalide

Input: root = [2,2,2]
Output: False
```

---

### 8. Lowest Common Ancestor ⭐⭐
**Énoncé:** Trouve le nœud ancêtre commun le plus PROCHE (LCA) de deux nœuds dans un BST.

**Complexité:** O(log n) average, O(n) worst en temps, O(1) en espace  
**Approche:** Traverse le BST selon les valeurs

**Exemples de test:**
```python
Input: root = [6,2,8,0,4,7,9,null,null,3,5], p = 2, q = 8
Output: 6

Input: root = [6,2,8,0,4,7,9,null,null,3,5], p = 2, q = 4
Output: 2
```

---

### 9. Binary Tree Level Order Traversal ⭐
**Énoncé:** Traverse l'arbre par NIVEAUX (BFS), retourne liste de listes.

**Complexité:** O(n) en temps, O(w) en espace (w = largeur max)  
**Approche:** BFS avec queue

**Exemples de test:**
```python
Input: root = [3,9,20,null,null,15,7]
Output: [[3],[9,20],[15,7]]

Input: root = [1]
Output: [[1]]

Input: root = []
Output: []
```

---

### 10. Construct Binary Tree from Inorder and Preorder ⭐⭐
**Énoncé:** Reconstruit un arbre binaire à partir de ses traversals Inorder et Preorder.

**Complexité:** O(n) en temps, O(n) en espace  
**Approche:** Preorder donne racine, Inorder donne gauche/droite

**Exemples de test:**
```python
Input: preorder = [3,9,20,15,7], inorder = [9,3,15,20,7]
Output: [3,9,20,null,null,15,7]

Input: preorder = [-1], inorder = [-1]
Output: [-1]
```

---

### 11. Serialize and Deserialize Binary Tree ⭐⭐⭐
**Énoncé:** Encode un arbre dans une string et décode-la pour reconstructir l'arbre.

**Complexité:** O(n) en temps, O(n) en espace  
**Approche:** Preorder traversal avec markers pour null

**Exemples de test:**
```python
Input: root = [1,2,3,null,null,4,5]
Output: "1,2,#,#,3,4,#,#,5,#,#"
Puis décode pour récupérer le même arbre
```

---

### 12. Maximum Path Sum ⭐⭐⭐
**Énoncé:** Trouve le chemin dans l'arbre avec la somme MAXIMALE (peut être n'importe quel chemin, pas forcément racine-feuille).

**Complexité:** O(n) en temps, O(h) en espace  
**Approche:** DFS post-order avec global max

**Exemples de test:**
```python
Input: root = [1,2,3]
Output: 6
Explication: Path 2->1->3 = 6

Input: root = [-10]
Output: -10
Cas limite: seul négatif
```

---

## Difficile 🔴

### 13. Binary Tree Maximum Path Sum ⭐⭐⭐
Voir ci-dessus - très important!

---

### 14. Vertical Order Traversal ⭐⭐
**Énoncé:** Traverse l'arbre verticalement (colonnes) et retourne les nœuds groupés par colonne.

**Complexité:** O(n log n) en temps, O(n) en espace  
**Approche:** DFS avec tracking de position (row, col)

**Exemples de test:**
```python
Input: root = [3,9,20,null,null,15,7]
Output: [[9],[3,15],[20],[7]]

Input: root = [1,2,3,4,5,6,7]
Output: [[4],[2],[1,5,6],[3],[7]]
```

---

# 📊 GRAPHES / GRAPHS

## Facile ⭐

### 1. Number of Islands ⭐
**Énoncé:** Compte le nombre d'îles (groupe de 1 connectés adjacemment) dans une grille de 0 et 1.

**Complexité:** O(m*n) en temps, O(m*n) worst en espace  
**Approche:** DFS ou BFS

**Exemples de test:**
```python
Input: grid = [
  ["1","1","1","1","0"],
  ["1","1","0","1","0"],
  ["1","1","0","0","0"],
  ["0","0","0","0","0"]
]
Output: 1

Input: grid = [
  ["1","1","0","0","0"],
  ["1","1","0","0","0"],
  ["0","0","1","0","0"],
  ["0","0","0","1","1"]
]
Output: 3
```

---

### 2. Flood Fill
**Énoncé:** Remplit une région avec une nouvelle couleur (comme l'outil bucket paint).

**Complexité:** O(m*n) en temps, O(m*n) worst en espace  
**Approche:** DFS ou BFS

**Exemples de test:**
```python
Input: image = [[1,1,1],[1,1,0],[1,0,1]], sr = 1, sc = 1, color = 2
Output: [[2,2,2],[2,2,0],[2,0,1]]

Input: image = [[0,0,0],[0,0,0]], sr = 0, sc = 0, color = 0
Output: [[0,0,0],[0,0,0]]
```

---

## Moyen 🟡

### 3. Clone Graph ⭐⭐
**Énoncé:** Crée une copie profonde d'un graphe.

**Complexité:** O(n+e) en temps, O(n) en espace  
**Approche:** DFS/BFS avec hash map pour mapper old -> new

**Exemples de test:**
```python
Input: adjList = [[2,4],[1,3],[2,4],[1,3]]
Output: Une copie complète du graphe
```

---

### 4. Course Schedule (Topological Sort) ⭐⭐
**Énoncé:** Vérifie s'il est possible de terminer tous les cours (DAG ou cycle?).

**Complexité:** O(n+e) en temps, O(n+e) en espace  
**Approche:** Topological sort avec Kahn's algorithm

**Exemples de test:**
```python
Input: numCourses = 2, prerequisites = [[1,0]]
Output: True

Input: numCourses = 2, prerequisites = [[1,0],[0,1]]
Output: False
Explication: Cycle détecté
```

---

### 5. Number of Connected Components in an Undirected Graph ⭐
**Énoncé:** Compte le nombre de composantes connectées.

**Complexité:** O(n+e) en temps, O(n) en espace  
**Approche:** DFS/BFS ou Union-Find

**Exemples de test:**
```python
Input: n = 5, edges = [[0,1],[1,2],[3,4]]
Output: 2
Explication: [0,1,2] et [3,4]

Input: n = 5, edges = [[0,1],[1,2],[2,3],[3,4]]
Output: 1
Explication: Tout connecté
```

---

### 6. Accounts Merge (Union-Find) ⭐⭐⭐
**Énoncé:** Compte d'email multiples possibles - fusionne les comptes d'une même personne.

**Complexité:** O(n*k log n) en temps, O(n*k) en espace  
**Approche:** Union-Find (Disjoint Set)

**Exemples de test:**
```python
Input: accounts = [["John","johnsmith@mail.com","john_newyork@mail.com"],
                   ["John","johnsmith@mail.com","john00@mail.com"],
                   ["Mary","mary@mail.com"],
                   ["John","johnnybravo@mail.com"]]
Output: [["John","john00@mail.com","john_newyork@mail.com","johnsmith@mail.com"],
         ["Mary","mary@mail.com"],
         ["John","johnnybravo@mail.com"]]
```

---

### 7. Pacific Atlantic Water Flow ⭐⭐
**Énoncé:** Trouve les cellules d'une matrice d'où l'eau peut s'écouler vers les deux océans.

**Complexité:** O(m*n) en temps, O(m*n) en espace  
**Approche:** DFS rétrograde depuis les bords

**Exemples de test:**
```python
Input: heights = [[4,2,7,3,4],[7,4,6,5,2],[8,7,2,4,9],[3,8,1,2,3],[7,4,8,1,0]]
Output: [[0,2],[0,4],[1,0],[1,1],[1,2],[1,3],[1,4],[2,0],[2,1],[2,2],[2,3],[2,4],[3,0],[3,1],[3,2],[3,3],[3,4],[4,0],[4,1],[4,2],[4,3],[4,4]]
```

---

## Difficile 🔴

### 8. Critical Connections in a Network (Bridges) ⭐⭐⭐
**Énoncé:** Trouve tous les bridges (arêtes critiques) dans un graphe non-dirigé.

**Complexité:** O(n+e) en temps, O(n+e) en espace  
**Approche:** Tarjan's algorithm ou DFS avec discovery/low times

**Exemples de test:**
```python
Input: n = 4, connections = [[0,1],[1,2],[2,0],[1,3]]
Output: [[1,3]]
Explication: Enlever [1,3] déconnecte le graphe
```

---

### 9. Word Ladder ⭐⭐⭐
**Énoncé:** Transforme un mot en un autre en changeant une lettre à la fois (tous dans une liste).

**Complexité:** O(n*l²*26) en temps, O(n*l) en espace  
**Approche:** BFS

**Exemples de test:**
```python
Input: beginWord = "hit", endWord = "cog", wordList = ["hot","dot","dog","lot","log","cog"]
Output: 5
Explication: hit -> hot -> dot -> dog -> cog

Input: beginWord = "hit", endWord = "cog", wordList = ["hot","dot","dog","lot","log"]
Output: 0
Explication: "cog" n'est pas dans la liste
```

---

# 💰 PROGRAMMATION DYNAMIQUE / DYNAMIC PROGRAMMING

## Facile ⭐

### 1. Climbing Stairs
**Énoncé:** Tu grimpes n marches. À chaque étape tu peux monter 1 ou 2 marches. Compte les manières différentes.

**Complexité:** O(n) en temps, O(1) en espace (optimisé)  
**Approche:** DP - c'est la séquence Fibonacci!

**Exemples de test:**
```python
Input: n = 2
Output: 2
Explication: 1+1, 2

Input: n = 3
Output: 3
Explication: 1+1+1, 1+2, 2+1

Input: n = 4
Output: 5
```

---

### 2. House Robber ⭐⭐
**Énoncé:** Les maisons sont en ligne. Tu peux voler l'argent mais pas deux maisons adjacentes. Maximise!

**Complexité:** O(n) en temps, O(1) en espace  
**Approche:** DP - max(rob current + 2 back, rob previous)

**Exemples de test:**
```python
Input: nums = [1,2,3,1]
Output: 4
Explication: Rob house 1 (1) + house 3 (3) = 4

Input: nums = [2,7,9,3,1]
Output: 12
Explication: Rob houses 1, 3, 5 = 2+9+1 = 12
```

---

## Moyen 🟡

### 3. Coin Change ⭐⭐
**Énoncé:** Nombre MINIMUM de pièces pour faire une somme donnée.

**Complexité:** O(n*m) en temps, O(m) en espace  
**Approche:** DP bottom-up

**Exemples de test:**
```python
Input: coins = [1,2,5], amount = 5
Output: 2
Explication: 5+0 ou 2+2+1

Input: coins = [2], amount = 3
Output: -1
Explication: Impossible

Input: coins = [10], amount = 10
Output: 1
```

---

### 4. Longest Increasing Subsequence (LIS) ⭐⭐
**Énoncé:** Trouve la LONGUEUR de la plus longue sous-séquence strictement croissante (pas forcément contiguë).

**Complexité:** O(n²) DP, O(n log n) binary search  
**Approche:** DP ou patience sorting with binary search

**Exemples de test:**
```python
Input: nums = [10,9,2,5,3,7,101,18]
Output: 4
Explication: [2,3,7,101]

Input: nums = [0,1,0,4,4,4,3,2,1]
Output: 2
```

---

### 5. Decode Ways ⭐⭐
**Énoncé:** Les chiffres 1-26 correspondent aux lettres. Compte les manières différentes de décoder.

**Complexité:** O(n) en temps, O(1) en espace  
**Approche:** DP

**Exemples de test:**
```python
Input: s = "12"
Output: 2
Explication: "1,2" ou "12"

Input: s = "226"
Output: 3
Explication: "2,2,6", "22,6", "2,26"

Input: s = "06"
Output: 0
Explication: 0 en début invalide
```

---

### 6. Partition Equal Subset Sum ⭐⭐
**Énoncé:** Vérifie si on peut partitioner le tableau en deux subsets avec sommes égales.

**Complexité:** O(n*sum) en temps, O(sum) en espace  
**Approche:** 0/1 Knapsack problem

**Exemples de test:**
```python
Input: nums = [1,5,11,5]
Output: True
Explication: [11] et [5,5,1]

Input: nums = [1,2,3,5]
Output: False
```

---

### 7. Unique Paths ⭐
**Énoncé:** Compte les manières différentes de traverser une grille du coin haut-gauche au bas-droit (droite/bas seulement).

**Complexité:** O(m*n) en temps, O(m*n) en espace  
**Approche:** DP 2D

**Exemples de test:**
```python
Input: m = 3, n = 7
Output: 28

Input: m = 3, n = 2
Output: 3

Input: m = 1, n = 1
Output: 1
```

---

## Difficile 🔴

### 8. Edit Distance (Levenshtein) ⭐⭐⭐
**Énoncé:** Nombre minimum d'opérations (insert, delete, replace) pour transformer word1 en word2.

**Complexité:** O(m*n) en temps, O(m*n) en espace  
**Approche:** DP 2D classique

**Exemples de test:**
```python
Input: word1 = "horse", word2 = "ros"
Output: 3

Input: word1 = "intention", word2 = "execution"
Output: 5
```

---

### 9. Burst Balloons ⭐⭐⭐
**Énoncé:** Tableau de ballons avec valeurs. Les ôter donne des points (valeur du ballon * voisins).

**Complexité:** O(n³) en temps, O(n²) en espace  
**Approche:** Interval DP

**Exemples de test:**
```python
Input: nums = [3,1,5,8]
Output: 167
Explication: Burst dans l'ordre [1,5,3,8] pour 1*3*5 + 5*3*8 + 3*8 + 8
```

---

# 🗺️ GÉOSPATIAL / GIS & GÉOMÉTRIE

## Facile ⭐

### 1. Point in Rectangle
**Énoncé:** Vérifie si un point P(x,y) est INSIDE un rectangle avec coins (x1,y1) et (x2,y2).

**Complexité:** O(1) en temps, O(1) en espace  
**Approche:** Vérification simple d'inégalités

**Exemples de test:**
```python
Input: x1=0, y1=0, x2=10, y2=10, px=5, py=5
Output: True

Input: x1=0, y1=0, x2=10, y2=10, px=10, py=10
Output: True (sur la bordure)

Input: x1=0, y1=0, x2=10, y2=10, px=11, py=5
Output: False
```

---

### 2. Distance Between Two Points
**Énoncé:** Distance euclidienne entre P1(x1,y1) et P2(x2,y2).

**Complexité:** O(1) en temps, O(1) en espace  
**Approche:** Formule distance = √((x2-x1)² + (y2-y1)²)

**Exemples de test:**
```python
Input: P1=(0,0), P2=(3,4)
Output: 5.0

Input: P1=(1,1), P2=(1,1)
Output: 0.0
```

---

## Moyen 🟡

### 3. Convex Hull ⭐⭐⭐
**Énoncé:** Trouve l'envelope convexe d'un ensemble de points (plus petit polygone contenant tous).

**Complexité:** O(n log n) en temps, O(n) en espace  
**Approche:** Graham scan ou Jarvis march

**Exemples de test:**
```python
Input: points = [[1,1],[1,0],[0,0],[0,1]]
Output: [[0,0],[1,0],[1,1],[0,1]]

Input: points = [[0,0],[0,4],[4,4],[3,1],[4,0]]
Output: [[0,0],[4,0],[4,4],[0,4]]
```

---

### 4. Line Intersection
**Énoncé:** Vérifie si deux segments de lignes se croisent.

**Complexité:** O(1) en temps, O(1) en espace  
**Approche:** Vector cross product

**Exemples de test:**
```python
Input: (0,0)-(2,2) et (0,2)-(2,0)
Output: True
Explication: Croisement au centre

Input: (0,0)-(1,1) et (2,2)-(3,3)
Output: False
Explication: Parallèles
```

---

### 5. Point in Polygon ⭐⭐
**Énoncé:** Vérifie si un point est INSIDE un polygon quelconque.

**Complexité:** O(n) en temps, O(1) en espace  
**Approche:** Ray casting algorithm

**Exemples de test:**
```python
Input: polygon = [[0,0],[4,0],[4,3],[2,4],[0,3]], point = [2,2]
Output: True

Input: polygon = [[0,0],[4,0],[4,3],[2,4],[0,3]], point = [2,4]
Output: False (sur la bordure, peut dépendre de la définition)
```

---

## Difficile 🔴

### 6. Closest Pair of Points ⭐⭐⭐
**Énoncé:** Trouve la PAIRE DE POINTS avec la plus PETITE distance.

**Complexité:** O(n log n) en temps, O(n) en espace  
**Approche:** Divide & conquer

**Exemples de test:**
```python
Input: points = [[0,0],[1,1],[2,2],[10,10]]
Output: 1.414...
Explication: Distance entre [0,0] et [1,1]
```

---

### 7. Rotating Calipers
**Énoncé:** Trouve le plus PETIT bounding rectangle d'un ensemble de points.

**Complexité:** O(n) après sorting  
**Approche:** Algorithme des calipers rotatifs

---

### 8. Voronoi Diagram Basics
**Énoncé:** Partition l'espace en régions pour chaque point (plus proche).

**Complexité:** O(n log n) en temps  
**Approche:** Fortune's algorithm (avancé)

---

### 9. Delaunay Triangulation
**Énoncé:** Triangulation optimale - maximise les angles minimums des triangles.

**Complexité:** O(n log n) en temps  
**Approche:** Incremental algorithm ou divide & conquer

---

# 🗄️ SQL

## Queries de Base

### 1. SELECT avec WHERE
**Énoncé:** Filtre les lignes selon une condition.

```sql
SELECT * FROM employees WHERE salary > 50000;
SELECT name, age FROM employees WHERE age >= 30 AND department = 'IT';
```

---

### 2. JOIN (INNER, LEFT, RIGHT, FULL)
**Énoncé:** Combine les données de plusieurs tables.

```sql
-- INNER JOIN: seulement correspondances
SELECT e.name, d.dept_name 
FROM employees e 
INNER JOIN departments d ON e.dept_id = d.id;

-- LEFT JOIN: tout de gauche + matches
SELECT e.name, d.dept_name 
FROM employees e 
LEFT JOIN departments d ON e.dept_id = d.id;
```

---

### 3. GROUP BY et HAVING
**Énoncé:** Groupe les données et filtre les groupes.

```sql
SELECT department, COUNT(*) as count 
FROM employees 
GROUP BY department 
HAVING COUNT(*) > 5;
```

---

### 4. Window Functions ⭐⭐
**Énoncé:** Calculs sur des "fenêtres" de lignes.

```sql
-- ROW_NUMBER, RANK, DENSE_RANK
SELECT name, salary, 
       ROW_NUMBER() OVER (ORDER BY salary DESC) as rank
FROM employees;

-- Running sum
SELECT name, salary,
       SUM(salary) OVER (ORDER BY hire_date) as running_total
FROM employees;
```

---

### 5. CTEs (Common Table Expressions) ⭐
**Énoncé:** Requête temporaire réutilisable.

```sql
WITH high_earners AS (
  SELECT * FROM employees WHERE salary > 100000
)
SELECT * FROM high_earners WHERE department = 'IT';

-- Recursive CTE
WITH RECURSIVE numbers AS (
  SELECT 1 as n
  UNION ALL
  SELECT n+1 FROM numbers WHERE n < 10
)
SELECT * FROM numbers;
```

---

## Moyen 🟡

### 6. Self Join
**Énoncé:** Jointure d'une table avec elle-même.

```sql
-- Trouvez les employés et leurs managers
SELECT e1.name as employee, e2.name as manager
FROM employees e1
LEFT JOIN employees e2 ON e1.manager_id = e2.id;
```

---

### 7. Subqueries
**Énoncé:** Requête imbriquée.

```sql
-- Scalar subquery
SELECT name, salary 
FROM employees 
WHERE salary > (SELECT AVG(salary) FROM employees);

-- IN subquery
SELECT * FROM products 
WHERE category_id IN (SELECT id FROM categories WHERE active = 1);
```

---

### 8. UNION / UNION ALL
**Énoncé:** Combine les résultats de plusieurs requêtes.

```sql
SELECT name, 'Employee' as type FROM employees
UNION
SELECT name, 'Manager' as type FROM managers;
```

---

## Difficile 🔴

### 9. Recursive Queries
**Énoncé:** Requêtes récursives pour données hiérarchiques.

```sql
-- Arborescence organisationnelle
WITH RECURSIVE org_tree AS (
  SELECT id, name, manager_id, 1 as level
  FROM employees
  WHERE manager_id IS NULL
  
  UNION ALL
  
  SELECT e.id, e.name, e.manager_id, ot.level + 1
  FROM employees e
  JOIN org_tree ot ON e.manager_id = ot.id
)
SELECT * FROM org_tree ORDER BY level, name;
```

---

### 10. Complex Window Functions
**Énoncé:** Analyses avancées avec WINDOW functions.

```sql
-- Percentile
SELECT name, salary,
       PERCENT_RANK() OVER (ORDER BY salary) as percentile
FROM employees;

-- LAG/LEAD pour valeurs précédentes/suivantes
SELECT name, salary,
       LAG(salary) OVER (ORDER BY hire_date) as prev_salary,
       LEAD(salary) OVER (ORDER BY hire_date) as next_salary
FROM employees;
```

---

# 🌐 PostGIS (Geographic Information Systems)

## Facile ⭐

### 1. ST_Distance
**Énoncé:** Distance entre deux géométries (points, lignes, polygones).

```sql
SELECT ST_Distance(
  ST_GeomFromText('POINT(0 0)'),
  ST_GeomFromText('POINT(3 4)')
) as distance;
-- Result: 5.0
```

---

### 2. ST_Contains
**Énoncé:** Vérifie si une géométrie contient une autre.

```sql
SELECT ST_Contains(
  ST_GeomFromText('POLYGON((0 0, 4 0, 4 3, 0 3, 0 0))'),
  ST_GeomFromText('POINT(2 2)')
) as contained;
-- Result: true
```

---

### 3. ST_Intersects
**Énoncé:** Vérifie si deux géométries se croisent.

```sql
SELECT ST_Intersects(
  ST_GeomFromText('LINESTRING(0 0, 2 2)'),
  ST_GeomFromText('LINESTRING(0 2, 2 0)')
) as intersects;
-- Result: true
```

---

### 4. Buffer Operations
**Énoncé:** Crée une zone tampon autour d'une géométrie.

```sql
-- Zone de 1km autour d'un point
SELECT ST_Buffer(
  ST_GeomFromText('POINT(-73.97 40.77)'),
  0.01
) as buffer_zone;
```

---

## Moyen 🟡

### 5. ST_DWithin ⭐
**Énoncé:** Vérifie si deux géométries sont DANS une distance donnée.

```sql
SELECT city_name 
FROM cities
WHERE ST_DWithin(
  location, 
  ST_GeomFromText('POINT(-73.97 40.77)'),
  1000  -- 1km en mètres
);
```

---

### 6. Spatial Joins
**Énoncé:** Jointure basée sur les relations spatiales.

```sql
-- Tous les magasins WITHIN une zone
SELECT s.name, z.zone_name
FROM stores s
JOIN zones z ON ST_Within(s.location, z.boundary);
```

---

### 7. Coordinate Transformation (ST_Transform) ⭐
**Énoncé:** Convertit entre différents systèmes de coordonnées.

```sql
-- WGS84 vers Web Mercator
SELECT ST_Transform(
  ST_GeomFromText('POINT(-73.97 40.77)', 4326),
  3857
) as mercator_point;
```

---

### 8. Nearest Neighbor Search
**Énoncé:** Trouve les points les plus proches (KNN).

```sql
SELECT name, location
FROM restaurants
ORDER BY location <-> ST_GeomFromText('POINT(-73.97 40.77)')
LIMIT 10;
```

---

## Difficile 🔴

### 9. Complex Spatial Analysis ⭐⭐
**Énoncé:** Analyses spatiales avancées.

```sql
-- Points en clusters
SELECT ST_ClusterDBSCAN(geom, eps := 10, minpoints := 5) as cluster_id,
       COUNT(*) as point_count
FROM points
GROUP BY cluster_id;
```

---

### 10. PostGIS Performance Tuning ⭐⭐
**Énoncé:** Optimisation des requêtes spatiales.

```sql
-- Index spatial (GIST ou BRIN)
CREATE INDEX idx_locations ON restaurants USING GIST(location);

-- Utiliser les index efficacement
SELECT * FROM restaurants 
WHERE location && ST_Buffer(ST_GeomFromText('POINT(0 0)'), 1000);
```

---

# ⚡ ALGORITHMES DE RECHERCHE & TRI

## Facile ⭐

### 1. Binary Search
**Énoncé:** Recherche dans un tableau TRIÉ. O(log n).

**Exemples:**
```python
Input: nums = [-1,0,3,5,9,12], target = 9
Output: 4

Input: nums = [-1,0,3,5,9,12], target = 13
Output: -1
```

---

### 2. Bubble Sort
```python
def bubbleSort(arr):
    n = len(arr)
    for i in range(n):
        for j in range(0, n-i-1):
            if arr[j] > arr[j+1]:
                arr[j], arr[j+1] = arr[j+1], arr[j]
```
**Complexité:** O(n²)

---

## Moyen 🟡

### 3. Quick Sort ⭐
**Complexité:** O(n log n) avg, O(n²) worst

---

### 4. Merge Sort
**Complexité:** O(n log n) garantie

---

### 5. Heap Sort
**Complexité:** O(n log n)

---

# ✨ TECHNIQUES AVANCÉES

1. **Two Pointers** - Résout efficacement les problèmes de paires/triplets
2. **Sliding Window** - Optimise les problèmes de subarrays/substrings
3. **DFS/BFS** - Parcours de graphes et arbres
4. **Backtracking** - Explore toutes les solutions possibles
5. **Greedy** - Choix optimal local = optimal global
6. **Divide & Conquer** - Divise le problème récursivement
7. **Bit Manipulation** - Opérations binaires efficaces
8. **Union-Find** - Gère les composantes connectées
9. **Topological Sort** - Ordonne les dépendances
10. **Floyd's Cycle Detection** - Détecte les cycles

---

*Last updated: 2026-07-06*
*Cette feuille de route couvre les concepts essentiels pour réussir les entretiens techniques.*
