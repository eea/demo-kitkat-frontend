# EEA KitKat Demo Frontend
[![Release](https://img.shields.io/github/v/release/eea/demo-kitkat-frontend?sort=semver)](https://github.com/eea/demo-kitkat-frontend/releases)
[![Pipeline](https://ci.eionet.europa.eu/buildStatus/icon?job=volto/demo-kitkat-frontend/master&subject=master)](https://ci.eionet.europa.eu/view/Github/job/volto/job/demo-kitkat-frontend/job/master/display/redirect)
[![Pipeline develop](https://ci.eionet.europa.eu/buildStatus/icon?job=volto%2Fdemo-kitkat-frontend%2Fdevelop&subject=develop)](https://ci.eionet.europa.eu/view/Github/job/volto/job/demo-kitkat-frontend/job/develop/lastBuild/display/redirect)
[![Release pipeline](https://ci.eionet.europa.eu/buildStatus/icon?job=volto%2Fdemo-kitkat-frontend%2F1.0.0-alpha.1&build=last&subject=release%20v1.0.0-alpha.1%20pipeline)](https://ci.eionet.europa.eu/view/Github/job/volto/job/demo-kitkat-frontend/job/1.0.0-alpha.1/lastBuild/display/redirect/)

Demo Volto Frontend for included add-ons in [volto-eea-kitkat](https://github.com/eea/volto-eea-kitkat) bundle.

## Documentation

A training on how to create your own website using Volto is available as part of the Plone training at [https://training.plone.org/5/volto/index.html](https://training.plone.org/5/volto/index.html).


## Getting started

1. Install `nvm`

        touch ~/.bash_profile
        curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.34.0/install.sh | bash

        source ~/.bash_profile
        nvm version

1. Install latest `NodeJS 16.x`:

        nvm install 16
        nvm use 16
        node -v
        v16.16.2

1. Install `yarn`

        curl -o- -L https://yarnpkg.com/install.sh | bash
        yarn -v

1. Clone:

        git clone https://github.com/eea/demo-kitkat-frontend.git
        cd demo-kitkat-frontend

1. Install

        yarn
        yarn build

1. Start backend

        docker-compose up -d
        docker-compose logs -f

1. Start frontend

        yarn start:prod

1. See application at http://localhost:3000


## Automated @eeacms dependencies upgrades

All the addon dependencies that are located in the dependencies section of `package.json` file that belong to @eeacms and have a `MAJOR.MINOR.PATCH` version are automatically upgraded on the release of a new version of the addon. This upgrade is done directly on the `develop` branch.

Exceptions from automated upgrades ( see https://docs.npmjs.com/cli/v8/configuring-npm/package-json#dependencies for dependency configuration examples ) :
* All github or local paths
* Any version intervals ( `^version` or `>version` or `MAJOR.MINOR.x` etc )


## Release

See [RELEASE.md](https://github.com/eea/ims-frontend/tree/master/RELEASE.md)


## Production

We use [Docker](https://www.docker.com/), [Rancher](https://rancher.com/) and [Jenkins](https://jenkins.io/) to deploy this application in production.


### Deploy

* Within `Rancher > Catalog > EEA`


### Upgrade

* Within your Rancher environment click on the `Upgrade available` yellow button next to your stack.

* Confirm the upgrade

* Or roll-back if something went wrong and abort the upgrade procedure.


## Copyright and license

The Initial Owner of the Original Code is European Environment Agency (EEA).
All Rights Reserved.

See [LICENSE.md](https://github.com/eea/demo-kitkat-frontend/blob/master/LICENSE.md) for details.


## Funding

[European Environment Agency (EU)](http://eea.europa.eu)
