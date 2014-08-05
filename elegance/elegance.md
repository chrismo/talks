# Healthy Programmer

.center[<img src="http://imagery.pragprog.com/products/323/jkthp.jpg" style="width: 50%;" />]

---

# Depression

.center.one-big[Greg Baugues http://blog.baugues.com/depression]

---

.center.one-big[<img src="http://cdn1.moneysavingmom.com/wp-content/uploads/2014/02/LivingSocial-Logo.jpg" style="width: 90%;" />]

---

layout: true
class: center, middle

---

# In Search of Elegance
???
Who am I?

Also wanted to do this talk since it's been on my mind recently and sort
of guinea pig it for you. I'd love feedback on it, it's still a bit 
rough around the edges.
---

# Elegant Code
???
What is Elegance? Steve Klabnik's philosophy in the time of software. 
---

## Win/Win
???
My own definition.
---

layout: false
class: left, top

# Trade-offs Suck

--

.center.two-big[Performs Better / Harder to Read]

--

.center.two-big[More Secure / Less Convenient]

---

layout: true
class: center, middle

---

# But That's Life
???
And most of our solutions have to cope with these trade-offs

---

#### except

---

layout: false
class: center, top

# Elegance FTW
???
But every once in a while we come across a solution that is Both/And instead
of Either/Or

--

.center.two-big[Clearer Code & Performs Better]

--

.center.two-big[More Secure & Easier To Use]
???
Over the years we've seen things within our industry come along that I believe 
are elegant solutions, or at least furthering our journey towards elegance...

---

# Big Time
???
Language-level, process, frameworks, QA technique

--

.center.four-big[OOP / Functional]
--
.center.four-big[Agile]
--
.center.four-big[Rails]
--
.center.four-big[TDD]

---

class: center, middle

# Isn't #IsTDDDead Dead?!
???
I don't intend to get into this debate

But thinking it through did help my identify where I think dhh went wrong, 
and I think this same pattern can apply to many situations where something
more elegant has been introduced in our industry

---

# Corrosive Effects
???
Anytime an elegant solution (win/win) gets over the initial adoption curve,
I believe we start to see various corrosive effects from groups within the 
community come to bear.  

Personal

Marooned -> mocks example. But don't blame the idea for the marooned.

Process -> end of the day, any conscientious developer wants to reflect on
their work and judge its value.
--
.center.three-big[Personal Gain]
--
.center.three-big[Marooned Explorers]
--
.center.three-big[Process over Product]

---

class: center, top

# Whether Ignorance or Malice
--
.center.one-big[Means over End]
???
All of these Corrosive Effects are just variations on people mistaking 
the means for the end.

But it can be difficult to judge, especially once something is into
or past the adoption phase and there's a LOT of activity around it, 
are we seeing corruption of an elegant idea, or is the supposed 
elegant solution inherently problematic .

---

class: center, middle

# End ➛ Elegance
???
And where I think dhh went wrong, was taking his legitimate observations
and laying them at the feet of TDD.

He saw the corrosive effects, but then blamed the end itself, rather than
seeing these as merely inevitable instances of people mistaking the means 
for the end.

---

# What About Trade-Offs?
???
Now if we back up a bit, it seems we _still_ have a struggle before we even
get to Corrosive Effects - I don't think trade-offs are the result of
corrosion as I've defined it, supplanting the Means for the End -- but that
Trade-Offs are a mere difficulty in grasping the End, due to limitations 
in my thinking, or inherent constraints in the problem.
--
.center.two-big[Limitations in Thinking]
--
.center.two-big[Inherent Constraints]
---

class: center, middle

# Elegance / Trade-Offs
???
And so to continue, I want to first switch the language from Elegance and 
Trade-Offs to 

---

class: center, middle

# Ideal / Pragmatic
???
Ideal and Pragmatic - because I think these words also capture this struggle
well. 

---

class: center, middle

![Pass the salt](http://imgs.xkcd.com/comics/the_general_problem.png)

???
All the time we have to grapple with where to draw the line in pursuit of the
ideal in order to keep things moving. Sometimes we know if we could just re-design
things first, then this new addition would be easier, but we frequently don't seem 
to have the time to 

---

.one-big[
(1) Write elegant code<br/>
(2) Attain Ideal<br/>
(3) Profit!
]
???
...do this the right way, and instead often times get caught up 
---

.one-big[
(1) Write first crap that comes to mind<br/>
(2) <strike>Attain Ideal</strike> #SHIPIT<br/>
(3) Profit???
]
???
in doing it this way. Ending many days with defeat.   
---

.one-big[
(1) Write first crap that comes to mind<br/>
(2) <strike>Attain Ideal</strike> #SHIPIT<br/>
(3) Profit!<br/>
(4) Bear the shame of being slain by yaks
]
???
Though - to be fair - unconstrained pursuit of the ideal doesn't always
 turn out so well (WATER)
---

.one-big-tall[
(1) Write elegant code<br/>
(2) Re-write it to be truly elegant<br/>
(3) ...<br/>
(4) Think about it some more<br/>
(5) <strike>Profit!</strike><br/>
(6) ...<br/>
(7) <strike>Attain Ideal!</strike> Go back to first principles
]

---

class: center, middle

# Ideal / Pragmatic
???
But I think it's important to understand this conflict and bear it in mind,
  especially in discussions around design and architecture. 

---

# Many, Small Services

.center.two-big[“I think we should be able to get a new, bare-bones service up in production in 5 minutes.”]
--
.center.two-big[“If it was that easy, we'd consume too many virtual instances and cause unnecessary expense.”]

---

# Ummmm....

.center.two-big[“So you think we should just have a few fat services?”]
--
.center.two-big[“No, that's the mess we have now.”]

---

# Hey - Wait ...

.center.two-big[“So what do you think we should do?”]
--
.center.two-big[“Well, we should have smaller services.”]

---

# If You'd Just ...

.center.two-big[“But that's what I'm saying!”]
--
.center.two-big[“But it's too expensive.”]

---

class: center, middle

![Shut Up I Hate You (Hyperbole and a Half)](http://content.screencast.com/users/the_chrismo/folders/Jing/media/76aaba9b-b388-4a90-bb72-5b92bfb0d41e/00000605.png)
???
It's at this point someone flips the plate of danishes off the conference room 
table and then everyone goes back to work.  

---

.one-big[
(1) Write first crap that comes to mind<br/>
(2) <strike>Attain Ideal</strike> #SHIPIT<br/>
(3) Profit???
]

---

class: center, top

# Context

.center.one-big[Ideal and Pragmatic]

???
I think clarifying the context of statements is important, and focus 
on debating either the ideal we're shooting for...

---

# Same Page

.center.two-big[“[Ideal!]”]
.center.two-big[“[Ideal!]”]

???
or the current constraints

---

# Same Page

.center.two-big[“[Pragmatic!]”]
.center.two-big[“[Pragmatic!]”]

???
but maybe not both simultaneously.

---

# Careful...

.center.two-big[“[Ideal!]”]
.center.two-big[“[Pragmatic!]”]

???
but maybe not both simultaneously.

---

class: center, middle, inverse

# AWKWARD SEGUE

![Segway Crash](http://i817.photobucket.com/albums/zz94/overkillphil/segway_crash.jpg)
???
I no longer have an awkward segue, but that slide's too awesome.

---

# In Search of Elegance
???
So far, we've looked at two general problems. 

--
.center.three-big[Corrosive Effects]
--
.center.three-big[The Problem of Pragmatism]
???
But I want to tack on a 3rd problem. 
--
.center.three-big[Personal Conflict]

---

# Conflict Resolution

.center.one-big.remark-code[Deadlock found when trying to get lock; try restarting transaction]
???
And as an example to play with, we go back to ...
---

class: center, middle

# MOAR #IsTDDDead?!

![Are You Kidding Me Meme Face](http://www.my-favorite-coloring.net/Images/Large/Famous-characters-Troll-face-Are-you-kidding-me-417533.png)
???
In the last IsTDDDead hangout, if you waded through it ...
---

class: center, middle

# With MOAR DHH

![DHH from IsTDDDead](http://i1.ytimg.com/vi/YNw4baDz6WA/0.jpg)
???
... there were some really interesting nuggets on the subject of confidence.

---

# TDD for Technical Confidence

.center.three-big[Make the problem easy<br/>then solve the easy problem.\*]

.right[ _\*Making the problem easy can be hard._ ]

.right.three-big[— Kent Beck]
???
First, Kent describes how TDD helps him drive out
the specifics of a design. "I've had an insight and I think if only I had 
this kind of object then I can separate out the complexity. So here's an 
example usage, and then I want to see the implementation, because 
sometimes the implementation will inform the API ... " and basically he
just goes on to describe the core idea of TDD, the design back that it
provides going back and forth between interface and implementation. 
 
---

# TDD for Personal Confidence

.big-para[Kent: “Programmers are prone to masochism. We'll do things over 
and over again. We'll put up with complicated systems, we'll be in 
dysfunctional social relationships at work and figure, oh well, people 
will just always yell at me. I grew up being taught to expect that. I'm just 
not going to feel confident, I'm not going to be able to measure progress, 
I'm not going to know whether I had any impact.”] 
???
But then he goes on to provide some more back story on his motivations for
 pursuing TDD.
 
And I know it's bad form to just read slides, but tough cookie.
---

# TDD for Personal Confidence

.big-para[Kent: “What I don't want to lose, is that the expectations of 
programming work have evolved in the last 10-15 years. I should be able 
to feel confident. I should be able to point to my contributions. I 
should have productive technical collaboration. Those things weren't true, 
they are true now. I don't want to lose those. If I had to sell [get rid 
of] TDD to get those, I would happily do it. To me that's far more important, 
that I can be my whole self at work. ... For me, TDD was an important part of 
achieving those effects, but it's really the effects [that matter].”] 
 
---

# TDD Intimidation

.big-para[DHH: “For me the purpose of getting involved [in IsTDDDead], was as much to give space to people 
I've talked to where TDD is not working for them, and they don't feel free 
to talk about TDD ... because they got accused of not being professional, 
because they weren't doing it right — because they _weren't_ getting 
confidence out of it, and feeling crappy about themselves.”] 

---

class: center, middle

# Not Just DHH
???
A friend of mine at the RailsConf keynote felt a bit vindicated by DHH's 
statements, and at a recent lunch here in 
Dallas, one of the other engineers mentioned he had a similar reaction as he 
doesn't have the same depth of experience on the subject that others like myself 
do and at times during rants about DHH in Campfire didn't necessarily feel 
comfortable to speak up and share his experiences. 

Which quickly led me back to   
  
---

class: center, middle

# Me
???
I have no shortage of confidence on this subject and am quickly frustrated by
DHH because I don't believe he knows his history very well and jumps to  
conclusions that don't appear to me to be very thoughtful. 
 
And yet I see how my own rants can steal space from the conversation for others 
like those DHH mentioned who may not always feel welcome to share their 
struggles or differences of opinion, and being confronted with that can see 
how I would contribute negatively to that.

---

class: center, middle

# You?
???
So what about you? Have you been on either side, or another side altogether
 in a debate, or in a situation where you simply did not feel you had room
 to put your two cents in?
 
If so, I encourage you to enter into the conversation. If your particular
 conversation is not safe, then obviously use your best judgment, but a portion
 of this talk wouldn't even exist had it not been for my co-worker saying
 something to me about the TDD thing at that lunch.
 
---

class: center, middle

# Common Ground
???
Because what's fascinating to me when looking at what drove Kent to promote
TDD in the first place, and what drove DHH to call out TDD recently was the
SAME THING - a desire to feel confident and to feel free in expressing 
oneself.

Or as Kent said, to be my whole self at work.
 
---

class: center, middle

# Culture
???
Our culture matters, I believe strongly in working to
have a culture of open and honest communication. The best people I've been
privileged to work with have always been humble, owning up to what they don't
know and open to hearing from others. That's what I strive for, even though
sometimes my own mouth gets in the way. 
 
So, thanks! 
 
---

# Thanks!!

.center.two-big[LivingSocial&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Dallas.rb]
.center.two-big[Chris Morris<br/>@the_chrismo | cLabs.org]
???
If you have any feedback for me on anything, I'd love to hear it. 
