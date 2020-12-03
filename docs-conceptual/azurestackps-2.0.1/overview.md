---
title: Обзор модуля администрирования PowerShell для Azure Stack Hub | Документация Майкрософт
description: Обзор модуля администрирования PowerShell Azure Stack Hub с инструкциями по установке и настройке.
author: sijuman
ms.author: sijuman
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 06/22/2020
ms.openlocfilehash: f9bb71e19ecfe34f2c8646973f7a10526d2e8673
ms.sourcegitcommit: 071b8c40c837ed4b2d65ce778339110d9e0899ab
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/01/2020
ms.locfileid: "96427927"
---
# <a name="azure-stack-hub-module-201"></a><span data-ttu-id="5d688-103">Модуль Azure Stack Hub 2.0.1</span><span class="sxs-lookup"><span data-stu-id="5d688-103">Azure Stack Hub Module 2.0.1</span></span>

## <a name="requirements"></a><span data-ttu-id="5d688-104">Требования</span><span class="sxs-lookup"><span data-stu-id="5d688-104">Requirements:</span></span>

<span data-ttu-id="5d688-105">Минимальная поддерживаемая версия Azure Stack Hub — 2002.</span><span class="sxs-lookup"><span data-stu-id="5d688-105">Minimum supported Azure Stack Hub version is 2002.</span></span>

<span data-ttu-id="5d688-106">Примечание. Сведения о более ранних версиях Azure Stack см. в разделе [Установка PowerShell для Azure Stack](/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell).</span><span class="sxs-lookup"><span data-stu-id="5d688-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install"></a><span data-ttu-id="5d688-107">Установка</span><span class="sxs-lookup"><span data-stu-id="5d688-107">Install</span></span>

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose -ErrorAction Continue
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose -ErrorAction Continue
Get-Module -Name Az.* -ListAvailable | Uninstall-Module -Force -Verbose -ErrorAction Continue

Install-Module -Name Az.BootStrapper -Force -AllowPrerelease

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Use-AzProfile -Profile 2019-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 2.0.1-preview -AllowPrerelease
```


## <a name="release-notes"></a><span data-ttu-id="5d688-108">Заметки о выпуске</span><span class="sxs-lookup"><span data-stu-id="5d688-108">Release Notes</span></span>

* <span data-ttu-id="5d688-109">Поддерживается в обновлении 2002.</span><span class="sxs-lookup"><span data-stu-id="5d688-109">Supported with 2002 update.</span></span>  

  <span data-ttu-id="5d688-110">Модуль Azure Stack Hub версии 2.0.0 является критическим изменением.</span><span class="sxs-lookup"><span data-stu-id="5d688-110">The Azure Stack Hub 2.0.0 is a breaking change.</span></span> <span data-ttu-id="5d688-111">Модуль использует модуль Az, а не модуль AzureRM.</span><span class="sxs-lookup"><span data-stu-id="5d688-111">The module uses the Az module rather than the AzureRM module.</span></span> <span data-ttu-id="5d688-112">См. [список критических изменений и руководство по миграции из AzureRM в Az Azure PowerShell в Azure Stack Hub](/azure-stack/operator/azure-stack-powershell-install).</span><span class="sxs-lookup"><span data-stu-id="5d688-112">You can find a migration guide and a list of breaking changes in [Migrate from AzureRM to Azure PowerShell Az in Azure Stack Hub](/azure-stack/operator/azure-stack-powershell-install).</span></span>