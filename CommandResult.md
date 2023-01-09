

# CommandResult


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**commandId** | [**CommandIdEnum**](#CommandIdEnum) | Command  _This field represents [messageBody.applicationMessage.applicationMessage.payload.commandId]_  |  [optional] |
|**commandCorrelationId** | **Long** | Random ID supplied by the Bobcat IoTPlatform  _This field represents [messageBody.applicationMessage.applicationMessage.payload.commandCorrelationId]_  |  [optional] |
|**commandResult** | [**CommandResultEnum**](#CommandResultEnum) | Outcome of the command  _This field represents [messageBody.applicationMessage.applicationMessage.payload.commandResult]_  |  [optional] |
|**commandParameterCount** | **Integer** | Number of 64 byte parameters in theCommand  _This field represents [messageBody.applicationMessage.applicationMessage.payload.commandParameters.commandParameterCount]_  |  [optional] |
|**sourceAddress** | **Integer** | CAN Source address of the Controllerwhich requested the RESP Active (Lock)Command  _This field represents [messageBody.applicationMessage.applicationMessage.payload.commandParameters.sourceAddress]_  |  [optional] |



## Enum: CommandIdEnum

| Name | Value |
|---- | -----|
| ACTIVE | &quot;REMOTE_ENGINE_START_PREVENTION_ACTIVE&quot; |
| INACTIVE | &quot;REMOTE_ENGINE_START_PREVENTION_INACTIVE&quot; |



## Enum: CommandResultEnum

| Name | Value |
|---- | -----|
| SUCCESS | &quot;SUCCESS&quot; |
| FAIL_START_NOT_REQUESTED | &quot;FAIL_START_NOT_REQUESTED&quot; |
| FAIL_STARTER_ACTIVE_GEAR_NOT_ENGAGED | &quot;FAIL_STARTER_ACTIVE_GEAR_NOT_ENGAGED&quot; |
| FAIL_STARTER_ACTIVE_GEAR_ENGAGED | &quot;FAIL_STARTER_ACTIVE_GEAR_ENGAGED&quot; |
| FAIL_START_FINISHED_INACTIVE_AFTER_PERIOD_OF_ACTIVITY | &quot;FAIL_START_FINISHED_INACTIVE_AFTER_PERIOD_OF_ACTIVITY&quot; |
| FAIL_STARTER_INHIBITED_DUE_TO_ENGINE_ALREADY_RUNNING | &quot;FAIL_STARTER_INHIBITED_DUE_TO_ENGINE_ALREADY_RUNNING&quot; |
| FAIL_STARTER_INHIBITED_DUE_TO_ENGINE_NOT_READY_TO_START | &quot;FAIL_STARTER_INHIBITED_DUE_TO_ENGINE_NOT_READY_TO_START&quot; |
| FAIL_STARTER_INHIBITED_DUE_TO_DRIVELINE_ENGAGED | &quot;FAIL_STARTER_INHIBITED_DUE_TO_DRIVELINE_ENGAGED&quot; |
| FAIL_STARTER_INHIBITED_DUE_TO_ACTIVE_IMMOBILIZER | &quot;FAIL_STARTER_INHIBITED_DUE_TO_ACTIVE_IMMOBILIZER&quot; |
| FAIL_STARTER_INHIBITED_DUE_TO_STARTER_OVER_TEMP | &quot;FAIL_STARTER_INHIBITED_DUE_TO_STARTER_OVER_TEMP&quot; |
| FAIL_STARTER_INHIBITED_REASON_UNKNOWN | &quot;FAIL_STARTER_INHIBITED_REASON_UNKNOWN&quot; |
| FAIL_ECU_ERROR_LEGACY | &quot;FAIL_ECU_ERROR_LEGACY&quot; |
| FAIL_ERROR | &quot;FAIL_ERROR&quot; |
| FAIL_NA | &quot;FAIL_NA&quot; |
| REMOTE_ENGINE_START_PREVENTION_ENABLED_NOT_ACTIVATED | &quot;REMOTE_ENGINE_START_PREVENTION_ENABLED_NOT_ACTIVATED&quot; |
| REMOTE_ENGINE_START_PREVENTION_ACTIVATED_LOCKED | &quot;REMOTE_ENGINE_START_PREVENTION_ACTIVATED_LOCKED&quot; |
| REMOTE_ENGINE_START_PREVENTION_DISABLED_UNLOCKED | &quot;REMOTE_ENGINE_START_PREVENTION_DISABLED_UNLOCKED&quot; |
| REMOTE_ENGINE_START_PREVENTION_UNKNOWN | &quot;REMOTE_ENGINE_START_PREVENTION_UNKNOWN&quot; |
| FAIL_ECU_ERROR | &quot;FAIL_ECU_ERROR&quot; |
| FAIL_TIMEOUT | &quot;FAIL_TIMEOUT&quot; |



