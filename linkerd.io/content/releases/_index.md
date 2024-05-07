+++
title = "Releases"
aliases = [ "edge" ]
weight = 18
+++

Releases and packages of Linkerd are available in several different forms.

## Stable releases

Stable release artifacts of Linkerd follow semantic versioning, with version
numbers of the form `2.major.minor` (in other words, `2` is a static prefix,
followed by the major version, then the minor). Changes in major version
denote large feature additions and possible breaking changes; changes in minor
versions denote safe upgrades without breaking changes.

As of February 2024, the the vendor community around Linkerd is responsible
for supported, stable release artifacts, with the Linkerd project itself only
producing edge release artifacts. Please read the [Linkerd 2.15.0
announcement](/2024/02/21/announcing-linkerd-2.15/#a-new-model-for-stable-releases)
for more details.

Known distributions of Linkerd with stable release artifacts include:

- [Buoyant Enterprise for Linkerd](https://docs.buoyant.io/buoyant-enterprise-linkerd)
  from Buoyant, creators of Linkerd.
  Latest version: **enterprise-2.15.2**
  [[release notes](https://docs.buoyant.io/release-notes/buoyant-enterprise-linkerd/enterprise-2.15.2/)].

## Edge releases

Edge release artifacts are published on a weekly or near-weekly basis as part
of the open source project. The full list of edge release artifacts can be
found on [the Linkerd GitHub releases
page](https://github.com/linkerd/linkerd2/releases).

Edge release artifacts contain the code in from the `main` branch at the point
in time when they were cut. Since all Linkerd development happens on `main` -
meaning that all changes land on the `main` branch, whether security patches,
features, bugfixes, or whatever else - this means they always have the latest
features and fixes, and have undergone automated testing as well as maintainer
code review. Edge releases may involve partial features that are later
modified or backed out. They may also involve breaking changes—of course, we
do our best to avoid this.

Edge release versioning follows the form `edge-y.m.n`, where `y` is the last two
digits of the year, `m` is the numeric month, and `n` is numeric edge release
count for that month. For example:

- `edge-23.9.1`: the first edge release shipped in September 2023
- `edge-24.1.3`: the third edge release shipped in January 2024

Using edge release artifacts and [reporting
bugs](https://github.com/linkerd/linkerd2/issues/new/choose) helps us ensure a rapid
pace of development and is a great way to help Linkerd.

### Edge Release Guidance

While we strive to always provide production-ready artifacts, we also publish
guidance for each edge release as part of its release notes, reflecting the
latest experience from the field. **This guidance can change over time**: as
we get new feedback from the field about a particular release, we will update
its guidance.

Release notes show an `Overall Status`, `Cautions`, and `Changes`.

#### Overall Status

The `Overall Status` will be one of the following:

[badge-recommended]: https://img.shields.io/badge/release_status-RECOMMENDED-lightgreen?logo=Linkerd
[badge-not-recommended]: https://img.shields.io/badge/release_status-NOT_RECOMMENDED-red?logo=Linkerd

![RECOMMENDED][badge-recommended]

**RECOMMENDED**: This release should be fine for general use. Note that a
Recommended release may still describe `Cautions`: if any are listed, read
them carefully to make sure they won't affect you.

![NOT RECOMMENDED][badge-not-recommended]

**NOT RECOMMENDED**: This release may work in some cases, but in general it is
not a good candidate for general use; the `Cautions` should explain why. Any
release marked with **NOT RECOMMENDED** will also recommend a release to
consider instead.

#### `Cautions`

The `Cautions` section will list any particular things that warrant special
attention before installing the release. In many cases, no `Cautions` will be
listed.

#### `Changes`

The `Changes` section will start with a short summary of significant changes,
then continue with the full changelog for the release. You should **always**
read at least the summary section before installing a release.

<!-- markdownlint-disable MD034 -->

Latest version: **{{% latestedge %}}** [[release
notes](https://github.com/linkerd/linkerd2/releases/tag/{{% latestedge %}})].
