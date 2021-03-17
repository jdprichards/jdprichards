# Cross Product Explained
<script defer>
    // for Anki 2.1
    MathJax.Hub.Config({ TeX: { extensions: ["color.js"] }});
</script>
<script type="text/x-mathjax-config">
    MathJax.Hub.processSectionDelay = 0;
    MathJax.Hub.Config({
        TeX: { extensions: ["color.js"] },
        messageStyle: 'none',
        showProcessingMessages: false,
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

<p style="font-size:16px">
During one of my games concepts lectures there was a general confusion about what is happening in it. So I am going to have a brief cover over it.<br>
</p>

<p style="font-size:14px">
This is my first time doing anything like this so sorry if the quality isn't amazing.
</p>

<p style="font-size:18px">
In this first video I am briefly covering what the cross product is and how I'd start to write it out:
</p>

<p style="font-size:16px">
The idea here is to put the two vectors into a form that easy to see and understand. <br><br>Two vectors here <em>V and W</em> each with their own x, y and z co-ordinate, we're going to find the <em>VxW</em>, remember this is <strong>different</strong> to <em>WxV</em>. Where I have put them in the following form
</p>

$$ \begin{pmatrix}X & Y & Z\\\ Vx & Vy & Vz \\\ Wx & Wy & Wz\end{pmatrix}$$


<iframe width="420" height="315"
src="https://www.youtube.com/embed/dIB3xGbndso" allowfullscreen>
</iframe>

<p style="font-size:18px"><br>
The Second video shows me starting to calculate the cross product. But just the x at the moment:
</p>
<p style="font-size:16px">
The equation to calculate X for the resulting vector is:</p>

$$  \color{Red}VyWz \color{white}- \color{Blue} VzWy$$

<p style="font-size:16px">
You can notice here to calculate the x value you don't need to use <em>Vx or Wx</em> so you can use the table like this.

$$\begin{pmatrix} Y & Z \\\ \color{Red}Vy &  \color{Blue}Vz \\\ \color{Blue}Wy & \color{Red}Wz  \end{pmatrix} $$


<p style="font-size:16px">
You can also notice that <em style="color:red">VyWz</em> directly diagonal from each other when you ignore X and so is <em style="color:blue">VzWy</em> its is from the right to left. So you can x into different parts each going diagonal.<br> </p><em style="font-size:18px; color:slateblue"> Important: the second half is negative: </em>

$$ - \color{Blue} VzWy $$

<p style="font-size:16px">You can see this as because the diagonal is going right to left its therefore minus.
</p>


<iframe width="420" height="315"
src="https://www.youtube.com/embed/z6x4OjVvPmM" allowfullscreen>
</iframe>

<p style="font-size:18px"> <br>The Third video shows me calculating Y similarly to X:</p>

$$ - (\color{Red} VxWz \color{white}- \color{Blue} VzWx\color{white})$$

<p style="font-size:16px">
Again you don't need to use <em>Vy or Wy</em> like the previous section with X, so you can use the table like this.</p>



$$\begin{pmatrix} X & Z \\\ \color{Red}Vx &  \color{Blue}Vz \\\ \color{Blue}Wx & \color{Red}Wz  \end{pmatrix} $$

<p style="font-size:16px">
<em style="color:red">VxWz</em> again are directly diagonal from each other when you ignore Y and so is <em style="fonnt-size:18px;color:blue">VzWx</em> its is from the right to left. So you can x into different parts each going diagonal.</p>
<p style="font-size:18px; color:slateblue">
<em> Important: the second half is negative</em></p>

$$ -(\color{Blue}VzWz\color{white}) $$
<p style="font-size:16px">You can see this as because the diagonal is going right to left its therefore minus.
</p>

<p style="font-size:16px">
With the way I've shown calculating Y:<br></p><em style="color:slateblue;font-size:18px"> Important: You'll want to minus everything in the brackets.</em>
<p style="font-size:16px">I have shown it this way as you can keep the rule for going from top left to bottom right and vice versa
</p>

<iframe width="420" height="315"
src="https://www.youtube.com/embed/Oq04485K2v8" allowfullscreen>
</iframe>

<p style="font-size:18px"> <br>The Forth video shows me calculating Z like both X and Y:</p>

<p style="font-size:16px">
The equation to calculate Y for the resulting vector is:<br></p>

$$\color{Red} VxWy \color{white}- \color{Blue}VyWx $$

<p style="font-size:16px">
Again you don't need to use <em>Vz or Wz</em> like the previous section with X and Y, so you can use the table like this.</p>


$${\begin{pmatrix} X & Y \\\ \color{Red}Vx & \color{Blue}Vy \\\ \color{Blue}Wx & \color{Red}Wy\end{pmatrix}}$$

<p style="font-size:16px">
<em style="color:Red">VxWy</em> again are directly diagonal from each other when you ignore Y and so is <em style="color:Blue">VyWx</em> its is from the right to left. So you can x into different parts each going diagonal.
<br><br>
<em style="color:slateblue;font-size:18px"> Important: the second half is negative:</em></p>

$$(\color{Blue}-VyWx\color{white})$$
<p style="font-size:16px">
You can see this as because the diagonal is going right to left its therefore minus.
</p>

<iframe width="420" height="315"
src="https://www.youtube.com/embed/MkU2XPSFeGA" allowfullscreen>
</iframe>

<p style="font-size:18px"> <br>The Fifth video shows me putting everything together to give the final answer (including the long equation):</p>

<p style="font-size:16px">
Now for the final section. This is simply putting everything you've caculated up here all into one. You've calculated the new X, Y and Z vectors so all you need to do is put them together.
</p>
<p style="font-size:16px">
At the end you get the equation:<br>
</p>

$$+ (\color{Red}VyWz \color{white}- \color{Blue} VzWy\color{white}) \text{ For X}$$ 
$$ - (\color{Red} VxWz \color{white}- \color{Blue} VzWx\color{white}) \text{ For Y}$$
$$+ (\color{Red} VxWy \color{white}- \color{Blue}VyWx\color{white}) \text{ For Z}$$
<p style="font-size:16px">
This is the resulting vector.


</p>
<iframe width="420" height="315"
src="https://www.youtube.com/embed/GojkhIdKIy0" allowfullscreen>
</iframe>

<p style="font-size:18px;color:DarkRed">
Click here to go to my next explainer video about:
<a href="Matrix.html">Matricies </a><br><br>
Or go below to find some questions to test your knowlege.<br>
</p>

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

With ${ V= 4x, 6y, 3z}$ and ${W = 7x, 2y, 2z}$
<br>
${V\times{}W}$
<br>

<button type="button" onclick="ShowAndHide('Answer1a');"> 
Get answer
</button>

<div id="Answer1a" style="display:none">
<p style="font-size:16px">
The answer to question 1a: <br>

${ \text{The answer:}}$

$$ \begin{pmatrix}
    X & Y & Z\\
    4 & 6 & 2\\
    7 & 2 & 2
\end{pmatrix}$$

Remember we have to add the times the same axis together than add them up.<br>


For the X: 

$$ \begin{pmatrix}
    Y & Z\\
    6 & 2\\
    2 & 2
\end{pmatrix}$$

$$[(6\times2)-(2\times2)]X$$
$$[(12)-(4)]X$$
$$ 8X $$

For the Y: 

$$ \begin{pmatrix}
    X & Z\\
    4 & 2\\
    7 & 2
\end{pmatrix}$$

$$-[(4\times2)-(7\times2)]Y$$
$$ -[(8)-(14)]Y$$
$$ -[-6]Y$$
$$ 6Y$$

For the Z: 

$$ \begin{pmatrix}
    X & Y\\
    4 & 6\\
    7 & 2
\end{pmatrix}$$

$$[(4\times2)-(7\times6)]Z$$
$$[(8)-(42)]Z$$
$$-34Z$$

Then you add them all together

$$ 8X + 6Y -34Z $$

So:

$${V\times W = 
\begin{pmatrix}
X & Y & Z \\
8X & 6Y & -34Z
\end{pmatrix}}$$
or just:

$$ V\times W = \begin{pmatrix}8, & 6, &-34\end{pmatrix} $$

This is the vector perpendicular to your vector V and W
</p>
</div>