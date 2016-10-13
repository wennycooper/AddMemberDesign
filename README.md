# AddMemberDesign

# Introduction

# Architecture
![](https://docs.google.com/drawings/d/1hBYZEY3nbv3LDb4_GBEzU-ImwHIez7PBUzLJudvB6HE/pub?w=1125&h=731)

# People Learning and Recognition
* Sequence Diagram
![](https://www.websequencediagrams.com/cgi-bin/cdraw?lz=VGl0bGUgcGVvcGxlTGVhcm5pbmcgYW5kAAwHUmVjb2duaXRpb24KCgpQYXJ0aWNpcGFudCBUYWJsZXQABg1QUFJlY29BcHAAHA1DT0IKCm5vdGUgbGVmdCBvZgAzCCAgICBwcmV2aWV3AAcFICggICAgKQABCykKZW5kIG5vdGUKCgBqBi0-AFwJOiBzdGFydENhcHR1cmluZwAOFWltYWdlcwABGQABGQAeFi4uLgoAgVwJLT4AgX0GOiBjAHsIUHJvZ3Jlc3MAASQAASQANBYuLi4AggUKAHwIc3RvcFNlbmRpbmdQaG90b3MAghwWZXRMYWJlbACCNRpUcmFpbmluZwCBVBR0ABUHAIFLHAABIwAjJQCBYAUAhCMTOgCEMgVyAIUNCiBldmVudCBjb21lcwCEDCMAhUUMAIM4XgCBGQtSZXN1bHRzCgoKCgoK&s=modern-blue)

* Topics 
 * startCapturing
 
        (topic name: /startCapturing, type: std_msgs/UInt8, value: 1(start) )

 * images 

        (topic name: /images, type: sensor_msgs/image, Hz=??)
         
 * capturingProgress 
 
        (topic name: /capturingProgress, type: std_msgs/UInt8, value: 0~100 )

 * setLabel 
 
        (topic name: /setLabel, type: std_msgs/String, value: "display name")
 
 * startTraining 
        
        (topic name: /startTraining, type: std_msgs/UInt8, value: 1(start) )
 
 * trainingProgress 
         
        (topic name: /trainingProgress, type: std_msgs/UInt8, value: 0~100) )
 
 * startRecognition 
 
        (topic name: /startRecognition, type: std_msgs/UInt8, value: 1(start) )
 
 * recognitionResult 
 
        (topic name: /recognitionResult, type: std_msgs/String, value: "display name" )

* Implementations
 * Tablet app
 * PPRecoApp on ROS


# AddMember
* Sequence Diagram
![](https://www.websequencediagrams.com/cgi-bin/cdraw?lz=VGl0bGUgYWRkTWVtYmVyIEZsb3cKClBhcnRpY2lwYW50IFJvYm90AAUNQ2xvdWQAFw1QaG9uZQoKACYFLT4AGwU6IGxvZ2luIHJlcS4KAC0FLT4ARgUADwpzcC4odG9rZW4pCm5vdGUgbGVmdCBvZgBrByAgIACBDQtldmVudAplbmQgbm90AGEKAEsHW29wdC1pbl0gZ2VuZXJhdGVBUEtRUkNvZGUKAEgTOgBXBVtRUjFdAEgKAIE1BwCBRQU6ABYHAIFSBQALCWluc3RhbGwgYXBwAAsPbGF1bmNoABQFAIF1EGFkZEFub255bW91c0ZyaWVuZACCDQUgKGRpc3BsYXlOYW1lLCByb2JvdElkKQCCIQgAgjsHAIFGCFVzZXIAgh0GcmlnaACCHwUAgn4GICAgIAA-CwCCLwV1c2VybgAFCHBhc3N3ACIGAF0HAII5CwCDCA8AgRYVc3AuICgASwgsAEkHKQCCcBAAgm4JY2Nlc3MAgnMHAIJeGzIAgmgRAIJuDDJdAIMcGWJsb2NrZQCBOQwAgxYOc2NhbgB4DQCCKA8Ag1gHAIIQGQBHEQCFMxkAg3MIAIU6EgAsDwCDVwVzACgUABEJc3AuKACDfgVMaXN0ADcKAIUFB3RyeUNvbm5lY3QAhwQHAIUQBgCGRgd3ZWJydGMgY2FsbACFUhl1bgCCJhIKCg&s=modern-blue)



* Implementations
 * Tablet app
 * Cloud service
 * Phone app
