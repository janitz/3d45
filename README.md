# 3d45
tools and information about dremel digilab 3d45
## 3d45_status
to get the status of the printer, you have to HTTP-POST GETPRINTERSTATUS<br>
(replace the ip with your printers ip)<br>
```batch
curl 192.168.0.26/command -X POST -H "Content-Type: application/x-form-urlencoded" -d "GETPRINTERSTATUS"
```
<br>
this will return a json string like this<br>
(but in one line)<br>
```json
{
    "buildPlate_target_temperature": 70,
    "chamber_temperature": 22,
    "door_open": 0,
    "elaspedtime": 1908,
    "error_code": 200,
    "extruder_target_temperature": 240,
    "fanSpeed": 0,
    "filament_type ": "PLA",
    "firmware_version": "v3.0_R02.09.04",
    "jobname": "D3_end_cap.gcode",
    "jobstatus": "building",
    "layer": 50,
    "message": "success",
    "networkBuild": 0,
    "platform_temperature": 69,
    "progress": 9.4000000000000004,
    "remaining": 11337,
    "status": "busy",
    "temperature": 239,
    "totalTime": 12514
}
```
<br>
## 3d45_livestream
to watch your printer print just open this link<br>
(replace the ip with your printers ip)<br>
`http://192.168.0.26:10123/?action=stream`
