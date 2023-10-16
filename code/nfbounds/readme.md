This folder contains the Magma code needed to verify many of the invariant theory computations from my paper "Uniform exponent bounds on primitive extensions of number fields."

The file "find-invariants.mag" contains many of the workhorse functions, described below.  The folder "receipts" contains the verification of the specific computations quoted in the paper, namely the proofs of Lemma 4.19 (which fidnds the minimal invariants of the Mathieu groups) and Theorem 5.8 (which gives bounds on small degree extensions of number fields).

Inside the file "find-invariants.mag", the key functions are:
1) FindIndependentInvarints( G,d).  Output = [Invariant degrees], success.  
	This computes all G-invariant polynomials of degree up to d, then computes the rank of the partial derivative matrix associated with these invariants, evaluated at a random n-tuple of integers (n being the degree of G) between -10 and 10.  If the matrix has full rank (=n), the function returns the degrees of the associated invariants.  The optional parameter trials (default 10) controls how many times times this random evaluation will be tried if the matrix is not full rank.  
