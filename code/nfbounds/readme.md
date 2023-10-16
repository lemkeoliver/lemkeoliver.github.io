This folder contains the Magma code needed to verify many of the invariant theory computations from my paper "Uniform exponent bounds on primitive extensions of number fields."

The file "find-invariants.mag" contains many of the workhorse functions, described below.  The folder "receipts" contains the verification of the specific computations quoted in the paper, namely the proofs of Lemma 4.19 (which fidnds the minimal invariants of the Mathieu groups) and Theorem 5.8 (which gives bounds on small degree extensions of number fields).

Inside the file "find-invariants.mag", the key functions are:
1) FindIndependentInvarints( G,d)  
	Output = [Invariant degrees], success, corank
	-----  
	This computes all G-invariant polynomials of degree up to d, then computes the rank of the partial derivative matrix associated with these invariants, evaluated at a random n-tuple of integers (n being the degree of G) between -height and height.  (Default: height:=10)  
	If the matrix has full rank n, the function returns the degrees of the associated invariants (along with success=true and corank=0).  If the matrix does not have full rank, it recomputes the rank evaluated at a different random tuple, up to trials times.  (Default: trials:=10)
	If none of these matrices have full rank, the function returns [], false, corank, where corank is n minus the maximum rank seen.
