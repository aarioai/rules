# Javascript/Typescript 规则技巧

* 浮点数向下取整，应优先使用 aa-js 的 `floatToInt()`，或者 `value | 0`
* 遍历数组优先使用 `for(const value of arr){}`，而不是 `for(let i=0; i<arr.length; i++)`，除非需要`i`值
  * 前者可读性更好，性能与后者差不多