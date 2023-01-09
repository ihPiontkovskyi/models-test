

# CalampType2Event


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**eventIndex** | **Integer** | The index number of the event that generated the report; values should range from 0-249. 255 represents a Real Time PEG Action request.          _This field represents [messageBody.eventIndex]_  |  [optional] |
|**eventCode** | [**EventCodeEnum**](#EventCodeEnum) | The event code assigned to the report as specified by the event’s Action Parameter  _This field represents [messageBody.eventCode]_  |  [optional] |
|**machineStatus** | [**MachineStatus**](MachineStatus.md) |  |  [optional] |



## Enum: EventCodeEnum

| Name | Value |
|---- | -----|
| ENTER_KEY | &quot;ENTER_KEY&quot; |
| START | &quot;START&quot; |
| HEARTBEAT_KEY_ON | &quot;HEARTBEAT_KEY_ON&quot; |
| STOP | &quot;STOP&quot; |
| REMOVE_KEY | &quot;REMOVE_KEY&quot; |
| PING | &quot;PING&quot; |
| START_TRAILERING | &quot;START_TRAILERING&quot; |
| STOP_TRAILERING | &quot;STOP_TRAILERING&quot; |
| HEARTBEAT_TRAILERING_6H | &quot;HEARTBEAT_TRAILERING_6H&quot; |
| HEARTBEAT_TRAILERING_20MIN | &quot;HEARTBEAT_TRAILERING_20MIN&quot; |
| LOW_BATTERY | &quot;LOW_BATTERY&quot; |
| GEOFENCE_CHANGE | &quot;GEOFENCE_CHANGE&quot; |
| EXTREMELY_LOW_BATTERY | &quot;EXTREMELY_LOW_BATTERY&quot; |
| ATTACHMENT_NUMBER_CHANGE | &quot;ATTACHMENT_NUMBER_CHANGE&quot; |
| USER_ID_CHANGE | &quot;USER_ID_CHANGE&quot; |
| EXTERNAL_POWER | &quot;EXTERNAL_POWER&quot; |
| INTERNAL_BATTERY | &quot;INTERNAL_BATTERY&quot; |



