# Introduction

## Teaching computational thinking and practice

- What is the role of computational training in our various fields?
- How can we scale training to meet demand?
- What technologies, languages, principles, and practices should we teach?
- What is the right balance between conceptual learning and hands-on training
  and practice?
- More generally, how should we train the next generation of scientists,
  statisticians, and engineers in computational methods and practices?

## Teaching computational thinking and practice

After this introduction, we have

- Teaching with Version Control (Randall J. LeVeque)
- Teaching data science from a computer science perspective: Experience from a first MOOC (Bill Howe)
- Teaching Computing to Engineers (Lorena A. Barba)

\vspace{5mm}
For abstracts and slides, please see:
\url{http://www.jarrodmillman.com/siam2015.html}

## Teaching statistical computing to undergraduates

- Context, motivation, and perspective
    - Historical background
    - Personal experience
- Issues, challenges, and questions 

\vspace{10mm}

For historical background, see \cite{speed2013brief}

# History

## Jerzy Neyman (1894--1981)

\begin{columns}[onlytextwidth]
    \begin{column}{0.5\textwidth}
      \centering
      \includegraphics[width=.8\textwidth]{fig/Neyman_3.png}
    \end{column}
    \begin{column}{0.5\textwidth}
      1933 Neyman-Pearson lemma\\
      1937 confidence interval\\
      1938 Statistics Laboratory\\
      1955 Department founded\\
    \end{column}
\end{columns}

## Evelyn Fix (1904--1965)

\begin{columns}[onlytextwidth]
    \begin{column}{0.5\textwidth}
      \centering
      \includegraphics[width=.8\textwidth]{fig/fix_evelyn2.png}
    \end{column}
    \begin{column}{0.5\textwidth}
      1942 led team of students and faculty wives
       involving war effort \\
       {\centering
      \includegraphics[width=.6\textwidth]{fig/563px-Marchant_SilentSpeed-8D.png}}
    \end{column}
\end{columns}

## David Freedman (1938--2008)

\begin{columns}[onlytextwidth]
    \begin{column}{0.5\textwidth}
      \centering
      \includegraphics[width=.8\textwidth]{fig/freedman.png}
    \end{column}
    \begin{column}{0.5\textwidth}
      Department's first computer
    \end{column}
\end{columns}


## Leo Breiman (1928--2005)

\begin{columns}[onlytextwidth]
    \begin{column}{0.5\textwidth}
      \centering
      \includegraphics[width=.8\textwidth]{fig/Leo_Breiman.png}
    \end{column}
    \begin{column}{0.5\textwidth}
      1982 first VAX (11/750)\\
      1986 statistical computing facility
    \end{column}
\end{columns}

## Statistical teaching software and online materials

- \textcolor{blue}{1980's} Berkeley Interactive Statistical System (BLss)
- \textcolor{blue}{1997-present} SticiGui
- \textcolor{blue}{late 1990's-present} R
- \textcolor{blue}{2010-present} Python

\vspace{10mm}
R is primary language for research and training

## What is offered?

Classes

- Concepts in Computing with Data (133)
- Introduction to Statistical Computing (243)
- Reproducible and Collaborative Statistical Data Science (159/259)

Bootcamps

- R, Python, Software carpentry, etc.

Groups

- BIDS, DLab, BITSS, Social computing, Hacker within, Py4science, etc.

Other departments

- EECS, Biostatistics, Information science, etc.



## Stat 133 --- Concepts in Computing with Data

\begin{figure}[t]
\centering
\includegraphics[height=.8\textheight]{fig/stats.pdf}
\end{figure}

## Stat 133 --- Concepts in Computing with Data

\begin{figure}[t]
\centering
\includegraphics[width=\textwidth]{fig/syllabus.png}
\end{figure}

\vspace{5mm}
\begin{flushright}                           
From \cite{nolan2010computing}
\end{flushright}                           
---

\begin{figure}[t]
\centering
\includegraphics[width=\textwidth]{fig/cruelty.png}
\end{figure}

\vspace{5mm}
\begin{flushright}
See \cite{dijkstra1988cruelty}
\end{flushright}

## Routine practice

- **Version control with Git**
- Process automation
- **Testing**
- Readability
- Infrastructure

\vspace{5mm}
\begin{flushright}
See \cite{millman2014developing}
\end{flushright}

## Version control with Git

Used for

- homework, labs, quizzes, and exams

Required me to

- teach Git
- provide clear instructions

Required students to

- install necessary software
- work at commandline
- work with text editor

## Workflow

1. Navigate to your stat133 directory (in Bash)
2. Run the `git pull` command (in Bash)
3. Make changes to the files (in your text editor)
4. Save the changes you made (in your text editor)
5. Run the `git add <filename>` command (in Bash)
6. Run the `git commit -m "put some informative message here"` command (in Bash)
7. Run the `git push` command (in Bash)

## Why automate?

- Assign and grade more student work
- Reduce latency in providing feedback
- Spend more time working directly with students  

## Testing R example

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

## Testing Python example

~~~ 
dna_bases = ["A", "C", "G", "T"]

def is_dna(dna):
    """ Check whether input is a DNA string.

    >>> is_dna("ATGATT")
    True
    >>> is_dna("ATGATU")
    False
    >>> is_dna("atgatt")
    False
    """
    return NotImplemented
~~~

## Lessons learned

- Command line interface
- Filesystem and data organization
- Interpeter confusion
- But it works (even though it doesn't run)
- Google and random trial-and-error

# Issues, challenges, and questions 

## Computing in the statistics curricula

\begin{figure}
\centering
\includegraphics[height=.65\textheight]{fig/venn.png}
\end{figure}

From \cite{nolan2010computing}

## Data Science in the Statistics Curricula

\begin{figure}
\centering
\includegraphics[height=.65\textheight]{fig/thinkingwithdata.png}
\end{figure}

\begin{flushright}
From \cite{hardin2014data}
\end{flushright}

## Trade-offs

- Easy vs. simple
- Getting stuff done vs. getting stuff right
- Doing what you know vs. knowing what to do

## Questions

- What is the role of computational training in our various fields?
- How can we scale training to meet demand?
- What technologies, languages, principles, and practices should we teach?
- What is the right balance between conceptual learning and hands-on training
  and practice?
- More generally, how should we train the next generation of scientists,
  statisticians, and engineers in computational methods and practices?

## References

\bibliographystyle{apacite}
\bibliography{slides}

----

\begin{center} \LARGE{Questions and discussion} \end{center}
