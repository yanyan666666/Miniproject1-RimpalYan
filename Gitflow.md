# Gitflow Workflow

## What Is GitFlow

GitFlow is a branching model for Git, created by Vincent Driessen. It has attracted a lot of attention because it is very well suited to collaboration and scaling the development team.

## Key Benefits

## Parallel Development

One of the great things about GitFlow is that it makes parallel development very easy, by isolating new development from finished work. New development (such as features and non-emergency bug fixes) is done in feature branches, and is only merged back into main body of code when the developer(s) is happy that the code is ready for release.

## Collaboration

Feature branches also make it easier for two or more developers to collaborate on the same feature, because each feature branch is a sandbox where the only changes are the changes necessary to get the new feature working. That makes it very easy to see and follow what each collaborator is doing.

## How It Works

New development (new features, non-emergency bug fixes) are built in feature branches:
![gitflow1](/image/GitFlow1)

Feature branches are branched off of the develop branch, and finished features and fixes are merged back into the develop branch when they’re ready for release:

![gitflow2](/image/GitFlow2)

When it is time to make a release, a release branch is created off of develop:

![gitflow3](/image/GitFlow3)

The code in the release branch is deployed onto a suitable test environment, tested, and any problems are fixed directly in the release branch. This deploy -> test -> fix -> redeploy -> retest cycle continues until you’re happy that the release is good enough to release to customers.

When the release is finished, the release branch is merged into master and into develop too, to make sure that any changes made in the release branch aren’t accidentally lost by new development.

![gitflow4](/image/GitFlow4)

The master branch tracks released code only. The only commits to master are merges from release branches and hotfix branches.<b>

Hotfix branches are used to create emergency fixes:

![gitflow5](/image/GitFlow5)

They are branched directly from a tagged release in the master branch, and when finished are merged back into both master and develop to make sure that the hotfix isn’t accidentally lost when the next regular release occurs.
