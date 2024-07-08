# STL
* Containers
* Array
* Vectors
* Lists
* Forward List
* Queue
* Deque
* Priority Queue
* Stack
* Set
* Multimap
* Multiset
* Unordered Map
* Unordered Set
* Unordered Multiset
* Unordered Multimap
* Iterators
* Algorithms
* Functor

## Stack STL
### Functions: 
* push() - adds element to the stack - O(1)
* pop() - Removes an element from the stack - O(1)
* top() - Returns the element at the top - O(1)
* size() - Returns the number of elements in the stack - O(1)
* empty() - Returns true if the stack is empty - O(1)

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

