---
title: Заметки о выпуске Azure PowerShell
description: Узнайте обо всех последних обновлениях модулей Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/15/2019
ms.openlocfilehash: f77d901169b0d98b2425a2e50d33a1789150b770
ms.sourcegitcommit: e598dc45a26ff5a71112383252b350d750144a47
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/17/2019
ms.locfileid: "75182559"
---
## <a name="320---december-2019"></a><span data-ttu-id="71c25-103">3.2.0 — декабрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="71c25-103">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="71c25-104">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="71c25-104">General</span></span>
* <span data-ttu-id="71c25-105">Обновление ссылок в .psd1 для использования относительного пути для всех модулей.</span><span class="sxs-lookup"><span data-stu-id="71c25-105">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="71c25-106">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71c25-106">Az.Accounts</span></span>
* <span data-ttu-id="71c25-107">Установка правильного параметра UserAgent для телеметрии на стороне клиента для Az 4.0 (предварительная версия).</span><span class="sxs-lookup"><span data-stu-id="71c25-107">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="71c25-108">Отображение понятного пользователю сообщения об ошибке, если в Az 4.0 (предварительная версия) не указан контекст.</span><span class="sxs-lookup"><span data-stu-id="71c25-108">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="71c25-109">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="71c25-109">Az.Batch</span></span>
* <span data-ttu-id="71c25-110">Исправлена проблема [№ 10602](https://github.com/Azure/azure-powershell/issues/10602), из-за которой использование командлета **New-AzBatchPool** приводило к неправильной отправке VirtualMachineConfiguration.ContainerConfiguration или VirtualMachineConfiguration.DataDisks на сервер.</span><span class="sxs-lookup"><span data-stu-id="71c25-110">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="71c25-111">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="71c25-111">Az.DataFactory</span></span>
* <span data-ttu-id="71c25-112">Обновление пакета SDK Фабрики данных для .NET до версии 4.5.0.</span><span class="sxs-lookup"><span data-stu-id="71c25-112">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="71c25-113">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="71c25-113">Az.FrontDoor</span></span>
* <span data-ttu-id="71c25-114">Включена поддержка исключений управляемых правил WAF.</span><span class="sxs-lookup"><span data-stu-id="71c25-114">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="71c25-115">Добавление SocketAddr в список автозавершения.</span><span class="sxs-lookup"><span data-stu-id="71c25-115">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="71c25-116">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="71c25-116">Az.HealthcareApis</span></span>
* <span data-ttu-id="71c25-117">Обработка исключений.</span><span class="sxs-lookup"><span data-stu-id="71c25-117">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="71c25-118">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="71c25-118">Az.KeyVault</span></span>
* <span data-ttu-id="71c25-119">Исправлена ошибка при получении доступа к значению, которое может быть не задано.</span><span class="sxs-lookup"><span data-stu-id="71c25-119">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="71c25-120">Управление сертификатами шифрования на основе эллиптических кривых.</span><span class="sxs-lookup"><span data-stu-id="71c25-120">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="71c25-121">Включена возможность указания кривой для политик сертификатов.</span><span class="sxs-lookup"><span data-stu-id="71c25-121">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="71c25-122">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="71c25-122">Az.Monitor</span></span>
* <span data-ttu-id="71c25-123">Добавление необязательного аргумента в команду добавления параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="71c25-123">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="71c25-124">Существующий аргумент switch указывает на то, что экспорт в Log Analytics должен выполняться в фиксированную схему</span><span class="sxs-lookup"><span data-stu-id="71c25-124">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="71c25-125">(выделенный тип данных).</span><span class="sxs-lookup"><span data-stu-id="71c25-125">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71c25-126">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71c25-126">Az.Network</span></span>
* <span data-ttu-id="71c25-127">В приложении AzureFirewall, NAT и сетевых правилах включена поддержка IpGroups.</span><span class="sxs-lookup"><span data-stu-id="71c25-127">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="71c25-128">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71c25-128">Az.Resources</span></span>
* <span data-ttu-id="71c25-129">Устранена проблема, из-за которой при развертывании шаблона не удавалось считать его параметр, если имя параметра конфликтовало с именем встроенного параметра.</span><span class="sxs-lookup"><span data-stu-id="71c25-129">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="71c25-130">Обновлены командлеты политики для использования новой версии API 2019-09-01 с поддержкой группирования в определениях наборов политик.</span><span class="sxs-lookup"><span data-stu-id="71c25-130">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="71c25-131">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71c25-131">Az.Sql</span></span>
* <span data-ttu-id="71c25-132">Обновлена функция автоматического создания расширенного хранилища для службы оценки уязвимостей в учетной записи StorageV2.</span><span class="sxs-lookup"><span data-stu-id="71c25-132">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="71c25-133">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="71c25-133">Az.Storage</span></span>
* <span data-ttu-id="71c25-134">Включена поддержка создания маркера SAS на основе удостоверения контейнера и большого двоичного объекта с аутентификацией Oauth на основе контекста службы хранилища:</span><span class="sxs-lookup"><span data-stu-id="71c25-134">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="71c25-135">New-AzStorageContainerSASToken;</span><span class="sxs-lookup"><span data-stu-id="71c25-135">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="71c25-136">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="71c25-136">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="71c25-137">Отозвана поддержка ключей делегирования пользователя учетной записи хранения, а также всех маркеров SAS удостоверения:</span><span class="sxs-lookup"><span data-stu-id="71c25-137">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="71c25-138">Revoke-AzStorageAccountUserDelegationKeys.</span><span class="sxs-lookup"><span data-stu-id="71c25-138">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="71c25-139">Выполнено обновление до Microsoft.Azure.Management.Storage версии 14.2.0 для включения поддержки нового API версии 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="71c25-139">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="71c25-140">Включена поддержка значения, превышающего 5120, в параметре QuotaGiB в командлетах для работы с общими папками в плоскости управления и добавлен псевдоним Quota для параметра QuotaGiB:</span><span class="sxs-lookup"><span data-stu-id="71c25-140">Support Share QuotaGiB more than 5120 in Management plane File Share cmdlets, and add parameter alias 'Quota' to parameter 'QuotaGiB'</span></span> 
    - <span data-ttu-id="71c25-141">New-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="71c25-141">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="71c25-142">Update-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="71c25-142">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="71c25-143">Добавлен псевдоним QuotaGiB для параметра Quota:</span><span class="sxs-lookup"><span data-stu-id="71c25-143">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="71c25-144">Set-AzStorageShareQuota.</span><span class="sxs-lookup"><span data-stu-id="71c25-144">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="71c25-145">Устранена проблема, из-за которой при использовании AzStorageContainerAcl могла очищаться хранимая политика доступа:</span><span class="sxs-lookup"><span data-stu-id="71c25-145">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="71c25-146">Set-AzStorageContainerAcl.</span><span class="sxs-lookup"><span data-stu-id="71c25-146">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="71c25-147">Версия 3.1.0 от ноября 2019 г.</span><span class="sxs-lookup"><span data-stu-id="71c25-147">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="71c25-148">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="71c25-148">Highlights since the last major release</span></span>
* <span data-ttu-id="71c25-149">Выпуск Az.DataBoxEdge 1.0.0</span><span class="sxs-lookup"><span data-stu-id="71c25-149">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="71c25-150">Выпуск Az.SqlVirtualMachine 1.0.0</span><span class="sxs-lookup"><span data-stu-id="71c25-150">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71c25-151">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71c25-151">Az.Compute</span></span>
* <span data-ttu-id="71c25-152">Функция повторного применения виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="71c25-152">VM Reapply feature</span></span>
    - <span data-ttu-id="71c25-153">Добавлен параметр повторного применения в командлет Set-AzVM.</span><span class="sxs-lookup"><span data-stu-id="71c25-153">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="71c25-154">Функция AutomaticRepairs масштабируемого набора виртуальных машин:</span><span class="sxs-lookup"><span data-stu-id="71c25-154">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="71c25-155">Добавлены параметры EnableAutomaticRepair, AutomaticRepairGracePeriod и AutomaticRepairMaxInstanceRepairsPercent в следующие командлеты:   New-AzVmssConfig Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="71c25-155">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="71c25-156">Включена поддержка образа из коллекции разных клиентов для New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="71c25-156">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="71c25-157">Добавлен фрагмент Spot в средство заполнения аргументов параметра Priority в командлетах New-AzVM, New-AzVMConfig и New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="71c25-157">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="71c25-158">Добавлены параметры DiskIOPSReadWrite и DiskMBpsReadWrite в командлет Add-AzVmssDataDisk.</span><span class="sxs-lookup"><span data-stu-id="71c25-158">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="71c25-159">Изменен параметр SourceImageId командлета New-AzGalleryImageVersion на необязательный.</span><span class="sxs-lookup"><span data-stu-id="71c25-159">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="71c25-160">Добавлены параметры OSDiskImage и DataDiskImage в командлет New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="71c25-160">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="71c25-161">Добавлен параметр HyperVGeneration в командлет New-AzGalleryImageDefinition.</span><span class="sxs-lookup"><span data-stu-id="71c25-161">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="71c25-162">Добавлены параметры SkipExtensionsOnOverprovisionedVMs в командлеты New-AzVmss, New-AzVmssConfig и Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="71c25-162">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="71c25-163">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="71c25-163">Az.DataBoxEdge</span></span>
* <span data-ttu-id="71c25-164">Добавлен командлет `Get-AzDataBoxEdgeOrder`.</span><span class="sxs-lookup"><span data-stu-id="71c25-164">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="71c25-165">Получение заказа.</span><span class="sxs-lookup"><span data-stu-id="71c25-165">Get the Order</span></span>
* <span data-ttu-id="71c25-166">Добавлен командлет `New-AzDataBoxEdgeOrder`.</span><span class="sxs-lookup"><span data-stu-id="71c25-166">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="71c25-167">Создание заказа.</span><span class="sxs-lookup"><span data-stu-id="71c25-167">Create new Order</span></span>
* <span data-ttu-id="71c25-168">Добавлен командлет `Remove-AzDataBoxEdgeOrder`.</span><span class="sxs-lookup"><span data-stu-id="71c25-168">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="71c25-169">Удаление заказа.</span><span class="sxs-lookup"><span data-stu-id="71c25-169">Remove the Order</span></span>
* <span data-ttu-id="71c25-170">Изменен командлет `New-AzDataBoxEdgeShare`.</span><span class="sxs-lookup"><span data-stu-id="71c25-170">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="71c25-171">Создание локальной общей папки.</span><span class="sxs-lookup"><span data-stu-id="71c25-171">Now creates Local Share</span></span>
* <span data-ttu-id="71c25-172">Добавлен командлет `Set-AzDataBoxEdgeRole`.</span><span class="sxs-lookup"><span data-stu-id="71c25-172">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="71c25-173">Сопоставление IotRole с общей папкой.</span><span class="sxs-lookup"><span data-stu-id="71c25-173">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="71c25-174">Добавлен командлет `Invoke-AzDataBoxEdgeDevice`.</span><span class="sxs-lookup"><span data-stu-id="71c25-174">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="71c25-175">Вызов проверки обновлений, скачивание обновления, установка обновления на устройстве.</span><span class="sxs-lookup"><span data-stu-id="71c25-175">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="71c25-176">Добавлен командлет `Get-AzDataBoxEdgeTrigger`.</span><span class="sxs-lookup"><span data-stu-id="71c25-176">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="71c25-177">Получение сведений о триггерах.</span><span class="sxs-lookup"><span data-stu-id="71c25-177">Gets the information about Triggers</span></span>
* <span data-ttu-id="71c25-178">Добавлен командлет `New-AzDataBoxEdgeTrigger`.</span><span class="sxs-lookup"><span data-stu-id="71c25-178">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="71c25-179">Создание триггеров.</span><span class="sxs-lookup"><span data-stu-id="71c25-179">Create new Triggers</span></span>
* <span data-ttu-id="71c25-180">Добавлен командлет `Remove-AzDataBoxEdgeTrigger`.</span><span class="sxs-lookup"><span data-stu-id="71c25-180">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="71c25-181">Удаление триггеров.</span><span class="sxs-lookup"><span data-stu-id="71c25-181">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="71c25-182">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="71c25-182">Az.DataFactory</span></span>
* <span data-ttu-id="71c25-183">Обновление пакета SDK Фабрики данных для .NET до версии 4.4.0.</span><span class="sxs-lookup"><span data-stu-id="71c25-183">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="71c25-184">Добавлен параметр ExpressCustomSetup в командлет Set-AzureRmDataFactoryV2IntegrationRuntime для включения конфигураций установки и сторонних компонентов без использования настраиваемого скрипта установки.</span><span class="sxs-lookup"><span data-stu-id="71c25-184">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="71c25-185">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="71c25-185">Az.DataLakeStore</span></span>
* <span data-ttu-id="71c25-186">Обновлена документация по Get-AzDataLakeStoreDeletedItem и Restore-AzDataLakeStoreDeletedItem.</span><span class="sxs-lookup"><span data-stu-id="71c25-186">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="71c25-187">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="71c25-187">Az.EventHub</span></span>
* <span data-ttu-id="71c25-188">Исправлена проблема № 10301. Исправлен формат даты маркера SAS.</span><span class="sxs-lookup"><span data-stu-id="71c25-188">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="71c25-189">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="71c25-189">Az.FrontDoor</span></span>
* <span data-ttu-id="71c25-190">Добавлен параметр MinimumTlsVersion в Enable-AzFrontDoorCustomDomainHttps и New-AzFrontDoorFrontendEndpointObject.</span><span class="sxs-lookup"><span data-stu-id="71c25-190">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="71c25-191">Добавлены параметры HealthProbeMethod и EnabledState в New-AzFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="71c25-191">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="71c25-192">Добавлен новый командлет для создания объекта BackendPoolsSettings для передачи при создании и обновлении Front Door.</span><span class="sxs-lookup"><span data-stu-id="71c25-192">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="71c25-193">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="71c25-193">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71c25-194">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71c25-194">Az.Network</span></span>
* <span data-ttu-id="71c25-195">Изменены примеры параметра FilterData Start-AzVirtualNetworkGatewayConnectionPacketCapture.md и Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="71c25-195">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="71c25-196">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="71c25-196">Az.PrivateDns</span></span>
* <span data-ttu-id="71c25-197">Пакет SDK PrivateDns для .NET обновлен до версии 1.0.0</span><span class="sxs-lookup"><span data-stu-id="71c25-197">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="71c25-198">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="71c25-198">Az.RecoveryServices</span></span>
* <span data-ttu-id="71c25-199">Включена поддержка Azure Site Recovery для выбора типа диска при включении защиты.</span><span class="sxs-lookup"><span data-stu-id="71c25-199">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="71c25-200">Внесено исправление Azure Site Recovery для изменения действия плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="71c25-200">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="71c25-201">Включена поддержка восстановления SQL Azure Backup для принятия баз данных файлового потока.</span><span class="sxs-lookup"><span data-stu-id="71c25-201">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="71c25-202">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="71c25-202">Az.RedisCache</span></span>
* <span data-ttu-id="71c25-203">Добавлен параметр MinimumTlsVersion в командлеты New-AzRedisCache и Set-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="71c25-203">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="71c25-204">Кроме того, добавлен параметр MinimumTlsVersion в выходные данные командлета Get-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="71c25-204">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="71c25-205">Добавлена проверка параметра -Size для командлетов Set-AzRedisCache и New-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="71c25-205">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="71c25-206">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71c25-206">Az.Resources</span></span>
- <span data-ttu-id="71c25-207">Обновлены командлеты политики для использования новой версии API 2019-06-01 с новым свойством EnforcementMode в назначении политики.</span><span class="sxs-lookup"><span data-stu-id="71c25-207">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="71c25-208">Обновлен пример справки по созданию определения политики</span><span class="sxs-lookup"><span data-stu-id="71c25-208">Updated create policy definition help example</span></span>
- <span data-ttu-id="71c25-209">Исправлена ошибка с параметром -ServicePrincipalName командлета Remove-AZADServicePrincipal с возвратом пустой ссылки, если имя субъекта службы не найдено.</span><span class="sxs-lookup"><span data-stu-id="71c25-209">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="71c25-210">Исправлена ошибка с New-AZADServicePrincipal с возвратом пустой ссылки, если у клиента нет подписки.</span><span class="sxs-lookup"><span data-stu-id="71c25-210">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="71c25-211">Изменен командлет New-AzAdServicePrincipal для добавления учетных данных только для связанного приложения.</span><span class="sxs-lookup"><span data-stu-id="71c25-211">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="71c25-212">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71c25-212">Az.Sql</span></span>
* <span data-ttu-id="71c25-213">Добавлена поддержка ReadReplicaCount для базы данных.</span><span class="sxs-lookup"><span data-stu-id="71c25-213">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="71c25-214">Исправлена ошибка с Set-AzSqlDatabase, если избыточность в пределах зоны не настроена.</span><span class="sxs-lookup"><span data-stu-id="71c25-214">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="71c25-215">Версия 3.0.0 от ноября 2019 г.</span><span class="sxs-lookup"><span data-stu-id="71c25-215">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="71c25-216">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="71c25-216">General</span></span>
* <span data-ttu-id="71c25-217">Выпущена версия Az.PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="71c25-217">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="71c25-218">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71c25-218">Az.Accounts</span></span>
* <span data-ttu-id="71c25-219">Добавлено сообщение об устаревании для псевдонима "Resolve-Error".</span><span class="sxs-lookup"><span data-stu-id="71c25-219">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="71c25-220">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="71c25-220">Az.Advisor</span></span>
* <span data-ttu-id="71c25-221">Добавлена новая категория Operational Excellence (Эффективность работы) в командлет Get-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="71c25-221">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="71c25-222">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="71c25-222">Az.Batch</span></span>
* <span data-ttu-id="71c25-223">`CoreQuota` в `BatchAccountContext` переименован в `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="71c25-223">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="71c25-224">Также появился новый `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="71c25-224">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="71c25-225">Это влияет на **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="71c25-225">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="71c25-226">Параметр **New-AzBatchTask** `-ResourceFile` теперь принимает коллекцию объектов `PSResourceFile`, которые можно создать с помощью нового командлета **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="71c25-226">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="71c25-227">Новый командлет **New-AzBatchResourceFile**, который помогает создавать объекты `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="71c25-227">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="71c25-228">Их можно передавать в **New-AzBatchTask** в параметре `-ResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="71c25-228">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="71c25-229">Это позволяет поддерживать два новых типа файлов ресурсов, которые дополняют существующий метод `HttpUrl`:</span><span class="sxs-lookup"><span data-stu-id="71c25-229">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="71c25-230">Файлы ресурсов на основе `AutoStorageContainerName` скачивают весь контейнер автоматического хранения в узел пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="71c25-230">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="71c25-231">Файлы ресурсов на основе `StorageContainerUrl` скачивают указанный в URL-адресе контейнер в узел пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="71c25-231">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="71c25-232">Удалено свойство `ApplicationPackages` в `PSApplication`, который возвращается из **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="71c25-232">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="71c25-233">Отдельные пакеты в приложении теперь можно извлечь с помощью **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="71c25-233">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="71c25-234">Например, `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="71c25-234">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="71c25-235">`ApplicationId` переименован в `ApplicationName` для **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** и **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="71c25-235">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="71c25-236">Теперь `ApplicationId` является псевдонимом для `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="71c25-236">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="71c25-237">Добавлено новое свойство `PSWindowsUserConfiguration` в `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="71c25-237">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="71c25-238">`Version` переименован в `Name` для `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="71c25-238">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="71c25-239">`BlobSource` переименован в `HttpUrl` для `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="71c25-239">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="71c25-240">Удалено свойство `OSDisk` из `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="71c25-240">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="71c25-241">Удалена операция **Set-AzBatchPoolOSVersion**.</span><span class="sxs-lookup"><span data-stu-id="71c25-241">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="71c25-242">Больше она не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="71c25-242">This operation is no longer supported.</span></span>
* <span data-ttu-id="71c25-243">Удалено `TargetOSVersion` из `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="71c25-243">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="71c25-244">`CurrentOSVersion` переименован в `OSVersion` для `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="71c25-244">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="71c25-245">Удалено `DataEgressGiB` и `DataIngressGiB` из `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="71c25-245">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="71c25-246">Операция **Get-AzBatchNodeAgentSku** удалена и заменена на **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="71c25-246">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span> 
  - <span data-ttu-id="71c25-247">**Get-AzBatchSupportedImage** возвращает те же данные, что и **Get-AzBatchNodeAgentSku**, но в более удобном формате.</span><span class="sxs-lookup"><span data-stu-id="71c25-247">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="71c25-248">Также возвращаются новые непроверенные образы.</span><span class="sxs-lookup"><span data-stu-id="71c25-248">New non-verified images are also now returned.</span></span> <span data-ttu-id="71c25-249">Включается и дополнительная информация о `Capabilities` и `BatchSupportEndOfLife` для каждого образа.</span><span class="sxs-lookup"><span data-stu-id="71c25-249">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="71c25-250">Добавлена возможность монтировать файловые системы на каждом узле пула с помощью нового параметра `MountConfiguration` в **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="71c25-250">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="71c25-251">Теперь поддерживаются правила безопасности сети, которые блокируют сетевой доступ к пулу по исходящему порту трафика.</span><span class="sxs-lookup"><span data-stu-id="71c25-251">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="71c25-252">Это выполняется с помощью свойства `SourcePortRanges` для `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="71c25-252">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="71c25-253">Что касается выполнения контейнеров, пакетная служба теперь поддерживает выполнение задачи в рабочей папке контейнера или рабочей папке задачи пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="71c25-253">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="71c25-254">Выбор зависит от параметра `WorkingDirectory` в `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="71c25-254">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="71c25-255">Добавлена возможность указать коллекцию общедоступных IP-адресов для `PSNetworkConfiguration` с помощью нового свойства `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="71c25-255">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="71c25-256">Это гарантирует, что узлы в пуле будут иметь IP-адреса из списка, предоставленного пользователем.</span><span class="sxs-lookup"><span data-stu-id="71c25-256">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="71c25-257">Если значение не задано, по умолчанию для `WaitForSuccess` в `PSSTartTask` используется значение `$True` (ранее `$False`).</span><span class="sxs-lookup"><span data-stu-id="71c25-257">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="71c25-258">Если значение не задано, по умолчанию для `Scope` в `PSAutoUserSpecification` используется значение `Pool` (ранее `Task` для Windows или `Pool` для Linux).</span><span class="sxs-lookup"><span data-stu-id="71c25-258">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="71c25-259">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="71c25-259">Az.Cdn</span></span>
* <span data-ttu-id="71c25-260">Добавлены UrlRewriteAction и CacheKeyQueryStringAction в RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="71c25-260">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="71c25-261">Исправлено несколько ошибок, таких как отсутствующий входной параметр Selector в командлете New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="71c25-261">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71c25-262">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71c25-262">Az.Compute</span></span>
* <span data-ttu-id="71c25-263">Функция набора шифрования диска</span><span class="sxs-lookup"><span data-stu-id="71c25-263">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="71c25-264">Новые командлеты:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="71c25-264">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="71c25-265">Добавлен параметр ProximityPlacementGroupId в следующие командлеты: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="71c25-265">DiskEncryptionSetId parameter is added to the following cmdlets: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span></span>        
        <span data-ttu-id="71c25-266">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="71c25-266">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="71c25-267">Параметры DiskEncryptionSetId и EncryptionType добавлены в следующие командлеты:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="71c25-267">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="71c25-268">Добавлен параметр PublicIPAddressVersion в New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="71c25-268">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="71c25-269">FileUris для расширения пользовательских скриптов теперь будет защищенным, а не общедоступным параметром</span><span class="sxs-lookup"><span data-stu-id="71c25-269">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="71c25-270">Добавлено ScaleInPolicy в командлеты New-AzVmss, New-AzVmssConfig и Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="71c25-270">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="71c25-271">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="71c25-271">Breaking changes</span></span>
    - <span data-ttu-id="71c25-272">Параметр UploadSizeInBytes применяется теперь вместо DiskSizeGB для New-AzDiskConfig, если CreateOption имеет значение Upload</span><span class="sxs-lookup"><span data-stu-id="71c25-272">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="71c25-273">PublishingProfile.Source.ManagedImage.Id заменяется на StorageProfile.Source.Id в объекте GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="71c25-273">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="71c25-274">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="71c25-274">Az.DataFactory</span></span>
* <span data-ttu-id="71c25-275">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.3.0.</span><span class="sxs-lookup"><span data-stu-id="71c25-275">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="71c25-276">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="71c25-276">Az.DataLakeStore</span></span>
* <span data-ttu-id="71c25-277">Обновлен пакет SDK для ADLS (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), включает следующие исправления</span><span class="sxs-lookup"><span data-stu-id="71c25-277">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="71c25-278">Не создается исключение при невозможности десериализовать значение времени создания для записи в корзине или каталоге.</span><span class="sxs-lookup"><span data-stu-id="71c25-278">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="71c25-279">Предоставляется параметр для времени ожидания запроса в adlsclient</span><span class="sxs-lookup"><span data-stu-id="71c25-279">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="71c25-280">Исправлена передача исходного значения syncflag для восстановления badoffset</span><span class="sxs-lookup"><span data-stu-id="71c25-280">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="71c25-281">Исправлена операция EnumerateDirectory, чтобы она извлекала токен продолжения после проверки ответа</span><span class="sxs-lookup"><span data-stu-id="71c25-281">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="71c25-282">Исправлена ошибка объединения</span><span class="sxs-lookup"><span data-stu-id="71c25-282">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="71c25-283">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="71c25-283">Az.FrontDoor</span></span>
* <span data-ttu-id="71c25-284">Исправлены разные опечатки в разных частях модуля</span><span class="sxs-lookup"><span data-stu-id="71c25-284">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="71c25-285">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="71c25-285">Az.HDInsight</span></span>
* <span data-ttu-id="71c25-286">Исправлена ошибка, из-за которой клиент получал сообщение об ошибке 'Not a valid Base-64 string' (Не является допустимой строкой Base64) при выполнении Get-AzHDInsightCluster для получения кластера с хранилищем ADLSGen1.</span><span class="sxs-lookup"><span data-stu-id="71c25-286">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="71c25-287">Добавлен параметр с именем ApplicationId в три командлета Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig и New-AzHDInsightCluster, чтобы клиент мог предоставить идентификатор приложения субъекта-службы для доступа к Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="71c25-287">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="71c25-288">Для Microsoft.Azure.Management.HDInsight изменена версия с 2.1.0 на 5.1.0</span><span class="sxs-lookup"><span data-stu-id="71c25-288">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="71c25-289">Удалены пять командлетов:</span><span class="sxs-lookup"><span data-stu-id="71c25-289">Removed five cmdlets:</span></span>
    - <span data-ttu-id="71c25-290">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="71c25-290">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="71c25-291">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="71c25-291">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="71c25-292">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="71c25-292">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="71c25-293">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="71c25-293">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="71c25-294">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="71c25-294">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="71c25-295">Добавлены три командлета:</span><span class="sxs-lookup"><span data-stu-id="71c25-295">Added three cmdlets:</span></span>
    - <span data-ttu-id="71c25-296">Get-AzHDInsightMonitoring заменяет собой Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="71c25-296">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="71c25-297">Enable-AzHDInsightMonitoring заменяет собой Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="71c25-297">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="71c25-298">Disable-AzHDInsightMonitoring заменяет собой Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="71c25-298">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="71c25-299">Исправлен командлет Get-AzHDInsightProperties, чтобы он поддерживал получение сведений о возможностях из определенного расположения.</span><span class="sxs-lookup"><span data-stu-id="71c25-299">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="71c25-300">Удалены наборы параметров ("Spark1", "Spark2") из Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="71c25-300">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="71c25-301">Добавлены примеры в справочные документы по командлету Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="71c25-301">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="71c25-302">Изменен тип выходных данных для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="71c25-302">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="71c25-303">Для Get-AzHDInsightProperties тип выходных данных изменен с CapabilitiesResponse на AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="71c25-303">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="71c25-304">Для Remove-AzHDInsightCluster тип выходных данных изменен с ClusterGetResponse на bool.</span><span class="sxs-lookup"><span data-stu-id="71c25-304">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="71c25-305">Для Set-AzHDInsightGatewaySettings тип выходных данных изменен с HttpConnectivitySettings на GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="71c25-305">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="71c25-306">Добавлены несколько условий для проверки сценариев.</span><span class="sxs-lookup"><span data-stu-id="71c25-306">Added some scenario test cases.</span></span>
* <span data-ttu-id="71c25-307">Удалены несколько псевдонимов: Add-AzHDInsightConfigValues, Get-AzHDInsightProperties.</span><span class="sxs-lookup"><span data-stu-id="71c25-307">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="71c25-308">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="71c25-308">Az.IotHub</span></span>
* <span data-ttu-id="71c25-309">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="71c25-309">Breaking changes:</span></span>
    - <span data-ttu-id="71c25-310">Командлет Add-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="71c25-310">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="71c25-311">Удален набор параметров __AllParameterSets для командлета Add-AzIotHubEventHubConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="71c25-311">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="71c25-312">Командлет Get-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="71c25-312">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="71c25-313">Удален набор параметров __AllParameterSets для командлета Get-AzIotHubEventHubConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="71c25-313">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="71c25-314">Удалено свойство OperationsMonitoringProperties для типа Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties.</span><span class="sxs-lookup"><span data-stu-id="71c25-314">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="71c25-315">Удалено свойство OperationsMonitoringProperties для типа Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties.</span><span class="sxs-lookup"><span data-stu-id="71c25-315">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="71c25-316">Командлет New-AzIotHubExportDevice больше не поддерживает псевдоним New-AzIotHubExportDevices.</span><span class="sxs-lookup"><span data-stu-id="71c25-316">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="71c25-317">Командлет New-AzIotHubImportDevice больше не поддерживает псевдоним New-AzIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="71c25-317">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="71c25-318">Командлет Remove-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="71c25-318">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="71c25-319">Удален набор параметров __AllParameterSets для командлета Remove-AzIotHubEventHubConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="71c25-319">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="71c25-320">Командлет Set-AzIotHub теперь не поддерживает параметр OperationsMonitoringProperties и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="71c25-320">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="71c25-321">Удален набор параметров UpdateOperationsMonitoringProperties для командлета Set-AzIotHub.</span><span class="sxs-lookup"><span data-stu-id="71c25-321">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="71c25-322">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="71c25-322">Az.RecoveryServices</span></span>
* <span data-ttu-id="71c25-323">Azure Site Recovery поддерживает настройку сетевых ресурсов, например групп безопасности сети, общедоступных IP-адресов и внутренних подсистем балансировки нагрузки из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="71c25-323">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="71c25-324">Azure Site Recovery поддерживает запись на управляемый диск из vMWare в Azure.</span><span class="sxs-lookup"><span data-stu-id="71c25-324">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="71c25-325">Azure Site Recovery поддерживает сокращение NIC из vMWare в Azure.</span><span class="sxs-lookup"><span data-stu-id="71c25-325">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="71c25-326">Azure Site Recovery поддерживает ускорение сети NIC из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="71c25-326">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="71c25-327">Azure Site Recovery поддерживает автоматическое обновление агента из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="71c25-327">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="71c25-328">Azure Site Recovery поддерживает стандартный SSD-накопитель из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="71c25-328">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="71c25-329">Azure Site Recovery поддерживает двухпроходное шифрование диска Azure из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="71c25-329">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="71c25-330">Azure Site Recovery поддерживает новый добавленный диск из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="71c25-330">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="71c25-331">Добавлена функция SoftDelete для виртуальных машин и соответствующие тесты</span><span class="sxs-lookup"><span data-stu-id="71c25-331">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="71c25-332">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71c25-332">Az.Resources</span></span>
* <span data-ttu-id="71c25-333">Обновлена сборка зависимостей Microsoft.Extensions.Caching.Memory с версии 1.1.1 до 2.2</span><span class="sxs-lookup"><span data-stu-id="71c25-333">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71c25-334">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71c25-334">Az.Network</span></span>
* <span data-ttu-id="71c25-335">Изменены все командлеты для PrivateEndpointConnection, чтобы они поддерживали универсальный поставщик служб.</span><span class="sxs-lookup"><span data-stu-id="71c25-335">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="71c25-336">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="71c25-336">Updated cmdlet:</span></span>
        - <span data-ttu-id="71c25-337">Approve-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="71c25-337">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="71c25-338">Deny-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="71c25-338">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="71c25-339">Get-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="71c25-339">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="71c25-340">Remove-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="71c25-340">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="71c25-341">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="71c25-341">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="71c25-342">Добавлен новый командлет для PrivateLinkResource, который поддерживает универсальный поставщик служб.</span><span class="sxs-lookup"><span data-stu-id="71c25-342">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="71c25-343">Новый командлет</span><span class="sxs-lookup"><span data-stu-id="71c25-343">New cmdlet:</span></span>
        - <span data-ttu-id="71c25-344">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="71c25-344">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="71c25-345">Добавлены новые поля и параметр для протокола прокси версии 2.</span><span class="sxs-lookup"><span data-stu-id="71c25-345">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="71c25-346">Добавлено свойство EnableProxyProtocol в PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="71c25-346">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="71c25-347">Добавлено свойство LinkIdentifier в PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="71c25-347">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="71c25-348">Обновлен New-AzPrivateLinkService для поддержки нового необязательного параметра EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="71c25-348">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="71c25-349">Исправлено описание параметра в справочной документации по командлету New-AzApplicationGatewaySku.</span><span class="sxs-lookup"><span data-stu-id="71c25-349">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="71c25-350">Новые командлеты для поддержки политики брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="71c25-350">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="71c25-351">Добавлена поддержка дочерних ресурсов RouteTables для VirtualHub</span><span class="sxs-lookup"><span data-stu-id="71c25-351">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="71c25-352">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="71c25-352">New cmdlets added:</span></span>
        - <span data-ttu-id="71c25-353">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="71c25-353">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="71c25-354">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="71c25-354">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="71c25-355">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="71c25-355">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="71c25-356">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="71c25-356">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="71c25-357">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="71c25-357">Set-AzVirtualHub</span></span>
* <span data-ttu-id="71c25-358">Добавлена поддержка новых свойств SKU для VirtualHub и VirtualWANType в VirtualWan</span><span class="sxs-lookup"><span data-stu-id="71c25-358">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="71c25-359">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="71c25-359">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="71c25-360">New-AzVirtualHub: добавлен параметр Sku</span><span class="sxs-lookup"><span data-stu-id="71c25-360">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="71c25-361">Update-AzVirtualHub: добавлен параметр Sku</span><span class="sxs-lookup"><span data-stu-id="71c25-361">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="71c25-362">New-AzVirtualWan: добавлен параметр VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="71c25-362">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="71c25-363">Update-AzVirtualWan: добавлен параметр VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="71c25-363">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="71c25-364">Добавлена поддержка свойства EnableInternetSecurity для HubVnetConnection, VpnConnection и ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="71c25-364">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="71c25-365">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="71c25-365">New cmdlets added:</span></span>
        - <span data-ttu-id="71c25-366">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="71c25-366">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="71c25-367">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="71c25-367">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="71c25-368">New-AzureRmVirtualHubVnetConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="71c25-368">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="71c25-369">New-AzureRmVpnConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="71c25-369">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="71c25-370">Update-AzureRmVpnConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="71c25-370">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="71c25-371">New-AzureRmExpressRouteConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="71c25-371">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="71c25-372">Set-AzureRmExpressRouteConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="71c25-372">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="71c25-373">Добавлена поддержка настройки политики верхнего уровня WebApplicationFirewall</span><span class="sxs-lookup"><span data-stu-id="71c25-373">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="71c25-374">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="71c25-374">New cmdlets added:</span></span>
        - <span data-ttu-id="71c25-375">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="71c25-375">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="71c25-376">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="71c25-376">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="71c25-377">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="71c25-377">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="71c25-378">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="71c25-378">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="71c25-379">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="71c25-379">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="71c25-380">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="71c25-380">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="71c25-381">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="71c25-381">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="71c25-382">New-AzApplicationGatewayFirewallPolicy: добавлены параметры PolicySetting, ManagedRule</span><span class="sxs-lookup"><span data-stu-id="71c25-382">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="71c25-383">Добавлена поддержка оператора Geo-Match для CustomRule</span><span class="sxs-lookup"><span data-stu-id="71c25-383">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="71c25-384">Добавлен параметр GeoMatch в оператор для FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="71c25-384">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="71c25-385">Добавлена поддержка политики брандмауэра perListener и perSite</span><span class="sxs-lookup"><span data-stu-id="71c25-385">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="71c25-386">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="71c25-386">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="71c25-387">New-AzApplicationGatewayHttpListener: добавлены параметры FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="71c25-387">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="71c25-388">New-AzApplicationGatewayPathRuleConfig: добавлены параметры FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="71c25-388">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="71c25-389">Исправлен учет регистра для требуемой подсети с именем AzureBastionSubnet в PSBastion</span><span class="sxs-lookup"><span data-stu-id="71c25-389">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="71c25-390">Поддержка полного доменного имени назначения в правилах сети и преобразованного полного доменного имени в правилах NAT для брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="71c25-390">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="71c25-391">Добавлена поддержка ресурсов верхнего уровня RouteTables для IpGroup</span><span class="sxs-lookup"><span data-stu-id="71c25-391">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="71c25-392">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="71c25-392">New cmdlets added:</span></span>
        - <span data-ttu-id="71c25-393">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="71c25-393">New-AzIpGroup</span></span>
        - <span data-ttu-id="71c25-394">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="71c25-394">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="71c25-395">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="71c25-395">Get-AzIpGroup</span></span>
        - <span data-ttu-id="71c25-396">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="71c25-396">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="71c25-397">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="71c25-397">Az.ServiceFabric</span></span>
* <span data-ttu-id="71c25-398">Удален командлет Add-AzServiceFabricApplicationCertificate, так как соответствующий сценарий выполняется командлетом Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="71c25-398">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="71c25-399">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71c25-399">Az.Sql</span></span>
* <span data-ttu-id="71c25-400">Добавлена поддержка восстановления удаленных баз данных в управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="71c25-400">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="71c25-401">Из кода удалены старые командлеты аудита.</span><span class="sxs-lookup"><span data-stu-id="71c25-401">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="71c25-402">Удалены нерекомендуемые псевдонимы:</span><span class="sxs-lookup"><span data-stu-id="71c25-402">Removed deprecated aliases:</span></span>
* <span data-ttu-id="71c25-403">Get-AzSqlDatabaseIndexRecommendations (вместо него используйте Get-AzSqlDatabaseIndexRecommendation)</span><span class="sxs-lookup"><span data-stu-id="71c25-403">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="71c25-404">Get-AzSqlDatabaseRestorePoints (вместо него используйте Get-AzSqlDatabaseRestorePoint)</span><span class="sxs-lookup"><span data-stu-id="71c25-404">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="71c25-405">Удален командлет Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="71c25-405">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="71c25-406">Удалены псевдонимы для нерекомендуемых командлетов параметров оценки уязвимостей</span><span class="sxs-lookup"><span data-stu-id="71c25-406">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="71c25-407">Командлеты расширенного обнаружения угроз объявлены устаревшими</span><span class="sxs-lookup"><span data-stu-id="71c25-407">Deprecate Advanced Threat Detection Settings cmdlets</span></span> 
* <span data-ttu-id="71c25-408">Добавлены командлеты для отключения и включения рекомендаций о конфиденциальности для столбцов в базе данных.</span><span class="sxs-lookup"><span data-stu-id="71c25-408">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="71c25-409">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="71c25-409">Az.Storage</span></span>
* <span data-ttu-id="71c25-410">Поддержка включения большой общей папки при создании или обновлении учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="71c25-410">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="71c25-411">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="71c25-411">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="71c25-412">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="71c25-412">Set-AzStorageAccount</span></span>
* <span data-ttu-id="71c25-413">При закрытии или получении маркера файла пропускается проверка того, является ли входной путь файлом или каталогом, чтобы избежать сбоев при получении объектов в состоянии DeletePending.</span><span class="sxs-lookup"><span data-stu-id="71c25-413">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="71c25-414">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="71c25-414">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="71c25-415">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="71c25-415">Close-AzStorageFileHandle</span></span>
    
## <a name="280---october-2019"></a><span data-ttu-id="71c25-416">2.8.0 — октябрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="71c25-416">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="71c25-417">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="71c25-417">General</span></span>
* <span data-ttu-id="71c25-418">Выпуск Az.HealthcareApis 1.0.0</span><span class="sxs-lookup"><span data-stu-id="71c25-418">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="71c25-419">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71c25-419">Az.Accounts</span></span>
* <span data-ttu-id="71c25-420">Обновление телеметрии и перезаписи URL-адресов для созданных модулей, исправление для модульных тестов Windows.</span><span class="sxs-lookup"><span data-stu-id="71c25-420">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="71c25-421">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="71c25-421">Az.ApiManagement</span></span>
* <span data-ttu-id="71c25-422">**Set-AzApiManagementApi** — в ApiVersionSet добавлена поддержка обновления API.</span><span class="sxs-lookup"><span data-stu-id="71c25-422">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="71c25-423">исправлена проблема https://github.com/Azure/azure-powershell/issues/10068.</span><span class="sxs-lookup"><span data-stu-id="71c25-423">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="71c25-424">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="71c25-424">Az.Automation</span></span>
* <span data-ttu-id="71c25-425">Исправлен командлет New-AzureAutomationSoftwareUpdateConfiguration для параметра перезагрузки Linux.</span><span class="sxs-lookup"><span data-stu-id="71c25-425">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="71c25-426">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="71c25-426">Az.Batch</span></span>
* <span data-ttu-id="71c25-427">Командлет **Get-AzBatchNodeAgentSku** объявлен устаревшим и будет заменен на **Get-AzBatchSupportImage** в версии 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="71c25-427">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71c25-428">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71c25-428">Az.Compute</span></span>
* <span data-ttu-id="71c25-429">В командлеты New-AzVM и New-AzVmss добавлены параметры Priority, EvictionPolicy и MaxPrice.</span><span class="sxs-lookup"><span data-stu-id="71c25-429">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="71c25-430">Исправлены предупреждающее сообщение для командлетов Add-AzVMAdditionalUnattendContent и Add-AzVMSshPublicKey и справочная документация по ним.</span><span class="sxs-lookup"><span data-stu-id="71c25-430">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="71c25-431">Для Set-AzVMDiskEncryptionExtension исправлено исключение -skipVmBackup для виртуальных машин Linux с управляемыми дисками.</span><span class="sxs-lookup"><span data-stu-id="71c25-431">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="71c25-432">Исправлена ошибка при изменении параметров шифрования в Set-AzVMDiskEncryptionExtension, реализован двухэтапный сценарий.</span><span class="sxs-lookup"><span data-stu-id="71c25-432">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="71c25-433">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="71c25-433">Az.DataFactory</span></span>
* <span data-ttu-id="71c25-434">Добавлены команды CRUD для потока данных Фабрики данных Azure версии 2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow и Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="71c25-434">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="71c25-435">Добавлены команды действий для сеанса отладки потока данных Фабрики данных Azure версии 2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand и Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="71c25-435">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="71c25-436">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.2.0.</span><span class="sxs-lookup"><span data-stu-id="71c25-436">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="71c25-437">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="71c25-437">Az.DataLakeStore</span></span>
* <span data-ttu-id="71c25-438">Проверка учетной записи исправлена так, чтобы учетные записи, содержащие знак "-", можно было передавать без домена.</span><span class="sxs-lookup"><span data-stu-id="71c25-438">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="71c25-439">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="71c25-439">Az.HealthcareApis</span></span>
* <span data-ttu-id="71c25-440">Версия PowerShell обновлена до 1.0.0.</span><span class="sxs-lookup"><span data-stu-id="71c25-440">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="71c25-441">Версия пакета SDK обновлена до 1.0.2.</span><span class="sxs-lookup"><span data-stu-id="71c25-441">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="71c25-442">В тестах обновлены ссылки на новую версию пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="71c25-442">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="71c25-443">Вложенная выходная структура заменена на плоскую.</span><span class="sxs-lookup"><span data-stu-id="71c25-443">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="71c25-444">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="71c25-444">Az.IotHub</span></span>
* <span data-ttu-id="71c25-445">Добавлен новый источник маршрутизации DigitalTwinChangeEvents.</span><span class="sxs-lookup"><span data-stu-id="71c25-445">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="71c25-446">Исправлены незначительные ошибки: Get-AzIothub не возвращает subscriptionId.</span><span class="sxs-lookup"><span data-stu-id="71c25-446">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="71c25-447">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="71c25-447">Az.Monitor</span></span>
* <span data-ttu-id="71c25-448">Добавлены новые получатели групп действий: -ItsmReceiver, -VoiceReceiver, -ArmRoleReceiver, -AzureFunctionReceiver, -LogicAppReceiver, -AutomationRunbookReceiver, -AzureAppPushReceiver.</span><span class="sxs-lookup"><span data-stu-id="71c25-448">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="71c25-449">Для получателей включите общую схему оповещений.</span><span class="sxs-lookup"><span data-stu-id="71c25-449">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="71c25-450">Это не касается получателей SMS, push-уведомлений приложения Azure, ITSM и голосовых сообщений.</span><span class="sxs-lookup"><span data-stu-id="71c25-450">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="71c25-451">Веб-перехватчики теперь поддерживают аутентификацию Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="71c25-451">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71c25-452">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71c25-452">Az.Network</span></span>
* <span data-ttu-id="71c25-453">Добавлен новый командлет Get-AzAvailableServiceAlias, позволяющий получить псевдонимы для политик конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="71c25-453">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="71c25-454">В подключениях шлюза виртуальной сети появилась возможность добавлять селекторы трафика.</span><span class="sxs-lookup"><span data-stu-id="71c25-454">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="71c25-455">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="71c25-455">New cmdlets added:</span></span>
        - <span data-ttu-id="71c25-456">New-AzureRmTrafficSelectorPolicy.</span><span class="sxs-lookup"><span data-stu-id="71c25-456">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="71c25-457">В командлеты добавлены необязательные параметры -TrafficSelectorPolicies, -New-AzureRmVirtualNetworkGatewayConnection, -Set-AzureRmVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="71c25-457">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="71c25-458">В конфигурациях правил сетевой безопасности добавлена поддержка протоколов ESP и AH.</span><span class="sxs-lookup"><span data-stu-id="71c25-458">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="71c25-459">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="71c25-459">Updated cmdlets:</span></span>
        - <span data-ttu-id="71c25-460">Add-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="71c25-460">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="71c25-461">New-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="71c25-461">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="71c25-462">Set-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="71c25-462">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="71c25-463">Улучшена обработка исключений в командлетах Cortex.</span><span class="sxs-lookup"><span data-stu-id="71c25-463">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="71c25-464">Выпущены новые поколения и номера SKU VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="71c25-464">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="71c25-465">Представлены новые поколения VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="71c25-465">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="71c25-466">Представлены новые номера SKU VirtualNetworkGateways с высокой пропускной способностью.</span><span class="sxs-lookup"><span data-stu-id="71c25-466">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="71c25-467">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="71c25-467">Az.RedisCache</span></span>
* <span data-ttu-id="71c25-468">В справочную документацию по Set-AzRedisCache добавлены недостающие значения для параметра -Size.</span><span class="sxs-lookup"><span data-stu-id="71c25-468">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="71c25-469">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71c25-469">Az.Sql</span></span>
* <span data-ttu-id="71c25-470">Добавлена возможность назначать администратора Active Directory в Управляемом экземпляре.</span><span class="sxs-lookup"><span data-stu-id="71c25-470">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="71c25-471">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="71c25-471">Az.Storage</span></span>
* <span data-ttu-id="71c25-472">Клиентская библиотека службы хранилища Azure обновлена до версии 11.1.0.</span><span class="sxs-lookup"><span data-stu-id="71c25-472">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="71c25-473">NextPageLink теперь позволяет получить список контейнеров с помощью API плоскости управления.</span><span class="sxs-lookup"><span data-stu-id="71c25-473">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="71c25-474">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="71c25-474">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="71c25-475">NextPageLink теперь позволяет получить список учетных записей хранения из подписки.</span><span class="sxs-lookup"><span data-stu-id="71c25-475">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="71c25-476">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="71c25-476">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="71c25-477">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="71c25-477">Az.StorageSync</span></span>
* <span data-ttu-id="71c25-478">Исправлена проблема 9810 с Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="71c25-478">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="71c25-479">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="71c25-479">Az.Websites</span></span>
* <span data-ttu-id="71c25-480">Обновление плана службы приложений с помощью Set-AzWebApp приводило к сбою приложения.</span><span class="sxs-lookup"><span data-stu-id="71c25-480">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="71c25-481">2.7.0 — сентябрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="71c25-481">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="71c25-482">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="71c25-482">Az.ApiManagement</span></span>
* <span data-ttu-id="71c25-483">В справочной документации по командлету Set-AzApiManagementPolicy обновлено описание параметра -Format.</span><span class="sxs-lookup"><span data-stu-id="71c25-483">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="71c25-484">Из справочной документации удалены ссылки на нерекомендуемый командлет Update-AzApiManagementDeployment.</span><span class="sxs-lookup"><span data-stu-id="71c25-484">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="71c25-485">Вместо него следует использовать командлет Set-AzApiManagement.</span><span class="sxs-lookup"><span data-stu-id="71c25-485">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="71c25-486">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="71c25-486">Az.Automation</span></span>
* <span data-ttu-id="71c25-487">В справочной документации по командлету Register-AzAutomationDscNode исправлена опечатка в примере.</span><span class="sxs-lookup"><span data-stu-id="71c25-487">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="71c25-488">Добавлено уточнение об ограничениях ОС для командлета Register-AzAutomationDSCNode.</span><span class="sxs-lookup"><span data-stu-id="71c25-488">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="71c25-489">Исправлено исключение пустой ссылки для параметра -Wait в командлете Start-AzAutomationRunbook.</span><span class="sxs-lookup"><span data-stu-id="71c25-489">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71c25-490">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71c25-490">Az.Compute</span></span>
* <span data-ttu-id="71c25-491">Добавлен параметр UploadSizeInBytes для командлета New-AzDiskConfig.</span><span class="sxs-lookup"><span data-stu-id="71c25-491">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="71c25-492">Добавлен добавочный параметр для командлета New-AzSnapshotConfig.</span><span class="sxs-lookup"><span data-stu-id="71c25-492">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="71c25-493">Для виртуальной машины добавлены такие функции с низким приоритетом:</span><span class="sxs-lookup"><span data-stu-id="71c25-493">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="71c25-494">Для командлета New-AzVMConfig добавлены параметры MaxPrice, EvictionPolicy и Priority.</span><span class="sxs-lookup"><span data-stu-id="71c25-494">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="71c25-495">Для командлетов New-AzVmssConfig, Update-AzVM и Update-AzVmss добавлен параметр MaxPrice.</span><span class="sxs-lookup"><span data-stu-id="71c25-495">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="71c25-496">Для командлета Get-AzAvailabilitySet устранена проблема со ссылкой на виртуальную машину, когда в нем перечисляются все группы доступности в подписке.</span><span class="sxs-lookup"><span data-stu-id="71c25-496">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="71c25-497">Исправлено исключение NULL для командлета Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="71c25-497">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="71c25-498">Исправлен метод поиска VHD для относительной конечной позиции.</span><span class="sxs-lookup"><span data-stu-id="71c25-498">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="71c25-499">Устранена проблема с UltraSSD для командлетов New-AzVM и Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="71c25-499">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="71c25-500">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="71c25-500">Az.DataFactory</span></span>
* <span data-ttu-id="71c25-501">Добавлены 3 новые команды для ADF версии 2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription и Get-AzDataFactoryV2TriggerSubscriptionStatus.</span><span class="sxs-lookup"><span data-stu-id="71c25-501">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="71c25-502">Пакет SDK ADF для .NET обновлен до версии 4.1.3.</span><span class="sxs-lookup"><span data-stu-id="71c25-502">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="71c25-503">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="71c25-503">Az.HDInsight</span></span>
* <span data-ttu-id="71c25-504">Укажите критические изменения.</span><span class="sxs-lookup"><span data-stu-id="71c25-504">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="71c25-505">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="71c25-505">Az.IotHub</span></span>
* <span data-ttu-id="71c25-506">Добавлена поддержка для вызова отработки отказа для IotHub в георегион аварийного восстановления.</span><span class="sxs-lookup"><span data-stu-id="71c25-506">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="71c25-507">Добавлена поддержка для управления обогащением сообщений для IotHub.</span><span class="sxs-lookup"><span data-stu-id="71c25-507">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="71c25-508">Ниже перечислены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="71c25-508">New cmdlets are:</span></span>
    - <span data-ttu-id="71c25-509">Add-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="71c25-509">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="71c25-510">Get-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="71c25-510">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="71c25-511">Remove-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="71c25-511">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="71c25-512">Set-AzIotHubMessageEnrichment.</span><span class="sxs-lookup"><span data-stu-id="71c25-512">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="71c25-513">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="71c25-513">Az.Monitor</span></span>
* <span data-ttu-id="71c25-514">Указание на самую последнюю версию пакета SDK для монитора, т. е. 0.24.1-preview:</span><span class="sxs-lookup"><span data-stu-id="71c25-514">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="71c25-515">В командлеты метрик добавлены некритические изменения, т. е. перечисление единиц поддерживает несколько новых значений.</span><span class="sxs-lookup"><span data-stu-id="71c25-515">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="71c25-516">Эти командлеты доступны только для чтения, поэтому входные данные командлетов не будут изменены.</span><span class="sxs-lookup"><span data-stu-id="71c25-516">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="71c25-517">Актуальная версия API запросов **ActionGroups** — **2019-06-01**. До этого была версия **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="71c25-517">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="71c25-518">Тесты сценария обновлены в соответствии с этим изменением.</span><span class="sxs-lookup"><span data-stu-id="71c25-518">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="71c25-519">В конструкторы классов **EmailReceiver** и **WebhookReceiver** добавлен один новый обязательный аргумент — логическое значение с именем **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="71c25-519">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="71c25-520">Сейчас для него установлено значение **false**, чтобы скрыть это критическое изменение от командлетов.</span><span class="sxs-lookup"><span data-stu-id="71c25-520">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="71c25-521">**Примечание**. Это временное изменение, которое должно быть подтверждено командой оповещения.</span><span class="sxs-lookup"><span data-stu-id="71c25-521">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="71c25-522">Порядок аргументов для конструктора класса **Source** (связанного с классом **ScheduledQueryRuleSource**) изменился по сравнению с предыдущим пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="71c25-522">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="71c25-523">Это изменение требует, чтобы были исправлены два модульных теста: они были скомпилированы, но не прошли тест.</span><span class="sxs-lookup"><span data-stu-id="71c25-523">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="71c25-524">Порядок аргументов для конструктора класса **AlertingAction** (связанного с классом **ScheduledQueryRuleSource**) изменился по сравнению с предыдущим пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="71c25-524">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="71c25-525">Это изменение требует, чтобы были исправлены два модульных теста: они были скомпилированы, но не прошли тест.</span><span class="sxs-lookup"><span data-stu-id="71c25-525">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="71c25-526">Добавлена поддержка критериев динамического порога для оповещения метрики версии 2:</span><span class="sxs-lookup"><span data-stu-id="71c25-526">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="71c25-527">New-AzMetricAlertRuleV2Criteria: теперь также позволяет создавать критерии динамического порога.</span><span class="sxs-lookup"><span data-stu-id="71c25-527">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="71c25-528">Add-AzMetricAlertRuleV2: теперь также позволяет принимать критерии динамического порога.</span><span class="sxs-lookup"><span data-stu-id="71c25-528">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="71c25-529">Добавлены усовершенствования в командлетах запланированных правил запросов (SQR).</span><span class="sxs-lookup"><span data-stu-id="71c25-529">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="71c25-530">Командлеты будут принимать параметр Location в обоих форматах: расположение (например, eastus) или отображаемое имя расположения (например, "восточная часть США").</span><span class="sxs-lookup"><span data-stu-id="71c25-530">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="71c25-531">Параметр Enabled проиллюстрирован в файлах справки надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="71c25-531">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="71c25-532">Добавлены примеры для необязательного параметра ActionGroup.</span><span class="sxs-lookup"><span data-stu-id="71c25-532">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="71c25-533">Все файлы справки улучшены.</span><span class="sxs-lookup"><span data-stu-id="71c25-533">Overall improved help files</span></span>
* <span data-ttu-id="71c25-534">Исправлена ошибка в определении типа области для командлета Set-AzActionRule.</span><span class="sxs-lookup"><span data-stu-id="71c25-534">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71c25-535">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71c25-535">Az.Network</span></span>
* <span data-ttu-id="71c25-536">Исправлен неправильный пример в справочной документации по командлету New-AzApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="71c25-536">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="71c25-537">В справочную документацию по командлету Get-AzNetworkWatcherPacketCapture добавлено примечание, посвященное извлечению всех свойств для записи пакетов.</span><span class="sxs-lookup"><span data-stu-id="71c25-537">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="71c25-538">В справочной документации по командлету Test-AzNetworkWatcherIPFlow исправлен пример: теперь он правильно перечисляет сетевые карты.</span><span class="sxs-lookup"><span data-stu-id="71c25-538">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="71c25-539">Улучшен анализ облачных исключений для отображения дополнительных сведений (при их наличии).</span><span class="sxs-lookup"><span data-stu-id="71c25-539">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="71c25-540">Улучшен анализ облачных исключений для обработки дополнительного типа исключения SDK.</span><span class="sxs-lookup"><span data-stu-id="71c25-540">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="71c25-541">Исправлено неправильное сопоставление моделей правил безопасности.</span><span class="sxs-lookup"><span data-stu-id="71c25-541">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="71c25-542">Добавлены свойства сетевого интерфейса для компонента частного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="71c25-542">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="71c25-543">Для интерфейса PSNetworkInterface добавлено свойство PrivateEndpoint с типом PSResourceId.</span><span class="sxs-lookup"><span data-stu-id="71c25-543">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="71c25-544">В PSNetworkInterfaceIPConfiguration добавлено свойство PrivateLinkConnectionProperties с типом PSIpConfigurationConnectivityInformation.</span><span class="sxs-lookup"><span data-stu-id="71c25-544">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="71c25-545">Добавлен новый класс модели: PSIpConfigurationConnectivityInformation.</span><span class="sxs-lookup"><span data-stu-id="71c25-545">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="71c25-546">Добавлен новый тип ApplicationRuleProtocolType "mssql" для ресурса Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="71c25-546">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="71c25-547">Поддержка многоканального подключения в Виртуальной глобальной сети:</span><span class="sxs-lookup"><span data-stu-id="71c25-547">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="71c25-548">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="71c25-548">New cmdlets</span></span>
        - <span data-ttu-id="71c25-549">New-AzVpnSiteLink;</span><span class="sxs-lookup"><span data-stu-id="71c25-549">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="71c25-550">New-AzVpnSiteLinkConnection;</span><span class="sxs-lookup"><span data-stu-id="71c25-550">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="71c25-551">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="71c25-551">Updated cmdlet:</span></span>
        - <span data-ttu-id="71c25-552">New-VpnSite;</span><span class="sxs-lookup"><span data-stu-id="71c25-552">New-VpnSite</span></span>
        - <span data-ttu-id="71c25-553">Update-VpnSite;</span><span class="sxs-lookup"><span data-stu-id="71c25-553">Update-VpnSite</span></span>
        - <span data-ttu-id="71c25-554">New-VpnConnection;</span><span class="sxs-lookup"><span data-stu-id="71c25-554">New-VpnConnection</span></span>
        - <span data-ttu-id="71c25-555">Update-VpnConnection.</span><span class="sxs-lookup"><span data-stu-id="71c25-555">Update-VpnConnection</span></span>
* <span data-ttu-id="71c25-556">Исправлены документы с некоторыми примерами PowerShell для использования командлетов AZ вместо командлетов AzureRM.</span><span class="sxs-lookup"><span data-stu-id="71c25-556">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="71c25-557">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="71c25-557">Az.RecoveryServices</span></span>
* <span data-ttu-id="71c25-558">Для объекта AzureVMpolicy добавлен новый атрибут — ProtectedItemsCount.</span><span class="sxs-lookup"><span data-stu-id="71c25-558">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="71c25-559">Добавлены тесты для политики виртуальной машины и восстановления исходной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="71c25-559">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="71c25-560">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71c25-560">Az.Resources</span></span>
* <span data-ttu-id="71c25-561">Исправлена ошибка, при которой не удавалось вызвать командлет New-AzRoleAssignment без параметра Scope.</span><span class="sxs-lookup"><span data-stu-id="71c25-561">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="71c25-562">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="71c25-562">Az.ServiceFabric</span></span>
* <span data-ttu-id="71c25-563">Исправлена опечатка в примере в справочной документации по командлету Update-AzServiceFabricReliability.</span><span class="sxs-lookup"><span data-stu-id="71c25-563">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="71c25-564">Добавлены новые командлеты для управления приложениями и службами:</span><span class="sxs-lookup"><span data-stu-id="71c25-564">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="71c25-565">New-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="71c25-565">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="71c25-566">New-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="71c25-566">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="71c25-567">New-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="71c25-567">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="71c25-568">New-AzServiceFabricService;</span><span class="sxs-lookup"><span data-stu-id="71c25-568">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="71c25-569">Update-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="71c25-569">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="71c25-570">Get-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="71c25-570">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="71c25-571">Get-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="71c25-571">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="71c25-572">Get-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="71c25-572">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="71c25-573">Get-AzServiceFabricService;</span><span class="sxs-lookup"><span data-stu-id="71c25-573">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="71c25-574">Remove-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="71c25-574">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="71c25-575">Remove-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="71c25-575">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="71c25-576">Remove-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="71c25-576">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="71c25-577">Remove-AzServiceFabricServic.</span><span class="sxs-lookup"><span data-stu-id="71c25-577">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="71c25-578">Пакет SDK для Service Fabric обновлен до версии 1.2.0, в которой используется версия API 2019-03-01 поставщика ресурсов Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="71c25-578">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="71c25-579">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="71c25-579">Az.SignalR</span></span>
* <span data-ttu-id="71c25-580">Добавлены командлеты Update, Restart, CheckNameAvailability и GetUsage.</span><span class="sxs-lookup"><span data-stu-id="71c25-580">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="71c25-581">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71c25-581">Az.Sql</span></span>
* <span data-ttu-id="71c25-582">Обновлен пример в справочной документации по командлету Get-AzSqlElasticPool.</span><span class="sxs-lookup"><span data-stu-id="71c25-582">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="71c25-583">Добавлен пример виртуального ядра для командлета создания эластичного пула (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="71c25-583">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="71c25-584">Удалена проверка свойства EmailAddresses и того, что свойство EmailAdmins правильное в случае, если свойство EmailAddresses пустое в командлетах Set-AzSqlServerAdvancedThreatProtectionPolicy и Set-AzSqlDatabaseAdvancedThreatProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="71c25-584">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="71c25-585">Теперь, если существует несколько параметров диагностики, включающих категорию аудита, параметры аудита сервера и базы данных удаляются.</span><span class="sxs-lookup"><span data-stu-id="71c25-585">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="71c25-586">Исправлена проверка адресов электронной почты в нескольких командлетах оценки уязвимостей SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting и Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="71c25-586">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="71c25-587">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="71c25-587">Az.Storage</span></span>
* <span data-ttu-id="71c25-588">Обновлен пример в справочной документации по командлету Get-AzStorageAccountKey.</span><span class="sxs-lookup"><span data-stu-id="71c25-588">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="71c25-589">Теперь при отправке и загрузке файла Azure в конечном файле сохраняются свойства SMB исходного файла (атрибуты файла, время создания файла, время последней записи файла).</span><span class="sxs-lookup"><span data-stu-id="71c25-589">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="71c25-590">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="71c25-590">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="71c25-591">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="71c25-591">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="71c25-592">Исправлена операция отправки блочного BLOB-объекта, в которой происходили сбои свойств и метаданных в контейнере с включенной ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="71c25-592">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="71c25-593">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="71c25-593">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="71c25-594">Добавлена поддержка управления общими папками Azure в API плоскости управления с помощью таких командлетов:</span><span class="sxs-lookup"><span data-stu-id="71c25-594">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="71c25-595">New-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="71c25-595">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="71c25-596">Get-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="71c25-596">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="71c25-597">Update-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="71c25-597">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="71c25-598">Remove-AzRmStorageShare.</span><span class="sxs-lookup"><span data-stu-id="71c25-598">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="71c25-599">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="71c25-599">Az.Websites</span></span>
* <span data-ttu-id="71c25-600">Устранена проблема, из-за которой теги webapp удалялись при переносе приложения в новый ASP.</span><span class="sxs-lookup"><span data-stu-id="71c25-600">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="71c25-601">Теперь командлет Publish-AzureWebapp работает в Linux и Windows.</span><span class="sxs-lookup"><span data-stu-id="71c25-601">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="71c25-602">Обновлен пример в справочной документации по командлету Get-AzWebAppPublishingProfile.</span><span class="sxs-lookup"><span data-stu-id="71c25-602">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="71c25-603">2.6.0 — август 2019 г.</span><span class="sxs-lookup"><span data-stu-id="71c25-603">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="71c25-604">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="71c25-604">General</span></span>
* <span data-ttu-id="71c25-605">Исправлены опечатки в модулях.</span><span class="sxs-lookup"><span data-stu-id="71c25-605">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="71c25-606">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71c25-606">Az.Accounts</span></span>
* <span data-ttu-id="71c25-607">Добавлена поддержка назначаемого пользователем удостоверения MSI при проверке подлинности в Функциях Azure (№ 9479).</span><span class="sxs-lookup"><span data-stu-id="71c25-607">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="71c25-608">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="71c25-608">Az.Aks</span></span>
* <span data-ttu-id="71c25-609">Устранена проблема с выходными данными для Get-AzAks.</span><span class="sxs-lookup"><span data-stu-id="71c25-609">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="71c25-610">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/9847.</span><span class="sxs-lookup"><span data-stu-id="71c25-610">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="71c25-611">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="71c25-611">Az.ApiManagement</span></span>
* <span data-ttu-id="71c25-612">исправлена проблема https://github.com/Azure/azure-powershell/issues/9351.</span><span class="sxs-lookup"><span data-stu-id="71c25-612">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="71c25-613">Обновлена версия NuGet для .NET, которая не накладывает ограничений на productId, apiId, groupId и userId.</span><span class="sxs-lookup"><span data-stu-id="71c25-613">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="71c25-614">**Get-AzApiManagementProduct**. Добавлена поддержка запросов к продуктам с помощью API.</span><span class="sxs-lookup"><span data-stu-id="71c25-614">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="71c25-615">**New-AzApiManagementApiRevision**. Устранена проблема, из-за которой не задавался параметр ApiRevisionDescription при создании новой редакции API https://github.com/Azure/azure-powershell/issues/9752.</span><span class="sxs-lookup"><span data-stu-id="71c25-615">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="71c25-616">Исправлено написание имени модели c PsApiManagementOAuth2AuthrozationServer на PsApiManagementOAuth2AuthorizationServer.</span><span class="sxs-lookup"><span data-stu-id="71c25-616">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="71c25-617">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="71c25-617">Az.Batch</span></span>
* <span data-ttu-id="71c25-618">Исправлена опечатка в написании Windows со строчной буквы в справочных сообщениях и документации.</span><span class="sxs-lookup"><span data-stu-id="71c25-618">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="71c25-619">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="71c25-619">Az.Cdn</span></span>
* <span data-ttu-id="71c25-620">Исправлена опечатка во вспомогательном приложении модуля CDN.</span><span class="sxs-lookup"><span data-stu-id="71c25-620">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71c25-621">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71c25-621">Az.Compute</span></span>
* <span data-ttu-id="71c25-622">Добавлен параметр VmssId в новый командлет Add New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="71c25-622">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="71c25-623">Добавлены параметры TerminateScheduledEvents и TerminateScheduledEventNotBeforeTimeoutInMinutes в New-AzVmssConfig и Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="71c25-623">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="71c25-624">Добавлено свойство HyperVGeneration в объект образа виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="71c25-624">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="71c25-625">Добавлены компоненты Host и HostGroup.</span><span class="sxs-lookup"><span data-stu-id="71c25-625">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="71c25-626">Новые командлеты:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="71c25-626">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="71c25-627">Параметр HostId добавлен в New-AzVMConfig и New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="71c25-627">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="71c25-628">Исправлен пример в документации по Invoke-AzVMRunCommand, в котором теперь используется правильное имя параметра.</span><span class="sxs-lookup"><span data-stu-id="71c25-628">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="71c25-629">Исправлено описание VolumeType в справочной документации по Set-AzVMDiskEncryptionExtension и Set-AzVmssDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="71c25-629">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="71c25-630">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="71c25-630">Az.DataFactory</span></span>
* <span data-ttu-id="71c25-631">Исправлена опечатка в написании Windows со строчной буквы в документации по New-AzDataFactoryEncryptValue.</span><span class="sxs-lookup"><span data-stu-id="71c25-631">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="71c25-632">Пакет SDK ADF для .NET обновлен до версии 4.1.2.</span><span class="sxs-lookup"><span data-stu-id="71c25-632">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="71c25-633">Добавлены параметры DataProxyIntegrationRuntimeName, DataProxyStagingLinkedServiceName и DataProxyStagingPath в командлет Set-AzureRmDataFactoryV2IntegrationRuntime, что позволяет настраивать локальную среду выполнения интеграции в качестве прокси-сервера для Azure-SSIS Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="71c25-633">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="71c25-634">Обновлены PSTriggerRun для отображения активированных конвейеров, сообщений и свойств и PSActivityRun для отображения типа действия.</span><span class="sxs-lookup"><span data-stu-id="71c25-634">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="71c25-635">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="71c25-635">Az.DataLakeStore</span></span>
* <span data-ttu-id="71c25-636">Устранена проблема, при которой Get-DataLakeStoreDeletedItem переставал отвечать на запросы при возникновении ошибок или удаленных исключений.</span><span class="sxs-lookup"><span data-stu-id="71c25-636">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="71c25-637">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="71c25-637">Az.EventHub</span></span>
* <span data-ttu-id="71c25-638">Исправлена проблема № 9658: опечатка в написании параметра VirtualNteworkRule у Set-AzEventHubNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="71c25-638">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="71c25-639">Исправлена проблема № 9558: в Set-AzEventHubNamespace используется PATCH вместо PUT.</span><span class="sxs-lookup"><span data-stu-id="71c25-639">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="71c25-640">В командлет Set-AzEventHubNamespace добавлен параметр EnableKafka.</span><span class="sxs-lookup"><span data-stu-id="71c25-640">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="71c25-641">Исправлена проблема № 9786: не удается создать правило с правами только для прослушивания.</span><span class="sxs-lookup"><span data-stu-id="71c25-641">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="71c25-642">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="71c25-642">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="71c25-643">Исправлено написание Azure со строчной буквы.</span><span class="sxs-lookup"><span data-stu-id="71c25-643">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="71c25-644">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="71c25-644">Az.Monitor</span></span>
* <span data-ttu-id="71c25-645">Исправлены неправильные имена параметров в справочной документации.</span><span class="sxs-lookup"><span data-stu-id="71c25-645">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71c25-646">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71c25-646">Az.Network</span></span>
* <span data-ttu-id="71c25-647">Обновлен New-AzPrivateLinkServiceIpConfig.</span><span class="sxs-lookup"><span data-stu-id="71c25-647">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="71c25-648">Параметр PublicIpAddress объявлен нерекомендуемым, так как он не используется на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="71c25-648">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="71c25-649">Добавлен необязательный параметр Primary, указывающий, является ли текущая IP-конфигурация основной.</span><span class="sxs-lookup"><span data-stu-id="71c25-649">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="71c25-650">Улучшена обработка исключений из-за ошибок запроса от пакета SDK. Устранена проблема, при которой исключения пакета SDK не обрабатывались правильно, из-за чего не отображались основные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="71c25-650">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="71c25-651">Настроена логика проверки для префикса IPv6 IP-адреса для проверки правильности длины префикса IPv6.</span><span class="sxs-lookup"><span data-stu-id="71c25-651">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="71c25-652">Обновлен Get-AzVirtualNetworkSubnetConfig: добавлен набор параметров для получения по идентификатору ресурса подсети.</span><span class="sxs-lookup"><span data-stu-id="71c25-652">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="71c25-653">Обновлено описание параметра Location для AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="71c25-653">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="71c25-654">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="71c25-654">Az.OperationalInsights</span></span>
* <span data-ttu-id="71c25-655">Обновлена документация по New-AzOperationalInsightsLinuxSyslogDataSource.</span><span class="sxs-lookup"><span data-stu-id="71c25-655">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="71c25-656">Добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="71c25-656">Added example</span></span>
    - <span data-ttu-id="71c25-657">Обновлено описание параметра -Name.</span><span class="sxs-lookup"><span data-stu-id="71c25-657">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="71c25-658">Добавлен пример для New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="71c25-658">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="71c25-659">Изменено описание параметра -Name для New-AzOperationalInsightsWindowsEventDataSource.</span><span class="sxs-lookup"><span data-stu-id="71c25-659">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="71c25-660">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="71c25-660">Az.RecoveryServices</span></span>
* <span data-ttu-id="71c25-661">Обновлен Get-AzRecoveryServicesBackupJobDetail.md.</span><span class="sxs-lookup"><span data-stu-id="71c25-661">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="71c25-662">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71c25-662">Az.Resources</span></span>
* <span data-ttu-id="71c25-663">Добавлена поддержка новой версии API 2019-05-10 для Microsoft.Resource.</span><span class="sxs-lookup"><span data-stu-id="71c25-663">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="71c25-664">Добавлена поддержка copy.count = 0 для переменных, ресурсов и свойств.</span><span class="sxs-lookup"><span data-stu-id="71c25-664">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="71c25-665">Ресурсы, у которых condition = false или copy.count = 0, будут удаляться в полном режиме.</span><span class="sxs-lookup"><span data-stu-id="71c25-665">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="71c25-666">В справочную документацию добавлен пример назначения политики на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="71c25-666">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="71c25-667">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="71c25-667">Az.ServiceBus</span></span>
* <span data-ttu-id="71c25-668">Исправлена проблема № 9658: опечатка в написании параметра VirtualNetworkRule В Set-AzServiceBusNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="71c25-668">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="71c25-669">Исправлена проблема № 9786: не удается создать правило с правами только для прослушивания.</span><span class="sxs-lookup"><span data-stu-id="71c25-669">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="71c25-670">Добавлена новая команда Test-AzServiceBusNameAvailability для проверки доступности имени для очереди и раздела.</span><span class="sxs-lookup"><span data-stu-id="71c25-670">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="71c25-671">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="71c25-671">Az.ServiceFabric</span></span>
* <span data-ttu-id="71c25-672">Устранены ошибки командлета для добавления типа узла:</span><span class="sxs-lookup"><span data-stu-id="71c25-672">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="71c25-673">ошибка NullReferenceException, возникавшая, если у группы ресурсов были другие VMSS, не связанные с кластером Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="71c25-673">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="71c25-674">Исправлена проблема https://github.com/Azure/azure-powershell/issues/8681.</span><span class="sxs-lookup"><span data-stu-id="71c25-674">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="71c25-675">Исправлена ошибка, из-за которой командлет завершился сбоем, если virtualNetwork находилась не в той группе ресурсов, к которой относится кластер.</span><span class="sxs-lookup"><span data-stu-id="71c25-675">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="71c25-676">Исправлена проблема https://github.com/Azure/azure-powershell/issues/8407.</span><span class="sxs-lookup"><span data-stu-id="71c25-676">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="71c25-677">Командлет Add-AzServiceFabricApplicationCertificate объявлен нерекомендуемым.</span><span class="sxs-lookup"><span data-stu-id="71c25-677">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="71c25-678">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71c25-678">Az.Sql</span></span>
* <span data-ttu-id="71c25-679">Обновление документации по старым командлетам аудита.</span><span class="sxs-lookup"><span data-stu-id="71c25-679">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="71c25-680">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="71c25-680">Az.Storage</span></span>
* <span data-ttu-id="71c25-681">Обновлена справка по Get/Close-AzStorageFileHandle: в примеры добавлены сценарии использования командлетов и обновлено описание параметров.</span><span class="sxs-lookup"><span data-stu-id="71c25-681">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="71c25-682">Добавлена поддержка StandardBlobTier в операции отправки BLOB-объекта и копирования BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="71c25-682">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="71c25-683">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="71c25-683">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="71c25-684">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="71c25-684">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="71c25-685">Добавлена поддержка приоритета восстановления в операцию копирования BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="71c25-685">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="71c25-686">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="71c25-686">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="71c25-687">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="71c25-687">Az.Websites</span></span>
* <span data-ttu-id="71c25-688">Добавлены уточнение для параметра -AppSettings в Set-AzWebApp и Set-AzWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="71c25-688">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="71c25-689">2.5.0 — июль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="71c25-689">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="71c25-690">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71c25-690">Az.Accounts</span></span>
* <span data-ttu-id="71c25-691">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="71c25-691">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="71c25-692">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="71c25-692">Az.ApplicationInsights</span></span>
* <span data-ttu-id="71c25-693">Исправлена опечатка в примере в документации по Remove-AzApplicationInsightsApiKey.</span><span class="sxs-lookup"><span data-stu-id="71c25-693">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="71c25-694">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="71c25-694">Az.Automation</span></span>
* <span data-ttu-id="71c25-695">Исправлена опечатка в строке ресурса.</span><span class="sxs-lookup"><span data-stu-id="71c25-695">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="71c25-696">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="71c25-696">Az.CognitiveServices</span></span>
* <span data-ttu-id="71c25-697">Добавлена поддержка NetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="71c25-697">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71c25-698">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71c25-698">Az.Compute</span></span>
* <span data-ttu-id="71c25-699">Добавлены недостающие свойства (ComputerName, OsName, OsVersion и HyperVGeneration) для объекта представления экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="71c25-699">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="71c25-700">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="71c25-700">Az.ContainerRegistry</span></span>
* <span data-ttu-id="71c25-701">Исправлена опечатка в Remove-AzContainerRegistryReplication для параметра репликации.</span><span class="sxs-lookup"><span data-stu-id="71c25-701">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="71c25-702">См. подробнее: https://github.com/Azure/azure-powershell/issues/9633.</span><span class="sxs-lookup"><span data-stu-id="71c25-702">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="71c25-703">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="71c25-703">Az.DataFactory</span></span>
* <span data-ttu-id="71c25-704">Пакет SDK для ADF .NET обновлен до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="71c25-704">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="71c25-705">Исправлена опечатка в документации по Get-AzDataFactoryV2PipelineRun.</span><span class="sxs-lookup"><span data-stu-id="71c25-705">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="71c25-706">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="71c25-706">Az.EventHub</span></span>
* <span data-ttu-id="71c25-707">Добавлен новый командлет для создания маркера SAS: New-AzEventHubAuthorizationRuleSASToken.</span><span class="sxs-lookup"><span data-stu-id="71c25-707">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="71c25-708">Добавлена проверка и сообщение об ошибке для случаев, когда для правил авторизации назначаются только права "Управление".</span><span class="sxs-lookup"><span data-stu-id="71c25-708">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="71c25-709">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="71c25-709">Az.KeyVault</span></span>
* <span data-ttu-id="71c25-710">Добавлена поддержка для настройки параметра KeySize в политиках сертификатов.</span><span class="sxs-lookup"><span data-stu-id="71c25-710">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="71c25-711">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="71c25-711">Az.LogicApp</span></span>
* <span data-ttu-id="71c25-712">Get-AzIntegrationAccountMap теперь надлежащим образом выводит все типы сопоставлений.</span><span class="sxs-lookup"><span data-stu-id="71c25-712">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="71c25-713">Добавлен новый параметр MapType для фильтрации.</span><span class="sxs-lookup"><span data-stu-id="71c25-713">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="71c25-714">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="71c25-714">Az.ManagedServices</span></span>
* <span data-ttu-id="71c25-715">Добавлена поддержка API версии 2019-06-01 (общедоступная).</span><span class="sxs-lookup"><span data-stu-id="71c25-715">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71c25-716">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71c25-716">Az.Network</span></span>
* <span data-ttu-id="71c25-717">Добавлена поддержка частной конечной точки и службы приватного канала.</span><span class="sxs-lookup"><span data-stu-id="71c25-717">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="71c25-718">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="71c25-718">New cmdlets</span></span>
        - <span data-ttu-id="71c25-719">Set-AzPrivateEndpoint.</span><span class="sxs-lookup"><span data-stu-id="71c25-719">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="71c25-720">Set-AzPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="71c25-720">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="71c25-721">Approve-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="71c25-721">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="71c25-722">Deny-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="71c25-722">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="71c25-723">Get-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="71c25-723">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="71c25-724">Remove-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="71c25-724">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="71c25-725">Test-AzPrivateLinkServiceVisibility.</span><span class="sxs-lookup"><span data-stu-id="71c25-725">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="71c25-726">Get-AzAutoApprovedPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="71c25-726">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="71c25-727">Обновлены следующие команды для функции: Флаг PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies в подсети в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="71c25-727">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="71c25-728">Обновлены командлеты New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig.</span><span class="sxs-lookup"><span data-stu-id="71c25-728">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="71c25-729">Добавлен необязательный параметр -PrivateEndpointNetworkPoliciesFlag, который определяет, следует ли применять сетевые политики к частной конечной точке в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="71c25-729">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="71c25-730">Добавлен необязательный параметр -PrivateLinkServiceNetworkPoliciesFlag, который определяет, следует ли применять сетевые политики к службе приватного канала в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="71c25-730">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="71c25-731">Параметр ServiceName командлета AzPrivateLinkService был переименован на Name с псевдонимом ServiceName для обеспечения обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="71c25-731">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="71c25-732">Включен протокол ICMP для настройки правил безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="71c25-732">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="71c25-733">Обновлены командлеты</span><span class="sxs-lookup"><span data-stu-id="71c25-733">Updated cmdlets</span></span>
        - <span data-ttu-id="71c25-734">Add-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="71c25-734">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="71c25-735">New-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="71c25-735">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="71c25-736">Set-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="71c25-736">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="71c25-737">Добавлен ConnectionProtocolType (Ikev1/Ikev2) в качестве настраиваемого параметра для командлета New-AzVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="71c25-737">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="71c25-738">Добавлен PrivateIpAddressVersion в LoadBalancerFrontendIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="71c25-738">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="71c25-739">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="71c25-739">Updated cmdlet:</span></span>
        - <span data-ttu-id="71c25-740">New-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="71c25-740">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="71c25-741">Add-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="71c25-741">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="71c25-742">Set-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="71c25-742">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="71c25-743">Команда New-AzApplicationGatewayProbeConfig Шлюза приложений обновлена для поддержки настраиваемого порта в зонде.</span><span class="sxs-lookup"><span data-stu-id="71c25-743">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="71c25-744">Обновлен командлет New-AzApplicationGatewayProbeConfig: добавлен необязательный параметр Port, который используется при проверке внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="71c25-744">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="71c25-745">Этот параметр применяется к номерам SKU Standard_V2 и WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="71c25-745">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="71c25-746">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="71c25-746">Az.OperationalInsights</span></span>
* <span data-ttu-id="71c25-747">Обновленная версия по умолчанию для сохраненных операций поиска имеет значение 1.</span><span class="sxs-lookup"><span data-stu-id="71c25-747">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="71c25-748">Исправлены ошибки при обработке регулярных выражений со значениями NULL в журналах.</span><span class="sxs-lookup"><span data-stu-id="71c25-748">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="71c25-749">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="71c25-749">Az.RecoveryServices</span></span>
* <span data-ttu-id="71c25-750">Обновлен файл Get-AzRecoveryServicesBackupJob.md.</span><span class="sxs-lookup"><span data-stu-id="71c25-750">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="71c25-751">Обновлен файл Get-AzRecoveryServicesBackupContainer.md.</span><span class="sxs-lookup"><span data-stu-id="71c25-751">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="71c25-752">Обновлен файл Get-AzRecoveryServicesVault.md.</span><span class="sxs-lookup"><span data-stu-id="71c25-752">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="71c25-753">Обновлен файл Wait-AzRecoveryServicesBackupJob.md.</span><span class="sxs-lookup"><span data-stu-id="71c25-753">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="71c25-754">Обновлен файл Set-AzRecoveryServicesVaultContext.md.</span><span class="sxs-lookup"><span data-stu-id="71c25-754">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="71c25-755">Обновлен файл Get-AzRecoveryServicesBackupItem.md.</span><span class="sxs-lookup"><span data-stu-id="71c25-755">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="71c25-756">Обновлен файл Get-AzRecoveryServicesBackupRecoveryPoint.md.</span><span class="sxs-lookup"><span data-stu-id="71c25-756">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="71c25-757">Обновлен файл Restore-AzRecoveryServicesBackupItem.md.</span><span class="sxs-lookup"><span data-stu-id="71c25-757">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="71c25-758">Обновлен вызов службы для отмены регистрации контейнера в общей папке Azure.</span><span class="sxs-lookup"><span data-stu-id="71c25-758">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="71c25-759">Обновлен файл Set-AzRecoveryServicesAsrAlertSetting.md.</span><span class="sxs-lookup"><span data-stu-id="71c25-759">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="71c25-760">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71c25-760">Az.Resources</span></span>
- <span data-ttu-id="71c25-761">Удален отсутствующий командлет, который упоминается в документации по New-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="71c25-761">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="71c25-762">Обновлены командлеты политик для использования новой версии API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="71c25-762">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="71c25-763">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="71c25-763">Az.ServiceBus</span></span>
* <span data-ttu-id="71c25-764">Добавлен новый командлет для создания маркера SAS: New-AzServiceBusAuthorizationRuleSASToken.</span><span class="sxs-lookup"><span data-stu-id="71c25-764">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="71c25-765">Добавлена проверка и сообщение об ошибке в ситуациях, когда для правил авторизации назначаются только права "Управление".</span><span class="sxs-lookup"><span data-stu-id="71c25-765">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="71c25-766">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71c25-766">Az.Sql</span></span>
* <span data-ttu-id="71c25-767">Исправлены отсутствующие примеры для командлета Set-AzSqlDatabaseSecondary.</span><span class="sxs-lookup"><span data-stu-id="71c25-767">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="71c25-768">Исправлены заданные повторяющиеся проверки для оценки наличия уязвимостей без указания адресов электронной почты.</span><span class="sxs-lookup"><span data-stu-id="71c25-768">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="71c25-769">Исправлена незначительная опечатка в сообщении предупреждения.</span><span class="sxs-lookup"><span data-stu-id="71c25-769">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="71c25-770">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="71c25-770">Az.Storage</span></span>
* <span data-ttu-id="71c25-771">Обновлен пример в справочной документации для использования командлетом Get-AzStorageAccount правильного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="71c25-771">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="71c25-772">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="71c25-772">Az.StorageSync</span></span>
* <span data-ttu-id="71c25-773">Добавлен командлет Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="71c25-773">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="71c25-774">Исправлена проблема № 9551, связанная с TierFilesOlderThanDays.</span><span class="sxs-lookup"><span data-stu-id="71c25-774">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="71c25-775">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="71c25-775">Az.Websites</span></span>
* <span data-ttu-id="71c25-776">Исправлена ошибка, при которой некоторые свойства SiteConfig не возвращались Get-AzWebApp и Set-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="71c25-776">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="71c25-777">Добавлен новый параметр Location в Get-AzDeletedWebApp и Restore-AzDeletedWebApp.</span><span class="sxs-lookup"><span data-stu-id="71c25-777">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="71c25-778">Исправлена ошибка, которая возникала при клонировании слотов веб-приложений с помощью командлета New-AzWebApp-IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="71c25-778">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="71c25-779">2.4.0 — июль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="71c25-779">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="71c25-780">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71c25-780">Az.Accounts</span></span>
* <span data-ttu-id="71c25-781">Добавлена поддержка командлетов профиля.</span><span class="sxs-lookup"><span data-stu-id="71c25-781">Add support for profile cmdlets</span></span>
* <span data-ttu-id="71c25-782">Добавлена поддержка сред и плоскостей данных в созданных командлетах.</span><span class="sxs-lookup"><span data-stu-id="71c25-782">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="71c25-783">Исправлена ошибка, когда в командлетах плоскости данных в Windows PowerShell в некоторых случаях использовалась неправильная конечная точка.</span><span class="sxs-lookup"><span data-stu-id="71c25-783">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="71c25-784">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="71c25-784">Az.Advisor</span></span>
* <span data-ttu-id="71c25-785">Выпущена общедоступная версия Az.Advisor.</span><span class="sxs-lookup"><span data-stu-id="71c25-785">GA release of Az.Advisor</span></span>
* <span data-ttu-id="71c25-786">Теперь этот модуль входит в сводный модуль `Az`.</span><span class="sxs-lookup"><span data-stu-id="71c25-786">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="71c25-787">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="71c25-787">Az.ApiManagement</span></span>
* <span data-ttu-id="71c25-788">исправлена проблема https://github.com/Azure/azure-powershell/issues/8671.</span><span class="sxs-lookup"><span data-stu-id="71c25-788">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="71c25-789">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="71c25-789">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="71c25-790">Добавлена поддержка запрашивания подписок по пользователю и продукту.</span><span class="sxs-lookup"><span data-stu-id="71c25-790">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="71c25-791">Добавлена поддержка создания запросов с использованием области "/", "/apis", "/apis/echo-api".</span><span class="sxs-lookup"><span data-stu-id="71c25-791">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="71c25-792">Исправлены проблемы https://github.com/Azure/azure-powershell/issues/9307 и https://github.com/Azure/azure-powershell/issues/8432.</span><span class="sxs-lookup"><span data-stu-id="71c25-792">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="71c25-793">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="71c25-793">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="71c25-794">Добавлена поддержка указания ApiVersion и ApiVersionSetId при импорте API-интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="71c25-794">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="71c25-795">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="71c25-795">Az.Automation</span></span>
* <span data-ttu-id="71c25-796">Исправлена ошибка командлета Set-AzAutomationConnectionFieldValue при обработке строкового значения.</span><span class="sxs-lookup"><span data-stu-id="71c25-796">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71c25-797">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71c25-797">Az.Compute</span></span>
* <span data-ttu-id="71c25-798">В New AzImageConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="71c25-798">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="71c25-799">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="71c25-799">Az.DataFactory</span></span>
* <span data-ttu-id="71c25-800">Обновление выходных данных командлетов ADF, предназначенных для получения числа выполнений действий, конвейеров и триггеров, для поддержки канала Select-Object.</span><span class="sxs-lookup"><span data-stu-id="71c25-800">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="71c25-801">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="71c25-801">Az.EventGrid</span></span>
* <span data-ttu-id="71c25-802">Исправлена опечатка в документации по командлету New-AzEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="71c25-802">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="71c25-803">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="71c25-803">Az.IotHub</span></span>
* <span data-ttu-id="71c25-804">Добавлена поддержка повторного создания ключей политики авторизации.</span><span class="sxs-lookup"><span data-stu-id="71c25-804">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71c25-805">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71c25-805">Az.Network</span></span>
* <span data-ttu-id="71c25-806">К тегам общедоступного IP-адреса добавлен тег RoutingPreference.</span><span class="sxs-lookup"><span data-stu-id="71c25-806">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="71c25-807">Улучшены примеры для справочной документации по командлету Get-AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="71c25-807">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="71c25-808">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="71c25-808">Az.PolicyInsights</span></span>
* <span data-ttu-id="71c25-809">Исправлена проблема с пустой ссылкой в командлете Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="71c25-809">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="71c25-810">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/9446.</span><span class="sxs-lookup"><span data-stu-id="71c25-810">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="71c25-811">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="71c25-811">Az.OperationalInsights</span></span>
* <span data-ttu-id="71c25-812">Исправленная модель источника данных CustomLog возвращена в командлет Get-AzOperationalInsightsDataSource.</span><span class="sxs-lookup"><span data-stu-id="71c25-812">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="71c25-813">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="71c25-813">Az.RecoveryServices</span></span>
* <span data-ttu-id="71c25-814">Выпущено исправление для команды get-policy для виртуальных машин IaaS.</span><span class="sxs-lookup"><span data-stu-id="71c25-814">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="71c25-815">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71c25-815">Az.Resources</span></span>
    - <span data-ttu-id="71c25-816">Исправлен текст справки по параметру Get-AzPolicyState -Top.</span><span class="sxs-lookup"><span data-stu-id="71c25-816">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="71c25-817">Добавлена поддержка разбиения по страницам на стороне клиента для Get-AzPolicyAlias.</span><span class="sxs-lookup"><span data-stu-id="71c25-817">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="71c25-818">Добавлены новые параметры для Set-AzPolicyAssignment, -PolicyParameters и -PolicyParametersObject.</span><span class="sxs-lookup"><span data-stu-id="71c25-818">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="71c25-819">Добавлен ряд обновлений документов и примеров для командлетов политик.</span><span class="sxs-lookup"><span data-stu-id="71c25-819">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="71c25-820">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="71c25-820">Az.ServiceBus</span></span>
* <span data-ttu-id="71c25-821">Исправление ошибки № 4938: командлет New-AzureRmServiceBusQueue возвращает ответ BadRequest (Недопустимый запрос) при задании значения MaxSizeInMegabytes.</span><span class="sxs-lookup"><span data-stu-id="71c25-821">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="71c25-822">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71c25-822">Az.Sql</span></span>
* <span data-ttu-id="71c25-823">Из выпуска предварительной версии в выпуск общедоступной версии добавлены командлеты группы отработки отказа экземпляра.</span><span class="sxs-lookup"><span data-stu-id="71c25-823">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="71c25-824">Поддержка аудита Azure SQL Server и баз данных с помощью новых командлетов:</span><span class="sxs-lookup"><span data-stu-id="71c25-824">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="71c25-825">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="71c25-825">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="71c25-826">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="71c25-826">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="71c25-827">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="71c25-827">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="71c25-828">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="71c25-828">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="71c25-829">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="71c25-829">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="71c25-830">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="71c25-830">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="71c25-831">Из параметров оценки уязвимостей удалены ограничения, касающиеся электронной почты.</span><span class="sxs-lookup"><span data-stu-id="71c25-831">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="71c25-832">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="71c25-832">Az.Storage</span></span>
* <span data-ttu-id="71c25-833">Два параметра в указанном ниже командлете — -IndexDocument и -ErrorDocument404Path, — которые ранее были обязательными, стали необязательными:</span><span class="sxs-lookup"><span data-stu-id="71c25-833">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="71c25-834">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="71c25-834">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="71c25-835">Обновлена справка по командлету Get-AzStorageBlobContent: добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="71c25-835">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="71c25-836">При сбое выполнения командлета с ошибкой StorageException отображаются дополнительные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="71c25-836">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="71c25-837">Добавлена поддержка создания или обновления учетной записи хранения с использованием проверки подлинности AAD DS для службы "Файлы Azure".</span><span class="sxs-lookup"><span data-stu-id="71c25-837">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="71c25-838">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="71c25-838">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="71c25-839">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="71c25-839">Set-AzStorageAccount</span></span>
* <span data-ttu-id="71c25-840">Добавлена поддержка перечисления или закрытия дескрипторов файлов для общей папки, каталога файлов или файла:</span><span class="sxs-lookup"><span data-stu-id="71c25-840">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="71c25-841">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="71c25-841">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="71c25-842">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="71c25-842">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="71c25-843">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="71c25-843">Az.StorageSync</span></span>
* <span data-ttu-id="71c25-844">Теперь этот модуль входит в сводный модуль `Az`.</span><span class="sxs-lookup"><span data-stu-id="71c25-844">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="71c25-845">2.3.2 — июнь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="71c25-845">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="71c25-846">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71c25-846">Az.Accounts</span></span>
* <span data-ttu-id="71c25-847">Исправлена ошибка, связанная с использованием неправильного URL-адреса для вызовов функций.</span><span class="sxs-lookup"><span data-stu-id="71c25-847">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="71c25-848">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8983.</span><span class="sxs-lookup"><span data-stu-id="71c25-848">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="71c25-849">Устранена проблема с псевдонимами из AzureRM для командлетов Az.</span><span class="sxs-lookup"><span data-stu-id="71c25-849">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="71c25-850">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="71c25-850">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="71c25-851">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest.</span><span class="sxs-lookup"><span data-stu-id="71c25-851">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71c25-852">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71c25-852">Az.Compute</span></span>
* <span data-ttu-id="71c25-853">Простые наборы параметров New-AzVm и New-AzVmss теперь принимают параметр ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="71c25-853">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="71c25-854">Исправлена опечатка в справочной документации по New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="71c25-854">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="71c25-855">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="71c25-855">Az.Dns</span></span>
* <span data-ttu-id="71c25-856">Исправлена опечатка в справочных примерах по использованию Set-AzDnsZone.</span><span class="sxs-lookup"><span data-stu-id="71c25-856">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="71c25-857">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="71c25-857">Az.EventGrid</span></span>
* <span data-ttu-id="71c25-858">Обновлен для использования API версии 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="71c25-858">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="71c25-859">Новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="71c25-859">New cmdlets:</span></span>
    - <span data-ttu-id="71c25-860">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="71c25-860">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="71c25-861">Создает домен Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="71c25-861">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="71c25-862">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="71c25-862">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="71c25-863">Возвращает сведения о домене Сетки событий или список всех доменов Сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="71c25-863">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="71c25-864">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="71c25-864">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="71c25-865">Удаляет домен Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="71c25-865">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="71c25-866">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="71c25-866">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="71c25-867">Повторно создает ключ общего доступа для домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="71c25-867">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="71c25-868">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="71c25-868">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="71c25-869">Возвращает ключи общего доступа, используемые для публикации событий в домене Сетки событий.</span><span class="sxs-lookup"><span data-stu-id="71c25-869">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="71c25-870">New-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="71c25-870">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="71c25-871">Создает раздел домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="71c25-871">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="71c25-872">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="71c25-872">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="71c25-873">Возвращает сведения о разделе домена Сетки событий или список всех разделов определенного домена Сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="71c25-873">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="71c25-874">Remove-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="71c25-874">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="71c25-875">Удаляет раздел домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="71c25-875">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="71c25-876">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="71c25-876">Updated cmdlets:</span></span>
    - <span data-ttu-id="71c25-877">New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="71c25-877">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="71c25-878">Добавляют новые обязательные параметры, обеспечивающие поддержку передачи по конвейеру для нового домена Сетки событий и раздела домена Сетки событий и позволяющие создавать подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="71c25-878">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="71c25-879">Добавляют новые обязательные параметры для указания имени нового домена Сетки событий и (или) имени раздела домена Сетки событий и позволяют создавать подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="71c25-879">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="71c25-880">Добавляют новые наборы параметров для доменов и разделов домена и позволяют повторно использовать существующие параметры (например, EndPointType, SubjectBeginsWith и т. д.).</span><span class="sxs-lookup"><span data-stu-id="71c25-880">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="71c25-881">Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="71c25-881">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="71c25-882">срока действия подписки на событие;</span><span class="sxs-lookup"><span data-stu-id="71c25-882">Event subscription expiration date,</span></span>
            - <span data-ttu-id="71c25-883">параметров расширенной фильтрации.</span><span class="sxs-lookup"><span data-stu-id="71c25-883">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="71c25-884">Добавляют новое перечисление для ServiceBusQueue в качестве места назначения.</span><span class="sxs-lookup"><span data-stu-id="71c25-884">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="71c25-885">Запрещают использование значение All в параметре -IncludedEventType и заменяют его следующим:</span><span class="sxs-lookup"><span data-stu-id="71c25-885">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="71c25-886">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="71c25-886">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="71c25-887">Добавляют новые необязательные параметры (Top, ODataQuery и NextLink) для поддержки разбиения на страницы и фильтрации результатов.</span><span class="sxs-lookup"><span data-stu-id="71c25-887">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="71c25-888">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="71c25-888">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="71c25-889">Добавляют новые обязательные параметры, обеспечивающие поддержку передачи по конвейеру для домена Сетки событий и раздела домена Сетки событий и позволяющие удалять подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="71c25-889">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="71c25-890">Добавляют новые обязательные параметры для указания имени домена Сетки событий и (или) имени раздела домена Сетки событий и позволяют удалять подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="71c25-890">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="71c25-891">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="71c25-891">Az.FrontDoor</span></span>
* <span data-ttu-id="71c25-892">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="71c25-892">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="71c25-893">Добавляет поддержку преобразований и новое значение оператора автозавершения (RegEx).</span><span class="sxs-lookup"><span data-stu-id="71c25-893">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="71c25-894">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="71c25-894">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="71c25-895">Добавляет новые значения автозавершения.</span><span class="sxs-lookup"><span data-stu-id="71c25-895">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71c25-896">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71c25-896">Az.Network</span></span>
* <span data-ttu-id="71c25-897">Добавляет поддержку ресурса шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="71c25-897">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="71c25-898">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="71c25-898">New cmdlets</span></span>
        - <span data-ttu-id="71c25-899">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="71c25-899">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="71c25-900">Добавляет AvailablePrivateEndpointType.</span><span class="sxs-lookup"><span data-stu-id="71c25-900">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="71c25-901">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="71c25-901">New cmdlets</span></span> 
        - <span data-ttu-id="71c25-902">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="71c25-902">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="71c25-903">Добавляет PrivatePrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="71c25-903">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="71c25-904">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="71c25-904">New cmdlets</span></span> 
        - <span data-ttu-id="71c25-905">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="71c25-905">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="71c25-906">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="71c25-906">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="71c25-907">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="71c25-907">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="71c25-908">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="71c25-908">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="71c25-909">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="71c25-909">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="71c25-910">Добавляет PrivateEndpoint.</span><span class="sxs-lookup"><span data-stu-id="71c25-910">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="71c25-911">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="71c25-911">New cmdlets</span></span>
        - <span data-ttu-id="71c25-912">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="71c25-912">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="71c25-913">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="71c25-913">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="71c25-914">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="71c25-914">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="71c25-915">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="71c25-915">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="71c25-916">Обновлены следующие команды для функции: флаг UseLocalAzureIpAddress для VPN-подключения.</span><span class="sxs-lookup"><span data-stu-id="71c25-916">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="71c25-917">Обновлен командлет New-AzVpnConnection. Добавлен необязательный параметр -UseLocalAzureIpAddress для указания того, что локальный IP-адрес Azure следует использовать в качестве исходного адреса при инициации подключения.</span><span class="sxs-lookup"><span data-stu-id="71c25-917">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="71c25-918">Обновлен командлет Set-AzVpnConnection. Добавлен необязательный параметр -UseLocalAzureIpAddress для указания того, что локальный IP-адрес Azure следует использовать в качестве исходного адреса при инициации подключения.</span><span class="sxs-lookup"><span data-stu-id="71c25-918">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="71c25-919">В пиринг ExpressRoute добавлено поле только для чтения PeeredConnections.</span><span class="sxs-lookup"><span data-stu-id="71c25-919">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="71c25-920">В ExpressRoute добавлено поле только для чтения GlobalReachEnabled.</span><span class="sxs-lookup"><span data-stu-id="71c25-920">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="71c25-921">Добавлен атрибут в рамках критического изменения, отменяющего статус устаревшего поля AllowGlobalReach в модели ExpressRouteCircuit.</span><span class="sxs-lookup"><span data-stu-id="71c25-921">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="71c25-922">Исправлена проблема, связанная с ошибкой 8756, при использовании TargetListenerID с командлетами AzApplicationGatewayRedirectConfiguration.</span><span class="sxs-lookup"><span data-stu-id="71c25-922">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="71c25-923">Исправлена ошибка в New-AzApplicationGatewayPathRuleConfig, не позволявшая задавать набор правил повторного создания.</span><span class="sxs-lookup"><span data-stu-id="71c25-923">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="71c25-924">Исправлено отображение VirtualNetworkTaps в NetworkInterfaceIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="71c25-924">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="71c25-925">Исправлены командлеты Cortex Get для отображения всех частей.</span><span class="sxs-lookup"><span data-stu-id="71c25-925">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="71c25-926">Исправлено создание ссылок VirtualHub для ExpressRouteGateways и VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="71c25-926">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="71c25-927">В AzureFirewall и NatGateway добавлена поддержка Зон доступности.</span><span class="sxs-lookup"><span data-stu-id="71c25-927">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="71c25-928">Добавлен командлет Get-AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="71c25-928">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="71c25-929">Добавлена поддержка нескольких общедоступных IP-адресов для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="71c25-929">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="71c25-930">Обновлен командлет New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="71c25-930">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="71c25-931">Добавлен параметр -PublicIpAddress, который принимает один или несколько объектов общедоступных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="71c25-931">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="71c25-932">Добавлен параметр -VirtualNetwork, который принимает объект виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="71c25-932">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="71c25-933">Добавлены методы AddPublicIpAddress и RemovePublicIpAddress для объекта брандмауэра. Они принимают объект общедоступного IP-адреса в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="71c25-933">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="71c25-934">Не рекомендуется использовать параметры -PublicIpName и -VirtualNetworkName.</span><span class="sxs-lookup"><span data-stu-id="71c25-934">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="71c25-935">Обновлены следующие команды для функции: В параметрах проверки подлинности AAD VPN-клиента задан ресурс шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="71c25-935">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="71c25-936">Обновлен командлет New-AzVirtualNetworkGateway: Добавлены необязательные параметры AadTenantUri, AadAudienceId, AadIssuerUri для возможности задавать в шлюзе параметры проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="71c25-936">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="71c25-937">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлены необязательные параметры AadTenantUri, AadAudienceId, AadIssuerUri для возможности задавать в шлюзе параметры проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="71c25-937">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="71c25-938">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлен необязательный параметр-переключатель RemoveAadAuthentication для удаления в шлюзе параметров проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="71c25-938">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="71c25-939">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="71c25-939">Az.OperationalInsights</span></span>
* <span data-ttu-id="71c25-940">Добавлена поддержка SKU **pergb2018** в команде New-AzureRmOperationalInsightsWorkspace.</span><span class="sxs-lookup"><span data-stu-id="71c25-940">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="71c25-941">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71c25-941">Az.Resources</span></span>
* <span data-ttu-id="71c25-942">Поддержка дополнительных вариантов экспорта шаблона.</span><span class="sxs-lookup"><span data-stu-id="71c25-942">Support for additional Template Export options</span></span>
    - <span data-ttu-id="71c25-943">В Export-AzResourceGroup добавлен параметр -SkipResourceNameParameterization.</span><span class="sxs-lookup"><span data-stu-id="71c25-943">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="71c25-944">В Export-AzResourceGroup добавлен параметр -SkipAllParameterization.</span><span class="sxs-lookup"><span data-stu-id="71c25-944">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="71c25-945">В Export-AzResourceGroup добавлен параметр -Resource для фильтрации экспортированных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="71c25-945">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="71c25-946">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="71c25-946">Az.ServiceFabric</span></span>
* <span data-ttu-id="71c25-947">Исправлена ошибка, связанная с получением иногда неправильных отпечатков при добавлении сертификата ByExistingKeyVault.</span><span class="sxs-lookup"><span data-stu-id="71c25-947">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="71c25-948">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71c25-948">Az.Sql</span></span>
* <span data-ttu-id="71c25-949">Исправлен суффикс конечной точки хранилища службы "Расширенная защита от угроз Azure".</span><span class="sxs-lookup"><span data-stu-id="71c25-949">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="71c25-950">Исправлена ошибка, связанная с возможностью пакета "Расширенная защита данных" переопределять политику службы "Расширенная защита от угроз".</span><span class="sxs-lookup"><span data-stu-id="71c25-950">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="71c25-951">Новые командлеты для Management.Sql позволяют клиентам добавлять ключи TDE и задавать средство защиты TDE для управляемых экземпляров.</span><span class="sxs-lookup"><span data-stu-id="71c25-951">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="71c25-952">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="71c25-952">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="71c25-953">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="71c25-953">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="71c25-954">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="71c25-954">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="71c25-955">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="71c25-955">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="71c25-956">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="71c25-956">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="71c25-957">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="71c25-957">Az.Storage</span></span>
* <span data-ttu-id="71c25-958">Поддержка класса Kind в FileStorage и значения Premium_ZRS в SkuName при создании учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="71c25-958">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="71c25-959">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="71c25-959">New-AzStorageAccount</span></span>
* <span data-ttu-id="71c25-960">Уточнено описание командлета неизменности BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="71c25-960">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="71c25-961">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="71c25-961">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="71c25-962">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="71c25-962">Az.Websites</span></span>
* <span data-ttu-id="71c25-963">Оптимизирует Get-AzWebAppCertificate для фильтрации по группе ресурсов на сервере, а не в клиенте.</span><span class="sxs-lookup"><span data-stu-id="71c25-963">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="71c25-964">Добавляет параметр-переключатель - UseDisasterRecovery в Get AzWebAppSnapshot.</span><span class="sxs-lookup"><span data-stu-id="71c25-964">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="71c25-965">2.2.0 — июнь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="71c25-965">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="71c25-966">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="71c25-966">Az.Cdn</span></span>
* <span data-ttu-id="71c25-967">Обновлены командлеты для поддержки функции rulesEngine на основе API версии 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="71c25-967">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71c25-968">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71c25-968">Az.Compute</span></span>
* <span data-ttu-id="71c25-969">Добавлен параметр `NoWait`, который запускает операцию и немедленно возвращает значение еще до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="71c25-969">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="71c25-970">Обновлены командлеты:   Export-AzLogAnalyticRequestRateByInterval; Export-AzLogAnalyticThrottledRequest; Remove-AzVM; Remove-AzVMAccessExtension; Remove-AzVMAEMExtension; Remove-AzVMChefExtension; Remove-AzVMCustomScriptExtension; Remove-AzVMDiagnosticsExtension; Remove-AzVMDiskEncryptionExtension; Remove-AzVMDscExtension; Remove-AzVMSqlServerExtension; Restart-AzVM; Set-AzVM; Set-AzVMAccessExtension; Set-AzVMADDomainExtension; Set-AzVMAEMExtension; Set-AzVMBginfoExtension; Set-AzVMChefExtension; Set-AzVMCustomScriptExtension; Set-AzVMDiagnosticsExtension; Set-AzVMDscExtension; Set-AzVMExtension; Start-AzVM; Stop-AzVM; Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="71c25-970">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="71c25-971">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="71c25-971">Az.EventHub</span></span>
* <span data-ttu-id="71c25-972">Исправлена ошибка № 9231. Командлет Get-AzEventHubNamespace не возвращал теги.</span><span class="sxs-lookup"><span data-stu-id="71c25-972">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="71c25-973">Исправлена ошибка № 9230. Командлет Get-AzEventHubNamespace возвращал значение ResourceGroup вместо ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="71c25-973">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71c25-974">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71c25-974">Az.Network</span></span>
* <span data-ttu-id="71c25-975">Обновлены параметры ResourceId и InputObject для ресурса Шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="71c25-975">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="71c25-976">Добавлены псевдонимы для параметров ResourceId и InputObject.</span><span class="sxs-lookup"><span data-stu-id="71c25-976">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="71c25-977">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="71c25-977">Az.PolicyInsights</span></span>
* <span data-ttu-id="71c25-978">Исправлена проблема с пустой ссылкой в командлете Get-AzPolicyEvent.</span><span class="sxs-lookup"><span data-stu-id="71c25-978">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="71c25-979">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="71c25-979">Az.RecoveryServices</span></span>
* <span data-ttu-id="71c25-980">Минимальный срок хранения политики IaaSVM изменился с 1 до 7 дней.</span><span class="sxs-lookup"><span data-stu-id="71c25-980">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="71c25-981">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="71c25-981">Az.ServiceBus</span></span>
* <span data-ttu-id="71c25-982">Исправлена ошибка № 9182. Командлет Get-AzServiceBusNamespace возвращал ResourceGroup вместо ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="71c25-982">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="71c25-983">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="71c25-983">Az.ServiceFabric</span></span>
* <span data-ttu-id="71c25-984">Исправлена опечатка в сообщении об ошибке для командлета Update-AzServiceFabricReliability.</span><span class="sxs-lookup"><span data-stu-id="71c25-984">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="71c25-985">Исправлен отсутствующей символ в командных строках Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="71c25-985">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="71c25-986">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71c25-986">Az.Sql</span></span>
* <span data-ttu-id="71c25-987">Для командлета New-AzureSqlInstance добавлен параметр DnsZonePartner, обеспечивающий поддержку AutoDr для Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="71c25-987">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="71c25-988">Командлет Get-AzSqlDatabaseSecureConnectionPolicy объявлен неподдерживаемым.</span><span class="sxs-lookup"><span data-stu-id="71c25-988">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="71c25-989">Командлеты обнаружения угроз переименованы в командлеты Расширенной защиты от угроз.</span><span class="sxs-lookup"><span data-stu-id="71c25-989">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="71c25-990">Параметры -StorageSizeInGB и -LicenseType командлета New-AzSqlInstance теперь необязательны.</span><span class="sxs-lookup"><span data-stu-id="71c25-990">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="71c25-991">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="71c25-991">Az.Websites</span></span>
* <span data-ttu-id="71c25-992">Исправлены проблемы, когда удалялись теги при использовании Set-AzWebApp и Set-AzWebAppSlot со свойством -WebApp.</span><span class="sxs-lookup"><span data-stu-id="71c25-992">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="71c25-993">2.1.0 — май 2019 г.</span><span class="sxs-lookup"><span data-stu-id="71c25-993">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="71c25-994">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="71c25-994">Az.ApiManagement</span></span>
* <span data-ttu-id="71c25-995">Созданы командлеты для управления диагностикой в глобальной области и в области API.</span><span class="sxs-lookup"><span data-stu-id="71c25-995">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="71c25-996">**Get-AzApiManagementDiagnostic** — получение диагностики, заданной глобально или на уровне области API.</span><span class="sxs-lookup"><span data-stu-id="71c25-996">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="71c25-997">**New-AzApiManagementDiagnostic** — создание диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="71c25-997">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="71c25-998">**New-AzApiManagementHttpMessageDiagnostic** — создание параметра диагностики, для которого регистрируются заголовки и размер байтов тела.</span><span class="sxs-lookup"><span data-stu-id="71c25-998">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="71c25-999">**New-AzApiManagementPipelineDiagnosticSetting** — создание параметров диагностики для сообщений HTTP, поступающих в шлюз или исходящих из него.</span><span class="sxs-lookup"><span data-stu-id="71c25-999">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="71c25-1000">**New-AzApiManagementSamplingSetting** — создание параметра выборки для запросов и ответов касательно диагностики.</span><span class="sxs-lookup"><span data-stu-id="71c25-1000">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="71c25-1001">**Remove-AzApiManagementDiagnostic** — удаление объекта диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="71c25-1001">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="71c25-1002">**Set-AzApiManagementDiagnostic** — обновление объекта диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="71c25-1002">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="71c25-1003">Созданы командлеты для управления кэшем в службе ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="71c25-1003">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="71c25-1004">**Get-AzApiManagementCache** — получение сведений о кэше, указанном идентификатором, или обо всех кэшах.</span><span class="sxs-lookup"><span data-stu-id="71c25-1004">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="71c25-1005">**New-AzApiManagementCache** — создание кэша по умолчанию или кэша в определенном регионе Azure.</span><span class="sxs-lookup"><span data-stu-id="71c25-1005">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="71c25-1006">**Remove-AzApiManagementCache** — удаление кэша.</span><span class="sxs-lookup"><span data-stu-id="71c25-1006">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="71c25-1007">**Update-AzApiManagementCache** — обновление кэша.</span><span class="sxs-lookup"><span data-stu-id="71c25-1007">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="71c25-1008">Созданы командлеты для управления схемой API.</span><span class="sxs-lookup"><span data-stu-id="71c25-1008">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="71c25-1009">**New-AzApiManagementSchema** — создание схемы для API.</span><span class="sxs-lookup"><span data-stu-id="71c25-1009">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="71c25-1010">**Get-AzApiManagementSchema** — получение схем, настроенных в API.</span><span class="sxs-lookup"><span data-stu-id="71c25-1010">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="71c25-1011">**Remove-AzApiManagementSchema** — удаление схемы, настроенной в API.</span><span class="sxs-lookup"><span data-stu-id="71c25-1011">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="71c25-1012">**Set-AzApiManagementSchema** — обновление схемы, настроенной в API.</span><span class="sxs-lookup"><span data-stu-id="71c25-1012">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="71c25-1013">Создан командлет для создания токена пользователя.</span><span class="sxs-lookup"><span data-stu-id="71c25-1013">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="71c25-1014">**New-AzApiManagementUserToken** — создание токена пользователя, по умолчанию действительного в течение 8 часов. С помощью этого командлета можно создавать токен для пользователя GIT.</span><span class="sxs-lookup"><span data-stu-id="71c25-1014">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="71c25-1015">Создан командлет для получения состояния сети.</span><span class="sxs-lookup"><span data-stu-id="71c25-1015">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="71c25-1016">**Get-AzApiManagementNetworkStatus** — получение состояния сети ресурсов, от которых зависит служба "Управление API".</span><span class="sxs-lookup"><span data-stu-id="71c25-1016">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="71c25-1017">Это полезно при развертывании службы ApiManagement в виртуальной сети и проверке того, не нарушена ли какая-либо из зависимостей.</span><span class="sxs-lookup"><span data-stu-id="71c25-1017">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="71c25-1018">Обновлен командлет **New-AzApiManagement** для управления службой ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="71c25-1018">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="71c25-1019">Добавлена поддержка нового SKU Consumption.</span><span class="sxs-lookup"><span data-stu-id="71c25-1019">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="71c25-1020">Добавлена поддержка для включения флага EnableClientCertificate в SKU Consumption.</span><span class="sxs-lookup"><span data-stu-id="71c25-1020">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="71c25-1021">Новый командлет **New-AzApiManagementSslSetting** позволяет настраивать параметр TLS/SSL для сервера (Backend) и внешнего интерфейса (Frontend).</span><span class="sxs-lookup"><span data-stu-id="71c25-1021">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="71c25-1022">Его также можно использовать для настройки Ciphers как 3DES, в ServerProtocols как Http2 для внешнего интерфейса (Frontend) службы ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="71c25-1022">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="71c25-1023">Добавлена поддержка настройки имени узла DeveloperPortal в службе ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="71c25-1023">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="71c25-1024">Обновлен командлет **Get-AzApiManagementSsoToken** для извлечения объекта PsApiManagement в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="71c25-1024">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="71c25-1025">Обновлен командлет для отображения встроенных сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="71c25-1025">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="71c25-1026">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Код ошибки: ValidationError. Сообщение об ошибке: "Некоторые поля содержат неправильные значения". Сведения об ошибке: [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="71c25-1026">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="71c25-1027">Обновлен командлет **Export-AzApiManagementApi** для экспортирования программных интерфейсов в формате OpenApi 3.0.</span><span class="sxs-lookup"><span data-stu-id="71c25-1027">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="71c25-1028">Обновлен командлет **Import-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="71c25-1028">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="71c25-1029">Для импортирования API из спецификации документа OpenApi 3.0.</span><span class="sxs-lookup"><span data-stu-id="71c25-1029">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="71c25-1030">Для переопределения свойства PsApiManagementSchema, указанного в любом документе (Swagger, Wadl, Wsdl, OpenApi).</span><span class="sxs-lookup"><span data-stu-id="71c25-1030">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="71c25-1031">Для переопределения свойства ServiceUrl, указанного в любом документе.</span><span class="sxs-lookup"><span data-stu-id="71c25-1031">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="71c25-1032">Обновлен командлет **Get-AzApiManagementPolicy** для возврата политики в формате, экранированном не для XML, с использованием rawxml.</span><span class="sxs-lookup"><span data-stu-id="71c25-1032">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="71c25-1033">Обновлен командлет **Set-AzApiManagementPolicy**. Он принимает политику в формате, экранированном не для XML, с использованием rawxml и в формате, экранированном для XML, с использованием XML.</span><span class="sxs-lookup"><span data-stu-id="71c25-1033">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="71c25-1034">Обновлен командлет **New-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="71c25-1034">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="71c25-1035">Для настройки API с помощью сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="71c25-1035">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="71c25-1036">Для создания API в ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="71c25-1036">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="71c25-1037">Для клонирования API с использованием значений SourceApiId и SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="71c25-1037">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="71c25-1038">Возможность настройки параметра SubscriptionRequired в области API.</span><span class="sxs-lookup"><span data-stu-id="71c25-1038">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="71c25-1039">Обновлен командлет **Set-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="71c25-1039">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="71c25-1040">Для настройки API с помощью сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="71c25-1040">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="71c25-1041">Для обновления API в ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="71c25-1041">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="71c25-1042">Возможность настройки параметра SubscriptionRequired в области API.</span><span class="sxs-lookup"><span data-stu-id="71c25-1042">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="71c25-1043">Обновлен командлет **New-AzApiManagementRevision**:</span><span class="sxs-lookup"><span data-stu-id="71c25-1043">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="71c25-1044">Для клонирования (копирования тегов, продуктов, операций и политик) существующей редакции с использованием SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="71c25-1044">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="71c25-1045">Новая редакция предполагает родительский идентификатор ApiId.</span><span class="sxs-lookup"><span data-stu-id="71c25-1045">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="71c25-1046">Для предоставления ApiRevisionDescription.</span><span class="sxs-lookup"><span data-stu-id="71c25-1046">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="71c25-1047">Для переопределения значения ServiceUrl при клонировании API.</span><span class="sxs-lookup"><span data-stu-id="71c25-1047">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="71c25-1048">Обновлен командлет **New-AzApiManagementIdentityProvider**:</span><span class="sxs-lookup"><span data-stu-id="71c25-1048">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="71c25-1049">Для настройки AAD или AADB2C с Authority.</span><span class="sxs-lookup"><span data-stu-id="71c25-1049">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="71c25-1050">Для установки политик SignupPolicy, SigninPolicy, ProfileEditingPolicy и PasswordResetPolicy.</span><span class="sxs-lookup"><span data-stu-id="71c25-1050">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="71c25-1051">Обновлен командлет **New-AzApiManagementSubscription**.</span><span class="sxs-lookup"><span data-stu-id="71c25-1051">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="71c25-1052">Для учета новой модели SubscriptonModel с помощью Scope и UserId.</span><span class="sxs-lookup"><span data-stu-id="71c25-1052">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="71c25-1053">Для учета прежней модели подписки с помощью ProductId и UserId.</span><span class="sxs-lookup"><span data-stu-id="71c25-1053">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="71c25-1054">Добавлена поддержка для включения AllowTracing на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="71c25-1054">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="71c25-1055">Обновлен командлет **Set-AzApiManagementSubscription**.</span><span class="sxs-lookup"><span data-stu-id="71c25-1055">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="71c25-1056">Для учета новой модели SubscriptonModel с помощью Scope и UserId.</span><span class="sxs-lookup"><span data-stu-id="71c25-1056">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="71c25-1057">Для учета прежней модели подписки с помощью ProductId и UserId.</span><span class="sxs-lookup"><span data-stu-id="71c25-1057">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="71c25-1058">Добавлена поддержка для включения AllowTracing на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="71c25-1058">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="71c25-1059">Следующие командлеты обновлены, чтобы принимать значение ResourceId в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="71c25-1059">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="71c25-1060">New-AzApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="71c25-1060">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="71c25-1061">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="71c25-1061">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="71c25-1062">Get-AzApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="71c25-1062">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="71c25-1063">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="71c25-1063">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="71c25-1064">Get-AzApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="71c25-1064">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="71c25-1065">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="71c25-1065">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="71c25-1066">Get-AzApiManagementAuthorizationServer.</span><span class="sxs-lookup"><span data-stu-id="71c25-1066">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="71c25-1067">Get-AzApiManagementBackend.</span><span class="sxs-lookup"><span data-stu-id="71c25-1067">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="71c25-1068">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="71c25-1068">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="71c25-1069">Get-AzApiManagementCertificate.</span><span class="sxs-lookup"><span data-stu-id="71c25-1069">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="71c25-1070">Remove-AzApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="71c25-1070">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="71c25-1071">Remove-AzApiManagementSubscription.</span><span class="sxs-lookup"><span data-stu-id="71c25-1071">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="71c25-1072">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="71c25-1072">Az.Automation</span></span>
* <span data-ttu-id="71c25-1073">Обновлен командлет Get-AzAutomationJobOutputRecord для обработки значений в формате JSON и в виде текстовой записи.</span><span class="sxs-lookup"><span data-stu-id="71c25-1073">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="71c25-1074">исправлена проблема https://github.com/Azure/azure-powershell/issues/7977.</span><span class="sxs-lookup"><span data-stu-id="71c25-1074">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="71c25-1075">исправлена проблема https://github.com/Azure/azure-powershell/issues/8600.</span><span class="sxs-lookup"><span data-stu-id="71c25-1075">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="71c25-1076">Поведение командлета Start-AzAutomationDscCompilationJob изменено так, чтобы сразу же запустить задание, а не ждать его завершения.</span><span class="sxs-lookup"><span data-stu-id="71c25-1076">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="71c25-1077">исправлена проблема https://github.com/Azure/azure-powershell/issues/8347.</span><span class="sxs-lookup"><span data-stu-id="71c25-1077">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="71c25-1078">Исправлен командлет Get-AzAutomationDscNode, возвращающий все узлы при использовании -Name.</span><span class="sxs-lookup"><span data-stu-id="71c25-1078">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="71c25-1079">Теперь он возвращает только соответствующий узел.</span><span class="sxs-lookup"><span data-stu-id="71c25-1079">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71c25-1080">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71c25-1080">Az.Compute</span></span>
* <span data-ttu-id="71c25-1081">Добавлены параметры ProtectFromScaleIn и ProtectFromScaleSetAction для командлета Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="71c25-1081">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="71c25-1082">Командлет New-AzVM с простым набором параметров теперь по умолчанию использует доступное расположение, если регион "восточная часть США" не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="71c25-1082">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="71c25-1083">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="71c25-1083">Az.DataLakeStore</span></span>
* <span data-ttu-id="71c25-1084">Обновлен пакет SDK ADLS для использования httpclient. В инфраструктуру Azure интегрирована проверка плоскости данных.</span><span class="sxs-lookup"><span data-stu-id="71c25-1084">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="71c25-1085">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="71c25-1085">Az.Monitor</span></span>
* <span data-ttu-id="71c25-1086">Исправлены неправильные имена параметров в справочных примерах.</span><span class="sxs-lookup"><span data-stu-id="71c25-1086">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71c25-1087">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71c25-1087">Az.Network</span></span>
* <span data-ttu-id="71c25-1088">Добавлен флаг DisableBgpRoutePropagation для выходных данных действующей таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="71c25-1088">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="71c25-1089">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="71c25-1089">Updated cmdlet:</span></span>
        - <span data-ttu-id="71c25-1090">Get-AzEffectiveRouteTable.</span><span class="sxs-lookup"><span data-stu-id="71c25-1090">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="71c25-1091">Исправлен двойной дефис в документации New-AzApplicationGatewayTrustedRootCertificate.</span><span class="sxs-lookup"><span data-stu-id="71c25-1091">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="71c25-1092">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71c25-1092">Az.Resources</span></span>
* <span data-ttu-id="71c25-1093">Добавлен новый командлет Get-AzureRmDenyAssignment для получения запрещающих назначений.</span><span class="sxs-lookup"><span data-stu-id="71c25-1093">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="71c25-1094">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71c25-1094">Az.Sql</span></span>
* <span data-ttu-id="71c25-1095">Командлеты Расширенной защиты от угроз переименованы на командлеты Расширенной защиты данных, и оценка уязвимости включена по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="71c25-1095">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="71c25-1096">2.0.0 — май 2019 г.</span><span class="sxs-lookup"><span data-stu-id="71c25-1096">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="71c25-1097">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71c25-1097">Az.Accounts</span></span>
* <span data-ttu-id="71c25-1098">Обновлена библиотека аутентификации для устранения проблем с ADFS при использовании аутентификации на основе имени пользователя и пароля.</span><span class="sxs-lookup"><span data-stu-id="71c25-1098">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="71c25-1099">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="71c25-1099">Az.CognitiveServices</span></span>
* <span data-ttu-id="71c25-1100">Отображается только заявление об отказе Bing для служб Поиска Bing.</span><span class="sxs-lookup"><span data-stu-id="71c25-1100">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="71c25-1101">Исправлена проблема с созданием учетной записи.</span><span class="sxs-lookup"><span data-stu-id="71c25-1101">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71c25-1102">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71c25-1102">Az.Compute</span></span>
* <span data-ttu-id="71c25-1103">Функция группы размещения близкого взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="71c25-1103">Proximity placement group feature.</span></span>
    - <span data-ttu-id="71c25-1104">Добавлены следующие новые командлеты:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="71c25-1104">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="71c25-1105">Новый параметр ProximityPlacementGroupId будет добавлен в следующие командлеты:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="71c25-1105">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="71c25-1106">В командлет New-AzGalleryImageVersion добавлен параметр StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="71c25-1106">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="71c25-1107">TargetRegion в командлете New-AzGalleryImageVersion может содержать StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="71c25-1107">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="71c25-1108">Параметр-переключатель SkipShutdown добавлен в командлеты Stop-AzVM и Stop-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="71c25-1108">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="71c25-1109">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="71c25-1109">Breaking changes</span></span>
    - <span data-ttu-id="71c25-1110">Командлет SET-AzVMBootDiagnostics изменен на Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="71c25-1110">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="71c25-1111">Командлет Export-AzLogAnalyticThrottledRequests изменен на Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="71c25-1111">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="71c25-1112">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="71c25-1112">Az.DeploymentManager</span></span>
* <span data-ttu-id="71c25-1113">Первая общедоступная версия командлетов диспетчера развертывания Azure</span><span class="sxs-lookup"><span data-stu-id="71c25-1113">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="71c25-1114">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="71c25-1114">Az.Dns</span></span>
* <span data-ttu-id="71c25-1115">Автоматическое делегирование DNS-сервера</span><span class="sxs-lookup"><span data-stu-id="71c25-1115">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="71c25-1116">Командлет для создания зоны DNS принимает имя родительской зоны в качестве дополнительного необязательного параметра.</span><span class="sxs-lookup"><span data-stu-id="71c25-1116">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="71c25-1117">Он добавляет записи NS в родительской зоне для созданной дочерней зоны.</span><span class="sxs-lookup"><span data-stu-id="71c25-1117">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="71c25-1118">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="71c25-1118">Az.FrontDoor</span></span>
* <span data-ttu-id="71c25-1119">Первая общедоступная версия командлетов Azure FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="71c25-1119">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="71c25-1120">Переименованы командлеты WAF для включения Waf.</span><span class="sxs-lookup"><span data-stu-id="71c25-1120">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="71c25-1121">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="71c25-1121">Az.HDInsight</span></span>
* <span data-ttu-id="71c25-1122">Удалены два командлета:</span><span class="sxs-lookup"><span data-stu-id="71c25-1122">Removed two cmdlets:</span></span>
    - <span data-ttu-id="71c25-1123">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="71c25-1123">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="71c25-1124">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="71c25-1124">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="71c25-1125">Добавлен новый командлет Set-AzHDInsightGatewayCredential для замены Grant-AzHDInsightHttpServicesAccess.</span><span class="sxs-lookup"><span data-stu-id="71c25-1125">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="71c25-1126">Обновлен командлет Get-AzHDInsightJobOutput для различения ролей читателя и оператора HDInsight:</span><span class="sxs-lookup"><span data-stu-id="71c25-1126">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="71c25-1127">Пользователям с ролью читателя не нужно указывать параметр DefaultStorageAccountKey явным образом, иначе возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="71c25-1127">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="71c25-1128">На пользователей с ролью оператора HDInsight это не повлияет.</span><span class="sxs-lookup"><span data-stu-id="71c25-1128">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="71c25-1129">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="71c25-1129">Az.Monitor</span></span>
* <span data-ttu-id="71c25-1130">Новые командлеты для API SQR (запланированное правило запросов)</span><span class="sxs-lookup"><span data-stu-id="71c25-1130">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="71c25-1131">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="71c25-1131">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="71c25-1132">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="71c25-1132">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="71c25-1133">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="71c25-1133">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="71c25-1134">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="71c25-1134">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="71c25-1135">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="71c25-1135">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="71c25-1136">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="71c25-1136">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="71c25-1137">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="71c25-1137">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="71c25-1138">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="71c25-1138">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="71c25-1139">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="71c25-1139">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="71c25-1140">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="71c25-1140">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="71c25-1141">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="71c25-1141">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="71c25-1142">См. подробнее об [API SQR](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules).</span><span class="sxs-lookup"><span data-stu-id="71c25-1142">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="71c25-1143">Обновлен файл Az.Monitor.md для включения командлетов для правила генерации оповещений на основе метрик GenV2(не классическая версия).</span><span class="sxs-lookup"><span data-stu-id="71c25-1143">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71c25-1144">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71c25-1144">Az.Network</span></span>
* <span data-ttu-id="71c25-1145">Добавлена поддержка для ресурса Шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="71c25-1145">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="71c25-1146">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="71c25-1146">New cmdlets</span></span>
        - <span data-ttu-id="71c25-1147">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="71c25-1147">New-AzNatGateway</span></span>
        - <span data-ttu-id="71c25-1148">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="71c25-1148">Get-AzNatGateway</span></span>
        - <span data-ttu-id="71c25-1149">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="71c25-1149">Set-AzNatGateway</span></span>
        - <span data-ttu-id="71c25-1150">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="71c25-1150">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="71c25-1151">Обновлены командлеты</span><span class="sxs-lookup"><span data-stu-id="71c25-1151">Updated cmdlets</span></span>
        - <span data-ttu-id="71c25-1152">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="71c25-1152">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="71c25-1153">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="71c25-1153">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="71c25-1154">Обновлены следующие команды для функции: Настройка и удаление пользовательских маршрутов через шлюз в Бруклине.</span><span class="sxs-lookup"><span data-stu-id="71c25-1154">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="71c25-1155">Обновлен командлет New-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.</span><span class="sxs-lookup"><span data-stu-id="71c25-1155">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="71c25-1156">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.</span><span class="sxs-lookup"><span data-stu-id="71c25-1156">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="71c25-1157">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="71c25-1157">Az.PolicyInsights</span></span>
* <span data-ttu-id="71c25-1158">Добавлена поддержка сведений об оценке политики запросов.</span><span class="sxs-lookup"><span data-stu-id="71c25-1158">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="71c25-1159">Добавлен параметр -Expand в командлет Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="71c25-1159">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="71c25-1160">Добавлена поддержка -Expand PolicyEvaluationDetails.</span><span class="sxs-lookup"><span data-stu-id="71c25-1160">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="71c25-1161">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="71c25-1161">Az.RecoveryServices</span></span>
* <span data-ttu-id="71c25-1162">Добавлена поддержка перекрестной подписки на Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="71c25-1162">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="71c25-1163">Добавлена возможность отмечать предстоящие критически важные изменения для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="71c25-1163">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="71c25-1164">Исправлены план восстановления и план действий для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="71c25-1164">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="71c25-1165">Исправлено сетевое сопоставление обновления Azure Site Recovery (Azure — Azure).</span><span class="sxs-lookup"><span data-stu-id="71c25-1165">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="71c25-1166">Исправлено направление защиты обновления Azure Site Recovery для управляемых дисков (Azure — Azure).</span><span class="sxs-lookup"><span data-stu-id="71c25-1166">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="71c25-1167">Добавлены другие незначительные исправления.</span><span class="sxs-lookup"><span data-stu-id="71c25-1167">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="71c25-1168">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="71c25-1168">Az.Relay</span></span>
* <span data-ttu-id="71c25-1169">Исправлены опечатки в сообщениях для клиентов.</span><span class="sxs-lookup"><span data-stu-id="71c25-1169">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="71c25-1170">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="71c25-1170">Az.ServiceBus</span></span>
* <span data-ttu-id="71c25-1171">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="71c25-1171">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="71c25-1172">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="71c25-1172">Az.Storage</span></span>
* <span data-ttu-id="71c25-1173">Выполнено обновление клиентской библиотеки хранилища до версии 10.0.1 (пространство имен всех объектов из этого пакета SDK изменено с Microsoft.WindowsAzure.Storage. *на Microsoft.Azure.Storage*).</span><span class="sxs-lookup"><span data-stu-id="71c25-1173">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="71c25-1174">Выполнено обновление до Microsoft.Azure.Management.Storage версии 11.0.0 для включения поддержки нового API версии 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="71c25-1174">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="71c25-1175">Значение свойства Kind по умолчанию в учетной записи хранения изменено со Storage на StorageV2.</span><span class="sxs-lookup"><span data-stu-id="71c25-1175">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="71c25-1176">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="71c25-1176">New-AzStorageAccount</span></span>
* <span data-ttu-id="71c25-1177">Изменено значение Sku.Name в выходных данных командлета учетной записи хранения в соответствии со значением Sku.Name во входных данных путем добавления _ (например, StandardLRS изменено на Standard_LRS).</span><span class="sxs-lookup"><span data-stu-id="71c25-1177">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="71c25-1178">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="71c25-1178">New-AzStorageAccount</span></span>
    - <span data-ttu-id="71c25-1179">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="71c25-1179">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="71c25-1180">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="71c25-1180">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="71c25-1181">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="71c25-1181">Az.Websites</span></span>
* <span data-ttu-id="71c25-1182">Свойство Kind теперь будет задаваться объектам PSSite, возвращаемым командлетом Get-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="71c25-1182">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="71c25-1183">Get-AzWebApp\*Metrics и Get-AzAppServicePlanMetrics считаются нерекомендуемыми.</span><span class="sxs-lookup"><span data-stu-id="71c25-1183">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="71c25-1184">1.8.0 — апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="71c25-1184">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="71c25-1185">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="71c25-1185">Highlights since the last major release</span></span>
* <span data-ttu-id="71c25-1186">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="71c25-1186">General availability of `Az` module</span></span>
* <span data-ttu-id="71c25-1187">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="71c25-1187">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="71c25-1188">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="71c25-1188">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="71c25-1189">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="71c25-1189">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="71c25-1190">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="71c25-1190">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="71c25-1191">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="71c25-1191">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="71c25-1192">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="71c25-1192">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="71c25-1193">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71c25-1193">Az.Accounts</span></span>
* <span data-ttu-id="71c25-1194">Обновлен командлет Uninstall-AzureRm для правильного удаления модулей в Mac.</span><span class="sxs-lookup"><span data-stu-id="71c25-1194">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="71c25-1195">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="71c25-1195">Az.Batch</span></span>
* <span data-ttu-id="71c25-1196">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="71c25-1196">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="71c25-1197">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="71c25-1197">Az.Cdn</span></span>
* <span data-ttu-id="71c25-1198">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="71c25-1198">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="71c25-1199">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="71c25-1199">Az.CognitiveServices</span></span>
* <span data-ttu-id="71c25-1200">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="71c25-1200">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71c25-1201">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71c25-1201">Az.Compute</span></span>
* <span data-ttu-id="71c25-1202">Устранена проблема с установкой AEM, если в идентификаторах ресурсов дисков группа ресурсов указана в нижнем регистре.</span><span class="sxs-lookup"><span data-stu-id="71c25-1202">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="71c25-1203">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="71c25-1203">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="71c25-1204">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="71c25-1204">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="71c25-1205">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="71c25-1205">Az.DataFactory</span></span>
* <span data-ttu-id="71c25-1206">Добавлены свойства SsisProperties, если NodeCount не имеет значения NULL для управляемой среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="71c25-1206">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="71c25-1207">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="71c25-1207">Az.DataLakeStore</span></span>
* <span data-ttu-id="71c25-1208">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="71c25-1208">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="71c25-1209">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="71c25-1209">Az.EventGrid</span></span>
* <span data-ttu-id="71c25-1210">Обновлен текст справки для конечной точки, указывающий, что необходимо создать ресурсы, прежде чем использовать командлеты для создания или обновления подписки на события.</span><span class="sxs-lookup"><span data-stu-id="71c25-1210">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="71c25-1211">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="71c25-1211">Az.EventHub</span></span>
* <span data-ttu-id="71c25-1212">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="71c25-1212">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="71c25-1213">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="71c25-1213">Az.HDInsight</span></span>
* <span data-ttu-id="71c25-1214">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="71c25-1214">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="71c25-1215">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="71c25-1215">Az.IotHub</span></span>
* <span data-ttu-id="71c25-1216">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="71c25-1216">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="71c25-1217">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="71c25-1217">Az.KeyVault</span></span>
* <span data-ttu-id="71c25-1218">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="71c25-1218">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="71c25-1219">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="71c25-1219">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="71c25-1220">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="71c25-1220">Az.MachineLearning</span></span>
* <span data-ttu-id="71c25-1221">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="71c25-1221">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="71c25-1222">Az.Media</span><span class="sxs-lookup"><span data-stu-id="71c25-1222">Az.Media</span></span>
* <span data-ttu-id="71c25-1223">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="71c25-1223">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="71c25-1224">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="71c25-1224">Az.Monitor</span></span>
  * <span data-ttu-id="71c25-1225">Добавлены новые командлеты для правила генерации оповещений на основе метрик GenV2 (не классических).</span><span class="sxs-lookup"><span data-stu-id="71c25-1225">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="71c25-1226">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="71c25-1226">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="71c25-1227">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="71c25-1227">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="71c25-1228">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="71c25-1228">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="71c25-1229">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="71c25-1229">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="71c25-1230">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="71c25-1230">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="71c25-1231">Обновлен пакет SDK Monitor до предварительной версии 0.22.0.</span><span class="sxs-lookup"><span data-stu-id="71c25-1231">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71c25-1232">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71c25-1232">Az.Network</span></span>
* <span data-ttu-id="71c25-1233">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="71c25-1233">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="71c25-1234">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="71c25-1234">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="71c25-1235">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="71c25-1235">Az.NotificationHubs</span></span>
* <span data-ttu-id="71c25-1236">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="71c25-1236">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="71c25-1237">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="71c25-1237">Az.OperationalInsights</span></span>
* <span data-ttu-id="71c25-1238">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="71c25-1238">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="71c25-1239">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="71c25-1239">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="71c25-1240">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="71c25-1240">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="71c25-1241">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="71c25-1241">Az.RecoveryServices</span></span>
* <span data-ttu-id="71c25-1242">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="71c25-1242">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="71c25-1243">Обновлен табличный формат для SQL на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="71c25-1243">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="71c25-1244">Добавлен альтернативный метод для получения расположения в Общей папке Azure.</span><span class="sxs-lookup"><span data-stu-id="71c25-1244">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="71c25-1245">Обновлено значение ScheduleRunDays в объекте SchedulePolicy в соответствии с часовым поясом.</span><span class="sxs-lookup"><span data-stu-id="71c25-1245">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="71c25-1246">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="71c25-1246">Az.RedisCache</span></span>
* <span data-ttu-id="71c25-1247">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="71c25-1247">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="71c25-1248">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71c25-1248">Az.Resources</span></span>
* <span data-ttu-id="71c25-1249">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="71c25-1249">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="71c25-1250">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71c25-1250">Az.Sql</span></span>
* <span data-ttu-id="71c25-1251">Заменена зависимость от пакета SDK монитора на обычный код.</span><span class="sxs-lookup"><span data-stu-id="71c25-1251">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="71c25-1252">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="71c25-1252">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="71c25-1253">Улучшен процесс классификации нескольких столбцов.</span><span class="sxs-lookup"><span data-stu-id="71c25-1253">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="71c25-1254">Добавлены свойства SKU (имя, семейство, производительность SKU) в отклике Get-AzSqlServerServiceObjective, а также по умолчанию задан табличный формат.</span><span class="sxs-lookup"><span data-stu-id="71c25-1254">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="71c25-1255">C помощью Get-AzSqlServerServiceObjective теперь можно получать список доступных целевых служб по расположению без необходимости заранее размещать сервер в регионе.</span><span class="sxs-lookup"><span data-stu-id="71c25-1255">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="71c25-1256">Поддерживается параметр часового пояса при создании Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="71c25-1256">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="71c25-1257">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="71c25-1257">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="71c25-1258">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="71c25-1258">Az.Websites</span></span>
* <span data-ttu-id="71c25-1259">Исправлены командлеты Set-AzWebApp и Set-AzWebAppSlot, которые теперь не удаляют теги при выполнении.</span><span class="sxs-lookup"><span data-stu-id="71c25-1259">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="71c25-1260">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="71c25-1260">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="71c25-1261">Обновлен пакет SDK веб-узлов.</span><span class="sxs-lookup"><span data-stu-id="71c25-1261">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="71c25-1262">Удалено свойство AdminSiteName из PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="71c25-1262">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="71c25-1263">1.7.0 —апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="71c25-1263">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="71c25-1264">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="71c25-1264">Highlights since the last major release</span></span>
* <span data-ttu-id="71c25-1265">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="71c25-1265">General availability of `Az` module</span></span>
* <span data-ttu-id="71c25-1266">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="71c25-1266">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="71c25-1267">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="71c25-1267">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="71c25-1268">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="71c25-1268">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="71c25-1269">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="71c25-1269">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="71c25-1270">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="71c25-1270">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="71c25-1271">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="71c25-1271">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="71c25-1272">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71c25-1272">Az.Accounts</span></span>
* <span data-ttu-id="71c25-1273">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment. Теперь они принимают параметр AzureAnalysisServicesEndpointResourceId.</span><span class="sxs-lookup"><span data-stu-id="71c25-1273">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="71c25-1274">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="71c25-1274">Az.AnalysisServices</span></span>
* <span data-ttu-id="71c25-1275">Использование ServiceClient в командлетах плоскости данных и удаление исходной логики проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="71c25-1275">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="71c25-1276">Add-AzureASAccount используется как оболочка для Connect-AzAccount во избежание критических изменений.</span><span class="sxs-lookup"><span data-stu-id="71c25-1276">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="71c25-1277">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="71c25-1277">Az.Automation</span></span>
* <span data-ttu-id="71c25-1278">Исправлена ошибка командлета New-AzAutomationSoftwareUpdateConfiguration, связанная с включением.</span><span class="sxs-lookup"><span data-stu-id="71c25-1278">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="71c25-1279">Теперь параметры IncludedKbNumber и IncludedPackageNameMask должны работать нормально.</span><span class="sxs-lookup"><span data-stu-id="71c25-1279">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="71c25-1280">Исправлена ошибка динамической группы управления обновлениями службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="71c25-1280">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71c25-1281">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71c25-1281">Az.Compute</span></span>
* <span data-ttu-id="71c25-1282">В командлеты New-AzDiskConfig и New-AzSnapshotConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="71c25-1282">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="71c25-1283">Теперь можно создавать виртуальные машину на основе образов из коллекции от других клиентов.</span><span class="sxs-lookup"><span data-stu-id="71c25-1283">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="71c25-1284">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="71c25-1284">Az.ContainerInstance</span></span>
* <span data-ttu-id="71c25-1285">Исправлена проблема в параметре -Command командлета New-AzContainerGroup, из-за которой в конце добавлялся пустой аргумент.</span><span class="sxs-lookup"><span data-stu-id="71c25-1285">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="71c25-1286">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="71c25-1286">Az.DataFactory</span></span>
* <span data-ttu-id="71c25-1287">Пакет SDK для ADF .NET обновлен до версии 3.0.2.</span><span class="sxs-lookup"><span data-stu-id="71c25-1287">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="71c25-1288">Командлет Set-AzDataFactoryV2 обновлен с помощью дополнительных параметров для настроек, связанных с RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="71c25-1288">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="71c25-1289">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71c25-1289">Az.Resources</span></span>
* <span data-ttu-id="71c25-1290">Улучшена обработка поставщиков Get-AzResource при предоставлении параметров -ResourceId или -ResourceGroupName, -Name и -ResourceType.</span><span class="sxs-lookup"><span data-stu-id="71c25-1290">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="71c25-1291">Улучшена обработка ошибок в командлетах Test-AzDeployment и Test-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="71c25-1291">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="71c25-1292">Теперь ошибки, возникающие за пределами проверки развертывания, обрабатываются и включаются в выходные данные команды.</span><span class="sxs-lookup"><span data-stu-id="71c25-1292">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="71c25-1293">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="71c25-1293">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="71c25-1294">Добавлен параметр-переключатель -IgnoreDynamicParameters, с помощью которого можно настроить командлеты развертывания так, чтобы они пропускали запросы в сценариях скриптов и заданий.</span><span class="sxs-lookup"><span data-stu-id="71c25-1294">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="71c25-1295">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="71c25-1295">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="71c25-1296">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71c25-1296">Az.Sql</span></span>
* <span data-ttu-id="71c25-1297">Поддержка классификации данных в базе данных.</span><span class="sxs-lookup"><span data-stu-id="71c25-1297">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="71c25-1298">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="71c25-1298">Az.Storage</span></span>
* <span data-ttu-id="71c25-1299">Подробные сообщения об ошибке передаются при создании контекста хранилища с помощью параметра -UseConnectedAccount, но без входа в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="71c25-1299">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="71c25-1300">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="71c25-1300">New-AzStorageContext</span></span>
* <span data-ttu-id="71c25-1301">Поддержка свойств службы управления BLOB-объектов в указанной учетной записи хранения с помощью API плоскости управления.</span><span class="sxs-lookup"><span data-stu-id="71c25-1301">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="71c25-1302">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="71c25-1302">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="71c25-1303">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="71c25-1303">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="71c25-1304">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="71c25-1304">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="71c25-1305">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="71c25-1305">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="71c25-1306">Поддержка параметра -AsJob в командлетах для отправки и скачивания больших двоичных объектов и файлов.</span><span class="sxs-lookup"><span data-stu-id="71c25-1306">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="71c25-1307">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="71c25-1307">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="71c25-1308">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="71c25-1308">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="71c25-1309">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="71c25-1309">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="71c25-1310">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="71c25-1310">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="71c25-1311">1.6.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="71c25-1311">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="71c25-1312">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="71c25-1312">Highlights since the last major release</span></span>
* <span data-ttu-id="71c25-1313">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="71c25-1313">General availability of `Az` module</span></span>
* <span data-ttu-id="71c25-1314">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="71c25-1314">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="71c25-1315">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="71c25-1315">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="71c25-1316">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="71c25-1316">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="71c25-1317">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="71c25-1317">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="71c25-1318">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="71c25-1318">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="71c25-1319">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="71c25-1319">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="71c25-1320">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="71c25-1320">Az.Automation</span></span>
* <span data-ttu-id="71c25-1321">В управление обновлениями службы автоматизации Azure внесены изменения для поддержки следующих новых функций:</span><span class="sxs-lookup"><span data-stu-id="71c25-1321">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="71c25-1322">динамическое группирование;</span><span class="sxs-lookup"><span data-stu-id="71c25-1322">Dynamic grouping</span></span>
    * <span data-ttu-id="71c25-1323">скрипты предварительного или последующего выполнения;</span><span class="sxs-lookup"><span data-stu-id="71c25-1323">Pre-Post script</span></span>
    * <span data-ttu-id="71c25-1324">параметр перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="71c25-1324">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71c25-1325">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71c25-1325">Az.Compute</span></span>
* <span data-ttu-id="71c25-1326">Устранена проблема, связанная с разрешением пути в Get-AzVmBootDiagnosticsData.</span><span class="sxs-lookup"><span data-stu-id="71c25-1326">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="71c25-1327">Обновление клиентской библиотеки вычислений до версии 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="71c25-1327">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="71c25-1328">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="71c25-1328">Az.KeyVault</span></span>
* <span data-ttu-id="71c25-1329">Добавлена поддержка подстановочных знаков в командлетах KeyVault.</span><span class="sxs-lookup"><span data-stu-id="71c25-1329">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71c25-1330">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71c25-1330">Az.Network</span></span>
* <span data-ttu-id="71c25-1331">Добавлена поддержка анализа угроз для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="71c25-1331">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="71c25-1332">Добавлены настраиваемые правила и ресурс верхнего уровня для политики брандмауэра Шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="71c25-1332">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="71c25-1333">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="71c25-1333">Az.RecoveryServices</span></span>
* <span data-ttu-id="71c25-1334">В политику виртуальной машины Azure добавлен объект SnapshotRetentionInDays для поддержки мгновенного восстановления.</span><span class="sxs-lookup"><span data-stu-id="71c25-1334">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="71c25-1335">Добавлена поддержка канала для отмены регистрации контейнера.</span><span class="sxs-lookup"><span data-stu-id="71c25-1335">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="71c25-1336">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71c25-1336">Az.Resources</span></span>
* <span data-ttu-id="71c25-1337">Обновлена поддержка подстановочных знаков для Get-AzResource и Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="71c25-1337">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="71c25-1338">Обновлены учетные данные, используемые при общих вызовах к ARM.</span><span class="sxs-lookup"><span data-stu-id="71c25-1338">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="71c25-1339">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71c25-1339">Az.Sql</span></span>
* <span data-ttu-id="71c25-1340">Изменен тип параметра (ExcludeDetectionType) командлетов для обнаружения угроз с DetectionTypes на string[] для поддержки актуального состояния при добавлении новых типов обнаружения и для поддержки автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="71c25-1340">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="71c25-1341">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="71c25-1341">Az.Storage</span></span>
* <span data-ttu-id="71c25-1342">Поддержка получения, настройки и удаления политики управления в учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="71c25-1342">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="71c25-1343">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="71c25-1343">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="71c25-1344">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="71c25-1344">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="71c25-1345">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="71c25-1345">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="71c25-1346">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="71c25-1346">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="71c25-1347">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="71c25-1347">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="71c25-1348">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="71c25-1348">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="71c25-1349">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="71c25-1349">Az.Websites</span></span>
* <span data-ttu-id="71c25-1350">Исправлена ошибка с шаблоном ARM, из-за которой прерывалось клонирование все слотов при использовании New-AzWebApp -IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="71c25-1350">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="71c25-1351">1.5.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="71c25-1351">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="71c25-1352">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71c25-1352">Az.Accounts</span></span>
* <span data-ttu-id="71c25-1353">Добавлена команда Register-AzModule для поддержки созданных командлетов AutoRest.</span><span class="sxs-lookup"><span data-stu-id="71c25-1353">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="71c25-1354">Обновлены примеры для Connect AzAccount.</span><span class="sxs-lookup"><span data-stu-id="71c25-1354">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="71c25-1355">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="71c25-1355">Az.Automation</span></span>
* <span data-ttu-id="71c25-1356">Исправлена проблема с получением некоторых ежемесячных расписаний в нескольких командлетах службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="71c25-1356">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="71c25-1357">Исправлен командлет Get-AzAutomationDscNode, возвращающий только первые 20 узлов.</span><span class="sxs-lookup"><span data-stu-id="71c25-1357">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="71c25-1358">Теперь он возвращает все узлы.</span><span class="sxs-lookup"><span data-stu-id="71c25-1358">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="71c25-1359">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="71c25-1359">Az.Cdn</span></span>
* <span data-ttu-id="71c25-1360">Добавлены новые командлеты PowerShell для включения и отключения HTTPS для личного домена и отключены устаревшие командлеты.</span><span class="sxs-lookup"><span data-stu-id="71c25-1360">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71c25-1361">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71c25-1361">Az.Compute</span></span>
* <span data-ttu-id="71c25-1362">Добавлена поддержка подстановочных знаков в командлетах Get.</span><span class="sxs-lookup"><span data-stu-id="71c25-1362">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="71c25-1363">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="71c25-1363">Az.DataFactory</span></span>
* <span data-ttu-id="71c25-1364">Обновлен пакет SDK для ADF .NET до версии 3.0.1.</span><span class="sxs-lookup"><span data-stu-id="71c25-1364">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="71c25-1365">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="71c25-1365">Az.LogicApp</span></span>
* <span data-ttu-id="71c25-1366">Исправлена проблема с получением только первой страницы результатов при выполнении команды ListWorkflows.</span><span class="sxs-lookup"><span data-stu-id="71c25-1366">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71c25-1367">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71c25-1367">Az.Network</span></span>
* <span data-ttu-id="71c25-1368">Добавлена поддержка подстановочных знаков в командлетах Network.</span><span class="sxs-lookup"><span data-stu-id="71c25-1368">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="71c25-1369">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="71c25-1369">Az.RecoveryServices</span></span>
* <span data-ttu-id="71c25-1370">Добавлена поддержка SQL Server на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="71c25-1370">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="71c25-1371">Обновление пакета SDK</span><span class="sxs-lookup"><span data-stu-id="71c25-1371">SDK Update</span></span>
* <span data-ttu-id="71c25-1372">Удалена проверка VMappContainer в Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="71c25-1372">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="71c25-1373">Добавлены параметры Name и ServerName для Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="71c25-1373">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="71c25-1374">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71c25-1374">Az.Resources</span></span>
* <span data-ttu-id="71c25-1375">Добавлен параметр `-TemplateObject` в командлеты для развертывания.</span><span class="sxs-lookup"><span data-stu-id="71c25-1375">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="71c25-1376">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2933.</span><span class="sxs-lookup"><span data-stu-id="71c25-1376">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="71c25-1377">Устранена проблема с передачей в конвейер результата `Get-AzResource` для `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="71c25-1377">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="71c25-1378">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8240.</span><span class="sxs-lookup"><span data-stu-id="71c25-1378">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="71c25-1379">Устранена проблема с изменением типа данных JSON при выполнении `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="71c25-1379">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="71c25-1380">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7930.</span><span class="sxs-lookup"><span data-stu-id="71c25-1380">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="71c25-1381">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71c25-1381">Az.Sql</span></span>
* <span data-ttu-id="71c25-1382">Обновление AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="71c25-1382">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="71c25-1383">Исправлено поведение для пограничного случая при создании параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="71c25-1383">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="71c25-1384">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="71c25-1384">Az.Storage</span></span>
* <span data-ttu-id="71c25-1385">Включена поддержка Kind BlockBlobStorage при создании учетной записи хранения для New-AzStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="71c25-1385">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="71c25-1386">1.4.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="71c25-1386">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="71c25-1387">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="71c25-1387">Az.AnalysisServices</span></span>
* <span data-ttu-id="71c25-1388">Командлет AddAzureASAccount устарел.</span><span class="sxs-lookup"><span data-stu-id="71c25-1388">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="71c25-1389">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="71c25-1389">Az.Automation</span></span>
* <span data-ttu-id="71c25-1390">Обновлена справка для командлета Import-AzAutomationDscNodeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="71c25-1390">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="71c25-1391">Добавлена проверка имени конфигурации для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="71c25-1391">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="71c25-1392">Улучшена обработка ошибок для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="71c25-1392">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="71c25-1393">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="71c25-1393">Az.CognitiveServices</span></span>
* <span data-ttu-id="71c25-1394">Добавлен параметр CustomSubdomainName — новый необязательный параметр для командлета New-AzCognitiveServicesAccount, который указывает поддомен для ресурса.</span><span class="sxs-lookup"><span data-stu-id="71c25-1394">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71c25-1395">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71c25-1395">Az.Compute</span></span>
* <span data-ttu-id="71c25-1396">Устранена проблема с идентификаторами наборов параметров.</span><span class="sxs-lookup"><span data-stu-id="71c25-1396">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="71c25-1397">Обновлен командлет Get-AzVMExtension для отображения списка всех установленных расширений, если не указан параметр Name.</span><span class="sxs-lookup"><span data-stu-id="71c25-1397">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="71c25-1398">Для командлета Update-AzImage добавлены параметры Tag и ResourceId.</span><span class="sxs-lookup"><span data-stu-id="71c25-1398">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="71c25-1399">Командлет Get-AzVmssVM, который выполняется без указания идентификатора экземпляра и с параметром InstanceView, может выводить виртуальные машины из VMSS с представлением экземпляра.</span><span class="sxs-lookup"><span data-stu-id="71c25-1399">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="71c25-1400">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="71c25-1400">Az.DataLakeStore</span></span>
* <span data-ttu-id="71c25-1401">Добавлены командлеты для перечисления и восстановления удаленного элемента ADL.</span><span class="sxs-lookup"><span data-stu-id="71c25-1401">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="71c25-1402">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="71c25-1402">Az.EventHub</span></span>
* <span data-ttu-id="71c25-1403">Добавлено новое логическое свойство SkipEmptyArchives для пропуска пустых архивов в классе CaptureDescription Eventhub.</span><span class="sxs-lookup"><span data-stu-id="71c25-1403">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="71c25-1404">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="71c25-1404">Az.KeyVault</span></span>
* <span data-ttu-id="71c25-1405">Исправлена расстановка тегов для командлета Set-AzKeyVaultSecret.</span><span class="sxs-lookup"><span data-stu-id="71c25-1405">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="71c25-1406">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="71c25-1406">Az.LogicApp</span></span>
* <span data-ttu-id="71c25-1407">Добавлен SKU "Базовый" для учетных записей интеграции.</span><span class="sxs-lookup"><span data-stu-id="71c25-1407">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="71c25-1408">Добавлены типы сопоставлений Liquid, а также XSLT 2.0 и XSLT 3.0.</span><span class="sxs-lookup"><span data-stu-id="71c25-1408">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="71c25-1409">Новые командлеты для сборок учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="71c25-1409">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="71c25-1410">Get-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="71c25-1410">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="71c25-1411">New-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="71c25-1411">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="71c25-1412">Remove-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="71c25-1412">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="71c25-1413">Set-AzIntegrationAccountAssembly.</span><span class="sxs-lookup"><span data-stu-id="71c25-1413">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="71c25-1414">Новые командлеты для конфигурации пакета учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="71c25-1414">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="71c25-1415">Get-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="71c25-1415">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="71c25-1416">New-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="71c25-1416">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="71c25-1417">Remove-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="71c25-1417">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="71c25-1418">Set-AzIntegrationAccountBatchConfiguration.</span><span class="sxs-lookup"><span data-stu-id="71c25-1418">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="71c25-1419">Обновлен пакет SDK Logic Apps до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="71c25-1419">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="71c25-1420">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="71c25-1420">Az.Monitor</span></span>
* <span data-ttu-id="71c25-1421">Обновлена справка для командлета Get-AzMetric.</span><span class="sxs-lookup"><span data-stu-id="71c25-1421">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71c25-1422">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71c25-1422">Az.Network</span></span>
* <span data-ttu-id="71c25-1423">Обновлен пример справки для командлета Add-AzApplicationGatewayCustomError.</span><span class="sxs-lookup"><span data-stu-id="71c25-1423">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="71c25-1424">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="71c25-1424">Az.OperationalInsights</span></span>
* <span data-ttu-id="71c25-1425">Дополнительная поддержка создания и получения источников данных ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="71c25-1425">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="71c25-1426">Добавлен новый тип ApplicationInsights для получения определенных или всех источников данных ApplicationInsights для указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="71c25-1426">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="71c25-1427">Добавлен командлет New-AzOperationalInsightsApplicationInsightsDataSource для создания источника данных с использованием параметров указанного ресурса Application-Insightss: subscription Id, resourceGroupName и name.</span><span class="sxs-lookup"><span data-stu-id="71c25-1427">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="71c25-1428">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71c25-1428">Az.Resources</span></span>
* <span data-ttu-id="71c25-1429">исправлена проблема https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="71c25-1429">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="71c25-1430">исправлена проблема https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="71c25-1430">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="71c25-1431">исправлена проблема https://github.com/Azure/azure-powershell/issues/6219.</span><span class="sxs-lookup"><span data-stu-id="71c25-1431">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="71c25-1432">Исправлена ошибка, препятствующая повторному созданию KeyCredentials.</span><span class="sxs-lookup"><span data-stu-id="71c25-1432">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="71c25-1433">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71c25-1433">Az.Sql</span></span>
* <span data-ttu-id="71c25-1434">Добавлена поддержка уровня гипермасштабирования в базе данных SQL.</span><span class="sxs-lookup"><span data-stu-id="71c25-1434">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="71c25-1435">Исправлена ошибка, из-за которой восстановление могло завершиться со сбоем при указании ненужных свойств в запросе на восстановление.</span><span class="sxs-lookup"><span data-stu-id="71c25-1435">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="71c25-1436">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="71c25-1436">Az.Websites</span></span>
* <span data-ttu-id="71c25-1437">Исправлен пример для командлета Get-AzWebAppSlotMetrics.</span><span class="sxs-lookup"><span data-stu-id="71c25-1437">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="71c25-1438">1.3.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="71c25-1438">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="71c25-1439">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71c25-1439">Az.Accounts</span></span>
* <span data-ttu-id="71c25-1440">Обновление до последней версии ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="71c25-1440">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="71c25-1441">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="71c25-1441">Az.AnalysisServices</span></span>
<span data-ttu-id="71c25-1442">Общедоступная версия модуля Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="71c25-1442">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71c25-1443">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71c25-1443">Az.Compute</span></span>
* <span data-ttu-id="71c25-1444">Расширение AEM: добавлена поддержка дисков UltraSSD, P60, P70 и P80.</span><span class="sxs-lookup"><span data-stu-id="71c25-1444">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="71c25-1445">Обновлено описание справки для командлета Set-AzVMBootDiagnostics.</span><span class="sxs-lookup"><span data-stu-id="71c25-1445">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="71c25-1446">Обновлено описание справки и пример для командлета Update-AzImage.</span><span class="sxs-lookup"><span data-stu-id="71c25-1446">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="71c25-1447">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="71c25-1447">Az.RecoveryServices</span></span>
<span data-ttu-id="71c25-1448">Общедоступная версия модуля Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="71c25-1448">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="71c25-1449">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71c25-1449">Az.Resources</span></span>
* <span data-ttu-id="71c25-1450">Исправлена расстановка тегов для групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="71c25-1450">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="71c25-1451">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="71c25-1451">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="71c25-1452">Исправлена проблема с игнорированием командлетом `Get-AzureRmRoleAssignment` параметра -ErrorAction.</span><span class="sxs-lookup"><span data-stu-id="71c25-1452">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="71c25-1453">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="71c25-1453">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="71c25-1454">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71c25-1454">Az.Sql</span></span>
* <span data-ttu-id="71c25-1455">Добавлен командлет Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="71c25-1455">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="71c25-1456">Исправлена проблема с появлением исключения NullRef при выполнении командлетов SQL, если не выполнен вход в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="71c25-1456">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="71c25-1457">Исправлено исключение NullRef в командлете Get-AzSqlCapability.</span><span class="sxs-lookup"><span data-stu-id="71c25-1457">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="71c25-1458">1.2.1 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="71c25-1458">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="71c25-1459">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71c25-1459">Az.Accounts</span></span>
* <span data-ttu-id="71c25-1460">Выпуск с правильной версией службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="71c25-1460">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="71c25-1461">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="71c25-1461">Az.AnalysisServices</span></span>
* <span data-ttu-id="71c25-1462">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="71c25-1462">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="71c25-1463">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="71c25-1463">Az.RecoveryServices</span></span>
* <span data-ttu-id="71c25-1464">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="71c25-1464">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="71c25-1465">1.2.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="71c25-1465">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="71c25-1466">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71c25-1466">Az.Accounts</span></span>
* <span data-ttu-id="71c25-1467">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="71c25-1467">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="71c25-1468">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="71c25-1468">Update incorrect online help URLs</span></span>
* <span data-ttu-id="71c25-1469">Добавлено предупреждающее сообщение в PS Core для модуля Uninstall-AzureRm.</span><span class="sxs-lookup"><span data-stu-id="71c25-1469">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="71c25-1470">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="71c25-1470">Az.Aks</span></span>
* <span data-ttu-id="71c25-1471">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="71c25-1471">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="71c25-1472">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="71c25-1472">Az.Automation</span></span>
* <span data-ttu-id="71c25-1473">Добавлена поддержка для модулей runbook Python 2.</span><span class="sxs-lookup"><span data-stu-id="71c25-1473">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="71c25-1474">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="71c25-1474">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="71c25-1475">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="71c25-1475">Az.Cdn</span></span>
* <span data-ttu-id="71c25-1476">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="71c25-1476">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71c25-1477">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71c25-1477">Az.Compute</span></span>
* <span data-ttu-id="71c25-1478">Добавлен командлет Invoke-AzVMReimage.</span><span class="sxs-lookup"><span data-stu-id="71c25-1478">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="71c25-1479">Добавлен параметр TempDisk к командлету Set-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="71c25-1479">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="71c25-1480">Исправлено предупреждающее сообщение командлета New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="71c25-1480">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="71c25-1481">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="71c25-1481">Az.ContainerRegistry</span></span>
* <span data-ttu-id="71c25-1482">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="71c25-1482">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="71c25-1483">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="71c25-1483">Az.DataFactory</span></span>
* <span data-ttu-id="71c25-1484">Пакет SDK ADF .Net обновлен до версии 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="71c25-1484">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="71c25-1485">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="71c25-1485">Az.DataLakeStore</span></span>
* <span data-ttu-id="71c25-1486">Исправлена проблема с конечной точкой ADLS при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="71c25-1486">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="71c25-1487">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7462.</span><span class="sxs-lookup"><span data-stu-id="71c25-1487">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="71c25-1488">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="71c25-1488">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="71c25-1489">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="71c25-1489">Az.IotHub</span></span>
* <span data-ttu-id="71c25-1490">Добавлен формат кодирования для командлета Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="71c25-1490">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="71c25-1491">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="71c25-1491">Az.KeyVault</span></span>
* <span data-ttu-id="71c25-1492">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="71c25-1492">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71c25-1493">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71c25-1493">Az.Network</span></span>
* <span data-ttu-id="71c25-1494">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="71c25-1494">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="71c25-1495">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71c25-1495">Az.Resources</span></span>
* <span data-ttu-id="71c25-1496">Исправлены неправильные примеры в справочной документации по командлетам New-AzADAppCredential и New-AzADSpCredential.</span><span class="sxs-lookup"><span data-stu-id="71c25-1496">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="71c25-1497">Исправлена проблема, при которой путь для параметра -TemplateFile не удавалось разрешить до выполнения командлетов развертывания групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="71c25-1497">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="71c25-1498">Az.Resources: исправлена документация для значения по умолчанию -Mode командлета New-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="71c25-1498">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="71c25-1499">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/7522.</span><span class="sxs-lookup"><span data-stu-id="71c25-1499">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="71c25-1500">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/5747.</span><span class="sxs-lookup"><span data-stu-id="71c25-1500">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="71c25-1501">Исправлена проблема с форматированием объекта PSResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="71c25-1501">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="71c25-1502">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2123.</span><span class="sxs-lookup"><span data-stu-id="71c25-1502">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="71c25-1503">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="71c25-1503">Az.ServiceFabric</span></span>
* <span data-ttu-id="71c25-1504">Исправлена проблема с появлением исключения в процессе отката при добавлении сертификата к модели VMSS: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="71c25-1504">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="71c25-1505">Исправлены некоторые сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="71c25-1505">Fix some error messages.</span></span>
* <span data-ttu-id="71c25-1506">Исправлена проблема с созданием кластера с шаблоном ARM по умолчанию для командлета New-AzServiceFabriCluster, который не работал с операцией миграции в Az.</span><span class="sxs-lookup"><span data-stu-id="71c25-1506">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="71c25-1507">Исправлена проблема с добавлением сертификата кластера или приложения: теперь они добавляются только в Масштабируемые наборы виртуальных машин, которые сопоставлены с кластером, путем проверки идентификатора кластера в расширении.</span><span class="sxs-lookup"><span data-stu-id="71c25-1507">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="71c25-1508">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="71c25-1508">Az.SignalR</span></span>
* <span data-ttu-id="71c25-1509">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="71c25-1509">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="71c25-1510">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71c25-1510">Az.Sql</span></span>
* <span data-ttu-id="71c25-1511">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="71c25-1511">Update incorrect online help URLs</span></span>
* <span data-ttu-id="71c25-1512">Обновлено описание параметра LicenseType с добавлением возможных значений.</span><span class="sxs-lookup"><span data-stu-id="71c25-1512">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="71c25-1513">Исправлена проблема с неправильным обновлением удостоверения управляемого экземпляра, если оно было единственным обновляемым свойством.</span><span class="sxs-lookup"><span data-stu-id="71c25-1513">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="71c25-1514">Поддержка пользовательских параметров сортировки в управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="71c25-1514">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="71c25-1515">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="71c25-1515">Az.Storage</span></span>
* <span data-ttu-id="71c25-1516">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="71c25-1516">Update incorrect online help URLs</span></span>
* <span data-ttu-id="71c25-1517">Добавлен вывод подробных сообщений об ошибке при получении или установке классических свойств ведения журнала или метрик в учетной записи хранилища класса Premium, так как учетная запись хранилища класса Premium не поддерживает классические функции ведения журнала и метрик.</span><span class="sxs-lookup"><span data-stu-id="71c25-1517">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="71c25-1518">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="71c25-1518">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="71c25-1519">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="71c25-1519">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="71c25-1520">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="71c25-1520">Az.TrafficManager</span></span>
* <span data-ttu-id="71c25-1521">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="71c25-1521">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="71c25-1522">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="71c25-1522">Az.Websites</span></span>
* <span data-ttu-id="71c25-1523">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="71c25-1523">Update incorrect online help URLs</span></span>
* <span data-ttu-id="71c25-1524">Исправлена работа командлета New-AzWebAppSSLBinding: сертификат отправляется в правильную группу ресурсов и правильное расположение, если приложение размещено в ASE.</span><span class="sxs-lookup"><span data-stu-id="71c25-1524">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="71c25-1525">Исправлена работа командлета New-AzWebAppSSLBinding: теги не перезаписываются при привязке SSL-сертификата к приложению.</span><span class="sxs-lookup"><span data-stu-id="71c25-1525">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="71c25-1526">1.1.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="71c25-1526">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="71c25-1527">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71c25-1527">Az.Accounts</span></span>
* <span data-ttu-id="71c25-1528">Добавление области "Local" в Enable-AzureRmAlias.</span><span class="sxs-lookup"><span data-stu-id="71c25-1528">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71c25-1529">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71c25-1529">Az.Compute</span></span>
* <span data-ttu-id="71c25-1530">Теперь имя не является обязательным в идентификаторе набора параметров для Restart/Start/Stop/Remove/Set-AzVM и Save-AzVMImage.</span><span class="sxs-lookup"><span data-stu-id="71c25-1530">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="71c25-1531">Обновлено описание идентификатора в файлах справки.</span><span class="sxs-lookup"><span data-stu-id="71c25-1531">Updated the description of ID in help files</span></span>
* <span data-ttu-id="71c25-1532">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="71c25-1532">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="71c25-1533">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="71c25-1533">Az.DataLakeStore</span></span>
* <span data-ttu-id="71c25-1534">Обновление версии пакета SDK для плоскости данных до 1.1.14 для устранения найденных проблем.</span><span class="sxs-lookup"><span data-stu-id="71c25-1534">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="71c25-1535">Исправлена обработка отрицательного времени доступа и времени изменения для getfilestatus и liststatus, исправлен токен отмены для асинхронных методов.</span><span class="sxs-lookup"><span data-stu-id="71c25-1535">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="71c25-1536">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="71c25-1536">Az.EventGrid</span></span>
* <span data-ttu-id="71c25-1537">Обновление для использования API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="71c25-1537">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="71c25-1538">Обновлены указанные ниже командлеты для поддержки нового сценария в API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="71c25-1538">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="71c25-1539">New-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="71c25-1539">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="71c25-1540">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="71c25-1540">Event Time-To-Live,</span></span>
        - <span data-ttu-id="71c25-1541">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="71c25-1541">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="71c25-1542">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="71c25-1542">Dead letter endpoint.</span></span>
    - <span data-ttu-id="71c25-1543">Update-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="71c25-1543">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="71c25-1544">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="71c25-1544">Event Time-To-Live,</span></span>
        - <span data-ttu-id="71c25-1545">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="71c25-1545">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="71c25-1546">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="71c25-1546">Dead letter endpoint.</span></span>
* <span data-ttu-id="71c25-1547">Для параметра EndpointType добавлены новые значения перечисления (storageQueue и hybridConnection) в командлеты New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="71c25-1547">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="71c25-1548">Если ожидается, что создание или обновление подписки на событие повлечет за собой действия со стороны пользователя, выполняемые вручную, отображается предупреждение при создании или обновлении подписки события.</span><span class="sxs-lookup"><span data-stu-id="71c25-1548">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="71c25-1549">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="71c25-1549">Az.IotHub</span></span>
* <span data-ttu-id="71c25-1550">Пакет SDK Центра Интернета вещей обновлен до последней версии.</span><span class="sxs-lookup"><span data-stu-id="71c25-1550">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="71c25-1551">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="71c25-1551">Az.LogicApp</span></span>
* <span data-ttu-id="71c25-1552">Get-AzLogicApp позволяет перечислить все параметры без указанного имени.</span><span class="sxs-lookup"><span data-stu-id="71c25-1552">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="71c25-1553">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71c25-1553">Az.Resources</span></span>
* <span data-ttu-id="71c25-1554">Исправлена проблема с набором параметров при предоставлении параметров "-ODataQuery" и "-ResourceId" для "Get-AzResource".</span><span class="sxs-lookup"><span data-stu-id="71c25-1554">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="71c25-1555">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7875.</span><span class="sxs-lookup"><span data-stu-id="71c25-1555">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="71c25-1556">Исправлена обработка параметра -Custom в New/Set-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="71c25-1556">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="71c25-1557">Исправлена опечатка в документации по New-AzDeployment.</span><span class="sxs-lookup"><span data-stu-id="71c25-1557">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="71c25-1558">Параметр "-MailNickname" стал обязательным для "New-AzADUser".</span><span class="sxs-lookup"><span data-stu-id="71c25-1558">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="71c25-1559">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8220.</span><span class="sxs-lookup"><span data-stu-id="71c25-1559">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="71c25-1560">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="71c25-1560">Az.SignalR</span></span>
* <span data-ttu-id="71c25-1561">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="71c25-1561">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="71c25-1562">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71c25-1562">Az.Sql</span></span>
* <span data-ttu-id="71c25-1563">Зависимость клиента управления хранением преобразована для общей реализации в пакете SDK.</span><span class="sxs-lookup"><span data-stu-id="71c25-1563">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="71c25-1564">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="71c25-1564">Az.Storage</span></span>
* <span data-ttu-id="71c25-1565">Установка параметра StorageAccountName для контекста хранилища в качестве реального имени учетной записи хранения, если она была создана с использованием токена Sas, OAuth или анонимного доступа.</span><span class="sxs-lookup"><span data-stu-id="71c25-1565">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="71c25-1566">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="71c25-1566">New-AzStorageContext</span></span>
* <span data-ttu-id="71c25-1567">Создание токена Sas большого двоичного объекта моментального снимка с параметром "-FullUri". Возвращаемый URI исправлен на URI моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="71c25-1567">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="71c25-1568">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="71c25-1568">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="71c25-1569">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="71c25-1569">Az.Websites</span></span>
* <span data-ttu-id="71c25-1570">Исправлена ошибка синтаксического анализа даты в "Get-AzDeletedWebApp".</span><span class="sxs-lookup"><span data-stu-id="71c25-1570">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="71c25-1571">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="71c25-1571">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="71c25-1572">1.0.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="71c25-1572">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="71c25-1573">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="71c25-1573">General</span></span>

- <span data-ttu-id="71c25-1574">Общедоступная версия модуля Az.</span><span class="sxs-lookup"><span data-stu-id="71c25-1574">General Availability of Az Module</span></span>
- <span data-ttu-id="71c25-1575">Справка в Интернете для каждого модуля.</span><span class="sxs-lookup"><span data-stu-id="71c25-1575">Online help for each module</span></span>
- <span data-ttu-id="71c25-1576">Дополнительные сведения и стратегию развития см. в статье [Announcing New Module 'Az'](https://aka.ms/azps-announce) (Объявление о новом модуле Az)</span><span class="sxs-lookup"><span data-stu-id="71c25-1576">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="71c25-1577">Сведения о миграции с AzureRM см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="71c25-1577">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="71c25-1578">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="71c25-1578">Az.Accounts</span></span>
- <span data-ttu-id="71c25-1579">Изменено с Az.Profile.</span><span class="sxs-lookup"><span data-stu-id="71c25-1579">Changed from Az.Profile</span></span>
- <span data-ttu-id="71c25-1580">Исправлены форматы таблиц для типов профиля и контекста.</span><span class="sxs-lookup"><span data-stu-id="71c25-1580">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="71c25-1581">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="71c25-1581">Az.ApiManagement</span></span>
- <span data-ttu-id="71c25-1582">Исправления для #7002.</span><span class="sxs-lookup"><span data-stu-id="71c25-1582">Fixes for #7002</span></span>
- <span data-ttu-id="71c25-1583">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="71c25-1583">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="71c25-1584">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="71c25-1584">Az.Batch</span></span>
- <span data-ttu-id="71c25-1585">Добавлена возможность видеть, какая версия агента узла пакетной службы Azure работает в пуле на каждой виртуальной машине, с помощью нового свойства `NodeAgentInformation` в `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="71c25-1585">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="71c25-1586">Значение `Caching` по умолчанию для `PSDataDisk` теперь `ReadWrite` вместо `None`.</span><span class="sxs-lookup"><span data-stu-id="71c25-1586">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="71c25-1587">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="71c25-1587">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="71c25-1588">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="71c25-1588">Az.Billing</span></span>
- <span data-ttu-id="71c25-1589">Объединены командлеты Billing, Consumption и UsageAggregates. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0).</span><span class="sxs-lookup"><span data-stu-id="71c25-1589">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="71c25-1590">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="71c25-1590">Az.CognitivServices</span></span>
- <span data-ttu-id="71c25-1591">Добавлены средства заполнения для SkuName и Typem, доступные в операции New-AzureRmCognitiveServicesAccount.</span><span class="sxs-lookup"><span data-stu-id="71c25-1591">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="71c25-1592">Удален набор параметров GetSkusWithAccountParamSetName из Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="71c25-1592">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="71c25-1593">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="71c25-1593">Az.ContainerInstance</span></span>
- <span data-ttu-id="71c25-1594">Добавлена поддержка ManagedIdentity.</span><span class="sxs-lookup"><span data-stu-id="71c25-1594">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="71c25-1595">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="71c25-1595">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="71c25-1596">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="71c25-1596">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="71c25-1597">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="71c25-1597">Az.DataLakeStore</span></span>
- <span data-ttu-id="71c25-1598">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="71c25-1598">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="71c25-1599">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="71c25-1599">Az.Monitor</span></span>
- <span data-ttu-id="71c25-1600">"Az.Insights" переименован в "Az.Monitor" и внесены другие незначительные критические изменения. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="71c25-1600">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="71c25-1601">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="71c25-1601">Az.KeyVault</span></span>
- <span data-ttu-id="71c25-1602">Из типов вывода удалено устаревшее свойство PurgeDisabled</span><span class="sxs-lookup"><span data-stu-id="71c25-1602">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="71c25-1603">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="71c25-1603">Az.MachineLearning</span></span>
- <span data-ttu-id="71c25-1604">Включены командлеты из модуля Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="71c25-1604">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="71c25-1605">Az.Media</span><span class="sxs-lookup"><span data-stu-id="71c25-1605">Az.Media</span></span>
- <span data-ttu-id="71c25-1606">Удаляет устаревший псевдоним Tags из New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="71c25-1606">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="71c25-1607">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71c25-1607">Az.Network</span></span>
<span data-ttu-id="71c25-1608">В шлюз приложений добавлена поддержка настройки RewriteRuleSets</span><span class="sxs-lookup"><span data-stu-id="71c25-1608">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="71c25-1609">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="71c25-1609">New cmdlets added:</span></span>
        - <span data-ttu-id="71c25-1610">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="71c25-1610">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="71c25-1611">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="71c25-1611">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="71c25-1612">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="71c25-1612">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="71c25-1613">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="71c25-1613">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="71c25-1614">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="71c25-1614">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="71c25-1615">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="71c25-1615">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="71c25-1616">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="71c25-1616">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="71c25-1617">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="71c25-1617">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="71c25-1618">В следующие командлеты добавлен необязательный параметр -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="71c25-1618">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="71c25-1619">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="71c25-1619">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="71c25-1620">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="71c25-1620">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="71c25-1621">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="71c25-1621">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="71c25-1622">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="71c25-1622">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="71c25-1623">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="71c25-1623">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="71c25-1624">New-AzureRmApplicationGatewayUrlPathMapConfig добавил с помощью идентификатора поддержку KeyVault для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="71c25-1624">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="71c25-1625">В следующие командлеты добавлен необязательный параметр -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="71c25-1625">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="71c25-1626">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="71c25-1626">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="71c25-1627">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="71c25-1627">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="71c25-1628">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="71c25-1628">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="71c25-1629">В командлет New-AzApplicationGateway добавлен необязательный параметр -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="71c25-1629">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="71c25-1630">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="71c25-1630">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="71c25-1631">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="71c25-1631">Az.OperationalInsights</span></span>
- <span data-ttu-id="71c25-1632">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="71c25-1632">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="71c25-1633">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="71c25-1633">Az.Profile</span></span>
- <span data-ttu-id="71c25-1634">Имя модуля изменено на Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="71c25-1634">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="71c25-1635">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="71c25-1635">Az.RecoveryServices</span></span>
- <span data-ttu-id="71c25-1636">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="71c25-1636">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="71c25-1637">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71c25-1637">Az.Resources</span></span>
- <span data-ttu-id="71c25-1638">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="71c25-1638">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="71c25-1639">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="71c25-1639">Az.ServiceFabric</span></span>
- <span data-ttu-id="71c25-1640">Поддержка спецификации сертификата по общему имени и отпечатку</span><span class="sxs-lookup"><span data-stu-id="71c25-1640">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="71c25-1641">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="71c25-1641">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="71c25-1642">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="71c25-1642">Az.SIgnalR</span></span>
- <span data-ttu-id="71c25-1643">Общедоступная версия командлетов PowerShell для SIgnalR</span><span class="sxs-lookup"><span data-stu-id="71c25-1643">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="71c25-1644">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71c25-1644">Az.Sql</span></span>
- <span data-ttu-id="71c25-1645">Добавлены новые типы обнаружения Data_Exfiltration и Unsafe_Action в командлеты обнаружения угроз</span><span class="sxs-lookup"><span data-stu-id="71c25-1645">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="71c25-1646">Примеры обновленной документации для командлетов аудита Sql</span><span class="sxs-lookup"><span data-stu-id="71c25-1646">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="71c25-1647">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="71c25-1647">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="71c25-1648">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="71c25-1648">Az.Storage</span></span>
- <span data-ttu-id="71c25-1649">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="71c25-1649">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="71c25-1650">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="71c25-1650">Az.Websites</span></span>
- <span data-ttu-id="71c25-1651">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="71c25-1651">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="71c25-1652">0.7.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="71c25-1652">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="71c25-1653">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="71c25-1653">General</span></span>

* <span data-ttu-id="71c25-1654">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="71c25-1654">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="71c25-1655">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71c25-1655">Az.Compute</span></span>

* <span data-ttu-id="71c25-1656">Добавлена поддержка UltraSSD и образов коллекции в простых наборах параметров для командлетов `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="71c25-1656">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="71c25-1657">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="71c25-1657">Az.DataLakeStore</span></span>

* <span data-ttu-id="71c25-1658">Исправлено косую черту в конце домена учетной записи ADLS</span><span class="sxs-lookup"><span data-stu-id="71c25-1658">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="71c25-1659">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="71c25-1659">Az.FrontDoor</span></span>

* <span data-ttu-id="71c25-1660">Исправлены некоторые неработающие ссылки</span><span class="sxs-lookup"><span data-stu-id="71c25-1660">Fixed some broken links</span></span>
    - <span data-ttu-id="71c25-1661">В статьях New-AzureRmFrontDoor и Set-AzureRmFrontDoor исправлена ссылка на статью командлета New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="71c25-1661">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="71c25-1662">В статье New-AzureRmFrontDoorManagedRuleObject исправлена ссылка на статью командлета New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="71c25-1662">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="71c25-1663">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="71c25-1663">Az.RecoveryServices</span></span>

* <span data-ttu-id="71c25-1664">Добавлены проверки на стороне клиента для операций восстановления общей папки Azure.</span><span class="sxs-lookup"><span data-stu-id="71c25-1664">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="71c25-1665">StorageAccountName и storageAccountResourceGroupName являются необязательными для восстановления afs.</span><span class="sxs-lookup"><span data-stu-id="71c25-1665">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="71c25-1666">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71c25-1666">Az.Resources</span></span>

* <span data-ttu-id="71c25-1667">Исправление для https://github.com/Azure/azure-powershell/issues/7679.</span><span class="sxs-lookup"><span data-stu-id="71c25-1667">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="71c25-1668">Обновите Get-AzureRmRoleAssignment, чтобы использовать область подписки, если она указана при запросе классических администраторов.</span><span class="sxs-lookup"><span data-stu-id="71c25-1668">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="71c25-1669">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71c25-1669">Az.Sql</span></span>

* <span data-ttu-id="71c25-1670">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="71c25-1670">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="71c25-1671">Устранена проблема с использованием Get-AzureRmSqlDatabaseVulnerabilityAssessment с .NET Core.</span><span class="sxs-lookup"><span data-stu-id="71c25-1671">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="71c25-1672">Изменена документация справочных сообщений, связанных с командлетами аудита SQL.</span><span class="sxs-lookup"><span data-stu-id="71c25-1672">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="71c25-1673">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="71c25-1673">Az.Storage</span></span>

* <span data-ttu-id="71c25-1674">Добавлено -EnableHierarchicalNamespace к New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="71c25-1674">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="71c25-1675">Устранена проблема, из-за которой командлет Copy File не может повторно использовать исходный контекст в пункте назначения, если не введен -DestContext</span><span class="sxs-lookup"><span data-stu-id="71c25-1675">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="71c25-1676">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="71c25-1676">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="71c25-1677">Поддержка статической конфигурации сайта</span><span class="sxs-lookup"><span data-stu-id="71c25-1677">Support Static Website configuration</span></span>
    - <span data-ttu-id="71c25-1678">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="71c25-1678">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="71c25-1679">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="71c25-1679">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="71c25-1680">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="71c25-1680">Az.Websites</span></span>

* <span data-ttu-id="71c25-1681">Set-AzureRmWebApp и Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="71c25-1681">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="71c25-1682">Добавлен новый параметр (-AzureStoragePath), который указывает путь службы хранилища Azure для подключения в приложениях-контейнерах Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="71c25-1682">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="71c25-1683">Используйте выходные данные нового командлета New-AzureRmWebAppAzureStoragePath в качестве параметра, чтобы задать пути к службе хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="71c25-1683">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="71c25-1684">0.6.1 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="71c25-1684">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="71c25-1685">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="71c25-1685">Az.ApiManagement</span></span>
* <span data-ttu-id="71c25-1686">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="71c25-1686">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="71c25-1687">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="71c25-1687">Az.Automation</span></span>
* <span data-ttu-id="71c25-1688">Командлеты службы автоматизации Azure на базе Swagger.</span><span class="sxs-lookup"><span data-stu-id="71c25-1688">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="71c25-1689">Добавлены командлеты для Управления обновлениями.</span><span class="sxs-lookup"><span data-stu-id="71c25-1689">Added Update Management cmdlets</span></span>
* <span data-ttu-id="71c25-1690">Добавлены командлеты для системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="71c25-1690">Added Source Control cmdlets</span></span>
* <span data-ttu-id="71c25-1691">Добавлен командлет Remove-AzureRmAutomationHybridWorkerGroup.</span><span class="sxs-lookup"><span data-stu-id="71c25-1691">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="71c25-1692">Исправлена команда DSC для регистрации узла.</span><span class="sxs-lookup"><span data-stu-id="71c25-1692">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="71c25-1693">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71c25-1693">Az.Compute</span></span>
* <span data-ttu-id="71c25-1694">Исправлена проблема с удостоверением, назначаемым системой.</span><span class="sxs-lookup"><span data-stu-id="71c25-1694">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="71c25-1695">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="71c25-1695">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="71c25-1696">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="71c25-1696">Az.ContainerInstance</span></span>
* <span data-ttu-id="71c25-1697">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="71c25-1697">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="71c25-1698">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="71c25-1698">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="71c25-1699">Обновлено описание в примерах командлетов для Marketplace.</span><span class="sxs-lookup"><span data-stu-id="71c25-1699">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="71c25-1700">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71c25-1700">Az.Network</span></span>
* <span data-ttu-id="71c25-1701">Добавлены командлеты New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="71c25-1701">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="71c25-1702">Протокол ICMP возвращен в список поддерживаемых сетевых протоколов Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="71c25-1702">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="71c25-1703">Обновлен командлет Test-AzureRmNetworkWatcherConnectivity, в который добавлена проверка идентификатора, адреса и порта целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="71c25-1703">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="71c25-1704">Исправлены проблемы с использованием памяти в карте виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="71c25-1704">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="71c25-1705">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="71c25-1705">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="71c25-1706">Внесено исправление для изменения политики, применяемой к защищенному общему файловому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="71c25-1706">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="71c25-1707">Параметры часового пояса преобразованы в верхний регистр.</span><span class="sxs-lookup"><span data-stu-id="71c25-1707">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="71c25-1708">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="71c25-1708">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="71c25-1709">Исправлен пример командлета New-AzureRmRecoveryServicesAsrProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="71c25-1709">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="71c25-1710">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="71c25-1710">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="71c25-1711">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="71c25-1711">Az.Relay</span></span>
* <span data-ttu-id="71c25-1712">Для командлета New-AzureRmRelayKey добавлен необязательный параметр -KeyValue, который позволяет пользователю указать значение ключа.</span><span class="sxs-lookup"><span data-stu-id="71c25-1712">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="71c25-1713">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71c25-1713">Az.Resources</span></span>
* <span data-ttu-id="71c25-1714">Обновлена справочная документация для параметров, связанных с удостоверением ресурса, в `New-AzureRmPolicyAssignment` и `Set-AzureRmPolicyAssignment`.</span><span class="sxs-lookup"><span data-stu-id="71c25-1714">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="71c25-1715">Добавлен пример командлета New-AzureRmPolicyDefinition, в котором используется параметр -Metadata.</span><span class="sxs-lookup"><span data-stu-id="71c25-1715">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="71c25-1716">Реализовано исправление, позволяющее сохранять регистр в ключах тегов NetStandard: #7678, #7703.</span><span class="sxs-lookup"><span data-stu-id="71c25-1716">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="71c25-1717">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="71c25-1717">Az.ServiceFabric</span></span>
* <span data-ttu-id="71c25-1718">Добавлены сообщения о нерекомендуемых компонентах для предстоящего выпуска критических изменений.</span><span class="sxs-lookup"><span data-stu-id="71c25-1718">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="71c25-1719">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71c25-1719">Az.Sql</span></span>
* <span data-ttu-id="71c25-1720">Добавлены новые командлеты для операций создания, просмотра, изменения и удаления в Управляемом экземпляре Базы данных SQL и Управляемой базе данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="71c25-1720">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="71c25-1721">Get-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="71c25-1721">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="71c25-1722">New-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="71c25-1722">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="71c25-1723">Set-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="71c25-1723">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="71c25-1724">Remove-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="71c25-1724">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="71c25-1725">Get-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="71c25-1725">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="71c25-1726">New-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="71c25-1726">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="71c25-1727">Restore-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="71c25-1727">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="71c25-1728">Remove-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="71c25-1728">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="71c25-1729">Добавлено расширенное управление политиками аудита для сервера или базы данных.</span><span class="sxs-lookup"><span data-stu-id="71c25-1729">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="71c25-1730">Добавлен новый параметр (PredicateExpression) для фильтрации журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="71c25-1730">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="71c25-1731">Внесены изменения в командлеты для использования клиентов SQL вместо устаревших клиентов.</span><span class="sxs-lookup"><span data-stu-id="71c25-1731">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="71c25-1732">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="71c25-1732">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="71c25-1733">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="71c25-1733">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="71c25-1734">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="71c25-1734">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="71c25-1735">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="71c25-1735">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="71c25-1736">Исправлена проблема с использованием командлета Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings с набором параметров, содержащим имена учетных записей хранения.</span><span class="sxs-lookup"><span data-stu-id="71c25-1736">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="71c25-1737">0.5.0 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="71c25-1737">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="71c25-1738">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="71c25-1738">General</span></span>
* <span data-ttu-id="71c25-1739">Добавлены средства заполнения ресурсов для многих основных командлетов — они позволяют вам переключать существующие имена ресурсов при вызове командлетов в интерактивном режиме</span><span class="sxs-lookup"><span data-stu-id="71c25-1739">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="71c25-1740">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="71c25-1740">Az.Profile</span></span>
* <span data-ttu-id="71c25-1741">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="71c25-1741">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="71c25-1742">В командлете Connect-AzAccount параметр TenantId переименован в Tenant и добавлен псевдоним для TenantId</span><span class="sxs-lookup"><span data-stu-id="71c25-1742">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="71c25-1743">Обновлено описание TenantId для командлета Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="71c25-1743">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="71c25-1744">Исправлено сообщение об ошибке при неудачной попытке входа в процессе предоставления домена клиента.</span><span class="sxs-lookup"><span data-stu-id="71c25-1744">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="71c25-1745">Устранена проблема с конфликтом имен контекста в учетных записях без подписок в клиенте.</span><span class="sxs-lookup"><span data-stu-id="71c25-1745">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="71c25-1746">Устранена проблема с конечными точками DataLake при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="71c25-1746">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="71c25-1747">Устранена проблема, при которой командлет Disconnect-AzAccount вызывал сбой при отсутствии подключения</span><span class="sxs-lookup"><span data-stu-id="71c25-1747">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="71c25-1748">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="71c25-1748">Az.CognitiveServices</span></span>
* <span data-ttu-id="71c25-1749">Добавлена операция Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="71c25-1749">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71c25-1750">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71c25-1750">Az.Compute</span></span>
* <span data-ttu-id="71c25-1751">Добавлены командлеты Add-AzVmssVMDataDisk и Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="71c25-1751">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="71c25-1752">Get-AzVMImage отображает AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="71c25-1752">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="71c25-1753">Устранена проблема, при которой значения параметров SetAzVMChefExtension -BootstrapOptions и -JsonAttribute нельзя было указать в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="71c25-1753">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="71c25-1754">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="71c25-1754">Az.DataLakeStore</span></span>
* <span data-ttu-id="71c25-1755">Обновлен пакет DataLake до версии 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="71c25-1755">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="71c25-1756">Параметр по умолчанию Concurrency добавлен к многопоточным операциям.</span><span class="sxs-lookup"><span data-stu-id="71c25-1756">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="71c25-1757">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="71c25-1757">Az.Insights</span></span>
* <span data-ttu-id="71c25-1758">Исправлена проблема № 7267 (область автомасштабирования).</span><span class="sxs-lookup"><span data-stu-id="71c25-1758">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="71c25-1759">Устранена проблема с созданием правила автомасштабирования, при которой перечисленные параметры не были указаны должным образом (выбор значений по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="71c25-1759">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="71c25-1760">Исправлена проблема № 7513 [Insights], при которой для командлета Set-AzDiagnosticSetting требовалось явное указание категорий во время создания параметра</span><span class="sxs-lookup"><span data-stu-id="71c25-1760">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="71c25-1761">Теперь явное указание категорий во время создания не требуется, и командлет выполняется надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="71c25-1761">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71c25-1762">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71c25-1762">Az.Network</span></span>
* <span data-ttu-id="71c25-1763">Параметр PeeringType является обязательным для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="71c25-1763">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="71c25-1764">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="71c25-1764">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="71c25-1765">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="71c25-1765">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="71c25-1766">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="71c25-1766">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="71c25-1767">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="71c25-1767">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="71c25-1768">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="71c25-1768">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="71c25-1769">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="71c25-1769">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="71c25-1770">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="71c25-1770">Az.PolicyInsights</span></span>
* <span data-ttu-id="71c25-1771">Добавлена политика исправления командлетов.</span><span class="sxs-lookup"><span data-stu-id="71c25-1771">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="71c25-1772">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71c25-1772">Az.Resources</span></span>
* <span data-ttu-id="71c25-1773">Исправление для https://github.com/Azure/azure-powershell/issues/7402.</span><span class="sxs-lookup"><span data-stu-id="71c25-1773">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="71c25-1774">Разрешено перечисление ресурсов с помощью параметра -ResourceId для командлета Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="71c25-1774">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="71c25-1775">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="71c25-1775">Az.ServiceBus</span></span>
* <span data-ttu-id="71c25-1776">Добавлено свойство только для чтения MigrationState в PSServiceBusMigrationConfigurationAttributes, которое позволяет узнать состояние Migration.</span><span class="sxs-lookup"><span data-stu-id="71c25-1776">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="71c25-1777">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="71c25-1777">Az.ServiceFabric</span></span>
* <span data-ttu-id="71c25-1778">Устранена проблема с добавлением сертификата в VMSS Linux.</span><span class="sxs-lookup"><span data-stu-id="71c25-1778">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="71c25-1779">Исправлен командлет Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="71c25-1779">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="71c25-1780">Используется правильный отпечаток нового сертификата (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="71c25-1780">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="71c25-1781">Исключение отображается правильно (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="71c25-1781">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="71c25-1782">Исправлен командлет Update-AzServiceFabricDurability для обновления конфигурации кластера перед началом операции CreateOrUpdate для масштабируемого набора виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="71c25-1782">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="71c25-1783">0.4.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="71c25-1783">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="71c25-1784">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="71c25-1784">Az.Profile</span></span>
* <span data-ttu-id="71c25-1785">Устранена проблема с Get-AzSubscription в CloudShell</span><span class="sxs-lookup"><span data-stu-id="71c25-1785">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="71c25-1786">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="71c25-1786">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71c25-1787">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71c25-1787">Az.Compute</span></span>
* <span data-ttu-id="71c25-1788">В список разрешений добавлены новые размеры виртуальных машин, для которых будет включено ускорение работы в сети при использовании простого набора параметров для New-AzVm</span><span class="sxs-lookup"><span data-stu-id="71c25-1788">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="71c25-1789">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="71c25-1789">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="71c25-1790">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="71c25-1790">Az.DataLakeStore</span></span>
* <span data-ttu-id="71c25-1791">Добавлена поддержка правил виртуальной сети:</span><span class="sxs-lookup"><span data-stu-id="71c25-1791">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="71c25-1792">Get-AzDataLakeStoreVirtualNetworkRule: получение или отображение правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="71c25-1792">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="71c25-1793">Add-AzDataLakeStoreVirtualNetworkRule: добавление правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="71c25-1793">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="71c25-1794">Set-AzDataLakeStoreVirtualNetworkRule: изменение указанного правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="71c25-1794">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="71c25-1795">Remove-AzDataLakeStoreVirtualNetworkRule: удаление правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="71c25-1795">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71c25-1796">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71c25-1796">Az.Network</span></span>
* <span data-ttu-id="71c25-1797">Обновлен командлет Test-AzNetworkWatcherConnectivity. Теперь он позволяет передать значение протокола в серверную часть.</span><span class="sxs-lookup"><span data-stu-id="71c25-1797">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="71c25-1798">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="71c25-1798">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="71c25-1799">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71c25-1799">Az.Resources</span></span>
* <span data-ttu-id="71c25-1800">Устранена проблема, из-за которой командлет Get-AzRoleDefinition возвращал непонятное исключение (если профиль по умолчанию не содержал подписки и область не была указана), благодаря добавлению понятного исключения в сценарий.</span><span class="sxs-lookup"><span data-stu-id="71c25-1800">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="71c25-1801">Также для набора параметров по умолчанию задано значение RoleDefinitionNameParameterSet.</span><span class="sxs-lookup"><span data-stu-id="71c25-1801">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="71c25-1802">0.3.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="71c25-1802">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="71c25-1803">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="71c25-1803">Azure.Storage</span></span>
* <span data-ttu-id="71c25-1804">Исправлена ошибка, из-за которой при копировании файла или большого двоичного объекта метаданные не копировались, если в целевом устройстве имелась проблема с метаданными.</span><span class="sxs-lookup"><span data-stu-id="71c25-1804">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="71c25-1805">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="71c25-1805">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="71c25-1806">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="71c25-1806">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="71c25-1807">Добавлена поддержка получения сведения об использовании ресурса хранилища для конкретного расположения. Также добавлено предупреждающее сообщение о том, что функция получения глобальных сведений об использовании ресурса хранилища устарела.</span><span class="sxs-lookup"><span data-stu-id="71c25-1807">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="71c25-1808">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="71c25-1808">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="71c25-1809">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="71c25-1809">Az.CognitiveServices</span></span>
* <span data-ttu-id="71c25-1810">Поддержка Get-AzCognitiveServicesAccountSkus без существующей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="71c25-1810">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="71c25-1811">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="71c25-1811">Az.Compute</span></span>
* <span data-ttu-id="71c25-1812">Исправлена команда Get-AzVM -ResourceGroupName <rg>, которая теперь может возвращать более 50 результатов</span><span class="sxs-lookup"><span data-stu-id="71c25-1812">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="71c25-1813">Добавлен пример использования SimpleParameterSet в справку командлета New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="71c25-1813">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="71c25-1814">Исправлена ошибка в сообщении о ходе выполнения для шифрования дисков Azure.</span><span class="sxs-lookup"><span data-stu-id="71c25-1814">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="71c25-1815">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="71c25-1815">Az.DataFactoryV2</span></span>
* <span data-ttu-id="71c25-1816">Пакет .NET SDK для ADF обновлен до версии 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="71c25-1816">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="71c25-1817">Az.Network</span><span class="sxs-lookup"><span data-stu-id="71c25-1817">Az.Network</span></span>
* <span data-ttu-id="71c25-1818">Добавлена функциональность NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="71c25-1818">Added NetworkProfile functionality.</span></span> <span data-ttu-id="71c25-1819">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="71c25-1819">new cmdlets added</span></span>
    - <span data-ttu-id="71c25-1820">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="71c25-1820">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="71c25-1821">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="71c25-1821">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="71c25-1822">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="71c25-1822">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="71c25-1823">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="71c25-1823">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="71c25-1824">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="71c25-1824">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="71c25-1825">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="71c25-1825">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="71c25-1826">Добавлен канал связи служб в модель подсети.</span><span class="sxs-lookup"><span data-stu-id="71c25-1826">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="71c25-1827">Добавлены командлеты: New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="71c25-1827">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="71c25-1828">Добавлены командлеты: Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="71c25-1828">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="71c25-1829">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="71c25-1829">Az.RedisCache</span></span>
* <span data-ttu-id="71c25-1830">С этого момента добавлена поддержка любой строки в качестве параметра Size.</span><span class="sxs-lookup"><span data-stu-id="71c25-1830">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="71c25-1831">Добавлено значение P5 во всплывающее окно PSArgumentCompleter.</span><span class="sxs-lookup"><span data-stu-id="71c25-1831">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="71c25-1832">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="71c25-1832">Az.Resources</span></span>
* <span data-ttu-id="71c25-1833">Добавлен отсутствующий параметр -Mode в командлет Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="71c25-1833">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="71c25-1834">Исправлена ошибка командлета Get-AzProviderOperation для операций, когда Origin содержит User</span><span class="sxs-lookup"><span data-stu-id="71c25-1834">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="71c25-1835">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="71c25-1835">Az.Sql</span></span>
* <span data-ttu-id="71c25-1836">Исправлена ошибка, при которой некоторые командлеты резервного копирования не распознавали текущую подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="71c25-1836">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="71c25-1837">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="71c25-1837">Az.Websites</span></span>
* <span data-ttu-id="71c25-1838">Новый командлет Get-AzWebAppContainerContinuousDeploymentUrl, который позволяет получить URL-адрес веб-перехватчика для развертывания контейнера</span><span class="sxs-lookup"><span data-stu-id="71c25-1838">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="71c25-1839">Новые командлеты New-AzWebAppContainerPSSession и Enter-WebAppContainerPSSession, которые позволяют инициировать удаленный сеанс PowerShell в приложении-контейнере Windows</span><span class="sxs-lookup"><span data-stu-id="71c25-1839">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="71c25-1840">0.2.0 — сентябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="71c25-1840">0.2.0 - September 2018</span></span>
 <span data-ttu-id="71c25-1841">Первый выпуск</span><span class="sxs-lookup"><span data-stu-id="71c25-1841">Initial Release</span></span>
