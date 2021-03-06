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

<p style="font-size:20px;color:blue">
What you'll first see and basic info
</p>

<p style="font-size:16px">
You'll want to connect to the router and open up the command line interface (CLI)
</p>

<p style="font-size:18px">
You might be given a message like:
</p>

<p style="font-size:18px;color:Red">
Would you like to enter the inital configuration mode? [Yes/No]
</p>

<p style="font-size:16px">
just enter No for now<br><br>
You'll then see this:
</p>

<p style="font-size:18px;color:Red">
Router></p> <p style="font-size:15px">This shows that you're in User EXEC Mode:<br> You have limited access to commands such as (ping, show and enable). You can't configure anything in this mode
</p>

<p style="font-size:16px">
To enter the Privileged EXEC mode. To be able to configure the router enter:
</p>

<p style="font-size:18px;color:red">
Router> enable
</p>

<p style="font-size:16px">
When you enter this you'll notice your prompt to change to:
</p>

<p style="font-size:18px;color:red">
Router#
</p>

<p style="font-size:15px">
This shows that you're in the Privilged EXEC mode: here you'll be  able to have more access to commands. (Will require a password if it has been set up) 
</p>

<p style="font-size:18px;color:red">
Router # show ~
</p>

<p style="font-size:15px">
This command gives information about the router  <e style="color:red"> show ?</e> gives you the possible options that can be used such as
</p>

<p style ="font-size:18px;color:Red">
Route# show ip interface brief
</p>

<p style="font-size:15px">
Which shows all of the ip interfaces you can use in the form:
</p>

<p style="font-size:15px;color:lightblue">
Interface | IP Address | OK? | method | status | Protocol<br><br>
FastEthernet0/0 | Unassigned | Yes | unset  | Administratively Down | Down<br>
FastEthernet0/1 | Unassigned | Yes | unset | Administratively Down | Down<br>
Serial0/0 | Unassigned | Yes | unset  | Administratively Down | Down<br>
Serial0/1 | Unassigned | Yes | unset | Administratively Down | Down
</p><br>

<p style="font-size:15px">
The FastEthernet interfaces can be used to connect to devices and switches on a network, whereas the serial interface can be used to connect to other routers.<br>
As you can see they're all administratively down meaning that even if they're physically connected to other devices they won't till this is disabled.
</p>

<p style="font-size:15px">
First I am going to change the name of my router and set the password for added security. But to do  this we need to be in router config mode to configure its settings. <br> Which can be done using the command
</p>

<p style="font-size:20px;color:blue">
Initial Router Configure
</p>
<p style="font-size:18px;color:red">
Router# configure terminal
</p>

<p style="font-size:15px">
This changes you into the configure mode where you can change the "global" settings for the router. If you want to change the settings of a specific interface you'll have to specify before changing it.
</p>

<p style="font-size:15px"> You'll be down the output to show the modes has changed: </p>
<p style="font-size:18px;color:Red"> Router(config)# </p>

<p style="font-size:15">
One of the first things you'll want to do in this mode is set the hostname, this helps you tell which router you're actually configuring. This is done by the command:</p>

<p style="font-size:18px;color:Red">
Router(config)# hostname <e style="color:pink"> (hostname)</e>
</p>

<p style="font-size:15">
This then changes your hostname to whatever you've chosen. For this instance lets say I entered:</p>

<p style="font-size:18px;color:Red">
Router(config)# hostname R0
</p> 

<p style="font-size:15">
You'd then be shown this, where the first part of your prompt has changed to the new hostname</p>

<p style="font-size:18px;color:Red">
R0(config)#
</p> 

<p style="font-size:20px;color:blue">
Router interface configure:
</p>

<p style="font-size:16px">
First things first you'll want to tell your router which interface to configure. This is done with the command:</p>

<p style="font-size:18px;color:Red">
R0(config)# interface <e style="color:pink"> (interface)</e>
</p> 

<p style="font-size:16px">
Lets choose one from above where we got the ip interfaces, I'll use FastEthernet0/0 this being the interface my PC is connected to.</p>

<p style="font-size:18px;color:Red">
R0(config)# interface <e style="color:pink"> FastEthernet0/0</e>
</p>

<p style="font-size:16px">
Note you input changes to:
</p>

<p style="font-size:18px;color:Red">
R0(config-if)#
</p> 

<p style="font-size:16px">
This shows you're now in config mode for the interface you choose.
</p>

<p style="font-size:16px">
You can then change the desciption of the interface. This is good practice so you know what this interfaces job is in the future. This is done by:
</p>

<p style="font-size:18px;color:Red">
R0(config-if)#description  <e style="color:pink"> (what it does)</e>
</p>

<p style="font-size:16px">
The next job is to give the interface an ip address so packets can be sent to it with the command:
</p>

<p style="font-size:18px;color:Red">
R0(config-if)#ip address  <e style="color:pink"> (ip address) (subnet mask)</e>
</p>

<p style="font-size:16px">
I won't go through how to calculate your subnet mask here (I may do in the future) but there are a number of great resources online to help you calculate the correct subnet mask for your network.
</p>

<p style="font-size:16px">
Once you have done that you can now turn your interface on. This is done by shutting down the administratively down mode you saw earlier, with the command:
</p>

<p style="font-size:18px;color:Red">
R0(config-if)#no shutdown
</p>

<p style="font-size:16px">
The shutdown component tells the interface to shutdown, but with the no it updates it so that it is no longer shutdown. If there are devices ready to connect with all the wires connected up, you'll get a prompt telling you the interface state has been changed to up:<br> <e style="font-size:18px;color:lightBlue"> Inteface ..... changed state to up</e>
<br><br> But if not it'll be changed to down rather than administratively down and you'll have to check why its not connecting. This tends to occur if you've not configured another router that is connected along that line. The message will look like this:<br>
<e style="font-size:18px;color:lightBlue"> Inteface ..... changed state to down </e>
</p>

<p style="font-size:20px;color:blue">
Securing your router:
</p>
<p style="font-size:16px">
Now the next thing is securing your router so not just anyone can access it and change the configuration you set up</p>

<p style="font-size:16px">
To start you want to secure entering the Privillaged EXEC Mode, using the command:</p>

<p style="font-size:18px;color:Red">
R0(Config)#enable secret <e style="color:pink">(Password)</e></p> 

<p style="font-size:16px">
This sets the password that you have to enter whenever you type in:</p>
<p style="font-size:18px;color:Red">
R0(Config)#enable</p>
<p style="font-size:16px">
You'll get a message stating:<br>
 </e>
<e style="font-size:18px;color:lightBlue"> Password:
</e><br>where you'll have to enter the password you set. You'll get 3 attempts to enter it until it states<br> <e style="font-size:18px;color:lightBlue"> % Bad secrets</e> <br>and you'll have to re-enter the enable command</p>

<p style="font-size:16px">
If you want to be able to access the router remotely (which will be very useful). You'll have to create an account on the router:</p>

<p style="font-size:18px;color:Red">
R0(config)#username <e style="color:pink">(username)</e> privallage <e style="color:pink">(privallage level)</e> secret <e style="color:pink">(password)</e></p>

<p style="font-size:16px">
Then you'll want to choose which terminal lines you want to be able to access the router. For this example I'll do all of them (0-4) As a default  router has 5 lines</p>

<p style="font-size:18px;color:Red">
R0(config)#line vty 0 4</p>
<p style="font-size:16px">
This will allow you to configure line 0 through 4 at once, you'll also notice the prompt changes to:</p>

<p style="font-size:18px;color:Red">
R0(config-line)#</p>
<p style="font-size:16px">
Showing you're successfully configuring the terminal lines.<br>Now you'll want to set the protocol that you want to use to access the router:</p>
<p style="font-size:18px;color:Red">
R0(config-line)#transport input ?</p>

<p style="font-size:16px">
Will show you the available protocols to login with, SSH and Tellent are the most commonly used. I'll be using ssh (secure shell host) since its more secure as its encrypted. Although it does take an extra few steps to set up:</p>

<p style="font-size:18px;color:Red">
R0(config-line)#transport input ssh</p>

<p style="font-size:16px">
For ssh to work properly you'll need to give the router a domain name to be accessed by:</p>

<p style="font-size:18px;color:Red">
R0(config)#ip domain-name <e style="color:pink">(domain name)</p>

<p style="font-size:16px">
For example as this is router 0 I'll set the domain name to router0.com</p>

<p style="font-size:18px;color:Red">
R0(config)#ip domain-name router0.com</p>

<p style="font-size:16px">
And now you'll want to create a key to encrypt all the data going through the router (Lets use RSA in this case):</p>

<p style="font-size:18px;color:Red">
R0(config)#crypto key generate RSA</p>

