# DEPRECATION

tab completions for bash are by now in upstream.

# lb-bash

this is just a bash port of [pseyfert/lb-zsh](https://github.com/pseyfert/lb-zsh).

## demo

See this [screencast](http://virgilio.mib.infn.it/~seyfert/videos/lb-bash.webm)

## how to

get the code
```
ssh lxplus.cern.ch
git clone https://github.com/pseyfert/lb-bash.git .bash_completion.d
```

load it by default by adding the following to your `$HOME/.bash_completion` file
```
for v in $(ls $HOME/.bash_completion.d/ | grep -v LICENSE | grep -v README | grep -v logo | grep -v svg)
  do
  . $HOME/.bash_completion.d/$v
done
```

(okay, loading the files is not super elegant, cleanup needed)

As personal preference, I also put

```
TAB: menu-complete
set show-all-if-ambiguous on
```

into `$HOME/.inputrc`.

## features

### getpack

lists all getpack'able packages

### git lb-checkout

completes `git lb-checkout [branches and tags] [packages in the chosen project]`

### git lb-use

suggest projects (not only the application projects like Brunel and DaVinci, but also Rec)

# other hints

The lhcb login scripts already set the bash prompt when invoking `SetupProject`
or `lb-run XXXX bash`.  To use this feature, you can set the following in your
`~/.bashrc`

```
export SP_PROMPT="yes"
```
