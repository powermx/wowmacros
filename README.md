## Macros para WoW
>Lista de Macros para WoW

-Macro para borrar grises:
```
/run for bag = 0,4,1 do for slot = 1, 32, 1 do local name = GetContainerItemLink(bag,slot); if name and string.find(name,"ff9d9d9d") then PickupContainerItem(bag,slot); DeleteCursorItem(); end; end; end 
```

-Macro para borrar blancos:
```
/run for bag = 0, 4 do for slot = 1, GetContainerNumSlots(bag) do local name = GetContainerItemLink(bag,slot) if name and string.find(name,"ffffffff") then PickupContainerItem(bag,slot) DeleteCursorItem() end end end 
```

-Macro para borrar verdes:
```
/run for bag = 0,4,1 do for slot = 1, 32, 1 do local name = GetContainerItemLink(bag,slot); if name and string.find(name,"ff1eff00") then PickupContainerItem(bag,slot); DeleteCursorItem(); end; end; end
```

-Macro para borrar azules:
```
/run for bag = 0,4,1 do for slot = 1, 32, 1 do local name = GetContainerItemLink(bag,slot); if name and string.find(name,"ff0070dd") then PickupContainerItem(bag,slot); DeleteCursorItem(); end; end; end
```

-Macro para borrar morados:
```
/run for bag = 0,4,1 do for slot = 1, 32, 1 do local name = GetContainerItemLink(bag,slot); if name and string.find(name,"ffa335ee") then PickupContainerItem(bag,slot); DeleteCursorItem(); end; end; end
```

- Macro para alejar Camara
```
/console CameraDistanceMaxFactor 4
```

- Macro para desbuggear Recount
```
/run local f = CreateFrame("frame",nil, UIParent); f:SetScript("OnUpdate", CombatLogClearEntries);
```

- Macro para saber coordenadas
```
/script SetMapToCurrentZone() local x,y=GetPlayerMapPosition("player") DEFAULT_CHAT_FRAME:AddMessage(format("%s, %s: %.1f, %.1f",GetZoneText(),GetSubZoneText(),x*100,y*100))
```
