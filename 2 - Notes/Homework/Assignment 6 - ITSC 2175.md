

2025-03-19 
10:38 PM


Tags: [[Discrete Math]], [[Proof Techniques]], [[Number Theory]], [[Function & Relations]], [[Graph Theory]] 


## Reference: 
https://webwork3.charlotte.edu/webwork2/ITSC2175AR/HW6/1/?effectiveUser=rahmed6


#### Problem 1:
![[Screenshot 2025-03-19 at 10.47.15 PM.png]]
###### Understanding the problem statement:
The problem is asking to prove a statement by contradiction:
- Original Statement (given in the problem): There exist NO integers a and b for which 21a + 30b = 1:
	- This means that the equation can never be satisfied no matter what integer values of a and b we choose. 
- Proof by Contradiction Approach (the problem asks us to take this approach):
	- We assume the OPPOSITE is TRUE to prove this statement and show that it leads to a contradiction. 
- Opposite (Negation) of the Statement: 
	- The opposite of "There exist NO integers a and b for which 21a + 30b = 1" is:
	- "There EXISTS integers a and b such that 21a + 30b = 1"
- Step-by-Step Process of Proof by Contradiction in this problem:
	- ASSUME that 21a+30b = 1 IS POSSIBLE
	- SHOW why this is IMPOSSIBLE using mathematical reasoning.
	- CONCLUDE that our assumption was WRONG, meaning the original statement must be TRUE

###### Defining Key Concepts Present in this Problem:
1. Linear Diophantine Equations:
	- An equation of the form ax + by = d is called a Linear Diophantine Equation
	- It has integer solutions IF AND ONLY IF the greatest common divisor (GCD) of a and b DIVIDES d.
2. Greatest Common Divisor (GCD):
	- The GCD of two numbers is the largest integer that evenly divides both. 
	- if GCD(a, b) does NOT divide d, then the equation ax + by = d has NO INTEGER SOLUTIONS
3. Euclidian Algorithm:
	- The Euclidean Algorithm is a method for finding the greatest common divisor (GCD) of two integers efficiently. 
	- The algorithm is as follows: GCD(a, b) = GCD(b, a  mod b)
		- This means that instead of working with a and b, we replace a with b and replace b with a mod b (the remainder when a is divided by b).
		- In the Euclidean Algorithm, we typically set up the gcd computation as gcd(larger number, smaller number) to ensure that when we apply the modulo operation, the remainder calculation works correctly without needing extra steps.
		- Repeat the process until b = 0, at which point a is the GCD.
		- Example: ![[Screenshot 2025-03-19 at 11.41.13 PM.png]]

###### Solving Problem 1: ![[IMG_6F0C87F005A2-1.jpeg]]
The correct answer is answer choice C based on the screenshot: "**There exist integers a and b for which 21a + 30b = 1**"

Final Notes For Problem 1:
 - **Proof by contradiction** is useful when proving something is **impossible**.
 - **Linear Diophantine equations** have solutions, if and only if, gcd(a, b) divides d.
 - The **Euclidean Algorithm** helps efficiently compute the **gcd** of two numbers.
 - When the gcd does not divide the right-hand side of the equation, then **no integer solutions exist**.



#### Problem 2:
![[Screenshot 2025-03-20 at 12.31.32 AM.png]]

##### How to Write a Proof for this Problem:

**Step 1: Understand the Statement to Prove**
- Before writing a proof, **read and understand** the statement.
- The given statement is:
	- "There exist no integers a and b for which 21a + 30b = 1."
- This means that no matter what values we choose for **a** and **b**, the equation **can never equal 1**.
- To prove this, we will use **proof by contradiction**. (as provided for us in the problem)

**Step 2: Assume the Opposite (Negation)**
- A **proof by contradiction** works by **assuming the opposite** of what we want to prove and showing that this assumption leads to a contradiction.
	- The **original statement** says: **No such integers a and b exist.**
	- The **opposite (negation)** is that integers a and b exist such that 21a + 30b = 1.**
- So, in the proof, we start by saying:
	- **"Assume that there exist integers a and b such that 21a + 30b = 1."**

**Step 3: Identify the Necessary Condition for a Solution**
- This equation is a **Linear Diophantine Equation** of the form: ax + by = d
- For **ax + by = d** to have integer solutions, the **greatest common divisor (gcd)** of **a** and **b** must **divide** **d**.
- In this case, the equation is: 21a + 30b = 1
- For integer solutions to exist, **gcd(21, 30) must divide 1**.

**Step 4: Compute gcd(21, 30) Using the Euclidean Algorithm**
- The **Euclidean Algorithm** helps compute the gcd efficiently.
- We perform the following steps:
	- Compute **30 mod 21**:
		- 30 divided by 21 gives **remainder 9**.
		- So, gcd(30, 21) = gcd(21, 9).
	- Compute **21 mod 9**:
		- 21 divided by 9 gives **remainder 3**.
		- So, gcd(21, 9) = gcd(9, 3).
	- Compute **9 mod 3**:
		- 9 divided by 3 gives **remainder 0**.
		- Since remainder = 0, gcd(9, 3) = 3.
- Thus, **gcd(21, 30) = 3**.

**Step 5: Check for a Contradiction**
- We found that **gcd(21,30) = 3**.
- For the equation **21a + 30b = 1** to have integer solutions, **gcd(21,30) must divide 1**.
- But **3 does not divide 1**, meaning **it is impossible for 21a + 30b = 1 to have integer solutions**.
- This **contradicts** our assumption that integer values of **a** and **b** exist.

**Step 6: Conclusion**
- Since our assumption led to a contradiction, our **original statement must be true**:
- "There exist no integers a and b for which 21a + 30b = 1."
- We write "Thus, the proof is complete."


**Solving Problem 2:**
The following is the proof for problem 2:
"We will prove the statement "There exist no integers a and b for which 21a + 30b = 1" by contradiction.

Step 1: Assume the opposite.  
Assume that there exist integers a and b such that 21a + 30b = 1.

Step 2: Compute gcd(21, 30).  
Using the Euclidean Algorithm:

1. 30 divided by 21 gives a remainder of 9, so gcd(30, 21) = gcd(21, 9).
2. 21 divided by 9 gives a remainder of 3, so gcd(21, 9) = gcd(9, 3).
3. 9 divided by 3 gives a remainder of 0, so gcd(9, 3) = 3.

Thus, gcd(21,30) = 3.

Step 3: Check for a contradiction.  
For the equation 21a + 30b = 1 to have integer solutions, gcd(21,30) must divide 1. However, since 3 does not divide 1, no such integers a and b can exist.

Step 4: Conclusion.  
This contradicts our assumption that 21a + 30b = 1 has integer solutions. Therefore, the original statement is true: there exist no integers a and b for which 21a + 30b = 1.

Thus, the proof is complete."

Summary for Writing a Proof for Problem 2:
1. **Understand the Question:**
    - Identify whether you need to prove existence or non-existence.
    - If proving non-existence, consider proof by contradiction.
2. **Assume the Opposite of What You Want to Prove:**
    - Here, we assumed that there do exist integers a and b such that 21a + 30b = 1.
3. **Use Mathematical Properties to Derive a Contradiction:**
    - We used the gcd property: If gcd(m, n) = d, then any integer combination of m and n must be divisible by d.
4. **Show the Contradiction Clearly:**
    - We showed that the left-hand side was always a multiple of 3, while the right-hand side was not.
5. **Conclude by Stating That the Assumption Was False:**
    - Since assuming the existence of such integers led to a contradiction, the original claim is true.



#### Problem 3:
![[Screenshot 2025-03-20 at 5.23.17 PM.png]]

###### Defining Key Concepts Present in this Problem:
1. Absolute Value:
	- For any real number y, the absolute value |y| is defined by:
		- |y| = { (y, if y >= 0) ,  (-y, if y < 0) }
	- |y| is the "distance" of y from 0 on the real number line
2. Proof by Cases:
	- A proof by cases strategy is where you split the problem into multiple scenarios aka "cases", ensuring those cases cover ALL possibilities. You then prove the statement in each case. If the statements holds in EVERY CASE, it holds in general; it holds for all real numbers in question.

###### Overall Strategy:
- We want to show that for EVERY real number x, the quantity |x - 6| + x is strictly greater than 3. 
- Notice that |x -6| depends on whether x - 6 is nonnegative or negative:
	- If x - 6 >= 0 (i.e., x >= 6), then |x - 6| = x - 6
	- If x - 6 < 0 (i.e., x < 6), then |x - 6| = -(x - 6) = 6 - x
- By considering these two cases separately, we can handle the absolute value in a straightforward way.


###### Proof by Cases:![[ProofbyCasesForProb3.pdf]]

###### Combining Cases:
- Case 1 covers all x >= 6, and in that range, |x - 6| + x > 3.
- Case 2 covers all x < 6, and in that range, |x - 6| + x = 6, which is also greater than 3.
- These two cases exhaust all possible real values of x. Therefore, for every real x, the statement |x - 6| + x > 3 is true.

###### Why This Works:
- Absolute Value "Splits" the Real Line: The expression |x - 6| changes form exactly at x = 6. This creates two "regions" to analyze. Proof by cases is the best way to handle such piecewise-defined functions.
- Each Case Must Be Proven Separately: We show the desired inequality in each region. Once both are confirmed, the statement holds everywhere.
- Key Insight: In Case 2, the sum |x - 6| + x simplifies to a constant (6), which is obviously greater than 3. In Case 1, the expression becomes 2x - 6, and because x >= 6, that expression easily surpasses 3.

###### Recap Main Ideas for Problem 3:
- Absolute value definition: |y| = y if y >= 0, and |y| = -y if y < 0.
- Proof by cases: Split the real line at the point where x - 6 = 0.
- Check each case thoroughly and conclude that the expression is greater than 3 in both scenarios.

**Solving Problem 3:**
![[Screenshot 2025-03-20 at 6.26.26 PM.png]]




#### Problem 4:
![[Screenshot 2025-03-20 at 6.28.42 PM.png]]

###### Key Definition: Cartesian Product:
- For two sets X and Y, their Cartesian product X * Y is defined as: 
	- X * Y = {(x, y) | x is in X, y is in Y}.
		![[IMG_DF278B66996D-1.jpeg]]
	- An ordered pair (a, b) is in X * Y if and only if:
		- a is an element of X, and
		- b is an element of Y.

###### The Sets A and B:
- We are given: A = {1, 2, 3}  and  B = {2, 6, 8}.
- Each question asks whether a particular ordered pair (x, y) is in certain Cartesian products.

###### How to Check if (x, y) is in a Cartesian Product:
- Identify the first coordinate x: It must be in the first set of the product.
- Identify the second coordinate y: It must be in the second set of the product.
- If both conditions are satisfied, (x, y) is in that Cartesian product. Otherwise, it is not.

**Solving Problem 4:**
Example of Solving the first part of Problem 4 (process goes the same with all the other (x, y) pairs:![[IMG_60FFB8B84C58-1.jpeg]]

Question 1 "Select all the cartesian products that (3, 6) is an element of." Correct Answer: D
- We want to see where (3, 6) can appear.
- For (3, 6) to be in X x Y, the set X must contain 3, and the set Y must contain 6.
- Only choice D has 3 in its first component set and 6 in its second component set.
- Therefore, (3, 6) is found only in D.
Question 2 "Select all the cartesian products that (8, 2) is an element of." Correct Answer: A and B (AB)
- For (8, 2) to be in X x Y, we need 8 in the first set X and 2 in the second set Y.
- Choices A and B both include 8 in their first component set and 2 in their second component set.
- Hence, (8, 2) belongs to A and B only.
Question 3 "Select all the cartesian products that (2, 2) is an element of." Correct Answer: A, B, C, and D (ABCD)
- For (2, 2) to be in X x Y, the first set X must contain 2, and the second set Y must contain 2.
- All four products (A, B, C, D) have 2 in the first component set and 2 in the second component set.
- Therefore, (2, 2) is in all of them.
Question 4 "Select all the cartesian products that (1, 1) is an element of." Correct Answer: D
- For (1, 1) to be in X x Y, the first set X must contain 1, and the second set Y must contain 1.
- Only the product labeled D has 1 in its first set and 1 in its second set.
- Thus, (1, 1) appears only in D.
![[Screenshot 2025-03-20 at 11.36.49 PM.png]]




#### Problem 5: 
![[Screenshot 2025-03-20 at 11.38.23 PM.png]]

###### Key Definition: Cartesian Product:
- For two sets X and Y, their Cartesian product X * Y is defined as: 
	- X * Y = {(x, y) | x is in X, y is in Y}.
- This means:
	- The **first** element of each ordered pair comes from X.
	- The **second** element of each ordered pair comes from Y.

###### The Sets A and B:
- We are given 2 sets in this problem:
	- A = {g, y}
	- B = {3, 4, 5}
- We want to find:
	- A x B
	- B x A
	- A x A
	- B x B

**Solving Problem 5:**![[SolvingProblem5.pdf]]
Why These Answers Are Correct:
- Each Cartesian product is simply every possible ordered pair where the first element comes from the first set and the second element comes from the second set.
- The order in the pairs matters: A x B is different from B x A unless A = B.
- Listing them systematically ensures no pair is missed and no extra pair is added.

Recap: Step-by-Step Process:
- Identify the sets involved (for example, A and B).
- Recall the definition of the Cartesian product.
- Combine every element of the first set with every element of the second set.
- Check for completeness: make sure you have all possible pairs, and only those pairs that meet the membership criteria (first from the first set, second from the second set).

Using this method, we confirm the solutions:
- A x B = {(g,3), (g,4), (g,5), (y,3), (y,4), (y,5)}
- B x A = {(3,g), (3,y), (4,g), (4,y), (5,g), (5,y)}
- A x A = {(g,g), (g,y), (y,g), (y,y)}
- B x B = {(3,3), (3,4), (3,5), (4,3), (4,4), (4,5), (5,3), (5,4), (5,5)}




#### Problem 6:
![[Screenshot 2025-03-21 at 12.53.47 AM.png]]

The problem states:
- A = {13, 23, 28, 30, 60}.
- R = { (a, b) in A x A : a divides b }, where "a divides b" means a evenly divides b.

###### Key Concept: "a divides b":
- The statement "a divides b" means there is an integer c such that b = c * a. In other words, b is a multiple of a. ![[IMG_DFD2EED53281-1 2.jpeg]]
###### How to Determine Each Ordered Pair (a, b):
- Form the set A x A: all possible ordered pairs (a, b) with a in A and b in A.
- Check divisibility: For each pair (a, b), see if a divides b. If yes, (a, b) belongs to R. Otherwise, it does not.

###### Step-by-Step Summary:
1. List all pairs (a, b) in A x A.
2. Apply the "divides" test: does a divide b?
3. Keep only those pairs that satisfy the condition.
4. Explain each pair in terms of multiplication (b = c * a).

**Solving Problem 6:**![[SolvingProblem6.pdf]]
Solution: R = { (13,13),(23,23),(28,28),(30,30),(30,60),(60,60) }




#### Problem 7:![[Screenshot 2025-03-21 at 4.21.04 AM.png]]
We have a directed graph with vertices {1, 2, 3, 4}. Each directed edge corresponds to an ordered pair (a, b) in the relation R. Specifically, an arrow (edge) from vertex a to vertex b means (a, b) is in R.

###### Key Terms and Solving the Problem:
- In-degree of a vertex v: the number of incoming edges to v.
	- In the context of the problem, look at all arrows in the diagram and see which ones point **into** vertex 1.
	- From the final solution, the pairs that end in 1 are: (4,1) (3,1) (2,1)
	- There are exactly 3 such edges, so the in-degree of vertex 1 is **3**.
	- If you are looking at the digraph directly, you would see 3 arrows directed **toward** vertex 1.
- Out-degree of a vertex v: the number of outgoing edges from v.
	- Look at all arrows in the diagram and see which ones start **at** vertex 4.
	- From the final solution, the pairs that start with 4 ( i.e., (4, y) ) are: (4,1) (4,3)
	- There are exactly 2 such edges, so the out-degree of vertex 4 is **2**.
	- Visually, you would see 2 arrows leaving vertex 4 in the diagram.
- Relation on a set of vertices: the set of all ordered pairs (a, b) for which there is a directed edge from a to b.
	- A relation represented by a digraph is the set of all ordered pairs (a, b) for which there is a directed edge from a to b.

**Solving Problem 7:**![[ProblemSolving7.pdf]]
By following these steps, you arrive at the same answers:
- In-degree of vertex 1 is 3.
- Out-degree of vertex 4 is 2.
- R = {(1,4), (4,1), (1,3), (3,1), (2,1), (2,3), (3,3), (4,3)}.


