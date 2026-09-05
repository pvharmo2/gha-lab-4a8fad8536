> **Automated research artifact — not the upstream project.**
>
> This repository is a disposable lab built by an automated harness for a
> master's thesis at Université Laval on reproducing published GitHub Actions
> workflow vulnerabilities. It is a verbatim snapshot of
> [`dbt-labs/actions`](https://github.com/dbt-labs/actions) at commit
> `ed19ee39fd410f9ebc3ef202a8c80879a3328697` (2026-04-01), redistributed under that
> project's own licence, whose file is included unchanged in this snapshot.
>
> The upstream project is **not** involved, is never targeted, and the
> vulnerability studied here is already public. Every secret and variable in
> this repository is a randomly generated dummy value — no real credential is
> present. Action references and runner images are pinned to what they resolved
> to on 2026-04-01; see `pinning.md` in the harness output for
> every change made to the snapshot.
>
> Questions or objections: jonathan@sports-lamitis.com

---

## Understanding actions

A set of GitHub [Actions](https://docs.github.com/en/actions/creating-actions/about-custom-actions) and [Reusable Workflows](https://docs.github.com/en/actions/using-workflows/reusing-workflows) for automating common tasks related to developing, maintaining, and testing dbt-core, database adapter plugins, and other dbt-labs open source projects. 

## Getting started

Actions and workflows should be self documented.  See individual actions for more info and instructions on how to use.

### Actions

- [Parse Semver Action](parse-semver)
- [Python Package Info Action](py-package-info)
- [Fetch Repository Branches](fetch-repo-branches)
- [Fetch Container Tags](fetch-container-tags)

### Workflows

- Changelog Handling
    - [Changelog Existence Check](.github/workflows/changelog-existence.yml)
- Scheduled Installation Tests
    - [Installation Tests](.github/workflows/test-dbt-installation-main.yml)
        - .github/workflows/test-dbt-installation-docker.yml
        - .github/workflows/test-dbt-installation-homebrew.yml
        - .github/workflows/test-dbt-installation-notify-job-statuses.yml
        - .github/workflows/test-dbt-installation-pip.yml
        - .github/workflows/test-dbt-installation-source.yml
    - [Release Branch Tests](.github/workflows/release-branch-tests.yml)
- Generic Shared Workflows
    - [Label Swapping](.github/workflows/swap-labels.yml)
    - [Open Issue in Another repo](.github/workflows/open-issue-in-repo.yml)
    - [Scheduled Repository Cleanup After Releases](.github/workflows/repository-cleanup.yml)
    - [Stale Bot Matrix](.github/workflows/stale-bot-matrix.yml)

- Jira Issue Syncing - used by dbt-metrics
    - .github/workflows/core-triage.yml
    - .github/workflows/jira-creation-actions.yml
    - .github/workflows/jira-creation.yml
    - .github/workflows/jira-label-actions.yml
    - .github/workflows/jira-label.yml
    - .github/workflows/jira-transition-actions.yml
    - .github/workflows/jira-transition.yml

## Reporting bugs and contributing code

- Want to report a bug or request a feature? Let us know and open [an issue](https://github.com/dbt-labs/actions/issues/new)
- Want to help us build oss actions? Check out the [Contributing Guide](https://github.com/dbt-labs/actions/blob/HEAD/CONTRIBUTING.md)

## Code of Conduct

Everyone interacting in the project's codebases, issue trackers, chat rooms, and mailing lists is expected to follow the [dbt Code of Conduct](https://community.getdbt.com/code-of-conduct).

