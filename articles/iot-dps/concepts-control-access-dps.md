---
title:  Access control and security for Azure IoT Hub Device Provisioning Service | Microsoft Docs
description: Overview on how to control access to Azure IoT Hub Device Provisioning Service (DPS), includes links to in-depth articles on Azure Active Directory integration (Public Preview) and SAS options.
author: jesusbar
ms.author: jesusbar
ms.service: iot-dps
ms.topic: conceptual
ms.date: 04/20/2022
ms.custom: ['Role: Cloud Development', 'Role: Azure IoT Hub Device Provisioning Service (DPS)', 'Role: Operations', devx-track-js, devx-track-csharp]
---

# Control access to Azure IoT Hub Device Provisioning Service (DPS)

This article describes the available options for securing your Azure IoT Hub Device Provisioning Service (DPS). The provisioning service uses *authentication* and *permissions* to grant access to each endpoint. Permissions allow the authentication process to limit access to a service instance based on functionality.

There are two different ways for controlling access to Azure IoT Hub DPS:

- **Shared access signatures** lets you group permissions and grant them to applications using access keys and signed security tokens. To learn more, see [Control access to Azure IoT Hub DPS with Shared Access Signatures and security tokens](how-to-control-access.md). 
- **Azure Active Directory (Azure AD) integration (Public Preview)** for service APIs. Azure provides identity-based authentication with Azure Active Directory and fine-grained authorization with Azure role-based access control (Azure RBAC). Azure AD and RBAC integration is supported for Azure IoT Hub DPS service APIs only. To learn more, see [Control access to Azure IoT Hub DPS with Azure Active Directory (Public Preview)](concepts-control-access-dps-azure-ad.md).



## Next steps

- [Control access to Azure IoT Hub DPS with Shared Access Signatures and security tokens](how-to-control-access.md)
- [Control access to Azure IoT Hub DPS with Azure Active Directory (Public Preview)](concepts-control-access-dps-azure-ad.md)
