These guidelines are based on the [Contributing to NVDA](https://github.com/nvaccess/nvda/wiki/Contributing) document.

It's assumed that you're working on Windows, with the last stable or master version of NVDA. For the examples related to Git, we'll assume you're using Git from the Windows command line (`windows+r`, `cmd`).

## Request changes ##

For anything other than minor bug fixes, please comment on an existing issue or create a new issue providing details about your proposed change. Unrelated changes should be addressed in separate issues. Include information about use cases, design, user experience, etc. This allows us to discuss these aspects and any other concerns that might arise, thus potentially avoiding a great deal of wasted time. 

If you're reporting a bug, include:

- Steps to reproduce.
- Actual behavior.
- Expected behavior.
- Any information which could be relevant, like specific programs or add-ons you are using.
- You can zip and attach your NVDA's log file. Also, more feedback could be required to debug and fix the reported bug.

If this is a minor/trivial change which definitely wouldn't require design, user experience or implementation discussion (e.g. a fix for a typo/obvious coding error), you can just create a pull request rather than using an issue first. 

For convenience, issues and pull request provide templates to help in the contribution process. They are based on the issue and pull request templates of the [NVDA repo](https://github.com/nvaccess/nvda).

Also, you can see and contribute our [code of conduct](https://github.com/nvdaes/reportSymbols/blob/master/CODE_OF_CONDUCT.md).

## Make changes ##

### If this is your first contribution ###

1. Fork the add-on repository on GitHub.
2. Clone your repo as follows:
`git clone https://github.com/yourGitHubUserName/reportSymbols`
3. From your local folder for the cloned repo, add this repo as your upstream remote:
`git remote add upstream https://github.com/nvdaes/reportSymbols`
4. Link the master branch of this repo with your local master branch, to receive updates from this repo:
`git fetch upstream`
`git branch -u upstream/master`

### Before making changes ###

1. Be sure you are in the master branch:
`git checkout master`
2. Update your master branch:
`git pull`
3. Create a topic branch. For instance, if your changes are related to issue 2, you could do:
`git checkout -b i2`

### Making changes ###

You can make changes in the add-on code, following the [Contributing to NVDA](https://github.com/nvaccess/nvda/wiki/Contributing) guidelines.

Add and commit changes providing a descriptive message, for instance:
`git add .`
`git commit`

> Buildvars.py: Change add-on description
>
> (Blank line)
>
> Make the add-on description consistent with the info provided in the readme.md file

### Submitting changes ###

- Build the add-on and test it on your system: `scons`
- If all is right, send changes to your branch on GitHub, for instance: `git push origin i2`
- Create a pull request on GitHub.
