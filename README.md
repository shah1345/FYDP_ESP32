## Custom ESP32 Device Features

Our custom ESP32 Computerddresses specific limitations present in standard ESP32 development boards commonly available in the market. Here's a breakdown of its enhancements:

1. **Increased Memory:** The custom device boasts enhanced memory specifications with 128MB ROM and 64MB RAM, providing substantial improvements over standard development boards. This augmentation ensures smoother operations and accommodates resource-intensive applications, a crucial factor for our targeted use case.

2. **Optimization for Low Power Consumption:** Through meticulous optimization efforts in both software and hardware, our device significantly reduces power consumption without compromising performance. In extensive tests, it successfully operated using a tiny 200mAh battery, sustaining functionality for approximately 3 hours. This translates to an impressive 31-day runtime for a single unit, emphasizing its efficiency and suitability for long-term deployments.

3. **Extended Network Range:** Unlike typical ESP32 development boards with a Wi-Fi range of 50-70 meters, our custom device offers an expanded coverage area of up to 300 meters. This augmented range, supported by both internal and external antenna options, enhances connectivity and usability across larger spaces or challenging environments.

4. **Industry 4.0 Compatibility:** To cater to industrial requirements, our device features an RS485 communication port. This addition facilitates seamless communication with machinery and equipment commonly found in Industry 4.0 setups, enhancing interoperability and integration capabilities.


##Why We use Web Server in FL

# Using a Web Server in Federated Learning

Federated Learning (FL) is a machine learning approach where models are trained across multiple decentralized devices or servers holding local data samples, without exchanging their data. Using a web server in FL provides several benefits:

## Centralized Coordination and Management

- **Model Aggregation**: In FL, models are trained locally on devices, and the updates are sent to a central server. The web server aggregates these updates to form a global model.

## Monitoring and Logging

- **Device Activity Monitoring**: The web server monitors the status and activity of all participating devices.
- **Performance Logging**: Logs performance metrics such as training time, accuracy, and loss.

## Scalability and Load Management

- **Handling Multiple Devices**: Efficiently manages communication between multiple devices, ensuring model updates are received and aggregated.
- **Resource Allocation**: Distributes computational resources effectively.

## Security and Privacy

- **Secure Communication**: Facilitates secure communication channels between devices and the central server.
- **Access Control**: Enforces access control policies to ensure only authorized devices participate.

## Data Aggregation and Analysis

- **Aggregating Logs and Metrics**: Collects logs and performance metrics from all devices for comprehensive analysis.
- **Centralized Data Repository**: Acts as a central repository for logs and metrics.

## User Interface and Visualization

- **Dashboard for Visualization**: Hosts a dashboard that provides a graphical user interface for visualizing the status and performance of the FL process.
- **Alerts and Notifications**: Sends alerts and notifications in case of anomalies or significant events.

## Example Code

Here is an example of how you might set up a simple web server for monitoring federated learning processes using Python and Flask:

```python
from flask import Flask, request, jsonify

app = Flask(__name__)

# Store logs in a simple dictionary
logs = {}

@app.route('/log', methods=['POST'])
def log_activity():
    data = request.get_json()
    device_id = data['device_id']
    logs[device_id] = data
    return jsonify({'status': 'success'})

@app.route('/logs', methods=['GET'])
def get_logs():
    return jsonify(logs)

if __name__ == '__main__':
    app.run(host='0.0.0.0', port=5000)




## Comparison Table

| Features                      | Custom Development Board | Common Development Board  |
|-------------------------------|---------------------|--------------------------------|
| ROM                           | 128 mb               | 16mb                          |
| RAM                           | 64 mb                | 4 mb                          |
| Power Consumption Efficiency  | Ultra-low power consumption | Standard               |
| Battery Life (200mAh)         | Approx. 4 Hours     | 20 min                         |
| Battery Life (1 Unit)         | Up to 31 Days       | Varies                         |
| Wi-Fi Range                   | Up to 300m          | Typically 50-70m               |
| Security Features             | AES-XTS-based flash encryption, RSA-based secure boot, digital signature and HMAC |Secure boot, Flash encryption|
| Network (2G/ 3G / 4G)         | Yes                 | Not Avilable                   |
| LoRa                          | Yes                 | Not Avilable                   |
| Ethernet                      | Yes (RJ45)          | Typically Not Avilable         |
| Antenna Options               | Internal & External | Typically Internal Only        |
| Industry Compatibility        | RS485 Port Included | Not Commonly Available         |
| Targeted Use Case Efficiency  | Optimized           | Standard                       |
| Target Applications | IoT, Smart Home, Wearables, Industrial, AI and ML applications           | IoT, Smart Home, Wearables, Industrial                       |

This table demonstrates the notable advantages of the custom ESP32 device over market-available ESP32 development boards in terms of memory, power efficiency, battery life, network range, antenna support, industry compatibility, and optimized performance for targeted use cases.



# Device Comparison

This table compares different devices in terms of various attributes:

| Attribute              | TinyPi                   | Raspberry Pi 4          | Computer              |
|------------------------|--------------------------|-------------------------|-----------------------|
| Power Consumption (30 Day's)      | 1 unit                   | 3.7 units               | 93 units              |
| Network Connectivity   | wifi/Ethernet/Celular    | wifi/Ethernet           | wifi/Ethernet         |
| Range   |Long    | 100 m           |  50 m         |
| Industrial COM Port    | Available                | No                      | No                    |
| Customizable           | Yes                      | No                      | No                    |
| Cost                   | 5,000 BDT                  | 15,000   BDT              | 45,000      BDT         |


# Device Information

- **Sketch Size:** 322,800 bytes (24.63% of Max Sketch Space)
- **Max Sketch Space:** 1,310,720 bytes
- **Sketch MD5:** 1073501068
- **SDK Version:** v4.4.5
- **Flash Chip Size:** 16,777,216 bytes
- **Flash Chip Speed:** 80,000,000
- **Flash Chip Mode:** 0
- **Chip ID:** 2175530136 (64-bit)
- **Chip Revision:** 1
- **CPU Frequency:** 240 MHz
- **Cycle Count:** 88,535,872
- **Heap Size:** 333,040 bytes
- **Free Heap:** 307,096 bytes
- **Min Free Heap:** 298,648 bytes
- **Max Allocatable Heap:** 110,580 bytes




# Power Efficiency Comparison

This project focuses on comparing the power efficiency between two devices that require different units of power.

## Overview

Two devices were analyzed:
- Computer: Consumes 93 units of power
- TinyPi: Consumes 1 unit of power

## Power Saving Calculation



Therefore, transitioning from Computer (93 units) to TinyPi (1 unit) results in approximately a 98.92% power-saving percentage. This signifies a significant improvement in power efficiency.

## Conclusion

The newer TinyPi is approximately 99% more power-efficient compared to the Computer, providing substantial power savings for the same task.







## Description

This comparison table outlines key features such as power consumption, network connectivity options, industrial COM port availability, customizability, and cost for TinyPi, Raspberry Pi 4, and a standard computer.

## Additional Information

Please note that the cost values are approximate and subject to change.

Feel free to contribute or update the information to keep it accurate and relevant.






