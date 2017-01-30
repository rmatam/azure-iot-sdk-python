# Samples for the Azure IoT device SDK for Python

This folder contains simple samples showing how to use the various features of the Microsoft Azure IoT Hub service from a device running Python.

## List of samples

* [Simple Sample](iothub_client_sample.py): shows how to connect to IoT Hub and send and receive messages using the AMQP, MQTT or HTTP protocol.
* [Class Sample using AMQP](iothub_client_sample_class.py): shows how to connect to IoT Hub with a HubManager class to send and receive messages using the AMQP protocol.
* [Simple Sample X-509](iothub_client_sample_x509.py):  shows how to authenticate a device using X-509 certs and send and receive messages.

And if you are looking for end to end samples that show how to do simple analytics and processing of the data generated by your device using Azure services such as Stream Analytics, Big Data, Machine Learning and others, check out our [E2E samples gallery](http://aka.ms/azureiotsamples).

## How to run the samples
In order to run the device samples you will first need the following prerequisites:
* [Setup your development environment][devbox-setup]
> Note: On Windows, it is recommended to install the **iothub-client** module package using pip (see link above).
* [Create an Azure IoT Hub instance][lnk-setup-iot-hub]
* [Create a device identity for your device][lnk-manage-iot-hub] and retreive the primary connection string for this device

Once you have a device identity for your sample,
* Get the sample files:
   * if you have cloned the repository, Navigate to the folder **device/samples**
   * if you are using the iothub_client module installed with pip, download the samples folder content to your target.
* Run the sample application using the following command to run the simple sample (replacing `<device connection string>` with the one generated previously):
    ```
	python iothub_client_sample.py -c < device connection string > -p < mqtt|http|amqp >
    ```
> You can get details on the options for the sample command line typing:
> `python iothub_client_sample.py -h`
* To run the other samples (x-509 and class), replace the name of the .py file in the command line and use the `-h` option to get the details on the available options

[lnk-setup-iot-hub]: https://aka.ms/howtocreateazureiothub
[lnk-manage-iot-hub]: https://aka.ms/manageiothub
[devbox-setup]: ../../doc/python-devbox-setup.md