# Using latex-action :octocat:

[![GitHub Actions Status](https://github.com/mxochicale/using-latex-action/workflows/Compiling-TeX/badge.svg)](https://github.com/mxochicale/using-latex-action/actions)

## Introduction 
[Cheng XU](https://xuc.me) developed a nice github action to build tex files called [latex-action](https://github.com/xu-cheng/latex-action).
So the idea of build your TeX files in Github was crazy for me that motivate me to create this repository with 
the purpose of documenting the necessary, and perhaps the non obvious, 
dependencies to build LaTeX examples in section of [tutorials](https://github.com/xu-cheng/latex-tutorial), 
xu's [cv](https://github.com/xu-cheng/cv) and a thesis template.

## Setting it up
1. Add `shh-rsa` key in https://github.com/settings/keys following [the documentation](https://help.github.com/en/github/authenticating-to-github/adding-a-new-ssh-key-to-your-github-account) in github.


2. Create a new secret variable called `DEPLOY_KEY` in   
https://github.com/mxochicale/using-latex-action/settings/secrets   
Where the value is taken from `id_rsa` with 
`vim ~/.ssh/id_rsa` which looks like:  
```
-----BEGIN RSA PRIVATE KEY-----
...
-----END RSA PRIVATE KEY-----
```

3. Create a gh-pages branch for the pdf files [(see more)](https://www.freecodecamp.org/forum/t/push-a-new-local-branch-to-a-remote-git-repository-and-track-it-too/13222).
```
git checkout -b generated-pdfs
rm -rf * README.md .github .gitignore *swp ~.git 
git add -A
git commit -m 'clean generated-pdfs branch'
git push origin generated-pdfs
```

## Logbook
* :fireworks: 2020-08-31T1522: The commit [3f56c3](https://github.com/mxochicale/learning-latex-action/commit/3f56c3afc27e2a6a1d0d764734d2ab666565bfb5)
adds [poster.tex](poster/main.tex) and figures to then build [poster.pdf](https://github.com/mxochicale/learning-latex-action/blob/gh-pages/poster.pdf)
 
* :fireworks: 2020-04-20T1847: Creates a [PR](https://github.com/mxochicale/using-latex-action/pull/2) to commit changes to 
example.tex and then to build [example.pdf](https://github.com/mxochicale/using-latex-action/blob/gh-pages/example.pdf)
 
* :fireworks: 2020-04-10T13-57: The commit [d073f64](https://github.com/mxochicale/using-latex-action/commit/d073f64c88d9c57406fe17a75c05652539299731) passed
ci creating [thesis.pdf](https://github.com/mxochicale/using-latex-action/blob/gh-pages/thesis.pdf) and available in the gh-pages 
as https://mxochicale.github.io/using-latex-action/thesis.pdf

* :fireworks: 2020-03-19T23-15: The commit [ccd018](https://github.com/mxochicale/using-latex-action/commit/ccd0187b8657787255d324ace9aa3f59bb6758a4) passed
ci creating [cv.pdf](https://github.com/mxochicale/using-latex-action/blob/gh-pages/cv.pdf) and available in the gh-pages 
as https://mxochicale.github.io/using-latex-action/cv.pdf

* :fireworks: 2020-03-18T22-13: The commit [13b9cb](https://github.com/mxochicale/using-latex-action/commit/13b9c6b296e89789e9d816a626f33430a9dcf0c3) 
passed ci creating [slides.pdf](https://github.com/mxochicale/using-latex-action/blob/gh-pages/slides.pdf) and available in the gh-pages 
as https://mxochicale.github.io/using-latex-action/slides.pdf

* :fireworks: 2020-03-15T23-10: The commit [518fff](https://github.com/mxochicale/using-latex-action/commit/518ffff66db0f74dc650746a6f873a0689b1dce3)
passed the ci creating [example.pdf](https://github.com/mxochicale/using-latex-action/blob/gh-pages/example.pdf) and available in the gh-pages 
as https://mxochicale.github.io/using-latex-action/example.pdf

* :fireworks: 2020-03-15T17-08: The commit [9c788fc](https://github.com/mxochicale/trying-latex-action/commit/9c788fc969b5944a70581bcf7ff425325b45396a) passed 
the test using '@actions/upload-release-asset' which upload a main.zip to the [Github Release](https://github.com/mxochicale/trying-latex-action/actions/runs/56217321). master.zip contains the PDF file.
 
## License 
[CC-BY 4.0](LICENCE)   
[![CC-BY 4.0](https://mirrors.creativecommons.org/presskit/buttons/88x31/svg/by.svg)](http://creativecommons.org/licenses/by/4.0/)
