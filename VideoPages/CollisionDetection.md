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
The idea of collision detection is extremely important, from making games to accurate simulations of the real world. There are a number of different types of collisions. Some basic ones are;
 </p>

<p style="font-size:16px;color:slateblue">
    -Point to sphere<br>
    -Sphere to Sphere<br>
    -Sphere to Box<br>
    -Box to Box
</p>

<p style="font-size:16px">
    The more complex the collision detection the more processing power it takes, to detect if it happens or not.
    <br><br>
    For example: If you have an object with alot of edges e.g Octagons  and higher, you'd have to check to see if each edge has a collision.<br><br> 
    However you can acheive a similar result by assuming the object is spherical and use its radius. Reducing the complexity of the equation and the processing it takes to decide if the collision occurs.
</p>
<br>
<p style="font-size:18px;color:Blue">
    Point to Sphere Collisions:
</p>

$$ \color{red} \text{Point 1 } \color{white} \text{Co-Ordinates(} \color{red} \text{P1}\color{white}\text{): }  \color{Red}P1_{\text{x}}\color{white}+ \color{Red}P1_{\text{y}} \color{white}+ \color{Red}P1_{\text{z}}$$

$$ 
    \color{green} \text{Sphere 1 } \color{white} \text{Co-Ordinates(} \color{green} \text{S1}\color{white}\text{): } 
    \color{green} S1_{\text{x}} \color{white}+ \color{green} S2_{\text{y}} \color{white} + \color{green} S2_{\text{z}} \color{white}\text{ Radius: } \color{green}S2_{\text{Rad}}
$$

$$ 
    \text{Now to find the distance between the spheres where their radia touch:}
 $$

$$ 
    \color{Orange}D \color{white}= \color{green}S1_{\text{Rad}}
$$

$$ 
    \text{To find the current distance between the objects, you use pythagorous}
 $$

 $$ 
    \color{Orange}d \color{white}= \sqrt{(\color{red}P1_{x}\color{white}-\color{green}S1_{x}\color{white})^2+(\color{red}P1_{y}\color{white}-\color{green}S1_{y}\color{white})^2\color{white}+(\color{red}P1_{z}\color{white}-\color{green}S1_{z}\color{white})^2}
$$

<p style="font-size:16px ">
    Collisions occur when the distance between the models is less or equal to the radius of the sphere.
</p>

$$ 
    \color{Orange}d \color{white} \leqslant\color{Orange}D
$$

$$
    \text{Or}
$$

$$ 
    \sqrt{(\color{red}P1_{x}\color{white}-\color{green}S1_{x}\color{white})^2+(\color{red}P1_{y}\color{white}-\color{green}S1_{y}\color{white})^2\color{white}+(\color{red}P1_{z}\color{white}-\color{green}S1_{z}\color{white})^2} \color{white} \leqslant \color{green} S1_{\text{Rad}}
$$


<p style="font-size:18px;color:Blue">
    Sphere to Sphere Collisions:
</p>

$$ 
    \color{red} \text{Sphere 1 } \color{white} \text{Co-Ordinates(} \color{red} \text{S1}\color{white}\text{): }  \color{Red}S1_{\text{x}}\color{white}+ \color{Red}S1_{\text{y}} \color{white}+ \color{Red}S1_{\text{z}} \color{white}\text{ Radius: } \color{Red}S1_{\text{Rad}}
$$

$$ 
    \color{green} \text{Sphere 2 } \color{white} \text{Co-Ordinates(} \color{green} \text{S2}\color{white}\text{): } 
    \color{green} S2_{\text{x}} \color{white}+ \color{green} S2_{\text{y}} \color{white} + \color{green} S2_{\text{z}} \color{white}\text{ Radius: } \color{green}S1_{\text{Rad}}
$$

$$ 
    \text{Now to find the distance between the spheres where their radia touch:} 
$$

$$ 
    \color{Orange}D \color{white}= \color{Red}S1_{\text{Rad}}\color{white}+\color{green}S2_{\text{Rad}}
$$

$$ 
    \text{To find the current distance between the objects, you use pythagorous}
 $$

 $$ 
    \color{Orange}d \color{white}= \sqrt{(\color{red}S1_{x}\color{white}-\color{green}S2_{x}\color{white})^2+(\color{red}S1_{y}\color{white}-\color{green}S2_{y}\color{white})^2\color{white}+(\color{red}S1_{z}\color{white}-\color{green}S2_{z}\color{white})^2}
$$

<p style="font-size:16px ">
    Collisions occur when the distance between the models is less or equal to the radia of the spheres. As they are constant round each sphere.
</p>

$$ 
    \color{Orange}d \color{white} \leqslant\color{Orange}D
$$

$$
    \text{Or}
$$

$$ 
    \sqrt{(\color{red}S1_{x}\color{white}-\color{green}S2_{x}\color{white})^2+(\color{red}S1_{y}\color{white}-\color{green}S2_{y}\color{white})^2\color{white}+(\color{red}S1_{z}\color{white}-\color{green}S2_{z}\color{white})^2} \leqslant \color{red} S1_{\text{Rad}} \color{white} +\color{green} S2_{\text{Rad}} 
$$

<br>

<p style="font-size:18px;color:Blue">
    Sphere to box collision:
</p>
<p style="font-size:16px">
    Sphere to box collision is even more complex than sphere to sphere as you have to keep track of more variables. Such as the individual dimensions of the box. This was just the radius of the sphere
</p>
