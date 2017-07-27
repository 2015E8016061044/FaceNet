
n: 2.7 / 3.6    
  安装：统一使用[Anaconda](https://www.continuum.io/downloads)安装。

+ TensorFlow: 1.2    
  安装：[Install with anaconda](https://www.tensorflow.org/install/install_mac#installing_with_anaconda)

+ [flake8](https://pypi.python.org/pypi/flake8): python代码检查    
  `conda install flake8`


### Python

代码风格应遵循[PEP 8 -- Style Guide for Python Code](https://www.python.org/dev/peps/pep-0008/)。


### Gitlab

1 开发前，新建分支

   ```git
   git checkout master
   git checkout -b XXX/YYY
   ```

2 开发中，commit应使用

   ```git
   git add your.files
   git commit -m "XXX: YYYYY"
   ```

   其中XXX规范如下：

   + ENH: 特性
   + BUG
   + CLN: 代码清理与重构
   + DOC: 文档
   + TST: 测试用例
   + BLD

   YYYYY是具体内容。可以使用中文，以描述清晰为准，可参考[Commits](http://git.intra.weibo.com/datasys/Prometheus/commits/master)。

3 开发后，推到Gitlab

   ```git
   git diff master --name-only -- '*.py' | flake8 --diff
   git push -u origin XXX/YYY
   ```

   提交[Merge Request](http://git.intra.weibo.com/datasys/Prometheus/merge_requests)，等待合并。

