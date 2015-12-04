# Data Structures

## Intro

## Linked Lists
### Singularly Linked Lists
#### Invariants 
1. An DList's size variable is always correct.
2. There is always a tail node whose next reference is null.

#### Code Example (Java)
```Java
public class ListNode {
  public int item;
  public ListNode next;
} 
public ListNode(int i, ListNode n) {
  item = i;
  next = n;
}
public ListNode(int i) {
  this(i, null);
}
```

```Java
public class SList {
  private SListNode head;             // First node in list.
  private int size;                   // Number of items in list.

  public SList() {                    // Here's how to represent an empty list.
    head = null;
    size = 0;
  }

  public void insertFront(Object item) {
    head = new SListNode(item, head);
    size++;
  }
}
    
```
#### Invariants 
#### Code Example (Java)
#### Visual Example
#### Run Times
- Insertion: O(1) 
- Deletion: O(1)
- Indexing: O(n)
- Searching: O(n)



### Doubly Linked Lists
#### Invariants 
1. An DList's size variable is always correct.
2. There is always a tail node whose next reference is null.
3. _item.next_ and _item.previous_ either points to an item or null (if tail or head).

#### Code Example (Java)
``` Java
public class ListNode {
  public int item;
  public ListNode next;
} 
public ListNode(int i, ListNode n) {
  item = i;
  next = n;
}
public ListNode(int i) {
  this(i, null);
}
```

``` Java
public class SList {
  private DListNode head;             // First node in list.
  private int size;                   // Number of items in list.

  public DList() {                    // Here's how to represent an empty list.
    head = null;
    tail = null;
    size = 0;
  }

  public void insertFront(Object item) {
    head = new SListNode(item, head);
    size++;
  }

  public void insertBack(Object item) {
    tail = new SListNode(item, head);
    size++;
  }
}
```

#### Visual Example

#### Run Times
- Insertion: O(1) 
- Deletion: O(1)
- Indexing: O(n)
- Searching: O(n)


### Hash Tables
#### Invariants 
1. n is the number of keys (words).
2. N buckets exists in a table.
3. n ≤ N << possible keys.
4. Load Factor is  n/N < 1 (Around 0.75 is ideal).

#### Code Example (Java)
#### Algorithm
Compression Function: 
  - h(hashCode) = hashCode mod N.
  - Better: h(hashCode) = ((a * (hashCode) + b) mod p) mod N
  - p is prime >> N, a & b are arbitrary positive ints.
  - Really Large Prime: 16908799
  - If hashCode % N is negative, add N.

#### Methods
| insert(key, value)      | find(key)               | remove(key)             |
|:-----------------------:|:-----------------------:|:-----------------------:|
|Compute the key's hash code and compress it to determine the entry's bucket.|Hash the key to determine its bucket.|Hash the key to determine its bucket.|
|Insert the entry (key and value together) into that bucket's list.|Search the list for an entry with the given key.|Search the list for an entry with the given key.|
||If found, return the entry; else, return null.|Remove it from the list if found.||
|||Return the entry or null.|



### Stacks
#### Invariants 
#### Code Example (Java)
#### Visual Example
#### Run Times

### Queues
#### Invariants 
#### Code Example (Java)
#### Visual Example
#### Run Times

## Trees
### Binary Trees
#### Invariants 
#### Code Example (Java)
#### Visual Example
#### Run Times

### 2-3-4 Trees
#### Invariants 
#### Code Example (Java)
#### Visual Example
#### Run Times

### Red Black Trees
#### Invariants 
#### Code Example (Java)
#### Visual Example
#### Run Times

### Splay Trees
#### Invariants 
#### Code Example (Java)
#### Visual Example
#### Run Times

### Traversals
#### Invariants 
#### Code Example (Java)
#### Visual Example
#### Run Times


## Heaps

## Graphs
### Undirected Graphs
#### Invariants 
#### Code Example (Java)
#### Visual Example
#### Run Times

### Directed Graphs
#### Invariants 
#### Code Example (Java)
#### Visual Example
#### Run Times

### Breadth First Search
### Depth First Search


## Disjoint Sets

## Resources
## Colophon
