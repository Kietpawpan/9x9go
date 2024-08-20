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
   
## Monteo Game Format:
Monteo Game Format (MGF) is a JavaScript code to create a 9 x 9 Go diagram for game annotation in _The Art of 9 x 9 Go: Superhuman Edition_, by Monteo da Westi and A Master of Go, 9 Dan++.

Each move is recorded with the following format:
> [!NOTE]  
> Move = [mark][stone color][move number][SGF coordinate]
> 
> [mark] = [cross, triangle, squared, circle, [text]] = [X,T,S,C, {[A,B,C,D]<==[A,K,B,C]}]
> 
> [stone color] = [black, white] = [b,w]
> 
> [move number] = [1, 2, ..., 81]
>
> SGF coordinate = [aa, ab, ..., ai, ba, ..., bi, ia, ..., ii]:

```
   a b c d e f g h i
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
Hence,
1. A black stone with number 3 at ee is b3ee
2. A white stone with number 4 at ef is w4ee
3. A black stone at cf is bcf
4. A white stone at dj is wdj
5. A triangle mark at dh is Mdh
6. A triangle mark on the black stone at ff is Tbff
7. A triangle mark on the white stone at fg is Twfg
8. A square mark on the black stone at ae is Sbae
9. A square mark on the white stone at af is Swaf
10. A circle mark on the black stone at ac is Cbac
11. A circle mark on the white stone at ec is Cwec
12. Mark A, B, C, D at fe, ff, aa, bc, respectively is Afe+Kff+Caa+Dbc, respectively.

> [!NOTE]  
> Multiple Moves = Move 1 + Move 2 + Move 3 +...+ Move N + b;
For example,
```
mgf = b1ee + w2ec + b3fg + w4cf + b5dd + w6dc + Acd + b;
```
> [!NOTE]  
> __+b__ at the end of MGF code helps create the board graphic.

  
## Credits
<img src="https://kietpawpan.github.io/9x9go/wood1.jpg" width="50">
The background image is the wood image by [2happy](https://www.stockvault.net/user/profile/87395)[https://www.stockvault.net/photo/124529/wood-background](https://www.stockvault.net/photo/124529/wood-background) 
  
## Exmamples
1. [Do not play a Thank You Move](https://kietpawpan.github.io/9x9go/c001ThankYou.html).

