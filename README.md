# business-git-hooks

## hook to check flake8/pylint before commit

Files needed to work:

* odoo-lint
  * executable file to launch:
    * pylint
      * configured from: https://github.com/OCA/maintainer-quality-tools
    * flake8
  * to create where you want, but the directory or the file must be added in the bin path
* pre-commit
  * will execute the odoo-lint check for specified repositories
  * to create in a git hooks template (in my case in: "/home/user/.git-templates/hooks")
  * see the following documentation to know how activate the git templates: https://git-template.readthedocs.io/en/latest/
  * for information, after configuring, to add hooks in existing git repository, just do "git init"  
  
These script deny to create a commit if we have errors on pylint or flake8.
That's useful to detect flake8 errors ASAP.

Examples of files are available in "pre-commit" directory.
