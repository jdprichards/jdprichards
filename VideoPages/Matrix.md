# Matrix beginner - Addition and Multiplication

<script defer>
    // for Anki 2.1
    MathJax.Hub.Config({ TeX: { extensions: ["color.js"] }});
</script>
<script type="text/x-mathjax-config">
    MathJax.Hub.processSectionDelay = 0;
    MathJax.Hub.Config({
        TeX: { extensions: ["color.js"] },
        messageStyle: 'none',
        showProcessingMesSsages: false,
        tex2jax: {
            inlineMath: [ ['$','$'], ['\\(','\\)'] ],
            displayMath: [ ['$$','$$'], ['\\[','\\]'] ],
            processEscapes: true
        }
        });
</script>
<script type="text/javascript">
    (function () {
        if (typeof MathJax === "undefined") {
            var script = document.createElement('script');
            script.type = 'text/javascript';
            script.src = 'https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.1/MathJax.js?config=TeX-MML-AM_CHTML';
            document.body.appendChild(script);
        }
    })();
</script>

<p style="font-size:18px;color:LightBlue">
Welcome to my first matrix explainer, I'll probably do a few explainers about this due to how complex it is. My previous explainer is on corss product at:
<a href="CrossProduct.html">Cross Product</a>
</p>

<p style="font-size:17px">
In this explainer I am going to go through the addition and mutiplaction of matricies. In later parts I'll go through different transformations. But I'm going to try and keep it basic here.<br><br> Representing Matricies:
</p><br>
<p style="font-size:16px">
Lets say you've got a Matrix V with 4 Rows and 4 Columns. It would look something like this:
</p>

$$\begin{pmatrix} 
V_{1,1} & V_{1,2} & V_{1,3} & V_{1,4}\\ 
V_{2,1} & V_{2,2} & V_{2,3} & V_{2,4} \\
V_{3,1} & V_{3,2} & V_{3,3} & V_{3,4} \\
V_{4,1} & V_{4,2} & V_{4,3} & V_{4,4}\end{pmatrix} $$

<em style="font-size:17px;color:slateblue">
Important: Matricies start at 1. But if you want to show them as arrays you'll want to use 0 instead. With the subscript first value showing the Row and the second the column: </em>


${\color{white}V_{row, column}}$




<br>

<p style="font-size:16px">
Matricies can vary in length and width, such like looking like this:
</p>

$$\begin{pmatrix} 
V_{1,1} & V_{1,2} & V_{1,3} & V_{1,4}\\ 
V_{2,1} & V_{2,2} & V_{2,3} & V_{2,4} \\
V_{3,1} & V_{3,2} & V_{3,3} & V_{3,4} \\
V_{4,1} & V_{4,2} & V_{4,3} & V_{4,4}\end{pmatrix} \text{or} \begin{pmatrix} 
V_{1,1} & V_{1,2} & V_{1,3}\\ 
V_{2,1} & V_{2,2} & V_{2,3} \\
V_{3,1} & V_{3,2} & V_{3,3} \\
\end{pmatrix} \text{or} \begin{pmatrix} 
V_{1,1} & V_{1,2} \\ 
V_{2,1} & V_{2,2} \end{pmatrix}$$

<p style="font-size:16px">
Being 4x4, 3x3 and 2x2 Matricies respectively.
</p><br>

<p style="font-size:18px">
Adding Matricies:</p>

<p style="font-size:16px">
You can add and take matricies together to give a new resultant matrix.</p>

<p style="font-size:17px;color:slateblue">
Important: You can only add together matricies of the same size (number of columns and rows) </p>

<p style="font-size:16px">
I am going to go through 2 examples. One using 2x2 matricies and another using 3x3 matricies:<p><br>

<em style="font-size:17px">
3 by 3:</em>

$$ \begin{pmatrix} 
\color{Red}V_{1,1} & \color{Red}V_{1,2} & \color{Red}V_{1,3}\\ 
\color{Red}V_{2,1} & \color{Red}V_{2,2} & \color{Red}V_{2,3} \\
\color{Red}V_{3,1} & \color{Red}V_{3,2} & \color{Red}V_{3,3} \\
\end{pmatrix} + \begin{pmatrix} 
\color{blue}W_{1,1} &\color{blue} W_{1,2} & \color{blue}W_{1,3}\\ 
\color{blue}W_{2,1} & \color{blue}W_{2,2} & \color{blue}W_{2,3} \\
\color{blue}W_{3,1} & \color{blue}W_{3,2} & \color{blue}W_{3,3} \\
\end{pmatrix}  = \begin{pmatrix} 
\color{Red}V_{1,1} \color{white} + \color{blue}W_{1,1} & \color{red}V_{1,2} \color{white} + \color{blue}W_{1,2} & \color{red}V_{1,3}\color{white} +\color{blue}W_{1,3}\\ 
\color{red}V_{2,1} \color{white} +\color{blue} W_{2,1}& \color{red}V_{2,2}  \color{white} +\color{blue} \color{red}\color{blue}W_{2,2}& \color{Red}V_{2,3}\color{white} + \color{blue}W_{2,3}\\
\color{Red}V_{3,1}\color{white} + \color{blue}W_{3,1}& \color{red}V_{3,2}\color{white} + \color{Blue}W_{3,2} & \color{Red}V_{3,3}\color{white} + \color{blue}W_{3,3}\\
\end{pmatrix}  $$ 

<em style="font-size:17px">
2 by 2:</em>


$$ \begin{pmatrix} 
\color{Red}V_{1,1} & \color{Red}V_{1,2}\\ 
\color{Red}V_{2,1} & \color{Red}V_{2,2}\\
\end{pmatrix} + \begin{pmatrix} 
\color{blue}W_{1,1} &\color{blue} W_{1,2}\\ 
\color{blue}W_{2,1} & \color{blue}W_{2,2} 
\end{pmatrix}  = \begin{pmatrix} 
\color{Red}V_{1,1} \color{white} + \color{blue}W_{1,1} & \color{red}V_{1,2} \color{white} + \color{blue}W_{1,2}\\ 
\color{red}V_{2,1} \color{white} +\color{blue} W_{2,1}& \color{red}V_{2,2}  \color{white} +\color{blue} \color{red}\color{blue}W_{2,2}
\end{pmatrix}$$ 

<p style="font-size:16px">

As you can see from above when adding two matricies together you add the same element from the individual matricies together such as ${\color{Red}V_{1,1} \color{white} +\color{blue}W_{1,1}}$ and is the same for each value for the new matrix
</p>
<br>
<p style="font-size:18px">
Mutiplying Matricies:
</p>

<p style="font-size:16px">
You can mutiply and divide two matricies together to give a new matrix, similar to how we did the addition.</p>

<em style="font-size:17px;color:slateblue">
Important: You can only mutiply two vectors when the number of columns in V = the number of rows in W.<br>
or rows A = columns B, notation depending.</em>
<p style="font-size:16px">
For example:<br>
<em  style="color:Red">
V </em> being a 2x3 Matrix and <em style="color:blue"> W </em> being a 3x2 matrix.
</p>


$$ \color{red}V \color{white} \color{blue}W \color{white}$$

$$\text{When } \color{Red}V \color{white}=  \begin{pmatrix} 
\color{red} V_{1,1} &\color{red} V_{1,2} & \color{red} V_{1,3} \\
\color{red} V_{2,1} & \color{red}  V_{2,2} & \color{red} V_{2,3} \\
\end{pmatrix} \text{And } \color{blue}W \color{white} =\begin{pmatrix} 
\color{blue}W_{1,1} & \color{blue}W_{1,2} \\
\color{blue}W_{2,1} & \color{blue}W_{2,2} \\
\color{blue}W_{3,1} & \color{blue}W_{3,2}
\end{pmatrix}$$


$$ \begin{pmatrix} 
\color{red} V_{1,1} &\color{red} V_{1,2} & \color{red} V_{1,3} \\
\color{red} V_{2,1} & \color{red}  V_{2,2} & \color{red} V_{2,3} \\
\end{pmatrix} \begin{pmatrix} 
\color{blue}W_{1,1} & \color{blue}W_{1,2} \\
\color{blue}W_{2,1} & \color{blue}W_{2,2} \\
\color{blue}W_{3,1} & \color{blue}W_{3,2}
\end{pmatrix} $$

 <p style="font-size:16px">
 So that the height of <em style="color:Red"> V </em> matches the width of <em style="color:blue"> W</em><br> This means that mutiplying two 3x3 matrixcies or 4x4 will also work (and is used alot)</p>
<br>
 <p style="font-size:17px">
 Now what would the resultant matrix look like?</p>


$$ \begin{pmatrix} 
(\color{Red}V_{1,1} \color{white}\times \color{blue}W_{1,1}\color{white}) + (\color{Red}V_{1,2} \color{white}\times \color{blue}W_{2,1}\color{white}) + (\color{Red}V_{1,3} \color{white}\times \color{blue}W_{3,1} \color{white})& (\color{red}V_{1,1} \color{white}\times\color{blue} W_{1,2} \color{white} )+ (\color{red}V_{1,2} \color{white}\times \color{blue}W_{2,2} \color{white} )+ (\color{red} V_{1,3} \color{white}\times \color{blue} W_{3,2} \color{white}) \\
(\color{red} V_{2,1} \color{white}\times \color{blue} W_{1,1}  \color{white})+(\color{red} V_{2,2} \color{white}\times\color{blue} W_{2,1}\color{white} )+  (\color{red} V_{2,3} \color{white}\times \color{blue}W_{3,1}\color{white}) & (\color{red}V_{2,1} \color{white}\times \color{blue}
W_{1,2}\color{white} )+ (\color{Red} V_{2,2}\color{white} \times \color{blue} W_{2,2} \color{white})+ (\color{red}V_{2,3} \color{white}\times \color{blue} W_{3,2} \color{white})\end{pmatrix}$$

<br>
<p style="font-size:17px">
As you can see here the <b style = "color:slateblue">resultant matrix </b> has been reduced to be a <b style="color:slateblue">2x2 matrix</b>. This is because it uses the height of <em style="color:Red"> V </em> and the width of <em style="color:blue"> W.</em> so if <em style="color:red">V </em> and <em style="color:blue"> W</em> were swapped round it would be a <b style="color:slateblue"> 3x3 Matrix </b><br>You can  recognise these as being the dot product</p>
<p style="font-size:16px">

For the first value in the matrix Lets call it Matrix
${ \color{Green}X }$ so:<br>

$${\begin{pmatrix} \color{green}X_{1,1} & \color{green}X_{1,2} \\ \color{green}X_{2,1} & \color{green}X_{2,2} \end{pmatrix}}$$

<br> ${\color{green}X_{1,1} \color{white}= (\color{orange}V_{1,1} \color{white}\times \color{purple}W_{1,1}\color{white}) + (\color{orange}V_{1,2} \color{white}\times \color{purple}W_{2,1}\color{white}) + (\color{orange}V_{1,3} \color{white}\times \color{purple}W_{3,1} \color{white})}$

$$ \begin{pmatrix} 
\color{orange} V_{1,1} &\color{red} V_{1,2} & \color{red} V_{1,3} \\
\color{red} V_{2,1} & \color{red}  V_{2,2} & \color{red} V_{2,3} \\
\end{pmatrix}  \begin{pmatrix}  
\color{purple}W_{1,1} & \color{blue}W_{1,2} \\
\color{blue}W_{2,1} & \color{blue}W_{2,2} \\
\color{blue}W_{3,1} & \color{blue}W_{3,2}
\end{pmatrix}\text{And}  \begin{pmatrix} 
\color{red} V_{1,1} &\color{orange} V_{1,2} & \color{red} V_{1,3} \\
\color{red} V_{2,1} & \color{red}  V_{2,2} & \color{red} V_{2,3} \\
\end{pmatrix} \begin{pmatrix} 
\color{blue}W_{1,1} & \color{blue}W_{1,2} \\
\color{purple}W_{2,1} & \color{blue}W_{2,2} \\
\color{blue}W_{3,1} & \color{blue}W_{3,2}
\end{pmatrix} $$
$$\text{And}
\begin{pmatrix} 
\color{red} V_{1,1} &\color{red} V_{1,2} & \color{orange} V_{1,3} \\
\color{red} V_{2,1} & \color{red}  V_{2,2} & \color{red} V_{2,3} \\
\end{pmatrix} \begin{pmatrix} 
\color{blue}W_{1,1} & \color{blue}W_{1,2} \\
\color{blue}W_{2,1} & \color{blue}W_{2,2} \\
\color{purple}W_{3,1} & \color{blue}W_{3,2}
\end{pmatrix}$$
<br>

You can see a common theme going along here: For ${\color{green}X_{1,1}}$ you can see that the only values used in ${\color{red}V}$ is in the first row ${\color{red}V_{1,x}}$ where the subscript ${\color{Red}x}$ shows the column. And the only values used in ${\color{blue}W}$ is the first column ${\color{blue}W_{Y,1}}$ where ${\color{blue}Y}$ shows the row being used. Lets follow this trend  for the next ${\color{green}X}$ value:
${\color{green}X_{2,1}}$:<br> <br>

${\color{green}X_{2,1} \color{white}= (\color{orange}V_{2,1} \color{white}\times \color{purple}W_{1,1}\color{white}) + (\color{orange}V_{2,2} \color{white}\times \color{purple}W_{2,1}\color{white}) + (\color{orange}V_{2,3} \color{white}\times \color{purple}W_{3,1} \color{white})}$ <br><br>


$$ \begin{pmatrix} 
\color{red} V_{1,1} &\color{red} V_{1,2} & \color{red} V_{1,3} \\
\color{orange} V_{2,1} & \color{red}  V_{2,2} & \color{red} V_{2,3} \\
\end{pmatrix}  \begin{pmatrix}  
\color{purple}W_{1,1} & \color{blue}W_{1,2} \\
\color{blue}W_{2,1} & \color{blue}W_{2,2} \\
\color{blue}W_{3,1} & \color{blue}W_{3,2}
\end{pmatrix}\text{And}  \begin{pmatrix} 
\color{red} V_{1,1} &\color{red} V_{1,2} & \color{red} V_{1,3} \\
\color{red} V_{2,1} & \color{orange}  V_{2,2} & \color{red} V_{2,3} \\
\end{pmatrix} \begin{pmatrix} 
\color{blue}W_{1,1} & \color{blue}W_{1,2} \\
\color{purple}W_{2,1} & \color{blue}W_{2,2} \\
\color{blue}W_{3,1} & \color{blue}W_{3,2}
\end{pmatrix} $$
$$\text{And}
\begin{pmatrix} 
\color{red} V_{1,1} &\color{red} V_{1,2} & \color{red} V_{1,3} \\
\color{red} V_{2,1} & \color{red}  V_{2,2} & \color{orange} V_{2,3} \\
\end{pmatrix} \begin{pmatrix} 
\color{blue}W_{1,1} & \color{blue}W_{1,2} \\
\color{blue}W_{2,1} & \color{blue}W_{2,2} \\
\color{purple}W_{3,1} & \color{blue}W_{3,2}
\end{pmatrix}$$
<br>

For ${\color{green}X_{2,1}}$ you can see that the only values used in ${\color{red}V}$ is in the second row ${\color{red}V_{2,x}}$ where the subscript ${\color{Red}x}$ shows the column. And the only values used in ${\color{blue}W}$ is the first column ${\color{blue}W_{Y,1}}$ where ${\color{blue}Y}$ shows the row being used.

$${\begin{pmatrix} \color{green}X_{1,1} & \color{green}X_{1,2} \\ \color{green}X_{2,1} & \color{green}X_{2,2} \end{pmatrix}}$$
Now when you look a this you can see that the first Value in the subscript ${\color{green}X_{\text{row},\text{column}}}$ relates to the row of ${\color{Red}V}$ being used and the column of ${\color{blue}W}$ being used This gets more complex as you use larger matricies so we get the help of computers, although its always useful to be able to do smaller ones such as 2x2 and 3x3 by hand. But it can get quite overwelming when you face 4x4 matricies or higher, you'll want to keep an eye out for making basic calculation errors.
</p><br>
<p style="font-size:18px;color:DarkRed">
Click here to go to my next explainer video about the:
<a href="MatrixScale.html">Scaling Matricies </a><br>
Or go below to find some questions to test your knowlege.<br>
</p>
<br>

<script>
function ShowAndHide(elementID)
{
    var element = document.getElementById(elementID)
    if (element.style.display === "none")
    {
        element.style.display = "block";
    }
    else
    {
        element.style.display="none";
    }
}
</script>

<p style ="font-size:16px">
Question 1:<br>
With the two matricies 

$$
V  = \begin{pmatrix} 
4 & 2 & 4 \\
6 & 3 & 9 \\
2 & 4 & 4
\end{pmatrix} \text{ And }
W = \begin{pmatrix} 
3 & 6 & 1 \\
2 & 3 & 2 \\
7 & 4 & 8
\end{pmatrix}
$$

1a. Find<br>
${V+W}$
</p>
<button type="button" onclick="ShowAndHide('Answer1a');"> 
Get answer
</button>

<div id="Answer1a" style="display:none">
<p style="font-size:16px">

$$
V+W  = \begin{pmatrix} 
4+3 & 2+6 & 4+1 \\
6+2 & 3+3 & 9+2 \\
2+7 & 4+4 & 4+8
\end{pmatrix}
$$

$$
V+W  = \begin{pmatrix} 
7 & 8 & 5 \\
8 & 6 & 11 \\
9 & 8 & 12
\end{pmatrix}
$$
</p>
</div>
<p style ="font-size:16px">
1b. Find<br>

${VW}$
<br>
<em>
you might want a calculator for mutiplying matricies, its very easy to  make a simple calculation error.
</em>
</p>
<button type="button" onclick="ShowAndHide('Answer1b');"> 
Get answer
</button>

<div id="Answer1b" style="display:none">
<p style="font-size:16px">

$$ VW = 
\begin{pmatrix}
(4 \times 3) + (2 \times 2) + (4 \times 7) & (4 \times 6) + (2 \times 3) + (4 \times 4) & (4 \times 1) + (2 \times 2) + (4 \times 8) \\
(6 \times 3) + (3 \times 2) + (9 \times 7) & (6 \times 6) + (3 \times 3) + (9 \times 4) & (6 \times 1) + (3 \times 2) + (9 \times 8) \\ 
(2 \times 3) + (4 \times 2) + (4 \times 7) & (2 \times 6) + (4 \times 3) + (4 \times 4) & (2 \times 1) + (4  \times 2) + (4 \times 8) 
\end{pmatrix}
$$

$$
VW = 
\begin{pmatrix}
12 + 4 + 8 & 24 + 6 + 16 & 4 + 4 + 32 \\
18 + 6 + 63 & 36 + 9 + 36 & 6 + 6 + 72 \\
6 + 8 + 28 & 12 + 12 + 16 & 2 + 8 +  32
\end{pmatrix}
$$

$$
VW =
\begin{pmatrix}
44 & 46 & 40 \\
87 & 81 & 84 \\
42 & 40 & 42
\end{pmatrix}
$$
</p>
</div>

<p style ="font-size:16px">
Question 2:<br>
With the two matricies 

$$
V  = \begin{pmatrix} 
2 & 5\\
6 & 11\\
\end{pmatrix} \text{ And }
W = \begin{pmatrix} 
3 & 4\\
7 & 2\\
\end{pmatrix}
$$
<p style ="font-size:16px">
2a. Find<br>

${V+W}$
</p>
<br>
<button type="button" onclick="ShowAndHide('Answer2a');"> 
Get answer
</button>

<div id="Answer2a" style="display:none">
<p style="font-size:16px">

$$\begin{pmatrix} 
5 & 9\\ 
13 & 13
\end{pmatrix}$$
</p>
</div>
<p style ="font-size:16px">
2b. Find<br>

${VW}$
</p>
<button type="button" onclick="ShowAndHide('Answer2b');"> 
Get answer
</button>

<div id="Answer2b" style="display:none">
<p style="font-size:16px">

$$\begin{pmatrix} 
41 & 19\\ 
95 & 46
\end{pmatrix}$$

</p>
</div>
<p style ="font-size:16px">
Question 3:<br>
With the two matricies 

$$
V  = \begin{pmatrix} 
8 & 3 & 7 \\
6 & 1 & 2 \\
\end{pmatrix} 
\text{ And }
W = \begin{pmatrix} 
9 & 7\\
5 & 4\\
2 & 7
\end{pmatrix}
$$
</p>
<p style ="font-size:16px">
3a. Find<br>

${V+W}$
</p>
<button type="button" onclick="ShowAndHide('Answer3a');"> 
Get answer
</button>

<div id="Answer3a" style="display:none">
<p style="font-size:16px">

This is not possible
</p>
</div>
<p style ="font-size:16px">
3b. Find<br>

${VW}$
</p>

<button type="button" onclick="ShowAndHide('Answer3b');"> 
Get answer
</button>

<div id="Answer3b" style="display:none">
<p style="font-size:16px">

$$\begin{pmatrix} 
101 & 117\\ 
63 & 60
\end{pmatrix}$$

</p>
</div>