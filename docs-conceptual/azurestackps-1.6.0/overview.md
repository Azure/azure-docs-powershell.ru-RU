---
title: Обзор модуля администрирования PowerShell для Azure Stack | Документация Майкрософт
description: Обзор модуля администрирования PowerShell для Azure Stack с инструкциями по установке и конфигурации.
author: bganapa
ms.author: bganapa
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 09/21/2018
ms.openlocfilehash: b0e85bec82b9b7c876b2bbf337b603c8d68cf6a3
ms.sourcegitcommit: d661f38bec34e65bf73913db59028e11fd78b131
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/05/2020
ms.locfileid: "63053321"
---
# <a name="azure-stack-module-160"></a><span data-ttu-id="7d594-103">Модуль Azure Stack 1.6.0</span><span class="sxs-lookup"><span data-stu-id="7d594-103">Azure Stack Module 1.6.0</span></span>

## <a name="requirements"></a><span data-ttu-id="7d594-104">Требования</span><span class="sxs-lookup"><span data-stu-id="7d594-104">Requirements:</span></span>
<span data-ttu-id="7d594-105">Минимальная поддерживаемая версия Azure Stack — 1811.</span><span class="sxs-lookup"><span data-stu-id="7d594-105">Minimum supported Azure Stack version is 1811.</span></span>

<span data-ttu-id="7d594-106">Примечание. Если вы используете более раннюю версию, установите версию 1.6.0.</span><span class="sxs-lookup"><span data-stu-id="7d594-106">Note: If you are using an earlier version install version 1.6.0</span></span>

## <a name="install"></a><span data-ttu-id="7d594-107">Установка</span><span class="sxs-lookup"><span data-stu-id="7d594-107">Install</span></span>
```
# Remove previous versions of AzureStack and AzureRM modules
Uninstall-Module -Name AzureRM -Force
Uninstall-Module -Name Azure.Storage -Force
Uninstall-Module -Name AzureStack -Force
Get-Module -Name "Azs*" -ListAvailable | Uninstall-Module  -Force 
Get-Module -Name "AzureRm*" -ListAvailable | Uninstall-Module  -Force

# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2018-03-01-hybrid -Force

# Install Azure Stack Admin Module
Install-Module -Name AzureStack -RequiredVersion 1.6.0
```

## <a name="release-notes"></a><span data-ttu-id="7d594-108">Заметки о выпуске</span><span class="sxs-lookup"><span data-stu-id="7d594-108">Release Notes</span></span>
* <span data-ttu-id="7d594-109">Поддержка в обновлении 1811.</span><span class="sxs-lookup"><span data-stu-id="7d594-109">Supported with 1811 update</span></span>
* <span data-ttu-id="7d594-110">Модуль Azs.Compute.Admin</span><span class="sxs-lookup"><span data-stu-id="7d594-110">Azs.Compute.Admin Module</span></span>
    * <span data-ttu-id="7d594-111">Исправлен отсутствующий префикс Azs для объекта New-DataDiskObject, добавлен псевдоним с предупреждением о том, что в дальнейшем командлет будет отмечен как нерекомендуемый.</span><span class="sxs-lookup"><span data-stu-id="7d594-111">Fixed missing Azs prefix for New-DataDiskObject and added alias with warning of future deprecation.</span></span>
* <span data-ttu-id="7d594-112">Модуль Azs.Update.Admin:</span><span class="sxs-lookup"><span data-stu-id="7d594-112">Azs.Update.Admin Module</span></span>
    * <span data-ttu-id="7d594-113">Добавлено предупреждение с рекомендацией запускать Test-AzureStack перед установкой AzsUpdate.</span><span class="sxs-lookup"><span data-stu-id="7d594-113">Added a warning to recommend running Test-AzureStack before Install-AzsUpdate</span></span>
* <span data-ttu-id="7d594-114">Azs.Fabric.Admin</span><span class="sxs-lookup"><span data-stu-id="7d594-114">Azs.Fabric.Admin</span></span>
    * <span data-ttu-id="7d594-115">Новый командлет (функции, поддерживаемые в Azure Stack 1811+):</span><span class="sxs-lookup"><span data-stu-id="7d594-115">New cmdlet (The features are supported by Azure Stack 1811+)</span></span>
        * <span data-ttu-id="7d594-116">Get-AzsDrive;</span><span class="sxs-lookup"><span data-stu-id="7d594-116">Get-AzsDrive</span></span>
        * <span data-ttu-id="7d594-117">Get-AzsVolume;</span><span class="sxs-lookup"><span data-stu-id="7d594-117">Get-AzsVolume</span></span>
        * <span data-ttu-id="7d594-118">Get-AzsStorageSubSystem.</span><span class="sxs-lookup"><span data-stu-id="7d594-118">Get-AzsStorageSubSystem</span></span>
    * <span data-ttu-id="7d594-119">Устаревшее</span><span class="sxs-lookup"><span data-stu-id="7d594-119">Deprecation</span></span>
        * <span data-ttu-id="7d594-120">Get-AzsInfrastructureVolume — это псевдоним для командлета Get-AzsVolume.</span><span class="sxs-lookup"><span data-stu-id="7d594-120">Get-AzsInfrastructureVolume is an alias now to the cmdlet Get-AzsVolume</span></span>
* <span data-ttu-id="7d594-121">Azs.InfrastructureInsights.Admin</span><span class="sxs-lookup"><span data-stu-id="7d594-121">Azs.InfrastructureInsights.Admin</span></span>
    *  <span data-ttu-id="7d594-122">Добавлен новый командлет Repair-AzsAlert.</span><span class="sxs-lookup"><span data-stu-id="7d594-122">Added a new cmdlet Repair-AzsAlert</span></span>
* <span data-ttu-id="7d594-123">Azs.Storage.Admin:</span><span class="sxs-lookup"><span data-stu-id="7d594-123">Azs.Storage.Admin</span></span>
    * <span data-ttu-id="7d594-124">Исправлена ошибка, возникающая, если значения квоты по умолчанию не используются.</span><span class="sxs-lookup"><span data-stu-id="7d594-124">Bug fix where default quota values are not being used</span></span>
* <span data-ttu-id="7d594-125">Модуль Azs.Subscriptions.Admin:</span><span class="sxs-lookup"><span data-stu-id="7d594-125">Azs.Subscriptions.Admin Module</span></span>
    * <span data-ttu-id="7d594-126">Исправлен отсутствующий префикс Azs для объекта New-AddonPlanDefinitionObject, добавлен псевдоним с предупреждением о том, что в дальнейшем командлет будет отмечен как нерекомендуемый.</span><span class="sxs-lookup"><span data-stu-id="7d594-126">Fixed missing Azs prefix for New-AddonPlanDefinitionObject and added alias with warning of future deprecation.</span></span>
