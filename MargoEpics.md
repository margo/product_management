# Margo Epics

This document is a temporary place to hold Parent and Child level epics while the Product Management team comes to consensus on the general structure of our epic backlog and the tooling we will use to store and manage it.

The "Lifeclcye Workflow of a Margo system" describes the major activities for interacting with a Margo based system. Each step represents a Parent epic. Those parent epics are expected to live for many Margo releases.

Under each Parent epic will be Child epics. The Child epics will be targeted for a specific Margo release.

**Notes from 25 March 2025**
- I included steps and Parent epics around device fleet managment, but I think we will need to discuss what scope of device fleet managment we expect to have in PR1, and subsequent releases.
- I added some Child epics to a few of the Parent epics as examples. Take a look specifically at "Build a Margo compatible application"...
	- In it I have the scope of PR1 being just Kubernetes and Docker based applications, and add in support for other open runtimes and vendor specific runtimes in GA1 (which I assume will be the release after PR1)
	- I discussed these epics with Armand, and he thinks they are at the right level for his purposes.
	- We of course can, and should, discuss if this is the scope we want for PR1 vs GA1. We could probably speed up PR1 if we choose just Kubernetes or Docker. 

<!---
***
## Grandparent Epic
As an end user, I want to be able to use a fleet manager to deploy, manage, and monitor apps on my edge devices. Those apps may come from one to many applications vendors, and the edge devices may come from one to many device vendors. 
***
--->
## Lifecycle Workflow of a Margo system
1. **Workload fleet manager** owner deploys a Margo compatible workload fleet manager
2. **Device fleet manager** owner deploys a Margo compatible device fleet manager
3. **App vendor** builds a Margo compatible application
4. **App vendor** registers app repository and app with the workload fleet manager
5. **Edge device vendor** builds a Margo compatible edge device
6. **End user** enrolls an edge device with a workload fleet manager
7. **End user** enrolls an edge device with a device fleet manager
8. **End user** deploys an application
9. **End user** monitors the execution of an application
10. **End user** monitors the state of an edge device
11. **App vendor** manages the apps in a repository
12. **End user** manages enrolled edge devices
13. **End user** manages deployed applications

## Parent Epic 1: Deploy a Margo compatible workload fleet manager

As a **workload fleet manager owner**, I want to deploy my fleet manager to make it available for secure interactions with edge devices and app vendor repositories for the management of workloads.
<details>
	<summary>Child Epics</summary>

### Child Epic 1.1

As a workload fleet manager owner, I want the Margo spec to define...

- The APIs a workload fleet manager must support to be Margo compliant
- The mechanism for establishing trust with edge devices
- The mechanism for establishing trust with app vendor repositories

Release Target: PR1

</details>

## Parent Epic 2: Deploy a Margo compatible device fleet manager

As a **device fleet manager owner**, I want to deploy my device fleet manager to make it available for secure interactions with edge devices for management of those edge devices.
<details>
	<summary>Child Epics</summary>

### Child Epic 2.1

As a workload fleet manager owner, I want the Margo spec to define...

- The APIs a device fleet manager must support to be Margo compliant
- The mechanism for establishing trust with edge devices
- The mechanism for establishing trust with app vendor repositories

Release Target: GA1

</details>


## Parent Epic 3: Build a Margo compatible application
As an **app vendor**, I want to create an application that is deployable by a Margo compatible workload fleet manager.
<details>
	<summary>Child Epics</summary>

### Child Epic 3.1

As an app vendor, I want the Margo spec to define how to make a Margo compatible application. Specifically, I want the Margo spec to...
- Define the metadata, and format for that metadata, that is used to describe an application
- Define how the deployment specific configuration parameters for an application are described
- Describe the format for defining the edge device requirements of an application
	- The definition should include common standard attributes (e.g. CPU architecture, storage capacity), and also permit for vendor specific attributes.
- Allow an app to be deployed to a Kubernetes based end device, a Docker based end device, or both.

Release Target: PR1

### Child Epic 3.2

As an app vendor, in addition to Kubernetes and Docker, I want the Margo spec to allow me to create an application that requires an alternative open runtime environment or vendor specific runtime environment.

Release Target: GA1

</details>

## Parent Epic 4: Register an app vendor repository and apps with the workload fleet manager
As an **app vendor**, I want to register my app repository and its apps with a Margo compatible workload fleet manager so that the end users of that workload fleet manager can deploy my app to their compatible edge devices.

Precondition: the workload fleet manager has been deployed and I have the necessary authorization to reigster my repository with the workload fleet manager.
<details>
	<summary>Child Epics</summary>

### Child Epic 4.1: Register an app vendor repository with with the workload fleet manager, PR1 Spec
As an app vendor I want the Margo spec to define the mechanism used for an app repository to interact with a workload fleet manager, and the process to register an app repository and its apps with a workload fleet manager.

Release Target: PR1
</details>


## Parent Epic 5: Build a Margo compatible edge device
As an **edge device vendor**, I want to build an edge device that can be enrolled with Margo compatible workload fleet managers and have device compatible apps deployed to it.

<details>
	<summary>Child Epics</summary>
</details>


## Parent Epic 6: Enroll an edge device with a workload fleet manager
As an **end user**, I want to enroll a Margo compatible edge device with a Margo compatible workload fleet manager so that apps that are compatible with the edge devices can be deployed to it. 

Precondition: Edge device has been obtained from an edge device vendor. Workload fleet manager has been deployed and I have the necessary authorization from the workload fleet manager to enroll edge devices with it.

<details>
	<summary>Child Epics</summary>
</details>

## Parent Epic 7: Enroll an edge device with a device fleet manager
As an **end user**, I want to enroll a Margo compatible edge device with a Margo compatible device fleet manager so that I can monitor and manage the device. 

Precondition: Edge device has been obtained from an edge device vendor. Device fleet manager has been deployed and I have the necessary authorization from the device fleet manager to enroll edge devices with it.

<details>
	<summary>Child Epics</summary>
</details>

## Parent Epic 8: Deploy an application
As an **end user**, I want to deploy a Margo compatible application to a Margo and application compatible edge device.

Precondition: The application I want to deploy is in a app repository that is registered with the workload fleet manager. The target edge device is enrolled with the workload fleet manager. 

<details>
	<summary>Child Epics</summary>
</details>

## Parent Epic 9: Monitor the execution of the application
As an **end user**, I want to monitor the execution of an application that has been deployed to my edge device.

Precondition: The application has been deployed to the edge device.

<details>
	<summary>Child Epics</summary>
</details>

## Parent Epic 10: Monitor the state of an edge device
As an **end user**, I want to monitor the state of my edge device.

Precondition: The edge device is enrolled with the workload fleet manager.

<details>
	<summary>Child Epics</summary>
</details>

## Parent Epic 11: Manage apps in a repository
As an **app vendor**, I want to manage the apps in my repository, e.g. update an existing app to a new version or delete an existing application.

<details>
	<summary>Child Epics</summary>
</details>

## Parent Epic 12: Manage enrolled edge devices
As an **end user**, I want to manage my enrolled devices, e.g. update details about previously enrolled devices, or unenroll previously enrolled devices.

<details>
	<summary>Child Epics</summary>
</details>

## Parent Epic 13: Manage deployed applications
As an **end user**, I want to manage the applications I have deployed to my end devices, e.g. change configuration, update to a newer version, or delete.

<details>
	<summary>Child Epics</summary>
</details>
