---
layout: default
title: Главная
---

# Алгоритмы и структуры данных

## Бинарный поиск

Сложность: $O(\log n)$

Формула:

$$
T(n) = T(n/2) + O(1)
$$

```cpp
int bin_search(vector<int>& a, int x) {
    int l = 0, r = a.size()-1;
    while (l <= r) {
        int m = (l + r) / 2;
        if (a[m] == x) return m;
        if (a[m] < x) l = m + 1;
        else r = m - 1;
    }
    return -1;
}
```
