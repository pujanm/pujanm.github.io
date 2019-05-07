---
layout: post
title: Google Summer of Code 2019 - Application experience
image: /img/gsoc_logo.png
tags: [GSoC, CERN, Python, Coding]
---

I am dividing my application experience into a number of steps and I have tried my best to provide as many as tips as possible for getting into this programme.

## 1) Finding the correct organization <br>
This was the most important part (obviously). First thing I decided was to find a project which I felt was in my standards, so I had started searching for organizations before their names were announced officially on **Google Search** and **GitHub** and found many of them who were coming (new ones) and some which were there from quite a long time and were coming again. Then while searching for projects I found this GitHub repo very useful for understanding the criteria of different organizations and what all is required to apply there and tech-stack involved in those orgs.

Then I came across **CERN-HSF** and found that they had an assessment test and based on the performance they help you further in building the proposal.
So basically it was an umbrella org. meaning it had many organizations within itself which was quite a lot like another GSoC site with a list of organizations in itself.

Then another project I came across was by **Debian** but didn’t go for it as I had already shortlisted 2 orgs so I felt at one point that quality of my proposals will decline if I go for writing many proposals at a time. So please shortlist only 5-6 projects **pre-GSoC** orgs are announced and then later preferably from my experience go for 2 as there is a limit of 3 proposals only.

So to conclude I shortlisted 2 orgs under **CERN-HSF** i.e. **Rucio** and **DIRAC** and contacted the respective mentors for the assessment tests and proposal writing.

Here both of my projects were purely based on **Python** where **Rucio** involved areas like Networking, Databases, and Distributed computing while **DIRAC** involved ElasticSearch, Monitoring, and again Distributed computing. These were the topics a bit different then I had worked on anything before and found them interesting too.

## 2) Communication with mentors and building the proposal <br>
Both of my projects involves contributions to their code base purely like not a **start from scratch** project.

Firstly, I would like to start with Rucio so their test was pretty easy just to set up the environment locally, running their test cases and to fix a small issue like even README changes were accepted (they were testing whether we are able to handle GitHub or not) and then they asked to simply start writing the proposal.

So I was a bit surprised rather confused as they just gave a simple command **you can start writing your proposal**. So I started finding a set of issues which were like projects and started interacting with the mentor. So my mentor basically briefed me about the issue and suggested to work on that single issue only as it was quite big and complicated and to prepare a proposal around it. Then the first thing I did was to read their documentation entirely just not reading some topics and done, I literally read their entire docs from start to end, did some experimentation which took me a week and I was deprived of sleep (which we will have to be used too now). 

Then after gathering some understanding, I started asking questions to the mentor. I had to think thrice at least before asking some question as they judge us based on the questions we ask like really don’t ask stupid questions which your mentor will not tell you it was but you must have that much understanding as they judge us based on that and they don’t spoon feed at all. Then beginning with my conversation I started asking meaningful questions and tried to extract as much as information as possible from the mentor as at the end this is the only thing you can do as we can’t just simply write anything arbitrary in the proposal we need to know our project in and out and the work we have to do well in detail. Don’t expect that mentors will tell you everything they check our responsiveness and our understanding and based on that they help us.

So I talked with my mentor almost daily like just missed Saturdays and Sundays (as they are on an off that day) till the day I submitted my proposal.
Then after information extraction, the next step was to start writing the proposal in a well-structured manner. This was the structure that I maintained (obviously it can be subjective) but it can help us to maintain a template: 
```
Title
Basic Details (Name, links, email, etc.)
About Me (Mentioned about myself, why I selected this project, and my time commitment)
Synopsis (Brief overview of the project)
Project Goals (This included Objectives, Tasks to be covered, implementation flow, and, testing details)
Timeline (I kept it weekly based)
Deliverables (What I plan to give at the end, future goals)
References (any external links you referred to while writing the proposal)
```

Then after writing my proposal in this structure, I asked the mentors to review
it and they provided some inputs as comments on the Google Doc and I made 
changes accordingly. 

**Then one thing we all have doubt is what to mention in the implementation details, timeline, etc. as other things are manageable right?** <br>
**Ans**:
One thing I would like to tell is first the time commitment part in the
**About Me** section. My mentor tried to ask me a tricky question like this there
```
please make sure that as much as possible is overlapping with central europe timezone. having a day job and then working on gsoc only during your nights is not good. if you have a day job in addition to gsoc, please say so.
```

So please don’t be lenient and mention that I have exams so I will be busy
half the time or I will go for other internships too with GSoC. Please don’t fall
into this trap as they expect you will be working for GSoC as a full-time job so
mention about this that I will work full-time for GSoC and will say prior to the
mentors if any emergency comes up.

Then coming towards the implementation details try to get familiar with the
codebase or depending on the nature of your project try to get around 
with things. Once that is done you will definitely get some self-boost in order 
to write the proposal. 

**Here is my way of writing the implementation flow:** <br>
```
1. Break the project into a set of achievable objectives.
2. Then cluster these objectives into a set of relevant tasks.
3. Then start writing details inside the tasks.
```

So talking about the details inside the task you can mention here whatever 
flow diagrams you want, code snapshots, etc. This is the part which needs to
be as detailed as possible. My mentors stressed a lot about being detailed in
this part.

Then further talking about the timeline try to mention out the timeline in 
accordance with the tasks that were developed before. What I did in my case
was starting from the community bonding period I mentioned that I will start 
coding in the mid of that. And please mention her what all you will document,
milestones, pull requests, etc. 

Then lastly mention about your final deliverables clearly like at the end what
will be achieved i.e. the overall state of their system due to our changes, 
benefits, etc.
Then in the future goals try to impress them by mentioning some things
that will be unique and you will be able to achieve them later after the GSoC
period as we should show them that we are willing to contribute even post
GSoC as this will showcase your enthusiasm to work with them. 
    
Concluding these were the things that I feel will help you in preparing your 
GSoC proposal well and at the end, I am also not selected yet so I can’t 
give you’ll surety that someone will get selected by following these
guidelines. I had given my good amount of time to prepare these proposals
and researching about various other things and it was not that piece of cake 
that can be achieved within a day or two so ….. start early : )

Sorry so in between I missed to mention about my other proposal i.e. the 
DIRAC one here the mentors were really impressed by my test performance
as it was real coding with four tasks involving unit testing, some OS things and
ElasticSearch related things. Then having experience of building the Rucio 
proposal helped me a lot here as again I had to be somewhat familiar with
their codebase, documentation, etc. and then asking proper questions the
mentors guided me properly otherwise the proposal template was similar to
the Rucio one obviously with the changes 

## 3) Submitting your proposal <br>
Please submit the proposal well ahead of time as don’t wait for that half an hour before the deadline like let me tell you a thing that happened with someone else. One guy had been working really hard on the proposal and but had some issue in his computer which showed that there were still 7 hours left with the submission (he was in IST and his PC showed GMT weird issue) then when he tried to submit the proposal he was not able to do that as the time had already passed away as the GSoC site takes the timestamp details from our local PCs and sadly he was not able to submit the proposal and the same thing happened with another guy as he had some issue with an image inside the doc pdf and at the end moment due to time constraint he was not able to upload the proposal even when he had it fully complete. The GSoC
committee won’t be able to help you with this as they clearly say please contribute out of GSoC if you are sure about your proposal. So this can be a nightmare for anyone out there. I submitted my proposal 3 days after the **“Students Apply”** period had started.

Lastly **“Best of Luck”** to whoever is reading this for preparing for GSoC and to myself too as I am not selected into the program yet : ) and sorry if it was too long!

**UPDATE:** I have been selected into GSoC 2019 and I will be working on the DIRAC project this summer!