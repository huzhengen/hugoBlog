---
title: "excel按照固定行数分割成多个文件"
date: 2018-12-28T09:22:27+08:00
draft: false
---

打开Excel，鼠标不要任何选择。按“Alt”+“f11”。双击左侧sheet

输入代码，**注意行数，可修改，现在是50**

```
Sub cfb()
Dim r, c, i, WJhangshu, WJshu, bt As Long
r = Range("A" & Rows.Count).End(xlUp).Row
c = Cells(1, Columns.Count).End(xlToLeft).Column
bt = 1 'title
WJhangshu = 50 'num
WJshu = IIf(r - bt Mod 20000, Int((r - bt) / WJhangshu), Int((r - bt) / WJhangshu) + 1)
For i = 0 To WJshu
    Workbooks.Add
    Application.DisplayAlerts = False
    ActiveWorkbook.SaveAs Filename:=ThisWorkbook.Path & "\" & Format(i, String(Len(WJshu), 0)) & ".xlsx"
    Application.DisplayAlerts = True
    ThisWorkbook.ActiveSheet.Range("A1").Resize(bt, c).Copy ActiveSheet.Range("A1")
    ThisWorkbook.ActiveSheet.Range("A" & bt + i * WJhangshu + 1).Resize(WJhangshu, c).Copy _
     ActiveSheet.Range("A" & bt + 1)
    ActiveWorkbook.Close True
Next
End Sub
```
然后回到原来的excel，Alt+f8，执行，完成，over。

分割后最后一个excel是空的，从0开始算的。