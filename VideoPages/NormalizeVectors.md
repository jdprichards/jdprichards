# Normalizing Vectors Explained
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

<p style="font-size:18px; color:lightBlue">
Welcome to my explanation on normalizing vectors. This is a fairly easy topic so won't be as long as my other explanations
</p><br>

<p style="font-size:17px">
In this first video I briefly go over what normalizing a vector is:</p>

<p style="font-size:16px">
The idea is that you have a vector <em style ="font-size:16;color:Red">V</em> that has components <em style ="color:Blue">Vx</em>, <em style ="color:Green">Vy</em> and <em style ="color:Yellow">Vz</em> to it.
When you normalize a vector you reduce the length of <em style="color:Red">V</em> to equal 1. This allows you to seperate the direction from the magitude.</p>


<iframe width="420" height="315"
src="https://www.youtube.com/embed/zNd_rduGIvA" allowfullscreen>
</iframe>

<br>
<p style="font-size:18px">
In this second video I go over how you normalize a vector in general form:
</p>

<p style="font-size:16px">
So I have a vector
</p>

$$ \color{Red} |V| \color{white} = \color{Blue} Vx \color{white}  + \color{Green}  Vy \color{white} + \color{Yellow}Vz $$

<p style="font-size:17px">
If you are only using 2 axis for example not using the <em style="color:Green">Y</em> Axis you just remove it from the equation.<br><br>The normalized V is:</p>

$$\color{Red} V \over{ \color{Red}\hat{V}} $$

<p style="font-size:18px">
Which is the vector over its magnitude given by:</p>

$$ \color{Red} |V| \color{White}= \sqrt{(\color{Blue}Vx^2 \color{white} + \color{Green} Vy^2 \color{white}+ \color{Yellow} Vz^2 \color{white})} $$

$$ \color{Red}\hat{V}\color{white} = \color{Blue}{Vx\over |V|} \color{white} + \color{Green} {Vy\over |V|} \color{white} + \color{Yellow}{Vz\over|V|}$$

<p style="font-size:16px">
Something that is worthy to note is that to magnitude:</p>

$$ \color{Red}\hat{|V|} \color{white}= \color{Red} 1 $$

<p style="font-size:15px">You can always check that the magnitude of your answer = 1 to confirm that it is a normalize vector.</p><br><br>

<iframe width="420" height="315"
src="https://www.youtube.com/embed/TGwAdduyPQk" allowfullscreen>
</iframe>

<br>
<p style="font-size:16px">
In this last video I go over how you normalize a vector using values form:
</p>
<p style="font-size:16px"> I am going to walkthrough how to calculate a normalized vector where:<br>

$$ \color{Blue} Vx = 5 $$
$$ \color{Green} Vy = 7 $$
$$ \color{Yellow} Vz = 4 $$
Giving:

$$ \color{Red}V \color{white}=\color{Blue} 5x \color{white} + \color{Green} 7y  \color{White}+  \color{Yellow}4z$$


 <p style="font-size:16px"> First the calculate <B style="color:Red">|V|</B> using the equation shown above:<br>

 $$ \color{Red} |V| \color{White}= \sqrt{(\color{Blue}5^2 \color{white} + \color{Green} 7^2 \color{white}+ \color{Yellow} 4^2 \color{white})} $$

 $$ \color{Red} |V| \color{White}= \sqrt{(\color{Blue}25 \color{white} + \color{Green} 49 \color{white}+ \color{Yellow} 16 \color{white})} =\sqrt{\color{Red} 90} $$

$$ \color{Red}\hat{V} \color{white} = \color{Blue}{5\over |V|} \color{white}+ \color{Green} {7\over |V|} \color{white}+ \color{Yellow} {4\over |V|}$$

$$ \color{Red}\hat{V} \color{white}= \color{Blue} {5\over \sqrt{90}} \color{white}+ \color{Green} {7\over \sqrt{90}} \color{white} + \color{Yellow} {4\over \sqrt{90}}$$

<i style="color:Purple; font-size:18px"><br>
Important: Remember the magnitude of a Normalize vector = 1</i>

<iframe width="420" height="315"
src="https://www.youtube.com/embed/BO_54FGy5S4" allowfullscreen>
</iframe><br>

<i style="color:Orange">
<u style="font-size:16px">Side note (Uses):</u>
<p style="font-size:15px">
If you have a constant vector direction but the magnitude varies its easier to just calculate the change in magnitude. Rather than having to use a calculation how much each component needs to change.<br>
E.g Getting a sudden boost in a game.</p></i>
<br> 

<p style="font-size:18px;color:DarkRed">
Click here to go to my next explainer video about the:
<a href="DotProduct.html">Dot Product</a></p>
