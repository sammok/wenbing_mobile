问病网 移动站
======

visit this mobile site via:  http://sammok.github.io/wenbing_mobile.


Sam 前端团队规范
=================
--by sam mok  2013.9.7
---------------------
> 

* 建立前端开发规范的好处
* 结构书写规范
* 命名规范
* 命名空间
* CSS书写规范
* 可读性，可访问性
* 代码性能

***
  
#1 建立前端开发规范的好处

    
    1.拥有一致的编码风格，团队成员之间可互相交接项目,不需要再适应对方的编码风格，上手快。

    2.由于高度格式化，查错方便，开发与维护方便，降低开发与维护成本。

    3.结构清晰，直观，模块独立，机动性强，模块的位置可随意移动。
    
    
    
#2 结构书写规范


    1.根据元素的意义来判断使用的标签，选择适合的语义化标签。

    2.缩进
        页面html代码要有一定层次(缩进)，加强代码的可读性。
        
    3.注释
        对特定的地方、模块加上注释，便于维护,与直观。

    
    
#3 命名规范

    良好的命名习惯，对一个WEB标准网站的开发来说，必将事半功倍。对于后续的维护以及修改更是方便。
        1、样式名称首字母统一为小写字母，不能为数字，下划线及特殊字符。
        2、样式命名尽量语义化，方便阅读，但长度尽量控制;
        3、样式命名为单词时，使用小驼峰式拼写(第二个单词开始,首字母大写)，例如：*keyWord*; *search_keyWord*;
        

#4 命名空间

    4.1 外部调用样式表
        预设：base.css
        预设样式为全站通用原子类(功能单一，不可再细分),并将各标签自	带的样式初始化,并带有常用的布局预设(如margin5 10 15 20..),几乎不会维护与改动。
        结构：main.css
        结构样式为整站除预设样式外，其他结构的样式。
    
    4.2 常用命名
        提取出常用的命名，可以根据语义化自己组合命名 如 atc_lst(文章列表);

        
#5 CSS书写规范
    1.书写风格
        按照一行流来写，即一个属性写一行，这样样式的可读性会大大提升，虽然会有一些留白占用空间，但带来的优势也是很大的， 
        在项目确定完毕之后，可以用CSS压缩软件删掉多余的留白.
    2.书写顺序
        按照  显示属性 > 宽高尺寸( 边距间距) >  文本 > 背景 > 边框 > 定位 > zoom > cursor
        Eg:
            overflow:hidden;
            display:block;
            float:left;
            width:112px;
            height:114px;
            line-height:114px;
            padding:0 10px;
            margin:0 12px 0 0;
            font:20px/114px “microsoft Yahei”;
            /*写font属性可去掉line-height属性*/
            background:#fff url( images/test.gif );
            border:1px solid #978a70;
            position:relative;
            left:0;
            right:0;
            z-index:1;
            zoom:1；
            cursor:pointer;
    
    3.注释格式: 为了更直观的阅读代码和快速定位模块范围
        S = start   E = end;
        - html注释   
        <!-- 主导航 S -->
        <!-- 主导航 E -->
        - CSS注释
        /* ===== 主导航 S =====*/
        - JS注释:;





#6.可读性，可访问性
    6.1可读性
        1.以纯图片为主的主标题模块
        - 在img标签加 alt 、title
        
        2.以图片背景为主的主标题模块
        - 在标题标签中加入标题的文本 与 overflow:hidden; text-indent:-200%;
        
        3.对于背景图(如标题的背景，大模块的圆角阴影背景图,渐变按钮)，为避免网络问题和服务器问题所导致的背景图加载过慢
        或者加载失败带来的阅读障碍(如字体是白色，背景图不能正常加载时，文本无法阅读)
        - 将background:url();之前插入相似颜色的纯色数值;
        
        Eg:  background:#ddd url(images/test.jpg) no-repeat;

***

团队开发规范将不断完善与补充，欢迎各位提出意见！

- sam mok 
- 2013年10月15日 20:16:08







