# STL
- [ ] Containers
- [x] Array
- [x] Vectors
- [x] Lists
- [x] Forward List
- [x] Queue
- [x] Deque
- [x] Priority Queue
- [x] Stack
- [x] Set
- [x] Multimap
- [x] Map
- [x] Multiset
- [x] Unordered Map
- [x] Unordered Set
- [x] Unordered Multiset
- [x] Unordered Multimap
- [ ] Iterators
- [ ] Algorithms
- [ ] Functor

## Array
### Functions: 
* at(i) / \[i]
* front()
* back()
* size()
* fill(element)
* empty()
* swap(array_name)
* data() - first element

## Vector
### Iterators
* begin()
* end()
* rbegin()
* rend()
### Capacity
* size()
* empty()
### Element Access
* at()
* front()
* back()
### Modifiers
* push_back()
* pop_back()
* insert(iterator, value)
* erase(iterator)
* clear()

## Stack 
### Functions: 
* push() - adds element to the stack - O(1)
* pop() - Removes an element from the stack - O(1)
* top() - Returns the element at the top - O(1)
* size() - Returns the number of elements in the stack - O(1)
* empty() - Returns true if the stack is empty - O(1)

## Queue
### Functions
* empty()
* size()
* front()
* back()
* push()
* pop()

## Deque
### Functions
* insert(iterator, value)
* push_front()
* push_back()
* pop_front()
* pop_back()
* clear()
* erase()
* begin()
* end()

## Priority Queue
### Comparator
```c++
#include <iostream>
#include <queue>
#include <vector>
using namespace std;

struct CustomComparator
{
    bool operator()(const pair<int, int> &p1, const pair<int, int> &p2)
    {
        return p1.second < p2.second;
    }
};

int main()
{
    priority_queue<pair<int, int>, vector<pair<int, int>>, CustomComparator> pq;

    pq.push({1, 10});
    pq.push({2, 5});
    pq.push({3, 20});
    pq.push({4, 15});

    cout << "Custom Comparator Priority Queue: ";
    while (!pq.empty())
    {
        pair<int, int> p = pq.top();
        cout << "(" << p.first << ", " << p.second << ") ";
        pq.pop();
    }

    return 0;
}
```

### Functions
* priority_queue<int, vector<int>, greater<int>> pq;
* empty()
* size()
* top()
* push()
* pop()

## List
### Functions
* front()
* back()
* push_front()
* push_back()
* pop_front()
* push_front()
* begin()
* end()
* empty()
* insert(iterator, value)
* assign(value, repititions)
* reverse()
* erase()
* sort()
* unique() - removes consecutive repeating values
* merge()
* clear()

## Forward List
* assign()
* push_front()
* pop_front()
* insert_after()
* erase_after()
* remove()
* clear()
* front()
* begin()
* end()
* unique()
* reverse()
* merge()
* sort()





## Map
### Creating a Map
```c++
#include <map>
map<key_type, value_type> map_name {{key1, value1}, {key2, value2}};
```

### Inserting Values
```c++
map['nitesh'] = 'jeganathan';
map.insert(make_pair('nitesh', 'jeganathan'));
```

### Map Methods
* clear() - Removes every element
* erase() - Either use key or iterator, or range using iterator
* find() - Find key, returns iterator if found else returns map.end()
* size()
* empty()
* count() - Gives count of key repititions

### Set
* Set
  * Stores values in sorted order
  * Stores only unique values
  * Elements can only be inserted or deleted, can't be modified
  * Can erase a range of iterators
  * Traversal using iterators
  * Sets are implemented as binary search trees
* Multiset
  * Stores values in sorted order
  * Allows storage of duplicate elements
  * Can erase a range of iterators
* Unordered Set
  * No sorted order
  * Stores only unique values
  * Implemented as hash tables
  * Can erase only the iterator, not a range
* Unordered Multiset
  * No sorted order
  * Stores duplicate values as well
  * Implemented as hash tables
  * Can erase only the iterator, not a range

Functions
* set<int, greater<int>> for decreasing values
* begin()
* end()
* size()
* empty()
* insert()
* erase()
* clear()
* find()
* count()

### Map 
* Map
  * Increasing order of keys
  * Self balancing BST
  * Log n insertion, searching, deletion + rebalancing if required
* Unordered Map
  * No ordering
  * Hash Table
  * O(n) insertion, searching, deletion + rebalancing if required
* Multimap
  * Increasing order of keys
  * Self Balancing BST
  * Allows duplicate keys to be inserted
* Unordered Multimap
  * No ordering
  * Hash Table
  * Allows duplicate keys to be inserted

### Iterators
Functions
* begin()
* end()
* advance() - advances the pointer itself
* next() - returns the advanced pointer
* prev() - returns the reduced pointer

Types
* Input Iterators
* Output Iterators
* Forward Iterator
* BiDirectional Iterator
* Random-Access Iterator

![image](https://github.com/user-attachments/assets/922aca83-a9b0-4e9f-8858-35ecfcba5769)

#### Input Iterator
* Single Pass Algorithms
* Equality/Inequality Operations
* Deferencing
* Incrementable
* Swappable
* Only can access, can't assign
* Can't be decremented
* No relational operators
* No arithmetic operators

#### Output Iterators
* Single Pass Algorithms
* Cant check for Equality/Inequality
* Deferencing
* Incrementable
* Swappable
* Only assigning, can't access
* Can't be decremented
* No relational operators
* No arithmetic operators
