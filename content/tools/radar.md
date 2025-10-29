+++
title = "Technology Radar"
+++

I'm not a fan of the granularity used by various tech publications; for personal use, I think three categories are plenty:

* **use**: technology I actively rely on and believe is a sound investment
* **trial**: technology about which I'm optimistic enough to experiment for promotion to "use"
* **avoid**: technology that I've either used and discarded, or that I have no plans to trial

This page is extremely opinionated; it represents my _preferences_, not a judgement of where the industry should be going.

## Languages

### Clojure

**avoid**

Clojure is a beautiful language that I just cannot recommend. My biggest complaints are:

* the build tools are either esoteric or too simplistic
* the namespace/import macro should be a felony. I shouldn't need a cheat sheet
* I think lazy evaluation should be opt-in, not the default
* the final nail in the coffin, however, was dynamic typing. I spent too much time chasing incoherent nil references around a call stack that was all to happy to punt them up to the next caller. I appreciate the elegance afforded, but I'm just far more productive with a powerful type system that lets me type errors out of existence at compiletime.

### Elixir

**trial**

I'm under no delusions about how niche Elixir is. However, I'm convinced of two things:

1. that the BEAM presents the best semantics for modern service development (it's what Java's Loom is (rather incompletely) iterating toward, after all)
2. that Phoenix Liveview has incredible ROI for engineers who aren't heavily invested in Javascript

Since I spend most of my time in backend or infrastructure, I'm not particularly interested in heavy Javascript investment. This creates a gap in my tools, where it's a lot of work to create anything involving a web presence or user interface. I think of Elixir as a high-level DSL for creating web systems.


### Java

**avoid**

Java is an acceptible, if uninspiring language. Its biggest flaws are:

* nullability by default
* mutability by default
* extreme verbosity
* unacceptably low-level concurrency

It's possible to write quite reasonable Java, but you're going to find yourself at odds with the default culture of the ecosystem, which is overwhelmingly dominated by Spring Boot.

In all my years writing Scala, I felt continual relief that I simply didn't have to deal with all the minutiae required to write threadsafe, "effective" Java. The idea of returning to all those code review debates and distractions from solving problems fills me with dread. Java is an institution, the JVM is incredible, and it's 2025.

### Python

**avoid**

This is the most successful language that still doesn't know how to put its pants on in the morning. Python is effective at a broad variety of jobs, is the primary game in town for machine learning applications, and yet there still isn't a compelling build tool story (though `uv` is promising!). I think significant whitespace is silly, and I think static types are table stakes.

This is a language that I'd advise others to learn, even though I have no use for it.

### Ruby

**use**

This is a strange one. Ruby is my go-to scripting language at the moment. Were it not for Elixir, I'd also consider Ruby best-in-class for rapid web development. I still think it's a slam dunk choice for the job, even though Elixir embodies more of the characteristics that I look for in a tool.

*If* I were trying to use a fully dynamic language, Ruby has the right balance of expressiveness and ease of use for the way I think about code. It's still the first language I reach for when a bash script exceeds about 2 lines, but I don't know if there's a reason to do much more of it if I'm getting into Elixir.

### Rust

**trial**

Rust is a language with a lot of hype. I've long been skeptical that it's a great fit for the kind of work I do. For the most part, a garbage-collected language offers the right tradeoffs for productivity. However, with Scala's future somewhat in doubt, there's something of an opportunity to try to stretch a little. Rust is probably the only modern language that has any appealing characteristics to me, and it would let me step into domains in which JVM languages aren't necessarily as apt. It's especially interesting to see how much Rust is showing up in data infrastructure solutions.

### Scala

**use**, possibly transition to **avoid**.

Scala is the closest language to what I consider the ideal professional programming language. I expect garbage collection, with succinct syntax, functional constructs, static types, excellent performance, and a concurrency layer more abstracted than that offered by, say, Java.

Scala does all of this. Unfortunately, Scala can't get out of its own way. Professionally, I've spent far more time than is acceptible dealing with `sbt`'s intricacies and breaking changes. Scala 3 was a lesson in how not to release a new version of a language, and there is no justification for creating a whitespace-significant language in 2025. Between the astounding loss in momentum and the high ratio of drama/scandal for such a small community, it's difficult to continue to recommend Scala, even though *there are no mainstream languages to take its place.*

