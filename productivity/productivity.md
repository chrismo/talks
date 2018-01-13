
layout: false
class: center, middle

## Habits of a 2.76x Developer

???

-- Talk prepped for Jan 2018 meetup of http://devproductivity.io

My name is Chris Morris, I'm the Director of Engineering at Mystery Science and technically still a core
team member of Bundler, but I haven't been able to contribute there in a long time.

Before we get into my talk today, some shout-outs

---

# Healthy Programmer

.center[<img src="http://imagery.pragprog.com/products/323/jkthp.jpg" style="width: 33%;" /> 
        <img src="http://33.media.tumblr.com/3a67e4ea496cbad39b23bf48e046c810/tumblr_nasiplAH851qhu3vxo1_500.gif" style="width: 50%" />]

???

This book was published in 2013, so, y'know, like light years ago, but The Healthy Programmer has some 
wonderfully practical advice for those of us who make a living the way we do.

In short: "Read this book so you don't die in your chair." Hat tip to my friend Sara Flemming for the gif. 

Also, I think we should just start saying Jeh-Gif in the spirit of compromise and unity.
/ I never know how to say it, so I just say it both ways.


---

# Open Sourcing Mental Illness

.center.four-big[osmihelp.org<br/><br/>]
.center[<img src="https://osmihelp.org/assets/img/osmi-logo-big.png" style="width: 33%" />]

???

The OSMI support forums evolved out of a site called Devpressed started by Greg Baugues, they can be a 
great place to get some support for yourself or if know someone who struggles with mental issues.

---

# The Pragmatic Programmer  

.center[<img src="https://imagery.pragprog.com/products/59/tpp.jpg?1339433898" style="width: 45%" />]

???

Then finally, since this talk will largely be on a process and tactical level, I have to give a shout
out to the classic Pragmatic Programmer book since a lot of the stuff in my talk is either ripped off
or inspired by this book.  

---

layout: false
class: center, middle

.center[<img src="10x.programmer.png"/>]

???

The idea of a 10x developer can at least be traced back to a 1996 book by Steve McConnell called
Rapid Development and possibly the 1st edition in 1993 of his book Code Complete, which in turn
cite earlier studies, the quality of which are easily called into question.   

---

layout: false
class: center, middle

.center[<img src="https://s3.amazonaws.com/titlepages.leanpub.com/leprechauns/hero?1498560320" style="width: 40%"/>]

???

For a counterpoint view on 10x and other topics, which arose specifically from a critique on Steve
McConnell's writings.

The 10x developer, or 5x, or 2x, or 1.1x may be a myth, but if they do exist, in my opinion they 
subsist on small habits that buy themselves
productivity over the long haul, vs. folks who can just type 10 times as fast as you.

---

# Trade-Offs

![Pass the salt](http://imgs.xkcd.com/comics/the_general_problem.png)

???

Most experienced developers understand that quality engineering involves trade-offs. Security vs. Convenience,
code that reads well vs. performs well, and short-term vs. long-term productivity.

---

class: center, middle

![Highway sign pointing to Hell](http://www.funnysigns.net/files/hell-froze-over.jpg)

???

The road to hell is paved with misguided compromises and shrug emoji. 

---

class: center, middle

![Spongebob Celebrating](http://2.bp.blogspot.com/-PuXgy-MI84k/Tzh7rQ4CgsI/AAAAAAAAAik/tG4i8LbEjNg/s1600/spongebob.gif)

???

The road to hellacious productivity is simply paved with better compromises.  

---

# Long > Short

.center[![Ketchup bottle](http://i.telegraph.co.uk/multimedia/archive/03245/ketchupembed_3245375b.jpg)]

???

Considering the long term impact of our decisions is usually the wiser approach.

---

# Sometimes You Gotta Ship

.center[![ShipIt Squirrel](https://qph.ec.quoracdn.net/main-qimg-c8781a4bb1f17e330b50cb35f851da05-c)]

???

Though sometimes we gotta get stuff out the door. So ... before we go into more detail
on longer term stuff, we should call out the necessity of shipping. Sometimes Short wins.

---

# Negotiate for the Long 

.center[<img src="https://qph.ec.quoracdn.net/main-qimg-c8781a4bb1f17e330b50cb35f851da05-c" style="width: 33%"/>
        <img src="http://i.telegraph.co.uk/multimedia/archive/03245/ketchupembed_3245375b.jpg" style="width: 33%"/>]

???

But when that happens, be sure to negotiate for time to clean up your mess. So you can 
have your squirrel and ketchup cake and eat it too.

---

class: center, middle

# Testing

???

I'm going to talk a lot about testing. Testing and Design go hand-and-hand really.
Musicians listen back to their songs, artists and sculptors step back to look over
their work. 

---

# Testing

Test yo self before yo self.fail!

???

Testing is really this larger behavior to help try and get it right the first time to minimize future changes and the associated costs with revisiting work.
Give yourself the best chance of getting it right the first time AND give yourself the best chance of changing it painlessly in the future. Iteration and feedback are the law of the land … do it in the small in the beginning, do it as you go down the road, too.

---

Testing

dbrady: It's 2018. Do you really think testing is good? All this talk of fast, clean, readable, etc I'm starting to feel like we think testing sucks. Slow, ugly, unreadable all suck. Fast, clean, readable isn't good, just less sucky. Is testing good, or just an accepted evil?

the_chrismo
@dbrady @alexford Tests help me think about and even shape the design of my production code. Built-in rubber duck. /me is happy :)
Jan 11, 2018, 4:50 PM
https://twitter.com/the_chrismo/status/951587076138442752

dbrady
@the_chrismo @alexford THIS is literally the first reply all day that proposes an intrinsic benefit of testing rather than an investment/cost to be minimized and/or whose eventual payoff is hoped to be maximized
Jan 11, 2018, 5:02 PM

---

# Test Suite as Deploy Checklist

A tiny robot QA army. “I wrote it down in my diary so I wouldn’t have to remember!” - https://memegenerator.net/img/instances/67492661/i-wrote-them-down-in-my-diary-so-that-i-wouldnt-have-to-remember.jpg

???
Tests serve as this long term sentry to help you remember all the things you wrote. Checklists are a powerful tool used in aviation and medicine. Our test suites are a huge, automated pre-deploy checklist.

---

# Tap the Breaks

_fast and furious_

???

Don't be obsessed with the speediness of your test suite. It can lead to over-mocking and other
short cuts which diminish the quality of your tests. 

---

# Alternative to Not-As-Fast-As-I-Want Tests

the_chrismo
@dbrady One alternative is a separate QA dept that's under-resourced on time and people and you have to wait 3+ weeks to get shrug-percent coverage.
Jan 11, 2018, 4:47 PM

---

# Likewise, maybe Integrate and Skimp on Units

???

Since quality is the goal, then maybe fewer tests that are more integrated are better than lots 
of unit tests. 

---

# Run Only What You Need

???

Run only tests that you need locally (LEARN HOW TO DO THIS), lean on CI to cover unlikely places being impacted. Remember these suites, store them up, when you notice patterns, maybe that's something you can abstract out into a gem.

 
---

Mind your boundaries. Services classes gems are just different mechanisms to enforce boundaries, count the cost. Sometimes we choose a harder boundary to force decoupling, when if we just tested in isolation more, we could achieve the same thing 
Sometimes moving code out into its own gem or service will help not only with the boundary, but with minimizing the test suite that needs to be run inside a monolith. Of course, now you’ve opened the door for integration test failures. 


---

# Use Tests as a Reminder

fail “Remember this” if Time.now > ‘2018-02-01’

---

# Creative Test Usages

???

I've used test automation to scan the test logs after a test suite run looking for credit card 
number patterns to help ensure we weren't logging them.

---

# Mock Love

???

Consider building a mock service, mock tool. Great for exploratory testing. (eInstruction mock receiver, GameStop mock Microsoft, MSci bulk mailer utility code, these can also fight the darkness)

---

# Test in Production

???

Sometimes the only way to test things in production is to test it in production. Do this judiciously, but recognize when you need it and use feature flags to protect the general user population. Trying to build up a staging environment that’s just like production so I don’t need to test in production can be a big distraction.
Make sure you can revert quickly. Rescue nil can be your friend when judiciously used in cases like this - but only temporarily.

---

# Refactoring / OOP

When in Branson … https://i.pinimg.com/474x/1c/d3/51/1cd3515613f1213dd47375c71bd2aa9d--branson-missouri-redneck.jpg
???
If you work in an OOP language, know your OOP. SOLID principles. Sandi Metz. Go with the grain. This isn’t so much about short term productivity, but buying you long term flexibility. Know your basic refactorings - if nothing else, know that most refactorings have an opposite. This is the more artsy side of engineering.


---

# Delete Old Code

???

It’s a time waster. It clogs your IDE, it gets included in grep results and can waste time doing analysis on stuff that’s not even used anymore. Production code coverage tools are a thing. https://github.com/danmayer/coverband

---

# Ask for Help

???

Rubber duck in Slack (have a rubber duck room). Rubber duck in your card/ticket. Take a walk and talk out loud like a crazy person. Come up for air, take breaks. 

---

# Pair
???
Pairing can yield interesting insights into how others do things. 

---

# Optimization
???
The general consensus on optimization is you shouldn’t optimize early … but it doesn’t hurt to learn some SQL to avoid some obvious places where AR / your option are issuing more queries than are necessary. Keep that SQL logging on. 


---


# Good commit messages
Explain yo self before you forget yo self.
???
Not just commit messages, code comments, class names, methods, readme. Pay attention to the distance between the code and where the documentation resides. If you need separate docs, maybe you can automate it so the source stays close to the source.


---

# Keep (and COMMIT!) your utility code
???

This is one habit I don’t see often enough. At LivingSocial, our ops folks were really good about ensuring console history was kept after someone left. That’s great. Except that if I’m taking the time to write it in the first place, stash it somewhere, commit it. You won’t come back to all of it, but that stuff you will come back to can be refined and iterated on, and eventually some of it will make it into the production codebase.

---
# DON’T DO THINGS MANUALLY
Automate yo self before you continue to do the same ol' damn thing over and over again until you 
give carpel tunnel to yo self.
???
As much as we love automation, it’s amazing how often we’ll still get into cesspools of manual labor.

---


# Hack in production
???
Put the code in an editor. Use a redefinition of the class to copy/paste code into prod console to play with it there. But then Keep it!

---

# Build the Light 
Dark is the default.


---

Healthy teams are productive teams - this trumps the rest.


---

.center[![Mystery Science logo](MSci.jpg)]