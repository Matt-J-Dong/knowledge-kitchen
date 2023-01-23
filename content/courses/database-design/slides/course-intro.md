---
title: Course Intro
layout: presentation
categories: [course-notes]
---

class: center, middle

# Course Intro

Database Design

---

# Agenda

1. [Welcome](#welcome)
1. [Who you are](#you)
1. [Topics](#topics)
1. [Structure](#structure)
1. [Software](#software)
1. [What Others Say](#evaluations)
1. [Conclusions](#conclusions)

---

name: welcome

# Welcome

---

template: welcome

## Course description

Introduces principles and applications of databases.

--

We survey a variety of common database systems, starting with _plain text data formats_ and _spreadsheets_, and moving into _relational databases_, _document-oriented databases_, with a light touch of more advanced topics like _application programming interfaces (APIs)_ and _blockchains_ (i.e. cryptocurrencies)

--

Students explore principles of database design and apply those principles to computer systems in general and in their respective fields of interest.

---

template: welcome

## What is a database anyway?

A database is any system or tool used for storing data.

--

- usually stores _structured_ data, although _unstructured_ data sets certainly do exist

--

- usually makes it _fast_ to find data you are looking for...

--

- ... especially data that meet _criteria_ you indicate

--

- usually easily-integrated into computer programs

---

template: welcome

## Conventions

While there might be, in theory, many different kinds of database systems, in practice only a few kinds dominate in today's workplace.

--

We will explore a few representatives of the most popular kinds.

---

name: you

# Who you are

---

template: you

## Profile

Who are you, really?

--

- trying to get through college

--

- doing what your parents and advisors tell you to do

--

- interested in programming

--

- interested in data analysis and statistics

--

- hoping to find a decent-paying job

--

- just having fun

--

- here for some other reason.... it doesn't matter!

--

**Welcome!**

---

template: you

## What you know

--

- some computer programming

--

- how to save a file to your hard drive

--

- how to find a file that you have saved to your hard drive

--

- what a file extension is

--

- the difference between uppercase and lowercase letters

---

name: topics

# Topics

---

template: topics

## Database systems

We will look in some detail at a few database systems:

--

- Text-based data formats (e.g. _CSV_, _JSON_, _XML_)

--

- Spreadsheets (e.g. Microsoft _Excel_, Google _Sheets_, Apple _Numbers_, OpenOffice _Calc_)

--

- *SQL*ite (an example of a _relational database_)

--

- _MongoDB_ (an example of a document-oriented database)

--

- _Pandas_ (a Python module for data analysis)

---

template: topics

## Teasers into other topics

We will take **brief looks** at a few exciting topics that might lead you towards future directions that interest you:

--

- Connecting databases to _web apps_

--

- Application programming interfaces (_APIs_)

--

- _Data visualization_

--

- Blockchain, _bitcoin_, and other cryptocurrencies

---

template: topics

## Skills we will develop

You cannot do contemporary work with data and databases without honing a few skills:

--

- _Python_ programming

--

- _Jupyter Notebooks_

--

- _SQL_ programming

--

- Version control (i.e. `git`)

---

template: topics

## Questions we will answer

There are common questions we will aim to answer:

--

- How do I set up my computer so I can work on data problems effectively?

--

- What are the most common problems that databases are designed to solve?

--

- How do you solve those problems?

--

- What are some of the considerations when choosing one database over another?

--

- How do I set up a database properly in a well-organized fashion?

--

- My internship requires me to know SQL.... what is that?

--

- My friend is making mad money at a start-up using MongoDB... can I learn that?

---

name: structure

# Structure

---

template: structure

## Overview

This course involves each of the following:

--

- Lectures

--

- Readings & watchings

--

- Quizzes

--

- Exercises (mostly individual, some group)

--

- Exams (two)

---

template: structure

## Grading

Grading is broken down as follows:

--

- 15%: Quizzes
- 35%: Assignments
- 25%: Midterm exam
- 25%: Final exam

---

template: structure

## Texts

No single textbook is necessary nor sufficient for this course. A few useful textual resources we will refer to as-needed:

--

- [Python for Everybody: Exploring Data Using Python 3 by Charles Severance](https://www.py4e.com/html3/)
- [Bad Data Handbook by Q. Ethan McCallum](https://bobcat.library.nyu.edu/primo-explore/fulldisplay?docid=nyu_aleph005835927&context=L&vid=NYU&lang=en_US)
- [Using SQLite by Jay A. Kreibich](https://bobcat.library.nyu.edu/primo-explore/fulldisplay?docid=nyu_aleph007031845&context=L&vid=NYU&lang=en_US)
- [Database Design by Adrienne Watt (primary author)](https://opentextbc.ca/dbdesign01/)
- [MongoDB Manual](https://docs.mongodb.com/manual/introduction/)

---

name: software

# Software

---

template: software

## Install these now

You will be required to have access to a computer set up for Python development. Install the following:

--

- [Anaconda](https://www.anaconda.com/products/individual)

--

- Git - [for Mac](https://git-scm.com/downloads) or [Git Bash](https://gitforwindows.org/) (part of Git for Windows)

--

- an account set up on [GitHub.com](https://github.com)

--

- [Visual Studio Code](https://code.visualstudio.com/)

--

- [Python extension for Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=ms-python.python)

--

- a file transfer program, such as [Cyberduck](https://cyberduck.io/)

---

template: software

## Using Bash on Windows

WINDOWS USERS - you should use Git Bash or Windows Subsystem for Linux (WSL) rather than Windows' default Powershell or other command line shell program. To set Git Bash or WSL as the default terminal shell within Visual Studio Code, you can try to follow the instructions in [the second answer here](https://stackoverflow.com/questions/42606837/how-do-i-use-bash-on-windows-from-the-visual-studio-code-integrated-terminal) by **Mahade Walid** and edited by **FruityOatyBar** (ignore the first answe, which is outdated).

---

name: evaluations

# What Others Say

--

## The Good

A sample of comments left by former students:

--

> Overall, I thought this course did a phenomenal job of introducing me to a variety of new skills, concepts, and techniques with which I had no prior experience.

--

> Assignments were definitely time–consuming, but learned a lot about a lot of different databases which I know will be useful down the road.

--

> Lectures were great—Prof. Bloomberg has a quiet but palpable confidence and delivered the material effectively. He's open to questions and discussion and his graders give relatively timely feedback. Assignments were also helpful in learning the content.

--

> Really nicely structured course. Professor Bloomberg definitely knows his stuff. Good balance between new content and interesting exercises to reinforce the material.

---

template: evaluations

## The Bad

A sample of comments left by former students:

--

> I personally wasn't a huge fan of the quizzes, even though I did well on all of them. I thought they often had unclear/vague questions and weren't the best way to reinforce the material. Given that there needs to be some quiz–like structure in the class, though, I'm not really sure if there's an alternative. So maybe clearer and less ambiguous questions on the quizzes would be nice.

--

> I wish it wasn't so monotonous. The information in lecture was all in the slides – there were only a few times that live coding occurred, and even then only for a few minutes.

--

> Speed up a little bit on the powerpoint (knowledge), and slow down a little bit on teaching the practical abilities.

--

> I would add smaller projects in between larger biweekly projects to help enhance material.

---

template: evaluations

## The Ugly

--

> I learned more from the tutors than I did from Amos. Avoid his as a teacher at all costs.

--

> Learned nothing much from the course. Also; the course name is pretty baffling. What I expected was to learn some inner mechanisms of relational databases. However; the actual course was more like getting the feet wet for different tools like MongoDB; web apps; and even Pandas. Some might have enjoyed the course but at least I didn't because I don't think this is something that is supposed to be taught in college.

---

template: evaluations

## Time commitment

![Time commitment](../assets/course-intro/time-commitment.png)

---

template: evaluations

## Openness

![Openness](../assets/course-intro/openness.png)

---

template: evaluations

## Challenge

![Challenge](../assets/course-intro/challenge.png)

---

template: evaluations

## Knowledge increase

![Knowledge increase](../assets/course-intro/knowledge-increase.png)

---

name: conclusions

# Conclusions

--

Thank you. Bye.
