
## Functional Dependency

When one attribute can be used to uniquely determine (or fetch) another.

For example, `Employee ID` can be used to determine `Employee Name`.

- Determining attribute = **Determinant** 
- Attribute being determined = **Dependent**

Represented as: 

$$
 A \rightarrow B
$$

For example:

$$
EmployeeID \rightarrow EmployeeName
$$


### Trivial Dependency

When

$$ 
    B \subset A
$$

And 

$$
 A \rightarrow B
$$

For example,

$$
DateOfBirth \rightarrow YearOfBirth
$$
$$
FullAddress \rightarrow City
$$

The dependent attribute (B) should really be a subset of the determinant (A) for it to be a trivial dependency. Being able to calculate an attribute on basis of another doesn't make the calculable attribute a subset. For example, `Age` can be determined from `Date of birth` but `Age` is NOT a subset of `Date of birth`.

### Partial

When an attribute is dependent on only a part of a composite primary key

### Transitive


## Multivalued
