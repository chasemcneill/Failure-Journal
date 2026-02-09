# Week [X] Learning Log

**Student Name:** [Chase McNeill]  
**Week of:** [Feb. 2 - Feb. 9]  
**Topic(s):** ["Data Structures"]

---

## What I Worked On This Week

**Assignment(s):**
- [ ] Worksheet [#2]
- [ ] Other: [describe]

---

## Challenges & Problem-Solving

### Challenge 1: [Brief descriptive title]

**What I was trying to do:**
How about the street address and type for rows 2,555 to 2,560?
**What went wrong:**
[Describe the error, confusion, or roadblock]
  Error in `[.data.frame`(gayguides, 5:6, 2555:2560) : 
  undefined columns selected. I entered the row and column incorrectly in the function, so I was asking to find columns 2555 to 2560, which do not exist. I just stared at it for a couple of minutes until I realized my mistake and fixed it.
**My problem-solving process:**
1. [gayguides[5:6, 2555:2560] Returned an error.]
2. [gayguides[2555:2560, 5:6] flipped the numbers around into their right posititions and it worked.]
3. [Additional attempts if relevant]

**Resources I consulted:**
- [ ] Documentation for [package/function]
- [ ] Stack Overflow: [describe what you searched for]
- [-] Course materials: [I looked at the examples above the question again.]
- [ ] Slack discussion
- [ ] Office hours
- [ ] Other: [describe]

**Resolution:**
 I entered the row and column incorrectly in the function, so I was asking to find columns 2555 to 2560, which do not exist. I just stared at it for a couple of minutes until I realized my mistake and fixed it by switching the numbers around.
**What I learned:**
To make sure I am paying attention to where a row and column is supposed to go in a function, because if there had been 2560 columns, I would have never recieved in error and just have the wrong answer to what I was trying to find.

---

### Challenge 2: [Brief descriptive title]

**can you create a matrix that has 3 rows with only even numbers from 2 to 18? 

**What went wrong:**
The roadblock was I could not figure out how to find only the even numbers from 2 to 18. 
**My problem-solving process:**
1. [Tried to run it without the correct function and it returned all of the numbers from 2:18 in 3 rows.]
2. [matrix(seq(2, 18, by = 2), byrow = TRUE, nrow = 3)
] created a matrix that stated at 2 and coninued by two to get all the even numbers up to 18 in 3 rows. packa
3. [Additional attempts if relevant]

**Resources I consulted:**
- [ - ] Documentation for [package/function]
I remembered the function seq() from a prior class and just used ?seq() to ensure I used it correctly. 
- [ ] Stack Overflow: [describe what you searched for]
- [ ] Course materials: [which ones]
- [ ] Slack discussion
- [ ] Office hours
- [ ] Other: [describe]

**Resolution:**
The function seq() allows you to create the sequence needed to answer the question. 
**What I learned:**
[If you forget how a function works, you can always ask the console.]

---

### Challenge 3 (Optional): [Brief descriptive title]

**What I was trying to do:**
[Describe the task or problem]

**What went wrong:**
[Describe the error, confusion, or roadblock]

**My problem-solving process:**
1. [First attempt - what you did and what happened]
2. [Second attempt - what you did and what happened]
3. [Additional attempts if relevant]

**Resources I consulted:**
- [ ] Documentation for [package/function]
- [ ] Stack Overflow: [describe what you searched for]
- [ ] Course materials: [which ones]
- [ ] Slack discussion
- [ ] Office hours
- [ ] Other: [describe]

**Resolution:**
[What ultimately worked or where you're still stuck]

**What I learned:**
[What did this teach you about the concept, the tool, or problem-solving?]

---

## Reflection

**What I understand well now:**
To always make sure you have the correct inputs in your function, or else you can get an incredibly wrong answer. 
**What I'm still confused about:**
The wording in some of these questions confuse me more than the coding does. For example, Can you create a subset that includes only women voters who lived on "Main" street (the street name contains "Main")? How many were there? # Hint: You'll need to search within the street column. Am I only supposed to find "Main Street" or any street that contains "Main" like "Maine Street?" I assumed it was the former. 
**Connection to historical research:**
Subsetting data could be beneficial to my interests in looking at information about volunteers in the Spanish-American War. Such as how old they were, what region they were from, etc. Also, could be beneficial for looking at census data. 


