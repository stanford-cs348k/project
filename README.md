# CS348K -- Final Project Guidelines

## Deadlines
  * Initial draft of project proposal
  * Checkpoint
  * Final project presentations and writeups

## Proposal Document

We could like for initial project proposals to be submitted by 11:59pm on June 9th.  We expect a proposal to be submitted as a PDF document on canvas, however it's fine if that PDF document is simply a list of student names and a link to a web site where all project work will be documented.  Here is a suggested template for a proposal.

* __Project Title:__  A great title is catchy, but also descriptive!

* __Names and SuNET ID's__ of the students working on the project

* __Summary:__ A brief 2-3 sentence summary of your project goals.  This statement should be output-driven in terms of a demo, chart/graph, or image that you hope to make when the project is complete.  For example, _"We are going extend the JITNet idea from the paper reading to explore the trade off between rapid learning and remembering knowledge from the past, in particular by training on a mini-batch containing new frames and randomly sampled old frames. We will demonstrate high accuracy and high efficiency on an example video stream where a camera holder repeatedly walks inside and back outside of my apartment."_  OR _"I am going to build a system for rapidly finding and labeling examples of objects of interest in a large video collection.  I am going to demonstrate success by creating datasets for three new object categories in the Waymo dataset."_

* __Task list:__ No more than a few paragraphs of description of what you will do.  If your project is about algorithmic innovation, what is your basic approach?  If your project is about implementing an existing paper, list the parts of the paper you will need to implement.
  * Short list of things you will implement in order to "complete the project" (i.e., you expect to get a passing if you execute on all of these)
  * List of at most 1 or 2 “nice to haves” if you find yourself ahead of schedule

* __Expected deliverables.__ This is where I want you to focus on what demo you are going to show during your presentation, or what graphs you hope to make in your report.  This might be the place where I'd like to see the most detail in your proposal, since if you define a clear goal, your project activities will involve just working back from this goal to determine what needs to be done.  Are you trying to demonstrate an application, scheduled via Halide running at 30fps on your laptop?  Is there a particular image you want to create?  

* __Optional:__ a list of dependencies that your project requires.  This might mean starter code you've already found on the internet Or a technical paper/publication/blog post that you will use as a reference.  It might mean datasets or models that you've already found online.  We just want to clearly understand what you are starting with.  


## Final Writeup Guidelines
 
Your final project writeup is due at 11:59pm on June 9th.  You will submit on Canvas.

The writeup may be as short as a few pages, provided you hit the main points of defining the problem, defining your specific solution, and properly analyze the results.  I'm particularly focused on evaluation and results. Below is a sketch of some structure to help.
 
### Background
 
Describe the problem being solved.  The purpose of the background is to give the reader the technical background to interpret whether your results suggest you solved the problem well.
 
* What are the inputs/outputs
* What are the goals/constraints on a solution
* What is the research question that you are asking? (what is a falsifiable hypothesis that your results will either falsify or support?)
* What is the crux of the problem to solve? (what is the hard part of the project that forced you to learn something or figure something out.)
 
### Approach
 
Your description should be sufficiently detailed to provide the course staff a basic understanding of your approach. It might be very useful to include a figure here illustrating components of the system and/or their mapping to parallel hardware/or a DNN architecture.
 
* If your project involved optimizing code. Please describe the process of how you iterated toward a solution (what measurements did you make) What did you try that did not work? How to parts of the problem map to cores, threads, or vector lanes?
 
* If your project involved optimizing a DNN architecture, please describe the resulting architecture here, and be sure to provide intuition about how your model architecture choices were motivated by your goals.
 
* If your project involved started with an existing piece of code or DNN model, please clearly describe what you started with here, so it's clear what work *you* actually did in your project.
 
### Results

__This is the most important part of the writeup.__  Begin by providing your own definition of success (this should be in terms of your goals).  In other words, re-iterate the question you were trying to answer, or the performance boost you were hoping to obtain.  Then describe what data/experiment needs to be run to provide evidence that the goals were either met or not met.
 
Then, in all cases, we want you to describe the relevant parts of your experimental setup.  What were the baseline algorithms? What machine was a performance test run on?  What did you measure?  What was the dataset used?
  
Finally, I want to see the results of an experiment that demonstrate success (or failure) to meet goals.  Sometimes great projects fail to meet their goals, or falsify a hypothesis, but they still do a great job in the scientific process of verifying this.
 
This might include:
* Provide graphs of speedup or execution time?
* Compare total flops or model size
* Compare precision and recall of a model.    
 
__IMPORTANT:__ I want you to interpret your graphs and numbers for me.  What this means will be very project dependent, but I want you to consider questions such as: Why does the graph look like it does? Does it make sense to you?  What limited your speedup? Is it a lack of parallelism? (dependencies) Communication or synchronization overhead? Data transfer (memory-bound or bus transfer bound)?  If a model is performing well, what are it's failure cases? When does it fail to generalize.
 
As you answer these questions, provide data and measurements to support your conclusions. If you are merely speculating, please state this explicitly. Performing a solid analysis of your implementation is a good way to pick up credit even if your optimization efforts did not yield the performance you were hoping for.
 
#### References 
 
Please provide a list of references used in the project.
