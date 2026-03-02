# Week [4] Learning Log

**Student Name:** [Chase McNeill]  
**Week of:** [Feb 24th - 28th]  
**Topic(s):** [Worksheet 3: Data Manipulation']

---

## What I Worked On This Week

**Assignment(s):**
- [ ] Worksheet [4]
- [ ] Other: [describe]

---

## Challenges & Problem-Solving

### Challenge 1: [Brief descriptive title]

**What I was trying to do:**
I had trouble figuring out the question: The amenity features column in gay guides contains a comma separated list of categorizations. (G), for example, stands for girls. However, this language changed over time and women's locations eventually are described as (L). What if we want to filter by any entry that has (G) OR (L) in the amenity feature column?  This is a bit more complicated because the entries are a comma separated list and (G) or (L) is often paired with other categorizations. How might you _search the dataframe for entries that match_ (G) or (L)
**What went wrong:**
Confused as to where to go because of the comma. 
**My problem-solving process:**
1. g_l_gayguides <- gayguides |> filter(grepl("(G)", gayguides$amenityfeatures))|filter(grepl("(L)", gayguides$amenityfeatures)) :Failed and gives the error message that the filter can only be applied to an object of class "logical."
2. g_l_gayguides <- gayguides |> filter(grepl("(G)|(L)", amenityfeatures)) : It worked as needed.
3. [Additional attempts if relevant]

**Resources I consulted:**
- [ ] Documentation for [package/function]
- [ ] Stack Overflow: [describe what you searched for]
- [ ] Course materials: [which ones]
- [ - ] Slack discussion: This was my slack question for the table. 
- [ ] Office hours
- [ ] Other: [describe]

**Resolution:**
g_l_gayguides <- gayguides |> filter(grepl("(G)|(L)", amenityfeatures)). 
**What I learned:**
for filter the or function needs to within grepl as a whole and not two different filter functions by themeselves. 

---

### Challenge 2: [Brief descriptive title]

**What I was trying to do:**
In the Boston Women Voters data, convert Occupation to a factor. What are the levels?]

**What went wrong:**
The major issue was that I did not capitalize occupation. 
**My problem-solving process:**
1. [BostonWomenVoters <- BostonWomenVoters |> mutate(occupation = as.factor(occupation))] - returns the error message: object 'occupation' not found Run `rlang::last_trace()` to see where the error occurred
2. BostonWomenVoters <- BostonWomenVoters |> mutate(Occupation = as.factor(Occupation))
levels(BostonWomenVoters$Occupation)

3. [Additional attempts if relevant]

**Resources I consulted:**
- [ - ] Documentation for [package/function]
- [ ] Stack Overflow: [describe what you searched for]
- [ ] Course materials: [which ones]
- [ ] Slack discussion
- [ ] Office hours
- [ ] Other: [describe]

**Resolution:**
Looked at the dataset again to make sure I was using the right wording. Thought it was right again and it failed. Then looked at the error message one more time and saw "occupation" in lowercase not found and realized it was probably in issue with capitalization. 
**What I learned:**
To ensure that I know how each column in the dataset is spelled. Also, I need to make sure to correctly read error messages. 

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
How much easier it is do these sorts of problems when using packages like tidyverse. 
**What I'm still confused about:**
Why not for the ward_missing section did we not just delete the NAs instead of making a new column for our new dataset. 
**Connection to historical research:**
Makes it a lot easier and faster to look at things discussed in the past. I can now easily input numbers as na, easily changed and alter columns and create new datasets for information I collect. For example, creating a new column that states when a certain volunteer is missing data in my SC_Volunteer sheet. 

