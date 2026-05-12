# LRU Cache Visualizer

**An interactive LRU cache visualization project.**

Live demo: https://23wh1a05e7.github.io/LRUCacheVisualizer/

---

## Overview

This repository contains an implementation of an LRU (Least Recently Used) cache. The cache stores a limited number of key-value pairs and evicts the least recently used item when capacity is exceeded.

## Features

- O(1) `get` and `put` operations
- Fixed capacity
- Automatic eviction of least recently used entries
- Reusable cache interface

## How it Works

The implementation uses:
- a hash map for fast key lookup
- a doubly linked list to track usage order

When a key is accessed or inserted, it moves to the head of the list as the most recently used entry. When the cache reaches its capacity, the tail entry is removed.

## API

### `LRUCache(capacity)`
Creates a new cache with the specified capacity.

### `get(key)`
- Returns the value associated with `key` if it exists
- Moves the item to the most recently used position
- Returns `-1` if the key is not found

### `put(key, value)`
- Inserts or updates a key-value pair
- Moves the key to the most recently used position
- Evicts the least recently used item if capacity is exceeded

## Example

```javascript
const cache = new LRUCache(3);

cache.put('a', 1);
cache.put('b', 2);
cache.put('c', 3);
console.log(cache.get('a')); // 1

cache.put('d', 4); // evicts 'b'
console.log(cache.get('b')); // -1
console.log(cache.get('c')); // 3
```

## Complexity

- `get`: O(1)
- `put`: O(1)

## Installation

1. Clone the repository.
2. Add the cache implementation to your project.
3. Use the `LRUCache` class in your application or tests.

## Testing

Recommended tests:
- retrieving existing keys
- missing keys return `-1`
- eviction when capacity is reached
- updating an existing key
- edge cases such as zero capacity

## Notes

- This cache is useful for performance-sensitive workloads.
- It is commonly used in applications that need to cache recent results while limiting memory usage.

---

**Last Updated**: May 2026
