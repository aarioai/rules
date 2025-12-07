# Shell 脚本规范


## 标准写法
```shell
# $# 不要加双引号
if [ $# -gt 0 ]; then echo $#; fi

```


## /bin/sh
```shell

```

## /bin/bash
```shell
# 当前脚本，如 /usr/local/project/demo/script.sh
readonly ME=$(AbsPath "${BASH_SOURCE[0]}")

# HERE 表示当前脚本所在目录，如 /usr/local/project/demo
readonly HERE="$(fullDirname "${BASH_SOURCE[0]}")"
 
# ROOT 表示当前项目根目录 /usr/local/project
readonly ROOT="$(cd "${CUR}/.." && pwd)"


```