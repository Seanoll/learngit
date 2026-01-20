### 命令（控制序列）：以\开头，大小写敏感：
- \LaTeX{}   latex的logo
- 必须参数用{}，可选参数用[]
### 注释以%开头
### 连续多个空格=单个空格=单个换行
## 文件结构
```
\documentclass{article} % 文档类
% 导言区(preamble): 加载宏包、定义命令、设置文档格式等

\begin{document}  % 文档开始
% 正文区(body): 文档的内容
Hello World!
\input{content.tex} %也可以导入其他文档的内容
\end{document} % 文档结束
```
## 文档类
- 基础文档类：article\report\book\beamer等
- 中文变体：ctexart\ctexrep\ctexbook\ctexbeamer等
- 可以通过可选参数指定字号、纸张大小、双面打印等选项
  `\documentclass[12pt,a4paper,twoside]{article}`
- 宏包相当于第三方库，可以引入更丰富的功能
- TEX Live full 自带大量宏包
- 通过texdoc package查看文档
## 段落
- 正常写作即可，以空行或\par分段
- 行首空格会被忽略，多个空格会被合并为一个
- 换行在非中文语境下视作一个空格
## 断行与断页
- 可以用\\或\newline强制断行
- 用\newpage新开一页
## 字形与字号
- 有两类修改字形的命令：  
{\bfseries bold}和\textbf{bold}  
前者是对作用域内所有内容生效，后者只对参数内容生效  
都是“内置”字体的不同样式
- 修改字号{\large Hi}
- 汉字一般不使用斜体
## 字符和标点
- 特殊字符需要转义，如\_,\%,\$ 
