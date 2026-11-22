# Independent Coding + DSA Practice Plan (Weeks 1–4)

This file makes the daily 60-minute coding block and 30-minute DSA block concrete. It follows the existing 24-week `ROADMAP.md`; it does not replace that roadmap.

**Daily target:** 60 minutes independent coding + 30 minutes DSA.  
**Important:** A DSA problem is not "learned" merely because its code passed.

---

# Part A — How to use the 60-minute independent coding block

For each day:
1. Spend 5–10 minutes writing the input, expected output, rules and edge cases.
2. Code without copying a solution.
3. Compile and test.
4. If stuck, use this help ladder: explain the requirement in your own words → write pseudocode → use a small example by hand → consult a hint. Do not jump straight to a full solution.
5. After solving, change one requirement and update the program.

Use the exact daily assignments below. If the task takes less than 60 minutes, add the listed extension or test extra edge cases. Do not add unrelated advanced topics just to fill time.

# Part B — How to learn a DSA pattern (not memorise an answer)

For every DSA problem, write a short Pattern Note containing:

- **Problem clue:** What wording or input property made me consider this pattern?
- **Brute force:** What is the straightforward solution? What is its time complexity?
- **Pattern:** Which pattern am I testing (e.g. traversal, frequency map, two pointers)?
- **Core idea / invariant:** What remains true while the algorithm runs?
- **Why it works:** Explain in plain language why the steps find the answer.
- **Complexity:** Time and extra space, with a reason.
- **Edge cases:** Empty input, one element, duplicates, negatives, already sorted, etc. as relevant.
- **Variation:** What small change to the question would change the solution?
- **Recall test:** Close the solution and re-code or explain it the next day, then again after 3 and 7 days.

### The 30-minute DSA session

- 5 min: Understand the question and create examples.
- 5 min: Think of brute force and its complexity.
- 12 min: Try the pattern and code it.
- 5 min: Dry-run, edge cases and complexity.
- 3 min: Write the Pattern Note and one variation.

If you cannot solve it in 12 minutes, do not spend the whole session staring at it. Take one hint, finish understanding it, and schedule a blank-editor reattempt. Learning the reasoning is more important than pretending to solve it unaided.

---

# Week 1 — Java basics + array traversal

## Day 1 — Variables, types, operators, input/output
**Independent coding (60 min)**
- Program 1: Read two integers and print sum, difference, product and quotient.
- Program 2: Convert Celsius to Fahrenheit.
- Program 3: Calculate simple interest from principal, rate and time.
- Test: zero values, negative values, decimal input and division by zero (handle it safely).

**DSA (30 min)**
- Problem: Find the maximum element in an integer array.
- Pattern: Linear traversal / maintaining a running best.
- Variation: Find the minimum; then find both minimum and maximum in one traversal.
- Pattern Note: Explain why each element only needs to be visited once.

## Day 2 — if/else, switch, boolean logic
**Independent coding**
- Program 1: Check even or odd.
- Program 2: Check positive, negative or zero.
- Program 3: Find the largest of three numbers.
- Program 4: Build a grade calculator using marks and clear boundary rules.
- Extension: Use `switch` to build a small menu-driven calculator.

**DSA**
- Problem: Find the second-largest distinct element in an array.
- Pattern: Single-pass traversal with two tracked values.
- Variation: Return "not found" if there is no second distinct value.
- Explain why duplicates must not be mistaken for the second-largest distinct value.

## Day 3 — for, while, do-while
**Independent coding**
- Program 1: Print numbers from 1 to N.
- Program 2: Print the multiplication table of a number.
- Program 3: Calculate the sum of digits.
- Program 4: Reverse an integer.
- Test: N=0, negative number, number ending in zero; consider integer overflow.

**DSA**
- Problem: Reverse an array in place.
- Pattern: Two pointers from both ends (introductory use).
- Variation: Reverse only a selected range of indices.
- Explain why swapping the outer pair and moving inward works.

## Day 4 — Methods, parameters, return values, overloading
**Independent coding**
- Create methods for `isEven`, `maxOfThree`, `sumOfDigits` and `reverseNumber`.
- Create overloaded `calculateArea` methods for a rectangle and a circle.
- Refactor at least two programs from Days 1–3 to call methods.
- Test method inputs at boundaries.

**DSA**
- Problem: Move all zeroes to the end while preserving the order of non-zero elements.
- Pattern: Two pointers / write index.
- Variation: Move negative values to the beginning, preserving relative order if possible.
- State what the write index represents at every step.

## Day 5 — Arrays and traversal
**Independent coding**
- Program 1: Read N values and calculate sum and average.
- Program 2: Find minimum and maximum.
- Program 3: Count even and odd values.
- Program 4: Copy an array and compare two arrays.
- Extension: Find the index of a target value; handle target not found.

**DSA**
- Problem: Check whether an array is sorted in non-decreasing order.
- Pattern: Adjacent comparison / one-pass scan.
- Variation: Find the first index where sorted order is broken.
- Explain why comparing neighbours is sufficient.

## Day 6 — Strings and StringBuilder
**Independent coding**
- Program 1: Count vowels and consonants.
- Program 2: Reverse a string using `StringBuilder`.
- Program 3: Check whether a string is a palindrome (state how spaces/case are treated).
- Program 4: Count words in a sentence.
- Test: empty string, one character, mixed case, spaces and punctuation.

**DSA**
- Problem: Valid palindrome after ignoring non-alphanumeric characters and case.
- Pattern: Two pointers moving inward.
- Variation: Check a plain palindrome without ignoring punctuation.
- Explain what each pointer skips and when the pointers move.

## Day 7 — Weekly revision
**Independent coding**
- Rebuild from a blank editor: calculator, grade calculator and array min/max.
- Pick one earlier program and add validation.
- Explain each method without reading the code.

**DSA**
- Reattempt Days 1, 3 and 6 without looking at notes.
- Choose one: explain brute force vs pattern solution on paper.
- Weekly review: list patterns you can explain, not merely questions completed.

---

# Week 2 — OOP + array/string pattern consolidation

## Day 8 — Classes, objects, fields, methods, constructors
**Independent coding**
- Create `BankAccount` with account number, holder name and balance.
- Add constructor and `deposit`, `withdraw`, `getBalance` methods.
- Create two objects and show that their balances are independent.
- Test invalid deposit and withdrawal amounts.

**DSA**
- Problem: Remove duplicates from a sorted array in place; return the new logical length.
- Pattern: Two pointers / slow-write and fast-scan.
- Variation: Keep at most two occurrences of each value.
- Explain the role of the slow pointer and fast pointer.

## Day 9 — Encapsulation, access modifiers, this, static
**Independent coding**
- Make fields private and expose safe methods.
- Reject negative deposits and withdrawals larger than the balance.
- Add a static counter for created accounts.
- Add a method to transfer money between two accounts; test insufficient funds.

**DSA**
- Problem: Two Sum (return indices of two values adding to target).
- First explain the brute-force nested-loop approach.
- Then solve using a HashMap if ready; otherwise understand the lookup idea and implement it after the lesson.
- Variation: Return whether any pair exists, not the indices.
- Explain what the map stores and why lookup is useful.

## Day 10 — Inheritance, super, overriding
**Independent coding**
- Create base class `Employee` with name and salary.
- Create `Developer` and `Manager` subclasses.
- Override a method that calculates or displays role-specific information.
- Use `super` to call the parent constructor.
- Test each subclass independently.

**DSA**
- Problem: Best Time to Buy and Sell Stock (one buy, one later sell).
- Pattern: One-pass scan / running minimum and best-so-far.
- Variation: Return the buy and sell indices as well as profit.
- Explain why the buy day must come before the sell day.

## Day 11 — Polymorphism and dynamic dispatch
**Independent coding**
- Create `PaymentMethod` with a `pay` method.
- Implement `CardPayment`, `UpiPayment` and `NetBankingPayment`.
- Store different payment objects in a `PaymentMethod[]`.
- Loop through the array and call `pay`; explain which implementation runs and why.

**DSA**
- Problem: Maximum sum of a contiguous subarray (Kadane's algorithm).
- Pattern: Running best / dynamic programming on a one-dimensional sequence.
- Variation: Return the start and end indices of the best subarray.
- Explain the meaning of the current-ending-here sum and global best.

## Day 12 — Abstract classes and interfaces
**Independent coding**
- Create an interface `Notifiable` with `sendNotification`.
- Implement it in `EmailNotification` and `SmsNotification`.
- Create an abstract class `Account` with a concrete common method and an abstract method.
- Write a short driver program that uses interface references.
- Explain when an interface is more suitable than an abstract base class in this example.

**DSA**
- Problem: Merge two sorted arrays into one sorted array.
- Pattern: Two pointers, one per input array.
- Variation: Merge two sorted lists when one input is empty.
- Explain why each pointer moves only when its current value is consumed.

## Day 13 — Composition, enums, packages, immutability basics
**Independent coding**
- Create an `Address` class and make it a field inside `Employee` (composition).
- Create an enum `TransactionStatus`.
- Create an immutable `Money` or `CustomerId` class with private final fields and no setters.
- Organise classes into sensible packages.
- Explain why composition models a "has-a" relationship.

**DSA**
- Problem: Rotate an array to the right by K positions.
- Pattern: Array manipulation; use the three-reversal technique after first understanding a simple extra-array solution.
- Variation: K can be greater than array length; reduce it using modulo.
- Explain why three reversals produce the desired rotation.

## Day 14 — OOP mini-project
**Independent coding**
- Build a console Employee Management application.
- Required operations: add employee, list employees, search by ID, update salary and remove employee.
- Use classes, encapsulation, constructors, methods, collections if already introduced, and input validation.
- Test duplicate IDs and searching for a missing employee.

**DSA**
- Reattempt Two Sum and Maximum Subarray from a blank editor.
- For each, explain brute force, improved approach, pattern clue and complexity.
- Weekly review: write a one-page comparison of traversal, two pointers and HashMap lookup.

---

# Week 3 — Collections + frequency counting

## Day 15 — List, ArrayList, LinkedList
**Independent coding**
- Store employee names in an `ArrayList`; add, update, remove and search.
- Iterate using for-loop, enhanced for-loop and Iterator.
- Compare `ArrayList` and `LinkedList` use cases in a short note.
- Test an empty list and invalid index handling.

**DSA**
- Problem: Contains Duplicate.
- Pattern: HashSet membership.
- Variation: Return the duplicate value(s), not just true/false.
- Explain why set lookup helps avoid comparing every pair.

## Day 16 — Set, HashSet, TreeSet
**Independent coding**
- Read a list of integers and remove duplicates with `HashSet`.
- Use `TreeSet` to display unique values in sorted order.
- Compare output ordering of HashSet and TreeSet.
- Test repeated values and empty input.

**DSA**
- Problem: Intersection of Two Arrays.
- Pattern: HashSet membership.
- Variation: Return the intersection with unique values only; then consider preserving duplicates.
- Explain how the chosen set represents values already seen.

## Day 17 — Map, HashMap, TreeMap
**Independent coding**
- Count frequency of each word in a sentence using `HashMap`.
- Count character frequency in a string.
- Build a phone directory using a map from name to number.
- Use `TreeMap` to display keys in sorted order.
- Test case sensitivity and repeated keys.

**DSA**
- Problem: First non-repeating character in a string.
- Pattern: Frequency map / two-pass counting.
- Variation: Return its index instead of the character.
- Explain why one pass counts and a later pass preserves original order.

## Day 18 — equals() and hashCode()
**Independent coding**
- Create an `Employee` class with employee ID and name.
- Implement `equals` and `hashCode` based on employee ID.
- Add two separate objects with the same ID to a `HashSet`; observe the result.
- Explain why equal objects must have equal hash codes.

**DSA**
- Problem: Valid Anagram.
- Pattern: Frequency counting.
- Variation: Handle uppercase/lowercase according to a stated rule.
- Explain why matching character counts proves the strings are anagrams.

## Day 19 — Comparable and Comparator
**Independent coding**
- Sort employees by salary using `Comparator`.
- Sort by name, then by salary as a tie-breaker.
- Implement `Comparable` for a simple class and compare it with an external Comparator.
- Test equal salaries and equal names.

**DSA**
- Problem: Top K Frequent Elements (start with a frequency map; sorting is acceptable as the first solution).
- Pattern: Frequency map + ordering/selection.
- Variation: Return the K least frequent elements.
- Explain the trade-off between sorting all distinct values and using a heap; heap can be a later extension.

## Day 20 — Queue, Deque, Stack and Big-O
**Independent coding**
- Implement browser back-history behaviour using a stack.
- Use a queue to process customer requests in arrival order.
- Use a deque to add/remove at both ends.
- Write Big-O for common operations you used; distinguish average-case from worst-case where relevant.

**DSA**
- Problem: Valid Parentheses.
- Pattern: Stack.
- Variation: Include all three bracket types `()`, `{}`, `[]`.
- Explain why the most recently opened bracket must be matched first (LIFO).

## Day 21 — Collections mini-project and review
**Independent coding**
- Upgrade Employee Management to use a `Map<Integer, Employee>`.
- Add duplicate-ID protection and search/update/delete.
- Sort employee results by salary.
- Test missing IDs, duplicate IDs and empty directory.

**DSA**
- Reattempt Contains Duplicate, First Non-Repeating Character and Valid Parentheses.
- For each, write the pattern clue and invariant before coding.
- Weekly review: make a pattern sheet for HashSet, HashMap/frequency counting and Stack.

---

# Week 4 — Java 8 + applying patterns

## Day 22 — Functional interfaces
**Independent coding**
- Write one custom functional interface and implement it with a lambda.
- Use `Predicate<Integer>` to test even numbers.
- Use `Function<String, Integer>` to calculate string length.
- Use `Consumer<String>` to print a value and `Supplier<Double>` to generate a value.
- Explain input and output types of each interface.

**DSA**
- Problem: Majority Element (first understand a frequency-map solution).
- Pattern: Frequency counting.
- Variation: Return a majority only if it occurs more than n/2 times.
- Optional extension: Learn Boyer–Moore voting after you can explain the counting solution.

## Day 23 — Lambda expressions and method references
**Independent coding**
- Sort a list of employees using a lambda.
- Replace a simple lambda with a method reference.
- Filter names by length and print them.
- Create a reusable predicate and combine two conditions.
- Explain what functional interface each lambda targets.

**DSA**
- Problem: Binary Search in a sorted array.
- Pattern: Binary search / shrinking search interval.
- Variation: Find the first occurrence of a target with duplicates.
- Explain the interval boundaries and why half the search space can be discarded.

## Day 24 — Stream filter, map, sorted, distinct, limit
**Independent coding**
- Given a list of integers, filter even values.
- Square each number using `map`.
- Remove duplicates and sort values.
- Get the first three matching values with `limit`.
- Rewrite one stream pipeline using a normal loop and compare readability.

**DSA**
- Problem: Search Insert Position.
- Pattern: Binary search on insertion boundary.
- Variation: Find the lower bound / first index whose value is greater than or equal to target.
- Explain what the left and right boundaries mean when the loop ends.

## Day 25 — collect, groupingBy, partitioningBy
**Independent coding**
- Group employees by department.
- Partition employees into salary bands using a predicate.
- Collect employee names into a list.
- Count employees per department.
- Explain the output data structure of each collector.

**DSA**
- Problem: Longest Substring Without Repeating Characters.
- Pattern: Sliding window + set/map.
- Variation: Return the substring itself, not just its length.
- Explain the window invariant: the current window contains no repeated characters.

## Day 26 — reduce and Optional
**Independent coding**
- Use `reduce` to calculate sum and product.
- Find the maximum value with a reduction or comparator.
- Use `Optional` for a search that may return no employee.
- Avoid calling `get()` without checking presence.
- Test empty collections.

**DSA**
- Problem: Minimum Size Subarray Sum (positive integers and target).
- Pattern: Sliding window with variable window size.
- Variation: Return the start/end indices of the shortest valid window.
- Explain why shrinking from the left is safe under the positive-number constraint.

## Day 27 — Java 8 stream exercises
**Independent coding**
- From employee data, find the highest-paid employee.
- Group employees by department and calculate average salary.
- Find the top three distinct salaries.
- Convert a list of strings to a map with a stated duplicate-key policy.
- Explain each stream pipeline step-by-step.

**DSA**
- Problem: Maximum Average Subarray I (fixed window size K).
- Pattern: Sliding window with fixed window size.
- Variation: Find the maximum sum for a window of size K.
- Explain why you add the new element and remove the element leaving the window.

## Day 28 — Java 8 and DSA revision
**Independent coding**
- Rebuild three earlier Java 8 exercises without notes.
- Refactor one loop-based solution into streams only where it improves clarity.
- Explain lambda, functional interface, stream intermediate and terminal operations.

**DSA**
- Reattempt Binary Search, Longest Substring Without Repeating Characters and Maximum Average Subarray.
- For each, explain the recognition clue, invariant, complexity and one variation.
- Create your first DSA pattern index with these categories: traversal, two pointers, HashSet/HashMap, frequency map, stack, binary search and sliding window.

---

# Pattern notebook template

Create one note per DSA pattern (not just per question):

```markdown
# Pattern: [Name]

## Recognition clues
- What constraints or wording suggest this pattern?

## Core idea
- Explain it in plain English.

## Invariant
- What must remain true while the algorithm runs?

## Template / pseudocode
- Write the reusable steps, not a memorised full answer.

## Complexity
- Time:
- Extra space:
- Why:

## Problems solved using this pattern
1.
2.
3.

## Variations and when the pattern does NOT apply
-

## Recall checks
- Next day:
- After 3 days:
- After 7 days:
```

# Completion rule

Mark a DSA problem as **understood** only when you can:
1. Explain the brute-force approach.
2. Explain why the pattern is appropriate.
3. State the invariant or key reasoning.
4. Code it again without viewing the solution.
5. Explain time and space complexity.
6. Solve or clearly reason through one variation.

If you needed a hint, that is fine. Record the hint and schedule a blank-editor reattempt. Honest tracking is more useful than a perfect-looking checklist.
