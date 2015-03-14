# Minisymposium overview

## MS78: Teaching computational thinking and practice

> - What is the role of computational training in our various fields?
> - How can we scale training to meet demand?
> - What technologies, languages, principles, and practices should we teach?
> - What is the right balance between conceptual learning and hands-on training
  and practice?
> - More generally, how should we train the next generation of scientists,
  statisticians, and engineers in computational methods and practices?

## MS78: Teaching computational thinking and practice

After this, we have

- Teaching with version control (Randall J. LeVeque)
- Teaching computing to engineers (Lorena A. Barba)
- Community discussion (Randall J. LeVeque)

\vspace{10mm}
For abstracts and slides, please see:
\url{http://www.jarrodmillman.com/siam2015.html}

# Context, motivation, and perspective

## What training is offered?

Classes

- Concepts in Computing with Data (133)
- Introduction to Statistical Computing (243/244)
- Reproducible and Collaborative Statistical Data Science (159/259)

. . .

Bootcamps

- R, Python, Software carpentry, etc.

. . .

Groups

- BIDS, DLab, BITSS, Social computing, Hacker within, Py4science, etc.

. . .

Other departments

- EECS, Biostatistics, School of Information, etc.

---

\begin{figure}[t]
\centering
\includegraphics[width=1\textwidth]{fig/homepage.png}
\end{figure}

\url{http://www.jarrodmillman.com/stat133-summer2014}

## What to cover?

\begin{figure}
\centering
\includegraphics[height=.65\textheight]{fig/venn.png}
\end{figure}

Nolan, D., & Lang, D. T. (2010). Computing in the statistics
curricula. The American Statistician, 64(2).

## What did I want to accomplish?

\textbf{Goal:}  write \emph{valid, executable R programs} which I could
run on my computer and behaved as specified

. . .

\vspace{10mm}

\textbf{Problem:}  students \emph{lack context} for why this is important
and their past experience had \emph{poorly prepared} them

---

\begin{figure}[t]
\centering
\includegraphics[width=1\textwidth]{fig/topics1.png}
\end{figure}

## Class setup

- Focus on students solving problems
- Tables and chairs (not stadium seating)
- Everyone works on their own laptop
- Extensive hands-on practice
- Extensive use of Git
- Running casestudy using Duke/Potti cancer trials
 
## The first week

> - Monday: Course overview and motivation
> - Tuesday: BASH, Git, and GitHub
>     - Lab: Install
> - Wednesday: R datastructures
> - Thursday: More Git
>     - Lab: Git
> - Friday: More R
>     - 1st homework assigned

## Working at the command line

- Foreign to most students
- Slow to embrace
- Lectures were short and focused on live demos
- Daily assignments

## Version control using Git and GitHub

Used for

- homework, labs, quizzes, and exams

. . .

Required me to

- teach Git
- provide clear instructions

. . .

Required students to

- install necessary software
- work at commandline
- work with text editor

## Basics of R programming

Focused on

- Datastructures (vectors, matrices, lists, dataframes)
- Vectorized operations and the `apply` family
- Using and writing functions
- Exploratory data analysis (summary statistics, boxplots, PCA)

. . .

Introduced

- Simulation and random number generation
- Hypothesis testing
- Clustering
- Regression 

## Simplified example assignment

~~~
to_celcius <- function(temp) {
    # take a vector of Farenheit temperatures
    # return a Celcius vector
}

tryCatch(
    checkEquals(to_celcius(c(32, 100, 210)),
                c(0, 340/9, 890/9)),
    error = function(err) errmsg(err)
)
~~~

## Automating grading

- Students submit work via Git
- Pull from each repo
- Source the submitted R file
- Test variables and functions
- Push scores and logfiles to each repo

## Why automate?

I do not trust myself to visually confirm the correctness of my own
code.  Why should I trust a myself or a TA to evaluate student code?

\vspace{5mm}
. . .

Moreover, automating the grading enabled me to:

- Assign and grade more student work
- Reduce latency in providing feedback
- Spend more time working directly with students  

## How did I automate?

- Wrote some Python code
- Used RPy to work with R files
- Test code correctness (did not use automated unit testing framework)
- Allow resubmissions for first several assignments
- Allow students to petition for a regrade (then regraded everyone)

\vspace{10mm}

\url{https://github.com/jarrodmillman/gradebook}

## Code quality vs. quantity

- Program correctness baseline
- Structured solutions
- Code reviews
- Office hours

# Issues, challenges, and questions

## Lessons learned

- Filesystem and data organization
- Command line interface
- Interpeter confusion
- But it works (even though it doesn't run)
- Google and random trial-and-error

## What would I improve

- Start with many mini-assignments
- More focus on code review
- More emphasis on group projects to increase amount of Git 
- More practice fixing broken or poorly written code
- More emphasis on concepts with short answer quizzes

## Stat 133 --- Concepts in Computing with Data

\begin{figure}[t]
\centering
\includegraphics[height=.8\textheight]{fig/stats.pdf}
\end{figure}

## Statistics 159/259 --- Reproducible and Collaborative Statistical Data Science

A project-based introduction to statistical data analysis.
Through case studies, computer laboratories, and a term project,
students will learn practical techniques and tools
for producing statistically sound and appropriate, reproducible, and verifiable
computational answers to scientific questions.
Course emphasizes version control, testing, process automation,
code review, and collaborative programming.
Software tools may include Bash, Git, Python, and LaTeX.

----

\begin{center} \LARGE{Questions and discussion} \end{center}

