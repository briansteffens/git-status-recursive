git-status-recursive
====================

Show branch and commit info of any git repositories in the current directory or
its subdirectories.

This is meant to help compare complicated repositories with lots of submodules.
By diffing the output of this command with another programmer working on the
same project, you can get a better idea for whether you're both working on the
same collection of branches and commits across all submodules in the project.

# Downloading

Use git to download the source:

```bash
git clone https://github.com/briansteffens/git-status-recursive
cd git-status-recursive
```

# Installing

Make sure you have python3 installed, and then:

```bash
sudo make install
```

# Usage

From a git repository (or anywhere, I guess):

```bash
git status-recursive
```

You should get some output like:

```
./
  On branch master
  8140197 Add a very important new feature

./submodules/critical-dependency
  On branch master
  c2d1263 Fix terrible bug

./submodules/not-so-critical-dependency
  HEAD detached at a97a0a8
  a97a0a8 Add something not too useful

./submodules/who-even-added-this
  On branch master
  85cd305 Add more useless bloat

./some-other-thing
  On branch fix-nonsense
  7e1acf3 Fix things
```

# Uninstalling

```bash
sudo make uninstall
```
