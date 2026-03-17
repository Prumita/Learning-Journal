### Release pipelines

Fraud detection model is a new policy being rolled out to branches. You wouldn't just email it to every branch manager on a Friday afternoon, there's a process. Need to review, watch ap ilot. Get approval, then do a rollout. Release pipeline is the same process on the conveyor belt. Same review, pilot, approval, rollout, but, automated.

Artifact sources.
In software world, get abit disappointed with the word artifact and some sort of cool artifact. In software world, what is an artifact?
Think of it, apart from this whole thing apart sources, repositories etc, before we look at any of that, think of an artifact as, where does the thing you're releasing come from? Wherever that is, that's the artifact source.
fuck I missed it.
Okay source control. 

Okay, release gates, how do they project  quality?

- No new blocker issues
- Code coverage on new code greater than 80%
- no licence violations
- no vulnerabilities in dependencies
- no new technical debt introduced
- compliance checks
- are there work items linked to the release
- is the release started by someone else as the code committer
- is the performance not affected fter a new release

  Technical Debt - Netflix example
  Needed to fast track their development and take some shortcuts in order to get ahead of Blockbuster. But need to go back later on to fix these things, and if you don't it creates a technical debt. Netflix were developing quickly, might do a temporary solution that lacks scalability etc. Later on you may forget about it, or not allocate resources to do it, so they hit their target to advance over Blockbuster in terms of teir availabilities and features, but they had holes.

  was the release started by someone different to the person that wrote the code?
  Personal ngihtmare if you have to understand code that has an error but someone else commited.


  We didn't really go over the other bullet points.

  ### Release process versus release

  - The release process involves all the steps that you go through when you move your artifact that comes from one of the artifact sources.
  - A release is a page or container that holds a versioned set of artifacts specified in a release pipeline in your CI/CD process. It holds all the information reuqired to carry out all the tasks and actions in the release pipeline, such as the stages (or environments), the tasks for each one, values of task parameters and variables, the release policies such as triggers, approvers and release queuing options.
  - There can be multiple releases from one release pipeline (or release process)
 
    If Lloyds runs the same pipeline 5 times this week? How many release processes do they have?
    Just 1, not 5. Because they're running the same pipeline, but there's only 1 process. Release is 5 times, but the process or the recipe is 1.
    Okay so that's 1 process. But how many releases?
    5. There are 5 releases.
    So they released 5 times on the 1 release process.

    ### Azure DeOps release pipelines
    - Support pipelines as code (via YAML)
    - most capabilities from classic release pipelines are available
   
    Your pipeline definition lives in your GitHub repo alongside your application code. We'll see this in the lab.
    Microsoft is pushing everyone towards YAML right now.
    
