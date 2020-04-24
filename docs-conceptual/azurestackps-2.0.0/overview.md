---
title: Обзор модуля администрирования PowerShell для Azure Stack Hub | Документация Майкрософт
description: Обзор модуля администрирования PowerShell Azure Stack Hub с инструкциями по установке и настройке.
author: sijuman
ms.author: sijuman
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 04/16/2020
ms.openlocfilehash: fd1f2a3778e348ba41b46acb4bdce19e18a7f4ec
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "81524971"
---
# <a name="azure-stack-hub-module-200"></a><span data-ttu-id="9fad5-103">Модуль Azure Stack Hub 2.0.0</span><span class="sxs-lookup"><span data-stu-id="9fad5-103">Azure Stack Hub Module 2.0.0</span></span>

## <a name="requirements"></a><span data-ttu-id="9fad5-104">Требования</span><span class="sxs-lookup"><span data-stu-id="9fad5-104">Requirements:</span></span>

<span data-ttu-id="9fad5-105">Минимальная поддерживаемая версия Azure Stack Hub — 2002.</span><span class="sxs-lookup"><span data-stu-id="9fad5-105">Minimum supported Azure Stack Hub version is 2002.</span></span>

<span data-ttu-id="9fad5-106">Примечание. Сведения о более ранних версиях Azure Stack см. в разделе [Установка PowerShell для Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell).</span><span class="sxs-lookup"><span data-stu-id="9fad5-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](https://docs.microsoft.com/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install"></a><span data-ttu-id="9fad5-107">Установка</span><span class="sxs-lookup"><span data-stu-id="9fad5-107">Install</span></span>

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose -ErrorAction Continue
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose -ErrorAction Continue
Get-Module -Name Az.* -ListAvailable | Uninstall-Module -Force -Verbose -ErrorAction Continue

Install-Module -Name Az.BootStrapper -Force -AllowPrerelease

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Use-AzProfile -Profile 2019-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 2.0.0-preview -AllowPrerelease
```


## <a name="release-notes"></a><span data-ttu-id="9fad5-108">Заметки о выпуске</span><span class="sxs-lookup"><span data-stu-id="9fad5-108">Release Notes</span></span>

* <span data-ttu-id="9fad5-109">Поддерживается в обновлении 2002.</span><span class="sxs-lookup"><span data-stu-id="9fad5-109">Supported with 2002 update.</span></span>  

  <span data-ttu-id="9fad5-110">Модуль Azure Stack Hub версии 2.0.0 является критическим изменением.</span><span class="sxs-lookup"><span data-stu-id="9fad5-110">The Azure Stack Hub 2.0.0 is a breaking change.</span></span> <span data-ttu-id="9fad5-111">Модуль использует модуль Az, а не модуль AzureRM.</span><span class="sxs-lookup"><span data-stu-id="9fad5-111">The module uses the Az module rather than the AzureRM module.</span></span> <span data-ttu-id="9fad5-112">См. [список критических изменений и руководство по миграции из AzureRM в Az Azure PowerShell в Azure Stack Hub](https://aka.ms/AA7qsji).</span><span class="sxs-lookup"><span data-stu-id="9fad5-112">You can find a migration guide and a list of breaking changes in [Migrate from AzureRM to Azure PowerShell Az in Azure Stack Hub](https://aka.ms/AA7qsji).</span></span>
