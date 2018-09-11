# Eventing Guide - Introduction
---
To effectively follow along with the guide, the following addons are highly recomended but they are in no way required.

---
### Support_EventScript
This mod introduces the ability to script your events, through the new scripting language EventScript. It removes the hurdle of sharing. It reduces the problem with huge amounts of events. It completely obliterates copying issues. Download. Install. Set your shortcuts of copy/paste/editor. Start scripting.

[Link to BL Forum thread](https://forum.blockland.us/index.php?topic=314714.0)<br>
[Direct download link](http://mirror.aposoc.net/Blockland/Support_EventScript.zip)

*Underneath is an example of exported events.*
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

---
### Client_DropDownSearch
Gone are the days of mindless scrolling in unnecessary long lists. Just type to filter down the list to rows starting with that you type. Once you've filtered the list to a manageable level, pick out the correct row. Just move the mouse cursor away from the drop down list and start scrolling!<br>
Alternatively, hold down ctrl or shift and press up/down arrow keys to move it.

[Link to BL Forum thread](https://forum.blockland.us/index.php?topic=291624.0)<br>
[Direct download link](http://bl.zeblote.com/files/Client_DropDownSearch/release/Client_DropDownSearch.zip)

![alt text](http://i.imgur.com/yeDg8f3.png "Drop Down Search example")

---
### Client_EventGUIPlus
An Event Shifting system, allowing you to shift events up and down within the events GUI. This is most useful if you use the Variable Events, because you can move things into or out of subareas as needed.

[Link to AddOn thread](http://orbs.daprogs.com/rtb/forum.returntoblockland.com/dlm/viewFilec1fb.html?id=209)<br>
[Direct download link](http://orbs.daprogs.com/rtb/forum.returntoblockland.com/dlm/Client_EventsGUIPlus.zip?id=209)

![alt text](http://orbs.daprogs.com/rtb/forum.returntoblockland.com/uploads/images/652f739287ac5b27ee367d3cea251b6f.png "Event GUI Plus example")
