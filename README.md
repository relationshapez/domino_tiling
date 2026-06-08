# Relationshapez: Domino Tiling

This is a single-file HTML activity for exploring the number of ways dominoes can tile a `2 × N` grid.

The activity is designed for small screens. The interface only asks for `N`, then displays the total number of tilings and a scrollable gallery showing each tiling.

## Remote Access

https://relationshapez.github.io/domino_tiling/

## Files

- `index.html` — the complete interactive activity
- `README.md` — this documentation file

## How to Use

1. Open `index.html` in a web browser.
2. Enter a positive integer value for `N`.
3. Read the total number of domino tilings at the top of the screen.
4. Scroll through the displayed tilings.

The first version limits `N` to at most `14` so that the full gallery remains practical on mobile devices. For `2 × N` boards, the number of tilings grows according to the Fibonacci pattern:

```text
T(1) = 1
T(2) = 2
T(N) = T(N - 1) + T(N - 2)
```

This happens because the left end of a `2 × N` board is tiled in one of two ways:

- one vertical domino, leaving a `2 × (N - 1)` board;
- two horizontal dominoes stacked on top of each other, leaving a `2 × (N - 2)` board.

## Design Notes

The page uses the GW blue and buff color scheme:

- GW Blue: `#033C5A`
- GW Buff: `#D6BF91`

The HTML file has no external dependencies and can be run locally or hosted as a static webpage.

## License

Copyright (c) 2026 Alan Miller.

This project is released under the **MIT License**.

See the [`LICENSE`](LICENSE) file for the full license text.
