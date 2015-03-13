# git_in_practice
original: https://github.com/GitInPractice/GitInPracticeRedux

# git config --global user.name
# roy
# git config --global user.email
# roy_radio@126.com

# git init GitInPracticeRedux

# git add GitInPractice.asciidoc
# git status

# git commit --message 'Initial commit of book.'

# git log

On OS X, there are tools such as GitX, GitX-dev is available at https://github.com/rowanj/gitx
Run gitk or gitx

# git log diff

# git diff master~1 master
# git diff --stat master~1 master
# git diff --word-diff master~1 master

Parsing refs
# git rev-parse master

# git remote --verbose

Pushing and setting an upstream branch
# git push --set-upstream origin master	(-u)

# git clone https://github.com/royzamplus/git_in_practice.git GitInPracticeRedux
# git clone https://github.com/royzamplus/git_in_practice.git GitInPracticeReduxPushTest

# git pull

Fetching changes from a remote without modifying local branches: git fetch
(git fetch == git fetch && git merge origin/master)
# git fetch

# git branch chapter-two

Checking out a local branch: git checkout
# git checkout chapter-two

# git merge chapter-two

Deleting remote branch
# git push --delete origin chapter-two

Deleting the current local branch after merging
# git branch --delete chapter-two

# git mv GitInPractice.asciidoc 01-IntroducingGitInPractice.asciidoc

# git rm GitInPracticeReviews.tmp

Resetting files to the last commit: git reset
# git reset --hard

Deleting untracked files: git clean
# git ls-files
# git ls-files --others

# git clean --force
# git clean -n (--dry-run)

# echo \*.tmp > .gitignore
# git clean --force -X

Temporarily stashing some changes: git stash
# git stash save

# git stash list
# git diff stash@{0}

# git stash pop / # git stash apply
# git stash clear

Listing assumed-unchanged files
# git update-index --assume-unchanged 01-IntroducingGitInPractice.asciidoc
# git ls-files -v
# git ls-files -v | grep '^[hsmrck?]' | cut -c 3-
# git update-index --no-assume-unchanged 01-IntroducingGitIn-Practice.asciidoc

# git log --author 'roy' --after 'Mar 10 2015' --grep 'file\.'

# git show HEAD^

# git log --format=email --reverse --max-count 2

# git log --format="%ar %an did: %s"

# git shortlog HEAD~6..HEAD

# git log --oneline --graph --decorate

Showing who last changed each line of a file: git blame
# git blame --date=short 01-IntroducingGitInPractice.asciidoc

Finding which commit caused a particular bug: git bisect
# git bisect start
# git bisect bad
# git bisect good <#>

# git show

# git bisect log

Force merge commit
# git merge --no-ff chapter-spacing

Resolving each merge conflict only once: git rerere
# git config --global --add rerere.enabled 1
# git rerere forget 01-IntroducingGitInPractice.asciidoc

# git tag v0.1
# git tag (--list/--force/--delete)

# git push --tags

Generating a version number based on previous tags: git describe
# git describe --tags

Adding a single commit to the current branch: git cherry-pick
# git cherry-pick v0.1-release

Reverting a previous commit: git revert
# git revert <#>

# git cherry --verbose master

# git reflog

# git reset HEAD^

# git rebase v0.1-release
