# Changelog

All notable changes to this project will be documented in this file.

This project adheres to [Semantic Versioning](https://semver.org/).

## 2.0.0 (2024-08-27)

### Changes

#### Feature
feat: return 'true' when all Rules pass and return 'false' if any Rule failes

#### Fix
- properly evaluate whether the Sem Ver was found inside a Markdown Header
- return 'false' in case the CHANGELOG file is not found in local checkout (do not crash Job)
- properly do multi-line search in CHANGELOG.md, with regex
- properly write Main branch ref name on CI console

#### Refactor
- add better name for Action Test Workflow and improve input description

#### Test
- add Test Case where the Sem Ver must be found through Pattern
- fix Test Case in which we expect Action to return 'true'
- add Github Workflow as Automated Test Cases for Scenarios when Action returns 'false'

#### CI
- setup Automated QA, PR Merge, Tagging, and Clean Up
- allow CI to pass, by allow Quality Gate to pass when docs are skipped
- redesign CI/CD Pipeline with Automated Deploment requiring both sets of Test Scenarios to pass
- add Reusable Workflow to delegate Signal for Automated Deployment (CD)


## 0.1.0 (2024-08-25)

This is the **first** ever release of the **Action Changelog CI** Open-Source Project.
- The project is hosted in a public repository on GitHub at [https://github.com/boromir674/action-changelog-ci](https://github.com/boromir674/action-changelog-ci)

### Initial Sources

- **Documentation Website**, writen in `markdown`
  - Build Process with `mkdocs`

- **CI/CD Pipeline** running on GitHub Actions at [https://github.com/boromir674/action-changelog-ci/actions](https://github.com/boromir674/action-changelog-ci/actions)
  - **CI**
    - `Test Docs` **Workflow**
  - **CD**
    - `Github Release` **Workflow**

