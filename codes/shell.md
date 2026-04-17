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
ME=$(AbsPath "${BASH_SOURCE[0]}")
readonly ME

# HERE 表示当前脚本所在目录，如 /usr/local/project/demo
HERE="$(AbsDir "${BASH_SOURCE[0]}")"
readonly HERE

# ROOT 表示当前项目根目录 /usr/local/project
ROOT="$(ParentDir "$CUR")"
readonly ROOT

```

```/bin/sh
# 要求root执行
if [ "$(id -u)" != '0' ]; then
  exec sudo "$0" "$@"
  return 0
fi
```
```/bin/bash
# 要求root执行
if ! IAmRoot; then
  exec sudo "${BASH_SOURCE[0]}" "$@"
  return 0
fi
```