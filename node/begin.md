### Node.js的学习起步

------

1. 安装Node环境

   - 下载node.js
   - 安装node.js
   - 确认是否安装成功
   - 环境变量

2. 第一个node.js程序

   - 执行一个js文件,脱离浏览器

     - 创建一个js脚本文件
     - 打开终端，定位到脚本文件所属目录
     - 输入node 文件名，执行对应文件
     - 注意：文件名不要使用node.js

   - 文件的操作（写文件）

     - 浏览器中的JavaScript是没有文件操作的能力的

     - Node中的JavaScript是可以有文件操作的

     - fs--是file-style的缩写，就是文件系统的意思

     - 在Node中如果想要进行文件的操作，就必须引入fs这个核心模块，这个核心模块中提供了所有文件操作相关的API

       ```
       //1、使用require方法加载fs核心模块
       var fs=require('fs')
       
       //2、读取文件
       //第一个参数是就是需要读取的文件路径
       第二个参数就是回调函数
       
       fs.readFile('./data/test.txt',function(error,data){
       //回调函数里面的两个参数分别是，错误信息和获得的数据
           console.log(data.toString())
       })
       ```

       

   - 写文件

     - 写文件,简单的错误处理

       ```
       var fs=require('fs')
       
       //第一个参数是需要写入的文件名，第二个参数是需要写入的内容，第三个是回调函数，里面有一个error参数
       fs.writeFile('./data/addFile>.txt','你好呀，Node.js',function(error){
       
       if(error){
           console.log('写入失败')
       }else{
           console.log('写入成功')
       
       }
       })
       ```

   - http:（创建服务器）

     ```
     //可以使用Node非常轻松的构建一个Web服务器，在Node中专门提供了一个核心模块：http,
     //http这个模块的职责就是帮我创建编写服务器
     
     //1、加载http核心模块
      var http=require('http')
     
      //2、使用http.createServer()方法创建一个Web服务器，返回一个Server实例
      var server=http.createServer()
     
      //3、服务器的作用：
      //提供服务，对数据的服务
      //浏览器发送请求------服务器端接收请求------处理请求--===给予反馈(发送响应)
     
      //客户端请求过来，就会自动触发服务器的request请求事件，然后执行第二个回调函数参数
      server.on('request',function(){
          console.log('收到服务器端的请求了')
      })
     
      //4、绑定端口号，启动服务器
      server.listen(3000,function(){
          console.log('服务器启动成功，可以通过  http://127.0.0.1:3000进行访问')
      })
     ```

   - 服务器对客户端的请求进行响应

     ```
     
     var http=require('http')
     
     var server=http.createServer()
     
     //request请求事件处理函数，需要接受两个参数
     //Request请求对象
     
     //Response响应对象
     server.on('request',function(request,response){
         console.log('收到服务器端的请求了'+request.url)
         //response对象有一个方法：write,可以用来给客户端发送响应数据，
         //wroite可以使用多次，但是在最后一定要使用end结束，不然客户端会一直处于等待状态
         response.write('hello')
         response.write('node.js')
     
         //告诉客户端，响应结束，可以樊哙信息给用户
         response.end()
     })
     
     server.listen(3000,function(){
         console.log('服务器启动成功，可以通过  http://127.0.0.1:3000进行访问')
     })
     ```

     

   - 思考：目前的服务器只能响应客户端一样的东西，当请求的路径不同的时候响应不同的东西

3. 