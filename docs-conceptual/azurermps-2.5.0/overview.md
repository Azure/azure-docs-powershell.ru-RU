---
title: Общие сведения о PowerShell для Azure Stack | Документация Майкрософт
description: Обзор PowerShell для Azure Stack с инструкциями по установке и конфигурации.
author: bganapa
ms.author: bganapa
manager: knithinc
ms.devlang: powershell
ms.topic: conceptual
ms.manager: knithinc
ms.date: 09/21/2018
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 4b72bbd1bda93767251e0ba3d488f798575d9115
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "89244319"
---
# <a name="azurerm-module-250"></a><span data-ttu-id="129a0-103">Модуль AzureRM версии 2.5.0</span><span class="sxs-lookup"><span data-stu-id="129a0-103">AzureRM Module 2.5.0</span></span>

## <a name="requirements"></a><span data-ttu-id="129a0-104">Требования</span><span class="sxs-lookup"><span data-stu-id="129a0-104">Requirements:</span></span>
<span data-ttu-id="129a0-105">Минимальная поддерживаемая версия Azure Stack — 1904.</span><span class="sxs-lookup"><span data-stu-id="129a0-105">Minimum supported Azure Stack version is 1904.</span></span>

<span data-ttu-id="129a0-106">Примечание. Если вы используете более раннюю версию, установите версию 1.2.11.</span><span class="sxs-lookup"><span data-stu-id="129a0-106">Note: If you are using an earlier version install version 1.2.11</span></span>


## <a name="install"></a><span data-ttu-id="129a0-107">Установка</span><span class="sxs-lookup"><span data-stu-id="129a0-107">Install</span></span>
```powershell-interactive
# Remove previous versions of AzureStack modules
Uninstall-Module -Name AzureStack -Force 
Uninstall-Module -Name AzureRM -Force 
Uninstall-Module AzureRM.AzureStackAdmin -Force -ErrorAction Continue
Uninstall-Module AzureRM.AzureStackStorage -Force -ErrorAction Continue
Get-Module Azs.* -ListAvailable | Uninstall-Module -Force
Get-Module Azure.* -ListAvailable | Uninstall-Module -Force


# Install the AzureRM.Bootstrapper module. Select Yes when prompted to install NuGet
Install-Module -Name AzureRm.BootStrapper

# Install and import the API Version Profile required by Azure Stack into the current PowerShell session.
Use-AzureRmProfile -Profile 2018-03-01-hybrid -Force

```

## <a name="release-notes"></a><span data-ttu-id="129a0-108">Заметки о выпуске</span><span class="sxs-lookup"><span data-stu-id="129a0-108">Release Notes</span></span>
* <span data-ttu-id="129a0-109">AzureRm.Resources;</span><span class="sxs-lookup"><span data-stu-id="129a0-109">AzureRm.Resources</span></span>
    * <span data-ttu-id="129a0-110">Новый модуль ресурсов с поддержкой API версии 2018-05-01 с профилем 2019-03-01-hybrid.</span><span class="sxs-lookup"><span data-stu-id="129a0-110">New Resources module supporting 2018-05-01 api version with 2019-03-01-hybrid profile</span></span>
    * <span data-ttu-id="129a0-111">Операции PolicyDefinition(2016-12-01) и PolicyAssisgment(2017-06-01-preview) по-прежнему выполняются со старыми версиями API.</span><span class="sxs-lookup"><span data-stu-id="129a0-111">PolicyDefinition(2016-12-01) and PolicyAssisgment(2017-06-01-preview) operations are still with old api versions</span></span>
* <span data-ttu-id="129a0-112">AzureRm.Compute;</span><span class="sxs-lookup"><span data-stu-id="129a0-112">AzureRm.Compute</span></span>
    * <span data-ttu-id="129a0-113">Новый модуль вычислений с поддержкой API версии 2017-12-01.</span><span class="sxs-lookup"><span data-stu-id="129a0-113">New compute module supporting 2017-12-01 api version.'</span></span>


* <span data-ttu-id="129a0-114">Этот выпуск соответствует профилю API Azure Stack 2019-03-01-hybrid.</span><span class="sxs-lookup"><span data-stu-id="129a0-114">This release corresponds to the azurestack specific api profile 2019-03-01-hybrid</span></span>
* <span data-ttu-id="129a0-115">Все модули зависят от модуля AzureRm.Profile такой же или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="129a0-115">All the modules are taking greater than or equal to dependency on the AzureRm.Profile module.</span></span>
* <span data-ttu-id="129a0-116">Версии API, поддерживаемые каждым из модулей, обновлены.</span><span class="sxs-lookup"><span data-stu-id="129a0-116">Api version suppoerted by  each of the modules are updated.</span></span> 
    * <span data-ttu-id="129a0-117">Модуль вычислений — 2017-12-30</span><span class="sxs-lookup"><span data-stu-id="129a0-117">Compute - 2017-12-30</span></span>
    * <span data-ttu-id="129a0-118">Network — 2017-10-01</span><span class="sxs-lookup"><span data-stu-id="129a0-118">Network - 2017-10-01</span></span>
    * <span data-ttu-id="129a0-119">Storage — 2016-01-01</span><span class="sxs-lookup"><span data-stu-id="129a0-119">Storage - 2016-01-01</span></span>
    * <span data-ttu-id="129a0-120">Resources — 2018-02-01</span><span class="sxs-lookup"><span data-stu-id="129a0-120">Resources - 2018-02-01</span></span>
    * <span data-ttu-id="129a0-121">Keyvault — 2016-10-01</span><span class="sxs-lookup"><span data-stu-id="129a0-121">Keyvault - 2016-10-01</span></span>
    * <span data-ttu-id="129a0-122">DNS — 2016-04-01</span><span class="sxs-lookup"><span data-stu-id="129a0-122">Dns - 2016-04-01</span></span>
* <span data-ttu-id="129a0-123">Полное сопоставление версий API для каждого типа ресурса можно найти в файле https://github.com/Azure/azure-rest-api-specs/blob/master/profile/2018-03-01-hybrid.json.</span><span class="sxs-lookup"><span data-stu-id="129a0-123">The complete api version map for each of the resource types can be found at https://github.com/Azure/azure-rest-api-specs/blob/master/profile/2018-03-01-hybrid.json</span></span>

## <a name="content"></a><span data-ttu-id="129a0-124">Содержимое:</span><span class="sxs-lookup"><span data-stu-id="129a0-124">Content:</span></span>
### <a name="azure-bridge"></a><span data-ttu-id="129a0-125">Мост Azure</span><span class="sxs-lookup"><span data-stu-id="129a0-125">Azure Bridge</span></span>
<span data-ttu-id="129a0-126">Предварительная версия модуля для администраторов компонента Azure Stack "Мост Azure", которая позволяет объединять образы из Azure.</span><span class="sxs-lookup"><span data-stu-id="129a0-126">Preview release of the Azure Stack AzureBridge administrator module which allows you to syndicate images from Azure.</span></span>

### <a name="backup"></a><span data-ttu-id="129a0-127">Резервное копирование</span><span class="sxs-lookup"><span data-stu-id="129a0-127">Backup</span></span>
<span data-ttu-id="129a0-128">Предварительная версия модуля для администраторов службы Backup, которая позволяет администраторам:</span><span class="sxs-lookup"><span data-stu-id="129a0-128">Preview release of the Backup administrator module that allows administrators to:</span></span>
- <span data-ttu-id="129a0-129">настраивать расположение для хранения резервных копий;</span><span class="sxs-lookup"><span data-stu-id="129a0-129">Configure where backups are stored</span></span>
- <span data-ttu-id="129a0-130">выполнять резервное копирование;</span><span class="sxs-lookup"><span data-stu-id="129a0-130">Perform backups</span></span>
- <span data-ttu-id="129a0-131">выводить список созданных резервных копий и выполнять на их основе восстановление.</span><span class="sxs-lookup"><span data-stu-id="129a0-131">List and restore completed backup</span></span>

### <a name="commerce"></a><span data-ttu-id="129a0-132">Коммерция</span><span class="sxs-lookup"><span data-stu-id="129a0-132">Commerce</span></span>
<span data-ttu-id="129a0-133">Предварительная версия модуля для администраторов средства коммерции в Azure Stack, которая позволяет просматривать статистические сведения об использовании данных для всей системы Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="129a0-133">Preview release of the Azure Stack Commerce administrator module which provides a way to view aggregate data usage across your Azure Stack system.</span></span>

### <a name="compute"></a><span data-ttu-id="129a0-134">Службы вычислений</span><span class="sxs-lookup"><span data-stu-id="129a0-134">Compute</span></span>
<span data-ttu-id="129a0-135">Предварительная версия модуля для администраторов вычислительных ресурсов в Azure Stack, которая предоставляет функции управления квотами вычислительных ресурсов, образами платформ, управляемыми дисками и расширениями виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="129a0-135">Preview release of the Azure Stack Compute administrator module which provides functionality to manage compute quotas, platform images, managed disks and virtual machine extensions.</span></span>

### <a name="fabric"></a><span data-ttu-id="129a0-136">Fabric</span><span class="sxs-lookup"><span data-stu-id="129a0-136">Fabric</span></span>
<span data-ttu-id="129a0-137">Предварительная версия модуля для администраторов Fabric в Azure Stack, которая позволяет администраторам просматривать компоненты инфраструктуры и управлять ими, выполняя следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="129a0-137">Preview release of the Azure Stack Fabric administrator module which allows administrators to view and manage infrastructure components:</span></span>
- <span data-ttu-id="129a0-138">остановка, запуск и завершение работы для узлов единиц масштабирования;</span><span class="sxs-lookup"><span data-stu-id="129a0-138">Stop, Start and Shutdown of scale unit nodes</span></span>
- <span data-ttu-id="129a0-139">очистка и возобновление работы узлов единиц масштабирования для связанных действий FRU;</span><span class="sxs-lookup"><span data-stu-id="129a0-139">Drain and Resume of scale unit nodes for FRU related activities</span></span>
- <span data-ttu-id="129a0-140">исправление узлов единиц масштабирования;</span><span class="sxs-lookup"><span data-stu-id="129a0-140">Repair of scale unit nodes</span></span>
- <span data-ttu-id="129a0-141">перезапуск роли инфраструктуры;</span><span class="sxs-lookup"><span data-stu-id="129a0-141">Restart of Infrastructure role</span></span>
- <span data-ttu-id="129a0-142">остановка, запуск и завершение работы экземпляров роли инфраструктуры;</span><span class="sxs-lookup"><span data-stu-id="129a0-142">Stop, Start and Shutdown of Infrastructure role instances</span></span>
- <span data-ttu-id="129a0-143">создание пулов IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="129a0-143">Create new IP Pools</span></span>


### <a name="gallery"></a><span data-ttu-id="129a0-144">Коллекции</span><span class="sxs-lookup"><span data-stu-id="129a0-144">Gallery</span></span>
<span data-ttu-id="129a0-145">Предварительная версия модуля для администраторов коллекций Azure Stack, которая предоставляет функции для управления элементами коллекции в Azure Stack Marketplace.</span><span class="sxs-lookup"><span data-stu-id="129a0-145">Preview release of the Azure Stack Gallery administrator module which provides functionality to manage gallery items in the Azure Stack marketplace.</span></span>

### <a name="infrastructure-insights"></a><span data-ttu-id="129a0-146">Infrastructure Insights</span><span class="sxs-lookup"><span data-stu-id="129a0-146">Infrastructure Insights</span></span>
<span data-ttu-id="129a0-147">Предварительная версия модуля для администраторов Infrastructure Insights, которая позволяет администраторам:</span><span class="sxs-lookup"><span data-stu-id="129a0-147">Preview release of the Infrastructure Insights administrator module which allows administrators:</span></span>
- <span data-ttu-id="129a0-148">просматривать сведения о работоспособности ресурсов отметок в Azure Stack;</span><span class="sxs-lookup"><span data-stu-id="129a0-148">View the health of their Azure Stack stamp resources</span></span>
- <span data-ttu-id="129a0-149">просматривать оповещения и управлять ими.</span><span class="sxs-lookup"><span data-stu-id="129a0-149">View and manage alerts</span></span>

### <a name="keyvault"></a><span data-ttu-id="129a0-150">Хранилище ключей</span><span class="sxs-lookup"><span data-stu-id="129a0-150">KeyVault</span></span>
<span data-ttu-id="129a0-151">Предварительная версия модуля для администраторов Key Vault в Azure Stack, которая позволяет администратору просматривать квоты Key Vault.</span><span class="sxs-lookup"><span data-stu-id="129a0-151">Preview release of the Azure Stack KeyVault administrator module which allows administrator to view KeyVault quotas.</span></span>

### <a name="network"></a><span data-ttu-id="129a0-152">Сеть</span><span class="sxs-lookup"><span data-stu-id="129a0-152">Network</span></span>
<span data-ttu-id="129a0-153">Предварительная версия модуля для администраторов сетей, которая позволяет:</span><span class="sxs-lookup"><span data-stu-id="129a0-153">Preview release of the Network administrator module which allows:</span></span>
- <span data-ttu-id="129a0-154">управлять квотами сети;</span><span class="sxs-lookup"><span data-stu-id="129a0-154">Management of network quotas</span></span>
- <span data-ttu-id="129a0-155">просматривать выделенные сетевые ресурсы, например общедоступные IP-адреса, виртуальные сети, подсистемы балансировки нагрузки;</span><span class="sxs-lookup"><span data-stu-id="129a0-155">View allocated network resources such as public IP addresses, virtual networks, load balancers</span></span>
- <span data-ttu-id="129a0-156">использовать командлет для отображения общих сведений об администраторе.</span><span class="sxs-lookup"><span data-stu-id="129a0-156">Provides a cmdlet which displays an administrator overview</span></span>

### <a name="storage"></a><span data-ttu-id="129a0-157">Память</span><span class="sxs-lookup"><span data-stu-id="129a0-157">Storage</span></span>
<span data-ttu-id="129a0-158">Предварительная версия модуля для администраторов хранилища Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="129a0-158">Preview release of the Azure Stack Storage administrator module.</span></span>  <span data-ttu-id="129a0-159">В этом выпуске мы предоставляем следующие функции:</span><span class="sxs-lookup"><span data-stu-id="129a0-159">In this release we provide the functionality to:</span></span>
- <span data-ttu-id="129a0-160">управление квотами хранилища;</span><span class="sxs-lookup"><span data-stu-id="129a0-160">Manage storage quotas</span></span>
- <span data-ttu-id="129a0-161">сборка мусора для удаленных ресурсов хранилища;</span><span class="sxs-lookup"><span data-stu-id="129a0-161">Garbage collect deleted storage resources</span></span>
- <span data-ttu-id="129a0-162">восстановление удаленных учетных записей хранения;</span><span class="sxs-lookup"><span data-stu-id="129a0-162">Restore deleted storage accounts</span></span>
- <span data-ttu-id="129a0-163">перенос контейнеров из одной общей папки в другую;</span><span class="sxs-lookup"><span data-stu-id="129a0-163">Migrate containers from one share to another</span></span>
- <span data-ttu-id="129a0-164">просмотр сведений об отдельных компонентах хранилища;</span><span class="sxs-lookup"><span data-stu-id="129a0-164">View information about the individual storage components</span></span>
- <span data-ttu-id="129a0-165">просмотр сведений об использовании и производительности.</span><span class="sxs-lookup"><span data-stu-id="129a0-165">View usage and performance information</span></span>

### <a name="subscription-admin"></a><span data-ttu-id="129a0-166">Администратор подписки</span><span class="sxs-lookup"><span data-stu-id="129a0-166">Subscription Admin</span></span>
<span data-ttu-id="129a0-167">Предварительная версия модуля для администраторов подписки Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="129a0-167">Preview release of the Azure Stack Subscription administrator module.</span></span>  <span data-ttu-id="129a0-168">Этот модуль предоставляет следующие функции для администраторов:</span><span class="sxs-lookup"><span data-stu-id="129a0-168">This module provides functionality for administrators to:</span></span>
- <span data-ttu-id="129a0-169">управление планами и предложениями;</span><span class="sxs-lookup"><span data-stu-id="129a0-169">Manage plans and offers</span></span>
- <span data-ttu-id="129a0-170">просмотр сведений об использовании и производительности.</span><span class="sxs-lookup"><span data-stu-id="129a0-170">View usage and performance information</span></span>
- <span data-ttu-id="129a0-171">Управление RBAC</span><span class="sxs-lookup"><span data-stu-id="129a0-171">Manage RBAC</span></span>

### <a name="subscription"></a><span data-ttu-id="129a0-172">Подписка</span><span class="sxs-lookup"><span data-stu-id="129a0-172">Subscription</span></span>
<span data-ttu-id="129a0-173">Предварительная версия модуля подписки Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="129a0-173">Preview release of the Azure Stack Subscription module.</span></span>  <span data-ttu-id="129a0-174">Этот модуль предоставляет следующие функции для пользователей:</span><span class="sxs-lookup"><span data-stu-id="129a0-174">This module provides functionality for Users to:</span></span>
- <span data-ttu-id="129a0-175">создание, удаление и изменение подписок.</span><span class="sxs-lookup"><span data-stu-id="129a0-175">Create, Delete and Update Subscriptions</span></span>

### <a name="update"></a><span data-ttu-id="129a0-176">Update</span><span class="sxs-lookup"><span data-stu-id="129a0-176">Update</span></span>
<span data-ttu-id="129a0-177">Предварительная версия модуля для администраторов обновлений Azure Stack.</span><span class="sxs-lookup"><span data-stu-id="129a0-177">Preview release of the Azure Stack Update administrator module.</span></span>  <span data-ttu-id="129a0-178">В этом модуле администраторы могут:</span><span class="sxs-lookup"><span data-stu-id="129a0-178">In this module administrators can:</span></span>
- <span data-ttu-id="129a0-179">выводить список и устанавливать доступные обновления;</span><span class="sxs-lookup"><span data-stu-id="129a0-179">List and install available updates</span></span>
- <span data-ttu-id="129a0-180">возобновлять прерванную установку обновлений;</span><span class="sxs-lookup"><span data-stu-id="129a0-180">Resume interrupted updates</span></span>
- <span data-ttu-id="129a0-181">просматривать установленные обновления.</span><span class="sxs-lookup"><span data-stu-id="129a0-181">View installed updates</span></span>
