# shell-aliases
Custom shell aliases based on https://github.com/ahmetb/kubectl-aliases

### Installation

You can directly download the [`.kubectl_aliases`](https://github.com/angelokurtis/shell-aliases/blob/master/.kubectl_aliases)
and save it in your $HOME directory:

```sh
wget -O ~/.kubectl_aliases https://raw.githubusercontent.com/angelokurtis/shell-aliases/master/.kubectl_aliases
```

Then edit your .bashrc/.zshrc file with:

```sh
[ -f ~/.kubectl_aliases ] && source <(cat ~/.kubectl_aliases | sed -r 's/(kubectl.*) --watch/watch \1/g')
```

You also can print the full command before running it just adding to your `.bashrc` or
`.zshrc` file:

```sh
function kubectl() { echo "+ kubectl $@">&2; command kubectl $@; }
```
