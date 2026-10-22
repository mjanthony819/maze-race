# maze race

Generate a random maze, then watch **breadth-first search** and **depth-first search** race to the exit — live on a canvas.

**Live demo:** https://mjanthony819.github.io/maze-race/

## what it does

- generates a perfect maze (exactly one path between any two cells) with an iterative recursive-backtracker
- animates BFS and DFS cell-by-cell — solo or head-to-head in **race** mode
- shows cells visited, final path length, and declares a winner
- size and speed controls, keyboard shortcuts (`space` = race, `r` = new maze), light/dark theme

## why BFS always finds the shortest path

The maze is an unweighted graph, so BFS explores in order of distance from the start — the first time it reaches the exit, that path is optimal. DFS dives deep on one branch and usually visits fewer cells in a deep corridor, but its path can wander. The race makes the trade-off visible.

## stack

Single `index.html` — vanilla JS + canvas, no build step, no libraries. Hosted on GitHub Pages.

## run locally

Open `index.html` in a browser, or:

```bash
python3 -m http.server 8000
```

---

Built with AI assistance (design and direction by [@mjanthony819](https://github.com/mjanthony819)).
