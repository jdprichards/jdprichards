# Configuring routers
<p style="font-size:16px">
Welcome to my little tutorial on configuring routers. I will be going over more of the command side of things. With the commands that are used and what they do.<br>
<a href="https://nevexo.space/networking/2021/02/24/cisco-packet-tracer-basic.html">Cameron</a>
has more of a video step by step walkthrough than me so be sure to check that out as well.
</p>

<p style="font-size:15px">
First you want to have a physical router or a simulation program to be able to use these: <br>
- if you have a physical router you'll want to connect to it via the console in port and use a terminal emulator such as putty.
<br>
- I use a simulation program called packet tracer which allows you to create a number of virtual devices and configure them as you would if you had them physically.</p>

<p style="font-size:16px">
You'll want to connect to the router and open up the command line interface (CLI)
</p>

<p style="font-size:18px">
You might be given a message like:</p>
<p style="font-size:16px;color:Red">
Would you like to enter the inital configuration mode? [Yes/No]
</p>
<p style="font-size:16px">
just enter No for now<br><br>
You'll then see this:
</p>

<p style="font-size:18px;color:Red">
Router></p> <p style="font-size:15px">This shows that you're in User EXEC Mode:<br> You have limited access to commands such as (ping, show and enable). You can't configure anything in this mode</p>
