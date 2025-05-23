# Smart Meter / Switch KWS-303L ( Modbus / Modbus - RTU / RS-485 )

## Review
My review of this device is [here](https://alexey.baldin.space/hobby/home-automation/smart-switch-kws-303l)

## General setup

| Property    | Value                             |
|-------------| ----------------------------------|
| Baud rate   | 9600                              |
| Parity      | none                              |
| Stop bits   | 1                                 |
| A           | red wire from RS 485 connector    |
| B           | black wire from RS 485 connector  |
 
## Holding registers - Modbus commands

| Register | Description                                 | R/W | Bytes | Example               | Gain |
|----------| --------------------------------------------|-----|-------|-----------------------|------|
| 0        | Connection Command                          | R   |       |                       |      |
| 1        | Rated voltage (V)(220V)                     | R   |       | 220V(Fixed) => 22000  | 100  |
| 2        | Rated current (A) (40A)                     | R   |       | 40A(Fixed) => 4000    | 100  |
| 5        | Hardware version lower bits (display board) | R   | 2     | V0.8                  |      |
| 14       | Active Voltage (V)                          | R   | 2     | 229.6V => 22960       | 100  |
| 18       | Active Amperage (A)                         | R   |       | 0.012A => 12          | 1000 |
| 26       | Active Power (W)                            | R   |       | 3.12W=> 312           | 100  |
| 34       | ??                                          | R   |       |                       |      |
| 42       | ??                                          | R   |       |                       |      |
| 48       | Power Factor                                | R   |       | 0.99 =>990            | 1000 |
| 51       | Active Frequency (Hz)                       | R   |       | 50Hz => 5000          | 100  |
| 55       | Consumed Energy (kWh)                       | R   |       | 5.5kWh => 5500        | 1000 |
| 60       | Active Temperature (Co)                     | R   |       | 25                    | 1    |
| 61       | Timing (minutes)                            | R   |       | 100 => 100            | 1    |
| 63       | Switch on / off relay                       | R   |       | On/Off => 1 / 0       | –    |
| 64       | Over Voltage Limit (V)                      | R   |       | 250V => 2500          | 10   |
| 65       | Under Voltage Limit (V)                     | R   |       | 85V => 850            | 10   |
| 66       | Over Amperage Limit (A)                     | R   |       | 26A => 260            | 10   |
| 67       | Over Power Limit (W)                        | R   |       | 11W => 110            | 10   |
| 71       | Back Light time (minutes)                   | R   |       | 6                     | 1    |
| 72       | Over Temperature Limit (Co)                 | R   |       | 50                    | 1    |
| 74       | Over Energy Limit (kWh)                     | R   |       | 12kWh=>1200           | 100  |
| 81       | Screen Rotation                             | R   |       | Normal/Rotated => 1/0 | –    |
| 82       | Black Light  %                              | R   |       | 80                    | 1    |


## Official protocl description

![KWS-303L](img/kws-303l.jpeg?raw=true "KWS-303L")