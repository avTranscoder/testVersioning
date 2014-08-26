testVersioning
==============

Test to auto release on github via changes in code sources.
This can be done using and CI, with GitHub API in Python.

A new release (major or minor) will create en new branch.
Release will juste replace the new version.
Majors mention changes in the  API (without retro compatibility).
Minors are upgraded version with compatibility.
