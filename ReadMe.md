#  Git Commit Msg
## _[Karma][karma] - Git Commit Msg_

### The reasons for these conventions:

- automatic generating of the changelog
- simple navigation through git history (e.g. ignoring style changes)

### Format of the commit message:
```
<type>(<scope>): <subject>

<body>

<footer>
```

### Example commit message:
```
fix(middleware): ensure Range headers adhere more closely to RFC 2616

Add one new dependency, use `range-parser` (Express dependency) to compute
range. It is more well-tested in the wild.'

Fixes #2310
```
### Message subject (first line)

The first line cannot be longer than 70 characters, the second line is always blank and other lines should be wrapped at 80 characters. The type and scope should always be lowercase as shown below.

##### Allowed `<type>` values:
"type" must be one of the following mentioned below!
- `build`: Build related changes (eg: npm related/ adding external dependencies)
- `chore`: A code change that external user won't see (updating grunt tasks etc; no production code change)
eg: change to .gitignore file or .prettierrc file
- `docs`: Documentation related changes (changes to the documentation)
- `feat`: A new feature (new feature for the user, not a new feature for build script) 
- `fix`: (bug fix for the user, not a fix to a build script)
- `perf`: A code that improves performance
- `refactor`: A code that neither fix bug nor adds a feature. (refactoring production code, eg. renaming a variable)
 eg: You can use this when there is semantic changes like renaming a variable/ function name
- `style`: A code that is related to styling (formatting, missing semi colons, etc; no production code change)
- `test`: Adding new test or making changes to existing test (adding missing tests, refactoring tests; no production code 

##### Example `<scope>` values: (is optional)
Scope must be noun and it represents the section of the section of the codebase

* init
* runner
* watcher
* config
* web-server
* proxy
* etc.

The `<scope>` can be empty (e.g. if the change is a global or difficult to assign to a single component), in which case the parentheses are omitted. In smaller projects such as Karma plugins, the `<scope>` is empty.
##### Message `<subject>`
- use imperative, present tense (eg: use "add" instead of "added" or "adds")
- don't use dot(.) at end
- don't capitalize first letter

##### Message `<body>`
ses the imperative, present tense: “change” not “changed” nor “changes”
includes motivation for the change and contrasts with previous behavior

>For more info about message body, see:
>
> - http://365git.tumblr.com/post/3308646748/writing-git-commit-messages
> - http://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html

##### Message `<footer>`
**Referencing issues**
Closed issues should be listed on a separate line in the footer prefixed with "Closes" keyword like this:

```
Closes #234
```
or in the case of multiple issues:
```
Closes #123, #245, #992
```

**Breaking changes**
All breaking changes have to be mentioned in footer with the description of the change, justification and migration notes.

>BREAKING CHANGE:
>
>`port-runner` command line option has changed to `runner-port`, so that it is
consistent with the configuration file syntax.
>To migrate your project, change all the commands, where you use `--port-runner`
to `--runner-port`.

## See More
- [dev.to][dev.to]
- [conventionalcommits.org][conventionalcommits.org]
- [gist.github.com/joshbuchea][gist.github.com/joshbuchea]
- [git-semantic-commits][git-semantic-commits]

## License

MIT

_Karma is released under the MIT license. Site by Friedel Ziegelmayer. Logo by Isaac Durazo_.

   [karma]: <https://karma-runner.github.io/6.3/dev/git-commit-msg.html>
   [dev.to]: <https://dev.to/i5han3/git-commit-message-convention-that-you-can-follow-1709>
   [conventionalcommits.org]: <https://www.conventionalcommits.org/en/v1.0.0/>
   [gist.github.com/joshbuchea]: <https://gist.github.com/joshbuchea/6f47e86d2510bce28f8e7f42ae84c716>
   [git-semantic-commits]: <https://github.com/fteem/git-semantic-commits>
