# Rolling Circles: a picture of the Chinese Remainder Theorem

An interactive page that shows the Chinese Remainder Theorem as wheels rolling along a number line. Each modulus gets its own wheel, and each wheel's
circumference equals its modulus. The answer to the system of congruences is the spot where every wheel touches the ground at the number you asked for.

I drew the idea in spring 2016, as an undergraduate trying to see why the theorem works. The connection between rotation and modular arithmetic turned out to go
back to Gauss, so this is a rediscovery of a classical idea in my own form.

## The idea in one picture

```text
number line:  0   1   2   3   4   5   6   7  [8]
mod 2 wheel:  0   1   0   1   0   1   0   1  [0]   4 full turns
mod 3 wheel:  0   1   2   0   1   2   0   1  [2]   2 2/3 turns
mod 5 wheel:  0   1   2   3   4   0   1   2  [3]   1 3/5 turns
                                              ^ all three line up: x = 8
```

The two formulas from my notes:

| Formula      | Meaning                                                                                       |
|--------------|-----------------------------------------------------------------------------------------------|
| `r = n / 2π` | A wheel for "mod n" has circumference n, so one full turn covers one full cycle of remainders |
| `x = n · R`  | A wheel that has turned R times has rolled R circumferences, so it sits at x                  |

## What the page does

- Rolls the wheels with a play button, a slider, and single steps, and stops where they all line up
- Lets you change the puzzle: two to four congruences, moduli from 2 to 13, checked for pairwise relatively prime moduli
- Shows how many times each wheel has turned, as a mixed fraction
- Works through the standard algebraic construction (`m`, `Mᵢ`, `yᵢ`, `x = Σ aᵢ·Mᵢ·yᵢ mod m`) for the same puzzle
- Shows each wheel as a phase on a circle cut into n equal slices
- Includes a scan of my original 2016 notes

## Run it

Open `index.html` in any browser. It is one self-contained file with no libraries and no build step. Add `?x=8` to the address to start at a position, or
`?theme=dark` to force the dark theme.

## Files

| Path                             | What it is                   |
|----------------------------------|------------------------------|
| `index.html`                     | The interactive page         |
| `assets/original-notes-2016.jpg` | My original hand-drawn notes |
