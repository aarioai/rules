# JS 工具

| 构建工具     | 依赖                 | 取代     | 特点                        | 适用    |
|----------|--------------------|--------|---------------------------|-------|
| Rolldown |                    | Rollup | 纯JS打包，不支持服务器端             | JS库开发 |
| Tsdown   | Rolldown           |        | 基于rolldown的 typescript 打包 | TS库开发 |
| Vite     | Rolldown（取代Rollup） |        | 浏览器、服务器端JS、CSS、HTML全功能打包  | 项目开发  |


## tsdown 说明

tsdown 是基于 rolldown 专门为简化 typescript 而开发的开箱即用工具

https://tsdown.dev/zh-CN/guide/


在 package.json 指定 tsdown --config ./tsdown.config.ts  之后，直接运行 npm run build 即可
```shell
# https://tsdown.dev/zh-CN/options/output-directory
.\node_modules\.bin\tsdown -d ./dist # 指定输出目录（默认 ./dist）

# https://tsdown.dev/zh-CN/options/output-format
.\node_modules\.bin\tsdown --format esm # 指定输出格式，默认 esm

.\node_modules\.bin\tsdown --minify # 压缩

.\node_modules\.bin\tsdown --silent # 屏蔽非错误日志
```

## jest 单元测试

```
expect(a).toMatch(b:RegExp)  // b.test(a)
expect(a:Set).toContain(b)  // a.contains(b)   a = new Set([])
expect(()=>a()).toThrow(t?:[string|Error|TypeError|RegExp])

expect(a).toEqual(b)  // 深度比较 a == b，一般适用对象、数组
expect(a).toBe(b)   // a === b
expect(a).toBeGreaterThan(b)  // a>b
expect(a).toBeGreaterThanOrEqual(b)  // a>=b
expect(a).toBeLessThan(b)  // a<b
expect(a).toBeLessThanOrEqual(b)  // a<=b
expect(a).toBeNull()
expect(a).toBeDefined()
expect(a).toBeUndefined()
expect(a).toBeTruthy()
expect(a).toBeFalsy()
```