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

$$\color{Red} V\color{white}\cdot{}\color{Red}W = \color{Red}|V||W|\color{orange}\cos{\color{lightBlue}\theta}$$

$\text{Where } \color{lightBlue}\theta \color{white}\text{ is the angle between the vectors}$

$$ \frac{\color{Red} V\color{white}\cdot{}\color{Red}W}{\color{Red}|V||W|} = \color{orange}\cos{\color{lightBlue}\theta} $$

$$ \color{lightBlue}\theta \color{white}=  \color{orange}\arccos{\color{white}\frac{\color{Red}V\color{white}\cdot \color{Red} W}{ \color{Red}|V||W|}} $$

<br>
<p style="font-size:16px">
Now onto an example:
<Br> Calculate the angle between V and W
<Br><br> Where V and W are: </p>

$$ \color{Red}V \color{white} = \color{Blue}4x \color{white} +\color{Green}6y \color{White}+ \color{Yellow} 8z$$

$$ \text{And} $$

$$ \color{Red}W \color{white}= \color{Blue}2x \color{white}+ \color{Green}8y \color{white}+ \color{yellow}3z $$

$$ \text{Then combining them like this} $$

$$ \color{Red}V\color{white}\cdot{}\color{Red}W \color{white}= \color{Blue} VxWx \color{white}+  \color{Green}VyWy\color{white}+\color{Yellow}VzWz $$

$$ \color{Red} V \color{white}\cdot \color{Red} W \color{White} = \color{Blue}4\color{white}\times\color{Blue}2\color{white} + \color{green} 6 \color{white}\times \color{Green} 8 \color{white} + \color{Yellow} 8 \color{white}\times \color{Yellow}3 $$

$$ \color{Red} V \color{white}\cdot \color{Red} W \color{White} = \color{Blue}8 \color{white} + \color{green} 48 \color{white} + \color{Yellow} 24 \color{white} = \color{Red}80$$
<br>

<p style="font-size:16px">

So now you've got the value of ${ \color{Red}V \color{white}\cdot\color{Red} W\color{white}}$ We need 2 more things to be able to calculate the angle between vectors and that is...
</p>

<p style="font-size:17px">

Finding the magnitude of ${ \color{Red}V}$ and ${ \color{Red} W}$

From my previous tutorials that the magnitude of a vector is:
</p>

$$ \color{Red}|V| \color{white}=  \sqrt{\color{Blue}Vx \color{white}+ \color{Green}Vy \color{white}+ \color{yellow}Vz} $$

<p style="font-size:17px">

From this equation we can caculate ${\color{Red}|V|}$ and ${\color{Red}|W|}$: 
</p>

$$ \color{Red}|V| \color{white}=  \sqrt{\color{Blue}4^2 \color{white}+ \color{Green}6^2 \color{white}+ \color{yellow}8^2}$$

$$ \color{Red}|V| \color{white}=  \sqrt{\color{Blue}16 \color{white}+ \color{Green}36 \color{white}+ \color{yellow}64}\color{white} =\sqrt{\color{Red}116} $$

$$ \color{Red}|W| \color{white}=  \sqrt{\color{Blue}2^2 \color{white}+ \color{Green}8 ^2\color{white}+ \color{yellow}3^2}$$

$$ \color{Red}|W| \color{white}=  \sqrt{\color{Blue}4 \color{white}+ \color{Green}64\color{white}+ \color{yellow}9}\color{white} = \sqrt{\color{Red}77}$$

<p style="font-size:17px">
Now to put this all together into one equation
</p>


$$ \color{Red} |V| \color{White} = \sqrt{\color{Red}116}\color{white}\text{, } \color{Red} |W| \color{white} = \sqrt{\color{Red}77}, \color{Red} V\color{white}\cdot\color{Red}W \color{white} = \color{Red}80$$

$$ \color{lightBlue}\theta \color{white}=  \color{orange}\arccos{\color{white}\frac{\color{Red}V\color{white}\cdot \color{Red} W}{ \color{Red}|V||W|}} $$

<p style="font-size:17px">
Substituting the numbers in</p>

$$ \color{lightBlue}\theta \color{white}=  \color{orange}\arccos{\color{white}\frac{\color{Red}80}{ \sqrt{\color{Red}116} \times \sqrt{\color{Red}77}}}$$

<p style="font-size:17px">
Then putting it all into the caculator or getting the computer to calculate it:</p>

$$ \color{lightBlue}\theta \color{white}= \color{orange} \arccos{\color{white}\frac{\color{Red}80}{ \sqrt{\color{Red}116} \times \sqrt{\color{Red}77}}} $$

<p style="font-size:16px">
And you can 

<p style="font-size:18px;color:DarkRed">
Click here to go to my next explainer video about the:
<a href="CrossProduct.html">Cross Product </a>
</p>
