# Table of Contents
- [1. Introduction](#1-introduction) 
   * [1.1 Project Overview](#11-project-overview)
   * [1.2 Project Deliverables](#12-project-deliverables)
   * [1.3 References](#13-references)
- [2. Decomposition Description](#2-decomposition-description)
   * [2.1 Module Decomposition](#21-module-decomposition)
       - [2.1.1 Framework Package Interactions](#211-framework-package-interactions)    
    - [2.1.2 Shout! Model Class Diagram](#212-shout!-model-class-diagram)
- [3. Interface Descriptions](#3-interface-descriptions)
   * [3.1 Colour Guidelines](#31-colour-guidelines)
   * [3.2 Font Guidelines](#32-font-guidelines)
   * [3.3 App Icons](#33-app-icons)
   * [3.4 Module Interface](#34-module-interface)
       - [3.4.1 Bluetooth View](#341-bluetooth-view)
    - [3.4.2 Home View](#342-home-view)
    - [3.4.3 Chat View](#343-chat-view)
    - [3.4.4 Settings View](#344-settings-view)
    - [3.4.5 Notification View](#345-notification-view)
    - [3.4.6 Report View](#346-report-view)
    - [3.4.7 About View](#347-about-view)
 - [4. Technical Process](#4-technical-process)
    * [4.1 Methods, Tools and Techniques](#41-methods-tools-techniques)
    * [4.2 Software Documentation](#42-software-documentation)
    
     
# 1. Introduction 

## 1.1 Project Overview

Shout! is a Bluetooth low energy (BLE) mesh-based messaging application that is supported on Android and iOS. It allows users to talk to other users within a single messaging room as long as they are all connected to the same Bluetooth mesh.

## 1.2 Project Deliverables

|no. | Deliverable | Deadline | Adjusted Deadline | 
| ----- | ---- | ----------- | ------- |
|1|Requirements| May 22, 2018| May 29, 2018|
|2|Requirements SQA| May 24, 2018| May 31, 2018|
|3|Analysis| June 2, 2018| June 2, 2018|
|4|Analysis SQA| June 19, 2018| June 4, 2018|
|5|GUI Prototype| June 21, 2018| July 10, 2018|
|6|GUI Prototype SQA| June 26, 2018| July 12, 2018|
|7|SPMP| June 26, 2018| - |
|8|SPMP SQA| June 28, 2018| - |
|9|Design| July 3, 2018| July 15, 2018|
|10|Design SQA| July 5 2018| July 17, 2018|
|11|Implementation| August 7, 2018| August 7, 2018|
|11|Implementation SQA| August 13, 2018| August 13, 2018|
Note: Testing runs in parallel with all deliverables


## 1.3 References

- Software Requirements Specification document for Shout!
- Analysis document for Shout!
- IEEE. IEEE Std 1016-1998 IEEE Recommended Practice for Software Design Descriptions. IEEE Computer Society, 1998

## 1.4 Overview 

This document is written following the guidelines of the IEEE Recommended Practice for Software Design Descriptions. It outlines the module, process, and data dependencies, as well as their detailed design and decomposition.

# 2. Decomposition Description 
## 2.1 Module Decomposition

### 2.1.1 Framework Package Interactions 

This design shows how the user interacts with the front end of the app (GUI), and then how the front end interacts with the backend


### 2.1.2 Shout! Model Class Diagram


### Android


# 3. Interface Descriptions
## 3.1 Colour Guidelines 


## 3.2 Font Guidelines 

- iOS: System Default (San Francisco)
- Android: Roboto
- Username colour: Web Safe Colours

## 3.3 App Icons



## 3.4 Module Interface 
### 3.4.1 Bluetooth View 



| Field | Type | Description | Gesture | 
| ----- | ---- | ----------- | ------- |
|lblChat|Label|Describes purpose of application||
|imgBluetooth|Image|Visualization of the Bluetooth symbol||
|btnStart|Button|Allows entrance to application only after bluetooth has been enable. |→  Home View|

### 3.4.2 Home View 



| Field | Type | Description | Gesture | 
| ----- | ---- | ----------- | ------- |
|imgLogo|Image|Application logo||
|lblNumber|Label|Dynamic number displaying the amount of reachable people from user current position||
|lblNearby|Label|Describes the purpose of the number||
|lblDisclaimers|Label|A disclaimer statement | → Terms of Service |
|btnEnter|Button|Allows entrance to Chat View only after a username has been submitted |→ Chat View |
|btnSettings|Button| Brings user to the Settings View where they can change preferences | → Setting View |
|txtfieldUsername | Text Field | Required username input before entrance to Chat View This is how the user will be identified in the chat. Must be distinct and 15 characters in length| |

### 3.4.3 Chat View 



| Field | Type | Description | Gesture | 
| ----- | ---- | ----------- | ------- |
|lblNumber|Label|Dynamic number displaying the amount of reachable people from user current position||
|txtfieldInput|Text Field|User enters message to be sent to other reachable users||
|btnBack|Button|Navigation Bar: Brings user back to Home View|→ Home View|
|btnRefresh|Button|Navigation Bar: Refresh the Chat View|→ Chat View|
|tableChat|Table|Displays the messages sent and received by application users. <p><p>Username Column: Colour is randomly assigned from web safe colour collection. Randomization is local to the user application. </p></p> <p>Message Column: Display message sent by users. Message gets text wrapped if length exceeds one line</p>||


### 3.4.4 Settings View



| Field | Type | Description | Gesture | 
| ----- | ---- | ----------- | ------- |
|btnBack|Button|Navigation Bar: Brings user back to Home View|→ Home View|
|btnNotif|Button|Brings user to Notification View <p><p>Within a table with two columns: image and label</p></p> |→ Notification View|
|btnReport|Button|Brings user to Report View <p><p>Within a table with two columns: image and label</p></p> |→ Report View|
|btnAbout|Button|Brings user to About View <p><p>Within a table with two columns: image and label</p></p> |→ About View|

### 3.4.5 Notification View 


| Field | Type | Description | Gesture | 
| ----- | ---- | ----------- | ------- |
|btnBack|Button|Navigation Bar: Brings user back to Settings View|→ Setting View|
|toggleShow|Toggle Button|Turns on/off application notification alerts <p><p>Within a table with two columns: label and toggle button</p></p> ||
|toggleSound|Toggle Button|Turns on/off application notification sound alerts <p><p>Within a table with two columns: label and toggle button</p></p> ||
|toggleVibrate|Toggle Button|Turns on/off application notification vibrate alerts <p><p>Within a table with two columns: label and toggle button</p></p> ||
|btnReset|Button|Resets options to default settings||

### 3.4.6 Report View 



| Field | Type | Description | Gesture | 
| ----- | ---- | ----------- | ------- |
|btnBack|Button|Navigation Bar: Brings user back to Settings View|→ Setting View|
|btnSend|Button|Sends user report to the developer’s team email. Internet connection is required. If there is no access to the internet, a pop-up alert will tell user to turn on their WiFi connection. | |
|lblDescribe|Label|Instructs user how to send the report.| |
|txtfieldReport|Text Field|User inputs the message they want to send to the developer team. <p><p>If report is successfully received, text field will be cleared of the messaged typed.</p></p>|

### 3.4.7 About View 


| Field | Type | Description | Gesture | 
| ----- | ---- | ----------- | ------- |
|btnBack|Button|Navigation Bar: Brings user back to Settings View|→ Setting View|
|btnTOS|Button|Brings user to terms of service and privacy policy documents. <p><p>Within a table: label and arrow button</p></p>|→ Terms of Service and Privacy Policy documents|
|btnSources|Button|Brings user to Sources View with that credits all the third-party sources that were used to create the application <p><p>Within a table: label and arrow button</p></p>|→ Sources View|
|btnTeam|Button|Brings user to Team View with details about the developer team <p><p>Within a table: label and arrow button</p></p>|→ Team View|

# 4. Technical Process
## 4.1 Methods, Tools and Techniques

Backend: Bluetooth 5.0 Low Energy (BLE) Mesh<br/>
Languages: Swift, Java, C<br/>
Repositories: GitHub<br/>
Project Management: GitHub, Slack<br/>

## 4.2 Software Documentation
Requirements<br/>
Analysis<br/>
Design


