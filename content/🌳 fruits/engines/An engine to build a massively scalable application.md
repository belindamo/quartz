Intention: get really good at frontend, ML modelling, marketing via AI writing tools

If I am to build a full stack app or extension in a few hours, do I have everything I need to do that? 
## What I suspect to be winning formula

Part I: Art
1. Model is fast, affordable, and accurate enough for use case
2. Effortless integrations, with balance of Joe Bidening but not too annoying
3. Interface has less clicks than existing option
4. Referral is easy for user to refer lots of other users

Part II: Business
1. Healthy SaaS metrics - [[🏡 scratchpad (<8 notes at a time)/How to saas]]
2. Healthy users, passionate and loyal past reason
3. Healthy conversion channel to signup metrics - [[🏡 scratchpad (<8 notes at a time)/how to user analytics]]

In reality this is pretty tricky because there are a few pieces to this:

Expertise areas required
1. Aesthetic design
2. Front-end code web app
3. Back-end server & databases
4. Model 
5. Marketing
	1. Landing page
2. Analytics tracking
3. Market landscape research

Processes
- How to design quickly?
- How to get a big audience for extension?
- Stack to host on something easy, fast, scalable?

## Scaling milestones
- Step 1: Win a niche 
- Step 2: Build up your distribution and brand
- Step 3: Leverage your data and brand to win adjacent niches and expand concentrically 
- Step 4: Repeat until IPO

## For AI extensions: Iterating on ML side
https://vivatranslate.slack.com/archives/C039ESW15S6/p1668477786270939
deploy model endpoints to prod frequently and often for testing. Like the time it takes to deploy an off-the-shelf model (whisper with no changes or GPT-3/GPT-2 with specific prompt) to a public endpoint should be <1 full day of work. Maybe even a couple of hours. If this is not true then our infra and/or process is broken

This is my hot take because to find out what resonates with users, we:  
1. deploy the most expensive off the shelf model/API that works well enough to start  
2. test for 30 min in a mock env. (like basic html page) with users or people who talk frequently with users (i.e. me/Tracy/non-engineers)  
3. if pass, deploy to production  
    a. if not, determine whether we need to (1) improve model or (2) it’s a deeper issue  
4. see how people use it  
    a. if they like, then we know to fine tune  
    b. if they don’t, then we determine whether to (1) improve model or (2) it’s a deeper issue  

Propose 1 full day for steps 1-3, assuming no holdups with chrome extension store.By doing so, we are able to test a lot of cool things quickly, past summarization. Plus, this is in line with process of testing big models first, see if they’re performant, then move to smaller maybe-fine tuned models that are faster.

## Web App
https://wickedblocks.dev/
Stack
- Tailwind
- React

Web app server triggered...
On web app view reusability
https://twitter.com/daveschatz/status/1593721401705656320?s=46&t=06HEJ0s32lr-dnOAFeLOWQ

## Landing page
Plenty of templates on Tailwind.

## Chrome Extension

### The Listing
**Format for Chrome extension
-   OVERVIEW
	- 1 tag line at top. No longer than a line
	- Next one is longer, like 3-5 lines. Explaining what exactly it is
	- Maybe a couple more 3-5 line blurbs
	- Some proof that we're great! 
	- Insert some features
	- Maybe some testimonials
	- Contact information at bottom
-   SCREENSHOT/VIDS
	- First is usually either a video or screenshot
		- If video, it's either
-   SUPPORT
	- For support, go to the website to submit. 

How to create the content of the overview and screenshots:
1. Take similar phrases from overviews of similar extensions that have 100k+ downloads and 4.5+ stars
2. Use those similar phrases but add twist that makes it even better
3. Plus - use their reviews to address further concerns

## Distribution
Set intention for each
- Twitter
	- Attract hires
- Tiktok
	- Max viral prospects

Could either:
- Hire fantastic and cheap content/marketing/growth folks from LatAm
- or AI writing/marketing tools
- or both!

## Case study - Viva Translate
2022-10

Key questions
- CODE
	- What does the code look like for each of the features below?
	- How do I breathe art into it, first and foremost? 
		- by understanding how it fully works. 
- DISTRIBUTE
	- How might we launch an extension to #1 in its category? 
	- How might we get an extension to get tens of thousands of downloads in 8 weeks
- How might we take these features and have code modules for... ^d67b23
	- X upon highlighting text
	- X upon input field focus
	- X upon detecting audio
	- X upon streaming text
	- X that is an overlay popup 
	- Signup in 1 step or less
	- Pay

- How might I give myself a README.md documentation cheatsheets to master all the pieces of...
	- Front-end
		- what are the current options?
		- how to build up a slick front-end fast?
		- CSS (using Github Copilot?)
		- React
	- Back-end
		- Database
	- Spin up a fast API
	- Spin up a fast database

How to speed this along with Github Copilot?

## Why is building an AI extension hard?
- Requires expertise from a fuckton of different skillsets, at present