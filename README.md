# OpenRail GitHub Organisation Configuration

[![Synchronise organization settings](https://github.com/OpenRailAssociation/openrail-org-config/actions/workflows/sync.yaml/badge.svg)](https://github.com/OpenRailAssociation/openrail-org-config/actions/workflows/sync.yaml)

Configuration of members, teams, repository permissions, and more.

These settings are automatically synchronised using [github-org-manager](https://github.com/OpenRailAssociation/github-org-manager).

## Making changes

Maintainers of OpenRail Association projects can request changes to their teams' and repositories' permissions. Please create a pull request in order to do so.

After the changes have been approved and merged, the changes will be executed via GitHub actions which takes ~2 minutes.

## Conventions

### File naming

Each team file under [`teams/`](./teams/) uses a prefix indicating the type of team:

| Prefix | Purpose | Example |
|---|---|---|
| `project-` | OpenRail incubation projects | `project-osrd.yaml` |
| `wg-` | Working groups | `wg-project-scouting.yaml` |
| `org-` | Organizational teams (OpenRail Team, TC, admin projects, meetup) | `org-technical-committee.yaml` |
| `external-` | External collaborations | `external-hack4rail.yaml` |

Each project or group gets exactly one file. Do not add your teams in another file.

### Team naming

* Team names are human-readable text with proper capitalization and spaces: `NGE Maintainers`, not `NGE-Admins` or `nge-maintainers`.
* Prepend your project name to keep names unique: `DAC Migration DSS Maintainers`, `Liblrs Maintainers`.
* Use "Maintainers" (not "Admins") for the elevated-permissions sub-team.

### Descriptions

Every team must have a `description` field. Use one of these patterns:

* Base team: "Members of the X project" / "Members of the X Working Group"
* Maintainer sub-team: "Maintainers of the X project" / "Maintainers of the X repository"
* Special-purpose teams: descriptive phrase ("Organizers of the Hack4Rail event", "Moderators of the Technical Committee retrospectives")

No leading "The" in descriptions.

### Team structure

* A project's base team gets `push` permission on its repos.
* A "Maintainers" sub-team (with `parent` set to the base team) gets `admin` permission for people who need to manage repo settings, branch protection, etc.
* Do not add individual user permissions to repositories. Use teams only.
* All organization members must belong to at least one team.

## License

The content of this repository is licensed under the [Apache 2.0 license](https://www.apache.org/licenses/LICENSE-2.0).
