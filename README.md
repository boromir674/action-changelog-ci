# CHANGELOG CI

> Github Action for `CHANGELOG` **Continuous Integration**

```mermaid
flowchart LR

REF_EXISTS?{Input Ref Exists?}
REF_EXISTS? --YES --> EXIST?

REF_EXISTS? --NO --> FAIL_N_EXIT(("Exit Step with failure"))

EXIST?{"File Exists?"}

EXIST? --YES --> CH
EXIST? --NO --> RET_FALSE

CH{"Has changed since `main`?"}

CH --YES --> PAT
CH --NO --> RET_FALSE

PAT{"Has markdown Section
matching Pattern?"}

PAT --YES --> RET_TRUE
PAT --NO --> RET_FALSE

RET_TRUE(("Return `true`"))
RET_FALSE(("Return `false`"))

```

## Features

1. Check whether your CHANGELOG was changed since `main` branch
2. Check if a new `Markdown Section` was added
3. Check if **Section Header** includes `Sem Ver` (see [Semantic Versioning](https://semver.org/))
4. If `version` supplied, check if **Section Header** includes that specific Semantic Version

## Get started

## Use Cases

Implementing a CI check for your `CHANGELOG.md`, during your release process.
