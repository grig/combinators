* Question: is there a systematic method such that giving any behavior like

    Xxyztuv = x(yx)(uvut) (or what you want)

can generate systematically a corresponding SK or BWCK -combinator? The answer is yes. I let you meditate the question. (This point will be made clear when we will meet the terrible little cousins of the combinators which are the lambda expression, (and which in our context will just abbreviate complex combinators), but I propose to progress and make sure that the SK combinator are Turing Universal.

I am not yet decided when I really should introduce you to the paradoxical combinators, which are rather crazy. Smullyan call them wise birds, but I guess it is an euphemism!

Mmhhh... Showing turing-universality through the use of some paradoxical combinator is easy (once we have defined the numbers), but there is a risk you take bad habits! Actually we don't need the paradoxical combinators to prove the turing universality of the SK forest, mmmmh...

Well actually I will be rather busy so I give you the definition of a paradoxical combinator and I let you search one.

First show that for any combinator A there is a combinator B such that AB = B. B is called a fixed point of A. (like the center of a wheel C is a fixed point of the rotations of the wheel: RC = C). It is a bit amazing that all combinators have a fixed point and that is what I propose you try to show. Here are hints for different arguments. 1) Show how to find a fixed point of A (Arbitrary combinator) using just B, M and A. (Mx = xx I recall). 2) The same using just the Lark L (Lxy = x(yy) I recall). Now, a paradoxical combinator Y is just a combinator which applied on that A will give the fixed point of A; that is YA will give a B such that AB = B, that is A(YA) gives YA, or more generally Y is a combinator satisfying Yx = x(Yx).

** Problem: fixed point of A

Show that for any combinator A there is a combinator B such that AB = B

*** Solution

    Ax = x, x=?

Fixpoint of S:

    SX = X. That is, X is such that for all y,
    SXy = Xy, that is, for all z
    SXyz = Xyz

let X = MX'

    S(X'X')yz = X'X'yz
    (X'X')z(yz) (1)           = X'X'yz (2)

let X' = SX'', then

(2) = SX''(SX'')yz = X''z(SX''yz) = X''z((X''z)(yz))
    = B(X''z)(X''z)(yz)

(1) = SX''(SX'')z(yz) = X''z(SX''z)(yz) = B(X''z)(SX'')z(yz)

    Xz(yz) = Xyz
    B(Xz)yz = Xyz

    B(Xz)y = Xy. let y = X, then
    B(Xz)X = XX = MX
    BBXzX = XX = MX



    X'X'yz = S(MX')yz = BSMX'yz
    X' = BSM
    X = M(BSM)

** Check:

   M(BSM)yz = BSM(BSM)yz = S(M(BSM))yz

Fixpoint of I:

    Ix = x

any combinator is a fixpoint of I

Fixpoint of K

    Kx = x
    Kxy = xy = x, that is, x is such that for all y
    xy = x
    M(BKM)y = BKM(BKM)y = K(M(BKM))y = M(BKM) !!!

    fixpoint of K is M(BKM). indeed,

    K(M(BKM))y = M(BKM); while M(BKM)y = M(BKM)


Search X as M(X')

    KXy = Xy = X

    Xy = M(X')y = X'X'y = M(X')
    X'X'y = KXy = K(MX')y = BKMX'y
    X' = BKM // is that legal?
    X = M(BKM)


** Fixpoint of B

BX = X

BXyz = Xyz

X = M(BBM)

Xyz = M(BBM)yz = BBM(BBM)yz = B(M(BBM))yz = BXyz

X = M(BBM) = BBM(BBM) = B(M(BBM)) = BX

** Fixpoint of M

X = M(BMM)

Xy = M(BMM)y = BMM(BMM)y = M(M(BMM))y

** Fixpoint of A

X = M(BAM) = BAM(BAM) = A(M(BAM)) = AX

* Y

YA = M(BAM)

fixpoint of Y is M(BYM), that is, YM(BYM) = Y
                                 BYM(BYM) = BY
                                 M(BYM)   = BY
                                 M(BYM)M  = BYM
                                 YYM      = BYM

Yx = M(BxM)

M(BxM) = BM(Bx)M = B(BM)BxM = B(BM)Bx(KMx) = S(B(BM)B)(KM)x

Y = S(B(BM)B)(KM)
