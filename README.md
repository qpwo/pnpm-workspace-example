## pnpm workspace example/template

[View this repo on github1s](https://github1s.com/qpwo/pnpm-workspace-example)

This is an example of a minimal repo using [pnpm's workspaces](https://pnpm.io/workspaces).

## Q & A

-   Q: How do I install on package from another within the workspace?
    -   A: Just `cd pkg1 && npm install pkg2`. It will look for pkg2 in the workspace first.
-   Q: What if the package's folder name differs from the "name" field in `package.json`?
    -   A: The name field is used. The folder name doesn't matter.
-   Q: Do I need to set `"name": "some-name-here"` in package.json?
    -   A: Yes if another package installs it. Folder names just have to match pnpm-workspace.yaml. You also have to set `"main": "some-file.js"`. Instructions for multiple exports from one package [here](https://stackoverflow.com/a/63058817).
-   Q: Do I need a pnpm-workspace.yaml?
    -   A: Yes.
-   Q: Do I need to put stuff in a `/packages/` subdir?
    -   A: No.
