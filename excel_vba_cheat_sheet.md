# 📊 Excel & VBA Cheat Sheet

Because sometimes you're forced to use Excel... and other times you have to automate it with a language that time forgot.

This sheet contains quick references for formulas, keyboard shortcuts, basic VBA, and Excel tasks you'll probably get stuck doing at least once a week.

---

## 🔢 Common Formulas

| Formula Type     | Formula Example                        | Description                        |
|------------------|----------------------------------------|------------------------------------|
| Math             | `=SUM(A1:A10)`                         | Adds up values                     |
| Average          | `=AVERAGE(B2:B6)`                      | Mean value                         |
| Conditional      | `=IF(C2>100,"High","Low")`             | Basic logic                        |
| VLOOKUP          | `=VLOOKUP(lookup, range, col, FALSE)`  | Old school lookup                  |
| XLOOKUP (new)    | `=XLOOKUP(lookup, range, return_range)`| Better lookup                      |
| Countif          | `=COUNTIF(A1:A10, ">10")`              | Counts values matching a condition|
| Text Functions   | `=LEFT(B2, 5)`                         | Grabs first 5 characters           |

---

## ⚡ Keyboard Shortcuts

| Action                    | Shortcut (Windows) | Shortcut (Mac) |
|---------------------------|--------------------|----------------|
| Insert row                | `Ctrl + Shift + "+"` | `Cmd + Shift + "+"` |
| Delete row                | `Ctrl + -`          | `Cmd + -`      |
| Save workbook             | `Ctrl + S`          | `Cmd + S`      |
| Show formulas             | `Ctrl + ~`          | `Cmd + ~`      |
| Autofill                  | `Ctrl + D`          | `Cmd + D`      |
| Select entire column      | `Ctrl + Space`      | `Cmd + Space`  |

---

## 🧠 Simple VBA Example

```vba
Sub AutoFillDate()
    Range("A1").Value = Date
End Sub
```

Adds today’s date into cell A1 when the macro runs.

---

## 🔄 Common VBA Tasks

| Task                          | VBA Snippet Example                                                      |
|-------------------------------|---------------------------------------------------------------------------|
| Loop through a range          | `For Each cell In Range("A1:A10")`                                       |
| Insert a row                  | `Rows(2).Insert`                                                         |
| Delete empty rows             | `If WorksheetFunction.CountA(Rows(i)) = 0 Then Rows(i).Delete`           |
| Copy data                     | `Range("A1:A10").Copy Destination:=Range("B1")`                           |
| Paste values only             | `Range("B1:B10").Value = Range("A1:A10").Value`                          |
| Find last used row            | `lastRow = Cells(Rows.Count, 1).End(xlUp).Row`                            |
| Run macro on workbook open    | `Private Sub Workbook_Open()`...`End Sub`                                |
| Add today's date to cell      | `Range("A1").Value = Date`                                               |

---

💬 Notes
- Always save as macro-enabled workbook (.xlsm)
- VBA editor: Alt + F11
- You can record a macro first, then tweak the VBA

---