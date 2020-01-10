---
title: Заметки о выпуске Azure PowerShell
description: Узнайте обо всех последних обновлениях модулей Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/15/2019
ms.openlocfilehash: fb934ed0f8bef5e2aff715debe5d406d54abf24f
ms.sourcegitcommit: 2d0c3ffaa5246f680784fa7e15b0d2536c27ff80
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2020
ms.locfileid: "75718990"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="7cf4c-103">Заметки о выпуске Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="7cf4c-103">Azure PowerShell release notes</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="7cf4c-104">3.3.0 — январь 2020 г.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-104">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7cf4c-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7cf4c-105">Az.Accounts</span></span>
* <span data-ttu-id="7cf4c-106">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment: теперь они принимают параметры AzureAttestationServiceEndpointResourceId и AzureAttestationServiceEndpointSuffix.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-106">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="7cf4c-107">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7cf4c-107">Az.Cdn</span></span>
* <span data-ttu-id="7cf4c-108">Теперь в командлете New-AzCdnEndpoint отображаются сведения сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-108">Display error response deatil in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7cf4c-109">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7cf4c-109">Az.Compute</span></span>
* <span data-ttu-id="7cf4c-110">Командлет Set-AzVMCustomScriptExtension исправлен для виртуальной машины с управляемым диском ОС без профиля ОС.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-110">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="7cf4c-111">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="7cf4c-111">Az.ContainerInstance</span></span>
* <span data-ttu-id="7cf4c-112">Исправлены имена параметров, используемые в примере командлета New-AzContainerGroup.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-112">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="7cf4c-113">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="7cf4c-113">Az.DataBoxEdge</span></span>
* <span data-ttu-id="7cf4c-114">Добавлен командлет Get-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-114">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="7cf4c-115">получение контейнера хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-115">Get the Edge Stroage Container</span></span>
* <span data-ttu-id="7cf4c-116">Добавлен командлет New-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-116">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="7cf4c-117">создание контейнера хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-117">Create new Edge Stroage Container</span></span>
* <span data-ttu-id="7cf4c-118">Добавлен командлет Remove-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-118">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="7cf4c-119">удаление контейнера хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-119">Remove the Edge Stroage Container</span></span>
* <span data-ttu-id="7cf4c-120">Добавлен командлет Invoke-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-120">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="7cf4c-121">вызов действия для обновления данных в контейнере хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-121">Invoke action to refresh data on Edge Stroage Container</span></span>
* <span data-ttu-id="7cf4c-122">Добавлен командлет Get-AzDataBoxEdgeStorageAccount:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-122">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="7cf4c-123">получение учетной записи хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-123">Get the Edge Stroage Account</span></span>
* <span data-ttu-id="7cf4c-124">Добавлен командлет New-AzDataBoxEdgeStorageAccount:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-124">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="7cf4c-125">создание учетной записи хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-125">Create new Edge Stroage Account</span></span>
* <span data-ttu-id="7cf4c-126">Добавлен командлет Remove-AzDataBoxEdgeStorageAccount:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-126">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="7cf4c-127">удаление учетной записи хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-127">Remove the Edge Stroage Account</span></span>
* <span data-ttu-id="7cf4c-128">Вызов командлета Invoke-AzDataBoxEdgeShare:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-128">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="7cf4c-129">вызов действия для обновления данных в общей папке.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-129">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="7cf4c-130">Добавлен командлет Set-AzDataBoxEdgeStorageAccountCredential:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-130">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="7cf4c-131">установка учетных данных для учетной записи хранилища Azure Data Box Edge.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-131">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7cf4c-132">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7cf4c-132">Az.DataFactory</span></span>
* <span data-ttu-id="7cf4c-133">Добавлены свойства AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId и VersionStatus для командлета Get-AzDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-133">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="7cf4c-134">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.6.0.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-134">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="7cf4c-135">Для командлета Set-AzureRmDataFactoryV2IntegrationRuntime добавлен параметр PublicIPs, позволяющий включить создание среды Azure-SSIS IR со статическими общедоступными IP-адресами.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-135">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="7cf4c-136">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="7cf4c-136">Az.DevTestLabs</span></span>
* <span data-ttu-id="7cf4c-137">Удалена недействительная ссылка в файле Get-AzDtlAllowedVMSizesPolicy.md.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-137">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7cf4c-138">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7cf4c-138">Az.EventHub</span></span>
* <span data-ttu-id="7cf4c-139">Устранена проблема № 10634: исправлена ссылка на пустой объект для удаления пространства имен концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-139">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="7cf4c-140">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="7cf4c-140">Az.HDInsight</span></span>
* <span data-ttu-id="7cf4c-141">Устранена ошибка в файле Invoke-AzHDInsightHiveJob.md.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-141">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="7cf4c-142">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="7cf4c-142">Az.MachineLearning</span></span>
* <span data-ttu-id="7cf4c-143">Вычислительная среда Машинного обучения больше недоступна, поэтому удалены следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-143">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="7cf4c-144">Get-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="7cf4c-144">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="7cf4c-145">Get-AzMlOpClusterKey;</span><span class="sxs-lookup"><span data-stu-id="7cf4c-145">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="7cf4c-146">New-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="7cf4c-146">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="7cf4c-147">Remove-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="7cf4c-147">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="7cf4c-148">Set-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="7cf4c-148">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="7cf4c-149">Test-AzMlOpClusterSystemServicesUpdateAvailability;</span><span class="sxs-lookup"><span data-stu-id="7cf4c-149">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="7cf4c-150">Update-AzMlOpClusterSystemService.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-150">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7cf4c-151">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7cf4c-151">Az.Network</span></span>
* <span data-ttu-id="7cf4c-152">Обновлена зависимость Microsoft.Azure.Management.Sql от предварительной версии 1.36 до предварительной версии 1.37.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-152">Upgrade dependancy of Microsoft.Azure.Management.Sql from 1.36-preivew to 1.37-preivew</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7cf4c-153">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7cf4c-153">Az.RecoveryServices</span></span>
* <span data-ttu-id="7cf4c-154">Добавлена поддержка Azure Site Recovery для виртуальных машин с управляемым диском, зашифрованных при хранении с помощью управляемых клиентом ключей, при восстановлении из Azure в поставщике Azure.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-154">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed leys for Azure to Azure provider.</span></span>
* <span data-ttu-id="7cf4c-155">Добавлена поддержка Azure Site Recovery для необязательного ввода идентификатора набора шифрования диска при включении защиты в рамках восстановления из VMware в Azure.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-155">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="7cf4c-156">Добавлена поддержка Azure Site Recovery для необязательного ввода идентификатора набора шифрования диска на уровне диска при включении защиты в рамках восстановления из VMware в Azure.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-156">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="7cf4c-157">Добавлена поддержка Azure Site Recovery для обновления элемента, защищенного репликацией, путем сопоставления набора шифрования диска при восстановлении из HyperV в Azure.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-157">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7cf4c-158">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7cf4c-158">Az.Resources</span></span>
* <span data-ttu-id="7cf4c-159">Исправлена ошибка в справочном документе о командлете Remove-AzTag.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-159">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="7cf4c-160">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7cf4c-160">Az.Sql</span></span>
* <span data-ttu-id="7cf4c-161">Исправлена функция основных командлетов установки оценки уязвимостей: теперь она позволяет работать с базой данных master для базы данных Azure и ограничить ее в системных базах данных управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-161">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="7cf4c-162">Устранена ошибка, возникающая при создании группы отработки отказа экземпляра SQL.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-162">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="7cf4c-163">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="7cf4c-163">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="7cf4c-164">Добавлен новый допустимый тип лицензии: DR (аварийное восстановление).</span><span class="sxs-lookup"><span data-stu-id="7cf4c-164">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7cf4c-165">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7cf4c-165">Az.Storage</span></span>
* <span data-ttu-id="7cf4c-166">Добавлено предупреждающее сообщение о критическом изменении значения DefaultAction в следующем выпуске:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-166">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="7cf4c-167">Update-AzStorageAccountNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-167">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="7cf4c-168">Включена поддержка получения времени последней синхронизации учетной записи хранения путем выполнения командлета Get-AzureRmStorageAccount с параметром -IncludeGeoReplicationStats:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-168">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span> 
    - <span data-ttu-id="7cf4c-169">Get-AzureRmStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-169">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="7cf4c-170">3.2.0 — декабрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-170">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="7cf4c-171">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="7cf4c-171">General</span></span>
* <span data-ttu-id="7cf4c-172">Обновление ссылок в .psd1 для использования относительного пути для всех модулей.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-172">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7cf4c-173">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7cf4c-173">Az.Accounts</span></span>
* <span data-ttu-id="7cf4c-174">Установка правильного параметра UserAgent для телеметрии на стороне клиента для Az 4.0 (предварительная версия).</span><span class="sxs-lookup"><span data-stu-id="7cf4c-174">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="7cf4c-175">Отображение понятного пользователю сообщения об ошибке, если в Az 4.0 (предварительная версия) не указан контекст.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-175">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="7cf4c-176">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="7cf4c-176">Az.Batch</span></span>
* <span data-ttu-id="7cf4c-177">Исправлена проблема [№ 10602](https://github.com/Azure/azure-powershell/issues/10602), из-за которой использование командлета **New-AzBatchPool** приводило к неправильной отправке VirtualMachineConfiguration.ContainerConfiguration или VirtualMachineConfiguration.DataDisks на сервер.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-177">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7cf4c-178">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7cf4c-178">Az.DataFactory</span></span>
* <span data-ttu-id="7cf4c-179">Обновление пакета SDK Фабрики данных для .NET до версии 4.5.0.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-179">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="7cf4c-180">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="7cf4c-180">Az.FrontDoor</span></span>
* <span data-ttu-id="7cf4c-181">Включена поддержка исключений управляемых правил WAF.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-181">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="7cf4c-182">Добавление SocketAddr в список автозавершения.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-182">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="7cf4c-183">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="7cf4c-183">Az.HealthcareApis</span></span>
* <span data-ttu-id="7cf4c-184">Обработка исключений.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-184">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7cf4c-185">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7cf4c-185">Az.KeyVault</span></span>
* <span data-ttu-id="7cf4c-186">Исправлена ошибка при получении доступа к значению, которое может быть не задано.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-186">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="7cf4c-187">Управление сертификатами шифрования на основе эллиптических кривых.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-187">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="7cf4c-188">Включена возможность указания кривой для политик сертификатов.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-188">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7cf4c-189">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7cf4c-189">Az.Monitor</span></span>
* <span data-ttu-id="7cf4c-190">Добавление необязательного аргумента в команду добавления параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-190">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="7cf4c-191">Существующий аргумент switch указывает на то, что экспорт в Log Analytics должен выполняться в фиксированную схему</span><span class="sxs-lookup"><span data-stu-id="7cf4c-191">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="7cf4c-192">(выделенный тип данных).</span><span class="sxs-lookup"><span data-stu-id="7cf4c-192">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7cf4c-193">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7cf4c-193">Az.Network</span></span>
* <span data-ttu-id="7cf4c-194">В приложении AzureFirewall, NAT и сетевых правилах включена поддержка IpGroups.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-194">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7cf4c-195">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7cf4c-195">Az.Resources</span></span>
* <span data-ttu-id="7cf4c-196">Устранена проблема, из-за которой при развертывании шаблона не удавалось считать его параметр, если имя параметра конфликтовало с именем встроенного параметра.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-196">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="7cf4c-197">Обновлены командлеты политики для использования новой версии API 2019-09-01 с поддержкой группирования в определениях наборов политик.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-197">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="7cf4c-198">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7cf4c-198">Az.Sql</span></span>
* <span data-ttu-id="7cf4c-199">Обновлена функция автоматического создания расширенного хранилища для службы оценки уязвимостей в учетной записи StorageV2.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-199">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7cf4c-200">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7cf4c-200">Az.Storage</span></span>
* <span data-ttu-id="7cf4c-201">Включена поддержка создания маркера SAS на основе удостоверения контейнера и большого двоичного объекта с аутентификацией Oauth на основе контекста службы хранилища:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-201">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="7cf4c-202">New-AzStorageContainerSASToken;</span><span class="sxs-lookup"><span data-stu-id="7cf4c-202">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="7cf4c-203">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="7cf4c-203">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="7cf4c-204">Отозвана поддержка ключей делегирования пользователя учетной записи хранения, а также всех маркеров SAS удостоверения:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-204">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="7cf4c-205">Revoke-AzStorageAccountUserDelegationKeys.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-205">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="7cf4c-206">Выполнено обновление до Microsoft.Azure.Management.Storage версии 14.2.0 для включения поддержки нового API версии 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-206">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="7cf4c-207">Включена поддержка QuotaGiB (квота общего ресурса в ГиБ) для значений свыше 5120 в командлетах для работы с общими папками в плоскости управления и добавлен псевдоним Quota для параметра QuotaGiB.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-207">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span> 
    - <span data-ttu-id="7cf4c-208">New-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="7cf4c-208">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="7cf4c-209">Update-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="7cf4c-209">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="7cf4c-210">Добавлен псевдоним QuotaGiB для параметра Quota:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-210">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="7cf4c-211">Set-AzStorageShareQuota.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-211">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="7cf4c-212">Устранена проблема, из-за которой при использовании AzStorageContainerAcl могла очищаться хранимая политика доступа:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-212">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="7cf4c-213">Set-AzStorageContainerAcl.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-213">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="7cf4c-214">Версия 3.1.0 от ноября 2019 г.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-214">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="7cf4c-215">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="7cf4c-215">Highlights since the last major release</span></span>
* <span data-ttu-id="7cf4c-216">Выпуск Az.DataBoxEdge 1.0.0</span><span class="sxs-lookup"><span data-stu-id="7cf4c-216">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="7cf4c-217">Выпуск Az.SqlVirtualMachine 1.0.0</span><span class="sxs-lookup"><span data-stu-id="7cf4c-217">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7cf4c-218">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7cf4c-218">Az.Compute</span></span>
* <span data-ttu-id="7cf4c-219">Функция повторного применения виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="7cf4c-219">VM Reapply feature</span></span>
    - <span data-ttu-id="7cf4c-220">Добавлен параметр повторного применения в командлет Set-AzVM.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-220">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="7cf4c-221">Функция AutomaticRepairs масштабируемого набора виртуальных машин:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-221">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="7cf4c-222">Добавлены параметры EnableAutomaticRepair, AutomaticRepairGracePeriod и AutomaticRepairMaxInstanceRepairsPercent в следующие командлеты:   New-AzVmssConfig Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7cf4c-222">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="7cf4c-223">Включена поддержка образа из коллекции разных клиентов для New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-223">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="7cf4c-224">Добавлен фрагмент Spot в средство заполнения аргументов параметра Priority в командлетах New-AzVM, New-AzVMConfig и New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-224">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="7cf4c-225">Добавлены параметры DiskIOPSReadWrite и DiskMBpsReadWrite в командлет Add-AzVmssDataDisk.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-225">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="7cf4c-226">Изменен параметр SourceImageId командлета New-AzGalleryImageVersion на необязательный.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-226">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="7cf4c-227">Добавлены параметры OSDiskImage и DataDiskImage в командлет New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-227">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="7cf4c-228">Добавлен параметр HyperVGeneration в командлет New-AzGalleryImageDefinition.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-228">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="7cf4c-229">Добавлены параметры SkipExtensionsOnOverprovisionedVMs в командлеты New-AzVmss, New-AzVmssConfig и Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-229">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="7cf4c-230">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="7cf4c-230">Az.DataBoxEdge</span></span>
* <span data-ttu-id="7cf4c-231">Добавлен командлет `Get-AzDataBoxEdgeOrder`.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-231">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="7cf4c-232">Получение заказа.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-232">Get the Order</span></span>
* <span data-ttu-id="7cf4c-233">Добавлен командлет `New-AzDataBoxEdgeOrder`.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-233">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="7cf4c-234">Создание заказа.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-234">Create new Order</span></span>
* <span data-ttu-id="7cf4c-235">Добавлен командлет `Remove-AzDataBoxEdgeOrder`.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-235">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="7cf4c-236">Удаление заказа.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-236">Remove the Order</span></span>
* <span data-ttu-id="7cf4c-237">Изменен командлет `New-AzDataBoxEdgeShare`.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-237">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="7cf4c-238">Создание локальной общей папки.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-238">Now creates Local Share</span></span>
* <span data-ttu-id="7cf4c-239">Добавлен командлет `Set-AzDataBoxEdgeRole`.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-239">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="7cf4c-240">Сопоставление IotRole с общей папкой.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-240">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="7cf4c-241">Добавлен командлет `Invoke-AzDataBoxEdgeDevice`.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-241">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="7cf4c-242">Вызов проверки обновлений, скачивание обновления, установка обновления на устройстве.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-242">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="7cf4c-243">Добавлен командлет `Get-AzDataBoxEdgeTrigger`.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-243">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="7cf4c-244">Получение сведений о триггерах.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-244">Gets the information about Triggers</span></span>
* <span data-ttu-id="7cf4c-245">Добавлен командлет `New-AzDataBoxEdgeTrigger`.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-245">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="7cf4c-246">Создание триггеров.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-246">Create new Triggers</span></span>
* <span data-ttu-id="7cf4c-247">Добавлен командлет `Remove-AzDataBoxEdgeTrigger`.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-247">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="7cf4c-248">Удаление триггеров.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-248">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7cf4c-249">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7cf4c-249">Az.DataFactory</span></span>
* <span data-ttu-id="7cf4c-250">Обновление пакета SDK Фабрики данных для .NET до версии 4.4.0.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-250">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="7cf4c-251">Добавлен параметр ExpressCustomSetup в командлет Set-AzureRmDataFactoryV2IntegrationRuntime для включения конфигураций установки и сторонних компонентов без использования настраиваемого скрипта установки.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-251">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7cf4c-252">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7cf4c-252">Az.DataLakeStore</span></span>
* <span data-ttu-id="7cf4c-253">Обновлена документация по Get-AzDataLakeStoreDeletedItem и Restore-AzDataLakeStoreDeletedItem.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-253">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7cf4c-254">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7cf4c-254">Az.EventHub</span></span>
* <span data-ttu-id="7cf4c-255">Исправлена проблема № 10301. Исправлен формат даты маркера SAS.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-255">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="7cf4c-256">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="7cf4c-256">Az.FrontDoor</span></span>
* <span data-ttu-id="7cf4c-257">Добавлен параметр MinimumTlsVersion в Enable-AzFrontDoorCustomDomainHttps и New-AzFrontDoorFrontendEndpointObject.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-257">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="7cf4c-258">Добавлены параметры HealthProbeMethod и EnabledState в New-AzFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-258">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="7cf4c-259">Добавлен новый командлет для создания объекта BackendPoolsSettings для передачи при создании и обновлении Front Door.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-259">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="7cf4c-260">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="7cf4c-260">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7cf4c-261">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7cf4c-261">Az.Network</span></span>
* <span data-ttu-id="7cf4c-262">Изменены примеры параметра FilterData Start-AzVirtualNetworkGatewayConnectionPacketCapture.md и Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-262">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="7cf4c-263">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="7cf4c-263">Az.PrivateDns</span></span>
* <span data-ttu-id="7cf4c-264">Пакет SDK PrivateDns для .NET обновлен до версии 1.0.0</span><span class="sxs-lookup"><span data-stu-id="7cf4c-264">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7cf4c-265">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7cf4c-265">Az.RecoveryServices</span></span>
* <span data-ttu-id="7cf4c-266">Включена поддержка Azure Site Recovery для выбора типа диска при включении защиты.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-266">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="7cf4c-267">Внесено исправление Azure Site Recovery для изменения действия плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-267">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="7cf4c-268">Включена поддержка восстановления SQL Azure Backup для принятия баз данных файлового потока.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-268">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="7cf4c-269">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="7cf4c-269">Az.RedisCache</span></span>
* <span data-ttu-id="7cf4c-270">Добавлен параметр MinimumTlsVersion в командлеты New-AzRedisCache и Set-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-270">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="7cf4c-271">Кроме того, добавлен параметр MinimumTlsVersion в выходные данные командлета Get-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-271">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="7cf4c-272">Добавлена проверка параметра -Size для командлетов Set-AzRedisCache и New-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-272">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="7cf4c-273">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7cf4c-273">Az.Resources</span></span>
- <span data-ttu-id="7cf4c-274">Обновлены командлеты политики для использования новой версии API 2019-06-01 с новым свойством EnforcementMode в назначении политики.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-274">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="7cf4c-275">Обновлен пример справки по созданию определения политики</span><span class="sxs-lookup"><span data-stu-id="7cf4c-275">Updated create policy definition help example</span></span>
- <span data-ttu-id="7cf4c-276">Исправлена ошибка с параметром -ServicePrincipalName командлета Remove-AZADServicePrincipal с возвратом пустой ссылки, если имя субъекта службы не найдено.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-276">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="7cf4c-277">Исправлена ошибка с New-AZADServicePrincipal с возвратом пустой ссылки, если у клиента нет подписки.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-277">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="7cf4c-278">Изменен командлет New-AzAdServicePrincipal для добавления учетных данных только для связанного приложения.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-278">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="7cf4c-279">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7cf4c-279">Az.Sql</span></span>
* <span data-ttu-id="7cf4c-280">Добавлена поддержка ReadReplicaCount для базы данных.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-280">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="7cf4c-281">Исправлена ошибка с Set-AzSqlDatabase, если избыточность в пределах зоны не настроена.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-281">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="7cf4c-282">Версия 3.0.0 от ноября 2019 г.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-282">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="7cf4c-283">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="7cf4c-283">General</span></span>
* <span data-ttu-id="7cf4c-284">Выпущена версия Az.PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="7cf4c-284">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7cf4c-285">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7cf4c-285">Az.Accounts</span></span>
* <span data-ttu-id="7cf4c-286">Добавлено сообщение об устаревании для псевдонима "Resolve-Error".</span><span class="sxs-lookup"><span data-stu-id="7cf4c-286">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="7cf4c-287">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="7cf4c-287">Az.Advisor</span></span>
* <span data-ttu-id="7cf4c-288">Добавлена новая категория Operational Excellence (Эффективность работы) в командлет Get-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-288">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="7cf4c-289">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="7cf4c-289">Az.Batch</span></span>
* <span data-ttu-id="7cf4c-290">`CoreQuota` в `BatchAccountContext` переименован в `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-290">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="7cf4c-291">Также появился новый `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-291">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="7cf4c-292">Это влияет на **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-292">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="7cf4c-293">Параметр **New-AzBatchTask** `-ResourceFile` теперь принимает коллекцию объектов `PSResourceFile`, которые можно создать с помощью нового командлета **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-293">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="7cf4c-294">Новый командлет **New-AzBatchResourceFile**, который помогает создавать объекты `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-294">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="7cf4c-295">Их можно передавать в **New-AzBatchTask** в параметре `-ResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-295">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="7cf4c-296">Это позволяет поддерживать два новых типа файлов ресурсов, которые дополняют существующий метод `HttpUrl`:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-296">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="7cf4c-297">Файлы ресурсов на основе `AutoStorageContainerName` скачивают весь контейнер автоматического хранения в узел пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-297">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="7cf4c-298">Файлы ресурсов на основе `StorageContainerUrl` скачивают указанный в URL-адресе контейнер в узел пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-298">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="7cf4c-299">Удалено свойство `ApplicationPackages` в `PSApplication`, который возвращается из **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-299">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="7cf4c-300">Отдельные пакеты в приложении теперь можно извлечь с помощью **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-300">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="7cf4c-301">Например: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-301">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="7cf4c-302">`ApplicationId` переименован в `ApplicationName` для **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication** и **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-302">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage**, **New-AzBatchApplicationPackage**, **Remove-AzBatchApplicationPackage**, **Get-AzBatchApplication**, **New-AzBatchApplication**, **Remove-AzBatchApplication**, and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="7cf4c-303">Теперь `ApplicationId` является псевдонимом для `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-303">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="7cf4c-304">Добавлено новое свойство `PSWindowsUserConfiguration` в `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-304">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="7cf4c-305">`Version` переименован в `Name` для `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-305">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="7cf4c-306">`BlobSource` переименован в `HttpUrl` для `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-306">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="7cf4c-307">Удалено свойство `OSDisk` из `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-307">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="7cf4c-308">Удалена операция **Set-AzBatchPoolOSVersion**.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-308">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="7cf4c-309">Больше она не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-309">This operation is no longer supported.</span></span>
* <span data-ttu-id="7cf4c-310">Удалено `TargetOSVersion` из `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-310">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="7cf4c-311">`CurrentOSVersion` переименован в `OSVersion` для `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-311">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="7cf4c-312">Удалено `DataEgressGiB` и `DataIngressGiB` из `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-312">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="7cf4c-313">Операция **Get-AzBatchNodeAgentSku** удалена и заменена на **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-313">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span> 
  - <span data-ttu-id="7cf4c-314">**Get-AzBatchSupportedImage** возвращает те же данные, что и **Get-AzBatchNodeAgentSku**, но в более удобном формате.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-314">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="7cf4c-315">Также возвращаются новые непроверенные образы.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-315">New non-verified images are also now returned.</span></span> <span data-ttu-id="7cf4c-316">Включается и дополнительная информация о `Capabilities` и `BatchSupportEndOfLife` для каждого образа.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-316">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="7cf4c-317">Добавлена возможность монтировать файловые системы на каждом узле пула с помощью нового параметра `MountConfiguration` в **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-317">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="7cf4c-318">Теперь поддерживаются правила безопасности сети, которые блокируют сетевой доступ к пулу по исходящему порту трафика.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-318">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="7cf4c-319">Это выполняется с помощью свойства `SourcePortRanges` для `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-319">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="7cf4c-320">Что касается выполнения контейнеров, пакетная служба теперь поддерживает выполнение задачи в рабочей папке контейнера или рабочей папке задачи пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-320">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="7cf4c-321">Выбор зависит от параметра `WorkingDirectory` в `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-321">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="7cf4c-322">Добавлена возможность указать коллекцию общедоступных IP-адресов для `PSNetworkConfiguration` с помощью нового свойства `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-322">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="7cf4c-323">Это гарантирует, что узлы в пуле будут иметь IP-адреса из списка, предоставленного пользователем.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-323">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="7cf4c-324">Если значение не задано, по умолчанию для `WaitForSuccess` в `PSSTartTask` используется значение `$True` (ранее `$False`).</span><span class="sxs-lookup"><span data-stu-id="7cf4c-324">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="7cf4c-325">Если значение не задано, по умолчанию для `Scope` в `PSAutoUserSpecification` используется значение `Pool` (ранее `Task` для Windows или `Pool` для Linux).</span><span class="sxs-lookup"><span data-stu-id="7cf4c-325">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="7cf4c-326">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7cf4c-326">Az.Cdn</span></span>
* <span data-ttu-id="7cf4c-327">Добавлены UrlRewriteAction и CacheKeyQueryStringAction в RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-327">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="7cf4c-328">Исправлено несколько ошибок, таких как отсутствующий входной параметр Selector в командлете New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-328">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7cf4c-329">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7cf4c-329">Az.Compute</span></span>
* <span data-ttu-id="7cf4c-330">Функция набора шифрования диска</span><span class="sxs-lookup"><span data-stu-id="7cf4c-330">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="7cf4c-331">Новые командлеты:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="7cf4c-331">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="7cf4c-332">Добавлен параметр ProximityPlacementGroupId в следующие командлеты: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span><span class="sxs-lookup"><span data-stu-id="7cf4c-332">DiskEncryptionSetId parameter is added to the following cmdlets: Set-AzImageOSDisk Set-AzVMOSDisk Set-AzVmssStorageProfile</span></span>        
        <span data-ttu-id="7cf4c-333">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="7cf4c-333">Add-AzImageDataDisk New-AzVMDataDisk Set-AzVMDataDisk Add-AzVMDataDisk Add-AzVmssDataDisk Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="7cf4c-334">Параметры DiskEncryptionSetId и EncryptionType добавлены в следующие командлеты:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="7cf4c-334">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="7cf4c-335">Добавлен параметр PublicIPAddressVersion в New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="7cf4c-335">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="7cf4c-336">FileUris для расширения пользовательских скриптов теперь будет защищенным, а не общедоступным параметром</span><span class="sxs-lookup"><span data-stu-id="7cf4c-336">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="7cf4c-337">Добавлено ScaleInPolicy в командлеты New-AzVmss, New-AzVmssConfig и Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="7cf4c-337">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="7cf4c-338">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="7cf4c-338">Breaking changes</span></span>
    - <span data-ttu-id="7cf4c-339">Параметр UploadSizeInBytes применяется теперь вместо DiskSizeGB для New-AzDiskConfig, если CreateOption имеет значение Upload</span><span class="sxs-lookup"><span data-stu-id="7cf4c-339">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="7cf4c-340">PublishingProfile.Source.ManagedImage.Id заменяется на StorageProfile.Source.Id в объекте GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="7cf4c-340">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7cf4c-341">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7cf4c-341">Az.DataFactory</span></span>
* <span data-ttu-id="7cf4c-342">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.3.0.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-342">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7cf4c-343">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7cf4c-343">Az.DataLakeStore</span></span>
* <span data-ttu-id="7cf4c-344">Обновлен пакет SDK для ADLS (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), включает следующие исправления</span><span class="sxs-lookup"><span data-stu-id="7cf4c-344">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="7cf4c-345">Не создается исключение при невозможности десериализовать значение времени создания для записи в корзине или каталоге.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-345">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="7cf4c-346">Предоставляется параметр для времени ожидания запроса в adlsclient</span><span class="sxs-lookup"><span data-stu-id="7cf4c-346">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="7cf4c-347">Исправлена передача исходного значения syncflag для восстановления badoffset</span><span class="sxs-lookup"><span data-stu-id="7cf4c-347">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="7cf4c-348">Исправлена операция EnumerateDirectory, чтобы она извлекала токен продолжения после проверки ответа</span><span class="sxs-lookup"><span data-stu-id="7cf4c-348">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="7cf4c-349">Исправлена ошибка объединения</span><span class="sxs-lookup"><span data-stu-id="7cf4c-349">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="7cf4c-350">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="7cf4c-350">Az.FrontDoor</span></span>
* <span data-ttu-id="7cf4c-351">Исправлены разные опечатки в разных частях модуля</span><span class="sxs-lookup"><span data-stu-id="7cf4c-351">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="7cf4c-352">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="7cf4c-352">Az.HDInsight</span></span>
* <span data-ttu-id="7cf4c-353">Исправлена ошибка, из-за которой клиент получал сообщение об ошибке 'Not a valid Base-64 string' (Не является допустимой строкой Base64) при выполнении Get-AzHDInsightCluster для получения кластера с хранилищем ADLSGen1.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-353">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="7cf4c-354">Добавлен параметр с именем ApplicationId в три командлета Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig и New-AzHDInsightCluster, чтобы клиент мог предоставить идентификатор приложения субъекта-службы для доступа к Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-354">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="7cf4c-355">Для Microsoft.Azure.Management.HDInsight изменена версия с 2.1.0 на 5.1.0</span><span class="sxs-lookup"><span data-stu-id="7cf4c-355">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="7cf4c-356">Удалены пять командлетов:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-356">Removed five cmdlets:</span></span>
    - <span data-ttu-id="7cf4c-357">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="7cf4c-357">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="7cf4c-358">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="7cf4c-358">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="7cf4c-359">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="7cf4c-359">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="7cf4c-360">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="7cf4c-360">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="7cf4c-361">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="7cf4c-361">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="7cf4c-362">Добавлены три командлета:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-362">Added three cmdlets:</span></span>
    - <span data-ttu-id="7cf4c-363">Get-AzHDInsightMonitoring заменяет собой Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-363">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="7cf4c-364">Enable-AzHDInsightMonitoring заменяет собой Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-364">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="7cf4c-365">Disable-AzHDInsightMonitoring заменяет собой Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-365">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="7cf4c-366">Исправлен командлет Get-AzHDInsightProperties, чтобы он поддерживал получение сведений о возможностях из определенного расположения.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-366">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="7cf4c-367">Удалены наборы параметров ("Spark1", "Spark2") из Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-367">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="7cf4c-368">Добавлены примеры в справочные документы по командлету Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-368">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="7cf4c-369">Изменен тип выходных данных для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-369">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="7cf4c-370">Для Get-AzHDInsightProperties тип выходных данных изменен с CapabilitiesResponse на AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-370">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="7cf4c-371">Для Remove-AzHDInsightCluster тип выходных данных изменен с ClusterGetResponse на bool.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-371">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="7cf4c-372">Для Set-AzHDInsightGatewaySettings тип выходных данных изменен с HttpConnectivitySettings на GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-372">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="7cf4c-373">Добавлены несколько условий для проверки сценариев.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-373">Added some scenario test cases.</span></span>
* <span data-ttu-id="7cf4c-374">Удалены несколько псевдонимов: Add-AzHDInsightConfigValues, Get-AzHDInsightProperties.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-374">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7cf4c-375">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7cf4c-375">Az.IotHub</span></span>
* <span data-ttu-id="7cf4c-376">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="7cf4c-376">Breaking changes:</span></span>
    - <span data-ttu-id="7cf4c-377">Командлет Add-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-377">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="7cf4c-378">Удален набор параметров __AllParameterSets для командлета Add-AzIotHubEventHubConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-378">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="7cf4c-379">Командлет Get-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-379">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="7cf4c-380">Удален набор параметров __AllParameterSets для командлета Get-AzIotHubEventHubConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-380">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="7cf4c-381">Удалено свойство OperationsMonitoringProperties для типа Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-381">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="7cf4c-382">Удалено свойство OperationsMonitoringProperties для типа Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-382">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="7cf4c-383">Командлет New-AzIotHubExportDevice больше не поддерживает псевдоним New-AzIotHubExportDevices.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-383">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="7cf4c-384">Командлет New-AzIotHubImportDevice больше не поддерживает псевдоним New-AzIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-384">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="7cf4c-385">Командлет Remove-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-385">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="7cf4c-386">Удален набор параметров __AllParameterSets для командлета Remove-AzIotHubEventHubConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-386">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="7cf4c-387">Командлет Set-AzIotHub теперь не поддерживает параметр OperationsMonitoringProperties и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-387">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="7cf4c-388">Удален набор параметров UpdateOperationsMonitoringProperties для командлета Set-AzIotHub.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-388">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7cf4c-389">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7cf4c-389">Az.RecoveryServices</span></span>
* <span data-ttu-id="7cf4c-390">Azure Site Recovery поддерживает настройку сетевых ресурсов, например групп безопасности сети, общедоступных IP-адресов и внутренних подсистем балансировки нагрузки из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-390">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="7cf4c-391">Azure Site Recovery поддерживает запись на управляемый диск из vMWare в Azure.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-391">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="7cf4c-392">Azure Site Recovery поддерживает сокращение NIC из vMWare в Azure.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-392">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="7cf4c-393">Azure Site Recovery поддерживает ускорение сети NIC из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-393">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="7cf4c-394">Azure Site Recovery поддерживает автоматическое обновление агента из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-394">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="7cf4c-395">Azure Site Recovery поддерживает стандартный SSD-накопитель из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-395">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="7cf4c-396">Azure Site Recovery поддерживает двухпроходное шифрование диска Azure из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-396">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="7cf4c-397">Azure Site Recovery поддерживает новый добавленный диск из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-397">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="7cf4c-398">Добавлена функция SoftDelete для виртуальных машин и соответствующие тесты</span><span class="sxs-lookup"><span data-stu-id="7cf4c-398">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="7cf4c-399">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7cf4c-399">Az.Resources</span></span>
* <span data-ttu-id="7cf4c-400">Обновлена сборка зависимостей Microsoft.Extensions.Caching.Memory с версии 1.1.1 до 2.2</span><span class="sxs-lookup"><span data-stu-id="7cf4c-400">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7cf4c-401">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7cf4c-401">Az.Network</span></span>
* <span data-ttu-id="7cf4c-402">Изменены все командлеты для PrivateEndpointConnection, чтобы они поддерживали универсальный поставщик служб.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-402">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="7cf4c-403">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-403">Updated cmdlet:</span></span>
        - <span data-ttu-id="7cf4c-404">Approve-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-404">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7cf4c-405">Deny-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-405">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7cf4c-406">Get-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-406">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7cf4c-407">Remove-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-407">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7cf4c-408">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7cf4c-408">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="7cf4c-409">Добавлен новый командлет для PrivateLinkResource, который поддерживает универсальный поставщик служб.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-409">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="7cf4c-410">Новый командлет</span><span class="sxs-lookup"><span data-stu-id="7cf4c-410">New cmdlet:</span></span>
        - <span data-ttu-id="7cf4c-411">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="7cf4c-411">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="7cf4c-412">Добавлены новые поля и параметр для протокола прокси версии 2.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-412">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="7cf4c-413">Добавлено свойство EnableProxyProtocol в PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7cf4c-413">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="7cf4c-414">Добавлено свойство LinkIdentifier в PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7cf4c-414">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="7cf4c-415">Обновлен New-AzPrivateLinkService для поддержки нового необязательного параметра EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-415">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="7cf4c-416">Исправлено описание параметра в справочной документации по командлету New-AzApplicationGatewaySku.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-416">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="7cf4c-417">Новые командлеты для поддержки политики брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="7cf4c-417">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="7cf4c-418">Добавлена поддержка дочерних ресурсов RouteTables для VirtualHub</span><span class="sxs-lookup"><span data-stu-id="7cf4c-418">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="7cf4c-419">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-419">New cmdlets added:</span></span>
        - <span data-ttu-id="7cf4c-420">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="7cf4c-420">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="7cf4c-421">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="7cf4c-421">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="7cf4c-422">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="7cf4c-422">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="7cf4c-423">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="7cf4c-423">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="7cf4c-424">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="7cf4c-424">Set-AzVirtualHub</span></span>
* <span data-ttu-id="7cf4c-425">Добавлена поддержка новых свойств SKU для VirtualHub и VirtualWANType в VirtualWan</span><span class="sxs-lookup"><span data-stu-id="7cf4c-425">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="7cf4c-426">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-426">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="7cf4c-427">New-AzVirtualHub: добавлен параметр Sku</span><span class="sxs-lookup"><span data-stu-id="7cf4c-427">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="7cf4c-428">Update-AzVirtualHub: добавлен параметр Sku</span><span class="sxs-lookup"><span data-stu-id="7cf4c-428">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="7cf4c-429">New-AzVirtualWan: добавлен параметр VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="7cf4c-429">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="7cf4c-430">Update-AzVirtualWan: добавлен параметр VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="7cf4c-430">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="7cf4c-431">Добавлена поддержка свойства EnableInternetSecurity для HubVnetConnection, VpnConnection и ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="7cf4c-431">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="7cf4c-432">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-432">New cmdlets added:</span></span>
        - <span data-ttu-id="7cf4c-433">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="7cf4c-433">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="7cf4c-434">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-434">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="7cf4c-435">New-AzureRmVirtualHubVnetConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="7cf4c-435">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="7cf4c-436">New-AzureRmVpnConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="7cf4c-436">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="7cf4c-437">Update-AzureRmVpnConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="7cf4c-437">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="7cf4c-438">New-AzureRmExpressRouteConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="7cf4c-438">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="7cf4c-439">Set-AzureRmExpressRouteConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="7cf4c-439">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="7cf4c-440">Добавлена поддержка настройки политики верхнего уровня WebApplicationFirewall</span><span class="sxs-lookup"><span data-stu-id="7cf4c-440">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="7cf4c-441">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-441">New cmdlets added:</span></span>
        - <span data-ttu-id="7cf4c-442">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="7cf4c-442">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="7cf4c-443">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="7cf4c-443">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="7cf4c-444">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="7cf4c-444">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="7cf4c-445">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="7cf4c-445">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="7cf4c-446">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="7cf4c-446">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="7cf4c-447">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="7cf4c-447">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="7cf4c-448">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-448">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="7cf4c-449">New-AzApplicationGatewayFirewallPolicy: добавлены параметры PolicySetting, ManagedRule</span><span class="sxs-lookup"><span data-stu-id="7cf4c-449">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="7cf4c-450">Добавлена поддержка оператора Geo-Match для CustomRule</span><span class="sxs-lookup"><span data-stu-id="7cf4c-450">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="7cf4c-451">Добавлен параметр GeoMatch в оператор для FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="7cf4c-451">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="7cf4c-452">Добавлена поддержка политики брандмауэра perListener и perSite</span><span class="sxs-lookup"><span data-stu-id="7cf4c-452">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="7cf4c-453">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-453">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="7cf4c-454">New-AzApplicationGatewayHttpListener: добавлены параметры FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="7cf4c-454">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="7cf4c-455">New-AzApplicationGatewayPathRuleConfig: добавлены параметры FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="7cf4c-455">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="7cf4c-456">Исправлен учет регистра для требуемой подсети с именем AzureBastionSubnet в PSBastion</span><span class="sxs-lookup"><span data-stu-id="7cf4c-456">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="7cf4c-457">Поддержка полного доменного имени назначения в правилах сети и преобразованного полного доменного имени в правилах NAT для брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="7cf4c-457">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="7cf4c-458">Добавлена поддержка ресурсов верхнего уровня RouteTables для IpGroup</span><span class="sxs-lookup"><span data-stu-id="7cf4c-458">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="7cf4c-459">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-459">New cmdlets added:</span></span>
        - <span data-ttu-id="7cf4c-460">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="7cf4c-460">New-AzIpGroup</span></span>
        - <span data-ttu-id="7cf4c-461">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="7cf4c-461">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="7cf4c-462">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="7cf4c-462">Get-AzIpGroup</span></span>
        - <span data-ttu-id="7cf4c-463">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="7cf4c-463">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7cf4c-464">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7cf4c-464">Az.ServiceFabric</span></span>
* <span data-ttu-id="7cf4c-465">Удален командлет Add-AzServiceFabricApplicationCertificate, так как соответствующий сценарий выполняется командлетом Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-465">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="7cf4c-466">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7cf4c-466">Az.Sql</span></span>
* <span data-ttu-id="7cf4c-467">Добавлена поддержка восстановления удаленных баз данных в управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-467">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="7cf4c-468">Из кода удалены старые командлеты аудита.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-468">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="7cf4c-469">Удалены нерекомендуемые псевдонимы:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-469">Removed deprecated aliases:</span></span>
* <span data-ttu-id="7cf4c-470">Get-AzSqlDatabaseIndexRecommendations (вместо него используйте Get-AzSqlDatabaseIndexRecommendation)</span><span class="sxs-lookup"><span data-stu-id="7cf4c-470">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="7cf4c-471">Get-AzSqlDatabaseRestorePoints (вместо него используйте Get-AzSqlDatabaseRestorePoint)</span><span class="sxs-lookup"><span data-stu-id="7cf4c-471">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="7cf4c-472">Удален командлет Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="7cf4c-472">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="7cf4c-473">Удалены псевдонимы для нерекомендуемых командлетов параметров оценки уязвимостей</span><span class="sxs-lookup"><span data-stu-id="7cf4c-473">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="7cf4c-474">Командлеты расширенного обнаружения угроз объявлены устаревшими</span><span class="sxs-lookup"><span data-stu-id="7cf4c-474">Deprecate Advanced Threat Detection Settings cmdlets</span></span> 
* <span data-ttu-id="7cf4c-475">Добавлены командлеты для отключения и включения рекомендаций о конфиденциальности для столбцов в базе данных.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-475">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7cf4c-476">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7cf4c-476">Az.Storage</span></span>
* <span data-ttu-id="7cf4c-477">Поддержка включения большой общей папки при создании или обновлении учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="7cf4c-477">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="7cf4c-478">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7cf4c-478">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="7cf4c-479">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7cf4c-479">Set-AzStorageAccount</span></span>
* <span data-ttu-id="7cf4c-480">При закрытии или получении маркера файла пропускается проверка того, является ли входной путь файлом или каталогом, чтобы избежать сбоев при получении объектов в состоянии DeletePending.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-480">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="7cf4c-481">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="7cf4c-481">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="7cf4c-482">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="7cf4c-482">Close-AzStorageFileHandle</span></span>
    
## <a name="280---october-2019"></a><span data-ttu-id="7cf4c-483">2.8.0 — октябрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-483">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="7cf4c-484">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="7cf4c-484">General</span></span>
* <span data-ttu-id="7cf4c-485">Выпуск Az.HealthcareApis 1.0.0</span><span class="sxs-lookup"><span data-stu-id="7cf4c-485">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7cf4c-486">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7cf4c-486">Az.Accounts</span></span>
* <span data-ttu-id="7cf4c-487">Обновление телеметрии и перезаписи URL-адресов для созданных модулей, исправление для модульных тестов Windows.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-487">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="7cf4c-488">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7cf4c-488">Az.ApiManagement</span></span>
* <span data-ttu-id="7cf4c-489">**Set-AzApiManagementApi** — в ApiVersionSet добавлена поддержка обновления API.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-489">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="7cf4c-490">исправлена проблема https://github.com/Azure/azure-powershell/issues/10068.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-490">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7cf4c-491">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7cf4c-491">Az.Automation</span></span>
* <span data-ttu-id="7cf4c-492">Исправлен командлет New-AzureAutomationSoftwareUpdateConfiguration для параметра перезагрузки Linux.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-492">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span> 

#### <a name="azbatch"></a><span data-ttu-id="7cf4c-493">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="7cf4c-493">Az.Batch</span></span>
* <span data-ttu-id="7cf4c-494">Командлет **Get-AzBatchNodeAgentSku** объявлен устаревшим и будет заменен на **Get-AzBatchSupportImage** в версии 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-494">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7cf4c-495">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7cf4c-495">Az.Compute</span></span>
* <span data-ttu-id="7cf4c-496">В командлеты New-AzVM и New-AzVmss добавлены параметры Priority, EvictionPolicy и MaxPrice.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-496">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="7cf4c-497">Исправлены предупреждающее сообщение для командлетов Add-AzVMAdditionalUnattendContent и Add-AzVMSshPublicKey и справочная документация по ним.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-497">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="7cf4c-498">Для Set-AzVMDiskEncryptionExtension исправлено исключение -skipVmBackup для виртуальных машин Linux с управляемыми дисками.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-498">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span> 
* <span data-ttu-id="7cf4c-499">Исправлена ошибка при изменении параметров шифрования в Set-AzVMDiskEncryptionExtension, реализован двухэтапный сценарий.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-499">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7cf4c-500">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7cf4c-500">Az.DataFactory</span></span>
* <span data-ttu-id="7cf4c-501">Добавлены команды CRUD для потока данных Фабрики данных Azure версии 2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow и Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-501">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="7cf4c-502">Добавлены команды действий для сеанса отладки потока данных Фабрики данных Azure версии 2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand и Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-502">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="7cf4c-503">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.2.0.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-503">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7cf4c-504">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7cf4c-504">Az.DataLakeStore</span></span>
* <span data-ttu-id="7cf4c-505">Проверка учетной записи исправлена так, чтобы учетные записи, содержащие знак "-", можно было передавать без домена.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-505">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="7cf4c-506">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="7cf4c-506">Az.HealthcareApis</span></span>
* <span data-ttu-id="7cf4c-507">Версия PowerShell обновлена до 1.0.0.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-507">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="7cf4c-508">Версия пакета SDK обновлена до 1.0.2.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-508">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="7cf4c-509">В тестах обновлены ссылки на новую версию пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-509">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="7cf4c-510">Вложенная выходная структура заменена на плоскую.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-510">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7cf4c-511">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7cf4c-511">Az.IotHub</span></span>
* <span data-ttu-id="7cf4c-512">Добавлен новый источник маршрутизации DigitalTwinChangeEvents.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-512">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="7cf4c-513">Исправлены незначительные ошибки: Get-AzIothub не возвращает subscriptionId.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-513">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span> 

#### <a name="azmonitor"></a><span data-ttu-id="7cf4c-514">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7cf4c-514">Az.Monitor</span></span>
* <span data-ttu-id="7cf4c-515">Добавлены новые получатели групп действий: -ItsmReceiver, -VoiceReceiver, -ArmRoleReceiver, -AzureFunctionReceiver, -LogicAppReceiver, -AutomationRunbookReceiver, -AzureAppPushReceiver.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-515">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="7cf4c-516">Для получателей включите общую схему оповещений.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-516">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="7cf4c-517">Это не касается получателей SMS, push-уведомлений приложения Azure, ITSM и голосовых сообщений.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-517">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="7cf4c-518">Веб-перехватчики теперь поддерживают аутентификацию Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-518">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7cf4c-519">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7cf4c-519">Az.Network</span></span>
* <span data-ttu-id="7cf4c-520">Добавлен новый командлет Get-AzAvailableServiceAlias, позволяющий получить псевдонимы для политик конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-520">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="7cf4c-521">В подключениях шлюза виртуальной сети появилась возможность добавлять селекторы трафика.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-521">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="7cf4c-522">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-522">New cmdlets added:</span></span>
        - <span data-ttu-id="7cf4c-523">New-AzureRmTrafficSelectorPolicy.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-523">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="7cf4c-524">В командлеты добавлены необязательные параметры -TrafficSelectorPolicies, -New-AzureRmVirtualNetworkGatewayConnection, -Set-AzureRmVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-524">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="7cf4c-525">В конфигурациях правил сетевой безопасности добавлена поддержка протоколов ESP и AH.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-525">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="7cf4c-526">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-526">Updated cmdlets:</span></span>
        - <span data-ttu-id="7cf4c-527">Add-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-527">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="7cf4c-528">New-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-528">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="7cf4c-529">Set-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-529">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="7cf4c-530">Улучшена обработка исключений в командлетах Cortex.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-530">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="7cf4c-531">Выпущены новые поколения и номера SKU VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-531">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="7cf4c-532">Представлены новые поколения VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-532">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="7cf4c-533">Представлены новые номера SKU VirtualNetworkGateways с высокой пропускной способностью.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-533">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="7cf4c-534">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="7cf4c-534">Az.RedisCache</span></span>
* <span data-ttu-id="7cf4c-535">В справочную документацию по Set-AzRedisCache добавлены недостающие значения для параметра -Size.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-535">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="7cf4c-536">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7cf4c-536">Az.Sql</span></span>
* <span data-ttu-id="7cf4c-537">Добавлена возможность назначать администратора Active Directory в Управляемом экземпляре.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-537">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7cf4c-538">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7cf4c-538">Az.Storage</span></span>
* <span data-ttu-id="7cf4c-539">Клиентская библиотека службы хранилища Azure обновлена до версии 11.1.0.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-539">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="7cf4c-540">NextPageLink теперь позволяет получить список контейнеров с помощью API плоскости управления.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-540">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="7cf4c-541">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="7cf4c-541">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="7cf4c-542">NextPageLink теперь позволяет получить список учетных записей хранения из подписки.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-542">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="7cf4c-543">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7cf4c-543">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="7cf4c-544">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="7cf4c-544">Az.StorageSync</span></span>
* <span data-ttu-id="7cf4c-545">Исправлена проблема 9810 с Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-545">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7cf4c-546">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7cf4c-546">Az.Websites</span></span>
* <span data-ttu-id="7cf4c-547">Обновление плана службы приложений с помощью Set-AzWebApp приводило к сбою приложения.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-547">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="7cf4c-548">2.7.0 — сентябрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-548">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="7cf4c-549">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7cf4c-549">Az.ApiManagement</span></span>
* <span data-ttu-id="7cf4c-550">В справочной документации по командлету Set-AzApiManagementPolicy обновлено описание параметра -Format.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-550">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="7cf4c-551">Из справочной документации удалены ссылки на нерекомендуемый командлет Update-AzApiManagementDeployment.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-551">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="7cf4c-552">Вместо него следует использовать командлет Set-AzApiManagement.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-552">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7cf4c-553">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7cf4c-553">Az.Automation</span></span>
* <span data-ttu-id="7cf4c-554">В справочной документации по командлету Register-AzAutomationDscNode исправлена опечатка в примере.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-554">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="7cf4c-555">Добавлено уточнение об ограничениях ОС для командлета Register-AzAutomationDSCNode.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-555">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="7cf4c-556">Исправлено исключение пустой ссылки для параметра -Wait в командлете Start-AzAutomationRunbook.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-556">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7cf4c-557">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7cf4c-557">Az.Compute</span></span>
* <span data-ttu-id="7cf4c-558">Добавлен параметр UploadSizeInBytes для командлета New-AzDiskConfig.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-558">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="7cf4c-559">Добавлен добавочный параметр для командлета New-AzSnapshotConfig.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-559">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="7cf4c-560">Для виртуальной машины добавлены такие функции с низким приоритетом:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-560">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="7cf4c-561">Для командлета New-AzVMConfig добавлены параметры MaxPrice, EvictionPolicy и Priority.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-561">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="7cf4c-562">Для командлетов New-AzVmssConfig, Update-AzVM и Update-AzVmss добавлен параметр MaxPrice.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-562">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="7cf4c-563">Для командлета Get-AzAvailabilitySet устранена проблема со ссылкой на виртуальную машину, когда в нем перечисляются все группы доступности в подписке.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-563">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="7cf4c-564">Исправлено исключение NULL для командлета Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-564">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="7cf4c-565">Исправлен метод поиска VHD для относительной конечной позиции.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-565">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="7cf4c-566">Устранена проблема с UltraSSD для командлетов New-AzVM и Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-566">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7cf4c-567">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7cf4c-567">Az.DataFactory</span></span>
* <span data-ttu-id="7cf4c-568">Добавлены 3 новые команды для ADF версии 2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription и Get-AzDataFactoryV2TriggerSubscriptionStatus.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-568">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="7cf4c-569">Пакет SDK ADF для .NET обновлен до версии 4.1.3.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-569">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="7cf4c-570">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="7cf4c-570">Az.HDInsight</span></span>
* <span data-ttu-id="7cf4c-571">Укажите критические изменения.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-571">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7cf4c-572">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7cf4c-572">Az.IotHub</span></span>
* <span data-ttu-id="7cf4c-573">Добавлена поддержка для вызова отработки отказа для IotHub в георегион аварийного восстановления.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-573">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="7cf4c-574">Добавлена поддержка для управления обогащением сообщений для IotHub.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-574">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="7cf4c-575">Ниже перечислены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-575">New cmdlets are:</span></span>
    - <span data-ttu-id="7cf4c-576">Add-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="7cf4c-576">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="7cf4c-577">Get-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="7cf4c-577">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="7cf4c-578">Remove-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="7cf4c-578">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="7cf4c-579">Set-AzIotHubMessageEnrichment.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-579">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7cf4c-580">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7cf4c-580">Az.Monitor</span></span>
* <span data-ttu-id="7cf4c-581">Указание на самую последнюю версию пакета SDK для монитора, т. е. 0.24.1-preview:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-581">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="7cf4c-582">В командлеты метрик добавлены некритические изменения, т. е. перечисление единиц поддерживает несколько новых значений.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-582">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="7cf4c-583">Эти командлеты доступны только для чтения, поэтому входные данные командлетов не будут изменены.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-583">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="7cf4c-584">Актуальная версия API запросов **ActionGroups** — **2019-06-01**. До этого была версия **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-584">The api-version of the **ActionGroups** requests is now **2019-06-01**, before it was **2018-03-01**.</span></span> <span data-ttu-id="7cf4c-585">Тесты сценария обновлены в соответствии с этим изменением.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-585">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="7cf4c-586">В конструкторы классов **EmailReceiver** и **WebhookReceiver** добавлен один новый обязательный аргумент — логическое значение с именем **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-586">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="7cf4c-587">Сейчас для него установлено значение **false**, чтобы скрыть это критическое изменение от командлетов.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-587">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="7cf4c-588">**Примечание**. Это временное изменение, которое должно быть подтверждено командой оповещения.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-588">**NOTE**: this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="7cf4c-589">Порядок аргументов для конструктора класса **Source** (связанного с классом **ScheduledQueryRuleSource**) изменился по сравнению с предыдущим пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-589">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="7cf4c-590">Это изменение требует, чтобы были исправлены два модульных теста: они были скомпилированы, но не прошли тест.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-590">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="7cf4c-591">Порядок аргументов для конструктора класса **AlertingAction** (связанного с классом **ScheduledQueryRuleSource**) изменился по сравнению с предыдущим пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-591">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="7cf4c-592">Это изменение требует, чтобы были исправлены два модульных теста: они были скомпилированы, но не прошли тест.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-592">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="7cf4c-593">Добавлена поддержка критериев динамического порога для оповещения метрики версии 2:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-593">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="7cf4c-594">New-AzMetricAlertRuleV2Criteria: теперь также позволяет создавать критерии динамического порога.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-594">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="7cf4c-595">Add-AzMetricAlertRuleV2: теперь также позволяет принимать критерии динамического порога.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-595">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="7cf4c-596">Добавлены усовершенствования в командлетах запланированных правил запросов (SQR).</span><span class="sxs-lookup"><span data-stu-id="7cf4c-596">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="7cf4c-597">Командлеты будут принимать параметр Location в обоих форматах: расположение (например, eastus) или отображаемое имя расположения (например, "восточная часть США").</span><span class="sxs-lookup"><span data-stu-id="7cf4c-597">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="7cf4c-598">Параметр Enabled проиллюстрирован в файлах справки надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-598">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="7cf4c-599">Добавлены примеры для необязательного параметра ActionGroup.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-599">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="7cf4c-600">Все файлы справки улучшены.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-600">Overall improved help files</span></span>
* <span data-ttu-id="7cf4c-601">Исправлена ошибка в определении типа области для командлета Set-AzActionRule.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-601">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7cf4c-602">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7cf4c-602">Az.Network</span></span>
* <span data-ttu-id="7cf4c-603">Исправлен неправильный пример в справочной документации по командлету New-AzApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-603">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span> 
* <span data-ttu-id="7cf4c-604">В справочную документацию по командлету Get-AzNetworkWatcherPacketCapture добавлено примечание, посвященное извлечению всех свойств для записи пакетов.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-604">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="7cf4c-605">В справочной документации по командлету Test-AzNetworkWatcherIPFlow исправлен пример: теперь он правильно перечисляет сетевые карты.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-605">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="7cf4c-606">Улучшен анализ облачных исключений для отображения дополнительных сведений (при их наличии).</span><span class="sxs-lookup"><span data-stu-id="7cf4c-606">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="7cf4c-607">Улучшен анализ облачных исключений для обработки дополнительного типа исключения SDK.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-607">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="7cf4c-608">Исправлено неправильное сопоставление моделей правил безопасности.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-608">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="7cf4c-609">Добавлены свойства сетевого интерфейса для компонента частного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-609">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="7cf4c-610">Для интерфейса PSNetworkInterface добавлено свойство PrivateEndpoint с типом PSResourceId.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-610">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="7cf4c-611">В PSNetworkInterfaceIPConfiguration добавлено свойство PrivateLinkConnectionProperties с типом PSIpConfigurationConnectivityInformation.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-611">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="7cf4c-612">Добавлен новый класс модели: PSIpConfigurationConnectivityInformation.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-612">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="7cf4c-613">Добавлен новый тип ApplicationRuleProtocolType "mssql" для ресурса Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-613">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="7cf4c-614">Поддержка многоканального подключения в Виртуальной глобальной сети:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-614">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="7cf4c-615">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="7cf4c-615">New cmdlets</span></span>
        - <span data-ttu-id="7cf4c-616">New-AzVpnSiteLink;</span><span class="sxs-lookup"><span data-stu-id="7cf4c-616">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="7cf4c-617">New-AzVpnSiteLinkConnection;</span><span class="sxs-lookup"><span data-stu-id="7cf4c-617">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="7cf4c-618">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-618">Updated cmdlet:</span></span>
        - <span data-ttu-id="7cf4c-619">New-VpnSite;</span><span class="sxs-lookup"><span data-stu-id="7cf4c-619">New-VpnSite</span></span>
        - <span data-ttu-id="7cf4c-620">Update-VpnSite;</span><span class="sxs-lookup"><span data-stu-id="7cf4c-620">Update-VpnSite</span></span>
        - <span data-ttu-id="7cf4c-621">New-VpnConnection;</span><span class="sxs-lookup"><span data-stu-id="7cf4c-621">New-VpnConnection</span></span>
        - <span data-ttu-id="7cf4c-622">Update-VpnConnection.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-622">Update-VpnConnection</span></span>
* <span data-ttu-id="7cf4c-623">Исправлены документы с некоторыми примерами PowerShell для использования командлетов AZ вместо командлетов AzureRM.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-623">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7cf4c-624">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7cf4c-624">Az.RecoveryServices</span></span>
* <span data-ttu-id="7cf4c-625">Для объекта AzureVMpolicy добавлен новый атрибут — ProtectedItemsCount.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-625">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="7cf4c-626">Добавлены тесты для политики виртуальной машины и восстановления исходной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-626">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="7cf4c-627">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7cf4c-627">Az.Resources</span></span>
* <span data-ttu-id="7cf4c-628">Исправлена ошибка, при которой не удавалось вызвать командлет New-AzRoleAssignment без параметра Scope.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-628">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7cf4c-629">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7cf4c-629">Az.ServiceFabric</span></span>
* <span data-ttu-id="7cf4c-630">Исправлена опечатка в примере в справочной документации по командлету Update-AzServiceFabricReliability.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-630">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="7cf4c-631">Добавлены новые командлеты для управления приложениями и службами:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-631">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="7cf4c-632">New-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="7cf4c-632">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="7cf4c-633">New-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="7cf4c-633">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="7cf4c-634">New-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="7cf4c-634">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="7cf4c-635">New-AzServiceFabricService;</span><span class="sxs-lookup"><span data-stu-id="7cf4c-635">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="7cf4c-636">Update-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="7cf4c-636">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="7cf4c-637">Get-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="7cf4c-637">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="7cf4c-638">Get-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="7cf4c-638">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="7cf4c-639">Get-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="7cf4c-639">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="7cf4c-640">Get-AzServiceFabricService;</span><span class="sxs-lookup"><span data-stu-id="7cf4c-640">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="7cf4c-641">Remove-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="7cf4c-641">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="7cf4c-642">Remove-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="7cf4c-642">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="7cf4c-643">Remove-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="7cf4c-643">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="7cf4c-644">Remove-AzServiceFabricServic.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-644">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="7cf4c-645">Пакет SDK для Service Fabric обновлен до версии 1.2.0, в которой используется версия API 2019-03-01 поставщика ресурсов Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-645">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="7cf4c-646">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="7cf4c-646">Az.SignalR</span></span>
* <span data-ttu-id="7cf4c-647">Добавлены командлеты Update, Restart, CheckNameAvailability и GetUsage.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-647">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="7cf4c-648">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7cf4c-648">Az.Sql</span></span>
* <span data-ttu-id="7cf4c-649">Обновлен пример в справочной документации по командлету Get-AzSqlElasticPool.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-649">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="7cf4c-650">Добавлен пример виртуального ядра для командлета создания эластичного пула (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="7cf4c-650">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="7cf4c-651">Удалена проверка свойства EmailAddresses и того, что свойство EmailAdmins правильное в случае, если свойство EmailAddresses пустое в командлетах Set-AzSqlServerAdvancedThreatProtectionPolicy и Set-AzSqlDatabaseAdvancedThreatProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-651">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="7cf4c-652">Теперь, если существует несколько параметров диагностики, включающих категорию аудита, параметры аудита сервера и базы данных удаляются.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-652">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="7cf4c-653">Исправлена проверка адресов электронной почты в нескольких командлетах оценки уязвимостей SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting и Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="7cf4c-653">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7cf4c-654">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7cf4c-654">Az.Storage</span></span>
* <span data-ttu-id="7cf4c-655">Обновлен пример в справочной документации по командлету Get-AzStorageAccountKey.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-655">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="7cf4c-656">Теперь при отправке и загрузке файла Azure в конечном файле сохраняются свойства SMB исходного файла (атрибуты файла, время создания файла, время последней записи файла).</span><span class="sxs-lookup"><span data-stu-id="7cf4c-656">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="7cf4c-657">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="7cf4c-657">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="7cf4c-658">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="7cf4c-658">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="7cf4c-659">Исправлена операция отправки блочного BLOB-объекта, в которой происходили сбои свойств и метаданных в контейнере с включенной ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-659">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="7cf4c-660">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="7cf4c-660">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="7cf4c-661">Добавлена поддержка управления общими папками Azure в API плоскости управления с помощью таких командлетов:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-661">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="7cf4c-662">New-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="7cf4c-662">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="7cf4c-663">Get-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="7cf4c-663">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="7cf4c-664">Update-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="7cf4c-664">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="7cf4c-665">Remove-AzRmStorageShare.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-665">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7cf4c-666">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7cf4c-666">Az.Websites</span></span>
* <span data-ttu-id="7cf4c-667">Устранена проблема, из-за которой теги webapp удалялись при переносе приложения в новый ASP.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-667">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="7cf4c-668">Теперь командлет Publish-AzureWebapp работает в Linux и Windows.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-668">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="7cf4c-669">Обновлен пример в справочной документации по командлету Get-AzWebAppPublishingProfile.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-669">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="7cf4c-670">2.6.0 — август 2019 г.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-670">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="7cf4c-671">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="7cf4c-671">General</span></span>
* <span data-ttu-id="7cf4c-672">Исправлены опечатки в модулях.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-672">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7cf4c-673">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7cf4c-673">Az.Accounts</span></span>
* <span data-ttu-id="7cf4c-674">Добавлена поддержка назначаемого пользователем удостоверения MSI при проверке подлинности в Функциях Azure (№ 9479).</span><span class="sxs-lookup"><span data-stu-id="7cf4c-674">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="7cf4c-675">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="7cf4c-675">Az.Aks</span></span>
* <span data-ttu-id="7cf4c-676">Устранена проблема с выходными данными для Get-AzAks.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-676">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="7cf4c-677">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/9847.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-677">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="7cf4c-678">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7cf4c-678">Az.ApiManagement</span></span>
* <span data-ttu-id="7cf4c-679">исправлена проблема https://github.com/Azure/azure-powershell/issues/9351.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-679">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="7cf4c-680">Обновлена версия NuGet для .NET, которая не накладывает ограничений на productId, apiId, groupId и userId.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-680">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="7cf4c-681">**Get-AzApiManagementProduct**. Добавлена поддержка запросов к продуктам с помощью API.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-681">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="7cf4c-682">**New-AzApiManagementApiRevision**. Устранена проблема, из-за которой не задавался параметр ApiRevisionDescription при создании новой редакции API https://github.com/Azure/azure-powershell/issues/9752.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-682">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="7cf4c-683">Исправлено написание имени модели c PsApiManagementOAuth2AuthrozationServer на PsApiManagementOAuth2AuthorizationServer.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-683">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="7cf4c-684">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="7cf4c-684">Az.Batch</span></span>
* <span data-ttu-id="7cf4c-685">Исправлена опечатка в написании Windows со строчной буквы в справочных сообщениях и документации.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-685">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="7cf4c-686">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7cf4c-686">Az.Cdn</span></span>
* <span data-ttu-id="7cf4c-687">Исправлена опечатка во вспомогательном приложении модуля CDN.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-687">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7cf4c-688">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7cf4c-688">Az.Compute</span></span>
* <span data-ttu-id="7cf4c-689">Добавлен параметр VmssId в новый командлет Add New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-689">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="7cf4c-690">Добавлены параметры TerminateScheduledEvents и TerminateScheduledEventNotBeforeTimeoutInMinutes в New-AzVmssConfig и Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-690">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="7cf4c-691">Добавлено свойство HyperVGeneration в объект образа виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-691">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="7cf4c-692">Добавлены компоненты Host и HostGroup.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-692">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="7cf4c-693">Новые командлеты:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="7cf4c-693">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="7cf4c-694">Параметр HostId добавлен в New-AzVMConfig и New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-694">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="7cf4c-695">Исправлен пример в документации по Invoke-AzVMRunCommand, в котором теперь используется правильное имя параметра.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-695">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="7cf4c-696">Исправлено описание VolumeType в справочной документации по Set-AzVMDiskEncryptionExtension и Set-AzVmssDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-696">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7cf4c-697">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7cf4c-697">Az.DataFactory</span></span>
* <span data-ttu-id="7cf4c-698">Исправлена опечатка в написании Windows со строчной буквы в документации по New-AzDataFactoryEncryptValue.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-698">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="7cf4c-699">Пакет SDK ADF для .NET обновлен до версии 4.1.2.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-699">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="7cf4c-700">Добавлены параметры DataProxyIntegrationRuntimeName, DataProxyStagingLinkedServiceName и DataProxyStagingPath в командлет Set-AzureRmDataFactoryV2IntegrationRuntime, что позволяет настраивать локальную среду выполнения интеграции в качестве прокси-сервера для Azure-SSIS Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-700">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="7cf4c-701">Обновлены PSTriggerRun для отображения активированных конвейеров, сообщений и свойств и PSActivityRun для отображения типа действия.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-701">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7cf4c-702">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7cf4c-702">Az.DataLakeStore</span></span>
* <span data-ttu-id="7cf4c-703">Устранена проблема, при которой Get-DataLakeStoreDeletedItem переставал отвечать на запросы при возникновении ошибок или удаленных исключений.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-703">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7cf4c-704">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7cf4c-704">Az.EventHub</span></span>
* <span data-ttu-id="7cf4c-705">Исправлена проблема № 9658: опечатка в написании параметра VirtualNteworkRule у Set-AzEventHubNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-705">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="7cf4c-706">Исправлена проблема № 9558: в Set-AzEventHubNamespace используется PATCH вместо PUT.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-706">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="7cf4c-707">В командлет Set-AzEventHubNamespace добавлен параметр EnableKafka.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-707">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="7cf4c-708">Исправлена проблема № 9786: не удается создать правило с правами только для прослушивания.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-708">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="7cf4c-709">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="7cf4c-709">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="7cf4c-710">Исправлено написание Azure со строчной буквы.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-710">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7cf4c-711">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7cf4c-711">Az.Monitor</span></span>
* <span data-ttu-id="7cf4c-712">Исправлены неправильные имена параметров в справочной документации.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-712">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7cf4c-713">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7cf4c-713">Az.Network</span></span>
* <span data-ttu-id="7cf4c-714">Обновлен New-AzPrivateLinkServiceIpConfig.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-714">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="7cf4c-715">Параметр PublicIpAddress объявлен нерекомендуемым, так как он не используется на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-715">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="7cf4c-716">Добавлен необязательный параметр Primary, указывающий, является ли текущая IP-конфигурация основной.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-716">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="7cf4c-717">Улучшена обработка исключений из-за ошибок запроса от пакета SDK. Устранена проблема, при которой исключения пакета SDK не обрабатывались правильно, из-за чего не отображались основные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-717">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="7cf4c-718">Настроена логика проверки для префикса IPv6 IP-адреса для проверки правильности длины префикса IPv6.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-718">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span> 
* <span data-ttu-id="7cf4c-719">Обновлен Get-AzVirtualNetworkSubnetConfig: добавлен набор параметров для получения по идентификатору ресурса подсети.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-719">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="7cf4c-720">Обновлено описание параметра Location для AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-720">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7cf4c-721">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7cf4c-721">Az.OperationalInsights</span></span>
* <span data-ttu-id="7cf4c-722">Обновлена документация по New-AzOperationalInsightsLinuxSyslogDataSource.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-722">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="7cf4c-723">Добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-723">Added example</span></span>
    - <span data-ttu-id="7cf4c-724">Обновлено описание параметра -Name.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-724">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="7cf4c-725">Добавлен пример для New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="7cf4c-725">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="7cf4c-726">Изменено описание параметра -Name для New-AzOperationalInsightsWindowsEventDataSource.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-726">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7cf4c-727">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7cf4c-727">Az.RecoveryServices</span></span>
* <span data-ttu-id="7cf4c-728">Обновлен Get-AzRecoveryServicesBackupJobDetail.md.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-728">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="7cf4c-729">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7cf4c-729">Az.Resources</span></span>
* <span data-ttu-id="7cf4c-730">Добавлена поддержка новой версии API 2019-05-10 для Microsoft.Resource.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-730">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="7cf4c-731">Добавлена поддержка copy.count = 0 для переменных, ресурсов и свойств.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-731">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="7cf4c-732">Ресурсы, у которых condition = false или copy.count = 0, будут удаляться в полном режиме.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-732">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="7cf4c-733">В справочную документацию добавлен пример назначения политики на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-733">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="7cf4c-734">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7cf4c-734">Az.ServiceBus</span></span>
* <span data-ttu-id="7cf4c-735">Исправлена проблема № 9658: опечатка в написании параметра VirtualNetworkRule В Set-AzServiceBusNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-735">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="7cf4c-736">Исправлена проблема № 9786: не удается создать правило с правами только для прослушивания.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-736">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="7cf4c-737">Добавлена новая команда Test-AzServiceBusNameAvailability для проверки доступности имени для очереди и раздела.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-737">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span> 

#### <a name="azservicefabric"></a><span data-ttu-id="7cf4c-738">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7cf4c-738">Az.ServiceFabric</span></span>
* <span data-ttu-id="7cf4c-739">Устранены ошибки командлета для добавления типа узла:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-739">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="7cf4c-740">ошибка NullReferenceException, возникавшая, если у группы ресурсов были другие VMSS, не связанные с кластером Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-740">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="7cf4c-741">Исправлена проблема https://github.com/Azure/azure-powershell/issues/8681.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-741">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="7cf4c-742">Исправлена ошибка, из-за которой командлет завершился сбоем, если virtualNetwork находилась не в той группе ресурсов, к которой относится кластер.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-742">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="7cf4c-743">Исправлена проблема https://github.com/Azure/azure-powershell/issues/8407.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-743">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="7cf4c-744">Командлет Add-AzServiceFabricApplicationCertificate объявлен нерекомендуемым.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-744">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="7cf4c-745">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7cf4c-745">Az.Sql</span></span>
* <span data-ttu-id="7cf4c-746">Обновление документации по старым командлетам аудита.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-746">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7cf4c-747">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7cf4c-747">Az.Storage</span></span>
* <span data-ttu-id="7cf4c-748">Обновлена справка по Get/Close-AzStorageFileHandle: в примеры добавлены сценарии использования командлетов и обновлено описание параметров.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-748">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="7cf4c-749">Добавлена поддержка StandardBlobTier в операции отправки BLOB-объекта и копирования BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-749">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="7cf4c-750">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="7cf4c-750">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="7cf4c-751">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="7cf4c-751">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="7cf4c-752">Добавлена поддержка приоритета восстановления в операцию копирования BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-752">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="7cf4c-753">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="7cf4c-753">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7cf4c-754">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7cf4c-754">Az.Websites</span></span>
* <span data-ttu-id="7cf4c-755">Добавлены уточнение для параметра -AppSettings в Set-AzWebApp и Set-AzWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-755">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="7cf4c-756">2.5.0 — июль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-756">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7cf4c-757">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7cf4c-757">Az.Accounts</span></span>
* <span data-ttu-id="7cf4c-758">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-758">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="7cf4c-759">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="7cf4c-759">Az.ApplicationInsights</span></span>
* <span data-ttu-id="7cf4c-760">Исправлена опечатка в примере в документации по Remove-AzApplicationInsightsApiKey.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-760">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span> 

#### <a name="azautomation"></a><span data-ttu-id="7cf4c-761">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7cf4c-761">Az.Automation</span></span>
* <span data-ttu-id="7cf4c-762">Исправлена опечатка в строке ресурса.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-762">Fix typo in resource string</span></span> 

#### <a name="azcognitiveservices"></a><span data-ttu-id="7cf4c-763">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7cf4c-763">Az.CognitiveServices</span></span>
* <span data-ttu-id="7cf4c-764">Добавлена поддержка NetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-764">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7cf4c-765">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7cf4c-765">Az.Compute</span></span>
* <span data-ttu-id="7cf4c-766">Добавлены недостающие свойства (ComputerName, OsName, OsVersion и HyperVGeneration) для объекта представления экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-766">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="7cf4c-767">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="7cf4c-767">Az.ContainerRegistry</span></span>
* <span data-ttu-id="7cf4c-768">Исправлена опечатка в Remove-AzContainerRegistryReplication для параметра репликации.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-768">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="7cf4c-769">См. подробнее: https://github.com/Azure/azure-powershell/issues/9633.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-769">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7cf4c-770">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7cf4c-770">Az.DataFactory</span></span>
* <span data-ttu-id="7cf4c-771">Пакет SDK для ADF .NET обновлен до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-771">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="7cf4c-772">Исправлена опечатка в документации по Get-AzDataFactoryV2PipelineRun.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-772">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7cf4c-773">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7cf4c-773">Az.EventHub</span></span>
* <span data-ttu-id="7cf4c-774">Добавлен новый командлет для создания маркера SAS: New-AzEventHubAuthorizationRuleSASToken.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-774">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="7cf4c-775">Добавлена проверка и сообщение об ошибке в ситуациях, когда для правил авторизации назначаются только права "Управление".</span><span class="sxs-lookup"><span data-stu-id="7cf4c-775">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7cf4c-776">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7cf4c-776">Az.KeyVault</span></span>
* <span data-ttu-id="7cf4c-777">Добавлена поддержка для настройки параметра KeySize в политиках сертификатов.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-777">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="7cf4c-778">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="7cf4c-778">Az.LogicApp</span></span>
* <span data-ttu-id="7cf4c-779">Get-AzIntegrationAccountMap теперь надлежащим образом выводит все типы сопоставлений.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-779">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="7cf4c-780">Добавлен новый параметр MapType для фильтрации.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-780">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="7cf4c-781">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="7cf4c-781">Az.ManagedServices</span></span>
* <span data-ttu-id="7cf4c-782">Добавлена поддержка API версии 2019-06-01 (общедоступная).</span><span class="sxs-lookup"><span data-stu-id="7cf4c-782">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7cf4c-783">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7cf4c-783">Az.Network</span></span>
* <span data-ttu-id="7cf4c-784">Добавлена поддержка частной конечной точки и службы приватного канала.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-784">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="7cf4c-785">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="7cf4c-785">New cmdlets</span></span>
        - <span data-ttu-id="7cf4c-786">Set-AzPrivateEndpoint.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-786">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="7cf4c-787">Set-AzPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-787">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="7cf4c-788">Approve-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-788">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7cf4c-789">Deny-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-789">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7cf4c-790">Get-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-790">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7cf4c-791">Remove-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-791">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="7cf4c-792">Test-AzPrivateLinkServiceVisibility.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-792">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="7cf4c-793">Get-AzAutoApprovedPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-793">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="7cf4c-794">Обновлены следующие команды для функции: Флаг PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies в подсети в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-794">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="7cf4c-795">Обновлены командлеты New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-795">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="7cf4c-796">Добавлен необязательный параметр -PrivateEndpointNetworkPoliciesFlag, который определяет, следует ли применять сетевые политики к частной конечной точке в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-796">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="7cf4c-797">Добавлен необязательный параметр -PrivateLinkServiceNetworkPoliciesFlag, который определяет, следует ли применять сетевые политики к службе приватного канала в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-797">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="7cf4c-798">Параметр ServiceName командлета AzPrivateLinkService был переименован на Name с псевдонимом ServiceName для обеспечения обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-798">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="7cf4c-799">Включен протокол ICMP для настройки правил безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-799">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="7cf4c-800">Обновлены командлеты</span><span class="sxs-lookup"><span data-stu-id="7cf4c-800">Updated cmdlets</span></span>
        - <span data-ttu-id="7cf4c-801">Add-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-801">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="7cf4c-802">New-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-802">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="7cf4c-803">Set-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-803">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="7cf4c-804">Добавлен ConnectionProtocolType (Ikev1/Ikev2) в качестве настраиваемого параметра для командлета New-AzVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-804">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="7cf4c-805">Добавлен PrivateIpAddressVersion в LoadBalancerFrontendIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-805">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="7cf4c-806">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-806">Updated cmdlet:</span></span>
        - <span data-ttu-id="7cf4c-807">New-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-807">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="7cf4c-808">Add-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-808">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="7cf4c-809">Set-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-809">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="7cf4c-810">Команда New-AzApplicationGatewayProbeConfig Шлюза приложений обновлена для поддержки настраиваемого порта в зонде.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-810">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="7cf4c-811">Обновлен командлет New-AzApplicationGatewayProbeConfig: добавлен необязательный параметр Port, который используется при проверке внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-811">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="7cf4c-812">Этот параметр применяется к номерам SKU Standard_V2 и WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-812">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7cf4c-813">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7cf4c-813">Az.OperationalInsights</span></span>
* <span data-ttu-id="7cf4c-814">Обновленная версия по умолчанию для сохраненных операций поиска имеет значение 1.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-814">Updated default version for saved searches to be 1.</span></span> 
* <span data-ttu-id="7cf4c-815">Исправлены ошибки при обработке регулярных выражений со значениями NULL в журналах.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-815">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7cf4c-816">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7cf4c-816">Az.RecoveryServices</span></span>
* <span data-ttu-id="7cf4c-817">Обновлен файл Get-AzRecoveryServicesBackupJob.md.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-817">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="7cf4c-818">Обновлен файл Get-AzRecoveryServicesBackupContainer.md.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-818">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="7cf4c-819">Обновлен файл Get-AzRecoveryServicesVault.md.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-819">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="7cf4c-820">Обновлен файл Wait-AzRecoveryServicesBackupJob.md.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-820">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="7cf4c-821">Обновлен файл Set-AzRecoveryServicesVaultContext.md.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-821">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="7cf4c-822">Обновлен файл Get-AzRecoveryServicesBackupItem.md.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-822">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="7cf4c-823">Обновлен файл Get-AzRecoveryServicesBackupRecoveryPoint.md.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-823">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="7cf4c-824">Обновлен файл Restore-AzRecoveryServicesBackupItem.md.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-824">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="7cf4c-825">Обновлен вызов службы для отмены регистрации контейнера в общей папке Azure.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-825">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="7cf4c-826">Обновлен файл Set-AzRecoveryServicesAsrAlertSetting.md.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-826">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="7cf4c-827">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7cf4c-827">Az.Resources</span></span>
- <span data-ttu-id="7cf4c-828">Удален отсутствующий командлет, который упоминается в документации по New-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-828">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="7cf4c-829">Обновлены командлеты политик для использования новой версии API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-829">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="7cf4c-830">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7cf4c-830">Az.ServiceBus</span></span>
* <span data-ttu-id="7cf4c-831">Добавлен новый командлет для создания маркера SAS: New-AzServiceBusAuthorizationRuleSASToken.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-831">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="7cf4c-832">Добавлена проверка и сообщение об ошибке в ситуациях, когда для правил авторизации назначаются только права "Управление".</span><span class="sxs-lookup"><span data-stu-id="7cf4c-832">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="7cf4c-833">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7cf4c-833">Az.Sql</span></span>
* <span data-ttu-id="7cf4c-834">Исправлены отсутствующие примеры для командлета Set-AzSqlDatabaseSecondary.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-834">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="7cf4c-835">Исправлены заданные повторяющиеся проверки для оценки наличия уязвимостей без указания адресов электронной почты.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-835">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="7cf4c-836">Исправлена незначительная опечатка в сообщении предупреждения.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-836">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7cf4c-837">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7cf4c-837">Az.Storage</span></span>
* <span data-ttu-id="7cf4c-838">Обновлен пример в справочной документации для использования командлетом Get-AzStorageAccount правильного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-838">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="7cf4c-839">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="7cf4c-839">Az.StorageSync</span></span>
* <span data-ttu-id="7cf4c-840">Добавлен командлет Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-840">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="7cf4c-841">Исправлена проблема № 9551, связанная с TierFilesOlderThanDays.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-841">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7cf4c-842">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7cf4c-842">Az.Websites</span></span>
* <span data-ttu-id="7cf4c-843">Исправлена ошибка, при которой некоторые свойства SiteConfig не возвращались Get-AzWebApp и Set-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-843">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="7cf4c-844">Добавлен новый параметр Location в Get-AzDeletedWebApp и Restore-AzDeletedWebApp.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-844">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="7cf4c-845">Исправлена ошибка, которая возникала при клонировании слотов веб-приложений с помощью командлета New-AzWebApp-IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-845">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="7cf4c-846">2.4.0 — июль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-846">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7cf4c-847">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7cf4c-847">Az.Accounts</span></span>
* <span data-ttu-id="7cf4c-848">Добавлена поддержка командлетов профиля.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-848">Add support for profile cmdlets</span></span>
* <span data-ttu-id="7cf4c-849">Добавлена поддержка сред и плоскостей данных в созданных командлетах.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-849">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="7cf4c-850">Исправлена ошибка, когда в командлетах плоскости данных в Windows PowerShell в некоторых случаях использовалась неправильная конечная точка.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-850">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="7cf4c-851">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="7cf4c-851">Az.Advisor</span></span>
* <span data-ttu-id="7cf4c-852">Выпущена общедоступная версия Az.Advisor.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-852">GA release of Az.Advisor</span></span>
* <span data-ttu-id="7cf4c-853">Теперь этот модуль входит в сводный модуль `Az`.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-853">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="7cf4c-854">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7cf4c-854">Az.ApiManagement</span></span>
* <span data-ttu-id="7cf4c-855">исправлена проблема https://github.com/Azure/azure-powershell/issues/8671.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-855">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="7cf4c-856">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="7cf4c-856">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="7cf4c-857">Добавлена поддержка запрашивания подписок по пользователю и продукту.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-857">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="7cf4c-858">Добавлена поддержка создания запросов с использованием области "/", "/apis", "/apis/echo-api".</span><span class="sxs-lookup"><span data-stu-id="7cf4c-858">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="7cf4c-859">Исправлены проблемы https://github.com/Azure/azure-powershell/issues/9307 и https://github.com/Azure/azure-powershell/issues/8432.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-859">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="7cf4c-860">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="7cf4c-860">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="7cf4c-861">Добавлена поддержка указания ApiVersion и ApiVersionSetId при импорте API-интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-861">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7cf4c-862">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7cf4c-862">Az.Automation</span></span>
* <span data-ttu-id="7cf4c-863">Исправлена ошибка командлета Set-AzAutomationConnectionFieldValue при обработке строкового значения.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-863">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7cf4c-864">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7cf4c-864">Az.Compute</span></span>
* <span data-ttu-id="7cf4c-865">В New AzImageConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-865">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7cf4c-866">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7cf4c-866">Az.DataFactory</span></span>
* <span data-ttu-id="7cf4c-867">Обновление выходных данных командлетов ADF, предназначенных для получения числа выполнений действий, конвейеров и триггеров, для поддержки канала Select-Object.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-867">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="7cf4c-868">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="7cf4c-868">Az.EventGrid</span></span>
* <span data-ttu-id="7cf4c-869">Исправлена опечатка в документации по командлету New-AzEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-869">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7cf4c-870">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7cf4c-870">Az.IotHub</span></span>
* <span data-ttu-id="7cf4c-871">Добавлена поддержка повторного создания ключей политики авторизации.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-871">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7cf4c-872">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7cf4c-872">Az.Network</span></span>
* <span data-ttu-id="7cf4c-873">К тегам общедоступного IP-адреса добавлен тег RoutingPreference.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-873">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="7cf4c-874">Улучшены примеры для справочной документации по командлету Get-AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-874">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="7cf4c-875">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="7cf4c-875">Az.PolicyInsights</span></span>
* <span data-ttu-id="7cf4c-876">Исправлена проблема с пустой ссылкой в командлете Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-876">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="7cf4c-877">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/9446.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-877">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7cf4c-878">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7cf4c-878">Az.OperationalInsights</span></span>
* <span data-ttu-id="7cf4c-879">Исправленная модель источника данных CustomLog возвращена в командлет Get-AzOperationalInsightsDataSource.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-879">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7cf4c-880">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7cf4c-880">Az.RecoveryServices</span></span>
* <span data-ttu-id="7cf4c-881">Выпущено исправление для команды get-policy для виртуальных машин IaaS.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-881">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="7cf4c-882">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7cf4c-882">Az.Resources</span></span>
    - <span data-ttu-id="7cf4c-883">Исправлен текст справки по параметру Get-AzPolicyState -Top.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-883">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="7cf4c-884">Добавлена поддержка разбиения по страницам на стороне клиента для Get-AzPolicyAlias.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-884">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="7cf4c-885">Добавлены новые параметры для Set-AzPolicyAssignment, -PolicyParameters и -PolicyParametersObject.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-885">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="7cf4c-886">Добавлен ряд обновлений документов и примеров для командлетов политик.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-886">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="7cf4c-887">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7cf4c-887">Az.ServiceBus</span></span>
* <span data-ttu-id="7cf4c-888">Исправление ошибки № 4938: командлет New-AzureRmServiceBusQueue возвращает ответ BadRequest (Недопустимый запрос) при задании значения MaxSizeInMegabytes.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-888">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="7cf4c-889">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7cf4c-889">Az.Sql</span></span>
* <span data-ttu-id="7cf4c-890">Из выпуска предварительной версии в выпуск общедоступной версии добавлены командлеты группы отработки отказа экземпляра.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-890">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="7cf4c-891">Поддержка аудита Azure SQL Server и баз данных с помощью новых командлетов:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-891">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="7cf4c-892">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="7cf4c-892">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="7cf4c-893">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="7cf4c-893">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="7cf4c-894">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="7cf4c-894">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="7cf4c-895">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="7cf4c-895">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="7cf4c-896">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="7cf4c-896">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="7cf4c-897">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="7cf4c-897">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="7cf4c-898">Из параметров оценки уязвимостей удалены ограничения, касающиеся электронной почты.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-898">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7cf4c-899">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7cf4c-899">Az.Storage</span></span>
* <span data-ttu-id="7cf4c-900">Два параметра в указанном ниже командлете — -IndexDocument и -ErrorDocument404Path, — которые ранее были обязательными, стали необязательными:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-900">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="7cf4c-901">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="7cf4c-901">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="7cf4c-902">Обновлена справка по командлету Get-AzStorageBlobContent: добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-902">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="7cf4c-903">При сбое выполнения командлета с ошибкой StorageException отображаются дополнительные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-903">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="7cf4c-904">Добавлена поддержка создания или обновления учетной записи хранения с использованием проверки подлинности AAD DS для службы "Файлы Azure".</span><span class="sxs-lookup"><span data-stu-id="7cf4c-904">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="7cf4c-905">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7cf4c-905">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="7cf4c-906">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7cf4c-906">Set-AzStorageAccount</span></span>
* <span data-ttu-id="7cf4c-907">Добавлена поддержка перечисления или закрытия дескрипторов файлов для общей папки, каталога файлов или файла:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-907">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="7cf4c-908">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="7cf4c-908">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="7cf4c-909">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="7cf4c-909">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="7cf4c-910">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="7cf4c-910">Az.StorageSync</span></span>
* <span data-ttu-id="7cf4c-911">Теперь этот модуль входит в сводный модуль `Az`.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-911">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="7cf4c-912">2.3.2 — июнь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-912">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7cf4c-913">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7cf4c-913">Az.Accounts</span></span>
* <span data-ttu-id="7cf4c-914">Исправлена ошибка, связанная с использованием неправильного URL-адреса для вызовов функций.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-914">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="7cf4c-915">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8983.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-915">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="7cf4c-916">Устранена проблема с псевдонимами из AzureRM для командлетов Az.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-916">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="7cf4c-917">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-917">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="7cf4c-918">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-918">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7cf4c-919">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7cf4c-919">Az.Compute</span></span>
* <span data-ttu-id="7cf4c-920">Простые наборы параметров New-AzVm и New-AzVmss теперь принимают параметр ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-920">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="7cf4c-921">Исправлена опечатка в справочной документации по New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-921">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="7cf4c-922">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="7cf4c-922">Az.Dns</span></span>
* <span data-ttu-id="7cf4c-923">Исправлена опечатка в справочных примерах по использованию Set-AzDnsZone.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-923">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="7cf4c-924">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="7cf4c-924">Az.EventGrid</span></span>
* <span data-ttu-id="7cf4c-925">Обновлен для использования API версии 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-925">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="7cf4c-926">Новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-926">New cmdlets:</span></span>
    - <span data-ttu-id="7cf4c-927">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="7cf4c-927">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="7cf4c-928">Создает домен Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-928">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="7cf4c-929">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="7cf4c-929">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="7cf4c-930">Возвращает сведения о домене Сетки событий или список всех доменов Сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-930">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="7cf4c-931">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="7cf4c-931">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="7cf4c-932">Удаляет домен Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-932">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="7cf4c-933">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="7cf4c-933">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="7cf4c-934">Повторно создает ключ общего доступа для домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-934">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="7cf4c-935">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="7cf4c-935">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="7cf4c-936">Возвращает ключи общего доступа, используемые для публикации событий в домене Сетки событий.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-936">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="7cf4c-937">New-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="7cf4c-937">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="7cf4c-938">Создает раздел домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-938">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="7cf4c-939">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="7cf4c-939">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="7cf4c-940">Возвращает сведения о разделе домена Сетки событий или список всех разделов определенного домена Сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-940">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span> 
    - <span data-ttu-id="7cf4c-941">Remove-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="7cf4c-941">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="7cf4c-942">Удаляет раздел домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-942">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="7cf4c-943">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-943">Updated cmdlets:</span></span>
    - <span data-ttu-id="7cf4c-944">New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="7cf4c-944">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="7cf4c-945">Добавляют новые обязательные параметры, обеспечивающие поддержку передачи по конвейеру для нового домена Сетки событий и раздела домена Сетки событий и позволяющие создавать подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-945">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="7cf4c-946">Добавляют новые обязательные параметры для указания имени нового домена Сетки событий и (или) имени раздела домена Сетки событий и позволяют создавать подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-946">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="7cf4c-947">Добавляют новые наборы параметров для доменов и разделов домена и позволяют повторно использовать существующие параметры (например, EndPointType, SubjectBeginsWith и т. д.).</span><span class="sxs-lookup"><span data-stu-id="7cf4c-947">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="7cf4c-948">Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-948">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="7cf4c-949">срока действия подписки на событие;</span><span class="sxs-lookup"><span data-stu-id="7cf4c-949">Event subscription expiration date,</span></span>
            - <span data-ttu-id="7cf4c-950">параметров расширенной фильтрации.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-950">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="7cf4c-951">Добавляют новое перечисление для ServiceBusQueue в качестве места назначения.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-951">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="7cf4c-952">Запрещают использование значение All в параметре -IncludedEventType и заменяют его следующим:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-952">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span> 
    - <span data-ttu-id="7cf4c-953">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="7cf4c-953">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="7cf4c-954">Добавляют новые необязательные параметры (Top, ODataQuery и NextLink) для поддержки разбиения на страницы и фильтрации результатов.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-954">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="7cf4c-955">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="7cf4c-955">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="7cf4c-956">Добавляют новые обязательные параметры, обеспечивающие поддержку передачи по конвейеру для домена Сетки событий и раздела домена Сетки событий и позволяющие удалять подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-956">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="7cf4c-957">Добавляют новые обязательные параметры для указания имени домена Сетки событий и (или) имени раздела домена Сетки событий и позволяют удалять подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-957">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="7cf4c-958">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="7cf4c-958">Az.FrontDoor</span></span>
* <span data-ttu-id="7cf4c-959">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="7cf4c-959">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="7cf4c-960">Добавляет поддержку преобразований и новое значение оператора автозавершения (RegEx).</span><span class="sxs-lookup"><span data-stu-id="7cf4c-960">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="7cf4c-961">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="7cf4c-961">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="7cf4c-962">Добавляет новые значения автозавершения.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-962">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7cf4c-963">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7cf4c-963">Az.Network</span></span>
* <span data-ttu-id="7cf4c-964">Добавляет поддержку ресурса шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-964">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="7cf4c-965">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="7cf4c-965">New cmdlets</span></span>
        - <span data-ttu-id="7cf4c-966">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="7cf4c-966">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="7cf4c-967">Добавляет AvailablePrivateEndpointType.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-967">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="7cf4c-968">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="7cf4c-968">New cmdlets</span></span> 
        - <span data-ttu-id="7cf4c-969">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="7cf4c-969">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="7cf4c-970">Добавляет PrivatePrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-970">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="7cf4c-971">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="7cf4c-971">New cmdlets</span></span> 
        - <span data-ttu-id="7cf4c-972">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7cf4c-972">Get-AzPrivateLinkService</span></span> 
        - <span data-ttu-id="7cf4c-973">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7cf4c-973">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="7cf4c-974">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="7cf4c-974">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="7cf4c-975">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="7cf4c-975">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="7cf4c-976">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7cf4c-976">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="7cf4c-977">Добавляет PrivateEndpoint.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-977">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="7cf4c-978">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="7cf4c-978">New cmdlets</span></span>
        - <span data-ttu-id="7cf4c-979">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="7cf4c-979">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="7cf4c-980">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="7cf4c-980">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="7cf4c-981">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="7cf4c-981">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="7cf4c-982">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="7cf4c-982">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="7cf4c-983">Обновлены следующие команды для функции: флаг UseLocalAzureIpAddress для VPN-подключения.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-983">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="7cf4c-984">Обновлен командлет New-AzVpnConnection. Добавлен необязательный параметр -UseLocalAzureIpAddress для указания того, что локальный IP-адрес Azure следует использовать в качестве исходного адреса при инициации подключения.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-984">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="7cf4c-985">Обновлен командлет Set-AzVpnConnection. Добавлен необязательный параметр -UseLocalAzureIpAddress для указания того, что локальный IP-адрес Azure следует использовать в качестве исходного адреса при инициации подключения.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-985">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="7cf4c-986">В пиринг ExpressRoute добавлено поле только для чтения PeeredConnections.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-986">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="7cf4c-987">В ExpressRoute добавлено поле только для чтения GlobalReachEnabled.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-987">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="7cf4c-988">Добавлен атрибут в рамках критического изменения, отменяющего статус устаревшего поля AllowGlobalReach в модели ExpressRouteCircuit.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-988">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="7cf4c-989">Исправлена проблема, связанная с ошибкой 8756, при использовании TargetListenerID с командлетами AzApplicationGatewayRedirectConfiguration.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-989">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="7cf4c-990">Исправлена ошибка в New-AzApplicationGatewayPathRuleConfig, не позволявшая задавать набор правил повторного создания.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-990">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="7cf4c-991">Исправлено отображение VirtualNetworkTaps в NetworkInterfaceIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-991">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="7cf4c-992">Исправлены командлеты Cortex Get для отображения всех частей.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-992">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="7cf4c-993">Исправлено создание ссылок VirtualHub для ExpressRouteGateways и VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-993">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="7cf4c-994">В AzureFirewall и NatGateway добавлена поддержка Зон доступности.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-994">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="7cf4c-995">Добавлен командлет Get-AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-995">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="7cf4c-996">Добавлена поддержка нескольких общедоступных IP-адресов для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-996">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="7cf4c-997">Обновлен командлет New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-997">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="7cf4c-998">Добавлен параметр -PublicIpAddress, который принимает один или несколько объектов общедоступных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-998">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="7cf4c-999">Добавлен параметр -VirtualNetwork, который принимает объект виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-999">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="7cf4c-1000">Добавлены методы AddPublicIpAddress и RemovePublicIpAddress для объекта брандмауэра. Они принимают объект общедоступного IP-адреса в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1000">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="7cf4c-1001">Не рекомендуется использовать параметры -PublicIpName и -VirtualNetworkName.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1001">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span> 
* <span data-ttu-id="7cf4c-1002">Обновлены следующие команды для функции: В параметрах проверки подлинности AAD VPN-клиента задан ресурс шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1002">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span> 
    - <span data-ttu-id="7cf4c-1003">Обновлен командлет New-AzVirtualNetworkGateway: Добавлены необязательные параметры AadTenantUri, AadAudienceId, AadIssuerUri для возможности задавать в шлюзе параметры проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1003">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="7cf4c-1004">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлены необязательные параметры AadTenantUri, AadAudienceId, AadIssuerUri для возможности задавать в шлюзе параметры проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1004">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="7cf4c-1005">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлен необязательный параметр-переключатель RemoveAadAuthentication для удаления в шлюзе параметров проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1005">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7cf4c-1006">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1006">Az.OperationalInsights</span></span>
* <span data-ttu-id="7cf4c-1007">Добавлена поддержка SKU **pergb2018** в команде New-AzureRmOperationalInsightsWorkspace.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1007">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="7cf4c-1008">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1008">Az.Resources</span></span>
* <span data-ttu-id="7cf4c-1009">Поддержка дополнительных вариантов экспорта шаблона.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1009">Support for additional Template Export options</span></span>
    - <span data-ttu-id="7cf4c-1010">В Export-AzResourceGroup добавлен параметр -SkipResourceNameParameterization.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1010">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="7cf4c-1011">В Export-AzResourceGroup добавлен параметр -SkipAllParameterization.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1011">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="7cf4c-1012">В Export-AzResourceGroup добавлен параметр -Resource для фильтрации экспортированных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1012">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7cf4c-1013">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1013">Az.ServiceFabric</span></span>
* <span data-ttu-id="7cf4c-1014">Исправлена ошибка, связанная с получением иногда неправильных отпечатков при добавлении сертификата ByExistingKeyVault.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1014">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="7cf4c-1015">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1015">Az.Sql</span></span>
* <span data-ttu-id="7cf4c-1016">Исправлен суффикс конечной точки хранилища службы "Расширенная защита от угроз Azure".</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1016">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="7cf4c-1017">Исправлена ошибка, связанная с возможностью пакета "Расширенная защита данных" переопределять политику службы "Расширенная защита от угроз".</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1017">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="7cf4c-1018">Новые командлеты для Management.Sql позволяют клиентам добавлять ключи TDE и задавать средство защиты TDE для управляемых экземпляров.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1018">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="7cf4c-1019">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1019">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="7cf4c-1020">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1020">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="7cf4c-1021">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1021">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="7cf4c-1022">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1022">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="7cf4c-1023">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1023">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7cf4c-1024">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1024">Az.Storage</span></span>
* <span data-ttu-id="7cf4c-1025">Поддержка класса Kind в FileStorage и значения Premium_ZRS в SkuName при создании учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1025">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="7cf4c-1026">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1026">New-AzStorageAccount</span></span>
* <span data-ttu-id="7cf4c-1027">Уточнено описание командлета неизменности BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1027">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="7cf4c-1028">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1028">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7cf4c-1029">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1029">Az.Websites</span></span>
* <span data-ttu-id="7cf4c-1030">Оптимизирует Get-AzWebAppCertificate для фильтрации по группе ресурсов на сервере, а не в клиенте.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1030">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="7cf4c-1031">Добавляет параметр-переключатель - UseDisasterRecovery в Get AzWebAppSnapshot.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1031">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="7cf4c-1032">2.2.0 — июнь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1032">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="7cf4c-1033">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1033">Az.Cdn</span></span>
* <span data-ttu-id="7cf4c-1034">Обновлены командлеты для поддержки функции rulesEngine на основе API версии 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1034">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7cf4c-1035">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1035">Az.Compute</span></span>
* <span data-ttu-id="7cf4c-1036">Добавлен параметр `NoWait`, который запускает операцию и немедленно возвращает значение еще до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1036">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="7cf4c-1037">Обновлены командлеты:   Export-AzLogAnalyticRequestRateByInterval; Export-AzLogAnalyticThrottledRequest; Remove-AzVM; Remove-AzVMAccessExtension; Remove-AzVMAEMExtension; Remove-AzVMChefExtension; Remove-AzVMCustomScriptExtension; Remove-AzVMDiagnosticsExtension; Remove-AzVMDiskEncryptionExtension; Remove-AzVMDscExtension; Remove-AzVMSqlServerExtension; Restart-AzVM; Set-AzVM; Set-AzVMAccessExtension; Set-AzVMADDomainExtension; Set-AzVMAEMExtension; Set-AzVMBginfoExtension; Set-AzVMChefExtension; Set-AzVMCustomScriptExtension; Set-AzVMDiagnosticsExtension; Set-AzVMDscExtension; Set-AzVMExtension; Start-AzVM; Stop-AzVM; Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1037">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7cf4c-1038">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1038">Az.EventHub</span></span>
* <span data-ttu-id="7cf4c-1039">Исправлена ошибка № 9231. Командлет Get-AzEventHubNamespace не возвращал теги.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1039">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="7cf4c-1040">Исправлена ошибка № 9230. Командлет Get-AzEventHubNamespace возвращал значение ResourceGroup вместо ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1040">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7cf4c-1041">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1041">Az.Network</span></span>
* <span data-ttu-id="7cf4c-1042">Обновлены параметры ResourceId и InputObject для ресурса Шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1042">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="7cf4c-1043">Добавлены псевдонимы для параметров ResourceId и InputObject.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1043">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="7cf4c-1044">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1044">Az.PolicyInsights</span></span>
* <span data-ttu-id="7cf4c-1045">Исправлена проблема с пустой ссылкой в командлете Get-AzPolicyEvent.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1045">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7cf4c-1046">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1046">Az.RecoveryServices</span></span>
* <span data-ttu-id="7cf4c-1047">Минимальный срок хранения политики IaaSVM изменился с 1 до 7 дней.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1047">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="7cf4c-1048">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1048">Az.ServiceBus</span></span>
* <span data-ttu-id="7cf4c-1049">Исправлена ошибка № 9182. Командлет Get-AzServiceBusNamespace возвращал ResourceGroup вместо ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1049">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7cf4c-1050">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1050">Az.ServiceFabric</span></span>
* <span data-ttu-id="7cf4c-1051">Исправлена опечатка в сообщении об ошибке для командлета Update-AzServiceFabricReliability.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1051">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="7cf4c-1052">Исправлен отсутствующей символ в командных строках Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1052">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="7cf4c-1053">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1053">Az.Sql</span></span>
* <span data-ttu-id="7cf4c-1054">Для командлета New-AzureSqlInstance добавлен параметр DnsZonePartner, обеспечивающий поддержку AutoDr для Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1054">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="7cf4c-1055">Командлет Get-AzSqlDatabaseSecureConnectionPolicy объявлен неподдерживаемым.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1055">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="7cf4c-1056">Командлеты обнаружения угроз переименованы в командлеты Расширенной защиты от угроз.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1056">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="7cf4c-1057">Параметры -StorageSizeInGB и -LicenseType командлета New-AzSqlInstance теперь необязательны.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1057">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7cf4c-1058">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1058">Az.Websites</span></span>
* <span data-ttu-id="7cf4c-1059">Исправлены проблемы, когда удалялись теги при использовании Set-AzWebApp и Set-AzWebAppSlot со свойством -WebApp.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1059">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="7cf4c-1060">2.1.0 — май 2019 г.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1060">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="7cf4c-1061">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1061">Az.ApiManagement</span></span>
* <span data-ttu-id="7cf4c-1062">Созданы командлеты для управления диагностикой в глобальной области и в области API.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1062">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="7cf4c-1063">**Get-AzApiManagementDiagnostic** — получение диагностики, заданной глобально или на уровне области API.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1063">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="7cf4c-1064">**New-AzApiManagementDiagnostic** — создание диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1064">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="7cf4c-1065">**New-AzApiManagementHttpMessageDiagnostic** — создание параметра диагностики, для которого регистрируются заголовки и размер байтов тела.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1065">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="7cf4c-1066">**New-AzApiManagementPipelineDiagnosticSetting** — создание параметров диагностики для сообщений HTTP, поступающих в шлюз или исходящих из него.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1066">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="7cf4c-1067">**New-AzApiManagementSamplingSetting** — создание параметра выборки для запросов и ответов касательно диагностики.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1067">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="7cf4c-1068">**Remove-AzApiManagementDiagnostic** — удаление объекта диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1068">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="7cf4c-1069">**Set-AzApiManagementDiagnostic** — обновление объекта диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1069">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="7cf4c-1070">Созданы командлеты для управления кэшем в службе ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1070">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="7cf4c-1071">**Get-AzApiManagementCache** — получение сведений о кэше, указанном идентификатором, или обо всех кэшах.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1071">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="7cf4c-1072">**New-AzApiManagementCache** — создание кэша по умолчанию или кэша в определенном регионе Azure.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1072">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="7cf4c-1073">**Remove-AzApiManagementCache** — удаление кэша.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1073">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="7cf4c-1074">**Update-AzApiManagementCache** — обновление кэша.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1074">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="7cf4c-1075">Созданы командлеты для управления схемой API.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1075">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="7cf4c-1076">**New-AzApiManagementSchema** — создание схемы для API.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1076">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="7cf4c-1077">**Get-AzApiManagementSchema** — получение схем, настроенных в API.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1077">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="7cf4c-1078">**Remove-AzApiManagementSchema** — удаление схемы, настроенной в API.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1078">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="7cf4c-1079">**Set-AzApiManagementSchema** — обновление схемы, настроенной в API.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1079">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="7cf4c-1080">Создан командлет для создания токена пользователя.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1080">Created new Cmdlet for generating a User Token.</span></span> 
    - <span data-ttu-id="7cf4c-1081">**New-AzApiManagementUserToken** — создание токена пользователя, по умолчанию действительного в течение 8 часов. С помощью этого командлета можно создавать токен для пользователя GIT.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1081">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="7cf4c-1082">Создан командлет для получения состояния сети.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1082">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="7cf4c-1083">**Get-AzApiManagementNetworkStatus** — получение состояния сети ресурсов, от которых зависит служба "Управление API".</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1083">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="7cf4c-1084">Это полезно при развертывании службы ApiManagement в виртуальной сети и проверке того, не нарушена ли какая-либо из зависимостей.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1084">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="7cf4c-1085">Обновлен командлет **New-AzApiManagement** для управления службой ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1085">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span> 
    - <span data-ttu-id="7cf4c-1086">Добавлена поддержка нового SKU Consumption.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1086">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="7cf4c-1087">Добавлена поддержка для включения флага EnableClientCertificate в SKU Consumption.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1087">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="7cf4c-1088">Новый командлет **New-AzApiManagementSslSetting** позволяет настраивать параметр TLS/SSL для сервера (Backend) и внешнего интерфейса (Frontend).</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1088">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="7cf4c-1089">Его также можно использовать для настройки Ciphers как 3DES, в ServerProtocols как Http2 для внешнего интерфейса (Frontend) службы ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1089">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="7cf4c-1090">Добавлена поддержка настройки имени узла DeveloperPortal в службе ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1090">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="7cf4c-1091">Обновлен командлет **Get-AzApiManagementSsoToken** для извлечения объекта PsApiManagement в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1091">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="7cf4c-1092">Обновлен командлет для отображения встроенных сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1092">Updated the cmdlet to display Error Messages inline</span></span> 
     > <span data-ttu-id="7cf4c-1093">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Код ошибки: ValidationError. Сообщение об ошибке: "Некоторые поля содержат неправильные значения". Сведения об ошибке: [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1093">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="7cf4c-1094">Обновлен командлет **Export-AzApiManagementApi** для экспортирования программных интерфейсов в формате OpenApi 3.0.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1094">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="7cf4c-1095">Обновлен командлет **Import-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1095">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="7cf4c-1096">Для импортирования API из спецификации документа OpenApi 3.0.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1096">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="7cf4c-1097">Для переопределения свойства PsApiManagementSchema, указанного в любом документе (Swagger, Wadl, Wsdl, OpenApi).</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1097">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="7cf4c-1098">Для переопределения свойства ServiceUrl, указанного в любом документе.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1098">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="7cf4c-1099">Обновлен командлет **Get-AzApiManagementPolicy** для возврата политики в формате, экранированном не для XML, с использованием rawxml.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1099">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="7cf4c-1100">Обновлен командлет **Set-AzApiManagementPolicy**. Он принимает политику в формате, экранированном не для XML, с использованием rawxml и в формате, экранированном для XML, с использованием XML.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1100">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="7cf4c-1101">Обновлен командлет **New-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1101">Updated cmdlet **New-AzApiManagementApi**</span></span> 
    - <span data-ttu-id="7cf4c-1102">Для настройки API с помощью сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1102">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="7cf4c-1103">Для создания API в ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1103">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="7cf4c-1104">Для клонирования API с использованием значений SourceApiId и SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1104">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="7cf4c-1105">Возможность настройки параметра SubscriptionRequired в области API.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1105">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="7cf4c-1106">Обновлен командлет **Set-AzApiManagementApi**:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1106">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="7cf4c-1107">Для настройки API с помощью сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1107">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="7cf4c-1108">Для обновления API в ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1108">To updated an API into an 'ApiVersionSet'</span></span>    
    - <span data-ttu-id="7cf4c-1109">Возможность настройки параметра SubscriptionRequired в области API.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1109">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span> 
* <span data-ttu-id="7cf4c-1110">Обновлен командлет **New-AzApiManagementRevision**:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1110">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="7cf4c-1111">Для клонирования (копирования тегов, продуктов, операций и политик) существующей редакции с использованием SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1111">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="7cf4c-1112">Новая редакция предполагает родительский идентификатор ApiId.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1112">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="7cf4c-1113">Для предоставления ApiRevisionDescription.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1113">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="7cf4c-1114">Для переопределения значения ServiceUrl при клонировании API.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1114">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="7cf4c-1115">Обновлен командлет **New-AzApiManagementIdentityProvider**:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1115">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="7cf4c-1116">Для настройки AAD или AADB2C с Authority.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1116">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="7cf4c-1117">Для установки политик SignupPolicy, SigninPolicy, ProfileEditingPolicy и PasswordResetPolicy.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1117">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="7cf4c-1118">Обновлен командлет **New-AzApiManagementSubscription**.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1118">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="7cf4c-1119">Для учета новой модели SubscriptonModel с помощью Scope и UserId.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1119">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="7cf4c-1120">Для учета прежней модели подписки с помощью ProductId и UserId.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1120">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="7cf4c-1121">Добавлена поддержка для включения AllowTracing на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1121">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="7cf4c-1122">Обновлен командлет **Set-AzApiManagementSubscription**.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1122">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="7cf4c-1123">Для учета новой модели SubscriptonModel с помощью Scope и UserId.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1123">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="7cf4c-1124">Для учета прежней модели подписки с помощью ProductId и UserId.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1124">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="7cf4c-1125">Добавлена поддержка для включения AllowTracing на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1125">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="7cf4c-1126">Следующие командлеты обновлены, чтобы принимать значение ResourceId в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1126">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="7cf4c-1127">New-AzApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1127">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="7cf4c-1128">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1128">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="7cf4c-1129">Get-AzApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1129">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="7cf4c-1130">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1130">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="7cf4c-1131">Get-AzApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1131">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="7cf4c-1132">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1132">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="7cf4c-1133">Get-AzApiManagementAuthorizationServer.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1133">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="7cf4c-1134">Get-AzApiManagementBackend.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1134">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="7cf4c-1135">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1135">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="7cf4c-1136">Get-AzApiManagementCertificate.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1136">'Get-AzApiManagementCertificate'</span></span> 
    - <span data-ttu-id="7cf4c-1137">Remove-AzApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1137">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="7cf4c-1138">Remove-AzApiManagementSubscription.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1138">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7cf4c-1139">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1139">Az.Automation</span></span>
* <span data-ttu-id="7cf4c-1140">Обновлен командлет Get-AzAutomationJobOutputRecord для обработки значений в формате JSON и в виде текстовой записи.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1140">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="7cf4c-1141">исправлена проблема https://github.com/Azure/azure-powershell/issues/7977.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1141">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="7cf4c-1142">исправлена проблема https://github.com/Azure/azure-powershell/issues/8600.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1142">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="7cf4c-1143">Поведение командлета Start-AzAutomationDscCompilationJob изменено так, чтобы сразу же запустить задание, а не ждать его завершения.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1143">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="7cf4c-1144">исправлена проблема https://github.com/Azure/azure-powershell/issues/8347.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1144">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="7cf4c-1145">Исправлен командлет Get-AzAutomationDscNode, возвращающий все узлы при использовании -Name.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1145">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="7cf4c-1146">Теперь он возвращает только соответствующий узел.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1146">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7cf4c-1147">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1147">Az.Compute</span></span>
* <span data-ttu-id="7cf4c-1148">Добавлены параметры ProtectFromScaleIn и ProtectFromScaleSetAction для командлета Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1148">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="7cf4c-1149">Командлет New-AzVM с простым набором параметров теперь по умолчанию использует доступное расположение, если регион "восточная часть США" не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1149">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7cf4c-1150">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1150">Az.DataLakeStore</span></span>
* <span data-ttu-id="7cf4c-1151">Обновлен пакет SDK ADLS для использования httpclient. В инфраструктуру Azure интегрирована проверка плоскости данных.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1151">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7cf4c-1152">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1152">Az.Monitor</span></span>
* <span data-ttu-id="7cf4c-1153">Исправлены неправильные имена параметров в справочных примерах.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1153">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7cf4c-1154">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1154">Az.Network</span></span>
* <span data-ttu-id="7cf4c-1155">Добавлен флаг DisableBgpRoutePropagation для выходных данных действующей таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1155">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="7cf4c-1156">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1156">Updated cmdlet:</span></span>
        - <span data-ttu-id="7cf4c-1157">Get-AzEffectiveRouteTable.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1157">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="7cf4c-1158">Исправлен двойной дефис в документации New-AzApplicationGatewayTrustedRootCertificate.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1158">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="7cf4c-1159">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1159">Az.Resources</span></span>
* <span data-ttu-id="7cf4c-1160">Добавлен новый командлет Get-AzureRmDenyAssignment для получения запрещающих назначений.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1160">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="7cf4c-1161">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1161">Az.Sql</span></span>
* <span data-ttu-id="7cf4c-1162">Командлеты Расширенной защиты от угроз переименованы на командлеты Расширенной защиты данных, и оценка уязвимости включена по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1162">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="7cf4c-1163">2.0.0 — май 2019 г.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1163">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7cf4c-1164">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1164">Az.Accounts</span></span>
* <span data-ttu-id="7cf4c-1165">Обновлена библиотека аутентификации для устранения проблем с ADFS при использовании аутентификации на основе имени пользователя и пароля.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1165">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="7cf4c-1166">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1166">Az.CognitiveServices</span></span>
* <span data-ttu-id="7cf4c-1167">Отображается только заявление об отказе Bing для служб Поиска Bing.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1167">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="7cf4c-1168">Исправлена проблема с созданием учетной записи.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1168">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7cf4c-1169">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1169">Az.Compute</span></span>
* <span data-ttu-id="7cf4c-1170">Функция группы размещения близкого взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1170">Proximity placement group feature.</span></span>
    - <span data-ttu-id="7cf4c-1171">Добавлены следующие новые командлеты:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1171">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="7cf4c-1172">Новый параметр ProximityPlacementGroupId будет добавлен в следующие командлеты:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1172">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="7cf4c-1173">В командлет New-AzGalleryImageVersion добавлен параметр StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1173">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="7cf4c-1174">TargetRegion в командлете New-AzGalleryImageVersion может содержать StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1174">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="7cf4c-1175">Параметр-переключатель SkipShutdown добавлен в командлеты Stop-AzVM и Stop-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1175">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>       
* <span data-ttu-id="7cf4c-1176">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1176">Breaking changes</span></span>
    - <span data-ttu-id="7cf4c-1177">Командлет SET-AzVMBootDiagnostics изменен на Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1177">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="7cf4c-1178">Командлет Export-AzLogAnalyticThrottledRequests изменен на Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1178">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="7cf4c-1179">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1179">Az.DeploymentManager</span></span>
* <span data-ttu-id="7cf4c-1180">Первая общедоступная версия командлетов диспетчера развертывания Azure</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1180">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="7cf4c-1181">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1181">Az.Dns</span></span>
* <span data-ttu-id="7cf4c-1182">Автоматическое делегирование DNS-сервера</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1182">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="7cf4c-1183">Командлет для создания зоны DNS принимает имя родительской зоны в качестве дополнительного необязательного параметра.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1183">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="7cf4c-1184">Он добавляет записи NS в родительской зоне для созданной дочерней зоны.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1184">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="7cf4c-1185">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1185">Az.FrontDoor</span></span>
* <span data-ttu-id="7cf4c-1186">Первая общедоступная версия командлетов Azure FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1186">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="7cf4c-1187">Переименованы командлеты WAF для включения Waf.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1187">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="7cf4c-1188">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1188">Az.HDInsight</span></span>
* <span data-ttu-id="7cf4c-1189">Удалены два командлета:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1189">Removed two cmdlets:</span></span>
    - <span data-ttu-id="7cf4c-1190">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1190">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="7cf4c-1191">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1191">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="7cf4c-1192">Добавлен новый командлет Set-AzHDInsightGatewayCredential для замены Grant-AzHDInsightHttpServicesAccess.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1192">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="7cf4c-1193">Обновлен командлет Get-AzHDInsightJobOutput для различения ролей читателя и оператора HDInsight:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1193">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="7cf4c-1194">Пользователям с ролью читателя не нужно указывать параметр DefaultStorageAccountKey явным образом, иначе возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1194">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="7cf4c-1195">На пользователей с ролью оператора HDInsight это не повлияет.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1195">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7cf4c-1196">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1196">Az.Monitor</span></span>
* <span data-ttu-id="7cf4c-1197">Новые командлеты для API SQR (запланированное правило запросов)</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1197">New cmdlets for SQR API (Scheduled Query Rule)</span></span>  
    - <span data-ttu-id="7cf4c-1198">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1198">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="7cf4c-1199">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1199">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="7cf4c-1200">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1200">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="7cf4c-1201">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1201">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="7cf4c-1202">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1202">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="7cf4c-1203">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1203">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="7cf4c-1204">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1204">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="7cf4c-1205">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1205">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="7cf4c-1206">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1206">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="7cf4c-1207">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1207">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="7cf4c-1208">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1208">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="7cf4c-1209">См. подробнее об [API SQR](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules).</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1209">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="7cf4c-1210">Обновлен файл Az.Monitor.md для включения командлетов для правила генерации оповещений на основе метрик GenV2(не классическая версия).</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1210">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7cf4c-1211">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1211">Az.Network</span></span>
* <span data-ttu-id="7cf4c-1212">Добавлена поддержка для ресурса Шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1212">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="7cf4c-1213">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1213">New cmdlets</span></span>
        - <span data-ttu-id="7cf4c-1214">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1214">New-AzNatGateway</span></span>
        - <span data-ttu-id="7cf4c-1215">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1215">Get-AzNatGateway</span></span>
        - <span data-ttu-id="7cf4c-1216">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1216">Set-AzNatGateway</span></span>
        - <span data-ttu-id="7cf4c-1217">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1217">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="7cf4c-1218">Обновлены командлеты</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1218">Updated cmdlets</span></span>
        - <span data-ttu-id="7cf4c-1219">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1219">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="7cf4c-1220">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1220">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="7cf4c-1221">Обновлены следующие команды для функции: Настройка и удаление пользовательских маршрутов через шлюз в Бруклине.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1221">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="7cf4c-1222">Обновлен командлет New-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1222">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="7cf4c-1223">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1223">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="7cf4c-1224">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1224">Az.PolicyInsights</span></span>
* <span data-ttu-id="7cf4c-1225">Добавлена поддержка сведений об оценке политики запросов.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1225">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="7cf4c-1226">Добавлен параметр -Expand в командлет Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1226">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="7cf4c-1227">Добавлена поддержка -Expand PolicyEvaluationDetails.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1227">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7cf4c-1228">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1228">Az.RecoveryServices</span></span>
* <span data-ttu-id="7cf4c-1229">Добавлена поддержка перекрестной подписки на Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1229">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="7cf4c-1230">Добавлена возможность отмечать предстоящие критически важные изменения для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1230">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="7cf4c-1231">Исправлены план восстановления и план действий для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1231">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="7cf4c-1232">Исправлено сетевое сопоставление обновления Azure Site Recovery (Azure — Azure).</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1232">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="7cf4c-1233">Исправлено направление защиты обновления Azure Site Recovery для управляемых дисков (Azure — Azure).</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1233">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="7cf4c-1234">Добавлены другие незначительные исправления.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1234">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="7cf4c-1235">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1235">Az.Relay</span></span>
* <span data-ttu-id="7cf4c-1236">Исправлены опечатки в сообщениях для клиентов.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1236">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="7cf4c-1237">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1237">Az.ServiceBus</span></span>
* <span data-ttu-id="7cf4c-1238">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1238">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7cf4c-1239">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1239">Az.Storage</span></span>
* <span data-ttu-id="7cf4c-1240">Выполнено обновление клиентской библиотеки хранилища до версии 10.0.1 (пространство имен всех объектов из этого пакета SDK изменено с Microsoft.WindowsAzure.Storage. *на Microsoft.Azure.Storage*).</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1240">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage.*' to 'Microsoft.Azure.Storage.*')</span></span>
* <span data-ttu-id="7cf4c-1241">Выполнено обновление до Microsoft.Azure.Management.Storage версии 11.0.0 для включения поддержки нового API версии 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1241">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="7cf4c-1242">Значение свойства Kind по умолчанию в учетной записи хранения изменено со Storage на StorageV2.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1242">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="7cf4c-1243">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1243">New-AzStorageAccount</span></span>
* <span data-ttu-id="7cf4c-1244">Изменено значение Sku.Name в выходных данных командлета учетной записи хранения в соответствии со значением Sku.Name во входных данных путем добавления _ (например, StandardLRS изменено на Standard_LRS).</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1244">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="7cf4c-1245">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1245">New-AzStorageAccount</span></span>
    - <span data-ttu-id="7cf4c-1246">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1246">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="7cf4c-1247">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1247">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7cf4c-1248">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1248">Az.Websites</span></span>
* <span data-ttu-id="7cf4c-1249">Свойство Kind теперь будет задаваться объектам PSSite, возвращаемым командлетом Get-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1249">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="7cf4c-1250">Get-AzWebApp\*Metrics и Get-AzAppServicePlanMetrics считаются нерекомендуемыми.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1250">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="7cf4c-1251">1.8.0 — апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1251">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="7cf4c-1252">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1252">Highlights since the last major release</span></span>
* <span data-ttu-id="7cf4c-1253">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1253">General availability of `Az` module</span></span>
* <span data-ttu-id="7cf4c-1254">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1254">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="7cf4c-1255">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1255">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="7cf4c-1256">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1256">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="7cf4c-1257">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1257">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="7cf4c-1258">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1258">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="7cf4c-1259">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1259">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7cf4c-1260">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1260">Az.Accounts</span></span>
* <span data-ttu-id="7cf4c-1261">Обновлен командлет Uninstall-AzureRm для правильного удаления модулей в Mac.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1261">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="7cf4c-1262">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1262">Az.Batch</span></span>
* <span data-ttu-id="7cf4c-1263">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1263">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="7cf4c-1264">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1264">Az.Cdn</span></span>
* <span data-ttu-id="7cf4c-1265">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1265">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="7cf4c-1266">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1266">Az.CognitiveServices</span></span>
* <span data-ttu-id="7cf4c-1267">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1267">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7cf4c-1268">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1268">Az.Compute</span></span>
* <span data-ttu-id="7cf4c-1269">Устранена проблема с установкой AEM, если в идентификаторах ресурсов дисков группа ресурсов указана в нижнем регистре.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1269">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="7cf4c-1270">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1270">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7cf4c-1271">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1271">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7cf4c-1272">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1272">Az.DataFactory</span></span>
* <span data-ttu-id="7cf4c-1273">Добавлены свойства SsisProperties, если NodeCount не имеет значения NULL для управляемой среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1273">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7cf4c-1274">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1274">Az.DataLakeStore</span></span>
* <span data-ttu-id="7cf4c-1275">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1275">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="7cf4c-1276">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1276">Az.EventGrid</span></span>
* <span data-ttu-id="7cf4c-1277">Обновлен текст справки для конечной точки, указывающий, что необходимо создать ресурсы, прежде чем использовать командлеты для создания или обновления подписки на события.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1277">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7cf4c-1278">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1278">Az.EventHub</span></span>
* <span data-ttu-id="7cf4c-1279">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1279">Added new cmdlets for NetworkRuleSet of Namespace</span></span> 

#### <a name="azhdinsight"></a><span data-ttu-id="7cf4c-1280">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1280">Az.HDInsight</span></span>
* <span data-ttu-id="7cf4c-1281">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1281">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7cf4c-1282">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1282">Az.IotHub</span></span>
* <span data-ttu-id="7cf4c-1283">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1283">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7cf4c-1284">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1284">Az.KeyVault</span></span>
* <span data-ttu-id="7cf4c-1285">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1285">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7cf4c-1286">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1286">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="7cf4c-1287">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1287">Az.MachineLearning</span></span>
* <span data-ttu-id="7cf4c-1288">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1288">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="7cf4c-1289">Az.Media</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1289">Az.Media</span></span>
* <span data-ttu-id="7cf4c-1290">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1290">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7cf4c-1291">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1291">Az.Monitor</span></span>
  * <span data-ttu-id="7cf4c-1292">Добавлены новые командлеты для правила генерации оповещений на основе метрик GenV2 (не классических).</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1292">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="7cf4c-1293">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1293">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="7cf4c-1294">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1294">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="7cf4c-1295">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1295">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="7cf4c-1296">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1296">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="7cf4c-1297">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1297">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="7cf4c-1298">Обновлен пакет SDK Monitor до предварительной версии 0.22.0.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1298">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7cf4c-1299">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1299">Az.Network</span></span>
* <span data-ttu-id="7cf4c-1300">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1300">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7cf4c-1301">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1301">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="7cf4c-1302">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1302">Az.NotificationHubs</span></span>
* <span data-ttu-id="7cf4c-1303">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1303">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7cf4c-1304">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1304">Az.OperationalInsights</span></span>
* <span data-ttu-id="7cf4c-1305">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1305">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="7cf4c-1306">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1306">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="7cf4c-1307">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1307">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7cf4c-1308">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1308">Az.RecoveryServices</span></span>
* <span data-ttu-id="7cf4c-1309">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1309">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7cf4c-1310">Обновлен табличный формат для SQL на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1310">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="7cf4c-1311">Добавлен альтернативный метод для получения расположения в Общей папке Azure.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1311">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="7cf4c-1312">Обновлено значение ScheduleRunDays в объекте SchedulePolicy в соответствии с часовым поясом.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1312">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="7cf4c-1313">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1313">Az.RedisCache</span></span>
* <span data-ttu-id="7cf4c-1314">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1314">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7cf4c-1315">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1315">Az.Resources</span></span>
* <span data-ttu-id="7cf4c-1316">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1316">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="7cf4c-1317">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1317">Az.Sql</span></span>
* <span data-ttu-id="7cf4c-1318">Заменена зависимость от пакета SDK монитора на обычный код.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1318">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="7cf4c-1319">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1319">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7cf4c-1320">Улучшен процесс классификации нескольких столбцов.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1320">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="7cf4c-1321">Добавлены свойства SKU (имя, семейство, производительность SKU) в отклике Get-AzSqlServerServiceObjective, а также по умолчанию задан табличный формат.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1321">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="7cf4c-1322">C помощью Get-AzSqlServerServiceObjective теперь можно получать список доступных целевых служб по расположению без необходимости заранее размещать сервер в регионе.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1322">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="7cf4c-1323">Поддерживается параметр часового пояса при создании Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1323">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="7cf4c-1324">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1324">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7cf4c-1325">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1325">Az.Websites</span></span>
* <span data-ttu-id="7cf4c-1326">Исправлены командлеты Set-AzWebApp и Set-AzWebAppSlot, которые теперь не удаляют теги при выполнении.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1326">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="7cf4c-1327">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1327">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="7cf4c-1328">Обновлен пакет SDK веб-узлов.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1328">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="7cf4c-1329">Удалено свойство AdminSiteName из PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1329">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="7cf4c-1330">1.7.0 —апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1330">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="7cf4c-1331">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1331">Highlights since the last major release</span></span>
* <span data-ttu-id="7cf4c-1332">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1332">General availability of `Az` module</span></span>
* <span data-ttu-id="7cf4c-1333">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1333">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="7cf4c-1334">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1334">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="7cf4c-1335">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1335">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="7cf4c-1336">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1336">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="7cf4c-1337">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1337">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="7cf4c-1338">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1338">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="7cf4c-1339">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1339">Az.Accounts</span></span>
* <span data-ttu-id="7cf4c-1340">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment. Теперь они принимают параметр AzureAnalysisServicesEndpointResourceId.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1340">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="7cf4c-1341">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1341">Az.AnalysisServices</span></span>
* <span data-ttu-id="7cf4c-1342">Использование ServiceClient в командлетах плоскости данных и удаление исходной логики проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1342">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="7cf4c-1343">Add-AzureASAccount используется как оболочка для Connect-AzAccount во избежание критических изменений.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1343">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7cf4c-1344">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1344">Az.Automation</span></span>
* <span data-ttu-id="7cf4c-1345">Исправлена ошибка командлета New-AzAutomationSoftwareUpdateConfiguration, связанная с включением.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1345">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="7cf4c-1346">Теперь параметры IncludedKbNumber и IncludedPackageNameMask должны работать нормально.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1346">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="7cf4c-1347">Исправлена ошибка динамической группы управления обновлениями службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1347">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7cf4c-1348">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1348">Az.Compute</span></span>
* <span data-ttu-id="7cf4c-1349">В командлеты New-AzDiskConfig и New-AzSnapshotConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1349">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="7cf4c-1350">Теперь можно создавать виртуальные машину на основе образов из коллекции от других клиентов.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1350">Allow VM creation with galley image from other tenants.</span></span> 

#### <a name="azcontainerinstance"></a><span data-ttu-id="7cf4c-1351">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1351">Az.ContainerInstance</span></span>
* <span data-ttu-id="7cf4c-1352">Исправлена проблема в параметре -Command командлета New-AzContainerGroup, из-за которой в конце добавлялся пустой аргумент.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1352">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7cf4c-1353">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1353">Az.DataFactory</span></span>
* <span data-ttu-id="7cf4c-1354">Пакет SDK для ADF .NET обновлен до версии 3.0.2.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1354">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="7cf4c-1355">Командлет Set-AzDataFactoryV2 обновлен с помощью дополнительных параметров для настроек, связанных с RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1355">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7cf4c-1356">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1356">Az.Resources</span></span>
* <span data-ttu-id="7cf4c-1357">Улучшена обработка поставщиков Get-AzResource при предоставлении параметров -ResourceId или -ResourceGroupName, -Name и -ResourceType.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1357">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="7cf4c-1358">Улучшена обработка ошибок в командлетах Test-AzDeployment и Test-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1358">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="7cf4c-1359">Теперь ошибки, возникающие за пределами проверки развертывания, обрабатываются и включаются в выходные данные команды.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1359">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="7cf4c-1360">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1360">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="7cf4c-1361">Добавлен параметр-переключатель -IgnoreDynamicParameters, с помощью которого можно настроить командлеты развертывания так, чтобы они пропускали запросы в сценариях скриптов и заданий.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1361">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="7cf4c-1362">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1362">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="7cf4c-1363">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1363">Az.Sql</span></span>
* <span data-ttu-id="7cf4c-1364">Поддержка классификации данных в базе данных.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1364">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7cf4c-1365">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1365">Az.Storage</span></span>
* <span data-ttu-id="7cf4c-1366">Подробные сообщения об ошибке передаются при создании контекста хранилища с помощью параметра -UseConnectedAccount, но без входа в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1366">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="7cf4c-1367">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1367">New-AzStorageContext</span></span>
* <span data-ttu-id="7cf4c-1368">Поддержка свойств службы управления BLOB-объектов в указанной учетной записи хранения с помощью API плоскости управления.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1368">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="7cf4c-1369">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1369">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="7cf4c-1370">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1370">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="7cf4c-1371">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1371">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="7cf4c-1372">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1372">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="7cf4c-1373">Поддержка параметра -AsJob в командлетах для отправки и скачивания больших двоичных объектов и файлов.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1373">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="7cf4c-1374">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1374">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="7cf4c-1375">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1375">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="7cf4c-1376">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1376">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="7cf4c-1377">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1377">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="7cf4c-1378">1.6.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1378">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="7cf4c-1379">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1379">Highlights since the last major release</span></span>
* <span data-ttu-id="7cf4c-1380">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1380">General availability of `Az` module</span></span>
* <span data-ttu-id="7cf4c-1381">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1381">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="7cf4c-1382">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1382">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="7cf4c-1383">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1383">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="7cf4c-1384">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1384">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="7cf4c-1385">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1385">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="7cf4c-1386">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1386">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7cf4c-1387">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1387">Az.Automation</span></span>
* <span data-ttu-id="7cf4c-1388">В управление обновлениями службы автоматизации Azure внесены изменения для поддержки следующих новых функций:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1388">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="7cf4c-1389">динамическое группирование;</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1389">Dynamic grouping</span></span>
    * <span data-ttu-id="7cf4c-1390">скрипты предварительного или последующего выполнения;</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1390">Pre-Post script</span></span>
    * <span data-ttu-id="7cf4c-1391">параметр перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1391">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7cf4c-1392">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1392">Az.Compute</span></span>
* <span data-ttu-id="7cf4c-1393">Устранена проблема, связанная с разрешением пути в Get-AzVmBootDiagnosticsData.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1393">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="7cf4c-1394">Обновление клиентской библиотеки вычислений до версии 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1394">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7cf4c-1395">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1395">Az.KeyVault</span></span>
* <span data-ttu-id="7cf4c-1396">Добавлена поддержка подстановочных знаков в командлетах KeyVault.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1396">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7cf4c-1397">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1397">Az.Network</span></span>
* <span data-ttu-id="7cf4c-1398">Добавлена поддержка анализа угроз для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1398">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="7cf4c-1399">Добавлены настраиваемые правила и ресурс верхнего уровня для политики брандмауэра Шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1399">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7cf4c-1400">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1400">Az.RecoveryServices</span></span>
* <span data-ttu-id="7cf4c-1401">В политику виртуальной машины Azure добавлен объект SnapshotRetentionInDays для поддержки мгновенного восстановления.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1401">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="7cf4c-1402">Добавлена поддержка канала для отмены регистрации контейнера.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1402">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="7cf4c-1403">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1403">Az.Resources</span></span>
* <span data-ttu-id="7cf4c-1404">Обновлена поддержка подстановочных знаков для Get-AzResource и Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1404">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="7cf4c-1405">Обновлены учетные данные, используемые при общих вызовах к ARM.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1405">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="7cf4c-1406">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1406">Az.Sql</span></span>
* <span data-ttu-id="7cf4c-1407">Изменен тип параметра (ExcludeDetectionType) командлетов для обнаружения угроз с DetectionTypes на string[] для поддержки актуального состояния при добавлении новых типов обнаружения и для поддержки автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1407">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7cf4c-1408">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1408">Az.Storage</span></span>
* <span data-ttu-id="7cf4c-1409">Поддержка получения, настройки и удаления политики управления в учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1409">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="7cf4c-1410">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1410">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="7cf4c-1411">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1411">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="7cf4c-1412">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1412">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="7cf4c-1413">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1413">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="7cf4c-1414">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1414">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="7cf4c-1415">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1415">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7cf4c-1416">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1416">Az.Websites</span></span>
* <span data-ttu-id="7cf4c-1417">Исправлена ошибка с шаблоном ARM, из-за которой прерывалось клонирование все слотов при использовании New-AzWebApp -IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1417">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span> 

## <a name="150---march-2019"></a><span data-ttu-id="7cf4c-1418">1.5.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1418">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7cf4c-1419">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1419">Az.Accounts</span></span>
* <span data-ttu-id="7cf4c-1420">Добавлена команда Register-AzModule для поддержки созданных командлетов AutoRest.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1420">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="7cf4c-1421">Обновлены примеры для Connect AzAccount.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1421">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7cf4c-1422">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1422">Az.Automation</span></span>
* <span data-ttu-id="7cf4c-1423">Исправлена проблема с получением некоторых ежемесячных расписаний в нескольких командлетах службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1423">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="7cf4c-1424">Исправлен командлет Get-AzAutomationDscNode, возвращающий только первые 20 узлов.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1424">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="7cf4c-1425">Теперь он возвращает все узлы.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1425">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="7cf4c-1426">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1426">Az.Cdn</span></span>
* <span data-ttu-id="7cf4c-1427">Добавлены новые командлеты PowerShell для включения и отключения HTTPS для личного домена и отключены устаревшие командлеты.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1427">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7cf4c-1428">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1428">Az.Compute</span></span>
* <span data-ttu-id="7cf4c-1429">Добавлена поддержка подстановочных знаков в командлетах Get.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1429">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7cf4c-1430">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1430">Az.DataFactory</span></span>
* <span data-ttu-id="7cf4c-1431">Обновлен пакет SDK для ADF .NET до версии 3.0.1.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1431">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="7cf4c-1432">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1432">Az.LogicApp</span></span>
* <span data-ttu-id="7cf4c-1433">Исправлена проблема с получением только первой страницы результатов при выполнении команды ListWorkflows.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1433">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7cf4c-1434">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1434">Az.Network</span></span>
* <span data-ttu-id="7cf4c-1435">Добавлена поддержка подстановочных знаков в командлетах Network.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1435">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7cf4c-1436">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1436">Az.RecoveryServices</span></span>
* <span data-ttu-id="7cf4c-1437">Добавлена поддержка SQL Server на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1437">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="7cf4c-1438">Обновление пакета SDK</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1438">SDK Update</span></span>
* <span data-ttu-id="7cf4c-1439">Удалена проверка VMappContainer в Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1439">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="7cf4c-1440">Добавлены параметры Name и ServerName для Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1440">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="7cf4c-1441">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1441">Az.Resources</span></span>
* <span data-ttu-id="7cf4c-1442">Добавлен параметр `-TemplateObject` в командлеты для развертывания.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1442">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="7cf4c-1443">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2933.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1443">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="7cf4c-1444">Устранена проблема с передачей в конвейер результата `Get-AzResource` для `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1444">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="7cf4c-1445">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8240.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1445">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="7cf4c-1446">Устранена проблема с изменением типа данных JSON при выполнении `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1446">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="7cf4c-1447">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7930.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1447">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="7cf4c-1448">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1448">Az.Sql</span></span>
* <span data-ttu-id="7cf4c-1449">Обновление AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1449">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="7cf4c-1450">Исправлено поведение для пограничного случая при создании параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1450">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7cf4c-1451">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1451">Az.Storage</span></span>
* <span data-ttu-id="7cf4c-1452">Включена поддержка Kind BlockBlobStorage при создании учетной записи хранения для New-AzStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1452">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="7cf4c-1453">1.4.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1453">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="7cf4c-1454">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1454">Az.AnalysisServices</span></span>
* <span data-ttu-id="7cf4c-1455">Командлет AddAzureASAccount устарел.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1455">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7cf4c-1456">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1456">Az.Automation</span></span>
* <span data-ttu-id="7cf4c-1457">Обновлена справка для командлета Import-AzAutomationDscNodeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1457">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="7cf4c-1458">Добавлена проверка имени конфигурации для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1458">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="7cf4c-1459">Улучшена обработка ошибок для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1459">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="7cf4c-1460">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1460">Az.CognitiveServices</span></span>
* <span data-ttu-id="7cf4c-1461">Добавлен параметр CustomSubdomainName — новый необязательный параметр для командлета New-AzCognitiveServicesAccount, который указывает поддомен для ресурса.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1461">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7cf4c-1462">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1462">Az.Compute</span></span>
* <span data-ttu-id="7cf4c-1463">Устранена проблема с идентификаторами наборов параметров.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1463">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="7cf4c-1464">Обновлен командлет Get-AzVMExtension для отображения списка всех установленных расширений, если не указан параметр Name.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1464">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="7cf4c-1465">Для командлета Update-AzImage добавлены параметры Tag и ResourceId.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1465">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="7cf4c-1466">Командлет Get-AzVmssVM, который выполняется без указания идентификатора экземпляра и с параметром InstanceView, может выводить виртуальные машины из VMSS с представлением экземпляра.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1466">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7cf4c-1467">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1467">Az.DataLakeStore</span></span>
* <span data-ttu-id="7cf4c-1468">Добавлены командлеты для перечисления и восстановления удаленного элемента ADL.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1468">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="7cf4c-1469">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1469">Az.EventHub</span></span>
* <span data-ttu-id="7cf4c-1470">Добавлено новое логическое свойство SkipEmptyArchives для пропуска пустых архивов в классе CaptureDescription Eventhub.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1470">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span> 

#### <a name="azkeyvault"></a><span data-ttu-id="7cf4c-1471">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1471">Az.KeyVault</span></span>
* <span data-ttu-id="7cf4c-1472">Исправлена расстановка тегов для командлета Set-AzKeyVaultSecret.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1472">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="7cf4c-1473">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1473">Az.LogicApp</span></span>
* <span data-ttu-id="7cf4c-1474">Добавлен SKU "Базовый" для учетных записей интеграции.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1474">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="7cf4c-1475">Добавлены типы сопоставлений Liquid, а также XSLT 2.0 и XSLT 3.0.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1475">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="7cf4c-1476">Новые командлеты для сборок учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1476">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="7cf4c-1477">Get-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1477">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="7cf4c-1478">New-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1478">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="7cf4c-1479">Remove-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1479">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="7cf4c-1480">Set-AzIntegrationAccountAssembly.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1480">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="7cf4c-1481">Новые командлеты для конфигурации пакета учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1481">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="7cf4c-1482">Get-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1482">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="7cf4c-1483">New-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1483">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="7cf4c-1484">Remove-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1484">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="7cf4c-1485">Set-AzIntegrationAccountBatchConfiguration.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1485">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="7cf4c-1486">Обновлен пакет SDK Logic Apps до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1486">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="7cf4c-1487">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1487">Az.Monitor</span></span>
* <span data-ttu-id="7cf4c-1488">Обновлена справка для командлета Get-AzMetric.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1488">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7cf4c-1489">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1489">Az.Network</span></span>
* <span data-ttu-id="7cf4c-1490">Обновлен пример справки для командлета Add-AzApplicationGatewayCustomError.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1490">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="7cf4c-1491">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1491">Az.OperationalInsights</span></span>
* <span data-ttu-id="7cf4c-1492">Дополнительная поддержка создания и получения источников данных ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1492">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="7cf4c-1493">Добавлен новый тип ApplicationInsights для получения определенных или всех источников данных ApplicationInsights для указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1493">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span> 
    - <span data-ttu-id="7cf4c-1494">Добавлен командлет New-AzOperationalInsightsApplicationInsightsDataSource для создания источника данных с использованием параметров указанного ресурса Application-Insightss: subscription Id, resourceGroupName и name.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1494">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span> 

#### <a name="azresources"></a><span data-ttu-id="7cf4c-1495">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1495">Az.Resources</span></span>
* <span data-ttu-id="7cf4c-1496">исправлена проблема https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1496">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="7cf4c-1497">исправлена проблема https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1497">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="7cf4c-1498">исправлена проблема https://github.com/Azure/azure-powershell/issues/6219.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1498">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="7cf4c-1499">Исправлена ошибка, препятствующая повторному созданию KeyCredentials.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1499">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="7cf4c-1500">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1500">Az.Sql</span></span>
* <span data-ttu-id="7cf4c-1501">Добавлена поддержка уровня гипермасштабирования в базе данных SQL.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1501">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="7cf4c-1502">Исправлена ошибка, из-за которой восстановление могло завершиться со сбоем при указании ненужных свойств в запросе на восстановление.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1502">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7cf4c-1503">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1503">Az.Websites</span></span>
* <span data-ttu-id="7cf4c-1504">Исправлен пример для командлета Get-AzWebAppSlotMetrics.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1504">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="7cf4c-1505">1.3.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1505">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7cf4c-1506">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1506">Az.Accounts</span></span>
* <span data-ttu-id="7cf4c-1507">Обновление до последней версии ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1507">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="7cf4c-1508">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1508">Az.AnalysisServices</span></span>
<span data-ttu-id="7cf4c-1509">Общедоступная версия модуля Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1509">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7cf4c-1510">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1510">Az.Compute</span></span>
* <span data-ttu-id="7cf4c-1511">Расширение AEM: добавлена поддержка дисков UltraSSD, P60, P70 и P80.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1511">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="7cf4c-1512">Обновлено описание справки для командлета Set-AzVMBootDiagnostics.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1512">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="7cf4c-1513">Обновлено описание справки и пример для командлета Update-AzImage.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1513">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7cf4c-1514">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1514">Az.RecoveryServices</span></span>
<span data-ttu-id="7cf4c-1515">Общедоступная версия модуля Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1515">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7cf4c-1516">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1516">Az.Resources</span></span>
* <span data-ttu-id="7cf4c-1517">Исправлена расстановка тегов для групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1517">Fix tagging for resource groups</span></span> 
    - <span data-ttu-id="7cf4c-1518">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1518">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="7cf4c-1519">Исправлена проблема с игнорированием командлетом `Get-AzureRmRoleAssignment` параметра -ErrorAction.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1519">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span> 
    - <span data-ttu-id="7cf4c-1520">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1520">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="7cf4c-1521">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1521">Az.Sql</span></span>
* <span data-ttu-id="7cf4c-1522">Добавлен командлет Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1522">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="7cf4c-1523">Исправлена проблема с появлением исключения NullRef при выполнении командлетов SQL, если не выполнен вход в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1523">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="7cf4c-1524">Исправлено исключение NullRef в командлете Get-AzSqlCapability.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1524">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="7cf4c-1525">1.2.1 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1525">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7cf4c-1526">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1526">Az.Accounts</span></span>
* <span data-ttu-id="7cf4c-1527">Выпуск с правильной версией службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1527">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="7cf4c-1528">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1528">Az.AnalysisServices</span></span>
* <span data-ttu-id="7cf4c-1529">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1529">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="7cf4c-1530">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1530">Az.RecoveryServices</span></span>
* <span data-ttu-id="7cf4c-1531">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1531">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="7cf4c-1532">1.2.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1532">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7cf4c-1533">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1533">Az.Accounts</span></span>
* <span data-ttu-id="7cf4c-1534">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1534">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="7cf4c-1535">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1535">Update incorrect online help URLs</span></span>
* <span data-ttu-id="7cf4c-1536">Добавлено предупреждающее сообщение в PS Core для модуля Uninstall-AzureRm.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1536">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="7cf4c-1537">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1537">Az.Aks</span></span>
* <span data-ttu-id="7cf4c-1538">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1538">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="7cf4c-1539">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1539">Az.Automation</span></span>
* <span data-ttu-id="7cf4c-1540">Добавлена поддержка для модулей runbook Python 2.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1540">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="7cf4c-1541">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1541">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="7cf4c-1542">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1542">Az.Cdn</span></span>
* <span data-ttu-id="7cf4c-1543">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1543">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7cf4c-1544">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1544">Az.Compute</span></span>
* <span data-ttu-id="7cf4c-1545">Добавлен командлет Invoke-AzVMReimage.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1545">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="7cf4c-1546">Добавлен параметр TempDisk к командлету Set-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1546">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="7cf4c-1547">Исправлено предупреждающее сообщение командлета New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1547">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="7cf4c-1548">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1548">Az.ContainerRegistry</span></span>
* <span data-ttu-id="7cf4c-1549">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1549">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="7cf4c-1550">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1550">Az.DataFactory</span></span>
* <span data-ttu-id="7cf4c-1551">Пакет SDK ADF .Net обновлен до версии 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1551">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7cf4c-1552">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1552">Az.DataLakeStore</span></span>
* <span data-ttu-id="7cf4c-1553">Исправлена проблема с конечной точкой ADLS при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1553">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="7cf4c-1554">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7462.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1554">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="7cf4c-1555">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1555">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7cf4c-1556">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1556">Az.IotHub</span></span>
* <span data-ttu-id="7cf4c-1557">Добавлен формат кодирования для командлета Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1557">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="7cf4c-1558">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1558">Az.KeyVault</span></span>
* <span data-ttu-id="7cf4c-1559">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1559">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7cf4c-1560">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1560">Az.Network</span></span>
* <span data-ttu-id="7cf4c-1561">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1561">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="7cf4c-1562">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1562">Az.Resources</span></span>
* <span data-ttu-id="7cf4c-1563">Исправлены неправильные примеры в справочной документации по командлетам New-AzADAppCredential и New-AzADSpCredential.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1563">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="7cf4c-1564">Исправлена проблема, при которой путь для параметра -TemplateFile не удавалось разрешить до выполнения командлетов развертывания групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1564">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="7cf4c-1565">Az.Resources: исправлена документация для значения по умолчанию -Mode командлета New-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1565">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="7cf4c-1566">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/7522.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1566">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="7cf4c-1567">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/5747.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1567">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="7cf4c-1568">Исправлена проблема с форматированием объекта PSResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1568">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="7cf4c-1569">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2123.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1569">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7cf4c-1570">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1570">Az.ServiceFabric</span></span>
* <span data-ttu-id="7cf4c-1571">Исправлена проблема с появлением исключения в процессе отката при добавлении сертификата к модели VMSS: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1571">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="7cf4c-1572">Исправлены некоторые сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1572">Fix some error messages.</span></span>
* <span data-ttu-id="7cf4c-1573">Исправлена проблема с созданием кластера с шаблоном ARM по умолчанию для командлета New-AzServiceFabriCluster, который не работал с операцией миграции в Az.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1573">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="7cf4c-1574">Исправлена проблема с добавлением сертификата кластера или приложения: теперь они добавляются только в Масштабируемые наборы виртуальных машин, которые сопоставлены с кластером, путем проверки идентификатора кластера в расширении.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1574">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="7cf4c-1575">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1575">Az.SignalR</span></span>
* <span data-ttu-id="7cf4c-1576">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1576">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="7cf4c-1577">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1577">Az.Sql</span></span>
* <span data-ttu-id="7cf4c-1578">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1578">Update incorrect online help URLs</span></span>
* <span data-ttu-id="7cf4c-1579">Обновлено описание параметра LicenseType с добавлением возможных значений.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1579">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="7cf4c-1580">Исправлена проблема с неправильным обновлением удостоверения управляемого экземпляра, если оно было единственным обновляемым свойством.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1580">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="7cf4c-1581">Поддержка пользовательских параметров сортировки в управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1581">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7cf4c-1582">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1582">Az.Storage</span></span>
* <span data-ttu-id="7cf4c-1583">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1583">Update incorrect online help URLs</span></span>
* <span data-ttu-id="7cf4c-1584">Добавлен вывод подробных сообщений об ошибке при получении или установке классических свойств ведения журнала или метрик в учетной записи хранилища класса Premium, так как учетная запись хранилища класса Premium не поддерживает классические функции ведения журнала и метрик.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1584">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="7cf4c-1585">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1585">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="7cf4c-1586">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1586">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="7cf4c-1587">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1587">Az.TrafficManager</span></span>
* <span data-ttu-id="7cf4c-1588">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1588">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7cf4c-1589">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1589">Az.Websites</span></span>
* <span data-ttu-id="7cf4c-1590">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1590">Update incorrect online help URLs</span></span>
* <span data-ttu-id="7cf4c-1591">Исправлена работа командлета New-AzWebAppSSLBinding: сертификат отправляется в правильную группу ресурсов и правильное расположение, если приложение размещено в ASE.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1591">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="7cf4c-1592">Исправлена работа командлета New-AzWebAppSSLBinding: теги не перезаписываются при привязке SSL-сертификата к приложению.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1592">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="7cf4c-1593">1.1.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1593">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="7cf4c-1594">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1594">Az.Accounts</span></span>
* <span data-ttu-id="7cf4c-1595">Добавление области "Local" в Enable-AzureRmAlias.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1595">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7cf4c-1596">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1596">Az.Compute</span></span>
* <span data-ttu-id="7cf4c-1597">Теперь имя не является обязательным в идентификаторе набора параметров для Restart/Start/Stop/Remove/Set-AzVM и Save-AzVMImage.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1597">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="7cf4c-1598">Обновлено описание идентификатора в файлах справки.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1598">Updated the description of ID in help files</span></span>
* <span data-ttu-id="7cf4c-1599">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1599">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7cf4c-1600">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1600">Az.DataLakeStore</span></span>
* <span data-ttu-id="7cf4c-1601">Обновление версии пакета SDK для плоскости данных до 1.1.14 для устранения найденных проблем.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1601">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="7cf4c-1602">Исправлена обработка отрицательного времени доступа и времени изменения для getfilestatus и liststatus, исправлен токен отмены для асинхронных методов.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1602">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="7cf4c-1603">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1603">Az.EventGrid</span></span>
* <span data-ttu-id="7cf4c-1604">Обновление для использования API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1604">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="7cf4c-1605">Обновлены указанные ниже командлеты для поддержки нового сценария в API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1605">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="7cf4c-1606">New-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1606">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="7cf4c-1607">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1607">Event Time-To-Live,</span></span>
        - <span data-ttu-id="7cf4c-1608">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1608">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="7cf4c-1609">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1609">Dead letter endpoint.</span></span>
    - <span data-ttu-id="7cf4c-1610">Update-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1610">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="7cf4c-1611">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1611">Event Time-To-Live,</span></span>
        - <span data-ttu-id="7cf4c-1612">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1612">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="7cf4c-1613">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1613">Dead letter endpoint.</span></span>
* <span data-ttu-id="7cf4c-1614">Для параметра EndpointType добавлены новые значения перечисления (storageQueue и hybridConnection) в командлеты New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1614">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="7cf4c-1615">Если ожидается, что создание или обновление подписки на событие повлечет за собой действия со стороны пользователя, выполняемые вручную, отображается предупреждение при создании или обновлении подписки события.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1615">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="7cf4c-1616">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1616">Az.IotHub</span></span>
* <span data-ttu-id="7cf4c-1617">Пакет SDK Центра Интернета вещей обновлен до последней версии.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1617">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="7cf4c-1618">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1618">Az.LogicApp</span></span>
* <span data-ttu-id="7cf4c-1619">Get-AzLogicApp позволяет перечислить все параметры без указанного имени.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1619">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="7cf4c-1620">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1620">Az.Resources</span></span>
* <span data-ttu-id="7cf4c-1621">Исправлена проблема с набором параметров при предоставлении параметров "-ODataQuery" и "-ResourceId" для "Get-AzResource".</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1621">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="7cf4c-1622">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7875.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1622">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="7cf4c-1623">Исправлена обработка параметра -Custom в New/Set-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1623">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="7cf4c-1624">Исправлена опечатка в документации по New-AzDeployment.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1624">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="7cf4c-1625">Параметр "-MailNickname" стал обязательным для "New-AzADUser".</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1625">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="7cf4c-1626">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8220.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1626">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="7cf4c-1627">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1627">Az.SignalR</span></span>
* <span data-ttu-id="7cf4c-1628">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1628">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="7cf4c-1629">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1629">Az.Sql</span></span>
* <span data-ttu-id="7cf4c-1630">Зависимость клиента управления хранением преобразована для общей реализации в пакете SDK.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1630">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="7cf4c-1631">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1631">Az.Storage</span></span>
* <span data-ttu-id="7cf4c-1632">Установка параметра StorageAccountName для контекста хранилища в качестве реального имени учетной записи хранения, если она была создана с использованием токена Sas, OAuth или анонимного доступа.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1632">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="7cf4c-1633">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1633">New-AzStorageContext</span></span>
* <span data-ttu-id="7cf4c-1634">Создание токена Sas большого двоичного объекта моментального снимка с параметром "-FullUri". Возвращаемый URI исправлен на URI моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1634">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="7cf4c-1635">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1635">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7cf4c-1636">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1636">Az.Websites</span></span>
* <span data-ttu-id="7cf4c-1637">Исправлена ошибка синтаксического анализа даты в "Get-AzDeletedWebApp".</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1637">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="7cf4c-1638">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1638">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="7cf4c-1639">1.0.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1639">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="7cf4c-1640">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1640">General</span></span>

- <span data-ttu-id="7cf4c-1641">Общедоступная версия модуля Az.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1641">General Availability of Az Module</span></span>
- <span data-ttu-id="7cf4c-1642">Справка в Интернете для каждого модуля.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1642">Online help for each module</span></span>
- <span data-ttu-id="7cf4c-1643">Дополнительные сведения и стратегию развития см. в статье [Announcing New Module 'Az'](https://aka.ms/azps-announce) (Объявление о новом модуле Az)</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1643">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="7cf4c-1644">Сведения о миграции с AzureRM см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1644">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="7cf4c-1645">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1645">Az.Accounts</span></span>
- <span data-ttu-id="7cf4c-1646">Изменено с Az.Profile.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1646">Changed from Az.Profile</span></span>
- <span data-ttu-id="7cf4c-1647">Исправлены форматы таблиц для типов профиля и контекста.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1647">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="7cf4c-1648">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1648">Az.ApiManagement</span></span>
- <span data-ttu-id="7cf4c-1649">Исправления для #7002.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1649">Fixes for #7002</span></span>
- <span data-ttu-id="7cf4c-1650">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1650">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="7cf4c-1651">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1651">Az.Batch</span></span>
- <span data-ttu-id="7cf4c-1652">Добавлена возможность видеть, какая версия агента узла пакетной службы Azure работает в пуле на каждой виртуальной машине, с помощью нового свойства `NodeAgentInformation` в `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1652">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="7cf4c-1653">Значение `Caching` по умолчанию для `PSDataDisk` теперь `ReadWrite` вместо `None`.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1653">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="7cf4c-1654">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1654">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="7cf4c-1655">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1655">Az.Billing</span></span>
- <span data-ttu-id="7cf4c-1656">Объединены командлеты Billing, Consumption и UsageAggregates. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0).</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1656">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="7cf4c-1657">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1657">Az.CognitivServices</span></span>
- <span data-ttu-id="7cf4c-1658">Добавлены средства заполнения для SkuName и Typem, доступные в операции New-AzureRmCognitiveServicesAccount.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1658">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="7cf4c-1659">Удален набор параметров GetSkusWithAccountParamSetName из Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1659">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="7cf4c-1660">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1660">Az.ContainerInstance</span></span>
- <span data-ttu-id="7cf4c-1661">Добавлена поддержка ManagedIdentity.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1661">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="7cf4c-1662">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1662">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="7cf4c-1663">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1663">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="7cf4c-1664">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1664">Az.DataLakeStore</span></span>
- <span data-ttu-id="7cf4c-1665">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1665">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="7cf4c-1666">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1666">Az.Monitor</span></span>
- <span data-ttu-id="7cf4c-1667">"Az.Insights" переименован в "Az.Monitor" и внесены другие незначительные критические изменения. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1667">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="7cf4c-1668">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1668">Az.KeyVault</span></span>
- <span data-ttu-id="7cf4c-1669">Из типов вывода удалено устаревшее свойство PurgeDisabled</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1669">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="7cf4c-1670">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1670">Az.MachineLearning</span></span>
- <span data-ttu-id="7cf4c-1671">Включены командлеты из модуля Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1671">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="7cf4c-1672">Az.Media</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1672">Az.Media</span></span>
- <span data-ttu-id="7cf4c-1673">Удаляет устаревший псевдоним Tags из New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1673">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="7cf4c-1674">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1674">Az.Network</span></span>
<span data-ttu-id="7cf4c-1675">В шлюз приложений добавлена поддержка настройки RewriteRuleSets</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1675">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="7cf4c-1676">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1676">New cmdlets added:</span></span>
        - <span data-ttu-id="7cf4c-1677">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1677">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="7cf4c-1678">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1678">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="7cf4c-1679">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1679">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="7cf4c-1680">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1680">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="7cf4c-1681">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1681">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="7cf4c-1682">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1682">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="7cf4c-1683">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1683">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="7cf4c-1684">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1684">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="7cf4c-1685">В следующие командлеты добавлен необязательный параметр -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1685">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="7cf4c-1686">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1686">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="7cf4c-1687">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1687">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="7cf4c-1688">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1688">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="7cf4c-1689">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1689">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="7cf4c-1690">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1690">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="7cf4c-1691">New-AzureRmApplicationGatewayUrlPathMapConfig добавил с помощью идентификатора поддержку KeyVault для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1691">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="7cf4c-1692">В следующие командлеты добавлен необязательный параметр -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1692">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="7cf4c-1693">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1693">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="7cf4c-1694">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1694">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="7cf4c-1695">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1695">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="7cf4c-1696">В командлет New-AzApplicationGateway добавлен необязательный параметр -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1696">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="7cf4c-1697">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1697">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="7cf4c-1698">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1698">Az.OperationalInsights</span></span>
- <span data-ttu-id="7cf4c-1699">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1699">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="7cf4c-1700">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1700">Az.Profile</span></span>
- <span data-ttu-id="7cf4c-1701">Имя модуля изменено на Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1701">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="7cf4c-1702">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1702">Az.RecoveryServices</span></span>
- <span data-ttu-id="7cf4c-1703">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1703">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="7cf4c-1704">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1704">Az.Resources</span></span>
- <span data-ttu-id="7cf4c-1705">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1705">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="7cf4c-1706">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1706">Az.ServiceFabric</span></span>
- <span data-ttu-id="7cf4c-1707">Поддержка спецификации сертификата по общему имени и отпечатку</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1707">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="7cf4c-1708">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1708">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="7cf4c-1709">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1709">Az.SIgnalR</span></span>
- <span data-ttu-id="7cf4c-1710">Общедоступная версия командлетов PowerShell для SIgnalR</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1710">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="7cf4c-1711">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1711">Az.Sql</span></span>
- <span data-ttu-id="7cf4c-1712">Добавлены новые типы обнаружения Data_Exfiltration и Unsafe_Action в командлеты обнаружения угроз</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1712">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="7cf4c-1713">Примеры обновленной документации для командлетов аудита Sql</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1713">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="7cf4c-1714">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1714">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="7cf4c-1715">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1715">Az.Storage</span></span>
- <span data-ttu-id="7cf4c-1716">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1716">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="7cf4c-1717">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1717">Az.Websites</span></span>
- <span data-ttu-id="7cf4c-1718">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1718">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="7cf4c-1719">0.7.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1719">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="7cf4c-1720">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1720">General</span></span>

* <span data-ttu-id="7cf4c-1721">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1721">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="7cf4c-1722">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1722">Az.Compute</span></span>

* <span data-ttu-id="7cf4c-1723">Добавлена поддержка UltraSSD и образов коллекции в простых наборах параметров для командлетов `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1723">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="7cf4c-1724">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1724">Az.DataLakeStore</span></span>

* <span data-ttu-id="7cf4c-1725">Исправлено косую черту в конце домена учетной записи ADLS</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1725">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="7cf4c-1726">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1726">Az.FrontDoor</span></span>

* <span data-ttu-id="7cf4c-1727">Исправлены некоторые неработающие ссылки</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1727">Fixed some broken links</span></span>
    - <span data-ttu-id="7cf4c-1728">В статьях New-AzureRmFrontDoor и Set-AzureRmFrontDoor исправлена ссылка на статью командлета New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1728">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="7cf4c-1729">В статье New-AzureRmFrontDoorManagedRuleObject исправлена ссылка на статью командлета New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1729">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="7cf4c-1730">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1730">Az.RecoveryServices</span></span>

* <span data-ttu-id="7cf4c-1731">Добавлены проверки на стороне клиента для операций восстановления общей папки Azure.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1731">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="7cf4c-1732">StorageAccountName и storageAccountResourceGroupName являются необязательными для восстановления afs.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1732">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="7cf4c-1733">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1733">Az.Resources</span></span>

* <span data-ttu-id="7cf4c-1734">Исправление для https://github.com/Azure/azure-powershell/issues/7679.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1734">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="7cf4c-1735">Обновите Get-AzureRmRoleAssignment, чтобы использовать область подписки, если она указана при запросе классических администраторов.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1735">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="7cf4c-1736">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1736">Az.Sql</span></span>

* <span data-ttu-id="7cf4c-1737">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1737">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="7cf4c-1738">Устранена проблема с использованием Get-AzureRmSqlDatabaseVulnerabilityAssessment с .NET Core.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1738">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="7cf4c-1739">Изменена документация справочных сообщений, связанных с командлетами аудита SQL.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1739">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="7cf4c-1740">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1740">Az.Storage</span></span>

* <span data-ttu-id="7cf4c-1741">Добавлено -EnableHierarchicalNamespace к New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1741">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="7cf4c-1742">Устранена проблема, из-за которой командлет Copy File не может повторно использовать исходный контекст в пункте назначения, если не введен -DestContext</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1742">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="7cf4c-1743">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1743">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="7cf4c-1744">Поддержка статической конфигурации сайта</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1744">Support Static Website configuration</span></span>
    - <span data-ttu-id="7cf4c-1745">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1745">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="7cf4c-1746">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1746">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="7cf4c-1747">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1747">Az.Websites</span></span>

* <span data-ttu-id="7cf4c-1748">Set-AzureRmWebApp и Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1748">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span> 
    - <span data-ttu-id="7cf4c-1749">Добавлен новый параметр (-AzureStoragePath), который указывает путь службы хранилища Azure для подключения в приложениях-контейнерах Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1749">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="7cf4c-1750">Используйте выходные данные нового командлета New-AzureRmWebAppAzureStoragePath в качестве параметра, чтобы задать пути к службе хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1750">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="7cf4c-1751">0.6.1 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1751">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="7cf4c-1752">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1752">Az.ApiManagement</span></span>
* <span data-ttu-id="7cf4c-1753">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1753">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="7cf4c-1754">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1754">Az.Automation</span></span>
* <span data-ttu-id="7cf4c-1755">Командлеты службы автоматизации Azure на базе Swagger.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1755">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="7cf4c-1756">Добавлены командлеты для Управления обновлениями.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1756">Added Update Management cmdlets</span></span>
* <span data-ttu-id="7cf4c-1757">Добавлены командлеты для системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1757">Added Source Control cmdlets</span></span>
* <span data-ttu-id="7cf4c-1758">Добавлен командлет Remove-AzureRmAutomationHybridWorkerGroup.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1758">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="7cf4c-1759">Исправлена команда DSC для регистрации узла.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1759">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="7cf4c-1760">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1760">Az.Compute</span></span>
* <span data-ttu-id="7cf4c-1761">Исправлена проблема с удостоверением, назначаемым системой.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1761">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="7cf4c-1762">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1762">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="7cf4c-1763">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1763">Az.ContainerInstance</span></span>
* <span data-ttu-id="7cf4c-1764">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1764">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="7cf4c-1765">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1765">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="7cf4c-1766">Обновлено описание в примерах командлетов для Marketplace.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1766">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="7cf4c-1767">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1767">Az.Network</span></span>
* <span data-ttu-id="7cf4c-1768">Добавлены командлеты New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1768">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="7cf4c-1769">Протокол ICMP возвращен в список поддерживаемых сетевых протоколов Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1769">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="7cf4c-1770">Обновлен командлет Test-AzureRmNetworkWatcherConnectivity, в который добавлена проверка идентификатора, адреса и порта целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1770">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span> 
* <span data-ttu-id="7cf4c-1771">Исправлены проблемы с использованием памяти в карте виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1771">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="7cf4c-1772">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1772">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="7cf4c-1773">Внесено исправление для изменения политики, применяемой к защищенному общему файловому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1773">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="7cf4c-1774">Параметры часового пояса преобразованы в верхний регистр.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1774">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="7cf4c-1775">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1775">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="7cf4c-1776">Исправлен пример командлета New-AzureRmRecoveryServicesAsrProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1776">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="7cf4c-1777">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1777">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="7cf4c-1778">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1778">Az.Relay</span></span>
* <span data-ttu-id="7cf4c-1779">Для командлета New-AzureRmRelayKey добавлен необязательный параметр -KeyValue, который позволяет пользователю указать значение ключа.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1779">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="7cf4c-1780">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1780">Az.Resources</span></span>
* <span data-ttu-id="7cf4c-1781">Обновлена справочная документация для параметров, связанных с удостоверением ресурса, в `New-AzureRmPolicyAssignment` и `Set-AzureRmPolicyAssignment`.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1781">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="7cf4c-1782">Добавлен пример командлета New-AzureRmPolicyDefinition, в котором используется параметр -Metadata.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1782">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="7cf4c-1783">Реализовано исправление, позволяющее сохранять регистр в ключах тегов NetStandard: #7678, #7703.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1783">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="7cf4c-1784">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1784">Az.ServiceFabric</span></span>
* <span data-ttu-id="7cf4c-1785">Добавлены сообщения о нерекомендуемых компонентах для предстоящего выпуска критических изменений.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1785">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="7cf4c-1786">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1786">Az.Sql</span></span>
* <span data-ttu-id="7cf4c-1787">Добавлены новые командлеты для операций создания, просмотра, изменения и удаления в Управляемом экземпляре Базы данных SQL и Управляемой базе данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1787">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="7cf4c-1788">Get-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1788">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="7cf4c-1789">New-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1789">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="7cf4c-1790">Set-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1790">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="7cf4c-1791">Remove-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1791">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="7cf4c-1792">Get-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1792">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="7cf4c-1793">New-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1793">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="7cf4c-1794">Restore-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1794">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="7cf4c-1795">Remove-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1795">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="7cf4c-1796">Добавлено расширенное управление политиками аудита для сервера или базы данных.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1796">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="7cf4c-1797">Добавлен новый параметр (PredicateExpression) для фильтрации журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1797">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="7cf4c-1798">Внесены изменения в командлеты для использования клиентов SQL вместо устаревших клиентов.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1798">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="7cf4c-1799">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1799">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="7cf4c-1800">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1800">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="7cf4c-1801">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1801">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="7cf4c-1802">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1802">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="7cf4c-1803">Исправлена проблема с использованием командлета Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings с набором параметров, содержащим имена учетных записей хранения.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1803">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="7cf4c-1804">0.5.0 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1804">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="7cf4c-1805">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1805">General</span></span>
* <span data-ttu-id="7cf4c-1806">Добавлены средства заполнения ресурсов для многих основных командлетов — они позволяют вам переключать существующие имена ресурсов при вызове командлетов в интерактивном режиме</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1806">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="7cf4c-1807">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1807">Az.Profile</span></span>
* <span data-ttu-id="7cf4c-1808">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1808">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="7cf4c-1809">В командлете Connect-AzAccount параметр TenantId переименован в Tenant и добавлен псевдоним для TenantId</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1809">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="7cf4c-1810">Обновлено описание TenantId для командлета Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1810">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="7cf4c-1811">Исправлено сообщение об ошибке при неудачной попытке входа в процессе предоставления домена клиента.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1811">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="7cf4c-1812">Устранена проблема с конфликтом имен контекста в учетных записях без подписок в клиенте.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1812">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="7cf4c-1813">Устранена проблема с конечными точками DataLake при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1813">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="7cf4c-1814">Устранена проблема, при которой командлет Disconnect-AzAccount вызывал сбой при отсутствии подключения</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1814">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="7cf4c-1815">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1815">Az.CognitiveServices</span></span>
* <span data-ttu-id="7cf4c-1816">Добавлена операция Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1816">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7cf4c-1817">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1817">Az.Compute</span></span>
* <span data-ttu-id="7cf4c-1818">Добавлены командлеты Add-AzVmssVMDataDisk и Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1818">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="7cf4c-1819">Get-AzVMImage отображает AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1819">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="7cf4c-1820">Устранена проблема, при которой значения параметров SetAzVMChefExtension -BootstrapOptions и -JsonAttribute нельзя было указать в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1820">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7cf4c-1821">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1821">Az.DataLakeStore</span></span>
* <span data-ttu-id="7cf4c-1822">Обновлен пакет DataLake до версии 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1822">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="7cf4c-1823">Параметр по умолчанию Concurrency добавлен к многопоточным операциям.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1823">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="7cf4c-1824">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1824">Az.Insights</span></span>
* <span data-ttu-id="7cf4c-1825">Исправлена проблема № 7267 (область автомасштабирования).</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1825">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="7cf4c-1826">Устранена проблема с созданием правила автомасштабирования, при которой перечисленные параметры не были указаны должным образом (выбор значений по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1826">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="7cf4c-1827">Исправлена проблема № 7513 [Insights], при которой для командлета Set-AzDiagnosticSetting требовалось явное указание категорий во время создания параметра</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1827">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="7cf4c-1828">Теперь явное указание категорий во время создания не требуется, и командлет выполняется надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1828">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7cf4c-1829">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1829">Az.Network</span></span>
* <span data-ttu-id="7cf4c-1830">Параметр PeeringType является обязательным для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1830">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="7cf4c-1831">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1831">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="7cf4c-1832">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1832">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="7cf4c-1833">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1833">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="7cf4c-1834">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1834">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="7cf4c-1835">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1835">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="7cf4c-1836">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1836">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="7cf4c-1837">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1837">Az.PolicyInsights</span></span>
* <span data-ttu-id="7cf4c-1838">Добавлена политика исправления командлетов.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1838">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="7cf4c-1839">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1839">Az.Resources</span></span>
* <span data-ttu-id="7cf4c-1840">Исправление для https://github.com/Azure/azure-powershell/issues/7402.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1840">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="7cf4c-1841">Разрешено перечисление ресурсов с помощью параметра -ResourceId для командлета Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1841">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="7cf4c-1842">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1842">Az.ServiceBus</span></span>
* <span data-ttu-id="7cf4c-1843">Добавлено свойство только для чтения MigrationState в PSServiceBusMigrationConfigurationAttributes, которое позволяет узнать состояние Migration.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1843">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="7cf4c-1844">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1844">Az.ServiceFabric</span></span>
* <span data-ttu-id="7cf4c-1845">Устранена проблема с добавлением сертификата в VMSS Linux.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1845">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="7cf4c-1846">Исправлен командлет Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1846">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="7cf4c-1847">Используется правильный отпечаток нового сертификата (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1847">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="7cf4c-1848">Исключение отображается правильно (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1848">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="7cf4c-1849">Исправлен командлет Update-AzServiceFabricDurability для обновления конфигурации кластера перед началом операции CreateOrUpdate для масштабируемого набора виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1849">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="7cf4c-1850">0.4.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1850">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="7cf4c-1851">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1851">Az.Profile</span></span>
* <span data-ttu-id="7cf4c-1852">Устранена проблема с Get-AzSubscription в CloudShell</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1852">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="7cf4c-1853">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1853">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7cf4c-1854">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1854">Az.Compute</span></span>
* <span data-ttu-id="7cf4c-1855">В список разрешений добавлены новые размеры виртуальных машин, для которых будет включено ускорение работы в сети при использовании простого набора параметров для New-AzVm</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1855">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="7cf4c-1856">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1856">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="7cf4c-1857">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1857">Az.DataLakeStore</span></span>
* <span data-ttu-id="7cf4c-1858">Добавлена поддержка правил виртуальной сети:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1858">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="7cf4c-1859">Get-AzDataLakeStoreVirtualNetworkRule: получение или отображение правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1859">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="7cf4c-1860">Add-AzDataLakeStoreVirtualNetworkRule: добавление правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1860">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="7cf4c-1861">Set-AzDataLakeStoreVirtualNetworkRule: изменение указанного правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1861">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="7cf4c-1862">Remove-AzDataLakeStoreVirtualNetworkRule: удаление правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1862">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7cf4c-1863">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1863">Az.Network</span></span>
* <span data-ttu-id="7cf4c-1864">Обновлен командлет Test-AzNetworkWatcherConnectivity. Теперь он позволяет передать значение протокола в серверную часть.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1864">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="7cf4c-1865">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1865">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="7cf4c-1866">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1866">Az.Resources</span></span>
* <span data-ttu-id="7cf4c-1867">Устранена проблема, из-за которой командлет Get-AzRoleDefinition возвращал непонятное исключение (если профиль по умолчанию не содержал подписки и область не была указана), благодаря добавлению понятного исключения в сценарий.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1867">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="7cf4c-1868">Также для набора параметров по умолчанию задано значение RoleDefinitionNameParameterSet.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1868">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="7cf4c-1869">0.3.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1869">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="7cf4c-1870">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1870">Azure.Storage</span></span>
* <span data-ttu-id="7cf4c-1871">Исправлена ошибка, из-за которой при копировании файла или большого двоичного объекта метаданные не копировались, если в целевом устройстве имелась проблема с метаданными.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1871">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="7cf4c-1872">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1872">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="7cf4c-1873">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1873">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="7cf4c-1874">Добавлена поддержка получения сведения об использовании ресурса хранилища для конкретного расположения. Также добавлено предупреждающее сообщение о том, что функция получения глобальных сведений об использовании ресурса хранилища устарела.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1874">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="7cf4c-1875">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1875">Get-AzStorageUsage</span></span>
    
#### <a name="azcognitiveservices"></a><span data-ttu-id="7cf4c-1876">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1876">Az.CognitiveServices</span></span>
* <span data-ttu-id="7cf4c-1877">Поддержка Get-AzCognitiveServicesAccountSkus без существующей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1877">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="7cf4c-1878">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1878">Az.Compute</span></span>
* <span data-ttu-id="7cf4c-1879">Исправлена команда Get-AzVM -ResourceGroupName <rg>, которая теперь может возвращать более 50 результатов</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1879">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="7cf4c-1880">Добавлен пример использования SimpleParameterSet в справку командлета New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1880">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="7cf4c-1881">Исправлена ошибка в сообщении о ходе выполнения для шифрования дисков Azure.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1881">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="7cf4c-1882">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1882">Az.DataFactoryV2</span></span>
* <span data-ttu-id="7cf4c-1883">Пакет .NET SDK для ADF обновлен до версии 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1883">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="7cf4c-1884">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1884">Az.Network</span></span>
* <span data-ttu-id="7cf4c-1885">Добавлена функциональность NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1885">Added NetworkProfile functionality.</span></span> <span data-ttu-id="7cf4c-1886">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1886">new cmdlets added</span></span>
    - <span data-ttu-id="7cf4c-1887">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1887">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="7cf4c-1888">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1888">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="7cf4c-1889">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1889">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="7cf4c-1890">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1890">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="7cf4c-1891">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1891">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="7cf4c-1892">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1892">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="7cf4c-1893">Добавлен канал связи служб в модель подсети.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1893">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="7cf4c-1894">Добавлены командлеты: New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1894">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="7cf4c-1895">Добавлены командлеты: Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1895">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="7cf4c-1896">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1896">Az.RedisCache</span></span>
* <span data-ttu-id="7cf4c-1897">С этого момента добавлена поддержка любой строки в качестве параметра Size.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1897">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="7cf4c-1898">Добавлено значение P5 во всплывающее окно PSArgumentCompleter.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1898">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="7cf4c-1899">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1899">Az.Resources</span></span>
* <span data-ttu-id="7cf4c-1900">Добавлен отсутствующий параметр -Mode в командлет Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1900">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="7cf4c-1901">Исправлена ошибка командлета Get-AzProviderOperation для операций, когда Origin содержит User</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1901">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="7cf4c-1902">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1902">Az.Sql</span></span>
* <span data-ttu-id="7cf4c-1903">Исправлена ошибка, при которой некоторые командлеты резервного копирования не распознавали текущую подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1903">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="7cf4c-1904">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1904">Az.Websites</span></span>
* <span data-ttu-id="7cf4c-1905">Новый командлет Get-AzWebAppContainerContinuousDeploymentUrl, который позволяет получить URL-адрес веб-перехватчика для развертывания контейнера</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1905">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="7cf4c-1906">Новые командлеты New-AzWebAppContainerPSSession и Enter-WebAppContainerPSSession, которые позволяют инициировать удаленный сеанс PowerShell в приложении-контейнере Windows</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1906">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="7cf4c-1907">0.2.0 — сентябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1907">0.2.0 - September 2018</span></span>
 <span data-ttu-id="7cf4c-1908">Начальный выпуск</span><span class="sxs-lookup"><span data-stu-id="7cf4c-1908">Initial Release</span></span>
