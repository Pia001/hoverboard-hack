# Chips
 
## Chips Sideboards
Ein Sideboard scheint ein Hoverboard mit einem Controller pro Seite zu sein.

### MM32SPIN05
War im ersten Hoverboard **Evemotion GPX-1**.  China-Hühnerfutter - kaum Ressourcen.

### GD32F130C6T6 oder GD32F130C8T6
Der GD32F130C8T6 steckt im **Nortok NK-1865K**.

Die beiden Chips ähneln sich stark - gleiches Datasheet: https://datasheetspdf.com/pdf-file/976682/GigaDevice/GD32F130C6T6/1
Seite 54: Unterschiede im Speicher: C8T6: 64KB, C6T6: 32KB

Max Gerhard (siehe Maintainer in den Repos) hat ein Linkerscript geschrieben was den C8T6 unterstützt: https://github.com/CommunityGD32Cores/gd32-pio-spl-package/blob/main/platformio/ldscripts/GD32F130C8T_DEFAULT.ld


Repo: https://github.com/EFeru/hoverboard-sideboard-hack-GD aber leider ist das Repo in der Variante GD32F130C**6**T6.

Die Ressourcenlage ist unübersichtlich:


| Repo | Kommentar |
| -----|---------------|
| https://github.com/flo199213/Hoverboard-Firmware-Hack-Gen2 | Abandoned, 3 Jahre alt, ist hier https://github.com/maxgerhardt/Hoverboard-Firmware-Hack-Gen2 geforked |
| https://github.com/maxgerhardt/Hoverboard-Firmware-Hack-Gen2 | Letzter Commit 9 Monate her für ein _HoverBoardGigaDevice_, Der gleiche Maintainer ist auch hier https://github.com/EFeru/hoverboard-sideboard-hack-GD unterwegs |
| https://github.com/EFeru/hoverboard-sideboard-hack-GD | Eferu hat wohl so die beste Doku am Start :rocket: Ausserdem verweisen die meisten "getting started" auf Eferu. Scheint (medio) gepflegt zu sein: der letzte Commit ist 3 Monate her. Lange Forkliste.

## Chips Sensorboards
Haben wir bis jetzt leider noch nie IRL gesehen.

### GD32F103RCT6 und  STM32F103RCT6
Haben beide sehr gute Ressourcen und werden von der FOC Firmware unterstützt (super flauschig). :cat:
https://github.com/EFeru/hoverboard-firmware-hack-FOC 

# Firmware und Varianten

## [Eferu DG](https://github.com/EFeru/hoverboard-sideboard-hack-GD)
### VARIANT_DEBUG
am erfolgversprechendsten im Bezug auf Arduino Befehle

### VARIANT_HOVERCAR
RC Receiver...interessant weil Befehle müssen oghnehin zum Board - Option auf selbstgebaute Fernbedienung mit Arduino

### VARIANT_HOVERBOARD
Das Ding benutzt die FOC Firmware - die mal grundsätzlich ultrafett ist :watermelon:

Interessant weil explizit die FOC Firmware benutzt wird und diese weitere Varianten bereit hält. Ob und wie wir diese benutzen können ist noch nicht klar.

