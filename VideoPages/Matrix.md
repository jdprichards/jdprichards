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
<a href="CrossProduct.html">Normalizing vectors</a>
</p>

<p style="font-size:17px">
In this explainer I am going to go through the addition and mutiplaction of matricies. In later parts I'll go through different transformations. But I'm going to try and keep it basic here.
</p><br>
<p style="font-size:16px">
Lets say you've got a Matrix V with 4 Rows and 4 Columns. It would look something like this:
</p>

$$\begin{pmatrix} 
V_{1,1} & V_{1,2} & V_{1,3} & V_{1,4}\\ 
V_{2,1} & V_{2,2} & V_{2,3} & V_{2,4} \\
V_{3,1} & V_{3,2} & V_{3,3} & V_{3,4} \\
V_{4,1} & V_{4,2} & V_{4,3} & V_{4,4}\end{pmatrix} $$

<em style="font-size:17px;color:purple">
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
</p>

<p style="font-size:18px">
Adding Matricies:</p>

<p style="font-size:16px">
You can add and take matricies together to give a new resultant matrix.</p>

<p style="font-size:17px;color:purple">
Important: You can only add together matricies of the same size (number of columns and rows) </p>

<p style="font-size:16px">
I am going to go through 2 examples. One using 2x2 matricies and another using 3x3 matricies:<p>

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

$$ \begin{pmatrix} 
\color{Red}V_{1,1} & \color{Red}V_{1,2}\\ 
\color{Red}V_{2,1} & \color{Red}V_{2,2}\\
\end{pmatrix} + \begin{pmatrix} 
\color{blue}W_{1,1} &\color{blue} W_{1,2}\\ 
\color{blue}W_{2,1} & \color{blue}W_{2,2} \\
\end{pmatrix}  = \begin{pmatrix} 
\color{Red}V_{1,1} \color{white} + \color{blue}W_{1,1} & \color{red}V_{1,2} \color{white} + \color{blue}W_{1,2}\\ 
\color{red}V_{2,1} \color{white} +\color{blue} W_{2,1}& \color{red}V_{2,2}  \color{white} +\color{blue} \color{red}\color{blue}W_{2,2}\\
\end{pmatrix}$$ 