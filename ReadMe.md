
# LaTeX Project Template

This repository contains a template for a LaTeX project, including the setup instructions for using LaTeX in Visual Studio Code (VSCode).

## Setup Instructions

### Step 1: Install MiKTeX

#### Windows
1. Download and install [MiKTeX](https://miktex.org/download) on your Windows machine.
2. Follow the default installation options and ensure that MiKTeX is added to your system's environment variables.
3. After installation, MiKTeX may prompt you to update packages. Click "Update now" and restart MiKTeX when prompted.

#### Linux
1. Install MiKTeX using your distribution's package manager:
   - For Ubuntu or Debian-based systems:
     ```bash
     sudo apt-get install miktex
     ```
   - For Fedora:
     ```bash
     sudo dnf install miktex
     ```
   - For Arch Linux:
     ```bash
     sudo pacman -S miktex
     ```
2. After installation, you may need to run `miktexsetup finish` to complete the setup.

#### macOS
1. Download and install [MiKTeX](https://miktex.org/howto/install-miktex-mac) for macOS.
2. Follow the default installation options.
3. After installation, MiKTeX may prompt you to update packages. Click "Update now" and restart MiKTeX when prompted.

### Step 2: Install Strawberry Perl

#### Windows
1. Download and install [Strawberry Perl](http://strawberryperl.com/) on your Windows machine.
2. Follow the default installation options and ensure that Strawberry Perl is added to your system's environment variables.

#### Linux and macOS
1. **Perl is typically pre-installed on Linux and macOS.** To check if Perl is installed, open a terminal and type:
   ```bash
   perl -v
   ```
   If Perl is installed, you should see the version information.

2. If Perl is not installed, you can install it using your package manager:
   - **Linux:**
     - For Ubuntu or Debian-based systems:
       ```bash
       sudo apt-get install perl
       ```
     - For Fedora:
       ```bash
       sudo dnf install perl
       ```
     - For Arch Linux:
       ```bash
       sudo pacman -S perl
       ```
   - **macOS:**
     - You can use Homebrew to install Perl if needed:
       ```bash
       brew install perl
       ```

3. No additional steps are needed for environment variables on Linux or macOS, as Perl should be accessible by default.

### Step 3: Install VSCode
1. Download and install [Visual Studio Code](https://code.visualstudio.com/).

### Step 4: Install LaTeX Workshop and LaTeX Utilities Extensions
1. Open VSCode.
2. Go to the Extensions view by clicking on the Extensions icon in the Activity Bar on the side of the window or by pressing `Ctrl+Shift+X`.
3. Search for `LaTeX Workshop` by James Yu and click "Install".
4. Optionally, search for `LaTeX Utilities` and install it as well.

### Step 5: Verify LaTeX Setup in VSCode
1. Open VSCode and create a new `.tex` file (e.g., `main.tex`).
2. Add a simple LaTeX document structure to the file and save it.
3. Compile the document using the `Ctrl+Alt+B` shortcut. If everything is set up correctly, a PDF file should be generated.

## Project Structure

```
latex-project/
├── .gitignore
├── .vscode/
│   └── settings.json       # VSCode settings specific to this project (optional)
├── main.tex                # Main LaTeX document file
├── sections/
│   ├── introduction.tex    # Section files for different parts of the document
│   ├── YOURSECTION_1.tex
│   ├── YOURSECTION_2.tex
│   └── YOURSECTION_3.tex
├── figures/
│   ├── figure1.png         # Images used in the document
│   └── figure2.pdf
├── bibliography.bib        # BibTeX file for references
├── sty/                    # Custom LaTeX style files (optional)
│   └── custom.sty
└── README.md               # Project description and usage instructions
```

## Compiling the Document

To compile the LaTeX document, follow these steps:

1. **Open the Project in VSCode:**
   - Ensure you have opened the root directory of this project in VSCode.

2. **Edit the `main.tex` File:**
   - Make changes to your LaTeX source file as needed.

3. **Build the Document:**
   - Use `Build Latex Project` button or the shortcut `Ctrl+Alt+B` to build the document. This will generate a PDF file in the project directory.

4. **View the PDF:**
   - The PDF will be opened in the integrated viewer in VSCode. If not, you can open it manually from the project directory.

## Adding References

1. **Edit `bibliography.bib`:**
   - Add your references to the `bibliography.bib` file using the BibTeX format.

2. **Cite References in `main.tex`:**
   - Use the `\cite{}` command in your `main.tex` file to cite your references.

3. **Compile the Document:**
   - Rebuild the document to include the bibliography and citations.
