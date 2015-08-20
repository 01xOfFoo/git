This repository contains miscellaneous git related stuff

## PS1 improvements

1. Open C:\Program Files\Git\etc\profile - file
2. Search for PS1
3. Replace or add after the code block the follow lines

```
fast_git_ps1 ()                                                                              
{                                                                                            
    printf -- "$(git branch 2>/dev/null | grep -e '\* ' | sed 's/^..\(.*\)/ {\1} /')"    
}                                                                                            

PS1='\[\033]0;$MSYSTEM:\w\007                                                                
\033[32m\]\u@\h \[\033[33m\w$(fast_git_ps1)\033[0m\]                                         
$ '
```
