## Exemplo 1
ax_scrollbar = session.findById("wnd[1]/usr/tblSAPLCZDITCTRL_4010").verticalScrollbar.Maximum ' Get the maximum scrollbar value
session.findById("wnd[1]/usr/tblSAPLCZDITCTRL_4010").verticalScrollbar.Position = max_scrollbar  ' Go to the end 

## Exemplo 2 
session.findById("wnd[0]").sendVKey 83 
myPosition = session.findById("wnd[1]/usr/tblSAPLCZDITCTRL_4010").verticalScrollbar.Position
do 
if session.findById("wnd[1]/usr/tblSAPLCZDITCTRL_4010/ctxtMAPL-MATNR[2,0]").Text = ""  then exit do
myPosition = myPosition + 1
session.findById("wnd[1]/usr/tblSAPLCZDITCTRL_4010").verticalScrollbar.Position = myPosition
loop 
msgbox myPosition
