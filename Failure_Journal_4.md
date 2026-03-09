# Week [5] Learning Log

**Student Name:** [Chase McNeill]  
**Week of:** [March 2nd March 4th]  
**Topic(s):** [Advanced Data Manipulation]

---

## What I Worked On This Week

**Assignment(s):**
- [ ] Worksheet [#5]
- [ ] Other: [describe]

---

## Challenges & Problem-Solving

### Challenge 1: [Brief descriptive title]

**What I was trying to do:**
I had a major issue doing anything in the Joins() section. 
**What went wrong:**
Never fully understood in class when we were going over it, so I was unable to complete the questions at first. 

**My problem-solving process:**
1. Attempted to combine regions and gayguides by just using left_join(gayguides, regions, by = c("state)). Which failed and I was confused as to why. 
2. regional_gayguides <- left_join(gayguides, regions, by = c("state" = "State.Code")). Suceeded after fully inputing what was need to join each of the data frames. 
3. [Additional attempts if relevant]

**Resources I consulted:**
- [ ] Documentation for [package/function]
- [ ] Stack Overflow: [describe what you searched for]
- [ ] Course materials: [which ones]
- [ - ] Slack discussion
Asked a question for the tech table, 
- [ ] Office hours
- [ ] Other: [describe]

**Resolution:**
Learning how to properly use the left_join() function and its specific restraints. 

**What I learned:**
That joining is an interesting set of functions, that if improperly inputed will do literally nothing. Also, I need to make sure to fully understand and ask questions about a concept before we move on from it. 

---

### Challenge 2: [Brief descriptive title]

**What I was trying to do:**
Widen the `sc.parks` dataset so that the column names are drawn from the type of recreation worker.
**What went wrong:**
The error was that I was using the wrong formato to get pivot_wider to work 
**My problem-solving process:**
1. sc <- sc.parks |> pivot_wider(names_to = type_of_worker, values_to = count)
2. sc <- sc.parks |> pivot_wider(names_from = type_of_worker, values_from = count)
3. [Additional attempts if relevant]

**Resources I consulted:**
- [ -] Documentation for [package/function]
- [ ] Stack Overflow: [describe what you searched for]
- [ -] Course materials: [which ones] 
Looked back at prior examples. 
- [ ] Slack discussion
- [ ] Office hours
- [ ] Other: [describe]

**Resolution:**
Using the correct documentation and learning the differences between two similar functions helps ensure you get the right answer. 

**What I learned:**
If you have troubel, just go bakc and look at the documentation. I will most likely not remeber every function, so if need be just look back. 
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
How to use tools from the forcats package to alter and control categories to ensure consistency and clarity within dataframes. Also, I understand how to properly use the left_join() function

**What I'm still confused about:**
I am still slightly confused on how all the join() functions work. For example, I would like to see an example of a full_join(). 

**Connection to historical research:**
The averaging fuction in summarize, could be an excellent way to look at numberical data. If I need to join two similar histoircal data frames, I now know how to do so. Lastly, the forcats package is a great way to clean historical data. 

