
    <title>搭建自己的 “一言 API” - Vann's Blog</title>
            <link rel="icon" type="image/ico" href="/usr/uploads/pic/favicon.ico">
        <meta name="description" content="什么是一言简单来说，一言指的就是一句话，可以是动漫中的台词，也可以是网络上的各种小段子。或是感动，或是开心，有或是单纯的回忆。来到这里，留下你所喜欢的那一句句话，与大家分享，这就是一言存在的目的..." />
<meta name="keywords" content="web,API" />
<meta name="generator" content="Typecho 1.2/18.10.23" />
<meta name="template" content="handsome" />
<link rel="alternate" type="application/rss+xml" title="搭建自己的 “一言 API” &raquo; Vann's Blog &raquo; RSS 2.0" href="https://blog.imvann.com/feed/3.html" />
<link rel="alternate" type="application/rdf+xml" title="搭建自己的 “一言 API” &raquo; Vann's Blog &raquo; RSS 1.0" href="https://blog.imvann.com/feed/rss/3.html" />
<link rel="alternate" type="application/atom+xml" title="搭建自己的 “一言 API” &raquo; Vann's Blog &raquo; ATOM 1.0" href="https://blog.imvann.com/feed/atom/3.html" />

<link rel="amphtml" href="https://blog.imvann.com/amp/3.html">
<link rel="miphtml" href="https://blog.imvann.com/mip/3.html">

        <!-- 第三方CDN加载CSS -->
        <link href="https://blog.imvann.com/usr/themes/handsome/assets/libs/bootstrap/css/bootstrap.min.css" rel="stylesheet">


    <!-- 本地css静态资源 -->
    <link rel="stylesheet" href="https://blog.imvann.com/usr/themes/handsome/assets/css/function.min.css?v=6.0.020191205" type="text/css" />
    <link rel="stylesheet" href="https://blog.imvann.com/usr/themes/handsome/assets/css/handsome.min.css?v=6.0.020191205" type="text/css" />



    <!--主题组件css文件加载-->
    <link rel="stylesheet" href="https://blog.imvann.com/usr/themes/handsome/assets/css/features/jquery.fancybox.min.css?v=6.0.020191205" type="text/css" />
        <link rel="stylesheet" href="https://blog.imvann.com/usr/themes/handsome/assets/css/features/newblack.min.css?v=6.0.020191205" type="text/css" />
        <link rel="stylesheet" href="https://blog.imvann.com/usr/themes/handsome/assets/css/features/code/vs.min.css?v=6.0.020191205" type="text/css" />
    
    <!--引入英文字体文件-->
        <link rel="stylesheet" href="https://blog.imvann.com/usr/themes/handsome/assets/css/font.min.css?v=6.0.020191205" type="text/css" />
    
    <style type="text/css">
        
        html.bg {
                   background-image:
               -moz-radial-gradient(-20% 140%, ellipse ,  rgba(235,167,171,.6) 30%,rgba(255,255,227,0) 50%),
               -moz-radial-gradient(60% 40%,ellipse,   #d9e3e5 10%,rgba(44,70,76,.0) 60%),
               -moz-linear-gradient(-45deg,  rgba(62,70,92,.8) -10%,rgba(220,230,200,.8) 80% )
               ;
           background-image:
               -o-radial-gradient(-20% 140%, ellipse ,  rgba(235,167,171,.6) 30%,rgba(255,255,227,0) 50%),
               -o-radial-gradient(60% 40%,ellipse,   #d9e3e5 10%,rgba(44,70,76,.0) 60%),
               -o-linear-gradient(-45deg,  rgba(62,70,92,.8) -10%,rgba(220,230,200,.8) 80% )
               ;
           background-image:
               -ms-radial-gradient(-20% 140%, ellipse ,  rgba(235,167,171,.6) 30%,rgba(255,255,227,0) 50%),
               -ms-radial-gradient(60% 40%,ellipse,   #d9e3e5 10%,rgba(44,70,76,.0) 60%),
               -ms-linear-gradient(-45deg,  rgba(62,70,92,.8) -10%,rgba(220,230,200,.8) 80% )
               ;
           background-image:
               -webkit-radial-gradient(-20% 140%, ellipse ,  rgba(235,167,171,.6) 30%,rgba(255,255,227,0) 50%),
               -webkit-radial-gradient(60% 40%,ellipse,   #d9e3e5 10%,rgba(44,70,76,.0) 60%),
               -webkit-linear-gradient(-45deg,  rgba(62,70,92,.8) -10%,rgba(220,230,200,.8) 80% )
               ;
        }
        .cool-transparent .off-screen+* .app-content-body {
                   background-image:
               -moz-radial-gradient(-20% 140%, ellipse ,  rgba(235,167,171,.6) 30%,rgba(255,255,227,0) 50%),
               -moz-radial-gradient(60% 40%,ellipse,   #d9e3e5 10%,rgba(44,70,76,.0) 60%),
               -moz-linear-gradient(-45deg,  rgba(62,70,92,.8) -10%,rgba(220,230,200,.8) 80% )
               ;
           background-image:
               -o-radial-gradient(-20% 140%, ellipse ,  rgba(235,167,171,.6) 30%,rgba(255,255,227,0) 50%),
               -o-radial-gradient(60% 40%,ellipse,   #d9e3e5 10%,rgba(44,70,76,.0) 60%),
               -o-linear-gradient(-45deg,  rgba(62,70,92,.8) -10%,rgba(220,230,200,.8) 80% )
               ;
           background-image:
               -ms-radial-gradient(-20% 140%, ellipse ,  rgba(235,167,171,.6) 30%,rgba(255,255,227,0) 50%),
               -ms-radial-gradient(60% 40%,ellipse,   #d9e3e5 10%,rgba(44,70,76,.0) 60%),
               -ms-linear-gradient(-45deg,  rgba(62,70,92,.8) -10%,rgba(220,230,200,.8) 80% )
               ;
           background-image:
               -webkit-radial-gradient(-20% 140%, ellipse ,  rgba(235,167,171,.6) 30%,rgba(255,255,227,0) 50%),
               -webkit-radial-gradient(60% 40%,ellipse,   #d9e3e5 10%,rgba(44,70,76,.0) 60%),
               -webkit-linear-gradient(-45deg,  rgba(62,70,92,.8) -10%,rgba(220,230,200,.8) 80% )
               ;
        }
@media (max-width:767px){
    html.bg {
        
        }
        .cool-transparent .off-screen+* .app-content-body {
        
        }
}
.blog-post .panel:not(article) {
    transition: all 0.3s;
}

.blog-post .panel:not(article):hover {
    transform: translateY(-10px);
    box-shadow: 0 8px 10px rgba(73, 90, 47, 0.47);
}
/*首页文章列表悬停上浮*/
.blog-post .panel-picture:not(article) {
    transition: all 0.3s;
}

.blog-post .panel-picture:not(article):hover {
    transform: translateY(-10px);
    box-shadow: 0 8px 10px rgba(73, 90, 47, 0.47);
}
/*首页文章列表悬停上浮*/
.blog-post .panel-small:not(article) {
    transition: all 0.3s;
}

.blog-post .panel-small:not(article):hover {
    transform: translateY(-10px);
    box-shadow: 0 8px 10px rgba(73, 90, 47, 0.47);
}    </style>

    <!--全站jquery-->
    <script src="https://blog.imvann.com/usr/themes/handsome/assets/libs/jquery/jquery.min.js"></script>

    <!--网站统计代码-->
    <!-- 百度统计 -->
<script>
var _hmt = _hmt || [];
(function() {
  var hm = document.createElement("script");
  hm.src = "https://hm.baidu.com/hm.js?df11b60e1dd9dd2de25c26c6a46811f2";
  var s = document.getElementsByTagName("script")[0]; 
  s.parentNode.insertBefore(hm, s);
})();
</script>
<!-- 百度统计 -->

<!--Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=UA-159361057-1"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());

  gtag('config', 'UA-159361057-1');
</script>
<!--Google Analytics End -->
    <script src="https://blog.imvann.com/usr/themes/handsome/assets/js/features/fancyMorph.min.js"></script>


</head>

<body id="body" class="fix-padding">

	<!-- aside -->
	  
  <div id="alllayout" class="app app-aside-fix container app-header-fixed ">  <!-- headnav -->
      <header id="header" class="fix-padding app-header navbar box-shadow-bottom-lg" role="menu">
      <!-- navbar header（交集处） -->
        <div class="text-ellipsis navbar-header bg-black">
        <button class="pull-right visible-xs" ui-toggle-class="show animated animated-lento fadeIn" target=".navbar-collapse">
            <span class="menu-icons"><i data-feather="search"></i></span>
        </button>
        <button class="pull-left visible-xs" ui-toggle-class="off-screen animated" target=".app-aside" ui-scroll="app">
            <span class="menu-icons"><i data-feather="menu"></i></span>
        </button>
        <!-- brand -->
        <a href="https://blog.imvann.com/" class="navbar-brand text-lt">
                                                <i class="fontello fontello-home"></i>
                                <span class="hidden-folded m-l-xs">Vann`s Blog</span>
                    </a>
        <!-- / brand -->
      </div>
      <!-- / navbar header -->

      <!-- navbar collapse（顶部导航栏） -->
    <div class="collapse pos-rlt navbar-collapse bg-black">
        <!-- search form -->
        <form id="searchform1" class="searchform navbar-form navbar-form-sm navbar-left shift" method="post"
              role="search">
          <div class="form-group">
            <div class="input-group rounded bg-white-pure box-shadow-wrap-normal">
              <input  autocomplete="off" id="search_input" type="search" name="s" class="transparent rounded form-control input-sm no-borders padder" required placeholder="输入关键词搜索…">
                <!--搜索提示-->
                <ul id="search_tips_drop" class="small-scroll-bar dropdown-menu hide" style="display: block;top: 
                30px; left: 0px;">
                </ul>
              <span id="search_submit" class="transparent input-group-btn" onclick=jumpForSearch(search_input.value)>
                  <button  type="submit" class="transparent btn btn-sm">
                      <span class="feathericons" id="icon-search"><i data-feather="search"></i></span>
                      <span class="feathericons animate-spin  hide" id="spin-search"><i
                                  data-feather="loader"></i></span>
<!--                      <i class="fontello fontello-search" id="icon-search"></i>-->
<!--                      <i class="animate-spin  fontello fontello-spinner hide" id="spin-search"></i>-->
                  </button>
              </span>
            </div>
          </div>
        </form>
          <a href="" style="display: none" id="searchUrl"></a>
        <!-- / search form -->
        
        <!--/开始修复搜索按钮-->
        <script type="text/javascript">
        function jumpForSearch(search_ct){
          if(search_ct.length>0){
            $.pjax({ 
            url: "https://"+document.domain+'/search/'+search_ct, 
            container: '#content',
            fragment: '#content',
            timeout: 8000
            });
          }
        }
        </script>
        <!--/修复搜索按钮结束-->
        
                <ul class="nav navbar-nav navbar-right">
                                                          <!--登录管理-->
          <li class="dropdown" id="easyLogin">
            <a onclick="return false" data-toggle="dropdown" class="dropdown-toggle clear" data-toggle="dropdown">
                        <span class="feathericons"><i data-feather="key"></i></span>
                        <b class="caret"></b><!--下三角符号-->
            </a>
            <!-- dropdown(已经登录) -->
                      <div class="dropdown-menu w-lg wrapper bg-white animated fadeIn" aria-labelledby="navbar-login-dropdown">
            <form id="Login_form" action="https://blog.imvann.com/index.php/action/login?_=8a7dfae16ab26f211888dc45959f4897" method="post">
              <div class="form-group">
                <label for="navbar-login-user">用户名</label>
                <input type="text" name="name" id="navbar-login-user" class="form-control" placeholder="用户名或电子邮箱"></div>
              <div class="form-group">
                <label for="navbar-login-password">密码</label>
                <input type="password" name="password" id="navbar-login-password" class="form-control" placeholder="密码"></div>
                <button style="width: 100%" type="submit" id="login-submit" name ="submitLogin" class="btn-rounded box-shadow-wrap-lg btn-gd-primary padder-lg">
                    <span>登录</span>
                    <span class="text-active">登录中...</span>
                    <span class="banLogin_text">刷新页面后登录</span>
                    <i class="animate-spin  fontello fontello-spinner hide" id="spin-login"></i>
                    <i class="animate-spin fontello fontello-refresh hide" id="ban-login"></i>
                </button>


              
              <input type="hidden" name="referer" value="https://blog.imvann.com"
                     data-current-url="value"></form>
          </div>
                    </li>
          <!--/登录管理-->
                    </ul>
      </div>
      <!-- / navbar collapse -->
  </header>
  <!-- / headnav -->

  <!--选择侧边栏的颜色-->
  <aside id="aside" class="app-aside hidden-xs bg-white">  <!--<aside>-->
        <div class="aside-wrap" layout="column">
        <div class="navi-wrap scroll-y scroll-hide" flex>
          <!-- user -->
          <div class="clearfix hidden-xs text-center hide  show" id="aside-user">
            <div class="dropdown wrapper ">
                <div ui-nav>
                          <a href="https://blog.imvann.com">
                            <span class="thumb-lg w-auto-folded avatar m-t-sm  ">
                  <img src="/usr/uploads/pic/Avatar.JPG" class="img-full img-circle normal-shadow">
                </span>
              </a>
                </div>
              <a href="#" data-toggle="dropdown" class="dropdown-toggle hidden-folded  ">
                <span class="clear">
                  <span class="block m-t-sm">
                    <strong class="font-bold text-lt">Vann</strong>
                    <b class="caret"></b>
                  </span>
                  <span class="text-muted text-xs block">竹杖芒鞋轻胜马</span>
                </span>
              </a>
              <!-- dropdown -->
              <ul class="dropdown-menu animated fadeInRight w hidden-folded no-padder">
                <li class="wrapper b-b m-b-sm bg-info m-n">
                  <span class="arrow top hidden-folded arrow-info"></span>
                  <div>
                                                  <p>下午好，是时候打个盹了</p>
                                  </div>
                  <div class="progress progress-xs m-b-none dker">
                    <div class="progress-bar bg-white" data-toggle="tooltip" data-original-title="时间已经度过58.33%" style="width: 58.33%"></div>
                  </div>
                </li>
              </ul>
              <!-- / dropdown -->
            </div>
          </div>
          <!-- / user -->

          <!-- nav -->
          <nav ui-nav class="navi clearfix">
            <ul class="nav">
             <!--index-->
                <div class="line dk hidden-folded"></div>
                <li class="hidden-folded padder m-t m-b-sm text-muted text-xs">
                <span>导航</span>
              </li>
                                          <!--主页-->
              <li>
                <a href="https://blog.imvann.com/" class="auto">
                    <span class="nav-icon"><i data-feather="home"></i></span>
                    <span>首页</span>
                </a>
              </li>
              <!-- /主页 -->
                            <li> <a target="_blank" href="https://blog.imvann.com/api/hitokoto" 
class ="auto"><span class="nav-icon"><i data-feather="music"></i></span><span>一言API</span></a></li><li> <a target="_blank" href="https://blog.imvann.com/api/jitang" 
class ="auto"><span class="nav-icon"><i data-feather="music"></i></span><span>毒鸡汤</span></a></li><li> <a target="_self" href="https://blog.imvann.com/cross.html" 
class ="auto"><span class="nav-icon"><i data-feather="music"></i></span><span>关于我</span></a></li>                              <li class="line dk"></li>
			<!--Components-->
              <li class="hidden-folded padder m-t m-b-sm text-muted text-xs">
                <span>组成</span>
              </li>
              <!--分类category-->
                              <li >
                <a class="auto">
                  <span class="pull-right text-muted">
                    <i class="fontello icon-fw fontello-angle-right text"></i>
                    <i class="fontello icon-fw fontello-angle-down text-active"></i>
                  </span>
<!--                  <i class="glyphicon glyphicon-th"></i>-->
                    <span class="nav-icon"><i data-feather="grid"></i></span>

                    <span>分类</span>
                </a>
                <ul class="nav nav-sub dk">
                  <li class="nav-sub-header">
                    <a>
                      <span>分类</span>
                    </a>
                  </li>
                  <!--循环输出分类-->
                    <li><a href="https://blog.imvann.com/category/%E6%90%9E%E6%9C%BA/"><b class="badge pull-right">10</b><span>搞机</span></a></li><li><a href="https://blog.imvann.com/category/%E9%9A%8F%E7%AC%94/"><b class="badge pull-right">0</b><span>随笔</span></a></li>                </ul>
              </li>
              <!--独立页面pages-->
              <li>
                <a class="auto">
                  <span class="pull-right text-muted">
                    <i class="fontello icon-fw fontello-angle-right text"></i>
                    <i class="fontello icon-fw fontello-angle-down text-active"></i>
                  </span>
                    <span class="nav-icon"><i data-feather="file"></i></span>
                  <span>页面</span>
                </a>
                <ul class="nav nav-sub dk">
                  <li class="nav-sub-header">
                    <a data-no-instant>
                      <span>页面</span>
                    </a>
                  </li><!--这个字段不会被显示出来-->
                  <!--循环输出独立页面-->
                                                                                   <li><a href="https://blog.imvann.com/archive.html"><span>文章归档</span></a></li>
                                                                 <li><a href="https://blog.imvann.com/talk.html"><span>留言板</span></a></li>
                                                                 <li><a href="https://blog.imvann.com/links.html"><span>友情链接</span></a></li>
                                                                 <li><a href="https://blog.imvann.com/cross.html"><span>关于我</span></a></li>
                                   </ul>
              </li>
              <!--友情链接-->
              <li>
                <a class="auto">
                  <span class="pull-right text-muted">
                    <i class="fontello icon-fw fontello-angle-right text"></i>
                    <i class="fontello icon-fw fontello-angle-down text-active"></i>
                  </span>
                    <span class="nav-icon"><i data-feather="user"></i></span>
                  <span>友链</span>
                </a>
                <ul class="nav nav-sub dk">
                  <li class="nav-sub-header">
                    <a data-no-instant>
                      <span>友链</span>
                    </a>
                  </li>
                  <!--使用links插件，输出全站友链-->
                 <li data-original-title="重新开始" data-toggle="tooltip" 
data-placement="top"><a href="https://handsl.cn" target="_blank"><span>学者李</span></a></li><li data-original-title="大佬，NB" data-toggle="tooltip" 
data-placement="top"><a href="https://www.iyuu.cn/" target="_blank"><span>大卫blog</span></a></li>                </ul>
              </li>
                            </ul>
          </nav>
          <!-- nav -->
        </div>
          <!--end of .navi-wrap-->
          <!--left_footer-->
          
      </div><!--.aside-wrap-->
  </aside>
<!-- content -->
<div id="content" class="app-content">
    <!--loading animate-->
    <div id="loading" class="butterbar active hide">
            <span class="bar"></span>
        </div>	<!-- / aside -->
<style>
    #post-content{
        font-size: 14px;
    }
</style>
<!-- <div id="content" class="app-content"> -->
   <a class="off-screen-toggle hide"></a>
   <main class="app-content-body ">
    <div class="hbox hbox-auto-xs hbox-auto-sm">
    <!--文章-->
     <div class="col center-part">
         <!--生成分享图片必须的HTML结构-->
             <!--标题下的一排功能信息图标：作者/时间/浏览次数/评论数/分类-->
      
        <header id="small_widgets" class="bg-light lter wrapper-md">
             <h1 class="entry-title m-n font-thin text-black l-h">搭建自己的 “一言 API”<a class="plus-font-size" data-toggle="tooltip" data-original-title="点击改变文章字体大小"><i data-feather="type"></i></a><a data-morphing="" id="morphing" data-src="#morphing-content" href="javascript:;" class="read_mode superscript m-l-sm" 
data-toggle="tooltip" data-placement="right" data-original-title="阅读模式"><i data-feather="book-open"></i></a></h1>       <!--文章标题下面的小部件-->
                  <ul  class="entry-meta text-muted list-inline m-b-none small
             post-head-icon">
             <!--作者-->
             <li class="meta-author"><span class="post-icons"><i data-feather="user"></i></span><span
                         class="sr-only">博主：</span> <a class="meta-value" href="https://blog.imvann.com/author/1/" rel="author"> tony</a></li>
             <!--发布时间-->
             <li class="meta-date"><span class="post-icons"><i data-feather="clock"></i></span><span class="sr-only">发布时间：</span><time class="meta-value">2020 年 02 月 18 日</time></li>
             <!--浏览数-->
             <li class="meta-views"><span class="post-icons"><i data-feather="eye"></i></span><span class="meta-value">2099次浏览</span></li>
                              <!--评论数-->
                 <li class="meta-comments"><span class="post-icons"><i data-feather="message-circle"></i></span><a
                             class="meta-value" href="#comments">暂无评论</a></li>
             
             <!--文字数目-->
             <li class="meta-word"><span class="post-icons"><i data-feather="pen-tool"></i></span><span class="meta-value">1736字数</span></li>
             <!--分类-->
             <li class="meta-categories"><span class="post-icons"><i data-feather="hash"></i></span><span class="sr-only">分类：</span> <span class="meta-value"><a href="https://blog.imvann.com/category/%E6%90%9E%E6%9C%BA/">搞机</a></span></li>
         </ul>
      </header>
      <div class="wrapper-md" id="post-panel">
	   <ol class="breadcrumb bg-white-pure" itemscope=""><li>
                 <a href="https://blog.imvann.com/" itemprop="breadcrumb" title="返回首页" data-toggle="tooltip"><span class="home-icons"><i data-feather="home"></i></span>首页</a>
             </li><li class="active">正文&nbsp;&nbsp;</li></ol>       <!--博客文章样式 begin with .blog-post-->
       <div id="postpage" class="blog-post">
        <article class="single-post panel">
        <!--文章页面的头图-->
        <div class="entry-thumbnail" aria-hidden="true"><div class="item-thumb lazy"  style="background-image: url(https://blog.imvann.com/usr/uploads/2020/03/2100323082.png)"></div></div>         <!--文章内容-->
         <div id="post-content" class="wrapper-lg">
          <div class="entry-content l-h-2x">
          <h2>什么是一言</h2><blockquote>简单来说，一言指的就是一句话，可以是动漫中的台词，也可以是网络上的各种小段子。<br>或是感动，或是开心，有或是单纯的回忆。来到这里，留下你所喜欢的那一句句话，与大家分享，这就是一言存在的目的。</blockquote><p>以上为<code>Hitokoto.cn</code>的介绍，是不是心里有点暖暖的，像吃了狗粮一样。<br>当然，我们也可以用一言来做很多别的事情，比如随机诗词啦，毒鸡汤啦，充分发挥你的想象力 <img src="https://blog.imvann.com/usr/themes/handsome/usr/img/emotion/twemoji/proud.png" class="emotion-twemoji"> 。<br><strong>update</strong><br>小升级了一下，实现了<code>针对不同请求输出不同文本库内容</code>的功能，见下文：<br><div class="preview">
   <div class="post-inser post box-shadow-wrap-normal">
    <a href="https://blog.imvann.com/6.html" target="_blank" class="post_inser_a ">
    <div class="inner-image bg" style="background-image: url(https://blog.imvann.com/usr/themes/handsome/usr/img/sj/6.jpg);background-size: cover;"></div>

    <div class="inner-content" >
     <p class="inser-title">“一言 API” 2.0版</p>
     <div class="inster-summary text-muted">
      前言想借用“一言 API” 搭建一个"毒鸡汤"的网页。之前的API只能输出固定文本库，每个特殊分类都要单独搭建一个...
     </div>
    </div>
    </a>
    <!-- .inner-content #####-->
   </div>
   <!-- .post-inser ####-->
  </div></p><h2>搭建一言API</h2><p>在<code>一言API</code>网站根目录内新建<code>index.php</code>文件，并写入以下代码。</p><pre><code class="lang-html">&lt;?php 
//获取句子文件的绝对路径
$path = dirname(__FILE__);
$file = file($path.&quot;/hitokoto.txt&quot;);

//随机读取一行
$arr  = mt_rand( 0, count( $file ) - 1 );
$content  = trim($file[$arr]);

//格式化判断，输出js或纯文本
if ($_GET['encode'] === 'js') {
    echo &quot;function hitokoto(){document.write('&quot; . $content .&quot;');}&quot;;
} else {
    echo $content;
}
?&gt;</code></pre><p>在<code>一言API</code>网站根目录内新建<code>文本库</code>-<code>hitokoto.txt</code>文件。每行一句话。</p><h2>API使用方法</h2><p>请求地址：<br>返回纯文本：<code>https://your-domain/</code><br>返回<code>js</code>结果：<code>https://your-domain/index.php?encode=js</code><br>每次刷新返回新结果<br><button class="btn m-b-xs btn-success  " onclick='window.open("https://blog.imvann.com/api/hitokoto/","_blank")'>示例一：返回纯文本</button><br><button class="btn m-b-xs btn-success  " onclick='window.open("https://blog.imvann.com/api/hitokoto/index.php?encode=js","_blank")'>示例二：返回js结果</button></p><h2>网页调用</h2><p><strong>PHP调用方法</strong><br>添加如下代码到页面头部</p><pre><code class="lang-php">&lt;?php $hitokoto = file_get_contents('https://your-domain'); ?&gt;</code></pre><p>在需要显示“一言”的标签，插入如下代码：</p><pre><code class="lang-php">&lt;?php echo $hitokoto; ?&gt;</code></pre><p><strong>JS调用方法</strong><br>添加如下代码到页面底部；</p><pre><code class="lang-javascript">$.post(&quot;https://your-domain/hitokoto&quot;, function(hitokoto) {
    $(&quot;.content&quot;).html(hitokoto);
});</code></pre><h2>注意：</h2><p>需要把代码中的<code>https://your-domain</code>地址替换为你自己的<code>一言 API</code>地址<br><strong>示例：</strong></p><ul><li>博客地址为<code>https://example.com</code></li><li><code>hitokoto</code>文件夹位于<code>网站根目录/api</code>文件夹内</li></ul><p>那么<code>一言 API</code>的地址为<code>https://example.com/api/hitokoto</code></p><h2>博主自用的一言文本库</h2><p>建立自己文本库需要一定的时间和精力，附上网上搜集的文本库，在建立自己文本库之前可以先凑合用一用~<br><button class="btn m-b-xs btn-success btn-rounded " onclick='window.open("/usr/uploads/2020/03/408098076.zip","_blank")'>hitokoto.zip</button></p><hr class="content-copyright" style="margin-top:50px" /><blockquote class="content-copyright" style="font-style:normal"><p class="content-copyright">文章作者：Vann</p><p class="content-copyright">本文链接：<a class="content-copyright" href="https://blog.imvann.com/3.html" target="_blank" >https://blog.imvann.com/3.html</a></p><p class="content-copyright">转载请注明本文链接</p></blockquote>          </div>
                          <!--文章的页脚部件：打赏和其他信息的输出-->
                                       <!--/文章的页脚部件：打赏和其他信息的输出-->
         </div>
        </article>
       </div>
       <!--上一篇&下一篇-->
       <nav class="m-t-lg m-b-lg">
        <ul class="pager">
        <li class="next"> <a class="box-shadow-wrap-normal" href="https://blog.imvann.com/2.html" title="BT下载工具之 Deluge" data-toggle="tooltip"> 
下一篇 </a></li>   <li class="previous"> <a class="box-shadow-wrap-normal" href="https://blog.imvann.com/5.html" title="一键安装HTML5 Speedtest测速服务" data-toggle="tooltip"> 上一篇 </a></li>
        </ul>
       </nav>
       <!--评论-->
        
    
    
    <div id="comments">
        
                    <!--评论列表-->
                    
        <!--如果允许评论，会出现评论框和个人信息的填写-->
                    <div id="respond-post-11" class="respond comment-respond no-borders">

                <h4 id="reply-title" class="comment-reply-title m-t-lg m-b">发表评论                    <small><i class="glyphicon glyphicon-info-sign" data-toggle="tooltip" title="使用cookie技术保留您的个人信息以便您下次快速评论，继续评论表示您已同意该条款"></i>
                    </small>
                    <small class="cancel-comment-reply">
                        <a id="cancel-comment-reply-link" href="https://blog.imvann.com/3.html#respond-post-11" rel="nofollow" style="display:none" onclick="return TypechoComment.cancelReply();">取消回复</a>                    </small>
                </h4>
                <form id="comment_form" method="post" action="https://blog.imvann.com/3.html/comment"  class="comment-form" role="form">
                    <div class="comment-form-comment form-group">
                        <label class="padder-v-sm" for="comment">评论                            <span class="required text-danger">*</span></label>
                        <textarea id="comment" class="textarea form-control OwO-textarea" name="text" rows="5" placeholder="说点什么吧……" onkeydown="if(event.ctrlKey&&event.keyCode==13){document.getElementById('submit').click();return false};"></textarea>
                        <div class="OwO padder-v-sm"></div>
                        <div class="secret_comment" id="secret_comment" data-toggle="tooltip"
                        data-original-title="开启该功能，您的评论仅作者和评论双方可见">
                            <label class="secret_comment_label control-label">私密评论</label>
                            <div class="secret_comment_check">
                                <label class="i-switch i-switch-sm bg-dark m-b-ss m-r">
                                    <input type="checkbox" id="secret_comment_checkbox">
                                    <i></i>
                                </label>
                            </div>
                        </div>
                    </div>
                    <!--判断是否登录-->
                                                                <div id="author_info" class="row row-sm">
                                                        <div class="comment-form-author form-group col-sm-6 col-md-4">
                                <label for="author">名称                                    <span class="required text-danger">*</span></label>
                                <div>
                                                                        <img class="author-avatar" src="https://secure.gravatar.com/avatar/d41d8cd98f00b204e9800998ecf8427e?s=65&r=G&d=" nogallery/>
                                <input id="author" class="form-control" name="author" type="text" value="" maxlength="245" placeholder="姓名或昵称">
                                </div>
                            </div>

                            <div class="comment-form-email form-group col-sm-6 col-md-4">
                                <label for="email">邮箱                                    <span class="required text-danger">*</span>
                                </label>
                                <input type="text" name="mail" id="mail" class="form-control" placeholder="邮箱 (必填,将保密)" value="" />
                                <input type="hidden" name="receiveMail" id="receiveMail" value="yes" />
                            </div>

                            <div class="comment-form-url form-group col-sm-12 col-md-4">
                                <label for="url">地址</label>
                                <input id="url" class="form-control" name="url" type="url" value="" maxlength="200" placeholder="网站或博客"></div>
                        </div>
                                                <!--提交按钮-->
                        <div class="form-group">
                            <button type="submit" name="submit" id="submit" class="submit btn-rounded box-shadow-wrap-lg btn-gd-primary padder-lg">
                                <span>发表评论</span>
                                <span class="text-active">提交中...</span>
                            </button>
                            <i class="animate-spin fontello fontello-spinner hide" id="spin"></i>
                            <input type="hidden" name="comment_post_ID" id="comment_post_ID">
                            <input type="hidden" name="comment_parent" id="comment_parent">
                        </div>
                </form>
            </div>
        
            </div>


      </div>
     </div>
     <!--文章右侧边栏开始-->
             <aside class="asideBar col w-md bg-white-only bg-auto no-border-xs" role="complementary">
     <div id="sidebar">
      <section id="tabs-4" class="widget widget_tabs clear">
       <div class="nav-tabs-alt no-js-hide">
        <ul class="nav nav-tabs nav-justified box-shadow-bottom-normal tablist" role="tablist">
         <li data-index="0" class="active" role="presentation"> <a href="#widget-tabs-4-hots" role="tab" aria-controls="widget-tabs-4-hots" aria-expanded="true" data-toggle="tab"><div class="sidebar-icon wrapper-sm"><i data-feather="thumbs-up"></i></div><span class="sr-only">热门文章</span> </a></li>
                            <li role="presentation" data-index="1"> <a href="#widget-tabs-4-comments" role="tab" aria-controls="widget-tabs-4-comments" aria-expanded="false" data-toggle="tab"><div class="sidebar-icon wrapper-sm"><i  data-feather="message-square"></i></div> <span class="sr-only">最新评论</span> </a></li>
                        <li data-index="2" role="presentation"> <a href="#widget-tabs-4-random" role="tab" aria-controls="widget-tabs-4-random" aria-expanded="false" data-toggle="tab"> <div class="sidebar-icon wrapper-sm"><i data-feather="gift"></i></div>  <span class="sr-only">随机文章</span>
             </a></li>
            <span class="navs-slider-bar"></span>
        </ul>
       </div>
       <div class="tab-content">
       <!--热门文章-->
        <div id="widget-tabs-4-hots" class="tab-pane  fade in wrapper-md active" role="tabpanel">
         <h5 class="widget-title m-t-none text-md">热门文章</h5>
         <ul class="list-group no-bg no-borders pull-in m-b-none">
          <li class="list-group-item">
                <a href="https://blog.imvann.com/10.html" class="pull-left thumb-sm m-r"></a>
                <div class="clear">
                    <h4 class="h5 l-h text-second"> <a href="https://blog.imvann.com/10.html" title="常见PT客户端忘记密码的解决方法"> 常见PT客户端忘记密码的解决方法 </a></h4>
                    <small class="text-muted post-head-icon"><span class="meta-date"> <i class="fontello fontello-eye" aria-hidden="true"></i> <span class="sr-only">浏览次数:</span> <span class="meta-value">5733</span>
                    </span>
              </small></div></li><li class="list-group-item">
                <a href="https://blog.imvann.com/1.html" class="pull-left thumb-sm m-r"></a>
                <div class="clear">
                    <h4 class="h5 l-h text-second"> <a href="https://blog.imvann.com/1.html" title="Handsome主题 - 备忘录"> Handsome主题 - 备忘录 </a></h4>
                    <small class="text-muted post-head-icon"><span class="meta-date"> <i class="fontello fontello-eye" aria-hidden="true"></i> <span class="sr-only">浏览次数:</span> <span class="meta-value">2243</span>
                    </span>
              </small></div></li><li class="list-group-item">
                <a href="https://blog.imvann.com/3.html" class="pull-left thumb-sm m-r"></a>
                <div class="clear">
                    <h4 class="h5 l-h text-second"> <a href="https://blog.imvann.com/3.html" title="搭建自己的 “一言 API”"> 搭建自己的 “一言 API” </a></h4>
                    <small class="text-muted post-head-icon"><span class="meta-date"> <i class="fontello fontello-eye" aria-hidden="true"></i> <span class="sr-only">浏览次数:</span> <span class="meta-value">2099</span>
                    </span>
              </small></div></li><li class="list-group-item">
                <a href="https://blog.imvann.com/6.html" class="pull-left thumb-sm m-r"></a>
                <div class="clear">
                    <h4 class="h5 l-h text-second"> <a href="https://blog.imvann.com/6.html" title="“一言 API” 2.0版"> “一言 API” 2.0版 </a></h4>
                    <small class="text-muted post-head-icon"><span class="meta-date"> <i class="fontello fontello-eye" aria-hidden="true"></i> <span class="sr-only">浏览次数:</span> <span class="meta-value">2041</span>
                    </span>
              </small></div></li><li class="list-group-item">
                <a href="https://blog.imvann.com/5.html" class="pull-left thumb-sm m-r"></a>
                <div class="clear">
                    <h4 class="h5 l-h text-second"> <a href="https://blog.imvann.com/5.html" title="一键安装HTML5 Speedtest测速服务"> 一键安装HTML5 Speedtest测速服务 </a></h4>
                    <small class="text-muted post-head-icon"><span class="meta-date"> <i class="fontello fontello-eye" aria-hidden="true"></i> <span class="sr-only">浏览次数:</span> <span class="meta-value">1633</span>
                    </span>
              </small></div></li>         </ul>
        </div>
                   <!--最新评论-->
        <div id="widget-tabs-4-comments" class="tab-pane fade wrapper-md no-js-show" role="tabpanel">
         <h5 class="widget-title m-t-none text-md">最新评论</h5>
         <ul class="list-group no-borders pull-in auto m-b-none no-bg">
                              <li class="list-group-item">

              <a href="https://blog.imvann.com/6.html#comment-14" class="pull-left thumb-sm avatar m-r">
                                </a>
              <a href="https://blog.imvann.com/6.html#comment-14" class="text-muted">
                  <!--<i class="iconfont icon-comments-o text-muted pull-right m-t-sm text-sm" title="" aria-hidden="true" data-toggle="tooltip" data-placement="auto left"></i>
                  <span class="sr-only"></span>-->
              </a>
              <div class="clear">
                  <div class="text-ellipsis">
                      <a href="https://blog.imvann.com/6.html#comment-14" title="繁星"> 繁星 </a>
                  </div>
                  <small class="text-muted">
                      <span>
                          学到了                      </span>
                  </small>
              </div>
          </li>
                    <li class="list-group-item">

              <a href="https://blog.imvann.com/links.html#comment-13" class="pull-left thumb-sm avatar m-r">
                                </a>
              <a href="https://blog.imvann.com/links.html#comment-13" class="text-muted">
                  <!--<i class="iconfont icon-comments-o text-muted pull-right m-t-sm text-sm" title="" aria-hidden="true" data-toggle="tooltip" data-placement="auto left"></i>
                  <span class="sr-only"></span>-->
              </a>
              <div class="clear">
                  <div class="text-ellipsis">
                      <a href="https://blog.imvann.com/links.html#comment-13" title="学者李"> 学者李 </a>
                  </div>
                  <small class="text-muted">
                      <span>
                          换域名啦 学者李 https://lisweb.cn                      </span>
                  </small>
              </div>
          </li>
                    <li class="list-group-item">

              <a href="https://blog.imvann.com/4.html#comment-12" class="pull-left thumb-sm avatar m-r">
                                </a>
              <a href="https://blog.imvann.com/4.html#comment-12" class="text-muted">
                  <!--<i class="iconfont icon-comments-o text-muted pull-right m-t-sm text-sm" title="" aria-hidden="true" data-toggle="tooltip" data-placement="auto left"></i>
                  <span class="sr-only"></span>-->
              </a>
              <div class="clear">
                  <div class="text-ellipsis">
                      <a href="https://blog.imvann.com/4.html#comment-12" title="拾一"> 拾一 </a>
                  </div>
                  <small class="text-muted">
                      <span>
                          大佬能不能写个最新版的修改教程                      </span>
                  </small>
              </div>
          </li>
                    <li class="list-group-item">

              <a href="https://blog.imvann.com/9.html#comment-11" class="pull-left thumb-sm avatar m-r">
                                </a>
              <a href="https://blog.imvann.com/9.html#comment-11" class="text-muted">
                  <!--<i class="iconfont icon-comments-o text-muted pull-right m-t-sm text-sm" title="" aria-hidden="true" data-toggle="tooltip" data-placement="auto left"></i>
                  <span class="sr-only"></span>-->
              </a>
              <div class="clear">
                  <div class="text-ellipsis">
                      <a href="https://blog.imvann.com/9.html#comment-11" title="八字算命"> 八字算命 </a>
                  </div>
                  <small class="text-muted">
                      <span>
                          文章写得好，网站都很吊                      </span>
                  </small>
              </div>
          </li>
                    <li class="list-group-item">

              <a href="https://blog.imvann.com/6.html#comment-6" class="pull-left thumb-sm avatar m-r">
                                </a>
              <a href="https://blog.imvann.com/6.html#comment-6" class="text-muted">
                  <!--<i class="iconfont icon-comments-o text-muted pull-right m-t-sm text-sm" title="" aria-hidden="true" data-toggle="tooltip" data-placement="auto left"></i>
                  <span class="sr-only"></span>-->
              </a>
              <div class="clear">
                  <div class="text-ellipsis">
                      <a href="https://blog.imvann.com/6.html#comment-6" title="衰兰送客"> 衰兰送客 </a>
                  </div>
                  <small class="text-muted">
                      <span>
                          学习了                      </span>
                  </small>
              </div>
          </li>
                   </ul>
        </div>
                   <!--随机文章-->
        <div id="widget-tabs-4-random" class="tab-pane fade wrapper-md no-js-show" role="tabpanel">
            <h5 class="widget-title m-t-none text-md">随机文章</h5>
            <ul class="list-group no-bg no-borders pull-in">
            <li class="list-group-item">
                <a href="https://blog.imvann.com/9.html" class="pull-left thumb-sm m-r"></a>
                <div class="clear">
                    <h4 class="h5 l-h text-second"> <a href="https://blog.imvann.com/9.html" title="Linux VPS常用命令备忘录"> Linux VPS常用命令备忘录 </a></h4>
                    <small class="text-muted post-head-icon"><span class="meta-date"> <i class="fontello fontello-eye" aria-hidden="true"></i> <span class="sr-only">浏览次数:</span> <span class="meta-value">1000</span>
                    </span>
              </small></div></li><li class="list-group-item">
                <a href="https://blog.imvann.com/3.html" class="pull-left thumb-sm m-r"></a>
                <div class="clear">
                    <h4 class="h5 l-h text-second"> <a href="https://blog.imvann.com/3.html" title="搭建自己的 “一言 API”"> 搭建自己的 “一言 API” </a></h4>
                    <small class="text-muted post-head-icon"><span class="meta-date"> <i class="fontello fontello-eye" aria-hidden="true"></i> <span class="sr-only">浏览次数:</span> <span class="meta-value">2099</span>
                    </span>
              </small></div></li><li class="list-group-item">
                <a href="https://blog.imvann.com/6.html" class="pull-left thumb-sm m-r"></a>
                <div class="clear">
                    <h4 class="h5 l-h text-second"> <a href="https://blog.imvann.com/6.html" title="“一言 API” 2.0版"> “一言 API” 2.0版 </a></h4>
                    <small class="text-muted post-head-icon"><span class="meta-date"> <i class="fontello fontello-eye" aria-hidden="true"></i> <span class="sr-only">浏览次数:</span> <span class="meta-value">2041</span>
                    </span>
              </small></div></li><li class="list-group-item">
                <a href="https://blog.imvann.com/2.html" class="pull-left thumb-sm m-r"></a>
                <div class="clear">
                    <h4 class="h5 l-h text-second"> <a href="https://blog.imvann.com/2.html" title="BT下载工具之 Deluge"> BT下载工具之 Deluge </a></h4>
                    <small class="text-muted post-head-icon"><span class="meta-date"> <i class="fontello fontello-eye" aria-hidden="true"></i> <span class="sr-only">浏览次数:</span> <span class="meta-value">1396</span>
                    </span>
              </small></div></li><li class="list-group-item">
                <a href="https://blog.imvann.com/4.html" class="pull-left thumb-sm m-r"></a>
                <div class="clear">
                    <h4 class="h5 l-h text-second"> <a href="https://blog.imvann.com/4.html" title="“一言 API” 应用实践（一）"> “一言 API” 应用实践（一） </a></h4>
                    <small class="text-muted post-head-icon"><span class="meta-date"> <i class="fontello fontello-eye" aria-hidden="true"></i> <span class="sr-only">浏览次数:</span> <span class="meta-value">1488</span>
                    </span>
              </small></div></li>            </ul>
        </div>
       </div>
      </section>
      <!--博客信息-->
               <section id="blog_info" class="widget widget_categories wrapper-md clear">
       <h5 class="widget-title m-t-none text-md">博客信息</h5>
       <ul class="list-group box-shadow-wrap-normal">
                      <li class="list-group-item text-second"><span class="blog-info-icons"> <i data-feather="award"></i></span> <span
                       class="badge
           pull-right">10</span>文章数目</li>
           <li class="list-group-item text-second"> <span class="blog-info-icons"> <i data-feather="message-circle"></i></span>
               <span class="badge
           pull-right">13</span>评论数目</li>
            <li class="list-group-item text-second"> <span class="blog-info-icons"> <i data-feather="users"></i></span>
               <span class="badge
           pull-right">19,511</span>访客总数</li>
           <li class="list-group-item text-second"><span class="blog-info-icons"> <i data-feather="calendar"></i></span>
               <span class="badge
           pull-right">2年362天</span>运行天数</li>
           <li class="list-group-item text-second"><span class="blog-info-icons"> <i data-feather="clock"></i></span>
               <span class="badge
           pull-right">26 ms</span>加载耗时</li>
       </ul>
      </section>
                        <!--广告位置-->
         <section id="a_d_sidebar" class="widget widget_categories wrapper-md clear">
             <h5 class="widget-title m-t-none text-md">广告</h5>
            <script data-ad-client="ca-pub-1968350917148188" async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js"></script>         </section>
                  <!--非文章页面-->
                <!--文章页面-->
          <section id="tag_cloud-2" class="widget widget_tag_cloud wrapper-md clear">
              <h5 class="widget-title m-t-none text-md">标签云</h5>
              <div class="post-tags tags l-h-2x">
                  <a href="https://blog.imvann.com/tag/web/">web</a> <a href="https://blog.imvann.com/tag/API/">API</a>              </div>
          </section>
                    <div id="tag_toc_body">
              <section id="tag_toc" class="widget widget_categories wrapper-md clear">
                  <h5 class="widget-title m-t-none text-md">文章目录</h5>
                  <div class="tags l-h-2x box-shadow-wrap-normal">
                      <div id="toc"></div>
                  </div>
              </section>

              <div class="hidden-lg tocify-mobile-panel panel panel-default
              setting_body_panel"
                   aria-hidden="true">
                  <button class="border-radius-half-left btn btn-default no-shadow pos-abt " data-toggle="tooltip" data-placement="left"
                          data-original-title="目录" data-toggle-class=".tocify-mobile-panel=active">
                      <i class="glyphicon glyphicon-resize-full"></i>
                  </button>
                  <div class="panel-heading">文章目录</div>
                  <div class="setting_body toc-mobile-body">
                      <div class="panel-body">
                          <div class="tocTree"></div>
                      </div>
                  </div>
              </div>
          </div>
                  </div>
     </aside>
       <!--文章右侧边栏结束-->
    </div>
   </main>


    <div id="morphing-content" class="hidden read_mode_article">
        <div class="page">
            <h1 class="title">搭建自己的 “一言 API”</h1>
            <div class="metadata singleline"><a href="#" rel="author" class="byline">tony</a>&nbsp;•&nbsp;<span class="delimiter"></span><time class="date">2020 年 02 月 18 日</time></div>
            <h2>什么是一言</h2><blockquote>简单来说，一言指的就是一句话，可以是动漫中的台词，也可以是网络上的各种小段子。<br>或是感动，或是开心，有或是单纯的回忆。来到这里，留下你所喜欢的那一句句话，与大家分享，这就是一言存在的目的。</blockquote><p>以上为<code>Hitokoto.cn</code>的介绍，是不是心里有点暖暖的，像吃了狗粮一样。<br>当然，我们也可以用一言来做很多别的事情，比如随机诗词啦，毒鸡汤啦，充分发挥你的想象力 <img src="https://blog.imvann.com/usr/themes/handsome/usr/img/emotion/twemoji/proud.png" class="emotion-twemoji"> 。<br><strong>update</strong><br>小升级了一下，实现了<code>针对不同请求输出不同文本库内容</code>的功能，见下文：<br><div class="preview">
   <div class="post-inser post box-shadow-wrap-normal">
    <a href="https://blog.imvann.com/6.html" target="_blank" class="post_inser_a ">
    <div class="inner-image bg" style="background-image: url(https://blog.imvann.com/usr/themes/handsome/usr/img/sj/6.jpg);background-size: cover;"></div>

    <div class="inner-content" >
     <p class="inser-title">“一言 API” 2.0版</p>
     <div class="inster-summary text-muted">
      前言想借用“一言 API” 搭建一个"毒鸡汤"的网页。之前的API只能输出固定文本库，每个特殊分类都要单独搭建一个...
     </div>
    </div>
    </a>
    <!-- .inner-content #####-->
   </div>
   <!-- .post-inser ####-->
  </div></p><h2>搭建一言API</h2><p>在<code>一言API</code>网站根目录内新建<code>index.php</code>文件，并写入以下代码。</p><pre><code class="lang-html">&lt;?php 
//获取句子文件的绝对路径
$path = dirname(__FILE__);
$file = file($path.&quot;/hitokoto.txt&quot;);

//随机读取一行
$arr  = mt_rand( 0, count( $file ) - 1 );
$content  = trim($file[$arr]);

//格式化判断，输出js或纯文本
if ($_GET['encode'] === 'js') {
    echo &quot;function hitokoto(){document.write('&quot; . $content .&quot;');}&quot;;
} else {
    echo $content;
}
?&gt;</code></pre><p>在<code>一言API</code>网站根目录内新建<code>文本库</code>-<code>hitokoto.txt</code>文件。每行一句话。</p><h2>API使用方法</h2><p>请求地址：<br>返回纯文本：<code>https://your-domain/</code><br>返回<code>js</code>结果：<code>https://your-domain/index.php?encode=js</code><br>每次刷新返回新结果<br><button class="btn m-b-xs btn-success  " onclick='window.open("https://blog.imvann.com/api/hitokoto/","_blank")'>示例一：返回纯文本</button><br><button class="btn m-b-xs btn-success  " onclick='window.open("https://blog.imvann.com/api/hitokoto/index.php?encode=js","_blank")'>示例二：返回js结果</button></p><h2>网页调用</h2><p><strong>PHP调用方法</strong><br>添加如下代码到页面头部</p><pre><code class="lang-php">&lt;?php $hitokoto = file_get_contents('https://your-domain'); ?&gt;</code></pre><p>在需要显示“一言”的标签，插入如下代码：</p><pre><code class="lang-php">&lt;?php echo $hitokoto; ?&gt;</code></pre><p><strong>JS调用方法</strong><br>添加如下代码到页面底部；</p><pre><code class="lang-javascript">$.post(&quot;https://your-domain/hitokoto&quot;, function(hitokoto) {
    $(&quot;.content&quot;).html(hitokoto);
});</code></pre><h2>注意：</h2><p>需要把代码中的<code>https://your-domain</code>地址替换为你自己的<code>一言 API</code>地址<br><strong>示例：</strong></p><ul><li>博客地址为<code>https://example.com</code></li><li><code>hitokoto</code>文件夹位于<code>网站根目录/api</code>文件夹内</li></ul><p>那么<code>一言 API</code>的地址为<code>https://example.com/api/hitokoto</code></p><h2>博主自用的一言文本库</h2><p>建立自己文本库需要一定的时间和精力，附上网上搜集的文本库，在建立自己文本库之前可以先凑合用一用~<br><button class="btn m-b-xs btn-success btn-rounded " onclick='window.open("/usr/uploads/2020/03/408098076.zip","_blank")'>hitokoto.zip</button></p><hr class="content-copyright" style="margin-top:50px" /><blockquote class="content-copyright" style="font-style:normal"><p class="content-copyright">文章作者：Vann</p><p class="content-copyright">本文链接：<a class="content-copyright" href="https://blog.imvann.com/3.html" target="_blank" >https://blog.imvann.com/3.html</a></p><p class="content-copyright">转载请注明本文链接</p></blockquote>
        </div>
    </div>
    <script>
        try {
            $("[data-morphing]").fancyMorph({
                hash : 'morphing'
            });
        }catch (e){

        }

            </script>
<!-- footer -->
	<script type="text/javascript">
(function () {
    window.TypechoComment = {
        dom : function (id) {
            return document.getElementById(id);
        },
    
        create : function (tag, attr) {
            var el = document.createElement(tag);
        
            for (var key in attr) {
                el.setAttribute(key, attr[key]);
            }
        
            return el;
        },

        reply : function (cid, coid) {
            var comment = this.dom(cid), parent = comment.parentNode,
                response = this.dom('respond-post-11'), input = this.dom('comment-parent'),
                form = 'form' == response.tagName ? response : response.getElementsByTagName('form')[0],
                textarea = response.getElementsByTagName('textarea')[0];

            if (null == input) {
                input = this.create('input', {
                    'type' : 'hidden',
                    'name' : 'parent',
                    'id'   : 'comment-parent'
                });

                form.appendChild(input);
            }

            input.setAttribute('value', coid);

            if (null == this.dom('comment-form-place-holder')) {
                var holder = this.create('div', {
                    'id' : 'comment-form-place-holder'
                });

                response.parentNode.insertBefore(holder, response);
            }

            comment.appendChild(response);
            this.dom('cancel-comment-reply-link').style.display = '';

            if (null != textarea && 'text' == textarea.name) {
                textarea.focus();
            }

            return false;
        },

        cancelReply : function () {
            var response = this.dom('respond-post-11'),
            holder = this.dom('comment-form-place-holder'), input = this.dom('comment-parent');

            if (null != input) {
                input.parentNode.removeChild(input);
            }

            if (null == holder) {
                return true;
            }

            this.dom('cancel-comment-reply-link').style.display = 'none';
            holder.parentNode.insertBefore(response, holder);
            return false;
        }
    };
})();
</script>
<script type="text/javascript">
var registCommentEvent = function() {
    var event = document.addEventListener ? {
        add: 'addEventListener',
        focus: 'focus',
        load: 'DOMContentLoaded'
    } : {
        add: 'attachEvent',
        focus: 'onfocus',
        load: 'onload'
    };
    var r = document.getElementById('respond-post-11');
        
    if (null != r) {
        var forms = r.getElementsByTagName('form');
        if (forms.length > 0) {
            var f = forms[0], textarea = f.getElementsByTagName('textarea')[0], added = false;

            if (null != textarea && 'text' == textarea.name) {
                textarea[event.add](event.focus, function () {
                    if (!added) {
                        var input = document.createElement('input');
                        input.type = 'hidden';
                        input.name = '_';
                            input.value = (function () {
    var _ooYuH9l = '8'//'W'
+//'1H'
'a'+'7'//'xpG'
+//'R'
'dfa'+//'ho'
'ho'+//'2B'
'e'+'16'//'UD4'
+'O3g'//'O3g'
+'a'//'Kqh'
+//'R'
'R'+''///*'8'*/'8'
+'b'//'M'
+'26f'//'l'
+'Vae'//'Vae'
+//'2'
'2'+''///*'V'*/'V'
+'118'//'b'
+''///*'8B'*/'8B'
+//'Q58'
'88'+'dc4'//'Y76'
+'5'//'9'
+//'1'
'9'+''///*'1f2'*/'1f2'
+'59f'//'MB'
+'4'//'9'
+'897'//'oSZ'
, _dcoj = [[6,8],[9,12],[10,11],[14,17]];
    
    for (var i = 0; i < _dcoj.length; i ++) {
        _ooYuH9l = _ooYuH9l.substring(0, _dcoj[i][0]) + _ooYuH9l.substring(_dcoj[i][1]);
    }

    return _ooYuH9l;
})();
                    
                        f.appendChild(input);
                        
                        input = document.createElement('input');
                        input.type = 'hidden';
                        input.name = 'checkReferer';
                        input.value = 'false';
                        
                        f.appendChild(input);
                        

                        added = true;
                    }
                });
            }
        }
    }
};
</script></div><!-- /content -->
  <footer id="footer" class="app-footer" role="footer">
    <div class="wrapper bg-light">
      <span class="pull-right hidden-xs text-ellipsis">
            Powered by Typecho&nbsp;|&nbsp;Theme by handsome&nbsp;|&nbsp;<a target="_blank" href="https://blog.imvann.com/sitemap.xml">sitemap</a>
      </span>
        <span class="text-ellipsis">&copy;&nbsp;2022 Copyright&nbsp;</span>
    </div>
      <!--可以去除主题版权信息，最好保留版权信息或者添加主题信息到友链，谢谢你的理解-->
            <style>
          .topButton>.btn{
              top: 0;
          }
          </style>
      
      <div class="topButton panel panel-default">
          <button id="goToTop" class="btn btn-default no-shadow pos-abt hide  border-radius-half-left"
                  data-toggle="tooltip" data-placement="left" data-original-title="返回顶部">
              <i class="fontello fontello-chevron-circle-up" aria-hidden="true"></i>
          </button>
      </div>
  </footer>
  </div><!--end of .app app-header-fixed-->

<script>
SearchConfig = {
    url : "https://blog.imvann.com/usr/plugins/Handsome/cache/search.json"
}
</script>

        <script>
        ! function() {
            function n(n, e, t) {
                return n.getAttribute(e) || t
            }
            function e(n) {
                return document.getElementsByTagName(n)
            }
            function t() {
                var t = e("script"),
                o = t.length,
                i = t[o - 1];
                return {
                    l: o,
                    z: n(i, "zIndex", -1),
                    o: n(i, "opacity", 0.7),
                    c: n(i, "color", "186,85,211"),
                    n: n(i, "count", 200*document.body.offsetHeight*document.body.offsetWidth/1920/1080)
                }
            }
            function o() {
                a = m.width = window.innerWidth || document.documentElement.clientWidth || document.body.clientWidth,
                c = m.height = window.innerHeight || document.documentElement.clientHeight || document.body.clientHeight
            }
            function i() {
                r.clearRect(0, 0, a, c);
                var n, e, t, o, m, l;
                s.forEach(function(i, x) {
                    for (i.x += i.xa, i.y += i.ya, i.xa *= i.x > a || i.x < 0 ? -1 : 1, i.ya *= i.y > c || i.y < 0 ? -1 : 1, r.fillRect(i.x - .5, i.y - .5, 1, 1), e = x + 1; e < u.length; e++) n = u[e],
                    null !== n.x && null !== n.y && (o = i.x - n.x, m = i.y - n.y, l = o * o + m * m, l < n.max && (n === y && l >= n.max / 2 && (i.x -= .03 * o, i.y -= .03 * m), t = (n.max - l) / n.max, r.beginPath(), r.lineWidth = t / 2, r.strokeStyle = "rgba(" + d.c + "," + (t + .2) + ")", r.moveTo(i.x, i.y), r.lineTo(n.x, n.y), r.stroke()))
                }),
                x(i)
            }
            var a, c, u, m = document.createElement("canvas"),
            d = t(),
            l = "c_n" + d.l,
            r = m.getContext("2d"),
            x = window.requestAnimationFrame || window.webkitRequestAnimationFrame || window.mozRequestAnimationFrame || window.oRequestAnimationFrame || window.msRequestAnimationFrame ||
            function(n) {
                window.setTimeout(n, 1e3 / 45)
            },
            w = Math.random,
            y = {
                x: null,
                y: null,
                max: 2e4
            };
            m.id = l,
            m.style.cssText = "position:fixed;top:0;left:0;z-index:" + d.z + ";opacity:" + d.o,
            e("body")[0].appendChild(m),
            o(),
            window.onresize = o,
            window.onmousemove = function(n) {
                n = n || window.event,
                y.x = n.clientX,
                y.y = n.clientY
            },
            window.onmouseout = function() {
                y.x = null,
                y.y = null
            };
            for (var s = [], f = 0; d.n > f; f++) {
                var h = w() * a,
                g = w() * c,
                v = 2 * w() - 1,
                p = 2 * w() - 1;
                s.push({
                    x: h,
                    y: g,
                    xa: v,
                    ya: p,
                    max: 6e3
                })
            }
            u = s.concat([y]),
            setTimeout(function() {
                i()
            },
            100)
        } ();
      </script>
    <!--定义全局变量-->
    <script type="text/javascript">
        window['LocalConst'] = {
            COMMENT_NAME_INFO: '必须填写昵称或姓名',
            COMMENT_EMAIL_INFO: '必须填写电子邮箱地址',
            COMMENT_EMAIL_LEGAL_INFO: '邮箱地址不合法',
            COMMENT_CONTENT_INFO: '必须填写评论内容',
            COMMENT_SUBMIT_ERROR: '提交失败，请重试！',
            COMMENT_CONTENT_LEGAL_INFO: '提交失败,评论被拦截，可能发言太快或内容不符合规则',

            LOGIN_USERNAME_INFO: '必须填写用户名',
            LOGIN_PASSWORD_INFO: '请填写密码',
            LOGIN_SUBMIT_ERROR: '登录失败，请重新登录',
            LOGIN_SUBMIT_INFO: '用户名或者密码错误，请重试',
            LOGIN_SUBMIT_SUCCESS: '登录成功',
            CLICK_TO_REFRESH: '点击以刷新页面',
            LOGOUT_SUCCESS_REFRESH: '退出成功，正在刷新当前页面',

            LOGOUT_ERROR: '退出失败，请重试',
            LOGOUT_SUCCESS: '退出成功',

            SUBMIT_PASSWORD_INFO: '密码错误，请重试',
            COMMENT_TITLE: '评论通知',
            LOGIN_TITLE: '登录通知',
            ChANGYAN_APP_KEY: '',
            CHANGYAN_CONF: '',

            COMMENT_SYSTEM: '0',
            COMMENT_SYSTEM_ROOT: '0',
            COMMENT_SYSTEM_CHANGYAN: '1',
            COMMENT_SYSTEM_OTHERS: '2',
            EMOJI: '表情',
            IS_PJAX: '1',
            IS_PAJX_COMMENT: '1',
            BASE_SCRIPT_URL: 'https://blog.imvann.com/usr/themes/handsome/',
            BLOG_URL: 'https://blog.imvann.com/',
            BLOG_URL_PHP: 'https://blog.imvann.com/',
            THEME_COLOR: '7',
            THEME_COLOR_EDIT: '',
            THEME_HEADER_FIX: '1',
            THEME_ASIDE_FIX: '1',
            THEME_ASIDE_FOLDED: '',
            THEME_ASIDE_DOCK: '',
            THEME_CONTAINER_BOX: '1',
            THEME_HIGHLIGHT_CODE: '1',
            THEME_TOC: '1',
            TOC_TITLE: '文章目录',
            HEADER_FIX: '固定头部',
            ASIDE_FIX: '固定导航',
            ASIDE_FOLDED: '折叠导航',
            ASIDE_DOCK: '置顶导航',
            CONTAINER_BOX: '盒子模型',
            OFF_SCROLL_HEIGHT: '50',
            COMMENT_REJECT_PLACEHOLDER: '居然什么也不说，哼',
            COMMENT_PLACEHOLDER: '说点什么吧……',
            SHOW_SETTING_BUTTON: '',
            THEME_VERSION: '6.0.020191205',

            OPERATION_NOTICE: '操作通知',
            SCREENSHOT_BEGIN: '正在生成当前页面截图……',
            SCREENSHOT_NOTICE: '点击顶部下载按钮保存当前卡片',
            SCREENSHORT_ERROR: '由于图片跨域原因导致截图失败',
            SCREENSHORT_SUCCESS: '截图成功',
            MUSIC_NOTICE: '播放通知',
            MUSIC_FAILE: '当前音乐地址无效，自动为您播放下一首',
            MUSIC_FAILE_END: '当前音乐地址无效',
            MUSIC_LIST_SUCCESS: '歌单歌曲加载成功',
            CDN_NAME: '',
            LAZY_LOAD: ''
        };

    </script> 
