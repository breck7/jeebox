# jeebox

http://jeebox.org - theo@jeebox.org

Compile:

    cd </path/to/jeebox-master>
    cmake -BBuild; cd Build; sudo make install

# About

Jeebox tries to fulfil the goal of describing everything. Here's an example of Jeebox syntax.

	You can (% describe anything, in: Jeebox)

[See real syntax examples here](http://jeebox.org/stuff/introduction). 

Jeebox is useful for describing:

* Code : Build a programming language using Jeebox, or anything with code-like syntax (databases).
* Save-files : For just about anything.
* Natural-language : English/Spanish/Russian/etc.
* Other things : Like maths! Or freely mix any combination of the above.
* Efficiency : A tighter more expressive alternative to JSON/XML.

(The original goal was to describe the meaning-of-code, as a step towards artificial-intelligence. But Jeebox doesn't have any AI in it, it's just a good data-format!)

Jeebox parses a UTF-8 string into a tree of 'nodes'. Jeebox is simple because each node only needs two strings to describe it, the `name` and the `type`. Jeebox is extensible (no keywords), meaning you can describe **anything** unambiguously. Being simple also makes Jeebox memory-tight.

Jeebox has a C-API and a C++ API (the C++ version is much easier to use).

Jeebox's parse-speed is near that of TinyXML2's, it's pretty fast! Jeebox is highly expressive, meaning that (depending on what you are doing) documents **can be** much smaller than XML/JSON, but never bigger. Jeebox is small at 158K compiled.

Jeebox has many features to make programmers lives easier and better. For example: "Double-quoted" strings can have embedded expressions, unicode and byte escape codes, or use \`backtick\` strings with none of that! [Read the website](http://jeebox.org/stuff/introduction) to see what I put into Jeebox. Also Jeebox **doesn't** have the bug that Javascript / C# / Java has, where a codepoint above `&#xFFFF;` can't be expressed.

Please email questions to theo@jeebox.org if you have any troubles using it! Emailing me **rather than giving up** will help me so much!


# Why use Jeebox?

Well... Jeebox has so many uses, the question might be "why not?"

Using Jeebox means you'll never need to write another parser again, you'll get all the most advanced features built-in. Also, assuming enough languages are expressed in Jeebox, this could reduce code-size because we replace many parsers with Jeebox! You could literally build an entire world where everything is expressed in Jeebox.

I built a programming language `Speedie` around Jeebox, so I know it's really easy to use and fun. `Speedie` is beautiful. I never feel "restricted" or get forced to make a mess (like C++ or many languages did).

Being open-sourced on github means that if you were worried about me not adding things you need, you could add them yourself. I'm not controlling anyone's future.

Jeebox can also describe human language, like English/Spanish/Hebrew/etc. A great idea would be to write a translation program based on jeebox! This would help improve Jeebox's use for real-world meaning. Only minor improvements would be needed, perhaps none.

Jeebox has incredible potential for translation, because it captures the grammatical structure of a sentance, it could improve accuracy by 10x-100x. The syntax is light, considering the amount of structure it describes!
    
Jeebox isn't unchanging, I will modify it slightly over time. But on the whole (been using it for 7 years) it's barely changed, just a few additions, almost no changes that break anything. Jeebox is stable and mature.

Jeebox has a lot of potential. It could become "The Unicode of programming languages". (I know that's just an idealistic version of reality! I know reality doesn't work like that.) I did say "potential".


# Notes

For the moment Jeebox is single-threaded and 32-bit only. I am working on making it 64-bit clean.

The Cpp/JB.cpp file is actually auto-generated by my compiler, `Speedie`. This means any changes to it, will be a little hard to merge back into the main source.

Speedie takes Speedie source-code, and turns it into C. Almost all early compilers did this! Even C++ and Java did this once. Speedie isn't part of the distribution, but it's nice to know that Jeebox is being used for a big real-world project (Speedie is based on Jeebox).

I'll release Speedie at some point in the future anyhow. Releasing Jeebox was a big enough job!
