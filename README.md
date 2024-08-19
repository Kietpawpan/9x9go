# 9x9go
HTML/CSS [Go board](https://kietpawpan.github.io/9x9go/) for 9 x 9 Go game annotation

## How to Use
1. To display moves in this 9 &times; 9 Go diagram, let's copy the moves being considered   from an SGF file. For example,
```
B[ee];W[bc];B[ef];W[bc]
```
3. Paste them to the input textarea of the [SGF to MGF Convertor](https://kietpawpan.github.io/9x9go/mgf.html). The SGF moves will be automatically converted to the MGF (Monteo Game Format) string.
4. Click the copy button and paste it in the index file, within the &lt;script&gt; tag, for the value of the sgf variable. For example,
```
var sgf = b;

```
5. The [SGF Viewer](https://kietpawpan.github.io/9x9go/SGFviewer.html) is used for displaying the game from an SGF moves.
6. The [MGF Viewer](https://kietpawpan.github.io/9x9go/MGFviewer.html) is used for ploting the game annotation, based on the MGF codes.
   
## MGF Codes for annotation:
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

