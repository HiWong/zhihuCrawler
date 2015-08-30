# 知乎爬虫

## 介绍

ZhihuCrawler是用C++编写的高效、支持异步网络I/O的知乎爬虫，目的是抓取最高赞回答、最高关注问题等数据。运行环境为支持epoll的平台。

## 使用

先找到浏览器访问知乎的cookie，将它复制到src/confic.cc下的cookie变量里。

编辑./startfile/seeds.txt, 将从这个文件指定的用户URL开始爬。

    make
    ./zhihuCrawler

可以访问http://localhost:8080来查看爬虫的状态。

## 输出

爬下的数据都存储在./datafile/rawData.raw下。
使用

    ./sort.sh

可以查看根据票数排序后的结果。
