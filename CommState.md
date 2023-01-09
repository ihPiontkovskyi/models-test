

# CommState

The current state of the wireless modem bit

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**networkTechnology** | [**NetworkTechnologyEnum**](#NetworkTechnologyEnum) | Network Technology  _This field represents [messageBody.status.commState.networkTechnology]_  |  [optional] |
|**inRoaming** | **Boolean** | Indicates when roaming used  _This field represents [messageBody.status.commState.flag_voice_connected]_  |  [optional] |
|**voiceConnected** | **Boolean** | Indicates when Voice Call is Active  _This field represents [messageBody.status.commState.flag_roaming]_  |  [optional] |
|**dataConnected** | **Boolean** | Indicates when Connected (PPP Session Up)  _This field represents [messageBody.status.commState.flag_data_connected]_  |  [optional] |
|**dataService** | **Boolean** | Data Service  _This field represents [messageBody.status.commState.flag_data_service]_  |  [optional] |
|**networkService** | **Boolean** | Network Service  _This field represents [messageBody.status.commState.flag_network_service]_  |  [optional] |
|**available** | **Boolean** | Available  _This field represents [messageBody.status.commState.flag_available]_  |  [optional] |



## Enum: NetworkTechnologyEnum

| Name | Value |
|---- | -----|
| CDMA_GSM_2G | &quot;CDMA_GSM_2G&quot; |
| UMTS_3G | &quot;UMTS_3G&quot; |
| LTE_4G | &quot;LTE_4G&quot; |
| RESERVED | &quot;RESERVED&quot; |



