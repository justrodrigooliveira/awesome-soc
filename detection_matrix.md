# Detection matrix

## Purpose

This kind of document aims at representing detection (and even response) capabilities, for specific ("feared") events/incidents that are considered as critical/priority.

The list of those feared events is supposed to be generated or identified by security watch and/or risk analysis. See "[detection engineering page](https://github.com/cyb3rxp/awesome-soc/blob/main/detection_engineering.md#how-to-feed-the-plan-phase)" for further details.

## Matrix sample

This detection matrix sample leverages the "top TTP / feared events" that I recommend to consider as priority. Feel free to add/remove some events, depending on the context.

| Feared event // sensor    | AV/EDR |  SEG  |  SWG  |  IDTP | CASB  |
| ------------------------- | ------ | ----- | ----- | ----- | ----- |
| Malware spread            |    X   |   X   |   X   |       |   X   |
| Malware cleaning error    |    X   |       |   X   |       |       |
| T1566: Business email compromise |        |   X   |       |   X   |   X   |
| T1071: C&C access from an asset  |    X   |       |   X   |       |   X   |
| T1078: Impossible travel         |        |       |   X   |   X   |   X   |
| T1566: Phishing on private employees' emails (GMail, Outlook.com, etc.) |   X    |       |   X   |      |      |
| T1059: Command and Scripting Interpreter |   X   |   X   |   X   |       |       |
| T1218: Signed Binary Proxy Execution |   X   |       |       |       |       |
| T1055: Process Injection  |   X   |       |       |       |       |
| T1569: System services    |   X   |       |       |       |       |
| T1053: Scheduled Task/Job |   X   |       |       |       |       |
| T1003: OS Credential Dumping |   X   |       |       |       |       |



## Matrix meaning/understanding

* The matrix enumerates all of the security sensors in place, for the SOC perimeter's detection capabilities we wish to represent;
  * By default, I used the 5 key security sensors for a SOC, as described [here](https://github.com/cyb3rxp/awesome-soc/blob/main/README.md#critical-sensors-for-a-soc).
* For each feared event, the idea is to identify all the security sensors that could/should help in detecting it.
* If, for some reasons, the detection of a feared event is not considered as working for a specific sensor, then the cross should not be there in the array, for that sensor and that feared event;
  * The provided matrix is meant to be an example, for "best cases", and "not always true in every IT environment";
  * As a consequence, the detection matrix has to be adapted, and kept up-to-date in time, for every organizations' environments that have a SOC in place. In order to do so, the best practices recommend to run regular purpleteaming sessions (see [management page](https://github.com/cyb3rxp/awesome-soc/blob/main/management.md#detection-quality-assessment) for further info), for instance once a year.
