# GramSchmidt
Orthonormalizes a set of vectors or polynomials using the Gram-Schmidt process. It works with different kinds of scalar products.

- basis is a list of numpyarrays which form the basis of a linear subspace
- func_sp is the function calculation the inner product. Currently included are the dot product as well as a polynomial scalar product

## Examples

Calculation of an othonormal basis from a basis of a subspace of $R^{n}$:

```python
basis = [np.array([1,-1,0]), np.array([1,0,-1])]

onormbasis = gs(SSP, basis)
print(onormbasis[0])
print(onormbasis[1])
```

    [ 0.70710678 -0.70710678  0.        ]
    [ 0.40824829  0.40824829 -0.81649658]


Calculation of an orthonormal basis from a basis of a subspace of $R[x]$:


```python
basis = [np.array([1,0,1]), np.array([1,0,0]), np.array([0,1,0])]

onormbasis = gs(polynomialSP, basis)
print(onormbasis[0])
print(onormbasis[1])
print(onormbasis[2])
```

    [0.73192505 0.         0.73192505]
    [ 1.30930734  0.         -3.27326835]
    [ -2.59807621  13.85640646 -12.99038106]



```python

```
