# CS348K Final Project Guidelines

## Proposal Document 

We expect a proposal to be submitted on Gradescope, however, it's fine to submit a PDF that just links to a website where all project work will be documented.  Here is a suggested template for a proposal. 

* __Project Title:__  A great title is catchy, but also descriptive!

* __Names and SuNET ID's__ of the students working on the project. You are allowed to work alone, or in teams.  We'll set expectations for the level of difficulty of projects on a project-by-project basis based on team size.

* __Summary:__ A brief 2-3 sentence summary of your project goals.  This summary is best if it begins with an output-driven statement terms of a demo, chart/graph, or image that you hope to make when the project is complete, and then follows up with 1-2 sentences about the approach.  For example:
  - "We are going to build a UI for rapidly finding and labeling examples of objects of interest in a large video collection.  We will demonstrate success by creating datasets for three new object categories in the publicly available Waymo dataset.  The system will contain components for visual similarity-based search and image clustering as key tools for finding data in the collection. By the end of the project we are going to contribute new label-sets for the three new categories."_
  - "We are going to implement the full HDR+ pipeline from the Google paper with a focus on generating high image quality. We are not going to worry about performance (we plan to implement in Python), but we do plan to implemente as many of the algorithms as possible from the paper.  We are going to start with the RAW files provided online on the HDR+ datasets site and compare our final output images in terms of quality against the reference images provided by the Google dataset."._
  - "We are going write schedules in TVM to optimize a DNN model architecture that we commonly use in our daily research. We have starter code in PyTorch that is used by our research lab (we already have it in hand). Our goal is to come up with an implementation that is at least 5x faster, achieved through both changes to DNN architecture design and also aggressive scheduling optimization (we've already profiled the system to identify hotspots). The 5X multiplier was deemed to be sufficient to change research iteration times after conversation with my research adviser."_ 
  - "We are going to implement a new game in the Madrona game programming engine developed by Prof. Kayvon's group.  The idea is to create a game environment that simulates robot decision making tasks in apartment floorplans (pick up the empty cups and bring them to the kitchen).  Given this environment we are going to take the PPO-based RL training code we already have, and use it to train policies that perform the desired task.  The project will include work to performance optimized the simulation environment we implement, and explore trade-offs in hyperparameters of the RL training loop.)" 
  - "We are going to read NVIDIA's latest papers on sample efficient ray tracing (based on the idea of ReSTIR).  We are going to implement our own versions of of htese algorithms in a GPU accelerated ray tracer, and show demo a demo of the system running in real-time.  We are going to start with a simple Vulcan-based ray tracer codebase that we implemented as a project in CS248, and add all the necessary features to perform ReSTIR accelerated many-light and global illumination sampling."

* __Inputs and outputs:__ List the inputs and outputs of the implementation, as well as the major constraints on your design (is the fundamental constraint machine performance? is it human time?).  In this section I want you to take lessons from the papers we've read that did a good job of articulating this problem setup. 

* __Task list:__ No more than a few paragraphs of description of what you will do.  If your project is about algorithmic innovation, what is the basic proposed approach?  If your project is about implementing an existing paper, list the parts of the paper you will need to implement.  Specifically, please make sure this section has:
    * A short list of things you will implement in order to "complete the project" (i.e., you expect to get a desirable grade if you execute on all of these)  __A VERY, VERY STRONG SUGGESTION is to make your first couple of tasks whatever needs to be done to get a code base running end-to-end.__  That is:
        * Download, compile, and run starter code on a simple "hello world" example or dataset. Applicable, please describe where you are getting the started code, start datasets, etc. from.
        * Pick (or create) the dataset that you will use on a daily basis throughout the project timeline.
        * Implement the baseline algorithm that your more advanced algorithm will be compared against.
        * Get the application to generate correct results (even without any optimization), etc. 
        * In other words, I want your projects to always be in a state where you can stop and evaluate how well you are doing end-to-end. Therefore, additional work always simply improves on the current results. __Your goal in the first week of the project should be *AT LEAST* to get to the state where all baselines are in place, or your code is running end-to-end on a trivial example__
  * List of at most 1 or 2 "nice to haves" if you find yourself ahead of schedule at the end of the quarter.
  * For projects with multiple students on a team, please attempt to assign responsibilities for the various components of the project.
  
* __Expected deliverables and/or evaluation.__ This is where I want you to focus on what demo you are going to show during your presentation, or what [sequence of] graphs you hope to make in your report.  This is the place where I'd like to see the most detail in your proposal, since if you define a clear goal, your project activities will involve just working back from this goal to determine what needs to be done.  Are you trying to demonstrate an application, scheduled via Halide running at 30 fps on your laptop?  Are you going to demonstrate reasonable accuracy models that were trained in 30 minutes of labeling work? Are you going to demonstrate a CUDA ray tracer that uses a BVH build using techniques from advanced graphics papers? Is there a particular image you want to create? __Specifically, I want you to consider and write down how will you evaluate/determine the extent to which you were successful.__

* __What are the biggest risks?__ Please document the biggest risks in the project.  Often there are points or blockers such as, if I can't get this code to compile/run, then I can't do the work.  Or, until I am successfully training this DNN and have reasonable trained model, I can't do aynthing else.  I want you to think through the risks on your project, and consider how to eliminate/derisk these aspects of the project with as little work as possible.

* __What you need help with?__. What advice would like from Kayvon and Arden? Are there papers you need references to? Do you need a machine or computing resources to succeed?

## Final Report

The writeup may be as short as a few pages, provided you hit the main points of defining the problem, defining your specific solution, and properly analyze the results. I'm particularly focused on evaluation and results. Following the structure below will help.

* You will make a presentation that should fit in a 6 minute slot.  __In this presentation, all project team members should speak, and you should aim for a total presentation time of about five minutes (to allow for setup).__ 
* Your final report should be handed in by Thursday June 6th, 11:59pm.

### Project Title

Give your project a snazzy title. :-)  Please list the names and Stanford email addresses of all students on the team.

### Background and Setup (approx 1 page)

Provide a description of the problem being solved.  The description can be short (like the introduction section of a paper), but make sure you hit all the main problem definition points we talked about in class:

* What are the inputs/outputs?
* What are the goals/constraints on a solution?
* What is the question that you are asking and trying to answer? (Or equivalently: what is the falsifiable hypothesis that your results will either falsify or support?)

And finally, given this setup of goals and constraints...
* What is the crux of the problem to solve? (What is the hard part of the project that forced you to learn something or figure something out.)

### Approach (approx 1-2 pages max)

Please describe your approach.  Please be brief (about a page or so max), but your description should be sufficiently detailed to provide the course staff a basic understanding of your approach. It might be very useful to include a figure here illustrating components of the system and/or their mapping to parallel hardware/or a DNN architecture.

* If your project involved optimizing code. Please describe the process of how you iterated toward a solution (what measurements did you make) What did you try that did not work? How to parts of the problem map to cores, threads, or vector lanes?

* If your project involved optimizing a DNN architecture, you could describe the architecture here, and be sure to provide intuition about how your model architecture choices were motivated by your goals.

* __If your project involved started with an existing piece of code or DNN model, please clearly describe what you started with here, so it's clear what work you actually did in your project. e.g., "We started with this codebase and made these changes..."__

### Evaluation and Results (as many pages as needed to make the points you want to make)

To the staff, this is the most important part of the writeup. Begin by providing your own definition of success (this should be in terms of your goals). In other words, re-iterate the question you were trying to answer, or the performance boost you were hoping to obtain. Then describe what data/experiment needs to be run to provide evidence that the goals were either met or not met.

Now describe the relevant parts of your experimental setup. What were the baseline algorithms? What machine was a performance test run on? What did you measure? What was the dataset used?  If you have a programming abstraction project, the experimental setup might include a description of the programs you implemented expressed using the API.

Finally, I want to see the results of an experiment that demonstrate success (or failure) to meet goals. Sometimes great projects fail to meet their goals, or falsify a hypothesis, but they still do a great job in the scientific process of verifying this.

This might include:

* Provide graphs of speedup or execution time?
* Compare total flops or model size
* Compare precision and recall of a model.
* Demonstrate that a 3D NeRF model was obtained, show output images of sufficient quality, etc.

IMPORTANT: In this writeup, I want you to interpret your graphs and numbers for me. What this means will be project dependent, but I want you to consider questions such as: Why does the graph look like it does? Does it make sense to you? What limited your speedup? Is it a lack of parallelism? (dependencies) Communication or synchronization overhead? Data transfer (memory-bound or bus transfer bound)? If a model is performing well, what are it's failure cases? When does it fail to generalize.

As you answer these questions, provide data and measurements to support your conclusions. If you are merely speculating, please state this explicitly. Performing a solid analysis of your implementation is a good way to pick up credit even if your optimization efforts did not yield the performance you were hoping for.

### Team Responsibilities

Please provide a [very short] breakdown of which parts of the project were performed by each team member. In general we hope to (and intend to) give all team members the same grade, but we still want to know what everyone worked on and what their role was.   

### References

Please provide a list of references used in the project.
