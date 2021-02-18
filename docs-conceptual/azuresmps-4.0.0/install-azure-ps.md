---
title: Установка и настройка модуля управления службами Azure PowerShell | Документация Майкрософт
description: Как установить и настроить Azure PowerShell для первого использования.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/06/2017
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 23ea4bcbd182cf1b063f2ae90921217de74a7044
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100401527"
---
# <a name="installing-the-azure-powershell-service-management-module"></a><span data-ttu-id="e6def-103">Установка модуля управления службами Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="e6def-103">Installing the Azure PowerShell Service Management module</span></span>

<span data-ttu-id="e6def-104">Предпочтительный способ установки Azure PowerShell — из [коллекции PowerShell](https://www.powershellgallery.com/).</span><span class="sxs-lookup"><span data-stu-id="e6def-104">Installing Azure PowerShell from the [PowerShell Gallery](https://www.powershellgallery.com/) is the preferred method of installation.</span></span>

## <a name="step-1-install-powershellget"></a><span data-ttu-id="e6def-105">Шаг 1. Установка PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="e6def-105">Step 1: Install PowerShellGet</span></span>

<span data-ttu-id="e6def-106">Чтобы установить элементы из коллекции PowerShell, требуется модуль PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="e6def-106">Installing items from the PowerShell Gallery requires the PowerShellGet module.</span></span> <span data-ttu-id="e6def-107">Убедитесь, что в системе установлена необходимая версия PowerShellGet и что выполнены другие требования к системе.</span><span class="sxs-lookup"><span data-stu-id="e6def-107">Make sure you have the appropriate version of PowerShellGet and other system requirements.</span></span> <span data-ttu-id="e6def-108">Выполните следующую команду, чтобы определить наличие PowerShellGet в вашей системе:</span><span class="sxs-lookup"><span data-stu-id="e6def-108">Run the following command to see if you have PowerShellGet installed on your system.</span></span>

```powershell
Get-InstalledModule PowerShellGet -AllVersions | Select-Object Name,Version,Path
```

<span data-ttu-id="e6def-109">Должен отобразиться результат, аналогичный следующему:</span><span class="sxs-lookup"><span data-stu-id="e6def-109">You should see something similar to the following output:</span></span>

```output
Name          Version Path
----          ------- ----
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

<span data-ttu-id="e6def-110">Если у вас не установлен PowerShellGet, перейдите к разделу [Как получить PowerShellGet](#how-to-get-powershellget).</span><span class="sxs-lookup"><span data-stu-id="e6def-110">If you do not have PowerShellGet installed, see the [How to get PowerShellGet](#how-to-get-powershellget).</span></span>

## <a name="step-2-install-azure-powershell"></a><span data-ttu-id="e6def-111">Шаг 2. Установите Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="e6def-111">Step 2: Install Azure PowerShell</span></span>

<span data-ttu-id="e6def-112">Войдите в консоль Windows PowerShell с правами администратора и выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="e6def-112">Run the following command from the Windows PowerShell console running as Administrator:</span></span>

```powershell
Install-Module Azure
```

<span data-ttu-id="e6def-113">Модуль Azure — это модуль свертки для командлетов Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="e6def-113">The Azure module is a rollup module for the Azure Resource Manager cmdlets.</span></span> <span data-ttu-id="e6def-114">При установке модуля AzureRM из коллекции PowerShell будут скачаны и установлены все модули Azure, которые ранее не были установлены.</span><span class="sxs-lookup"><span data-stu-id="e6def-114">When you install the AzureRM module, any other Azure modules that have not previously been installed will be downloaded and installed from the PowerShell Gallery.</span></span>

<span data-ttu-id="e6def-115">Модуль управления службой Azure использует те же зависимости, что и модули Azure PowerShell Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="e6def-115">The Azure Service Management module shares dependencies with the Azure PowerShell Resource Manager modules.</span></span> <span data-ttu-id="e6def-116">Если вы установили модули Azure PowerShell Resource Manager, необходимо добавить параметр `-AllowClobber` в команду установки.</span><span class="sxs-lookup"><span data-stu-id="e6def-116">If you have installed the Azure PowerShell Resource Manager modules, you will need to add the `-AllowClobber` parameter to the install command.</span></span> <span data-ttu-id="e6def-117">Таким образом все существующие общие зависимости будут обновлены.</span><span class="sxs-lookup"><span data-stu-id="e6def-117">This allows this existing shared dependencies to be updated.</span></span> <span data-ttu-id="e6def-118">Если этот параметр отсутствует, происходит сбой установки модуля.</span><span class="sxs-lookup"><span data-stu-id="e6def-118">Without this parameter, installation of the module fails.</span></span>

```powershell
Install-Module Azure -AllowClobber
```

<span data-ttu-id="e6def-119">После установки этого модуля вы можете импортировать модуль, выполнив следующую команду:</span><span class="sxs-lookup"><span data-stu-id="e6def-119">After you install this module, you can import the module by running the following command:</span></span>

```powershell
Import-Module Azure
```

## <a name="to-use-the-cmdlets"></a><span data-ttu-id="e6def-120">Использование командлетов</span><span class="sxs-lookup"><span data-stu-id="e6def-120">To use the cmdlets</span></span>

<span data-ttu-id="e6def-121">Чтобы начать работу с командлетами управления службами Azure, сначала войдите в свою учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="e6def-121">To start working with the Azure Service Management cmdlets, first log on to your Azure account.</span></span> <span data-ttu-id="e6def-122">Чтобы войти в учетную запись, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="e6def-122">To log on to your account, run the following command:</span></span>

```powershell
Add-AzureAccount
```

<span data-ttu-id="e6def-123">Когда вы войдете в Azure, Azure PowerShell создаст контекст для этого сеанса.</span><span class="sxs-lookup"><span data-stu-id="e6def-123">After logging into Azure, Azure PowerShell creates a context for the given session.</span></span> <span data-ttu-id="e6def-124">Этот контекст содержит среду Azure PowerShell, учетную запись, клиент и подписку, которые будут использоваться для всех командлетов в этом сеансе.</span><span class="sxs-lookup"><span data-stu-id="e6def-124">That context contains the Azure PowerShell environment, account, tenant, and subscription that will be used for all cmdlets within that session.</span></span> <span data-ttu-id="e6def-125">Теперь вы готовы использовать следующие модули.</span><span class="sxs-lookup"><span data-stu-id="e6def-125">Now you are ready to use the modules below.</span></span>

## <a name="azure-service-management-cmdlets"></a><span data-ttu-id="e6def-126">Командлеты для управления службами Azure</span><span class="sxs-lookup"><span data-stu-id="e6def-126">Azure Service Management cmdlets</span></span>

<span data-ttu-id="e6def-127">Модули Azure PowerShell часто обновляются.</span><span class="sxs-lookup"><span data-stu-id="e6def-127">Azure PowerShell modules are updated frequently.</span></span> <span data-ttu-id="e6def-128">Если вы заметили, что онлайн-справка по командлетам содержит командлеты и параметры, которых нет в вашем модуле, скачайте и установите последнюю версию модуля.</span><span class="sxs-lookup"><span data-stu-id="e6def-128">If you notice that the online cmdlet help includes cmdlets or parameters that are not in your module, download and install the latest version of the module.</span></span> <span data-ttu-id="e6def-129">Чтобы найти версию своего модуля, введите: `(Get-InstalledModule Azure).Version`.</span><span class="sxs-lookup"><span data-stu-id="e6def-129">To find the version of your module, type: `(Get-InstalledModule Azure).Version`.</span></span>

<span data-ttu-id="e6def-130">Примеры скриптов, с помощью которых можно автоматизировать некоторые распространенные задачи в Azure, см. в [центре скриптов Microsoft Azure](https://www.windowsazure.com/documentation/scripts/).</span><span class="sxs-lookup"><span data-stu-id="e6def-130">For sample scripts that can help you automate some of the common tasks in Azure, see the [Windows Azure Script Center](https://www.windowsazure.com/documentation/scripts/).</span></span>

<span data-ttu-id="e6def-131">Общие сведения об установке, обучении, использовании и настройке Windows PowerShell см. в статье, посвященной [работе со скриптами в Windows PowerShell](/powershell/scripting/learn/ps101/00-introduction).</span><span class="sxs-lookup"><span data-stu-id="e6def-131">For general information about installing, learning, using, and customizing Windows PowerShell, see [Scripting with Windows PowerShell](/powershell/scripting/learn/ps101/00-introduction).</span></span>

### <a name="how-to-get-powershellget"></a><span data-ttu-id="e6def-132">Как установить PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="e6def-132">How to get PowerShellGet</span></span>

|<span data-ttu-id="e6def-133">Сценарий</span><span class="sxs-lookup"><span data-stu-id="e6def-133">OS Version</span></span>|<span data-ttu-id="e6def-134">Инструкции по установке</span><span class="sxs-lookup"><span data-stu-id="e6def-134">Install instructions</span></span>|
|---|---|
|<span data-ttu-id="e6def-135">Используется Windows 10 или Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e6def-135">I have Windows 10 or Windows Server 2016</span></span>|<span data-ttu-id="e6def-136">Встроен в пакет Windows Management Framework (WMF) 5.0, который входит в состав ОС</span><span class="sxs-lookup"><span data-stu-id="e6def-136">Built into Windows Management Framework (WMF) 5.0 included in the OS</span></span>|
|<span data-ttu-id="e6def-137">Обновление до PowerShell 5.0</span><span class="sxs-lookup"><span data-stu-id="e6def-137">I want to upgrade to PowerShell 5</span></span>|[<span data-ttu-id="e6def-138">Установите последнюю версию WMF</span><span class="sxs-lookup"><span data-stu-id="e6def-138">Install the latest version of WMF</span></span>](https://www.microsoft.com/download/details.aspx?id=54616)|

<div id="helpmechoose"/>

### <a name="checking-the-version-of-azure-powershell"></a><span data-ttu-id="e6def-139">Проверка версии Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="e6def-139">Checking the version of Azure PowerShell</span></span>

<span data-ttu-id="e6def-140">Хотя мы советуем выполнить обновление до последней версии как можно раньше, несколько версий Azure PowerShell все еще поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="e6def-140">Although we encourage you to upgrade to the latest version as early as possible, several versions of Azure PowerShell are support.</span></span> <span data-ttu-id="e6def-141">Чтобы определить, какая версия Azure PowerShell установлена, выполните в командной строке команду `Get-InstalledModule Azure`.</span><span class="sxs-lookup"><span data-stu-id="e6def-141">To determine the version of Azure PowerShell you have installed, run `Get-InstalledModule Azure` from your command line.</span></span>

```powershell
Get-InstalledModule Azure -AllVersions | Select-Object Name,Version,Path
```
