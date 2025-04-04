

2025-03-22 
05:09 PM


Tags: [[Discrete Math]], [[Function & Relations]], [[Proof Techniques]], [[Integer Properties]], [[Number Theory]], [[Graph Theory]], [[Partial Order]]


## Reference:![[Screenshot 2025-03-22 at 5.14.00 PM.png]]


## Integer Properties:


##### Computing Values of MOD operations

Definition:
- Modulus Operation (mod):
	- The modulus operator (denoted as a % b OR a MOD b), computes the REMAINDER when one integer is divided by another. It is often represented as:                                                                                      a MOD n         OR          a % n                                                            where:
		- **a** is the **dividend** (the number being divided).
		- **n** is the **divisor** (the number by which **a** is divided).

Explanation:
- Concept 
	- The **mod** operation determines the remainder left over when **a** is divided by **n**. It is essential in fields such as number theory, computer science, and cryptography.
- Mathematical Relationship
	- The division algorithm states that for any integers **a** and **n** (with **n > 0**), there exist unique integers **q** (the quotient) and **r** (the remainder) such that:                                                                         **a = n × q + r**, with **0 ≤ r < n**.
- Programming Note:
	- In many programming languages, the modulus operator is represented by the **%** symbol. For example, in Python, `17 % 5` evaluates to **2**.

Formulas and Equations:
- Basic Formula
	- a mod n = r                                                                                                                               where,
		- **a:** Dividend.
		- **n:** Divisor.
		- **r:** Remainder, satisfying **0 ≤ r < n**.

- Division Equation:
	- a = n × q + r                                                                                                                                    where,
		- **q:** Quotient (result of integer division).
		- **r:** Remainder (result of the mod operation).

- Mod Operation Formula:
	- a mod n = a - n × floor(a / n)                                                                                                         where,
		- **a**: Dividend (the number to be divided).
		- **n**: Divisor (the number by which a is divided).
		- **floor(a / n)**: The floor of the quotient a / n, i.e., the largest integer less than or equal to a / n.

- Labeled Formulas:
	-  ![[IMG_C58D22467DD3-1.jpeg]]
	- ![[IMG_6BCF37682614-1.jpeg]]

- Examples:
	- ![[IMG_71B26AC0D186-1.jpeg]]




##### Convert a Given Number to the Asked Number Base

Definition:
- Number Base Conversion:
	- The process of changing a number from one **numeral system** (or base) to another. For example, converting a number from **decimal** (base 10) to **binary** (base 2), **octal** (base 8), or **hexadecimal** (base 16).
- Base (Radix):
	- The total number of unique digits, including zero, that a numeral system uses. For instance:
		- **Decimal (Base 10):** Uses digits 0–9.
		- **Binary (Base 2):** Uses digits 0 and 1.
		- **Hexadecimal (Base 16):** Uses digits 0–9 and letters A–F.\

Examples:
- ![[IMG_AD671D21D92C-1.jpeg]]




##### Finding the LCM and GCD of Numbers

Definition:
- Greatest Common Divisor (GCD):
	- The **GCD** of two or more integers is the largest integer that divides each of the numbers without leaving a remainder. It is also known as the **Greatest Common Factor (GCF)** or **Highest Common Factor (HCF)**.
- Least Common Multiple (LCM):
	- The **LCM** of two or more integers is the smallest integer that is a multiple of each of the numbers.

Explanation:
- GCD (Greatest Common Divisor):
	- **Purpose:** To find the largest number that evenly divides a set of numbers.
	- **Method:** Often computed using the **Euclidean Algorithm**, which involves iterative division.
		- The Euclidean Algorithm is a method for finding the greatest common divisor (GCD) of two integers efficiently. 
		- The algorithm is as follows: 
			- GCD(a, b) = GCD(b, a  mod b)
				- This means that instead of working with a and b, we replace a with b and replace b with a mod b (the remainder when a is divided by b).
				- In the Euclidean Algorithm, we typically set up the gcd computation as gcd(larger number, smaller number) to ensure that when we apply the modulo operation, the remainder calculation works correctly without needing extra steps.
				- Repeat the process until b = 0, at which point a is the GCD.
	- **Key Point:** For any two numbers, the GCD is a measure of their shared factors.
- LCM (Least Common Multiple):
	- **Purpose:** To determine the smallest common multiple shared by a set of numbers.
	- **Method:** Can be computed using the relationship between the LCM and GCD for two numbers, or by listing multiples.
	- **Key Point:** The LCM is useful for problems involving synchronization of cycles, adding fractions, and solving problems with periodic events.

Formulas & Equations:
- Relationship Between LCM and GCD (for two numbers, a and b):
	- a × b = GCD(a, b) × LCM(a, b)                                                                                                      where,
		- **a, b:** The two integers.
		- **GCD(a, b):** The greatest common divisor of a and b.
		- **LCM(a, b):** The least common multiple of a and b.
- Euclidean Algorithm for GCD:
	- **Step 1:** If **b = 0**, then **GCD(a, b) = a**.
	- **Step 2:** Otherwise, compute **GCD(b, a mod b)**.
	- **Repeat:** Continue the process until the remainder is 0.
- Formula for LCM Using GCD:
	- LCM(a, b) = (a × b) / GCD(a, b)

Examples:
-  ![[GCDLCMexamples.pdf]]



##### Congruency (x congruent to y mod n)

Definition: 
- Congruency:
	- Two integers **x** and **y** are said to be **congruent modulo n** (written as **x ≡ y (mod n)**) if their difference **(x - y)** is divisible by the positive integer **n**.
		- Mathematically:                                                                                                                                           **x ≡ y (mod n)** if and only if **n** divides **(x - y)**
		  OR                                                                                                                                                                x ≡ y (mod n)   ⇔   n | (x - y)                                                                         where:
			- **x:** First integer.
			- **y:** Second integer.
			- **n:** The modulus (a positive integer).
			- **n | (x - y):** Reads as "n divides (x - y)", indicating there exists an integer **k** such that **x - y = n × k**.
		- ![[IMG_D25A13194B5D-1.jpeg]]

Explanation:
- Concept Overview:
	- Modular Arithmetic:
	  Congruency is a key concept in modular arithmetic, where numbers "wrap around" after reaching a certain value **n**.
	- Equivalence Relation:
	  The relation **x ≡ y (mod n)** is an equivalence relation, meaning it is:
		- **Reflexive:** Every number is congruent to itself (x ≡ x (mod n)).
		- **Symmetric:** If x ≡ y (mod n), then y ≡ x (mod n).
		- **Transitive:** If x ≡ y (mod n) and y ≡ z (mod n), then x ≡ z (mod n).
- Key Points: 
	- Divisibility:
	  The statement **n divides (x - y)** means there exists an integer **k** such that:                                                                         x - y = n × k
	- Same Remainder:
	  Alternatively, **x** and **y** are congruent modulo **n** if they yield the same remainder when divided by **n**.

Examples:
- ![[CongruencyExamples.pdf]]




## Proofs:


##### Proof Techniques: Direct, Contrapositive, Contradiction, and Cases

Definition:
- Direct Proof:
	- A method where you start with known facts or assumptions and logically deduce the conclusion using definitions, axioms, and previously established theorems.
- Proof by Contrapositive::
	- An indirect method that proves an implication **P → Q** by demonstrating that its contrapositive **(¬Q → ¬P)** is true.
- Proof by Contradiction:
	- An approach that assumes the negation of the statement to be proven and shows that this assumption leads to a logical contradiction, thereby proving the original statement.
- Proof by Cases:
	- A strategy that involves breaking the proof into several distinct cases that together cover all possible scenarios. The statement is then proven for each case individually.

Explanation:
- Direct Proof:
	- **Approach:** Begin with the hypothesis and use a series of logical steps to arrive at the conclusion.
	- **Key Idea:** Demonstrates the truth of a statement by straightforward reasoning.
- Proof by Contrapositive:
	- **Approach:** Instead of proving **P → Q** directly, prove **¬Q → ¬P**.
	- **Key Idea:** Since an implication is logically equivalent to its contrapositive, establishing the latter validates the original statement.
- Proof by Contradiction:
	- **Approach:** Assume that the statement is false and derive a contradiction from that assumption.
	- **Key Idea:** The emergence of a contradiction implies that the original assumption (that the statement is false) is untenable, so the statement must be true.
- Proof by Cases:
	- **Approach:** Divide the problem into a finite number of cases that cover all possibilities, and prove the statement in each case.
	- **Key Idea:** When each case confirms the statement, the overall statement is true regardless of which case applies.

Proof Structure:
- While these proof methods do not have "formulas" in the conventional sense, they follow specific logical structures:
	- Direct Proof Structure:
		1. Assume **P** (the hypothesis).
		2. Use logical steps to derive **Q** (the conclusion).
	- Contrapositive Proof Structure:
		1. Assume **¬Q** (the negation of the conclusion).
		2. Deduce **¬P** (the negation of the hypothesis).
		3. Conclude that **P → Q** is true since **¬Q → ¬P** is established.
	- Proof by Contradiction Structure:
		1. Assume **¬S** (the negation of the statement **S** to be proven).
		2. Derive a contradiction (e.g., **A** and **¬A**).
		3. Conclude that **S** must be true.
	- Proof by Cases Structure:
		1. Identify all possible cases that exhaust the possibilities (e.g., **Case 1**, **Case 2**, etc.).
		2. Prove the statement for each individual case.
		3. Conclude that the statement is universally true.

Examples:
- ![[ProofTechExamples.pdf]] 

Summary:

 - Direct Proof:
	 - Proves a statement by a straightforward chain of logical reasoning from hypothesis to conclusion.
- Proof by Contrapositive:
	- Validates an implication by proving the contrapositive; since an implication and its contrapositive are logically equivalent, this method is often simpler.
- Proof by Contradiction:
	- Assumes the negation of the desired conclusion and shows that this assumption leads to a contradiction, thereby affirming the truth of the original statement.
- Proof by Cases:
	- Divides the problem into separate, exhaustive cases and proves the statement individually for each case.




## Relations / Digraphs:


##### Arrow Diagrams

Definition:
- Arrow Diagrams:
	- A visual tool used to represent **functions** or **relations** between two sets. In an arrow diagram, each element of the **domain** is connected by an arrow to an element of the **codomain**, illustrating how elements are mapped or related.

Explanation:
- Purpose and Usage:
	- **Visualization:** Arrow diagrams simplify the understanding of abstract mathematical concepts by visually showing the mapping between elements of two sets.
	- **Functions and Relations:** They are commonly used to represent **functions**, where each element in the domain has a unique corresponding element in the codomain, as well as more general **relations** which might not have a unique pairing.
- Key Components:
	- Domain:
		- The set of all input values. In the diagram, these are typically displayed on the left side.
	-  Codomain/Range:
		- The set of possible output values. These are usually shown on the right side.
	- Arrows:
		- Lines connecting elements from the domain to the codomain. Each arrow represents an ordered pair (a, f(a)) in a function or a relationship between elements in a relation.
- Characteristics in Functions:
	- **One-to-One (Injective):** Each element in the domain maps to a unique element in the codomain.
	- **Many-to-One:** Different elements in the domain can map to the same element in the codomain.
	- **Onto (Surjective):** Every element in the codomain is mapped by at least one element in the domain.
	- **One-to-One Correspondence (Bijective):** The function is both one-to-one and onto.

Formulas & Equations:
- Function Notation:
	- A function represented in an arrow diagram can be denoted as:                                                                                    f: A → B                                                                                                    where:
		- **f:** Represents the function.
		- **A:** The **domain** (set of inputs).
		- **B:** The **codomain** (set of outputs).
		- Each arrow corresponds to a pair (a, f(a)) where a belongs to A
	- ![[IMG_DE5A1057037E-1 2.jpeg]]

Examples:
- ![[ArrowDiagramsExamples.pdf]]

Summary:
- **Arrow Diagrams** are an effective **visual representation** of functions and relations.
- They help illustrate how each element of the **domain** is mapped to an element of the **codomain** using arrows.
- **Key concepts** include the understanding of one-to-one, many-to-one, and onto mappings.
- These diagrams are widely used in **mathematics** and **logic** to facilitate comprehension and analysis of abstract relationships.




##### Determining the Properties of a Given Relation

Definition:
- Relation
	- A relation **R** on a set **A** is a collection of ordered pairs **(a, b)** where **a** and **b** are in **A**.
	- **(a, b) is in R** means “a is related to b.”
- Reflexive
	- A relation **R** is reflexive if every element in **A** is related to itself.
	- For all **a** in **A**, (**a**, **a**) is in **R**.
	- **For all a, b in A** means we consider every possible choice of a and b from the set A.
	- ∀a ∈ A, (a, a) ∈ R
- Symmetric
	- A relation **R** is symmetric if whenever an element **a** is related to **b**, then **b** is also related to **a**.
	- For all **a**, **b** in **A**, if (**a**, **b**) is in **R**, then (**b**, **a**) is in **R**.
	- **If (a, b) is in R, then (b, a) is in R** captures the idea of symmetry: a relates to b implies b relates to a.
	- ∀a, b ∈ A, (a, b) ∈ R ⇒ (b, a) ∈ R
- Anti-symmetric
	- A relation **R** is anti-symmetric if, for all **a** and **b** in **A**, whenever **a** is related to **b** and **b** is related to **a**, then **a** equals **b**.
	- For all **a**, **b** in **A**, if (**a**, **b**) is in **R** and (**b**, **a**) is in **R**, then **a** = **b**.
	- **If (a, b) is in R and (b, a) is in R, then a = b** enforces that no two distinct elements can be mutually related, which is anti-symmetry.
	- ∀a, b ∈ A, ( (a, b) ∈ R and (b, a) ∈ R) ) ⇒ a = b
- Transitive
	- A relation **R** is transitive if whenever an element **a** is related to **b** and **b** is related to **c**, then **a** is also related to **c**.
	- For all **a**, **b**, **c** in **A**, if (**a**, **b**) is in **R** and (**b**, **c**) is in **R**, then (**a**, **c**) is in **R**.
	- **If (a, b) is in R and (b, c) is in R, then (a, c) is in R** says that transitivity “passes” the relation along a chain of elements.
	- ∀a, b, c ∈ A, (a, b) ∈ R and (b, c) ∈ R ⇒ (a, c) ∈ R

Explanation:
- Understanding Relations:
	- A relation can be thought of as a rule that assigns a relationship between elements of a set. The properties of a relation determine how elements interact within that set.
- Key Concepts:
	- Reflexivity:
		- Every element must "loop back" to itself. This property ensures that the relation includes the pairs (a, a) for all **(a, b) is in R**
		- ∀a ∈ A, (a, a) ∈ R
	- Symmetry:
		- The relation works in both directions. If a is connected to b, then b must also be connected to a.
		- ∀a, b ∈ A, (a, b) ∈ R ⇒ (b, a) ∈ R
	- Anti-symmetry:
		- This property restricts the possibility of having distinct elements mutually related. If both (a, b) and (b, a) are in the relation, then it forces a and b to be the same element.
		- ∀a, b ∈ A, ( (a, b) ∈ R and (b, a) ∈ R) ) ⇒ a = b
	- Transitivity:
		- The relation "passes through" connected elements. If a is related to b and b is related to c, then there must be a direct relation from a to c.
		- ∀a, b, c ∈ A, (a, b) ∈ R and (b, c) ∈ R ⇒ (a, c) ∈ R

Formulas and Equations:
- **Reflexivity**: ∀a ∈ A, (a, a) ∈ R
	- ![[IMG_27E8F356733D-1.jpeg]]
	
- **Symmetry**: ∀a, b ∈ A, (a, b) ∈ R ⇒ (b, a) ∈ R
	- ![[IMG_BB1EFFCF2614-1.jpeg]]
	
- **Anti-Symmetry**: ∀a, b ∈ A, ( (a, b) ∈ R and (b, a) ∈ R) ) ⇒ a = b
	- ![[IMG_F36EA5D85509-1.jpeg]]
	
-  **Transitivity**: ∀a, b, c ∈ A, ( (a, b) ∈ R and (b, c) ∈ R) ) ⇒ (a, c) ∈ R
	- ![[IMG_456DE1A5CA36-1.jpeg]]

Examples:
- ![[DPoGRExamples.pdf]]




##### Walks, Trails, Circuits, Paths, and Cycles

Definition:
- Walk:
	- A walk in a graph is any sequence of vertices and edges where vertices and edges may be repeated.
	- Notation:
	  W = (v₀, e₁, v₁, e₂, …, eₖ, vₖ)                                                                                                           where,
		- v = vertice
		- e = edge
- Trail:
	- A trail is a walk with the restriction that no edge is repeated (vertices may be repeated).
	- Key point: Each edge appears at most once.
- Path:
	- A path is a trail where no vertex is repeated (which implies no edge is repeated).
	- This is also known as a simple path.
- Circuit:
	- A circuit is a trail that starts and ends at the same vertex (i.e., it is closed), with all edges distinct.
	- The only repeated vertex is the starting/ending vertex.
- Cycle:
	- A cycle is a closed path, meaning it is a circuit where, except for the starting/ending vertex, all vertices (and edges) are distinct.
	- It represents a loop with no repetition aside from the start/end vertex.

Explanation:
- Walks:
	- Structure: A sequence v₀, v₁, …, vₖ such that for each consecutive pair (vᵢ, vᵢ₊₁) there is an edge in the graph.
	- Flexibility: Vertices and edges may be repeated.
	- Usage: Used to explore connectivity and distances in graphs.
- Trails:
	- Restriction: Each edge is used only once.
	- Difference from Walks: Vertices may repeat, but edges cannot.
	- Usage: Useful when analyzing unique routes through a graph.
- Paths:
	- Restriction: Neither vertices nor edges are repeated.
	- Significance: Represents a straightforward, simple route between two vertices.
	- Usage: Essential for finding shortest paths and establishing connectivity without cycles.
- Circuits:
	- Characteristic: A trail that returns to the starting vertex, forming a closed loop.
	- Restriction: All edges are distinct, though the starting vertex is repeated.
	- Usage: Important in detecting cycles in networks.
- Cycles:
	- Characteristic: A circuit with the additional restriction that, aside from the starting/ending vertex, no vertex is repeated.
	- Usage: Crucial for identifying loops in graphs.

Formulas:
- Walk Representation:
	- W = (v₀, e₁, v₁, e₂, …, eₖ, vₖ)
		- - vᵢ: vertices in the sequence
		- eᵢ: edges connecting vᵢ₋₁ and vᵢ
- Trail Condition:
	- For a trail T:
	  eᵢ ≠ eⱼ for all i ≠ j
- Path Condition:
	- For a path P:
	  vᵢ ≠ vⱼ for all i ≠ j
- Circuit/Cycle Representation:
	- A closed trail or path is represented as:
	  C = (v₀, e₁, v₁, …, eₖ, v₀)
		- Circuit: Requires all edges (eᵢ) to be distinct.
		- Cycle: Additionally requires all vertices (except the starting/ending vertex) to be distinct.

Examples:
- **Example 1: Walk in a Graph**  
    Scenario: Consider a graph with vertices A, B, C and edges AB, BC, CA.  
    Walk Example: A → B → C → A → B  
    Explanation: This sequence is a walk because it may repeat vertices (like A and B) and edges.
- **Example 2: Trail in a Graph**  
    Scenario: Using the same graph with vertices A, B, C and edges AB, BC, CA.  
    Trail Example: A → B → C → A  
    Explanation: This is a trail because no edge is repeated, even though vertex A appears twice (start and end).
- **Example 3: Path in a Graph**  
    Scenario: Consider a graph with vertices A, B, C, D and edges AB, BC, CD.  
    Path Example: A → B → C → D  
    Explanation: This is a path since all vertices and edges are distinct.
- **Example 4: Circuit in a Graph**  
    Scenario: Consider a graph with vertices X, Y, Z and edges XY, YZ, ZX.  
    Circuit Example: X → Y → Z → X  
    Explanation: This is a circuit because it forms a closed trail: it starts and ends at X with no repeated edges.
- **Example 5: Cycle in a Graph**  
    Scenario: Consider a graph with vertices P, Q, R, S forming a square with edges PQ, QR, RS, SP.  
    Cycle Example: P → Q → R → S → P  
    Explanation: This is a cycle as it is a closed path with all vertices (except the repeated P) being distinct.

Summary:
- **Walk:**  
    Any sequence of vertices and edges; repetition is allowed.
- **Trail:**  
    A walk with no repeated edges.
- **Path:**  
    A trail with no repeated vertices; represents a simple route.
- **Circuit:**  
    A closed trail (starts and ends at the same vertex) with no repeated edges.
- **Cycle:**  
    A closed path (circuit) with no repeated vertices (other than the starting/ending vertex).




##### Finding the Output of Composition of Relations

Definition:
- **Composition of Relations:**  
    Given two relations R and S, where
    - R is a relation from set A to set B (i.e., R ⊆ A × B), and
    - S is a relation from set B to set C (i.e., S ⊆ B × C),  
        the composition of R and S is a relation from A to C. It is denoted by S ∘ R and defined as:
    S ∘ R = { (a, c) | ∃ b ∈ B such that (a, b) ∈ R and (b, c) ∈ S }
- **Key Idea:**  
    An element a from set A is related to an element c in set C if there is an intermediate element b in B connecting them via R and S.

Explanation:
- **Process of Composition:**
    1. Start with an ordered pair (a, b) from the relation R.
    2. For the same b, find all ordered pairs (b, c) in the relation S.
    3. For each matching b, include the ordered pair (a, c) in S ∘ R.
- **Important Concepts:**
    - **Intermediate Element:**  
        b is the "bridge" connecting a and c.
    - **Output Relation:**  
        The resulting relation S ∘ R consists of all pairs (a, c) that can be connected through some b in the intermediate set.

Forumula:
- **Composition Formula:**  
	S ∘ R = { (a, c) | ∃ b ∈ B such that (a, b) ∈ R and (b, c) ∈ S }
	where:
	- a: Element from the domain of R (set A).
	- b: Intermediate element in the codomain of R and the domain of S (set B).
	- c: Element from the codomain of S (set C).

Examples:
- **Example 1: Numerical Relations**
    - **Given:**  
        R = { (1, 2), (2, 3), (3, 4) }  
        S = { (2, 5), (3, 6), (4, 7) }
    - **Process:**
        - For (1, 2) in R:  
            Look for pairs in S with first element 2.  
            (2, 5) is found, so include (1, 5) in S ∘ R.
        - For (2, 3) in R:  
            Look for pairs in S with first element 3.  
            (3, 6) is found, so include (2, 6) in S ∘ R.
        - For (3, 4) in R:  
            Look for pairs in S with first element 4.  
            (4, 7) is found, so include (3, 7) in S ∘ R.
    - **Result:**  
        S ∘ R = { (1, 5), (2, 6), (3, 7) }
- **Example 2: Relations with Multiple Outputs**
    - **Given:**  
        R = { (a, b), (a, c) }  
        S = { (b, x), (c, y), (c, z) }
    - **Process:**
        - For (a, b) in R:  
            Look for pairs in S with first element b.  
            (b, x) is found, so include (a, x) in S ∘ R.
        - For (a, c) in R:  
            Look for pairs in S with first element c.  
            (c, y) and (c, z) are found, so include (a, y) and (a, z) in S ∘ R.
    - **Result:**  
        S ∘ R = { (a, x), (a, y), (a, z) }
- **Example 3: Graphical Representation**
    - **Scenario:**  
        Consider sets:  
        A = {1, 2}, B = {3, 4}, C = {5, 6}  
        Relations:  
        R = { (1, 3), (2, 4) }  
        S = { (3, 5), (3, 6), (4, 6) }
    - **Process:**
        - For (1, 3) in R:  
            Look for pairs in S with first element 3.  
            Both (3, 5) and (3, 6) are present, so include (1, 5) and (1, 6) in S ∘ R.
        - For (2, 4) in R:  
            Look for pairs in S with first element 4.  
            (4, 6) is found, so include (2, 6) in S ∘ R.
    - **Result:**  
        S ∘ R = { (1, 5), (1, 6), (2, 6) }

Summary:
- **Composition of Relations** involves connecting two relations by finding common intermediate elements.
- **Key Steps:**
    - Identify the ordered pairs in the first relation R.
    - For each pair (a, b) in R, find all pairs (b, c) in S.
    - The output is the set of all pairs (a, c) such that there is a connecting element b.
- **Formula Recap:**  
    S ∘ R = { (a, c) | ∃ b ∈ B such that (a, b) ∈ R and (b, c) ∈ S }
- **Applications:**  
    This concept is essential in mathematics and computer science for understanding relations, function composition, and even database queries.




##### Checking the Properties of a Partial Order and an Equivalence Relation


###### Partial Order

Definition:
- **Partial Order:**  
	A relation R on a set A is a partial order if it satisfies three properties:
	- **Reflexive:** For every a ∈ A, (a, a) ∈ R.
	- **Anti-symmetric:** For all a, b ∈ A, if (a, b) ∈ R and (b, a) ∈ R, then a = b.
	- **Transitive:** For all a, b, c ∈ A, if (a, b) ∈ R and (b, c) ∈ R, then (a, c) ∈ R.

Additional Concepts:
- **Minimal Element:**  
    An element m ∈ A is minimal if there is no element a ∈ A (with a ≠ m) such that (a, m) ∈ R.
- **Maximal Element:**  
    An element M ∈ A is maximal if there is no element a ∈ A (with a ≠ M) such that (M, a) ∈ R.

Formulas:
- **Reflexivity:**  
    ∀ a ∈ A, (a, a) ∈ R.
- **Anti-symmetry:**  
    ∀ a, b ∈ A, ( (a, b) ∈ R and (b, a) ∈ R ) )⇒ a = b.
- **Transitivity:**  
    ∀ a, b, c ∈ A, ( (a, b) ∈ R and (b, c) ∈ R ) )⇒ (a, c) ∈ R.
- **Minimal Element:**  
    m ∈ A is minimal if ¬∃ a ∈ A such that (a, m) ∈ R and a ≠ m.
- **Maximal Element:**  
    M ∈ A is maximal if ¬∃ a ∈ A such that (M, a) ∈ R and a ≠ M.

Examples:
- **Example 1: Total Order on Numbers**  
    Scenario: Let A = {1, 2, 3} with the relation ≤ (usual "less than or equal to").  
    Steps:
    - Reflexivity: 1 ≤ 1, 2 ≤ 2, 3 ≤ 3.
    - Anti-symmetry: If a ≤ b and b ≤ a, then a = b.
    - Transitivity: If a ≤ b and b ≤ c, then a ≤ c.
    - Minimal Element: 1 (no element is less than 1).
    - Maximal Element: 3 (no element is greater than 3).  
        Conclusion: ≤ on {1, 2, 3} is a partial order.
- **Example 2: Subset Relation**  
    Scenario: Let A = P({1,2}) = {∅, {1}, {2}, {1,2}} with the relation ⊆.  
    Steps:
    - Reflexivity: Every subset is a subset of itself.
    - Anti-symmetry: If X ⊆ Y and Y ⊆ X, then X = Y.
    - Transitivity: If X ⊆ Y and Y ⊆ Z, then X ⊆ Z.
    - Minimal Element: ∅ (no subset is strictly contained in ∅).
    - Maximal Element: {1,2} (no subset strictly contains {1,2}).  
        Conclusion: ⊆ is a partial order on P({1,2}).


###### Equivalence Relation

Definition:
- **Equivalence Relation:**  
	A relation ~ on a set A is an equivalence relation if it satisfies:
	- **Reflexive:** For every a ∈ A, a ~ a.
	- **Symmetric:** For all a, b ∈ A, if a ~ b, then b ~ a.
	- **Transitive:** For all a, b, c ∈ A, if a ~ b and b ~ c, then a ~ c.

Formulas:
- - **Reflexivity:**  
    ∀ a ∈ A, a ~ a.
- **Symmetry:**  
    ∀ a, b ∈ A, (a ~ b) ⇒ (b ~ a).
- **Transitivity:**  
    ∀ a, b, c ∈ A, ( (a ~ b) and (b ~ c) ) ⇒ a ~ c.

Examples:
- **Example 3: Congruence Modulo n**  
    Scenario: Define a relation on the set of integers where a ~ b if a ≡ b (mod n).  
    Steps:
    - Reflexivity: For any integer a, a - a = 0, which is divisible by n.
    - Symmetry: If a - b is divisible by n, then b - a is also divisible by n.
    - Transitivity: If a ≡ b (mod n) and b ≡ c (mod n), then a ≡ c (mod n).  
        Conclusion: Congruence modulo n is an equivalence relation.
- **Example 4: Same Remainder When Divided by 3**  
    Scenario: Define a ~ b on integers if they leave the same remainder when divided by 3.  
    Steps:
    - Reflexivity: Every integer has the same remainder as itself.
    - Symmetry: If a and b have the same remainder, then b and a do as well.
    - Transitivity: If a and b have the same remainder, and b and c have the same remainder, then a and c have the same remainder.  
        Conclusion: This relation is an equivalence relation.


Summary:
- **Partial Order Properties:**
    - Reflexive: ∀ a ∈ A, (a, a) ∈ R
    - Anti-symmetric: ∀ a, b ∈ A, ( (a, b) ∈ R and (b, a) ∈ R ) ⇒ a = b
    - Transitive: ∀ a, b, c ∈ A,  ( (a, b) ∈ R and (b, c) ∈ R) ) ⇒ (a, c) ∈ R
    - Minimal/Maximal Elements: Determined by checking for the absence of elements preceding (minimal) or following (maximal) a given element.
- **Equivalence Relation Properties:**
    - Reflexive: ∀ a ∈ A, a ~ a
    - Symmetric: ∀ a, b ∈ A, (a ~ b) ⇒ (b ~ a)
    - Transitive: ∀ a, b, c ∈ A, ( (a ~ b) and (b ~ c) ) ⇒ a ~ c


































  








