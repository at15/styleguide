# Style Guide

A style guide for my side projects.

## TODO

- [ ] links to language specific style guide
- [ ] merge go style guide from go-learning and dyweb/gommon

## GitHub

- try to use one word as project name

TBD

- use `UpperCase` for project name?

## Workflow

TODO: this part has changed a lot w/ the new milestone and components based approach, e.g. no longer use issue

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

Examples: [benchhub](https://github.com/benchhub/benchhub)

- `doc`
  - `CHANGELOG.md`
  - `ROADMAP.md`
  - `design`
    - `README.md` link to all design doc that cross multiple components
    - `schema.md` e.g. database schema
  - `components`
    - `comp-1`
      - `README.md` link to log and milestones, and high level design?
      - `feature-a.md` big feature on that component that worth a dedicated note
    - `README.md` tree to all components
  - `milestones`
    - `v0.0.1-small-feature-a-of-medium-feature-1`
      - `README.md` break up features, components and implementation order
      - `comp-1.md` component notes specific to this milestone
    - `v0.1.0-medium-feature-1`
    - `v1.0.0-a-major-release-that-i-will-never-reach`
    - `README.md` tree to all milestones
  - `log`
    - `2020-02-03.md` diary with nothing special
    - `2020-02-04-design-schema.md` special events should show up in file name
- `hack`
  - `Dockerfile`
- `Makefile`
- `README.md`

## Documentation

TODO: this part has changed a lot w/ the new milestone and components based approach

### Roadmap

For upcoming, order by release number ASC, so recent development is on the top.
For finished, order by release number DESC. It may not be same as release note so keep it in Roadmap.

```
## Upcoming

### v0.0.3

- improve compression

### v0.0.4

- add new index schema

## Finished

## v0.0.2

- fix bugs

## v0.0.1

- introduced a new bug
```

### Changelog

Order by release number DESC, so recent release is on the op

```
## v0.0.2

- fix bugs

## v0.0.1

- introduced a new bug
```