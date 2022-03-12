# LaTeX Template for Howest MCT thesis 

This is a LaTeX template for the bachelor thesis of the MCT course at Howest, Belgium.

## Installation

1) Install LaTeX: `texlive` package group on Linux, or see https://www.tug.org/texlive/ for Windows & macOS.
2) Install the Pygments package: `pip install Pygments` to make code blocks work properly 
3) Install the LaTeX-Workshop extension in Visual Studio Code
4) Add the following to your VSCode settings by opening the JSON settings (`Ctrl+Shift+P` > `Preferences: Open Settings (JSON)`):

(I didn't test this JSON on Windows, create an issue if you encounter problems.)
```json
"latex-workshop.latex.recipes": [
	{
		"name": "latexmk 🔃",
		"tools": ["latexmk"]
	}
	],
"latex-workshop.latex.tools": [
	{
		"name": "latexmk",
		"command": "latexmk",
		"args": [
			"-synctex=1",
			"-interaction=nonstopmode",
			"-file-line-error",
			"-pdf",
			"-shell-escape",
			"-outdir=%OUTDIR%",
			"-cd",
			"%DOC%"
		],
		"env": {}
	}
]
```

5) Compile your LaTeX document using the green arrow in the top right when the .tex file is opened.
