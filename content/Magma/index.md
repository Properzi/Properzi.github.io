---
title: "Magma Workshop"
linktitle: "Magma Workshop"
type: book
---

# Magma Workshop

Here there is a collection of some magma exercises done during the
[magma workshop](https://leandrovendramin.org/magma/)

---

## Exercises

### Rings
<details>
<summary>Click to expand: Calculate the order of a group</summary>

**Exercise**:
Compute \(\mathcal{U}(\mathbb{Z}/5[X])\).

<details>
<summary>Click to reveal the solution</summary>


**Solution**:
```magma
>n := 5;
>R := IntegerRing(n);
>P<X> := PolynomialRing(R);
>U, phi := UnitGroup(R);
>U;
Abelian Group isomorphic to Z/4
Defined on 1 generator
Relations:
    4*U.1 = 0

