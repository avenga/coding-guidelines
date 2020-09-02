# Project Sheet - [Project Name]

## General Information

|                       |                                                    |                              |                             |
| --------------------- | -------------------------------------------------- | ---------------------------- | --------------------------- |
| __Client__            | [client name]                                      | __Project Manager__          | [project manager name]      |
| __Tech Lead__         | [tech lead name]                                   | __Status__                   | [status]                    |
| __Planned Lifecycle__ | [lifecycle name and Date 1]                        | [lifecycle name and Date 2]  | [lifecycle name and Date 3] |

## URLs & Credentials

|                 |                                                                                        |
| --------------- | -------------------------------------------------------------------------------------- |
| __Development__ | [link to web URL of development environment] |
| __Repository__  | [link to git repo] |
| __Readme__      | [link to README.md] |
| __Code Style__  | <https://github.com/avenga/coding-guidelines> |

## Languages

* TypeScript
* JavaScript
* Bash
* SCSS

## Technologies

_Note_: Most technologies are tracked in `package.json` files and will not be duplicated here to minimize chores.

| Software       | Version   | Notes         |
| -------------- | --------- | ------------- |
| git-crypt      | >=0.6.0   | backend & etl |
| Docker         | >=v19     | backend & etl |
| docker-compose | >=1.25.5  | backend & etl |
| Bash           | >=v4      | ops           |
| tar            | >=1.32    | ops           |
| jq             | >=1.6     | ops           |
| kubectl        | >=v1.18.3 | ops           |

## Testing

| Software     | Version             | Notes         |
| ------------ | ------------------- | ------------- |
| Mocha + Chai | see `package.json`s | backend & etl |
| nyc          | see `package.json`s | backend & etl |
| Jest         | see `package.json`  | frontend      |

Coverage summary is tracked in each build on GitLab.

## Logging/Monitoring

| Software | Version            | Notes   |
| -------- | ------------------ | ------- |
| winston  | see `package.json` | backend |

## CI/CD/Hosting

The client hosts on-premise using VMs.

| Service/Tool   | Notes                                                                                         |
| -------------- | --------------------------------------------------------------------------------------------- |
| Avenga Hosting | for development only                                                                          |
| CI             | Compile check, linting, tests on GitLab for MRs and pushes to `master` by GitLab CI           |
| CD             | `master` commits can be triggered manually to be deployed to the dev environment by GitLab CI |
