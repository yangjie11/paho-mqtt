# paho-mqtt

[Chinese](README_ZH.md) | English

## 1 Introduction

- [Paho MQTT](http://www.eclipse.org/paho/downloads.php) is a client based on MQTT protocol implemented by Eclipse. This package is in Eclipse [paho-mqtt](https://github.com/eclipse/paho.mqtt.embedded-c) A set of MQTT client programs designed based on the source code package.

- For the features of the `paho-mqtt` software package and the introduction of the MQTT protocol, please refer to [Package Details](docs/introduction.md).

### 1.1 Directory structure

The directory structure of the `paho-mqtt` package is as follows:

```
pahomqtt
├───docs
│ └───figures            // Documents use pictures
│ │ api.md               // API instructions
│ │ introduction.md      // Introduction document
│ │ principle.md         // Implementation principle
│ │ README.md            // Document structure description
│ │ samples.md           // package sample
│ │ user-guide.md        // Instructions
│ └───version.md         // version
├───MQTTClient-RT        // transplant file
├───MQTTPacket           // source file
├───samples              // sample code
│ mqtt_sample.c          // Software package application sample code
├───tests                // mqtt function test program
│ LICENSE                // package license
│ README.md              // Software package instructions
└───SConscript           // RT-Thread default build script
```

### 1.2 License

The `paho-mqtt` package is licensed under the Eclipse Public License-v 1.0, see the `LICENSE` file for details.

### 1.3 Dependency

- RT-Thread 3.0+

## 2. Get the software package

To use the `paho-mqtt` software package, you need to use the menuconfig command in the BSP directory to open the Env configuration interface, and select the Paho MQTT software package in the `RT-Thread online packages → IoT-internet of things`, the operation interface is as shown in the figure below:

![Select Paho MQTT package](docs/figures/select_mqtt_package.png)

After selecting the appropriate configuration items, use the `pkgs --update` command to download the software package and add it to the project.

## 3. Use paho-mqtt

* For how to use it from scratch, please refer to [User Manual](docs/user-guide.md).
* For complete API documentation, please refer to [API Manual](docs/api.md).
* For detailed sample introduction, please refer to [Sample Document](docs/samples.md).
* For the working principle of MQTT protocol, please refer to [Working Principle](docs/principle.md).
* More **Detailed introduction documents** are located in the [`/docs`](/docs) folder, **Please check before using the package for development**.

## 4. Matters needing attention

- Fill in the account password of the proxy server correctly

    If the account password is incorrect, the MQTT client will not be able to connect to the MQTT server correctly.

- Reasonably configure the MQTT thread stack

    If you use MQTT TLS to encrypt the connection, the MQTT thread stack needs at least 6144 bytes.

## 5. Contact & Thanks

* Maintenance: RT-Thread development team
* Homepage: https://github.com/RT-Thread-packages/paho-mqtt
