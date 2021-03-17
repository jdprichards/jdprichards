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

<em style="font-size:16px;color:slateblue ">
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
Which will give you the result

${ \approx \text{means approximately equal to}}$</p>

$$ \color{lightBlue}\theta \color{white}= \color{orange} \arccos{\color{white}\frac{\color{Red}80}{ \sqrt{\color{Red}116} \times \sqrt{\color{Red}77}} \approx \color{lightblue} 137.4^{\circ}} $$

<p style="font-size:17px">
And this is your final value for the angle between vectors.
</p>
<p style ="font-size:15px">
I am planning on doing a coding walkthrough how you could calculate this in a side a programing using the TL-Engine. A game engine used in the first year of the computer science course at UCLan.
</p>

<p style="font-size:18px;color:DarkRed">
Click here to go to my next explainer video about the:
<a href="CrossProduct.html">Cross Product </a><br><br>

Or go below to find some questions to test your knowlege.<br>
<em style="font-size:18px;color:slateblue">
Important: If you are asked to calculate the angle between vectors in the exam you can use a calculator; but its a good idea to be able to do the dot product by hand.
</em>

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

1a. find:<br>
${V\cdot{}W}$
</p>

<button type="button" onclick="ShowAndHide('Answer1a');"> 
Get answer
</button>

<div id="Answer1a" style="display:none">
<p style="font-size:16px">
The answer to question 1a: <br>

${ \text{The answer:}}$

Remember we have to add the times the same axis together than add them up.<br>

For the X: $${4\times7 = 28}$$

For the Y: $${6\times2 = 12}$$

For the Z: $${3\times2 = 6}$$

Then you add them all together

$${28+12+6 = 46}$$

So:

$${V\cdot{}W = 46}$$
</p>
</div>

1b. find:<br>
The angle between V and W.<br>
<button type="button" onclick="ShowAndHide('Answer1b');"> 
Get answer
</button>

<div id="Answer1b" style="display:none">

${\text{The answer:}}$

First remember the equation is:

$${W\cdot{}V\over{|V|\times|W|}}$$

$${V\cdot{}W \text{ Is the answer to the above question: 46}}$$

But you need to calculate ${|V|}$ and ${|W|}$:

$$ |V| = \sqrt{Vx^2+Vy^2+Vz^2}  \text{ And } |V| = \sqrt{Wx^2+Wy^2+Wz^2} $$

$$ |V| = \sqrt{4^2+6^2+3^2}= \sqrt{61}$$
$$ |W| = \sqrt{7^2+2^2+2^2} = \sqrt{57}$$

Now to put this all together

$$ \frac{46}{\sqrt{61}\times\sqrt{57}}\approx 0.7801093556963545... $$

$$ \arccos{(0.7801093556963545
)} \approx 38.73 $$

$$ \text{Or just} $$

$$ \arccos{\frac{46}{\sqrt{61}\times\sqrt{57}}}\approx 38.73$$
</div>
<br>
<p style="font-size:16px">
For the next 2 questions I won't do a step by step walkthough, but I will give the answers.
</p>

<p style ="font-size:16px">
Question 2:<br>

With ${ V= 6x, 2y, 3z}$ and ${W = 3x, 4y, 3z}$
<br>

1a. find:<br>
${V\cdot{}W}$
</p>

<button type="button" onclick="ShowAndHide('Answer2a');"> 
Get answer
</button>

<div id="Answer2a" style="display:none">
<p style="font-size:16px">
The answer to question 2a: <br>

${ \text{The answer: 31}}$
</p>
</div><br>
2b. find:<br>

The angle between V and W.

<button type="button" onclick="ShowAndHide('Answer2b');"> 
Get answer
</button>

<div id="Answer2b" style="display:none">
The answer to question 2b: <br>

$$29.3$$
</div>

<p style ="font-size:16px">
Question 3:<br>

With ${ V= 5x, 2y, 7z}$ and ${W = 2x, 6y, 4z}$
<br>

3a. find:<br>
${V\cdot{}W}$
</p>

<button type="button" onclick="ShowAndHide('Answer3a');"> 
Get answer
</button>

<div id="Answer3a" style="display:none">
The answer to question 3a: <br>

$$ 40 $$
</div>
<br>


<p>
3b. find:<br>
The angle between V and W.

</p>
<button type="button" onclick="ShowAndHide('Answer3b');"> 
Get answer
</button>
<div id="Answer3b" style="display:none">
The answer to question 3b: <br>

$$19.5$$
</div>
