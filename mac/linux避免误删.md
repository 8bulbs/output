```bash
$ cd
$ cd ../../home
$ mkdir -p ~/.Trash
$ vi ~/.bashrc
```

贴入如下代码

```text
alias rm=trash        
alias rl='ls ~/.Trash'  
alias ur=undelfile  
undelfile()  
{  
  mv -i ~/.Trash/$@ ./  
}  
trash()  
{  
  mv $@ ~/.Trash/  
}
cleartrash()  
{  
    read -p "Clear trash?[n]" confirm  
    [ $confirm == 'y' ] || [ $confirm == 'Y' ]  && /usr/bin/rm -rf ~/.Trash/*  
}
```

```bash
$ source ~/.bashrc
```
至此可用指令 rm(删除), ur(撤销), rl(列出回收站), cleartrash(清空回收站）

参考： [http://www.cnblogs.com/qzqdy/p/9299595.html](http://www.cnblogs.com/qzqdy/p/9299595.html)

