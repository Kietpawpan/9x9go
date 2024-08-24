# artof9x9.js
_A web application for creating HTML/CSS [9 x 9 Go diagram](https://kietpawpan.github.io/9x9go/) to support 9 x 9 Go game annotation in The Art of 9x9 Go ebook_

## How to Use
1. To display moves in this 9 &times; 9 Go diagram, let's copy the moves being considered   from an SGF file. For example,
```
B[ee];W[ec];B[fg];W[cf];B[dd];W[dc]
```
2. Paste the SGF moves into the input box of the [SGF Viewer](https://kietpawpan.github.io/9x9go/SGFviewer.html), to display the 9 x 9 Go diagram accordingly.
3. Or, paste the SGF moves into the input box of the [SGF to MGF Convertor](https://kietpawpan.github.io/9x9go/mgf.html), to convert the SGF moves to the MGF moves. 
4. Copy the MGF moves from step 3 and paste them into the input box of the [MGF Viewer](https://kietpawpan.github.io/9x9go/MGFviewer.html), to display the annotation diagram.
   
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
<img src="https://kietpawpan.github.io/9x9go/wood1.jpg" width="200"></img>

Image by 2happy<br>[https://www.stockvault.net/photo/124529/wood-background](https://www.stockvault.net/photo/124529/wood-background) 
  
## Examples
1. [Do not play Thank-you moves](https://kietpawpan.github.io/9x9go/c001ThankYou.html).
2. [One-pont jump is usually the best](https://kietpawpan.github.io/9x9go/c002OPJ.html).
