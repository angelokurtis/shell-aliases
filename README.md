# shell-aliases
Custom shell aliases based on https://github.com/ahmetb/kubectl-aliases

### Installation

You can directly download the [`.kubectl_aliases`](https://rawgit.com/ahmetb/kubectl-alias/master/.kubectl_aliases) file
and save it in your $HOME directory, then edit your .bashrc/.zshrc file with:

```sh
[ -f ~/.kubectl_aliases ] && source <(cat ~/.kubectl_aliases | sed -r 's/(kubectl.*) --watch/watch \1/g')
```

**Print the full command before running it:** Add this to your `.bashrc` or
`.zshrc` file:

```sh
function kubectl() { echo "+ kubectl $@">&2; command kubectl $@; }
```
