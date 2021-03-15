# Matrix - Scaling

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
Welcome to my second matrix explainer, this explainer will focus on the scaling on matricies in the X, Y and Z axis. You can check out my previous explainer here about:<br>
<a href="Matrix.html">Matrix Beginner - Adding and Mutiplying</a>
</p>
<br>

<p style="font-size:16px">
Right in this tutorial we are going to be looking over scaling an in game object using a matrix.<br><br>
A matrix can look <em> very </em> confussing to look at so the first thing I'm going to do is try and break it down.</p>
<p style="font-size:18px">
Lets call it matrix M, which is a 4x4 matrix:</p>
<p style="font-size:16px">

It will be in the form: ${M_{\text{Row,Column}}}$

</p>

$$ 
\begin{pmatrix}
&\color{blue}\text{X comp} & \color{green}\text{Y comp} & \color{yellow}\text{Z comp}\\
\color{blue}\text{X-Axis}&M_{1,1} & M_{1,2} & M_{1,3} & M_{1,4}\\
\color{green}\text{Y-Axis}&M_{2,1} & M_{2,2} & M_{2,3} & M_{2,4}\\
\color{yellow}\text{Z-axis}&M_{3,1} & M_{3,2} & M_{3,3} & M_{3,4}\\
\color{red}\text{Pos}&M_{4,1} & M_{4,2} & M_{4,3} & M_{4,4}
\end{pmatrix}
$$

<p style="font-size:16px">
The bottom row or <em style="color:Red">row 4</em>, shows the current position of the object so that is quite easy to seperate from the rest</p>

<p style="font-size:16px">
The final column, or column 4 should just be ignored now.
As it doesn't have much functional use<br>
</p>

<p style="font-size:16px">
Now moving onto actually scaling a model<br>
You can do many different types of scaling, such as only scaling a certain axis, or scaling axis by different amounts, or just scaling the whole model at once. Each of these have changes in the the objects matrix, and I'm going to try and go through them.
</p>
<br>

<p style="font-size:18px; color:blue">
Scaling the X-axis
</p>

<p style="font-size:16px">
The first one will be trying to scale in just the X-Axis, ignoring all the others.
</p>

<p style="font-size:16px">
As I've labled above you only want to focus on the X-axis (the first row). As the others relate to the other axis of the general position of the object. <br><br>
If you mess around with changing the values randomly yourself you'll notice the objects shape will morph and change. <br><br>
The idea of strenching in one axis, you have to increase all the components of that axis, if you don't the object won't stetch properly (but can  look quite  cool).
</p>

$$ 
\begin{pmatrix}
&\color{blue}\text{X comp} & \color{green}\text{Y comp} & \color{yellow}\text{Z comp}\\
\color{blue}\text{X-Axis}&\colorbox{blue}M_\colorbox{blue}{1,1} & \colorbox{blue}M_\colorbox{blue}{1,2} & \colorbox{blue}M_\colorbox{blue}{1,3} & M_{1,4}\\
\color{green}\text{Y-Axis}&M_{2,1} & M_{2,2} & M_{2,3} & M_{2,4}\\
\color{yellow}\text{Z-axis}&M_{3,1} & M_{3,2} & M_{3,3} & M_{3,4}\\
\color{red}\text{Pos}&M_{4,1} & M_{4,2} & M_{4,3} & M_{4,4}
\end{pmatrix}
$$


<p style="font-size:18px; color:blue">
Scaling the Y-axis
</p>

<p style="font-size:16px">
As I've labled above you only want to focus on the X-axis (the first row). As the others relate to the other axis of the general position of the object. <br><br>
If you mess around with changing the values randomly yourself you'll notice the objects shape will morph and change. <br><br>
The idea of strenching in one axis, you have to increase all the components of that axis, if you don't the object won't stetch properly (but can  look quite  cool).
</p>

$$ 
\begin{pmatrix}
&\color{blue}\text{X comp} & \color{green}\text{Y comp} & \color{yellow}\text{Z comp}\\
\color{blue}\text{X-Axis}&M_
{1,1} & M_{1,2} & M_{1,3} & M_{1,4}\\
\color{green}\text{Y-Axis}&M_{2,1} & M_{2,2} & M_{2,3} & M_{2,4}\\
\color{yellow}\text{Z-axis}&M_{3,1} & M_{3,2} & M_{3,3} & M_{3,4}\\
\color{red}\text{Pos}&M_{4,1} & M_{4,2} & M_{4,3} & M_{4,4}
\end{pmatrix}
$$