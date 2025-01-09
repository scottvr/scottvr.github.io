---
title: openai jukebox - fix for RuntimeError: Failed to initialize NCCL
date: 2022-10-01
lhayout: post
---


### status

Some time back, I started to document a fix and share a patch diff for this, and evidently neglected to save my changes anywhere so all that is left of the effort is this doc I just found to be recovered when I started Libre Write a moment ago. I figure that even unfinished, this much may help someone struggling to get an openai jukebox colab to work here in the modern day (November 2022) after folks have apparently long since abandoned such things. 

I leave this here, as I found it.. incomplete and with me lacking the motivation presently to go back and figure out what it was I was going to publish when finished because even incomplete, random red arrow image pointing at nothing included, it still offers an explanation and the simplest fix I found for the issue tracked at <b>https://github.com/openai/jukebox/issues/18 ( RuntimeError: Failed to initialize NCCL )</b> when running <a href="https://colab.research.google.com/github/sirbots/jukebox-the-continuator/blob/master/Jukebox_the_Continuator.ipynb">https://colab.research.google.com/github/sirbots/jukebox-the-continuator/blob/master/Jukebox_the_Continuator.ipynb</a> or even, with enough motivation, <a href="https://colab.research.google.com/github/openai/jukebox/blob/master/jukebox/Interacting_with_Jukebox.ipynb">github/openai/jukebox/blob/master/jukebox/Interacting_with_Jukebox.ipynb</a>

### the problem

From dist_utils.py:

![image](https://github.com/user-attachments/assets/631e6f22-1592-46ba-a69b-d02adefb71e6)


<hr>
This causes the jupyter kernel to bind to tcp port 29500 and *listen* on the loopback interface (because torch.dist.is_available() returns true) as if it is to be the MPI master, and it starts making connections to itself, as you see below.

![image](https://github.com/user-attachments/assets/74f8fbfb-a947-4cf5-85be-5566e686a905)

### the symptom

If you interrupt or otherwise re-run the notebook from the same
Jupyter kernel, this tcp port will already be in use and the call to
_<u>setup_</u><span style="text-decoration: none">dist_from_mpi()
will try for n_attempts times and then bail out.</span></div>


### the <strike>fix</strike>workaround

A simple fix for this behavior is
to `Restart runtime` or `Restart and run all`
from Colab's Runtime menu, which will free the port so that 
the setup_dist_from_mpi() call can succeed (for the first time, like before, again but the same condition will occur if you attempt to re-execute the cell in the same Jupyter runtime.)


## hope that was helpful!
