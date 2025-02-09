## Template based on [ITESM-MIT-MasterThesis](https://www.overleaf.com/project/67a8d5d2840f0d9ff5c938e4)
- [Basic PDF example](example.pdf)
- Main file [MIT-MasterThesis.tex](src/MIT-MasterThesis.tex)
- Changed to use `biblatex`
    - Directly inserts bibliography on main file [MIT-MasterThesis.tex:44](src/MIT-MasterThesis.tex#L44)
    - Uses IEEE style [MIT-MasterThesis.tex:19](src/MIT-MasterThesis.tex#L19)
- Created define `dissertationLocation`
    - Uses value on [MIT-MasterThesis.tex:37](src/MIT-MasterThesis.tex#L37)
- Working build using VSCode (WSL Ubuntu) and LaTeX + LaTeX workshop extensions
    - Build directly from main file [MIT-MasterThesis.tex](src/MIT-MasterThesis.tex)
    - [.gitignore](.gitignore#L1) automatically ignores `build` folder inside `src`
    - Strongly recommended to modify VSCode's User JSON settings to create all LaTeX output in a `build` folder
        - Command Palette (CTRL+SHIFT+P) -> Open user settings (JSON) -> Add the following
    ```json
    "latex-workshop.latex.outDir": "./build",
    "latex-workshop.latex.clean.subfolder.enabled": true,
    "latex-workshop.latex.clean.fileTypes": [
        "*.aux",
        "*.bbl",
        "*.blg",
        "*.lof",
        "*.lot",
        "*.fls",
        "*.log",
        "*.out",
        "*.toc",
        "*.synctex.gz",
        "*.fdb_latexmk"
    ],