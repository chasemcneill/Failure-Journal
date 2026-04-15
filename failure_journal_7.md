# Week [X] Learning Log

**Student Name:** [Chase McNeill]  
**Week of:** [April 13th]  
**Topic(s):** ["Text Analysis"]

---

## What I Worked On This Week

**Assignment(s):**
- [ ] Worksheet 7
- [ ] Other: [describe]

**AI tools used this week:**
- [ ] ChatGPT
- [ -] Claude
- [ ] GitHub Copilot
- [ ] Other: [specify]
- [ ] Did not use AI this week

---

## Challenges & Problem-Solving

### Challenge 1: [Brief descriptive title]

**What I was trying to do:**
[Trying to get the entire section on co-occurance to work.]

**What went wrong:**
[It would just output a white screen if I used the example or followed the directions.]

**Did you use AI to troubleshoot this challenge?** [No]

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
[I was going to ask about why the example did not work in slack and it had already been asked with Dori having an example to fix the problem. ]

**My problem-solving process:**
1. [swapped out the n >= 114 because that was the highest number]
2. [That made no sense so I swapped it to 100 and it looked better.]
3. [Swapped it out once more for 75, because 100 still did not have many entries.]
4. [For the create section I changed the 125 to 175 ties to 50 to 75 because the original question did not actually work with my data.]

**Resources I consulted:**
- [ ] Documentation for [package/function]
- [ ] Stack Overflow: [describe what you searched for]
- [ ] Course materials: [which ones]
- [- ] Slack discussion
- [ ] Office hours
- [ ] Other: [describe]

---

**Resolution:**
[Looking at the documentation and seeing that the numbers did not fit. ]

**What I learned:**
[If a problem exists, sometimes it may be a slight error that just need to be looked at a bit further. ]

**Verification:**
[Used a bunch of numbers until I felt like it fit what the original question was probably asking. For example, I used 25 to 75 originally, but that had way too many inputs so I changed it to 50 to 75. ]

---

### Challenge 2: [Brief descriptive title]

**What I was trying to do:**
[I was trying to find the tf_idf scores in the 1920s for the Mind and Body data frame. ]

**What went wrong:**
[The code just kept coming back as failiing or not responding. ]

**Did you use AI to troubleshoot this challenge?** [Yes]

---

#### If YES, I used AI:

**My prompt to AI:**
```
[tidy_mind_body2 <- tidy_mind_body  |>
  count(doc_id, word, sort = TRUE)  |> 
  bind_tf_idf(word, doc_id, n) |> 
  filter(Year >= 1920 & Year <= 1929) why does this not work]
```

**AI's response:**
```r
# The problem is that filter() can't find the Year column after your previous operations. Here's why: When you use count(doc_id, word, sort = TRUE), it creates a new data frame with only three columns: doc_id word n. The Year column from your original metadata gets dropped in this process. Then when you try to filter(Year >= 1920 & Year <= 1929), R can't find that column. Solution: Filter by year before you start your counting and tf-idf calculations:


```

**How I evaluated the AI's suggestion:**

**What I implemented and why:**
[The AIs suggestion was really helpful because it helped me see an issue I probably would have had to mess with for a bit otherwise.]

**What I modified and why:**
[Moved my filter() line to the beginning, because if it is at the end there is no Year to filter. ]

**What I rejected and why:**
[Did not reject anything because my question ended up very specific.]

**Additional resources I consulted:**
- [ ] Documentation for [package/function]
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
[What ultimately worked or where you're still stuck]

**What I learned:**
[What did this teach you? Did AI help or hinder your understanding?]

**Verification:**
[How did you verify the code worked correctly? What did you test?]

---

## Reflection

**What I understand well now:**
[Text analysis allows for a lot of cool data points to be created that allow for further research. Instead of having to fully invest in every document, you can maybe use it to find the general consesus and ideas you need to lool further into. ]

**What I'm still confused about:**
[The only real question I had was about when to use stemming, but that was already answered. Other than that, maybe where to find different packages of stop_words I could use.]

**How AI affected my learning this week:**
[AI helped me figure out smaller issues that would have taken longer to figure out without it. I would not necessarily say it was extremely beneficial, but it was helpful pointing out my simple mistake.]

**Evolving AI strategy:**
[I do not really think I have gotten any better at using AI. I really just use the same strategies and almost always type out code and "why does this not work."]

**Connection to historical research:**
[If I ever have a large amount of writings to comb through, it can be vital in getting an overall idea of what I need to look out for. Also, could be beneficial looking at census records. Whether that be jobs which have evolved, continued or died over time. ]

