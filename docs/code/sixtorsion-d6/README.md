## Robert J. Lemke Oliver's code repository

This is the main hub for code related to the paper "Asymptotics for 6-torsion and D_6-extensions", available on the arxiv here: arxiv link.

In particular, the Magma files above were used in the computations of local etale algebras over Q2 and Q3 during the course of the proof of Theorem 1.4.  The file `etale-algebras.mag` loads the two subfiles `etale-algebras-Q2.mag` and `etale-algebras-Q3.mag` in turn, and the file `etale-algebras-output.txt` records the output of running that Magma file.  The heart of the computation is in those two subfiles, which each pull substantially from the [LMFDB](https://www.lmfdb.org/).
