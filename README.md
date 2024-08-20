# 9x9go
HTML/CSS [Go board](https://kietpawpan.github.io/9x9go/) for 9 x 9 Go game annotation

## How to Use
1. To display moves in this 9 &times; 9 Go diagram, let's copy the moves being considered   from an SGF file. For example,
```
B[ee];W[bc];B[ef];W[bc]
```
2. The [SGF Viewer](https://kietpawpan.github.io/9x9go/SGFviewer.html) is used for displaying the game from an SGF moves.
3. Paste the SGF moves to the input textarea of the [SGF to MGF Convertor](https://kietpawpan.github.io/9x9go/mgf.html). The SGF moves will be automatically converted to the MGF (Monteo Game Format) string.

4. Learn to know the MGF code. For example,
```
b1ee;w2ec;b3fg;w4cf;b5dd;w6dc;Acd
```
5. Paste the MGF code into the [MGF Viewer](https://kietpawpan.github.io/9x9go/MGFviewer.html) to plot the annotation diagram.
   
## MGF Codes for annotation:
Monteo Game Format (MGF) is a code of Go moves in JavaScript. Each move is recorded with the following format:
> [!NOTE]  
> Move = [mark][stone color][move number][SGF coordinate]
> [mark] = [cross, triangle, squared, circle] = [X,T,S,C]
> [stone color] = [black, white] = [b,w]
> [move number] = [1, 2, ..., 81]
> SGF coordinate = [aa, ab, ..., ai, ba, ..., bi, ia, ..., ii]:

```
.  a b c d e f g h i
a aa . . . . . . . .
b  . . . . . . . . .
c  . . . . . . . . .
d  . . . . . . . . .
e  . . . . ee . . . .
f  . . . . . . . . .
g  . . . . . . . . .
h  . . . . . . . . .
i  . . . . . . . . ii 
```
1. A black stone with number 3 at ee: b3ee
2. A white stone with number 4 at ef: w4ee
3. A black stone at cf: bcf
4. A white stone at dj: wdj
5. A triangle mark at dh: Mdh
6. A triangle mark on the black stone at ff: Tbff
7. A triangle mark on the white stone at fg: Twfg
8. A square mark on the black stone at ae: Sbae
9. A square mark on the white stone at af: Swaf
10. A circle mark on the black stone at ac: Cbac
11. A circle mark on the white stone at ec: Cwec
12. Mark A, B, C, D) at fe, ff, aa, bc, respectively: Afe+Kff+Caa+Dbc

> [!NOTE]  
> __+b__ at the end of MGF code helps create the board graphic.

> [!IMPORTANT]  
> ## Credits
> > Wood image by [2happy](https://www.stockvault.net/user/profile/87395)
> > > [https://www.stockvault.net/photo/124529/wood-background](https://www.stockvault.net/photo/124529/wood-background) 
  
## Exmamples
1. [Do not play a Thank You Move](https://kietpawpan.github.io/9x9go/c001ThankYou.html).

