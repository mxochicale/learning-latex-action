<h1 align="center">
  Using latex-action
</h1>
<p align="center">
  Using and testing latex-action
</p>
<p align="center">
[![GitHub Actions Status](https://github.com/mxochicale/using-latex-action/workflows/Github%20Actions%20CI/badge.svg)](https://github.com/mxochicale/using-latex-action/actions)
</p>

## Intro
Cheng XU has developed a super nice github action to build tex files called [latex-action](https://github.com/xu-cheng/latex-action).
That said, this repository has the aim of documenting the necesary, and not obvious, dependencies to run some of the examples in [tutorials](https://github.com/xu-cheng/latex-tutorial) or even xu's [cv](https://github.com/xu-cheng/cv).

## Setting it up
1. add `shh-rsa` key in https://github.com/settings/keys following [this](https://help.github.com/en/github/authenticating-to-github/adding-a-new-ssh-key-to-your-github-account)

2. create secret variable `DEPLOY_KEY` in https://github.com/mxochicale/using-latex-action/settings/secrets
using: `~/.ssh/id_rsa` that contains 
```
-----BEGIN RSA PRIVATE KEY-----
~
-----END RSA PRIVATE KEY-----
```

3. create a gh-pages branch
```
git checkout -b gh-pages
git push -u origin gh-pages
```
For more, see [this](https://www.freecodecamp.org/forum/t/push-a-new-local-branch-to-a-remote-git-repository-and-track-it-too/13222).

## Milestones
* [2020-03-15T2310]: The commit [518fff](https://github.com/mxochicale/using-latex-action/commit/518ffff66db0f74dc650746a6f873a0689b1dce3)
passed the ci and it creates [example.pdf](https://github.com/mxochicale/using-latex-action/blob/gh-pages/example.pdf) in the gh-pages branch.

* [2020-03-15T1708]: The commit [9c788fc](https://github.com/mxochicale/trying-latex-action/commit/9c788fc969b5944a70581bcf7ff425325b45396a) passed 
the test using '@actions/upload-release-asset' which upload a main.zip to the [Github Release](https://github.com/mxochicale/trying-latex-action/actions/runs/56217321). master.zip contains the PDF file.
 
## License
[![CC-BY 4.0](https://mirrors.creativecommons.org/presskit/buttons/88x31/svg/by.svg)](http://creativecommons.org/licenses/by/4.0/)
