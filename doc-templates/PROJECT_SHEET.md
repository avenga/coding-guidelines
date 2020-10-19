# Project Sheet - [Project Name]

## General Information

|                       |                             |                             |                             |
| --------------------- | --------------------------- | --------------------------- | --------------------------- |
| **Client**            | [client name]               | **Project Manager**         | [project manager name]      |
| **Tech Lead**         | [tech lead name]            | **Status**                  | [status]                    |
| **Planned Lifecycle** | [lifecycle name and Date 1] | [lifecycle name and Date 2] | [lifecycle name and Date 3] |

## URLs & Credentials

|                     |                                               |
| ------------------- | --------------------------------------------- |
| **Development**     | [link to web URL of development environment]  |
| **Repository**      | [link to git repo]                            |
| **Product backlog** | [link to web URL of product backlog]          |
| **Readme**          | [link to README.md]                           |
| **Changelog**       | [link to CHANGELOG.md]                        |
| **Code Style**      | <https://github.com/avenga/coding-guidelines> |

## Languages

- TypeScript
- JavaScript
- Bash
- SCSS

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

Coverage summary is tracked in each build on GitLab ([link]).

## Manual testing

Link to test scenarios: [link]

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

## External integrations

List of external integrations:

| Integration | Notes                                                |
| ----------- | ---------------------------------------------------- |
| GTM         | Acount name and infromation about administrator name |

## API documentation

Link to Swagger: [swagger]

## Actors/User roles

| Actor         | Role   | Description          | Contact information |
| ------------- | ------ | -------------------- | ------------------- |
| **Avenga**    |
| Administrator | Admin  | Setup new users etc. | user@example.com    |
| Editor        | Editor | Adding content       | user@example.com    |
| Visitor       | none   | Visiting website     | user@example.com    |
| **Client**    |
| Administrator | Admin  | Setup new users etc. | user@example.com    |
| Editor        | Editor | Adding content       | user@example.com    |
| Visitor       | none   | Visiting website     | user@example.com    |
