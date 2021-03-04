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
Important: Matricies start at 1, instead of 0 as arrays. With the first value showing the Row and the second the column.
</em>

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
Important: You can only mutiply two vectors when the number of rows of one equals the number of columns in the other and the same vise versa.</em>
<p style="font-size:16px">
For example:<br>
<em  style="color:Red">
V </em> being a 2x3 Matrix and <em style="color:blue"> W </em> being a 3x2 matrix.
</p>

$$ \color{Red}V \color{white}=  \begin{pmatrix} 
\color{red} V_{1,1} &\color{red} V_{1,2} & \color{red} V_{1,3} \\
\color{red} V_{2,1} & \color{red}  V_{2,2} & \color{red} V_{2,3} \\
\end{pmatrix} \text{And } \color{blue}W \color{white} =\begin{pmatrix} 
\color{blue}W_{1,1} & \color{blue}W_{1,2} \\
\color{blue}W_{2,1} & \color{blue}W_{2,2} \\
\color{blue}W_{3,1} & \color{blue}W_{3,2}
\end{pmatrix}$$

$$ \color{red}V \color{white}\cdot \color{blue}W$$

$$ \begin{pmatrix} 
\color{red} V_{1,1} &\color{red} V_{1,2} & \color{red} V_{1,3} \\
\color{red} V_{2,1} & \color{red}  V_{2,2} & \color{red} V_{2,3} \\
\end{pmatrix} \cdot  \begin{pmatrix} 
\color{blue}W_{1,1} & \color{blue}W_{1,2} \\
\color{blue}W_{2,1} & \color{blue}W_{2,2} \\
\color{blue}W_{3,1} & \color{blue}W_{3,2}
\end{pmatrix} $$

 <p style="font-size:16px">
 So that the height of <em style="color:Red"> V </em> matches the width of <em style="color:blue"> W</em><br> This means that mutiplying two 3x3 matrixcies or 4x4 will also work (and is used alot)</p>
<br>
 <p style="font-size:17px">
 Now what would the resultant matrix look like?</p>

$$ \color{Red}V\color{white}\cdot\color{blue} W$$
$$ \begin{pmatrix} 
\color{red} V_{1,1} &\color{red} V_{1,2} & \color{red} V_{1,3} \\
\color{red} V_{2,1} & \color{red}  V_{2,2} & \color{red} V_{2,3} \\
\end{pmatrix} \cdot  \begin{pmatrix} 
\color{blue}W_{1,1} & \color{blue}W_{1,2} \\
\color{blue}W_{2,1} & \color{blue}W_{2,2} \\
\color{blue}W_{3,1} & \color{blue}W_{3,2}
\end{pmatrix} $$

$$ \begin{pmatrix} 
(\color{Red}V_{1,1} \color{white}\times \color{blue}W_{1,1}\color{white}) + (\color{Red}V_{1,2} \color{white}\times \color{blue}W_{2,1}\color{white}) + (\color{Red}V_{1,3} \color{white}\times \color{blue}W_{3,1} \color{white})& (\color{red}V_{1,1} \color{white}\times\color{blue} W_{1,2} \color{white} )+ (\color{red}V_{1,2} \color{white}\times \color{blue}W_{2,2} \color{white} )+ (\color{red} V_{1,3} \color{white}\times \color{blue} W_{3,2} \color{white}) \\
(\color{red} V_{2,1} \color{white}\times \color{blue} W_{1,1}  \color{white})+(\color{red} V_{2,2} \color{white}\times\color{blue} W_{2,1}\color{white} )+  (\color{red} V_{2,3} \color{white}\times \color{blue}W_{3,1}\color{white}) & (\color{red}V_{2,1} \color{white}\times \color{blue}
W_{1,2}\color{white} )+ (\color{Red} V_{2,2}\color{white} \times \color{blue} W_{2,2} \color{white})+ (\color{red}V_{2,3} \color{white}\times \color{blue} W_{3,2} \color{white})\end{pmatrix}$$

<br>
<p style="font-size:17px">
As you can see here the <b style = "color:slateblue">resultant matrix </b> has been reduced to be a <b style="color:slateblue">2x2 matrix</b>. This is because it uses the height of <em style="color:Red"> V </em> and the width of <em style="color:blue"> W.</em> so if <em style="color:red">V </em> and <em style="color:blue"> W</em> were swapped round it would be a <b style="color:slateblue"> 3x3 Matrix </b></p>
<p style="font-size:16px">

For the first value in the matrix Lets call it Matrix
${ \color{Green}X }$ so:<br>

$${\begin{pmatrix} \color{green}X_{1,1} & \color{green}X_{1,2} \\ \color{green}X_{2,1} & \color{green}X_{2,2} \end{pmatrix}}$$

<br> ${\color{green}X_{1,1} \color{white}= (\color{orange}V_{1,1} \color{white}\times \color{purple}W_{1,1}\color{white}) + (\color{orange}V_{1,2} \color{white}\times \color{purple}W_{2,1}\color{white}) + (\color{orange}V_{1,3} \color{white}\times \color{purple}W_{3,1} \color{white})}$

$$ \begin{pmatrix} 
\color{orange} V_{1,1} &\color{red} V_{1,2} & \color{red} V_{1,3} \\
\color{red} V_{2,1} & \color{red}  V_{2,2} & \color{red} V_{2,3} \\
\end{pmatrix}  \cdot\begin{pmatrix}  
\color{purple}W_{1,1} & \color{blue}W_{1,2} \\
\color{blue}W_{2,1} & \color{blue}W_{2,2} \\
\color{blue}W_{3,1} & \color{blue}W_{3,2}
\end{pmatrix}\text{And}  \begin{pmatrix} 
\color{red} V_{1,1} &\color{orange} V_{1,2} & \color{red} V_{1,3} \\
\color{red} V_{2,1} & \color{red}  V_{2,2} & \color{red} V_{2,3} \\
\end{pmatrix}\cdot \begin{pmatrix} 
\color{blue}W_{1,1} & \color{blue}W_{1,2} \\
\color{purple}W_{2,1} & \color{blue}W_{2,2} \\
\color{blue}W_{3,1} & \color{blue}W_{3,2}
\end{pmatrix} $$
$$\text{And}
\begin{pmatrix} 
\color{red} V_{1,1} &\color{red} V_{1,2} & \color{orange} V_{1,3} \\
\color{red} V_{2,1} & \color{red}  V_{2,2} & \color{red} V_{2,3} \\
\end{pmatrix} \cdot\begin{pmatrix} 
\color{blue}W_{1,1} & \color{blue}W_{1,2} \\
\color{blue}W_{2,1} & \color{blue}W_{2,2} \\
\color{purple}W_{3,1} & \color{blue}W_{3,2}
\end{pmatrix}$$
<br>

You can see a common theme going along here: For ${\color{green}X_{1,1}}$ you can see that the only values used in ${\color{red}V}$ is in the first row ${\color{red}V_{1,x}}$ where the subscript ${\color{Red}X}$ shows the column. And the only values used in ${\color{blue}W}$ is the first column ${\color{blue}W_{Y,1}}$ where ${\color{blue}Y}$ shows the row being used. Lets follow this trend  for the next ${\color{green}X}$ value:
${\color{green}X_{2,1}}$:<br> <br>

${\color{green}X_{2,1} \color{white}= (\color{orange}V_{2,1} \color{white}\times \color{purple}W_{1,1}\color{white}) + (\color{orange}V_{2,2} \color{white}\times \color{purple}W_{2,1}\color{white}) + (\color{orange}V_{2,3} \color{white}\times \color{purple}W_{3,1} \color{white})}$ <br><br>


$$ \begin{pmatrix} 
\color{red} V_{1,1} &\color{red} V_{1,2} & \color{red} V_{1,3} \\
\color{orange} V_{2,1} & \color{red}  V_{2,2} & \color{red} V_{2,3} \\
\end{pmatrix}  \cdot\begin{pmatrix}  
\color{purple}W_{1,1} & \color{blue}W_{1,2} \\
\color{blue}W_{2,1} & \color{blue}W_{2,2} \\
\color{blue}W_{3,1} & \color{blue}W_{3,2}
\end{pmatrix}\text{And}  \begin{pmatrix} 
\color{red} V_{1,1} &\color{red} V_{1,2} & \color{red} V_{1,3} \\
\color{red} V_{2,1} & \color{orange}  V_{2,2} & \color{red} V_{2,3} \\
\end{pmatrix}\cdot \begin{pmatrix} 
\color{blue}W_{1,1} & \color{blue}W_{1,2} \\
\color{purple}W_{2,1} & \color{blue}W_{2,2} \\
\color{blue}W_{3,1} & \color{blue}W_{3,2}
\end{pmatrix} $$
$$\text{And}
\begin{pmatrix} 
\color{red} V_{1,1} &\color{red} V_{1,2} & \color{red} V_{1,3} \\
\color{red} V_{2,1} & \color{red}  V_{2,2} & \color{orange} V_{2,3} \\
\end{pmatrix} \cdot\begin{pmatrix} 
\color{blue}W_{1,1} & \color{blue}W_{1,2} \\
\color{blue}W_{2,1} & \color{blue}W_{2,2} \\
\color{purple}W_{3,1} & \color{blue}W_{3,2}
\end{pmatrix}$$
<br>

For ${\color{green}X_{2,1}}$ you can see that the only values used in ${\color{red}V}$ is in the second row ${\color{red}V_{2,x}}$ where the subscript ${\color{Red}X}$ shows the column. And the only values used in ${\color{blue}W}$ is the first column ${\color{blue}W_{Y,1}}$ where ${\color{blue}Y}$ shows the row being used.

$${\begin{pmatrix} \color{green}X_{1,1} & \color{green}X_{1,2} \\ \color{green}X_{2,1} & \color{green}X_{2,2} \end{pmatrix}}$$
Now when you look a this you can see that the first Value in the subscript ${\color{green}X_{\text{row},\text{column}}}$ relates to the row of ${\color{Red}V}$ being used and the column of ${\color{blue}W}$ being used.
</p><br>
<p style="font-size:18px;color:DarkRed">
Click here to go to my next explainer video about the:
<a href="MatrixScale.html">Scaling Matricies </a>
</p>