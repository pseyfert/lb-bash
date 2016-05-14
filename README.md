# lb-bash

this is just a bash port of pseyfert/lb-zsh.

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
for v in $(ls $HOME/.bash_completion.d/ | grep -v LICENSE | grep -v README)
  do
  . $HOME/.bash_completion.d/$v
done
```

(okay, loading the files is not super elegant, cleanup needed)
