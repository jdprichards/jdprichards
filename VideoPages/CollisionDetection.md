# Collision Detection

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
<p style="font-size:18px;color:blue">
Introduction to collisions
</p>

<p style="font-size:17px">
The idea of collision detection is extremely important, from making games to accurate simulations of the real world. There are a number of different types of collisions. Some basic ones are; </p>

<p style="font-size:16px;color:slateblue">-Point to sphere<br>-Sphere to Sphere<br>-Sphere to Box<br>-Box to Box</p>

<p style="font-size:16px">
The more complex the collision detection the more processing power it takes, to detect if it happens or not.<br><br>
For example: If you have an object with alot of edges e.g Octagons  and higher, you'd have to check to see if each edge has a collision.<br><br> However you can acheive a similar result by assuming the object is spherical and use its radius. Reducing the complexity of the equation and the processing it takes to decide if the collision occurs.
</p>

<p style="font-size:18px;color:Blue">
Sphere to Sphere Collisions:
</p>

$$ \color{red} \text{Sphere 1 \color{white} Co-Ordinates( \color{red}S1 \color{white}): } \color{Red}S1_{\text{x}}\color{white}+ \color{Red}S1_{\text{y}} \color{white}+ \color{Red}S1_{\text{z}} \color{white}\text{ Radius: } \color{Red}S1_{\text{Rad}}$$

$$ \text{\color{green} Sphere 2 \color{white} Co-Ordinates( \color{green}S2 \color{white}): } \color{green} S2_{\text{x}} \color{white}+ \color{green} S1_{\text{y}} \color{white} + \color{green} S1_{\text{z}} \color{white}\text{ Radius: } \color{green}S1_{\text{Rad}}$$