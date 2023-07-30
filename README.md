# rubic_cube_calculator
Calculator for Rubic's Cube operations

---

# Notation

## clockwise 90 degrees rotations
- F = front face clockwise 90 degrees turn
- R = right face clockwise 90 degrees turn
- B = back face clockwise 90 degrees turn
- L = left face clockwise 90 degrees turn
- U = up face clockwise 90 degrees turn
- D = down face clockwise 90 degrees turn

## cycle notation
See https://en.wikipedia.org/wiki/Permutation#Cycle_notation

- F = (ful,fru,fdr,fld) (fu,fr,fd,fl)
- R = (ruf,rbu,rdb,rfd) (ru,rb,rd,rf)
- B = (bur,blu,bdl,brd) (bu,bl,bd,br)
- L = (lub,lfu,ldf,lbd) (lu,lf,ld,lb)
- U = (ufr,ulf,ubl,urb) (uf,ul,ub,ur)
- D = (drf,dbr,dlb,dfl) (df,dr,db,dl)

For example: F consists of permutating 4 corner pieces (ful,fru,fdr,fld) while also permutating 4 edge pieces (fu,fr,fd,fl).

When calculating (FR)^4, which means repeating 4 times doing a F followed by a R rotation, we get:
> (ful,ldf,rfd,dbr,urb)++ (fru)+ (fu,fr,ur,fd,br,fl,dr)

The + sign in (fru)+ means that fru is not mapped to itself, but instead mapped to a rotated version of itself, where the faces map like this:
> f -> r, r-> u, u -> f

In the (ful,ldf,rfd,dbr,urb)++ permutation, the last corner piece "urb" maps not directly to "ful", but rather to "lfu" like this:
> u -> l, r -> f, b -> u
