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

![](https://www.websequencediagrams.com/cgi-bin/cdraw?lz=VGl0bGUgcGVvcGxlTGVhcm5pbmcgYW5kAAwHUmVjb2duaXRpb24KCgpQYXJ0aWNpcGFudCBUYWJsZXQABg1QUFJlY29BcHAKIwAeDG9wZW5GYWNlCgpub3RlIGxlZnQgb2YAOgc6CiAgICBsAHIIZXZlbnQgY29tZXMKZW5kIG5vdAAiFgAyBXByZXZpZXcAPgUgKCAgICApAAELKQA3CwCBKAYtPgCBGgk6IHJvc3NlcnZpY2UgY2FsbCAvdHJhaW4AgXsFIm5hbWU6ICdMYWJlbCciACcYdG9waWM6IC9pbWFnZXMKAIF2CS0-AIFVBwAZDGNhcHR1cmluZ1Byb2dyZXNzICgxMCUpAARYMgBEGC4uLgB2WgCBTAUAg2EFcmlnaACDYgUAhAsKICAgIHN0YXJ0IACCZQVpbmcgdGhlIG1vZGVsAINKI3N0b3Agc2VuZGluZyAAgmwHAIQZCgoAgmAfAGsIAIJvDwAFMACCUgUAOjAzAFMXLi4uAIEDMwCCWgoAhjYUcgCHJwoAhjYXAIVnJHdob2FtaSAicmVxdWVzdDogJ3lvJyIAhWEmAIYHJQCFARgAhi4WAIcgCHJlc3BvbmQgWwCBWwtSZXN1bHRzXQoKCgoKCg&s=modern-blue)

* Services & Topics 
 * rosservice call /trainning
 
        (name: 'Label' )

 * rostopic: images  

        (topic name: /images, type: sensor_msgs/image, Hz=??)
         
 * rostopic: capturingProgress 
 
        (topic name: /capturingProgress, type: std_msgs/UInt8, value: 0~100 )
        (when the value = 100, the tablet app should stop publishing anymore images)

 * rostopic: trainingProgress 
         
        (topic name: /trainingProgress, type: std_msgs/UInt8, value: 0~100) )
 
 * rosservice call /whoami "request: 'yo'"   // to start recognition
 
         
 * rosservice respond recognitionResult 
 
        ??(topic name: /recognitionResult, type: std_msgs/String, value: "display name" )

* Implementations
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

