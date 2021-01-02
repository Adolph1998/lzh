# Welcome to lzh Blog

# 目录
[toc]

## go

### google wire 

#### debug学习
* 借助wire comand
```
wire help

Subcommands:
        check            打印发现的任何导线错误
        commands         列出所有命令名
        diff             在现有的wire_gen.go文件和生成的内容之间输出差异
        flags            描述所有已知的顶级标志
        gen              为每个程序包生成wire_gen.go文件
        help             描述子命令及其语法
        show             描述所有顶级提供程序集
```

1. 常见错误
 - 嵌套循环： 
 ```
 service:
  project1
  wire1
  service2:
    project2
    wire2
  
  project2调用了project1的方法导致嵌套循环
 ```
 
