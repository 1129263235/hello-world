<!DOCTYPE html>
<html>
<head lang="en">
  <meta charset="UTF-8">
  <title></title>
  <style type="text/css">
    * {
      margin: 0;
      padding: 0;
      font-size: 12px;
    }
    
    ul {
      list-style: none;
    }
    
    a {
      text-decoration: none;
    }
    
    .wrapper {
      width: 298px;
      height: 248px;
      margin: 100px auto 0;
      border: 1px solid pink;
      overflow: hidden;
    }
    
    #left, #center, #right {
      float: left;
    }
    
    #left li, #right li {
      background: url(images/lili.jpg) repeat-x;
    }
    
    #left li a, #right li a {
      display: block;
      width: 48px;
      height: 27px;
      border-bottom: 1px solid pink;
      line-height: 27px;
      text-align: center;
      color: black;
    }
    
    #left li a:hover, #right li a:hover {
      background-image: url(images/abg.gif);
    }
    
    #center {
      border-left: 1px solid pink;
      border-right: 1px solid pink;
    }
  </style>
  
  <script src="http://libs.baidu.com/jquery/1.11.3/jquery.min.js"></script>
  <script>
      $(function(){
          $('#left>li').mouseenter(function(){
              //让center中对应的下标显示，其他的隐藏
              var idx = $(this).index();
              console.log(idx); 
            //   打印下标
            $('#center>li:eq('+idx+')').show().siblings().hide();
          });
          $('#right>li').mouseenter(function(){
              //让center中对应的下标显示，其他的隐藏
              var idx = $(this).index();
              console.log(idx); 
              idx = idx + 9;
            //   打印下标
            $('#center>li').eq(idx).show().siblings().hide();
            //注意此处的eq写法
          });
      })
      
  </script>

</head>
<body>
<div class="wrapper">
  
  <ul id="left">
    <li><a href="#">女靴</a></li>
    <li><a href="#">雪地靴</a></li>
    <li><a href="#">冬裙</a></li>
    <li><a href="#">呢大衣</a></li>
    <li><a href="#">毛衣</a></li>
    <li><a href="#">棉服</a></li>
    <li><a href="#">女裤</a></li>
    <li><a href="#">羽绒服</a></li>
    <li><a href="#">牛仔裤</a></li>
  </ul>
  <ul id="center">
    <li><a href="#"><img src="images/女靴.jpg" width="200" height="250"/></a></li>
    <li><a href="#"><img src="images/雪地靴.jpg" width="200" height="250"/></a></li>
    <li><a href="#"><img src="images/冬裙.jpg" width="200" height="250"/></a></li>
    <li><a href="#"><img src="images/呢大衣.jpg" width="200" height="250"/></a></li>
    <li><a href="#"><img src="images/毛衣.jpg" width="200" height="250"/></a></li>
    <li><a href="#"><img src="images/棉服.jpg" width="200" height="250"/></a></li>
    <li><a href="#"><img src="images/女裤.jpg" width="200" height="250"/></a></li>
    <li><a href="#"><img src="images/羽绒服.jpg" width="200" height="250"/></a></li>
    <li><a href="#"><img src="images/牛仔裤.jpg" width="200" height="250"/></a></li>
    <li><a href="#"><img src="images/女包.jpg" width="200" height="250"/></a></li>
    <li><a href="#"><img src="images/男靴.jpg" width="200" height="250"/></a></li>
    <li><a href="#"><img src="images/登山鞋.jpg" width="200" height="250"/></a></li>
    <li><a href="#"><img src="images/皮带.jpg" width="200" height="250"/></a></li>
    <li><a href="#"><img src="images/围巾.jpg" width="200" height="250"/></a></li>
    <li><a href="#"><img src="images/皮衣.jpg" width="200" height="250"/></a></li>
    <li><a href="#"><img src="images/男毛衣.jpg" width="200" height="250"/></a></li>
    <li><a href="#"><img src="images/男棉服.jpg" width="200" height="250"/></a></li>
    <li><a href="#"><img src="images/男包.jpg" width="200" height="250"/></a></li>
  
  </ul>
  <ul id="right">
    <li><a href="#">女包</a></li>
    <li><a href="#">男靴</a></li>
    <li><a href="#">登山鞋</a></li>
    <li><a href="#">皮带</a></li>
    <li><a href="#">围巾</a></li>
    <li><a href="#">皮衣</a></li>
    <li><a href="#">男毛衣</a></li>
    <li><a href="#">男棉服</a></li>
    <li><a href="#">男包</a></li>
  </ul>

</div>
</body>
</html>
