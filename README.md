# NP HTML5, CSS3, and JavaScript 6e Tutorial 12, Case Problem 3

## Description:
```
1.  Use your editor to open the js_nodes_txt.html and js_tree_txt.js files from the html12 > case3 folder. Enter your name and the date in the comment section of each file, and save them as js_nodes.html and js_tree.js respectively.
2.  Go to the js_nodes.html file in your editor. Within the document head, create links to the js_tree.css style sheet file and the js_tree.js JavaScript file. Load the js_tree.js file asynchronously.
3.  Take some time to study the code of the HTML file and then save your changes to the document.
4.  Return to the js_tree.js file in your editor. Jorge wants you to keep track of the total count of nodes, element nodes, text nodes, and white-space nodes. Below the comment section, create the following global variables: nodeCount, elemCount, textCount, and wsCount and set their initial values to 0.
5. Create an event handler that runs the makeTree() function when the page loads.
6.  The makeTree() function will be used to create the node tree for the source article on the page. Create the makeTree() function, adding the commands described in Steps 7 through 10.
7.  Within the makeTree() function, create the following aside element fragment <aside id="treeBox"> <h1>Node Tree</h1> </aside> and append it to the section element with the ID "main".
8.  The node tree will be created within an ordered list. Declare a variable named nodeList contain¬ing the initial ol element node that will be the foundation of the node tree and append it to the aside element fragment.
9.  The node tree will be based on the contents of the elements matching the CSS selector "#main article". Declare a variable named sourceArticle that points to these elements. (Hint: Use the querySelectorAll() method.)
10.  The contents of the node tree and the count of the different global variables will be updated using a function named makeBranches(), which you will create shortly. Call the makeBranches() function using the sourceArticle and nodeList variables as parameter values.
11.  Create the makeBranches() function that will be used to append node branches to the node tree diagram. The function will have two parameters named treeNode and nestedList. The treeNode parameter stores the current node from the source article and the nestedList parameter stores the structure of the node tree displayed in the web page. Add the commands described in Steps 12 through 17 to the function.
12.  Each time the makeBranches() function is called, it is because a new node has been discovered in the source article. Increase the value of the nodeCount variable by 1.
13.  Create the following list item HTML fragment, storing the list item element in the liElem variable and the span element node in the spanElem variable: <li> +—<span></span> </li>
14.  Append the spanElement node to the liElem element node; append the liElem node to the nestedList element node.
15. If treeNode represents an element node, then do the following:
  a.  Increase the value of the elemCount variable by 1.
  b.  Add the class attribute to the spanElem node, setting its value to "elementNode".
  c.  Append the text string "<element>" to the spanElem node, where element is the name of the HTML element. (Hint: Use the textContent property to append the text of the element tag and not the element tag itself.)
16. Else if treeNode represents a text node, do the following:
  a.  Increase the value of the textCount variable by 1.
  b.  Declare the variable textString equal to the value of the text node.
  c.  Jorge has provided a function named isWhiteSpaceNode() to determine whether a text node represents white space or not. Call the isWhiteSpaceNode() function using textString as the parameter value. If the function returns the value true, then do the following:
    i.  Increase the value of the wsCount variable by 1
    ii.  Change the class attribute of the spanElem node to "whiteSpaceNode"
    iii.  Append the text string "#text" to the spanElem node
  d. If the isWhiteSpaceNode() function returns the value false, then do the following:
    i.  Change the class attribute of the spanElem node to "textNode"
    ii.  Append the text string "text" to the spanElem node where text is the value of the textString variable
17. The makeBranches() function should recursively move through the different levels of nodes in the source article. To apply recursion, test whether the number of child nodes of treeNode is greater than zero. If it is, then do the following:
  a.  Create the following HTML fragment as an element node with the name newList: <ol>|</ol>
  b.  Append newList to the nestedList element node.
  c.  Loop through the child nodes of treeNode using n to represent each child node and, for each child node, call the makeBranches() function using n and newList as the parameter values.
18.  Return to the makeTree() function and add commands to display the total count of nodes, element nodes, text nodes, and whitespace nodes within the span elements whose IDs are "totalNodes", "elemNodes", "textNodes", and "wsNodes", respectively.
19.  Document your work with informative comments throughout the JavaScript file.
20.  Save your changes to the file and load js_nodes.html in your browser. Verify that the browser dis¬plays the schematic diagram of the node tree for the Working with Nodes article. Further verify that the second paragraph of the article reports 238 total nodes in the document, comprised of 98 element nodes, and 140 text nodes (of which 57 are whitespace nodes).

```
