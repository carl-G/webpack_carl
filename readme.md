## webpack 原理解析

# 项目结构

|-- forestpack
    |-- dist                            // 打包目录
    |   |-- bundle.js
    |   |-- index.html
    |-- lib                             // 核心文件，主要包括compiler和parser
    |   |-- compiler.js                 // 编译相关。Compiler为一个类, 并且有run方法去开启编译，还有构建module（buildModule）和输出文件（emitFiles）
    |   |-- index.js                    // 实例化Compiler类，并将配置参数（对应forstpack.config.js）传入
    |   |-- parser.js                   // 解析相关。包含解析AST（getAST）、收集依赖（getDependencies）、转换（es6转es5）
    |   |-- test.js                     // 测试文件，用于测试方法函数打console使用
    |-- src                             // 源代码。也就对应我们的业务代码
    |   |-- greeting.js
    |   |-- index.js
    |-- firstpack.config.js             // 配置文件。类似webpack.config.js
    |-- package.json                    // node.js => package.json