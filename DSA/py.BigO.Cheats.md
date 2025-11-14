
# **Python DS & Methods – Master Cheatsheet**

## **1️⃣ Numbers**

* `int, float, complex` → arithmetic, type conversion → **O(1) time & space**
* `abs(x), pow(x,y)` → **O(1)**

---

## **2️⃣ Strings (Immutable)**

* Index: `s[i]` → O(1), Slice: `s[start:stop:step]` → O(k)
* Concat: `s1+s2` → O(n+m), Repeat: `s*k` → O(n*k)
* Methods: `.lower()/.upper()/.strip()/.replace()/.split()/''.join(list)` → O(n)
* Membership: `'x' in s` → O(n)
* Helpers: palindrome check, sliding window, case conversion → O(n)

---

## **3️⃣ Lists / Arrays**

* Index: O(1), Append: O(1) amortized, Insert/remove: O(n), Pop(end): O(1)
* Slice copy: O(k), Sort: O(n log n), Reverse: O(n)
* 2D Lists: `matrix[i][j]` → O(1), Iteration → O(rows*cols)

---

## **4️⃣ Tuples**

* Immutable list, Index O(1), Convert: `list(t)` / `tuple(list)` → O(n)

---

## **5️⃣ Sets**

* Unordered, unique
* Add/remove/check: O(1) avg
* Union/intersect/diff: O(min(len(a),len(b)))

---

## **6️⃣ Dictionaries / HashMap**

* Access/Insert/Delete: O(1) avg
* Iteration `.keys()/.values()/.items()` → O(n)

---

## **7️⃣ Deque / Queue**

```python
from collections import deque
q.append()/appendleft()/pop()/popleft() → O(1)
```

---

## **8️⃣ Stack**

* List: `.append()` / `.pop()` → O(1) LIFO

---

## **9️⃣ LinkedList**

* Append: O(n) (O(1) w/ tail), Prepend: O(1), Delete/search: O(n)

---

## **🔟 Trees**

* Node: `val, left, right`
* Traversals (in/pre/post) → O(n) time, O(h) space
* BST access/insert/delete → O(log n) avg, O(n) worst

---

## **1️⃣1️⃣ Graphs**

* Adj List: `dict[node]=[neighbors]` → O(V+E) traversal
* Adj Matrix: `matrix[n][n]` → O(V²) space
* BFS/DFS → O(V+E) time, O(V) space

---

## **1️⃣2️⃣ Heap / PriorityQueue**

```python
import heapq
heapify(list) → O(n)
heappush / heappop → O(log n)
peek min → O(1)
```

---

## **1️⃣3️⃣ Counter / defaultdict**

```python
from collections import Counter, defaultdict
Counter(list) → freq count O(n)
dd = defaultdict(list) → O(1) insert
```

---

## **1️⃣4️⃣ Advanced Helpers**

* `enumerate()`, `zip()`, `map()`, `filter()` → O(n)
* `all()/any()`, `min()/max(key=func)`, `reversed()` → O(n)
* `deepcopy()` vs `copy()` → O(n)

---

## **1️⃣5️⃣ Composite Structures**

* List of lists, Dict of lists, Array of sets → O(1) access per element, O(k) iterate inner
* Tree/Graph as HashMap of arrays → O(V+E) traverse

---

## **📊 Quick Big-O Summary**

| DS / Method      | Access   | Insert   | Delete   | Search | Notes                 |
| ---------------- | -------- | -------- | -------- | ------ | --------------------- |
| List             | O(1)     | O(n)     | O(n)     | O(n)   | append O(1) amortized |
| Tuple            | O(1)     | –        | –        | O(n)   | immutable             |
| Set              | O(1)     | O(1)     | O(1)     | O(1)   | avg case              |
| Dict             | O(1)     | O(1)     | O(1)     | O(1)   | avg case              |
| Stack / Queue    | O(1)     | O(1)     | O(1)     | –      | deque recommended     |
| LinkedList       | O(n)     | O(1)     | O(n)     | O(n)   | depends on head/tail  |
| Tree (BT/BST)    | O(log n) | O(log n) | O(log n) | O(n)   | binary, balanced      |
| Graph (adj list) | O(V+E)   | O(1)     | O(1)     | O(V+E) | traversal cost        |
| Heap             | O(n)     | O(log n) | O(log n) | O(n)   | min/max heap          |
