## Contributing (Step-by-step) :memo:

[![Join the chat at https://gitter.im/bobdrop/bobapp](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/bobdrop/bobapp?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

1. Clone the Repo:

        git clone https://github.com/bobdrop/bobapp.git

 > If you love to simulate the production environment install vagrant and thin run `vagrant up` inside the project dir

2. Create a new Branch:

        cd bobapp
        git checkout -b new_bobapp_branch

 > Please keep your code clean: one feature or bug-fix per branch. If you find another bug, you want to fix while being in a new branch, please fix it in a separated branch instead.

3. Code
  * Adhere to common conventions you see in the existing code
  * Include tests, and ensure they pass

4. Follow the Coding Conventions
  * two spaces, no tabs
  * no trailing whitespaces, blank lines should have no spaces
  * use spaces around operators, after commas, colons, semicolons, around `{` and before `}`
  * no space after `(`, `[` or before `]`, `)`
  * use Ruby 1.9 hash syntax: prefer `{ a: 1 }` over `{ :a => 1 }`
  * prefer `class << self; def method; end` over `def self.method` for class methods
  * prefer `{ ... }` over `do ... end` for single-line blocks, avoid using `{ ... }` for multi-line blocks
  * avoid `return` when not required

5. Commit

  For every commit please write a short (max 72 characters) summary in the first line followed with a blank line and then more detailed descriptions of the change. Use markdown syntax for simple styling.

  **NEVER leave the commit message blank!** Provide a detailed, clear, and complete description of your commit!

6. Update your branch

  ```
  git fetch origin
  git rebase origin/master
  ```

7. Fork

  ```
  git remote add mine git@github.com:<your user name>/bobapp.git
  ```

8. Push to your remote

  ```
  git push mine new_bobapp_branch
  ```

9. Issue a Pull Request

  Before submitting a pull-request, clean up the history, go over your commits and squash together minor changes and fixes into the corresponding commits. You can squash commits with the interactive rebase command:

  ```
  git fetch origin
  git checkout new_bobapp_branch
  git rebase origin/master
  git rebase -i

  < the editor opens and allows you to change the commit history >
  < follow the instructions on the bottom of the editor >

  git push -f mine new_bobapp_branch
  ```

  In order to make a pull request,
  * Navigate to the bobapp repository you just pushed to (e.g. https://github.com/your-user-name/bobapp)
  * Click "Pull Request".
  * Write your branch name in the branch field (this is filled with "master" by default)
  * Click "Update Commit Range".
  * Ensure the changesets you introduced are included in the "Commits" tab.
  * Ensure that the "Files Changed" incorporate all of your changes.
  * Fill in some details about your potential patch including a meaningful title.
  * Click "Send pull request".

