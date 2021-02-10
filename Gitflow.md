# Gitflow Workflow

## What Is GitFlow

GitFlow is a branching model for Git, created by Vincent Driessen. It has attracted a lot of attention because it is very well suited to collaboration and scaling the development team.

## Key Benefits

### Parallel Development

One of the great things about GitFlow is that it makes parallel development very easy, by isolating new development from finished work. New development (such as features and non-emergency bug fixes) is done in feature branches, and is only merged back into main body of code when the developer(s) is happy that the code is ready for release.

### Collaboration

Feature branches also make it easier for two or more developers to collaborate on the same feature, because each feature branch is a sandbox where the only changes are the changes necessary to get the new feature working. That makes it very easy to see and follow what each collaborator is doing.

## How It Works

New development (new features, non-emergency bug fixes) are built in feature branches:
![gitflow1](/image/GitFlow1.png)

Feature branches are branched off of the develop branch, and finished features and fixes are merged back into the develop branch when they’re ready for release:

![gitflow2](/image/GitFlow2.png)

When it is time to make a release, a release branch is created off of develop:

![gitflow3](/image/GitFlow3.png)

The code in the release branch is deployed onto a suitable test environment, tested, and any problems are fixed directly in the release branch. This deploy -> test -> fix -> redeploy -> retest cycle continues until you’re happy that the release is good enough to release to customers.

When the release is finished, the release branch is merged into master and into develop too, to make sure that any changes made in the release branch aren’t accidentally lost by new development.

![gitflow4](/image/GitFlow4.png)

The master branch tracks released code only. The only commits to master are merges from release branches and hotfix branches.<b>

Hotfix branches are used to create emergency fixes:

![gitflow5](/image/GitFlow5.png)

They are branched directly from a tagged release in the master branch, and when finished are merged back into both master and develop to make sure that the hotfix isn’t accidentally lost when the next regular release occurs.

## How does using Git, Docker, Automated Testing, and continuous Integration help

* Dockers are integrated with source control management tools such as GitHub and Integration tools like Jenkins. 
* The code is then pushed by the developers into GitHub, test the code that automatically triggers a build using Jenkins creating an image. The image is added to the Docker registry to deal with inconsistencies between different environmental issues.
* Continuous integration is a development practice in which developers integrate code into a shared repository several times a day, supporting integrating new functionality with the existing code. This integrated code also ensures no errors in the runtime environment, allowing us to check how it reacts with other changes.
* Developers use Dockers in building their code and test their code in any environment to catch bugs early in the application development life cycle. Dockers are useful in streamlining the process. It helps to save time on builds and allows developers to run tests in parallel.
* In this way the results are coherence in every organization's software development process since it helps build software quickly. Therefore, the productivity and competitiveness of an organization are improved.
