# artof9x9.js
_A commercial web application for creating HTML/CSS [Go board](https://kietpawpan.github.io/9x9go/) to support 9 x 9 Go game annotation_

## How to Use
1. To display moves in this 9 &times; 9 Go diagram, let's copy the moves being considered   from an SGF file. For example,
```
B[ee];W[bc];B[ef];W[bc]
```
2. The [SGF Viewer](https://kietpawpan.github.io/9x9go/SGFviewer.html) is used for displaying the game from an SGF moves.
3. The [SGF to MGF Convertor](https://kietpawpan.github.io/9x9go/mgf.html) is used for converting SGF moves to the MGF codes.

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
<img src="https://kietpawpan.github.io/9x9go/wood1.jpg" width="200"></img>

Image by 2happy<br>[https://www.stockvault.net/photo/124529/wood-background](https://www.stockvault.net/photo/124529/wood-background) 
  
## Exmamples
1. [Do not play Thank-you moves](https://kietpawpan.github.io/9x9go/c001ThankYou.html).
```
<!DOCTYPE html>

<html>
<head>
	<meta charset="utf-8">
	<meta name="viewport" content="width=device-width, initial-scale=1">
	<title>The Art of 9 &times 9 Go</title>
	<link rel="stylesheet" href="9x9Board.css">
	<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>
</head>

<body onload="mgf()">
</head>
<body>

  

<div class="grid-container" id='board'></div><br><span style="float:left;margin-left:50px;font-size:15px;color:#686360;">Copyright &copy; 2024 by Monte Kietpawpan. All rights reserved.</span>



<p style="margin-top:-460px;"><b>

<!------------------TITLE------------------>


</b><font style="font-size:20px;"><b>


<!------------------SUB------------5a5858------>



</b></font>
<textarea id="mgf" style="resize:none;margin-top:-12px;"></textarea>


<span style="position:absolute;margin-top:392px;margin-left:-240px;font-size:30px;color:white;">
<a href="#" class="previous">&laquo;</a>
<a href="#" class="next">&raquo;</a>
<br></span>


<textarea id='record' style="width:400px;height:100px;" placeholder="MGF input" hidden>



<!------------------MGF CODE------------------>

B1ee;w2ec;b3fg;w4cf;b5dd;w6dc;Acd


</textarea><br>
<!--button onclick="copy1()" class="button btn">COPY</button -->
</p>



<!------------------COMMENT------------------>
<script>
        const load = document.getElementById('mgf');
	const comment ="DO NOT PLAY THANK-YOU MOVES\n\nWhite 6 forces Black to make a good cut at A, blocking the road between the upper white group and the lower white stone, while making Black ready to attack White 4."; 
	load.value=comment;
	load.style.height= load.scrollHeight +"px";
</script>

<script src="artof9x9.js"></script>




</body>
</html>

```
# A Guide to Mastering 9x9 Go: Tactics and Strategy
Go, an ancient Chinese board game, is renowned for its simplicity and complexity. This guide will delve into the intricacies of 9x9 Go, providing you with the tools to develop your skills and become a proficient player.

### Understanding the Basics
- The Board: A square grid of 9x9 intersections.
- Pieces: Black and white stones.
- Objective: To control more territory on the board than your opponent.

### Key Concepts
- Liberties: The empty spaces surrounding a group of stones.
- Life and Death: A group of stones is considered alive if it can maintain liberties, and dead if it cannot.
- Territory: The area of the board controlled by a player.
- Influence: The potential for a group of stones to expand its territory.

### Basic Tactics
- Capturing: Removing an opponent's group of stones with no liberties.
- Ko: A repeating sequence of captures and recaptures.
- Suicide: Playing a stone in a way that results in your own group's capture.
- Connecting: Joining two groups of stones together.
- Surrounding: Isolating an opponent's group from the rest of the board.

### Strategic Principles
- Control of the Center: The center of the board is a strategic advantage, as it provides access to all areas.
- Thickness: Having a thick group of stones is more secure than a thin one.
- Eyes: A group of stones with two or more empty spaces surrounded by its own stones is considered alive.
- Shape: Good shape allows for flexibility and expansion.
- Timing: Knowing when to attack, defend, or play passively is crucial.

### Advanced Tactics
- Tesuji: A subtle and effective move that often involves sacrificing a stone to gain a larger advantage.
- Ladder: A sequence of moves that can lead to a capture or the creation of an eye.
- Corner Play: Understanding how to control the corners of the board is essential for good strategy.

### Practice and Improvement
- Playing Regularly: The more you play, the better you will become.
- Analyzing Games: Review your games to identify mistakes and learn from your opponents.
- Studying Professional Games: Learn from the best players by analyzing their games.
- Online Resources: There are many online resources available, including Go servers, tutorials, and books.

By understanding these concepts and practicing regularly, you can develop your Go skills and become a formidable opponent. Remember, Go is a game of patience, strategy, and creativity. Enjoy the journey!

> [!Note]
> This is a basic outline of 9x9 Go. For more in-depth knowledge, consider exploring specific tactics and strategies, as well as studying professional games and analyzing your own.

## The Art of 9 x 9 Go: Advanced Strategies
This book is designed for experienced Go players seeking to elevate their game to new heights. We will delve into advanced strategic concepts, tactical subtleties, and endgame techniques that will help you outmaneuver your opponents and achieve victory.

### Part I: Strategic Foundations
- Control of the Center: Beyond the basic principle, explore advanced techniques for controlling the center, such as creating a fortress or using strategic threats.
- Corner Play: Master the intricacies of corner play, including corner kos, corner life, and strategic corner threats.
- Edge Play: Understand the importance of edge control and how to use it to create strategic advantages.
- Influence and Shape: Learn how to maximize your influence on the board and create efficient shapes that support your strategic goals.

### Part II: Tactical Refinements
- Tesuji: Explore a wide range of tesuji, including those involving kos, ladders, and strategic sacrifices.
- Counting Liberties: Master the art of counting liberties accurately, as it is essential for making sound judgments in tactical situations.
- Tactical Patterns: Recognize common tactical patterns and understand how to respond to them effectively.
- Strategic Sacrifices: Learn when and how to make strategic sacrifices to gain a larger advantage.

### Part III: Endgame Mastery
- Endgame Techniques: Study advanced endgame techniques, such as counting points, capturing remaining groups, and securing territory.
- Endgame Reading: Develop the ability to read endgame positions accurately and make optimal decisions.
- Endgame Traps: Learn to recognize and avoid endgame traps set by your opponents.
- Endgame Ethics: Understand the importance of fair play and ethical conduct in endgame situations.

### Part IV: Psychological Warfare
- Reading Your Opponent: Learn how to analyze your opponent's playing style and use that information to your advantage.
- Mental Toughness: Develop the mental fortitude to handle pressure and maintain focus in difficult situations.
- Time Management: Learn how to manage your time effectively, especially in timed games.
- Post-Game Analysis: Analyze your games carefully to identify mistakes and improve your play.

### Advanced Case Studies
- Professional Game Analysis: Analyze professional games in detail, focusing on strategic and tactical concepts.
- Your Own Games: Analyze your own games to identify areas for improvement and apply the strategies and techniques you have learned.

By mastering these advanced concepts, you can elevate your Go game to a new level. Remember, practice is key to improvement. Continue to challenge yourself and enjoy the journey of becoming a truly exceptional Go player.
