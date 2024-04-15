# Реализация стандартных контейнеров C++;

# Оглавление

1. [List Structure](#List)
2. [Stack Structure](#Stack)
3. [Queue Structure](#Queue)
4. [AVL Tree](#AVLTree)
5. [Map Structure](#Map)
6. [Set Structure](#Set)
7. [Array Structure](#Array)
8. [Multiset Structure](#Multiset)

В папке `containers` представлены реализации `list.h`, `stack.h`, `queue.h`, `vector.h`, `set.h`, `map.h`.

### List:
```CPP
struct Node {
    value_type value_;
    Node *prev_;
    Node *next_;

    Node(const value_type &value)
        : value_(value), prev_(nullptr), next_(nullptr) {}
  };

  Node *head_;
  Node *tail_;
  Node *end_;
  size_type size_;
```

### Stack:
```CPP
struct Node {
    T data;
    Node* next;
    Node(const T& value);
  };
  Node* top_;
```

### Queue:
```CPP
struct Node {
    T data;
    Node *next;
    Node(const T &value);
  };
  Node *front_;
  Node *rear_;
```
`Vector Structure`
```CPP
  T* data;
  size_t capacity;
  size_t size;
```

> Реализация классов Map и Set построена на базе класса, реализующего красно-черное дерево.

### AVLTree:
```CPP
struct AVLNode {
    Key key;
    Value value;
    AVLNode* left;
    AVLNode* right;
    AVLNode* parent;
    int height;
    AVLNode(const Key& k, const Value& v, AVLNode* p)
        : key(k),
          value(v),
          left(nullptr),
          right(nullptr),
          parent(p),
          height(1) {}
  }
```

### Map:
```CPP
AVLTree<Key, Value> tree;
```

### Set:
```CPP
AVLTree<Value> tree;
```

В папке `containers_plus` представлены реализации `array.h`, `multiset.h`.
### Array
```CPP
T data[N]
```

### Multiset
```CPP
multiset<T> data
```
