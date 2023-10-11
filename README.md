# Anathema.Meta
Documentation of the approach used to build Anathema

# Dependencies
* Not using features like Issues on Github - want to minimise dependence on the platform
* Issues/Todos should be written in .md files
* Pull requests are OK though
* This is not mainstream best practice but this is how I want to do it
* Library csprojects should be built against the most restrictive/lowest version runtime practicable (ideally .NET FX 2.0 if it doesn't mean compromising the codebase).
  * Later runtimes are mostly supersets of this, so building them against .NET 7.0 or whatever *should* be trivial
  * If adding LINQ or whatever makes a codebase significantly better, go ahead and use a later runtime
* External dependencies should be injected through shims - the core and interface projects should generally not reference external libraries
* We want to be able to build against a transpiler which may or may not even have Newtonsoft
