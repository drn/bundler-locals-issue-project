# Bundler Locals Issue Repro

## Instructions

* `$ mkdir -p ~/Desktop/bundler-locals-issue`
* `$ cd ~/Desktop/bundler-locals-issue`
* `$ git clone git@github.com:drn/bundler-locals-issue-project.git project`
* `$ git clone git@github.com:drn/bundler-locals-issue-gem.git gem`
* `$ cd ~/Desktop/bundler-locals-issue/project`
* `$ bundle config local.bundler-locals-issue ~/Desktop/bundler-locals-issue/gem`
* `$ bundle install` or `$ bundle update bundler-locals-issue`
  * **Reproduces Issue**
* `$ bundle config --delete local.bundler-locals-issue`

## Example Run

```
~ ❯ mkdir -p ~/Desktop/bundler-locals-issue
~ ❯ cd ~/Desktop/bundler-locals-issue
bundler-locals-issue ❯ git clone git@github.com:drn/bundler-locals-issue-project.git project
Cloning into 'project'...
remote: Counting objects: 5, done.
remote: Compressing objects: 100% (5/5), done.
remote: Total 5 (delta 0), reused 5 (delta 0), pack-reused 0
Receiving objects: 100% (5/5), done.
Checking connectivity... done.
bundler-locals-issue ❯ git clone git@github.com:drn/bundler-locals-issue-gem.git gem
Cloning into 'gem'...
remote: Counting objects: 9, done.
remote: Compressing objects: 100% (6/6), done.
remote: Total 9 (delta 0), reused 9 (delta 0), pack-reused 0
Receiving objects: 100% (9/9), done.
Checking connectivity... done.
bundler-locals-issue ❯ cd ~/Desktop/bundler-locals-issue/project
project ⭠ master ❯ bundle config local.bundler-locals-issue ~/Desktop/bundler-locals-issue/gem
project ⭠ master ❯ bundle install
https://github.com/drn/bundler-locals-issue-gem (at TA-1000@d8a205d) is not yet checked
out. Run `bundle install` first.
project ⭠ master ❯ bundle update bundler-locals-issue
https://github.com/drn/bundler-locals-issue-gem (at TA-1000@d8a205d) is not yet checked
out. Run `bundle install` first.
project ⭠ master ❯ bundler --version
Bundler version 1.12.5
```
