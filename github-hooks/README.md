# Github Hooks

Github hooks allow scripts to be run automatically when specific events occur
within the Github workflow. To add these functionallities to your local repo,
just copy the files into the .git/hooks folder. You may need to change the
permissions to make them executable.

## pre-commit

This script is executed when you attempt to push a commit. The hook does the
following: 

 * It aborts the commit if the version string does not follow our conventions
   (e.g., v1.23.4 for master or v1.23.4-9xxxx for dev).
   
 * When pushing to master, it requires you enter an irritating magic word
   ("prettyplease"). This annoying behavior is there to make you think twice
   before pushing to master (since most commits should go to dev branches and
   only stable releases should go to master).

 * ensures the version string in `package.yaml` matches the version string in `USAGE`.
