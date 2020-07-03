###  <script>元素

######   属性：

- [ ] async（异步下载）：可选，立即下载脚本，只对外部脚本有效

- [ ] defer（延迟执行）：可选，延迟到文档解析显示后在执行，外部脚本

- [ ] src：可选，需要用的外部文件的地址,不一定为js文件

- [ ] type：可选，language的代替属性，一般为text/javascript

   MIME:编写代码使用的脚本语言的类型，控制服务器与浏览器传输的形式，默认      application/javascript

- [ ] charset：可选，src设置代码的字符集，出现乱码的时候用，一般不用

- [ ] language：已废弃，表示脚本语言

  ##### 问题：

  - [ ] 包含在<script>元素内部的js代码从上到下依次**预处理+执行**

  - [ ] 不能在代码中使用</script>,改正<\/script>用在动态生成js代码时（写api文档）

  - [ ] 位置   head（页面渲染前执行，例如和css相关的）---->body元素中页面内容后面（一般）

  - [ ] 当src中不为js文件时，注意返回正确的MIME类型application/javascript

  - [ ] 不能同时引入内部与外部的js文件，内部会被忽略

  - [ ] src跨域，可引外部域文件

  - [ ] defer，async脚本都不一定按顺序执行，当两个脚本相关时，会错乱（最好不用）

  - [ ] 内部js性能更高，外部js可维护，可缓存，适应未来

  - [ ] 浏览器设置，ctrl+shift+delete清楚缓存，或者src=’url？随机数‘

  - [ ] XHTML不能使用'<'和'>',

    1.使用转义符

    2.

    ```
    <script>
    //<![CDATA]  浏览器不兼容XHTML时，将CDATA标签注释掉            
    function(){
    
    }
    //]]>
    </script>
    ```

  - [ ] <script>标签一定要闭合，不能写<script   src=".....js" /        

    

    ​       

    ​        

  