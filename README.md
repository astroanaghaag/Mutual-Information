# Mutual-Information

This code calculates the **Mutual Information (MI)** between two variables using a histogram-based probability estimation.

## Requirements

- Python 3.10 or later

### Python Packages

- numpy
- scipy
- matplotlib (optional, for visualization)

- ## Input

The program requires two datasets of equal length.

Example:

```
x = [x₁, x₂, ...]
y = [y₁, y₂, ...]
```

The input may be

- NumPy arrays
- Text files
- CSV files

Depending on the implementation.

The Mutual Information (MI) between two variables \(X\) and \(Y\) is computed from their individual and joint entropies as

\[
I(X;Y)=H(X)+H(Y)-H(X,Y),
\]

where

H(x), H(y) are entropy of x and Y , H(x,y) is the joint entropy




## Entropy estimation

The entropy of a variable is estimated using a histogram-based probability distribution. Given a dataset \(X\), the data are divided into \(n\) histogram bins, and the probability of each bin is calculated

The accuracy of the entropy estimate depends on the choice of the number of histogram bins (`n`)

The procedure is:

1. Compute the entropy of the variable for a range of bin numbers.
2. Plot entropy \(H(X)\) as a function of the number of bins.
3. Identify the region where the entropy values become approximately constant (i.e., the entropy saturates).
4. Choose the corresponding value of `n` from this saturation region for all subsequent entropy and Mutual Information calculations.


## References
 Cover, T. M., & Thomas, J. A. (2006),
*Elements of Information Theory*,
Wiley.




