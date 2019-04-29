# jeebox

http://jeebox.org – theo@jeebox.org

Compile using:

    cd </path/to/jeebox-master>
    cmake -BBuild; cd Build; sudo make

# About
Jeebox tries to fulfil the goal of describing everything. Here's an example of Jeebox syntax.

	You can (% describe anything, in: Jeebox)

[See real syntax examples here](http://jeebox.org/stuff/introduction). 

Jeebox is useful for describing:

* Code (like C++ only better)
* Save-files (for just about anything)
* Natural-language (English/Spanish/Russian/etc)
* A faster, tighter alternative to JSON/XML.
* Other things (maths equations, physics equations, invent your own use).

The original goal was to describe the meaning-of-code, as a step towards artificial-intelligence. But Jeebox doesn't have any AI in it, it's just a good data-format!

Jeebox parses data into a tree. Jeebox is extensible (like XML), it has no keywords. This means you can describe anything very easily.

Jeebox has a C-API and a C++ API. It parses UTF-8 only. The parse-speed is around the same as TinyXML2's parse-speed, it's pretty fast! Jeebox tends to be very expressive, meaning documents can be much smaller than XML/JSON. Jeebox is small at 158K compiled.

The C++ interface is quite easy to use (automated memory-management). The model for Jeebox is very simple! Jeebox nodes can be described with two strings only, the `name` and the `type`. Being simple makes Jeebox memory-tight.

Jeebox has many features designed for programmers, compiled from my 20 year experience. For example string support is pretty good, strings can have embedded expressions, unicode and byte escape codes, and more. [Read the website](http://jeebox.org/stuff/introduction) to see what I put into Jeebox.

This is the first release so email any questions to theo@jeebox.org!


# Why use Jeebox?

Well... Jeebox has so many uses, the question might be "why not use Jeebox?" I've built a programming language around Jeebox, so I know it's really easy to use and fun to use. The language is beautiful, and I never feel "restricted", because I can always just use more of the existing Jeebox syntax. If you were writing a programming language, then using Jeebox means you basically don't need to write your own parser.

Being open-sourced on github means that if you were worried about me not adding things you needed, you could add them yourself. So I'm not controlling anyone's future.

Jeebox can also describe human language, like English/Spanish/Hebrew/etc. I think writing a translation program would be a great idea! This would help test and improve Jeebox' use for describing real-world meaning. Only minor improvements would be needed, perhaps none.

Jeebox has incredible potential when it comes to translation, because it captures the grammatical structure of a sentance, it could improve accuracy by 10x-100x. The syntax is light, considering the amount of grammatical structure it describes!
    
Jeebox isn't unchanging, I will modify it slightly over time. But on the whole (I've been using it for 7 years) it's barely changed, just a few additions, almost no changes that break anything. Jeebox is pretty stable and mature!

Jeebox has a lot of potential. It could become "The Unicode of programming languages". (I know that's just an idealistic version of reality! I know reality doesn't work like that.) I did say "potential".


# Notes

For the moment Jeebox is 32-bit only. However the tests work and you can compile projects with it. I am working on a 64-bit version. My 32-bit version made some assumptions that aren't valid in 64-bits. Jeebox is single-threaded only.

The Cpp/JB.cpp file is actually auto-generated by my compiler, `Speedie`. This means any changes to it, will be a little hard to merge back into the main source.

Speedie takes Speedie source-code, and turns it into C. Almost all early compilers did this! Even C++ and Java did this once. Speedie isn't part of the distribution, but it's nice to know that Jeebox is being used for a big real-world project (Speedie is based on Jeebox).

I'll release Speedie at some point in the future anyhow. Releasing Jeebox was a big enough job!
