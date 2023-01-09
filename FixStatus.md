

# FixStatus

The current fix status of the GPS receiver

## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**invalidTime** | **Boolean** | Indicate is a machine in state after a power-up or reset and before a valid time-sync has been obtained.    _This field represents [messageBody.status.fixStatus.payload.flagInvalidTime]_  |  [optional] |
|**historic** | **Boolean** | Indicate is the message has been logged by the LMU.    _This field represents [messageBody.status.fixStatus.payload.flagHistoric]_  |  [optional] |
|**flag2dFix** | **Boolean** | Indicates when 3 or fewer satellites are seen/used in the GPS fix. (i.e. with 3 satellites or less, an altitude value cannot be calculated)    _This field represents [messageBody.status.fixStatus.payload.flag2dFix]_  |  [optional] |
|**invalidFix** | **Boolean** | Indicates is a machine in state after a power-up or reset and before a valid fix is obtained.  _This field represents [messageBody.status.fixStatus.payload.flagInvalidFix]_  |  [optional] |
|**lastKnown** | **Boolean** | Indicates when the current GPS fix is invalid but a previous fix’s value is available.  _This field represents [messageBody.status.fixStatus.payload.flagLastKnown]_  |  [optional] |
|**differentiallyCorrected** | **Boolean** | Indicates when WAAS DGPS is enabled (S-Register 139) and the position has been differentially corrected  _This field represents [messageBody.status.fixStatus.payload.flagDifferentiallyCorrected]_  |  [optional] |
|**predicted** | **Boolean** | Indicates when the position update has a horizontal position accuracy estimate that is less than the Horizontal Position Accuracy Threshold defined in S-Register 142 (and the threshold is non-zero).  _This field represents [messageBody.status.fixStatus.payload.flagPredicted]_  |  [optional] |



