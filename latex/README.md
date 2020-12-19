# Using latex docker for vs-code

With the following extensions:

[latex-workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop)

[docker containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)

    {
        // ... YOUR OTHER SETTINGS ...

        // latex
        "latex-workshop.docker.enabled": true,
        "latex-workshop.latex.outDir": "./out",
        "latex-workshop.synctex.afterBuild.enabled": true,
        "latex-workshop.view.pdf.viewer": "tab",
        "latex-workshop.docker.image.latex": "dgrnwd/latex",
        // End
    }

create a test file `test.tex` :

    \documentclass{article}
    \begin{document}
    A \LaTeX \ document.
    \end{document}
