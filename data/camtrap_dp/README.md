```mermaid
flowchart LR
    deployment("deployment"):::deployment
    event1("event"):::observation
    event2("event"):::observation

    obs1("observation"):::observation
    obs2("observation"):::observation
    obs3("observation"):::observation
    obs4("observation"):::observation
    obs5("observation"):::observation
    obs6("observation"):::observation
    obs7("observation"):::observation
    obs8("observation"):::observation
    obs9("observation"):::observation
    

    media1("media"):::observation
    media2("media"):::observation
    media3("media"):::observation
    media4("media"):::observation
    media5("media"):::observation
    media6("media"):::observation

    latitude("latitude"):::deployment
    longitude("longitude"):::deployment
    deploymentStart("deploymentStart"):::deployment
    deploymentEnd("deploymentEnd"):::deployment
    cameratraits("camera traits (8)"):::deployment
    baitUse("baitUse"):::deployment
    habitat("habitat"):::deployment
    deploymentGroups("deploymentGroups"):::deployment

    eventStart("eventStart"):::observation
    eventEnd("eventEnd"):::observation
    observationType("observationType"):::observation
    scientificName("scientificName"):::observation
    count("count"):::observation
    lifeStage("lifeStage"):::observation
    sex("sex"):::observation
    bboxX("bboxX"):::observation
    classification("classification"):::observation

    eventStart2("eventStart"):::observation
    eventEnd2("eventEnd"):::observation
    observationType2("observationType"):::observation
    scientificName2("scientificName"):::observation
    count2("count"):::observation
    etc("..."):::observation

    captureMethod("captureMethod"):::media
    timestamp("timestamp"):::media
    filePath("filePath"):::media
    fileName("fileName"):::media
    fileMediaType("fileMediaType"):::media

    classDef deployment fill:#fff,stroke-width:4px,stroke:#000;
    classDef observation fill:#ccc,stroke-width:1px,stroke:#000;
    classDef media       fill:#fff,stroke-width:1px,stroke:#000, stroke-dasharray:6;

deployment --> event1
deployment --> latitude
deployment --> longitude
deployment --> deploymentStart
deployment --> deploymentEnd
deployment --> cameratraits
deployment --> baitUse
deployment --> habitat
deployment --> deploymentGroups


    event1 --> obs1
        obs1 --> count2
        obs1--> eventStart2
        obs1 --> eventEnd2
        obs1 --> observationType2
        obs1 --> scientificName2
        obs1 --> etc

    event1 --> media1
        media1 --> obs2
             obs2 --> classification
    event1 --> media2
        media2 --> obs3
    event1 --> media3
        media3 --> obs4
            obs4 --> count
            obs4 --> lifeStage
            obs4 --> sex
            obs4 --> eventStart
            obs4 --> eventEnd
            obs4 --> observationType
            obs4 --> scientificName
            obs4 --> bboxX
    event1 --> media4
        media4 --> obs5


deployment --> event2
    event2 --> obs6
    event2 --> obs7
   
    event2 --> media5
        media5 --> obs8
        media5 --> captureMethod
        media5 --> timestamp
        media5 --> filePath
        media5 --> fileName
        media5 --> fileMediaType
    event2 --> media6
        media6 --> obs9
```
