
# LaTeX Project with custom.sty

This repository contains a LaTeX project template that includes the use of a custom style file `custom.sty`. This file allows you to define and reuse custom LaTeX commands, environments, and formatting rules across multiple documents.

## What is `custom.sty`?

- `custom.sty` is a user-defined LaTeX style file where you can store custom commands, environments, or settings that you frequently use in your LaTeX documents.
- Using a `.sty` file like `custom.sty` helps you maintain a clean and modular LaTeX codebase, making it easier to manage and reuse across different projects.

## Why Use a `.sty` File?

1. **Modularity:** Encapsulate custom commands and formatting rules in a separate file to keep your main LaTeX document clean and readable.
2. **Reusability:** Reuse the same style and formatting across multiple documents without rewriting the LaTeX code.
3. **Consistency:** Ensure consistent formatting across documents by using the same `.sty` file.

## Example `custom.sty` File

Here’s a simple example of what might be included in a `custom.sty` file:

```latex
% custom.sty - Custom LaTeX Style File

\ProvidesPackage{custom}  % Provide package name

% Custom command to highlight text
\newcommand{\highlight}[1]{\textbf{\textcolor{red}{#1}}}

% Custom environment for a colored box
\usepackage{tcolorbox}
\newenvironment{mybox}[1][Important]
  {\begin{tcolorbox}[colback=yellow!10!white, colframe=red!50!black, title=#1]}
  {\end{tcolorbox}}

% Custom section formatting
\usepackage{titlesec}
\titleformat{\section}
  {\normalfont\Large\bfseries\color{blue}} % Format section titles
  {\thesection}{1em}{}

% Any other customizations can be added here
```

## How to Use `custom.sty` in Your LaTeX Document

### Step 1: Create the `custom.sty` File

- Place the `custom.sty` file in your project's `sty/` directory (or any other directory, as long as you specify the correct path).

### Step 2: Include the `custom.sty` File in Your LaTeX Document

- In your `main.tex` or any other LaTeX file where you want to use the customizations, include the `custom.sty` file with the `\usepackage{}` command.

```latex
\documentclass{article}
\usepackage[utf8]{inputenc}
\usepackage{graphicx}
\usepackage{custom}  % Include your custom style file

\title{Your Document Title}
\author{Your Name}
\date{\today}

\begin{document}

\maketitle

\section{Introduction}

This is a sample document.

% Using the custom \highlight command
Here is some \highlight{important} text.

% Using the custom mybox environment
\begin{mybox}[Note]
This is a custom box created using the mybox environment.
\end{mybox}

\end{document}
```

### Step 3: Compile Your Document

- Compile your LaTeX document as usual. The custom commands and environments defined in `custom.sty` will be available throughout your document.

## Benefits of Using `custom.sty`

- **Centralized Customization:** All your custom LaTeX code is in one place, making it easier to manage and update.
- **Easy Collaboration:** Share the `custom.sty` file with collaborators to ensure everyone is using the same formatting and commands.
- **Scalability:** As your LaTeX projects grow, you can add more customizations to `custom.sty` without cluttering your main document.