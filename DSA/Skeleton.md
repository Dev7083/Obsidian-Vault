 **Java fast templates for DSA** :

---

# 🚀 1. FAST INPUT + MAIN TEMPLATE

```java
import java.util.*;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();
        int[] arr = new int[n];

        for(int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }

        // Call your function
        System.out.println(solve(arr, n));
    }

    static int solve(int[] arr, int n) {
        // logic here
        return 0;
    }
}
```

👉 Use this as base for almost all problems

---

# ⚡ 2. ARRAY + HASHMAP TEMPLATE

```java
// Frequency map
Map<Integer, Integer> map = new HashMap<>();

for(int num : arr) {
    map.put(num, map.getOrDefault(num, 0) + 1);
}
```

👉 Used in:

* Two Sum
* Frequency count
* Subarray problems

---

# 🔁 3. TWO POINTER TEMPLATE

```java
int left = 0, right = arr.length - 1;

while(left < right) {
    if(arr[left] + arr[right] == target) {
        // found
        left++;
        right--;
    } else if(arr[left] + arr[right] < target) {
        left++;
    } else {
        right--;
    }
}
```

---

# 🪟 4. SLIDING WINDOW TEMPLATE

```java
int left = 0, sum = 0;

for(int right = 0; right < arr.length; right++) {
    sum += arr[right];

    while(sum > k) {
        sum -= arr[left];
        left++;
    }

    // update answer here
}
```

---

# 🔄 5. BINARY SEARCH TEMPLATE

```java
int left = 0, right = arr.length - 1;

while(left <= right) {
    int mid = left + (right - left) / 2;

    if(arr[mid] == target) return mid;
    else if(arr[mid] < target) left = mid + 1;
    else right = mid - 1;
}
return -1;
```

---

# 🌳 6. TREE TEMPLATE

```java
class TreeNode {
    int val;
    TreeNode left, right;

    TreeNode(int val) {
        this.val = val;
    }
}
```

### DFS (Recursive)

```java
void dfs(TreeNode root) {
    if(root == null) return;

    dfs(root.left);
    dfs(root.right);
}
```

### BFS (Level Order)

```java
Queue<TreeNode> q = new LinkedList<>();
q.add(root);

while(!q.isEmpty()) {
    TreeNode node = q.poll();

    if(node.left != null) q.add(node.left);
    if(node.right != null) q.add(node.right);
}
```

---

# 🔗 7. LINKED LIST TEMPLATE

```java
class ListNode {
    int val;
    ListNode next;

    ListNode(int val) {
        this.val = val;
    }
}
```

### Reverse Linked List

```java
ListNode prev = null, curr = head;

while(curr != null) {
    ListNode next = curr.next;
    curr.next = prev;
    prev = curr;
    curr = next;
}
return prev;
```

---

# 🌐 8. GRAPH TEMPLATE (BFS + DFS)

### Adjacency List

```java
List<List<Integer>> graph = new ArrayList<>();

for(int i = 0; i < n; i++) {
    graph.add(new ArrayList<>());
}
```

### BFS

```java
Queue<Integer> q = new LinkedList<>();
boolean[] visited = new boolean[n];

q.add(0);
visited[0] = true;

while(!q.isEmpty()) {
    int node = q.poll();

    for(int nei : graph.get(node)) {
        if(!visited[nei]) {
            visited[nei] = true;
            q.add(nei);
        }
    }
}
```

### DFS

```java
void dfs(int node, boolean[] visited, List<List<Integer>> graph) {
    visited[node] = true;

    for(int nei : graph.get(node)) {
        if(!visited[nei]) {
            dfs(nei, visited, graph);
        }
    }
}
```

---

# 🔥 9. HEAP (PRIORITY QUEUE)

```java
PriorityQueue<Integer> minHeap = new PriorityQueue<>();
PriorityQueue<Integer> maxHeap = new PriorityQueue<>(Collections.reverseOrder());

minHeap.add(10);
minHeap.poll();
```

---

# 🧠 10. DP TEMPLATE (MEMOIZATION)

```java
int[] dp = new int[n];
Arrays.fill(dp, -1);

int solve(int n) {
    if(n <= 1) return n;

    if(dp[n] != -1) return dp[n];

    return dp[n] = solve(n-1) + solve(n-2);
}
```

---

# ⚡ BONUS: FAST TYPING TRICKS

### 🔹 Use short variable names

```java
int l = 0, r = n - 1;
```

### 🔹 Use enhanced loops

```java
for(int x : arr)
```

### 🔹 Use built-in methods

```java
Arrays.sort(arr);
Collections.sort(list);
```

---
