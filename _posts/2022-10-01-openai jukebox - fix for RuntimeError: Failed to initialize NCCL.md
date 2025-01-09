----
title: openai jukebox - fix for RuntimeError: Failed to initialize NCCL
date: 2022-10-01
layout: post
----


<html>
<head>
	<title>openai jukebox - fix for RuntimeError: Failed to initialize NCCL</title>
<style>
html, body {
width: 666px;
        display: block;
        margin-bottom: 3em;
}
body {
        display: block;
        margin-bottom: 3em;
}
a:link { text-decoration: none; }
a:visited { text-decoration: none; }
a:hover { text-decoration: none; }
a:active { text-decoration: none; }

.column {
width: 666px;
   display: block;
  margin-bottom: 2em;
}
div {
           font-family: Consolas, monaco, monospace; font-size: 16px; font-style: normal; font-variant: normal; font-weight: 400; 
width: 666px;
   display: block;
  margin-bottom: 2em;
}
             </style>

</head>

<body>

	<H2>openai jukebox - fix for RuntimeError: Failed to initialize NCCL</H2>
<div >
<br>
I started to document a fix and share a patch diff for this, and evidently neglected to save my changes anywhere so all that is left of the effort is this doc I just found to be recovered when I started Libre Write a moment ago. I figure that even unfinished, this much may help someone struggling to get an openai jukebox colab to work here in the modern day (November 2022) after folks have apparently long since abandoned such things. 
</div>
<div >
  I leave this here, as I found it.. incomplete and with me lacking the motivation presently to go back and figure out what it was I was going to publish when finished because even incomplete, random red arrow image pointing at nothing included, it still offers an explanation and the simplest fix I found for the issue tracked at <b>https://github.com/openai/jukebox/issues/18 ( RuntimeError: Failed to initialize NCCL )</b> when running <a href="https://colab.research.google.com/github/sirbots/jukebox-the-continuator/blob/master/Jukebox_the_Continuator.ipynb">https://colab.research.google.com/github/sirbots/jukebox-the-continuator/blob/master/Jukebox_the_Continuator.ipynb</a> or even, with enough motivation, <a href="https://colab.research.google.com/github/openai/jukebox/blob/master/jukebox/Interacting_with_Jukebox.ipynb">github/openai/jukebox/blob/master/jukebox/Interacting_with_Jukebox.ipynb</a>
</div>
<div >
<hr/>
</div>
<div >
From dist_utils.py:</div>
<div >
<span> <img src="jukeboxfix_html_31a844a260f122e5.png" name="Image3" align="left" width="665">
<div>
<br><br>
<span>

<hr>


<hr>
This causes the jupyter kernel to bind to tcp port 29500 and *listen* on the loopback interface (because torch.dist.is_available() returns true) as if it is to be the MPI master, and it starts making connections to itself, as you see below.
</span>
</div>
<div >
</div>
<div >
 <img src="jukeboxfix_html_6845e7057e62d9a7.png" name="Image2" align="left" width="665" border="0"/>
</div>
<div >
If you interrupt or otherwise re-run the notebook from the same
Jupyter kernel, this tcp port will already be in use and the call to
_<u>setup_</u><span style="text-decoration: none">dist_from_mpi()
will try for n_attempts times and then bail out.</span></div>
<div >
<span style="text-decoration: none">A simple fix for this behavior is
to &ldquo;Restart runtime&rdquo; or &ldquo;Restart and run all&rdquo;
from Colab&rsquo;s Runtime menu, which will free up the port so that
it the setup_dist_from_mpi() call can succeed (for the first time,
like before, again but the same condition will occur if you attempt
to re-execute the cell in the same Jupyter runtime.</span><span style="text-decoration: none">)</span></div>
<div >
<img src="jukeboxfix_html_a685a7859b2430fc.gif" name="Shape1" alt="Shape1" align="left"/>
</div>
<div >
<br/>

</div>
<div >
<br/>

</div>
</body>
</html>
