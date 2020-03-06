---
title: Обзор модуля администрирования PowerShell для Azure Stack | Документация Майкрософт
description: Обзор модуля администрирования PowerShell для Azure Stack с инструкциями по установке и конфигурации.
author: sijuman
ms.author: sijuman
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 02/24/2020
ms.openlocfilehash: ec406c80de6b457f7e340a23fe8caf2ab83be46a
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2020
ms.locfileid: "78264416"
---
# <a name="azure-stack-module-180"></a><span data-ttu-id="43b2c-103">Модуль Azure Stack 1.8.0</span><span class="sxs-lookup"><span data-stu-id="43b2c-103">Azure Stack Module 1.8.0</span></span>

## <a name="requirements"></a><span data-ttu-id="43b2c-104">Требования</span><span class="sxs-lookup"><span data-stu-id="43b2c-104">Requirements:</span></span>

<span data-ttu-id="43b2c-105">Минимальная поддерживаемая версия Azure Stack — 1910.</span><span class="sxs-lookup"><span data-stu-id="43b2c-105">Minimum supported Azure Stack version is 1910.</span></span>

<span data-ttu-id="43b2c-106">Примечание. Сведения о более ранних версиях Azure Stack см. в разделе [Установка PowerShell для Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell).</span><span class="sxs-lookup"><span data-stu-id="43b2c-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install"></a><span data-ttu-id="43b2c-107">Установка</span><span class="sxs-lookup"><span data-stu-id="43b2c-107">Install</span></span>

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2019-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.8.0
```

## <a name="release-notes"></a><span data-ttu-id="43b2c-108">Заметки о выпуске</span><span class="sxs-lookup"><span data-stu-id="43b2c-108">Release Notes</span></span>

* <span data-ttu-id="43b2c-109">Поддерживается в обновлении 1910.</span><span class="sxs-lookup"><span data-stu-id="43b2c-109">Supported with 1910 update</span></span>
* <span data-ttu-id="43b2c-110">Внесенные изменения:</span><span class="sxs-lookup"><span data-stu-id="43b2c-110">Changes include:</span></span>

    - <span data-ttu-id="43b2c-111">**Новый модуль администрирования DRP**. Поставщик ресурсов развертывания (DRP) поддерживает управляемые развертывания поставщиков ресурсов в Azure Stack Hub.</span><span class="sxs-lookup"><span data-stu-id="43b2c-111">**New DRP Admin module**: The Deployment Resource Provider (DRP) enables orchestrated deployments of resource providers to Azure Stack Hub.</span></span> <span data-ttu-id="43b2c-112">Эти команды взаимодействуют со слоем Azure Resource Manager для взаимодействия с DRP.</span><span class="sxs-lookup"><span data-stu-id="43b2c-112">These commands interact with the Azure Resource Manager layer to interact with DRP.</span></span>

    - <span data-ttu-id="43b2c-113">**BRP**:</span><span class="sxs-lookup"><span data-stu-id="43b2c-113">**BRP**:</span></span>
        - <span data-ttu-id="43b2c-114">поддержка восстановления одной роли для резервного копирования инфраструктуры Azure Stack;</span><span class="sxs-lookup"><span data-stu-id="43b2c-114">Support single role restore for Azures stack infrastructure backup.</span></span>
        - <span data-ttu-id="43b2c-115">добавлен параметр `RoleName` в командлет R `estore-AzsBackup`.</span><span class="sxs-lookup"><span data-stu-id="43b2c-115">Add parameter `RoleName` to cmdlet R`estore-AzsBackup`.</span></span>

    - <span data-ttu-id="43b2c-116">**FRP**: критические изменения для ресурсов **диска** и **тома**, используемых с API версии 2019-05-01.</span><span class="sxs-lookup"><span data-stu-id="43b2c-116">**FRP**: Breaking changes for **Drive** and **Volume** resources with API version 2019-05-01.</span></span> <span data-ttu-id="43b2c-117">Функции, поддерживаемые в Azure Stack Hub 1910 и более поздних версиях:</span><span class="sxs-lookup"><span data-stu-id="43b2c-117">The features are supported by Azure Stack Hub 1910 and later:</span></span>
        - <span data-ttu-id="43b2c-118">значения идентификатора `Name` `HealthStatus` и `OperationalStatus` были изменены;</span><span class="sxs-lookup"><span data-stu-id="43b2c-118">The value of ID, `Name`, `HealthStatus`, and `OperationalStatus` have been changed.</span></span>
        - <span data-ttu-id="43b2c-119">включена поддержка новых свойств `FirmwareVersion`, `IsIndicationEnabled`, `Manufacturer` и `StoragePool` для ресурсов **диска**;</span><span class="sxs-lookup"><span data-stu-id="43b2c-119">Supported new properties `FirmwareVersion`, `IsIndicationEnabled`, `Manufacturer`, and `StoragePool` for **Drive** resources.</span></span>
        - <span data-ttu-id="43b2c-120">свойства `CanPool` и `CannotPoolReason` ресурсов **диска** являются устаревшими; вместо них используйте `OperationalStatus`.</span><span class="sxs-lookup"><span data-stu-id="43b2c-120">The properties `CanPool` and `CannotPoolReason` of **Drive** resources have been deprecated; use `OperationalStatus` instead.</span></span>
