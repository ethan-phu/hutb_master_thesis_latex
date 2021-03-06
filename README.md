# CSU Thesis LaTex

湖南工商大学硕士论文LaTex模板。

由于本人水平有限，不能把所有论文的排版格式要求定义在LaTex样式文件中，撰写论文时必须在`main.tex`的文件上进行修改，本模板已经将所有的章节进行了拆分，你可以参考已经放入`chapter`文件夹中的文件，进行编写你的目录结构，然后将你所需要写的论文内容分别写入对应的章节文件。bib格式的参考文献放入`references.bib`文件。

目前只是初步实现，还需要做细节上的调整。

## 使用

该模板必须使用`xelatex`+`biber`命令编译。

```shall
xelatex -synctex=1 -interaction=nonstopmode main.tex
biber main
xelatex -synctex=1 -interaction=nonstopmode main.tex
xelatex -synctex=1 -interaction=nonstopmode main.tex
```

在windows平台运行`compile.bat`可以快捷地编译`main.tex`，`clean.bat`可以清理编译过程中产生的中间文件。linux平台使用对应的`.sh`文件。

**注意**： 论文使用的中文字体包括宋体、黑体、楷书和华文新魏，操作系统必须包含这些字体，否则编译失败。


填写扉页的中图分类号时查阅[中国图书馆分类法](http://www.ztflh.com/)。

## github action 使用方法「强烈推荐」


### 盲审版本

盲审版本需要隐去学生和导师信息。封面和扉页的信息可以通过`main.tex`导言区的设置去掉个人信息，如
```tex
%\blindreviewtrue
\blindreviewfalse
```
改成
```tex
\blindreviewtrue
%\blindreviewfalse
```
致谢和参考文献中相关姓名需要手动删除。

## 参考资料

- 主要参考郭大侠编写的[LaTex模板](https://github.com/CSGrandeur/CSU-Thesis-LaTeX-Template)。
- latex入门教程《一份不太简短的latex2e介绍》。通过`texdoc lshort-zh-cn`查看。
- CTEX介绍《CTEX宏集手册》，`texdoc ctex`。
- 《The LATEX2E Sources》，`texdoc source2e`。
- 《Standard Document Classes for LATEX version 2e》，`texdoc article`。
- 需要用到的各种latex宏包介绍。
