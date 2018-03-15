vue笔记
入手的教程笔记 整理的比较全 https://segmentfault.com/a/1190000012692321
《vue-cli#2.0 webpack 配置分析》webpack 配置说明 强烈推荐看 https://juejin.im/post/584e48b2ac502e006c74a120

##vue模板注意事项：
<template> 这里只能有一个对象，不能有多个</template>

比如：
<template>
    <div>
        对象1
    </div>
    <span>
        对象2
    </span>
</template>
template内部包括了2个对象，需要把这两个对象放到一个div里就可以。
否则会提示一下错误：Component template should contain exactly one root element. If you are using v-if on multip
正确的写法：
<template>
    <div>
        <div>
            对象1
        </div>
        <span>
            对象2
        </span>
    </div>
</template>

## 常见错误：
    1.没有正确import 使用了不存在的变量：
    比如：增加路由后，没有import 
    2.经常会有增加了路由，但是没有在router.js里添加变量，或者没有添加导入.vue