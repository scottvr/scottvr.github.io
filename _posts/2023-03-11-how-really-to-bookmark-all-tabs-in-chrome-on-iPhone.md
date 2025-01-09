---
title: How to bookmark all tabs in Chrome for iOS (or "The Unreasonable Stability of Chrome on iOS")
date: 2023-03-11
---


<html>
<head>
  <meta charset="UTF-8">
  <meta name="description" content="Finally a guide showing you a better and easier way to bookmark all tabs in Chrome and iOS, none of that syncing to a PC opening them all there and then bookmarking them from the PC. That's silly.">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap@4.5.3/dist/css/bootstrap.min.css" integrity="sha384-TX8t27EcRE3e/ihU7zmQxVncDAy5uIKz4rEkgIXeMed4M0jlfIDPvg6uqKI2xXr2" crossorigin="anonymous">
  <style>
    html, body {
       overflow-x: hidden;
       margin-left: 0px;
    }
    body {
       position: relative;
      background-color: #fffdfc;
      padding: 5px;
    }
    pre { white-space: pre-wrap }
    .shrink {
    /*  transform: (0.8,0.8); */
    }
    .footer {
	    text-align: center;
	    vertical-align: middle;
	    display: flex;
      justify-content: space-between;
    }
    .spaced {
	    text-align: center;
	    vertical-align: text-top;
	    display: flex;
      justify-content: space-between;
    }


    @media only screen and (max-width: 1200px) and (min-width: 360px) {
        .column {
            justify-content: stretch;
            flex-basis: calc(100% - 2em);
        }
    }
    @media only screen and (min-width: 1200px) {
      .row {
       display: flex;
      }
      .column {
        justify-content: space-evenly;
        flex-basis: calc(50% - 2em);
      }
      .third-column {
        justify-content: space-evenly;
        flex-basis: calc(33% - 2em);
      }
      .column-border {
        border: 1px solid #000;
        padding:  7px;
        margin: 7px;
        justify-content: space-evenly;
        flex-basis: calc(50% - 2em);
      }
      .row-border {
        border: 1px solid #000;
        padding:  7px;
        margin: 7px;
        justify-content: space-evenly;
        flex-basis: calc(50% - 2em);
      }
      .alright {
        display: inline;
        text-align: right;
      }
      .govert {
        margin-top: 2em;
        text-align: left;
      }
      .covert {
          display: inline;
          vertical-align: middle;
      }
      .instruct {
  	    white-space: nowrap;
      }
      .instruct-text {
  	    display: inline-block;
  	    width: calc(100% - 400px);
  	    height: 500px;
  	    margin-left: 10px ;
  	    white-space: normal;
  	    vertical-align: middle;
      }
  }
  </style>
</head>

<body>
<div class="container">
<!-- // single wide column in top row -->
<div class="row govert">
<br>
<p style="margin-top: 2em;">
<h2 class="text-warning text-monospace">How to bookmark all tabs in Chrome for iOS</h2><br><hr><br></p>
<div class="text-secondary text-italic"><br></div>
<div style="font-family: Consolas,monaco,monospace; font-size: 14px">
<div class="text-secondary text-italic"> Or "The Unreasonable Stability of Chrome on iOS"</div>
scottvr at paperclipmaximizer.ai <span style="font-size: 12px">(2023)</span></div>
</p>
</div>
<hr width="50%">
<div class="row">
	<p class="govert"> For years now the <b>number of tabs</b> consistently open in Chrome on my iPhone has been, well, an unknown but certainly large number. Since long ago the number of open tabs on my phone has been at least 100. I know this because the tab "button" at the bottom of the mobile Chrome screen carries on it a two digit indicator, displaying how many tabs you have open, since that isn't apparent given the single-tab-focus interface afforded us by the phone's display. I know this because once you have more than 99 tabs open, Chrome for mobile completely stops keeping track for you how many tabs you have open, replacing the digital indicator with a sideways smiley emoticon, which I will admit does feel like an appropriate symbol as the number of open tabs on a handheld device approaches <b>ludicrous levels</b>. The ASCII emoji seems sorta like an Easter egg from the Chrome mobile engineering team, as a way to say <b>"lolwtf?"</b> in response to my habit of keeping an ungodly quantity of tabs open, waiting to be read.</p>
</div>
<div class="row"><p> Now, of course, anyone who has used Chrome on a PC knows that trying to sustain normal machine functions while running Chrome with 100 tabs open is a foolish endeavor, and that eventually your machine will grind to a halt because of it, or you will assist its <b>inevitable suicide</b> once Chrome has started to get all... Chrome-y. You’ll definiteley have to force-kill the app at some point, regardless of the quantity of open tabs or allegedly free system resources. Hopefully you have hit shift-ctrl-d before it gets to that point, bookmarking all the urls in tabs intended for another day that just hasn't come. But I digress. <b>(<i>I do that a lot</b> in the course of writing up this "quick" how-to, and <a tabindex="0" class="text-dark font-weight-bolder" href="#how-to"><span class="text-warning">if you're already feeling a bit</span> TL;DR</a>, you may click that to scroll to the actual instructions, skipping my lead-up commentary.</i><b>)</b></p>
</div>
<div class="row"><p>It's actually been a source of some consternation that at any point in time I expected Chrome for iOS to go the same route as Chrome for Windows has; that is, devolve into crappy software that is extremely frustrating to use, and that some day, like has happened many times on Windows machines, Chrome will crash and die, and the sessions open at that time will be lost, unrecoverable...  where even tedious manual searching through history cannot be entirely succesful even if one were willing to spend that much time and effort trying. <i>On my iPhone</i> though, <b>Chrome is rock solid</b>.  The way that it deals with (or doesn't) open-but-not-in-focus tabs is efficient and reliable, and Google needs to consider applying the same sort of solution to the its non-mobile namesake so that using the product is not the cycle of <b>bloat/crash/kill</b>, which inevitably becomes part of a desktop Chrome user’s normal workflow.</p>
</div>
<div class="row">
	<p>Anyway, where I was going with this and am slowly getting around to actually stating, is that the results from Googling how to bookmark all tabs on mobile Chrome would lead one to believe that there is no equivalent in the mobile app to <b>shift-control-d</b> on PC, and also no shortage of people offering <b>convoluted solutions</b> to the  problem in public forums, such as <a href="https://www.google.com/search?q=how+bookmark+all+tabs+chroms+ios&oq=how+bookmark+all+tabs+chroms+ios&aqs=chrome..69i57.6682j0j15&sourceid=chrome&ie=UTF-8"><i>using the Chrome Sync functionality to view the mobile device's open tabs from your pc’s Chrome history, and then select and open them all</a>(since there is no way to do what would seem obvious - right-click on a url in history and "add bookmark") in Chrome on your pc and <b>then</b> bookmark them there, which can be synced back to your mobile device.</i> While that would work, it would be in no way convenient, epecially when dealing with the unkown - but doubtlessly very large - number of tabs that I would be dealing with. </i></p>
</div>
<div class="row">
<p>
Even if that approach <i>was</i> the only way... As has been discussed up to now, opening 100+ tabs on the Windows version of Chrome is not a given to win. Attempting that will kill even my 16 core 5GHz i9 with 32GB RAM sure as shit so I don't really see it as a viable option, though you saw me.. I tried. And the other obvious solution to having  thia vast quantity of tabs I'm not looking at (but don't want to *lose*) doesn't sound any more attractive really, which would be just individually bookmarking and closing them one at a time. It might take as long as it has for me to accumulate them in the first place as well.
</p>
</div>
<div class="row">
	<p> So today (well, not really today, but rather the day I started writing this document that I just found on *actual* today today, unfinished but evidently published to a live site in an incomplete and embarrassing state. Though the article is titled as an instructional to finally provide a correct answer to the how to question, I had put this document online without actually explaining <b>how-to</b>. I just sorta lamented the state of Chrome for PC and then pasted a GPT-3 summarization of what I had written so far at the  bottom. *shrug*) - today I am here now to remedy that.   I figured out <i>how to <b>bookmark all</b></i> in mobile Chrome, and in doing so doscovered what the smiley face tab count indicator represents in my case, and figured some may find it interesting. (The <b>magnitude of the number surprised even me</b>.)</p>
</div>
<div class="row">
	<p> Now that I'm writing this (again), it occurs to me that perhaps I could have stayed better on task if I had taken a more positive approach to writing initially on the topic, perhaps focusing on how remarkably well Chrome on iOS works - both in general, and especially as compared to Chrome on a desktop platform. But, that said... who among us has <i>not</i> become disillusioned with Chrome today and nostalgic for the performance it once offered tnd delivered to us that prompted us to switch to it in the first place so many years ago, when it was Mozilla increasingly suffering from bloat. And then.. there was <b>ie</b>. Internet Explorer was, well.. <b>still ie</b>, and not much more needs to be said about that. Chrome had been the shot in the arm that web browsing needed at the time, but now, today... the once <b>spritely and powerfuli</b> browser leads the others only in terms of frustrating bloat, insufferable lag, and oh, so much crashing. Mozilla has urely seen Chrome's sorry state and perhaps sees in it another chance at winning the browser wars with Firefox, and heck.. even Microsoft is in the game now for that matter, since Bing now has CHatGPT - if you use Edge (and have been accepted to early access), making even the modern evolution of ie (which is itself based on Chromium) begin to look enticing. So I take  little personal responsibility for the tone of this message</p>
</div>
<div class="row">
<p> I should take a moment, however, to give thanks and props to the team responsible for the Chrome on iOS product. It knows how not to waste resources on tabs that aren't presently in focus, which I suspect accounts for the majority of the difference between the two solutions. I've probably said enough on the matter though already,  and you probably came here to learn <b>how to save all open tabs as bookmarks in Chrome on iOS</b> but  have been subject to my random stream-of-consciousness bashing of Chrome for desltop to this point.</p>
</div>
<div class="row">
<p> I will delay no further... I've even now taken some screenshots from  my phone so that when I link to this updated version of the doc, hopefully it will be decent to look at and easy to read. (I write this page ssh'd into my webserver, editing in vim, manually adding html markup as I go along. I'm not really a front-end guy, as is most certainly obvious. I should probably consider making use of a blogging platform or some such, but old habits die hard I guess.)</p>
</div>
<br>
<div class="row spaced">
<span class="spaced">So let me opine no more, but get straight to sharing knowledge via facts. Having said all of that...</span> <span class="spaced fs-3 font-weight-bolder"> <i>Let's begin!</i></span>
</div>
<span id="how-to"></span>
<br>
<hr>

<div class="row">
  <div class="column">
       <h3><b>Screenshots of Chrome from my phone.</b></h3>
<p style="vertical-align: bottom;">The image with the marked up arrow shows the area where, for up to 99 tabs, Chrome had displayed a count of how many I had open. You can see the old school ASCII sideways smiley face where the number used to be. It has been this way for years as I continue to accumulate open tabs, with apparently no negative impact on iOS Chrome's performance.</p>
      <br>
      <h2 class="text-warning text-monospace">How many tabs is <span class="text-secondary">:-)</span> anyway?</h2>
<center>
        <br>
        <img style="vertical-align: top;" src="https://killsignal.net/images/IMG_7889b.jpg"></img>
	<br><br>
        <p class="text-secondary text-monospace">That many. That's how many browser tabs I have open on my phone presently. I've been asked, and now I can answer.</p>
</center>

  </div>
  <div class="column alright">
     <img src="https://killsignal.net/images/IMG_7890.jpg"></img>
  </div> 
</div>

<br><br>
<HR>
<div class="row">
	<h2 class="text-warning text-monospace">So how exactly <i>do</i> we bookmark all tabs in Chrome on mobile?</h2>
</div> 
<div class="row"><p>
	Oh yes, that was my intent when I started writing this, wasn't it? That's what lead you here yet I've spent all of this time complaining, while yet resisting the urge to rail against unbounded leaky memory hogging Chrome essentially DoS'ing my system if I dare to leave it running even while I am using some other app. I haven't even mentioned the out-of-control google crash handler processes that serve some ironic purpose other than recovering from unexpected faults and I have already exceeded any estimable word count for writing on this topic by a good measure, all without really discussing the main topic inteded for this article! So perhaps I can deliver to you now the elusive instructions for the equivalent of shift-control-d on Windows within the mobile app, by way of pictures which surely are worth thousands of these words.
	</p>
</div>
	<br>
<div class="row">
	<div class="instruct">
     <img src="https://killsignal.net/images/IMG_7896.jpg" class="covert">

     <div class="instruct-text h2 alright">
	With Chrome loaded and in the foreground, press the aforementioned square at the bottom of the screen that is either displaying a two-digit integer, or shows a sideways ASCII smiley face emoticon, bringing you to the tab screen shown here. 
	<br><br><br><br>
	Tap "Edit" at the bottom left of the Chrome screen.
     </div>
	</div>
</div>
<br>
<hr style="width: 80%; height: 5px; border: none; background-color: #CCC">
<br>
<div class="row">
	<div class="instruct">
     <img src="https://killsignal.net/images/IMG_7897.jpg" class="covert">
	<div class="instruct-text h2 alright">
The "Select Tabs" and "Close All Tabs" menu will appear just above where you tapped, as shown in this image.
	</div>
	</div>
</div>

<br>
<hr style="width: 80%; height: 5px; border: none; background-color: #CCC">
<br>
<div class="row">
	<div class="instruct">
     <img src="https://killsignal.net/images/IMG_7898.jpg"></img>
	<div class="instruct-text h2 alright">
		Tapping on "Select Tabs" will display the "Select All", "Select Tabs", and "Done" options at the top of the screen, and little hollow blue circles will appear on the tab thumbnails, allowing them to be toggled as selected or not. <br><br><br>We have far too many tabs to be tapping in circles to select them.
		<br><br><br>
		Tap "Select All" in the top left, which will (naturally) cause every open tab to be selected. 
	</div>
	</div>
</div>

<br>
<hr style="width: 80%; height: 5px; border: none; background-color: #CCC">
<br>
<div class="row">
	<div class="instruct">

     <img src="https://killsignal.net/images/IMG_7899.jpg" class="covert">
	<div class="instruct-text h2 alright">
		Now all of the hollow circles in the top right of every tab thumbnail have become solid blue circles with white check marks on them. At the top of the screen, flanked on either side by "Deselect All"" and  "Done", you will see a number. In this case we see that 5,005 tabs are selected (amounting to all tabs currently open.) <h3><i>Et Voila!</i></h3>
	</div>
	</div>
</div>

<br>
<hr style="width: 80%; height: 5px; border: none; background-color: #CCC">
<br>
<div class="row">
	<div class="instruct">
		<img src="https://killsignal.net/images/IMG_7900.jpg" class="covert">
	<div class="instruct-text h2 alright">
		And for the Grand Finale, select "Add to Bookmarks". <br><br>You have just accomplished the equivalent of pressing shift-control-d (bookmark all tabs on your desktop system running Chrome), but minus the hanging and crashing pains that are normally a risk, and as a bonus found out how many tabs you really have open. <br><br><br><h4>(Or, alternatively, you have accomplished your goal of learning the number of tabs open and, in the process, how to bookmark all of them. I don't remember  which was my goal and which was a side effect now. Nevertheless, you can now start closing those years-old stale tabs without any of the painful anxiety and fomo that would normally accompany the task.</h4>  <h3><b>Q.E.D.</b></h  3>
	</div>
</div>
</div>
<br>
<hr>
<div class="footer text-muted">
		<span><a class="text-muted" href="https://www.paperclipmaximizer.ai">paperclipmaximizer.ai</a></span><span> | </span><span><a class="text-muted" href="https://www.killsignal.net/">killsignal.net</a></span><span> | </span><span> <a class="text-muted" href="https://www.disumbrationist.art">Disumbrationist.art</a</span>
</div>
</div> <!-- // end of container -->
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha1/dist/js/bootstrap.bundle.min.js" integrity="sha384-w76AqPfDkMBDXo30jS1Sgez6pr3x5MlQ1ZAGC+nuZB+EYdgRZgiwxhTBTkF7CXvN" crossorigin="anonymous"></script>
</body>
</html>

