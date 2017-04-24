## Welcome to Julia's Software Engineering Page

### January 16th, 2017

What Software Engineering Means to Me:

```markdown
It seems as though everyone in my family is a genius in their own way,
but my father is a genius in almost every way. He has a degree in 
Aerospace Engineering, Software Engineering, and Electrical Engineering,
so let's just say he has a lot of books about every subject. As a child,
we used to take things apart and try and build other things from the parts
we had disassembled, he would solder every circuit board I would shove at him,
and we would do every "nerdy" activity together, me being the imagination, and
he the one to actually create the things I dreamed up. 

Software Engineering is being able to make the things I dream up myself,
and figuring out how to bring them to life, the imagination just helps
me find things to make.

```

The Pragmatic Programmer Chapter 1:

```markdown
While I can appreciate the beginning of this chapter telling me to be 
accountable for myself, I think they might have put this lecture in the
wrong book. It probably belongs in a school handbook or a self-help
book, and seems superfluous, but maybe someone out ther got something
out of it, but I doubt it.

# Important:
**Entropy is a term from physics that refers to the amount of "disorder" 
in a system. Unfortunately, the laws of thermodynamics guarantee that the
entropy in the universe tends toward a maximum. When disorder increases in 
software, programmers call it "software rot."**

**Know when to stop: Don't spoil a perfectly good program by overembellishment 
and over-refinement. Move on, and let your code stand in its own right for a while.
It may not be perfect. Don't worry: it could never be perfect.**


In conclusion, this book is not at all what I was expecting. I was
expecting something along the lines of "this is how you do this"
and "here is a good program for doing this" but seem to be face-to-face
with a "programmer's self help book," which isn't horrible, I suppose.
I enjoy the real life scenarios to make something 2D seem 3D, and more
relatable in content.
```

The Pragmatic Programmer Chapter 2:

```markdown
Firstly, starting off a chapter with a Star Trek reference will always have my 
attention, so this must be a good one.

One of the more interesting subjects in this chapter is the idea of programmers 
constantly "cleaning" code, and bug fixes being a constant task. I don't
have much experience with debugging except those occasional updates I get
on the apps on my phone. These updates, I know, are worked on between each 
update, but it does make me wonder: at what point does an update become so 
necessary that the developers push it to their (sometimes) millions of users?
This answer may vary from person to person, but if the work is never done in
debugging and updating, when do they decide to take a break and send out what
they've accomplished? It's like counting to infinity: why can't I wrap my brain
around the fact that it cannot end.

This whole chapter has been mostly about clean code: documentation, lack of 
repeats, traceability, and reversibility. These things should be engraved in 
my brain by now, but the examples were immensely helpful in showing real-world
reasons to justify why I should do it, I always have, but I'm glad to have a real reason,
and not just a teacher telling me that I need to do it just because I do.

Prototyping describes my programming experience really well:
"Prototyping is a learning experience. Its value lies not in the code produced, 
but in the lessons learned."


**Fun Class Note:**
Software Development Cycle:
1. Plan
2. Design
3. Build
4. Test
5. Deliver
6. Maintain
7. Retire
```
The Pragmatic Programmer Chapter 3:
```markdown
Things I absorbed:
1. Plain Text is good, it will outlive me
2. Code generators are code that generates other code (which isn't a definition, at all).
3. Debugging is hard for really arrogant people, and probably me.
4. Use source code control or die, basically.

I am not entirely in love with this book mainly because I have yet to even
attempt most of these things, and I am not understanding them by reading
"what not to do." I know these are mostly just suggestions on how to "act"
while programming, but they're preaching to a brick wall, because I do not/
have not done most of these things. 

Frequently, the book talks about reversibility and how important it is,
but lacks information on how to literally accomplish that. It's like if the
bible had just been like "BE A GOOD PERSON" and not had a list of things not 
to do (aka the 10 Commandments)(No I'm not religious but this is the simplest anology
I could think of).

The one section that actually did make some sense was the suggestion to become 
extremely proficient in one editor, like Intellij. Every day I try to find more
shortcuts in the application, making code more simple and quicker to accomplish.
I'm still not very proficient in the program, but the more I use it the better
I get.
```

12 Factor 
```markdown
1.
When the site began to talk about "Codebase" I was a tad confused
as I am in most things in computer science, as it is all very abstract. 
Fortunately, the diagrams helped make some more sense of the subject.
*A codebase is any single repo, or any set of repos who share a root commit*
*A deploy is a running instance of the app.*
*A distributed system is multiple codebases*
Though these notes may be helpful, it does seem a little overkill to 
have so many technicalities in what to call something, but I guess I 
do not know enough to comment on the subject.

2.
*A twelve-factor app never relies on implicit existence of system-wide packages.*
I cannot lie, this one seems like a someone might be rambling on about why
Twelve-factor apps are better than everything else. It almost seems cocky 
as they diss system-wide packages.

3.
An app’s config is everything that is likely to vary between deploys, which includes:
1. Resource handles to the database, Memcached, and other backing services
2. Credentials to external services such as Amazon S3 or Twitter
3. Per-deploy values such as the canonical hostname for the deploy

"Apps sometimes store config as constants in the code. This is a violation of twelve-factor,
which requires strict separation of config from code."
Uh oh, someone's getting all high and mighty again.

4.
*A backing service is any service the app consumes over the network as part of its normal operation.*
*The code for a twelve-factor app makes no distinction between local and third party services.*
*Each distinct backing service is a resource*

5.
*The build stage is a transform which converts a code repo into an executable bundle known as a build.*
Would you look at that, I've done this one!
*The release stage takes the build produced by the build stage and combines it with 
the deploy’s current config.*
*The run stage (also known as “runtime”) runs the app in the execution environment, 
by launching some set of the app’s processes against a selected release.*
*The twelve-factor app uses strict separation between the build, release, and run stages.*

6.
*Twelve-factor processes are stateless and share-nothing.*
AKA everything needs to be stored in a database heck yes!
Running from the command line, alright!

7.
*The twelve-factor app is completely self-contained and does not rely on runtime
injection of a webserver into the execution environment to create a web-facing service.*
I feel like I'm being sold a fancy purse or a subscription to something the way they 
talk about how "advanced" and "exclusive" this process is.
*exports HTTP as a service by binding to a port*
Yay I get this, port numbers and stuff!

8.
...processing? This one had a lot of words I did not know, and using the Google did not help.

9.
*The twelve-factor app’s processes are disposable, meaning they can be started or stopped at a moment’s notice.*
Processes minimize startup time.
Processes should "shut down gracefully" *cue eye roll*

10.
*The twelve-factor app is designed for continuous deployment by keeping the gap
between development and production small.*
The table here actually makes some sense, and so do the "job descriptions"
attached to it.

11.
Logs.
Heck yeah. I know this one already.

12.
Admin processes, is this like user functionality?

I was not the biggest fan of this reading (which isn't surprising) because it, like
the others, got on quite a high horse and didn't come down. Some of the pages had
good information, but I felt like I was being shamed for not doing this before.
```

Mythical Man Month
```markdown
"All programmers are optimists" is an excellent way to start a paragraph that accurately
describes all my group programming experience: we always think it will all be fine,
and it rarely ever is. 
Creative activity: the idea, the implementation, and the interaction.
Bad ideas and "holes" become visible during implementation, and inadequacies are exposed.
*Cost does indeed vary as the product of the number of men and the number of months.
Progress does not*
Basically the man month only works in a world where communism also works.
A software task is set up as 1/3 planning, 1/6 coding, 1/4 component test, 1/4 system test.

*Adding manpower to a late software project only makes it later*

Well, I actually liked this reading for once (yay!) as it uses math and human behavior
to disprove this magical idea around productivity and adding people, which I have noticed,
really desn't work. So it is nice to see it disproved.
```
The Pragmatic Programmer Chapter 4
```markdown
Here is what I absorbed from this chapter:

1. Don't trust anyone else's code
2. Don't trust your own code
3. Don't trust anyone, while we're at it
4. Your software will never be perfect!
5. Use exceptions
6. CRASH STUFF AWW YEAH
7. Be pragmatic

Basically, trust no one and also you'll never ever ever be perfect. I mean not even your
"Hello World" will be perfect so don't try, ok?? I mean, not really, but it felt like
that. Also, think about all the things that could go wrong, and do them. Then fix it.

Oh yeah, and use "finally" in Java if you can. It is your friend.

One more thing, finish what you started, and if you can't finish it completely, 
finish what you can.
```
The Pragmatic Programmer Chapter 5
```markdown
Code must be flexible, just like we must be flexible. This means documentation, good style, and good
variable names as well as good testing.

Decoupling, yay! But first, coupling. Coupling is a term that describes the relationship 
between two entities in a software system (usually classes). When a class uses another class, or 
communicates with it, it's said to 'depend' on that other class, and so these classes are 'coupled'.
At least one of them 'knows' about the other. The idea is that we should try to keep the coupling
between classes in our systems as 'loose' as possible: hence 'loose coupling' or sometimes 'decoupling'.

Metaprogramming: refers to a variety of ways a program has knowledge of itself or can manipulate itself.
Bascially, it's code that can write itself. So use it.

Temporal coupling: a common design problem that occurs in API design which occurs when there's an
implicit relationship between two, or more, members of a class requiring clients to invoke
one member before the other. This tightly couples the members in the temporal dimension.
