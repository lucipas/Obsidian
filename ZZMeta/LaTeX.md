
```latex
$\ce{CO2 + C -> 2 CO}$
$\ce{Hg^2+ ->[I-] HgI2 ->[I-] [Hg^{II}I4]^2-}$
$C_p[\ce{H2O(l)}] = \pu{75.3 J // mol K}$
$\ce{H2O}$
$\ce{H+}$
$\ce{Y^{99+}}$
$\ce{2 H2O}$
$\ce{^{227}_{90}Th+}$
$\ce{A -> B}$
$\ce{A <- B}$
$\ce{A <=> B}$
$\ce{A ->[H2
```
$\ce{CO2 + C -> 2 CO}$
$\ce{Hg^2+ ->[I-] HgI2 ->[I-] [Hg^{II}I4]^2-}$
$C_p[\ce{H2O(l)}] = \pu{75.3 J // mol K}$
$\ce{H2O}$
$\ce{H+}$
$\ce{Y^{99+}}$
$\ce{2 H2O}$
$\ce{^{227}_{90}Th+}$
$\ce{A -> B}$
$\ce{A <- B}$
$\ce{A <=> B}$
$\ce{A ->[H2O] B}$


```latex
% Introductory paragraph
% This LaTeX cheat sheet is designed to help beginners get started with using LaTeX, a powerful typesetting system commonly used for academic and scientific documents. LaTeX allows you to create well-structured documents with ease, providing precise control over formatting and layout. In this cheat sheet, we cover a range of essential commands and packages, with explanations and examples to help you understand their usage. 

% \documentclass[OPTIONS]{CLASS}: Defines the overall layout of the document. Common classes are article, report, book.
\documentclass{article}

% \usepackage[OPTIONS]{PACKAGE}: Includes additional packages to extend LaTeX functionalities. Graphicx for example inserts functionalities for images. A good analogy for packages are libraries in other languages
\usepackage{graphicx}

% \title{TITLE}: Defines the document title.
\title{LaTeX Cheat Sheet}
% \author{AUTHOR}: Defines the document author.
\author{Andrew Montalbano}
% \date{DATE}: Defines the document date.
\date{March 2024}
% Required for hyperlinks
\usepackage{hyperref}

% Required for color text
\usepackage{xcolor}

% Configure hyperlink colors
\hypersetup{
    colorlinks=true,
    urlcolor=blue,  % Color for URL links
    citecolor=black, % Color for citation links
    linkcolor=black, % Color for internal links
}

% Required for highlighting text
\usepackage{soul} 

% Required for bibliography management
\usepackage{biblatex}
% Add the bibliography file
\addbibresource{citations.bib} 

% Required for enhanced referencing
\usepackage{cleveref} 

% Required for subfigures
\usepackage{subcaption}

% Required for positioning floats
\usepackage{float} 

% Required for multiple columns
\usepackage{multicol} 

% Required for page layout
\usepackage[landscape]{geometry}

% Required for displaying keyboard shortcuts
\usepackage{menukeys} 

% \geometry{OPTIONS}: Sets page dimensions and margins. Example options are top, left, right, bottom.
\geometry{top=.5in,left=.5in,right=.5in,bottom=.5in}

% Turn off header and footer
\pagestyle{empty}


% \renewcommand{\COMMAND}[ARGUMENTS]{NEW_DEFINITION}: Redefines an existing command with a new definition. We will use the following three commands to reduce the whitespace for the cheatsheet. Don't worry too much about these commands
\makeatletter
\renewcommand{\section}{\@startsection{section}{1}{0mm}%
                                {-1ex plus -.5ex minus -.2ex}%
                                {0.5ex plus .2ex}%x
                                {\normalfont\large\bfseries}}
\renewcommand{\subsection}{\@startsection{subsection}{2}{0mm}%
                                {-1explus -.5ex minus -.2ex}%
                                {0.5ex plus .2ex}%
                                {\normalfont\normalsize\bfseries}}
\renewcommand{\subsubsection}{\@startsection{subsubsection}{3}{0mm}%
                                {-1ex plus -.5ex minus -.2ex}%
                                {1ex plus .2ex}%
                                {\normalfont\small\bfseries}}
\makeatother

% Don't print section numbers
\setcounter{secnumdepth}{0}

% Set paragraph formatting
\setlength{\parindent}{0pt}
\setlength{\parskip}{0pt plus 0.5ex}

% \begin{ENVIRONMENT} ... \end{ENVIRONMENT}: Begins and ends an environment. For example \begin{document} starts our document and \end{docuement} concludes it. Everything between \begin and \end will be displayed in the document
\begin{document}

% We will use a four colmun layout to reduce whitespace
\begin{multicols}{4}
{\huge\LaTeX} is a powerful text editing suite. Here is a list of helpful commands!

% \section{TITLE}, \subsection{TITLE}, etc.: Creates a new section, subsection, etc., with the given title.
\section{Text Commands}
% To show LaTeX commands as text, we use the \verb command. This tells latex to directly print the text, and not to execute the commands. 
\subsection{Verbatim}
\begin{center}
\begin{tabular}{ll}
\verb|\verb| & print line \\
\verb|\begin{verbatim}| & print multiple \\
\end{tabular}
\end{center}
\subsection{Text Emphasis}
\begin{center}
    \begin{tabular}{ll}
    \verb|\textit{text}| & \textit{Italicize text} \\
    \verb|\textbf{text}| & \textbf{Bold text}\\
    \verb|\textsc{text}| & \textsc{Small Caps}\\
    \verb|\emph{text}| & \emph{Emphasized}\\
    \verb|\underline{text}| & \underline{Underline}
\end{tabular}
\end{center}
\vspace{-8pt}
\subsection{Font Size}
\begin{center}
 \begin{tabular}{ll}
\verb|\tiny|          &  \tiny{tiny} \\
\verb|\scriptsize|    &  \scriptsize{scriptsize} \\
\verb|\footnotesize|  &  \footnotesize{footnotesize} \\
\verb|\small|         &  \small{small} \\
\verb|\normalsize|    &  \normalsize{normalsize} \\
\verb|\large|         &  \large{large} \\
\verb|\Large|         &  \Large{Large} \\ 
\verb|\LARGE|         &  \LARGE{LARGE} \\
\verb|\huge|          &  \huge{huge} \\
\verb|\Huge|          &  \Huge{Huge}
\end{tabular}   
\end{center}
\vspace{-8pt}
\subsection{Inline Symbols}
\begin{tabular}{rl}
\verb|\&| & \& \\
\verb|\textbar| & \textbar\\ 
\verb|\textbackslash| & \textbackslash\\
\verb|\%| & \%\\
\verb|\$| &\$ 
\end{tabular}
\subsection{Sections}
Sections are made with \verb|section|
\begin{center}
    \begin{tabular}{ll}
        \verb|section{Title}| & {\large\textbf{Title}} \\
        \verb|subsection{Title}| & {\normalsize\textbf{Title}} \\
        \verb|subsubsection{Title}| & {\small\textbf{Title}} \\
    \end{tabular}
\end{center}
\subsection{Spacing}
\begin{tabular}{ll}
    \verb|\vspace{X}| & Move text vertically X \\
    \verb|\vfill| & Fill text vertically\\
    \verb|\\| & Creates a new line\\
    \verb|\newpage| & Makes a new page
\end{tabular}
\section{Tabular Commands}
Create a table by:
\vspace{-5pt}
\begin{verbatim}
\begin{tabular}{cc}
    a & b  \\
    c & d
\end{tabular}
\end{verbatim}
\subsection{Column Specifications}
\begin{center}
\begin{tabular}{c|l|r}
    center & left & right\\
    c & l & r\\
\end{tabular}   
\end{center}

Add horizontal lines with \verb|\hline| at the start or end of each row; or vertical lines with \verb!|! when setting column alignment


\section{Equations}
Use \verb|$$| to place equations inline, or display them with \verb|\begin{equation}|

\subsection{Math Symbols}
Symbols are produced with commands, usually their English name or an abbreviation of it
\begin{center}
\begin{tabular}{cc|cc}
    
    \verb|\pi| & $\pi$ & \verb|\Pi| & $\Pi$ \\
    \verb|\infy| & $\infty$ & \verb|\pm| & $\pm$ \\
    \verb|\hat a| & $\hat a$ & \verb|\dot a| & $\dot a$
\end{tabular}    
\end{center}
\subsection{Math Operations}
Operations are produced by functions
\begin{center}
    \begin{tabular}{cc}
    \verb|\frac{a}{b}| & $\frac{a}{b}$ \\
    \verb|a^{x}| & $a^{x}$ \\
    \verb|a_{x}| & $a_{x}$ \\
    \verb|\sum^a_b| & $\sum^a_b$\\
    \verb|\int^b_a| & $\int^b_a$\\
    \verb|\lim_a| & $\lim_a$\\
\end{tabular}
\end{center}
\subsection{Combing Operations}
\Cref{eqn:anExampleEquation} shows how multiple operations can be combined in sequence
\begin{equation}\label{eqn:anExampleEquation}
    \overbrace{\int_a^b}^{\texttt{\makebox[0pt]{\textbackslash int\_a\^{}b} }}f(x)dx = \underbrace{\lim_{n\rightarrow\infty}}_{\texttt{\makebox[0pt]{\textbackslash lim\_\{{n\textbackslash rightarrow\textbackslash infty\}}}}} \overbrace{\sum^n_{i=1}}^{\texttt{\makebox[0pt]{\textbackslash sum\^{}n\_\{i=1\}}}} f(x_i)\Delta x
\end{equation}
where $\Delta x=\frac{b-a}{n}$ and $x_i = a + \Delta x\times i$
\section{Comments}
To leave comments, use \%. Nothing after \% will be displayed/executed.

\section{Packages}
Packages are powerful libraries that add new functionality to \LaTeX. Use \verb|\usepackage[OPTIONS]{NAME}| before \verb|\begin{document}|\\
Several commonly used libraries are:
\begin{tabular}{ll}
    \verb|hyperref| & used for hyperlinks \\
    \verb|soul| & \hl{used for highlighting}\\
    \verb|xcolor| & {\color{red} Add} {\color{blue} colors}\\
    \verb|asmath| & More math terms\\
    \verb|biblatex| & Add citations \cite{myPaper}\\
    \verb|cleveref| & Better references\\
    \verb|subcaption| & Need for subfigures\\
    \verb|float| & Floats images
\end{tabular}
\section{Biblatex}
The bibtex citation of an article looks like:
\begin{verbatim}
@article{Ref Name,
  title={Paper title},
  author={Authors},
  journal={A good Journal},
  year={Year},
}
\end{verbatim}
Place all of them them in a new file called \verb|citations.bib|\\
Then:\\
\begin{tabular}{ll}
   \verb|\cite| & cite a paper \\
   \verb|\parencite| & (cite a paper)\\
   \verb|\printbibliography| & display bib.
\end{tabular}

\section{Overleaf Short-cuts}
\begin{tabular}{ll}
    \verb|ctrl* + enter| & compile doc. \\
    \verb|ctrl* + /| & comment section\\
    \verb|ctrl* + b| & \textbf{bold}\\
    \verb|ctrl* + i| & \textit{italicize}\\
    \verb|ctrl + U| & UPPERCASE\\
    \verb|ctrl + shift + U| & lowercase\\
    \verb|ctrl + space| & autocomplete\\
    \verb|alt + shift + |\arrowkey{^} & move line
\end{tabular}
* use \cmd\ instead of \verb|ctrl| on Mac
\vfill

\section{Figures}
To create a figure, use \verb|\begin{figure}|
\begin{figure}[H]
    \centering
    \includegraphics[width=0.3\linewidth]{Subject.png}
    \caption{Tofu!}
    \label{fig:enter-label}
\end{figure}
Use \verb|\subfigures| to make figures side-by-side, needs package \verb|subcaption|
\begin{figure}[H]
     \centering
     \begin{subfigure}{0.49\linewidth}
         \centering
         \includegraphics[width=\linewidth]{Subject 3.png}
         \caption{Meow}
         \label{imgA}
     \end{subfigure}
     \hfill
     \begin{subfigure}{0.49\linewidth}
         \centering
         \includegraphics[width=\linewidth]{IMG_0546 2.png}
         \caption{Tofu's House}
         \label{imgB}
     \end{subfigure}
        \caption{Tofu relaxing}
        \label{fig:twoImages}
\end{figure}
% \printbibliography
To scale the image, we commonly scale its width to match the page width, but we can also scale the image overall.
\begin{tabular}{ll}
    \verb|width=\textwidth| & sets image width\\
    \verb|scale=NUM| & scales by NUM 
\end{tabular}

\section{List items}
To create lists of things, we can use either \verb|enumerate| or \verb|itemize|
\vspace{-8pt}
\begin{enumerate}
    \item \verb|enumerate| creates a numbered list
    \itemsep0em 
    \item \verb|itemize| creates a bulleted list
    \itemsep0em 
    \begin{itemize}
        \item They can be nested!
    \end{itemize}
\end{enumerate}

\section{Commands}
For repeated operations, a macro can be created with \verb|\newcommand{}[]{}|. 
ex.: \verb|\newcommand{\hello}{Hello!}|

These or existing commands can be modified by \verb|\renewcommand{}{}| ex.: \\
\verb|\renewcommand{\hello}{Bonjour!}|

\end{multicols}

\end{document}
```
