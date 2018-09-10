## URI与URL
URI用字符串标识某一互联网资源（指向资源使用的协议类型成为协议方案，有http，ftp，file，telnet等），URL表示地点，URL是URI的子集。

## http
http是无状态的（不保存通讯状态。）

**常见http方法**
GET：获取资源（也可以传输实体，但是不推荐）
POST：传输实体
<table>
  <tr>
    <tb>方法</tb>
    <tb>长度</tb>
    <tb>编码</tb>
    <tb>安全性</tb>
    <tb>可缓存</tb>
    <tb>幂等性</tb>
  </tr>
  <tr>
    <th>GET</th>
    <tb>长度受限</tb>
    <tb>ASCII</tb>
    <tb>不安全</tb>
    <tb>可缓存</tb>
    <tb>幂等性</tb>
  </tr>
  <tr>
    <th>POST</th>
    <tb>不受限</tb>
    <tb>无限制</tb>
    <tb>安全</tb>
    <tb>不可缓存</tb>
    <tb>不幂等</tb>
  </tr>
</table>
