# Week [X] Learning Log

**Student Name:** [Chase McNeill]  
**Week of:** [April 6th]  
**Topic(s):** ["Data Visualization with ggplot"]

---

## What I Worked On This Week

**Assignment(s):**
- [6 ] Worksheet [#]
- [ ] Other: [describe]

**AI tools used this week:**
- [ ] ChatGPT
- [ 1] Claude
- [ ] GitHub Copilot
- [ ] Other: [specify]
- [ ] Did not use AI this week

---

## Challenges & Problem-Solving

### Challenge 1: [Brief descriptive title]

**What I was trying to do:**
[For my plot one, I wanted to change the Age column to combine ages into ten year periods. ]

**What went wrong:**
[I tried to do each one individually, like "21", but it failed. ]

**Did you use AI to troubleshoot this challenge?** [Yes]

---

#### If YES, I used AI:

**My prompt to AI:**
```
[bwv_ward <- bwv_ward |>
mutate(
Age = fct_collapse(Age,
"20-29" = c("20", "21", "22", "23", "24", "25", "26", "27", "28", "29"))) why is it not working?
]
```

**AI's response:**
```
The issue is that fct_collapse() requires a factor, but Age is likely numeric or character from your group_by(). Convert it to a factor first:
bwv_ward <- bwv_ward |>
mutate(
Age = fct_collapse(Age,
"20-29" = c("20", "21", "22", "23", "24", "25", "26", "27", "28", "29"))) why is it not working
Did not work again, after I tried to shorten it so I asked? 
bwv_ward <- bwv_ward |>
mutate(
Age = as.factor(Age),
Age = fct_collapse(Age,
"20-29" = 20:29)) why is not working?
Output:

91 x 16
The issue is that fct_collapse() requires a factor, but Age is likely numeric or character from your group_by(). Convert it to a factor first:

Or split it into two steps:

The as.factor() converts Age to a factor so fct_collapse() can work with it properly.

bwv_ward <- bwv_ward |>
mutate(
Age = as.factor(Age),
Age = fct_collapse(Age,
"20-29" = 20:29)) why is not working

The issue is that 20:29 creates numeric values, but fct_collapse() needs character strings. Convert the range to characters:
bwv_ward <- bwv_ward |>
  mutate(
    Age = as.factor(Age),
    Age = fct_collapse(Age,
      "20-29" = as.character(20:29)))

```

**How I evaluated the AI's suggestion:**
The original suggestion was alright, but did not fully explain what I wanted. The second suggestion helped me fully create what I needed to answer the question I had made. 
**What I implemented and why:**
The second suggestion is what I implemented, because it did what I needed it to do. 

**What I modified and why:**
[I just used the code it suggested to create the other age brackets, because if the original worked it should work for all of the,. ]

**What I rejected and why:**
[The first suggestion was mostly rejected because it did not fully answer what I was looking for in the end.]

**Additional resources I consulted:**
- [- ] Documentation for [package/function]
- [ ] Stack Overflow: [describe]
- [ ] Course materials: [which ones]
- [ ] Slack discussion
- [ ] Office hours
- [ ] Other: [describe]


echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> ~/.zprofile
eval "$(/opt/homebrew/bin/brew shellenv)"
---

#### If NO, I didn't use AI:

**Why I chose not to use AI:**
[Explain your reasoning - wanted to understand it myself, AI struggles with this type of problem, etc.]

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

---

**Resolution:**
[In the end the second suggestion really helped me piece what I needed to help lay out what was needed to make the code that would graaph what I was looking for.]

**What I learned:**
[A majore lesson to be learned is that wording and how you ask questions compeltely alters how beneficial AI might be. My first suggestion was only slightly beneficial, but after retrying, my second suggestion helped create the rest of the plot. ]

**Verification:**
[I verified it by running the code to see whether or not it made the Age column hold one section with all the 20-29 year olds.]

---

### Challenge 2: [Brief descriptive title]

**What I was trying to do:**
[I needed to get rid of the X in front of the year in the "year" column. ]

**What went wrong:**
[I had no idea how to get rid of the X in front of the year in the "year" columns inputs.]

**Did you use AI to troubleshoot this challenge?** [Yes]

---

#### If YES, I used AI:

**My prompt to AI:**
```
[how to eliminate the xbefore the number in the year column for rec_long2?]
```

**AI's response:**
```
# The "x" prefix comes from the pivot_longer() operation when column names start with numbers. Use parse_number() or str_remove() to fix it:
rec_long2 <- rec_long |>
  mutate(
    type_of_worker = fct_collapse(type_of_worker,
      "paid" = c("female paid", "male paid"),
      "volunteer" = c("men volunteer", "volunteer", "women volunteer")),
    year = parse_number(year)) |>
  group_by(type_of_worker, year) |>
  summarize(count = mean(count, na.rm = TRUE))
Or alternatively:
year = as.numeric(str_remove(year, "^x"))

The parse_number() approach is simpler—it extracts just the numeric portion of the string, removing the "x" prefix automatically.
```

**How I evaluated the AI's suggestion:**

**What I implemented and why:**
[They were all appropraite and very helpful. ]

**What I modified and why:**
[I decided against using the second suggestion (str_remove), because the first one looked far simpler. ]

**What I rejected and why:**
[I decided against using the second suggestion (str_remove), because the first one looked far simpler.]

**Additional resources I consulted:**
- [ ] Documentation for [package/function]
- [ ] Stack Overflow: [describe]
- [ ] Course materials: [which ones]
- [ ] Slack discussion
- [ ] Office hours
- [-] Other: [describe]
It was originally explained in class, I however was not fast enough to write down the code. 

---

#### If NO, I didn't use AI:

**Why I chose not to use AI:**
[Explain your reasoning - wanted to understand it myself, AI struggles with this type of problem, etc.]

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

---

**Resolution:**
[Using the parse_number function]

**What I learned:**
[The AI was beneficial, because we have yet to really hit on something prior to last class.]

**Verification:**
[Just ran the code and looked at the data frame to see whether the Xs were deleted.]
---

## Reflection

**What I understand well now:**
[How to properly create graphs with ggplot, and the most interesting tool to use within this week's instruction (facet_wrap)]

**What I'm still confused about:**
[When to use geom_histogram over geom_col. ]

**How AI affected my learning this week:**
[AI was beneficial in helping me solve problems I had yet to encounter in class or in worksheets. It has helped my learning in helping show routes to questions I may not have figured out otherwise. There was only a small issue with my first example.]

**Evolving AI strategy:**
[Asking questions and properly framing what is asked. If not propely explained, you will get a worse output than if your explanation of what you are looking for is not extremely clear. I think when I have inputed specific lines of code, it has been more helpful.] 

**Connection to historical research:**
[The ability to create visual representations of data with ggplot is extremely beneficial. It allows for greater explanations of datasets I may work on, while also allowing for an additive interesting aspect for a presentation. I could use it for potential research into trade with Cuba and the United States, especially over time. ]

