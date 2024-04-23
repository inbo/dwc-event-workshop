```mermaid
flowchart LR
    deployment("deployment"):::deployment
    seq1("sequence"):::observation
    seq2("sequence"):::observation

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
    cameraModel("cameraModel"):::deployment
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

%% Deployment level

deployment --> seq1
deployment --> seq2

deployment --> deploymentStart
deployment --> deploymentEnd
deployment --> latitude
deployment --> longitude
deployment --> habitat
deployment --> cameraModel
deployment --> baitUse
deployment --> deploymentGroups

%% Sequence 1
seq1 --> obs1
seq1 --> media1
seq1 --> media2
seq1 --> media3
seq1 --> media4

    %% Sequence-based observation 1
        obs1--> eventStart
        obs1 --> eventEnd
        obs1 --> count
        obs1 --> observationType
        obs1 --> scientificName
        obs1 --> etc

    %% Media-based observation 1
        media1 --> obs2
        media2 --> obs3
        media3 --> obs4
            obs4 --> eventStart2
            obs4 --> eventEnd2
            obs4 --> count2
            obs4 --> observationType2
            obs4 --> lifeStage
            obs4 --> sex
            obs4 --> scientificName2
            obs4 --> classification
            obs4 --> bboxX
        media4 --> obs5

%% Sequence 2
seq2 --> obs6
seq2 --> obs7
seq2 --> media5
seq2 --> media6

    %% Media-based observation 2
        media5 --> obs8
        media6 --> obs9


        %% Multimedia files
        media5 --> captureMethod
        media5 --> timestamp
        media5 --> filePath
        media5 --> fileName
        media5 --> fileMediaType

```
