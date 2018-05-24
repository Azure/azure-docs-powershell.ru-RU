---
title: Установка и настройка модуля управления службами Azure PowerShell | Документация Майкрософт
description: Как установить и настроить Azure PowerShell для первого использования.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/06/2017
ms.openlocfilehash: 6f0f56dd09913ac535552aaa06c8e4431d78c24a
ms.sourcegitcommit: 5971c92cb023bdd1d71fa2ad0a3b378abfbd092a
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/23/2018
---
# <a name="installing-the-azure-powershell-service-management-module"></a><span data-ttu-id="2f33c-103">Установка модуля управления службами Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="2f33c-103">Installing the Azure PowerShell Service Management module</span></span>

<span data-ttu-id="2f33c-104">Предпочтительный способ установки Azure PowerShell — из [коллекции PowerShell](https://www.powershellgallery.com/).</span><span class="sxs-lookup"><span data-stu-id="2f33c-104">Installing Azure PowerShell from the [PowerShell Gallery](https://www.powershellgallery.com/) is the preferred method of installation.</span></span>

## <a name="step-1-install-powershellget"></a><span data-ttu-id="2f33c-105">Шаг 1. Установка PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="2f33c-105">Step 1: Install PowerShellGet</span></span>

<span data-ttu-id="2f33c-106">Чтобы установить элементы из коллекции PowerShell, требуется модуль PowerShellGet.</span><span class="sxs-lookup"><span data-stu-id="2f33c-106">Installing items from the PowerShell Gallery requires the PowerShellGet module.</span></span> <span data-ttu-id="2f33c-107">Убедитесь, что в системе установлена необходимая версия PowerShellGet и что выполнены другие требования к системе.</span><span class="sxs-lookup"><span data-stu-id="2f33c-107">Make sure you have the appropriate version of PowerShellGet and other system requirements.</span></span> <span data-ttu-id="2f33c-108">Выполните следующую команду, чтобы определить наличие PowerShellGet в вашей системе:</span><span class="sxs-lookup"><span data-stu-id="2f33c-108">Run the following command to see if you have PowerShellGet installed on your system.</span></span>

```powershell
Get-Module PowerShellGet -list | Select-Object Name,Version,Path
```

<span data-ttu-id="2f33c-109">Должен отобразиться похожий результат:</span><span class="sxs-lookup"><span data-stu-id="2f33c-109">You should see something similar to the following output:</span></span>

```
Name          Version Path
----          ------- ----
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

<span data-ttu-id="2f33c-110">Если у вас не установлен PowerShellGet, перейдите к разделу [Как получить PowerShellGet](#how-to-get-powershellget).</span><span class="sxs-lookup"><span data-stu-id="2f33c-110">If you do not have PowerShellGet installed, see the [How to get PowerShellGet](#how-to-get-powershellget).</span></span>

## <a name="step-2-install-azure-powershell"></a><span data-ttu-id="2f33c-111">Шаг 2. Установка Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="2f33c-111">Step 2: Install Azure PowerShell</span></span>

<span data-ttu-id="2f33c-112">Войдите в консоль Windows PowerShell с правами администратора и выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="2f33c-112">Run the following command from the Windows PowerShell console running as Administrator:</span></span>

```powershell
Install-Module Azure
```

<span data-ttu-id="2f33c-113">Модуль Azure — это модуль свертки для командлетов Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="2f33c-113">The Azure module is a rollup module for the Azure Resource Manager cmdlets.</span></span> <span data-ttu-id="2f33c-114">При установке модуля AzureRM из коллекции PowerShell будут скачаны и установлены все модули Azure, которые ранее не были установлены.</span><span class="sxs-lookup"><span data-stu-id="2f33c-114">When you install the AzureRM module, any other Azure modules that have not previously been installed will be downloaded and installed from the PowerShell Gallery.</span></span>

<span data-ttu-id="2f33c-115">Модуль управления службой Azure использует те же зависимости, что и модули Azure PowerShell Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="2f33c-115">The Azure Service Management module shares dependencies with the Azure PowerShell Resource Manager modules.</span></span> <span data-ttu-id="2f33c-116">Если вы установили модули Azure PowerShell Resource Manager, необходимо добавить параметр `-AllowClobber` в команду установки.</span><span class="sxs-lookup"><span data-stu-id="2f33c-116">If you have installed the Azure PowerShell Resource Manager modules, you will need to add the `-AllowClobber` parameter to the install command.</span></span> <span data-ttu-id="2f33c-117">Таким образом все существующие общие зависимости будут обновлены.</span><span class="sxs-lookup"><span data-stu-id="2f33c-117">This allows this existing shared dependencies to be updated.</span></span> <span data-ttu-id="2f33c-118">Если этот параметр отсутствует, происходит сбой установки модуля.</span><span class="sxs-lookup"><span data-stu-id="2f33c-118">Without this parameter, installation of the module fails.</span></span>

```powershell
Install-Module Azure -AllowClobber
```

<span data-ttu-id="2f33c-119">После установки этого модуля вы можете импортировать модуль, выполнив следующую команду:</span><span class="sxs-lookup"><span data-stu-id="2f33c-119">After you install this module, you can import the module by running the following command:</span></span>

```powershell
Import-Module Azure
```

## <a name="to-use-the-cmdlets"></a><span data-ttu-id="2f33c-120">Использование командлетов</span><span class="sxs-lookup"><span data-stu-id="2f33c-120">To use the cmdlets</span></span>

<span data-ttu-id="2f33c-121">Чтобы начать работу с командлетами управления службами Azure, сначала войдите в свою учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="2f33c-121">To start working with the Azure Service Management cmdlets, first log on to your Azure account.</span></span> <span data-ttu-id="2f33c-122">Чтобы войти в учетную запись, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="2f33c-122">To log on to your account, run the following command:</span></span>

```powershell
Add-AzureAccount
```

<span data-ttu-id="2f33c-123">Когда вы войдете в Azure, Azure PowerShell создаст контекст для этого сеанса.</span><span class="sxs-lookup"><span data-stu-id="2f33c-123">After logging into Azure, Azure PowerShell creates a context for the given session.</span></span> <span data-ttu-id="2f33c-124">Этот контекст содержит среду Azure PowerShell, учетную запись, клиент и подписку, которые будут использоваться для всех командлетов в этом сеансе.</span><span class="sxs-lookup"><span data-stu-id="2f33c-124">That context contains the Azure PowerShell environment, account, tenant, and subscription that will be used for all cmdlets within that session.</span></span> <span data-ttu-id="2f33c-125">Теперь вы готовы использовать следующие модули.</span><span class="sxs-lookup"><span data-stu-id="2f33c-125">Now you are ready to use the modules below.</span></span>

## <a name="azure-service-management-cmdlets"></a><span data-ttu-id="2f33c-126">Командлеты для управления службами Azure</span><span class="sxs-lookup"><span data-stu-id="2f33c-126">Azure Service Management cmdlets</span></span>

<span data-ttu-id="2f33c-127">Модули Azure PowerShell часто обновляются.</span><span class="sxs-lookup"><span data-stu-id="2f33c-127">Azure PowerShell modules are updated frequently.</span></span> <span data-ttu-id="2f33c-128">Если вы заметили, что онлайн-справка по командлетам содержит командлеты и параметры, которых нет в вашем модуле, скачайте и установите последнюю версию модуля.</span><span class="sxs-lookup"><span data-stu-id="2f33c-128">If you notice that the online cmdlet help includes cmdlets or parameters that are not in your module, download and install the latest version of the module.</span></span> <span data-ttu-id="2f33c-129">Чтобы найти версию своего модуля, введите: `(Get-Module Azure).Version`.</span><span class="sxs-lookup"><span data-stu-id="2f33c-129">To find the version of your module, type: `(Get-Module Azure).Version`.</span></span>

<span data-ttu-id="2f33c-130">Примеры скриптов, с помощью которых можно автоматизировать некоторые распространенные задачи в Azure, см. в [центре скриптов Microsoft Azure](http://www.windowsazure.com/documentation/scripts/).</span><span class="sxs-lookup"><span data-stu-id="2f33c-130">For sample scripts that can help you automate some of the common tasks in Azure, see the [Windows Azure Script Center](http://www.windowsazure.com/documentation/scripts/).</span></span>

<span data-ttu-id="2f33c-131">Общие сведения об установке, обучении, использовании и настройке Windows PowerShell см. в статье, посвященной [работе со скриптами в Windows PowerShell](http://go.microsoft.com/fwlink/p/?linkid=320210).</span><span class="sxs-lookup"><span data-stu-id="2f33c-131">For general information about installing, learning, using, and customizing Windows PowerShell, see [Scripting with Windows PowerShell](http://go.microsoft.com/fwlink/p/?linkid=320210).</span></span>

### <a name="how-to-get-powershellget"></a><span data-ttu-id="2f33c-132">Как получить PowerShellGet</span><span class="sxs-lookup"><span data-stu-id="2f33c-132">How to get PowerShellGet</span></span>

|<span data-ttu-id="2f33c-133">Сценарий</span><span class="sxs-lookup"><span data-stu-id="2f33c-133">OS Version</span></span>|<span data-ttu-id="2f33c-134">Инструкции по установке</span><span class="sxs-lookup"><span data-stu-id="2f33c-134">Install instructions</span></span>|
|---|---|
|<span data-ttu-id="2f33c-135">Используется Windows 10 или Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="2f33c-135">I have Windows 10 or Windows Server 2016</span></span>|<span data-ttu-id="2f33c-136">Встроены в Windows Management Framework (WMF) 5.0, которая входит в состав ОС</span><span class="sxs-lookup"><span data-stu-id="2f33c-136">Built into Windows Management Framework (WMF) 5.0 included in the OS</span></span>|
|<span data-ttu-id="2f33c-137">Обновление до PowerShell 5.0</span><span class="sxs-lookup"><span data-stu-id="2f33c-137">I want to upgrade to PowerShell 5</span></span>|[<span data-ttu-id="2f33c-138">Установите последнюю версию WMF</span><span class="sxs-lookup"><span data-stu-id="2f33c-138">Install the latest version of WMF</span></span>](https://www.microsoft.com/en-us/download/details.aspx?id=54616)|
|<span data-ttu-id="2f33c-139">Используется версия Windows с PowerShell 3 или PowerShell 4</span><span class="sxs-lookup"><span data-stu-id="2f33c-139">I am running on a version of Windows with PowerShell 3 or PowerShell 4</span></span>|[<span data-ttu-id="2f33c-140">Скачайте модули PackageManagement</span><span class="sxs-lookup"><span data-stu-id="2f33c-140">Get the PackageManagement modules</span></span>](http://go.microsoft.com/fwlink/?LinkID=746217)|

<a id="helpmechoose"></a>
### <a name="checking-the-version-of-azure-powershell"></a><span data-ttu-id="2f33c-141">Проверка версии Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="2f33c-141">Checking the version of Azure PowerShell</span></span>

<span data-ttu-id="2f33c-142">Хотя мы советуем выполнить обновление до последней версии как можно раньше, несколько версий Azure PowerShell все еще поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="2f33c-142">Although we encourage you to upgrade to the latest version as early as possible, several versions of Azure PowerShell are support.</span></span> <span data-ttu-id="2f33c-143">Чтобы определить, какая версия Azure PowerShell установлена, выполните в командной строке команду `Get-Module AzureRM`.</span><span class="sxs-lookup"><span data-stu-id="2f33c-143">To determine the version of Azure PowerShell you have installed, run `Get-Module AzureRM` from your command line.</span></span>

```powershell
Get-Module AzureRM -list | Select-Object Name,Version,Path
```
