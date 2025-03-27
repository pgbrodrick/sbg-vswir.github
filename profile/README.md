# Surface Biology and Geology (SBG) VSWIR Science and Applications

This organization contains the data product algorithms for the Surface Biology and Geology VSWIR sensor.

## SBG-VSWIR Algorithm Overview

The SBG-VSWIR data product algorithms include:
- [Level 1b Radiance](https://github.com/sbg-vswir/sbg-vswir-l1b-radiance)
- [Level 2a Reflectance](https://github.com/sbg-vswir/sbg-vswir-l2a-reflectance)
- [Level 2b Aquatic](https://github.com/sbg-vswir/sbg-vswir-l2b-aquatic)
- [Level 2b Hydrology/Snow Physics](https://github.com/sbg-vswir/sbg-vswir-l2b-hydrology-snow-physics)
- [Level 2b Geology](https://github.com/sbg-vswir/sbg-vswir-l2b-geology)
- [Level 2b Terrestrial Vegetation](https://github.com/sbg-vswir/sbg-vswir-l2b-terrestrial-veg)
- [Level 2b Fractional Cover](https://github.com/sbg-vswir/sbg-vswir-l2b-cover/blob/main/README.md)


## Related Repositories and Organizations
- [ISOFIT Atmospheric Correction](https://github.com/isofit/isofit)
- [The EMIT Science Data System](https://github.com/emit-sds)

---------------------------------------------------------------------------

# Contributing Guidelines

Thank you for your interest in contributing to the SBG-VSWIR science repositories. 
If you are just getting started, please review the guidelines below to understand how and where you can
best support and contribute to this project.  Typical contributions may include:

* Code patches
* Feature enhancements
* Documentation improvements
* Bug reports

If you have ideas for new additions, or suggested alterations to the algorithm theoretical
basis documents that's great - please contact the maintainers
by submitting issue tickets, and we can coordinate efforts.  Our general policy
is for the maintainers to delegate technical authority to individuals to make
changes and additions to specific topics.  Mission priorities will mean that not
all suggested changes are incorporated into primary repositories, in which case
we strongly encourage forks and code re-use as needed.  Major suggested changes (alterations to
algorithms or to workflows) should be pieces that are supported by peer-reviewed literature,
and should be referenced when initially recommended.  Comparisons against the mission
baseline will likely be required in order to accept major changes.


## Getting Started

Start by checking in on the project's roadmap and current issue list to get a sense
of what the active development and/or feature requests are.

If you have discovered a new issue or task, then go ahead and create a new
issue.


## Fork and Create a Branch

SpectralUnmixing follows the `Standard Fork and Pull Request <https://gist.github.com/Chaser324/ce0505fbed06b947d962>`_ workflow.

When you have chosen an issue to work on, start by `forking <https://help.github.com/articles/fork-a-repo/>`_ the repo.

Then, create a branch with a descriptive name.  A good branch name starts with
the issue number you are working on followed by some descriptive text.  For
example, if you are working on issue #113 you would run:

```
  git checkout -b 113-add-spectral-residual
```


## Testing

When codebases have developed to the point where they hold working mission code, they will also include
test cases that are executed through github actions.  Tests must be completed before a pull request
can be accepted.  Additional tests may be requested by the maintainers for large changes. Please see
individual repositories for additional guidance on local testing (language and process dependent).


As outlined above, our development strategy employs continuous integration and unit testing to validate all changes.  We appreciate you writing additional tests for new modifications or features.  
Implement Your Changes and Create a Pull Request

------------------------------------------------

At this point, you are ready to implement your changes!

As you develop, you should make sure that your branch doesn't veer too far from \<repos\>'s dev branch.  To do this, switch back to your dev branch and make
sure it's up to date with \<repos\>'s dev branch:

.. code::

  git remote add upstream https://github.com/sbg-vswir/\<repos\>.git
  git checkout dev
  git pull upstream dev


Then update your feature branch from your local copy of dev, and push it!  We recommend using git's rebase call when possible.

.. code::

  git checkout 113-add-spectral-residual
  git rebase dev
  git push --set-upstream origin 113-add-spectral-residual


When you are ready to submit your changes back to the \<repos\> repo, go to GitHub
and make a `Pull Request <https://help.github.com/articles/creating-a-pull-request/>`_

## Keeping your Pull Request Updated

If a maintainer asks you to "rebase" your PR, they're saying that a lot of code
has changed, and that you need to update your branch so it's easier to merge.

Here's the suggested workflow:

.. code::

  git checkout 113-add-spectral-residual
  git pull --rebase upstream dev
  git push --force-with-lease 113-add-spectral-residual

Project Decision Making
-----------------------

Minor changes follow an expedited acceptance process.  These are things like:

* Bug fixes
* Unit tests
* Documentation
* Consolidation that does not change algorithm results or provide significant new functionality
* New functionality initiated by maintainers, or over which authority has been delegated in advance by maintainers (e.g. through issue assignment)

Minor change pull requests are accepted once they:

* Pass unit tests and adhere to project coding conventions
* Get signoff from at least one maintainer, with no objections from any other maintainer

Accepted minor changes will be released in the next major or minor release version. Hotfixes will be expedited as needed.

Major changes include:

* New functionality, including examples, data, and algorithm changes, over which authority was not delegated in advance.
* Official releases
* Project policy updates

These are accepted through consensus of a quorum of maintainers.  Final resolution to any disagreement lies
with the SBG-VSWIR Project Scientist or delegated authority.  **If you would like to include any new algorithms or examples, we highly recommend that they are supported by peer reviewed scientific research.** The goal of this repository
and community structure, however, is to avoid major conflicts - hence the encouragement to reach out early to 
discuss new ideas.  Algorithmic advances will be considered using a combination of review of evidence-based efficacy (with
a particular emphases on generality), coupled with an evaluation of the computational resources required for implementation.

## Release Steps (for Maintainers)

Individual repositories will specify release steps for maintainers.

## Contributors

Major contributors will be designated in the CITATION.cff file for each repository. Authority for the designation
of additional contributors lies with the individual repositories maintainers (with disagreements resolved by the SBG-VSWIR Project Scientist) - in general, accepted Pull Requests that include major changes will be considered grounds for being listed as a contributor.