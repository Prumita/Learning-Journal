# Waterfall

We know what this is! 5 steps are Requirements, Design, Development, Testing, Deployment. It's sequential (goes in order) and linear (moves in one direction only). 
Has it's place but is limited.

# Agile

Better! Overall.

Couple of different techniques here, scrum and kanban.

Scrum emphasises close collaboration and breaking things down.
Sprint is usually 1 to 4 weeks.

Kanban board.
Different categorised columns. Different stages of the project overall.
Timelines go from left to right. Backlog usually, then a work in progress, then testing, then final we've finished it section.
Don't want to overstack WIP. Individual tasks and work them through the system.
Need something demonstratable at the end of each sprint. As a stakeholder it provides confidence, direction, a chance to feed back.

Scrum roles
Scrum Master
Facilitator of the scrum. They:
- Faciliatate
- Improve
- Protect
- Reward
- Educate
- Encourage

They are helping planning meetings, define sprint goals, look at the backlog.

Sprint planning:
- Preparation
- Sprint goal definition
- Story selection
- Task estimation
- Planning poker
- Voting
- Consensus building
- Finalisation

Traditional project management way is this idea of planning poker. Not the easiest thing to explain. The project manager finds it quite difficult to explain even!
Task estimation.
People utilise as what they think of. Decide how many story points you'll have in a sprint. Quantifiable based off of ways of working, might differ.
Hypothetical, 20 story points. Capacity of workload. 
HIgh priority, customer really needs it.
Quantify the amount that I'm going to put into this. 
Debate over how long something is going to take. 8 out of 20, would have 12 remaining?
Capcity? Working out how much you can do. You know the next 2 week spring, 2 people working full time. 5 working days each per week, 29 days.
A days worth of work. So 19 days left.

Okay I don't think that was really explained at all?

Sprint master has an idea of everyone's capacity and ways of working etc. Product owner would want to push things forward from the backlog.
Sprint goal would need to be defined. HIgh level goal, what do we want to achieve at the end of the particular sprint.

## BUrndown Chart

y axis total number of story points, and we've got iterations or springs on the right.

Each spring, 10 story points. 

## Backlog

Effectively, we want to make sure that we are constantly understanding where the priorities are. What are the different user stories that we have available. How do we want to change based on the sprint, outcome of the previous sprint?
If doesn't mean that if it's in the backlog, the priorities are elsewhere. There's value to them.
Product owner comes in, makes sure the backlog is managed. Clarifying requirements. Make sure they align to overall project objectives.

So part of this is back log grooming.

If we've got the initial back log of ideas, refined and created into things that are functional.
Always have enough of the top items in the backlog groomed and estimated. They're in a good position and they have time put against them so we know how long they are going to take so they are ready to go into a sprint.
All the stories can be gathered, reviewed, prepared for the meeting.

## DoD (Definition of Done)
Figure that out, what is your definition of done?
Once all those things are ticked off, your story is done.

So for example there should be code, should be testing, should be peer review, story goal should be met.

It should be INVEST

Independent - Not copying something else.
NEgotiable - Can tweak and change
Valuable - Has some tangible value, worth us investing in
Estimable - Can we quantify it? How much time will it take?
Small enough? - This is a story, not a huge massive topic? 
Testable - Can we tell that we've managed to achieve it?

If a user story hits all the above, then it's well refined and eventually deliverable.

Need some sort of acceptance criteria, like definition fo done, when can we call the story complete?

Iterative refinement is also important. They will be refined with input from all over, so we can continuously improve and ensure that other user stories remain relevant and viable.

So think of answering as:

As a -
I want to -
so that I can - 

I remember phrasing things like this for Jira. We want to understand why we want to do this change. want to make sure we're working on something worthwhile.

So the starting point of a user story, there might be some problems.

Group lab

Story one 'As a customer service rep, I need an interface so that I can access customer data'

Specificity is a key problem with this, need way more detail on the interface, way more understanding of what they actually want to get out of that interface.

Story two 'as a user, I need to adminster accounts so that I can control account access'

## User story checklist

- Keep it short
- Keep it simple
- write from the perspective of the user
- Make the value/benefit of the story clear - what is the reason for the story?
- Describe one piece of functionality. If you have to write and break it into two stories that's fine
- Use stories as a team
- Use acceptance criteria to show an MVP (minimum viable product)

Epics! Woohoo Jira.
If we want to break down our stories into little chunks. Epic might be an overarching thing with different components relating to it. High level description, still aligned to the user story way of working.

## Lean (Six-Sigma) Framework

Inspired by Ford and invented in the Toyota factory.
Focused on the elimination of all waste
Toyota identified types of waste and wastefulness
  - Defects
  - Overproduction
  - Useless waiting
  - Underutilised talent
  - Excess processing
  - Transportation
  - Motion

The six-sigma DMAIC process we're familiar with:

- Define
- Measure
- Analyse
- Improve
- Control

Lean PIllars
- Define Value
- Map Value Stream
- Create Flow
- Establish Pull
- Pursuit Perfection

 ### Define Value
  You might see the value, does the end user?

 ### Map value stream

### Create flow
  Make sure things are smooth, continuous, not clunky

### Establish Pull
Need to figure out where the demand is coming from. React to things based on the need from the customers. So rather than forecasting or production schedules, don't make more than we need, just meet demand.

### Pursuit Perfection
Unlikely to be perfect on the first pass but we should be striving for perfection. Continuously iterate and change, don't just settle.
That seems really odd to me.

Dr Robert Charette in 1993 introduced the concept of optimising efficiency.
12 principles of lean software development.

Collaborative data workflow
CRISP-DM

Starts with business understanding. They have a problem they want to use data science to solve.
Customers are churning. End of their policy or subscription they don't renew it. 
Business wants to use the data science team to come up with a solution. Can we predict who is likely to leave and then offer them incentives? Can we identify why they are leaving?
Data understanding. What data can we use to sort this business problem? 
It looks very similar basically, business understanding ot data understanding to data prep to modelling to evaluation and then back to more business understanding or deployment. 
The thing here is that that cycle happens many times maybe by itself, but just to provide a baseline model. Then you might move alone to a refined model, but then do mre. That's what the diagram seems to be sayuing.

  # Scientific Method into data projects
  Anothe cycle that goes around, but it looks like this
  Make Observations
  Think of INteresting Questions
  Formulate Hypotheses
  Develop Testable Predictions
  Gather Data to Test Predictions (might then need to refine, alter, expand these and go back to develop)
  Otherwise make theoreis.

  

