# Don't be a <blank> programmer!
### [fit] or: what I wish I would have known before/during/after University

^ How many of you would consider yourselves as C++ programmers?
  Back-end developers?
  Full-stack developers?

---

# [fit] SYNTAX vs. SEMANTICS

---

## Syntax: The order in which symbols, words, or phrases are combined to form programs.

---

> "You have a syntax error, dumbf**k.""
-- the Urban Dictionary

^ Used in a more familiar context of a compiler and source code, we've probably all encountered something like this.

---

## This means the same thing...

```cpp
#include <iostream>

 int main()
 {
 	std::cout << "Hello, World.";
 }
 ```

---

## ...as this

```javascript
function hello() {
  console.log('Hello, world!');
}

hello();
```

---

## ...and this

```brainfuck
++++++++++[>+++++++>++++++++++>+++>+<<<<-]
>++.>+.+++++++..+++.>++.<<+++++++++++++++.
>.+++.------.--------.>+.>.
```

---

## ...and even this

```bash
Ook. Ook? Ook. Ook. Ook. Ook. Ook. Ook. Ook. Ook. Ook. Ook. Ook. Ook. Ook. Ook.
Ook. Ook. Ook. Ook. Ook! Ook? Ook? Ook. Ook. Ook. Ook. Ook. Ook. Ook. Ook. Ook.
Ook. Ook. Ook. Ook. Ook. Ook. Ook. Ook. Ook. Ook? Ook! Ook! Ook? Ook! Ook? Ook.
Ook! Ook. Ook. Ook? Ook. Ook. Ook. Ook. Ook. Ook. Ook. Ook. Ook. Ook. Ook. Ook.
Ook. Ook. Ook! Ook? Ook? Ook. Ook. Ook. Ook. Ook. Ook. Ook. Ook. Ook. Ook. Ook?
Ook! Ook! Ook? Ook! Ook? Ook. Ook. Ook. Ook! Ook. Ook. Ook. Ook. Ook. Ook. Ook.
Ook. Ook. Ook. Ook. Ook. Ook. Ook. Ook. Ook! Ook. Ook! Ook. Ook. Ook. Ook. Ook.
Ook. Ook. Ook! Ook. Ook. Ook? Ook. Ook? Ook. Ook? Ook. Ook. Ook. Ook. Ook. Ook.
Ook. Ook. Ook. Ook. Ook. Ook. Ook. Ook. Ook. Ook. Ook! Ook? Ook? Ook. Ook. Ook.
Ook. Ook. Ook. Ook. Ook. Ook. Ook. Ook? Ook! Ook! Ook? Ook! Ook? Ook. Ook! Ook.
Ook. Ook? Ook. Ook? Ook. Ook? Ook. Ook. Ook. Ook. Ook. Ook. Ook. Ook. Ook. Ook.
Ook. Ook. Ook. Ook. Ook. Ook. Ook. Ook. Ook. Ook. Ook! Ook? Ook? Ook. Ook. Ook.
Ook. Ook. Ook. Ook. Ook. Ook. Ook. Ook. Ook. Ook. Ook. Ook. Ook. Ook. Ook. Ook.
Ook. Ook? Ook! Ook! Ook? Ook! Ook? Ook. Ook! Ook! Ook! Ook! Ook! Ook! Ook! Ook.
Ook? Ook. Ook? Ook. Ook? Ook. Ook? Ook. Ook! Ook. Ook. Ook. Ook. Ook. Ook. Ook.
Ook! Ook. Ook! Ook! Ook! Ook! Ook! Ook! Ook! Ook! Ook! Ook! Ook! Ook! Ook! Ook.
Ook! Ook! Ook! Ook! Ook! Ook! Ook! Ook! Ook! Ook! Ook! Ook! Ook! Ook! Ook! Ook!
Ook! Ook. Ook. Ook? Ook. Ook? Ook. Ook. Ook! Ook.
```

^ Yes, someone invented a programming language that even orangoutangs can use.

---

## "Hi, I'm Chris, and I'm a _JavaScript_ programmer."

^ Quick digression: why doesn't it sound weird when we say this?

---

## "Hi, I'm Chris, and I'm a _Crayola_ artist."

[filename.jpg]

^ But I'd obviously never want to call myself this!

---

## Quantitative != Qualitative

^ It doesn't matter whether we're talking about programming languages, art,
  poetry, music, or any other creative medium: there is a distinction between
  how something looks, and how something _feels_ and _works_.

---

> "The power to understand and predict the quantities of the world should not be restricted to those with a freakish knack for manipulating abstract symbols."
-- Bret Victor

^ One of my idols, Bret Victor said in an essay called "Kill Math", that "the power
  to understand and predict the quantities of the world should not be restricted to those
  with a freakish knack for manipulating abstract symbols". Bret was talking about Math
  and more specifically, mathematical notation which I'm sure many of us hated learning
  about in school. The lessons of math are undoubtedly very profound, and if expressed
  carefully, they can even be intuitive, but a lot of us just can't get past
  manipulating _symbols_.

---

## Semantics: the branch of linguistics and logic concerned with meaning.

^ More specifically, whenever I say "semantics", I really mean conceptual semantics,
  which is the study of the cognitive structure of meaning, not just how symbols are related to each other.

---

> "The purpose of internet forums is to argue over _semantics_."
-- the Urban Dictionary

---

## If I wrote this...

```cpp
#include <iostream>>

 int main() {
 	std:cout "Hello, World.'
}
```

^ Let's go back to our C++ example for a minute; I have here a program that I likely wrote in my first programming class.
  If I shoved this into gcc and tried to compile it, it would get very angry with me.

---

## I'd get this...

 ```zsh
 gcc -o test test.cc
test.cc:1:20: warning: extra tokens at end of #include directive
      [-Wextra-tokens]
#include <iostream>>
                   ^
                   //
test.cc:4:11: warning: missing terminating '"' character [-Winvalid-pp-token]
 std:cout "Hello, World.'
          ^
test.cc:4:6: error: use of undeclared identifier 'cout'; did you mean
      'std::cout'?
 std:cout "Hello, World.'
     ^~~~
     std::cout
/Applications/Xcode.app/Contents/Developer/Toolchains/XcodeDefault.xctoolchain/usr/bin/../include/c++/v1/iostream:50:33: note:
      'std::cout' declared here
extern _LIBCPP_FUNC_VIS ostream cout;
                                ^
test.cc:4:10: error: expected ';' after expression
 std:cout "Hello, World.'
         ^
         ;
test.cc:4:11: error: expected expression
 std:cout "Hello, World.'
          ^
test.cc:4:26: error: expected '}'
 std:cout "Hello, World.'
                         ^
test.cc:4:6: warning: expression result unused [-Wunused-value]
 std:cout "Hello, World.'
     ^~~~
3 warnings and 4 errors generated.
```

^ What I wrote was obviously correct in the semantic sense: in another language, it might even be
  syntactically valid, but gcc does not understand that made-up language I just invented.

---

## Should I learn _X_[^*]?

[^*]: Insert name of thing (library/language/framework) you read about on Hacker News here

---

## [fit] YES

^ Learning new syntax is helpful and can open your eyes to new possibilities in programming.

---

## Should I learn _X_[^*] because _Y_[^**]?

[^*]: Insert name of syntactical thing (library/language/framework) you want to learn here

[^**]: One of "Just so I can get a job", "Chris said so", or "All the cool developers are doing it"

^ Because Chris is a programming Messiah and you should accept his wisdom without question?

---

## [fit] NO

---

## What _should_ I learn?

^ The best piece of advice I can give to you is this: don't _just_ learn syntax. Learn semantics too.
  While syntax is important, it's really easy to look up (I forget these all the time, so I have to).
  It's not so easy to look up abstract concepts, and even worse, it's almost impossible to apply them
  without ever having used them before.

---

> Design Patterns:
> "The atoms of software engineering"
-- Zen Programmer Crabl

^ These are abstract elements of software architecture: singletons, factories, function composition.
  Architectures like Flux, MVC, the Observer pattern, N-tier architecture, etc.
  These nuggets of abstraction can be implemented in any language, regardless of syntax, but you need to
  recognize when you need them, when you don't, and how to apply them. Learn how to refactor these things,
  how to compose them, and make something awesome.

---

# Programming Paradigms

^ Things like functional vs. imperative vs. declarative programming. Again, you could argue with your
  friends at parties for HOURS about which is the correct one to use. The answer is: they're all valid.
  Use the one that's best suited to the task, and easiest to reason about. Context is everything.

---

# Testing

^ If I had known about unit testing, and integration testing, I would have aced every one of my intro CS
  classes. Instead, I spent HOURS running through all my programs manually trying every possible
  permutation and combination of inputs to make sure I didn't have bugs (I always had bugs). At work,
  unit testing has saved my ass countless times, so look into it if you haven't already.

---

# Teamwork

^ That brings me to my final point of what you should learn: effective teamwork. Programming is a
  collaborative sport, and it's important to realize that programs are meant to be read by HUMANS
  over COMPUTERS. A computer can read your program really fast, and (for the most part), if your program is
  syntactically valid, it doesn't care if you use sporadic indentation, single-letter variable names, or other
  things that will make your co-workers want to stab you. As design-patter God, Martin Fowler puts it:

---

> "Any fool can write code that a computer can understand. Good programmers write code that humans can understand."
-- Martin Fowler, God of Design Patterns

---

## Don't let your toolset define who you are as a programmer!

^ As soon as you start calling yourself a .Net developer, or an AngularJS
  developer, you box yourself in. You limit your possibilities. You fall into
  the trap of using your "golden hammer" for everything, and sooner or later
  you're going to end up with a bruised thumb. Don't lock yourself in, and
  embrace yourself as the artist you really are.

---

# [fit] Hi, I'm Chris. I'm a _programmer_.

---
