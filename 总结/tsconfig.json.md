1. tsconfig.json 存在根目录，typescript 编译成JavaScript时的配置选项。
2. 使用tsc 生成配置文件
   
        tsc --init
3. 配置说明：
   
        {
            "compilerOptions": {
                "module": "commonjs",
                // 编译成js 那个规范，（es3,es5,es2015,es2016）
                "target": "es5",
                "noImplicitAny": false,
                "sourceMap": false，

                // 监视ts 文件，一旦更改，自动重新编译
                "watch":true
            }
        }