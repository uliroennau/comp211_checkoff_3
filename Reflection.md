# Reflection

## How I approached learning MLFQ

I started with no background at all. When I first started my conversation with Claude, it went straight into MLFQ's rules, so I had to ask it to start from the ground up. From there, my learning followed a chain of first understanding how a CPU core is limited to run a single program at a time, understanding First Come, First Served, Shortest Job First, Round-Robin, and finally Multilevel Feedback Queues. I was first introduced to "first-draft rules," which served to be a good segway into MLFQs but were ultimately too breakable, which led to an adjustment of them that fixed the issues.

## Representative Prompts

1. *"Assume I don't know anything about scheduling... I need really from the ground up knowledge."* This reset the conversation to a level I could follow.
2. *"I'm not sure I understand response time... why is the turnaround for job C 120 milliseconds and not 10?"* I had confused how much work a job needs with how long it takes from arrival to finish. Separating run time from turnaround was the turning point for me.
3. *"Wait, so giving up CPU time refreshes your slice?... It would still have to make a sacrifice of being put back in some queue, no?"* I pushed back on the claim that a cheating program could take "nearly all" of the CPU. Claude agreed and corrected it: the 90% figure only holds against jobs at a lower level.

## How I engaged with AI

I used Claude as a tutor instead of a simple answer key. After every new concept that was explained, I worked through practice problems by hand that were corrected by Claude before moving on (and I made real mistakes along the way if you take a look at the chat!). I also caught an overstatement that Claude made, and I checked the material against Chapter 8 of *Operating Systems: Three Easy Pieces*. As for the presentation, I asked for input as to how I could structure the slides and what content that we went through would be key to include. I chose an animated walkthrough over running code (which was discussed with CeCe).

## What I'd do differently

I think that reading the chapter mentioned above *alongside* the conversation with Claude would help as I could fact-check more frequently and not just at the end. I would also explain each idea in my own words before asking for the next one; though the questions that I worked through helped in a way analogous to this, explaining the concepts to myself may have been even better!
