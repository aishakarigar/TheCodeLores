---
layout: page
title: Comic 003 – The Off-by-One Apocalypse
---

![Comic 03 – The Off-by-One Apocalypse](./comic.png)

*When your loop forgets where the top floor ends…* 🛗💀

---

## 💥 Problem  
Every developer’s first nemesis:  
the **off-by-one error** — a tiny bug that opens doors to chaos.

Imagine an engineer programming an elevator for a building with **floors 0 to n-1**.  
But instead of stopping there, they add a shiny **“n” button** —  
one extra floor that doesn’t exist.

When someone presses it, the doors open...  
to *nothing*. The elevator hangs in the void,  
and the passenger screams:  
> “This wasn’t in the floor plan!” 😱

---

## 💻 Code Example (C++)

```cpp
#include <iostream>
using namespace std;

int main() {
    int floors = 5;

    for (int i = 0; i <= floors; i++) {  // ⚠️ Off-by-one error!
        cout << "Stopping at floor " << i << endl;
    }

    cout << "Doors opening at floor " << floors << "...\n";
    cout << "Error: floor not found!\n";

    return 0;
}
````

---

## 💻 Code Example (Python)

```python
floors = 5

for i in range(0, 6):  # ⚠️ Off-by-one error! range(0, 6) → runs 6 times
    print(f"Stopping at floor {i}")

print("Doors opening at floor 5...")
print("Error: floor not found!")
```

---

## 🧩 Lesson

The difference between `< n` and `<= n` decides whether you:
✅ stop safely within bounds — or
❌ overstep into an invalid range.

In most languages, arrays and loops start at `0`
and end *before* reaching `n`.
That’s why your conditions should use `< n` — not `<= n`.

**Rule of thumb:**
Count starts at zero, but ends one step before `n`.
Miss that step, and your code will take one too many.

---

## 🌍 Real-World Connection

Off-by-one errors lurk in loops, pagination,
date ranges, and even spacecraft code.

NASA once lost the Mars Climate Orbiter due to a **tiny calculation error** —
proving that even one wrong boundary can send you miles off course.

In programming, one misplaced `=` can do the same.
Precision keeps your software — and your elevators — from falling apart. 🚀

---

## 🦸 CodeLore

Our engineer wanted to make life easier —
one extra floor, what could go wrong?

But the “n-th floor” didn’t exist.
When the doors opened, the world did too.

> “For i = 0; i <= n; i++ —
> and just like that, the elevator reached the end of reality.”

---

🔙 [Back to TheCodeLores Home](../../index.md)

📅 Published: November 2025
✍️ Author: [Aisha Karigar](https://github.com/aishakarigar)

