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
var sgf = b1de+w2fe+b3ee+w4fd+b5ff+w6gf+b7gg+w8fg+b9ef+w10gh
+b11hg+w12hh+b13eg+w14fh+b15ge+w16hf+b17he+w18ig+b19fc+w20gd
+b21gc+w22hd+b23ed+w24be+b25hc+w26ie+b27bc+w28cg+b29cf+w30bf
+b31ch+w32cc+b33cb+w34dg+b35dh+w36bh+b37eh+w38dc+b39bd+w40ec
+b41cd+w42fb+b43gb+w44bb+b45eb+w46db+b47fa+w48ca+b49ea+w50da
+b51df+w52bg+b53bi+w54ab+b55ah+w56ci+b57di+w58ag+b59ae+w60ac
+b61ad+w62ha+b63hb+w64fi+b65ce+w66ai+b67ci+w68ei+b69ah+w70ic
+b71ib+w72ai+b73ba+w74aa+b75ah+w76ga+b77ia+w78ai+b79ga+w80id
+b;

```
## MGF Codes for annotation:
1. A black stone with number 3 at ee: b3ee
2. A white stone with number 4 at ef: w4ee
3. A black stone at cf: bcf
4. A white stone at dj: wdj
5. A triangle mark at dh: Tdh
6. A square mark at fi: Sfi
7. A circle mark at ae: Cae
8. A triangle mark on the black stone at ff: Tbff
9. A triangle mark on the white stone at fg: Twfg
10. A square mark on the black stone at ae: Sbae
11. A square mark on the white stone at af: Swaf
12. A circle mark on the black stone at ac: Cbac
13. A circle mark on the white stone at ec: Cwec
14. Mark A, B, C, D) at fe, ff, aa, bc, respectively: Afe+Bff+Caa+Dbc

> [!NOTE]  
> __+b__ at the end of MGF code helps create the board graphic.
 
