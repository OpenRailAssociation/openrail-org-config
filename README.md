# OpenRail GitHub Organisation Configuration

[![Synchronise organization settings](https://github.com/OpenRailAssociation/openrail-org-config/actions/workflows/sync.yaml/badge.svg)](https://github.com/OpenRailAssociation/openrail-org-config/actions/workflows/sync.yaml)

Configuration of members, teams, repository permissions, and more.

These settings are automatically synchronised using [github-org-manager](https://github.com/OpenRailAssociation/github-org-manager).

## Making changes

Maintainers of OpenRail Association projects can request changes to their teams' and repositories' permissions. Please create a pull request in order to do so.

Requirements:
* For each OpenRail project, a separate file under [`teams`](./teams/) shall be present, so please do not add your teams in another file.
* Make sure that any team name is unique by prepending your project name. For example, if your project goes by the name "Fantasy Open Source Railway Improver", the file could be called `fosri.yaml`, and a team name could be `FOSRI-Maintainers`.

After the changes have been approved and merged, the changes will be executed via GitHub actions which takes ~2 minutes.

## License

The content of this repository is licensed under the [Apache 2.0 license](https://www.apache.org/licenses/LICENSE-2.0).
