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
<p style="font-size:15px">
Lets say you've got a Matrix V with 4 Rows and 4 Columns. It would look something like this:
</p>

$$\begin{pmatrix} 
V_{11} & V_{12} & V_{13} & V_{14}\\ 
V_{21} & V_{22} & V_{23} & V_{24} \\
V_{31} & V_{32} & V_{33} & V_{34} \\
V_{41} & V_{42} & V_{43} & V_{44}\end{pmatrix} $$

<em style="font-size:15px;color:purple">
Important Matricies  start at 1, instead of 0 as arrays.
</em>