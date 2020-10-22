# Various Small `git` Tools and Scripts

## Tools

### `git-format-patchsets`

Format multi-patches, i.e. patch files with multiple complete commits
inside, from a given commit range. Commits can be assigned to/picked for
patch-sets interactively (similar to git rebase), or via a `Patchset:
<name>` tag.

Usage:
```
git format-patchset [-t|--from-tags] [-a|--no-confirm] <revision-range>

  -t --from-tags   Look for 'Patchset:' tags in commit messages and
                   assign patch-set based on this. Commits without a
                   'Patchset:' tag will be formatted in their own file.

  -a --no-confirm  Do not open editor for interactive assignment, i.e.
                   perform assignment automatically without user
                   interaction. Only valid with -t/--from-tags.
```

Examples:
```
git format-patchset -t v4.19.152
git format-patchset -t -a v4.19.152..HEAD
```


## Installation

Add this directory to your path.
