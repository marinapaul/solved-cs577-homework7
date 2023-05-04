Download Link: https://assignmentchef.com/product/solved-cs577-homework7
<br>
<ol>

 <li> Suppose we are given an integer <em>k</em>, together with a flow network <em>N </em>= (<em>V,E,c</em>) in which every edge has capacity 1. Design an algorithm to identify <em>k </em>edges in <em>N </em>such that after deleting those <em>k </em>edges, the maximum value of a flow in the remaining network is as small as possible. Your algorithm should run in time polynomial in <em>n </em>and <em>m</em>.</li>

 <li>Given a flow network <em>N </em>= (<em>V,E,c</em>) with source <em>s </em>and sink <em>t</em>, we say that a node <em>v </em>∈ <em>V </em>is <em>upstream </em>if, for all minimum <em>s</em>–<em>t </em>cuts (<em>S,T</em>) of <em>G</em>, <em>v </em>∈ <em>S</em>. In other words, <em>v </em>lies on the <em>s</em>-side of every minimum <em>s</em>–<em>t </em> Analogously, we say that <em>v </em>is <em>downstream </em>if <em>v </em>∈ <em>T </em>for every minimum <em>s</em>–<em>t </em>cut (<em>S,T</em>) of <em>G</em>. We call <em>v central </em>if it is neither upstream nor downstream.</li>

</ol>

Design an algorithm that takes <em>N </em>and a flow <em>f </em>of maximum value in <em>N</em>, and classifies each of the nodes of <em>N </em>as being upstream, downstream, or central. Your algorithm should run in linear time.

<h1>Regular problems</h1>

<ol start="3">

 <li>[Graded, 3 points] A given network <em>G </em>with integer capacities may have more than one minimum <em>s</em>–<em>t </em> Define the <em>densest </em>minimum <em>s</em>–<em>t </em>cut to be any minimum <em>s</em>–<em>t </em>cut (<em>S,T</em>) of <em>G </em>with the greatest number of edges crossing from <em>S </em>to <em>T</em>.

  <ul>

   <li>Suppose we have access to a black box called MaxFlow. MaxFlow takes as input a network <em>N </em>and outputs a flow of maximum value for <em>N</em>. Design an algorithm to find a densest minimum <em>s</em>–<em>t </em>cut of <em>G </em>using at most one call to MaxFlow. Outside of MaxFlow, your algorithm should run in linear time. You may assume that standard arithmetic operations can be done in constant time.</li>

   <li>Design an algorithm to determine whether <em>G </em>contains a unique densest minimum <em>s</em>–<em>t </em> Once again, you can make at most one call to MaxFlow. Outside of MaxFlow, your algorithm should run in linear time. You may assume that standard arithmetic operations can be done in constant time.</li>

  </ul></li>

 <li>Consider a network with integer capacities. An edge is called <em>upper-binding </em>if increasing its capacity by one unit increases the maximum flow value in the network. An edge is called <em>lower-binding </em>if reducing its capacity by one unit decreases the maximum flow value in the network.</li>

</ol>

1

<ul>

 <li>For the network <em>G </em>below determine a maximum flow <em>f</em><sup>∗</sup>, the residual network <em>G<sub>f</sub></em>∗, and a minimum cut. Also identify all of the upper-binding edges and all of the lower-binding edges.</li>

 <li>Develop an algorithm for finding all the upper-binding edges in a network <em>G </em>when given <em>G </em>and a maximum flow <em>f</em><sup>∗ </sup>in <em>G</em>. Your algorithm should run in linear time.</li>

 <li>Develop an algorithm for finding all the lower-binding edges in a network <em>G </em>when given <em>G </em>and an integer maximum flow <em>f</em><sup>∗ </sup>in <em>G</em>. Your algorithm should run in time polynomial in <em>n </em>and <em>m</em>. Can you make it run in linear time?</li>

</ul>

<ol start="5">

 <li>A given network can have many minimum <em>st</em>-cuts.

  <ul>

   <li>Determine precisely how large the number of minimum <em>st</em>-cuts in a graph can be as a function of <em>n</em>.</li>

   <li>Show that if (<em>S</em><sub>1</sub><em>,T</em><sub>1</sub>) and (<em>S</em><sub>2</sub><em>,T</em><sub>2</sub>) are both minimum <em>st</em>-cuts in a given network, then so is (<em>S</em><sub>1</sub>∪ <em>S</em><sub>2</sub><em>,T</em><sub>1</sub>∩ <em>T</em><sub>2</sub>). How does this generalize to more than 2 <em>st</em>-cuts?</li>

   <li>Design an algorithm that, given a network, generates a collection of minimum <em>st</em>-cuts</li>

  </ul></li>

</ol>

(<em>S</em><sub>1</sub><em>,T</em><sub>1</sub>)<em>,</em>(<em>S</em><sub>2</sub><em>,T</em><sub>2</sub>)<em>,… </em>such that every minimum cut of the network can be written as

(∪<em>i</em>∈<em>I</em><em>S</em><em>i,</em>∩<em>i</em>∈<em>I</em><em>T</em><em>i</em>)

for some subset <em>I </em>of indices. Your algorithm should run in time polynomial in <em>n </em>and <em>m</em>.

<h1>Challenge problem</h1>

<ol start="6">

 <li>Problem J from the 2007 ACM-ICPC World Finals (see next page). Your algorithm should</li>

</ol>

<em>.</em>

run in time polynomial in <em>n </em>= <em>R </em>+ <em>T</em>.

<h1>Programming problem</h1>

<ol start="7">

 <li>SPOJ problem <a href="http://www.spoj.com/problems/POTHOLE">Potholers</a> (problem code POTHOLE).</li>

</ol>

2










Problem J

Tunnels

Input File: tunnels.in




Curses! A handsome spy has somehow escaped from your elaborate deathtrap, overpowered your guards, and stolen your secret world domination plans. Now he is running loose in your volcano base, risking your entire evil operation. He must be stopped before he escapes!

Fortunately, you are watching the spy’s progress from your secret control room, and you have planned for just such an eventuality. Your base consists of a complicated network of rooms connected by non-intersecting tunnels. Every room has a closed-circuit camera in it (allowing you to track the spy wherever he goes), and every tunnel has a small explosive charge in it, powerful enough to permanently collapse it. The spy is too quick to be caught in a collapse, so you’ll have to strategically collapse tunnels to prevent him from traveling from his initial room to the outside of your base.

Damage to your base will be expensive to repair, so you’d like to ruin as few tunnels as possible. Find a strategy that minimizes the number of tunnels you’ll need to collapse, no matter how clever the spy is. To be safe, you’ll have to assume that the spy knows all about your tunnel system. Your main advantage is the fact that you can collapse tunnels whenever you like, based on your observations as the spy moves through the tunnels.




<h2>Input</h2>

The input consists of several test cases. Each test case begins with a line containing integers <em>R</em> (1 ≤ <em>R</em> ≤ 50) and <em>T </em>(1 ≤ <em>T</em> ≤ 1000), which are the number of rooms and tunnels in your base respectively. Rooms are numbered from 1 to <em>R</em>. <em>T</em> lines follow, each with two integers <em>x</em>, <em>y</em> (0 ≤ <em>x</em>,<em>y</em> ≤ <em>R</em>), which are the room numbers on either end of a tunnel; a 0 indicates that the tunnel connects to the outside. More than one tunnel may connect a pair of rooms.

The spy always starts out in room 1. Input is terminated by a line containing two zeros.




<h2>Output</h2>

For each test case, print a line containing the test case number (beginning with 1) followed by the minimum number of tunnels that must be collapsed, in the worst case. Use the sample output format and print a blank line after each test case.




<h2>         Sample Input                                                Output for the Sample Input</h2>

<table width="580">

 <tbody>

  <tr>

   <td width="290">4 61 21  32  43  44  04 04 61 21 31  42  03  04  00 0</td>

   <td width="290">Case 1: 2 Case 2: 2</td>

  </tr>

 </tbody>

</table>

19 of 20