

# CalampStatus

CalAmp LM Direct Status

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**altitude** | **Double** | The altitude reading of the GPS receiver measured in meters  _This field represents [messageBody.status.altitude]_  |  [optional] |
|**rssi** | **Integer** | The received signal strength of the wireless modem in dBm  _This field represents [messageBody.status.altitude]_  |  [optional] |
|**hdop** | **Double** | The GPS Horizontal Dilution of Precision  _This field represents [messageBody.status.altitude]_  |  [optional] |
|**latitude** | **Double** | The latitude reading of the GPS receiver, measured in degrees  _This field represents [messageBody.status.altitude]_  |  [optional] |
|**longitude** | **Double** | The longitude reading of the GPS receiver, measured in degrees  _This field represents [messageBody.status.altitude]_  |  [optional] |
|**speed** | **Double** | The speed as reported by the GPS receiver, measured in meters per second  _This field represents [messageBody.status.altitude]_  |  [optional] |
|**updateTime** | **LocalDate** | The time tag of the message in seconds.  _This field represents [messageBody.status.updateTime]_  |  [optional] |
|**timeOfFix** | **LocalDate** | The last known time of fix from the GPS satellites.  _This field represents [messageBody.status.timeOfFix]_  |  [optional] |
|**heading** | **Integer** | The heading value reported in degrees from true North  _This field represents [messageBody.status.heading]_  |  [optional] |
|**satellites** | **Integer** | The number of satellites used in the GPS solution   _This field represents [messageBody.status.satellites]_  |  [optional] |
|**carrier** | **Integer** | The identifier of the Carrier/Operator the wireless modem is currently using. For GSM, HSPA, and LTE networks, this is the MNC (mobile network code). For CDMA networks this is the SID (system identification number).  _This field represents [messageBody.status.carrier]_  |  [optional] |
|**fixStatus** | [**FixStatus**](FixStatus.md) |  |  [optional] |
|**commState** | [**CommState**](CommState.md) |  |  [optional] |
|**unitStatus** | [**UnitStatus**](UnitStatus.md) |  |  [optional] |



