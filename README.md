# RemoteAssistanceAR

This project is developed in the context of the course INF6802 I followed at Polytechnique Montréal, as part of my PhD degree.

This PhD project aims at exploring how to assist people having cognitive deficiencies during their daily activities by means of augmented reality.
For this scenario, a person is looking for an object at home. She forgot where it is. She puts her augmented reality headset (Hololens 1 in our case), and calls a caregiver. The caregiver receives the video stream from the Hololens and can add virtual annotations to the physical environment of the person. Those annotations are the following:
- Forbidden sign
- Target sign
- Sending a text message
- Showing a guidance arrow
The first 2 annotations are dependant of the depth. In other word, the caregiver clicks on the video stream, and the annotation is displayed on the first physical item found in the 3D environment of the person wearing the Hololens. This is done thanks to a raycast.
The 2 last annotations are independant of the depth. The text is shown for 10 seconds before being removed.

The video stream is grabbed thanks to the LowLatencyMRC module from Microsoft: https://github.com/Microsoft/MixedRealityCompanionKit/tree/master/MixedRemoteViewCompositor/Samples/LowLatencyMRC

This solution comes with 2 applications:
- A Windows app (based on the LowLatencyMRC module from Microsoft, but most of the code has been rewritten to add new functionalities), that compiles with Visual Studio 2015, in x86.
- A Unity app that is targeted to be deployed on the Hololens 1. It used several features of the HoloToolkit (https://github.com/Microsoft/MixedRealityToolkit-Unity/releases, version 2017.4.3).
