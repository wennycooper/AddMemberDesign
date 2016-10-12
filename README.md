# AddMemberDesign

# Introduction

# Architecture
![](https://docs.google.com/drawings/d/1hBYZEY3nbv3LDb4_GBEzU-ImwHIez7PBUzLJudvB6HE/pub?w=1125&h=731)

# AddMember
* Sequence Diagram
![](https://www.websequencediagrams.com/cgi-bin/cdraw?lz=VGl0bGUgYWRkTWVtYmVyIEZsb3cKClBhcnRpY2lwYW50IFJvYm90AAUNQ2xvdWQAFw1QaG9uZQoKACYFLT4AGwU6IHNpZ25JbiByZXEuCgAuBS0-AEcFAA8Lc3AuKHRva2VuKQpub3RlIGxlZnQgb2YAbQcgICAAgQ8LZXZlbnQKZW5kIG5vdABjCgBMB1tvcHQtaW5dIGdlbmVyYXRlQVBLUVJDb2RlCgBIEzoAVwVbUVIxXQBICgCBNwcAgUcFOgAWBwCBVAUACwlpbnN0YWxsIGFwcAALD2xhdW5jaAAUBQCBdxBhZGRGcmllbmQAggUFIChkaXNwTmFtZSwgcm9ib3RJZCkAghYIAIIxBwCBOghVc2VyAIIRBnJpZ2gAghMFAIJ0BiAgICB1c2VyTmFtZQCCIAUASwgAgi0FcGFzc3cAHwYAWgcAgioLAIJ6DwCBEAxzcC4gKABPCCwAQAcpAIJYEACCVgljY2VzcwCCWwcAgkYbMgCCRRwyXQCDAxlibG9ja2UAgS8MAIJ9DnNjYW4Adw0AghsPAIM_BwCCGhIAghgHAEcRAIUbGgBqCACFIhMALg9nZXQAhikFTGlzdAAvFAARD3NwLigAg38FTGlzdABDCgCEegd0cnlQaW5nAIZ4BwCBFw5lbmROb3RpZmljYXRpbwCGXgYARQYAhEQLAIZmB0dDTQCFaRl1bgCCVhIKCgo&s=modern-blue)



* Implementations
 * Tablet app
 * Cloud service
 * Phone app
 

# People Learning and Recognition
* Sequence Diagram
![](https://www.websequencediagrams.com/cgi-bin/cdraw?lz=VGl0bGUgcGVvcGxlTGVhcm5pbmcgYW5kAAwHUmVjb2duaXRpb24KCgpQYXJ0aWNpcGFudCBUYWJsZXQABg1QUFJlY29BcHAAHA1DT0IKCm5vdGUgbGVmdCBvZgAzCCAgICBwcmV2aWV3AAcFICggICAgKQABCykKZW5kIG5vdGUKCgBqBi0-AFwJOiBzdGFydENhcHR1cmluZwAOFWltYWdlcwABGQABGQAeFi4uLgoAgVwJLT4AgX0GOiBjAHsIUHJvZ3Jlc3MAASQAASQANBYuLi4AggUKAHwIc3RvcFNlbmRpbmdQaG90b3MAghwWZXRMYWJlbACCNRpUcmFpbmluZwCBVBR0ABUHAIFLHAABIwAjJQCBYAUAhCMTOgCEMgVyAIUNCiBldmVudCBjb21lcwCEDCMAhUUMAIM4XgCBGQtSZXN1bHRzCgoKCgoK&s=modern-blue)

* Topics 
 * startCapturing (topic name: /startCapturing, type: std_msgs/UInt8)
 * images (topic name: /images, type: sensor_msgs/image, Hz=??)
 * capturingProgress
 * setLabel
 * startTraining
 * trainingProgress
 * startRecognition
 * recognitionResult

* Implementations
 * Tablet app
 * PPRecoApp on ROS
