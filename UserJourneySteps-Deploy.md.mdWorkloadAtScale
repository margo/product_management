# Step-by-step scenario
**Persona**: Julia, plant operations manager @  CheeseNaanz Ltd.

Description :
CheeseNaanz, locally recognized for their delicious cheese naans, decided to go global.
They are convinced that digitalization, will help them to maintain their high-quality standards while scaling up their manufacturing capacity with new plants in other regions of the world.. 
Julia has identified two apps, The SoftSense and SmartCam workloads, performing real-time quality inspection and providing closed loop feedback to the baking control algorithm. These workloads require to be hosted close to the baking line. For this harsh environment, CheeseNaanz has selected edge devices from supplier ToughEdge AG.  Julia will first test and validate the concept at their headquarters and subsequently deploy and maintain these apps at scale in the production facilities, using MyFleet@FingerTips software, their common fleet management software.
Below step-by-step description represents the user journey articulated in this video: https://drive.google.com/file/d/11UzWpRg0zXi-tXHN2KslnTfM-2YRwU-n/view?usp=drive_link

Step-by-step:
1.	Julia wants to deploy the SmartCam and Softsense workloads to the ToughEdge device “EDV-73” in her plant, using her Workload fleetmanager software, MyFleet@FingerTips
2.	The Workload fleet manager onboards & registers the ToughEdge device, and discovers its device capabilities. A trust relationship is established between these entities. If desired, the Workload fleet manager can double check (verify) the authenticity with the YoughEdge device manufacturer. 
3.	The Workload fleet manager registers the SmartCam and Softsense workloads  and discovers its workload requirements. It identifies the repositories of its vendors and establishes a trust relationship with these entities. It is assumed that every vendor has a public & secured endpoint/repository. Workload fleet managers and users may decide to replicate repos in different locations.
4.	The Workload fleet manager uses private processes to verify the match between the SmartCam and Softsense workloads and the TougEdge device. this is done on Julia’s request. Remark: this matching process is out of scope for Margo. Margo only enables this matching process to happen, with the provided information and established trust. As needed, the workload fleet manager collects observability information from the device, to have the latest, up-to-date device status, valuable for the matching exercise.
5.	The match is found and confirmed. The Workload Fleet manager generates the Deployment manifest for the targeted edge device.
6.	The Edge device discovers the new state and pulls the deployment manifest.
7.	The ToughEdge device starts deploying the SmartCam and Softsense workloads by pulling the required artifacts and configuration information from the repos indicated in the deployment manifest. These repos can be hosted in multiple locations. 
8.	The ToughEdge device informs the Workload fleet manager about the outcome of the deployment task. We assume it is successful. The workload fleet manager collects the new observability information associated with the new state of the device. 
9.	Julia sees that the SmartCam and Softsense workloads to the ToughEdge device “EDV-73” and requests the Workload fleet manager to repeat the process for the remainder of their process plants
