# FamilyTree

Family Tree Data Structure in Java

Step 1

At first glance, a big part of the coursework could be completed by thinking of the family tree as a linked list data structure in which the “next” node always points to the next child, partner or sibling! 

This part was quite easy to implement knowing that we only had to create the first ancestor and add a partner, a first child and some siblings for that first child. For all intensive purposes the first child with it’s siblings, considering the siblings were not connected to the parents, acted exactly like a Linked List would. 

Things seemed to get a little bit more complicated when we actually had to start searching for different nodes and displaying them based on the identifier variable. As well as when we had to add partners and children to siblings

As the tree gets bigger, our functions needed to be a bit more complex and sophisticated 

Step 2

We added identifiers in our structure that mimicked the size of the tree so that they would automatically be incremented, much like in a database. 

Iterating through the tree as it got bigger proved to be a bit more challenging, because we had to account for not just a linear structure, but we had to actually think of ways we can use back-tracking so that once we reached a dead-end we could go back to a check-point of sorts that we could continue down a different path to find a specified node.

After some research we realized one of the ways we could actually iterate through the tree in order to look for specific nodes with specific identifiers would be the DFS algorithm (Depth-First-Search). We used a custom recursive version of this algorithm to loop through the Tree and once it finds the Node we are looking for it sets it on a variable we can later use to extract the information! 

The DFS algorithm visited each node recursively, we chose the pre-order traversal version (we could also choose in-order and post-order). We started looking for the children first, then the partners and finally the siblings. Of course because of the recursive nature whenever a node was visited it followed the same steps until an ancestor was found. Which is why we used a boolean variable to determine whether the search was complete.

This was basically the algorithm that would enable us to do ancestor lookups based on their ID. 

It was therefore used in pretty much all of the base functions that would require this functionality, such as printing the specific ancestor we are looking for and his immediate tree, adding a first child (or siblings to the first child) to an ancestor or adding a partner. 

Main

From then on we simply had to create a Menu to put it all together, and create the appropriate exceptions for when the user tries to input something that is not appropriate to what we want. 

We used switch-case for the Menu Logic and the Scanner class from java.util.Scanner for the Input handling! 
