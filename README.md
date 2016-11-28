# AddMemberDesign

# Meetings
* [2016/10/12] Initial draft review
* [2016/10/13] Final design review
* [2016/11/28] Design revised by Will and KKuei

# Introduction

# Architecture
![](https://docs.google.com/drawings/d/1hBYZEY3nbv3LDb4_GBEzU-ImwHIez7PBUzLJudvB6HE/pub?w=1125&h=731)

# People Learning and Recognition
* Sequence Diagram

![](https://www.websequencediagrams.com/cgi-bin/cdraw?lz=VGl0bGUgcGVvcGxlTGVhcm5pbmcgYW5kAAwHUmVjb2duaXRpb24KCgpQYXJ0aWNpcGFudCBUYWJsZXQABg1QUFJlY29BcHAKIwAeDG9wZW5GYWNlCgpub3RlIGxlZnQgb2YAOgc6CiAgICBsAHIIZXZlbnQgY29tZXMKZW5kIG5vdAAiFgAyBXByZXZpZXcAPgUgKCAgICApAAELKQA3CwCBKAYtPgCBGgk6IHJvc3RvcGljOiAvY21kVHJhaW4AgXgFKHdpdGggbGFiZWwpABghcm9wcGVkSW1hZ2VzCgCBdwktPgCBVgcAWA1hcHR1cmluZ1Byb2dyZXNzICgxMCUAA2AyAEsYLi4uAH1hAIFaBQCDcAVyaWdoAINxBQCEGgogICAgc3RhcnQgdHJhaQCEcwV0aGUgbW9kZWwAg1kjc3RvcCBzZW5kaW5nIGkAgnsGAIQoCgoAgm4fAGsIAIJ9DwAFMACCWQUAOjAzAFMXLi4uAIEDMwCCWgoAhkUUcgCHNgoAhkUXAIV5IQCHdwwAhWIsAIYOLACFCBgAhjQeAIFSC1Jlc3VsdHMKCgoKCgoK&s=modern-blue)

* Topic names and message types 
 * rostopic /cmdTrainning   // command to start training with label
>topic name: /cmdTraining, type: std_msgs/String  
>values: data = label

 * rostopic: /croppedImages  
>topic name: /croppedImages, type: sensor_msgs/image
         
 * rostopic: /capturingProgress 
>topic name: /capturingProgress, type: std_msgs/UInt8, 
>values: data = 0~100 (Note: when the value.data = 100, the tablet app should stop publishing images)

 * rostopic: /trainingProgress 
>topic name: /trainingProgress, type: std_msgs/UInt8, 
>values: data = 0~100 
 
 * rostopic: /cmdRecognition   // to start recognition
>topic name: /cmdRecognition, type: std_msgs/Bool
>values: data = True
         
 * rostopic: /recognitionResults   
>topic name: /recognitionResults, type: std_msgs/String
>values: data = label 

* Implementations on
 * Tablet app
 * PPRecoApp on ROS


# AddMember
* Sequence Diagram
![](https://www.websequencediagrams.com/cgi-bin/cdraw?lz=VGl0bGUgYWRkTWVtYmVyIEZsb3cKClBhcnRpY2lwYW50IFJvYm90AAUNQ2xvdWQAFw1QaG9uZQoKACYFLT4AGwU6IGxvZ2luIHJlcS4KAC0FLT4ARgUADwpzcC4odG9rZW4pCm5vdGUgbGVmdCBvZgBrByAgIACBDQtldmVudAplbmQgbm90AGEKAEsHW29wdC1pbl0gZ2VuZXJhdGVBUEtRUkNvZGUKAEgTOgBXBVtRUjFdAEgKAIE1BwCBRQU6ABYHAIFSBQALCWluc3RhbGwgYXBwAAsPbGF1bmNoABQFAIF1EGFkZEFub255bW91c0ZyaWVuZACCDQUgKGRpc3BsYXlOYW1lLCByb2JvdElkKQCCIQgAgjsHAIFGCFVzZXIAgh0GcmlnaACCHwUAgn4GICAgIAA-CwCCLwV1c2VybgAFCHBhc3N3ACIGAF0HAII5CwCDCA8AgRYVc3AuICgASwgsAEkHKQCCcBAAgm4JY2Nlc3MAgnMHAIJeGzIAgmgRAIJuDDJdAIMcGWJsb2NrZQCBOQwAgxYOc2NhbgB4DQCCKA8Ag1gHAIIQGQBHEQCFMxkAg3MIAIU6EgAsDwCDVwVzACgUABEJc3AuKACDfgVMaXN0ADcKAIUFB3RyeUNvbm5lY3QAhwQHAIUQBgCGRgd3ZWJydGMgY2FsbACFUhl1bgCCJhIKCg&s=modern-blue)


* Implementations
 * Tablet app
 
    1. store a label <-> displayName mapping table
    2. convert images to ROS messages (type: std_msgs/Image) and publishing 
    3. call related APIs
    
  
 * Cloud service
 
    1. add a new web service "addAnonymousFriend"
   
 * Phone app

# References

