<h1>项目简介</h1>
&nbsp;&nbsp;&nbsp;&nbsp;数据越来越多，传统的关系型数据库支撑不了，分布式数据仓库又非常贵。几十亿、几百亿、甚至几千亿的数据量，如何才能高效的分析？<br>
mdrill是由阿里妈妈开源的一套数据的软件，针对TB级数据量，能够仅用10台机器，达到秒级响应，数据能实时导入,可以对任意的维度进行组合与过滤。<br>
&nbsp;&nbsp;&nbsp;&nbsp;mdrill作为数据在线分析处理软件，可以在几秒到几十秒的时间，分析百亿级别的任意组合维度的数据。<br>
在阿里10台机器完成每日30亿的数据存储，其中10亿为实时的数据导入，20亿为离线导入。目前集群的总存储1000多亿80~400维度的数据。

<h1>mdrill的特性</h1>
<b>1.满足大数据查询需求：</b>adhoc每天的数据量为30亿条，随着日积月累，数据会越来越大，mdrill采用列存储，索引，分布式技术，适当的分区等满足用户对数据的实时在线分析的需求。<br>
<b>2.支持增量更新：</b>离线形式的mdrill数据支持按照分区方式的增量更新。<br>
<b>3.支持实时数据导入：</b>在仅有10台机器的情况下，支持每天10亿级别（高峰每小时2亿）的实时导入。<br>
<b>4.响应时间快：</b>列存储、倒排索引、高效的数据压缩、内存计算，各种缓存、分区、分布式处理等等这些技术，使得mdrill可以仅在几秒到几十秒的时间分析百亿级别的数据。<br>
<b>5.低成本：</b>目前在阿里adhoc仅仅使用10台48G内存的PC机，但确存储了超过千亿规模的数据。<br>
<b>6.全文检索模式：</b>在mdrill的全文检索模式数据可以直接存储在hdfs中，并且以每天160亿*70维度的数据增量提供全文检索服务（注：该模式下不能进行统计，只能进行关键词匹配查询数据明细）<br>


<h1> 发行日志</h1>
 2013.07.24 version 0.18-beta  初始化版本  <br>
 2013.08.07 version 0.18.1-beta bug fix <a href="https://github.com/alibaba/mdrill/wiki/018_1">see detail</a>  <br>
 2013.08.17 version 0.18.2-beta speed up <a href="https://github.com/alibaba/mdrill/wiki/018_2">see detail</a>  (<a href="http://yunpan.cn/QXn4tRAzx8NIL" target="_blank">下载</a>) <br>
 2013.09.01 version 0.19-alpha HA by replication <a href="https://github.com/alibaba/mdrill/wiki/019_alpha">see detail</a>  (此版本需要一定时间的测试与调整，慎用) <br>
 2013.09.26 version 0.19.1-beta Bug Fix <a href="https://github.com/alibaba/mdrill/wiki/019_beta_1">see detail</a>  (<a href="http://yunpan.cn/QGprqdtDD7r2x" target="_blank">下载</a>) <br>
 2013.09.29 version 0.19.2-beta Bug Fix (<a href="http://yunpan.cn/QGC7TX2tupBcn" target="_blank">下载</a>) <br>
 2013.10.09 version 0.19.3-beta speed up (此版本有严重BUG,请勿使用,<a href="http://yunpan.cn/QbreqTZbusDtu" target="_blank">下载</a>) <br>
 2013.10.13 version 0.19.4-beta mergerServer优化&&bugfix (推荐版本,<a href="http://yunpan.cn/Qbk4ebcjuUyjL" target="_blank">下载</a>,依赖的zeromq从<a href="http://yunpan.cn/QGp3QIMaBbnpy" target="_blank">这里下载</a>) <br>
 2013.11.19 version 0.20.1-alpha 使用hdfs进行检索&&实时append <a href="https://github.com/alibaba/mdrill/wiki/020_1">see detail</a>(alpha版本，慎用。 <a href="http://yunpan.cn/QUypgcZpmvwwv" target="_blank">源码下载</a>) <br>
 2013.12.03 version 0.20.2-alpha 全文检索模式优化 <a href="https://github.com/alibaba/mdrill/wiki/020_2">see detail</a>(alpha版本，慎用。 <a href="http://yunpan.cn/QUeabpfm9bHwG" target="_blank">源码下载</a>) <br>
 2013.12.05 version 0.20.3-alpha bugfix (alpha版本，慎用。 <a href="http://yunpan.cn/QU9u6YIRUyVin" target="_blank">源码下载</a>) <br>
 2014.01.02 version 0.20.4-alpha 通过editlog来保证实时数据的可靠性 <a href="https://github.com/alibaba/mdrill/wiki/0_20_4_alpha" >see detail</a>(alpha版本，慎用。 <a href="http://yunpan.cn/QDTNyLH6NjyeA" target="_blank">源码下载</a>) <br>
 2014.01.14 version 0.20.5-alpha bug fix (<a href="http://yunpan.cn/QzP6H2vfgW5k8" target="_blank">下载</a>) <br>
 2014.01.26 version 0.20.6-alpha bug fix (<a href="http://yunpan.taobao.com/share/link/N62RcRYGa" target="_blank">下载</a>) <br>
 2014.02.08 version 0.20.7-alpha cache改进 <a href="https://github.com/alibaba/mdrill/wiki/0.20.7">see detail</a>  (推荐版本。 <a href="http://yunpan.taobao.com/share/link/662RdRlqL" target="_blank">点击这里下载</a> 。依赖的zeromq从<a href="http://yunpan.cn/QGp3QIMaBbnpy" target="_blank">这里下载</a>) <br>

 
 http://yunpan.taobao.com/share/link/662RdRlqL
 <h1>版本源码路径</h1>
 https://github.com/alibaba/mdrill/tree/master/release  <br>


<h1>资源列表</h1>
<ul>
<li><a href="https://github.com/alibaba/mdrill/wiki/info" target="_blank">mdrill介绍</a></li>
<li><a href="http://yunpan.cn/QUDeVwrMQPjc4" target="_blank">mdrill介绍PPT</a></li>
<li><a href="https://github.com/alibaba/mdrill/blob/master/doc/INSTALL.docx?raw=true" target="_blank">安装部署</a></li>
<li><a href="https://github.com/alibaba/mdrill/blob/master/doc/MSql.docx?raw=true" target="_blank">sql使用手册</a></li>
<li><a href="https://github.com/alibaba/mdrill/wiki/plan" target="_blank">版本开发计划</a></li>
<li><a href="https://github.com/alibaba/mdrill/wiki/adhoc" target="_blank">阿里妈妈-AdHoc-基于mdrill的大数据自助分析平台</a></li>



<li><a hfef="http://www.apache.org/licenses/LICENSE-2.0" target="_blank">LICENSE</a></li>
</ul>

<h1>mdrill Core contributors</h1>
<ul>
<li><a href="https://github.com/muyannian">母延年(子落)</a>、<a href="http://user.qzone.qq.com/2253209">秦剑(含光)</a>、<a href="https://github.com/bwzheng2010">郑博文(士远)</a>、陈鹏(伯时)、木晗、逸客、张壮、凌凝</li>
</ul>
<h1>jstorm Core contributors <a href="https://github.com/alibaba/jstorm" target="_blank">点击进入</a></h1>
<ul>
<li><a href="https://github.com/longdafeng">封仲淹(纪君祥)</a>、<a href="https://github.com/tumen">李鑫(丙吉)</a>、<a href="https://github.com/muyannian">母延年(子落)</a>、<a href="https://github.com/zhouxinxust">周鑫(陈均)</a></li>



</ul>


<h1>其他</h1>
<ul>
<li><a href="https://github.com/alibaba/mdrill/wiki/faq" target="_blank">FAQ</a></li>
<li>mdrill技术交流群:171465049</li>
<li>微博：<a href="http://weibo.com/mynyannian" >http://weibo.com/mynyannian</a></li>

</ul>
