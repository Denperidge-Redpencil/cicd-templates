# Archival notice
This repository has been deprecated in favour of the [denperidge-redpencil/ci-quickstart repository on GitHub](https://github.com/Denperidge-Redpencil/ci-quickstart).

# Redpencil.io's CI/CD Templates

A repository for ready-to-use, but easily adaptable, quickstarts for CI/CD.

Structure/navigation:
- On [Woodpecker](woodpecker/) (recommended)...
    - ... using [Ember](woodpecker/ember/), I want to...
        - ... [run tests](woodpecker/ember/test.woodpecker.yml)
        - ... [build dry run](woodpecker/ember/build-dry-run.woodpecker.yml)
        - ... [push the latest build](woodpecker/ember/push-latest-build.woodpecker.yml)
        - ... [push the tagged build](woodpecker/ember/push-latest-build.woodpecker.yml) 
    - ... building a [Dockerised service](woodpecker/service/), I want to...
        - ... [build and push](woodpecker/service/build-and-push.woodpecker.yml)
        - ... [build and push (tagged)](woodpecker/service/build-and-push-tag.woodpecker.yml)
        - ... [dry run](woodpecker/service/dry-run.woodpecker.yml)
    - ... for a [Python](woodpecker/python/) project, I want to ...
        - ... [publish a package to pypi](woodpecker/python/pypi-publish.yml)
        - ... [run my project & commit the changes](woodpecker/python/run-and-commit.yml)

- On [Drone](drone/)...
    - ... using [Ember](drone/ember/), I want to...
        - ... [run tests](drone/ember/.drone.yml)
        - ... [build dry run](drone/ember/.drone.yml)
        - ... [push the latest build](drone/ember/.drone.yml)
        - ... [push the tagged build](drone/ember/.drone.yml)
    - ... building a [Dockerised service](woodpecker/service/), I want to...
        - ... [build and push](drone/service/.drone.yml)
        - ... [build and push (tagged)](drone/service/.drone.yml)
        - ... [dry run](drone/service/.drone.yml)



## Discussions
### Navigation order
While seemingly random, there is a logic behind it!

#### Folder structure
- The structure is as follows: `{platform}/{language/toolkit}/{action}`
- An example would be `{woodpecker,drone}/{ember,service}/{test,build}.yml`.

#### Woodpecker above Drone
Due to a slow shift towards the open source Woodpecker as opposed to the proprietary Drone, Woodpecker has been moved upwards in the navigation

#### Actions are not alphabetically ordered
The navigation is ordered as to what would commonly happen first. Testing is put above building, building above releasing, etc.

### Drone actions all navigate towards one file
Drone does not natively support splitting pipelines into different files. So the navigation all goes to one file. Sorry about that.

