See http://github.com/raganwald/homoiconic/tree/master/2008-11-12/combinator_chemistry.md

# Intro

sxyz = xz(yz)
kxy = x

# Exercises

   (ss)kkk = sk(kk)k = kk((kk)k) = kkk = k
   kkk(ss) = k(ss)
   (kk)(kk)(kk) = k(kk)
   (kkk)(kkk)(kkk) = k(kkk)(kkk) = (kkk) = k

   k = k
   kk = kk
   kkk = k
   kkkk = kk
   kkkkk = kkk = k
   kkkkkk = kkkk = kk
   kkkkkkk = kkkkk = kkk = k

A little more advanced exerciaes: is there a molecule, let us called it I, having the following dynamic: (X refers to any molecule).

  Ix = x I=?

  I = k -
  I = s -
  I = ks -
  I = sk -
  I = kk -
  I = ss -
  I = sss -
  I = skk skkx = kx(kx) = x

  Ix = skkx = kx(kx) = x

## New programming exercises:

Find combinators M, B, W, L, T such that

     Mx = xx

### Solution

     xx = Ix(Ix) = SIIx => M = SII

## B
     Bxyz = x(yz)

### Solution

     x(yz) = S?yz, ?z = x. Kxz = x => x(yz) = S(Kx)yz = ((KS)x)(Kx)yz = S(KS)Kxyz
     B = S(KS)K

## W

     Wxy = xyy

### Solution

     xyy = (xy)y =
            = (xy)(?xy) = (xy)(KIxy) = Sx(KIx)y = Sx((KI)x)y
            = SS(KI)xy

### Check:
    SS(KI)xy = Sx(KIx)y = xy(KIxy) = xy(Iy) = xyy
    W = SS(KI)

## L
   Lxy = x(yy)

### Solution

    Lxy = x(yy) = (Kxy)(yy) = S(Kx)yy = (KSx)(Kx)yy = S(KS)Kxyy =
    S(KS)K(Wxy)
    Lxy = x(yy) = x(My) = (Kxy)(My) = S(Kx)My = (KSx)(Kx)My = S(KS)KxMy

    S(Kx)yy = ?xy


    S(Kx)y = ?x

    Lxy = x(yy)

    x(yy) = Kxy(yy) = S(Kx)My = S(Kx)My = (KSx)(Kx)My = S(KS)KxMy =
    (S(KS)Kx)(KMx)y = S(S(KS)K)(KM)xy

    L = S(S(KS)K)(KM)

### Check

    S(S(KS)K)(KM)xy = S(KS)Kx(KMx)y = S(KS)KxMy = (KSx)(Kx)My = S(Kx)My =
    (Kxy)(My) = x(My) = x(yy)

### Another solution

    x(yy) = Bxyy = (Bx)yy = W(Bx)y = BWBxy

### check

    BWBxy = W(Bx)y -- dynamics of B
          = (Bx)yy -- dynamics of W
          = Bxyy
          = x(yy)

## T

   Txy = yx

### Solution

   yx = y(Kxy) = (Iy)(Kxy) = SI(Kx)y = (K(SI)x)(Kx)y = S(K(SI))Kxy

   T = S(K(SI))K

   Txy = S(K(SI))Kxy = (K(SI)x)(Kx)y = SI(Kx)y = Iy(Kxy) = yx

### Another

    yx = y(Kxy) = SI(Kx)y = B(SI)Kxy

## C

   Cxyz = xzy

### Solution 1

    xzy = xz(Kyz) = Sx(Ky)z = K(Sx)y(Ky)z = S(K(Sx))Kyz = S((KKx)(Sx))Kyz
        = S(S(KK)Sx)Kyz = ((KS)x)((S(KK)S)x)Kyz
        = S(KS)(S(KK)S)xK yz = ;; (K = (KKx))
        = S(KS)(S(KK)S)x((KK)x) yz
        = S(S(KS)(S(KK)S))(KK)xyz

    C = S(S(KS)(S(KK)S))(KK)

### Solution 2

    xzy = xz(Kyz) = Sx(Ky)z = B(Sx)Kyz = BBSxKyz = BBSx(KKx)yz
        = S(BBS)(KK)xyz

    C = S(BBS)(KK)

## INFINITY

INFINITY dynamically transform into INFINITY itself.

### Solution

   MM = MM, thus,
   INFINITY = MM

## S

We have seen how to program the blue bird B, the cardinal C and the
Warbler W with the kestrel K and the starling S. Could you define the
starling S from B, W and C? I give you the first line:

         Sxyz = xz(yz)
              = Cx(yz)z
              = B(Cx)yzz
              = (B(Cx)y)zz
              = W(B(Cx)y)z
              = W(BBCxy)z
              = W((BBCx)y)z
              = BW(BBCx)yz
              = BW((BBC)x)yz
              = B(BW)(BBC)xyz
