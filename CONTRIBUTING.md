---
type: Contribution Guide
title: Brainquiver Contribution Guide
description: How to propose a change to a Brainquiver repository, who decides on it, and what a change must meet.
status: stable
tags: [contributing, community]
generated:
  by: human:ciprian-florin_ifrim
  at: 2026-10-01T12:35:31Z
edited:
  by: claude-code/opus-5.5
  at: 2026-10-01T16:47:40Z
---

# Brainquiver Contribution Guide

Every public Brainquiver repository takes contributions through GitHub, as an issue or a pull request. This guide applies to all of them, and each repository's README adds its own build, tests and rules. Every participant follows the [code of conduct](https://github.com/brainquiver/.github/blob/main/CODE_OF_CONDUCT.md). A contribution is licensed under the repository's license.

## 1. Roles

Ciprian-Florin Ifrim, [@CiprianFlorin-Ifrim](https://github.com/CiprianFlorin-Ifrim), maintains every repository. The maintainer reviews and merges each pull request, answers issues and vulnerability reports, enforces the code of conduct, and publishes releases. A contributor is anybody who opens an issue or a pull request. The admin account `eng-bq` belongs to the organization, so Brainquiver can merge, triage and release if the maintainer cannot.

## 2. Decisions

The maintainer decides on each change in its pull request. The discussion of a change stays in its pull request or its issue, where everybody can read it. A question or an idea about one repository goes to that repository's Discussions, and a general one goes to the organization's [Discussions](https://github.com/orgs/brainquiver/discussions). A repository without Discussions of its own uses the organization's. A large change starts as an issue, so its direction is agreed before the code exists. A pull request that the maintainer declines is closed with the reason in its thread.

## 3. Change Process

A change reaches `main` in four steps.

1. Open an issue for a bug or a large change. A small fix can start as a pull request.
2. Fork the repository, and make a branch named `<type>/<two to five words>`, such as `fix/stable-answer-order`.
3. Make the change, and run the checks that the repository's README names.
4. Open a pull request against `main`, with the reason for the change in its first paragraph.

The maintainer merges a pull request by squash once its checks pass, so each change becomes one commit on `main`.

## 4. Change Requirements

Each rule states what a change must meet, and its reason states what goes wrong otherwise.

| Rule | Reason |
| --- | --- |
| **Write each commit subject as `type(scope): what applies`, in the imperative and in 72 characters at most.** | A subject such as `fix(attachments): refuse a path outside the root` says what the change does before anybody opens the diff. |
| **Give each bug fix a test that fails on the old code.** | Only a failure on the old code proves that the fix changed something. |
| **Add tests for each new feature in the same pull request.** | A test catches the next change that breaks the feature. |
| **Match the style of the code around the change, and pass the formatter and the linter that the README names.** | With one style, a diff shows only the change. |
| **Keep each pull request to one change.** | A squash merge makes each pull request one commit. |

The types are `feat`, `fix`, `perf`, `refactor`, `docs`, `test`, `build`, `ci`, `style` and `revert`.

## 5. Vulnerability Reports

A vulnerability goes to the maintainer privately, through the Report a vulnerability form in the Security tab of the affected repository. The form opens a private advisory, where the maintainer answers. A public issue would show the fault to everyone before a fix exists. Some repositories add their own security policy, with what the code protects and how a report is handled.
