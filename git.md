# Git

## Auto Completion

On Mac, install Git auto completion via Homebrew:

```bash
brew install git bash-completion
```

Then, add the following to your `~/.bash_profile` or whatever Homebrew tells you:

```bash
[[ -r "/opt/homebrew/etc/profile.d/bash_completion.sh" ]] && . "/opt/homebrew/etc/profile.d/bash_completion.sh"
```

That worked on my laptop, but this is what was suggested by Homebrew on my iMac.

```bash
[[ -r "/usr/local/etc/profile.d/bash_completion.sh" ]] && . "/usr/local/etc/profile.d/bash_completion.sh"
```
