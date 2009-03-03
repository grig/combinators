Well, you should be able to solve an exercise like finding a
combinator A such that its dynamics is described by Axyz =
y(yx)zz. Some other day we will make this precise by giving an
algorithm for solving such problem (which solutions exist in all
"sufficiently rich forest like the SK or BWCK forest). With the fixed
point combinators you should be able to solve "recursive equations"
like: find a A such that its dynamics is described recursively by Axyz
= xxA(Ayy)z. How? Just find a B such that Baxyz = xxa(ayy)z (A has
been replaced by a variable a). This is a traditional (non recursive)
exercise. Then YB gives the solution of the recursive equation. (Y is
the traditional name for a paradoxical combinator). Exercise: why?

## Solution

   B(YB) = YB
   B(YB)xyz = xx(YB)(YByy)z = YBxyz
let YB = A, then
    Axyz = xxA(Ayy)z

# exercises

Find an infinite eliminator E, that is a bird which eliminates all its
variables: Ex = E, Exy = E, etc.

Find an perpetual permutator, that is a bird which forever permutes
its two inputs: its dynamics is as follow: Pxy =: Pyx =: Pxy =: Pyx
etc. (I recall "=:" is the reduction symbol of the dynamics; it is the
left to right reading of the "dynamics").

Etc. I mean: solve the following equations (little letters like x, y z
are put for any combinator, A is put for the precise combinator we are
ask searching for):

# Ax = A

## solution

Let's find B such that

      Bax = a
      B = K
      A = YB = YK = SLLK

# Ax = xA

  Bax = xa
  B = T = B(SI)K
  A = YB = YT = SLLT

# Axy = Ayx

  Baxy = ayx
  B = C
  A = YB = YC

# Ax = AAx

  Bax = aax

  aax = (aa)x = Max, so B = M, A = YB = YM

# A = AA

  Ba = aa

  B = M => A = YM

# Ax = AA

  Xax = aa

  aa = Ma = K(Ma)x = BKMax
  X = BKM
  A = YX = YBKM

# Ax = x(Ax)

  Bax = x(ax)
  x(ax) = Ix(ax) = SIax
  B = SI => A = YB = YSI
