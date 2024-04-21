---
id: kvhrmep1fakpx0f8myafnlm
title: Map
desc: ''
updated: 1713649125547
created: 1713641905407
---

- To represent group of objects as key value pairs
- NOT a child interface of [[lang.java.lib.collection.interface]]
- Therefore, strictly speaking, [[lang.java.lib.collection.interface]] is NOT root interface of Collection framework
- Duplicates
  - Keys - [[lang.java.lib.collection.tags.duplicates.not allowed]]
  - Values - [[lang.java.lib.collection.tags.duplicates.allowed]]

## [[lang.java.lib.collection.map.hash]] vs [[lang.java.lib.collection.map.hashtable]]

|               | HashMap                                                        | Hashtable                                                 |
|---------------|----------------------------------------------------------------|-----------------------------------------------------------|
| Introduced in | 1.2                                                            | 1.0                                                       |
| Thread Safety | Not thread safe (not synchronized) => works with single thread | Thread safe (synchronized) => works with multiple threads |
| Speed         | Faster                                                         | Slower                                                    |
| Null key      | One null key allowed                                           | Null key not allowed                                      |


Child classes/interfaces:

- [[lang.java.lib.collection.map.hash]]
- [[lang.java.lib.collection.map.weakhash]]
- [[lang.java.lib.collection.map.identityhash]]
- [[lang.java.lib.collection.map.sorted]] (I)
- [[lang.java.lib.collection.map.hashtable]]
