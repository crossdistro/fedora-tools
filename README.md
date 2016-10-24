# Wrapper over Fedora package maintainance tools

Note: The use cases below are untested. Use with care.

## Make a fix and a build ##

fptool --master --bump --scratch-build --commit --push --build

## Make a scratch build from locally generated SRPM ##

fptool --scratch-build

## Bump a rawhide package to a newer version ##

## Prepare rawhide to replace branches ##

## Update branches to match rawhide, build and issue updates ##

fptool --branches="f23 f22" --merge --push --build --update

## Create a private branch and a scratch build ##

Make changes (on top of any branch but preferably on the right one so that it merges easily).

fptool \
    --rhbug="1234567" --branch=f23 \
    --private-branch --bump --scratch-build --commit --push --stay
