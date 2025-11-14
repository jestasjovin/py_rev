# **Python DS & Collections – Big-O Cheatsheet**

---

## **1. Lists / Arrays**

* `arr[i]` → Access O(1) | Space O(n)
* `arr.append(x)` → Add end O(1) amortized
* `arr.insert(i,x)` → Add at index O(n)
* `arr.pop()` → Remove last O(1)
* `arr.pop(i)` → Remove at index O(n)
* `x in arr` → Search O(n)
* `arr.sort()` → O(n log n)
* `arr.reverse()` → O(n)

---

## **2. Strings**

* `s[i]` → Access O(1)
* `s + t` → Concatenation O(n+m)
* `s * k` → Repeat O(n*k)
* `s.lower() / s.upper()` → O(n)
* `s.strip()` → O(n)
* `s.replace(a,b)` → O(n)
* `''.join(list)` → O(n)
* `s.split(sep)` → O(n)
* `x in s` → O(n)

**Helpers:**

* Palindrome check → `s == s[::-1]` → O(n)
* Case conversion → `s.lower()` / `s.upper()` → O(n)
* Sliding window sum/max → O(n)

---

## **3. Sets**

* `s.add(x)` → O(1) avg
* `s.remove(x)` → O(1) avg
* `x in s` → O(1) avg
* Iteration → O(n)
* `s1 & s2` / `s1 | s2` → O(len(s1)+len(s2))

---

## **4. Tuples**

* Access → O(1)
* Iterate → O(n)
* Convert to list → O(n)

---

## **5. Dictionaries / HashMaps**

* `d[key]` → Access O(1) avg
* `d[key] = val` → Insert/update O(1) avg
* `del d[key]` → Delete O(1) avg
* Iteration → O(n)

---

## **6. Deque / Queue**

* `append / appendleft` → O(1)
* `pop / popleft` → O(1)
* Indexing → O(n)
* Iteration → O(n)

---

## **7. Stack (List)**

* `stack.append(x)` → Push O(1) amortized
* `stack.pop()` → Pop O(1)
* `stack[-1]` → Peek O(1)

---

## **8. LinkedList**

* Append → O(n) (O(1) with tail)
* Prepend → O(1)
* Search → O(n)
* Delete → O(n)

---

## **9. Trees (Binary / BST)**

* Access/Insert/Delete → O(log n) avg, O(n) worst
* Traversals (in/pre/post) → O(n)

---

## **10. Graphs**

* **Adjacency List:** Space O(V+E), Iterate neighbors O(k)
* **Adjacency Matrix:** Space O(V²), Iterate neighbors O(V)
* BFS / DFS → O(V+E)

---

## **11. Heap / PriorityQueue**

* `heapify(list)` → O(n)
* `heappush(heap, x)` → O(log n)
* `heappop(heap)` → O(log n)
* Peek min → O(1)

---

## **12. Counter / Frequency Map**

* Count all elements → O(n)
* Access count → O(1)

---

## **13. Misc / Helpers**

* 2D array `[i][j]` → Access O(1)
* `enumerate(list)` → O(n)
* String → list → `list(s)` → O(n)
* List → string → `''.join(list)` → O(n)

---

**Tips for FAANG prep:**

* Always mention **time & space** in interviews.
* Know **alternate ways** (e.g., list vs deque vs linked list).
* Memorize **common method complexities** (`append`, `pop`, `insert`, `sort`, `in`).













---
---
---
---

## **1. Numbers**

* `int`, `float`, `complex` → basic arithmetic, type conversion.
* `abs(x)` → absolute value.
* `pow(x,y)` → x^y.
* **O(1)** time & space.

---

## **2. Strings**

* Immutable.
* Indexing: `s[0]`, `s[-1]` → O(1)
* Slicing: `s[::2]` → O(n)
* Concatenation: `s1 + s2` → O(n+m)
* Repetition: `s*2` → O(n*k)
* Useful methods:

  * `.lower()` / `.upper()` → O(n)
  * `.strip()` → O(n)
  * `.replace(a,b)` → O(n)
  * `.split(sep)` → O(n)
  * `"-".join(list)` → O(n)
  * `.startswith() / .endswith()` → O(k)
  * `.count(sub)` → O(n)
  * `.isdigit() / .isalpha()` → O(n)
  * f-strings / `.format()` → O(n)

---

## **3. Lists / Arrays**

* Dynamic array.
* Indexing: O(1)
* Append: `list.append(x)` → O(1) amortized
* Insert: `list.insert(i,x)` → O(n)
* Remove by value: `list.remove(x)` → O(n)
* Pop: `list.pop()` → O(1), `pop(i)` → O(n)
* Slice copy: `list[1:3]` → O(k)
* Sorting: `list.sort()` → O(n log n)
* Reverse: `list.reverse()` → O(n)

---

## **4. Tuples**

* Immutable list.
* Indexing: O(1)
* Convert: `list(t)` → O(n), `tuple(list)` → O(n)

---

## **5. Sets**

* Unordered, unique.
* Add / remove / discard → O(1) avg
* Membership `x in s` → O(1) avg
* Union `a|b`, Intersection `a&b`, Difference `a-b` → O(min(len(a),len(b)))

---

## **6. Dictionaries / HashMaps**

* Key-value mapping.
* Access / update / insert → O(1) avg
* Delete: `del d[k]`, `d.pop(k)` → O(1) avg
* Methods: `.keys()`, `.values()`, `.items()`, `.get(k)`, `.setdefault(k, default)` → O(1) avg

---

## **7. Deque / Queue**

```python
from collections import deque
q = deque()
q.append(x)      # enqueue O(1)
q.appendleft(x)  # O(1)
q.pop()          # O(1)
q.popleft()      # O(1)
```

---

## **8. Stack**

* LIFO via list: `stack.append(x)` → push O(1), `stack.pop()` → O(1)

---

## **9. LinkedList**

* Node-based structure.
* Append: O(n)
* Prepend: O(1)
* Delete by value: O(n)

---

## **10. Trees**

* Binary Tree Node: left, right
* Traversals:

  * Inorder / Preorder / Postorder → O(n) time, O(h) space (recursion)

---

## **11. Graphs**

* Representation:

  * Adjacency List: `dict[node] = [neighbors]` → O(V+E) traversal
  * Adjacency Matrix: `matrix[n][n]` → O(V^2) space
* BFS / DFS → O(V+E) time, O(V) space

---

## **12. Heap / PriorityQueue**

```python
import heapq
heap = [3,1,2]
heapq.heapify(heap)     # O(n)
heapq.heappush(heap,0)  # O(log n)
heapq.heappop(heap)     # O(log n)
```

---

## **13. Counter / defaultdict**

```python
from collections import Counter, defaultdict
c = Counter([1,2,2,3])    # O(n)
dd = defaultdict(list)
dd['a'].append(1)          # O(1)
```

---

## **14. 2D Lists / Matrices**

* Access: `matrix[i][j]` → O(1)
* Iteration: nested loops → O(rows*cols)

---

## **15. Composite Structures**

* List of lists → O(1) access per element
* HashMap of lists → O(1) access by key, O(k) iterate inner list
* Array of hashsets → O(1) add/remove, O(1) membership
* Tree/graph as hashmap of arrays → O(V+E) traverse

---

## **16. Advanced Helpers**

* `enumerate(iterable)` → index + value, O(n)
* `zip(a,b)` → O(n)
* `map(func, iterable)` → O(n)
* `filter(func, iterable)` → O(n)
* `all(iterable)` / `any(iterable)` → O(n)
* `min(iterable, key=func)` / `max(...)` → O(n)
* `reversed(iterable)` → O(n)
* `deepcopy()` vs `copy()` → O(n)

---

**✅ Summary Big-O Table (Common Ops)**

| DS / Method      | Access   | Insert   | Delete   | Search | Notes                 |
| ---------------- | -------- | -------- | -------- | ------ | --------------------- |
| List             | O(1)     | O(n)     | O(n)     | O(n)   | append O(1) amortized |
| Tuple            | O(1)     | –        | –        | O(n)   | immutable             |
| Set              | O(1)     | O(1)     | O(1)     | O(1)   | avg case              |
| Dict             | O(1)     | O(1)     | O(1)     | O(1)   | avg case              |
| Stack / Queue    | O(1)     | O(1)     | O(1)     | –      | deque recommended     |
| LinkedList       | O(n)     | O(1)     | O(n)     | O(n)   | depends on head/tail  |
| Tree (BT/BTI)    | O(log n) | O(log n) | O(log n) | O(n)   | binary, balanced      |
| Graph (adj list) | O(V+E)   | O(1)     | O(1)     | O(V+E) | traversal cost        |
| Heap             | O(n)     | O(log n) | O(log n) | O(n)   | min/max heap          |




---
---
---

# **Python Data Structures & Methods – Master Cheatsheet**

## **1️⃣ Numbers**

* `int, float, complex`
* `abs(x), pow(x,y)`
* **O(1) time & space**

---

## **2️⃣ Strings** (Immutable)

* Index: `s[i]` O(1)
* Slice: `s[start:stop:step]` O(k)
* Concat: `s1+s2` O(n+m)
* Repeat: `s*k` O(n*k)
* Methods:

  * `.lower()/.upper()`, `.strip()`, `.replace()`, `.split()`, `"-".join(list)` → O(n)
  * `.startswith()/endswith()`, `.count(sub)`, `.isdigit()/isalpha()` → O(n)

**Helpers:** palindrome check, sliding window, case conversion

---

## **3️⃣ List / Array**

* Dynamic array
* Index: O(1), Append: O(1) amortized, Insert/Remove: O(n), Pop(end): O(1)
* Slice copy: O(k), Sort: O(n log n), Reverse: O(n)
* 2D list: `matrix[i][j]` → O(1), nested loops → O(rows*cols)

---

## **4️⃣ Tuple** (Immutable)

* Index: O(1), convert: `list(t)` / `tuple(list)` O(n)

---

## **5️⃣ Set**

* Unordered, unique
* Add/Remove/Check: O(1) avg
* Union/Intersect/Diff: O(min(len(a),len(b)))

---

## **6️⃣ Dict / HashMap**

* Access/Insert/Delete: O(1) avg
* Iter: `.keys()/.values()/.items()` → O(n)

---

## **7️⃣ Deque / Queue**

```python
from collections import deque
q.append(x)/appendleft(x)/pop()/popleft() → O(1)
```

---

## **8️⃣ Stack**

* List: `.append()` / `.pop()` → O(1)
* LIFO

---

## **9️⃣ LinkedList**

* Append: O(n), Prepend: O(1), Delete by value: O(n)
* Node-based: `val + next`

---

## **🔟 Trees**

* Node: `val, left, right`
* Traversals: Inorder / Preorder / Postorder → O(n) time, O(h) space

---

## **1️⃣1️⃣ Graphs**

* Adjacency List: `dict[node] = [neighbors]` → O(V+E) traversal
* Adjacency Matrix: `matrix[n][n]` → O(V^2) space
* BFS / DFS → O(V+E) time, O(V) space

---

## **1️⃣2️⃣ Heap / PriorityQueue**

```python
import heapq
heapq.heapify(list) → O(n)
heappush / heappop → O(log n)
```

---

## **1️⃣3️⃣ Counter / defaultdict**

```python
from collections import Counter, defaultdict
Counter(list) → freq count O(n)
defaultdict(list) → O(1) per insertion
```

---

## **1️⃣4️⃣ Advanced Helpers**

* `enumerate(iterable)` → index + value O(n)
* `zip(a,b)`, `map(func,iterable)`, `filter(func,iterable)` → O(n)
* `all()/any()`, `min()/max(key=func)`, `reversed()` → O(n)
* `deepcopy()` vs `copy()` → O(n)

---

## **1️⃣5️⃣ Composite Structures**

* List of lists, dict of lists, array of sets → O(1) access, O(k) iterate
* Tree/graph as hashmap of arrays → O(V+E) traverse

---

## **📊 Big-O Quick Summary**

| DS / Method      | Access   | Insert   | Delete   | Search | Notes                 |
| ---------------- | -------- | -------- | -------- | ------ | --------------------- |
| List             | O(1)     | O(n)     | O(n)     | O(n)   | append O(1) amortized |
| Tuple            | O(1)     | –        | –        | O(n)   | immutable             |
| Set              | O(1)     | O(1)     | O(1)     | O(1)   | avg case              |
| Dict             | O(1)     | O(1)     | O(1)     | O(1)   | avg case              |
| Stack / Queue    | O(1)     | O(1)     | O(1)     | –      | deque recommended     |
| LinkedList       | O(n)     | O(1)     | O(n)     | O(n)   | depends on head/tail  |
| Tree (BT/BTI)    | O(log n) | O(log n) | O(log n) | O(n)   | binary, balanced      |
| Graph (adj list) | O(V+E)   | O(1)     | O(1)     | O(V+E) | traversal cost        |
| Heap             | O(n)     | O(log n) | O(log n) | O(n)   | min/max heap          |

