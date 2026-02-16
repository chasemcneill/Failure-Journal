# Week [3] Learning Log

**Student Name:** Chase McNeill 
**Week of:** Feb 9th-16th
**Topic(s):**  Loops, Conditionals and Functions

---

## What I Worked On This Week

**Assignment(s):**
- [ ] Worksheet [#3]
- [ ] Other: [describe]

---

## Challenges & Problem-Solving

### Challenge 1: [Use grepl() to search for the word "Bar" ]

**What I was trying to do:**
Modify the above loop to only print titles that contain the word "Bar"? 

**What went wrong:**
I had made a function that was at first so terribly wrong, that I had to kill the terminal. The major issue was that I was returning every line as true or false instead of the actual lines and just the title.

**My problem-solving process:**
1. for (i in 1:length(gayguides$title)) { print(grepl("Bar", gayguides$title[], ignore.case = TRUE)) } Failed and had to kill the terminal. 
2. Tried to fix it and it only returned true or false. 
3. Asked slack, and my question was answered in class, as I simply messed up the if statement and printing. 

**Resources I consulted:**
- [ ] Documentation for [package/function]
- [ ] Stack Overflow: [describe what you searched for]
- [ ] Course materials: [which ones]
- [ -] Slack discussion
- [ ] Office hours
- [ ] Other: [describe]

**Resolution:**
for (i in 1:length(gayguides$title)) {
  if(grepl("Bar", gayguides$title[i], ignore.case = TRUE)) {
  print(gayguides$title[i]) 
  }
} Proprely using the if and print functions. 

**What I learned:**
Not much, because my very next issue was a problem printing the correct answer, yet again. But in all seriousness, knowing when to ask help and seek consultation. 

---

### Challenge 2: Bringing It All Together
]

**What I was trying to do:**
How to get the code to only output the last thing found in the function. 

**What went wrong:**
I had put the print() function inside of outside of it. 

**My problem-solving process:**
1. locations_in_state <- 0
count_by_state <- function(abstate) {
  data(gayguides)
  for (i in 1:nrow(gayguides)) {
    if (gayguides$state[i] == abstate) {
    locations_in_state <-locations_in_state + 1
     print(paste("There are", locations_in_state, "locations in", abstate, sep=" "))
    } else {
      next
    }
  }
}
I had put both the print() function inside the loop, while the counter was outside of it. 
2. count_by_state <- function(abstate) {
  data(gayguides)
  locations_in_state <- 0
  for (i in 1:nrow(gayguides)) {
    if (gayguides$state[i] == abstate) {
    locations_in_state <-locations_in_state + 1
    } else {
      next 
    } 
  }
  print(paste("There are", locations_in_state, "locations in", abstate, sep=" "))
}
Fixed the order and the output ended up becoming just the one line I was looking for. 
3. [Additional attempts if relevant]

**Resources I consulted:**
- [ ] Documentation for [package/function]
- [ ] Stack Overflow: [describe what you searched for]
- [ ] Course materials: [which ones]
- [ - ] Slack discussion
Sent you a direct message. 
- [ ] Office hours
- [ ] Other: [describe]

**Resolution:**
Fixing the issue of where both the counter and print() function need to go when creating new functions. Otherwise, I will end up with 410 lines when I am only looking for one. 

**What I learned:**
That I really need to get better at where and when to insert the print function. Both of my challenges this week were a direct result of this issue. 

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
How to use loops, conditionals, and functions together to make functions that are powerful and incredibly useful for prospective research.  

**What I'm still confused about:**
The only problem I had this week was where to insert the print() function. I hope that I now fully understand it, but we shall see. 

**Connection to historical research:**
The bringing it all together section shows how powerful functions can be when you know how to create them and have the proper information available. I could have used this week's coding on my research into newspapers discussing the Spanish-American War by looking at each newspaper entry I have, for example, the date of April 21st, 1898. A function that could help me see which days are most significant nationwide. 