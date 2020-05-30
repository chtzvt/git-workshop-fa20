# Grok

[![Build Status](https://jenkins.nhq/buildStatus/icon?job=Charlton%2FGrok%2Fmaster)](https://jenkins.nhq/job/Charlton/job/Grok/job/master/)

Welcome to Grok: a simple, straightforward testing and continuous integration framework for introductory computer programming courses.

Grok makes it easy for students to write, debug, and test code by introducing them to the core concepts of build scripting, automated testing, and continuous integration. Grok is equal parts an educational aid and development tool, as it abstracts or otherwise assists with a number of clerical aspects of academic software development which often frustrate beginners.

Grok helps students gain an understanding of:
- Version control with Git
- Continuous Integration (via Travis CI)
- Static code analysis
- Makefiles and build scripting
- Automated testing

## Philosophy

Grok exists first and foremost as an educational tool, the hope being that a thin layer of syntactic sugar will be enough for beginners to immediately enjoy the benefits of advanced tooling while at the same time gaining a conceptual understanding of it ([grokking](https://www.merriam-webster.com/dictionary/grok), in other words) at their own pace through their use.

Why is this necessary? From a software development standpoint, it's an unfortunate fact that many first-year Computer Science students enter university at a disadvantage. Professors are often laser-focused on theory and syntax, and many provide little guidance to students in regards to useful development tools (and for the few that do, many of those tools are not reflective of modern software development practices). Furthermore, departments often favor less beginner-friendly languages such a C or Java, which can prove difficult enough on their own for newcomers to master.

A concerning number of students are left to their own devices when determining appropriate tools and development workflows. They are not introduced to development practices which would save significant amounts of testing and debugging time, nor are they given exposure to industry-standard tooling that would otherwise prepare them for the workplace. This results in a great deal of frustration for new programmers, who are duped into accepting inefficient, time-consuming, and disorganized workflows, simply because they are unaware of the wide availability of these advanced tools (or even that such tools exist).

As the initial intended audience for this project is students taking part in my university's introductory programming class, the scripts and tools in use are centered around the C language and the development workflow for these courses. However, Grok's concepts, scripts, and tooling are easily adaptable to projects written languages other than C.


## Grok's Structure

Grok itself is nothing more than a collection of scripts within a defined directory structure. As a result, Grok is lightweight, flexible, and straightforward.

More specifically, Grok's core is composed of:
1. A simple directory structure for repositories
2. An easy to use and understand Makefile
3. A build script for mass, automated testing

_Note: While the dependency on Travis CI is optional, its use is highly encouraged. Even without Travis, however, many of Grok's other features remain available._

#### Makefile

Grok's Makefile contains a set of idiomatic, easily understood rules for building and testing projects.


#### Directory Structure

Grok's directory structure reflects that of many so-called "monorepos" used in introductory computer programming courses. As such, Grok may be easily integrated with any Git repository which includes Grok's build scripts and the following directory structure:

```
Top Level Directory
  - build.sh
  - .travis.yml

  Project Subfolder 1
    - src
      - project_main.c
    - makefile

  Project Subfolder 2
    - src
      - project_main.c
    - makefile

  [...]
```



```
[![Build Status](https://travis-ci.com/<username>/<reponame>.svg?token=<your_token>&branch=master)](https://travis-ci.com/<username>/<reponame>)
```
