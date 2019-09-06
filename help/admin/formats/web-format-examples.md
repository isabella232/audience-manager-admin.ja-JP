---
description: 一般的に使用される HTTP マクロの組み合わせの例。
seo-description: 一般的に使用される HTTP マクロの組み合わせの例。
seo-title: HTTP 形式マクロの例
title: HTTP 形式マクロの例
uuid: a81a2e2a- de7e-4b6a-8771- fcfa0dc74570
translation-type: tm+mt
source-git-commit: 4c6d1752ff10d2d3d12cab88e823f25f5ef4fcd0

---


# HTTP 形式マクロの例 {#http-format-macro-examples}

Examples of some commonly used [!DNL HTTP] macro combinations.

See the [HTTP Format Macros](../formats/web-formats.md) for a list of macros and their definitions.

<table id="table_D5FAC5D056ED49D79FA883197EF8F42E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> マクロの例 </th> 
   <th colname="col2" class="entry"> 出力形式 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <code>&lt;PID_ALIAS&gt;|&lt;DP_UUID&gt;|&lt;TRAITALIAS_LIST; separator=","&gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>pid_alias|dp_uuid|trait_1,trait_2</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>&lt;PID_ALIAS&gt;|count:&lt;NUM_USERS&gt;|users:[&lt;USER_LIST:{user|&lt;user.aamUuid&gt;:&lt;user.dpUuid&gt;}; separator=", "&gt;]</code> </p> </td> 
   <td colname="col2"> <p> <code>"pid_alias|count:2|users:[uuid1:dpuuid1, uuid2:dpuuid2]"</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>&lt;USER_AGENT&gt;|&lt;IP&gt;|&lt;TIMESTAMP&gt;|&lt;RANDOM&gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>"Firefox|255.255.255.255|1395758143|42341"</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>&lt;USER_LIST:{u|&lt;u.userAgent&gt;|&lt;u.ip&gt;|&lt;u.timestamp&gt;|&lt;u.random&gt;}; separator=", "&gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>"Firefox|255.255.255.255|1395758143|42341"</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>&lt;DP_UUIDS.1&gt; AND &lt;DP_UUIDS.2&gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>dpuuid1 AND dpuuid2</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>users:[&lt;USER_LIST:{user|&lt;user.dpUuids.1&gt; AND &lt;user.dpUuids.2&gt;}; separator=", "&gt;]</code> </p> </td> 
   <td colname="col2"> <p> <code>users:[dpuuid1 AND dpuuid2]</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>test_known_string=loremlipsum&amp;segid=&lt;TRAITALIAS_LIST; separator=","&gt;&amp;test_dpuuid_1000=&lt;DP_UUIDS.1000&gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>test_known_string=loremlipsum&amp;segid=trait_1,trait_2&amp;test_dpuuid_1000=dpuuid_1000</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>test_dpuuids=&lt;DP_UUIDS.(DPID)&gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>test_dpuuids=dpuuid2</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>"&lt;PID_ALIAS&gt;|&lt;DP_UUID&gt;|&lt;TRAITALIAS_LIST; separator=","&gt;|&lt;REMOVED_TRAITALIAS_LIST; separator=","&gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>pid_alias|dp_uuid|trait_1,trait_2|trait_3,trait_4</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 
     <code>{"Users":[&lt; USER_ LIST:{user|&lt; OPEN_ BRECKER&gt;
"AAM_ UUID":"&lt; user. AAMUuid&gt;"，
"DataCarner_ UUID":"&lt; user. Dpuuid&gt;"，
「セグメント」:[&lt; user. segments:{seg|&lt; OPEN_ BROCKER&gt;"Segment":"&lt; seg. TraitAlias&gt;"&lt; CLOSE_ BACCEE&gt;};separator=»，
"Removed_ Segments":[&lt; user. removeSegments:{rseg|&lt; OPEN_ BROCKER&gt;"Segment":"&lt; rseg. traitAlias&gt;"&lt; CLOSE_ BACCEE&gt;};separator=»，
&lt; CLOSE_ BROCKER&gt;};separator=»， </code>
  </p> </td> 
   <td colname="col2"> <p> 
     <code>{
"Users":[
{
"AAM_ UUID":"uuid1"，
"DataCarner_ UUID":"dpuuid1"，
「セグメント」:[
{
「セグメント」:"alias1"
}，
{
「セグメント」:"alias2"
}
]，
"Removed_ Segments":[
{
「セグメント」:"alias3"
}，
{
「セグメント」:"alias4"
}
]
}
]
} </code>
  </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 
     <code>{"Users":[&lt; USER_ LIST:{user|&lt; OPEN_ BRECKER&gt;
"AAM_ UUID":"&lt; user. AAMUuid&gt;"，
"DataCarner_ UUID":"&lt; user. Dpuuid&gt;"，
「セグメント」:[&lt; user. segments:{seg|&lt; OPEN_ BROCKER&gt;"Segment":"&lt; seg. TraitAlias&gt;"，"Status":"&lt; seg. status&gt;"&lt; CLOSE_ BANKER&gt;};separator=»，
&lt; CLOSE_ BROCKER&gt;};separator=»， </code>
  </p> </td> 
   <td colname="col2"> <p> 
     <code>{
"Users":[
{
"AAM_ UUID":"uuid1"，
"DataCarner_ UUID":"dpuuid1"，
「セグメント」:[
{
「セグメント」:"alias1"
"Status":"1"
}，
{
「セグメント」:"alias2"
"Status":"0"
}
]
}
]
} </code>
  </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>&lt;PID_ALIAS&gt;|&lt;DP_UUID&gt;|&lt;SEGMENTS:{seg|&lt;seg.traitAlias&gt;}; separator=\",\"&gt;|&lt;REMOVED_SEGMENTS:{seg|&lt;seg.traitAlias&gt;}; separator=\",\"&gt;</code> </p> </td> 
   <td colname="col2"> <p> <code>pid_alias|dp_uuid|trait_1,trait_2|trait_3,trait_4</code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <code>&lt;if(user.segments &amp;&amp; user.removedSegments)&gt;&lt;COMMA&gt;&lt;endif&gt;</code> </p> </td> 
   <td colname="col2"> <p><code>segments</code> フィールドと <code>removedSegments</code> フィールドが空でない場合、コンマが出力されます。この条件は、セグメントのリストと削除済みセグメントのリストを結合するための POST リクエストで使用できます。 </p> </td> 
  </tr> 
 </tbody> 
</table>