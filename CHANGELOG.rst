^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Changelog for package quadprogpp
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

0.0.2 (2019-12-03)
------------------
* made comileable via catkin
* Merge pull request `#12 <https://github.com/LCAS/QuadProgpp/issues/12>`_ from tiramisueanne/master
  Fix incorrect comparison in Array.hh.
  Thanks to tiramisueanne for the contribution
* Fix incorrect comparison in Array.hh
* Merge pull request `#7 <https://github.com/LCAS/QuadProgpp/issues/7>`_ from yuki-koyama/remove-unused-variable-warnings
  Remove an unused variable declaration
* Merge pull request `#8 <https://github.com/LCAS/QuadProgpp/issues/8>`_ from yuki-koyama/remove-register-from-headers
  Remove "register" from public headers for C++17
* Merge pull request `#9 <https://github.com/LCAS/QuadProgpp/issues/9>`_ from Migdal-Research/fix-warnings-sept-20
  Fix warnings from compilation
* Make implementations of add/delete_constraint take unsigned int
  Before this, the declaration was changed to unsigned int for
  add_constraint and delete_constraint, but the implementation used
  an `int&`. This is especially bad for `delete_constraint` as it
  used a variable that needs to be unsigned to -1 to indicate "not
  found". It did then however not use this to check if the constraint to
  delete was found - instead it would exhibit some unknown behavior caused
  by a -1 being a very large number.
* Drop unused but set variable 'q'
  The variable q is initialized with a 0 and set to various values
  but it is never read. This commit removes the variable 'q'.
* Fix warnings with mismatch of signed/unsigned integer
  Step 1
* Move variables declaration into "for" expressions for better consistency
* Remove the "register" keyword from headers as it was removed in C++17
* Remove an unused variable declaration
* Merge pull request `#6 <https://github.com/LCAS/QuadProgpp/issues/6>`_ from dyollb/fix/get_rid_of_string_literatal_warnings
  fix warning: "conversion from string literal to 'char *' is deprecated"
* get rid of warnings:
  "conversion from string literal to 'char *' is deprecated"
* Merge pull request `#4 <https://github.com/LCAS/QuadProgpp/issues/4>`_ from esquires/namespace
  add quadprogpp namespace
* add quadprogpp namespace
* Merge pull request `#2 <https://github.com/LCAS/QuadProgpp/issues/2>`_ from harrysummer/myfork
* add install make target in CMake script
* Fixed licensing information (it was not consistent across files).
* Updated license information in sources.
* Amended links in the markdown.
* Added reference to Goldfarb-Idnani paper.
* Welcoming contributions.
* Changed old sourceforge url.
* Added a patch by Takano Akio about a minor numerical inconsistency.
* Essentially a port of the sourceforge version to github, using cmake toolchain.
* Initial commit
* Contributors: Bryn Lloyd, Eric Squires, Harry Summer, Henrik Lindberg, Luca Di Gaspero, Marc Hanheide, Yuki Koyama, liuq, tiramisueanne
