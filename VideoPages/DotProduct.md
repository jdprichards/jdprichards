# Dot Product Explained

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

<p style="font-size:18px;color:LightBlue">
Welcome to my Dot product explainer. This is a bit  more complex than my previous explaination about: <a href="NormalizeVectors.html">Normalizing vectors</a>
</p>

<p style="font-size:17px">
In this explainer I am going to show you how to calculate the dot product of two vectors. And give some examples on its uses and show how you would implement it into code.
</p>
<br>
<p style="font-size:18px">
The Dot Product of  vectors V and W:
</p>
<p style="font-size:16px">
Put in the form:
</p>

$$ V \cdot W $$

<p style="font-size:16px">
Given the vectors:
</p>

$$ V = Vx + Vy + Vz$$
$$ \text{ And }$$
$$ W = Wx + Wy +Wz$$
<br>
<p style="font-size:16px">
The Dot Product of vectors V and W would be calculated as:</p>

$$ V\cdot{}W = VxWx+ VyWy+VzWz $$
<em style="font-size:16px;color:purple ">
Important: This value is a scalar so doesn't have a direction like vectors do. Meaning you get a singular value for the answer. Rather than it being split up into X, Y and Z
</em><br>


<p style="font-size:18px;color:DarkRed">
Click here to go to my next explainer video about the:
<a href="CrossProduct.html">Cross Product </a>
</p>
