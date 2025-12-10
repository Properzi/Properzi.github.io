---
title: "Magma Workshop"
linktitle: "Some Exercises"
type: book
---

# Exercises

Here is a collection of some magma exercises done during the
[magma workshop](https://leandrovendramin.org/magma/)

---


## Groups
---

### Actions

The functions
```magma
CosetAction(G, H) : Grp, Grp -> Hom(Grp), GrpPerm, Grp
```
and 
```magma
RegularRepresentation(G, H) : Grp, Grp -> Hom(Grp), GrpPerm, Grp
```
construct the permutation representation of $G$ on the (right) cosets of $H$ in $G$.
It returns the homomorphism, the image and (if possible) the kernel.

Note that you can get only the image using 
```magma
CosetImage(G, H) : Grp, Grp -> GrpPerm
```

and only the kernel using
```magma
CosetKernel(G, H) : Grp, Grp -> Grp
```


---
**Exercise**:  
Let $G$ be the group ```magma
G:=SmallGroup(96,3);
```
Can you give me a (faithful) permutation representation of $G$?
```


<details>
<summary>Click to reveal the solution</summary>

**Solution**:
```magma
> G:=SmallGroup(96,3);
> H:=sub<G|G.0>;
> f, P, K:=CosetAction(G,H);
> f;
Homomorphism of GrpPC : G into GrpPerm: P, Degree 96 induced by
    G.1 |--> (1, 65, 33)(2, 66, 34)(3, 67, 35)(4, 68, 36)(5, 69, 37)(6, 70,
        38)(7, 71, 39)(8, 72, 40)(9, 73, 41)(10, 74, 42)(11, 75, 43)(12, 76,
        44)(13, 77, 45)(14, 78, 46)(15, 79, 47)(16, 80, 48)(17, 81, 49)(18, 82,
        50)(19, 83, 51)(20, 84, 52)(21, 85, 53)(22, 86, 54)(23, 87, 55)(24, 88,
        56)(25, 89, 57)(26, 90, 58)(27, 91, 59)(28, 92, 60)(29, 93, 61)(30, 94,
        62)(31, 95, 63)(32, 96, 64)
    G.2 |--> (1, 23, 7, 17)(2, 24, 8, 18)(3, 21, 5, 19)(4, 22, 6, 20)(9, 31, 15,
        25)(10, 32, 16, 26)(11, 29, 13, 27)(12, 30, 14, 28)(33, 45, 37, 41)(34,
        46, 38, 42)(35, 47, 39, 43)(36, 48, 40, 44)(49, 62, 53, 58)(50, 61, 54,
        57)(51, 64, 55, 60)(52, 63, 56, 59)(65, 90, 68, 91)(66, 89, 67, 92)(69,
        94, 72, 95)(70, 93, 71, 96)(73, 86, 76, 87)(74, 85, 75, 88)(77, 82, 80,
        83)(78, 81, 79, 84)
    G.3 |--> (1, 13, 5, 9)(2, 14, 6, 10)(3, 15, 7, 11)(4, 16, 8, 12)(17, 30, 21,
        26)(18, 29, 22, 25)(19, 32, 23, 28)(20, 31, 24, 27)(33, 58, 36, 59)(34,
        57, 35, 60)(37, 62, 40, 63)(38, 61, 39, 64)(41, 54, 44, 55)(42, 53, 43,
        56)(45, 50, 48, 51)(46, 49, 47, 52)(65, 87, 71, 81)(66, 88, 72, 82)(67,
        85, 69, 83)(68, 86, 70, 84)(73, 95, 79, 89)(74, 96, 80, 90)(75, 93, 77,
        91)(76, 94, 78, 92)
    G.4 |--> (1, 5)(2, 6)(3, 7)(4, 8)(9, 13)(10, 14)(11, 15)(12, 16)(17, 21)(18,
        22)(19, 23)(20, 24)(25, 29)(26, 30)(27, 31)(28, 32)(33, 36)(34, 35)(37,
        40)(38, 39)(41, 44)(42, 43)(45, 48)(46, 47)(49, 52)(50, 51)(53, 56)(54,
        55)(57, 60)(58, 59)(61, 64)(62, 63)(65, 71)(66, 72)(67, 69)(68, 70)(73,
        79)(74, 80)(75, 77)(76, 78)(81, 87)(82, 88)(83, 85)(84, 86)(89, 95)(90,
        96)(91, 93)(92, 94)
    G.5 |--> (1, 3)(2, 4)(5, 7)(6, 8)(9, 11)(10, 12)(13, 15)(14, 16)(17, 19)(18,
        20)(21, 23)(22, 24)(25, 27)(26, 28)(29, 31)(30, 32)(33, 40)(34, 39)(35,
        38)(36, 37)(41, 48)(42, 47)(43, 46)(44, 45)(49, 56)(50, 55)(51, 54)(52,
        53)(57, 64)(58, 63)(59, 62)(60, 61)(65, 70)(66, 69)(67, 72)(68, 71)(73,
        78)(74, 77)(75, 80)(76, 79)(81, 86)(82, 85)(83, 88)(84, 87)(89, 94)(90,
        93)(91, 96)(92, 95)
    G.6 |--> (1, 2)(3, 4)(5, 6)(7, 8)(9, 10)(11, 12)(13, 14)(15, 16)(17, 18)(19,
        20)(21, 22)(23, 24)(25, 26)(27, 28)(29, 30)(31, 32)(33, 34)(35, 36)(37,
        38)(39, 40)(41, 42)(43, 44)(45, 46)(47, 48)(49, 50)(51, 52)(53, 54)(55,
        56)(57, 58)(59, 60)(61, 62)(63, 64)(65, 66)(67, 68)(69, 70)(71, 72)(73,
        74)(75, 76)(77, 78)(79, 80)(81, 82)(83, 84)(85, 86)(87, 88)(89, 90)(91,
        92)(93, 94)(95, 96)

> K;
GrpPC of order 1
PC-Relations:

```

<details>

---

**Exercise**:  
Write a function that returns the multiplication table of a given
group.

<details>
<summary>Click to reveal the solution</summary>

**Solution**:
```magma
>
> 
> 
> 
> 

```
<details>



## Rings

---

**Exercise**:  
Compute \(\mathcal{U}(\mathbb{Z}/5[X])\).

<details>
<summary>Click to reveal the solution</summary>

**Solution**:
```magma
> n := 5;
> R := IntegerRing(n);
> P<X> := PolynomialRing(R);
> U, phi := UnitGroup(R);
> U;
Abelian Group isomorphic to Z/4
Defined on 1 generator
Relations:
    4*U.1 = 0
```

</details>

---

**Exercise**:  
Prove that $\mathbb{Q}[\sqrt{2}]$ is a field.  
Find the multiplicative inverse of a non-zero element of the form  
\(x+y\sqrt{2}\in\mathbb{Q}[\sqrt{2}]\).  

<details>
<summary>Click to reveal the solution</summary>

```magma
> P<x> := PolynomialRing(Rationals());
> I := ideal<P | x^2 - 2>;
> Qsqrt2<a> := quo<P | I>;
> IsField(Qsqrt2);
true;
> x := 3;
> y := 1;
> alpha := x + y*a;
> alpha_inv := 1/alpha;
> alpha_inv;
-1/7*a + 3/7
```

</details>

---

**Exercise**:  
Prove that every ideal of $\mathbb{Z}$ is of the form \(n\mathbb{Z}\) for some \(n\ge 0\).

<details>
<summary>Click to reveal the solution</summary>

```magma
> Z := Integers();
> n := 6;
> m := 15;
> I := ideal<Z | n, m>;
> I;
Ideal of Integer Ring generated by 3
```

</details>

---

**Exercise**:  
There is no ring homomorphism \(\mathbb{Z}/6 \to \mathbb{Z}/15\). Explain why.

<details>
<summary>Click to reveal the solution</summary>

```magma
// No homomorphism exists because 1 ↦ 1 must hold, 
// but then images of units must be units.
// In Z/6, 5 is a unit, but in Z/15 it is not.
```

</details>

---

**Exercise**:

<details>
<summary>Click to reveal the solution</summary>

```magma
// Solution placeholder
```

</details>

---

**Exercise**:

<details>
<summary>Click to reveal the solution</summary>

```magma
// Solution placeholder
```

</details>

---

**Exercise**:

<details>
<summary>Click to reveal the solution</summary>

```magma
// Solution placeholder
```

</details>

---


