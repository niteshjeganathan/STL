# STL
- [ ] Containers
- [x] Array
- [x] Vectors
- [ ] Lists
- [ ] Forward List
- [x] Queue
- [x] Deque
- [ ] Priority Queue
- [x] Stack
- [ ] Set
- [ ] Multimap
- [x] Map
- [ ] Multiset
- [ ] Unordered Map
- [ ] Unordered Set
- [ ] Unordered Multiset
- [ ] Unordered Multimap
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

