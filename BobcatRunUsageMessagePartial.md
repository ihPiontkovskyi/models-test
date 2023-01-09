

# BobcatRunUsageMessagePartial

Bobcat Run Usage Message

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**seatbarOpenCount** | **Integer** | Seatbar position - Times Cycled (count)  _This field represents [messageBody.applicationMessage.applicationMessage.payload.seatbarOpenCount]_  |  [optional] |
|**doorOpenCount** | **Integer** | Door position - Times Opened (count)  _This field represents [messageBody.applicationMessage.applicationMessage.payload.doorOpenCount]_  |  [optional] |
|**workgroupOnCount** | **Integer** | Workgroup State - Time not OFF (s)  _This field represents [messageBody.applicationMessage.applicationMessage.payload.workgroupOnCount]_  |  [optional] |
|**driveStateOnCount** | **Integer** | Drive State - Time not OFF (s)  _This field represents [messageBody.applicationMessage.applicationMessage.payload.driveStateOnCount]_  |  [optional] |
|**engineStateCrankingCount** | **Integer** | Engine State - Times cranking (count)  _This field represents [messageBody.applicationMessage.applicationMessage.payload.engineStateCrankingCount]_  |  [optional] |
|**engineStateCrankingDuration** | **Integer** | Engine State - Time during last crank (s)  _This field represents [messageBody.applicationMessage.applicationMessage.payload.engineStateCrankingDuration]_  |  [optional] |
|**engineStateCrankingMax** | **Integer** | Engine State - Max cranking time (s)  _This field represents [messageBody.applicationMessage.applicationMessage.payload.engineStateCrankingMax]_  |  [optional] |
|**engineOnTime** | **Integer** | Total time on (s)  _This field represents [messageBody.applicationMessage.applicationMessage.payload.engineOnTime]_  |  [optional] |
|**throttlePositionBinned** | **Map&lt;String, Long&gt;** | Total amount of time (in seconds) spent in the given throttle position range while the machine is running (engine on). Bins (in order): 1. 0 to 25% 2. 26 to 50% 3. 51 to 75% 4. 76 to 100%  _This field represents [messageBody.applicationMessage.applicationMessage.payload.throttlePositionBinned]_  |  [optional] |
|**engineSpeedDurationBinned** | **Map&lt;String, Long&gt;** | Total amount of time (in seconds) spent in the given engine speed range (RPM) while the machine is running (engine on). Bins (in order): 1. 0 to 1099 RPM 2. 1100 - 1199 RPM 3. 1200 - 1299 RPM 4. 1300 - 1399 RPM 5. 1400 - 1499 RPM 6. 1500 - 1599 RPM 7. 1600 - 1699 RPM 8. 1700 - 1799 RPM 9. 1800 - 1899 RPM 10. 1900 - 1999 RPM 11. 2000 - 2099 RPM 12. 2100 - 2199 RPM 13. 2200 - 2299 RPM 14. 2300 - 2399 RPM 15. 2400 - 2499 RPM 16. 2500 - 2599 RPM 17. 2600 - 2699 RPM 18. 2700 - 2799 RPM 19. 2800+ RPM  _This field represents [messageBody.applicationMessage.applicationMessage.payload.engineSpeedDurationBinned]_  |  [optional] |
|**loadDurationBinned** | **Map&lt;String, Long&gt;** | Total amount of time (in seconds) spent in the given torque range (% of max torque) while the machine is running (engine on). Bins (in order): 1. &lt; 5% 2. 5 to 9% 3. 10 to 14% 4. 15 to 19% 5. 20 to 24% 6. 25 to 29% 7. 30 to 34% 8. 35 to 39% 9. 40 to 50% 10. 51 and up  _This field represents [messageBody.applicationMessage.applicationMessage.payload.loadDurationBinned]_  |  [optional] |
|**defTemperatureBinned** | **Map&lt;String, Long&gt;** | Total amount of time (in seconds) spent in the given DEF temperature range while the machine is running (engine on). Bins (in order): 1. &lt; -13 °C 2. -13 to 15 °C 3. 16 to 43 °C 4. 44 to 54 °C 5. 55 to 65 °C 6. 66+ °C  _This field represents [messageBody.applicationMessage.applicationMessage.payload.defTemperatureBinned]_  |  [optional] |
|**engineCoolantTemperatureBinned** | **Map&lt;String, Long&gt;** | Total amount of time (in seconds) spent in the given Engine temperature range while the machine is running (engine on). Bins (in order): 1. &lt; 83 °C 2. 83 to 88 °C 3. 89 to 93 °C 4. 94 to 99 °C 5. 100 to 104 °C 6. 105 to 110 °C 7. 111 to 115 °C 8. 116+ °C  _This field represents [messageBody.applicationMessage.applicationMessage.payload.engineCoolantTemperatureBinned]_  |  [optional] |
|**defConcentrationBinned** | **Map&lt;String, Long&gt;** | Total amount of time (in seconds) spent in the given DEF concentration range while the machine is running (engine on). Bins (in order): 1. 0 to 19.75% 2. 20 to 26.75% 3. 27 to 29.75% 4. 30 to 31.75% 5. 32 to 33.75% 6. 34 to 37.75% 7. 38 to 41.75% 8. 42 to 44.75% 9. 45 to 59.75% 10. 60+ %  _This field represents [messageBody.applicationMessage.applicationMessage.payload.defConcentrationBinned]_  |  [optional] |
|**twoSpeedOnBinned** | **Integer** | Total amount of time spent (in seconds) with Two Speed enabled.  _This field represents [messageBody.applicationMessage.applicationMessage.payload.twoSpeedOnBinned]_  |  [optional] |
|**driveResponseBinned** | **Map&lt;String, Long&gt;** | Present the time distribution within each drive response range bins during each machine operation event  _This field represents [messageBody.applicationMessage.applicationMessage.payload.driveResponseBinned]_  |  [optional] |
|**frontBaseSolenoidBinned** | **Integer** | Amount of time (in seconds) with the front base solenoid turned on.  _This field represents [messageBody.applicationMessage.applicationMessage.payload.frontBaseSolenoidBinned]_  |  [optional] |
|**frontRodSolenoidBinned** | **Integer** | Amount of time (in seconds) with the front rod solenoid turned on.  _This field represents [messageBody.applicationMessage.applicationMessage.payload.frontRodSolenoidBinned]_  |  [optional] |
|**rearBaseSolenoidBinned** | **Integer** | Amount of time (in seconds) with the rear base solenoid turned on.  _This field represents [messageBody.applicationMessage.applicationMessage.payload.rearBaseSolenoidBinned]_  |  [optional] |
|**rearRodSolenoidBinned** | **Integer** | Amount of time (in seconds) with the rear rod solenoid turned on.  _This field represents [messageBody.applicationMessage.applicationMessage.payload.rearRodSolenoidBinned]_  |  [optional] |
|**highFlowSolenoidBinned** | **Integer** | Amount of time (in seconds) with the high flow solenoid turned on.  _This field represents [messageBody.applicationMessage.applicationMessage.payload.highFlowSolenoidBinned]_  |  [optional] |
|**auxiliaryBinned** | **Integer** | Amount of time (in seconds) with auxiliaries turned on.  _This field represents [messageBody.applicationMessage.applicationMessage.payload.auxiliaryBinned]_  |  [optional] |
|**highFlowBinned** | **Integer** | Amount of time (in seconds) with high flow turned on.  _This field represents [messageBody.applicationMessage.applicationMessage.payload.highFlowBinned]_  |  [optional] |
|**hydraulicOilTemperatureBinned** | **Map&lt;String, Long&gt;** | Total amount of time (in seconds) spent in the given hydraulic oil temperature range while the machine is running (engine on). Bins (in order): 1. &lt; 38 °C 2. 38 to 59 °C 3. 60 to 70 °C 4. 71 to 81 °C 5. 82 to 87 °C 6. 88 to 93 °C 7. 94 to 98 °C 8. 99 to 104 °C 9. 105 to 110 °C 10. 111+ °C  _This field represents [messageBody.applicationMessage.applicationMessage.payload.hydraulicOilTemperatureBinned]_  |  [optional] |
|**machineStatus** | [**MachineStatus**](MachineStatus.md) |  |  [optional] |



