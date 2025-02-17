---
title: Baseline and custom checks
description: Learn about the concept of Microsoft Defender for IoT baseline.
ms.topic: conceptual
ms.date: 03/28/2022
---

# Microsoft Defender for IoT baseline and custom checks

> [!NOTE]
> The Microsoft Defender for IoT legacy agent has been replaced by our new micro-agent experience, and will not be supported after **March 31, 2023**. For more information, see [Create custom alerts](quickstart-create-custom-alerts.md) and [Defender for IoT Hub custom security alerts](concept-customizable-security-alerts.md).
>


This article explains Defender for IoT baseline, and summarizes all associated properties of baseline custom checks.

## Baseline

A baseline establishes standard behavior for each device and makes it easier to establish unusual behavior or deviation from expected norms.

## Baseline custom checks

Baseline custom checks establish a custom list of checks for each device baseline using the **Module identity twin** of the device.

## Setting baseline properties

1. In your IoT Hub, locate and select the device you wish to change.

1. Click on the device, and then click the **azureiotsecurity** module.

1. Click **Module Identity Twin**.

1. Upload the **baseline custom checks** file to the device.

1. Add baseline properties to the Defender-IoT-micro-agent and click **Save**.

### Baseline custom check file example

To configure baseline custom checks:

   ```json
    "desired": {
      "ms_iotn:urn_azureiot_Security_SecurityAgentConfiguration": {
        "baselineCustomChecksEnabled": {
          "value" : true
        },
        "baselineCustomChecksFilePath": {
          "value" : "/home/user/full_path.xml"
        },
        "baselineCustomChecksFileHash": {
          "value" : "#hashexample!"
        }
      }
    },
   ```

## Baseline custom check properties

| Name| Status | Valid values| Default values| Description |
|------|-----|------|-----|-----|
|baselineCustomChecksEnabled|Required: true |Valid values: **Boolean** |Default value: **false** |Max time interval before high priority messages is sent.|
|baselineCustomChecksFilePath |Required: true|Valid values: **String**, **null** |Default value: **null** |Full path of the baseline xml configuration|
|baselineCustomChecksFileHash |Required: true|Valid values: **String**, **null** |Default value: **null** |`sha256sum` of the xml configuration file. Use the [sha256sum reference](https://linux.die.net/man/1/sha256sum) for additional information. |

To review additional baseline examples, see [custom baseline example -1](https://ascforiot.blob.core.windows.net/public/custom_baseline_example_hyperv_ubuntu1804.xml) and [custom baseline example -2](https://ascforiot.blob.core.windows.net/public/oms_audits.xml).

## Next steps

- Access your [raw security data](how-to-security-data-access.md)
- [Investigate a device](how-to-investigate-device.md)
- Understand and explore [security recommendations](concept-recommendations.md)
- Understand and explore [security alerts](concept-security-alerts.md)
