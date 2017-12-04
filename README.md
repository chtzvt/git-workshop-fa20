# Grok

Welcome to Grok: a simple, straightforward testing and continuous integration framework for introductory computer programming courses.

Grok makes it simple for students to write, build, and test code, and introduces them to the core concepts of build scripting, automated testing, and continuous integration. Grok is equal parts an educational aid and development tool, as it abstracts or otherwise assists with a number of clerical aspects of academic software development.

Grok helps students gain an understanding of:
- Version control with Git
- Continuous Integration (Via Travis CI)
- Static code analysis
- Makefiles and build scripting
- Automated testing

Grok itself is nothing more than a collection of scripts within a defined directory structure, the goal of this project being to provide just enough syntactic sugar between the tools and the student for them to gain an understanding of (or to [grok](https://www.merriam-webster.com/dictionary/grok), in other words) them.

By lowering the barrier to entry, the hope is that students will have an opportunity to enjoy the benefits of this tooling while gaining a more intimate familiarity with them at their own learning pace.


## Grok's Structure

To provide the above, Grok's core is composed of:
1. A simple directory structure for repositories
2. An easy to use and understand Makefile
3. A build script for mass, automated testing


_Note: While the dependency on Travis CI is optional, its use is highly encouraged. Without Travis, however, many of Grok's other features remain available._

Grok's Makefile contains a set of idiomatic, easily understood rules for building and testing projects.


#### Directory Structure

Grok's directory structure reflects that of many so-called "monorepos" used in introductory computer programming courses. As such, Grok may be easily integrated with any Git repository which includes the build scripts and the following directory structure:

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

Additionally, Grok's scripts and tooling are easily adaptable to repositories which contain only a single project, or projects written in a language other than C.

```
[![Build Status](https://travis-ci.com/<username>/<reponame>.svg?token=<your_token>&branch=master)](https://travis-ci.com/<username>/<reponame>)
```
