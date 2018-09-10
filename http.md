## URI与URL
URI用字符串标识某一互联网资源（指向资源使用的协议类型成为协议方案，有http，ftp，file，telnet等），URL表示地点，URL是URI的子集。  

## http
http是无状态的（不保存通讯状态。）  

**常见http方法**  
GET：获取资源（也可以传输实体，但是不推荐）  
POST：传输实体  
<table>
  <tr>
    <td>方法</td>
    <td>长度</td>
    <td>编码</td>
    <td>安全性</td>
    <td>可缓存</td>
    <td>幂等性</td>
  </tr>
  <tr>
    <th>GET</th>
    <td>长度受限</td>
    <td>ASCII</td>
    <td>不安全</td>
    <td>可缓存</td>
    <td>幂等性</td>
  </tr>
  <tr>
    <th>POST</th>
    <td>不受限</td>
    <td>无限制</td>
    <td>安全</td>
    <td>不可缓存</td>
    <td>不幂等</td>
  </tr>
</table>
PUT方法：传输文件  
类似于FTP，要求在请求报文中的主体包含文件内容，然后保存到请求的URI指定位置。
Http/1.1的PUT方法自身不带验证机制，任何人都可以上传文件，存在安全问题，一般web网站不适用。
HEAD：获取报文首部
和GET方法一样，但是不返回报文主体，用于确认URI的有效性及资源更新的日期时间等。
DELETE：删除文件，Http/1.1的DELETE方法自身不带验证机制，存在安全问题，一般web网站不适用。
OPTIONS：询问指定URI的支持方法，
TRACE：追踪路径，让Web服务器将之前的请求通信返回给客户端的方法。
CONNECT：要求用隧道协议连接代理，主要使用SSL，TSL协议加密传输。

HTTP1.0和HTTP1.1

<table>
  <tr>
    <td>协议</td>
    <td>方法支持</td>
    <td>连接</td>
  </tr>
  <tr>
    <th>HTTP1.0</th>
    <td>GET，POST，PUT，HEAD，DELETE,LINK,UNLINK</td>
    <td>非持久连接</td>
  </tr>
  <tr>
    <th>HTTP1.1</th>
    <td>GET，POST，PUT，HEAD，DELETE，OPTIONS，TRACE，CONNECT</td>
    <td>持久连接+管线化</td>
  </tr>
</table>

## Cookie的状态管理  
HTTP无状态可以减少服务器的CPU内存资源消耗，并使得HTTP协议简单。
Cookie技术通过在请求和响应报文中写入Cookie信息来控制客户端状态。
Cookie可以通过服务器端发送响应报文的Set-Cookie首部字段，通知客户端保存Cookie。
步骤：
没有cookie时：
1.客户端发出请求，服务端记住谁发送的
2.服务端在响应中添加Cookie后返回，客户端保存Cookie
有Cookie时：
1.客户端请求中添加Cookie后发送，服务端检查Cookie
2.服务端响应
