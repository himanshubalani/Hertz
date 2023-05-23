---
title: "Teaching a kid how machines learn"
datePublished: Wed Aug 17 2022 16:21:35 GMT+0000 (Coordinated Universal Time)
cuid: cl6xtmrx1076jvknvg9z3c7w3
slug: teaching-a-kid-how-machines-learn
cover: https://cdn.hashnode.com/res/hashnode/image/unsplash/5VJLeQ-TrKs/upload/v1660636209935/A6lHCZtsQV.jpeg
tags: introduction, neural-networks, deep-learning, blogswithcc

---

## Introduction
On the internet,  algorithms are all around you. You are reading this blog (among other things) because an algorithm tricked you into clicking, and the algorithm noticed. When you open Twitter, an algorithm (say Arc) decides what you see. When you find photos, the Arc algorithm does the finding, maybe even making you a mini movie (looking at your Google Photos 👀 )
When you buy something, the algorithm sets a price and the Arc algorithm at your bank sees if it's not a fraud. With this in mind, you might want to know how these little algorithmic robots that shape our world work.

## How were the first bots made
Humans built algorithmic bots by giving them instructions that humans could explain.

"If this, then that."

![1_nx9uh_BoKsKjklzfKePeSA.gif](https://cdn.hashnode.com/res/hashnode/image/upload/v1660576321006/PR3NU_dbF.gif align="center")
<a href="https://uxdesign.cc/monsieur-b%C3%A9zier-and-his-elegant-curves-52769cca1490"> Source </a>

But many problems are just too big and hard for a human to write simple instructions for. There are a gazillion financial transactions a second, which ones are fraudulent? There are a bazillion videos on YouTube. Which few should the user see as recommendations? Which ones shouldn't be allowed on the site at all?

Algorithmic bots give answers to these questions. They aren't perfect, but much better than what a human could do. But how these bots work exactly no one knows. Not even the humans who build them.

Now companies that use these bots don't want to talk about how they work because the bots are valuable assets, VERY valuable. And how their brains are built is a guarded trade secret.

So let's talk about one of the more unusual but understandable ways bots CAN be "built" without understanding how their brains work.

## Example

Say you want a bot that can recognize what is in a picture. Is it a dog, or is it a cat?

It's easy for humans (even children), but it's impossible to just tell a bot in bot language how to do it because we just know that's a Dog. We can say in words what makes them different, but bots don't understand words.

So to get a bot that can do this sorting, you don't build it yourself. You build a bot that builds bots, and a bot that teaches bots. These bots' brains are simpler, something a smart human programmer can make. The builder bot builds bots, though it's not very good at it. At first, it connects the wires and modules (if, then, else) in the bot's brains almost at random. Of course, a teacher bot can't tell a dog from a cat either; if the human could build a teacher bot to do that, well, then, problem solved.

Instead, the human gives the teacher bot a bunch of "Dog" photos, "Cat" photos, and an answer key to which photo is what. Teacher bots can't teach, but teacher bots can test student bots.
The student bots are bad at what they do in the beginning. Very, VERY, bad. And it's not their fault they were built that way.

Grades in hand, the student bots that did best are put to one side, the others deleted. Builder but still isn't good at building bots, but now it takes that left and makes copies with changes in new combinations. Back to the test they go.

Teacher bot tests again, and builder bot builds again and again, and again. Now a builder that builds at random, a teacher that doesn't teach, just tests, and students who can't learn, in theory, shouldn't work, but in practice, it does.

Partly because in every iteration, the builder bot keeps the best and discards the rest, and partly because the teacher bot isn't testing a dozen students, but thousands of students. The test isn't ten questions, but a million questions. And how many times does the test, build, test loop repeat? As many as necessary.

At first, students that survive are just lucky, but by combining enough lucky bots, keeping only what works, and randomly messing around with new copies of that eventually a student bot emerges that isn't lucky, that can perhaps barely tell Dogs from Cats.

As this bot is copied and changed, the average test score slowly rises, and thus the grade needed to survive the next round gets higher and higher. Keep this up and eventually, a student bot will emerge, who can tell a dog from a cat in a photo it's never seen before pretty well.

But how the student bot does this, neither the teacher bot, the builder bot, nor the human overseer can understand. Nor the student bot itself. After keeping so many useful random changes, the wiring in its head is incredibly complicated, and while an individual line of code may be understood, and clusters of code's general purpose vaguely grasped, the whole code is beyond understanding


<iframe src="https://gifer.com/embed/7Vp" width=480 height=360 frameBorder="0" allowFullScreen></iframe><p><a href="https://gifer.com">via GIFER</a></p>

So this is how a bot that's good at one thing is made
Thanks for reading my first blog.