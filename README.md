# Windows 11 - Disable Telemetry


Telemetry data collection under Windows 11 works similarly to Windows 10. To disable Windows 11 telemetry data collection, only two registry entries need to be changed as of today:


``` 
HKLM\SYSTEM\CurrentControlSet\Services\DiagTrack\Start = 4
```

```
HKLM\SYSTEM\CurentControlSet\Control\WMI\Autologger\
AutoLogger-DiagTrack-Listener\Start = 0
``` 

Dadurch wird die Telemetriedatenerhebung unterbunden. Allerdings werden weiterhin Daten an Microsoft durch die Verwendung von Windows Defender SmartScreen gesendet. 
Um die Datenübertragung zu verhindern, muss der SmartScreen wie folgt deaktiviert werden:

```
GPO-Einstellungen -> Computerkonfiguration -> Administrative Vorlagen -> Windows Komponenten -> 
Datei-Explorer -> Windows Defender SmartScreen konfigurieren 
"Deaktiviert" auswählen

```
