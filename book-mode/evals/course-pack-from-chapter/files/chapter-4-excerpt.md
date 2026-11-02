# Chapter 4. Stability of linear systems (excerpt)

## 4.1 The notion of stability [p. 101]

A linear time-invariant system is stable in the bounded-input, bounded-output (BIBO) sense if every bounded input produces a bounded output.

For a system with transfer function H(s) = B(s) / A(s), with no common factors between B(s) and A(s), the equation A(s) = 0 is called the characteristic equation and its roots are the poles of the system.

[p. 102]

The system is stable if and only if all its poles have negative real parts, that is, they lie in the left half of the s-plane. If at least one pole has a positive real part, the system is unstable: its response contains a term that grows without bound.

Simple poles on the imaginary axis give a response that neither decays nor grows; such a system is called marginally stable. It is not BIBO stable: for example, the integrator H(s) = 1/s answers a unit step with a ramp, which grows without bound.

A necessary condition: for A(s) = a_n s^n + a_(n-1) s^(n-1) + ... + a_1 s + a_0 with a_n > 0, all coefficients must be present and positive. The condition is also sufficient for n = 1 and n = 2, but not for n >= 3.

## 4.2 The Routh criterion [p. 103]

The Routh criterion decides stability from the coefficients of A(s), without computing the roots.

Build the Routh table. Its first row holds a_n, a_(n-2), a_(n-4), ...; its second row holds a_(n-1), a_(n-3), a_(n-5), .... Each element of the next row is computed from the two rows above it; for example, the first element of the third row is

b_1 = (a_(n-1) a_(n-2) - a_n a_(n-3)) / a_(n-1).

Continue until the row for s^0.

[p. 104]

The number of sign changes in the first column of the table equals the number of roots of A(s) with positive real parts. The system is stable if and only if all elements of the first column have the same sign.

Example 1. A(s) = s^3 + 2s^2 + 3s + 4.
Row s^3: 1, 3. Row s^2: 2, 4. Row s^1: (2*3 - 1*4) / 2 = 1. Row s^0: 4.
First column: 1, 2, 1, 4. No sign changes: the system is stable.

Example 2. A(s) = s^3 + s^2 + 2s + 8.
Row s^3: 1, 2. Row s^2: 1, 8. Row s^1: (1*2 - 1*8) / 1 = -6. Row s^0: 8.
First column: 1, 1, -6, 8. Two sign changes: two roots in the right half-plane, so the system is unstable.

[p. 105]

Special cases. If a zero appears in the first column while the rest of its row is not zero, replace it with a small positive number epsilon and continue. If a whole row becomes zero, the polynomial has roots placed symmetrically about the origin; form the auxiliary polynomial from the row above, differentiate it, and use its coefficients in place of the zero row.
