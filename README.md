# CS348K Final Project Guidelines

## Deadlines

  * May 4, Initial draft of project proposal
  * Jun 3, Final project presentations (in class)
  * Jun 4, Final project writeups due

## Proposal Document (due May 4 -- soft deadline, feel free to submit earlier)

We could like for initial project proposals to be submitted by May 4th.  We expect a proposal to be submitted on Gradescope, however, submitted a PDF that just links to a website where all project work will be documented.  Here is a suggested template for a proposal.  __Note: This is a soft deadline.  It's more important to get the right project in place than to rush a proposal to meet the deadline.  However, those that do get proposals in on time will be the first to get staff feedback.__

* __Project Title:__  A great title is catchy, but also descriptive!

* __Names and SuNET ID's__ of the students working on the project

* __Summary:__ A brief 2-3 sentence summary of your project goals.  This summary is best if it begins with an output-driven statement terms of a demo, chart/graph, or image that you hope to make when the project is complete, and then follows up with 1-2 sentences about the approach.  For example:

> _"We are going extend the JITNet idea from the paper reading to explore the trade off between rapid learning and remembering knowledge from the past, in particular, by training on a mini-batch containing new frames and randomly sampled old frames. We will demonstrate high accuracy and high efficiency on an example video stream where a camera holder repeatedly walks inside and back outside of my apartment."_

> _"We are going to build a UI for rapidly finding and labeling examples of objects of interest in a large video collection.  We will demonstrate success by creating datasets for three new object categories in the Waymo dataset.  The system will contain components for visual similarity-based search and image clustering as key tools for finding data in the collection."_

> _"We are going to implement the full HDR+ pipeline from the Google paper with a focus on generating high image quality and much faster performance than assignment 1".
> 
> _"We are going write schedules in TVM to optimize a DNN model architecture that we commonly use in our daily research.  Our goal is to run 10x faster, achieved through both better architecture design and also aggressive optimization, which will significantly change our research iteration times."_ 


* __Task list:__ No more than a few paragraphs of description of what you will do.  If your project is about algorithmic innovation, what is your basic approach?  If your project is about implementing an existing paper, list the parts of the paper you will need to implement.  Specifically, please make sure this section has:
  * A short list of things you will implement in order to "complete the project" (i.e., you expect to get a passing if you execute on all of these)  __A VERY, VERY STRONG SUGGESTION is to make your first couple of tasks whatever needs to be done to get a code base running end-to-end.  That is, download, compile, and run starter code on a simple dataset.  Implement the baseline algorithm that your more advanced algorithm will be compared against.  Get the application to generate correct results (even without any optimization), etc. In other words, I want your projects to always be in a state where you can stop and evaluate how well you are doing. Therefore, additional work simply improves on the current results.  Your goal for the May 22 checkpoint should be *AT LEAST* to the state where all baselines are in place, or your code is running end-to-end on a trivial example.___
  * List of at most 1 or 2 "nice to haves" if you find yourself ahead of schedule at the end of the quarter.

* __Expected deliverables.__ This is where I want you to focus on what demo you are going to show during your presentation, or what graphs you hope to make in your report.  This might be the place where I'd like to see the most detail in your proposal, since if you define a clear goal, your project activities will involve just working back from this goal to determine what needs to be done.  Are you trying to demonstrate an application, scheduled via Halide running at 30fps on your laptop?  Is there a particular image you want to create?  

* __Optional:__ a list of dependencies that your project requires.  This might mean starter code you've already found on the internet Or a technical paper/publication/blog post that you will use as a reference.  It might mean datasets or models that you've already found online.  We just want to clearly understand what you are starting with.  

## Final Writeup Guidelines (due June 4)
 
Your final project writeup is due at 4pm PT on June 4th.  You will submit on Gradescope.

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
 
__IMPORTANT:__ In this writeup, _I want you to interpret your graphs and numbers for me_.  What this means will be project dependent, but I want you to consider questions such as: Why does the graph look like it does? Does it make sense to you?  What limited your speedup? Is it a lack of parallelism? (dependencies) Communication or synchronization overhead? Data transfer (memory-bound or bus transfer bound)?  If a model is performing well, what are it's failure cases? When does it fail to generalize.
 
As you answer these questions, provide data and measurements to support your conclusions. If you are merely speculating, please state this explicitly. Performing a solid analysis of your implementation is a good way to pick up credit even if your optimization efforts did not yield the performance you were hoping for.
 
#### References 
 
Please provide a list of references used in the project.

