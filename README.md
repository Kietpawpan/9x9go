# 9x9go
[Go board](https://kietpawpan.github.io/9x9go/) for 9 x 9 Go game annotation

## Documentation
1. Copy an SGF file (moves only)
2. Convert the SGF moves to the MGF string with the [SGF to MGF Convertor](https://kietpawpan.github.io/9x9go/mgf.html)
3. Copy the MGF string and paste it in the index file, as the sgf variable's value. 
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
