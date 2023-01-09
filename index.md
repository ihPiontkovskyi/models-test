# calamp-models

## Compiling and deploying

For assembly and integration of the generated models follow the release processing described [here](../../README.md)

## Usage

After the models' artifact was deployed, you can use bom dependency to include any package from datamodel that you need

```xml

<dependency>
  <groupId>com.doosan.iot.datamodel</groupId>
  <artifactId>bom</artifactId>
  <version>2.1.5-SNAPSHOT</version>
</dependency>
```

Also, you can insert calamp models dependency directly but preferred the first variant

## Model Serializing

At this moment, our generated models use Jackson for serialization and deserialization. All required fields for
inheritance will be set automatically.

**Serialization example**

```java
public class Example {
  public static void serialization(String[] args) throws IOException {
    // You need to instantiate Jackson Mapper to serialize/deserialize objects
    ObjectMapper mapper = new ObjectMapper()
        .registerModule(new JavaTimeModule());

    //Instantiate different fields of models
    MachineStatus status = new MachineStatus()
        .attachmentId(255L)
        .bobcatActiveFaultCount(0L)
        .cumulativeFuelUsage(94.5)
        .defLevel(93.2)
        .deviceBatteryVoltage(11.886)
        .dm1ActiveFaultCount(0L)
        .engineHours(18.85)
        .engineSpeed(0.0)
        .fuelLevel(87.6)
        .internalBatteryVoltage(0.926)
        .serviceClockHours(-18L)
        .userId(255L);

    UnitStatus unitStatus = new UnitStatus()
        .updateStatusError(false)
        .gpsAntennaError(false)
        .gpsSelfTestError(false)
        .gpsTracking(false);

    FixStatus fixStatus = new FixStatus()
        .flag2dFix(false)
        .historic(false)
        .lastKnown(false)
        .invalidFix(false)
        .differentiallyCorrected(false)
        .predicted(false)
        .invalidTime(false);

    CommState commState = new CommState()
        .available(true)
        .dataConnected(true)
        .dataService(true)
        .inRoaming(false)
        .networkService(false)
        .networkTechnology(CommState.NetworkTechnologyEnum.LTE_4G)
        .voiceConnected(false);

    CalampStatus eventStatus = new CalampStatus()
        .altitude(238.09)
        .carrier(410L)
        .hdop(1.2)
        .heading(181L)
        .latitude(44.9848555)
        .longitude(-93.2199235)
        .rssi(-66L)
        .satellites(10L)
        .speed(0.0)
        .timeOfFix(LocalDate.of(2022, 12, 15))
        .updateTime(LocalDate.of(2022, 12, 12))
        .unitStatus(unitStatus)
        .fixStatus(fixStatus)
        .commState(commState);

    //Instantiate application message for type 5 event
    BobcatInstantMessage message = new BobcatInstantMessage()
        .auxiliary(0L)
        .brakeSwitch(0L)
        .defConcentration(32.75)
        .defTemperature(15L)
        .doorPosition(1L)
        .driveResponse(1L)
        .driveState(0L)
        .engineCoolantTemperature(49L)
        .engineFuelTemperature(18L)
        .engineOilPressure(500L)
        .engineOilTemperature(92.75)
        .engineStateCrankingState(3L)
        .frontBaseSolenoid(0L)
        .frontRodSolenoid(0L)
        .fuelConsumption(2.05)
        .fuelRailPressure(0.3984375)
        .highFlow(0L)
        .highFlowSolenoid(0L)
        .hydraulicChargePressure(2874.0)
        .hydraulicOilTemperature(23L)
        .load(130L)
        .rearBaseSolenoid(0L)
        .rearRodSolenoid(0L)
        .seatbarPosition(1L)
        .steeringDriftForward(92L)
        .steeringDriftReverse(100L)
        .throttlePosition(16.0)
        .workgroupState(0L)
        .machineStatus(status);

    //Instantiate exact message for type 5 event
    CalampType5Event instantEvent = new CalampType5Event()
        .applicationMessage(message)
        .messageType(EVENT_REPORT_MESSAGE)
        .serviceType(ACKNOWLEDGED_REQUEST)
        .esn("6001001072")
        .sequenceNumber(68L)
        .status(eventStatus)
        .serialNumber("BS4B12237");

    CalampEvent calampEventModel = new CalampEvent()
        .calampIngestEvent(instantEvent);

    //serialization
    String eventString = mapper.writeValueAsString(calampEventModel);
  }
}
```

Example of json output

```json
{
  "calampIngestEvent": {
    "eventType": "CalampType5Event",
    "esn": "6001001072",
    "serialNumber": "BS4B12237",
    "serviceType": "ACKNOWLEDGED_REQUEST",
    "messageType": "EVENT_REPORT_MESSAGE",
    "sequenceNumber": 68,
    "status": {
      "altitude": 238.09,
      "rssi": -66,
      "hdop": 1.2,
      "latitude": 44.9848555,
      "longitude": -93.2199235,
      "speed": 0.0,
      "updateTime": 19338,
      "timeOfFix": 19341,
      "heading": 181,
      "satellites": 10,
      "carrier": 410,
      "fixStatus": {
        "invalidTime": false,
        "historic": false,
        "flag2dFix": false,
        "invalidFix": false,
        "lastKnown": false,
        "differentiallyCorrected": false,
        "predicted": false
      },
      "commState": {
        "networkTechnology": "LTE_4G",
        "inRoaming": false,
        "voiceConnected": false,
        "dataConnected": true,
        "dataService": true,
        "networkService": false,
        "available": true
      },
      "unitStatus": {
        "gpsTracking": false,
        "gpsSelfTestError": false,
        "gpsAntennaError": false,
        "updateStatusError": false
      }
    },
    "applicationMessage": {
      "applicationMessageId": "BobcatInstantMessage",
      "mapVersion": null,
      "defTemperature": 15,
      "engineCoolantTemperature": 49,
      "hydraulicOilTemperature": 23,
      "engineOilPressure": 500,
      "load": 130,
      "fuelRailPressure": 0.3984375,
      "hydraulicChargePressure": 2874.0,
      "throttlePosition": 16.0,
      "engineOilTemperature": 92.75,
      "defConcentration": 32.75,
      "engineFuelTemperature": 18,
      "fuelConsumption": 2.05,
      "brakeSwitch": 0,
      "seatbarPosition": 1,
      "doorPosition": 1,
      "workgroupState": 0,
      "driveState": 0,
      "driveResponse": 1,
      "steeringDriftForward": 92,
      "steeringDriftReverse": 100,
      "frontBaseSolenoid": 0,
      "frontRodSolenoid": 0,
      "rearBaseSolenoid": 0,
      "rearRodSolenoid": 0,
      "highFlowSolenoid": 0,
      "engineStateCrankingState": 3,
      "auxiliary": 0,
      "highFlow": 0,
      "machineStatus": {
        "engineHours": 18.85,
        "internalBatteryVoltage": 0.926,
        "deviceBatteryVoltage": 11.886,
        "fuelLevel": 87.6,
        "serviceClockHours": -18,
        "engineSpeed": 0.0,
        "defLevel": 93.2,
        "cumulativeFuelUsage": 94.5,
        "attachmentId": 255,
        "userId": 255,
        "dm1ActiveFaultCount": 0,
        "bobcatActiveFaultCount": 0
      }
    }
  }
}
```

## Model Deserializing

At this place you have a separate cases

1. If you need to process a concrete message type with a concrete application message payload (means that you know what
   exactly types are, based on IoT topics)

```java
public class Example {
  public static void deserialization(String[] args) throws IOException {
    // You need to instantiate Jackson Mapper to serialize/deserialize objects
    ObjectMapper mapper = new ObjectMapper().registerModule(new JavaTimeModule());
    // eventString - means serialized json
    String eventString = "eventString";

    //deserializing of json
    CalampEvent calampEvent = mapper.readValue(cleansedString, CalampEvent.class);
    //cast to type 5 (same approach for type 2)
    CalampType5Event type5Event = (CalampType5Event) calampEvent.getCalampIngestEvent();
    //cast to proper application message
    BobcatInstantMessage message = (BobcatInstantMessage) type5Event.getApplicationMessage();
  }
}
```

2. If you don't know anything about message type and payload, and you need to process common fields for all types (like
   location, etc)

```java
public class Example {
  public static void deserialization(String[] args) throws IOException {
    // You need to instantiate Jackson Mapper to serialize/deserialize objects
    ObjectMapper mapper = new ObjectMapper().registerModule(new JavaTimeModule());
    // eventString - means serialized json
    String eventString = "eventString";

    //deserializing of json
    CalampEvent calampEvent = mapper.readValue(cleansedString, CalampEvent.class);
    //cast to domain event that include all common fields
    CalampIngestEvent event = calampEvent.getCalampIngestEvent();
  }
}
```

## Details for models

Inside the CalampEvent model, we store a field with the type CalampIngestEvent,
CalampType5Event and CalampType2Event inherit CalampIngestEvent, and CalampIngestEvent store common fields for type 2 and type 5 events

Same approach was used for application message

[BobcatApplicationMessage](/BobcatApplicationMessage.md))
[BobcatApplicationMessage](/BobcatApplicationMessage.md)
[BobcatEngineFaultCodesMessage](/BobcatEngineFaultCodesMessage.md)
[BobcatHeatmapMessage](/BobcatHeatmapMessage.md)
[BobcatInstantMessage](/BobcatInstantMessage.md)
[BobcatMultipleFaultMessage](/BobcatMultipleFaultMessage.md)
[BobcatRunMessage](/BobcatRunMessage.md)
[BobcatRunUsageMessage](/BobcatRunUsageMessage.md)
[BobcatSoftMessage](/BobcatSoftMessage.md)
[CalampEvent](/CalampEvent.md)
[CalampIngestEvent](/CalampIngestEvent.md)
[CalampStatus](/CalampStatus.md)
[CalampType2Event](/CalampType2Event.md)
[CalampType5Event](/CalampType5Event.md)
[CommandResult](/CommandResult.md)
[CommState](/CommState.md)
[FixStatus](/FixStatus.md)
[MachineStatus](/MachineStatus.md)

