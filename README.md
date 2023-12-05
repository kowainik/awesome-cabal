# Awesome Cabal

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

***A curated list of awesome resources for the Haskell Cabal build tool.***

Cabal — **C**ommon **A**rchitecture for **B**uilding **A**pplications and
**L**ibraries — is the tool to build and maintain
[Haskell](https://www.haskell.org/) packages.

## Table of Contents

 * [Resources](#resources)
 * [Installation](#installation)
 * [Introduction](#introduction)
 * [Scaffolding](#scaffolding)
 * [Cabal Configuration Format](#cabal-configuration-format)
 * [Components](#components)
 * [Backpack](#backpack)
 * [PVP](#pvp)
 * [Cabal Assistants](#cabal-assistants)
 * [CI](#ci)
 * [Integration](#integration)
 * [Custom Setup](#custom-setup)
 * [OS Manifests](#os-manifests)
 * [IDE](#ide)
 * [Cross Compilation](#cross-compilation)
 * [Cabal for Development](#cabal-for-development)
 * [Cabal in GSoC](#cabal-in-gsoc)
 * [History](#history)
 * [Community](#community)

## Resources

 * [Official website](https://www.haskell.org/cabal/)
 * [Official documentation](https://www.haskell.org/cabal/users-guide/)
 * [`haskell/cabal`](https://github.com/haskell/cabal): Official GitHub source
   repository.

## Installation

*There are various means of installing `Cabal`. Depending on your operating
system and prefered method, you can choose a suitable way to do that.*

 * [`ghcup`](https://www.haskell.org/ghcup/):
   Haskell toolchain installer for **Linux** and **macOS**.
   Use `ghcup install-cabal` command to install Cabal. Refer to the
   [documentation](https://gitlab.haskell.org/haskell/ghcup-hs) for more details.
 * [HVR ppa](https://launchpad.net/~hvr/+archive/ubuntu/ghc):
   PPA for **Ubuntu** that includes releases of `Cabal`.
 * [Windows setup](https://hub.zhox.com/posts/introducing-haskell-dev/):
   The easiest way to setup a Haskell environment on **Windows** using
   [Chocolatey](https://chocolatey.org/).
 * [Download binary](https://www.haskell.org/cabal/download.html):
   Install `Cabal` on **all** operating systems from sources or by downloading
   the binary.
 * [`CabalChoco`](https://github.com/Mistuke/CabalChoco):
   Chocolatey sources for pure Cabal installs on **Windows**.
 * [Debian packages](https://downloads.haskell.org/debian/):
   Install packages built specifically for **Debian 9 (Stretch)**.
 * [macOS setup](https://haskell.futurice.com/):
   Python script to install `Cabal` on **macOS**.
 * [`ghcups`](https://github.com/kakkun61/ghcups):
   `ghcup` for PowerShell on **Windows**.

#### Blog posts

 * [Managing GHC versions with ghcup](https://qfpl.io/posts/multiple-ghcs-ghcup/):
   How to install different GHCs and Cabal.

## Introduction

*Write-ups and examples that could help to get into `Cabal` and start using it.*

 * [Getting started with Haskell and Cabal](https://cabal.readthedocs.io/en/latest/getting-started.html)
 * [Intoduction](https://www.haskell.org/cabal/users-guide/intro.html):
   Official documentation's introduction.
 * [Haskell build tools (by Kowainik)](https://kowainik.github.io/posts/2018-06-21-haskell-build-tools):
   Description of the basic workflows with the main Haskell build tools. You can
   go straight to the [Cabal section of the post](https://kowainik.github.io/posts/2018-06-21-haskell-build-tools#cabal).
 * [Introduction to Cabal (video)](https://haskell-at-work.com/episodes/2018-05-13-introduction-to-cabal.html):
   In this video Haskell at Work explores the basics of Cabal including the
   family of `new-` commands.
 * [Haskell Aliases](https://vrom911.github.io/blog/haskell-aliases):
   Shell aliases for Haskell build tools for higher productivity.
 * [Organizing Our Package](https://mmhaskell.com/blog/2020/1/6/organizing-our-package):
   Walk through the process of creating and managing a new Haskell project.
 * [Making the most of Cabal](https://lukelau.me/haskell/posts/making-the-most-of-cabal/):
   Showcase of different Cabal features.

## Scaffolding

 * [Quick start](https://www.haskell.org/cabal/users-guide/developing-packages.html#quickstart):
   Using `cabal init` command to create a project.
 * [`summoner`](https://hackage.haskell.org/package/summoner):
   CLI tool for scaffolding fully configured batteries-included production-level
   Haskell projects.
 * [`summoner-tui`](https://hackage.haskell.org/package/summoner-tui):
   TUI tool for scaffolding fully configured batteries-included production-level
   Haskell projects.
 * [`hi`](https://hackage.haskell.org/package/hi):
   Generate scaffold for cabal project.
 * [`example-cabal-project`](https://github.com/jkachmar/example-cabal-project):
   A simple example project using cabal-install, Nix, and direnv.

## `Cabal` Configuration Format

*`.cabal` files use a special format to specify package configurations.*

 * [Docs](https://www.haskell.org/cabal/users-guide/developing-packages.html#pkg-desc):
   Official documentation on the package description format.
 * [CHANGELOG](https://www.haskell.org/cabal/users-guide/file-format-changelog.html):
   Package description format specification history.
 * [Minimal cabal files](https://medium.com/@danidiaz/minimal-cabal-files-revisited-a5810215b0d9):
   Explanation of the minimal possible cabal configuration.
 * [`cabal-fmt`](https://hackage.haskell.org/package/cabal-fmt):
   CLI tool to format `.cabal` files.
 * ~~[`cabal-info`](https://hackage.haskell.org/package/cabal-info):
   Simple command-line interface to read and output information from the
   `.cabal` file.~~ (archived, Cabal-1.x only)

## Components

*Useful information on various Cabal components. These could be useful blog
posts on specific features, or description of handy parts of the Cabal
specification.*

 * [Common Stanzas](https://vrom911.github.io/blog/common-stanzas):
   Blog post about Cabal's common stanzas feature.
 * [Multiple Libraries](https://fgaz.me/posts/2019-11-14-cabal-multiple-libraries/):
   Blog post about Cabal's multiple libraries feature.
 * [Foreign libraries](https://qnikst.github.io/posts/2018-05-02-cabal-foreign-library.html):
   Blog post about Cabal's foreign libraries feature.
 * [Foreign libraries example](https://github.com/pdlla/haskell-ffi-cabal-foreign-library-examples):
   Example usage of foreign libraries.
 * [source-repository-package](https://cabal.readthedocs.io/en/latest/cabal-project.html#specifying-packages-from-remote-version-control-locations):
   Specifying packages from remote version control locations (e.g. how to use
   GitHub dependencies in the Cabal packages).
 * [cabal gen-bounds](https://medium.com/@danidiaz/cabal-gen-bounds-630f6de716d9):
   A command to generate lower and upper bounds for dependencies in the `.cabal`
   file.
 * [`cabal-bounds`](https://hackage.haskell.org/package/cabal-bounds):
   A command line program for managing the bounds/versions of the dependencies
   in a cabal file.
 * [`cabal-cargs`](https://hackage.haskell.org/package/cabal-cargs):
   A command line program for extracting compiler arguments from a cabal file.
 * [Mix-ins](https://twitter.com/ChShersh/status/1053205244438503429):
   Usage of the Cabal's `mixin` feature to replace default `Prelude`.

## Backpack

*__Backpack__ is a feature that allows implementing mix-in libraries in Haskell.
Mix-in libraries can have signatures which permit implementations of values and
types to be deferred, while allowing a library with missing implementations to
still be type-checked.*

### Official documentation

 * [Edward Z. Yang thesis](https://github.com/ezyang/thesis)
 * [GHC Wiki: Backpack](https://gitlab.haskell.org/ghc/ghc/wikis/backpack)
 * [GHC User Guide: Module Signature](https://downloads.haskell.org/ghc/latest/docs/html/users_guide/separate_compilation.html#module-signatures)
 * [Cabal user guide: `signatures` field](https://www.haskell.org/cabal/users-guide/developing-packages.html?highlight=backpack#pkg-field-library-signatures)
 * [Cabal user guide: `mixins` field](https://www.haskell.org/cabal/users-guide/developing-packages.html?highlight=backpack#pkg-field-mixins)

### Tutorials

 * [Edward Z. Yang blog](http://blog.ezyang.com/category/haskell/backpack/):
   Blog posts about Backpack implementation and usage from the Backpack author.
 * [Picnic: Put containers into backpack (by Kowainik)](https://kowainik.github.io/posts/2018-08-19-picnic-put-containers-into-a-backpack):
   This blog post walks the reader through the Backpack implementation of the
   uniform interface for containers (`Map`s and `Set`s).
 * [Really small Backpack example](https://github.com/danidiaz/really-small-backpack-example):
   A small tutorial on the very basics of the Backpack module system.

### Libraries

 * [`backpack-str`](https://github.com/haskell-backpack/backpack-str):
   Signatures for string types.
 * [`reflex-backpack`](https://github.com/ezyang/reflex-backpack):
   Backpack implementation of Reflex.
 * [`containers-backpack`](https://github.com/kowainik/containers-backpack):
   Signatures for various containers (e.g. `Map`, `HashMap`, etc.)
 * [`streamy`](https://github.com/danidiaz/streamy):
   Signatures for streaming libraries.
 * [`unpacked-containers`](https://hackage.haskell.org/package/unpacked-containers):
   Unpacked sets and maps exploiting Backpack's ability to unpack through
   signatures.

### Talks

 * [Backpack to Work (by Edward Z. Yang)](https://www.youtube.com/watch?v=A3ehG4GQpxU)
 * [Picnic: put containers into a Backpack (by Dmitrii Kovanikov)](https://www.youtube.com/watch?v=GLtp3Xy7Rps)

## PVP

*It is recommended for Haskell packages to follow PvP — Package versioning
Policy.*

 * [PVP](https://pvp.haskell.org/):
   Official Haskell documentation on versioning.
 * [`pvp`](https://github.com/haskell/pvp):
   The GitHub repository to create issues against.
 * [`policeman` (by Kowainik)](https://github.com/kowainik/policeman):
   Policeman assists to properly choose the next version number according
   to PVP (Packaging Version Policy) for the Haskell packages based on the
   semantical changes to the interface.
 * [`check-pvp`](https://hackage.haskell.org/package/check-pvp):
   Check whether module and package imports conform to the PVP.

## Cabal Assistants

*CLI tools that provide additional interface to `cabal-install`.*

 * [`cabal-install`](https://hackage.haskell.org/package/cabal-install):
   The command-line interface for Cabal and Hackage.
 * [`vabal`](https://hackage.haskell.org/package/vabal):
   The cabal companion that leverages Cabal's capabilities of working with
   different GHC versions.
 * [`hkgr`](https://hackage.haskell.org/package/hkgr):
   Tool to help make new releases of Haskell packages, with commands for git
   tagging, pristine sdist, and uploading to Hackage.
 * [`releaser`](https://github.com/domenkozar/releaser):
   Automation of Haskell package release process.
 * [`iridium`](https://hackage.haskell.org/package/iridium):
   This tool aims to automate several typical steps when uploading a new package
   version to Hackage.
 * [Haskell package QA](https://oleg.fi/gists/posts/2018-01-08-haskell-package-qa.html):
   New things in Haskell package QA.
 * [`cabal-plan`](https://hackage.haskell.org/package/cabal-plan):
   Library and utility for processing cabal's `plan.json` file.
 * [`cabal-extras`](https://github.com/phadej/cabal-extras):
   A tool suite to aid Haskell development using `cabal-install`.
 * [`cabal-helper`](https://hackage.haskell.org/package/cabal-helper):
   Give Haskell development tools access to the same environment which build
   tools such as Cabal normally provide to the compiler.
 * [`cabal-sort`](https://hackage.haskell.org/package/cabal-sort):
   Given a number of cabal package files, this program reads all those files and
   emits them topologically sorted according to their dependencies.
 * [`mafia`](https://github.com/haskell-mafia/mafia):
   Lightweight but opinionated wrapper around Cabal that makes working on
   Haskell projects fun and easy.
 * [`cabal-scripts`](https://hackage.haskell.org/package/cabal-scripts):
   Collection of Bash Shell scripts for support of Cabal package development.
 * [`cabalish`](https://hackage.haskell.org/package/cabalish):
   Provides access to the cabal file data for shell scripts.
 * [`cab`](https://hackage.haskell.org/package/cab):
   A MacPorts-like maintenance command of Haskell Cabal packages.
 * [`cabal-edit`](https://github.com/sdiehl/cabal-edit):
   A utility for managing Hackage dependencies from the command line.
 * [`cabal-clean`](https://github.com/andreasabel/cabal-clean):
   Removes compilation artefacts in dist-newstyle/build from older versions of
   the package or superseded minor versions of GHC.

### Dependencies analysers

 * [`cabalgraph`](https://hackage.haskell.org/package/cabalgraph):
   Generate pretty graphs of module trees from `.cabal` files.
 * [`cabal-progdeps`](https://hackage.haskell.org/package/cabal-progdeps):
   Show dependencies of program being built in current directory.
 * [`weeder`](https://github.com/ocharles/weeder):
   Tool for detecting redundant Cabal package dependencies that uses `.hie`
   files introduced in GHC-8.8.
 * [`packdeps`](https://hackage.haskell.org/package/packdeps):
   A library and command line tool for checking if the upper bounds in your
   Cabal package's dependency list excludes the newest package available.
 * [`jailbreak-cabal`](https://hackage.haskell.org/package/jailbreak-cabal):
   Strip version restrictions from build dependencies in the `.cabal` files.

## CI

*Information about how to set up Continious Integration on Haskell packages.*

#### Travis

 * [Dead simple Haskell Travis settings for cabal and stack](https://kodimensional.dev/posts/2019-02-25-haskell-travis):
   Blog post about Travis CI settings for Haskell projects with Cabal and Stack.
 * [`haskell-ci`](https://hackage.haskell.org/package/haskell-ci):
   Cabal package script generator for Travis CI.
 * [Testing with Travis](https://qfpl.io/posts/testing-with-travis/):
   Blog post about how to quickly and easily set up continuous integration for
   your open source Haskell projects hosted on GitHub.

#### AppVeyor

 * [Haskell & AppVeyor Chocolatey Introduction](https://hub.zhox.com/posts/chocolatey-introduction/):
   Stey-by-step description of building Haskel packages with Chocolatey and
   Cabal on AppVeyor CI.
 * [`appveyor.yml` example](https://github.com/kowainik/tomland/blob/main/appveyor.yml):
   Minimal working example of the `appveyor.yml` configuration file.

#### GitHub Actions

 * [Dead simple cross-platform GitHub Actions for Haskell](https://kodimensional.dev/github-actions):
   Blog post about cross-platform GitHub Actions CI settings for
   Haskell projects with Cabal and Stack.
 * [`haskell-ci`](https://hackage.haskell.org/package/haskell-ci):
   Cabal package script generator for GitHub Actions CI.
 * [`setup-haskell`](https://github.com/actions/setup-haskell):
   Set up your GitHub Actions workflow with a specific version of Haskell (GHC
   and Cabal).
 * [`actions/cache`](https://github.com/actions/cache/blob/main/examples.md#haskell---cabal):
   This action allows caching dependencies and build outputs to improve workflow
   execution time.
 * [`cabal-plan-bounds`](https://discourse.haskell.org/t/don-t-edit-dependency-bounds-manually-with-this-ci-setup/5539):
   Never write bounds manually, instead derive them from what CI is actually testing.

#### Circle CI

 * [Circle CI orbs](https://circleci.com/orbs/registry/orb/haskell-works/haskell-build-2):
   Haskell Orb that Builds a Haskell application using Cabal on Circle CI.

#### *Generic CI*

 * [`packcheck`](https://github.com/composewell/packcheck):
   Universal build and CI testing for Haskell packages. Can produce
   configurations for Travis, AppVeyor and Circle CI.
 * [`cabal-cache`](https://hackage.haskell.org/package/cabal-cache):
   Tool for caching built cabal new-build packages.
 * [`hw-ci-assist`](https://hackage.haskell.org/package/hw-ci-assist):
   CI Assistant for Haskell projects which implements package caching.

#### Docker

 * [`docker-ghc`](https://github.com/phadej/docker-ghc):
   GHC + Cabal docker image.
 * [`ghc-musl`](https://github.com/utdemir/ghc-musl):
   Docker image with GHC+musl and Cabal for static executables.
 * [Docker Haskell example](https://oleg.fi/gists/posts/2019-07-04-docker-haskell-example.html):
   Multi-stage docker build of Haskell webapp.

#### Deployment

 * [Heroku buildpack GHC](https://github.com/begriffs/heroku-buildpack-ghc):
   Buildpack for deploying Haskell apps to Heroku.
 * [Haskell on Heroku](http://web.archive.org/web/20150423211821/https://haskellonheroku.com/tutorial/):
   This tutorial shows how to develop a simple Haskell web app and deploy it to
   Heroku.

## Integration

*Cabal integration with other configuration languages and formats.*

 * [`dhall-to-cabal`](https://hackage.haskell.org/package/dhall-to-cabal):
   Compiles Dhall expressions to Cabal files.
 * [`cabal-to-dhall`](https://hackage.haskell.org/package/dhall-to-cabal):
   The opposite of `dhall-to-cabal`. Compiles Cabal to Dhall expressions.
 * [`cabal2nix`](https://hackage.haskell.org/package/cabal2nix):
   Convert Cabal files into Nix build instructions.
 * [`nix2cabal`](https://github.com/bef0/nix2cabal):
   The opposite of `cabal2nix`. It lets you define a Haskell package in Nix and
   generate a Cabal file using that definition.
 * [`cabal2bazel`](https://github.com/google/cabal2bazel):
   A tool to help with fetching Cabal packages from Hackage and importing them
   as packages into `cabal2bazel`.
 * [`cargo-cabal`](https://github.com/yvan-sraka/cargo-cabal):
   A tool that helps you to turn in one command a Rust crate into a Haskell Cabal library.
 * [`jenga`](https://hackage.haskell.org/package/jenga):
   Generate a `cabal.freeze` file from a `stack.yaml`.
 * [`stack2cabal`](https://hackage.haskell.org/package/stack2cabal):
   Convert stack projects to `cabal.project` + `cabal.project.freeze`.
 * [`shake-cabal`](https://hackage.haskell.org/package/shake-cabal):
   A library for using `shake` alongside Cabal.

## Custom Setup

*`Setup.hs` helpers to use in `custom-setup` stanzas with the `Custom` build
type.*

 * [Dependencies for Cabal Setup.hs and other goodies](http://www.well-typed.com/blog/2015/07/cabal-setup-deps/)
 * [`autopack`](https://github.com/kowainik/autopack) (by Kowainik): Automatically discovers Haskell modules and populates `exposed-modules`.
 * [`proto-lens-setup`](https://hackage.haskell.org/package/proto-lens-setup):
   Cabal support for codegen with `proto-lens`.
 * [`liquidhaskell-cabal`](https://hackage.haskell.org/package/liquidhaskell-cabal):
   Liquid Haskell integration for Cabal and Stack.
 * [`liquidhaskell-cabal-demo`](https://hackage.haskell.org/package/liquidhaskell-cabal-demo):
   Demo of Liquid Haskell integration for Cabal and Stack.
 * [`cabal-build-programs`](https://hackage.haskell.org/package/cabal-build-programs):
   Lets you use custom Cabal fields for executable dependencies.
 * [`chs-cabal`](https://hackage.haskell.org/package/chs-cabal):
   Cabal with c2hs dependencies.
 * [`ats-setup`](https://hackage.haskell.org/package/ats-setup):
   ATS scripts for Cabal builds.
 * [`asset-bundle`](https://hackage.haskell.org/package/asset-bundle):
   A build-time Cabal library that bundles executables with assets.
 * [`cabal-bundle-clib`](https://hackage.haskell.org/package/cabal-bundle-clib):
   Bundling C/C++ projects in Cabal package made easy.
 * [`cabal-toolkit`](https://hackage.haskell.org/package/cabal-toolkit):
   Helper functions for writing custom `Setup.hs` scripts.
 * [`quipper-cabal`](https://hackage.haskell.org/package/quipper-cabal):
   Some functions to aid in the creation of Cabal packages for Quipper.

## OS Manifests

*Tools to generate system packages meta information from Haskell packages.*

 * [`cabal-debian`](https://hackage.haskell.org/package/cabal-debian):
   Create a Debianization for a Cabal package.
 * [`cabal-flatpak`](https://hackage.haskell.org/package/cabal-flatpak):
   Generate a FlatPak manifest from a Cabal package description.
 * [`cabal-macosx`](https://hackage.haskell.org/package/cabal-macosx):
   Cabal support for creating Mac OSX application bundles.
 * [`cabal-rpm`](https://hackage.haskell.org/package/cabal-rpm):
   RPM packaging tool for Haskell Cabal-based packages.
 * [`cabal2spec`](https://hackage.haskell.org/package/cabal2spec):
   Convert Cabal files into rpm spec files.
 * [`cblrepo`](https://hackage.haskell.org/package/cblrepo):
   Tool to simplify managing a consistent set of Haskell packages for
   distributions.
 * [`exherbo-cabal`](https://hackage.haskell.org/package/exherbo-cabal):
   Generates package description from `.cabal` files in format of exheres-0
   for Exherbo Linux.
 * [`hackport`](https://hackage.haskell.org/package/hackport):
   A command line tool to manage an overlay of Gentoo ebuilds that are generated
   from a hackage repo of Cabal packages.

## IDE

*Helper tools for Cabal support in various Integrated Development Environments.*

 * [Haskell IDE Setup with cabal and nix](https://github.com/shivamashtikar/haskell-setup):
   Haskell setup for vscode with cabal and nix.
 * [`codex`](https://hackage.haskell.org/package/codex):
   A ctags file generator for Cabal project dependencies.
 * [`vim-cabal-indent`](https://github.com/h-youhei/vim-cabal-indent):
   `.cabal` files indentation plugin for Vim.
 * [`vim-syntax-haskell-cabal`](https://github.com/Twinside/vim-syntax-haskell-cabal):
   Cabal syntax highlighting plugin for Vim.

## Cross Compilation

 * [The Haskell Cabal and cross compilation](https://medium.com/@zw3rk/the-haskell-cabal-and-cross-compilation-e9885fd5e2f):
   Cross compiling packages with Cabal.

## Cabal for Development

*Haskell libraries to parse and work with files in the Cabal format.*

 * [`Cabal`](https://hackage.haskell.org/package/Cabal):
   Official library to parse and analyze `.cabal` files.
 * [`cabal-lenses`](https://hackage.haskell.org/package/cabal-lenses):
   Lenses and traversals for the `Cabal` library.
 * [`cabal-install-parsers`](https://hackage.haskell.org/package/cabal-install-parsers):
   Parsers for `.cabal`, `cabal.project`, `cabal.config` and `01-index.tar`
   files.
 * [`cabal-file-th`](https://hackage.haskell.org/package/cabal-file-th):
   Template Haskell expressions for reading fields from a project's cabal file.
 * [`cabal-test-quickcheck`](https://hackage.haskell.org/package/cabal-test-quickcheck):
   QuickCheck for Cabal.
 * [`cabal-doctest`](https://hackage.haskell.org/package/cabal-doctest):
   A Setup.hs helper for doctests running.
 * [`doctest-extract`](https://hackage.haskell.org/package/doctest-extract):
   Standalone extraction of doctest code. Optionally emits a list of Test modules for insertion in a Cabal package description.
 * [`simple-cabal`](https://hackage.haskell.org/package/simple-cabal):
   Find and read `.cabal` files, and a Cabal dependency compatibility layer.
 * [`cabal-file`](https://hackage.haskell.org/package/cabal-file):
   Cabal file access.

## Cabal in GSoC

*Work on Cabal during Google Summer of Code.*

 * [GSoC 2018: `cabal new-{install,repl,run,clean,sdist}`, Cabal scripts](https://typedr.at/posts/what-i-did-on-my-summer-vacation/):
   Description of work to finish bringing Cabal’s Nix-style local builds (the
   new- commands, at least for now) up to parity with the old stateful
   methodology of using `cabal-install`.
 * [GSoC Cabal Nix](https://gitlab.haskell.org/ghc/ghc/wikis/commentary/gsoc-cabal-nix):
   How bringing Nix-style package management facilities to cabal can solve
   various cabal problems and help in effective mitigation of cabal hell.

## History

 * [Old Cabal](https://www.haskell.org/cabal/old.html):
   Really old Cabal stuff.
 * [Announcing New Cabal](http://blog.ezyang.com/2016/05/announcing-cabal-new-build-nix-style-local-builds/):
   `cabal new-build`, also known as “Nix-style local builds”, is a new command
   inspired by Nix that comes with `cabal-install 1.24`.
 * [Cabal 2.0](http://coldwa.st/e/blog/2017-09-09-Cabal-2-0.html):
   What's new in Cabal and `cabal-install` 2.0.

## Community

 * [cabal-devel](http://www.haskell.org/mailman/listinfo/cabal-devel):
   Development discussion takes place on the cabal-devel mailing list.
 * [Libraries mailing list](http://www.haskell.org/mailman/listinfo/libraries):
   Questions can be sent to the Haskell libraries mailing list.
 * [Issue reporting](https://github.com/haskell/cabal/issues/new):
   GitHub issue creation page.

## Contribute to this repository

Improvements to the Awesome Cabal list are more than welcome. Please read the
[contributing guidelines](https://github.com/kowainik/awesome-cabal/blob/main/CONTRIBUTING.md),
go ahead and make the difference!

## License

[![CC0](https://mirrors.creativecommons.org/presskit/buttons/88x31/svg/cc-zero.svg)](https://creativecommons.org/publicdomain/zero/1.0/)
