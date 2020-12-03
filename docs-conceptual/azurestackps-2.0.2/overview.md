---
title: Обзор модуля администрирования PowerShell для Azure Stack Hub | Документация Майкрософт
description: Обзор модуля администрирования PowerShell Azure Stack Hub с инструкциями по установке и настройке.
author: sijuman
ms.author: sijuman
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 08/06/2020
ms.openlocfilehash: 10eaf23e5134ea9788a81477038d735fe3bd59e0
ms.sourcegitcommit: 071b8c40c837ed4b2d65ce778339110d9e0899ab
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/01/2020
ms.locfileid: "96426992"
---
# <a name="azure-stack-hub-module-202"></a><span data-ttu-id="a3790-103">Модуль Azure Stack Hub 2.0.2</span><span class="sxs-lookup"><span data-stu-id="a3790-103">Azure Stack Hub Module 2.0.2</span></span>

## <a name="requirements"></a><span data-ttu-id="a3790-104">Требования</span><span class="sxs-lookup"><span data-stu-id="a3790-104">Requirements:</span></span>

<span data-ttu-id="a3790-105">Минимальная поддерживаемая версия Azure Stack Hub — 2002.</span><span class="sxs-lookup"><span data-stu-id="a3790-105">Minimum supported Azure Stack Hub version is 2002.</span></span>

<span data-ttu-id="a3790-106">Примечание. Сведения о более ранних версиях Azure Stack см. в разделе [Установка PowerShell для Azure Stack](/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell).</span><span class="sxs-lookup"><span data-stu-id="a3790-106">Note: For earlier versions of Azure Stack check [Install Azure Stack Powershell](/azure/azure-stack/azure-stack-powershell-install#install-azure-stack-powershell)</span></span>

## <a name="install"></a><span data-ttu-id="a3790-107">Установка</span><span class="sxs-lookup"><span data-stu-id="a3790-107">Install</span></span>

```powershell
# Remove previous versions of AzureStack and AzureRM modules
Get-Module -Name Azure* -ListAvailable | Uninstall-Module -Force -Verbose -ErrorAction Continue
Get-Module -Name Azs.* -ListAvailable | Uninstall-Module -Force -Verbose -ErrorAction Continue
Get-Module -Name Az.* -ListAvailable | Uninstall-Module -Force -Verbose -ErrorAction Continue

Install-Module -Name Az.BootStrapper -Force -AllowPrerelease

# Install and import the API Version Modules required by Azure Stack into the current PowerShell session.
Use-AzProfile -Profile 2019-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 2.0.2-preview -AllowPrerelease
```


## <a name="release-notes"></a><span data-ttu-id="a3790-108">Заметки о выпуске</span><span class="sxs-lookup"><span data-stu-id="a3790-108">Release Notes</span></span>

* <span data-ttu-id="a3790-109">Поддерживается в обновлении 2002.</span><span class="sxs-lookup"><span data-stu-id="a3790-109">Supported with 2002 update.</span></span>  

  <span data-ttu-id="a3790-110">Модуль Azure Stack Hub версии 2.0.0 является критическим изменением.</span><span class="sxs-lookup"><span data-stu-id="a3790-110">The Azure Stack Hub 2.0.0 is a breaking change.</span></span> <span data-ttu-id="a3790-111">Модуль использует модуль Az, а не модуль AzureRM.</span><span class="sxs-lookup"><span data-stu-id="a3790-111">The module uses the Az module rather than the AzureRM module.</span></span> <span data-ttu-id="a3790-112">См. [список критических изменений и руководство по миграции из AzureRM в Az Azure PowerShell в Azure Stack Hub](/azure-stack/operator/azure-stack-powershell-install).</span><span class="sxs-lookup"><span data-stu-id="a3790-112">You can find a migration guide and a list of breaking changes in [Migrate from AzureRM to Azure PowerShell Az in Azure Stack Hub](/azure-stack/operator/azure-stack-powershell-install).</span></span>