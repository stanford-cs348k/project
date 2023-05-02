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
        * Download, compile, and run starter code on a simple "hello world" example or dataset
        * Pick (or create) the dataset that you will use on a daily basis throughout the project timeline.
        * Implement the baseline algorithm that your more advanced algorithm will be compared against.
        * Get the application to generate correct results (even without any optimization), etc. 
        * In other words, I want your projects to always be in a state where you can stop and evaluate how well you are doing end-to-end. Therefore, additional work always simply improves on the current results. __Your goal in the first week of the project should be *AT LEAST* to get to the state where all baselines are in place, or your code is running end-to-end on a trivial example__
  * List of at most 1 or 2 "nice to haves" if you find yourself ahead of schedule at the end of the quarter.
  * For projects with multiple students on a team, please attempt to assign responsibilities for the various components of the project.
  
* __What you need help with:__. What advise would like from Kayvon and Arden? Are there papers you need references to? Do you need a machine or computing resources to succeed?

* __What are the biggest risks?__ Please document the biggest risks in the project.  Often there are points or blockers such as, if I can't get this code to compile/run, then I can't do the work.  Or, until I am successfully training this DNN and have reasonable trained model, I can't do aynthing else.  I want you to think through the risks on your project, and consider how to eliminate/derisk these aspects of the project with as little work as possible.





* __Expected deliverables and/or evaluation.__ This is where I want you to focus on what demo you are going to show during your presentation, or what [sequence of] graphs you hope to make in your report.  This is the place where I'd like to see the most detail in your proposal, since if you define a clear goal, your project activities will involve just working back from this goal to determine what needs to be done.  Are you trying to demonstrate an application, scheduled via Halide running at 30 fps on your laptop?  Are you going to demonstrate reasonable accuracy models that were trained in 30 minutes of labeling work? Are you going to demonstrate a CUDA ray tracer that uses a BVH build using techniques from advanced graphics papers? Is there a particular image you want to create? __Specifically, I want you to consider and write down how will you evaluate/determine the extent to which you were successful.__

* __Optional:__ a list of dependencies that your project requires.  This might mean starter code you've already found on the internet Or a technical paper/publication/blog post that you will use as a reference.  It might mean datasets or models that you've already found online or computing resources you need. (e.g., access to GPUs)  We just want to clearly understand what you are starting with.  
