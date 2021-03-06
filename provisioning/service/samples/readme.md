# Samples for the Azure IoT Device Provisioning Service SDK for Node.js

This file can be found in http://github.com/azure/azure-iot-sdk-node/provisioning/service/samples

This folder contains simple samples showing how to use the various features of the Microsoft Azure IoT Device Provisioning Service from an application running JavaScript code.

## List of samples

* Create a simple IndividualEnrollment object.
   *  [create_individual_enrollment.js][create-individual-enrollment]
* Create a simple EnrollmentGroup object.
   *  [create_enrollment_group.js][create-enrollment-group]
* Create a couple of IndividualEnrollments and delete them.
   *  [create_delete.js][create-delete]
* Create queries for IndividualEnrollments, EnrollmentGroups and DeviceRegistrationStates that belong to an EnrollmentGroup.
   *  [query.js][query-link]
* Perform BulkEnrollmentOperations to do various CRUD operations.
   *  [run_bulk_operation.js][run-bulk-operation]


## How to run the samples

In order to run the device samples you will first need the following prerequisites:
* Node.js v4 or above on your target device. (Check out [Nodejs.org](https://nodejs.org/) for more info)
* [Setup Azure IoT Device Provisioning ][lnk-setup-iot-provisioning] Stop before executing the the Create and provision a simulated device section.  The samples below will perform these steps.

<<<<<<<<<<<<<<<<<<link to how to obtain an endorsment key!!!!>>>>>>>>>>>>>>>>>>

Get the following files from the current folder:
* [package.json][package-json]
* **__sample_file.js__** (where **__sample_file.js__** is one of the files listed above and available in this folder)

Place the files in the folder of your choice on the target machine/device then go through the following steps:

* From a shell or Node.js command prompt, navigate to the folder where you placed the sample files. For creating an IndividualEnrollment do:

```
$ npm install
$ node create_individual_enrollment.js "<the connection string for the Device Provisioning instance enclosed in quotes>" "<an endorsement key in quotes>"
```


* For creating an EnrollmentGroup do:
<<<<<<<<<<<<<<<<<<<<<<<<<<<<<Link to how to create a signing certificate>>>>>>>>>>>>>>>>>>>>>>>>>>>>>


```
$ npm install
$ node create_enrollment_group.js "<the connection string for the Device Provisioning instance enclosed in quotes>" "<The name of a file containing a pem or cer representation of a signing certificate>"
```

* The other samples simply require the connection string:

```
$ npm install
$ node create_delete.js "<the connection string for the Device Provisioning instance enclosed in quotes>"
```

* In order to monitor the results of running the sample, use the portal for the Device Provisioning Service which can display group or individual enrollments.


## Read More
For more information on how to use this library refer to the documents below:
- [Prepare your node.js development environment][node-devbox-setup]
- [Setup IoT Hub][lnk-setup-iot-hub]
- [Provision devices][lnk-manage-iot-hub]
- [Node API reference][node-api-reference]

[lnk-setup-iot-provisioning]: https://docs.microsoft.com/en-us/azure/iot-dps/quick-setup-auto-provision
[lnk-setup-iot-hub]: https://aka.ms/howtocreateazureiothub
[lnk-manage-iot-hub]: https://aka.ms/manageiothub
[node-api-reference]: https://docs.microsoft.com/en-us/javascript/api/azure-iot-device/
[node-devbox-setup]: ../../doc/node-devbox-setup.md
[create-individual-enrollment]: [https://github.com/azure/azure-iot-sdk-node/tree/master/provisioning/service/samples/create_individual_enrollment.js]
[create-enrollment-group]: [https://github.com/azure/azure-iot-sdk-node/tree/master/provisioning/service/samples/create_enrollment_group.js]
[create-delete]: [https://github.com/azure/azure-iot-sdk-node/tree/master/provisioning/service/samples/create_delete.js]
[query-link]: [https://github.com/azure/azure-iot-sdk-node/tree/master/provisioning/service/samples/query.js]
[run-bulk-operation]: [https://github.com/azure/azure-iot-sdk-node/tree/master/provisioning/service/samples/query.js]
[package-json]: [https://github.com/azure/azure-iot-sdk-node/tree/master/provisioning/service/samples/package.json]
