`change-indent` branch is collect changes to have 3-space indent.

See the original "README.md" file in `main` branch for the details about the original software.

I have no desire to push the changes to "psf/Black". Instead of a
"fork-on-GitHub", I would have preferred some way to be able to "clone; make
changes in a separate branch; perhaps catch up with original repository once a
while". That requires more work (clone original locally; send a copy to GitHub;
catch up locally with original repository; send changes to GitHub.).

Changes as of @c2473c58510eaf175b64340b2c3724d8d5796ef8 (or, first 3 changes of `change-indent` branch so far) are untested as (original: https://freeradical.zone/@ax6761/114381086710704054 ) ...

```
Setting up of the environment (to test 3-space indent change to "black") pooped ...

*/venv-black/bin/pre-commit run -a
...
An unexpected error has occurred: CalledProcessError: command: ('*/venv-black/bin/python', '-mnodeenv', '--prebuilt', '--clean-src', 'HOME/.cache/pre-commit/repolm4s31om/node_env-default')
return code: 1
stdout: (none)
stderr:
     * Install prebuilt node (23.11.0) .Failed to download from https://nodejs.org/download/release/v2

... amazingly enough there is no "node*freebsd*" file at https://nodejs.org/download/release/v23.11.0/ .

Black, make assumptions much? Or, is testing of the software on #FreeBSD unsupported, which is not mentioned at https://black.readthedocs.io/en/latest/contributing/the_basics.html ?

Installing the FreeBSD "node23" package did not cause "pre-commit run -a" to not try to fetch the nonexistent file. Did hope somewhat that that would; oh well. (Undid the uselessness with swift "zfs-rollback(8)" to get back to "node22" package.)
```
