# How To Learn Hacking

from: http://www.catb.org/esr/faqs/hacking-howto.html

Eric Steven Raymond
Thyrsus Enterprises

    <esr@thyrsus.com>
    
Copyright © 2014 Eric S. Raymond

Revision History
Revision 1.2	2014-11-30	esr
New section on being original.
Revision 1.1	2014-11-23	esr
Incorporated feedback from G+, including good suggestions by Peter da Silva and John D. Bell.
Revision 1.0	2014-11-21	esr
Initial version.
Table of Contents
[TOC]


## What Is Hacking?

The “hacking” we'll be talking about in this document is exploratory programming in an open-source environment. If you think “hacking” has anything to do with computer crime or security breaking and came here to learn that, you can go away now. There's nothing for you here.

Translations of this document are available in: Hungarian

Hacking is primarily[1] a style of programming, and following the recommendations in this document can be an effective way to acquire general-purpose programming skills. This path is not guaranteed to work for everybody; it appears to work best for those who start with an above-average talent for programming and a fair degree of mental flexibility. People who successfully learn this style tend to become generalists with skills that are not strongly tied to a particular application domain or language.

Note that one can be doing hacking without being a hacker. “Hacking”, broadly speaking, is a description of a method and style; “hacker” implies that you hack, and are also attached to a particular culture or historical tradition that uses this method. Properly, “hacker” is an honorific bestowed by other hackers.

Hacking doesn't have enough formal apparatus to be a full-fledged methodology in the way the term is used in software engineering, but it does have some characteristics that tend to set it apart from other styles of programming.

Hacking is done on open source. Today, hacking skills are the individual micro-level of what is called “open source development” at the social macro-level. [2] A programmer working in the hacking style expects and readily uses peer review of source code by others to supplement and amplify his or her individual ability.

Hacking is lightweight and exploratory. Rigid procedures and elaborate a-priori specifications have no place in hacking; instead, the tendency is try-it-and-find-out with a rapid release tempo.

Hacking places a high value on modularity and reuse. In the hacking style, you try hard never to write a piece of code that can only be used once. You bias towards making general tools or libraries that can be specialized into what you want by freezing some arguments/variables or supplying a context.

Hacking favors scrap-and-rebuild over patch-and-extend. An essential part of hacking is ruthlessly throwing away code that has become overcomplicated or crufty, no matter how much time you have invested in it.

The hacking style has been closely associated with the technical tradition of the Unix operating system[3]

Recently it has become evident that hacking blends well with the “agile programming” style. Agile techniques such as pair programming and feature stories adapt readily to hacking and vice-versa. In part this is because the early thought leaders of agile were influenced by the open source community. But there has since been traffic in the other direction as well, with open-source projects increasingly adopting techniques such as test-driven development.

## Stages of Learning How To Hack

Learning to compose music has three stages. First, you have to learn the basic mechanical technique of an instrument — fingering and how to play scales. Then you have to train your ear to understand musical patterns. Finally, you must learn how to recombine musical patterns into original creations. Hacking is similar.

The hacking equivalent of fingering is learning the capabilities of programming languages, and the mechanics of using tools like editors, interpreters, and compilers. (If you don't understand these terms, see The Unix and Internet Fundamentals HOWTO.) We won't cover those mechanics here as they vary too much according to what language you're using. Tutorials for all the languages you might want to use are available on the Web; use a search engine.

The equivalent of playing scales is writing small programs, alone. Unfortunately, playing scales (a) doesn't teach you anything about music, and (b) is boring as hell. Similarly, writing toy programs doesn't tend to teach you much about hacking, and (b) will tend to de-motivate you unless the program immediately solves a problem you care about.

Most formal programming instruction gets to playing scales and stops. Thus, it tends to produce coders who are poor at collaborating with each other and have the equivalent of no ear for music — a poor feel for software design and architecture.

## The Incremental-Hacking Cycle

There is a better way to learn. I call it the incremental-hacking cycle.

1. First, pick a program that does something you are interested in. Ideally, it should be a program you use regularly and have opinions about. The next best thing is a program you don't normally use, but that does something you think is interesting. For this learning method to work, you should avoid trying to hack on code that bores you.

The program you choose doesn't have to do anything serious. Many programmers have honed their skills by improving games that they enjoyed. The only drawback to this is that modern games are often quite large and complicated, and may be beyond the grasp of a raw beginner. For this reason, you may want to investigate one of the classic text-oriented games that still survive; nethack is a prime example, and there are many others.

2. If you don't already know the program, learn how to use it. Read the documentation. Develop a mental model of how it works.

3. Pick a small feature to change or add.

4. Search the code until you find the part you need to modify.

Note: you should specifically not try to read the entire program. You will just exhaust and frustrate yourself if you do that. Instead, use the module structure of the code to zero in on just the part you need to understand. Along the way, you will learn things about how the whole program fits together.

It's a good exercise to add explanatory comments and notes to the code as you figure out things about it. This will help your memory, and will help you organize your thoughts as well.

5. Make, test, debug, and document your change.

Documenting your change is important. If you develop the habit of doing this early, you'll produce much higher-quality work.

6. Send your change as a patch to the program maintainers. See the Software Release Practice HOWTO for tips on how to do this in an effective and polite way.

I originally described this as an optional step; a wise friend pointed out that probably I shouldn't have. Solitary noodling on your instrument is all very well for practice, but music is completed and validated when the creativity in it is heard by other people. Solitary noodling on your computer is similarly good for practice, but hacking is completed when other people use what you wrote. That real-world test is important.

Sometimes (oftener when you are just starting) your patches will be rejected. You need to learn to cope with this. It doesn't mean you're doomed to fail in your quest; usually what it does mean is that you have not read the code carefully enough, or (just as usually) you have missed something important aboout the culture and practices of the developmemt group you are trying to contribute to. These mistakes can be repaired.

7. Now, ask yourself: do I understand this entire program?

If yes, you're done. If no, go back to step 3. This time, pick a different and perhaps slightly more difficult thing to change.

The point of this exercise is to learn how to sneak up on the problem of understanding a program, rather than trying to tackle all of the complexity at once. As you go through this loop several times, you will gradually develop a more complete representation in your mind of the way the whole program fits together. At some point you will reach a threshold where you understand it all — or anyway enough of it for whatever your final purpose is.

## Developing Your Design Sense

To train yourself, start small. If possible, first do the incremental-hacking cycle as an exercise on very small programs or scripts, 10-50 lines. These may be hard to find, as most programs of any use are larger than this. Most programs this small are scripts in shell, Perl, Python, or Tcl; that's a trait to look for when trawling the Web for them.

When you have done the incremental-hacking cycle on several very small programs (or if you are unlucky enough to not find any suitable very small ones), try it on slightly larger programs. Look for codebases in the range of 100-500 lines.

When you master that level, go to the order of magnitude, 1000-5000 lines. By the time you master the 1K-5K level, you will have entered the bottom end of the capability range of what is usually considered a skilled programmer.

At or before the 1K-5K level, you should occasionally begin to notice that you are having itches to change the structure or organization of a program, not just its features. You may find yourself thinking “This code is ugly” and having feelings about making it prettier and cleaner.

When this happens, pay attention. This is your design sense trying to wake up. Don't rush to patch in another feature. Instead, start to explore the program that gives you this itch at a higher level. Now might be a good time to try to read all the code, but don't be too concerned if you can't; most programs are just too big and messy for gulping them down all at once to work. Just try to get a grip on what you need to know to clean things up.

You are now entering the intermediate portion of learning to hack. This involves not merely changing surface-visible features but doing what is called “refactoring” — reorganizing the code internally so that it is cleaner and has better architecture (better hiding of data, narrower interfaces between different parts, more functional separation among modules).

Once your design sense (your equivalent of musical ear) is activated, you'll often find that you start refactoring each program you work on as rapidly as the third or fourth time around the incremental-hacking cycle.

In fact, this is exactly how skilled hackers normally approach learning the code of large programs — by tinkering and refactoring and rewriting until they grok what is going on. You make small changes in order to learn how to make large ones.

If you successfully refactor three or four large systems, you will not just develop strong programming skills, you will be on your way to something much more rare and powerful: becoming a software architect, one who can do original design of large software systems.

This is the only way I know of for fledgling software architects to train their design sense. It may be the only way there is.

## Being original

In my analogy with music, I said that you eventually need to learn how to recombine musical patterns (which you have learned by listening to music and practicing performance) into original compositions. I chose that way of describing creativity carefully, because it applies to software even more than it does to music.

Before you have read and absorbed the lessons of a lot of code, you will probably not have in your head the pattern library you need to be creative on scales larger than very small ones. One purpose of doing the incremental-hacking cycle is to immerse yourself in a lot of code — at increasing complexity scales — under circumstances that provide you with motivation to keep reading.

Eventually you will lead group projects and do entirely original work. Do not feel you have to rush this or force it; if you give your skills time to mature, your first original composition will be better for it. By contributing effectively to existing open-source projects you will learn the skills (including the communications skills) that you need to run your own projects.


[1] It is certainly possible to hack things other than software, and people in the maker culture do it. But the term “hacking” originated among people who tinkered with software and still radiates out from there. Besides, the author is not really qualified to write about learning other kinds.

[2] In former times, people hacked on closed source, when they could, because there was no alternative. Things have changed for the better.

[3] Before 1983 or so the association between hacking and Unix was less strong, but the details of how that changed are now mainly relevant only to historians.