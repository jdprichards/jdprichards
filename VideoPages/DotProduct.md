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
The Dot Product of  vectors <em style="color:Red">V</em> and <em style="color:Red">W</em>:
</p>
<p style="font-size:16px">
Put in the form:
</p>

$$ \color{Red}V \color{white}\cdot \color{Red}W $$

<p style="font-size:16px">
Given the vectors:
</p>

$$ \color{Red}V \color{white}= \color{Blue}Vx \color{white}+ \color{Green}Vy \color{white}+ \color{Yellow}Vz$$

$$ \text{ And }$$

$$\color{Red} W\color{white}= \color{Blue}Wx \color{white}+ \color{Green}Wy \color{white}+ \color{Yellow}Wz$$

<br>
<p style="font-size:16px">
The Dot Product of vectors V and W would be calculated as:</p>

$$ \color{Red}V\color{white}\cdot{}\color{Red}W \color{white}= \color{Blue} VxWx \color{white}+  \color{Green}VyWy\color{white}+\color{Yellow}VzWz $$

<em style="font-size:16px;color:purple ">
Important: This value is a scalar so doesn't have a direction like vectors do. Meaning you get a singular value for the answer. Rather than it being split up into X, Y and Z
</em><br>

<p style="font-size:17px">
The stage is using the calculation of the dot product to get the angle between the vectors.<br>
Using the equation:
</p>

$$\color{Red} V\color{white}\cdot{}\color{Red}W = \color{Red}|V||W|\color{orange}\cos{\color{lightBlue}\theta} $$

$\text{Where } \color{lightBlue}\theta \color{white}\text{ is the angle between the vectors}$

$$ \frac{\color{Red} V\color{white}\cdot{}\color{Red}W}{\color{Red}|V||W|} = \color{orange}\cos{\color{lightBlue}\theta} $$

$$ \color{lightBlue}\theta \color{white}=  \color{orange}\arccos{\color{white}\frac{\color{Red}V\color{white}\cdot \color{Red} W}{ \color{Red}|V||W|}} $$

<p style="font-size:18px;color:DarkRed">
Click here to go to my next explainer video about the:
<a href="CrossProduct.html">Cross Product </a>
</p>
