# 在 Git Bash 中显示中文字符
*   在 `${HOME}/.profile` 中设置：

        alias ls="ls --show-control-chars --color=auto"
        export LESSCHARSET=utf-8
效果：      
Git Bash 中 `ls` 能够正常显示中文文件名。       
分页时可以正常显示中文。 



*   在 `${HOME}/.inputrc` 中设置：

        set output-meta on
        set convert-meta off
效果：      
Git Bash 中可以正常输入中文（比如，在 `git commit` 提交时）。 

