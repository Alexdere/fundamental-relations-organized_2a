# Reproducibility — Exact Arithmetic Experiments

## Experiment E1 (reproduced 2026-10-17)
**Frame: F-C/F-P.** Compute (S_k=\sum_{i=1}^k p_i^2) for every prime (p_i<10,000,000), using arbitrary-precision integers. Check whether (8S_k+1) is an odd square; for such cases the triangular index is (t=(\sqrt{8S_k+1}-1)/2). Check separately whether (t) is a square.

Exact algorithm (Python 3, requires SymPy):
```python
from math import isqrt
from sympy import primerange

s = 0
triangular_hits = []
square_index_hits = []
for k, p in enumerate(primerange(2, 10_000_000), start=1):
    s += p*p
    h = isqrt(8*s+1)
    if h*h == 8*s+1:
        t = (h-1)//2
        triangular_hits.append((k,p,t,s))
        n = isqrt(t)
        if n*n == t:
            square_index_hits.append((k,p,n,s))
print(triangular_hits)
print(square_index_hits)
```

**Reproduced output:**
```text
[(7, 17, 36, 666), (86, 443, 3169, 5022865)]
[(7, 17, 6, 666)]
```

**Count:** 664579 primes, upper bound exclusive. This proves only the output for this search domain.

## Experiment E2 (direct Pell validation)
**Frame F-D.** For each pair ((n,m)) from recurrence ((3n+4m,2n+3m)), check (n^2-2m^2=-1), (a=T_{n-1},b=T_n), and (a^2+b^2=(nm)^2). First pairs ((1,1),(7,5),(41,29),(239,169)).

## Planned tests
- Modulo-prime filters for (S_k=T_{n^2}) before more expensive searches.
- Alternative polynomial index maps (f(n)).
- Counterexample searches against overgeneralized geometric claims.

## Integrity
Use exact integers and `isqrt`, not floating-point equality. Save inputs, code, bound, outputs, and date in the experiment ledger when extending.
