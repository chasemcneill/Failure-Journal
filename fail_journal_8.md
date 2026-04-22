# Week [X] Learning Log

**Student Name:** [Chase McNeill]  
**Week of:** [April 20th]  
**Topic(s):** [Worksheet 8: Topic Modeling]

---

## What I Worked On This Week

**Assignment(s):**
- [ -] Worksheet [#]
- [ ] Other: [describe]

**AI tools used this week:**
- [ ] ChatGPT
- [- ] Claude
- [ ] GitHub Copilot
- [ ] Other: [specify]
- [ ] Did not use AI this week

---

## Challenges & Problem-Solving

### Challenge 1: [Brief descriptive title]

**What I was trying to do:**
[Needed to find the correct k value and the amount of words needed for my document term matrix]

**What went wrong:**
[The value of K as 10 just was not all that good.]

**Did you use AI to troubleshoot this challenge?** [ No]

---

#### If YES, I used AI:

**My prompt to AI:**
```
[Copy your exact prompt here]
```

**AI's response:**
```r
# Paste the relevant code or explanation AI provided -- this can brief and abbreviated or summarized if the response is long.
```

**How I evaluated the AI's suggestion:**

**What I implemented and why:**
[Which parts of the AI's suggestion were appropriate?]

**What I modified and why:**
[What did you change? Why was the change necessary?]

**What I rejected and why:**
[What suggestions did you not use? Why were they inappropriate?]

**Additional resources I consulted:**
- [ ] Documentation for [package/function]
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
[This was more of a plug and play problem, that I do not think AI is helpful for or I have no general clue how to ask it otherwise]

**My problem-solving process:**
1. [am_city_lda <- LDA(am_city_dtm, 
              k = 10, 
              method = "Gibbs",
              control = list(seed = 23415, iter = 2000, burnin = 1000))] Not the greatest.
2. [am_city_lda2 <- LDA(am_city_dtm, 
              k = 15, 
              method = "Gibbs",
              control = list(seed = 23415, iter = 2000, burnin = 1000))] too much word overlap.
3. [am_city_lda5 <- LDA(am_city_dtm, 
              k = 12, 
              method = "Gibbs",
              control = list(seed = 23415, iter = 2000, burnin = 1000))] Decent, but I liked my next choice more. 
4. am_city_lda4 <- LDA(am_city_dtm, 
              k = 7, 
              method = "Gibbs",
              control = list(seed = 23415, iter = 2000, burnin = 1000)) Perfect, and I just used the number 7 for every other corresponding thing I used. Also plug and played them into other graphing and word clouds. 

**Resources I consulted:**
- [ ] Documentation for [package/function]
- [ ] Stack Overflow: [describe what you searched for]
- [ -] Course materials: [which ones]
This worksheet and the example from class. 
- [ ] Slack discussion
- [ ] Office hours
- [ ] Other: [describe]

---

**Resolution:**
[Just plugging and plugging.]

**What I learned:**
[Topic modeling takes a long while to get to where you want it to go, so do not fret if it does not work the first time. ]

**Verification:**
[Just kept using it throughout the rest of the exercise. ]

---

### Challenge 2: [Brief descriptive title]

**What I was trying to do:**
[Wanted to add color to my bar graph. ]

**What went wrong:**
[Forgot where it needed to be put, whether using a plus or within the parentheses.]

**Did you use AI to troubleshoot this challenge?** [Yes]

---

#### If YES, I used AI:

**My prompt to AI:**
```
[how to chnage color for geom_bar]
```

**AI's response:**
```r
# To change the color of geom_bar, use the fill parameter: geom_bar(fill = " steelblue", stat = "identity").
```

**How I evaluated the AI's suggestion:**
# It was good and worked. 

**What I implemented and why:**
[I implemented where it was put within the code. ]

**What I modified and why:**
[I changed the color that was recommended bceause I think red and blue are just simpler than "steelblue." I also had the change of color as + color = "blue", so I deleted that. ]

**What I rejected and why:**
[Nothing]

**Additional resources I consulted:**
- [ -] Documentation for [package/function]
Probably could have just done this, but using AI was faster and I ended up looking at it afterward to make sure it workd. 
- [ ] Stack Overflow: [describe]
- [ ] Course materials: [which ones]
- [ ] Slack discussion
- [ ] Office hours
- [ ] Other: [describe]

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
[The suggestion worked.]

**What I learned:**
[AI helped in a way, but it was more of a blond moment than anything else.]

**Verification:**
[Just inserted it into my full line of code and it worked in changing the color of the graph.]

---

## Reflection

**What I understand well now:**
[The difference between topic modeling and text analysis, and how overall research pathways alter which one probably should be used. ]

**What I'm still confused about:**
[I could not figure out how to use the mind and body dataset instead of the amcity for the last section. The major issue was that my computer would not find the mind and body data from my computer no matter what I did.]

**How AI affected my learning this week:**
[AI did not make me any better, but it was helpful in speeding us a specific process. My example being, how to put color in a bar graph. ]

**Evolving AI strategy:**
[I really do not think I got any better this week. I tried to use it to help me figure out the problem with trying to use the mind and body data, but everything it tried to tell me to do, I had already attempted or just would not work. Which led me to using the Am cities instead.]

**Connection to historical research:**
[If I wanted to look at topics in 1898 and how they compared with the Spanish-American War, it could possibly be helpful. Whether looking at one specific newspaper or multiple across differing dates, if I had the data all I would have to do would model it and hit run. If it brought out anything interesting it would allow me the opportuinity to look into it. If not, then at least it is something you can do in the background.]

