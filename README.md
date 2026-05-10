# LRU Cache Visualizer

**An interactive LRU cache visualization project.**

Live demo: https://23wh1a05e7.github.io/SortingAlgorithmVisualizer/

---

## Project Overview

This project demonstrates the Least Recently Used (LRU) cache eviction policy through a browser-based visualizer. It helps learners see how `get` and `put` operations affect cache contents and eviction order.

## Features

- Set cache capacity
- `get(key)` to access stored values
- `put(key, value)` to add or update cache entries
- Visual indicator for hits and misses
- Eviction of the least recently used item when capacity is exceeded
- Live animation of cache order and internal state

## Installation

### Prerequisites
- Node.js
- npm

### Setup

```bash
git clone https://github.com/23wh1a05e7/SortingAlgorithmVisualizer.git
cd SortingAlgorithmVisualizer
npm install
npm start
```

Open `http://localhost:3000` in your browser.

## Build

```bash
npm run build
```

## Deployment (GitHub Pages)

Add the following to `package.json`:

```json
"homepage": "https://23wh1a05e7.github.io/SortingAlgorithmVisualizer",
"scripts": {
  "predeploy": "npm run build",
  "deploy": "gh-pages -d build"
}
```

Then run:

```bash
npm install --save-dev gh-pages
npm run deploy
```

## How LRU Works

- `get(key)`: Returns the value if the key exists, and marks that key as most recently used.
- `put(key, value)`: Adds or updates the key, marks it as most recently used, and evicts the least recently used key if needed.

## Notes

- Use the cache form to simulate operations.
- The visualizer is designed for learning and algorithm explanation.
- Extend it by adding other cache policies such as FIFO, LFU, or MRU.
