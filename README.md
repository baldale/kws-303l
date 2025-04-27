# Smart Meter / Switch KWS-303L ( Modbus / Modbus - RTU / RS-485 )

## Review
My review of this device is [here](https://alexey.baldin.space/hobby/home-automation/smart-switch-kws-303l)

## General setup

| Property	   | Value                             |
|-------------| ----------------------------------|
| Baud rate   | 9600                              |
| Parity	     | even                              |
| Stop bits   | 1                                 |
| A	          | red wire from RS 485 connector    |
| B	          | black wire from RS 485 connector  |
 
## Holding registers - Modbus commands

| Register	| Description	                | Example               | Gain |
|----------| ----------------------------|-----------------------|------|
| 1	       | Rated voltage (V)(220V)	    | 220V(Fixed) => 22000  | 100  |
| 2	       | Rated current (A) (40A)	    | 40A(Fixed) => 4000    | 100  |
| 14	      | Active Voltage (V)	         | 229.6V => 22960       | 100  |
| 18	      | Active Amperage (A)	        | 0.012A => 12          | 1000 |
| 26	      | Active Power (W)	           | 3.12W=> 312           | 10   |
| 34	      | ??                          |                       | 		   |
| 42	      | ??	                         | 	                     |      |
| 48	      | Power Factor	               | 0.99 =>990            | 1000 |
| 51	      | Active Frequency (Hz)	      | 50Hz => 5000          | 100  |
| 55	      | Consumed Energy (kWh)	      | 5.5kWh => 5500        | 1000 |
| 60	      | Active Temperature (Co)	    | 25                    | 1    |
| 61	      | Timing (minutes)	           | 100 => 100            | 1    |
| 63	      | Switch on / off	relay       | On/Off => 1 / 0       | –    |
| 64	      | Over Voltage Limit (V)      | 250V => 2500          | 10   |
| 65	      | Under Voltage Limit (V)	    | 85V => 850            | 10   |
| 66	      | Over Amperage Limit (A)	    | 26A => 260            | 10   |
| 67	      | Over Power Limit (W)	       | 11W => 110            | 10   |
| 71	      | Back Light time (minutes)	  | 6                     | 1    |
| 72	      | Over Temperature Limit (Co)	| 51                    | 10   |
| 74	      | Over Energy Limit (kWh)	    | 12kWh=>1200           | 100  |
| 81	      | Screen Rotation	            | Normal/Rotated => 1/0 | –    |
| 82	      | Black Light  %              | 80	                   | 1    |
