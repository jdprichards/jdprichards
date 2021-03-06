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

<p style="font-size:17px">
The idea of collision detection is extremely important, from making games to accurate simulations of the real world. There are a number of different types of collisions. Some basic ones are; </p><br>

<p style="font-size:16px;color:slateblue">-Point to sphere<br>-Sphere to Sphere<br>-Sphere to Box<br>-Box to Box</p>

<p style="font-size:16px">
The more complex the collision detection the more processing power it takes, to detect if it happens or not.<br>For example: If you have an object with alot of edges, you'd have to check to see if each edge has a collision.<br> However you can acheive a similar result by assuming the object is spherical and use its radius. Reducing the complexity of the equation and the processing it takes to decide if the collision occurs.
