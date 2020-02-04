# Style Guide

A style guide for my side projects.

## GitHub



## Workflow

### Design

- create a issue with title `[design][component-name] XXX`
  - put it into the component's project
- create file under `doc/design`, update `doc/design/README.md`.
- update `doc/roadmap.md` to add todo items and re order existing timeline.

### Implementation

- find it from roadmap
- create a issue with title `[impl][component-name] XXX`
  - put it into the component's project
  - assign a milestone (release number)
- create a new branch `component-name/feature-name/status` e.g. `gobench/parse/init`
- keep track of progress in `doc/log`
- update `doc/roadmap.md`

### Release

- move unfinished work in this release to next release in `doc/roadmap`

## Directory layout

- doc
  - changelog.md
  - roadmap.md
  - design
    - README.md link to all the docs
    - schema.md e.g. database schema
  - log
    - 2020-02
      - 2020-02-03.md diary with nothing special
      - 2020-02-04-design-schema.md special events should show up in file name
- hack
  - Dockerfile
- Makefile
- README.md