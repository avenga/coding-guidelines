#### How to use this template

This document should be used to provide information about how to build the
software it is included with.
Given examples should be replaced and this document should be maintained
whenever changes to any mentioned processes are made or new ones are added.

### Language

English

### Format

- Markdown
- max. line length of ~120 characters

### Structure

- Remove the segment "How to use this template" when done.
- The title of the project should be changed and one paragraph of introductory text should be added.
- Any categories marked as optional can be left out if they are unnecessary.
- Otherwise don't change the structure and order of this document.

---

# Project title

One Paragraph of project description goes here.

## Environments

List of available environments that this project could be deployed to.
Provide as much information as possible (URLs, Host, etc.).

- [staging](https://staging.example.com)
  - Basic-Auth: Link to credentials (syspass etc.)
  - Host: https://hosting-plattform/
- [production](https://www.example.com)
  - Host: https://hosting-plattform/

## Requirements

### Services

List of used Services (DBs, external Services, Platforms, etc.).

- MySQL 5.7
- [SendGrid](https://app.sendgrid.com/)
  - Credentials: Link to credentials (...)

### CI Pipeline

Explain the continuous integration process.

- [CI](https://link-to-ci-pipeline.com)
  - merge in `master` will deploy to `staging` environment

### Tools

List of required tools. Tools that are dependend on others should be indented
by one step under their dependency.
If specific versions are required, those should be appended as `@{version}`.

- node@9.10.1
  - npm
- docker
  - docker-compose

### OS (optional)

List of available operating systems if there are any limits.

## Tasks

List tasks that can be used to facilitate a successful build. Include any
available parameters, such as environment variables or command line arguments.

- Provide descriptive parameter names: `-p {port}`
- Mark environment variables using all caps: `NODE_ENV={env}`
- Specify default values for parameters: `-p {port} [80]`
- List possible values in parentheses: `NODE_ENV={env} (develop|production)`
- Add description or clarification: `-p {port}` &mdash; HTTP port
- Mark optional parameters as such: `-p` &mdash; _(optional)_ &ndash; HTTP port
- Do not use a name for boolean parameters: `--production`

---

- `yarn build`
  - `-p {port}` &mdash; HTTP port of the application
  - `--verbose` &mdash; _(optional)_ &ndash; Enable lowest log level
  - `NODE_ENV={env} (develop|production) [develop]` &mdash; _(optional)_ &ndash;
    Build environment used to pick config file

### Build

Any tasks used to build the software.
