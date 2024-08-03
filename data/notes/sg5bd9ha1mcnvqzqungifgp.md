

- Child interface of [[lang.java.lib.collection.iterators.iterator]]
- Most powerful cursor
- Bidirectional
- Has methods to replace and add new objects.

## Methods

Forward

- `public boolean hasNext()`
- `public Object next()`
- `public int nextIndex()`

Extra capabilities

- `public void remove()`
- `public void set(Object new)` → replace
- `public void add(Object new)`

Backward

- `public boolean hasPrevious()`
- `public Object previous()`
- `public int previousIndex()`

The `set()` method of `ListIterator` interface is used to replace the last element which is returned by the `next()` or `previous()` along with the given element. The call can be added only if neither `remove()` nor `add(E)` method have been called.
