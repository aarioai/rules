## 分支说明
默认主分支一律使用 main （取代以前的master，如果出现master分支，应当通知运维人员变更该分支为main分支）

## 提交格式
> <type>(<scope>):<subject>
```
docs(tutorial/2): 添加使用说明
fix(ae.Error): use ae.Error.Text()
docs: reorganize information about interpolation

```
## <type> 类型
```txt
feat:引入新功能
fix:修复bug
style:更新UI样式文件
format:格式化代码
docs;添加/更新文档
perf:提高性能/优化
init:初次提交/初始化项目
test:增加测试代码
refactor:改进代码结构/代码格式
patch:添加重要补丁
file:添加文件文件
publish:发布新版本[新版本]
tag:发布版本/添加标签
config:修改配置文件[配置)
git:添加或修改gitignore文件[不可见]
chore:构建过程或辅助工具的变动
ci:对CI配置文件和脚本的更改
revert:恢复(Revertacommit)，是把这次提交的修改给还原
```

## <scope> 影响范围
比如控制层、数据层、视图层等