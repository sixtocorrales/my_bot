# Overview
Welcome to the Orbbec SDK (hereinafter referred to as "SDK") tutorial! The SDK not only provides a concise high-level API, but also a flexible and comprehensive low-level API to help you use and quickly understand Orbbec 3D cameras in detail. 

# Features
Orbbec SDK is a cross-platform (Windows, Android, Linux) software development kit that provides device parameter configuration, data stream reading and stream processing for 3D sensing cameras such as Orbbec structured light, binocular, and iToF.

**Core functions: **

- Depth camera access and related parameter settings 
- RGB camera access and related parameter settings (eg exposure and white balance) 
- Sensor access and related parameter settings (eg gyroscope and accelerometer) 
- Frame synchronization and alignment control 
- Point cloud data 
- Algorithmic capabilities such as filtering 
- Multi-OS and Wrapper support. 

**Highlights:**

SDK design goals: thin + flexible + high scalability. 

- "Thin": Provides the ability to obtain device data at the minimum level and high performance 
- "Flexible": Modular sensor function, flexible combination of different devices 
- "Highly Scalable": Supports increasingly diversified devices and systems, and plug-in algorithms for different scenarios 

What's included in the SDK:

| Content | Description                                                  |
| --- | --- |
| Code example | These simple examples demonstrate how to easily use the SDK to include code snippets that access the camera into your application. Includes color flow, depth flow, point cloud, alignment, recording, and more.  |
| tool | OrbbecViewer: A tool that demonstrates the main basic functions and parameter configuration of the 3D sensing camera using the SDK to help developers quickly understand and verify the capabilities of the SDK and the 3D sensing camera. With this application, you can quickly access your depth camera to view the depth stream, visualize point clouds, record and playback data streams, configure your camera settings.  |

# Hardware products supported by the SDK




| SDK version | Product | Firmware version |
| --- | --- | --- |
| v1.7.4	  | Gemini 2 XL     | Obox: V1.2.5  VL:1.4.54 |
|       	  | Astra 2         | 2.8.20                    |
| 		      | Gemini 2 L      | 1.4.32                     |
| 		      | Gemini 2        | 1.4.60 /1.4.76                    |
|             | Femto Mega      | 1.1.7  (window10、ubuntu20.04、ubuntu22.04)                     |
|             | Astra+         | 1.0.22/1.0.21/1.0.20/1.0.19 |
|             | Femto          | 1.6.7                       |
|             | Femto W       | 1.1.8          |
|             | DaBai          | 2436                        |
|             | DaBai DCW      | 2460                        |
|             | DaBai DW       | 2606                        |
|             | Astra Mini Pro | 1007                        |
|             | Gemini E       | 3460                        |
|             | Gemini E Lite  | 3606                  |
|             | Gemini         | 3.0.18                      |
|             | Astra Mini S Pro | 1.0.05                      |
| v1.6.3	  | Astra2         | 2.8.20                     |
| 		      | Gemini2 L      | 1.4.32                     |
|             | Gemini2        | 1.4.60/1.4.76                     |
|             | FemtoMega      | 1.1.7  (windows10、linux (PC) ubuntu20.04、ubuntu22.04)                     |
|             | Astra+         | 1.0.22/1.0.21/1.0.20/1.0.19 |
|             | Femto          | 1.6.7                       |
|             | Femto W       | 1.1.8    					 |
|             | Dabai          | 2436                        |
|             | Dabai DCW      | 2460                        |
|             | Dabai DW       | 2606                        |
|             | Astra Mini     | 2418                        |
|             | Astra Mini Pro | 1007                        |
|             | Astra Pro Plus | 2513                        |
|             | A1 Pro         | 3057                        |
|             | Gemini E       | 3460                        |
|             | Gemini E Lite  | 3606              			 |
|             | Gemini         | 3.0.18                      |
|             | Deeyea         | 3012/3015                   |
| v1.5.7      | Gemini2        | 1.4.60                     |
|             | FemtoMega      | 1.1.5 (windows10、ubuntu20.04、ubuntu22.04)                      |
|             | Astra+         | 1.0.22/1.0.21/1.0.20/1.0.19 |
|             | Femto          | 1.6.7                       |
|             | Femto W       | 1.1.8    					 |
|             | Dabai          | 2436                        |
|             | Dabai DCW      | 2460                        |
|             | Dabai DW       | 2606                        |
|             | Astra Mini     | 2418                        |
|             | Astra Mini Pro | 1007                        |
|             | Astra Pro Plus | 2513                        |
|             | A1 Pro         | 3057                        |
|             | Gemini E       | 3460                        |
|             | Gemini E Lite  | 3606              			 |
|             | Gemini         | 3.0.18                      |
|             | Deeyea         | 3012/3015                   |

# SDK system requirements
| Operating system | Requirement                                                  | Description |
| --- | --- | --- |
| Windows | - Windows 10 April 2018 (version 1803, operating system build 17134) release (x64) or higher<br />- 4 GB RAM<br />- USB2.0 and above ports<br /> | The generation of the VS project depends on the installation of the VS version and the cmake version, and supports VS2015/vs2017/vs2019 |
| Android | - Android 6/7/8/9/10 |  |
| Linux | - Linux Ubuntu 16.04/18.04/20.04/22.04 (x64)<br />- support ARM/ARM64<br />-4 GB RAM<br />- USB2.0 and above ports<br /> |Support GCC 7.5|
| Arm32 | <br />- Linux Ubuntu 16.04/18.04/20.04/22.04<br />- 4 GB RAM<br />- USB2.0 and above ports<br /> |  Support GCC 7.5 |
| Arm64 | <br />- Linux Ubuntu 18.04/20.04/22.04<br />- 4 GB RAM<br />- USB2.0 and above ports<br /> |  Support GCC 7.5 |
| *MacOS | <br />- M series chip, 11.0 and above os systems. <br />- 4 GB RAM<br />- USB3.0 <br /> | Beta version, supported hardware products: Gemini2, Gemini2 L, Astra2 |

* Note: supported Arm platforms: jestson nano (arm64), A311D (arm64), Raspberry Pi 4 (arm64), Raspberry Pi 3 (arm32), rk3399 (arm64), other Arm systems, may need to Cross-compile.

# Supported Languages & Wrapper


![1](.\OrbbecSDK_Overview_Document_img\1.png)





# SDK Architecture
![2](.\OrbbecSDK_Overview_Document_img\2.png)

**Low-level API/High-level API/Wrappers**

The API layer encapsulates core business components and provides APIs for different wrappers.

**Basic business layer**

The realization of the core business logic framework realizes the functions of Low Level and High Level.

**Platform abstraction layer**

Cross-platform components shield the implementation of different operating systems and provide a unified access method. 

**Platform implementation layer**

The driver implementation of each platform.
