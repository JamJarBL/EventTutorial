# EventTutorial
---
This is a test

```Lua
[x][0] onActivate -> Self -> VCE_modVariable("Brick", "loopmax", "Set", 10)
[x][0] onActivate -> Self -> VCE_modVariable("Brick", "loop", "Set", 0)
[x][1] onActivate -> Self -> VCE_retroCheck("ifBrickName", "!=", "START", "3 3")
[x][1] onVariableTrue -> Self -> VCE_ifValue("<var:br:loop>", "<", "<var:br:loopmax>", "3 8")
[x][0] onVariableTrue -> Self -> VCE_modVariable("Brick", "a<var:br:loop>", "Set", 0)
[x][0] onVariableTrue -> Self -> playSound("ClickPlant.wav")
[x][0] onVariableFalse -> Self -> playSound("Beep_EKG.wav")
[x][0] onVariableTrue -> Client -> BottomPrint("<var:br:loop> <var:br:loopmax>", 3, 0)
[x][0] onVariableTrue -> Self -> VCE_modVariable("Brick", "loop", "Add", 1)
```
