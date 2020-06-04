# 设置云服务器元数据<a name="ZH-CN_TOPIC_0025560298"></a>

## 功能介绍<a name="section61558535185333"></a>

设置云服务器元数据。

-   如果元数据中没有待设置字段，则自动添加该字段。
-   如果元数据中已存在待设置字段，则直接设置字段值。
-   如果元数据中的字段不在请求参数中，则保持不变

## 接口约束<a name="section39865556127"></a>

云服务器状态（云服务器的OS-EXT-STS:vm\_state属性）必须是active，stopped，paused或者suspended。

## URI<a name="section47451206185333"></a>

POST /v2.1/\{project\_id\}/servers/\{server\_id\}/metadata

参数说明请参见[表1](#table18618337185333)。

**表 1**  参数说明

<a name="table18618337185333"></a>
<table><thead align="left"><tr id="row17183202185333"><th class="cellrowborder" valign="top" width="19.99%" id="mcps1.2.4.1.1"><p id="p5187119"><a name="p5187119"></a><a name="p5187119"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="18.67%" id="mcps1.2.4.1.2"><p id="p17503500"><a name="p17503500"></a><a name="p17503500"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="61.339999999999996%" id="mcps1.2.4.1.3"><p id="p8497414"><a name="p8497414"></a><a name="p8497414"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row30151070185333"><td class="cellrowborder" valign="top" width="19.99%" headers="mcps1.2.4.1.1 "><p id="p26317623185333"><a name="p26317623185333"></a><a name="p26317623185333"></a>project_id</p>
</td>
<td class="cellrowborder" valign="top" width="18.67%" headers="mcps1.2.4.1.2 "><p id="p51352688185333"><a name="p51352688185333"></a><a name="p51352688185333"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="61.339999999999996%" headers="mcps1.2.4.1.3 "><p id="p37593705"><a name="p37593705"></a><a name="p37593705"></a>项目ID。</p>
<p id="p1180512217438"><a name="p1180512217438"></a><a name="p1180512217438"></a>获取方法请参见<a href="获取项目ID.md">获取项目ID</a>。</p>
</td>
</tr>
<tr id="row56472316185333"><td class="cellrowborder" valign="top" width="19.99%" headers="mcps1.2.4.1.1 "><p id="p10854909185333"><a name="p10854909185333"></a><a name="p10854909185333"></a>server_id</p>
</td>
<td class="cellrowborder" valign="top" width="18.67%" headers="mcps1.2.4.1.2 "><p id="p6832475185333"><a name="p6832475185333"></a><a name="p6832475185333"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="61.339999999999996%" headers="mcps1.2.4.1.3 "><p id="p16559613185333"><a name="p16559613185333"></a><a name="p16559613185333"></a>云服务器ID。</p>
</td>
</tr>
</tbody>
</table>

## 请求消息<a name="section14818796185333"></a>

请求参数如[表2](#table52485804185333)所示。

**表 2**  请求参数

<a name="table52485804185333"></a>
<table><thead align="left"><tr id="row22430249185333"><th class="cellrowborder" valign="top" width="15.229999999999999%" id="mcps1.2.5.1.1"><p id="p4910858185333"><a name="p4910858185333"></a><a name="p4910858185333"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="17.29%" id="mcps1.2.5.1.2"><p id="p62235249185333"><a name="p62235249185333"></a><a name="p62235249185333"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="24.060000000000002%" id="mcps1.2.5.1.3"><p id="p7890371185333"><a name="p7890371185333"></a><a name="p7890371185333"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="43.419999999999995%" id="mcps1.2.5.1.4"><p id="p35140330185333"><a name="p35140330185333"></a><a name="p35140330185333"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row27794510185333"><td class="cellrowborder" valign="top" width="15.229999999999999%" headers="mcps1.2.5.1.1 "><p id="p36762838185333"><a name="p36762838185333"></a><a name="p36762838185333"></a>metadata</p>
</td>
<td class="cellrowborder" valign="top" width="17.29%" headers="mcps1.2.5.1.2 "><p id="p24999915185333"><a name="p24999915185333"></a><a name="p24999915185333"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="24.060000000000002%" headers="mcps1.2.5.1.3 "><p id="p11727220185333"><a name="p11727220185333"></a><a name="p11727220185333"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="43.419999999999995%" headers="mcps1.2.5.1.4 "><p id="p26317995185333"><a name="p26317995185333"></a><a name="p26317995185333"></a>用户自定义metadata键值对。</p>
</td>
</tr>
</tbody>
</table>

**表 3**  metadata数据结构说明

<a name="table59792218185333"></a>
<table><thead align="left"><tr id="row39910345185333"><th class="cellrowborder" valign="top" width="24.060000000000002%" id="mcps1.2.5.1.1"><p id="p11512487185333"><a name="p11512487185333"></a><a name="p11512487185333"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="14.85%" id="mcps1.2.5.1.2"><p id="p60096221185333"><a name="p60096221185333"></a><a name="p60096221185333"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="17.86%" id="mcps1.2.5.1.3"><p id="p35955732185333"><a name="p35955732185333"></a><a name="p35955732185333"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="43.230000000000004%" id="mcps1.2.5.1.4"><p id="p26733171185333"><a name="p26733171185333"></a><a name="p26733171185333"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row15890112034514"><td class="cellrowborder" valign="top" width="24.060000000000002%" headers="mcps1.2.5.1.1 "><p id="p1089262011454"><a name="p1089262011454"></a><a name="p1089262011454"></a>key</p>
</td>
<td class="cellrowborder" valign="top" width="14.85%" headers="mcps1.2.5.1.2 "><p id="p18894122014512"><a name="p18894122014512"></a><a name="p18894122014512"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="17.86%" headers="mcps1.2.5.1.3 "><p id="p220493014454"><a name="p220493014454"></a><a name="p220493014454"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="43.230000000000004%" headers="mcps1.2.5.1.4 "><p id="p19894192011457"><a name="p19894192011457"></a><a name="p19894192011457"></a>键。</p>
<p id="p146113814453"><a name="p146113814453"></a><a name="p146113814453"></a>最大长度255个Unicode字符，不能为空。可以为大写字母（A-Z）、小写字母（a-z）、数字（0-9）、中划线（-）、下划线（_）、冒号（:）和小数点（.）。</p>
</td>
</tr>
<tr id="row17903267185333"><td class="cellrowborder" valign="top" width="24.060000000000002%" headers="mcps1.2.5.1.1 "><p id="p40878540185333"><a name="p40878540185333"></a><a name="p40878540185333"></a>value</p>
</td>
<td class="cellrowborder" valign="top" width="14.85%" headers="mcps1.2.5.1.2 "><p id="p22827413185333"><a name="p22827413185333"></a><a name="p22827413185333"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="17.86%" headers="mcps1.2.5.1.3 "><p id="p37081126185333"><a name="p37081126185333"></a><a name="p37081126185333"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="43.230000000000004%" headers="mcps1.2.5.1.4 "><p id="p999582373317"><a name="p999582373317"></a><a name="p999582373317"></a>值。</p>
<p id="p58906615396"><a name="p58906615396"></a><a name="p58906615396"></a>最大长度为255个Unicode字符。</p>
</td>
</tr>
</tbody>
</table>

## 响应消息<a name="section22254218185333"></a>

响应参数如[表4](#table48150236185333)所示。

**表 4**  响应参数

<a name="table48150236185333"></a>
<table><thead align="left"><tr id="row64499137185333"><th class="cellrowborder" valign="top" width="21.93%" id="mcps1.2.4.1.1"><p id="p57047574185333"><a name="p57047574185333"></a><a name="p57047574185333"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="27.189999999999998%" id="mcps1.2.4.1.2"><p id="p57450759185333"><a name="p57450759185333"></a><a name="p57450759185333"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50.88%" id="mcps1.2.4.1.3"><p id="p22999934185333"><a name="p22999934185333"></a><a name="p22999934185333"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row51055328185333"><td class="cellrowborder" valign="top" width="21.93%" headers="mcps1.2.4.1.1 "><p id="p41840919185333"><a name="p41840919185333"></a><a name="p41840919185333"></a>metadata</p>
</td>
<td class="cellrowborder" valign="top" width="27.189999999999998%" headers="mcps1.2.4.1.2 "><p id="p33671307185333"><a name="p33671307185333"></a><a name="p33671307185333"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="50.88%" headers="mcps1.2.4.1.3 "><p id="p51647808185333"><a name="p51647808185333"></a><a name="p51647808185333"></a>用户自定义metadata键值对。</p>
</td>
</tr>
</tbody>
</table>

## 请求示例<a name="section1124134931510"></a>

```
POST https://{endpoint}/v2.1/{project_id}/servers/{server_id}/metadata
```

```
{
    "metadata": {
        "key": "value"
    }
}
```

## 响应示例<a name="section111751241184111"></a>

```
{
    "metadata":{
        "key":"value"
    }
} 
```

## 返回值<a name="section46706088185333"></a>

请参考[通用请求返回值](通用请求返回值.md)。

