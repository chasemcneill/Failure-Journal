# Week [X] Learning Log

**Student Name:** [Chase McNeill]  
**Week of:** [April 20]  
**Topic(s):** [Worksheet 9: Mapping]

---

## What I Worked On This Week

**Assignment(s):**
- [ -] Worksheet [#]
- [ -] Other: [describe]
    Hugo and our final project

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
[Geocode the Boston Women Voters dataset. Note that the data does include street addresses but because they are broken into parts - street address number, street, etc - you'll need to combine them into a full address to pass to the geocoding function and the next question: Create a map that uses your geocoded data from the Boston Women Voters dataset. ]

**What went wrong:**
[I was trying to create a new variable, "address," and I continued to fail in making it not consist of just NAs. No matter what I put the answer just came out NA. Then when I tried to map it, nothing came of it. ]

**Did you use AI to troubleshoot this challenge?** [Yes]

---

#### If YES, I used AI:

**My prompt to AI:**
```
[ggplot() +
geom_map(data = usa, map = usa, aes(long, lat, map_id=region), fill = "lightgray", color = "black") +
geom_point(data = bwv_data_coordinates, mapping = aes(x = lon, y = lat), color = "orange", size = 3)
why doe this not work]
and 
why does this not actually cause any inputs into the new columns of latitude and longitude?
```

**AI's response:**
```r
# The issue is with the column names. When you geocoded bwv_data_coordinates, the function created columns named latitude and longitude, but your code is looking for lon and lat (which are the column names in the gayguides dataset)
#The issue is likely with how the lat and long parameters are being passed to geocode(). Try one of these solutions:

#Option 1: Quote the column names

#Option 2: Use the default column names (don't specify lat/long)

#This will create lat and long columns by default.

#Option 3: Check what columns were actually created
#After running the code, check what columns exist:
```

**How I evaluated the AI's suggestion:**

**What I implemented and why:**
[I tried all of the implementations and none of them worked because there was a problem further down the ladder that was causing the issue. ]

**What I modified and why:**
[I had to change the original inputs in how I had the address being created, because I had it the wrong way. ]

**What I rejected and why:**
[All of them, because I was not asking the correct question. ]

**Additional resources I consulted:**
- [ ] Documentation for [package/function]
- [ ] Stack Overflow: [describe]
- [ ] Course materials: [which ones]
- [ ] Slack discussion
- [ ] Office hours
- [- ] Other: [describe]
    Figured it out in class when Dr. Regan showed me that I had inputed the order of the adress incoreclty as I had the street number after the street instead of before. 


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
[Figured it out in class when Dr. Regan showed me that I had inputed the order of the adress incorrecty, as I had the street number after the street name instead of before the street name. ]

**What I learned:**
[If you are not asking the right questions, AI can be extremely useless. Sometimes the issue is not where you think it is. ]

**Verification:**
[I looked at the documentation and it now had longitude and latitude and then mapped it.]

---

### Challenge 2: [Brief descriptive title]

**What I was trying to do:**
[rec.data.coordinates <- rec.data %>% geocode(city = city, state = state, method='osm', lat = latitude, long = longitude)
head(rec.data.coordinates), would not run. ]

**What went wrong:**
[The line of code in the example did not run, so I could not do anyhting invoving the rec.data.coordinates, which was caused by my r not being updated. This led to the issue of all my packages not running correctly, which needed to be fixed. ]

**Did you use AI to troubleshoot this challenge?** [Yes]

---

#### If YES, I used AI:

**My prompt to AI:**
```
[All of my prompts: 
1. how do i update all my past r packages from 4.3 to my current version of r
2. how to move packages from version 4.to my current version of r on my computer
3. library(DigitalMethodsData)
why is there no package when there is a package
]
```

**AI's response:**
```r
# You're running R 4.5.3. To update all your packages from 4.3 to your current version, run this command in R: update.packages(). Also gave out fully automated versions of it. 

#  Just said to use the update.packeges() again or # Copy 4.3 packages to 4.5.3 cp -r ~/Library/R/arm64/4.3/library ~/Library/R/arm64/4.5/library. Did not really work. 

# The issue is that DigitalMethodsData likely wasn't installed in your R 4.5.3 library yet. When you upgrade R versions, packages don't automatically transfer. You need to reinstall them.A ccording to your worksheet, DigitalMethodsData is hosted on GitHub and requires the devtools package to install. Let me help you install it: Then proceeds to do it for me. 
```

**How I evaluated the AI's suggestion:**

**What I implemented and why:**
[The first and third responses were extremely beneficial because it allowed me to complete the rest of the worksheet. ]

**What I modified and why:**
[I needed to update r and then update or reinstall all my packages again. ]

**What I rejected and why:**
[My second prompt was virtually useless because it only outputed what I asked in the first prompt.]

**Additional resources I consulted:**
- [ ] Documentation for [package/function]
- [ ] Stack Overflow: [describe]
- [ ] Course materials: [which ones]
- [ -] Slack discussion
Figured out in class that the issue was that I was running an older version of r. 
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
[Updating r and then reinstalling or updating all my packages.]

**What I learned:**
[That I need to keep r and my packages updated so that I do not have to go through this again.]

**Verification:**
[Went back through all the other worksheets to make sure I had everything reinstalled and then reinputed the example that first did not do anything and it worked.]

---

## Reflection

**What I understand well now:**
[The different viablities of mapping tools. What you may need from a map depends on what you want to do with it. Do you want it to be interactive? Do you want it in an article? These things seperate which tool you may use. ]

**What I'm still confused about:**
[Is there a way to just get the city and the streets by themselves without having to have the entire state?]

**How AI affected my learning this week:**
[AI was extremely beneficial in fixing all my packages and updating r to where I could use it much faster if I had to manually input everything myself. While I also failed to use it correctly in my first issue,]

**Evolving AI strategy:**
[The power of a question. If the question is not correctly issued then the output will be useless.]

**Connection to historical research:**
[It could be beneficial mapping major areas specific to the Spanish-American War. Also, for a project looking at sugar production, it would be beneficial to map it with what was learned in the sf section.]

