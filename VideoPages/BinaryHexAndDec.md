# Hexadecimal, Binary and Decimal

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


<p style="font-size:18px;color:lightblue">
Hello there! In this page I'm going to be going over hexadecimal, binary and decimal. Its a relatively easy topic but can be explained badly.
</p>

<p style="font-size:18px;color:blue">
Decimal
</p>

<p style ="font-size:16px">
So decimal is easy, you've been doing it since you were a kid. Its just your normal number system<em style="color:Red"> base 10</em>. Meaning there are <em style="color:yellow">10</em> possible numbers per unit. <em style="color:yellow">0</em> through to<em style="color:yellow"> 9</em>.<br><br> As you go from right the left the value of the unit gets bigger by <em style="color:yellow">10</em> each time due to it being <em style="color:Red">base 10</em>. And increases like:<br><em style="color:yellow">1, 10, 100, 1000, etc <br>
Example: 205</em>
</p>

<p style="font-size:18px;color:blue">
Binary
</p>

<p style ="font-size:16px">
Binary is a bit more complex but you'll also be fairly used to it. Its just your 1s and 0s that the computer used. The determine whether a transistor (The things that make up the computer) is on or off. It is <em style="color:Red">base 2</em> meaning there can be <em style="color:Red">2 possible values, 0 and 1</em>.<br><br>
A bit is a single binary unit, a byte is 8<br>
<em style="color:yellow">Bit: 0 or 1<br>
Byte: 1000100<br></em>
You can convert bits to decimal but I will go over that later.<br><br>
With binary being <em style="color:Red">base 2</em> when you go from right to left the value gets bigger by <em style="color:Red">x2</em> similar to decimal just with a different base so it increases differently.<br>
The first bit is 1 meaning it increases in the pattern.<br><em style="color:yellow">
1, 2, 4, 8, 16, 32, 64, 128</em>
</p>

<p style="font-size:18px;color:blue">
Hexadecimal:
</p>

<p style="font-size:16px">

Hexadecimal is a bit of a inbetween for decimal and binary in my mind, it's easier for computers to work with than decimal but they'll still have to convert it to binary to use.<br>
And for us humans its easier to read than a long list of bytes.<br>
A hexadecimal number is <em style="color:Red">base 16</em> meaning that it has <em style="color:yellow">16</em> possible values,<em style="color:yellow"> 0-9</em> is normal like a number, but then you use letters for the other <em style="color:yellow">6</em> values <em style="color:yellow">A</em> to <em style="color:yellow">F</em>.<br><br>
Since a hex number is <em style="color:Red">base 16</em>. for each number it increases by<em style="color:Red"> x16</em> so the first value is  ${\color{yellow}16^0 = 1}$ the second ${\color{yellow}16^1=16}$ the third ${\color{yellow}16^2= 256}$ etc 
</p>

<p style="font-size:18px;color:blue">
Decimal to Binary Conversion:
</p>

<p style="font-size:16px">
In this section we're going to cover how to convert a binary number to decimal. First of all we'll repesent the power of each bit. In this case we'll use assume all the bits in the byte is a 1.</p>

$$ 1 1 1 1 1 1 1 1 $$

<table class="center" style="width:50%;margin-left:auto;margin-right:auto">
    <tr> 
        <th>128</th>
        <th>64</th>
        <th>32</th>
        <th>16</th>
        <th>8</th>
        <th>4</th>
        <th>2</th>
        <th>1</th>
    </tr>
    <tr style="color:yellow">
        <td>1</td>
        <td>1</td>
        <td>1</td>
        <td>1</td>
        <td>1</td>
        <td>1</td>
        <td>1</td>
        <td>1</td>
    </tr>
</table>


<p style="font-size:16px">
Then you add them all together, if its a 1 it means that bit is "on" so you add it, if it was zero you wouldn't.
</p>

$$ 
\color{yellow}128 \color{white}+\color{yellow} 64 \color{white}+ \color{yellow}32\color{white} +\color{yellow} 16\color{white}+ \color{yellow}8\color{white} +\color{yellow} 4 \color{white} + \color{yellow}2\color{white} +\color{white} \color{yellow}1\color{white}= \color{yellow}255
$$

<br>
<p style ="font-size:16px">
Lets do another example with the binary number:
</p>

$$ 1 1 0 0 1 1 0 1 $$

<table class="center" style="width:50%;margin-left:auto;margin-right:auto">
    <tr> 
        <th>128</th>
        <th>64</th>
        <th>32</th>
        <th>16</th>
        <th>8</th>
        <th>4</th>
        <th>2</th>
        <th>1</th>
    </tr>
    <tr>
        <td style="color:yellow">1</td>
        <td style="color:yellow">1</td>
        <td  style="color:red">0</td>
        <td style="color:red">0</td>
        <td style="color:yellow">1</td>
        <td style="color:yellow">1</td>
        <td style="color:red">0</td>
        <td style="color:yellow">1</td>
    </tr>
</table>

<p style ="font-size:16px">
I've changed the colours so red shows the <em style="color:Red">0</em> "off" bits and yellow shows the <em style="color:yellow">1</em> "on"  bits.
</p>

$$ 
\color{yellow}128 \color{white}+\color{yellow} 64 \color{white}+ \color{red}32\color{white} +\color{red} 16\color{white}+ \color{yellow}8\color{white} +\color{yellow} 4 \color{white} + \color{red}2\color{white} +\color{white} \color{yellow}1\color{white}= \color{yellow}255
$$

$$ 
\color{yellow}128 \color{white}+\color{yellow} 64 \color{white} + \color{yellow}8\color{white} +\color{yellow} 4 \color{white} +\color{white} \color{yellow}1\color{white}= \color{yellow}205
$$