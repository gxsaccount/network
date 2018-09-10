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
