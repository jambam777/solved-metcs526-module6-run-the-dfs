Download Link: https://assignmentchef.com/product/solved-metcs526-module6-run-the-dfs
<br>
<strong>Problem 1 (</strong> Run the DFS on the following graph beginning at node G and show the sequence of nodes generated by the search. When you have two or more choices as the next node to visit, choose them in the alphabetical order.

After completing the DFS, classify each edge as a <em>tree edge, </em>a<em> forward edge, </em>a<em> back edge,</em> or a <em>cross edge</em>.

<strong>Problem 2 .</strong> Run the BFS on the following graph beginning at node I and show the sequence of nodes generated by the search. When you have two or more choices as the next node to visit, choose them in the alphabetical order.

<strong>Problem 3 .</strong> Run the Dijkstra’s algorithm on the following graph beginning at node

<strong>Problem 3-</strong>. After each iteration, show the D values of all nodes (initial D values are shown above each node in red).

<strong>Problem 3-</strong> Show the shortest path from S to every other node generated by the algorithm

<strong>Problem 4</strong>Run the Prim-Jarnik algorithm on the following graph beginning at node <em>a</em>

<strong>Problem 4-</strong>. Show the sequence of nodes in the order they are brought into the “cloud.” <strong>Problem 4-(2)</strong>. Show the minimum spanning tree T, generated by the algorithm, as a set of edges.

<strong>Problem 5 </strong> A friend relationship is a binary relation defined for two persons denoted <em>f</em>(<em>p</em>1, <em>p</em>2), where <em>p</em>1 and <em>p</em>2 are two persons. The meaning is that <em>p</em>1 is a friend of <em>p</em>2. Properties of the friend relationship are:

<ul>

 <li>If<em> f</em>(<em>p</em>1, <em>p</em>2), then <em>f</em>(<em>p</em>2, <em>p</em>1): If <em>p</em>1 is a friend of <em>p</em>2, then <em>p</em>2 is a friend of <em>p</em></li>

 <li>If <em>f</em>(<em>p</em>1, <em>p</em>2) and <em>f</em>(<em>p</em>2, <em>p</em>3), then <em>f</em>(<em>p</em>1, <em>p</em>3): If <em>p</em>1 is a friend of <em>p</em>2 and <em>p</em>2 is a friend of <em>p</em>3, then <em>p</em>1 is a friend of <em>p</em></li>

</ul>




You must write a program named <em>Hw6_P5.java</em> that implements the following requirements.




<ul>

 <li>Your program must read friend relationships among people from an input file named <em>txt</em>. The format of an input file is shown below:</li>

</ul>




John, Isobel

Nathan, John

Rebecka, Yorst

Maria, Yorst

Doloris, Maria

Yorst, Doloris




<ul>

 <li>Your program must store the friend relationships in a (simplified) adjacency matrix, which is a two-dimensional matrix. For example, given the above friend relationships, the corresponding adjacency matrix should be:</li>

</ul>




<table width="599">

 <tbody>

  <tr>

   <td width="75"> </td>

   <td width="75">Doloris</td>

   <td width="75">Isobel</td>

   <td width="75">John</td>

   <td width="75">Maria</td>

   <td width="75">Nathan</td>

   <td width="75">Rebecka</td>

   <td width="75">Yorst</td>

  </tr>

  <tr>

   <td width="75">Doloris</td>

   <td width="75"> </td>

   <td width="75"> </td>

   <td width="75"> </td>

   <td width="75">1</td>

   <td width="75"> </td>

   <td width="75"> </td>

   <td width="75">1</td>

  </tr>

  <tr>

   <td width="75">Isobel</td>

   <td width="75"> </td>

   <td width="75"> </td>

   <td width="75">1</td>

   <td width="75"> </td>

   <td width="75"> </td>

   <td width="75"> </td>

   <td width="75"> </td>

  </tr>

  <tr>

   <td width="75">John</td>

   <td width="75"> </td>

   <td width="75">1</td>

   <td width="75"> </td>

   <td width="75"> </td>

   <td width="75">1</td>

   <td width="75"> </td>

   <td width="75"> </td>

  </tr>

  <tr>

   <td width="75">Maria</td>

   <td width="75">1</td>

   <td width="75"> </td>

   <td width="75"> </td>

   <td width="75"> </td>

   <td width="75"> </td>

   <td width="75"> </td>

   <td width="75">1</td>

  </tr>

  <tr>

   <td width="75">Nathan</td>

   <td width="75"> </td>

   <td width="75"> </td>

   <td width="75">1</td>

   <td width="75"> </td>

   <td width="75"> </td>

   <td width="75"> </td>

   <td width="75"> </td>

  </tr>

  <tr>

   <td width="75">Rebecka</td>

   <td width="75"> </td>

   <td width="75"> </td>

   <td width="75"> </td>

   <td width="75"> </td>

   <td width="75"> </td>

   <td width="75"> </td>

   <td width="75">1</td>

  </tr>

  <tr>

   <td width="75">Yorst</td>

   <td width="75">1</td>

   <td width="75"> </td>

   <td width="75"> </td>

   <td width="75">1</td>

   <td width="75"> </td>

   <td width="75">1</td>

   <td width="75"> </td>

  </tr>

 </tbody>

</table>




Note that in the matrix above, names of persons are shown instead of array indexes for easy illustration.




<ul>

 <li>Your program must print the adjacency matrix on the screen (to show that the adjacency matrix was correctly constructed), like the one shown above.</li>

 <li>Then, your program must display the following main menu:</li>

</ul>




Main Menu




Search options:

<ol>

 <li>Friends of a person 2. Friend or not?</li>

 <li>Exit</li>

</ol>




Enter option number:




<ul>

 <li>Your program must read an option a user enters and perform the following:</li>

 <li>If the option entered is smaller than 1 or greater than 3, then your program must issue an appropriate error message and redisplay the main menu.</li>

 <li>If the option entered is 1, then your program must prompt the user to enter the name of a person and perform the following o If the name does not exist in the adjacency matrix, then issue an appropriate error message and redisplay the main menu.

  <ul>

   <li>If the name exists, then display all friends of the person.</li>

   <li>Redisplay the main menu.</li>

  </ul></li>

 <li>If the option entered is 2, then your program must prompt the user to enter names of two persons separated by a space and perform the following o If any of the two names does not exist in the adjacency matrix, then issue an appropriate error message and redisplay the main menu.

  <ul>

   <li>If both names exist, then display <em>Yes</em> if they are friends and <em>No</em></li>

   <li>Redisplay the main menu</li>

  </ul></li>

 <li>If the option entered is 3, then your program must display an appropriate parting message on the screen and terminate the program.</li>

</ul>




Note that this program can be implemented using many data structures. However, for this assignment, you must use an adjacency matrix to store friend relationships and you may use other additional data structures if you want.




<strong><u>Deliverables</u></strong>




You must submit the following files:




You need to submit the following files:

<ul>

 <li><em>pdf</em>: This file must include:</li>

 <li>Answers to problems 1 through 5.</li>

 <li>Discussion/observation of Problem 6: This part must include what you observed and learned from this experiment and it must be “substantive.”</li>

 <li><em>java</em></li>

 <li>Other files, if any.</li>

</ul>




Combine all files into a single archive file and name it <em>LastName_FirstName_hw6.EXT</em>, where <em>EXT</em> is an appropriate archive file extension, such as <em>zip</em> or <em>rar</em>.

<strong> </strong>