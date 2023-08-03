# bash-template

![GitHub last commit (branch)](https://img.shields.io/github/last-commit/yeenbean/bash-template/master?style=for-the-badge)
![GitHub issues](https://img.shields.io/github/issues/yeenbean/bash-template?style=for-the-badge)
![GitHub](https://img.shields.io/github/license/yeenbean/bash-template?style=for-the-badge)



A simple starting place for new Bash scripts. This script:

- Uses `/usr/bin/env bash` for portability.
- Uses the unofficial
[Bash Strict Mode](http://redsymbol.net/articles/unofficial-bash-strict-mode/).
- Checks that bash 4 is executing the script.

## Usage

### Option 1: clone this repository as a template

The easiest way to get started is by clicking the green **Use this template**
button, then selecting **Create a new repository**. You will then be guided
through creating a new repository in your account that uses the files in this
repository as a template!

### Option 2: Visual Studio Code snippet

Open the user snippets file called "shellscript.json" and add the following:

```json
"Bash Strict Mode Starter": {
  "prefix": "starter",
  "body": ["#!/usr/bin/env bash","#","# Short description goes here. Maximum 3 sentences. If possible, keep each line","# under 80 characters for easy readability.","","","init() {","  set -euo pipefail # strict mode","  #set -x            # uncomment when debugging your script","  IFS=$'\\n\\t'       # IFS restricted to newline and tab","}","","","main() {","  init # run init function","  echo success","}","","","# make sure bash 4 is being used and run the script, exit otherwise","# this prevents people from running the script with an unsupported interpreter","if [ -z \"${BASH_VERSINFO}\" ] || [ -z \"${BASH_VERSINFO[0]}\" ] || [ ${BASH_VERSINFO[0]} -lt 4 ]","then","  echo \"This script requires Bash version 4 or newer.\"","  exit 1","else","  main","fi"],
  "description": "A starter script for a Bash shell script."
}
```

## Issues

The issues tracker contains both issues and feature requests. There are
templates available if you're not sure how to submit your issue.

### Issues for Newcomers

Occasionally, I will mark simple issues with the **good first issue** label so
that newcomers to `git` can learn the ropes. If you're new, please check these
out to get your hands dirty!

If you have absolutely no experience to the `git` workflow, or you need a
refresher, check out [this site](http://rogerdudler.github.io/git-guide/) made
by [rogerdudler](https://github.com/rogerdudler)!

## Contributing

1. Fork this repository
1. Add your change
1. Create a pull request

_Note: I am testing GitKraken's GitFlow feature with this repository. You are
**NOT** required to follow this style of contribution._
