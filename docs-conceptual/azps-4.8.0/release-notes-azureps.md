---
title: Заметки о выпуске Azure PowerShell
description: Узнайте обо всех последних обновлениях модулей Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/10/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: ea374b23e85c16393e5de16b043ae0c28545cb61
ms.sourcegitcommit: 2036538797dd088728aee5ac5021472454d82eb2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2020
ms.locfileid: "93408077"
---
# <a name="azure-powershell-release-notes"></a><span data-ttu-id="cfa18-103">Заметки о выпуске Azure PowerShell</span><span class="sxs-lookup"><span data-stu-id="cfa18-103">Azure PowerShell release notes</span></span>

## <a name="480---october-2020"></a><span data-ttu-id="cfa18-104">4.8.0 — октябрь 2020 г.</span><span class="sxs-lookup"><span data-stu-id="cfa18-104">4.8.0 - October 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cfa18-105">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cfa18-105">Az.Accounts</span></span>
* <span data-ttu-id="cfa18-106">Исправлена проблема с анализом фиксированных дат DateTime в общих библиотеках [№ 13045]</span><span class="sxs-lookup"><span data-stu-id="cfa18-106">Fixed DateTime parse issue in common libraries [#13045]</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cfa18-107">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cfa18-107">Az.CognitiveServices</span></span>
* <span data-ttu-id="cfa18-108">Добавлен командлет New-AzCognitiveServicesAccountApiProperty.</span><span class="sxs-lookup"><span data-stu-id="cfa18-108">Added 'New-AzCognitiveServicesAccountApiProperty' cmdlet.</span></span>
* <span data-ttu-id="cfa18-109">Добавлена поддержка параметра ApiProperty для New-AzCognitiveServicesAccount и Set-AzCognitiveServicesAccount.</span><span class="sxs-lookup"><span data-stu-id="cfa18-109">Supported 'ApiProperty' parameter for 'New-AzCognitiveServicesAccount' and 'Set-AzCognitiveServicesAccount'</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cfa18-110">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cfa18-110">Az.Compute</span></span>
* <span data-ttu-id="cfa18-111">Исправлена проблема в Update-ASRRecoveryPlan путем заполнения FailoverTypes.</span><span class="sxs-lookup"><span data-stu-id="cfa18-111">Fixed issue in 'Update-ASRRecoveryPlan' by populating FailoverTypes</span></span>
* <span data-ttu-id="cfa18-112">В командлет Get-AzVmImage добавлены необязательные параметры -Top и -OrderBy.</span><span class="sxs-lookup"><span data-stu-id="cfa18-112">Added the '-Top' and '-OrderBy' optional parameters to the 'Get-AzVmImage' cmdlet.</span></span> 

#### <a name="azdatabricks"></a><span data-ttu-id="cfa18-113">Az.Databricks</span><span class="sxs-lookup"><span data-stu-id="cfa18-113">Az.Databricks</span></span>
* <span data-ttu-id="cfa18-114">Вышла общедоступная версия модуля Az.Databricks.</span><span class="sxs-lookup"><span data-stu-id="cfa18-114">General availability of 'Az.Databricks' module</span></span>
* <span data-ttu-id="cfa18-115">Добавлена поддержка пиринга между виртуальными сетями</span><span class="sxs-lookup"><span data-stu-id="cfa18-115">Added support for virtual network peering</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cfa18-116">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cfa18-116">Az.DataFactory</span></span>
* <span data-ttu-id="cfa18-117">Исправлена опечатка в выходных сообщениях</span><span class="sxs-lookup"><span data-stu-id="cfa18-117">Fixed typo in output messages</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="cfa18-118">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="cfa18-118">Az.EventHub</span></span>
* <span data-ttu-id="cfa18-119">Добавлен необязательный параметр-переключатель TrustedServiceAccessEnabled в командлет Set-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="cfa18-119">Added optional switch parameter 'TrustedServiceAccessEnabled' to 'Set-AzEventHubNetworkRuleSet' cmdlet</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="cfa18-120">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cfa18-120">Az.HDInsight</span></span>
* <span data-ttu-id="cfa18-121">Добавлено предупреждающее сообщение о том, что планируется прекращение поддержки параметров PublicNetworkAccessType и OutboundPublicNetworkAccessType</span><span class="sxs-lookup"><span data-stu-id="cfa18-121">Added warning message for planning to deprecate the parameters 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType'</span></span>
* <span data-ttu-id="cfa18-122">Добавлено предупреждающее сообщение о том, что планируется замена параметра DefaultStorageAccountName на StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="cfa18-122">Added warning message for planning to replace the parameter 'DefaultStorageAccountName' with 'StorageAccountResourceId'</span></span>
* <span data-ttu-id="cfa18-123">Добавлено предупреждающее сообщение о том, что планируется замена параметра DefaultStorageAccountKey на StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="cfa18-123">Added warning message for planning to replace the parameter 'DefaultStorageAccountKey' with 'StorageAccountKey'</span></span>
* <span data-ttu-id="cfa18-124">Добавлено предупреждающее сообщение о том, что планируется замена параметра DefaultStorageAccountType на StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="cfa18-124">Added warning message for planning to replace the parameter 'DefaultStorageAccountType' with 'StorageAccountType'</span></span>
* <span data-ttu-id="cfa18-125">Добавлено предупреждающее сообщение о том, что планируется замена параметра DefaultStorageContainer на StorageContainer</span><span class="sxs-lookup"><span data-stu-id="cfa18-125">Added warning message for planning to replace the parameter 'DefaultStorageContainer' with 'StorageContainer'</span></span>
* <span data-ttu-id="cfa18-126">Добавлено предупреждающее сообщение о том, что планируется замена параметра DefaultStorageRootPath на StorageRootPath</span><span class="sxs-lookup"><span data-stu-id="cfa18-126">Added warning message for planning to replace the parameter 'DefaultStorageRootPath' with 'StorageRootPath'</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cfa18-127">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cfa18-127">Az.IotHub</span></span>
* <span data-ttu-id="cfa18-128">Обновлен пакет SDK для устройств.</span><span class="sxs-lookup"><span data-stu-id="cfa18-128">Updated devices sdk.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cfa18-129">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cfa18-129">Az.KeyVault</span></span>
* <span data-ttu-id="cfa18-130">Указана точная дата удаления свойства SecretValueText</span><span class="sxs-lookup"><span data-stu-id="cfa18-130">Provided the detailed date of removing property SecretValueText</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="cfa18-131">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="cfa18-131">Az.ManagedServices</span></span>
* <span data-ttu-id="cfa18-132">Изменены предупреждения о критических изменениях в командлетах назначения и определения управляемых служб.</span><span class="sxs-lookup"><span data-stu-id="cfa18-132">Updated breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cfa18-133">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cfa18-133">Az.Monitor</span></span>
* <span data-ttu-id="cfa18-134">Исправлена ошибка, не позволявшая подавить предупреждающие сообщения.</span><span class="sxs-lookup"><span data-stu-id="cfa18-134">Fixed the bug that warning message cannot be suppressed.</span></span> <span data-ttu-id="cfa18-135">[№ 12889]</span><span class="sxs-lookup"><span data-stu-id="cfa18-135">[#12889]</span></span>
* <span data-ttu-id="cfa18-136">Добавлена поддержка параметра SkipMetricValidation в критериях правила генерации оповещений.</span><span class="sxs-lookup"><span data-stu-id="cfa18-136">Supported 'SkipMetricValidation' parameter in alert rule criteria.</span></span> <span data-ttu-id="cfa18-137">Это позволяет создать правило генерации оповещений для пользовательской метрики, которая еще не создана, настроив пропуск проверки этой метрики.</span><span class="sxs-lookup"><span data-stu-id="cfa18-137">Allows creating an alert rule on a custom metric that isn't yet emitted, by causing the metric validation to be skipped.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cfa18-138">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cfa18-138">Az.Network</span></span>
* <span data-ttu-id="cfa18-139">Добавлена политика Office365 в ресурс VPNSite</span><span class="sxs-lookup"><span data-stu-id="cfa18-139">Added Office365 Policy to VPNSite Resource</span></span>
    - <span data-ttu-id="cfa18-140">New-AzO365PolicyProperty</span><span class="sxs-lookup"><span data-stu-id="cfa18-140">'New-AzO365PolicyProperty'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cfa18-141">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cfa18-141">Az.RecoveryServices</span></span>
* <span data-ttu-id="cfa18-142">Добавлена проверка имени контейнера для резервного копирования рабочей нагрузки.</span><span class="sxs-lookup"><span data-stu-id="cfa18-142">Added container name validation for workload backup.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="cfa18-143">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="cfa18-143">Az.RedisCache</span></span>
* <span data-ttu-id="cfa18-144">Устранен сбой командлетов New-AzRedisCache и Set-AzRedisCache из-за проблемы с разрешениями, связанной с регистрацией поставщика ресурсов Microsoft.Cache</span><span class="sxs-lookup"><span data-stu-id="cfa18-144">Made 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets not fail because of permission issue related to registering Microsoft.Cache RP</span></span>

#### <a name="azsql"></a><span data-ttu-id="cfa18-145">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cfa18-145">Az.Sql</span></span>
* <span data-ttu-id="cfa18-146">Добавлен параметр BackupStorageRedundancy к следующим командлетам:</span><span class="sxs-lookup"><span data-stu-id="cfa18-146">Added BackupStorageRedundancy to the following:</span></span> 
    - <span data-ttu-id="cfa18-147">Restore-AzureRmSqlDatabase;</span><span class="sxs-lookup"><span data-stu-id="cfa18-147">'Restore-AzureRmSqlDatabase'</span></span>
    - <span data-ttu-id="cfa18-148">New-AzSqlDatabaseCopy;</span><span class="sxs-lookup"><span data-stu-id="cfa18-148">'New-AzSqlDatabaseCopy'</span></span>
    - <span data-ttu-id="cfa18-149">New-AzSqlDatabaseSecondary.</span><span class="sxs-lookup"><span data-stu-id="cfa18-149">'New-AzSqlDatabaseSecondary'</span></span>
* <span data-ttu-id="cfa18-150">Удален учет регистра для параметра BackupStorageRedundancy во всех ссылках на базы данных SQL</span><span class="sxs-lookup"><span data-stu-id="cfa18-150">Removed case sensitivity for BackupStorageRedundancy parameter for all SQL DB references</span></span> 
* <span data-ttu-id="cfa18-151">Обновлены имена в предупреждающем сообщении BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="cfa18-151">Updated BackupStorageRedundancy warning message names</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cfa18-152">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cfa18-152">Az.Storage</span></span>
* <span data-ttu-id="cfa18-153">Добавлена поддержка включения, отключения и получения свойств обратимого удаления для общей папки в службе файлов учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="cfa18-153">Supported enable/disable/get share soft delete properties on file Service of a Storage account</span></span>
    - <span data-ttu-id="cfa18-154">Update-AzStorageFileServiceProperty</span><span class="sxs-lookup"><span data-stu-id="cfa18-154">'Update-AzStorageFileServiceProperty'</span></span>
    - <span data-ttu-id="cfa18-155">Get-AzStorageFileServiceProperty</span><span class="sxs-lookup"><span data-stu-id="cfa18-155">'Get-AzStorageFileServiceProperty'</span></span>
* <span data-ttu-id="cfa18-156">Поддерживается вывод списка общих папок в учетной записи хранения, включая удаленные общие папки, а также добавлена возможность получить данные об использовании одной общей папки.</span><span class="sxs-lookup"><span data-stu-id="cfa18-156">Supported list file shares include the deleted ones of a Storage account, and Get single file share usage</span></span>
    - <span data-ttu-id="cfa18-157">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="cfa18-157">'Get-AzRmStorageShare'</span></span>
* <span data-ttu-id="cfa18-158">Добавлено восстановление удаленной общей папки</span><span class="sxs-lookup"><span data-stu-id="cfa18-158">Supported restore a deleted file share</span></span>
    - <span data-ttu-id="cfa18-159">Restore-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="cfa18-159">'Restore-AzRmStorageShare'</span></span>
* <span data-ttu-id="cfa18-160">Изменены командлеты для изменения свойств службы BLOB-объектов. Эти командлеты не получают свойства с сервера, а только сохраняют новые параметры на сервер.</span><span class="sxs-lookup"><span data-stu-id="cfa18-160">Changed the cmdlets for modify blob service properties, won't get the original properties from server, but only set the modified properties to server.</span></span>
    - <span data-ttu-id="cfa18-161">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="cfa18-161">'Enable-AzStorageBlobDeleteRetentionPolicy'</span></span>
    - <span data-ttu-id="cfa18-162">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="cfa18-162">'Disable-AzStorageBlobDeleteRetentionPolicy'</span></span>  
    - <span data-ttu-id="cfa18-163">Enable-AzStorageBlobRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="cfa18-163">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="cfa18-164">Disable-AzStorageBlobRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="cfa18-164">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="cfa18-165">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="cfa18-165">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="cfa18-166">Устранена проблема с получением справки для значения по умолчанию для параметра -Kind командлета New-AzStorageAccount [№ 12189]</span><span class="sxs-lookup"><span data-stu-id="cfa18-166">Fixed help issue for New-AzStorageAccount parameter -Kind default value [#12189]</span></span>
* <span data-ttu-id="cfa18-167">Устранена проблема путем добавления примера правильной настройки ContentType для отправки большого двоичного объекта [№ 12989]</span><span class="sxs-lookup"><span data-stu-id="cfa18-167">Fixed issue by add example to show how to set correct ContentType in blob upload [#12989]</span></span>

## <a name="470---september-2020"></a><span data-ttu-id="cfa18-168">4.7.0 — сентябрь 2020 г.</span><span class="sxs-lookup"><span data-stu-id="cfa18-168">4.7.0 - September 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cfa18-169">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cfa18-169">Az.Accounts</span></span>
* <span data-ttu-id="cfa18-170">Изменен формат сообщений о предстоящих критических изменениях.</span><span class="sxs-lookup"><span data-stu-id="cfa18-170">Formatted the upcoming breaking change messages</span></span>
* <span data-ttu-id="cfa18-171">Версия Azure.Core обновлена до 1.4.1.</span><span class="sxs-lookup"><span data-stu-id="cfa18-171">Updated Azure.Core to 1.4.1</span></span>

#### <a name="azaks"></a><span data-ttu-id="cfa18-172">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="cfa18-172">Az.Aks</span></span>
* <span data-ttu-id="cfa18-173">Добавлена логика проверки параметров на стороне клиента для командлетов New-AzAksCluster, Set-AzAksCluster и New-AzAksNodePool.</span><span class="sxs-lookup"><span data-stu-id="cfa18-173">Added client side parameter validation logic for 'New-AzAksCluster', 'Set-AzAksCluster' and 'New-AzAksNodePool'.</span></span> <span data-ttu-id="cfa18-174">[12372]</span><span class="sxs-lookup"><span data-stu-id="cfa18-174">[#12372]</span></span>
* <span data-ttu-id="cfa18-175">Добавлена поддержка для надстроек в командлете New-AzAksCluster.</span><span class="sxs-lookup"><span data-stu-id="cfa18-175">Added support for add-ons in 'New-AzAksCluster'.</span></span> <span data-ttu-id="cfa18-176">[11239]</span><span class="sxs-lookup"><span data-stu-id="cfa18-176">[#11239]</span></span>
* <span data-ttu-id="cfa18-177">Добавлены командлеты Enable-AzAksAddOn и Disable-AzAksAddOn для надстроек.</span><span class="sxs-lookup"><span data-stu-id="cfa18-177">Added cmdlets 'Enable-AzAksAddOn' and 'Disable-AzAksAddOn' for add-ons.</span></span> <span data-ttu-id="cfa18-178">[11239]</span><span class="sxs-lookup"><span data-stu-id="cfa18-178">[#11239]</span></span>
* <span data-ttu-id="cfa18-179">Добавлен параметр GenerateSshKey для командлета New-AzAksCluster.</span><span class="sxs-lookup"><span data-stu-id="cfa18-179">Added parameter 'GenerateSshKey' for 'New-AzAksCluster'.</span></span> <span data-ttu-id="cfa18-180">[12371]</span><span class="sxs-lookup"><span data-stu-id="cfa18-180">[#12371]</span></span>
* <span data-ttu-id="cfa18-181">Обновлена версия API до 2020-06-01.</span><span class="sxs-lookup"><span data-stu-id="cfa18-181">Updated api version to 2020-06-01.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cfa18-182">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cfa18-182">Az.CognitiveServices</span></span>
* <span data-ttu-id="cfa18-183">Реализовано отображение дополнительных юридических условий для определенных API.</span><span class="sxs-lookup"><span data-stu-id="cfa18-183">Showed additional legal terms for certain APIs.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cfa18-184">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cfa18-184">Az.Compute</span></span>
* <span data-ttu-id="cfa18-185">Добавлен необязательный параметр -EncryptionType к командлету New-AzVmDiskEncryptionSetConfig.</span><span class="sxs-lookup"><span data-stu-id="cfa18-185">Added the '-EncryptionType' optional parameter to 'New-AzVmDiskEncryptionSetConfig'</span></span>
* <span data-ttu-id="cfa18-186">Новые командлеты для нового типа ресурсов: DiskAccess (Get-AzDiskAccess, New-AzDiskAccess, Get-AzDiskAccess).</span><span class="sxs-lookup"><span data-stu-id="cfa18-186">New cmdlets for new resource type: DiskAccess 'Get-AzDiskAccess', 'New-AzDiskAccess', 'Get-AzDiskAccess'</span></span>
* <span data-ttu-id="cfa18-187">Добавлены необязательные параметры -DiskAccessId и -NetworkAccessPolicy к командлету New-AzSnapshotConfig.</span><span class="sxs-lookup"><span data-stu-id="cfa18-187">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzSnapshotConfig'</span></span>
* <span data-ttu-id="cfa18-188">Добавлены необязательные параметры -DiskAccessId и -NetworkAccessPolicy к командлету New-AzDiskConfig.</span><span class="sxs-lookup"><span data-stu-id="cfa18-188">Added optional parameters '-DiskAccessId' and '-NetworkAccessPolicy' to 'New-AzDiskConfig'</span></span>
* <span data-ttu-id="cfa18-189">Добавлено свойство PatchStatus к представлению экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="cfa18-189">Added 'PatchStatus' property to VirtualMachine Instance View</span></span>
* <span data-ttu-id="cfa18-190">Добавлено свойство VMHealth к представлению экземпляра виртуальной машины, которое является возвращенным объектом при вызове Get-AzVm с параметром -Status.</span><span class="sxs-lookup"><span data-stu-id="cfa18-190">Added 'VMHealth' property to the virtual machine's instance view, which is the returned object when 'Get-AzVm' is invoked with '-Status'</span></span>
* <span data-ttu-id="cfa18-191">Добавлено поле AssignedHost к представлениям экземпляра Get-AzVM и Get-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="cfa18-191">Added 'AssignedHost' field to 'Get-AzVM' and 'Get-AzVmss' instance views.</span></span> <span data-ttu-id="cfa18-192">В поле отображается идентификатор ресурса для экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="cfa18-192">The field shows the resource id of the virtual machine instance</span></span>
* <span data-ttu-id="cfa18-193">Добавлен необязательный параметр -SupportAutomaticPlacement к командлету New-AzHostGroup.</span><span class="sxs-lookup"><span data-stu-id="cfa18-193">Added optional parameter '-SupportAutomaticPlacement' to 'New-AzHostGroup'</span></span> 
* <span data-ttu-id="cfa18-194">Добавлен параметр -HostGroupId к командлетам New-AzVm и New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="cfa18-194">Added the '-HostGroupId' parameter to 'New-AzVm' and 'New-AzVmss'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cfa18-195">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cfa18-195">Az.DataFactory</span></span>
* <span data-ttu-id="cfa18-196">Версия пакета SDK ADF для .NET обновлена до 4.11.0.</span><span class="sxs-lookup"><span data-stu-id="cfa18-196">Updated ADF .Net SDK version to 4.11.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="cfa18-197">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="cfa18-197">Az.EventHub</span></span>
* <span data-ttu-id="cfa18-198">Добавлены новые командлеты кластера: New-AzEventHubCluster, Set-AzEventHubCluster, Get-AzEventHubCluster, Remove-AzEventHubCluster, Get-AzEventHubClustersAvailableRegions.</span><span class="sxs-lookup"><span data-stu-id="cfa18-198">Added new Cluster cmdlets - 'New-AzEventHubCluster', 'Set-AzEventHubCluster', 'Get-AzEventHubCluster', 'Remove-AzEventHubCluster', 'Get-AzEventHubClustersAvailableRegions'.</span></span>
* <span data-ttu-id="cfa18-199">Исправление для проблемы № 10722: исправление ошибки, из-за которой свойству AuthorizationRule.Rights назначалось только значение Listen (Прослушивание).</span><span class="sxs-lookup"><span data-stu-id="cfa18-199">Fixed for issue #10722 : Fix for assigning only 'Listen' to AuthorizationRule rights.</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="cfa18-200">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="cfa18-200">Az.Functions</span></span>
* <span data-ttu-id="cfa18-201">Удалена возможность создавать Функции версии 2 в регионах, которые не поддерживают ее.</span><span class="sxs-lookup"><span data-stu-id="cfa18-201">Removed the ability to create v2 Functions in regions that do not support it.</span></span>
* <span data-ttu-id="cfa18-202">PowerShell 6.2 не рекомендуется к использованию.</span><span class="sxs-lookup"><span data-stu-id="cfa18-202">Deprecated PowerShell 6.2.</span></span> <span data-ttu-id="cfa18-203">Добавлено предупреждение при создании пользователем приложения-функции PowerShell 6.2 о том, что рекомендуется создать приложение-функцию PowerShell 7.0.</span><span class="sxs-lookup"><span data-stu-id="cfa18-203">Added a warning for when a user creates a PowerShell 6.2 function app that advises them to create a PowerShell 7.0 function app instead.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="cfa18-204">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cfa18-204">Az.HDInsight</span></span>
* <span data-ttu-id="cfa18-205">Добавлена поддержка создания кластера с использованием конфигурации автомасштабирования.</span><span class="sxs-lookup"><span data-stu-id="cfa18-205">Supported creating cluster with Autoscale configuration</span></span>
    - <span data-ttu-id="cfa18-206">Добавлен новый параметр AutoscaleConfiguration к командлету New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="cfa18-206">Add new parameter 'AutoscaleConfiguration' to the cmdlet 'New-AzHDInsightCluster'</span></span>
* <span data-ttu-id="cfa18-207">Добавлена поддержка управления конфигурацией автомасштабирования для кластера.</span><span class="sxs-lookup"><span data-stu-id="cfa18-207">Supported operating cluster's Autoscale configuration</span></span>
    - <span data-ttu-id="cfa18-208">Добавлен новый командлет Get-AzHDInsihgtClusterAutoscaleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="cfa18-208">Add new cmdlet 'Get-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="cfa18-209">Добавлен новый командлет New-AzHDInsihgtClusterAutoscaleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="cfa18-209">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="cfa18-210">Добавлен новый командлет Set-AzHDInsihgtClusterAutoscaleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="cfa18-210">Add new cmdlet 'Set-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="cfa18-211">Добавлен новый командлет Remove-AzHDInsihgtClusterAutoscaleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="cfa18-211">Add new cmdlet 'Remove-AzHDInsihgtClusterAutoscaleConfiguration'</span></span>
    - <span data-ttu-id="cfa18-212">Добавлен новый командлет New-AzHDInsihgtClusterAutoscaleScheduleCondition.</span><span class="sxs-lookup"><span data-stu-id="cfa18-212">Add new cmdlet 'New-AzHDInsihgtClusterAutoscaleScheduleCondition'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cfa18-213">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cfa18-213">Az.KeyVault</span></span>
* <span data-ttu-id="cfa18-214">Добавлена поддержка авторизации с помощью RBAC [10557].</span><span class="sxs-lookup"><span data-stu-id="cfa18-214">Added support for RBAC authorization [#10557]</span></span>
* <span data-ttu-id="cfa18-215">Расширена обработка ошибок в командлете Set-AzKeyVaultAccessPolicy [4007].</span><span class="sxs-lookup"><span data-stu-id="cfa18-215">Enhanced error handling in 'Set-AzKeyVaultAccessPolicy' [#4007]</span></span>

#### <a name="azkusto"></a><span data-ttu-id="cfa18-216">Az.Kusto</span><span class="sxs-lookup"><span data-stu-id="cfa18-216">Az.Kusto</span></span>
* <span data-ttu-id="cfa18-217">Выпущена общедоступная версия модуля Az.Kusto.</span><span class="sxs-lookup"><span data-stu-id="cfa18-217">General availability of 'Az.Kusto' module</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cfa18-218">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cfa18-218">Az.Network</span></span>
* <span data-ttu-id="cfa18-219">[Критическое изменение] Обновлены приведенные ниже командлеты для соответствия виртуальному маршрутизатору ресурсов и виртуальному концентратору.</span><span class="sxs-lookup"><span data-stu-id="cfa18-219">[Breaking Change] Updated below cmdlets to align resource virtual router and virtual hub</span></span>
    - <span data-ttu-id="cfa18-220">New-AzVirtualRouter:</span><span class="sxs-lookup"><span data-stu-id="cfa18-220">'New-AzVirtualRouter':</span></span> 
        - <span data-ttu-id="cfa18-221">Добавлен параметр -HostedSubnet для поддержки дочернего ресурса конфигурации IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="cfa18-221">Added -HostedSubnet parameter to support IP configuration child resource</span></span>
        - <span data-ttu-id="cfa18-222">Удалены параметры -HostedGateway и -HostedGatewayId.</span><span class="sxs-lookup"><span data-stu-id="cfa18-222">deleted -HostedGateway and -HostedGatewayId</span></span>
    - <span data-ttu-id="cfa18-223">Get-AzVirtualRouter:</span><span class="sxs-lookup"><span data-stu-id="cfa18-223">'Get-AzVirtualRouter':</span></span>
        - <span data-ttu-id="cfa18-224">добавлен набор параметров на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="cfa18-224">Added subscription level parameter set</span></span>
    - <span data-ttu-id="cfa18-225">Remove-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="cfa18-225">'Remove-AzVirtualRouter'</span></span>
    - <span data-ttu-id="cfa18-226">Add-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="cfa18-226">'Add-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="cfa18-227">Get-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="cfa18-227">'Get-AzVirtualRouterPeer'</span></span>
    - <span data-ttu-id="cfa18-228">Remove-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="cfa18-228">'Remove-AzVirtualRouterPeer'</span></span>
* <span data-ttu-id="cfa18-229">Добавлен новый командлет для порта Azure Express Route.</span><span class="sxs-lookup"><span data-stu-id="cfa18-229">Added new cmdlet for Azure Express Route Port</span></span>
    - <span data-ttu-id="cfa18-230">New-AzExpressRoutePortLOA</span><span class="sxs-lookup"><span data-stu-id="cfa18-230">'New-AzExpressRoutePortLOA'</span></span>
* <span data-ttu-id="cfa18-231">Добавлено свойство RemoteBgpCommunities к ресурсу пиринга виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="cfa18-231">Added RemoteBgpCommunities property to the VirtualNetwork Peering Resource</span></span>
* <span data-ttu-id="cfa18-232">Изменено сообщение с предупреждением для New-AzLoadBalancerFrontendIpConfig, New-AzPublicIpAddress и New-AzPublicIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="cfa18-232">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>
* <span data-ttu-id="cfa18-233">Добавлено свойство VpnGatewayIpConfigurations в выходные данные командлета Get-AzVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="cfa18-233">Added VpnGatewayIpConfigurations to 'Get-AzVpnGateway' output</span></span>
* <span data-ttu-id="cfa18-234">Исправлена ошибка командлета Set-AzApplicationGatewaySslCertificate [9488].</span><span class="sxs-lookup"><span data-stu-id="cfa18-234">Fixed bug for 'Set-AzApplicationGatewaySslCertificate' [#9488]</span></span>
* <span data-ttu-id="cfa18-235">Добавлен параметр AllowActiveFTP в AzureFirewall.</span><span class="sxs-lookup"><span data-stu-id="cfa18-235">Added 'AllowActiveFTP' parameter to 'AzureFirewall'</span></span>
* <span data-ttu-id="cfa18-236">Обновлены следующие команды для функции: Включена возможность настройки и удаления параметров безопасности в Интернете на VPN-шлюзе P2S виртуальной глобальной сети.</span><span class="sxs-lookup"><span data-stu-id="cfa18-236">Updated below commands for feature: Enable internet security set/remove on VirtualWan P2SVpnGateway.</span></span>
- <span data-ttu-id="cfa18-237">Обновлен командлет New-AzP2sVpnGateway: Добавлен необязательный параметр EnableInternetSecurityFlag для клиентов, позволяющий задать значение true для включения безопасности в Интернете на VPN-шлюзе P2S, который будет применяться к клиентам с подключениями типа "точка — сеть".</span><span class="sxs-lookup"><span data-stu-id="cfa18-237">Updated 'New-AzP2sVpnGateway': Added optional switch parameter 'EnableInternetSecurityFlag' for customers to set true to enable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
- <span data-ttu-id="cfa18-238">Обновлен командлет Update-AzP2sVpnGateway: Добавлены необязательные параметры EnableInternetSecurityFlag и DisableInternetSecurityFlag для клиентов, позволяющий задать значение true/false для включения/отключения безопасности в Интернете на VPN-шлюзе P2S, который будет применяться к клиентам с подключениями типа "точка — сеть".</span><span class="sxs-lookup"><span data-stu-id="cfa18-238">Updated 'Update-AzP2sVpnGateway': Added optional switch parameters 'EnableInternetSecurityFlag' or 'DisableInternetSecurityFlag' for customers to set true/false to enable/disable internet security on P2SVpnGateway, which will be applied for Point to site clients.</span></span>
* <span data-ttu-id="cfa18-239">Добавлен новый командлет Reset-AzP2sVpnGateway для клиентов, позволяющий сбрасывать и перезагружать VPN-шлюз P2S виртуальной глобальной сети для устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="cfa18-239">Added new cmdlet 'Reset-AzP2sVpnGateway' for customers to reset/reboot their VirtualWan P2SVpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="cfa18-240">Добавлен новый командлет Reset-AzVpnGateway для клиентов, позволяющий сбрасывать и перезагружать VPN-шлюз виртуальной глобальной сети для устранения неполадок.</span><span class="sxs-lookup"><span data-stu-id="cfa18-240">Added new cmdlet 'Reset-AzVpnGateway' for customers to reset/reboot their VirtualWan VpnGateway for troubleshooting.</span></span>
* <span data-ttu-id="cfa18-241">Обновлен командлет Set-AzVirtualNetworkSubnetConfig.</span><span class="sxs-lookup"><span data-stu-id="cfa18-241">Updated 'Set-AzVirtualNetworkSubnetConfig'</span></span>
    - <span data-ttu-id="cfa18-242">Для свойств группы безопасности сети и таблицы маршрутизации подсети теперь задаются значения NULL, если они явно указаны в параметрах [1548][9718].</span><span class="sxs-lookup"><span data-stu-id="cfa18-242">Set NSG and Route Table properties of subnet to null if explicitly set in parameters [#1548][#9718]</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cfa18-243">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cfa18-243">Az.RecoveryServices</span></span>
* <span data-ttu-id="cfa18-244">Исправлено состояние удаления для элементов резервного копирования рабочей нагрузки.</span><span class="sxs-lookup"><span data-stu-id="cfa18-244">Fixed the Delete State for workload Backup Items.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cfa18-245">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cfa18-245">Az.Resources</span></span>
* <span data-ttu-id="cfa18-246">Добавлена отсутствующая проверка для командлета Set-AzRoleAssignment.</span><span class="sxs-lookup"><span data-stu-id="cfa18-246">Added missing check for Set-AzRoleAssignment</span></span>
* <span data-ttu-id="cfa18-247">Добавлен важный атрибут в параметр SubscriptionId командлета Get-AzResourceGroupDeploymentOperation.</span><span class="sxs-lookup"><span data-stu-id="cfa18-247">Added breaking change attribute to 'SubscriptionId' parameter of 'Get-AzResourceGroupDeploymentOperation'</span></span>
* <span data-ttu-id="cfa18-248">Обновлены командлеты What-If шаблона ARM для отображения изменений ресурса Ignore последними.</span><span class="sxs-lookup"><span data-stu-id="cfa18-248">Updated ARM template What-If cmdlets to show 'Ignore' resource changes last</span></span>
* <span data-ttu-id="cfa18-249">Исправлены проблемы безопасности и сериализации параметров массива для командлетов развертывания [12773].</span><span class="sxs-lookup"><span data-stu-id="cfa18-249">Fixed secure and array parameter serialization issues for deployment cmdlets [#12773]</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="cfa18-250">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cfa18-250">Az.ServiceFabric</span></span>
* <span data-ttu-id="cfa18-251">Добавлены новые командлеты для управляемых кластеров и типов узлов:</span><span class="sxs-lookup"><span data-stu-id="cfa18-251">Added new cmdlets for managed clusters and node types:</span></span>
    - <span data-ttu-id="cfa18-252">New-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="cfa18-252">'New-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="cfa18-253">Get-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="cfa18-253">'Get-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="cfa18-254">Set-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="cfa18-254">'Set-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="cfa18-255">Remove-AzServiceFabricManagedCluster</span><span class="sxs-lookup"><span data-stu-id="cfa18-255">'Remove-AzServiceFabricManagedCluster'</span></span>
    - <span data-ttu-id="cfa18-256">Add-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="cfa18-256">'Add-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="cfa18-257">Remove-AzServiceFabricManagedClusterClientCertificate</span><span class="sxs-lookup"><span data-stu-id="cfa18-257">'Remove-AzServiceFabricManagedClusterClientCertificate'</span></span>
    - <span data-ttu-id="cfa18-258">New-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="cfa18-258">'New-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="cfa18-259">Get-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="cfa18-259">'Get-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="cfa18-260">Set-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="cfa18-260">'Set-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="cfa18-261">Remove-AzServiceFabricManagedNodeType</span><span class="sxs-lookup"><span data-stu-id="cfa18-261">'Remove-AzServiceFabricManagedNodeType'</span></span>
    - <span data-ttu-id="cfa18-262">Add-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="cfa18-262">'Add-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="cfa18-263">Add-AzServiceFabricManagedNodeTypeVMSecret</span><span class="sxs-lookup"><span data-stu-id="cfa18-263">'Add-AzServiceFabricManagedNodeTypeVMSecret'</span></span>
    - <span data-ttu-id="cfa18-264">Remove-AzServiceFabricManagedNodeTypeVMExtension</span><span class="sxs-lookup"><span data-stu-id="cfa18-264">'Remove-AzServiceFabricManagedNodeTypeVMExtension'</span></span>
    - <span data-ttu-id="cfa18-265">Restart-AzServiceFabricManagedNodeTyp</span><span class="sxs-lookup"><span data-stu-id="cfa18-265">'Restart-AzServiceFabricManagedNodeTyp'</span></span>
* <span data-ttu-id="cfa18-266">Пакет SDK для Service Fabric обновлен до версии 1.2.0, в которой используется версия API 2020-03-01 поставщика ресурсов Service Fabric для текущей модели и 2020-01-01-preview для управляемых кластеров.</span><span class="sxs-lookup"><span data-stu-id="cfa18-266">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2020-03-01 for the current model and 2020-01-01-preview for managed clusters.</span></span>

#### <a name="azsql"></a><span data-ttu-id="cfa18-267">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cfa18-267">Az.Sql</span></span>
* <span data-ttu-id="cfa18-268">Добавлен параметр BackupStorageRedundancy к командлетам New-AzSqlInstance и Get-AzSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="cfa18-268">Added BackupStorageRedundancy to 'New-AzSqlInstance' and 'Get-AzSqlInstance'</span></span>
* <span data-ttu-id="cfa18-269">Добавлен командлет Get-AzSqlServerActiveDirectoryOnlyAuthentication.</span><span class="sxs-lookup"><span data-stu-id="cfa18-269">Added cmdlet 'Get-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="cfa18-270">Добавлен командлет Enable-AzSqlServerActiveDirectoryOnlyAuthentication.</span><span class="sxs-lookup"><span data-stu-id="cfa18-270">Added cmdlet 'Enable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="cfa18-271">Добавлен параметр Force к командлету New-AzSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="cfa18-271">Added Force parameter to 'New-AzSqlInstance'</span></span>
* <span data-ttu-id="cfa18-272">Добавлены командлеты для службы воспроизведения журнала управляемой базы данных.</span><span class="sxs-lookup"><span data-stu-id="cfa18-272">Added cmdlets for Managed Database Log Replay service</span></span>
    - <span data-ttu-id="cfa18-273">Start-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="cfa18-273">'Start-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="cfa18-274">Get-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="cfa18-274">'Get-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="cfa18-275">Complete-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="cfa18-275">'Complete-AzSqlInstanceDatabaseLogReplay'</span></span>
    - <span data-ttu-id="cfa18-276">Stop-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="cfa18-276">'Stop-AzSqlInstanceDatabaseLogReplay'</span></span>
* <span data-ttu-id="cfa18-277">Добавлен командлет Get-AzSqlInstanceActiveDirectoryOnlyAuthentication.</span><span class="sxs-lookup"><span data-stu-id="cfa18-277">Added cmdlet 'Get-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="cfa18-278">Добавлен командлет Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication.</span><span class="sxs-lookup"><span data-stu-id="cfa18-278">Added cmdlet 'Enable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="cfa18-279">Добавлен командлет Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication.</span><span class="sxs-lookup"><span data-stu-id="cfa18-279">Added cmdlet 'Disable-AzSqlInstanceActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="cfa18-280">Обновлены командлеты New-AzSqlDatabaseImport и New-AzSqlDatabaseExport для поддержки функциональности сетевой изоляции.</span><span class="sxs-lookup"><span data-stu-id="cfa18-280">Updated cmdlets 'New-AzSqlDatabaseImport' and 'New-AzSqlDatabaseExport' to support network isolation functionality</span></span>
* <span data-ttu-id="cfa18-281">Добавлен командлет New-AzSqlDatabaseImportExisting.</span><span class="sxs-lookup"><span data-stu-id="cfa18-281">Added cmdlet 'New-AzSqlDatabaseImportExisting'</span></span>
* <span data-ttu-id="cfa18-282">Обновлены командлеты баз данных для поддержки указания типа хранилища резервных копий.</span><span class="sxs-lookup"><span data-stu-id="cfa18-282">Updated Databases cmdlets to support backup storage type specification</span></span>
* <span data-ttu-id="cfa18-283">Добавлен параметр Force к командлету New-AzSqlDatabase.</span><span class="sxs-lookup"><span data-stu-id="cfa18-283">Added Force parameter to 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="cfa18-284">Добавлено предупреждение для конфигурации BackupStorageRedundancy в выбранных регионах в командлете New-AzSqlDatabase.</span><span class="sxs-lookup"><span data-stu-id="cfa18-284">Added warning for BackupStorageRedundancy configuration in select regions in 'New-AzSqlDatabase'</span></span>
* <span data-ttu-id="cfa18-285">Обновлены командлеты ActiveDirectoryOnlyAuthentication для сервера и экземпляра для включения ResourceId и InputObject.</span><span class="sxs-lookup"><span data-stu-id="cfa18-285">Updated ActiveDirectoryOnlyAuthentication cmdlets for server and instance to include ResourceId and InputObject</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cfa18-286">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cfa18-286">Az.Storage</span></span>
* <span data-ttu-id="cfa18-287">Исправлен сбой отправки BLOB-объекта путем обновления до Microsoft.Azure.Storage.DataMovement 2.0.0 [12220].</span><span class="sxs-lookup"><span data-stu-id="cfa18-287">Fixed upload blob fail by upgrade to Microsoft.Azure.Storage.DataMovement 2.0.0 [#12220]</span></span>
* <span data-ttu-id="cfa18-288">Реализована поддержка восстановления до точки во времени.</span><span class="sxs-lookup"><span data-stu-id="cfa18-288">Supported Point In Time Restore</span></span>
    - <span data-ttu-id="cfa18-289">Enable-AzStorageBlobRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="cfa18-289">'Enable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="cfa18-290">Disable-AzStorageBlobRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="cfa18-290">'Disable-AzStorageBlobRestorePolicy'</span></span>
    - <span data-ttu-id="cfa18-291">New-AzStorageBlobRangeToRestore</span><span class="sxs-lookup"><span data-stu-id="cfa18-291">'New-AzStorageBlobRangeToRestore'</span></span>
    - <span data-ttu-id="cfa18-292">Restore-AzStorageBlobRange</span><span class="sxs-lookup"><span data-stu-id="cfa18-292">'Restore-AzStorageBlobRange'</span></span>
* <span data-ttu-id="cfa18-293">Реализована поддержка получения состояния восстановления BLOB-объекта путем выполнения командлета Get-AzureRmStorageAccount с параметром -IncludeBlobRestoreStatus.</span><span class="sxs-lookup"><span data-stu-id="cfa18-293">Supported get blob restore status of Storage account by run get-AzureRMStorageAccount with parameter -IncludeBlobRestoreStatus</span></span> 
    - <span data-ttu-id="cfa18-294">Get-AzureRMStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cfa18-294">'Get-AzureRMStorageAccount'</span></span>
* <span data-ttu-id="cfa18-295">Добавлено важное сообщение с предупреждением о предстоящем изменении выходных данных командлета.</span><span class="sxs-lookup"><span data-stu-id="cfa18-295">Added breaking change warning message for upcoming cmdlet output change</span></span>
    - <span data-ttu-id="cfa18-296">Get-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="cfa18-296">'Get-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="cfa18-297">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="cfa18-297">'Set-AzStorageContainerStoredAccessPolicy'</span></span>
    - <span data-ttu-id="cfa18-298">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="cfa18-298">'Set-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="cfa18-299">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="cfa18-299">'Get-AzStorageAccountManagementPolicy'</span></span>
    - <span data-ttu-id="cfa18-300">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="cfa18-300">'Add-AzStorageAccountManagementPolicyAction'</span></span>
    - <span data-ttu-id="cfa18-301">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="cfa18-301">'New-AzStorageAccountManagementPolicyRule'</span></span>
* <span data-ttu-id="cfa18-302">Версия пакета SDK Microsoft.Azure.Cosmos.Table обновлена до 1.0.8.</span><span class="sxs-lookup"><span data-stu-id="cfa18-302">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.8</span></span>

### <a name="thanks-to-our-community-contributors"></a><span data-ttu-id="cfa18-303">Благодарим наших участников сообщества</span><span class="sxs-lookup"><span data-stu-id="cfa18-303">Thanks to our community contributors</span></span>
* <span data-ttu-id="cfa18-304">Томас Ван Лере (Thomas Van Laere) (@ThomVanL), добавление Dockerfile-alpine-3.10 (12911).</span><span class="sxs-lookup"><span data-stu-id="cfa18-304">Thomas Van Laere (@ThomVanL), Add Dockerfile-alpine-3.10 (#12911)</span></span> 
* <span data-ttu-id="cfa18-305">Лохит Чаудари Чилукури (Lohith Chowdary Chilukuri) (@Lochiluk), обновление Remove-AzNetworkInterfaceIpConfig.md (12807).</span><span class="sxs-lookup"><span data-stu-id="cfa18-305">Lohith Chowdary Chilukuri (@Lochiluk), Update Remove-AzNetworkInterfaceIpConfig.md (#12807)</span></span> 
* <span data-ttu-id="cfa18-306">Роберт Стрэнд (Roberth Strand) (@roberthstrand), Get-AzResourceGroup — новый пример и очистка (12828).</span><span class="sxs-lookup"><span data-stu-id="cfa18-306">Roberth Strand (@roberthstrand), Get-AzResourceGroup - New example, and cleanup (#12828)</span></span> 
* <span data-ttu-id="cfa18-307">Рави Мишра (Ravi Mishra) (@inmishrar), обновление стека среды выполнения веб-приложений Azure до .NET Core (12833).</span><span class="sxs-lookup"><span data-stu-id="cfa18-307">Ravi Mishra (@inmishrar), update Azure Web App runtime stack to DOTNETCORE (#12833)</span></span> 
* <span data-ttu-id="cfa18-308">@jack-education, обновление Set-AzVirtualNetworkSubnetConfig для разрешения удаления группы безопасности сети и таблицы маршрутизации из подсети (12351).</span><span class="sxs-lookup"><span data-stu-id="cfa18-308">@jack-education, Updated Set-AzVirtualNetworkSubnetConfig to allow NSG and Route Table to be removed from subnet (#12351)</span></span> 
* <span data-ttu-id="cfa18-309">@hagop-globanet, обновление Add-AzApplicationGatewayCustomError.md (12784).</span><span class="sxs-lookup"><span data-stu-id="cfa18-309">@hagop-globanet, Update Add-AzApplicationGatewayCustomError.md (#12784)</span></span> 
* <span data-ttu-id="cfa18-310">Джошуа Ван Даален (Joshua Van Daalen) (@greenSacrifice)</span><span class="sxs-lookup"><span data-stu-id="cfa18-310">Joshua Van Daalen (@greenSacrifice)</span></span>
  * <span data-ttu-id="cfa18-311">Изменение правописания Proeprty на Property (12821)</span><span class="sxs-lookup"><span data-stu-id="cfa18-311">Update spelling of Property to Property (#12821)</span></span> 
  * <span data-ttu-id="cfa18-312">Обновление примеров New-AzResourceLock.md (12806)</span><span class="sxs-lookup"><span data-stu-id="cfa18-312">Update New-AzResourceLock.md examples (#12806)</span></span>
* <span data-ttu-id="cfa18-313">Эрагон Риддл (Eragon Riddle) (@eragonriddle), исправлено имя поля параметра в примере (12825)</span><span class="sxs-lookup"><span data-stu-id="cfa18-313">Eragon Riddle (@eragonriddle), Corrected parameter field name in the example (#12825)</span></span> 
* <span data-ttu-id="cfa18-314">@rossifumax, исправление опечатки в New-AzConfigurationAssignment.md (12701)</span><span class="sxs-lookup"><span data-stu-id="cfa18-314">@rossifumax, Fix typo in New-AzConfigurationAssignment.md (#12701)</span></span>

## <a name="461---august-2020"></a><span data-ttu-id="cfa18-315">4.6.1 — август 2020 г.</span><span class="sxs-lookup"><span data-stu-id="cfa18-315">4.6.1 - August 2020</span></span>
#### <a name="azcompute"></a><span data-ttu-id="cfa18-316">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cfa18-316">Az.Compute</span></span>
* <span data-ttu-id="cfa18-317">Исправлен параметр -EncryptionAtHost в New-AzVm для удаления значения false по умолчанию [№ 12776].</span><span class="sxs-lookup"><span data-stu-id="cfa18-317">Patched '-EncryptionAtHost' parameter in 'New-AzVm' to remove default value of false [#12776]</span></span>

## <a name="460---august-2020"></a><span data-ttu-id="cfa18-318">4.6.0 — август 2020 г.</span><span class="sxs-lookup"><span data-stu-id="cfa18-318">4.6.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cfa18-319">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cfa18-319">Az.Accounts</span></span>
* <span data-ttu-id="cfa18-320">Загружаются все общедоступные облачные среды, когда конечная точка обнаружения не возвращает AzureCloud по умолчанию или другие общедоступные среды [№ 12633]</span><span class="sxs-lookup"><span data-stu-id="cfa18-320">Loaded all public cloud environments when discovery endpoint doesn't return default AzureCloud or other public environments [#12633]</span></span>
* <span data-ttu-id="cfa18-321">В Get-AzSubscription предоставлен параметр SubscriptionPolicies [№ 12551].</span><span class="sxs-lookup"><span data-stu-id="cfa18-321">Exposed SubscriptionPolicies in 'Get-AzSubscription' [#12551]</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cfa18-322">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cfa18-322">Az.Automation</span></span>
* <span data-ttu-id="cfa18-323">В Set-AzAutomationWebhook добавлен параметр -RunOn для определения группы гибридной рабочей роли.</span><span class="sxs-lookup"><span data-stu-id="cfa18-323">Added '-RunOn' parameters to 'Set-AzAutomationWebhook' to specify a Hybrid Worker Group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cfa18-324">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cfa18-324">Az.Compute</span></span>
* <span data-ttu-id="cfa18-325">В New-AzVm, New-AzVmss, New-AzVMConfig, New-AzVmssConfig, Update-AzVM и Update-AzVmss добавлен параметр -EncryptionAtHost.</span><span class="sxs-lookup"><span data-stu-id="cfa18-325">Added '-EncryptionAtHost' parameter to 'New-AzVm', 'New-AzVmss', 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVM', and 'Update-AzVmss'</span></span>
* <span data-ttu-id="cfa18-326">В возвращаемый объект Get-AzVM и Get-AzVmss добавлен параметр SecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="cfa18-326">Added 'SecurityProfile' to 'Get-AzVM' and 'Get-AzVmss' return object</span></span>
* <span data-ttu-id="cfa18-327">В Get-AzHostGroup добавлен необязательный параметр -InstanceView.</span><span class="sxs-lookup"><span data-stu-id="cfa18-327">Added '-InstanceView' switch as optional parameter to 'Get-AzHostGroup'</span></span>
* <span data-ttu-id="cfa18-328">Добавлен новый командлет Invoke-AzVmPatchAssessment.</span><span class="sxs-lookup"><span data-stu-id="cfa18-328">Added new cmdlet 'Invoke-AzVmPatchAssessment'</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cfa18-329">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cfa18-329">Az.DataFactory</span></span>
* <span data-ttu-id="cfa18-330">В класс PSPipelineRun добавлены отсутствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="cfa18-330">Added missing properties to PSPipelineRun class.</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="cfa18-331">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cfa18-331">Az.HDInsight</span></span>
* <span data-ttu-id="cfa18-332">Включена поддержка создания кластера с функцией шифрования на узле.</span><span class="sxs-lookup"><span data-stu-id="cfa18-332">Supported creating cluster with encryption at host feature.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cfa18-333">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cfa18-333">Az.KeyVault</span></span>
* <span data-ttu-id="cfa18-334">Добавлены предупреждающие сообщения для планирования отключения обратимого удаления.</span><span class="sxs-lookup"><span data-stu-id="cfa18-334">Added warning messages for planning to disable soft delete</span></span>
* <span data-ttu-id="cfa18-335">Добавлены предупреждающие сообщения для планирования удаления атрибута SecretValueText.</span><span class="sxs-lookup"><span data-stu-id="cfa18-335">Added warning messages for planning to remove attribute SecretValueText</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="cfa18-336">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="cfa18-336">Az.Maintenance</span></span>
* <span data-ttu-id="cfa18-337">В New-AzMaintenanceConfiguration добавлены дополнительные поля, связанные с расписанием.</span><span class="sxs-lookup"><span data-stu-id="cfa18-337">Added optional schedule related fields to 'New-AzMaintenanceConfiguration'</span></span>
* <span data-ttu-id="cfa18-338">Добавлен новый командлет для Get-AzMaintenancePublicConfiguration.</span><span class="sxs-lookup"><span data-stu-id="cfa18-338">Added new cmdlet for 'Get-AzMaintenancePublicConfiguration'</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="cfa18-339">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="cfa18-339">Az.ManagedServices</span></span>
* <span data-ttu-id="cfa18-340">Добавлены предупреждения о критических изменениях в командлетах назначения и определения управляемых служб.</span><span class="sxs-lookup"><span data-stu-id="cfa18-340">Added breaking change warnings on cmdlets of managed services assignment and definition</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cfa18-341">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cfa18-341">Az.Monitor</span></span>
* <span data-ttu-id="cfa18-342">Расширен набор параметров, заданный в Set-AzDiagnosticSetting, для разделения включения журналов и метрик [№ 12482].</span><span class="sxs-lookup"><span data-stu-id="cfa18-342">Extended the parameter set in 'Set-AzDiagnosticSetting' for separation of Logs and Metrics enablement [#12482]</span></span>
* <span data-ttu-id="cfa18-343">Для Add-AzMetricAlertRuleV2 исправлена ошибка, возникающая при получении оповещения метрики из конвейера.</span><span class="sxs-lookup"><span data-stu-id="cfa18-343">Fixed bug for 'Add-AzMetricAlertRuleV2' when getting metric alert from pipeline</span></span>

#### <a name="azresources"></a><span data-ttu-id="cfa18-344">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cfa18-344">Az.Resources</span></span>
* <span data-ttu-id="cfa18-345">Изменен ответ Get-AzPolicyAlias для включения сведений о том, изменяется ли этот псевдоним Политикой Azure.</span><span class="sxs-lookup"><span data-stu-id="cfa18-345">Updated 'Get-AzPolicyAlias' response to include information indicating whether the alias is modifiable by Azure Policy.</span></span>
* <span data-ttu-id="cfa18-346">Создан новый командлет Set-AzRoleAssignment.</span><span class="sxs-lookup"><span data-stu-id="cfa18-346">Created new cmdlet 'Set-AzRoleAssignment'</span></span>
* <span data-ttu-id="cfa18-347">Добавлен командлет Get-AzDeploymentManagementGroupWhatIfResult для получения результатов выполнения What-If в шаблоне ARM в области группы управления.</span><span class="sxs-lookup"><span data-stu-id="cfa18-347">Added 'Get-AzDeploymentManagementGroupWhatIfResult' for getting ARM template What-If results at management Group scope</span></span>
* <span data-ttu-id="cfa18-348">Добавлен командлет Get-AzTenantWhatIfResult для получения результатов выполнения What-If в шаблоне ARM в области арендатора.</span><span class="sxs-lookup"><span data-stu-id="cfa18-348">Added 'Get-AzTenantWhatIfResult' new cmdlet for getting ARM template What-If results at tenant scope</span></span>
* <span data-ttu-id="cfa18-349">Переопределены параметры -WhatIf и -Confirm для New-AzManagementGroupDeployment и New-AzTenantDeployment для использования результатов выполнения What-If в шаблоне ARM.</span><span class="sxs-lookup"><span data-stu-id="cfa18-349">Overrode '-WhatIf' and '-Confirm' for 'New-AzManagementGroupDeployment' and 'New-AzTenantDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="cfa18-350">Исправлено поведение параметров -WhatIf и -Confirm для новых командлетов развертывания, чтобы они соответствовали значению False.</span><span class="sxs-lookup"><span data-stu-id="cfa18-350">Fixed the behaviors of '-WhatIf' and '-Confirm' for new deployment cmdlets so they comply with False and</span></span> 
* <span data-ttu-id="cfa18-351">Исправлена ошибка сериализации для -TemplateObject и TemplateParameterObject [№ 1528] [№ 6292].</span><span class="sxs-lookup"><span data-stu-id="cfa18-351">Fixed serialization error for '-TemplateObject' and 'TemplateParameterObject' [#1528] [#6292]</span></span>
* <span data-ttu-id="cfa18-352">Добавлен атрибут критического изменения в Get-AzResourceGroupDeploymentOperation для предстоящего изменения типа выходных данных.</span><span class="sxs-lookup"><span data-stu-id="cfa18-352">Added breaking change attribute to 'Get-AzResourceGroupDeploymentOperation' for the upcoming output type change</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="cfa18-353">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="cfa18-353">Az.SignalR</span></span>
* <span data-ttu-id="cfa18-354">Исправлены ошибки файлов справки Restart-AzSignalR и Update-AzSignalR.</span><span class="sxs-lookup"><span data-stu-id="cfa18-354">Fixed 'Restart-AzSignalR' and 'Update-AzSignalR' help files errors</span></span>
* <span data-ttu-id="cfa18-355">Добавлены командлеты Update-AzSignalRNetworkAcl, Set-AzSignalRUpstream.</span><span class="sxs-lookup"><span data-stu-id="cfa18-355">Added cmdlets 'Update-AzSignalRNetworkAcl', 'Set-AzSignalRUpstream'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cfa18-356">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cfa18-356">Az.Storage</span></span>
* <span data-ttu-id="cfa18-357">Поддерживается ускорение запросов больших двоичных объектов:</span><span class="sxs-lookup"><span data-stu-id="cfa18-357">Supported blob query acceleration</span></span>
    -  <span data-ttu-id="cfa18-358">Get-AzStorageBlobQueryResult;</span><span class="sxs-lookup"><span data-stu-id="cfa18-358">'Get-AzStorageBlobQueryResult'</span></span>
    -  <span data-ttu-id="cfa18-359">New-AzStorageBlobQueryConfig.</span><span class="sxs-lookup"><span data-stu-id="cfa18-359">'New-AzStorageBlobQueryConfig'</span></span>
* <span data-ttu-id="cfa18-360">Обновлен файл справки; дополнено описание и исправлена опечатка.</span><span class="sxs-lookup"><span data-stu-id="cfa18-360">Updated help file, added more description, and fixed typo</span></span>
    -  <span data-ttu-id="cfa18-361">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="cfa18-361">'Start-AzStorageBlobCopy'</span></span>
    -  <span data-ttu-id="cfa18-362">Get-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="cfa18-362">'Get-AzDataLakeGen2Item'</span></span>
* <span data-ttu-id="cfa18-363">Исправлена ошибка, из-за которой работа большого двоичного объекта завершается ошибкой, если связанный подкаталог не существует [№ 12592].</span><span class="sxs-lookup"><span data-stu-id="cfa18-363">Fixed download blob fail when related sub directory not exist [#12592]</span></span>
    -  <span data-ttu-id="cfa18-364">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="cfa18-364">'Get-AzStorageBlobContent'</span></span>
* <span data-ttu-id="cfa18-365">Включена поддержка задания, получения и удаления политики репликации объекта в учетных записях хранения:</span><span class="sxs-lookup"><span data-stu-id="cfa18-365">Supported Set/Get/Remove Object Replication Policy on Storage accounts</span></span>
    - <span data-ttu-id="cfa18-366">New-AzStorageObjectReplicationPolicyRule;</span><span class="sxs-lookup"><span data-stu-id="cfa18-366">'New-AzStorageObjectReplicationPolicyRule'</span></span>
    - <span data-ttu-id="cfa18-367">Set-AzStorageObjectReplicationPolicy;</span><span class="sxs-lookup"><span data-stu-id="cfa18-367">'Set-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="cfa18-368">Get-AzStorageObjectReplicationPolicy;</span><span class="sxs-lookup"><span data-stu-id="cfa18-368">'Get-AzStorageObjectReplicationPolicy'</span></span>
    - <span data-ttu-id="cfa18-369">Remove-AzStorageObjectReplicationPolicy.</span><span class="sxs-lookup"><span data-stu-id="cfa18-369">'Remove-AzStorageObjectReplicationPolicy'</span></span>
* <span data-ttu-id="cfa18-370">Включена поддержка включения и отключения канала изменений в службе BLOB-объектов учетной записи хранения:</span><span class="sxs-lookup"><span data-stu-id="cfa18-370">Supported enable/disable ChangeFeed on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="cfa18-371">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="cfa18-371">'Update-AzStorageBlobServiceProperty'</span></span>

## <a name="450---august-2020"></a><span data-ttu-id="cfa18-372">4.5.0 — август 2020 г.</span><span class="sxs-lookup"><span data-stu-id="cfa18-372">4.5.0 - August 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cfa18-373">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cfa18-373">Az.Accounts</span></span>
* <span data-ttu-id="cfa18-374">Командлет Connect-AzAccount теперь принимает параметр MaxContextPopulation (№ 9865).</span><span class="sxs-lookup"><span data-stu-id="cfa18-374">Updated 'Connect-AzAccount' to accept parameter 'MaxContextPopulation' [#9865]</span></span>
* <span data-ttu-id="cfa18-375">Версия SubscriptionClient обновлена до 2019-06-01 и поддерживает отображение доменов арендаторов (№ 9838).</span><span class="sxs-lookup"><span data-stu-id="cfa18-375">Updated SubscriptionClient version to 2019-06-01 and display tenant domains [#9838]</span></span>
* <span data-ttu-id="cfa18-376">Добавлена поддержка домашнего арендатора и сведений managedBy арендатора для подписки.</span><span class="sxs-lookup"><span data-stu-id="cfa18-376">Supported home tenant and managedBy tenant information of subscription</span></span>
* <span data-ttu-id="cfa18-377">Исправлено имя модуля и сведения о версии в данных телеметрии.</span><span class="sxs-lookup"><span data-stu-id="cfa18-377">Corrected module name, version info in telemetry data</span></span>
* <span data-ttu-id="cfa18-378">Исправлено поведение SqlDatabaseDnsSuffix и ServiceManagementUrl, когда конечная точка метаданных среды возвращает несовместимое значение.</span><span class="sxs-lookup"><span data-stu-id="cfa18-378">Adjusted SqlDatabaseDnsSuffix and ServiceManagementUrl if environment metadata endpoint returns incompatible value</span></span>

#### <a name="azaks"></a><span data-ttu-id="cfa18-379">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="cfa18-379">Az.Aks</span></span>
* <span data-ttu-id="cfa18-380">Параметр ClientIdAndSecret замен на ServicePrincipalIdAndSecret и задан в виде псевдонима (№ 12381).</span><span class="sxs-lookup"><span data-stu-id="cfa18-380">Removed 'ClientIdAndSecret' to 'ServicePrincipalIdAndSecret' and set 'ClientIdAndSecret' as an alias [#12381].</span></span>
* <span data-ttu-id="cfa18-381">Командлеты Get-AzAks, New-AzAks, Remove-AzAks, Set-AzAks заменены на Get-AzAksCluster, New-AzAksCluster, Remove-AzAksCluster, Set-AzAksCluster. Исходные командлеты заданы в виде псевдонимов (№ 12373).</span><span class="sxs-lookup"><span data-stu-id="cfa18-381">Removed 'Get-AzAks'/'New-AzAks'/'Remove-AzAks'/'Set-AzAks' to 'Get-AzAksCluster'/'New-AzAksCluster'/'Remove-AzAksCluster'/'Set-AzAksCluster' and set the original ones as alias [#12373].</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="cfa18-382">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cfa18-382">Az.ApiManagement</span></span>
* <span data-ttu-id="cfa18-383">Добавлен новый командлет Add-AzApiManagementApiToGateway.</span><span class="sxs-lookup"><span data-stu-id="cfa18-383">Added new 'Add-AzApiManagementApiToGateway' cmdlet.</span></span>
* <span data-ttu-id="cfa18-384">Добавлен новый командлет Get-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="cfa18-384">Added new 'Get-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="cfa18-385">Добавлен новый командлет Get-AzApiManagementGatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="cfa18-385">Added new 'Get-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="cfa18-386">Добавлен новый командлет Get-AzApiManagementGatewayKey.</span><span class="sxs-lookup"><span data-stu-id="cfa18-386">Added new 'Get-AzApiManagementGatewayKey' cmdlet.</span></span>
* <span data-ttu-id="cfa18-387">Добавлен новый командлет New-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="cfa18-387">Added new 'New-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="cfa18-388">Добавлен новый командлет New-AzApiManagementGatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="cfa18-388">Added new 'New-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="cfa18-389">Добавлен новый командлет New-AzApiManagementResourceLocationObject.</span><span class="sxs-lookup"><span data-stu-id="cfa18-389">Added new 'New-AzApiManagementResourceLocationObject' cmdlet.</span></span>
* <span data-ttu-id="cfa18-390">Добавлен новый командлет Remove-AzApiManagementApiFromGateway.</span><span class="sxs-lookup"><span data-stu-id="cfa18-390">Added new 'Remove-AzApiManagementApiFromGateway' cmdlet.</span></span>
* <span data-ttu-id="cfa18-391">Добавлен новый командлет Remove-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="cfa18-391">Added new 'Remove-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="cfa18-392">Добавлен новый командлет Remove-AzApiManagementGatewayHostnameConfiguration.</span><span class="sxs-lookup"><span data-stu-id="cfa18-392">Added new 'Remove-AzApiManagementGatewayHostnameConfiguration' cmdlet.</span></span>
* <span data-ttu-id="cfa18-393">Добавлен новый командлет Update-AzApiManagementGateway.</span><span class="sxs-lookup"><span data-stu-id="cfa18-393">Added new 'Update-AzApiManagementGateway' cmdlet.</span></span>
* <span data-ttu-id="cfa18-394">Добавлен новый необязательный параметр [-GatewayId] в командлет Get-AzApiManagementApi.</span><span class="sxs-lookup"><span data-stu-id="cfa18-394">Added new optional [-GatewayId] parameter to the 'Get-AzApiManagementApi' cmdlet.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cfa18-395">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cfa18-395">Az.CognitiveServices</span></span>
* <span data-ttu-id="cfa18-396">Задано явное использование действия "Отклонить" в качестве действия NetworkRules по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cfa18-396">Used 'Deny' specifically as NetworkRules default action.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="cfa18-397">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="cfa18-397">Az.FrontDoor</span></span>
* <span data-ttu-id="cfa18-398">Исправлена проблема, связанная с возникновением исключения при попытке Enum.Parse привести значение NULL к значениям перечисления Enabled или Disabled (№ 12344).</span><span class="sxs-lookup"><span data-stu-id="cfa18-398">Fixed an issue where an exception is being thrown when Enum.Parse tries to coerce a null value to an Enabled or Disabled enum values [#12344]</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="cfa18-399">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cfa18-399">Az.HDInsight</span></span>
* <span data-ttu-id="cfa18-400">Добавлена поддержка создания кластера с функцией шифрования передаваемых данных.</span><span class="sxs-lookup"><span data-stu-id="cfa18-400">Supported creating cluster with encryption in transit feature.</span></span>
    - <span data-ttu-id="cfa18-401">Добавлен новый параметр EncryptionInTransit в командлет New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="cfa18-401">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="cfa18-402">Добавлен новый параметр EncryptionInTransit в командлет New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="cfa18-402">Add new parameter 'EncryptionInTransit' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="cfa18-403">Добавлена поддержка создания кластера с функцией приватного канала:</span><span class="sxs-lookup"><span data-stu-id="cfa18-403">Supported creating cluster with private link feature:</span></span>
    - <span data-ttu-id="cfa18-404">Добавлен новый параметр PublicNetworkAccessType и OutboundPublicNetworkAccessType в командлет New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="cfa18-404">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightCluster'</span></span>
    - <span data-ttu-id="cfa18-405">Добавлен новый параметр PublicNetworkAccessType и OutboundPublicNetworkAccessType в командлет New-AzHDInsightClusterConfig.</span><span class="sxs-lookup"><span data-stu-id="cfa18-405">Add new parameter 'PublicNetworkAccessType' and 'OutboundPublicNetworkAccessType' to the cmdlet 'New-AzHDInsightClusterConfig'</span></span>
* <span data-ttu-id="cfa18-406">Реализовано возвращение сведений о виртуальной сети при вызове New-AzHDInsightCluster или Get-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="cfa18-406">Returned virtual network information when calling 'New-AzHDInsightCluster' or 'Get-AzHDInsightCluster'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cfa18-407">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cfa18-407">Az.Network</span></span>
* <span data-ttu-id="cfa18-408">Включена поддержка параметра AddressPrefixType в Remove-AzExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="cfa18-408">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="cfa18-409">Реализованы некритические изменения: функциональность PeerAddressType для частного пиринга в Remove-AzExpressRouteCircutPeeringConfig.</span><span class="sxs-lookup"><span data-stu-id="cfa18-409">Added non-breaking changes: PeerAddressType functionality for Private Peering in 'Remove-AzExpressRouteCircutPeeringConfig'.</span></span>
* <span data-ttu-id="cfa18-410">Код изменен для игнорирования регистра в параметрах AddressPrefixType и PeerAddressType.</span><span class="sxs-lookup"><span data-stu-id="cfa18-410">Code changed to ignore case for AddressPrefixType and PeerAddressType parameter.</span></span>
* <span data-ttu-id="cfa18-411">Изменено сообщение с предупреждением для New-AzLoadBalancerFrontendIpConfig, New-AzPublicIpAddress и New-AzPublicIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="cfa18-411">Modified the warning message for 'New-AzLoadBalancerFrontendIpConfig', 'New-AzPublicIpAddress' and 'New-AzPublicIpPrefix'.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="cfa18-412">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cfa18-412">Az.OperationalInsights</span></span>
* <span data-ttu-id="cfa18-413">Добавлен параметр -ForceDelete для Remove-AzOperationalInsightsworkspace.</span><span class="sxs-lookup"><span data-stu-id="cfa18-413">Added '-ForceDelete' option for 'Remove-AzOperationalInsightsworkspace'</span></span>
* <span data-ttu-id="cfa18-414">Добавлен новый командлет Get-AzOperationalInsightsDeletedWorkspace.</span><span class="sxs-lookup"><span data-stu-id="cfa18-414">Added new cmdlet 'Get-AzOperationalInsightsDeletedWorkspace'</span></span>
* <span data-ttu-id="cfa18-415">Добавлен новый командлет Restore-AzOperationalInsightsWorkspace.</span><span class="sxs-lookup"><span data-stu-id="cfa18-415">Added new cmdlet 'Restore-AzOperationalInsightsWorkspace'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cfa18-416">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cfa18-416">Az.RecoveryServices</span></span>
* <span data-ttu-id="cfa18-417">Улучшена работа с обнаружением контейнеров и элементов Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="cfa18-417">Improved the Azure Backup container/item discovery experience.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cfa18-418">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cfa18-418">Az.Resources</span></span>
* <span data-ttu-id="cfa18-419">Добавлены свойства Condition, ConditionVersion и Description в New-AzRoleAssignment.</span><span class="sxs-lookup"><span data-stu-id="cfa18-419">Added properties 'Condition', 'ConditionVersion' and 'Description' to 'New-AzRoleAssignment'</span></span>
    - <span data-ttu-id="cfa18-420">Это касается всех соответствующих изменений моделей данных.</span><span class="sxs-lookup"><span data-stu-id="cfa18-420">This included all the relevant changes to the data models</span></span>

#### <a name="azsql"></a><span data-ttu-id="cfa18-421">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cfa18-421">Az.Sql</span></span>
* <span data-ttu-id="cfa18-422">Исправлена ошибка, связанная с потенциальным игнорированием регистра имени сервера в New-AzSqlServer и Set-AzSqlServer.</span><span class="sxs-lookup"><span data-stu-id="cfa18-422">Fixed potential server name case insensitive error in 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="cfa18-423">Исправлена ошибка, из-за которой возвращалось неправильное имя существующей базы данных в New-AzSqlDatabaseSecondary.</span><span class="sxs-lookup"><span data-stu-id="cfa18-423">Fixed wrong database name returned on existing database error in 'New-AzSqlDatabaseSecondary'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cfa18-424">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cfa18-424">Az.Storage</span></span>
* <span data-ttu-id="cfa18-425">Добавлена поддержка создания маркера SAS контейнера и BLOB-объекта с новым разрешением x,t.</span><span class="sxs-lookup"><span data-stu-id="cfa18-425">Supported create container/blob Sas token with new permission x,t</span></span>
    -  <span data-ttu-id="cfa18-426">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="cfa18-426">'New-AzStorageBlobSASToken'</span></span>
    -  <span data-ttu-id="cfa18-427">New-AzStorageContainerSASToken</span><span class="sxs-lookup"><span data-stu-id="cfa18-427">'New-AzStorageContainerSASToken'</span></span>
* <span data-ttu-id="cfa18-428">Добавлена поддержка создания маркера SAS учетной записи с новым разрешением x,t,f.</span><span class="sxs-lookup"><span data-stu-id="cfa18-428">Supported create account Sas token with new permission x,t,f</span></span>
    -  <span data-ttu-id="cfa18-429">New-AzStorageAccountSASToken</span><span class="sxs-lookup"><span data-stu-id="cfa18-429">'New-AzStorageAccountSASToken'</span></span>
* <span data-ttu-id="cfa18-430">Добавлена поддержка получения данных об использовании одной общей папки.</span><span class="sxs-lookup"><span data-stu-id="cfa18-430">Supported get single file share usage</span></span>
    - <span data-ttu-id="cfa18-431">Get-AzRmStorageShare</span><span class="sxs-lookup"><span data-stu-id="cfa18-431">'Get-AzRmStorageShare'</span></span>

## <a name="440---july-2020"></a><span data-ttu-id="cfa18-432">4.4.0 — июль 2020 г.</span><span class="sxs-lookup"><span data-stu-id="cfa18-432">4.4.0 - July 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cfa18-433">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cfa18-433">Az.Accounts</span></span>
* <span data-ttu-id="cfa18-434">Добавлен новый командлет Invoke-AzRestMethod.</span><span class="sxs-lookup"><span data-stu-id="cfa18-434">Added new cmdlet 'Invoke-AzRestMethod'</span></span>
* <span data-ttu-id="cfa18-435">Устранена неполадка, из-за которой могли возникать ошибки с проверкой подлинности в сценариях с несколькими процессами, такими как выполнение нескольких командлетов Azure PowerShell с помощью Start-Job [№ 9448].</span><span class="sxs-lookup"><span data-stu-id="cfa18-435">Fixed an issue that may cause authentication errors in multi-process scenarios such as running multiple Azure PowerShell cmdlets using 'Start-Job' [#9448]</span></span>

#### <a name="azaks"></a><span data-ttu-id="cfa18-436">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="cfa18-436">Az.Aks</span></span>
* <span data-ttu-id="cfa18-437">Исправлена ошибка, из-за которой Get-AzAks выводит не все кластеры [ №12296].</span><span class="sxs-lookup"><span data-stu-id="cfa18-437">Fixed bug 'Get-AzAks' doesn't get all clusters [#12296]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="cfa18-438">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="cfa18-438">Az.AnalysisServices</span></span>
* <span data-ttu-id="cfa18-439">Удалена ссылка на проект для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="cfa18-439">Removed project reference to Authentication</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cfa18-440">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cfa18-440">Az.Automation</span></span>
* <span data-ttu-id="cfa18-441">Исправлена ошибка, из-за которой строка с escape-символами не преобразовывалась в объект JSON.</span><span class="sxs-lookup"><span data-stu-id="cfa18-441">Fixed the issue that string with escape chars cannot be converted into json object.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cfa18-442">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cfa18-442">Az.Compute</span></span>
* <span data-ttu-id="cfa18-443">Добавлено предупреждение, которое отображается при использовании New-AzVmss, если версия образа не является последней.</span><span class="sxs-lookup"><span data-stu-id="cfa18-443">Added warning when using 'New-AzVmss' without 'latest' image version</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cfa18-444">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cfa18-444">Az.DataFactory</span></span>
* <span data-ttu-id="cfa18-445">Добавлены глобальные параметры в Фабрику данных.</span><span class="sxs-lookup"><span data-stu-id="cfa18-445">Added global parameters to Data Factory.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="cfa18-446">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="cfa18-446">Az.EventGrid</span></span>
* <span data-ttu-id="cfa18-447">Обновлен модуль для использования API версии 2020-06-01.</span><span class="sxs-lookup"><span data-stu-id="cfa18-447">Updated to use the 2020-06-01 API version.</span></span>
* <span data-ttu-id="cfa18-448">Добавлены новые возможности:</span><span class="sxs-lookup"><span data-stu-id="cfa18-448">Added new features:</span></span>
    - <span data-ttu-id="cfa18-449">сопоставление входных данных;</span><span class="sxs-lookup"><span data-stu-id="cfa18-449">Input mapping</span></span>
    - <span data-ttu-id="cfa18-450">схема доставки событий;</span><span class="sxs-lookup"><span data-stu-id="cfa18-450">Event Delivery Schema</span></span>
    - <span data-ttu-id="cfa18-451">Приватный канал</span><span class="sxs-lookup"><span data-stu-id="cfa18-451">Private Link</span></span>
    - <span data-ttu-id="cfa18-452">схема событий облака (версия 1.0);</span><span class="sxs-lookup"><span data-stu-id="cfa18-452">Cloud Event V10 Schema</span></span>
    - <span data-ttu-id="cfa18-453">раздел служебной шины как назначение;</span><span class="sxs-lookup"><span data-stu-id="cfa18-453">Service Bus Topic As Destination</span></span>
    - <span data-ttu-id="cfa18-454">функция Azure как назначение;</span><span class="sxs-lookup"><span data-stu-id="cfa18-454">Azure Function As Destination</span></span>
    - <span data-ttu-id="cfa18-455">пакетная обработка данных веб-перехватчика;</span><span class="sxs-lookup"><span data-stu-id="cfa18-455">WebHook Batching</span></span>
    - <span data-ttu-id="cfa18-456">безопасный веб-перехватчик (поддержка AAD);</span><span class="sxs-lookup"><span data-stu-id="cfa18-456">Secure webhook (AAD support)</span></span>
    - <span data-ttu-id="cfa18-457">фильтрация IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="cfa18-457">IpFiltering</span></span>
* <span data-ttu-id="cfa18-458">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="cfa18-458">Updated cmdlets:</span></span>
    - <span data-ttu-id="cfa18-459">New-AzEventGridSubscription или Update-AzEventGridSubscription:</span><span class="sxs-lookup"><span data-stu-id="cfa18-459">'New-AzEventGridSubscription'/'Update-AzEventGridSubscription':</span></span>
        - <span data-ttu-id="cfa18-460">Добавлены новые необязательные параметры для поддержки пакетной обработки данных веб-перехватчика.</span><span class="sxs-lookup"><span data-stu-id="cfa18-460">Add new optional parameters to support webhook batching.</span></span>
        - <span data-ttu-id="cfa18-461">Добавлены новые необязательные параметры для поддержки безопасного веб-перехватчика с использованием AAD.</span><span class="sxs-lookup"><span data-stu-id="cfa18-461">Add new optional parameters to support secured webhook using AAD.</span></span>
        - <span data-ttu-id="cfa18-462">Добавлено новое перечисление для параметра EndpointType, чтобы обеспечить поддержку функции Azure и раздела служебной шины в качестве назначения.</span><span class="sxs-lookup"><span data-stu-id="cfa18-462">Add new enum for EndpointType parameter to support azure function and service bus topic as new destinations.</span></span>
        - <span data-ttu-id="cfa18-463">Добавлен новый необязательный параметр для схемы доставки.</span><span class="sxs-lookup"><span data-stu-id="cfa18-463">Add new optional parameter for delivery schema.</span></span>
    - <span data-ttu-id="cfa18-464">New-AzEventGridTopic или Update-AzEventGridTopic и New-AzEventGridDomain или Update-AzEventGridDomain:</span><span class="sxs-lookup"><span data-stu-id="cfa18-464">'New-AzEventGridTopic'/'Update-AzEventGridTopic' and 'New-AzEventGridDomain'/'Update-AzEventGridDomain':</span></span>
        - <span data-ttu-id="cfa18-465">Добавлены новые необязательные параметры для поддержки фильтрации IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="cfa18-465">Add new optional parameters to support IpFiltering.</span></span>
    - <span data-ttu-id="cfa18-466">New-AzEventGridTopic или New-AzEventGridDomain:</span><span class="sxs-lookup"><span data-stu-id="cfa18-466">'New-AzEventGridTopic'/'New-AzEventGridDomain':</span></span>
        - <span data-ttu-id="cfa18-467">Добавлены новые необязательные параметры для поддержки сопоставления входных данных.</span><span class="sxs-lookup"><span data-stu-id="cfa18-467">Add new optional parameters to support Input mapping.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="cfa18-468">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="cfa18-468">Az.FrontDoor</span></span>
* <span data-ttu-id="cfa18-469">Обновлен модуль для использования API версии 2020-05-01.</span><span class="sxs-lookup"><span data-stu-id="cfa18-469">Updated module to use API 2020-05-01</span></span>
* <span data-ttu-id="cfa18-470">Включена поддержка Приватного канала для ресурсов службы хранилища, Key Vault и службы веб-приложений.</span><span class="sxs-lookup"><span data-stu-id="cfa18-470">Added Private link support for Storage, Keyvault and Web App Service resources</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="cfa18-471">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cfa18-471">Az.HDInsight</span></span>
* <span data-ttu-id="cfa18-472">Включена поддержка создания кластера с хранилищем ADLS 1-го и 2-го поколения в национальных облаках.</span><span class="sxs-lookup"><span data-stu-id="cfa18-472">Supported creating cluster with ADLSGen1/2 storage in national clouds.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cfa18-473">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cfa18-473">Az.Monitor</span></span>
* <span data-ttu-id="cfa18-474">Исправлена ошибка с Get-AzDiagnosticSetting, связанная с присвоением значения NULL метрикам или журналам [№ 12272].</span><span class="sxs-lookup"><span data-stu-id="cfa18-474">Fixed bug for 'Get-AzDiagnosticSetting' when metrics or logs are null [#12272]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cfa18-475">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cfa18-475">Az.Network</span></span>
* <span data-ttu-id="cfa18-476">Исправлены ошибки с переключением параметров для подключения виртуальной сети концентратора к глобальной виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="cfa18-476">Fixed parameters swap in VWan HubVnet connection</span></span>
* <span data-ttu-id="cfa18-477">Добавлены новые командлеты для сайтов сетевых виртуальных модулей Azure.</span><span class="sxs-lookup"><span data-stu-id="cfa18-477">Added new cmdlets for Azure Network Virtual Appliance Sites</span></span>
    - <span data-ttu-id="cfa18-478">Get-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="cfa18-478">'Get-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="cfa18-479">New-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="cfa18-479">'New-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="cfa18-480">Remove-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="cfa18-480">'Remove-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="cfa18-481">Update-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="cfa18-481">'Update-AzVirtualApplianceSite'</span></span>
    - <span data-ttu-id="cfa18-482">New-AzOffice365PolicyProperty</span><span class="sxs-lookup"><span data-stu-id="cfa18-482">'New-AzOffice365PolicyProperty'</span></span>
* <span data-ttu-id="cfa18-483">Добавлены новые командлеты для сетевого виртуального модуля Azure.</span><span class="sxs-lookup"><span data-stu-id="cfa18-483">Added new cmdlets for Azure Network Virtual Appliance</span></span>
    - <span data-ttu-id="cfa18-484">Get-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="cfa18-484">'Get-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="cfa18-485">New-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="cfa18-485">'New-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="cfa18-486">Remove-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="cfa18-486">'Remove-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="cfa18-487">Update-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="cfa18-487">'Update-AzNetworkVirtualAppliance'</span></span>
    - <span data-ttu-id="cfa18-488">Get-AzNetworkVirtualApplianceSku</span><span class="sxs-lookup"><span data-stu-id="cfa18-488">'Get-AzNetworkVirtualApplianceSku'</span></span>
    - <span data-ttu-id="cfa18-489">New-AzVirtualApplianceSkuProperty</span><span class="sxs-lookup"><span data-stu-id="cfa18-489">'New-AzVirtualApplianceSkuProperty'</span></span>
* <span data-ttu-id="cfa18-490">Общие командлеты для Шлюза приложений, подключенного к Приватному каналу.</span><span class="sxs-lookup"><span data-stu-id="cfa18-490">Onboarded Application Gateway to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="cfa18-491">Общие командлеты для службы синхронизации хранилища, подключенной к Приватному каналу.</span><span class="sxs-lookup"><span data-stu-id="cfa18-491">Onboarded StorageSync to Private Link Common Cmdlets</span></span>
* <span data-ttu-id="cfa18-492">Общие командлеты для службы SignalR, подключенной к Приватному каналу.</span><span class="sxs-lookup"><span data-stu-id="cfa18-492">Onboarded SignalR to Private Link Common Cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cfa18-493">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cfa18-493">Az.RecoveryServices</span></span>
* <span data-ttu-id="cfa18-494">Удалена ссылка на проект для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="cfa18-494">Removed project reference to Authentication</span></span>
* <span data-ttu-id="cfa18-495">В Azure Backup представлена более точная справка по командлетам.</span><span class="sxs-lookup"><span data-stu-id="cfa18-495">Azure Backup tuned cmdlets help text to be more accurate.</span></span>
* <span data-ttu-id="cfa18-496">В Azure Backup включена поддержка выборки заданий агента MAB с помощью командлета Get-AzRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="cfa18-496">Azure Backup added support for fetching MAB agent jobs using 'Get-AzRecoveryServicesBackupJob' cmdlet.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cfa18-497">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cfa18-497">Az.Resources</span></span>
* <span data-ttu-id="cfa18-498">Обновлен командлет Save-AzResourceGroupDeploymentTemplate для использования пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="cfa18-498">Updated 'Save-AzResourceGroupDeploymentTemplate' to use the SDK.</span></span>
* <span data-ttu-id="cfa18-499">Добавлен командлет Unregister-AzResourceProvider.</span><span class="sxs-lookup"><span data-stu-id="cfa18-499">Added 'Unregister-AzResourceProvider' cmdlet.</span></span>

#### <a name="azsql"></a><span data-ttu-id="cfa18-500">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cfa18-500">Az.Sql</span></span>
* <span data-ttu-id="cfa18-501">Включена поддержка субъекта-службы и гостевых пользователей для командлета Set-AzSqlInstanceActiveDirectoryAdministrator.</span><span class="sxs-lookup"><span data-stu-id="cfa18-501">Added support for Service principal and guest users in Set-AzSqlInstanceActiveDirectoryAdministrator cmdlet'</span></span>
* <span data-ttu-id="cfa18-502">Исправлена ошибка в командлетах классификации данных.</span><span class="sxs-lookup"><span data-stu-id="cfa18-502">Fixed a bug in Data Classification cmdlets.'</span></span>
* <span data-ttu-id="cfa18-503">Включена поддержка отработки отказа Управляемого экземпляра SQL Azure. Invoke-AzSqlInstanceFailover</span><span class="sxs-lookup"><span data-stu-id="cfa18-503">Added support for Azure SQL Managed Instance failover: 'Invoke-AzSqlInstanceFailover'</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cfa18-504">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cfa18-504">Az.Storage</span></span>
* <span data-ttu-id="cfa18-505">Исправлена ошибка, из-за которой в некоторых командлетах плоскости данных не добавлялся объект UserAgent.</span><span class="sxs-lookup"><span data-stu-id="cfa18-505">Fixed the issue that UserAgent is not added for some data plane cmdlets.</span></span>
* <span data-ttu-id="cfa18-506">Включена поддержка создания и обновления учетной записи хранения с использованием MinimumTlsVersion и AllowBlobPublicAccess.</span><span class="sxs-lookup"><span data-stu-id="cfa18-506">Supported create/update Storage account with MinimumTlsVersion and AllowBlobPublicAccess</span></span>
    -  <span data-ttu-id="cfa18-507">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cfa18-507">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="cfa18-508">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cfa18-508">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="cfa18-509">Включена поддержка включения и отключения управления версиями в службе BLOB-объектов учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="cfa18-509">Support enable/disable versioning on Blob Service of a Storage account</span></span>
    - <span data-ttu-id="cfa18-510">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="cfa18-510">'Update-AzStorageBlobServiceProperty'</span></span>
* <span data-ttu-id="cfa18-511">Включена поддержка вывода списка BLOB-объектов с данными о версиях BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="cfa18-511">Support list blobs with blob versions</span></span>
    - <span data-ttu-id="cfa18-512">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="cfa18-512">'Get-AzStorageBlob'</span></span>
* <span data-ttu-id="cfa18-513">Включена поддержка получения или удаления одного моментального снимка BLOB-объекта или версии BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="cfa18-513">Support get/remove single blob snapshot or blob version</span></span>
    - <span data-ttu-id="cfa18-514">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="cfa18-514">'Get-AzStorageBlob'</span></span>
    - <span data-ttu-id="cfa18-515">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="cfa18-515">'Remove-AzStorageBlob'</span></span>
* <span data-ttu-id="cfa18-516">Включена поддержка конвейера на основе BLOB-объекта, созданного с помощью Azure.Storage.Blobs версии 12.</span><span class="sxs-lookup"><span data-stu-id="cfa18-516">Support pipeline from blob object generated from Azure.Storage.Blobs V12</span></span>
    - <span data-ttu-id="cfa18-517">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="cfa18-517">'Get-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="cfa18-518">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="cfa18-518">'New-AzStorageBlobSASToken'</span></span>
    - <span data-ttu-id="cfa18-519">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="cfa18-519">'Remove-AzStorageBlob'</span></span>
    - <span data-ttu-id="cfa18-520">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="cfa18-520">'Set-AzStorageBlobContent'</span></span>
    - <span data-ttu-id="cfa18-521">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="cfa18-521">'Start-AzStorageBlobCopy'</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="cfa18-522">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="cfa18-522">Az.StorageSync</span></span>
* <span data-ttu-id="cfa18-523">Добавлена новая версия пакета SDK StorageSync, предназначенная для API версии 2020-03-01.</span><span class="sxs-lookup"><span data-stu-id="cfa18-523">Added a new version StorageSync SDK targeting ApiVersion 2020-03-01</span></span>
* <span data-ttu-id="cfa18-524">Добавлен командлет для обновления службы синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="cfa18-524">Added Update Storage Sync Service cmdlet</span></span>
    - <span data-ttu-id="cfa18-525">Set-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="cfa18-525">'Set-AzStorageSyncService'</span></span>
* <span data-ttu-id="cfa18-526">Добавлены классы IncomingTrafficPolicy и IncomingTrafficPolicy в командлеты службы синхронизации хранилища.</span><span class="sxs-lookup"><span data-stu-id="cfa18-526">Added IncomingTrafficPolicy and PrivateEndpointConnections to StorageSyncService cmdlets.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cfa18-527">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cfa18-527">Az.Websites</span></span>
* <span data-ttu-id="cfa18-528">Включена поддержка выполнения операций для слотов, которые находятся не в той же группе ресурсов, что и план службы приложений.</span><span class="sxs-lookup"><span data-stu-id="cfa18-528">Added support to perform operations for Slots not in the same resource group as the App Service Plan</span></span>

## <a name="430---june-2020"></a><span data-ttu-id="cfa18-529">4.3.0 — июнь 2020 года</span><span class="sxs-lookup"><span data-stu-id="cfa18-529">4.3.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cfa18-530">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cfa18-530">Az.Accounts</span></span>
* <span data-ttu-id="cfa18-531">Включена поддержка обнаружения параметров среды по умолчанию и добавления окружения с помощью командлета Add-AzEnvironment.</span><span class="sxs-lookup"><span data-stu-id="cfa18-531">Supported discovering environment setting by default and adding environment via 'Add-AzEnvironment'</span></span>
* <span data-ttu-id="cfa18-532">Обновлены предварительно загруженные сборки [№ 12024], [№ 11976].</span><span class="sxs-lookup"><span data-stu-id="cfa18-532">Update preloaded assemblies [#12024], [#11976]</span></span>
* <span data-ttu-id="cfa18-533">Обновлена сборка Azure.Core.</span><span class="sxs-lookup"><span data-stu-id="cfa18-533">Updated Azure.Core assembly</span></span>
* <span data-ttu-id="cfa18-534">Исправлена ошибка, из-за которой выполнение Connect-AzAccount может завершаться сбоем при многопоточном выполнении [№ 11201].</span><span class="sxs-lookup"><span data-stu-id="cfa18-534">Fixed an issue that may cause 'Connect-AzAccount' to fail in multi-threaded execution [#11201]</span></span>

#### <a name="azaks"></a><span data-ttu-id="cfa18-535">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="cfa18-535">Az.Aks</span></span>
* <span data-ttu-id="cfa18-536">Заменено использование старого [API AccessProfile](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) вызовами API [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) и [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials).</span><span class="sxs-lookup"><span data-stu-id="cfa18-536">Replaced usage of old [AccessProfile API](https://docs.microsoft.com/rest/api/aks/managedclusters/getaccessprofile) with calls to [ListClusterAdmin](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusteradmincredentials) and [ListClusterUser](https://docs.microsoft.com/rest/api/aks/managedclusters/listclusterusercredentials) APIs</span></span>

#### <a name="azbatch"></a><span data-ttu-id="cfa18-537">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="cfa18-537">Az.Batch</span></span>
* <span data-ttu-id="cfa18-538">Изменена версия SDK для Microsoft.Azure.Management.Batch для Az.Batch на 11.0.0.</span><span class="sxs-lookup"><span data-stu-id="cfa18-538">Updated Az.Batch to use 'Microsoft.Azure.Management.Batch' SDK version to 11.0.0</span></span>
* <span data-ttu-id="cfa18-539">Включена возможность задать удостоверение BatchAccount в командлете New-AzBatchAccount.</span><span class="sxs-lookup"><span data-stu-id="cfa18-539">Added the ability to set the BatchAccount Identity in the 'New-AzBatchAccount' cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cfa18-540">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cfa18-540">Az.CognitiveServices</span></span>
* <span data-ttu-id="cfa18-541">Включена поддержка отображения возможностей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="cfa18-541">Supported displaying account capabilities.</span></span>
* <span data-ttu-id="cfa18-542">Включена поддержка изменения PublicNetworkAccess.</span><span class="sxs-lookup"><span data-stu-id="cfa18-542">Supported modifying PublicNetworkAccess.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cfa18-543">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cfa18-543">Az.Compute</span></span>
* <span data-ttu-id="cfa18-544">Добавлен параметр SimulateEviction в командлеты Set-AzVM и Set-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="cfa18-544">Added SimulateEviction parameter to Set-AzVM and Set-AzVmssVM cmdlets.</span></span>
* <span data-ttu-id="cfa18-545">Добавлен фрагмент Premium_LRS в средство заполнения аргументов параметра StorageAccountType для командлета New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="cfa18-545">Added 'Premium_LRS' to the argument completer of StorageAccountType parameter for New-AzGalleryImageVersion cmdlet.</span></span>
* <span data-ttu-id="cfa18-546">Добавлены подсостояния для VMCustomScriptExtension [№ 11297].</span><span class="sxs-lookup"><span data-stu-id="cfa18-546">Added Substatuses to VMCustomScriptExtension [#11297]</span></span>
* <span data-ttu-id="cfa18-547">Добавлен фрагмент Delete в средство заполнения аргументов параметра EvictionPolicy для командлетов New-AzVM и New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="cfa18-547">Added 'Delete' to the argument completer of EvictionPolicy parameter for New-AzVM and New-AzVMConfig cmdlets.</span></span>
* <span data-ttu-id="cfa18-548">Исправлено имя нового расширения виртуальной машины для SAP.</span><span class="sxs-lookup"><span data-stu-id="cfa18-548">Fixed name of new VM Extension for SAP</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cfa18-549">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cfa18-549">Az.DataFactory</span></span>
* <span data-ttu-id="cfa18-550">Обновлен пакет SDK ADF для .NET до версии 4.9.0.</span><span class="sxs-lookup"><span data-stu-id="cfa18-550">Updated ADF .Net SDK version to 4.9.0</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="cfa18-551">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="cfa18-551">Az.EventHub</span></span>
* <span data-ttu-id="cfa18-552">Добавлены параметры управляемого удостоверения для командлетов New-AzEventHubNamespace и Set-AzEventHubNamespace.</span><span class="sxs-lookup"><span data-stu-id="cfa18-552">Added Managed Identity parameters to 'New-AzEventHubNamespace' and 'Set-AzEventHubNamespace' cmdlets</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="cfa18-553">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="cfa18-553">Az.Functions</span></span>
* <span data-ttu-id="cfa18-554">Включена поддержка создания приложений-функций PowerShell 7.0 и Java 11.</span><span class="sxs-lookup"><span data-stu-id="cfa18-554">Added support to create PowerShell 7.0 and Java 11 function apps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="cfa18-555">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cfa18-555">Az.HDInsight</span></span>
* <span data-ttu-id="cfa18-556">Включена поддержка перечисления узлов и перезагрузка отдельных узлов кластера HDInsight.</span><span class="sxs-lookup"><span data-stu-id="cfa18-556">Supported listing hosts and restart specific hosts of the HDInsight cluster.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="cfa18-557">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="cfa18-557">Az.HealthcareApis</span></span>
* <span data-ttu-id="cfa18-558">Обновлен пакет SDK до версии 1.1.0.</span><span class="sxs-lookup"><span data-stu-id="cfa18-558">Updated the SDK version to 1.1.0</span></span>
* <span data-ttu-id="cfa18-559">Включена поддержка параметров экспорта и управляемого удостоверения.</span><span class="sxs-lookup"><span data-stu-id="cfa18-559">Added support for Export settings and Managed Identity</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cfa18-560">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cfa18-560">Az.Monitor</span></span>
* <span data-ttu-id="cfa18-561">Исправлен входной параметр объекта для Set-AzActivityLogAlert.</span><span class="sxs-lookup"><span data-stu-id="cfa18-561">Fixed input object parameter for 'Set-AzActivityLogAlert'</span></span>
* <span data-ttu-id="cfa18-562">Исправлен параметр InputObject для Set-AzActionGroup [№ 10868].</span><span class="sxs-lookup"><span data-stu-id="cfa18-562">Fixed 'InputObject' parameter for 'Set-AzActionGroup' [#10868]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cfa18-563">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cfa18-563">Az.Network</span></span>
* <span data-ttu-id="cfa18-564">Включена поддержка параметра AddressPrefixType в Remove-AzExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="cfa18-564">Added support for AddressPrefixType parameter to 'Remove-AzExpressRouteCircuitConnectionConfig'</span></span>
* <span data-ttu-id="cfa18-565">Добавлены новые командлеты для политики Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="cfa18-565">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="cfa18-566">New-AzFirewallPolicyDnsSetting</span><span class="sxs-lookup"><span data-stu-id="cfa18-566">'New-AzFirewallPolicyDnsSetting'</span></span>
    - <span data-ttu-id="cfa18-567">Включена поддержка полного доменного имени назначения в правилах сети для политики брандмауэра.</span><span class="sxs-lookup"><span data-stu-id="cfa18-567">Support for Destination FQDN in Network Rules for Firewall Policy</span></span>
* <span data-ttu-id="cfa18-568">Включена поддержка операций серверного пула адресов:</span><span class="sxs-lookup"><span data-stu-id="cfa18-568">Added support for backend address pool operations</span></span>
    - <span data-ttu-id="cfa18-569">New-AzLoadBalancerBackendAddressConfig</span><span class="sxs-lookup"><span data-stu-id="cfa18-569">'New-AzLoadBalancerBackendAddressConfig'</span></span>
    - <span data-ttu-id="cfa18-570">New-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="cfa18-570">'New-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="cfa18-571">Set-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="cfa18-571">'Set-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="cfa18-572">Remove-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="cfa18-572">'Remove-AzLoadBalancerBackendAddressPool'</span></span>
    - <span data-ttu-id="cfa18-573">Get-AzLoadBalancerBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="cfa18-573">'Get-AzLoadBalancerBackendAddressPool'</span></span>
* <span data-ttu-id="cfa18-574">Добавлена проверка имени для New-AzIpGroup.</span><span class="sxs-lookup"><span data-stu-id="cfa18-574">Added name validation for 'New-AzIpGroup'</span></span>
* <span data-ttu-id="cfa18-575">Добавлены новые командлеты для политики Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="cfa18-575">Added new cmdlets for Azure FirewallPolicy</span></span>
    - <span data-ttu-id="cfa18-576">New-AzFirewallPolicyThreatIntelWhitelist</span><span class="sxs-lookup"><span data-stu-id="cfa18-576">'New-AzFirewallPolicyThreatIntelWhitelist'</span></span>
* <span data-ttu-id="cfa18-577">Обновлены следующие команды для функции: Включена возможность настройки и удаления пользовательских DNS-серверов в шлюзе VPN P2S виртуальной глобальной сети.</span><span class="sxs-lookup"><span data-stu-id="cfa18-577">Updated below commands for feature: Custom dns servers set/remove on VirtualWan P2SVpnGateway.</span></span>
    - <span data-ttu-id="cfa18-578">Обновлен командлет New-AzP2sVpnGateway: добавлен необязательный параметр -CustomDnsServer, чтобы пользователи могли указывать свои DNS-серверы для настройки в шлюзе VPN P2S для использования клиентами с подключением "точка — сеть".</span><span class="sxs-lookup"><span data-stu-id="cfa18-578">Updated New-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
    - <span data-ttu-id="cfa18-579">Обновлен командлет Update-AzP2sVpnGateway: добавлен необязательный параметр -CustomDnsServer, чтобы пользователи могли указывать свои DNS-серверы для настройки в шлюзе VPN P2S для использования клиентами с подключением "точка — сеть".</span><span class="sxs-lookup"><span data-stu-id="cfa18-579">Updated Update-AzP2sVpnGateway: Added optional parameter '-CustomDnsServer' for customers to specify their dns servers to set on P2SVpnGateway, which can be used by Point to site clients.</span></span>
* <span data-ttu-id="cfa18-580">Обновлен командлет Update-AzVpnGateway:</span><span class="sxs-lookup"><span data-stu-id="cfa18-580">Updated 'Update-AzVpnGateway'</span></span>
    - <span data-ttu-id="cfa18-581">добавлен необязательный параметр -BgpPeeringAddress, чтобы клиенты могли указывать пользовательские маршруты BGP для настройки в шлюзе VPN.</span><span class="sxs-lookup"><span data-stu-id="cfa18-581">Added optional parameter '-BgpPeeringAddress' for customers to specify their custom bgps to set on VpnGateway.</span></span>
* <span data-ttu-id="cfa18-582">Добавлен новый командлет для сброса состояния маршрутизации ресурса VirtualHub:</span><span class="sxs-lookup"><span data-stu-id="cfa18-582">Added new cmdlet to support resetting the routing state of a VirtualHub resource:</span></span>
    - <span data-ttu-id="cfa18-583">Reset-AzHubRouter</span><span class="sxs-lookup"><span data-stu-id="cfa18-583">'Reset-AzHubRouter'</span></span>
* <span data-ttu-id="cfa18-584">Следующие обновления основаны на последнем изменении Swagger для политики брандмауэра:</span><span class="sxs-lookup"><span data-stu-id="cfa18-584">Updated below things based on recent swagger change for Firewall Policy</span></span>
    - <span data-ttu-id="cfa18-585">изменены имена для RuleGroup, RuleCollectionGroup и RuleType;</span><span class="sxs-lookup"><span data-stu-id="cfa18-585">Changes names for RuleGroup, RuleCollectionGroup and RuleType</span></span>
    - <span data-ttu-id="cfa18-586">включена поддержка коллекций правил NAT политики брандмауэра для поддержки нескольких коллекций правил NAT.</span><span class="sxs-lookup"><span data-stu-id="cfa18-586">Added support for Firewall Policy NAT Rule Collections to support multiple NAT Rule Collection</span></span>
* <span data-ttu-id="cfa18-587">[Критическое изменение] Добавлен обязательный параметр SourceIpGroup для командлетов New-AzFirewallPolicyApplicationRule и New-AzFirewallPolicyNetworkRule.</span><span class="sxs-lookup"><span data-stu-id="cfa18-587">[Breaking Change] Added mandatory parameter 'SourceIpGroup' for 'New-AzFirewallPolicyApplicationRule' and 'New-AzFirewallPolicyNetworkRule'.</span></span>
* <span data-ttu-id="cfa18-588">[Критическое изменение] Параметр SourceAddress для командлета New-AzFirewallPolicyApplicationRule сделан обязательным.</span><span class="sxs-lookup"><span data-stu-id="cfa18-588">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="cfa18-589">[Критическое изменение] Параметр SourceAddress для командлета New-AzFirewallPolicyApplicationRule сделан обязательным.</span><span class="sxs-lookup"><span data-stu-id="cfa18-589">[Breaking Change] Fixed 'New-AzFirewallPolicyApplicationRule', parameter 'SourceAddress' to be mandatory.</span></span>
* <span data-ttu-id="cfa18-590">[Критическое изменение] Удалены обязательные параметры: TranslatedAddress и TranslatedPort для командлета New-AzFirewallPolicyNatRuleCollection.</span><span class="sxs-lookup"><span data-stu-id="cfa18-590">[Breaking Change] Removed mandatory parameters: 'TranslatedAddress', 'TranslatedPort' for 'New-AzFirewallPolicyNatRuleCollection'.</span></span>
* <span data-ttu-id="cfa18-591">Добавлены новые командлеты для поддержки Приватного канала в Шлюзе приложений:</span><span class="sxs-lookup"><span data-stu-id="cfa18-591">Added new cmdlets to support PrivateLink On Application Gateway</span></span>
    - <span data-ttu-id="cfa18-592">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="cfa18-592">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="cfa18-593">Get-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="cfa18-593">'Get-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="cfa18-594">New-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="cfa18-594">'New-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="cfa18-595">Set-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="cfa18-595">'Set-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="cfa18-596">Remove-AzApplicationGatewayPrivateLinkConfiguration</span><span class="sxs-lookup"><span data-stu-id="cfa18-596">'Remove-AzApplicationGatewayPrivateLinkConfiguration'</span></span>
    - <span data-ttu-id="cfa18-597">New-AzApplicationGatewayPrivateLinkIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="cfa18-597">'New-AzApplicationGatewayPrivateLinkIpConfiguration'</span></span>
* <span data-ttu-id="cfa18-598">Добавлены новые командлеты для дочернего ресурса HubRouteTables VirtualHub:</span><span class="sxs-lookup"><span data-stu-id="cfa18-598">Added new cmdlets for HubRouteTables child resource of VirtualHub.</span></span>
    - <span data-ttu-id="cfa18-599">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="cfa18-599">'New-AzVHubRoute'</span></span>
    - <span data-ttu-id="cfa18-600">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="cfa18-600">'New-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="cfa18-601">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="cfa18-601">'Get-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="cfa18-602">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="cfa18-602">'Update-AzVHubRouteTable'</span></span>
    - <span data-ttu-id="cfa18-603">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="cfa18-603">'Remove-AzVHubRouteTable'</span></span>
* <span data-ttu-id="cfa18-604">Обновлены существующие командлеты для включения поддержки необязательного входного параметра RoutingConfiguration для настраиваемой маршрутизации в виртуальной глобальной сети.</span><span class="sxs-lookup"><span data-stu-id="cfa18-604">Updated existing cmdlets to support optional RoutingConfiguration input parameter for custom routing in VirtualWan.</span></span>
    - <span data-ttu-id="cfa18-605">New-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="cfa18-605">'New-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="cfa18-606">Set-AzExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="cfa18-606">'Set-AzExpressRouteConnection'</span></span>
    - <span data-ttu-id="cfa18-607">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="cfa18-607">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="cfa18-608">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="cfa18-608">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="cfa18-609">New-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="cfa18-609">'New-AzVpnConnection'</span></span>
    - <span data-ttu-id="cfa18-610">Update-AzVpnConnection</span><span class="sxs-lookup"><span data-stu-id="cfa18-610">'Update-AzVpnConnection'</span></span>
    - <span data-ttu-id="cfa18-611">New-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="cfa18-611">'New-AzP2sVpnGateway'</span></span>
    - <span data-ttu-id="cfa18-612">Update-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="cfa18-612">'Update-AzP2sVpnGateway'</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="cfa18-613">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cfa18-613">Az.OperationalInsights</span></span>
* <span data-ttu-id="cfa18-614">Исправлена ошибка, из-за которой PSWorkspace не реализует IOperationalInsightsWorkspace [№ 12135].</span><span class="sxs-lookup"><span data-stu-id="cfa18-614">Fixed bug PSWorkspace doesn't implement IOperationalInsightsWorkspace [#12135]</span></span>
* <span data-ttu-id="cfa18-615">Добавлено значение pergb2018 в действительный набор значений параметра Sku в командлете Set-AzOperationalInsightsWorkspace.</span><span class="sxs-lookup"><span data-stu-id="cfa18-615">Added 'pergb2018' to valid value set of parameter 'Sku' in 'Set-AzOperationalInsightsWorkspace'</span></span> 
* <span data-ttu-id="cfa18-616">Добавлен псевдоним FunctionParameters для параметра FunctionParameter:</span><span class="sxs-lookup"><span data-stu-id="cfa18-616">Added alias 'FunctionParameters' for parameter 'FunctionParameter' to</span></span>
    - <span data-ttu-id="cfa18-617">New-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="cfa18-617">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="cfa18-618">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="cfa18-618">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cfa18-619">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cfa18-619">Az.RecoveryServices</span></span>
* <span data-ttu-id="cfa18-620">Включена поддержка выборки элементов MAB в Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="cfa18-620">Azure Backup added support for fetching MAB items.</span></span>
* <span data-ttu-id="cfa18-621">Включена поддержка типа диска StandardSSD_LRS в Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="cfa18-621">Azure Site Recovery supports disk type 'StandardSSD_LRS'</span></span>

#### <a name="azresources"></a><span data-ttu-id="cfa18-622">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cfa18-622">Az.Resources</span></span>
* <span data-ttu-id="cfa18-623">Добавлены параметры UsageLocation, GivenName, Surname, AccountEnabled, MailNickname, Mail для PSADUser [№ 10526], [№ 10497].</span><span class="sxs-lookup"><span data-stu-id="cfa18-623">Added 'UsageLocation', 'GivenName', 'Surname', 'AccountEnabled', 'MailNickname', 'Mail' on 'PSADUser' [#10526] [#10497]</span></span>
* <span data-ttu-id="cfa18-624">Исправлена ошибка, из-за которой параметр -Mail не работает в командлете Get-AzADUser [№ 11981].</span><span class="sxs-lookup"><span data-stu-id="cfa18-624">Fixed issue that '-Mail' doesn't work on 'Get-AzADUser' [#11981]</span></span>
* <span data-ttu-id="cfa18-625">Добавлен параметр -ExcludeChangeType в командлеты Get-AzDeploymentWhatIfResult и Get-AzResourceGroupDeploymentWhatIfResult.</span><span class="sxs-lookup"><span data-stu-id="cfa18-625">Added '-ExcludeChangeType' parameter to 'Get-AzDeploymentWhatIfResult' and 'Get-AzResourceGroupDeploymentWhatIfResult'</span></span>
* <span data-ttu-id="cfa18-626">Добавлен параметр -WhatIfExcludeChangeType в командлеты New-AzDeployment и New-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="cfa18-626">Added '-WhatIfExcludeChangeType' parameter to 'New-AzDeployment' and 'New-AzResourceGroupDeployment'</span></span>
* <span data-ttu-id="cfa18-627">Обновлены командлеты Test-Az\*Deployment для отображения улучшенных сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="cfa18-627">Updated 'Test-Az\*Deployment' cmdlets to show better error messages</span></span>
* <span data-ttu-id="cfa18-628">Исправлено справочное сообщение для параметра -Name в командлетах создания развертывания и командлетах What-If.</span><span class="sxs-lookup"><span data-stu-id="cfa18-628">Fixed help message for '-Name' parameter of deployment create and What-If cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="cfa18-629">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cfa18-629">Az.Sql</span></span>
* <span data-ttu-id="cfa18-630">Включена поддержка субъекта-службы для командлета настройки администратора Azure Active Directory SQL Server.</span><span class="sxs-lookup"><span data-stu-id="cfa18-630">Added support for service principal for Set SQL Server Azure Active Directory Admin cmdlet</span></span>
* <span data-ttu-id="cfa18-631">Исправлена ошибка синхронизации в командлетах классификации данных.</span><span class="sxs-lookup"><span data-stu-id="cfa18-631">Fixed sync issue in Data Classification cmdlets.</span></span>
* <span data-ttu-id="cfa18-632">Включена поддержка поиска пользователей по адресу электронной почты в командлете Set-AzSqlServerActiveDirectoryAdministrator [№ 12192].</span><span class="sxs-lookup"><span data-stu-id="cfa18-632">Supported searching user by mail on 'Set-AzSqlServerActiveDirectoryAdministrator' [#12192]</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cfa18-633">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cfa18-633">Az.Storage</span></span>
* <span data-ttu-id="cfa18-634">Включена поддержка создания учетной записи хранения с помощью RequireInfrastructureEncryption.</span><span class="sxs-lookup"><span data-stu-id="cfa18-634">Supported create Storage account with RequireInfrastructureEncryption</span></span>
    -  <span data-ttu-id="cfa18-635">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cfa18-635">'New-AzStorageAccount'</span></span>
* <span data-ttu-id="cfa18-636">Перемещена логика загрузки Azure.Core в Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="cfa18-636">Moved the logic of loading Azure.Core to Az.Accounts</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cfa18-637">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cfa18-637">Az.Websites</span></span>
* <span data-ttu-id="cfa18-638">В командлет Restore-AzDeletedWebApp добавлена защитная мера при удалении созданного веб-приложения, если восстановление завершилось сбоем.</span><span class="sxs-lookup"><span data-stu-id="cfa18-638">Added safeguard to delete created webapp if restore failed in 'Restore-AzDeletedWebApp'</span></span>
* <span data-ttu-id="cfa18-639">Добавлены параметры SourceWebApp.Location для командлетов New-AzWebApp и New-AzWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="cfa18-639">Added 'SourceWebApp.Location' for 'New-AzWebApp' and 'New-AzWebAppSlot'</span></span>
* <span data-ttu-id="cfa18-640">Исправлена ошибка, препятствующая изменению параметров контейнера в командлетах Set-AzWebApp и Set-AzWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="cfa18-640">Fixed bug that prevented changing Container settings in 'Set-AzWebApp' and 'Set-AzWebAppSlot'</span></span>
* <span data-ttu-id="cfa18-641">Исправлена ошибка получения SiteConfig, когда параметр -Name не указан для командлета Get-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="cfa18-641">Fixed bug to get SiteConfig when -Name is not given for Get-AzWebApp</span></span>
* <span data-ttu-id="cfa18-642">Включена поддержка создания приложений ASP для Linux.</span><span class="sxs-lookup"><span data-stu-id="cfa18-642">Added a support to create ASP for Linux Apps</span></span>
* <span data-ttu-id="cfa18-643">Добавлены исключения для клонирования в группах ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cfa18-643">Added exceptions for clone across resource groups</span></span>

## <a name="420---june-2020"></a><span data-ttu-id="cfa18-644">4.2.0 — июнь 2020 г.</span><span class="sxs-lookup"><span data-stu-id="cfa18-644">4.2.0 - June 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cfa18-645">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cfa18-645">Az.Accounts</span></span>
* <span data-ttu-id="cfa18-646">Исправлена проблема, из-за которой модуль Az мог пропускать журналы в заданиях службы автоматизации или PowerShell [№ 11492].</span><span class="sxs-lookup"><span data-stu-id="cfa18-646">Fixed an issue that may cause Az to skip logs in Azure Automation or PowerShell jobs [#11492]</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="cfa18-647">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="cfa18-647">Az.AnalysisServices</span></span>
* <span data-ttu-id="cfa18-648">Обновлена версия сборки командлетов плоскости данных.</span><span class="sxs-lookup"><span data-stu-id="cfa18-648">Updated assembly version of data plane cmdlets</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="cfa18-649">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cfa18-649">Az.ApiManagement</span></span>
* <span data-ttu-id="cfa18-650">Обновлена версия сборки командлетов управления службами.</span><span class="sxs-lookup"><span data-stu-id="cfa18-650">Updated assembly version of service management cmdlets</span></span>

#### <a name="azbilling"></a><span data-ttu-id="cfa18-651">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="cfa18-651">Az.Billing</span></span>
* <span data-ttu-id="cfa18-652">Обновлена версия сборки командлетов потребления.</span><span class="sxs-lookup"><span data-stu-id="cfa18-652">Updated assembly version of consumption cmdlets</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cfa18-653">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cfa18-653">Az.CognitiveServices</span></span>
* <span data-ttu-id="cfa18-654">Реализована поддержка элементов управления PrivateEndpoint и PublicNetworkAccess.</span><span class="sxs-lookup"><span data-stu-id="cfa18-654">Support PrivateEndpoint and PublicNetworkAccess control.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="cfa18-655">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cfa18-655">Az.DataFactory</span></span>
* <span data-ttu-id="cfa18-656">Обновлена версия сборки командлетов фабрики данных версии 2.</span><span class="sxs-lookup"><span data-stu-id="cfa18-656">Updated assembly version of data factory V2 cmdlets</span></span>

#### <a name="azdatashare"></a><span data-ttu-id="cfa18-657">Az.DataShare</span><span class="sxs-lookup"><span data-stu-id="cfa18-657">Az.DataShare</span></span>
* <span data-ttu-id="cfa18-658">Вышла общедоступная версия модуля Az.DataShare.</span><span class="sxs-lookup"><span data-stu-id="cfa18-658">General availability of ''Az.DataShare'' module</span></span>

#### <a name="azdesktopvirtualization"></a><span data-ttu-id="cfa18-659">Az.DesktopVirtualization</span><span class="sxs-lookup"><span data-stu-id="cfa18-659">Az.DesktopVirtualization</span></span>
* <span data-ttu-id="cfa18-660">Вышла общедоступная версия модуля Az.DesktopVirtualization.</span><span class="sxs-lookup"><span data-stu-id="cfa18-660">General availability of ''Az.DesktopVirtualization'' module</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="cfa18-661">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cfa18-661">Az.OperationalInsights</span></span>
* <span data-ttu-id="cfa18-662">Пакет SDK обновлен до версии 0.21.0.</span><span class="sxs-lookup"><span data-stu-id="cfa18-662">Upgraded SDK to 0.21.0</span></span>
* <span data-ttu-id="cfa18-663">Добавлены дополнительные параметры в следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="cfa18-663">Added optional parameters to</span></span> 
    - <span data-ttu-id="cfa18-664">New-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="cfa18-664">'New-AzOperationalInsightsSavedSearch'</span></span>
    - <span data-ttu-id="cfa18-665">Set-AzOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="cfa18-665">'Set-AzOperationalInsightsSavedSearch'</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="cfa18-666">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="cfa18-666">Az.PolicyInsights</span></span>
* <span data-ttu-id="cfa18-667">Исправлен пример 3 для командлета Start-AzPolicyComplianceScan.</span><span class="sxs-lookup"><span data-stu-id="cfa18-667">Corrected example 3 for 'Start-AzPolicyComplianceScan'</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="cfa18-668">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="cfa18-668">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="cfa18-669">Обновлена версия сборки командлетов PowerBI.</span><span class="sxs-lookup"><span data-stu-id="cfa18-669">Updated assembly version of PowerBI cmdlets</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="cfa18-670">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="cfa18-670">Az.PrivateDns</span></span>
* <span data-ttu-id="cfa18-671">Исправлено форматирование строки с подробными выходными данными командлета Remove-AzPrivateDnsRecordSet.</span><span class="sxs-lookup"><span data-stu-id="cfa18-671">Corrected verbose output string formatting for Remove-AzPrivateDnsRecordSet</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cfa18-672">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cfa18-672">Az.RecoveryServices</span></span>
* <span data-ttu-id="cfa18-673">Реализована поддержка Azure Site Recovery для создания плана восстановления и репликации между зонами из входного XML-файла.</span><span class="sxs-lookup"><span data-stu-id="cfa18-673">Azure Site Recovery support for creating recovery plan for zone to zone replication from xml input.</span></span>
* <span data-ttu-id="cfa18-674">Обновлена версия сборки командлетов SiteRecovery и Backup.</span><span class="sxs-lookup"><span data-stu-id="cfa18-674">Updated assembly version of SiteRecovery and Backup cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="cfa18-675">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cfa18-675">Az.Resources</span></span>
* <span data-ttu-id="cfa18-676">Добавлен параметр Tail в командлеты Get-AzDeploymentScriptLog и Save-AzDeploymentScriptLog.</span><span class="sxs-lookup"><span data-stu-id="cfa18-676">Added Tail parameter to Get-AzDeploymentScriptLog and Save-AzDeploymentScriptLog cmdlets</span></span>
* <span data-ttu-id="cfa18-677">Отформатировано свойство Output и включено в отображаемые выходные данные командлета Get-AzDeploymentScript.</span><span class="sxs-lookup"><span data-stu-id="cfa18-677">Formatted Output property and show it on the Get-AzDeploymentScript cmdlet output</span></span>
* <span data-ttu-id="cfa18-678">Параметр -DeploymentScriptInputObject переименован в -DeploymentScriptObject.</span><span class="sxs-lookup"><span data-stu-id="cfa18-678">Renamed -DeploymentScriptInputObject parameter to -DeploymentScriptObject</span></span>
* <span data-ttu-id="cfa18-679">Исправлена ошибка с отсутствующими именами файлов или целевых объектов в сообщениях командлетов.</span><span class="sxs-lookup"><span data-stu-id="cfa18-679">Fixed missing file/target name in cmdlet messages.</span></span>
* <span data-ttu-id="cfa18-680">Обновлена версия сборки командлетов диспетчера ресурсов и обработчика тегов.</span><span class="sxs-lookup"><span data-stu-id="cfa18-680">Updated assembly version of resource manager and tags cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="cfa18-681">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cfa18-681">Az.Sql</span></span>
* <span data-ttu-id="cfa18-682">Добавлен параметр UsePrivateLinkConnection в командлеты New-AzSqlSyncGroup, Update-AzSqlSyncGroup, New-AzSqlSyncMember и Update-AzSqlSyncMember.</span><span class="sxs-lookup"><span data-stu-id="cfa18-682">Added UsePrivateLinkConnection to 'New-AzSqlSyncGroup', 'Update-AzSqlSyncGroup', 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="cfa18-683">Добавлен параметр SyncMemberAzureDatabaseResourceId в командлеты New-AzSqlSyncMember и Update-AzSqlSyncMember.</span><span class="sxs-lookup"><span data-stu-id="cfa18-683">Added SyncMemberAzureDatabaseResourceId to 'New-AzSqlSyncMember' and 'Update-AzSqlSyncMember'</span></span>
* <span data-ttu-id="cfa18-684">Реализована поддержка поиска гостевых пользователей в командлете для настройки администратора Active Directory в SQL Server Azure.</span><span class="sxs-lookup"><span data-stu-id="cfa18-684">Added Guest user lookup support to Set SQL Server Azure Active Directory Admin cmdlet</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cfa18-685">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cfa18-685">Az.Storage</span></span>
* <span data-ttu-id="cfa18-686">Обновлена версия сборки командлетов плоскости данных.</span><span class="sxs-lookup"><span data-stu-id="cfa18-686">Updated assembly version of data plane cmdlets</span></span>

## <a name="410---may-2020"></a><span data-ttu-id="cfa18-687">4.1.0 — май 2020 г.</span><span class="sxs-lookup"><span data-stu-id="cfa18-687">4.1.0 - May 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="cfa18-688">Основные сведения о новых возможностях с момента последнего выпуска</span><span class="sxs-lookup"><span data-stu-id="cfa18-688">Highlights since the last release</span></span>
* <span data-ttu-id="cfa18-689">Поддерживаемые версии PowerShell: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="cfa18-689">Supported PowerShell versions: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>
* <span data-ttu-id="cfa18-690">Вышла общедоступная версия модуля Az.Functions.</span><span class="sxs-lookup"><span data-stu-id="cfa18-690">General availability of Az.Functions</span></span> 
* <span data-ttu-id="cfa18-691">Состоялся основной выпуск Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources и Az.Storage.</span><span class="sxs-lookup"><span data-stu-id="cfa18-691">Az.ApiManagement, Az.Batch, Az.Compute, Az.KeyVault, Az.Monitor, Az.Network, Az.OperationalInsights, Az.Resources, and Az.Storage have major release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="cfa18-692">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cfa18-692">Az.Accounts</span></span>
* <span data-ttu-id="cfa18-693">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment. Теперь они принимают параметры AzureSynapseAnalyticsEndpointResourceId и AzureSynapseAnalyticsEndpointSuffix.</span><span class="sxs-lookup"><span data-stu-id="cfa18-693">Updated 'Add-AzEnvironment' and 'Set-AzEnvironment' to accept parameters 'AzureSynapseAnalyticsEndpointResourceId' and 'AzureSynapseAnalyticsEndpointSuffix'</span></span>
* <span data-ttu-id="cfa18-694">В Az.Accounts добавлены сборки, связанные с Azure.Core. Добавлена поддержка Windows PowerShell 5.1, PowerShell Core 6.2.4 и PowerShell 7+.</span><span class="sxs-lookup"><span data-stu-id="cfa18-694">Added Azure.Core related assemblies into Az.Accounts, supported PowerShell platforms include Windows PowerShell 5.1, PowerShell Core 6.2.4, PowerShell 7+</span></span>

#### <a name="azaks"></a><span data-ttu-id="cfa18-695">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="cfa18-695">Az.Aks</span></span>
* <span data-ttu-id="cfa18-696">Версия API обновлена до 2019-10-01.</span><span class="sxs-lookup"><span data-stu-id="cfa18-696">Upgraded API Version to 2019-10-01</span></span>
* <span data-ttu-id="cfa18-697">Добавлена возможность создания контейнера Windows в службе Azure Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="cfa18-697">Supported to create AKS using Windows container</span></span>
* <span data-ttu-id="cfa18-698">Добавлены новые командлеты: New-AzAksNodePool, Update-AzAksNodePool, Remove-AzAksNodePool, Get-AzAksNodePool, Install-AzAksKubectl, Get-AzAksVersion.</span><span class="sxs-lookup"><span data-stu-id="cfa18-698">Provided new cmdlets: 'New-AzAksNodePool', 'Update-AzAksNodePool', 'Remove-AzAksNodePool',        'Get-AzAksNodePool', 'Install-AzAksKubectl', 'Get-AzAksVersion'</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="cfa18-699">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cfa18-699">Az.ApiManagement</span></span>
* <span data-ttu-id="cfa18-700">В New-AzApiManagement и Set-AzApiManagement параметр -AssignIdentity переименован в -SystemAssignedIdentity.</span><span class="sxs-lookup"><span data-stu-id="cfa18-700">'New-AzApiManagement' and 'Set-AzApiManagement': [-AssignIdentity] parameter renamed as [-SystemAssignedIdentity]</span></span>
* <span data-ttu-id="cfa18-701">В New-AzApiManagement и Set-AzApiManagement добавлен новый параметр -UserAssignedIdentity <строка[]>.</span><span class="sxs-lookup"><span data-stu-id="cfa18-701">'New-AzApiManagement' and 'Set-AzApiManagement': New parameter added: [-UserAssignedIdentity <String[]>]</span></span>
* <span data-ttu-id="cfa18-702">Командлет Get-AzApiManagementProperty переименован в Get-AzApiManagementNamedValue.</span><span class="sxs-lookup"><span data-stu-id="cfa18-702">'Get-AzApiManagementProperty': renamed as 'Get-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="cfa18-703">Параметр PropertyId переименован в NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="cfa18-703">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="cfa18-704">Командлет New-AzApiManagementProperty переименован в New-AzApiManagementNamedValue.</span><span class="sxs-lookup"><span data-stu-id="cfa18-704">'New-AzApiManagementProperty': renamed as 'New-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="cfa18-705">Параметр PropertyId переименован в NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="cfa18-705">PropertyId parameter renamed as NamedValueId.</span></span> 
* <span data-ttu-id="cfa18-706">Командлет Set-AzApiManagementProperty переименован в Set-AzApiManagementNamedValue.</span><span class="sxs-lookup"><span data-stu-id="cfa18-706">'Set-AzApiManagementProperty': renamed as 'Set-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="cfa18-707">Параметр PropertyId переименован в NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="cfa18-707">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="cfa18-708">Командлет Remove-AzApiManagementProperty переименован в Remove-AzApiManagementNamedValue.</span><span class="sxs-lookup"><span data-stu-id="cfa18-708">'Remove-AzApiManagementProperty': renamed as 'Remove-AzApiManagementNamedValue'.</span></span> <span data-ttu-id="cfa18-709">Параметр PropertyId переименован в NamedValueId.</span><span class="sxs-lookup"><span data-stu-id="cfa18-709">PropertyId parameter renamed as NamedValueId.</span></span>
* <span data-ttu-id="cfa18-710">Добавлен новый командлет Get-AzApiManagementAuthorizationServerClientSecret, а Get-AzApiManagementAuthorizationServer теперь не возвращает секрет клиента.</span><span class="sxs-lookup"><span data-stu-id="cfa18-710">Added new 'Get-AzApiManagementAuthorizationServerClientSecret' cmdlet and 'Get-AzApiManagementAuthorizationServer' will not return client secret anymore.</span></span>
* <span data-ttu-id="cfa18-711">Добавлен новый командлет Get-AzApiManagementNamedValueSecretValue, а Get-AzApiManagementNamedValue теперь не возвращает значение секрета.</span><span class="sxs-lookup"><span data-stu-id="cfa18-711">Added new 'Get-AzApiManagementNamedValueSecretValue' cmdlet and 'Get-AzApiManagementNamedValue' will not return secret value.</span></span>
* <span data-ttu-id="cfa18-712">Добавлен новый командлет Get-AzApiManagementOpenIdConnectProviderClientSecret, а Get-AzApiManagementOpenIdConnectProvider теперь не возвращает секрет клиента.</span><span class="sxs-lookup"><span data-stu-id="cfa18-712">Added new 'Get-AzApiManagementOpenIdConnectProviderClientSecret' cmdlet and 'Get-AzApiManagementOpenIdConnectProvider' will not return client secret anymore.</span></span>
* <span data-ttu-id="cfa18-713">Добавлен новый командлет Get-AzApiManagementSubscriptionKey, а Get-AzApiManagementSubscription теперь не возвращает ключи подписки.</span><span class="sxs-lookup"><span data-stu-id="cfa18-713">Added new 'Get-AzApiManagementSubscriptionKey' cmdlet and 'Get-AzApiManagementSubscription' will not return subscription keys anymore.</span></span>
* <span data-ttu-id="cfa18-714">Добавлен новый командлет Get-AzApiManagementTenantAccessSecret, а Get-AzApiManagementTenantAccess теперь не возвращает ключи.</span><span class="sxs-lookup"><span data-stu-id="cfa18-714">Added new 'Get-AzApiManagementTenantAccessSecret' cmdlet and 'Get-AzApiManagementTenantAccess' will not return keys anymore.</span></span>
* <span data-ttu-id="cfa18-715">Добавлен новый командлет Get-AzApiManagementTenantGitAccessSecret, а Get-AzApiManagementTenantGitAccess теперь не возвращает ключи.</span><span class="sxs-lookup"><span data-stu-id="cfa18-715">Added new 'Get-AzApiManagementTenantGitAccessSecret' cmdlet and 'Get-AzApiManagementTenantGitAccess' will not return keys anymore.</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="cfa18-716">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="cfa18-716">Az.ApplicationInsights</span></span>
* <span data-ttu-id="cfa18-717">В New-AzApplicationInsights добавлены параметры RetentionInDays, PublicNetworkAccessForIngestion и PublicNetworkAccessForQuery.</span><span class="sxs-lookup"><span data-stu-id="cfa18-717">Added Parameters: 'RetentionInDays' 'PublicNetworkAccessForIngestion' 'PublicNetworkAccessForQuery' for 'New-AzApplicationInsights'</span></span>
* <span data-ttu-id="cfa18-718">Создан командлет Update-AzApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="cfa18-718">Created cmdlet 'Update-AzApplicationInsights'</span></span>
* <span data-ttu-id="cfa18-719">Созданы командлеты для связанной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="cfa18-719">Created cmdlets for Linked Storage Account</span></span>

#### <a name="azbatch"></a><span data-ttu-id="cfa18-720">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="cfa18-720">Az.Batch</span></span>
* <span data-ttu-id="cfa18-721">В командлеты Az.Batch добавлена поддержка пакетов SDK Microsoft.Azure.Batch версии 13.0.0 и SDK Microsoft.Azure.Management.Batch версии 9.0.0.</span><span class="sxs-lookup"><span data-stu-id="cfa18-721">Updated Az.Batch to use 'Microsoft.Azure.Batch' SDK version 13.0.0 and 'Microsoft.Azure.Management.Batch' SDK version 9.0.0.</span></span>
* <span data-ttu-id="cfa18-722">Теперь в New-AzBatchCertificate можно выбрать тип добавляемого сертификата с помощью нового параметра -CertificateKind.</span><span class="sxs-lookup"><span data-stu-id="cfa18-722">Added the ability to select the kind of certificate being added using the new '-CertificateKind' parameter to 'New-AzBatchCertificate'.</span></span>
* <span data-ttu-id="cfa18-723">В PSApplication удалено свойство ApplicationPackages.</span><span class="sxs-lookup"><span data-stu-id="cfa18-723">Removed 'ApplicationPackages' property from 'PSApplication' which was previously always ''.</span></span>
  - <span data-ttu-id="cfa18-724">Отдельные пакеты в приложении теперь можно извлечь с помощью Get-AzBatchApplicationPackage.</span><span class="sxs-lookup"><span data-stu-id="cfa18-724">The specific packages inside of an application now can be retrieved using 'Get-AzBatchApplicationPackage'.</span></span> <span data-ttu-id="cfa18-725">Пример: Get-AzBatchApplication -AccountName моя_учетная_запись -ResourceGroupName моя_группа_ресурсов -ApplicationId мое_приложение.</span><span class="sxs-lookup"><span data-stu-id="cfa18-725">For example: 'Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication'.</span></span>
* <span data-ttu-id="cfa18-726">При создании пула с помощью New-AzBatchPool свойство VirtualMachineImageId элемента PSImageReference теперь может ссылаться только на образ из Общей коллекции образов.</span><span class="sxs-lookup"><span data-stu-id="cfa18-726">When creating a pool using 'New-AzBatchPool', the 'VirtualMachineImageId' property of 'PSImageReference' can now only refer to a Shared Image Gallery image.</span></span>
* <span data-ttu-id="cfa18-727">При создании пула с помощью New-AzBatchPool пул можно подготовить без общедоступного IP-адреса, используя новое свойство PublicIPAddressConfiguration элемента PSNetworkConfiguration.</span><span class="sxs-lookup"><span data-stu-id="cfa18-727">When creating a pool using 'New-AzBatchPool', the pool can be provisioned without a public IP using the new 'PublicIPAddressConfiguration' property of 'PSNetworkConfiguration'.</span></span>
  - <span data-ttu-id="cfa18-728">Свойство PublicIPs элемента PSNetworkConfiguration было передано элементу PSPublicIPAddressConfiguration.</span><span class="sxs-lookup"><span data-stu-id="cfa18-728">The 'PublicIPs' property of 'PSNetworkConfiguration' has moved in to 'PSPublicIPAddressConfiguration' as well.</span></span> <span data-ttu-id="cfa18-729">Это свойство можно указать, только если параметру IPAddressProvisioningType присвоено значение UserManaged.</span><span class="sxs-lookup"><span data-stu-id="cfa18-729">This property can only be specified if 'IPAddressProvisioningType' is 'UserManaged'.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cfa18-730">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cfa18-730">Az.Compute</span></span>
* <span data-ttu-id="cfa18-731">В командлет Update-AzVM добавлен параметр HostId.</span><span class="sxs-lookup"><span data-stu-id="cfa18-731">Added HostId parameter to 'Update-AzVM' cmdlet</span></span>
* <span data-ttu-id="cfa18-732">Обновлена справочная документация по командлетам New-AzVMConfig, New-AzVmssConfig, Update-AzVmss, Set-AzVMOperatingSystem и Set-AzVmssOsProfile.</span><span class="sxs-lookup"><span data-stu-id="cfa18-732">Updated Help documents for 'New-AzVMConfig', 'New-AzVmssConfig', 'Update-AzVmss', 'Set-AzVMOperatingSystem' and 'Set-AzVmssOsProfile' cmdlets.</span></span>
* <span data-ttu-id="cfa18-733">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="cfa18-733">Breaking changes</span></span>
    - <span data-ttu-id="cfa18-734">Параметр FilterExpression удален из командлета Get-AzVMImage.</span><span class="sxs-lookup"><span data-stu-id="cfa18-734">FilterExpression parameter is removed from 'Get-AzVMImage' cmdlet.</span></span>
    - <span data-ttu-id="cfa18-735">Параметр AssignIdentity удален из командлетов New-AzVmssConfig, New-AzVMConfig и Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="cfa18-735">AssignIdentity parameter is removed from 'New-AzVmssConfig', 'New-AzVMConfig' and 'Update-AzVM' cmdlets.</span></span>
    - <span data-ttu-id="cfa18-736">Параметр AutomaticRepairMaxInstanceRepairsPercent удален из командлетов New-AzVmssConfig и Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="cfa18-736">AutomaticRepairMaxInstanceRepairsPercent is removed from 'New-AzVmssConfig' and 'Update-AzVmss' cmdlets.</span></span>
    - <span data-ttu-id="cfa18-737">Свойства AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus и VirtualMachineScaleSetsColocationStatus удалены из ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="cfa18-737">AvailabilitySetsColocationStatus, VirtualMachinesColocationStatus and VirtualMachineScaleSetsColocationStatus properties are removed from ProximityPlacementGroup.</span></span>
    - <span data-ttu-id="cfa18-738">Свойство MaxInstanceRepairsPercent удалено из AutomaticRepairsPolicy.</span><span class="sxs-lookup"><span data-stu-id="cfa18-738">MaxInstanceRepairsPercent property is removed from AutomaticRepairsPolicy.</span></span>
    - <span data-ttu-id="cfa18-739">Типы AvailabilitySets, VirtualMachines и VirtualMachineScaleSets изменены с IList<SubResource> на IList<SubResourceWithColocationStatus>.</span><span class="sxs-lookup"><span data-stu-id="cfa18-739">The types of AvailabilitySets, VirtualMachines and VirtualMachineScaleSets are changed from IList<SubResource> to IList<SubResourceWithColocationStatus>.</span></span>
* <span data-ttu-id="cfa18-740">Уточнено описание командлета Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="cfa18-740">Description for 'Get-AzVM' cmdlet has been updated to better describe it.</span></span> 

#### <a name="azdatafactory"></a><span data-ttu-id="cfa18-741">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cfa18-741">Az.DataFactory</span></span>
* <span data-ttu-id="cfa18-742">Добавлена поддержка операций CRUD для свойств среды выполнения потока данных в управляемой среде выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="cfa18-742">Supported CRUD of data flow runtime properties in Managed IR.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="cfa18-743">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="cfa18-743">Az.FrontDoor</span></span>
* <span data-ttu-id="cfa18-744">Добавлены новые командлеты для создания, обновления, извлечения и удаления объекта обработчика правил Front Door.</span><span class="sxs-lookup"><span data-stu-id="cfa18-744">Added new cmdlets for creation, update, retreival, and deletion of Front Door Rules Engine object</span></span>
* <span data-ttu-id="cfa18-745">Добавлены вспомогательные командлеты для создания объекта обработчика правил Front Door.</span><span class="sxs-lookup"><span data-stu-id="cfa18-745">Added helper cmdlets for construction of Front Door Rules Engine object</span></span>
* <span data-ttu-id="cfa18-746">Добавлена ссылка обработчика правил на объект правила маршрутизации Front Door.</span><span class="sxs-lookup"><span data-stu-id="cfa18-746">Added Rules Engine reference to Front Door Routing Rule object.</span></span>
* <span data-ttu-id="cfa18-747">Добавлены параметры Приватного канала на серверный объект Front Door.</span><span class="sxs-lookup"><span data-stu-id="cfa18-747">Added Private Link parameters to Front Door Backend object</span></span>

#### <a name="azfunctions"></a><span data-ttu-id="cfa18-748">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="cfa18-748">Az.Functions</span></span>
* <span data-ttu-id="cfa18-749">Вышла общедоступная версия модуля Az.Functions.</span><span class="sxs-lookup"><span data-stu-id="cfa18-749">General availability of ''Az.Functions'' module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="cfa18-750">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cfa18-750">Az.HDInsight</span></span>
* <span data-ttu-id="cfa18-751">Добавлена поддержка шифрования управляемых клиентом ключей.</span><span class="sxs-lookup"><span data-stu-id="cfa18-751">Supported Customer-managed key disk encryption.</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="cfa18-752">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="cfa18-752">Az.HealthcareApis</span></span>
* <span data-ttu-id="cfa18-753">Политики доступа для текущего субъекта теперь не используются по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cfa18-753">Access policies are no longer defaulted to the current principal</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cfa18-754">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cfa18-754">Az.IotHub</span></span>
* <span data-ttu-id="cfa18-755">Добавлен командлет для вызова запроса в центре Интернета вещей для получения данных с помощью SQL-подобного языка.</span><span class="sxs-lookup"><span data-stu-id="cfa18-755">Added cmdlet to invoke a query in an IoT hub to retrieve information using a SQL-like language.</span></span>
* <span data-ttu-id="cfa18-756">Устранена проблема, когда с помощью Add-AzIotHubDevice не удавалось создать устройство с поддержкой IoT Edge без дочерних устройств (№ 11597).</span><span class="sxs-lookup"><span data-stu-id="cfa18-756">Fix issue that 'Add-AzIotHubDevice' fails to create Edge Enabled Device without child devices [#11597]</span></span>
* <span data-ttu-id="cfa18-757">Добавлен командлет для создания маркера SAS для Центра Интернета вещей, устройства или модуля.</span><span class="sxs-lookup"><span data-stu-id="cfa18-757">Added cmdlet to generate SAS token for Iot Hub, device or module.</span></span>
* <span data-ttu-id="cfa18-758">Добавлен командлет для вызова запроса метрик конфигурации.</span><span class="sxs-lookup"><span data-stu-id="cfa18-758">Added cmdlet to invoke configuration metrics query.</span></span>
* <span data-ttu-id="cfa18-759">Появилась возможность управлять автоматическим развертыванием IoT Edge в большом масштабе.</span><span class="sxs-lookup"><span data-stu-id="cfa18-759">Manage IoT Edge automatic deployment at scale.</span></span> <span data-ttu-id="cfa18-760">Ниже перечислены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="cfa18-760">New cmdlets are:</span></span>
    - <span data-ttu-id="cfa18-761">Add-AzIotHubDeployment;</span><span class="sxs-lookup"><span data-stu-id="cfa18-761">'Add-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="cfa18-762">Get-AzIotHubDeployment;</span><span class="sxs-lookup"><span data-stu-id="cfa18-762">'Get-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="cfa18-763">Remove-AzIotHubDeployment;</span><span class="sxs-lookup"><span data-stu-id="cfa18-763">'Remove-AzIotHubDeployment'</span></span>
    - <span data-ttu-id="cfa18-764">Set-AzIotHubDeployment.</span><span class="sxs-lookup"><span data-stu-id="cfa18-764">'Set-AzIotHubDeployment'</span></span>
* <span data-ttu-id="cfa18-765">Добавлен командлет для вызова запроса метрик развертывания IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="cfa18-765">Added cmdlet to invoke an IoT Edge deployment metrics query.</span></span>
* <span data-ttu-id="cfa18-766">Добавлен командлет для применения содержимого конфигурации к указанному пограничному устройству.</span><span class="sxs-lookup"><span data-stu-id="cfa18-766">Added cmdlet to apply the configuration content to the specified edge device.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cfa18-767">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cfa18-767">Az.KeyVault</span></span>
* <span data-ttu-id="cfa18-768">Удалены два псевдонима: New-AzKeyVaultCertificateAdministratorDetails и New-AzKeyVaultCertificateOrganizationDetails.</span><span class="sxs-lookup"><span data-stu-id="cfa18-768">Removed two aliases: 'New-AzKeyVaultCertificateAdministratorDetails' and 'New-AzKeyVaultCertificateOrganizationDetails'</span></span>
* <span data-ttu-id="cfa18-769">При создании хранилища ключей обратимое удаление включено по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cfa18-769">Enabled soft delete by default when creating a key vault</span></span>
* <span data-ttu-id="cfa18-770">Можно задать правила сети, чтобы при создании хранилища ключей управлять доступом из определенных сетевых расположений.</span><span class="sxs-lookup"><span data-stu-id="cfa18-770">Network rules can be set to govern the accessibility from specific network locations when creating a key vault</span></span>
* <span data-ttu-id="cfa18-771">Добавлена возможность создания собственных ключей (BYOK).</span><span class="sxs-lookup"><span data-stu-id="cfa18-771">Added support to bring your own key (BYOK)</span></span>
    - <span data-ttu-id="cfa18-772">С помощью Add-AzKeyVaultKey теперь можно создавать ключ обмена ключами.</span><span class="sxs-lookup"><span data-stu-id="cfa18-772">'Add-AzKeyVaultKey' supports generating a key exchange key</span></span>
    - <span data-ttu-id="cfa18-773">С помощью Get-AzKeyVaultKey можно скачать открытый ключ в формате PEM.</span><span class="sxs-lookup"><span data-stu-id="cfa18-773">'Get-AzKeyVaultKey' supports downloading a public key in PEM format</span></span>
* <span data-ttu-id="cfa18-774">Обновлен раздел KeyOps справочной документации по Add-AzKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="cfa18-774">Updated the 'KeyOps' part of the help document of 'Add-AzKeyVaultKey'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cfa18-775">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cfa18-775">Az.Monitor</span></span>
* <span data-ttu-id="cfa18-776">Исправлена ошибка Set-AzDiagnosticSettings, когда политика хранения не применялась ко всем категориям (№ 11589).</span><span class="sxs-lookup"><span data-stu-id="cfa18-776">Fixed bug for 'Set-AzDiagnosticSettings', retention policy won't apply to all categories [#11589]</span></span>
* <span data-ttu-id="cfa18-777">Добавлена поддержка критериев доступности веб-теста для оповещения метрики версии 2.</span><span class="sxs-lookup"><span data-stu-id="cfa18-777">Supported WebTest availability criteria for metric alert V2</span></span>
    - <span data-ttu-id="cfa18-778">В New-AzMetricAlertRuleV2Criteria добавлена возможность создавать критерии доступности веб-теста.</span><span class="sxs-lookup"><span data-stu-id="cfa18-778">'New-AzMetricAlertRuleV2Criteria': an option to create webtest availability criteria was added</span></span>
    - <span data-ttu-id="cfa18-779">Add-AzMetricAlertRuleV2 теперь поддерживает новые критерии доступности веб-теста.</span><span class="sxs-lookup"><span data-stu-id="cfa18-779">'Add-AzMetricAlertRuleV2': supports the new webtest availability criteria</span></span>
* <span data-ttu-id="cfa18-780">В PSLogProfile исправлено избыточное определение RetentionPolicy (№ 7608).</span><span class="sxs-lookup"><span data-stu-id="cfa18-780">Removed redundant definition for RetentionPolicy in PSLogProfile [#7608]</span></span>
* <span data-ttu-id="cfa18-781">В PSEventData удалены избыточные определения свойств (№ 11353).</span><span class="sxs-lookup"><span data-stu-id="cfa18-781">Removed redundant properties difined in PSEventData [#11353]</span></span>
* <span data-ttu-id="cfa18-782">Командлет Get-AzLog переименован в Get-AzActivityLog.</span><span class="sxs-lookup"><span data-stu-id="cfa18-782">Renamed 'Get-AzLog' to 'Get-AzActivityLog'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cfa18-783">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cfa18-783">Az.Network</span></span>
* <span data-ttu-id="cfa18-784">Добавлен атрибут критического изменения, сообщающий о том, что поведение зоны по умолчанию будет изменено.</span><span class="sxs-lookup"><span data-stu-id="cfa18-784">Added breaking change attribute to notify that Zone default behaviour will be changed</span></span>
    - <span data-ttu-id="cfa18-785">New-AzPublicIpAddress;</span><span class="sxs-lookup"><span data-stu-id="cfa18-785">'New-AzPublicIpAddress'</span></span>
    - <span data-ttu-id="cfa18-786">New-AzPublicIpPrefix;</span><span class="sxs-lookup"><span data-stu-id="cfa18-786">'New-AzPublicIpPrefix'</span></span>
    - <span data-ttu-id="cfa18-787">New-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="cfa18-787">'New-AzLoadBalancerFrontendIpConfig'</span></span>
* <span data-ttu-id="cfa18-788">Добавлена поддержка нового ресурса верхнего уровня SecurityPartnerProvider.</span><span class="sxs-lookup"><span data-stu-id="cfa18-788">Added support for a new top level resource SecurityPartnerProvider</span></span>
    - <span data-ttu-id="cfa18-789">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="cfa18-789">New cmdlets added:</span></span>
        - <span data-ttu-id="cfa18-790">New-AzSecurityPartnerProvider;</span><span class="sxs-lookup"><span data-stu-id="cfa18-790">New-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="cfa18-791">Remove-AzSecurityPartnerProvider;</span><span class="sxs-lookup"><span data-stu-id="cfa18-791">Remove-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="cfa18-792">Get-AzSecurityPartnerProvider;</span><span class="sxs-lookup"><span data-stu-id="cfa18-792">Get-AzSecurityPartnerProvider</span></span>
        - <span data-ttu-id="cfa18-793">Set-AzSecurityPartnerProvider.</span><span class="sxs-lookup"><span data-stu-id="cfa18-793">Set-AzSecurityPartnerProvider</span></span>
* <span data-ttu-id="cfa18-794">В PSPrivateLinkResource добавлен параметр RequiredZoneNames, а в PSPrivateEndpointConnection — GroupId.</span><span class="sxs-lookup"><span data-stu-id="cfa18-794">Added 'RequiredZoneNames' on 'PSPrivateLinkResource' and 'GroupId' on 'PSPrivateEndpointConnection'</span></span>
* <span data-ttu-id="cfa18-795">Исправлен неправильный тип параметра SuccessThresholdRoundTripTimeMs для New-AzNetworkWatcherConnectionMonitorTestConfigurationObject.</span><span class="sxs-lookup"><span data-stu-id="cfa18-795">Fixed incorrect type of SuccessThresholdRoundTripTimeMs parameter for New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>
* <span data-ttu-id="cfa18-796">В командлетах VirtualWan аргументу AllowVnetToVnetTraffic теперь по умолчанию присвоено значение True.</span><span class="sxs-lookup"><span data-stu-id="cfa18-796">Updated VirtualWan cmdlets to set default value of AllowVnetToVnetTraffic argument to True.</span></span>
    - <span data-ttu-id="cfa18-797">New-AzVirtualWan;</span><span class="sxs-lookup"><span data-stu-id="cfa18-797">'New-AzVirtualWan'</span></span>
    - <span data-ttu-id="cfa18-798">Update-AzVirtualWan.</span><span class="sxs-lookup"><span data-stu-id="cfa18-798">'Update-AzVirtualWan'</span></span>
* <span data-ttu-id="cfa18-799">Добавлены новые командлеты для поддержки группы зон DNS для частной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="cfa18-799">Added new cmdlets to support DNS zone group for private endpoint</span></span>
    - <span data-ttu-id="cfa18-800">New-AzPrivateDnsZoneConfig;</span><span class="sxs-lookup"><span data-stu-id="cfa18-800">'New-AzPrivateDnsZoneConfig'</span></span>
    - <span data-ttu-id="cfa18-801">Get-AzPrivateDnsZoneGroup;</span><span class="sxs-lookup"><span data-stu-id="cfa18-801">'Get-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="cfa18-802">New-AzPrivateDnsZoneGroup;</span><span class="sxs-lookup"><span data-stu-id="cfa18-802">'New-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="cfa18-803">Set-AzPrivateDnsZoneGroup;</span><span class="sxs-lookup"><span data-stu-id="cfa18-803">'Set-AzPrivateDnsZoneGroup'</span></span>
    - <span data-ttu-id="cfa18-804">Remove-AzPrivateDnsZoneGroup.</span><span class="sxs-lookup"><span data-stu-id="cfa18-804">'Remove-AzPrivateDnsZoneGroup'</span></span>
* <span data-ttu-id="cfa18-805">В AzureFirewall добавлены параметры DNSEnableProxy, DNSRequireProxyForNetworkRules и DNSServers.</span><span class="sxs-lookup"><span data-stu-id="cfa18-805">Added 'DNSEnableProxy', 'DNSRequireProxyForNetworkRules' and 'DNSServers' parameters to 'AzureFirewall'</span></span>
* <span data-ttu-id="cfa18-806">В AzureFirewall добавлены параметры EnableDnsProxy, DnsProxyNotRequiredForNetworkRule и DnsServer.</span><span class="sxs-lookup"><span data-stu-id="cfa18-806">Added 'EnableDnsProxy', 'DnsProxyNotRequiredForNetworkRule' and 'DnsServer' parameters to 'AzureFirewall'</span></span>
    - <span data-ttu-id="cfa18-807">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="cfa18-807">Updated cmdlet:</span></span>
        - <span data-ttu-id="cfa18-808">New-AzFirewall.</span><span class="sxs-lookup"><span data-stu-id="cfa18-808">New-AzFirewall</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="cfa18-809">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cfa18-809">Az.OperationalInsights</span></span>
* <span data-ttu-id="cfa18-810">Обновлен устаревший код для использования новых пакетов SDK.</span><span class="sxs-lookup"><span data-stu-id="cfa18-810">Updated legacy code to apply new generated SDK</span></span>
* <span data-ttu-id="cfa18-811">Из-за устаревших API-интерфейсов удалены следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="cfa18-811">Deleted cmdlets due to deprecated APIs</span></span>
    - <span data-ttu-id="cfa18-812">Get-AzOperationalInsightsSavedSearchResult (псевдоним Get-AzOperationalInsightsSavedSearchResults);</span><span class="sxs-lookup"><span data-stu-id="cfa18-812">'Get-AzOperationalInsightsSavedSearchResult' (alias 'Get-AzOperationalInsightsSavedSearchResults')</span></span>
    - <span data-ttu-id="cfa18-813">Get-AzOperationalInsightsSearchResult (псевдоним Get-AzOperationalInsightsSearchResults);</span><span class="sxs-lookup"><span data-stu-id="cfa18-813">'Get-AzOperationalInsightsSearchResult' (alias 'Get-AzOperationalInsightsSearchResults')</span></span>
    - <span data-ttu-id="cfa18-814">Get-AzOperationalInsightsLinkTarget (псевдоним Get-AzOperationalInsightsLinkTargets).</span><span class="sxs-lookup"><span data-stu-id="cfa18-814">'Get-AzOperationalInsightsLinkTarget' (alias 'Get-AzOperationalInsightsLinkTargets')</span></span>
* <span data-ttu-id="cfa18-815">В Set-AzOperationalInsightsWorkspace и New-AzOperationalInsightsWorkspace добавлены новые параметры.</span><span class="sxs-lookup"><span data-stu-id="cfa18-815">Added parameters for 'Set-AzOperationalInsightsWorkspace' and 'New-AzOperationalInsightsWorkspace'</span></span>
* <span data-ttu-id="cfa18-816">Созданы командлеты для связанной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="cfa18-816">Created cmdlets for Linked Stoarge Account</span></span>
* <span data-ttu-id="cfa18-817">Созданы командлеты для кластеров и связанной службы.</span><span class="sxs-lookup"><span data-stu-id="cfa18-817">Created cmdlets for Clusters and Linked Service</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cfa18-818">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cfa18-818">Az.RecoveryServices</span></span>
* <span data-ttu-id="cfa18-819">В Azure Site Recovery добавлена поддержка защиты поставщика Azure для групп размещения виртуальных машин Azure близкого взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="cfa18-819">Azure Site Recovery added support for protecting proximity placement group virtual machines for Azure to Azure provider.</span></span>
* <span data-ttu-id="cfa18-820">В Azure Site Recovery добавлена поддержка репликации из зоны в зону.</span><span class="sxs-lookup"><span data-stu-id="cfa18-820">Azure Site Recovery added support for zone to zone replication.</span></span>
* <span data-ttu-id="cfa18-821">В Azure Backup добавлена поддержка долгосрочного хранения для точек восстановления общей папки Azure.</span><span class="sxs-lookup"><span data-stu-id="cfa18-821">Azure Backup Added Long term retention support for Azure FileShare Recovery Points.</span></span>
* <span data-ttu-id="cfa18-822">В выходные данные командлета Get-AzRecoveryServicesBackupItem добавлены свойства исключения диска, добавленного в Azure Backup.</span><span class="sxs-lookup"><span data-stu-id="cfa18-822">Azure Backup Added disk exclusion properties to 'Get-AzRecoveryServicesBackupItem' cmdlet output.</span></span>
* <span data-ttu-id="cfa18-823">Добавлена частная конечная точка для файла учетных данных хранилища для службы Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="cfa18-823">Added private endpoint for Vault credential file for site recovery service.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cfa18-824">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cfa18-824">Az.Resources</span></span>
* <span data-ttu-id="cfa18-825">Добавлено предупреждение о задержке представления при создании определения роли.</span><span class="sxs-lookup"><span data-stu-id="cfa18-825">Added message warning about view delay when creating a new Role Definition</span></span>
* <span data-ttu-id="cfa18-826">Командлеты политики теперь выводят строго типизированные объекты.</span><span class="sxs-lookup"><span data-stu-id="cfa18-826">Changed policy cmdlets to output strongly-typed objects</span></span>
* <span data-ttu-id="cfa18-827">Из командлета Get-AzResourceLock удален параметр -TenantLevel (№ 11335).</span><span class="sxs-lookup"><span data-stu-id="cfa18-827">Removed '-TenantLevel' parameter used for on the 'Get-AzResourceLock' cmdlet [#11335]</span></span>
* <span data-ttu-id="cfa18-828">Исправлена ошибка с Remove-AzResourceGroup -Id ResourceId (№ 9882).</span><span class="sxs-lookup"><span data-stu-id="cfa18-828">Fixed 'Remove-AzResourceGroup -Id ResourceId'[#9882]</span></span>
* <span data-ttu-id="cfa18-829">Добавлен новый командлет для получения результатов анализа гипотетических вариантов из шаблона ARM в области группы ресурсов: Get-AzDeploymentResourceGroupWhatIfResult.</span><span class="sxs-lookup"><span data-stu-id="cfa18-829">Added new cmdlet for getting ARM template What-If results at resource group scope: 'Get-AzDeploymentResourceGroupWhatIfResult'</span></span>
* <span data-ttu-id="cfa18-830">Добавлен новый командлет для получения результатов анализа гипотетических вариантов из шаблона ARM в области подписки: Get-AzDeploymentWhatIfResult.</span><span class="sxs-lookup"><span data-stu-id="cfa18-830">Added new cmdlet for getting ARM template What-If results at subscription scope: 'Get-AzDeploymentWhatIfResult'</span></span>
   - <span data-ttu-id="cfa18-831">Alias: Get-AzSubscriptionDeploymentWhatIf.</span><span class="sxs-lookup"><span data-stu-id="cfa18-831">Alias: 'Get-AzSubscriptionDeploymentWhatIf'</span></span>
* <span data-ttu-id="cfa18-832">Переопределены параметры -WhatIf и -Confirm для New-AzDeployment и New-AzResourceGroupDeployment для использования результатов анализа гипотетических вариантов из шаблона ARM.</span><span class="sxs-lookup"><span data-stu-id="cfa18-832">Overrode '-WhatIf' and '-Confirm' parameters for 'New-AzDeployment' and 'New-AzResourceGroupDeployment' to use ARM template What-If results</span></span>
* <span data-ttu-id="cfa18-833">В командлеты развертывания добавлено сообщение об устаревании для параметра ApiVersion.</span><span class="sxs-lookup"><span data-stu-id="cfa18-833">Added deprecation message for 'ApiVersion' parameter in deployment cmdlets</span></span>
* <span data-ttu-id="cfa18-834">Добавлена возможность отображения улучшенных сообщений об ошибках при развертывании.</span><span class="sxs-lookup"><span data-stu-id="cfa18-834">Added capability to show improved error messages for deployment failures</span></span>
* <span data-ttu-id="cfa18-835">Добавлена возможность регистрации correlationId для сбоев развертывания.</span><span class="sxs-lookup"><span data-stu-id="cfa18-835">Added correlationId logging for deployment failures</span></span>
* <span data-ttu-id="cfa18-836">В выходные данные скрипта развертывания добавлено свойство error.</span><span class="sxs-lookup"><span data-stu-id="cfa18-836">Added 'error' property to the deployment script output</span></span>
* <span data-ttu-id="cfa18-837">Пакет NuGet Microsoft.Azure.Management.ResourceManager обновлен до версии 3.7.1-preview.</span><span class="sxs-lookup"><span data-stu-id="cfa18-837">Updated nuget Microsoft.Azure.Management.ResourceManager to '3.7.1-preview'</span></span>
* <span data-ttu-id="cfa18-838">Удаленные определенные тестовые случаи как свойство error в DeploymentValidateResult были изменены на доступные только для чтения из пакета NuGet версии 3.7.1-preview.</span><span class="sxs-lookup"><span data-stu-id="cfa18-838">Removed specific test cases as Error property in DeploymentValidateResult has changed to readonly from nuget 3.7.1-preview</span></span>
* <span data-ttu-id="cfa18-839">Добавлен GenericResourceExpanded из пакета SDK ResourceManager версии 3.7.1-preview.</span><span class="sxs-lookup"><span data-stu-id="cfa18-839">Brought GenericResourceExpanded from SDK ResourceManager 3.7.1-preview</span></span>
* <span data-ttu-id="cfa18-840">Добавлена поддержка тегов для всех командлетов Get для развертывания, а также для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="cfa18-840">Added tag support for all Get cmdlets for deployment, as well as</span></span>
    - <span data-ttu-id="cfa18-841">New-AzDeployment;</span><span class="sxs-lookup"><span data-stu-id="cfa18-841">'New-AzDeployment'</span></span>
    - <span data-ttu-id="cfa18-842">New-AzManagementGroupDeployment;</span><span class="sxs-lookup"><span data-stu-id="cfa18-842">'New-AzManagementGroupDeployment'</span></span>
    - <span data-ttu-id="cfa18-843">New-AzResourceGroupDeployment;</span><span class="sxs-lookup"><span data-stu-id="cfa18-843">'New-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="cfa18-844">New-AzTenantDeployment.</span><span class="sxs-lookup"><span data-stu-id="cfa18-844">'New-AzTenantDeployment'</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="cfa18-845">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cfa18-845">Az.ServiceFabric</span></span>
* <span data-ttu-id="cfa18-846">Исправлена ошибка при добавлении сертификата с помощью параметра -SecretIdentifier, когда возвращался неправильный отпечаток сертификата.</span><span class="sxs-lookup"><span data-stu-id="cfa18-846">Fixed bug in add certificate using --SecretIdentifier that was getting the wrong certificate thumbprint</span></span>

#### <a name="azsql"></a><span data-ttu-id="cfa18-847">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cfa18-847">Az.Sql</span></span>
* <span data-ttu-id="cfa18-848">Оптимизирована работа следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="cfa18-848">Enhance performance of:</span></span>
    - <span data-ttu-id="cfa18-849">Set-AzSqlDatabaseSensitivityClassification;</span><span class="sxs-lookup"><span data-stu-id="cfa18-849">'Set-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="cfa18-850">Set-AzSqlInstanceDatabaseSensitivityClassification;</span><span class="sxs-lookup"><span data-stu-id="cfa18-850">'Set-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="cfa18-851">Remove-AzSqlDatabaseSensitivityClassification;</span><span class="sxs-lookup"><span data-stu-id="cfa18-851">'Remove-AzSqlDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="cfa18-852">Remove-AzSqlInstanceDatabaseSensitivityClassification;</span><span class="sxs-lookup"><span data-stu-id="cfa18-852">'Remove-AzSqlInstanceDatabaseSensitivityClassification'</span></span>
    - <span data-ttu-id="cfa18-853">Enable-AzSqlDatabaseSensitivityRecommendation;</span><span class="sxs-lookup"><span data-stu-id="cfa18-853">'Enable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="cfa18-854">Enable-AzSqlInstanceDatabaseSensitivityRecommendation;</span><span class="sxs-lookup"><span data-stu-id="cfa18-854">'Enable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="cfa18-855">Disable-AzSqlDatabaseSensitivityRecommendation;</span><span class="sxs-lookup"><span data-stu-id="cfa18-855">'Disable-AzSqlDatabaseSensitivityRecommendation'</span></span>
    - <span data-ttu-id="cfa18-856">Disable-AzSqlInstanceDatabaseSensitivityRecommendation.</span><span class="sxs-lookup"><span data-stu-id="cfa18-856">'Disable-AzSqlInstanceDatabaseSensitivityRecommendation'</span></span>
* <span data-ttu-id="cfa18-857">Удалена проверка на стороне клиента параметра RetentionDays из командлета Set-AzSqlDatabaseBackupShortTermRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="cfa18-857">Removed client-side validation of 'RetentionDays' parameter from cmdlet 'Set-AzSqlDatabaseBackupShortTermRetentionPolicy'</span></span>
* <span data-ttu-id="cfa18-858">Добавлен аудит учетной записи хранения в виртуальной сети. Исправлена ошибка при создании роли участника данных BLOB-объектов хранилища.</span><span class="sxs-lookup"><span data-stu-id="cfa18-858">Auditing to a storage account in Vnet, fixing a bug when creating a Storage Blob Data Contributor role.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cfa18-859">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cfa18-859">Az.Storage</span></span>
* <span data-ttu-id="cfa18-860">В командлет Get-AzStorageAccount добавлен параметр -AsJob.</span><span class="sxs-lookup"><span data-stu-id="cfa18-860">Added '-AsJob' to get/list account cmdlet 'Get-AzStorageAccount'</span></span>
* <span data-ttu-id="cfa18-861">Параметр KeyVersion теперь является необязательным при изменении учетной записи хранения с помощью KeyvaultEncryption, что обеспечивает поддержку автоматической смены ключа.</span><span class="sxs-lookup"><span data-stu-id="cfa18-861">Make KeyVersion to optional when update Storage account with KeyvaultEncryption, to support key auto-rotation</span></span>
    - <span data-ttu-id="cfa18-862">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cfa18-862">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="cfa18-863">Исправлена ошибка при удалении каталога файлов Azure с конвейером.</span><span class="sxs-lookup"><span data-stu-id="cfa18-863">Fixed remove Azure File Directory fail with pipeline</span></span>
    - <span data-ttu-id="cfa18-864">Remove-AzStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="cfa18-864">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="cfa18-865">Исправлена ошибка 9880. Значение DefaultAction для NetWorkRule приведено в соответствие со Swagger.</span><span class="sxs-lookup"><span data-stu-id="cfa18-865">Fixed [#9880]: Change NetWorkRule DefaultAction value defination to align with swagger.</span></span>
    - <span data-ttu-id="cfa18-866">Update-AzStorageAccountNetworkRuleSet;</span><span class="sxs-lookup"><span data-stu-id="cfa18-866">'Update-AzStorageAccountNetworkRuleSet'</span></span>
    - <span data-ttu-id="cfa18-867">Get-AzStorageAccountNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="cfa18-867">'Get-AzStorageAccountNetworkRuleSet'</span></span>
* <span data-ttu-id="cfa18-868">Исправлена ошибка 11624. При добавлении NetworkRules дублирующиеся правила пропускаются, чтобы не происходил сбой сервера.</span><span class="sxs-lookup"><span data-stu-id="cfa18-868">Fixed [#11624]: Skip duplicated rules when add NetworkRules, to avoid server failure</span></span>
    - <span data-ttu-id="cfa18-869">Add-AzStorageAccountNetworkRule.</span><span class="sxs-lookup"><span data-stu-id="cfa18-869">'Add-AzStorageAccountNetworkRule'</span></span>
* <span data-ttu-id="cfa18-870">Версия пакета SDK Microsoft.Azure.Cosmos.Table обновлена до 1.0.7.</span><span class="sxs-lookup"><span data-stu-id="cfa18-870">Upgraded Microsoft.Azure.Cosmos.Table SDK to 1.0.7</span></span>
* <span data-ttu-id="cfa18-871">Добавлено предупреждающее сообщение, напоминающее пользователю о необходимости повторного вывода списка с помощью ContinuationToken, когда в списке элементов Data Lake 2-го поколения возвращается только часть элементов.</span><span class="sxs-lookup"><span data-stu-id="cfa18-871">Added a warning message to remind user to list again with ContinuationToken when only part items are returned in list DataLake Gen2 Items,</span></span>
    - <span data-ttu-id="cfa18-872">Get-AzDataLakeGen2ChildItem</span><span class="sxs-lookup"><span data-stu-id="cfa18-872">'Get-AzDataLakeGen2ChildItem'</span></span>
* <span data-ttu-id="cfa18-873">Добавлена возможность создания или изменения учетной записи хранения с использованием проверки подлинности Active Directory для Файлов Azure.</span><span class="sxs-lookup"><span data-stu-id="cfa18-873">Supported to create or update Storage account with Azure Files Active Directory Domain Service Authentication</span></span>
    -  <span data-ttu-id="cfa18-874">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cfa18-874">'New-AzStorageAccount'</span></span>
    -  <span data-ttu-id="cfa18-875">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cfa18-875">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="cfa18-876">Добавлена возможность создания и просмотра ключей Kerberos учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="cfa18-876">Supported to new or list Kerberos keys of Storage account</span></span>
    -  <span data-ttu-id="cfa18-877">New-AzStorageAccountKey;</span><span class="sxs-lookup"><span data-stu-id="cfa18-877">'New-AzStorageAccountKey'</span></span>
    -  <span data-ttu-id="cfa18-878">Get-AzStorageAccountKey.</span><span class="sxs-lookup"><span data-stu-id="cfa18-878">'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="cfa18-879">Добавлена возможность отработки отказа для учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="cfa18-879">Supported failover Storage account</span></span>
    - <span data-ttu-id="cfa18-880">Invoke-AzStorageAccountFailover.</span><span class="sxs-lookup"><span data-stu-id="cfa18-880">'Invoke-AzStorageAccountFailover'</span></span>
* <span data-ttu-id="cfa18-881">Обновлена справка по Get-AzStorageBlobCopyState.</span><span class="sxs-lookup"><span data-stu-id="cfa18-881">Updated help of 'Get-AzStorageBlobCopyState'</span></span>
* <span data-ttu-id="cfa18-882">Обновлена справка по Get-AzStorageFileCopyState и Start-AzStorageBlobCopy.</span><span class="sxs-lookup"><span data-stu-id="cfa18-882">Updated help of 'Get-AzStorageFileCopyState' and 'Start-AzStorageBlobCopy'</span></span>
* <span data-ttu-id="cfa18-883">Появилась интегрированная клиентская библиотека хранилища версии 12 для командлетов очередей и файлов.</span><span class="sxs-lookup"><span data-stu-id="cfa18-883">Integrated Storage client library v12 to Queue and File cmdlets</span></span>
* <span data-ttu-id="cfa18-884">Тип выходных данных изменен с CloudFile на AzureStorageFile. Первоначальные выходные данные теперь становятся дочерним элементом нового типа выходных данных.</span><span class="sxs-lookup"><span data-stu-id="cfa18-884">Changed output type from CloudFile to AzureStorageFile, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="cfa18-885">Get-AzStorageFile;</span><span class="sxs-lookup"><span data-stu-id="cfa18-885">'Get-AzStorageFile'</span></span>
    - <span data-ttu-id="cfa18-886">Remove-AzStorageFile;</span><span class="sxs-lookup"><span data-stu-id="cfa18-886">'Remove-AzStorageFile'</span></span>
    - <span data-ttu-id="cfa18-887">Get-AzStorageFileContent;</span><span class="sxs-lookup"><span data-stu-id="cfa18-887">'Get-AzStorageFileContent'</span></span>
    - <span data-ttu-id="cfa18-888">Set-AzStorageFileContent;</span><span class="sxs-lookup"><span data-stu-id="cfa18-888">'Set-AzStorageFileContent'</span></span>
    - <span data-ttu-id="cfa18-889">Start-AzStorageFileCopy.</span><span class="sxs-lookup"><span data-stu-id="cfa18-889">'Start-AzStorageFileCopy'</span></span>
* <span data-ttu-id="cfa18-890">Тип выходных данных изменен с CloudFileDirectory на AzureStorageFileDirectory. Первоначальные выходные данные теперь становятся дочерним элементом нового типа выходных данных.</span><span class="sxs-lookup"><span data-stu-id="cfa18-890">Changed output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="cfa18-891">New-AzStorageDirectory;</span><span class="sxs-lookup"><span data-stu-id="cfa18-891">'New-AzStorageDirectory'</span></span>
    - <span data-ttu-id="cfa18-892">Remove-AzStorageDirectory.</span><span class="sxs-lookup"><span data-stu-id="cfa18-892">'Remove-AzStorageDirectory'</span></span>
* <span data-ttu-id="cfa18-893">Тип выходных данных изменен с CloudFileShare на AzureStorageFileShare. Первоначальные выходные данные теперь становятся дочерним элементом нового типа выходных данных.</span><span class="sxs-lookup"><span data-stu-id="cfa18-893">Changed output type from CloudFileShare to AzureStorageFileShare, the original output will become a child property of the new output</span></span>
    - <span data-ttu-id="cfa18-894">Get-AzStorageShare;</span><span class="sxs-lookup"><span data-stu-id="cfa18-894">'Get-AzStorageShare'</span></span>
    - <span data-ttu-id="cfa18-895">New-AzStorageShare;</span><span class="sxs-lookup"><span data-stu-id="cfa18-895">'New-AzStorageShare'</span></span>
    - <span data-ttu-id="cfa18-896">Remove-AzStorageShare.</span><span class="sxs-lookup"><span data-stu-id="cfa18-896">'Remove-AzStorageShare'</span></span>
* <span data-ttu-id="cfa18-897">Тип выходных данных изменен с FileShareProperties на AzureStorageFileShare. Первоначальные выходные данные теперь становятся дочерним элементом нового типа выходных данных.</span><span class="sxs-lookup"><span data-stu-id="cfa18-897">Changed output type from FileShareProperties to AzureStorageFileShare, the original output will become a sub child property of the new output</span></span>
    - <span data-ttu-id="cfa18-898">Set-AzStorageShareQuota.</span><span class="sxs-lookup"><span data-stu-id="cfa18-898">'Set-AzStorageShareQuota'</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="cfa18-899">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="cfa18-899">Az.TrafficManager</span></span>
* <span data-ttu-id="cfa18-900">Исправлено неправильное имя профиля в подробных выходных данных DisableAzureTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="cfa18-900">Fixed incorrect profile name in 'DisableAzureTrafficManagerEndpoint' verbose output</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cfa18-901">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cfa18-901">Az.Websites</span></span>
* <span data-ttu-id="cfa18-902">Исправлена опечатка в справке по Update-AzWebAppAccessRestrictionConfig.</span><span class="sxs-lookup"><span data-stu-id="cfa18-902">Fixed typo on help of 'Update-AzWebAppAccessRestrictionConfig'.</span></span>

## <a name="380---april-2020"></a><span data-ttu-id="cfa18-903">3.8.0 — апрель 2020 г.</span><span class="sxs-lookup"><span data-stu-id="cfa18-903">3.8.0 - April 2020</span></span>
### <a name="highlights-since-the-last-release"></a><span data-ttu-id="cfa18-904">Основные сведения о новых возможностях с момента последнего выпуска</span><span class="sxs-lookup"><span data-stu-id="cfa18-904">Highlights since the last release</span></span>
* <span data-ttu-id="cfa18-905">Версии PowerShell, которые поддерживает Az.Storage: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span><span class="sxs-lookup"><span data-stu-id="cfa18-905">PowerShell versions that Az.Storage supports: Windows PowerShell 5.1, PowerShell Core 6.2.4+, PowerShell 7</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="cfa18-906">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cfa18-906">Az.Accounts</span></span>
* <span data-ttu-id="cfa18-907">Обновлен URL-адрес опроса Azure PowerShell в Resolve-AzError [11507].</span><span class="sxs-lookup"><span data-stu-id="cfa18-907">Updated Azure PowerShell survey URL in 'Resolve-AzError' [#11507]</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="cfa18-908">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cfa18-908">Az.ApiManagement</span></span>
* <span data-ttu-id="cfa18-909">Добавлено уведомление о критическом изменении для изменения выходных данных командлетов, выполняющих действия с файлами в Azure, в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="cfa18-909">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="cfa18-910">Обновлена документация для Set-AzApiManagementGroup с указанием параметра GroupId.</span><span class="sxs-lookup"><span data-stu-id="cfa18-910">'Set-AzApiManagementGroup' Updated documentation to specify the GroupId parameter</span></span>

#### <a name="azcdn"></a><span data-ttu-id="cfa18-911">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="cfa18-911">Az.Cdn</span></span>
* <span data-ttu-id="cfa18-912">Исправлено отображение ценовой категории (SKU), связанной с ChinaCDN.</span><span class="sxs-lookup"><span data-stu-id="cfa18-912">Fixed ChinaCDN related pricing SKU display</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cfa18-913">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cfa18-913">Az.CognitiveServices</span></span>
* <span data-ttu-id="cfa18-914">Включена поддержка Identity, Encryption, UserOwnedStorage.</span><span class="sxs-lookup"><span data-stu-id="cfa18-914">Supported Identity, Encryption, UserOwnedStorage</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cfa18-915">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cfa18-915">Az.Compute</span></span>
* <span data-ttu-id="cfa18-916">Добавлен командлет Set-AzVmssOrchestrationServiceState.</span><span class="sxs-lookup"><span data-stu-id="cfa18-916">Added 'Set-AzVmssOrchestrationServiceState' cmdlet.</span></span>
* <span data-ttu-id="cfa18-917">Get-AzVmss с параметром -InstanceView отображает состояния OrchestrationService.</span><span class="sxs-lookup"><span data-stu-id="cfa18-917">'Get-AzVmss' with -InstanceView shows OrchestrationService states.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cfa18-918">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cfa18-918">Az.IotHub</span></span>
* <span data-ttu-id="cfa18-919">Реализовано управление конфигурацией двойника устройства Интернета вещей. Новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="cfa18-919">Manage IoT device twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="cfa18-920">Get-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="cfa18-920">'Get-AzIotHubDeviceTwin'</span></span>
    - <span data-ttu-id="cfa18-921">Update-AzIotHubDeviceTwin</span><span class="sxs-lookup"><span data-stu-id="cfa18-921">'Update-AzIotHubDeviceTwin'</span></span>
* <span data-ttu-id="cfa18-922">Добавлен командлет для вызова прямого метода на устройстве в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="cfa18-922">Added cmdlet to invoke direct method on a device in an Iot Hub.</span></span>
* <span data-ttu-id="cfa18-923">Реализовано управление конфигурацией двойника модуля устройства Интернета вещей. Новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="cfa18-923">Manage IoT device module twin configuration, New cmdlets are:</span></span>
    - <span data-ttu-id="cfa18-924">Get-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="cfa18-924">'Get-AzIotHubModuleTwin'</span></span>
    - <span data-ttu-id="cfa18-925">Update-AzIotHubModuleTwin</span><span class="sxs-lookup"><span data-stu-id="cfa18-925">'Update-AzIotHubModuleTwin'</span></span>
* <span data-ttu-id="cfa18-926">Реализовано управление конфигурацией автоматического управления устройствами в центре Интернета вещей в большом масштабе.</span><span class="sxs-lookup"><span data-stu-id="cfa18-926">Manage IoT automatic device management configuration at scale.</span></span> <span data-ttu-id="cfa18-927">Ниже перечислены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="cfa18-927">New cmdlets are:</span></span>
    - <span data-ttu-id="cfa18-928">Add-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="cfa18-928">'Add-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="cfa18-929">Get-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="cfa18-929">'Get-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="cfa18-930">Remove-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="cfa18-930">'Remove-AzIotHubConfiguration'</span></span>
    - <span data-ttu-id="cfa18-931">Set-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="cfa18-931">'Set-AzIotHubConfiguration'</span></span>
* <span data-ttu-id="cfa18-932">Добавлен командлет для вызова метода периферийного модуля в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="cfa18-932">Added cmdlet to invoke an edge module method in an Iot Hub.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cfa18-933">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cfa18-933">Az.KeyVault</span></span>
* <span data-ttu-id="cfa18-934">Добавлен новый командлет Update-AzKeyVault, который может включать защиту от обратимого удаления и очистки в хранилище.</span><span class="sxs-lookup"><span data-stu-id="cfa18-934">Added a new cmdlet 'Update-AzKeyVault' that can enable soft delete and purge protection on a vault</span></span>
* <span data-ttu-id="cfa18-935">Включена поддержка Microsoft.PowerShell.SecretManagement [11178].</span><span class="sxs-lookup"><span data-stu-id="cfa18-935">Added support to Microsoft.PowerShell.SecretManagement [#11178]</span></span>
* <span data-ttu-id="cfa18-936">Исправлена ошибка в примерах Remove-AzKeyVaultManagedStorageSasDefinition [11479].</span><span class="sxs-lookup"><span data-stu-id="cfa18-936">Fixed error in the examples of 'Remove-AzKeyVaultManagedStorageSasDefinition' [#11479]</span></span>
* <span data-ttu-id="cfa18-937">Включена поддержка частной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="cfa18-937">Added support to private endpoint</span></span>

#### <a name="azmaintenance"></a><span data-ttu-id="cfa18-938">Az.Maintenance</span><span class="sxs-lookup"><span data-stu-id="cfa18-938">Az.Maintenance</span></span>
* <span data-ttu-id="cfa18-939">Опубликована версия выпуска командлетов обслуживания для общедоступной версии.</span><span class="sxs-lookup"><span data-stu-id="cfa18-939">Publishing release version of Maintenance cmdlets for GA</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cfa18-940">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cfa18-940">Az.Monitor</span></span>
* <span data-ttu-id="cfa18-941">Добавлены командлеты для области приватных каналов:</span><span class="sxs-lookup"><span data-stu-id="cfa18-941">Added cmdlets for private link scope</span></span>
    - <span data-ttu-id="cfa18-942">Get-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="cfa18-942">'Get-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="cfa18-943">Remove-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="cfa18-943">'Remove-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="cfa18-944">New-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="cfa18-944">'New-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="cfa18-945">Update-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="cfa18-945">'Update-AzInsightsPrivateLinkScope'</span></span>
    - <span data-ttu-id="cfa18-946">Get-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="cfa18-946">'Get-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="cfa18-947">New-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="cfa18-947">'New-AzInsightsPrivateLinkScopedResource'</span></span>
    - <span data-ttu-id="cfa18-948">Remove-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="cfa18-948">'Remove-AzInsightsPrivateLinkScopedResource'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cfa18-949">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cfa18-949">Az.Network</span></span>
* <span data-ttu-id="cfa18-950">Обновлены командлеты для включения подключения на частном IP-адресе для шлюза виртуальной сети:</span><span class="sxs-lookup"><span data-stu-id="cfa18-950">Updated cmdlets to enable connection on private IP for Virtual Network Gateway.</span></span>
    - <span data-ttu-id="cfa18-951">New-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cfa18-951">'New-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="cfa18-952">Set-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cfa18-952">'Set-AzVirtualNetworkGateway'</span></span>
    - <span data-ttu-id="cfa18-953">New-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="cfa18-953">'New-AzVirtualNetworkGatewayConnection'</span></span>
    - <span data-ttu-id="cfa18-954">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="cfa18-954">'Set-AzVirtualNetworkGatewayConnection'</span></span>
* <span data-ttu-id="cfa18-955">Обновлены командлеты для включения шлюзов LocalNetworkGateways и сайтов VpnSites на основе FQDN:</span><span class="sxs-lookup"><span data-stu-id="cfa18-955">Updated cmdlets to enable FQDN based LocalNetworkGateways and VpnSites</span></span>
    - <span data-ttu-id="cfa18-956">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cfa18-956">'New-AzLocalNetworkGateway'</span></span>
    - <span data-ttu-id="cfa18-957">New-AzVpnSiteLink</span><span class="sxs-lookup"><span data-stu-id="cfa18-957">'New-AzVpnSiteLink'</span></span>
* <span data-ttu-id="cfa18-958">Включена поддержка семейства адресов IPv6 в ExpressRouteCircuitConnectionConfig (Global Reach).</span><span class="sxs-lookup"><span data-stu-id="cfa18-958">Added support for IPv6 address family in ExpressRouteCircuitConnectionConfig (Global Reach)</span></span>
    - <span data-ttu-id="cfa18-959">Добавлен командлет Set-AzExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="cfa18-959">Added 'Set-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="cfa18-960">Позволяет выполнять настройку всех существующих свойств, включая IPv6CircuitConnectionProperties.</span><span class="sxs-lookup"><span data-stu-id="cfa18-960">allows setting of all the existing properties including the IPv6CircuitConnectionProperties</span></span>
    - <span data-ttu-id="cfa18-961">Обновлен командлет Add-AzExpressRouteCircuitConnectionConfig.</span><span class="sxs-lookup"><span data-stu-id="cfa18-961">Updated 'Add-AzExpressRouteCircuitConnectionConfig'</span></span>
        - <span data-ttu-id="cfa18-962">Добавлен еще один необязательный параметр AddressPrefixType для указания семейства адресов префикса адреса.</span><span class="sxs-lookup"><span data-stu-id="cfa18-962">Added another optional parameter AddressPrefixType to specify the address family of address prefix</span></span>
* <span data-ttu-id="cfa18-963">Обновлены командлеты для включения параметра времени ожидания для обнаружения неиспользуемых одноранговых узлов (DPD) в подключениях шлюзов виртуальных сетей.</span><span class="sxs-lookup"><span data-stu-id="cfa18-963">Updated cmdlets to enable setting of DPD Timeout on Virtual Network Gateway Connections.</span></span>
    - <span data-ttu-id="cfa18-964">New-AzVirtualNetworkGatewayConnection;</span><span class="sxs-lookup"><span data-stu-id="cfa18-964">New-AzVirtualNetworkGatewayConnection</span></span>
    - <span data-ttu-id="cfa18-965">Set-AzVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="cfa18-965">Set-AzVirtualNetworkGatewayConnection</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="cfa18-966">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="cfa18-966">Az.PolicyInsights</span></span>
* <span data-ttu-id="cfa18-967">Добавлен командлет Start-AzPolicyComplianceScan для запуска проверок соответствия политикам.</span><span class="sxs-lookup"><span data-stu-id="cfa18-967">Added 'Start-AzPolicyComplianceScan' cmdlet for triggering policy compliance scans</span></span>
* <span data-ttu-id="cfa18-968">Добавлены версии определения политики, определения набора и назначения в выходные данные командлета Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="cfa18-968">Added policy definition, set definition, and assignment versions to 'Get-AzPolicyState' output</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="cfa18-969">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cfa18-969">Az.ServiceFabric</span></span>
* <span data-ttu-id="cfa18-970">Улучшено форматирование и наглядность кода в примерах New-AzServiceFabricCluster.</span><span class="sxs-lookup"><span data-stu-id="cfa18-970">Improved code formatting and usability of 'New-AzServiceFabricCluster' examples</span></span>

#### <a name="azsql"></a><span data-ttu-id="cfa18-971">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cfa18-971">Az.Sql</span></span>
* <span data-ttu-id="cfa18-972">Добавлены командлеты Get-AzSqlInstanceOperation и Stop-AzSqlInstanceOperation.</span><span class="sxs-lookup"><span data-stu-id="cfa18-972">Added cmdlets 'Get-AzSqlInstanceOperation' and 'Stop-AzSqlInstanceOperation'</span></span>
* <span data-ttu-id="cfa18-973">Включен аудит учетной записи хранения в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="cfa18-973">Supported auditing to a storage account in VNet.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cfa18-974">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cfa18-974">Az.Storage</span></span>
* <span data-ttu-id="cfa18-975">Добавлено уведомление о критическом изменении для изменения выходных данных командлетов, выполняющих действия с файлами в Azure, в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="cfa18-975">Added breaking change notice for Azure File cmdlets output change in a future release</span></span>
* <span data-ttu-id="cfa18-976">Включена поддержка новых имен SKU StandardGZRS, StandardRAGZRS при создании или обновлении учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="cfa18-976">Supported new SkuName StandardGZRS, StandardRAGZRS when create/update Storage account</span></span>
    - <span data-ttu-id="cfa18-977">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cfa18-977">'New-AzStorageAccount'</span></span>
    - <span data-ttu-id="cfa18-978">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cfa18-978">'Set-AzStorageAccount'</span></span>
* <span data-ttu-id="cfa18-979">Добавлена поддержка DataLake 2-го поколения.</span><span class="sxs-lookup"><span data-stu-id="cfa18-979">Supported DataLake Gen2</span></span>
    - <span data-ttu-id="cfa18-980">New-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="cfa18-980">'New-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="cfa18-981">Get-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="cfa18-981">'Get-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="cfa18-982">Get-AzDataLakeGen2ChildItem</span><span class="sxs-lookup"><span data-stu-id="cfa18-982">'Get-AzDataLakeGen2ChildItem'</span></span>
    - <span data-ttu-id="cfa18-983">Move-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="cfa18-983">'Move-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="cfa18-984">Set-AzDataLakeGen2ItemAclObject</span><span class="sxs-lookup"><span data-stu-id="cfa18-984">'Set-AzDataLakeGen2ItemAclObject'</span></span>
    - <span data-ttu-id="cfa18-985">Update-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="cfa18-985">'Update-AzDataLakeGen2Item'</span></span>
    - <span data-ttu-id="cfa18-986">Get-AzDataLakeGen2ItemContent</span><span class="sxs-lookup"><span data-stu-id="cfa18-986">'Get-AzDataLakeGen2ItemContent'</span></span>
    - <span data-ttu-id="cfa18-987">Remove-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="cfa18-987">'Remove-AzDataLakeGen2Item'</span></span>

## <a name="0100-preview---april-2020"></a><span data-ttu-id="cfa18-988">0.10.0-preview — апрель 2020 г.</span><span class="sxs-lookup"><span data-stu-id="cfa18-988">0.10.0-preview - April 2020</span></span>
### <a name="general"></a><span data-ttu-id="cfa18-989">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="cfa18-989">General</span></span>
* <span data-ttu-id="cfa18-990">Модуль Az стали доступными в предварительной версии в Azure Stack Hub.</span><span class="sxs-lookup"><span data-stu-id="cfa18-990">Az modules is now available in preview on Azure Stack Hub.</span></span> <span data-ttu-id="cfa18-991">Это обеспечивает кросс-платформенную совместимость с Linux и macOs.</span><span class="sxs-lookup"><span data-stu-id="cfa18-991">This allows for cross-platform compatibility with Linux and macOs.</span></span> <span data-ttu-id="cfa18-992">Azure Stack Hub теперь поддерживает PowerShell Core с модулями Az (см. [дополнительные сведения](https://aka.ms/az4AzureStack))</span><span class="sxs-lookup"><span data-stu-id="cfa18-992">Azure Stack Hub now supports PowerShell core with the Az modules, more information [here](https://aka.ms/az4AzureStack)</span></span>
* <span data-ttu-id="cfa18-993">Модули Az поддерживают профиль 2019-03-01-hybrid:</span><span class="sxs-lookup"><span data-stu-id="cfa18-993">Az modules support profile 2019-03-01-hybrid:</span></span>
  - <span data-ttu-id="cfa18-994">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="cfa18-994">Az.Billing</span></span>
  - <span data-ttu-id="cfa18-995">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cfa18-995">Az.Compute</span></span>
  - <span data-ttu-id="cfa18-996">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="cfa18-996">Az.DataBoxEdge</span></span>
  - <span data-ttu-id="cfa18-997">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="cfa18-997">Az.EventHub</span></span>
  - <span data-ttu-id="cfa18-998">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cfa18-998">Az.IotHub</span></span>
  - <span data-ttu-id="cfa18-999">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cfa18-999">Az.KeyVault</span></span>
  - <span data-ttu-id="cfa18-1000">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cfa18-1000">Az.Monitor</span></span>
  - <span data-ttu-id="cfa18-1001">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cfa18-1001">Az.Network</span></span>
  - <span data-ttu-id="cfa18-1002">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cfa18-1002">Az.Resources</span></span>
  - <span data-ttu-id="cfa18-1003">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cfa18-1003">Az.Storage</span></span>
  - <span data-ttu-id="cfa18-1004">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cfa18-1004">Az.Websites</span></span>
* <span data-ttu-id="cfa18-1005">В PowerShell появились три новых модуля Az, которые работают с Azure Stack Hub: Az.Databox, Az.IotHub и Az.EventHub.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1005">Three new PowerShell modules for az have been introduced that work with Azure Stack Hub, which are Az.Databox, Az.IotHub, and Az.EventHub</span></span>
* <span data-ttu-id="cfa18-1006">Команды остаются прежними же за исключением незначительных изменений, таких как изменение AzureRM на Az.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1006">Commands remain relatively the same, with minor changes such as changing AzureRM to Az</span></span>
* <span data-ttu-id="cfa18-1007">См. обновленную ссылку на документацию по [PowerShell для Azure Stack Hub](https://aka.ms/InstallASHPowerShell)</span><span class="sxs-lookup"><span data-stu-id="cfa18-1007">Updated link to PowerShell documentation for Azure Stack Hub can be found [here](https://aka.ms/InstallASHPowerShell)</span></span>

## <a name="370---march-2020"></a><span data-ttu-id="cfa18-1008">3.7.0 — март 2020 г.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1008">3.7.0 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cfa18-1009">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cfa18-1009">Az.Accounts</span></span>
* <span data-ttu-id="cfa18-1010">Исправлено исключение NullReferenceException командлетов Get-AzTenant/Get-AzDefault/Set-AzDefault, если вход не выполнен [10292]</span><span class="sxs-lookup"><span data-stu-id="cfa18-1010">Fixed 'Get-AzTenant'/'Get-AzDefault'/'Set-AzDefault' throw NullReferenceException when not login [#10292]</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cfa18-1011">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cfa18-1011">Az.Compute</span></span>
* <span data-ttu-id="cfa18-1012">Добавлены следующие параметры к командлету New-AzDiskConfig:</span><span class="sxs-lookup"><span data-stu-id="cfa18-1012">Added the following parameters to 'New-AzDiskConfig' cmdlet:</span></span>
    - <span data-ttu-id="cfa18-1013">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span><span class="sxs-lookup"><span data-stu-id="cfa18-1013">DiskIOPSReadOnly, DiskMBpsReadOnly, MaxSharesCount, GalleryImageReference</span></span>
* <span data-ttu-id="cfa18-1014">Разрешено свойство Encryption для параметра Target командлета New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1014">Allowed Encryption property to Target parameter of 'New-AzGalleryImageVersion' cmdlet.</span></span>
* <span data-ttu-id="cfa18-1015">Исправлена проблема с tempDisk для командлетов Set-AzVmss -Reimage и Invoke-AzVMReimage.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1015">Fixed tempDisk issue for 'Set-AzVmss' -Reimage and 'Invoke-AzVMReimage' cmdlets.</span></span> <span data-ttu-id="cfa18-1016">[11354]</span><span class="sxs-lookup"><span data-stu-id="cfa18-1016">[#11354]</span></span>
* <span data-ttu-id="cfa18-1017">Добавлена поддержка нового расширения SAP для указанных ниже командлетов</span><span class="sxs-lookup"><span data-stu-id="cfa18-1017">Added support to below cmdlets for new SAP Extension</span></span>
    - <span data-ttu-id="cfa18-1018">Set-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="cfa18-1018">'Set-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="cfa18-1019">Get-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="cfa18-1019">'Get-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="cfa18-1020">Remove-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="cfa18-1020">'Remove-AzVMAEMExtension'</span></span>
    - <span data-ttu-id="cfa18-1021">Update-AzVMAEMExtension</span><span class="sxs-lookup"><span data-stu-id="cfa18-1021">'Update-AzVMAEMExtension'</span></span>
* <span data-ttu-id="cfa18-1022">Исправлены ошибки в примерах справки</span><span class="sxs-lookup"><span data-stu-id="cfa18-1022">Fixed errors in examples of help document</span></span>
* <span data-ttu-id="cfa18-1023">Показано точное строковое значение в табличном формате для свойства PowerState виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1023">Showed the exact string value for VM PowerState in the table format.</span></span>
* <span data-ttu-id="cfa18-1024">New-AzVmssConfig: исправлена сериализация свойства AutomaticRepairs, если параметр SinglePlacementGroup отключен.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1024">'New-AzVmssConfig': fixed serialization of AutomaticRepairs property when SinglePlacementGroup is disabled.</span></span> <span data-ttu-id="cfa18-1025">[11257]</span><span class="sxs-lookup"><span data-stu-id="cfa18-1025">[#11257]</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cfa18-1026">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cfa18-1026">Az.DataFactory</span></span>
* <span data-ttu-id="cfa18-1027">Пакет SDK ADF для .NET обновлен до версии 4.8.0.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1027">Updated ADF .Net SDK version to 4.8.0</span></span>
* <span data-ttu-id="cfa18-1028">Добавлены необязательные параметры для команды Invoke-AzDataFactoryV2Pipeline для поддержки повторного запуска.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1028">Added optional parameters to 'Invoke-AzDataFactoryV2Pipeline' command to support rerun</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cfa18-1029">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cfa18-1029">Az.DataLakeStore</span></span>
* <span data-ttu-id="cfa18-1030">Добавлено описание критического изменения для Export-AzDataLakeStoreItem и Import-AzDataLakeStoreItem.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1030">Added breaking change description for 'Export-AzDataLakeStoreItem' and 'Import-AzDataLakeStoreItem'</span></span>
* <span data-ttu-id="cfa18-1031">Добавлен параметр кодирования байтов для New-AzDataLakeStoreItem, Add-AzDAtaLakeStoreItemContent и Get-AzDAtaLakeStoreItemContent.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1031">Added option of Byte encoding for 'New-AzDataLakeStoreItem', 'Add-AzDAtaLakeStoreItemContent', and 'Get-AzDAtaLakeStoreItemContent'</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="cfa18-1032">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cfa18-1032">Az.HDInsight</span></span>
* <span data-ttu-id="cfa18-1033">Добавлена поддержка указания минимальной поддерживаемой версии TLS при создании кластера.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1033">Supported specifying minimal supported TLS version when creating cluster.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cfa18-1034">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cfa18-1034">Az.IotHub</span></span>
* <span data-ttu-id="cfa18-1035">Добавлена поддержка для управления распределенными параметрами на отдельных устройствах.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1035">Added support to manage distributed settings per-device.</span></span> <span data-ttu-id="cfa18-1036">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1036">New Cmdlets are:</span></span>
    - <span data-ttu-id="cfa18-1037">Get-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="cfa18-1037">'Get-AzIotHubDistributedTracing'</span></span>
    - <span data-ttu-id="cfa18-1038">Set-AzIotHubDistributedTracing</span><span class="sxs-lookup"><span data-stu-id="cfa18-1038">'Set-AzIotHubDistributedTracing'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cfa18-1039">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cfa18-1039">Az.KeyVault</span></span>
* <span data-ttu-id="cfa18-1040">Добавлены атрибуты критических изменений для New-AzKeyVault.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1040">Added breaking change attributes to 'New-AzKeyVault'</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cfa18-1041">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cfa18-1041">Az.Monitor</span></span>
* <span data-ttu-id="cfa18-1042">Обновлена документация для New-AzScheduledQueryRuleLogMetricTrigger.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1042">Updated documentation for 'New-AzScheduledQueryRuleLogMetricTrigger'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cfa18-1043">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cfa18-1043">Az.Network</span></span>
* <span data-ttu-id="cfa18-1044">Обновлены командлеты для поддержки подключений VirtualHubVnetConnections между клиентами</span><span class="sxs-lookup"><span data-stu-id="cfa18-1044">Updated cmdlets to allow cross-tenant VirtualHubVnetConnections</span></span>
    - <span data-ttu-id="cfa18-1045">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="cfa18-1045">'New-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="cfa18-1046">Update-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="cfa18-1046">'Update-AzVirtualHubVnetConnection'</span></span>
    - <span data-ttu-id="cfa18-1047">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="cfa18-1047">'New-AzVirtualHub'</span></span>
    - <span data-ttu-id="cfa18-1048">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="cfa18-1048">'Update-AzVirtualHub'</span></span>
* <span data-ttu-id="cfa18-1049">Удалена зависимость пакета SDK для управления SQL.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1049">Removed Sql Management SDK dependency</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="cfa18-1050">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="cfa18-1050">Az.PolicyInsights</span></span>
* <span data-ttu-id="cfa18-1051">Улучшены сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1051">Improved error messages</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cfa18-1052">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cfa18-1052">Az.RecoveryServices</span></span>
* <span data-ttu-id="cfa18-1053">В Azure Site Recovery реализована поддержка повторной защиты и обновлены свойства зашифрованных виртуальных машин диска Azure.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1053">Azure Site Recovery added support for doing reprotect and updated vm properties for Azure disk encrypted Virtual Machines.</span></span>
* <span data-ttu-id="cfa18-1054">Добавлена возможность мониторинг аварийного восстановления для свойств VmwareToAzure в Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1054">Added Azure Site Recovery VmwareToAzure properties DR monitoring</span></span>
* <span data-ttu-id="cfa18-1055">В Azure Backup реализована поддержка повторного обновления политики для элементов с ошибками.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1055">Azure Backup added support for retrying policy update for failed items.</span></span>
* <span data-ttu-id="cfa18-1056">В Azure Backup реализована поддержка параметров исключения диска во время резервного копирования и восстановления.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1056">Azure Backup Added support for disk exclusion settings during backup and restore.</span></span>
* <span data-ttu-id="cfa18-1057">В Azure Backup реализована поддержка восстановления нескольких файлов или папок в AzureFileShare</span><span class="sxs-lookup"><span data-stu-id="cfa18-1057">Azure Backup Added Support for Restoring Multiple files/folders in AzureFileShare</span></span>
* <span data-ttu-id="cfa18-1058">В Azure Backup реализована поддержка указанной пользователем группы Resourcegroup при обновлении политики IaasVM.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1058">Azure Backup Added support for User-specified Resourcegroup support while updating IaasVM Policy</span></span>

#### <a name="azresources"></a><span data-ttu-id="cfa18-1059">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cfa18-1059">Az.Resources</span></span>
* <span data-ttu-id="cfa18-1060">Исправлена команда Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType для использования фактической версии apiVersion ресурсов (а не версии apiVersion по умолчанию) [11267].</span><span class="sxs-lookup"><span data-stu-id="cfa18-1060">Fixed 'Get-AzResource -ResourceGroupName -Name -ExpandProperties -ResourceType' to use actual apiVersion of resources instead of default apiVersion [#11267]</span></span>
* <span data-ttu-id="cfa18-1061">Добавлена возможность регистрации correlationId для сценариев с ошибками.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1061">Added correlationId logging for error scenarios</span></span>
* <span data-ttu-id="cfa18-1062">Незначительно изменена документация по Get-AzResourceLock.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1062">Small documentation change to 'Get-AzResourceLock'.</span></span> <span data-ttu-id="cfa18-1063">Добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1063">Added example.</span></span>
* <span data-ttu-id="cfa18-1064">Экранирована одинарная кавычка в значении параметра Get-AzADUser [11317].</span><span class="sxs-lookup"><span data-stu-id="cfa18-1064">Escaped single quote in parameter value of 'Get-AzADUser' [#11317]</span></span>
* <span data-ttu-id="cfa18-1065">Добавлены новые командлеты для сценариев развертывания (Get-AzDeploymentScript, Get-AzDeploymentScriptLog, Save-AzDeploymentScriptLog, Remove-AzDeploymentScript).</span><span class="sxs-lookup"><span data-stu-id="cfa18-1065">Added new cmdlets for Deployment Scripts ('Get-AzDeploymentScript', 'Get-AzDeploymentScriptLog', 'Save-AzDeploymentScriptLog', 'Remove-AzDeploymentScript')</span></span>

#### <a name="azsql"></a><span data-ttu-id="cfa18-1066">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cfa18-1066">Az.Sql</span></span>
* <span data-ttu-id="cfa18-1067">Добавлен параметр вторичной реплики для чтения для командлета Invoke-AzSqlDatabaseFailover.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1067">Added readable secondary parameter to 'Invoke-AzSqlDatabaseFailover'</span></span>
* <span data-ttu-id="cfa18-1068">Добавлен командлет Disable-AzSqlServerActiveDirectoryOnlyAuthentication.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1068">Added cmdlet 'Disable-AzSqlServerActiveDirectoryOnlyAuthentication'</span></span>
* <span data-ttu-id="cfa18-1069">Сохранен приоритет конфиденциальности при классификации столбцов в базе данных.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1069">Saved sensitivity rank when classifying columns in the database.</span></span>

#### <a name="azsupport"></a><span data-ttu-id="cfa18-1070">Az.Support</span><span class="sxs-lookup"><span data-stu-id="cfa18-1070">Az.Support</span></span>
* <span data-ttu-id="cfa18-1071">Модуль Az.Support стал общедоступным.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1071">General availability of 'Az.Support' module</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cfa18-1072">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cfa18-1072">Az.Websites</span></span>
* <span data-ttu-id="cfa18-1073">Реализована поддержка работы с правилами маршрутизации трафика веб-приложения через указанные ниже командлеты</span><span class="sxs-lookup"><span data-stu-id="cfa18-1073">Added support for working with webapp Traffic Routing Rules via below new cmdlets</span></span>
    - <span data-ttu-id="cfa18-1074">Get-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="cfa18-1074">'Get-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="cfa18-1075">Update-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="cfa18-1075">'Update-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="cfa18-1076">Add-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="cfa18-1076">'Add-AzWebAppTrafficRouting'</span></span>
    - <span data-ttu-id="cfa18-1077">Remove-AzWebAppTrafficRouting</span><span class="sxs-lookup"><span data-stu-id="cfa18-1077">'Remove-AzWebAppTrafficRouting'</span></span>

## <a name="361---march-2020"></a><span data-ttu-id="cfa18-1078">3.6.1 — март 2020 г.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1078">3.6.1 - March 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cfa18-1079">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cfa18-1079">Az.Accounts</span></span>
* <span data-ttu-id="cfa18-1080">Открытие страницы опроса Azure PowerShell в Send-Feedback [11020].</span><span class="sxs-lookup"><span data-stu-id="cfa18-1080">Open Azure PowerShell survey page in 'Send-Feedback' [#11020]</span></span>
* <span data-ttu-id="cfa18-1081">Отображение URL-адреса опроса Azure PowerShell в Resolve-Error [11021].</span><span class="sxs-lookup"><span data-stu-id="cfa18-1081">Display Azure PowerShell survey URL in 'Resolve-Error' [#11021]</span></span>
* <span data-ttu-id="cfa18-1082">Добавлена версия Az в UserAgent.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1082">Added Az version in UserAgent</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="cfa18-1083">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cfa18-1083">Az.ApiManagement</span></span>
* <span data-ttu-id="cfa18-1084">Включена поддержка получения и настройки личного домена в конечной точке DeveloperPortal [11007].</span><span class="sxs-lookup"><span data-stu-id="cfa18-1084">Added support for retrieving and configuring Custom Domain on the DeveloperPortal Endpoint [#11007]</span></span>
* <span data-ttu-id="cfa18-1085">Export-AzApiManagementApi: включена поддержка скачивания определения API в формате JSON [9987].</span><span class="sxs-lookup"><span data-stu-id="cfa18-1085">'Export-AzApiManagementApi' Added support for downloading Api Definition in Json format [#9987]</span></span>
* <span data-ttu-id="cfa18-1086">Import-AzApiManagementApi: включена поддержка импорта определения OpenApi 3.0 из документа JSON.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1086">'Import-AzApiManagementApi' Added support for importing OpenApi 3.0 definition from Json document</span></span>
* <span data-ttu-id="cfa18-1087">New-AzApiManagementIdentityProvider и Set-AzApiManagementIdentityProvider: включена поддержка настройки входа арендатора для поставщика AAD B2C [9784].</span><span class="sxs-lookup"><span data-stu-id="cfa18-1087">'New-AzApiManagementIdentityProvider' and 'Set-AzApiManagementIdentityProvider' Added support for configuring 'Signin Tenant' for AAD B2C Provider [#9784]</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cfa18-1088">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cfa18-1088">Az.DataLakeStore</span></span>
* <span data-ttu-id="cfa18-1089">Добавлена ссылка на System.Buffers явным образом в CSPROJ и PSD1.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1089">Added reference to System.Buffers explicitly in csproj and psd1.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cfa18-1090">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cfa18-1090">Az.IotHub</span></span>
* <span data-ttu-id="cfa18-1091">Добавлена возможность управления устройствами в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1091">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="cfa18-1092">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1092">New Cmdlets are:</span></span>
    - <span data-ttu-id="cfa18-1093">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="cfa18-1093">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="cfa18-1094">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="cfa18-1094">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="cfa18-1095">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="cfa18-1095">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="cfa18-1096">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="cfa18-1096">'Set-AzIotHubDevice'</span></span>
* <span data-ttu-id="cfa18-1097">Включена поддержка управления модулями в целевом устройстве Интернета вещей в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1097">Added support to manage modules on a target Iot device in an Iot Hub.</span></span> <span data-ttu-id="cfa18-1098">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1098">New Cmdlets are:</span></span>
    - <span data-ttu-id="cfa18-1099">Add-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="cfa18-1099">'Add-AzIotHubModule'</span></span>
    - <span data-ttu-id="cfa18-1100">Get-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="cfa18-1100">'Get-AzIotHubModule'</span></span>
    - <span data-ttu-id="cfa18-1101">Remove-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="cfa18-1101">'Remove-AzIotHubModule'</span></span>
    - <span data-ttu-id="cfa18-1102">Set-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="cfa18-1102">'Set-AzIotHubModule'</span></span>
* <span data-ttu-id="cfa18-1103">Добавлен командлет для получения строки подключения целевого устройства Интернета вещей в центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1103">Added cmdlet to get the connection string of a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="cfa18-1104">Добавлен командлет для получения строки подключения модуля на целевом устройстве Интернета вещей в центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1104">Added cmdlet to get the connection string of a module on a target IoT device in an Iot Hub.</span></span>
* <span data-ttu-id="cfa18-1105">Включена поддержка для получения или настройки родительского устройства для устройства Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1105">Added support to get/set parent device of an IoT device.</span></span> <span data-ttu-id="cfa18-1106">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1106">New Cmdlets are:</span></span>
    - <span data-ttu-id="cfa18-1107">Get-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="cfa18-1107">'Get-AzIotHubDeviceParent'</span></span>
    - <span data-ttu-id="cfa18-1108">Set-AzIotHubDeviceParent</span><span class="sxs-lookup"><span data-stu-id="cfa18-1108">'Set-AzIotHubDeviceParent'</span></span>
* <span data-ttu-id="cfa18-1109">Включена поддержка управления связью "родители — потомки" устройства.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1109">Added support to manage device parent-child relationship.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cfa18-1110">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cfa18-1110">Az.Monitor</span></span>
* <span data-ttu-id="cfa18-1111">Исправлено выходное значение для Get-AzMetricDefinition [9714].</span><span class="sxs-lookup"><span data-stu-id="cfa18-1111">Fixed output value for 'Get-AzMetricDefinition' [#9714]</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cfa18-1112">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cfa18-1112">Az.Network</span></span>
* <span data-ttu-id="cfa18-1113">Обновлен пакет SDK для управления SQL.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1113">Updated Sql Management SDK.</span></span>
* <span data-ttu-id="cfa18-1114">Исправлена проблема с разницей в именовании в классе PrivateLinkServiceConnectionState.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1114">Fixed a naming-difference issue in PrivateLinkServiceConnectionState class.</span></span>
    - <span data-ttu-id="cfa18-1115">Сопоставление ActionsRequired с ActionRequired.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1115">Mapping the field ActionsRequired to ActionRequired.</span></span>
* <span data-ttu-id="cfa18-1116">Добавление PublicNetworkAccess в команды New-AzSqlServer и Set-AzSqlServer.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1116">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>

#### <a name="azresources"></a><span data-ttu-id="cfa18-1117">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cfa18-1117">Az.Resources</span></span>
* <span data-ttu-id="cfa18-1118">Исправлена ошибка пустой ссылки в Get-AzRoleAssignment.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1118">Fixed for null reference bug in 'Get-AzRoleAssignment'</span></span>
* <span data-ttu-id="cfa18-1119">Параметры -Force и -PassThru помечены необязательными в Remove-AzADGroup [10849].</span><span class="sxs-lookup"><span data-stu-id="cfa18-1119">Marked switch '-Force' and '-PassThru' optional in 'Remove-AzADGroup' [#10849]</span></span>
* <span data-ttu-id="cfa18-1120">Исправлена ошибка, из-за которой MailNickname не возвращается в Remove-AzADGroup [11167].</span><span class="sxs-lookup"><span data-stu-id="cfa18-1120">Fixed issue that 'MailNickname' doesn't return in 'Remove-AzADGroup' [#11167]</span></span>
* <span data-ttu-id="cfa18-1121">Исправлена ошибка, из-за которой операция канала Remove-AzADGroup не работает [11171].</span><span class="sxs-lookup"><span data-stu-id="cfa18-1121">Fixed issue that 'Remove-AzADGroup' pipe operation doesn't work [#11171]</span></span>
* <span data-ttu-id="cfa18-1122">Исправлена ошибка с пустой ссылкой в GetAzureRoleAssignmentCommand.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1122">Fixed for null reference bug in GetAzureRoleAssignmentCommand</span></span>
* <span data-ttu-id="cfa18-1123">Добавлено критическое изменение атрибутов для будущих изменений командлетов политик.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1123">Added breaking change attributes for upcoming changes to policy cmdlets</span></span>
* <span data-ttu-id="cfa18-1124">Обновлена команда Get-AzResourceGroup для выполнения фильтрации тегов группы ресурсов на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1124">Updated 'Get-AzResourceGroup' to perform resource group tag filtering on server-side</span></span>
* <span data-ttu-id="cfa18-1125">Расширены командлеты Tag для включения поддержки параметра -ResourceId.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1125">Extended Tag cmdlets to accept -ResourceId</span></span>
    - <span data-ttu-id="cfa18-1126">Get-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="cfa18-1126">Get-AzTag -ResourceId</span></span>
    - <span data-ttu-id="cfa18-1127">New-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="cfa18-1127">New-AzTag -ResourceId</span></span>
    - <span data-ttu-id="cfa18-1128">Remove-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="cfa18-1128">Remove-AzTag -ResourceId</span></span>
* <span data-ttu-id="cfa18-1129">Добавлен новый командлет Tag.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1129">Added new Tag cmdlet</span></span>
    - <span data-ttu-id="cfa18-1130">Update-AzTag -ResourceId</span><span class="sxs-lookup"><span data-stu-id="cfa18-1130">Update-AzTag -ResourceId</span></span>
* <span data-ttu-id="cfa18-1131">Предоставляется ScopedDeployment из пакета SDK 3.3.0.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1131">Brought ScopedDeployment from SDK 3.3.0</span></span>

#### <a name="azsql"></a><span data-ttu-id="cfa18-1132">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cfa18-1132">Az.Sql</span></span>
* <span data-ttu-id="cfa18-1133">Добавление PublicNetworkAccess в команды New-AzSqlServer и Set-AzSqlServer.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1133">Added PublicNetworkAccess to 'New-AzSqlServer' and 'Set-AzSqlServer'</span></span>
* <span data-ttu-id="cfa18-1134">Включена поддержка конфигурации резервного копирования долгосрочного хранения для управляемых баз данных.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1134">Added support for Long Term Retention backup configuration for Managed Databases</span></span>
    - <span data-ttu-id="cfa18-1135">Получение или настройка политики LTR в управляемой базе данных.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1135">Get/Set LTR policy on a managed database</span></span>
    - <span data-ttu-id="cfa18-1136">Получение резервных копий LTR по управляемой базе данных, управляемому экземпляру или расположению.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1136">Get LTR backup(s) by managed database, managed instance, or by location</span></span>
    - <span data-ttu-id="cfa18-1137">Удаление резервной копии LTR.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1137">Remove an LTR backup</span></span>
    - <span data-ttu-id="cfa18-1138">Восстановление резервной копии LTR для создания новой управляемой базы данных.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1138">Restore an LTR backup to create a new managed database</span></span>
* <span data-ttu-id="cfa18-1139">Добавление MinimalTlsVersion в New-AzSqlServer и Set-AzSqlServer.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1139">Added MinimalTlsVersion to New-AzSqlServer and Set-AzSqlServer</span></span>
* <span data-ttu-id="cfa18-1140">Добавление MinimalTlsVersion в New-AzSqlInstance и Set-AzSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1140">Added MinimalTlsVersion to New-AzSqlInstance and Set-AzSqlInstance</span></span>
* <span data-ttu-id="cfa18-1141">Обновлена версия пакета SDK для SQL для Az.Network.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1141">Bumped SQL SDK version for Az.Network</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cfa18-1142">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cfa18-1142">Az.Storage</span></span>
* <span data-ttu-id="cfa18-1143">Включена поддержка AllowProtectedAppendWrite в ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1143">Supported AllowProtectedAppendWrite in ImmutabilityPolicy</span></span>
    - <span data-ttu-id="cfa18-1144">Set-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="cfa18-1144">'Set-AzRmStorageContainerImmutabilityPolicy'</span></span>
* <span data-ttu-id="cfa18-1145">Добавлено предупреждение о критическом изменении для изменения типа AzureStorageTable в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1145">Added breaking change warning message for AzureStorageTable type change in a future release</span></span>
    - <span data-ttu-id="cfa18-1146">New-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="cfa18-1146">'New-AzStorageTable'</span></span>
    - <span data-ttu-id="cfa18-1147">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="cfa18-1147">'Get-AzStorageTable'</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cfa18-1148">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cfa18-1148">Az.Websites</span></span>
* <span data-ttu-id="cfa18-1149">Добавлен параметр Tag для New-AzAppServicePlan и Set-AzAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1149">Added Tag parameter for 'New-AzAppServicePlan' and 'Set-AzAppServicePlan'</span></span>
* <span data-ttu-id="cfa18-1150">Завершение выполнения командлета, если при добавлении личного домена на веб-сайт возникает исключение.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1150">Stop cmdlet execution if an exception is thrown when adding a custom domain to a website</span></span>
* <span data-ttu-id="cfa18-1151">Включена поддержка выполнения операций для Служб приложений, которые находятся не в той же группе ресурсов, что и план службы приложений.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1151">Added support to perform operations for App Services not in the same resource group as the App Service Plan</span></span>
* <span data-ttu-id="cfa18-1152">Применение ограничения доступа к WebApp/Function в разных группах ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1152">Applied access restriction to WebApp/Function in different resource groups</span></span>
* <span data-ttu-id="cfa18-1153">Исправлена ошибка с указанием пользовательских имен узлов для WebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1153">Fixed issue to set custom hostnames for WebAppSlots</span></span>

## <a name="350---february-2020"></a><span data-ttu-id="cfa18-1154">3.5.0 — февраль 2020 г.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1154">3.5.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="cfa18-1155">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="cfa18-1155">Highlights since the last major release</span></span>
* <span data-ttu-id="cfa18-1156">Обновлены данные телеметрии на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1156">Updated client side telemetry.</span></span>
* <span data-ttu-id="cfa18-1157">В Az.IotHub добавлены командлеты для управления устройствами.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1157">Az.IotHub added cmdlets to support to manage devices.</span></span>
* <span data-ttu-id="cfa18-1158">В Az.SqlVirtualMachine добавлены командлеты для прослушивателя группы доступности.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1158">Az.SqlVirtualMachine added cmdlets for Availability Group Listener.</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="cfa18-1159">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cfa18-1159">Az.Accounts</span></span>
* <span data-ttu-id="cfa18-1160">В данные телеметрии на стороне клиента добавлены такие сведения, как идентификатор подписки, идентификатор арендатора и время выполнения.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1160">Added SubscriptionId, TenantId, and execution time into data of client side telemetry</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cfa18-1161">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cfa18-1161">Az.Automation</span></span>
* <span data-ttu-id="cfa18-1162">Исправлена опечатка в примере 1 в справочной документации по New-AzAutomationSoftwareUpdateConfiguration.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1162">Fixed typo in Example 1 in reference documentation for 'New-AzAutomationSoftwareUpdateConfiguration'</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cfa18-1163">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cfa18-1163">Az.CognitiveServices</span></span>
* <span data-ttu-id="cfa18-1164">Обновлен пакет SDK до версии 7.0.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1164">Updated SDK to 7.0</span></span>
* <span data-ttu-id="cfa18-1165">Улучшено сообщение об ошибке, которое появляется, если ответы сервера не содержат текст.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1165">Improved error message when server responses empty body</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cfa18-1166">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cfa18-1166">Az.Compute</span></span>
* <span data-ttu-id="cfa18-1167">Разрешено использовать пустое значение для ProximityPlacementGroupId во время обновления.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1167">Allowed empty value for ProximityPlacementGroupId during update</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="cfa18-1168">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="cfa18-1168">Az.FrontDoor</span></span>
* <span data-ttu-id="cfa18-1169">Добавлен командлет для получения определений управляемых правил, которые могут использоваться в WAF.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1169">Added cmdlet to get managed rule definitions that can be used in WAF</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cfa18-1170">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cfa18-1170">Az.IotHub</span></span>
* <span data-ttu-id="cfa18-1171">Добавлена возможность управления устройствами в Центре Интернета вещей.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1171">Added support to manage devices in an Iot Hub.</span></span> <span data-ttu-id="cfa18-1172">Ниже перечислены новые командлеты.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1172">New Cmdlets are:</span></span>
    - <span data-ttu-id="cfa18-1173">Add-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="cfa18-1173">'Add-AzIotHubDevice'</span></span>
    - <span data-ttu-id="cfa18-1174">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="cfa18-1174">'Get-AzIotHubDevice'</span></span>
    - <span data-ttu-id="cfa18-1175">Remove-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="cfa18-1175">'Remove-AzIotHubDevice'</span></span>
    - <span data-ttu-id="cfa18-1176">Set-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="cfa18-1176">'Set-AzIotHubDevice'</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cfa18-1177">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cfa18-1177">Az.KeyVault</span></span>
* <span data-ttu-id="cfa18-1178">Устранен дублирующийся текст для Add-AzKeyVaultKey.md.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1178">Fixed duplicated text for Add-AzKeyVaultKey.md</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cfa18-1179">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cfa18-1179">Az.Monitor</span></span>
* <span data-ttu-id="cfa18-1180">Исправлено описание командлета Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1180">Fixed description of the Get-AzLog cmdlet.</span></span>
* <span data-ttu-id="cfa18-1181">В команду New-AzMetricAlertRuleV2 добавлен новый параметр ActionGroupId.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1181">A new parameter called ActionGroupId was added to 'New-AzMetricAlertRuleV2' command.</span></span>
    - <span data-ttu-id="cfa18-1182">Пользователь может предоставить ActionGroupId(string) или ActionGorup(ActivityLogAlertActionGroup).</span><span class="sxs-lookup"><span data-stu-id="cfa18-1182">The user can provide either ActionGroupId(string) or ActionGorup(ActivityLogAlertActionGroup).</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cfa18-1183">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cfa18-1183">Az.Network</span></span>
* <span data-ttu-id="cfa18-1184">Добавлен еще один параметр -EnableProxyProtocol для командлета New-AzPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1184">Added one extra parameter note for parameter '-EnableProxyProtocol' for 'New-AzPrivateLinkService' cmdlet.</span></span>
* <span data-ttu-id="cfa18-1185">Исправлен пример FilterData в Start-AzVirtualNetworkGatewayConnectionPacketCapture.md и Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1185">Fixed FilterData example in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="cfa18-1186">Добавлен пример Packet Capture для всех внутренних и внешних пакетов в Start-AzVirtualNetworkGatewayConnectionPacketCapture.md и Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1186">Added Packet Capture example for capture all inner and outer packets in Start-AzVirtualNetworkGatewayConnectionPacketCapture.md and Start-AzVirtualnetworkGatewayPacketCapture.md.</span></span>
* <span data-ttu-id="cfa18-1187">Добавлена поддерживаемая политика Брандмауэра Azure в брандмауэрах виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1187">Supported Azure Firewall Policy on VNet Firewalls</span></span>
    - <span data-ttu-id="cfa18-1188">Новые командлеты не добавлены.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1188">No new cmdlets are added.</span></span> <span data-ttu-id="cfa18-1189">Снято ограничение политики брандмауэра в брандмауэрах виртуальных сетей.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1189">Relaxing the restriction for firewall policy on VNet firewalls</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cfa18-1190">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cfa18-1190">Az.RecoveryServices</span></span>
* <span data-ttu-id="cfa18-1191">Добавлена возможность восстановления в виде файлов для Баз данных SQL.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1191">Added Support for Restore-as-files for SQL Databases.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cfa18-1192">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cfa18-1192">Az.Resources</span></span>
* <span data-ttu-id="cfa18-1193">Выполнен рефакторинг командлетов развертывания шаблона.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1193">Refactored template deployment cmdlets</span></span>
    - <span data-ttu-id="cfa18-1194">Добавлены новые командлеты для управления развертываниями в группе управления: \*-AzManagementGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1194">Added new cmdlets for managing deployments at management group: \*-AzManagementGroupDeployment</span></span>
    - <span data-ttu-id="cfa18-1195">Добавлены новые командлеты для управления развертываниями в области арендатора: \*-AzTenantDeployment.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1195">Added new cmdlets for managing deployments at tenant scope: \*-AzTenantDeployment</span></span>
    - <span data-ttu-id="cfa18-1196">Выполнен рефакторинг командлетов \*-AzDeployment для работы в области подписки.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1196">Refactored \*-AzDeployment cmdlets to work specifically at subscription scope</span></span>
    - <span data-ttu-id="cfa18-1197">Созданы псевдонимы \*-AzSubscriptionDeployment для командлетов \*-AzDeployment.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1197">Created aliases \*-AzSubscriptionDeployment for \*-AzDeployment cmdlets</span></span>
* <span data-ttu-id="cfa18-1198">Исправлен командлет Update-AzADApplication, когда параметр AvailableToOtherTenants не задан.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1198">Fixed 'Update-AzADApplication' when parameter 'AvailableToOtherTenants' is not set</span></span>
* <span data-ttu-id="cfa18-1199">Удален набор параметров ApplicationObjectWithoutCredentialParameterSet, чтобы предотвратить возникновение AmbiguousParameterSetException.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1199">Removed ApplicationObjectWithoutCredentialParameterSet to avoid AmbiguousParameterSetException.</span></span>
* <span data-ttu-id="cfa18-1200">Повторно созданы файлы справки.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1200">Regenerated help files</span></span>

#### <a name="azsql"></a><span data-ttu-id="cfa18-1201">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cfa18-1201">Az.Sql</span></span>
* <span data-ttu-id="cfa18-1202">Добавлена возможность восстановления точки во времени между подписками в Управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1202">Added support for cross subscription point in time restore on Managed Instances.</span></span>
* <span data-ttu-id="cfa18-1203">Добавлена возможность изменения существующего поколения оборудования Управляемого экземпляра SQL.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1203">Added support for changing existing Sql Managed Instance hardware generation</span></span>
* <span data-ttu-id="cfa18-1204">Исправлены примеры справки Update-AzSqlServerVulnerabilityAssessmentSetting: выходные данные параметра и свойства — EmailAdmins.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1204">Fixed 'Update-AzSqlServerVulnerabilityAssessmentSetting' help examples: parameter/property output - EmailAdmins</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="cfa18-1205">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="cfa18-1205">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="cfa18-1206">Добавлены командлеты для прослушивателя группы доступности.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1206">Added cmdlets for Availability Group Listener</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="cfa18-1207">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="cfa18-1207">Az.StorageSync</span></span>
* <span data-ttu-id="cfa18-1208">В командлете Invoke-AzStorageSyncCompatibilityCheck обновлены поддерживаемые наборы символов.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1208">Updated supported character sets in 'Invoke-AzStorageSyncCompatibilityCheck'.</span></span>

## <a name="340---february-2020"></a><span data-ttu-id="cfa18-1209">3.4.0 — февраль 2020 г.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1209">3.4.0 - February 2020</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="cfa18-1210">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="cfa18-1210">Highlights since the last major release</span></span>
* <span data-ttu-id="cfa18-1211">Выпущена первоначальная версия 0.1.0 Az.CosmosDB</span><span class="sxs-lookup"><span data-stu-id="cfa18-1211">Az.CosmosDB initial version 0.1.0 released</span></span>
* <span data-ttu-id="cfa18-1212">Добавлена поддержка Az.Network ConnectionMonitor V2</span><span class="sxs-lookup"><span data-stu-id="cfa18-1212">Az.Network ConnectionMonitor V2 support added</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="cfa18-1213">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cfa18-1213">Az.Accounts</span></span>
* <span data-ttu-id="cfa18-1214">Отключить автоматическое сохранение контекста, если AzureRmContext.json недоступен</span><span class="sxs-lookup"><span data-stu-id="cfa18-1214">Disable context auto saving when AzureRmContext.json not available</span></span>
* <span data-ttu-id="cfa18-1215">Обновление ссылки на Azure Powershell Common до предварительной версии 1.3.5</span><span class="sxs-lookup"><span data-stu-id="cfa18-1215">Update the reference to Azure Powershell Common to 1.3.5-preview</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="cfa18-1216">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cfa18-1216">Az.ApiManagement</span></span>
* <span data-ttu-id="cfa18-1217">**Get-AzApiManagementApiSchema** Исправлено получение схемы Open-API, связанной с API https://github.com/Azure/azure-powershell/issues/10626</span><span class="sxs-lookup"><span data-stu-id="cfa18-1217">**Get-AzApiManagementApiSchema** Fixed getting Open-Api Schema associated with an API   https://github.com/Azure/azure-powershell/issues/10626</span></span>
* <span data-ttu-id="cfa18-1218">**New-AzApiManagementProduct** _ и _ *Set-AzApiManagementProduct*\*</span><span class="sxs-lookup"><span data-stu-id="cfa18-1218">**New-AzApiManagementProduct** _ and _ *Set-AzApiManagementProduct*\*</span></span>
  - <span data-ttu-id="cfa18-1219">Исправить документацию для https://github.com/Azure/azure-powershell/issues/10472</span><span class="sxs-lookup"><span data-stu-id="cfa18-1219">Fix documentation for https://github.com/Azure/azure-powershell/issues/10472</span></span>
* <span data-ttu-id="cfa18-1220">**Set-AzApiManagementApi** Добавлен пример, показывающий, как обновить ServiceUrl с помощью командлета</span><span class="sxs-lookup"><span data-stu-id="cfa18-1220">**Set-AzApiManagementApi** Added example to show how to update the ServiceUrl using the cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cfa18-1221">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cfa18-1221">Az.Compute</span></span>
* <span data-ttu-id="cfa18-1222">Ограничение числа состояний виртуальных машин до 100, чтобы избежать регулирования при выполнении Get-AzVM-Status без имени виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1222">Limit the number of VM status to 100 to avoid throttling when Get-AzVM -Status is performed without VM name.</span></span>
* <span data-ttu-id="cfa18-1223">Добавление обновления командлета -AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="cfa18-1223">Add Update-AzDiskEncryptionSet cmdlet</span></span>
* <span data-ttu-id="cfa18-1224">Добавление параметров EncryptionType и DiskEncryptionSetId в следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="cfa18-1224">Add EncryptionType and DiskEncryptionSetId parameters to the following cmdlets:</span></span>
    - <span data-ttu-id="cfa18-1225">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="cfa18-1225">New-AzDiskUpdateConfig, New-AzSnapshotUpdateConfig</span></span>
* <span data-ttu-id="cfa18-1226">Добавление параметра ColocationStatus в командлет Get-AzProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1226">Add ColocationStatus parameter to Get-AzProximityPlacementGroup cmdlet.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cfa18-1227">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cfa18-1227">Az.DataFactory</span></span>
* <span data-ttu-id="cfa18-1228">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.7.0.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1228">Update ADF .Net SDK version to 4.7.0</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="cfa18-1229">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="cfa18-1229">Az.DeploymentManager</span></span>
* <span data-ttu-id="cfa18-1230">Добавляет операции LIST для ресурсов</span><span class="sxs-lookup"><span data-stu-id="cfa18-1230">Adds LIST operations for resources</span></span>
* <span data-ttu-id="cfa18-1231">Добавляет возможность выполнения операций на этапах Проверки работоспособности</span><span class="sxs-lookup"><span data-stu-id="cfa18-1231">Adds capability for performing operations on Health Check steps</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="cfa18-1232">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cfa18-1232">Az.HDInsight</span></span>
* <span data-ttu-id="cfa18-1233">Исправление ошибки в документе New-AzHDInsightCluster.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1233">Fix document error of New-AzHDInsightCluster.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cfa18-1234">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cfa18-1234">Az.KeyVault</span></span>
* <span data-ttu-id="cfa18-1235">Добавление Псевдонимов имени в атрибут VaultName, чтобы Remove-AzureKeyVault соответствовал New-AzureKeyVault.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1235">Add Name alias to VaultName attribute to make Remove-AzureKeyVault consistent with New-AzureKeyVault.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cfa18-1236">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cfa18-1236">Az.Network</span></span>
* <span data-ttu-id="cfa18-1237">В Set-AzNetworkWatcherConfigFlowLog.md добавлен новый пример для демонстрации сценария отключения Аналитики трафика.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1237">New example added to Set-AzNetworkWatcherConfigFlowLog.md to demonstrate Traffic Analytics disable scenario.</span></span>
* <span data-ttu-id="cfa18-1238">Добавление поддержки назначения IP-конфигурации для брандмауэра Azure — выделенная подсеть и общедоступный IP-адрес, которые брандмауэр будет использовать для управления трафиком</span><span class="sxs-lookup"><span data-stu-id="cfa18-1238">Add support for assigning management IP configuration to Azure Firewall - a dedicated subnet and Public IP that the firewall will use for its management traffic</span></span>
    - <span data-ttu-id="cfa18-1239">Обновлен командлет New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="cfa18-1239">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="cfa18-1240">добавлен параметр — ManagementPublicIpAddress (необязательный), который принимает объект общедоступного IP-адреса</span><span class="sxs-lookup"><span data-stu-id="cfa18-1240">Added parameter -ManagementPublicIpAddress (not mandatory) which accepts a Public IP Address object</span></span>
        - <span data-ttu-id="cfa18-1241">Добавлен метод SetManagementIpConfiguration для объекта брандмауэра — в качестве входных данных требуется подсеть и общедоступный IP-адрес — имя подсети должно быть "AzureFirewallManagementSubnet"</span><span class="sxs-lookup"><span data-stu-id="cfa18-1241">Added method SetManagementIpConfiguration on firewall object - requires a subnet and a Public IP address as input - subnet name must be 'AzureFirewallManagementSubnet'</span></span>
* <span data-ttu-id="cfa18-1242">Исправлены примеры Get-AzNetworkSecurityGroup для отображения примеров для группы безопасности сети (NSG) вместо сетевых интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1242">Corrected Get-AzNetworkSecurityGroup examples to show examples for NSG's instead of network interfaces.</span></span>
* <span data-ttu-id="cfa18-1243">Исправлена опечатка в команде New-AzVpnSite, которая препятствовала завершению параметра идентификатором ресурса.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1243">Fixed typo in New-AzVpnSite command that was preventing resource id completer from completing a parameter.</span></span>
* <span data-ttu-id="cfa18-1244">Добавлена поддержка конфигурации в наборе действий для правил подстановки URL-адресов в шлюзе приложения.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1244">Added support for Url Confiugration in Rewrite Rules Action Set in the Application Gateway</span></span>
    - <span data-ttu-id="cfa18-1245">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="cfa18-1245">New cmdlets added:</span></span>
        - <span data-ttu-id="cfa18-1246">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="cfa18-1246">New-AzApplicationGatewayRewriteRuleUrlConfiguration</span></span>
    - <span data-ttu-id="cfa18-1247">В следующие командлеты добавлен необязательный параметр — UrlConfiguration</span><span class="sxs-lookup"><span data-stu-id="cfa18-1247">Cmdlets updated with optional parameter - UrlConfiguration</span></span>
        - <span data-ttu-id="cfa18-1248">New-AzApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="cfa18-1248">New-AzApplicationGatewayRewriteRuleActionSet</span></span>
* <span data-ttu-id="cfa18-1249">Добавление поддержки для ресурсов NetworkWatcher ConnectionMonitor версии 2</span><span class="sxs-lookup"><span data-stu-id="cfa18-1249">Add suppport for NetworkWatcher ConnectionMonitor version 2 resources</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="cfa18-1250">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="cfa18-1250">Az.PolicyInsights</span></span>
* <span data-ttu-id="cfa18-1251">Поддержка оценки соответствия до определения того, какой ресурс нужно исправить</span><span class="sxs-lookup"><span data-stu-id="cfa18-1251">Support evaluating compliance prior to determining what resource to remediate</span></span>
    - <span data-ttu-id="cfa18-1252">Добавление параметра "—ResourceDiscoverMode" в Start-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="cfa18-1252">Add '-ResourceDiscoverMode' parameter to Start-AzPolicyRemediation</span></span>
* <span data-ttu-id="cfa18-1253">Добавление командлета Get-AzPolicyMetadata для получения ресурсов метаданных политики</span><span class="sxs-lookup"><span data-stu-id="cfa18-1253">Add Get-AzPolicyMetadata cmdlet for getting policy metadata resources</span></span>
* <span data-ttu-id="cfa18-1254">Get-AzPolicyState и Get-AzPolicyStateSummary обновлены для API версии 2019-10-01</span><span class="sxs-lookup"><span data-stu-id="cfa18-1254">Updated Get-AzPolicyState and Get-AzPolicyStateSummary for API version 2019-10-01</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cfa18-1255">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cfa18-1255">Az.RecoveryServices</span></span>
* <span data-ttu-id="cfa18-1256">Поддержка Azure Site Recovery для удаления реплицированного диска.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1256">Azure Site Recovery support for removing a replicated disk.</span></span>
* <span data-ttu-id="cfa18-1257">В Azure Backup добавлена ​​поддержка добавления тегов при создании Хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1257">Azure Backup added support for adding tags while creating a Recovery Services Vault.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cfa18-1258">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cfa18-1258">Az.Resources</span></span>
* <span data-ttu-id="cfa18-1259">Сделайте команду "Область" необязательной в командлетах \*—AzPolicyAssignment с настройкой по умолчанию для контекстной подписки</span><span class="sxs-lookup"><span data-stu-id="cfa18-1259">Make -Scope optional in \*-AzPolicyAssignment cmdlets with default to context subscription</span></span>
* <span data-ttu-id="cfa18-1260">Добавление примеров создания ADServicePrincipal с паролем и ключом учетных данных</span><span class="sxs-lookup"><span data-stu-id="cfa18-1260">Add examples of creating ADServicePrincipal with password and key credential</span></span>

#### <a name="azsql"></a><span data-ttu-id="cfa18-1261">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cfa18-1261">Az.Sql</span></span>
<span data-ttu-id="cfa18-1262">Исправление командлета New-AzSqlDatabaseSecondary, чтобы проверить существование PartnerDatabaseName, а не DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1262">Fix New-AzSqlDatabaseSecondary cmdlet to check for PartnerDatabaseName existence instead of DatabaseName existence.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cfa18-1263">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cfa18-1263">Az.Storage</span></span>
* <span data-ttu-id="cfa18-1264">Поддержка набора шифрования типа ключа таблиц и очередей в создании учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="cfa18-1264">Support set Table/Queue Encryption Keytype in Create Storage Account</span></span>
    - <span data-ttu-id="cfa18-1265">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cfa18-1265">New-AzStorageAccount</span></span>
* <span data-ttu-id="cfa18-1266">Представление RequestId, если StorageException не имеет ExtendedErrorInformation</span><span class="sxs-lookup"><span data-stu-id="cfa18-1266">Show RequestId when StorageException don't have ExtendedErrorInformation</span></span>
* <span data-ttu-id="cfa18-1267">Исправление примера 6 командлета Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="cfa18-1267">Fix the Example 6 of cmdlet Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cfa18-1268">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cfa18-1268">Az.Websites</span></span>
* <span data-ttu-id="cfa18-1269">Set-AzWebapp и Set-AzWebappSlot поддерживают свойства AlwaysOn, MinTls и FtpsState</span><span class="sxs-lookup"><span data-stu-id="cfa18-1269">Set-AzWebapp and Set-AzWebappSlot supports AlwaysOn, MinTls and FtpsState properties</span></span>
* <span data-ttu-id="cfa18-1270">Устранение проблемы, при которой параметр HttpsOnly с одновременным изменением AppservicePlan с помощью одной команды Set-AzWebApp сбрасывал значение HttpsOnly до значения по умолчанию</span><span class="sxs-lookup"><span data-stu-id="cfa18-1270">Fixing issue where setting HttpsOnly along with changing AppservicePlan at the same time using the single Set-AzWebApp Command, was resetting HttpsOnly to default value</span></span>

## <a name="330---january-2020"></a><span data-ttu-id="cfa18-1271">3.3.0 — январь 2020 г.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1271">3.3.0 - January 2020</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cfa18-1272">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cfa18-1272">Az.Accounts</span></span>
* <span data-ttu-id="cfa18-1273">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment: теперь они принимают параметры AzureAttestationServiceEndpointResourceId и AzureAttestationServiceEndpointSuffix.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1273">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameters AzureAttestationServiceEndpointResourceId and AzureAttestationServiceEndpointSuffix</span></span>

#### <a name="azcdn"></a><span data-ttu-id="cfa18-1274">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="cfa18-1274">Az.Cdn</span></span>
* <span data-ttu-id="cfa18-1275">Теперь в командлете New-AzCdnEndpoint отображаются сведения из сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1275">Display error response detail in New-AzCdnEndpoint cmdlet</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cfa18-1276">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cfa18-1276">Az.Compute</span></span>
* <span data-ttu-id="cfa18-1277">Командлет Set-AzVMCustomScriptExtension исправлен для виртуальной машины с управляемым диском ОС без профиля ОС.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1277">Fix Set-AzVMCustomScriptExtension cmdlet for a VM with managed OD disk which does not have OS profile.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="cfa18-1278">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="cfa18-1278">Az.ContainerInstance</span></span>
* <span data-ttu-id="cfa18-1279">Исправлены имена параметров, используемые в примере командлета New-AzContainerGroup.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1279">Fixed parameter names used by example of New-AzContainerGroup</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="cfa18-1280">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="cfa18-1280">Az.DataBoxEdge</span></span>
* <span data-ttu-id="cfa18-1281">Добавлен командлет Get-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="cfa18-1281">Added cmdlet 'Get-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="cfa18-1282">получение контейнера хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1282">Get the Edge Storage Container</span></span>
* <span data-ttu-id="cfa18-1283">Добавлен командлет New-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="cfa18-1283">Added cmdlet 'New-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="cfa18-1284">создание контейнера хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1284">Create new Edge Strorage Container</span></span>
* <span data-ttu-id="cfa18-1285">Добавлен командлет Remove-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="cfa18-1285">Added cmdlet 'Remove-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="cfa18-1286">удаление контейнера хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1286">Remove the Edge Storage Container</span></span>
* <span data-ttu-id="cfa18-1287">Добавлен командлет Invoke-AzDataBoxEdgeStorageContainer:</span><span class="sxs-lookup"><span data-stu-id="cfa18-1287">Added cmdlet 'Invoke-AzDataBoxEdgeStorageContainer'</span></span>
  - <span data-ttu-id="cfa18-1288">вызов действия для обновления данных в контейнере хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1288">Invoke action to refresh data on Edge Storage Container</span></span>
* <span data-ttu-id="cfa18-1289">Добавлен командлет Get-AzDataBoxEdgeStorageAccount:</span><span class="sxs-lookup"><span data-stu-id="cfa18-1289">Added cmdlet 'Get-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="cfa18-1290">получение учетной записи хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1290">Get the Edge Storage Account</span></span>
* <span data-ttu-id="cfa18-1291">Добавлен командлет New-AzDataBoxEdgeStorageAccount:</span><span class="sxs-lookup"><span data-stu-id="cfa18-1291">Added cmdlet 'New-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="cfa18-1292">создание учетной записи хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1292">Create new Edge Storage Account</span></span>
* <span data-ttu-id="cfa18-1293">Добавлен командлет Remove-AzDataBoxEdgeStorageAccount:</span><span class="sxs-lookup"><span data-stu-id="cfa18-1293">Added cmdlet 'Remove-AzDataBoxEdgeStorageAccount'</span></span>
  - <span data-ttu-id="cfa18-1294">удаление учетной записи хранилища Edge.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1294">Remove the Edge Storage Account</span></span>
* <span data-ttu-id="cfa18-1295">Вызов командлета Invoke-AzDataBoxEdgeShare:</span><span class="sxs-lookup"><span data-stu-id="cfa18-1295">Invoke cmdlet 'Invoke-AzDataBoxEdgeShare'</span></span>
  - <span data-ttu-id="cfa18-1296">вызов действия для обновления данных в общей папке.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1296">Invoke action to refresh data on share</span></span>
* <span data-ttu-id="cfa18-1297">Добавлен командлет Set-AzDataBoxEdgeStorageAccountCredential:</span><span class="sxs-lookup"><span data-stu-id="cfa18-1297">Added cmdlet 'Set-AzDataBoxEdgeStorageAccountCredential'</span></span>
  - <span data-ttu-id="cfa18-1298">установка учетных данных для учетной записи хранилища Azure Data Box Edge.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1298">Set the az databoxedge storage account credential</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cfa18-1299">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cfa18-1299">Az.DataFactory</span></span>
* <span data-ttu-id="cfa18-1300">Добавлены свойства AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId и VersionStatus для командлета Get-AzDataFactoryV2IntegrationRuntime.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1300">Add AutoUpdateETA, LatestVersion, PushedVersion, TaskQueueId and VersionStatus properties for Get-AzDataFactoryV2IntegrationRuntime cmd</span></span>
* <span data-ttu-id="cfa18-1301">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.6.0.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1301">Update ADF .Net SDK version to 4.6.0</span></span>
* <span data-ttu-id="cfa18-1302">Для командлета Set-AzureRmDataFactoryV2IntegrationRuntime добавлен параметр PublicIPs, позволяющий включить создание среды Azure-SSIS IR со статическими общедоступными IP-адресами.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1302">Add parameter 'PublicIPs' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable create Azure-SSIS IR with static public IP addresses.</span></span>

#### <a name="azdevtestlabs"></a><span data-ttu-id="cfa18-1303">Az.DevTestLabs</span><span class="sxs-lookup"><span data-stu-id="cfa18-1303">Az.DevTestLabs</span></span>
* <span data-ttu-id="cfa18-1304">Удалена недействительная ссылка в файле Get-AzDtlAllowedVMSizesPolicy.md.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1304">Remove the broken link in Get-AzDtlAllowedVMSizesPolicy.md</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="cfa18-1305">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="cfa18-1305">Az.EventHub</span></span>
* <span data-ttu-id="cfa18-1306">Устранена проблема № 10634: исправлена ссылка на пустой объект для удаления пространства имен концентратора событий.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1306">Fix for issue 10634 : Fix the null Object reference for remove eventhubnamespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="cfa18-1307">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cfa18-1307">Az.HDInsight</span></span>
* <span data-ttu-id="cfa18-1308">Устранена ошибка в файле Invoke-AzHDInsightHiveJob.md.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1308">Fix Invoke-AzHDInsightHiveJob.md error.</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="cfa18-1309">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="cfa18-1309">Az.MachineLearning</span></span>
* <span data-ttu-id="cfa18-1310">Вычислительная среда Машинного обучения больше недоступна, поэтому удалены следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="cfa18-1310">Removed below cmdlets because MachineLearningCompute is not available any longer</span></span>
  - <span data-ttu-id="cfa18-1311">Get-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="cfa18-1311">Get-AzMlOpCluster</span></span>
  - <span data-ttu-id="cfa18-1312">Get-AzMlOpClusterKey;</span><span class="sxs-lookup"><span data-stu-id="cfa18-1312">Get-AzMlOpClusterKey</span></span>
  - <span data-ttu-id="cfa18-1313">New-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="cfa18-1313">New-AzMlOpCluster</span></span>
  - <span data-ttu-id="cfa18-1314">Remove-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="cfa18-1314">Remove-AzMlOpCluster</span></span>
  - <span data-ttu-id="cfa18-1315">Set-AzMlOpCluster;</span><span class="sxs-lookup"><span data-stu-id="cfa18-1315">Set-AzMlOpCluster</span></span>
  - <span data-ttu-id="cfa18-1316">Test-AzMlOpClusterSystemServicesUpdateAvailability;</span><span class="sxs-lookup"><span data-stu-id="cfa18-1316">Test-AzMlOpClusterSystemServicesUpdateAvailability</span></span>
  - <span data-ttu-id="cfa18-1317">Update-AzMlOpClusterSystemService.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1317">Update-AzMlOpClusterSystemService</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cfa18-1318">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cfa18-1318">Az.Network</span></span>
* <span data-ttu-id="cfa18-1319">Обновлена зависимость Microsoft.Azure.Management.Sql от предварительной версии 1.36 до предварительной версии 1.37.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1319">Upgrade dependency of Microsoft.Azure.Management.Sql from 1.36-preview to 1.37-preview</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cfa18-1320">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cfa18-1320">Az.RecoveryServices</span></span>
* <span data-ttu-id="cfa18-1321">Добавлена поддержка Azure Site Recovery для виртуальных машин с управляемым диском, зашифрованных при хранении с помощью управляемых клиентом ключей, при восстановлении из Azure в поставщике Azure.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1321">Azure Site Recovery change support for managed disk vms encrypted at rest with customer managed keys for Azure to Azure provider.</span></span>
* <span data-ttu-id="cfa18-1322">Добавлена поддержка Azure Site Recovery для необязательного ввода идентификатора набора шифрования диска при включении защиты в рамках восстановления из VMware в Azure.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1322">Azure Site Recovery support to input disk encryption Set Id as optional input at enabling protection for Vmware to Azure.</span></span>
* <span data-ttu-id="cfa18-1323">Добавлена поддержка Azure Site Recovery для необязательного ввода идентификатора набора шифрования диска на уровне диска при включении защиты в рамках восстановления из VMware в Azure.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1323">Azure Site Recovery support to input disk encryption Set Id as optional input at disk level to enable protection for Vmware to Azure.</span></span>
* <span data-ttu-id="cfa18-1324">Добавлена поддержка Azure Site Recovery для обновления элемента, защищенного репликацией, путем сопоставления набора шифрования диска при восстановлении из HyperV в Azure.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1324">Azure Site Recovery support to update replication protected item with disk encryption set Map for HyperV to Azure.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cfa18-1325">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cfa18-1325">Az.Resources</span></span>
* <span data-ttu-id="cfa18-1326">Исправлена ошибка в справочном документе о командлете Remove-AzTag.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1326">Fix an error in help document of 'Remove-AzTag'.</span></span>

#### <a name="azsql"></a><span data-ttu-id="cfa18-1327">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cfa18-1327">Az.Sql</span></span>
* <span data-ttu-id="cfa18-1328">Исправлена функция основных командлетов установки оценки уязвимостей: теперь она позволяет работать с базой данных master для базы данных Azure и ограничить ее в системных базах данных управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1328">Fix vulnerability assessment set baseline cmdlets functionality to work on master db for azure database and limit it on managed instance system databases.</span></span>
* <span data-ttu-id="cfa18-1329">Устранена ошибка, возникающая при создании группы отработки отказа экземпляра SQL.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1329">Fix an error when creating SQL instance failover group</span></span>

#### <a name="azsqlvirtualmachine"></a><span data-ttu-id="cfa18-1330">Az.SqlVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="cfa18-1330">Az.SqlVirtualMachine</span></span>
* <span data-ttu-id="cfa18-1331">Добавлен новый допустимый тип лицензии: DR (аварийное восстановление).</span><span class="sxs-lookup"><span data-stu-id="cfa18-1331">Add DR as a new valid License type</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cfa18-1332">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cfa18-1332">Az.Storage</span></span>
* <span data-ttu-id="cfa18-1333">Добавлено предупреждающее сообщение о критическом изменении значения DefaultAction в следующем выпуске:</span><span class="sxs-lookup"><span data-stu-id="cfa18-1333">Add breaking change warning message for DefaultAction Value change in a future release</span></span>
    - <span data-ttu-id="cfa18-1334">Update-AzStorageAccountNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1334">Update-AzStorageAccountNetworkRuleSet</span></span>
* <span data-ttu-id="cfa18-1335">Включена поддержка получения времени последней синхронизации учетной записи хранения путем выполнения командлета Get-AzureRmStorageAccount с параметром -IncludeGeoReplicationStats:</span><span class="sxs-lookup"><span data-stu-id="cfa18-1335">Support Get last sync time of Storage account by run get-AzureRMStorageAccount with parameter -IncludeGeoReplicationStats</span></span>
    - <span data-ttu-id="cfa18-1336">Get-AzureRmStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1336">Get-AzureRMStorageAccount</span></span>

## <a name="320---december-2019"></a><span data-ttu-id="cfa18-1337">3.2.0 — декабрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1337">3.2.0 - December 2019</span></span>

### <a name="general"></a><span data-ttu-id="cfa18-1338">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="cfa18-1338">General</span></span>
* <span data-ttu-id="cfa18-1339">Обновление ссылок в .psd1 для использования относительного пути для всех модулей.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1339">Update references in .psd1 to use relative path for all modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="cfa18-1340">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cfa18-1340">Az.Accounts</span></span>
* <span data-ttu-id="cfa18-1341">Установка правильного параметра UserAgent для телеметрии на стороне клиента для Az 4.0 (предварительная версия).</span><span class="sxs-lookup"><span data-stu-id="cfa18-1341">Set correct UserAgent for client-side telemetry for Az 4.0 preview</span></span>
* <span data-ttu-id="cfa18-1342">Отображение понятного пользователю сообщения об ошибке, если в Az 4.0 (предварительная версия) не указан контекст.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1342">Display user friendly error message when context is null in Az 4.0 preview</span></span>

#### <a name="azbatch"></a><span data-ttu-id="cfa18-1343">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="cfa18-1343">Az.Batch</span></span>
* <span data-ttu-id="cfa18-1344">Исправлена проблема [№ 10602](https://github.com/Azure/azure-powershell/issues/10602), из-за которой использование командлета **New-AzBatchPool** приводило к неправильной отправке VirtualMachineConfiguration.ContainerConfiguration или VirtualMachineConfiguration.DataDisks на сервер.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1344">Fix issue [#10602](https://github.com/Azure/azure-powershell/issues/10602), where **New-AzBatchPool** did not properly send 'VirtualMachineConfiguration.ContainerConfiguration' or 'VirtualMachineConfiguration.DataDisks' to the server.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cfa18-1345">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cfa18-1345">Az.DataFactory</span></span>
* <span data-ttu-id="cfa18-1346">Обновление пакета SDK Фабрики данных для .NET до версии 4.5.0.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1346">Update ADF .Net SDK version to 4.5.0</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="cfa18-1347">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="cfa18-1347">Az.FrontDoor</span></span>
* <span data-ttu-id="cfa18-1348">Включена поддержка исключений управляемых правил WAF.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1348">Added WAF managed rules exclusion support</span></span>
* <span data-ttu-id="cfa18-1349">Добавление SocketAddr в список автозавершения.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1349">Add SocketAddr to auto-complete</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="cfa18-1350">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="cfa18-1350">Az.HealthcareApis</span></span>
* <span data-ttu-id="cfa18-1351">Обработка исключений.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1351">Exception Handling</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cfa18-1352">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cfa18-1352">Az.KeyVault</span></span>
* <span data-ttu-id="cfa18-1353">Исправлена ошибка при получении доступа к значению, которое может быть не задано.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1353">Fixed error accessing value that is potentially not set</span></span>
* <span data-ttu-id="cfa18-1354">Управление сертификатами шифрования на основе эллиптических кривых.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1354">Elliptic Curve Cryptography Certificate Managment</span></span>
    - <span data-ttu-id="cfa18-1355">Включена возможность указания кривой для политик сертификатов.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1355">Added support to specify the Curve for Certificate Policies</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cfa18-1356">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cfa18-1356">Az.Monitor</span></span>
* <span data-ttu-id="cfa18-1357">Добавление необязательного аргумента в команду добавления параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1357">Adding optional argument to the Add Diagnostic Settings command.</span></span> <span data-ttu-id="cfa18-1358">Существующий аргумент switch указывает на то, что экспорт в Log Analytics должен выполняться в фиксированную схему</span><span class="sxs-lookup"><span data-stu-id="cfa18-1358">A switch argument that if present indicates that the export to Log Analytics must be to a fixed schema (a.k.a.</span></span> <span data-ttu-id="cfa18-1359">(выделенный тип данных).</span><span class="sxs-lookup"><span data-stu-id="cfa18-1359">dedicated, data type)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cfa18-1360">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cfa18-1360">Az.Network</span></span>
* <span data-ttu-id="cfa18-1361">В приложении AzureFirewall, NAT и сетевых правилах включена поддержка IpGroups.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1361">Support for IpGroups in AzureFirewall Application,Nat & Network Rules.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cfa18-1362">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cfa18-1362">Az.Resources</span></span>
* <span data-ttu-id="cfa18-1363">Устранена проблема, из-за которой при развертывании шаблона не удавалось считать его параметр, если имя параметра конфликтовало с именем встроенного параметра.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1363">Fix an issue where template deployment fails to read a template parameter if its name conflicts with some built-in parameter name.</span></span>
* <span data-ttu-id="cfa18-1364">Обновлены командлеты политики для использования новой версии API 2019-09-01 с поддержкой группирования в определениях наборов политик.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1364">Updated policy cmdlets to use new api version 2019-09-01 that introduces grouping support within policy set definitions.</span></span>

#### <a name="azsql"></a><span data-ttu-id="cfa18-1365">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cfa18-1365">Az.Sql</span></span>
* <span data-ttu-id="cfa18-1366">Обновлена функция автоматического создания расширенного хранилища для службы оценки уязвимостей в учетной записи StorageV2.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1366">Upgraded storage creation in Vulnerability Assessment auto enablement to StorageV2</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cfa18-1367">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cfa18-1367">Az.Storage</span></span>
* <span data-ttu-id="cfa18-1368">Включена поддержка создания маркера SAS на основе удостоверения контейнера и большого двоичного объекта с аутентификацией Oauth на основе контекста службы хранилища:</span><span class="sxs-lookup"><span data-stu-id="cfa18-1368">Support generate Blob/Constainer Idenity based SAS token with Storage Context based on Oauth authentication</span></span>
    - <span data-ttu-id="cfa18-1369">New-AzStorageContainerSASToken;</span><span class="sxs-lookup"><span data-stu-id="cfa18-1369">New-AzStorageContainerSASToken</span></span>
    - <span data-ttu-id="cfa18-1370">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="cfa18-1370">New-AzStorageBlobSASToken</span></span>
* <span data-ttu-id="cfa18-1371">Отозвана поддержка ключей делегирования пользователя учетной записи хранения, а также всех маркеров SAS удостоверения:</span><span class="sxs-lookup"><span data-stu-id="cfa18-1371">Support revoke Storage Account User Delegation Keys, so all Idenity SAS tokens are revoked</span></span>
    - <span data-ttu-id="cfa18-1372">Revoke-AzStorageAccountUserDelegationKeys.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1372">Revoke-AzStorageAccountUserDelegationKeys</span></span>
* <span data-ttu-id="cfa18-1373">Выполнено обновление до Microsoft.Azure.Management.Storage версии 14.2.0 для включения поддержки нового API версии 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1373">Upgrade to Microsoft.Azure.Management.Storage 14.2.0, to support new API version 2019-06-01.</span></span>
* <span data-ttu-id="cfa18-1374">Включена поддержка QuotaGiB (квота общего ресурса в ГиБ) для значений свыше 5120 в командлетах для работы с общими папками в плоскости управления и добавлен псевдоним Quota для параметра QuotaGiB.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1374">Support of QuotaGiB (Share Quota in Gibibye) for values of more than 5120 in the Management plane of File Share cmdlets and added the 'Quota' parameter alias to the 'QuotaGiB' parameter.</span></span>
    - <span data-ttu-id="cfa18-1375">New-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="cfa18-1375">New-AzRmStorageShare</span></span>
    - <span data-ttu-id="cfa18-1376">Update-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="cfa18-1376">Update-AzRmStorageShare</span></span>
* <span data-ttu-id="cfa18-1377">Добавлен псевдоним QuotaGiB для параметра Quota:</span><span class="sxs-lookup"><span data-stu-id="cfa18-1377">Add parameter alias 'QuotaGiB' to parameter 'Quota'</span></span>
    - <span data-ttu-id="cfa18-1378">Set-AzStorageShareQuota.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1378">Set-AzStorageShareQuota</span></span>
* <span data-ttu-id="cfa18-1379">Устранена проблема, из-за которой при использовании AzStorageContainerAcl могла очищаться хранимая политика доступа:</span><span class="sxs-lookup"><span data-stu-id="cfa18-1379">Fix the issue that Set-AzStorageContainerAcl can clean up the stored Access Policy</span></span>
    - <span data-ttu-id="cfa18-1380">Set-AzStorageContainerAcl.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1380">Set-AzStorageContainerAcl</span></span>

## <a name="310---november-2019"></a><span data-ttu-id="cfa18-1381">Версия 3.1.0 от ноября 2019 г.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1381">3.1.0 - November 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="cfa18-1382">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="cfa18-1382">Highlights since the last major release</span></span>
* <span data-ttu-id="cfa18-1383">Выпуск Az.DataBoxEdge 1.0.0</span><span class="sxs-lookup"><span data-stu-id="cfa18-1383">Az.DataBoxEdge 1.0.0 released</span></span>
* <span data-ttu-id="cfa18-1384">Выпуск Az.SqlVirtualMachine 1.0.0</span><span class="sxs-lookup"><span data-stu-id="cfa18-1384">Az.SqlVirtualMachine 1.0.0 released</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cfa18-1385">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cfa18-1385">Az.Compute</span></span>
* <span data-ttu-id="cfa18-1386">Функция повторного применения виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="cfa18-1386">VM Reapply feature</span></span>
    - <span data-ttu-id="cfa18-1387">Добавлен параметр повторного применения в командлет Set-AzVM.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1387">Add Reapply parameter to Set-AzVM cmdlet</span></span>
* <span data-ttu-id="cfa18-1388">Функция AutomaticRepairs масштабируемого набора виртуальных машин:</span><span class="sxs-lookup"><span data-stu-id="cfa18-1388">VM Scale Set AutomaticRepairs feature:</span></span>
    - <span data-ttu-id="cfa18-1389">Добавлены параметры EnableAutomaticRepair, AutomaticRepairGracePeriod и AutomaticRepairMaxInstanceRepairsPercent в следующие командлеты:   New-AzVmssConfig Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="cfa18-1389">Add EnableAutomaticRepair, AutomaticRepairGracePeriod, and AutomaticRepairMaxInstanceRepairsPercent parameters to the following cmdlets:   New-AzVmssConfig   Update-AzVmss</span></span>
* <span data-ttu-id="cfa18-1390">Включена поддержка образа из коллекции разных клиентов для New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1390">Cross tenant gallery image support for New-AzVM</span></span>
* <span data-ttu-id="cfa18-1391">Добавлен фрагмент Spot в средство заполнения аргументов параметра Priority в командлетах New-AzVM, New-AzVMConfig и New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1391">Add 'Spot' to the argument completer of Priority parameter in New-AzVM, New-AzVMConfig and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="cfa18-1392">Добавлены параметры DiskIOPSReadWrite и DiskMBpsReadWrite в командлет Add-AzVmssDataDisk.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1392">Add DiskIOPSReadWrite and DiskMBpsReadWrite parameters to Add-AzVmssDataDisk cmdlet</span></span>
* <span data-ttu-id="cfa18-1393">Изменен параметр SourceImageId командлета New-AzGalleryImageVersion на необязательный.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1393">Change SourceImageId parameter of New-AzGalleryImageVersion cmdlet to optional</span></span>
* <span data-ttu-id="cfa18-1394">Добавлены параметры OSDiskImage и DataDiskImage в командлет New-AzGalleryImageVersion.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1394">Add OSDiskImage and DataDiskImage parameters to New-AzGalleryImageVersion cmdlet</span></span>
* <span data-ttu-id="cfa18-1395">Добавлен параметр HyperVGeneration в командлет New-AzGalleryImageDefinition.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1395">Add HyperVGeneration parameter to New-AzGalleryImageDefinition cmdlet</span></span>
* <span data-ttu-id="cfa18-1396">Добавлены параметры SkipExtensionsOnOverprovisionedVMs в командлеты New-AzVmss, New-AzVmssConfig и Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1396">Add SkipExtensionsOnOverprovisionedVMs parameters to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>

#### <a name="azdataboxedge"></a><span data-ttu-id="cfa18-1397">Az.DataBoxEdge</span><span class="sxs-lookup"><span data-stu-id="cfa18-1397">Az.DataBoxEdge</span></span>
* <span data-ttu-id="cfa18-1398">Добавлен командлет `Get-AzDataBoxEdgeOrder`.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1398">Added cmdlet `Get-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="cfa18-1399">Получение заказа.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1399">Get the Order</span></span>
* <span data-ttu-id="cfa18-1400">Добавлен командлет `New-AzDataBoxEdgeOrder`.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1400">Added cmdlet `New-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="cfa18-1401">Создание заказа.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1401">Create new Order</span></span>
* <span data-ttu-id="cfa18-1402">Добавлен командлет `Remove-AzDataBoxEdgeOrder`.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1402">Added cmdlet `Remove-AzDataBoxEdgeOrder`</span></span>
    - <span data-ttu-id="cfa18-1403">Удаление заказа.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1403">Remove the Order</span></span>
* <span data-ttu-id="cfa18-1404">Изменен командлет `New-AzDataBoxEdgeShare`.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1404">Change in cmdlet `New-AzDataBoxEdgeShare`</span></span>
    - <span data-ttu-id="cfa18-1405">Создание локальной общей папки.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1405">Now creates Local Share</span></span>
* <span data-ttu-id="cfa18-1406">Добавлен командлет `Set-AzDataBoxEdgeRole`.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1406">Added cmdlet `Set-AzDataBoxEdgeRole`</span></span>
    - <span data-ttu-id="cfa18-1407">Сопоставление IotRole с общей папкой.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1407">Now IotRole can be mapped to Share</span></span>
* <span data-ttu-id="cfa18-1408">Добавлен командлет `Invoke-AzDataBoxEdgeDevice`.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1408">Added cmdlet `Invoke-AzDataBoxEdgeDevice`</span></span>
    - <span data-ttu-id="cfa18-1409">Вызов проверки обновлений, скачивание обновления, установка обновления на устройстве.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1409">Invoke scan update, download update, install updates on the device</span></span>
* <span data-ttu-id="cfa18-1410">Добавлен командлет `Get-AzDataBoxEdgeTrigger`.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1410">Added cmdlet `Get-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="cfa18-1411">Получение сведений о триггерах.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1411">Gets the information about Triggers</span></span>
* <span data-ttu-id="cfa18-1412">Добавлен командлет `New-AzDataBoxEdgeTrigger`.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1412">Added cmdlet `New-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="cfa18-1413">Создание триггеров.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1413">Create new Triggers</span></span>
* <span data-ttu-id="cfa18-1414">Добавлен командлет `Remove-AzDataBoxEdgeTrigger`.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1414">Added cmdlet `Remove-AzDataBoxEdgeTrigger`</span></span>
    - <span data-ttu-id="cfa18-1415">Удаление триггеров.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1415">Remove the Triggers</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cfa18-1416">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cfa18-1416">Az.DataFactory</span></span>
* <span data-ttu-id="cfa18-1417">Обновление пакета SDK Фабрики данных для .NET до версии 4.4.0.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1417">Update ADF .Net SDK version to 4.4.0</span></span>
* <span data-ttu-id="cfa18-1418">Добавлен параметр ExpressCustomSetup в командлет Set-AzureRmDataFactoryV2IntegrationRuntime для включения конфигураций установки и сторонних компонентов без использования настраиваемого скрипта установки.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1418">Add parameter 'ExpressCustomSetup' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable setup configurations and 3rd party components without custom setup script.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cfa18-1419">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cfa18-1419">Az.DataLakeStore</span></span>
* <span data-ttu-id="cfa18-1420">Обновлена документация по Get-AzDataLakeStoreDeletedItem и Restore-AzDataLakeStoreDeletedItem.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1420">Update documentation of Get-AzDataLakeStoreDeletedItem and Restore-AzDataLakeStoreDeletedItem</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="cfa18-1421">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="cfa18-1421">Az.EventHub</span></span>
* <span data-ttu-id="cfa18-1422">Исправлена проблема № 10301. Исправлен формат даты маркера SAS.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1422">Fix for issue 10301 : Fix the SAS Token date format</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="cfa18-1423">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="cfa18-1423">Az.FrontDoor</span></span>
* <span data-ttu-id="cfa18-1424">Добавлен параметр MinimumTlsVersion в Enable-AzFrontDoorCustomDomainHttps и New-AzFrontDoorFrontendEndpointObject.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1424">Add MinimumTlsVersion parameter to Enable-AzFrontDoorCustomDomainHttps and New-AzFrontDoorFrontendEndpointObject</span></span>
* <span data-ttu-id="cfa18-1425">Добавлены параметры HealthProbeMethod и EnabledState в New-AzFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1425">Add HealthProbeMethod and EnabledState parameters to New-AzFrontDoorHealthProbeSettingObject</span></span>
* <span data-ttu-id="cfa18-1426">Добавлен новый командлет для создания объекта BackendPoolsSettings для передачи при создании и обновлении Front Door.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1426">Add new cmdlet to create BackendPoolsSettings objec to pass into creation/update of Front Door</span></span>
    - <span data-ttu-id="cfa18-1427">New-AzFrontDoorBackendPoolsSettingObject</span><span class="sxs-lookup"><span data-stu-id="cfa18-1427">New-AzFrontDoorBackendPoolsSettingObject</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cfa18-1428">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cfa18-1428">Az.Network</span></span>
* <span data-ttu-id="cfa18-1429">Изменены примеры параметра FilterData Start-AzVirtualNetworkGatewayConnectionPacketCapture.md и Start-AzVirtualnetworkGatewayPacketCapture.md.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1429">Change 'Start-AzVirtualNetworkGatewayConnectionPacketCapture.md' and 'Start-AzVirtualnetworkGatewayPacketCapture.md' FilterData option examples.</span></span>

#### <a name="azprivatedns"></a><span data-ttu-id="cfa18-1430">Az.PrivateDns</span><span class="sxs-lookup"><span data-stu-id="cfa18-1430">Az.PrivateDns</span></span>
* <span data-ttu-id="cfa18-1431">Пакет SDK PrivateDns для .NET обновлен до версии 1.0.0</span><span class="sxs-lookup"><span data-stu-id="cfa18-1431">Updated PrivateDns .net sdk to version 1.0.0</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cfa18-1432">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cfa18-1432">Az.RecoveryServices</span></span>
* <span data-ttu-id="cfa18-1433">Включена поддержка Azure Site Recovery для выбора типа диска при включении защиты.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1433">Azure Site Recovery support to select disk type at enabling protection.</span></span>
* <span data-ttu-id="cfa18-1434">Внесено исправление Azure Site Recovery для изменения действия плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1434">Azure Site Recovery bug fix for recovery plan action edit.</span></span>
* <span data-ttu-id="cfa18-1435">Включена поддержка восстановления SQL Azure Backup для принятия баз данных файлового потока.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1435">Azure Backup SQL Restore support to accept filestream DBs.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="cfa18-1436">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="cfa18-1436">Az.RedisCache</span></span>
* <span data-ttu-id="cfa18-1437">Добавлен параметр MinimumTlsVersion в командлеты New-AzRedisCache и Set-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1437">Added 'MinimumTlsVersion' parameter in 'New-AzRedisCache' and 'Set-AzRedisCache' cmdlets.</span></span> <span data-ttu-id="cfa18-1438">Кроме того, добавлен параметр MinimumTlsVersion в выходные данные командлета Get-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1438">Also, added 'MinimumTlsVersion' in the output of 'Get-AzRedisCache' cmdlet.</span></span>
* <span data-ttu-id="cfa18-1439">Добавлена проверка параметра -Size для командлетов Set-AzRedisCache и New-AzRedisCache.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1439">Added validation on '-Size' parameter for 'Set-AzRedisCache' and 'New-AzRedisCache' cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="cfa18-1440">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cfa18-1440">Az.Resources</span></span>
- <span data-ttu-id="cfa18-1441">Обновлены командлеты политики для использования новой версии API 2019-06-01 с новым свойством EnforcementMode в назначении политики.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1441">Updated policy cmdlets to use new api version 2019-06-01 that has new EnforcementMode property in policy assignment.</span></span>
- <span data-ttu-id="cfa18-1442">Обновлен пример справки по созданию определения политики</span><span class="sxs-lookup"><span data-stu-id="cfa18-1442">Updated create policy definition help example</span></span>
- <span data-ttu-id="cfa18-1443">Исправлена ошибка с параметром -ServicePrincipalName командлета Remove-AZADServicePrincipal с возвратом пустой ссылки, если имя субъекта службы не найдено.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1443">Fix bug Remove-AZADServicePrincipal -ServicePrincipalName, throw null reference when service principal name not found.</span></span>
- <span data-ttu-id="cfa18-1444">Исправлена ошибка с New-AZADServicePrincipal с возвратом пустой ссылки, если у клиента нет подписки.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1444">Fix bug New-AZADServicePrincipal, throw null reference when tenant doesn't have any subscription.</span></span>
- <span data-ttu-id="cfa18-1445">Изменен командлет New-AzAdServicePrincipal для добавления учетных данных только для связанного приложения.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1445">Change New-AzAdServicePrincipal to add credentials only to associated application.</span></span>

#### <a name="azsql"></a><span data-ttu-id="cfa18-1446">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cfa18-1446">Az.Sql</span></span>
* <span data-ttu-id="cfa18-1447">Добавлена поддержка ReadReplicaCount для базы данных.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1447">Added support for database ReadReplicaCount.</span></span>
* <span data-ttu-id="cfa18-1448">Исправлена ошибка с Set-AzSqlDatabase, если избыточность в пределах зоны не настроена.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1448">Fixed Set-AzSqlDatabase when zone redundancy not set</span></span>

## <a name="300---november-2019"></a><span data-ttu-id="cfa18-1449">Версия 3.0.0 от ноября 2019 г.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1449">3.0.0 - November 2019</span></span>
### <a name="general"></a><span data-ttu-id="cfa18-1450">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="cfa18-1450">General</span></span>
* <span data-ttu-id="cfa18-1451">Выпущена версия Az.PrivateDns 1.0.0</span><span class="sxs-lookup"><span data-stu-id="cfa18-1451">Az.PrivateDns 1.0.0 released</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="cfa18-1452">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cfa18-1452">Az.Accounts</span></span>
* <span data-ttu-id="cfa18-1453">Добавлено сообщение об устаревании для псевдонима "Resolve-Error".</span><span class="sxs-lookup"><span data-stu-id="cfa18-1453">Add a deprecation message for 'Resolve-Error' alias.</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="cfa18-1454">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="cfa18-1454">Az.Advisor</span></span>
* <span data-ttu-id="cfa18-1455">Добавлена новая категория Operational Excellence (Эффективность работы) в командлет Get-AzAdvisorRecommendation.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1455">Added new category 'Operational Excellence' to Get-AzAdvisorRecommendation cmdlet.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="cfa18-1456">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="cfa18-1456">Az.Batch</span></span>
* <span data-ttu-id="cfa18-1457">`CoreQuota` в `BatchAccountContext` переименован в `DedicatedCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1457">Renamed `CoreQuota` on `BatchAccountContext` to `DedicatedCoreQuota`.</span></span> <span data-ttu-id="cfa18-1458">Также появился новый `LowPriorityCoreQuota`.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1458">There is also a new `LowPriorityCoreQuota`.</span></span>
  - <span data-ttu-id="cfa18-1459">Это влияет на **Get-AzBatchAccount**.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1459">This impacts **Get-AzBatchAccount**.</span></span>
* <span data-ttu-id="cfa18-1460">Параметр **New-AzBatchTask** `-ResourceFile` теперь принимает коллекцию объектов `PSResourceFile`, которые можно создать с помощью нового командлета **New-AzBatchResourceFile**.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1460">**New-AzBatchTask** `-ResourceFile` parameter now takes a collection of `PSResourceFile` objects, which can be constructed using the new **New-AzBatchResourceFile** cmdlet.</span></span>
* <span data-ttu-id="cfa18-1461">Новый командлет **New-AzBatchResourceFile** , который помогает создавать объекты `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1461">New **New-AzBatchResourceFile** cmdlet to help create `PSResourceFile` objects.</span></span> <span data-ttu-id="cfa18-1462">Их можно передавать в **New-AzBatchTask** в параметре `-ResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1462">These can be supplied to **New-AzBatchTask** on the `-ResourceFile` parameter.</span></span>
  - <span data-ttu-id="cfa18-1463">Это позволяет поддерживать два новых типа файлов ресурсов, которые дополняют существующий метод `HttpUrl`:</span><span class="sxs-lookup"><span data-stu-id="cfa18-1463">This supports two new kinds of resource file in addition to the existing `HttpUrl` way:</span></span>
    - <span data-ttu-id="cfa18-1464">Файлы ресурсов на основе `AutoStorageContainerName` скачивают весь контейнер автоматического хранения в узел пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1464">`AutoStorageContainerName` based resource files download an entire auto-storage container to the Batch node.</span></span>
    - <span data-ttu-id="cfa18-1465">Файлы ресурсов на основе `StorageContainerUrl` скачивают указанный в URL-адресе контейнер в узел пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1465">`StorageContainerUrl` based resource files download the container specified in the URL to the Batch node.</span></span>
* <span data-ttu-id="cfa18-1466">Удалено свойство `ApplicationPackages` в `PSApplication`, который возвращается из **Get-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1466">Removed `ApplicationPackages` property of `PSApplication` returned by **Get-AzBatchApplication**.</span></span>
  - <span data-ttu-id="cfa18-1467">Отдельные пакеты в приложении теперь можно извлечь с помощью **Get-AzBatchApplicationPackage**.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1467">The specific packages inside of an application now can be retrieved using **Get-AzBatchApplicationPackage**.</span></span> <span data-ttu-id="cfa18-1468">Например: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1468">For example: `Get-AzBatchApplication -AccountName myaccount -ResourceGroupName myresourcegroup -ApplicationId myapplication`.</span></span>
* <span data-ttu-id="cfa18-1469">`ApplicationId` переименован в `ApplicationName` для **Get-AzBatchApplicationPackage** , **New-AzBatchApplicationPackage** , **Remove-AzBatchApplicationPackage** , **Get-AzBatchApplication** , **New-AzBatchApplication** , **Remove-AzBatchApplication** и **Set-AzBatchApplication**.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1469">Renamed `ApplicationId` to `ApplicationName` on **Get-AzBatchApplicationPackage** , **New-AzBatchApplicationPackage** , **Remove-AzBatchApplicationPackage** , **Get-AzBatchApplication** , **New-AzBatchApplication** , **Remove-AzBatchApplication** , and **Set-AzBatchApplication**.</span></span>
  - <span data-ttu-id="cfa18-1470">Теперь `ApplicationId` является псевдонимом для `ApplicationName`.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1470">`ApplicationId` now is an alias of `ApplicationName`.</span></span>
* <span data-ttu-id="cfa18-1471">Добавлено новое свойство `PSWindowsUserConfiguration` в `PSUserAccount`.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1471">Added new `PSWindowsUserConfiguration` property to `PSUserAccount`.</span></span>
* <span data-ttu-id="cfa18-1472">`Version` переименован в `Name` для `PSApplicationPackage`.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1472">Renamed `Version` to `Name` on `PSApplicationPackage`.</span></span>
* <span data-ttu-id="cfa18-1473">`BlobSource` переименован в `HttpUrl` для `PSResourceFile`.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1473">Renamed `BlobSource` to `HttpUrl` on `PSResourceFile`.</span></span>
* <span data-ttu-id="cfa18-1474">Удалено свойство `OSDisk` из `PSVirtualMachineConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1474">Removed `OSDisk` property from `PSVirtualMachineConfiguration`.</span></span>
* <span data-ttu-id="cfa18-1475">Удалена операция **Set-AzBatchPoolOSVersion**.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1475">Removed **Set-AzBatchPoolOSVersion**.</span></span> <span data-ttu-id="cfa18-1476">Больше она не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1476">This operation is no longer supported.</span></span>
* <span data-ttu-id="cfa18-1477">Удалено `TargetOSVersion` из `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1477">Removed `TargetOSVersion` from `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="cfa18-1478">`CurrentOSVersion` переименован в `OSVersion` для `PSCloudServiceConfiguration`.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1478">Renamed `CurrentOSVersion` to `OSVersion` on `PSCloudServiceConfiguration`.</span></span>
* <span data-ttu-id="cfa18-1479">Удалено `DataEgressGiB` и `DataIngressGiB` из `PSPoolUsageMetrics`.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1479">Removed `DataEgressGiB` and `DataIngressGiB` from `PSPoolUsageMetrics`.</span></span>
* <span data-ttu-id="cfa18-1480">Операция **Get-AzBatchNodeAgentSku** удалена и заменена на **Get-AzBatchSupportedImage**.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1480">Removed **Get-AzBatchNodeAgentSku** and replaced it with  **Get-AzBatchSupportedImage**.</span></span>
  - <span data-ttu-id="cfa18-1481">**Get-AzBatchSupportedImage** возвращает те же данные, что и **Get-AzBatchNodeAgentSku** , но в более удобном формате.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1481">**Get-AzBatchSupportedImage** returns the same data as **Get-AzBatchNodeAgentSku** but in a more friendly format.</span></span>
  - <span data-ttu-id="cfa18-1482">Также возвращаются новые непроверенные образы.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1482">New non-verified images are also now returned.</span></span> <span data-ttu-id="cfa18-1483">Включается и дополнительная информация о `Capabilities` и `BatchSupportEndOfLife` для каждого образа.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1483">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>
* <span data-ttu-id="cfa18-1484">Добавлена возможность монтировать файловые системы на каждом узле пула с помощью нового параметра `MountConfiguration` в **New-AzBatchPool**.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1484">Added ability to mount remote file-systems on each node of a pool via the new `MountConfiguration` parameter of **New-AzBatchPool**.</span></span>
* <span data-ttu-id="cfa18-1485">Теперь поддерживаются правила безопасности сети, которые блокируют сетевой доступ к пулу по исходящему порту трафика.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1485">Now support network security rules blocking network access to a pool based on the source port of the traffic.</span></span> <span data-ttu-id="cfa18-1486">Это выполняется с помощью свойства `SourcePortRanges` для `PSNetworkSecurityGroupRule`.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1486">This is done via the `SourcePortRanges` property on `PSNetworkSecurityGroupRule`.</span></span>
* <span data-ttu-id="cfa18-1487">Что касается выполнения контейнеров, пакетная служба теперь поддерживает выполнение задачи в рабочей папке контейнера или рабочей папке задачи пакетной службы.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1487">When running a container, Batch now supports executing the task in the container working directory or in the Batch task working directory.</span></span> <span data-ttu-id="cfa18-1488">Выбор зависит от параметра `WorkingDirectory` в `PSTaskContainerSettings`.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1488">This is controlled by the `WorkingDirectory` property on `PSTaskContainerSettings`.</span></span>
* <span data-ttu-id="cfa18-1489">Добавлена возможность указать коллекцию общедоступных IP-адресов для `PSNetworkConfiguration` с помощью нового свойства `PublicIPs`.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1489">Added ability to specify a collection of public IPs on `PSNetworkConfiguration` via the new `PublicIPs` property.</span></span> <span data-ttu-id="cfa18-1490">Это гарантирует, что узлы в пуле будут иметь IP-адреса из списка, предоставленного пользователем.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1490">This guarantees nodes in the Pool will have an IP from the list user provided IPs.</span></span>
* <span data-ttu-id="cfa18-1491">Если значение не задано, по умолчанию для `WaitForSuccess` в `PSSTartTask` используется значение `$True` (ранее `$False`).</span><span class="sxs-lookup"><span data-stu-id="cfa18-1491">When not specified, the default value of `WaitForSuccess` on `PSSTartTask` is now `$True` (was `$False`).</span></span>
* <span data-ttu-id="cfa18-1492">Если значение не задано, по умолчанию для `Scope` в `PSAutoUserSpecification` используется значение `Pool` (ранее `Task` для Windows или `Pool` для Linux).</span><span class="sxs-lookup"><span data-stu-id="cfa18-1492">When not specified, the default value of `Scope` on `PSAutoUserSpecification` is now `Pool` (was `Task` on Windows and `Pool` on Linux).</span></span>

#### <a name="azcdn"></a><span data-ttu-id="cfa18-1493">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="cfa18-1493">Az.Cdn</span></span>
* <span data-ttu-id="cfa18-1494">Добавлены UrlRewriteAction и CacheKeyQueryStringAction в RulesEngine.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1494">Introduced UrlRewriteAction and CacheKeyQueryStringAction to RulesEngine.</span></span>
* <span data-ttu-id="cfa18-1495">Исправлено несколько ошибок, таких как отсутствующий входной параметр Selector в командлете New-AzDeliveryRuleCondition.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1495">Fixed several bugs like missing 'Selector' Input in New-AzDeliveryRuleCondition cmdlet.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cfa18-1496">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cfa18-1496">Az.Compute</span></span>
* <span data-ttu-id="cfa18-1497">Функция набора шифрования диска</span><span class="sxs-lookup"><span data-stu-id="cfa18-1497">Disk Encryption Set feature</span></span>
    - <span data-ttu-id="cfa18-1498">Новые командлеты:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span><span class="sxs-lookup"><span data-stu-id="cfa18-1498">New cmdlets:   New-AzDiskEncryptionSetConfig   New-AzDiskEncryptionSet   Get-AzDiskEncryptionSet   Remove-AzDiskEncryptionSet</span></span>
    - <span data-ttu-id="cfa18-1499">Добавлен параметр ProximityPlacementGroupId в следующие командлеты:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="cfa18-1499">DiskEncryptionSetId parameter is added to the following cmdlets:   Set-AzImageOSDisk   Set-AzVMOSDisk   Set-AzVmssStorageProfile   Add-AzImageDataDisk   New-AzVMDataDisk   Set-AzVMDataDisk   Add-AzVMDataDisk   Add-AzVmssDataDisk   Add-AzVmssVMDataDisk</span></span>
    - <span data-ttu-id="cfa18-1500">Параметры DiskEncryptionSetId и EncryptionType добавлены в следующие командлеты:   New-AzDiskConfig   New-AzSnapshotConfig</span><span class="sxs-lookup"><span data-stu-id="cfa18-1500">DiskEncryptionSetId and EncryptionType parameters are added to the following cmdlets:   New-AzDiskConfig   New-AzSnapshotConfig</span></span>
* <span data-ttu-id="cfa18-1501">Добавлен параметр PublicIPAddressVersion в New-AzVmssIPConfig</span><span class="sxs-lookup"><span data-stu-id="cfa18-1501">Add PublicIPAddressVersion parameter to New-AzVmssIPConfig</span></span>
* <span data-ttu-id="cfa18-1502">FileUris для расширения пользовательских скриптов теперь будет защищенным, а не общедоступным параметром</span><span class="sxs-lookup"><span data-stu-id="cfa18-1502">Move FileUris of custom script extension from public setting to protected setting</span></span>
* <span data-ttu-id="cfa18-1503">Добавлено ScaleInPolicy в командлеты New-AzVmss, New-AzVmssConfig и Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="cfa18-1503">Add ScaleInPolicy to New-AzVmss, New-AzVmssConfig and Update-AzVmss cmdlets</span></span>
* <span data-ttu-id="cfa18-1504">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="cfa18-1504">Breaking changes</span></span>
    - <span data-ttu-id="cfa18-1505">Параметр UploadSizeInBytes применяется теперь вместо DiskSizeGB для New-AzDiskConfig, если CreateOption имеет значение Upload</span><span class="sxs-lookup"><span data-stu-id="cfa18-1505">UploadSizeInBytes parameter is used instead of DiskSizeGB for New-AzDiskConfig when CreateOption is Upload</span></span>
    - <span data-ttu-id="cfa18-1506">PublishingProfile.Source.ManagedImage.Id заменяется на StorageProfile.Source.Id в объекте GalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="cfa18-1506">PublishingProfile.Source.ManagedImage.Id is replaced with StorageProfile.Source.Id in GalleryImageVersion object</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cfa18-1507">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cfa18-1507">Az.DataFactory</span></span>
* <span data-ttu-id="cfa18-1508">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.3.0.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1508">Update ADF .Net SDK version to 4.3.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cfa18-1509">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cfa18-1509">Az.DataLakeStore</span></span>
* <span data-ttu-id="cfa18-1510">Обновлен пакет SDK для ADLS (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), включает следующие исправления</span><span class="sxs-lookup"><span data-stu-id="cfa18-1510">Update ADLS SDK version (https://github.com/Azure/azure-data-lake-store-net/blob/preview-alpha/CHANGELOG.md#version-123-alpha), brings following fixes</span></span>
* <span data-ttu-id="cfa18-1511">Не создается исключение при невозможности десериализовать значение времени создания для записи в корзине или каталоге.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1511">Avoid throwing exception while unable to deserialize the creationtime of the trash or directory entry.</span></span>
* <span data-ttu-id="cfa18-1512">Предоставляется параметр для времени ожидания запроса в adlsclient</span><span class="sxs-lookup"><span data-stu-id="cfa18-1512">Expose setting per request timeout in adlsclient</span></span>
* <span data-ttu-id="cfa18-1513">Исправлена передача исходного значения syncflag для восстановления badoffset</span><span class="sxs-lookup"><span data-stu-id="cfa18-1513">Fix passing the original syncflag for badoffset recovery</span></span>
* <span data-ttu-id="cfa18-1514">Исправлена операция EnumerateDirectory, чтобы она извлекала токен продолжения после проверки ответа</span><span class="sxs-lookup"><span data-stu-id="cfa18-1514">Fix EnumerateDirectory to retrieve continuation token once response is checked</span></span>
* <span data-ttu-id="cfa18-1515">Исправлена ошибка объединения</span><span class="sxs-lookup"><span data-stu-id="cfa18-1515">Fix Concat Bug</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="cfa18-1516">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="cfa18-1516">Az.FrontDoor</span></span>
* <span data-ttu-id="cfa18-1517">Исправлены разные опечатки в разных частях модуля</span><span class="sxs-lookup"><span data-stu-id="cfa18-1517">Fixed miscellaneous typos across module</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="cfa18-1518">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cfa18-1518">Az.HDInsight</span></span>
* <span data-ttu-id="cfa18-1519">Исправлена ошибка, из-за которой клиент получал сообщение об ошибке 'Not a valid Base-64 string' (Не является допустимой строкой Base64) при выполнении Get-AzHDInsightCluster для получения кластера с хранилищем ADLSGen1.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1519">Fixed the bug that customer will get 'Not a valid Base-64 string' error when using Get-AzHDInsightCluster to get the cluster with ADLSGen1 storage.</span></span>
* <span data-ttu-id="cfa18-1520">Добавлен параметр с именем ApplicationId в три командлета Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig и New-AzHDInsightCluster, чтобы клиент мог предоставить идентификатор приложения субъекта-службы для доступа к Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1520">Add a parameter named 'ApplicationId' to three cmdlets Add-AzHDInsightClusterIdentity, New-AzHDInsightClusterConfig and New-AzHDInsightCluster so that customer can provide the service principal application id for accessing Azure Data Lake.</span></span>
* <span data-ttu-id="cfa18-1521">Для Microsoft.Azure.Management.HDInsight изменена версия с 2.1.0 на 5.1.0</span><span class="sxs-lookup"><span data-stu-id="cfa18-1521">Changed Microsoft.Azure.Management.HDInsight from 2.1.0 to 5.1.0</span></span>
* <span data-ttu-id="cfa18-1522">Удалены пять командлетов:</span><span class="sxs-lookup"><span data-stu-id="cfa18-1522">Removed five cmdlets:</span></span>
    - <span data-ttu-id="cfa18-1523">Get-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="cfa18-1523">Get-AzHDInsightOMS</span></span>
    - <span data-ttu-id="cfa18-1524">Enable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="cfa18-1524">Enable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="cfa18-1525">Disable-AzHDInsightOMS</span><span class="sxs-lookup"><span data-stu-id="cfa18-1525">Disable-AzHDInsightOMS</span></span>
    - <span data-ttu-id="cfa18-1526">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="cfa18-1526">Grant-AzHDInsightRdpServicesAccess</span></span>
    - <span data-ttu-id="cfa18-1527">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="cfa18-1527">Revoke-AzHDInsightRdpServicesAccess</span></span>
* <span data-ttu-id="cfa18-1528">Добавлены три командлета:</span><span class="sxs-lookup"><span data-stu-id="cfa18-1528">Added three cmdlets:</span></span>
    - <span data-ttu-id="cfa18-1529">Get-AzHDInsightMonitoring заменяет собой Get-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1529">Get-AzHDInsightMonitoring to replace Get-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="cfa18-1530">Enable-AzHDInsightMonitoring заменяет собой Enable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1530">Enable-AzHDInsightMonitoring to replace Enable-AzHDInsightOMS.</span></span>
    - <span data-ttu-id="cfa18-1531">Disable-AzHDInsightMonitoring заменяет собой Disable-AzHDInsightOMS.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1531">Disable-AzHDInsightMonitoring to replace Disable-AzHDInsightOMS.</span></span>
* <span data-ttu-id="cfa18-1532">Исправлен командлет Get-AzHDInsightProperties, чтобы он поддерживал получение сведений о возможностях из определенного расположения.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1532">Fixed cmdlet Get-AzHDInsightProperties to support get capabilities information from a specific location.</span></span>
* <span data-ttu-id="cfa18-1533">Удалены наборы параметров ("Spark1", "Spark2") из Add-AzHDInsightConfigValue.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1533">Removed parameter sets('Spark1', 'Spark2') from Add-AzHDInsightConfigValue.</span></span>
* <span data-ttu-id="cfa18-1534">Добавлены примеры в справочные документы по командлету Add-AzHDInsightSecurityProfile.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1534">Add examples to the help documents of cmdlet Add-AzHDInsightSecurityProfile.</span></span>
* <span data-ttu-id="cfa18-1535">Изменен тип выходных данных для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="cfa18-1535">Changed output type of the following cmdlets:</span></span>
*  - <span data-ttu-id="cfa18-1536">Для Get-AzHDInsightProperties тип выходных данных изменен с CapabilitiesResponse на AzureHDInsightCapabilities.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1536">Changed the output type of Get-AzHDInsightProperties from  CapabilitiesResponse to AzureHDInsightCapabilities.</span></span>
*  - <span data-ttu-id="cfa18-1537">Для Remove-AzHDInsightCluster тип выходных данных изменен с ClusterGetResponse на bool.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1537">Changed the output type of Remove-AzHDInsightCluster from ClusterGetResponse to bool.</span></span>
*  - <span data-ttu-id="cfa18-1538">Для Set-AzHDInsightGatewaySettings тип выходных данных изменен с HttpConnectivitySettings на GatewaySettings.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1538">Changed the output type of Set-AzHDInsightGatewaySettings HttpConnectivitySettings to GatewaySettings.</span></span>
* <span data-ttu-id="cfa18-1539">Добавлены несколько условий для проверки сценариев.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1539">Added some scenario test cases.</span></span>
* <span data-ttu-id="cfa18-1540">Удалены несколько псевдонимов: Add-AzHDInsightConfigValues, Get-AzHDInsightProperties.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1540">Remove some alias: 'Add-AzHDInsightConfigValues', 'Get-AzHDInsightProperties'.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cfa18-1541">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cfa18-1541">Az.IotHub</span></span>
* <span data-ttu-id="cfa18-1542">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="cfa18-1542">Breaking changes:</span></span>
    - <span data-ttu-id="cfa18-1543">Командлет Add-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1543">The cmdlet 'Add-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="cfa18-1544">Удален набор параметров __AllParameterSets для командлета Add-AzIotHubEventHubConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1544">The parameter set '__AllParameterSets' for cmdlet 'Add-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="cfa18-1545">Командлет Get-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1545">The cmdlet 'Get-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="cfa18-1546">Удален набор параметров __AllParameterSets для командлета Get-AzIotHubEventHubConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1546">The parameter set '__AllParameterSets' for cmdlet 'Get-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="cfa18-1547">Удалено свойство OperationsMonitoringProperties для типа Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1547">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubProperties' has been removed.</span></span>
    - <span data-ttu-id="cfa18-1548">Удалено свойство OperationsMonitoringProperties для типа Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1548">The property 'OperationsMonitoringProperties' of type 'Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHubInputProperties' has been removed.</span></span>
    - <span data-ttu-id="cfa18-1549">Командлет New-AzIotHubExportDevice больше не поддерживает псевдоним New-AzIotHubExportDevices.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1549">The cmdlet 'New-AzIotHubExportDevice' no longer supports the alias 'New-AzIotHubExportDevices'.</span></span>
    - <span data-ttu-id="cfa18-1550">Командлет New-AzIotHubImportDevice больше не поддерживает псевдоним New-AzIotHubImportDevices.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1550">The cmdlet 'New-AzIotHubImportDevice' no longer supports the alias 'New-AzIotHubImportDevices'.</span></span>
    - <span data-ttu-id="cfa18-1551">Командлет Remove-AzIotHubEventHubConsumerGroup теперь не поддерживает параметр EventHubEndpointName и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1551">The cmdlet 'Remove-AzIotHubEventHubConsumerGroup' no longer supports the parameter 'EventHubEndpointName' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="cfa18-1552">Удален набор параметров __AllParameterSets для командлета Remove-AzIotHubEventHubConsumerGroup.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1552">The parameter set '__AllParameterSets' for cmdlet 'Remove-AzIotHubEventHubConsumerGroup' has been removed.</span></span>
    - <span data-ttu-id="cfa18-1553">Командлет Set-AzIotHub теперь не поддерживает параметр OperationsMonitoringProperties и не найдены псевдонимы для исходного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1553">The cmdlet 'Set-AzIotHub' no longer supports the parameter 'OperationsMonitoringProperties' and no alias was found for the original parameter name.</span></span>
    - <span data-ttu-id="cfa18-1554">Удален набор параметров UpdateOperationsMonitoringProperties для командлета Set-AzIotHub.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1554">The parameter set 'UpdateOperationsMonitoringProperties' for cmdlet 'Set-AzIotHub' has been removed.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cfa18-1555">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cfa18-1555">Az.RecoveryServices</span></span>
* <span data-ttu-id="cfa18-1556">Azure Site Recovery поддерживает настройку сетевых ресурсов, например групп безопасности сети, общедоступных IP-адресов и внутренних подсистем балансировки нагрузки из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1556">Azure Site Recovery support to configure networking resources like NSG, public IP and internal load balancers for Azure to Azure.</span></span>
* <span data-ttu-id="cfa18-1557">Azure Site Recovery поддерживает запись на управляемый диск из vMWare в Azure.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1557">Azure Site Recovery Support to write to managed disk for vMWare to Azure.</span></span>
* <span data-ttu-id="cfa18-1558">Azure Site Recovery поддерживает сокращение NIC из vMWare в Azure.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1558">Azure Site Recovery Support to NIC reduction for vMWare to Azure.</span></span>
* <span data-ttu-id="cfa18-1559">Azure Site Recovery поддерживает ускорение сети NIC из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1559">Azure Site Recovery Support to accelerated networking for Azure to Azure.</span></span>
* <span data-ttu-id="cfa18-1560">Azure Site Recovery поддерживает автоматическое обновление агента из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1560">Azure Site Recovery Support to agent auto update for Azure to Azure.</span></span>
* <span data-ttu-id="cfa18-1561">Azure Site Recovery поддерживает стандартный SSD-накопитель из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1561">Azure Site Recovery Support to Standard SSD for Azure to Azure.</span></span>
* <span data-ttu-id="cfa18-1562">Azure Site Recovery поддерживает двухпроходное шифрование диска Azure из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1562">Azure Site Recovery Support to Azure Disk Encryption two pass for Azure to Azure.</span></span>
* <span data-ttu-id="cfa18-1563">Azure Site Recovery поддерживает новый добавленный диск из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1563">Azure Site Recovery Support to protect newly added disk for Azure to Azure.</span></span>
* <span data-ttu-id="cfa18-1564">Добавлена функция SoftDelete для виртуальных машин и соответствующие тесты</span><span class="sxs-lookup"><span data-stu-id="cfa18-1564">Added SoftDelete feature for VM and added tests for softdelete</span></span>

#### <a name="azresources"></a><span data-ttu-id="cfa18-1565">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cfa18-1565">Az.Resources</span></span>
* <span data-ttu-id="cfa18-1566">Обновлена сборка зависимостей Microsoft.Extensions.Caching.Memory с версии 1.1.1 до 2.2</span><span class="sxs-lookup"><span data-stu-id="cfa18-1566">Update dependency assembly Microsoft.Extensions.Caching.Memory from 1.1.1 to 2.2</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cfa18-1567">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cfa18-1567">Az.Network</span></span>
* <span data-ttu-id="cfa18-1568">Изменены все командлеты для PrivateEndpointConnection, чтобы они поддерживали универсальный поставщик служб.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1568">Change all cmdlets for PrivateEndpointConnection to support generic service provider.</span></span>
    - <span data-ttu-id="cfa18-1569">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="cfa18-1569">Updated cmdlet:</span></span>
        - <span data-ttu-id="cfa18-1570">Approve-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1570">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="cfa18-1571">Deny-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1571">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="cfa18-1572">Get-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1572">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="cfa18-1573">Remove-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1573">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="cfa18-1574">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="cfa18-1574">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="cfa18-1575">Добавлен новый командлет для PrivateLinkResource, который поддерживает универсальный поставщик служб.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1575">Add new cmdlet for PrivateLinkResource and it also support generic service provider.</span></span>
    - <span data-ttu-id="cfa18-1576">Новый командлет</span><span class="sxs-lookup"><span data-stu-id="cfa18-1576">New cmdlet:</span></span>
        - <span data-ttu-id="cfa18-1577">Get-AzPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="cfa18-1577">Get-AzPrivateLinkResource</span></span>
* <span data-ttu-id="cfa18-1578">Добавлены новые поля и параметр для протокола прокси версии 2.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1578">Add new fields and parameter for the feature Proxy Protocol V2.</span></span>
    - <span data-ttu-id="cfa18-1579">Добавлено свойство EnableProxyProtocol в PrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="cfa18-1579">Add property EnableProxyProtocol in PrivateLinkService</span></span>
    - <span data-ttu-id="cfa18-1580">Добавлено свойство LinkIdentifier в PrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="cfa18-1580">Add property LinkIdentifier in PrivateEndpointConnection</span></span>
    - <span data-ttu-id="cfa18-1581">Обновлен New-AzPrivateLinkService для поддержки нового необязательного параметра EnableProxyProtocol.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1581">Updated New-AzPrivateLinkService to add a new optional parameter EnableProxyProtocol.</span></span>
* <span data-ttu-id="cfa18-1582">Исправлено описание параметра в справочной документации по командлету New-AzApplicationGatewaySku.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1582">Fix incorrect parameter description in 'New-AzApplicationGatewaySku' reference documentation</span></span>
* <span data-ttu-id="cfa18-1583">Новые командлеты для поддержки политики брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="cfa18-1583">New cmdlets to support the azure firewall policy</span></span>
* <span data-ttu-id="cfa18-1584">Добавлена поддержка дочерних ресурсов RouteTables для VirtualHub</span><span class="sxs-lookup"><span data-stu-id="cfa18-1584">Add support for child resource RouteTables of VirtualHub</span></span>
    - <span data-ttu-id="cfa18-1585">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="cfa18-1585">New cmdlets added:</span></span>
        - <span data-ttu-id="cfa18-1586">Add-AzVirtualHubRoute</span><span class="sxs-lookup"><span data-stu-id="cfa18-1586">Add-AzVirtualHubRoute</span></span>
        - <span data-ttu-id="cfa18-1587">Add-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="cfa18-1587">Add-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="cfa18-1588">Get-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="cfa18-1588">Get-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="cfa18-1589">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="cfa18-1589">Remove-AzVirtualHubRouteTable</span></span>
        - <span data-ttu-id="cfa18-1590">Set-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="cfa18-1590">Set-AzVirtualHub</span></span>
* <span data-ttu-id="cfa18-1591">Добавлена поддержка новых свойств SKU для VirtualHub и VirtualWANType в VirtualWan</span><span class="sxs-lookup"><span data-stu-id="cfa18-1591">Add support for new properties Sku of VirtualHub and VirtualWANType of VirtualWan</span></span>
    - <span data-ttu-id="cfa18-1592">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="cfa18-1592">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="cfa18-1593">New-AzVirtualHub: добавлен параметр Sku</span><span class="sxs-lookup"><span data-stu-id="cfa18-1593">New-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="cfa18-1594">Update-AzVirtualHub: добавлен параметр Sku</span><span class="sxs-lookup"><span data-stu-id="cfa18-1594">Update-AzVirtualHub : added parameter Sku</span></span>
        - <span data-ttu-id="cfa18-1595">New-AzVirtualWan: добавлен параметр VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="cfa18-1595">New-AzVirtualWan : added parameter VirtualWANType</span></span>
        - <span data-ttu-id="cfa18-1596">Update-AzVirtualWan: добавлен параметр VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="cfa18-1596">Update-AzVirtualWan : added parameter VirtualWANType</span></span>
* <span data-ttu-id="cfa18-1597">Добавлена поддержка свойства EnableInternetSecurity для HubVnetConnection, VpnConnection и ExpressRouteConnection</span><span class="sxs-lookup"><span data-stu-id="cfa18-1597">Add support for EnableInternetSecurity property for HubVnetConnection, VpnConnection and ExpressRouteConnection</span></span>
    - <span data-ttu-id="cfa18-1598">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="cfa18-1598">New cmdlets added:</span></span>
        - <span data-ttu-id="cfa18-1599">Update-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="cfa18-1599">Update-AzureRmVirtualHubVnetConnection</span></span>
    - <span data-ttu-id="cfa18-1600">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="cfa18-1600">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="cfa18-1601">New-AzureRmVirtualHubVnetConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="cfa18-1601">New-AzureRmVirtualHubVnetConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="cfa18-1602">New-AzureRmVpnConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="cfa18-1602">New-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="cfa18-1603">Update-AzureRmVpnConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="cfa18-1603">Update-AzureRmVpnConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="cfa18-1604">New-AzureRmExpressRouteConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="cfa18-1604">New-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
        - <span data-ttu-id="cfa18-1605">Set-AzureRmExpressRouteConnection: добавлен параметр EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="cfa18-1605">Set-AzureRmExpressRouteConnection : added parameter EnableInternetSecurity</span></span>
* <span data-ttu-id="cfa18-1606">Добавлена поддержка настройки политики верхнего уровня WebApplicationFirewall</span><span class="sxs-lookup"><span data-stu-id="cfa18-1606">Add support for Configuring TopLevel WebApplicationFirewall Policy</span></span>
    - <span data-ttu-id="cfa18-1607">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="cfa18-1607">New cmdlets added:</span></span>
        - <span data-ttu-id="cfa18-1608">New-AzApplicationGatewayFirewallPolicySetting</span><span class="sxs-lookup"><span data-stu-id="cfa18-1608">New-AzApplicationGatewayFirewallPolicySetting</span></span>
        - <span data-ttu-id="cfa18-1609">New-AzApplicationGatewayFirewallPolicyExclusion</span><span class="sxs-lookup"><span data-stu-id="cfa18-1609">New-AzApplicationGatewayFirewallPolicyExclusion</span></span>
        - <span data-ttu-id="cfa18-1610">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span><span class="sxs-lookup"><span data-stu-id="cfa18-1610">New-AzApplicationGatewayFirewallPolicyManagedRuleGroupOverride</span></span>
        - <span data-ttu-id="cfa18-1611">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span><span class="sxs-lookup"><span data-stu-id="cfa18-1611">New-AzApplicationGatewayFirewallPolicyManagedRuleOverride</span></span>
        - <span data-ttu-id="cfa18-1612">New-AzApplicationGatewayFirewallPolicyManagedRule</span><span class="sxs-lookup"><span data-stu-id="cfa18-1612">New-AzApplicationGatewayFirewallPolicyManagedRule</span></span>
        - <span data-ttu-id="cfa18-1613">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span><span class="sxs-lookup"><span data-stu-id="cfa18-1613">New-AzApplicationGatewayFirewallPolicyManagedRuleSet</span></span>
    - <span data-ttu-id="cfa18-1614">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="cfa18-1614">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="cfa18-1615">New-AzApplicationGatewayFirewallPolicy: добавлены параметры PolicySetting, ManagedRule</span><span class="sxs-lookup"><span data-stu-id="cfa18-1615">New-AzApplicationGatewayFirewallPolicy : added parameter PolicySetting, ManagedRule</span></span>
* <span data-ttu-id="cfa18-1616">Добавлена поддержка оператора Geo-Match для CustomRule</span><span class="sxs-lookup"><span data-stu-id="cfa18-1616">Added support for Geo-Match operator on CustomRule</span></span>
    - <span data-ttu-id="cfa18-1617">Добавлен параметр GeoMatch в оператор для FirewallCondition</span><span class="sxs-lookup"><span data-stu-id="cfa18-1617">Added GeoMatch to the operator on the FirewallCondition</span></span>
* <span data-ttu-id="cfa18-1618">Добавлена поддержка политики брандмауэра perListener и perSite</span><span class="sxs-lookup"><span data-stu-id="cfa18-1618">Added support for perListener and perSite Firewall policy</span></span>
    - <span data-ttu-id="cfa18-1619">В следующие командлеты добавлены необязательные параметры:</span><span class="sxs-lookup"><span data-stu-id="cfa18-1619">Cmdlets updated with optional parameters:</span></span>
        - <span data-ttu-id="cfa18-1620">New-AzApplicationGatewayHttpListener: добавлены параметры FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="cfa18-1620">New-AzApplicationGatewayHttpListener : added parameter FirewallPolicy, FirewallPolicyId</span></span>
        - <span data-ttu-id="cfa18-1621">New-AzApplicationGatewayPathRuleConfig: добавлены параметры FirewallPolicy, FirewallPolicyId</span><span class="sxs-lookup"><span data-stu-id="cfa18-1621">New-AzApplicationGatewayPathRuleConfig : added parameter FirewallPolicy, FirewallPolicyId</span></span>
* <span data-ttu-id="cfa18-1622">Исправлен учет регистра для требуемой подсети с именем AzureBastionSubnet в PSBastion</span><span class="sxs-lookup"><span data-stu-id="cfa18-1622">Fix required subnet with name AzureBastionSubnet in 'PSBastion' can be case insensitive</span></span>
* <span data-ttu-id="cfa18-1623">Поддержка полного доменного имени назначения в правилах сети и преобразованного полного доменного имени в правилах NAT для брандмауэра Azure</span><span class="sxs-lookup"><span data-stu-id="cfa18-1623">Support for Destination FQDNs in Network Rules and Translated FQDN in NAT Rules for Azure Firewall</span></span>
* <span data-ttu-id="cfa18-1624">Добавлена поддержка ресурсов верхнего уровня RouteTables для IpGroup</span><span class="sxs-lookup"><span data-stu-id="cfa18-1624">Add support for top level resource RouteTables of IpGroup</span></span>
    - <span data-ttu-id="cfa18-1625">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="cfa18-1625">New cmdlets added:</span></span>
        - <span data-ttu-id="cfa18-1626">New-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="cfa18-1626">New-AzIpGroup</span></span>
        - <span data-ttu-id="cfa18-1627">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="cfa18-1627">Remove-AzIpGroup</span></span>
        - <span data-ttu-id="cfa18-1628">Get-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="cfa18-1628">Get-AzIpGroup</span></span>
        - <span data-ttu-id="cfa18-1629">Set-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="cfa18-1629">Set-AzIpGroup</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="cfa18-1630">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cfa18-1630">Az.ServiceFabric</span></span>
* <span data-ttu-id="cfa18-1631">Удален командлет Add-AzServiceFabricApplicationCertificate, так как соответствующий сценарий выполняется командлетом Add-AzVmssSecret.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1631">Remove Add-AzServiceFabricApplicationCertificate cmdlet as this scenario is covered by Add-AzVmssSecret.</span></span>

#### <a name="azsql"></a><span data-ttu-id="cfa18-1632">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cfa18-1632">Az.Sql</span></span>
* <span data-ttu-id="cfa18-1633">Добавлена поддержка восстановления удаленных баз данных в управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1633">Added support for restore of dropped databases on Managed Instances.</span></span>
* <span data-ttu-id="cfa18-1634">Из кода удалены старые командлеты аудита.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1634">Deprecated from code old auditing cmdlets.</span></span>
* <span data-ttu-id="cfa18-1635">Удалены нерекомендуемые псевдонимы:</span><span class="sxs-lookup"><span data-stu-id="cfa18-1635">Removed deprecated aliases:</span></span>
* <span data-ttu-id="cfa18-1636">Get-AzSqlDatabaseIndexRecommendations (вместо него используйте Get-AzSqlDatabaseIndexRecommendation)</span><span class="sxs-lookup"><span data-stu-id="cfa18-1636">Get-AzSqlDatabaseIndexRecommendations (use Get-AzSqlDatabaseIndexRecommendation instead)</span></span>
* <span data-ttu-id="cfa18-1637">Get-AzSqlDatabaseRestorePoints (вместо него используйте Get-AzSqlDatabaseRestorePoint)</span><span class="sxs-lookup"><span data-stu-id="cfa18-1637">Get-AzSqlDatabaseRestorePoints (use Get-AzSqlDatabaseRestorePoint instead)</span></span>
* <span data-ttu-id="cfa18-1638">Удален командлет Get-AzSqlDatabaseSecureConnectionPolicy</span><span class="sxs-lookup"><span data-stu-id="cfa18-1638">Remove Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="cfa18-1639">Удалены псевдонимы для нерекомендуемых командлетов параметров оценки уязвимостей</span><span class="sxs-lookup"><span data-stu-id="cfa18-1639">Remove aliases for deprecated Vulnerability Assessment Settings cmdlets</span></span>
* <span data-ttu-id="cfa18-1640">Командлеты расширенного обнаружения угроз объявлены устаревшими</span><span class="sxs-lookup"><span data-stu-id="cfa18-1640">Deprecate Advanced Threat Detection Settings cmdlets</span></span>
* <span data-ttu-id="cfa18-1641">Добавлены командлеты для отключения и включения рекомендаций о конфиденциальности для столбцов в базе данных.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1641">Adding cmdlets to Disable and enable sensitivity recommendations on columns in a database.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cfa18-1642">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cfa18-1642">Az.Storage</span></span>
* <span data-ttu-id="cfa18-1643">Поддержка включения большой общей папки при создании или обновлении учетной записи хранения</span><span class="sxs-lookup"><span data-stu-id="cfa18-1643">Support enable Large File share when create or update Storage account</span></span>
    -  <span data-ttu-id="cfa18-1644">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cfa18-1644">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="cfa18-1645">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cfa18-1645">Set-AzStorageAccount</span></span>
* <span data-ttu-id="cfa18-1646">При закрытии или получении маркера файла пропускается проверка того, является ли входной путь файлом или каталогом, чтобы избежать сбоев при получении объектов в состоянии DeletePending.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1646">When close/get File handle, skip check the input path is File directory or File, to avoid failure with object in DeletePending status</span></span>
    -  <span data-ttu-id="cfa18-1647">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="cfa18-1647">Get-AzStorageFileHandle</span></span>
    -  <span data-ttu-id="cfa18-1648">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="cfa18-1648">Close-AzStorageFileHandle</span></span>

## <a name="280---october-2019"></a><span data-ttu-id="cfa18-1649">2.8.0 — октябрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1649">2.8.0 - October 2019</span></span>
### <a name="general"></a><span data-ttu-id="cfa18-1650">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="cfa18-1650">General</span></span>
* <span data-ttu-id="cfa18-1651">Выпуск Az.HealthcareApis 1.0.0</span><span class="sxs-lookup"><span data-stu-id="cfa18-1651">Az.HealthcareApis 1.0.0 release</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="cfa18-1652">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cfa18-1652">Az.Accounts</span></span>
* <span data-ttu-id="cfa18-1653">Обновление телеметрии и перезаписи URL-адресов для созданных модулей, исправление для модульных тестов Windows.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1653">Update telemetry and url rewriting for generated modules, fix windows unit tests.</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="cfa18-1654">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cfa18-1654">Az.ApiManagement</span></span>
* <span data-ttu-id="cfa18-1655">**Set-AzApiManagementApi**  — в ApiVersionSet добавлена поддержка обновления API.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1655">**Set-AzApiManagementApi** - Added support for Updating Api into ApiVersionSet</span></span>
    - <span data-ttu-id="cfa18-1656">исправлена проблема https://github.com/Azure/azure-powershell/issues/10068.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1656">Fix for issue https://github.com/Azure/azure-powershell/issues/10068</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cfa18-1657">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cfa18-1657">Az.Automation</span></span>
* <span data-ttu-id="cfa18-1658">Исправлен командлет New-AzureAutomationSoftwareUpdateConfiguration для параметра перезагрузки Linux.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1658">Fixed New-AzureAutomationSoftwareUpdateConfiguration cmdlet for Linux reboot setting parameter.</span></span>

#### <a name="azbatch"></a><span data-ttu-id="cfa18-1659">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="cfa18-1659">Az.Batch</span></span>
* <span data-ttu-id="cfa18-1660">Командлет **Get-AzBatchNodeAgentSku** объявлен устаревшим и будет заменен на **Get-AzBatchSupportImage** в версии 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1660">**Get-AzBatchNodeAgentSku** is deprecated and will be replaced by **Get-AzBatchSupportImage** in version 2.0.0.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cfa18-1661">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cfa18-1661">Az.Compute</span></span>
* <span data-ttu-id="cfa18-1662">В командлеты New-AzVM и New-AzVmss добавлены параметры Priority, EvictionPolicy и MaxPrice.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1662">Add Priority, EvictionPolicy, and MaxPrice parameters to New-AzVM and New-AzVmss cmdlets</span></span>
* <span data-ttu-id="cfa18-1663">Исправлены предупреждающее сообщение для командлетов Add-AzVMAdditionalUnattendContent и Add-AzVMSshPublicKey и справочная документация по ним.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1663">Fix warning message and help document for Add-AzVMAdditionalUnattendContent and Add-AzVMSshPublicKey cmdlets</span></span>
* <span data-ttu-id="cfa18-1664">Для Set-AzVMDiskEncryptionExtension исправлено исключение -skipVmBackup для виртуальных машин Linux с управляемыми дисками.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1664">Fix -skipVmBackup exception for Linux VMs with managed disks for Set-AzVMDiskEncryptionExtension.</span></span>
* <span data-ttu-id="cfa18-1665">Исправлена ошибка при изменении параметров шифрования в Set-AzVMDiskEncryptionExtension, реализован двухэтапный сценарий.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1665">Fix bug in update encryption settings in Set-AzVMDiskEncryptionExtension, two pass scenario.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cfa18-1666">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cfa18-1666">Az.DataFactory</span></span>
* <span data-ttu-id="cfa18-1667">Добавлены команды CRUD для потока данных Фабрики данных Azure версии 2: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow и Get-AzDataFactoryV2DataFlow.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1667">Adding CRUD commands for ADF V2 data flow: Set-AzDataFactoryV2DataFlow, Remove-AzDataFactoryV2DataFlow, and Get-AzDataFactoryV2DataFlow.</span></span>
* <span data-ttu-id="cfa18-1668">Добавлены команды действий для сеанса отладки потока данных Фабрики данных Azure версии 2: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand и Stop-AzDataFactoryV2DataFlowDebugSession.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1668">Adding action commands for ADF V2 data flow debug Session: Start-AzDataFactoryV2DataFlowDebugSession, Get-AzDataFactoryV2DataFlowDebugSession, Add-AzDataFactoryV2DataFlowDebugSessionPackage, Invoke-AzDataFactoryV2DataFlowDebugSessionCommand and Stop-AzDataFactoryV2DataFlowDebugSession.</span></span>
* <span data-ttu-id="cfa18-1669">Пакет SDK Фабрики данных Azure для .NET обновлен до версии 4.2.0.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1669">Update ADF .Net SDK version to 4.2.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cfa18-1670">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cfa18-1670">Az.DataLakeStore</span></span>
* <span data-ttu-id="cfa18-1671">Проверка учетной записи исправлена так, чтобы учетные записи, содержащие знак "-", можно было передавать без домена.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1671">Fix account validation so that accounts with '-' can be passed without domain</span></span>

#### <a name="azhealthcareapis"></a><span data-ttu-id="cfa18-1672">Az.HealthcareApis</span><span class="sxs-lookup"><span data-stu-id="cfa18-1672">Az.HealthcareApis</span></span>
* <span data-ttu-id="cfa18-1673">Версия PowerShell обновлена до 1.0.0.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1673">Updated the powershell version to 1.0.0</span></span>
* <span data-ttu-id="cfa18-1674">Версия пакета SDK обновлена до 1.0.2.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1674">Updated the SDK version to 1.0.2</span></span>
* <span data-ttu-id="cfa18-1675">В тестах обновлены ссылки на новую версию пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1675">Update in tests to refer to new SDK version</span></span>
* <span data-ttu-id="cfa18-1676">Вложенная выходная структура заменена на плоскую.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1676">Updated the output structure from nested to flattened.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cfa18-1677">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cfa18-1677">Az.IotHub</span></span>
* <span data-ttu-id="cfa18-1678">Добавлен новый источник маршрутизации DigitalTwinChangeEvents.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1678">Add new routing source: DigitalTwinChangeEvents</span></span>
* <span data-ttu-id="cfa18-1679">Исправлены незначительные ошибки: Get-AzIothub не возвращает subscriptionId.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1679">Minor bug fix: Get-AzIothub not returning subscriptionId</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cfa18-1680">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cfa18-1680">Az.Monitor</span></span>
* <span data-ttu-id="cfa18-1681">Добавлены новые получатели групп действий: -ItsmReceiver, -VoiceReceiver, -ArmRoleReceiver, -AzureFunctionReceiver, -LogicAppReceiver, -AutomationRunbookReceiver, -AzureAppPushReceiver.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1681">New action group receivers added for action group   -ItsmReceiver   -VoiceReceiver   -ArmRoleReceiver   -AzureFunctionReceiver   -LogicAppReceiver   -AutomationRunbookReceiver   -AzureAppPushReceiver</span></span>
* <span data-ttu-id="cfa18-1682">Для получателей включите общую схему оповещений.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1682">Use common alert schema enabled for the receivers.</span></span> <span data-ttu-id="cfa18-1683">Это не касается получателей SMS, push-уведомлений приложения Azure, ITSM и голосовых сообщений.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1683">This is not applicable for SMS, Azure App push , ITSM and Voice recievers</span></span>
* <span data-ttu-id="cfa18-1684">Веб-перехватчики теперь поддерживают аутентификацию Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1684">Webhooks now supports Azure active directory authentication .</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cfa18-1685">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cfa18-1685">Az.Network</span></span>
* <span data-ttu-id="cfa18-1686">Добавлен новый командлет Get-AzAvailableServiceAlias, позволяющий получить псевдонимы для политик конечной точки службы.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1686">Add new cmdlet Get-AzAvailableServiceAlias which can be called to get the aliases that can be used for Service Endpoint Policies.</span></span>
* <span data-ttu-id="cfa18-1687">В подключениях шлюза виртуальной сети появилась возможность добавлять селекторы трафика.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1687">Added support for the adding traffic selectors to Virtual Network Gateway Connections</span></span>
    - <span data-ttu-id="cfa18-1688">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="cfa18-1688">New cmdlets added:</span></span>
        - <span data-ttu-id="cfa18-1689">New-AzureRmTrafficSelectorPolicy.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1689">New-AzureRmTrafficSelectorPolicy</span></span>
    - <span data-ttu-id="cfa18-1690">В командлеты добавлены необязательные параметры -TrafficSelectorPolicies, -New-AzureRmVirtualNetworkGatewayConnection, -Set-AzureRmVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1690">Cmdlets updated with optional parameter -TrafficSelectorPolicies   -New-AzureRmVirtualNetworkGatewayConnection   -Set-AzureRmVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="cfa18-1691">В конфигурациях правил сетевой безопасности добавлена поддержка протоколов ESP и AH.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1691">Add support for ESP and AH protocols in network security rule configurations</span></span>
    - <span data-ttu-id="cfa18-1692">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="cfa18-1692">Updated cmdlets:</span></span>
        - <span data-ttu-id="cfa18-1693">Add-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1693">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="cfa18-1694">New-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1694">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="cfa18-1695">Set-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1695">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="cfa18-1696">Улучшена обработка исключений в командлетах Cortex.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1696">Improve handling of exceptions in Cortex cmdlets</span></span>
* <span data-ttu-id="cfa18-1697">Выпущены новые поколения и номера SKU VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1697">New Generations and SKUs for VirtualNetworkGateways</span></span>
  - <span data-ttu-id="cfa18-1698">Представлены новые поколения VirtualNetworkGateways.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1698">Introduce new Generations for VirtualNetworkGateways.</span></span>
  - <span data-ttu-id="cfa18-1699">Представлены новые номера SKU VirtualNetworkGateways с высокой пропускной способностью.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1699">Introduce new high throughput SKUs for VirtualNetworkGateways.</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="cfa18-1700">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="cfa18-1700">Az.RedisCache</span></span>
* <span data-ttu-id="cfa18-1701">В справочную документацию по Set-AzRedisCache добавлены недостающие значения для параметра -Size.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1701">Updated 'Set-AzRedisCache' reference documentation to include missing values for '-Size' parameter</span></span>

#### <a name="azsql"></a><span data-ttu-id="cfa18-1702">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cfa18-1702">Az.Sql</span></span>
* <span data-ttu-id="cfa18-1703">Добавлена возможность назначать администратора Active Directory в Управляемом экземпляре.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1703">Add support for setting Active Directory Administrator on Managed Instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cfa18-1704">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cfa18-1704">Az.Storage</span></span>
* <span data-ttu-id="cfa18-1705">Клиентская библиотека службы хранилища Azure обновлена до версии 11.1.0.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1705">Upgrade Storage Client Library to 11.1.0</span></span>
* <span data-ttu-id="cfa18-1706">NextPageLink теперь позволяет получить список контейнеров с помощью API плоскости управления.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1706">List containers with Management plane API, will list with NextPageLink</span></span>
    -  <span data-ttu-id="cfa18-1707">Get-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="cfa18-1707">Get-AzRmStorageContainer</span></span>
* <span data-ttu-id="cfa18-1708">NextPageLink теперь позволяет получить список учетных записей хранения из подписки.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1708">List Storage accounts from subscription, will list with NextPageLink</span></span>
    -  <span data-ttu-id="cfa18-1709">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cfa18-1709">Get-AzStorageAccount</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="cfa18-1710">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="cfa18-1710">Az.StorageSync</span></span>
* <span data-ttu-id="cfa18-1711">Исправлена проблема 9810 с Reset-AzStorageSyncServerCertificate.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1711">Fix Issue 9810 in Reset-AzStorageSyncServerCertificate.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cfa18-1712">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cfa18-1712">Az.Websites</span></span>
* <span data-ttu-id="cfa18-1713">Обновление плана службы приложений с помощью Set-AzWebApp приводило к сбою приложения.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1713">Set-AzWebApp updating ASP of an app was failing</span></span>

## <a name="270---september-2019"></a><span data-ttu-id="cfa18-1714">2.7.0 — сентябрь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1714">2.7.0 - September 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="cfa18-1715">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cfa18-1715">Az.ApiManagement</span></span>
* <span data-ttu-id="cfa18-1716">В справочной документации по командлету Set-AzApiManagementPolicy обновлено описание параметра -Format.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1716">Update '-Format' parameter description in 'Set-AzApiManagementPolicy' reference documentation</span></span>
* <span data-ttu-id="cfa18-1717">Из справочной документации удалены ссылки на нерекомендуемый командлет Update-AzApiManagementDeployment.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1717">Removed references of deprecated cmdlet 'Update-AzApiManagementDeployment' from reference documentation.</span></span> <span data-ttu-id="cfa18-1718">Вместо него следует использовать командлет Set-AzApiManagement.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1718">Use 'Set-AzApiManagement' instead.</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cfa18-1719">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cfa18-1719">Az.Automation</span></span>
* <span data-ttu-id="cfa18-1720">В справочной документации по командлету Register-AzAutomationDscNode исправлена опечатка в примере.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1720">Fixed example typo in reference documentation for 'Register-AzAutomationDscNode'</span></span>
* <span data-ttu-id="cfa18-1721">Добавлено уточнение об ограничениях ОС для командлета Register-AzAutomationDSCNode.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1721">Added clarification on OS restriction to Register-AzAutomationDSCNode</span></span>
* <span data-ttu-id="cfa18-1722">Исправлено исключение пустой ссылки для параметра -Wait в командлете Start-AzAutomationRunbook.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1722">Fixed Start-AzAutomationRunbook cmdlet Null reference exception for -Wait option.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cfa18-1723">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cfa18-1723">Az.Compute</span></span>
* <span data-ttu-id="cfa18-1724">Добавлен параметр UploadSizeInBytes для командлета New-AzDiskConfig.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1724">Add UploadSizeInBytes parameter tp New-AzDiskConfig</span></span>
* <span data-ttu-id="cfa18-1725">Добавлен добавочный параметр для командлета New-AzSnapshotConfig.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1725">Add Incremental parameter to New-AzSnapshotConfig</span></span>
* <span data-ttu-id="cfa18-1726">Для виртуальной машины добавлены такие функции с низким приоритетом:</span><span class="sxs-lookup"><span data-stu-id="cfa18-1726">Add a low priority virtual machine feature:</span></span>
    - <span data-ttu-id="cfa18-1727">Для командлета New-AzVMConfig добавлены параметры MaxPrice, EvictionPolicy и Priority.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1727">MaxPrice, EvictionPolicy and Priority parameters are added to New-AzVMConfig.</span></span>
    - <span data-ttu-id="cfa18-1728">Для командлетов New-AzVmssConfig, Update-AzVM и Update-AzVmss добавлен параметр MaxPrice.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1728">MaxPrice parameter is added to New-AzVmssConfig, Update-AzVM and Update-AzVmss cmdlets.</span></span>
* <span data-ttu-id="cfa18-1729">Для командлета Get-AzAvailabilitySet устранена проблема со ссылкой на виртуальную машину, когда в нем перечисляются все группы доступности в подписке.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1729">Fix VM reference issue for Get-AzAvailabilitySet cmdlet when it lists all availability sets in the subscription.</span></span>
* <span data-ttu-id="cfa18-1730">Исправлено исключение NULL для командлета Get-AzRemoteDesktopFile.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1730">Fix the null exception for Get-AzRemoteDesktopFile.</span></span>
* <span data-ttu-id="cfa18-1731">Исправлен метод поиска VHD для относительной конечной позиции.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1731">Fix VHD Seek method for end-relative position.</span></span>
* <span data-ttu-id="cfa18-1732">Устранена проблема с UltraSSD для командлетов New-AzVM и Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1732">Fix UltraSSD issue for New-AzVM and Update-AzVM.</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cfa18-1733">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cfa18-1733">Az.DataFactory</span></span>
* <span data-ttu-id="cfa18-1734">Добавлены 3 новые команды для ADF версии 2: Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription и Get-AzDataFactoryV2TriggerSubscriptionStatus.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1734">Adding 3 new commands for ADF V2 - Add-AzDataFactoryV2TriggerSubscription, Remove-AzDataFactoryV2TriggerSubscription, and Get-AzDataFactoryV2TriggerSubscriptionStatus</span></span>
* <span data-ttu-id="cfa18-1735">Пакет SDK ADF для .NET обновлен до версии 4.1.3.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1735">Updated ADF .Net SDK version to 4.1.3</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="cfa18-1736">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cfa18-1736">Az.HDInsight</span></span>
* <span data-ttu-id="cfa18-1737">Укажите критические изменения.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1737">Call out breaking changes</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cfa18-1738">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cfa18-1738">Az.IotHub</span></span>
* <span data-ttu-id="cfa18-1739">Добавлена поддержка для вызова отработки отказа для IotHub в георегион аварийного восстановления.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1739">Add support to invoke failover for an IotHub to the geo-paired disaster recovery region.</span></span>
* <span data-ttu-id="cfa18-1740">Добавлена поддержка для управления обогащением сообщений для IotHub.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1740">Add support to manage message enrichment for an IotHub.</span></span> <span data-ttu-id="cfa18-1741">Ниже перечислены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="cfa18-1741">New cmdlets are:</span></span>
    - <span data-ttu-id="cfa18-1742">Add-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="cfa18-1742">Add-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="cfa18-1743">Get-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="cfa18-1743">Get-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="cfa18-1744">Remove-AzIotHubMessageEnrichment;</span><span class="sxs-lookup"><span data-stu-id="cfa18-1744">Remove-AzIotHubMessageEnrichment</span></span>
    - <span data-ttu-id="cfa18-1745">Set-AzIotHubMessageEnrichment.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1745">Set-AzIotHubMessageEnrichment</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cfa18-1746">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cfa18-1746">Az.Monitor</span></span>
* <span data-ttu-id="cfa18-1747">Указание на самую последнюю версию пакета SDK для монитора, т. е. 0.24.1-preview:</span><span class="sxs-lookup"><span data-stu-id="cfa18-1747">Pointing to the most recent Monitor SDK, i.e. 0.24.1-preview</span></span>
   - <span data-ttu-id="cfa18-1748">В командлеты метрик добавлены некритические изменения, т. е. перечисление единиц поддерживает несколько новых значений.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1748">Adds non-braking changes to the Metrics cmdlets, i.e. the Unit enumeration supports several new values.</span></span> <span data-ttu-id="cfa18-1749">Эти командлеты доступны только для чтения, поэтому входные данные командлетов не будут изменены.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1749">These are read-only cmdlets, so there would be no change in the input of the cmdlets.</span></span>
   - <span data-ttu-id="cfa18-1750">Актуальная версия API запросов **ActionGroups**  — **2019-06-01**. До этого была версия **2018-03-01**.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1750">The api-version of the **ActionGroups** requests is now **2019-06-01** , before it was **2018-03-01**.</span></span> <span data-ttu-id="cfa18-1751">Тесты сценария обновлены в соответствии с этим изменением.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1751">The scenario tests have been updated to accommodate for this change.</span></span>
   - <span data-ttu-id="cfa18-1752">В конструкторы классов **EmailReceiver** и **WebhookReceiver** добавлен один новый обязательный аргумент — логическое значение с именем **useCommonAlertSchema**.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1752">The constructors for the classes **EmailReceiver** and **WebhookReceiver** added one new mandatory argument, i.e. a Boolean value called **useCommonAlertSchema**.</span></span> <span data-ttu-id="cfa18-1753">Сейчас для него установлено значение **false** , чтобы скрыть это критическое изменение от командлетов.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1753">Currently, the value is fixed to **false** to hide this breaking change from the cmdlets.</span></span> <span data-ttu-id="cfa18-1754">**Примечание**. Это временное изменение, которое должно быть подтверждено командой оповещения.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1754">**NOTE** : this is a temporary change that must be validated by the Alerts team.</span></span>
   - <span data-ttu-id="cfa18-1755">Порядок аргументов для конструктора класса **Source** (связанного с классом **ScheduledQueryRuleSource** ) изменился по сравнению с предыдущим пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1755">The order of the arguments for the constructor of the class **Source** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="cfa18-1756">Это изменение требует, чтобы были исправлены два модульных теста: они были скомпилированы, но не прошли тест.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1756">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
   - <span data-ttu-id="cfa18-1757">Порядок аргументов для конструктора класса **AlertingAction** (связанного с классом **ScheduledQueryRuleSource** ) изменился по сравнению с предыдущим пакетом SDK.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1757">The order of the arguments for the constructor of the class **AlertingAction** (related to the **ScheduledQueryRuleSource** class) changed from the previous SDK.</span></span> <span data-ttu-id="cfa18-1758">Это изменение требует, чтобы были исправлены два модульных теста: они были скомпилированы, но не прошли тест.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1758">This change required two unit tests to the be fixed: they compiled, but failed to pass the tests.</span></span>
* <span data-ttu-id="cfa18-1759">Добавлена поддержка критериев динамического порога для оповещения метрики версии 2:</span><span class="sxs-lookup"><span data-stu-id="cfa18-1759">Support Dynamic Threshold criteria for metric alert V2</span></span>
    - <span data-ttu-id="cfa18-1760">New-AzMetricAlertRuleV2Criteria: теперь также позволяет создавать критерии динамического порога.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1760">New-AzMetricAlertRuleV2Criteria: now creats dynamic threshold criteria also</span></span>
    - <span data-ttu-id="cfa18-1761">Add-AzMetricAlertRuleV2: теперь также позволяет принимать критерии динамического порога.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1761">Add-AzMetricAlertRuleV2: now accept dynamic threshold criteria also</span></span>
* <span data-ttu-id="cfa18-1762">Добавлены усовершенствования в командлетах запланированных правил запросов (SQR).</span><span class="sxs-lookup"><span data-stu-id="cfa18-1762">Improvements in Scheduled Query Rule cmdlets (SQR)</span></span>
 - <span data-ttu-id="cfa18-1763">Командлеты будут принимать параметр Location в обоих форматах: расположение (например, eastus) или отображаемое имя расположения (например, "восточная часть США").</span><span class="sxs-lookup"><span data-stu-id="cfa18-1763">Cmdlets will accept 'Location' paramater in both formats, either the location (e.g. eastus) or the location display name (e.g. East US)</span></span>
 - <span data-ttu-id="cfa18-1764">Параметр Enabled проиллюстрирован в файлах справки надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1764">Illustrated 'Enabled' parameter in help files properly</span></span>
 - <span data-ttu-id="cfa18-1765">Добавлены примеры для необязательного параметра ActionGroup.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1765">Added examples for 'ActionGroup' optional parameter</span></span>
 - <span data-ttu-id="cfa18-1766">Все файлы справки улучшены.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1766">Overall improved help files</span></span>
* <span data-ttu-id="cfa18-1767">Исправлена ошибка в определении типа области для командлета Set-AzActionRule.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1767">Fix bug in determining scope type for 'Set-AzActionRule'</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cfa18-1768">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cfa18-1768">Az.Network</span></span>
* <span data-ttu-id="cfa18-1769">Исправлен неправильный пример в справочной документации по командлету New-AzApplicationGateway.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1769">Fix incorrect example in 'New-AzApplicationGateway' reference documentation</span></span>
* <span data-ttu-id="cfa18-1770">В справочную документацию по командлету Get-AzNetworkWatcherPacketCapture добавлено примечание, посвященное извлечению всех свойств для записи пакетов.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1770">Add note in 'Get-AzNetworkWatcherPacketCapture' reference documentation about retrieving all properties for a packet capture</span></span>
* <span data-ttu-id="cfa18-1771">В справочной документации по командлету Test-AzNetworkWatcherIPFlow исправлен пример: теперь он правильно перечисляет сетевые карты.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1771">Fixed example in 'Test-AzNetworkWatcherIPFlow' reference documentation to correctly enumerate NICs</span></span>
* <span data-ttu-id="cfa18-1772">Улучшен анализ облачных исключений для отображения дополнительных сведений (при их наличии).</span><span class="sxs-lookup"><span data-stu-id="cfa18-1772">Improved cloud exception parsing to display additional details if they are present</span></span>
* <span data-ttu-id="cfa18-1773">Улучшен анализ облачных исключений для обработки дополнительного типа исключения SDK.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1773">Improved cloud exception parsing to handle additional type of SDK exception</span></span>
* <span data-ttu-id="cfa18-1774">Исправлено неправильное сопоставление моделей правил безопасности.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1774">Fixed incorrect mapping of Security Rule models</span></span>
* <span data-ttu-id="cfa18-1775">Добавлены свойства сетевого интерфейса для компонента частного IP-адреса.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1775">Added properties to network interface for private ip feature</span></span>
    - <span data-ttu-id="cfa18-1776">Для интерфейса PSNetworkInterface добавлено свойство PrivateEndpoint с типом PSResourceId.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1776">Added property 'PrivateEndpoint' as type of PSResourceId to PSNetworkInterface</span></span>
    - <span data-ttu-id="cfa18-1777">В PSNetworkInterfaceIPConfiguration добавлено свойство PrivateLinkConnectionProperties с типом PSIpConfigurationConnectivityInformation.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1777">Added property 'PrivateLinkConnectionProperties' as type of PSIpConfigurationConnectivityInformation to PSNetworkInterfaceIPConfiguration</span></span>
    - <span data-ttu-id="cfa18-1778">Добавлен новый класс модели: PSIpConfigurationConnectivityInformation.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1778">Added new model class PSIpConfigurationConnectivityInformation</span></span>
* <span data-ttu-id="cfa18-1779">Добавлен новый тип ApplicationRuleProtocolType "mssql" для ресурса Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1779">Added new ApplicationRuleProtocolType 'mssql' for Azure Firewall resource</span></span>
* <span data-ttu-id="cfa18-1780">Поддержка многоканального подключения в Виртуальной глобальной сети:</span><span class="sxs-lookup"><span data-stu-id="cfa18-1780">MultiLink support in Virtual WAN</span></span>
    - <span data-ttu-id="cfa18-1781">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="cfa18-1781">New cmdlets</span></span>
        - <span data-ttu-id="cfa18-1782">New-AzVpnSiteLink;</span><span class="sxs-lookup"><span data-stu-id="cfa18-1782">New-AzVpnSiteLink</span></span>
        - <span data-ttu-id="cfa18-1783">New-AzVpnSiteLinkConnection;</span><span class="sxs-lookup"><span data-stu-id="cfa18-1783">New-AzVpnSiteLinkConnection</span></span>
    - <span data-ttu-id="cfa18-1784">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="cfa18-1784">Updated cmdlet:</span></span>
        - <span data-ttu-id="cfa18-1785">New-VpnSite;</span><span class="sxs-lookup"><span data-stu-id="cfa18-1785">New-VpnSite</span></span>
        - <span data-ttu-id="cfa18-1786">Update-VpnSite;</span><span class="sxs-lookup"><span data-stu-id="cfa18-1786">Update-VpnSite</span></span>
        - <span data-ttu-id="cfa18-1787">New-VpnConnection;</span><span class="sxs-lookup"><span data-stu-id="cfa18-1787">New-VpnConnection</span></span>
        - <span data-ttu-id="cfa18-1788">Update-VpnConnection.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1788">Update-VpnConnection</span></span>
* <span data-ttu-id="cfa18-1789">Исправлены документы с некоторыми примерами PowerShell для использования командлетов AZ вместо командлетов AzureRM.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1789">Fixed documents for some PowerShell examples to use Az cmdlets instead of AzureRM cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cfa18-1790">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cfa18-1790">Az.RecoveryServices</span></span>
* <span data-ttu-id="cfa18-1791">Для объекта AzureVMpolicy добавлен новый атрибут — ProtectedItemsCount.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1791">Update AzureVMpolicy Object with ProtectedItemsCount Attribute</span></span>
* <span data-ttu-id="cfa18-1792">Добавлены тесты для политики виртуальной машины и восстановления исходной учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1792">Added Tests for VM policy and Original Storage Account Restore</span></span>

#### <a name="azresources"></a><span data-ttu-id="cfa18-1793">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cfa18-1793">Az.Resources</span></span>
* <span data-ttu-id="cfa18-1794">Исправлена ошибка, при которой не удавалось вызвать командлет New-AzRoleAssignment без параметра Scope.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1794">Fix bug where New-AzRoleAssignment could not be called without parameter Scope.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="cfa18-1795">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cfa18-1795">Az.ServiceFabric</span></span>
* <span data-ttu-id="cfa18-1796">Исправлена опечатка в примере в справочной документации по командлету Update-AzServiceFabricReliability.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1796">Fixed typo in example for 'Update-AzServiceFabricReliability' reference documentation</span></span>
* <span data-ttu-id="cfa18-1797">Добавлены новые командлеты для управления приложениями и службами:</span><span class="sxs-lookup"><span data-stu-id="cfa18-1797">Adding new cmdlets to manage appliaction and services:</span></span>
    - <span data-ttu-id="cfa18-1798">New-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="cfa18-1798">New-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="cfa18-1799">New-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="cfa18-1799">New-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="cfa18-1800">New-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="cfa18-1800">New-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="cfa18-1801">New-AzServiceFabricService;</span><span class="sxs-lookup"><span data-stu-id="cfa18-1801">New-AzServiceFabricService</span></span>
    - <span data-ttu-id="cfa18-1802">Update-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="cfa18-1802">Update-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="cfa18-1803">Get-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="cfa18-1803">Get-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="cfa18-1804">Get-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="cfa18-1804">Get-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="cfa18-1805">Get-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="cfa18-1805">Get-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="cfa18-1806">Get-AzServiceFabricService;</span><span class="sxs-lookup"><span data-stu-id="cfa18-1806">Get-AzServiceFabricService</span></span>
    - <span data-ttu-id="cfa18-1807">Remove-AzServiceFabricApplication;</span><span class="sxs-lookup"><span data-stu-id="cfa18-1807">Remove-AzServiceFabricApplication</span></span>
    - <span data-ttu-id="cfa18-1808">Remove-AzServiceFabricApplicationType;</span><span class="sxs-lookup"><span data-stu-id="cfa18-1808">Remove-AzServiceFabricApplicationType</span></span>
    - <span data-ttu-id="cfa18-1809">Remove-AzServiceFabricApplicationTypeVersion;</span><span class="sxs-lookup"><span data-stu-id="cfa18-1809">Remove-AzServiceFabricApplicationTypeVersion</span></span>
    - <span data-ttu-id="cfa18-1810">Remove-AzServiceFabricServic.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1810">Remove-AzServiceFabricServic</span></span>
* <span data-ttu-id="cfa18-1811">Пакет SDK для Service Fabric обновлен до версии 1.2.0, в которой используется версия API 2019-03-01 поставщика ресурсов Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1811">Upgraded Service Fabric SDK to version 1.2.0 which uses service fabric resource provider api-version 2019-03-01.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="cfa18-1812">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="cfa18-1812">Az.SignalR</span></span>
* <span data-ttu-id="cfa18-1813">Добавлены командлеты Update, Restart, CheckNameAvailability и GetUsage.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1813">Add Update, Restart, CheckNameAvailability, GetUsage Cmdlets</span></span>

#### <a name="azsql"></a><span data-ttu-id="cfa18-1814">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cfa18-1814">Az.Sql</span></span>
* <span data-ttu-id="cfa18-1815">Обновлен пример в справочной документации по командлету Get-AzSqlElasticPool.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1815">Update example in reference documentation for 'Get-AzSqlElasticPool'</span></span>
* <span data-ttu-id="cfa18-1816">Добавлен пример виртуального ядра для командлета создания эластичного пула (New-AzSqlElasticPool).</span><span class="sxs-lookup"><span data-stu-id="cfa18-1816">Added vCore example to creating an elastic pool (New-AzSqlElasticPool).</span></span>
* <span data-ttu-id="cfa18-1817">Удалена проверка свойства EmailAddresses и того, что свойство EmailAdmins правильное в случае, если свойство EmailAddresses пустое в командлетах Set-AzSqlServerAdvancedThreatProtectionPolicy и Set-AzSqlDatabaseAdvancedThreatProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1817">Remove the validation of EmailAddresses and the check that EmailAdmins is not false in case EmailAddresses is empty in Set-AzSqlServerAdvancedThreatProtectionPolicy and Set-AzSqlDatabaseAdvancedThreatProtectionPolicy</span></span>
* <span data-ttu-id="cfa18-1818">Теперь, если существует несколько параметров диагностики, включающих категорию аудита, параметры аудита сервера и базы данных удаляются.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1818">Enabled removal of server/database auditing settings when multiple diagnostic settings that enable audit category exist.</span></span>
* <span data-ttu-id="cfa18-1819">Исправлена проверка адресов электронной почты в нескольких командлетах оценки уязвимостей SQL (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting и Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span><span class="sxs-lookup"><span data-stu-id="cfa18-1819">Fix email addresses validation in multiple Sql Vulnerability Assessment cmdlets (Update-AzSqlDatabaseVulnerabilityAssessmentSetting, Update-AzSqlServerVulnerabilityAssessmentSetting, Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting and Update-AzSqlInstanceVulnerabilityAssessmentSetting).</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cfa18-1820">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cfa18-1820">Az.Storage</span></span>
* <span data-ttu-id="cfa18-1821">Обновлен пример в справочной документации по командлету Get-AzStorageAccountKey.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1821">Updated example in reference documentation for 'Get-AzStorageAccountKey'</span></span>
* <span data-ttu-id="cfa18-1822">Теперь при отправке и загрузке файла Azure в конечном файле сохраняются свойства SMB исходного файла (атрибуты файла, время создания файла, время последней записи файла).</span><span class="sxs-lookup"><span data-stu-id="cfa18-1822">In upload/Downalod Azure File,support perserve the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the destination file</span></span>
    -  <span data-ttu-id="cfa18-1823">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="cfa18-1823">Set-AzStorageFileContent</span></span>
    -  <span data-ttu-id="cfa18-1824">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="cfa18-1824">Get-AzStorageFileContent</span></span>
* <span data-ttu-id="cfa18-1825">Исправлена операция отправки блочного BLOB-объекта, в которой происходили сбои свойств и метаданных в контейнере с включенной ImmutabilityPolicy.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1825">Fix Upload block blob with properties/metadate fail on container enabled ImmutabilityPolicy.</span></span>
    -  <span data-ttu-id="cfa18-1826">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="cfa18-1826">Set-AzStorageBlobContent</span></span>
* <span data-ttu-id="cfa18-1827">Добавлена поддержка управления общими папками Azure в API плоскости управления с помощью таких командлетов:</span><span class="sxs-lookup"><span data-stu-id="cfa18-1827">Support manage Azure File shares with Management plane API</span></span>
    -  <span data-ttu-id="cfa18-1828">New-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="cfa18-1828">New-AzRmStorageShare</span></span>
    -  <span data-ttu-id="cfa18-1829">Get-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="cfa18-1829">Get-AzRmStorageShare</span></span>
    -  <span data-ttu-id="cfa18-1830">Update-AzRmStorageShare;</span><span class="sxs-lookup"><span data-stu-id="cfa18-1830">Update-AzRmStorageShare</span></span>
    -  <span data-ttu-id="cfa18-1831">Remove-AzRmStorageShare.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1831">Remove-AzRmStorageShare</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cfa18-1832">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cfa18-1832">Az.Websites</span></span>
* <span data-ttu-id="cfa18-1833">Устранена проблема, из-за которой теги webapp удалялись при переносе приложения в новый ASP.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1833">Fixing issue where webapp Tags were getting deleted when migrating App to new ASPwhere webapp Tags were getting deleted when migrating App to new ASP</span></span>
* <span data-ttu-id="cfa18-1834">Теперь командлет Publish-AzureWebapp работает в Linux и Windows.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1834">Fixing the Publish-AzureWebapp to work across Linux and windows</span></span>
* <span data-ttu-id="cfa18-1835">Обновлен пример в справочной документации по командлету Get-AzWebAppPublishingProfile.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1835">Update example in 'Get-AzWebAppPublishingProfile' reference documentation</span></span>

## <a name="260---august-2019"></a><span data-ttu-id="cfa18-1836">2.6.0 — август 2019 г.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1836">2.6.0 - August 2019</span></span>
#### <a name="general"></a><span data-ttu-id="cfa18-1837">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="cfa18-1837">General</span></span>
* <span data-ttu-id="cfa18-1838">Исправлены опечатки в модулях.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1838">Fixed miscellaneous typos across numerous modules</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="cfa18-1839">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cfa18-1839">Az.Accounts</span></span>
* <span data-ttu-id="cfa18-1840">Добавлена поддержка назначаемого пользователем удостоверения MSI при проверке подлинности в Функциях Azure (№ 9479).</span><span class="sxs-lookup"><span data-stu-id="cfa18-1840">Support user-assigned MSI in Azure Functiosn Authentication (#9479)</span></span>

#### <a name="azaks"></a><span data-ttu-id="cfa18-1841">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="cfa18-1841">Az.Aks</span></span>
* <span data-ttu-id="cfa18-1842">Устранена проблема с выходными данными для Get-AzAks.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1842">Fix issue with output for 'Get-AzAks'</span></span>
    * <span data-ttu-id="cfa18-1843">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/9847.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1843">More information here: https://github.com/Azure/azure-powershell/issues/9847</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="cfa18-1844">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cfa18-1844">Az.ApiManagement</span></span>
* <span data-ttu-id="cfa18-1845">исправлена проблема https://github.com/Azure/azure-powershell/issues/9351.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1845">Fix for issue https://github.com/Azure/azure-powershell/issues/9351</span></span>
    - <span data-ttu-id="cfa18-1846">Обновлена версия NuGet для .NET, которая не накладывает ограничений на productId, apiId, groupId и userId.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1846">Update .net nuget version, which does not enforce restrictions on productId, apiId, groupId and userId</span></span>
* <span data-ttu-id="cfa18-1847">**Get-AzApiManagementProduct**. Добавлена поддержка запросов к продуктам с помощью API.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1847">**Get-AzApiManagementProduct** - Added support for querying products using Api.</span></span>
  https://github.com/Azure/azure-powershell/issues/9482
* <span data-ttu-id="cfa18-1848">**New-AzApiManagementApiRevision**. Устранена проблема, из-за которой не задавался параметр ApiRevisionDescription при создании новой редакции API https://github.com/Azure/azure-powershell/issues/9752.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1848">**New-AzApiManagementApiRevision** - Fix for issue where ApiRevisionDescription was not being set when creating new api revision https://github.com/Azure/azure-powershell/issues/9752</span></span>
* <span data-ttu-id="cfa18-1849">Исправлено написание имени модели c PsApiManagementOAuth2AuthrozationServer на PsApiManagementOAuth2AuthorizationServer.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1849">Fixed typo in model 'PsApiManagementOAuth2AuthrozationServer' to 'PsApiManagementOAuth2AuthorizationServer'</span></span>

#### <a name="azbatch"></a><span data-ttu-id="cfa18-1850">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="cfa18-1850">Az.Batch</span></span>
* <span data-ttu-id="cfa18-1851">Исправлена опечатка в написании Windows со строчной буквы в справочных сообщениях и документации.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1851">Fixed typo in help message and documentation to capitalize Windows</span></span>

#### <a name="azcdn"></a><span data-ttu-id="cfa18-1852">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="cfa18-1852">Az.Cdn</span></span>
* <span data-ttu-id="cfa18-1853">Исправлена опечатка во вспомогательном приложении модуля CDN.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1853">Fixed a typo in CDN module conversion helper</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cfa18-1854">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cfa18-1854">Az.Compute</span></span>
* <span data-ttu-id="cfa18-1855">Добавлен параметр VmssId в новый командлет Add New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1855">Add VmssId to New-AzVMConfig cmdlet</span></span>
* <span data-ttu-id="cfa18-1856">Добавлены параметры TerminateScheduledEvents и TerminateScheduledEventNotBeforeTimeoutInMinutes в New-AzVmssConfig и Update-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1856">Add TerminateScheduledEvents and TerminateScheduledEventNotBeforeTimeoutInMinutes parameters to New-AzVmssConfig and Update-AzVmss</span></span>
* <span data-ttu-id="cfa18-1857">Добавлено свойство HyperVGeneration в объект образа виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1857">Add HyperVGeneration property to VM image object</span></span>
* <span data-ttu-id="cfa18-1858">Добавлены компоненты Host и HostGroup.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1858">Add Host and HostGroup features</span></span>
    - <span data-ttu-id="cfa18-1859">Новые командлеты:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="cfa18-1859">New cmdlets:   New-AzHostGroup   New-AzHost   Get-AzHostGroup   Get-AzHost   Remove-AzHostGroup   Remove-AzHost</span></span>
    - <span data-ttu-id="cfa18-1860">Параметр HostId добавлен в New-AzVMConfig и New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1860">HostId parameter is added to New-AzVMConfig and New-AzVM</span></span>
* <span data-ttu-id="cfa18-1861">Исправлен пример в документации по Invoke-AzVMRunCommand, в котором теперь используется правильное имя параметра.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1861">Update example in 'Invoke-AzVMRunCommand' documentation to use correct parameter name</span></span>
* <span data-ttu-id="cfa18-1862">Исправлено описание VolumeType в справочной документации по Set-AzVMDiskEncryptionExtension и Set-AzVmssDiskEncryptionExtension.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1862">Update '-VolumeType' description in 'Set-AzVMDiskEncryptionExtension' and 'Set-AzVmssDiskEncryptionExtension' reference documentation</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cfa18-1863">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cfa18-1863">Az.DataFactory</span></span>
* <span data-ttu-id="cfa18-1864">Исправлена опечатка в написании Windows со строчной буквы в документации по New-AzDataFactoryEncryptValue.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1864">Fix typo to capitalize 'Windows' in 'New-AzDataFactoryEncryptValue' documentation</span></span>
* <span data-ttu-id="cfa18-1865">Пакет SDK ADF для .NET обновлен до версии 4.1.2.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1865">Updated ADF .Net SDK version to 4.1.2</span></span>
* <span data-ttu-id="cfa18-1866">Добавлены параметры DataProxyIntegrationRuntimeName, DataProxyStagingLinkedServiceName и DataProxyStagingPath в командлет Set-AzureRmDataFactoryV2IntegrationRuntime, что позволяет настраивать локальную среду выполнения интеграции в качестве прокси-сервера для Azure-SSIS Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1866">Add parameter 'DataProxyIntegrationRuntimeName', 'DataProxyStagingLinkedServiceName' and 'DataProxyStagingPath' for 'Set-AzureRmDataFactoryV2IntegrationRuntime' cmd to enable set up Self-Hosted Integration Runtime as a proxy for SSIS Integration Runtime</span></span>
* <span data-ttu-id="cfa18-1867">Обновлены PSTriggerRun для отображения активированных конвейеров, сообщений и свойств и PSActivityRun для отображения типа действия.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1867">Updated PSTriggerRun to show the triggered pipelines, message and properties, and PSActivityRun to show the activity type</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cfa18-1868">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cfa18-1868">Az.DataLakeStore</span></span>
* <span data-ttu-id="cfa18-1869">Устранена проблема, при которой Get-DataLakeStoreDeletedItem переставал отвечать на запросы при возникновении ошибок или удаленных исключений.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1869">Fix hanging of Get-DataLakeStoreDeletedItem for any errors or remote exceptions.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="cfa18-1870">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="cfa18-1870">Az.EventHub</span></span>
* <span data-ttu-id="cfa18-1871">Исправлена проблема № 9658: опечатка в написании параметра VirtualNteworkRule у Set-AzEventHubNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1871">Fix for issue #9658 : Typo VirtualNteworkRule parameter in Set-AzEventHubNetworkRuleSet</span></span>
* <span data-ttu-id="cfa18-1872">Исправлена проблема № 9558: в Set-AzEventHubNamespace используется PATCH вместо PUT.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1872">Fix for issue #9558 : Set-AzEventHubNamespace is using PATCH instead of PUT</span></span>
* <span data-ttu-id="cfa18-1873">В командлет Set-AzEventHubNamespace добавлен параметр EnableKafka.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1873">added EnableKafka parameter to Set-AzEventHubNamespace cmdlet</span></span>
* <span data-ttu-id="cfa18-1874">Исправлена проблема № 9786: не удается создать правило с правами только для прослушивания.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1874">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>

#### <a name="azmarketplaceordering"></a><span data-ttu-id="cfa18-1875">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="cfa18-1875">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="cfa18-1876">Исправлено написание Azure со строчной буквы.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1876">Fixed documentation typo where 'Azure' was all lowercase letters</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cfa18-1877">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cfa18-1877">Az.Monitor</span></span>
* <span data-ttu-id="cfa18-1878">Исправлены неправильные имена параметров в справочной документации.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1878">Fixed incorrect parameter name in help documentation</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cfa18-1879">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cfa18-1879">Az.Network</span></span>
* <span data-ttu-id="cfa18-1880">Обновлен New-AzPrivateLinkServiceIpConfig.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1880">Updated New-AzPrivateLinkServiceIpConfig</span></span>
    - <span data-ttu-id="cfa18-1881">Параметр PublicIpAddress объявлен нерекомендуемым, так как он не используется на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1881">Deprecated the paramster 'PublicIpAddress' since this is never used in the server side.</span></span>
    - <span data-ttu-id="cfa18-1882">Добавлен необязательный параметр Primary, указывающий, является ли текущая IP-конфигурация основной.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1882">Added one optional parameter 'Primary' that indicate the current ip configuration is primary one or not.</span></span>
* <span data-ttu-id="cfa18-1883">Улучшена обработка исключений из-за ошибок запроса от пакета SDK. Устранена проблема, при которой исключения пакета SDK не обрабатывались правильно, из-за чего не отображались основные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1883">Improved handling of request error exception from SDK   -Fixes the issue that previously SDK exceptions aren't handled correctly which results in key error details not being displayed</span></span>
* <span data-ttu-id="cfa18-1884">Настроена логика проверки для префикса IPv6 IP-адреса для проверки правильности длины префикса IPv6.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1884">Adjusted validation logic for Ipv6 IP Prefix to check for correct IPv6 prefix length.</span></span>
* <span data-ttu-id="cfa18-1885">Обновлен Get-AzVirtualNetworkSubnetConfig: добавлен набор параметров для получения по идентификатору ресурса подсети.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1885">Updated Get-AzVirtualNetworkSubnetConfig: Added parameter set to get by subnet resource id.</span></span>
* <span data-ttu-id="cfa18-1886">Обновлено описание параметра Location для AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1886">Updated description of Location parameter for AzNetworkServiceTag</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="cfa18-1887">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cfa18-1887">Az.OperationalInsights</span></span>
* <span data-ttu-id="cfa18-1888">Обновлена документация по New-AzOperationalInsightsLinuxSyslogDataSource.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1888">Updated documentation for 'New-AzOperationalInsightsLinuxSyslogDataSource'</span></span>
    - <span data-ttu-id="cfa18-1889">Добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1889">Added example</span></span>
    - <span data-ttu-id="cfa18-1890">Обновлено описание параметра -Name.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1890">Updated description for '-Name' parameter</span></span>
* <span data-ttu-id="cfa18-1891">Добавлен пример для New-AzOperationalInsightsWindowsEventDataSource</span><span class="sxs-lookup"><span data-stu-id="cfa18-1891">Added an example for New-AzOperationalInsightsWindowsEventDataSource</span></span>
* <span data-ttu-id="cfa18-1892">Изменено описание параметра -Name для New-AzOperationalInsightsWindowsEventDataSource.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1892">Changed the description of the -Name parameter for New-AzOperationalInsightsWindowsEventDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cfa18-1893">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cfa18-1893">Az.RecoveryServices</span></span>
* <span data-ttu-id="cfa18-1894">Обновлен Get-AzRecoveryServicesBackupJobDetail.md.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1894">Update 'Get-AzRecoveryServicesBackupJobDetail.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="cfa18-1895">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cfa18-1895">Az.Resources</span></span>
* <span data-ttu-id="cfa18-1896">Добавлена поддержка новой версии API 2019-05-10 для Microsoft.Resource.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1896">Add support for new api version 2019-05-10 for Microsoft.Resource</span></span>
    - <span data-ttu-id="cfa18-1897">Добавлена поддержка copy.count = 0 для переменных, ресурсов и свойств.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1897">Add support for 'copy.count = 0' for variables, resources and properties</span></span>
    - <span data-ttu-id="cfa18-1898">Ресурсы, у которых condition = false или copy.count = 0, будут удаляться в полном режиме.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1898">Resources with 'condition = false' or 'copy.count = 0' will be deleted in complete mode</span></span>
* <span data-ttu-id="cfa18-1899">В справочную документацию добавлен пример назначения политики на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1899">Add an example of assigning policy at subscription level to help doc</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="cfa18-1900">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="cfa18-1900">Az.ServiceBus</span></span>
* <span data-ttu-id="cfa18-1901">Исправлена проблема № 9658: опечатка в написании параметра VirtualNetworkRule В Set-AzServiceBusNetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1901">Fix for issue #9658 : Typo VirtualNetworkRule parameter in Set-AzServiceBusNetworkRuleSet</span></span>
* <span data-ttu-id="cfa18-1902">Исправлена проблема № 9786: не удается создать правило с правами только для прослушивания.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1902">Fix for issue #9786 : cannot create a rule with Listen only rights</span></span>
* <span data-ttu-id="cfa18-1903">Добавлена новая команда Test-AzServiceBusNameAvailability для проверки доступности имени для очереди и раздела.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1903">Added new command 'Test-AzServiceBusNameAvailability' to check the name availability for queue and topic</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="cfa18-1904">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cfa18-1904">Az.ServiceFabric</span></span>
* <span data-ttu-id="cfa18-1905">Устранены ошибки командлета для добавления типа узла:</span><span class="sxs-lookup"><span data-stu-id="cfa18-1905">Fix add node type cmdlet bugs:</span></span>
    - <span data-ttu-id="cfa18-1906">ошибка NullReferenceException, возникавшая, если у группы ресурсов были другие VMSS, не связанные с кластером Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1906">NullReferenceException bug when resource group had other vmss not related to the service fabric cluster.</span></span> <span data-ttu-id="cfa18-1907">Исправлена проблема https://github.com/Azure/azure-powershell/issues/8681.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1907">Fixes issue: https://github.com/Azure/azure-powershell/issues/8681</span></span>
    - <span data-ttu-id="cfa18-1908">Исправлена ошибка, из-за которой командлет завершился сбоем, если virtualNetwork находилась не в той группе ресурсов, к которой относится кластер.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1908">Fix bug where cmdlet failed if virtualNetwork was in a different resource group that the cluster.</span></span> <span data-ttu-id="cfa18-1909">Исправлена проблема https://github.com/Azure/azure-powershell/issues/8407.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1909">fixes issue: https://github.com/Azure/azure-powershell/issues/8407</span></span>
    - <span data-ttu-id="cfa18-1910">Командлет Add-AzServiceFabricApplicationCertificate объявлен нерекомендуемым.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1910">Deprecating Add-AzServiceFabricApplicationCertificate cmdlet</span></span>

#### <a name="azsql"></a><span data-ttu-id="cfa18-1911">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cfa18-1911">Az.Sql</span></span>
* <span data-ttu-id="cfa18-1912">Обновление документации по старым командлетам аудита.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1912">Update documentation of old Auditing cmdlets.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cfa18-1913">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cfa18-1913">Az.Storage</span></span>
* <span data-ttu-id="cfa18-1914">Обновлена справка по Get/Close-AzStorageFileHandle: в примеры добавлены сценарии использования командлетов и обновлено описание параметров.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1914">Update help for Get/Close-AzStorageFileHandle, by add more scenarios to cmdlet examples and update parameter descriptions</span></span>
* <span data-ttu-id="cfa18-1915">Добавлена поддержка StandardBlobTier в операции отправки BLOB-объекта и копирования BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1915">Support StandardBlobTier in upload blob and copy blob</span></span>
    -  <span data-ttu-id="cfa18-1916">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="cfa18-1916">Set-AzStorageBlobContent</span></span>
    -  <span data-ttu-id="cfa18-1917">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="cfa18-1917">Start-AzStorageBlobCopy</span></span>
* <span data-ttu-id="cfa18-1918">Добавлена поддержка приоритета восстановления в операцию копирования BLOB-объекта.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1918">Support Rehydrate Priority in copy blob</span></span>
    -  <span data-ttu-id="cfa18-1919">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="cfa18-1919">Start-AzStorageBlobCopy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cfa18-1920">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cfa18-1920">Az.Websites</span></span>
* <span data-ttu-id="cfa18-1921">Добавлены уточнение для параметра -AppSettings в Set-AzWebApp и Set-AzWebAppSlot.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1921">Add clarification around -AppSettings parameter in Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <a name="250---july-2019"></a><span data-ttu-id="cfa18-1922">2.5.0 — июль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1922">2.5.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cfa18-1923">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cfa18-1923">Az.Accounts</span></span>
* <span data-ttu-id="cfa18-1924">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1924">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azapplicationinsights"></a><span data-ttu-id="cfa18-1925">Az.ApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="cfa18-1925">Az.ApplicationInsights</span></span>
* <span data-ttu-id="cfa18-1926">Исправлена опечатка в примере в документации по Remove-AzApplicationInsightsApiKey.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1926">Fix example typo in 'Remove-AzApplicationInsightsApiKey' documentation</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cfa18-1927">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cfa18-1927">Az.Automation</span></span>
* <span data-ttu-id="cfa18-1928">Исправлена опечатка в строке ресурса.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1928">Fix typo in resource string</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cfa18-1929">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cfa18-1929">Az.CognitiveServices</span></span>
* <span data-ttu-id="cfa18-1930">Добавлена поддержка NetworkRuleSet.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1930">Added NetworkRuleSet support.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cfa18-1931">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cfa18-1931">Az.Compute</span></span>
* <span data-ttu-id="cfa18-1932">Добавлены недостающие свойства (ComputerName, OsName, OsVersion и HyperVGeneration) для объекта представления экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1932">Add missing properties (ComputerName, OsName, OsVersion and HyperVGeneration) of VM instance view object.</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="cfa18-1933">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="cfa18-1933">Az.ContainerRegistry</span></span>
* <span data-ttu-id="cfa18-1934">Исправлена опечатка в Remove-AzContainerRegistryReplication для параметра репликации.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1934">Fix typo in Remove-AzContainerRegistryReplication for Replication parameter</span></span>
    - <span data-ttu-id="cfa18-1935">См. подробнее: https://github.com/Azure/azure-powershell/issues/9633.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1935">More information here https://github.com/Azure/azure-powershell/issues/9633</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cfa18-1936">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cfa18-1936">Az.DataFactory</span></span>
* <span data-ttu-id="cfa18-1937">Пакет SDK для ADF .NET обновлен до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1937">Updated ADF .Net SDK version to 4.1.0</span></span>
* <span data-ttu-id="cfa18-1938">Исправлена опечатка в документации по Get-AzDataFactoryV2PipelineRun.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1938">Fix typo in documentation for 'Get-AzDataFactoryV2PipelineRun'</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="cfa18-1939">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="cfa18-1939">Az.EventHub</span></span>
* <span data-ttu-id="cfa18-1940">Добавлен новый командлет для создания маркера SAS: New-AzEventHubAuthorizationRuleSASToken.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1940">Added new cmmdlet added for generating SAS token : New-AzEventHubAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="cfa18-1941">Добавлена проверка и сообщение об ошибке в ситуациях, когда для правил авторизации назначаются только права "Управление".</span><span class="sxs-lookup"><span data-stu-id="cfa18-1941">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cfa18-1942">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cfa18-1942">Az.KeyVault</span></span>
* <span data-ttu-id="cfa18-1943">Добавлена поддержка для настройки параметра KeySize в политиках сертификатов.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1943">Added support to specify the KeySize for Certificate Policies</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="cfa18-1944">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="cfa18-1944">Az.LogicApp</span></span>
* <span data-ttu-id="cfa18-1945">Get-AzIntegrationAccountMap теперь надлежащим образом выводит все типы сопоставлений.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1945">Fix for Get-AzIntegrationAccountMap to list all map types</span></span>
    - <span data-ttu-id="cfa18-1946">Добавлен новый параметр MapType для фильтрации.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1946">Added new MapType parameter for filtering</span></span>

#### <a name="azmanagedservices"></a><span data-ttu-id="cfa18-1947">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="cfa18-1947">Az.ManagedServices</span></span>
* <span data-ttu-id="cfa18-1948">Добавлена поддержка API версии 2019-06-01 (общедоступная).</span><span class="sxs-lookup"><span data-stu-id="cfa18-1948">Added support for api version 2019-06-01 (GA)</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cfa18-1949">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cfa18-1949">Az.Network</span></span>
* <span data-ttu-id="cfa18-1950">Добавлена поддержка частной конечной точки и службы приватного канала.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1950">Add support for private endpoint and private link service</span></span>
    - <span data-ttu-id="cfa18-1951">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="cfa18-1951">New cmdlets</span></span>
        - <span data-ttu-id="cfa18-1952">Set-AzPrivateEndpoint.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1952">Set-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="cfa18-1953">Set-AzPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1953">Set-AzPrivateLinkService</span></span>
        - <span data-ttu-id="cfa18-1954">Approve-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1954">Approve-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="cfa18-1955">Deny-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1955">Deny-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="cfa18-1956">Get-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1956">Get-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="cfa18-1957">Remove-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1957">Remove-AzPrivateEndpointConnection</span></span>
        - <span data-ttu-id="cfa18-1958">Test-AzPrivateLinkServiceVisibility.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1958">Test-AzPrivateLinkServiceVisibility</span></span>
        - <span data-ttu-id="cfa18-1959">Get-AzAutoApprovedPrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1959">Get-AzAutoApprovedPrivateLinkService</span></span>
* <span data-ttu-id="cfa18-1960">Обновлены следующие команды для функции: Флаг PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies в подсети в виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1960">Updated below commands for feature: PrivateEndpointNetworkPolicies/PrivateLinkServiceNetworkPolicies flag on Subnet in Virtualnetwork</span></span>
    - <span data-ttu-id="cfa18-1961">Обновлены командлеты New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1961">Updated New-AzVirtualNetworkSubnetConfig/Set-AzVirtualNetworkSubnetConfig/Add-AzVirtualNetworkSubnetConfig</span></span>
        - <span data-ttu-id="cfa18-1962">Добавлен необязательный параметр -PrivateEndpointNetworkPoliciesFlag, который определяет, следует ли применять сетевые политики к частной конечной точке в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1962">Added optional parameter -PrivateEndpointNetworkPoliciesFlag that configures whether to apply network policies on private endpoint in this subnet.</span></span>
        - <span data-ttu-id="cfa18-1963">Добавлен необязательный параметр -PrivateLinkServiceNetworkPoliciesFlag, который определяет, следует ли применять сетевые политики к службе приватного канала в этой подсети.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1963">Added optional parameter -PrivateLinkServiceNetworkPoliciesFlag that configures whether to apply network policies network policies on private link service in this subnet.</span></span>
* <span data-ttu-id="cfa18-1964">Параметр ServiceName командлета AzPrivateLinkService был переименован на Name с псевдонимом ServiceName для обеспечения обратной совместимости.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1964">AzPrivateLinkService's cmdlet parameter 'ServiceName' was renamed to 'Name' with an alias 'ServiceName' for backward compatibility</span></span>
* <span data-ttu-id="cfa18-1965">Включен протокол ICMP для настройки правил безопасности сети.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1965">Enable ICMP protocol for network security rule configurations</span></span>
    - <span data-ttu-id="cfa18-1966">Обновлены командлеты</span><span class="sxs-lookup"><span data-stu-id="cfa18-1966">Updated cmdlets</span></span>
        - <span data-ttu-id="cfa18-1967">Add-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1967">Add-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="cfa18-1968">New-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1968">New-AzNetworkSecurityRuleConfig</span></span>
        - <span data-ttu-id="cfa18-1969">Set-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1969">Set-AzNetworkSecurityRuleConfig</span></span>
* <span data-ttu-id="cfa18-1970">Добавлен ConnectionProtocolType (Ikev1/Ikev2) в качестве настраиваемого параметра для командлета New-AzVirtualNetworkGatewayConnection.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1970">Add ConnectionProtocolType (Ikev1/Ikev2) as a configurable parameter for New-AzVirtualNetworkGatewayConnection</span></span>
* <span data-ttu-id="cfa18-1971">Добавлен PrivateIpAddressVersion в LoadBalancerFrontendIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1971">Add PrivateIpAddressVersion in LoadBalancerFrontendIpConfiguration</span></span>
    - <span data-ttu-id="cfa18-1972">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="cfa18-1972">Updated cmdlet:</span></span>
        - <span data-ttu-id="cfa18-1973">New-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1973">New-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="cfa18-1974">Add-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1974">Add-AzLoadBalancerFrontendIpConfig</span></span>
        - <span data-ttu-id="cfa18-1975">Set-AzLoadBalancerFrontendIpConfig.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1975">Set-AzLoadBalancerFrontendIpConfig</span></span>
* <span data-ttu-id="cfa18-1976">Команда New-AzApplicationGatewayProbeConfig Шлюза приложений обновлена для поддержки настраиваемого порта в зонде.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1976">Application Gateway New-AzApplicationGatewayProbeConfig command update for supporting custom port in Probe</span></span>
    - <span data-ttu-id="cfa18-1977">Обновлен командлет New-AzApplicationGatewayProbeConfig: добавлен необязательный параметр Port, который используется при проверке внутреннего сервера.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1977">Updated New-AzApplicationGatewayProbeConfig: Added optional parameter Port which is used for probing backend server.</span></span> <span data-ttu-id="cfa18-1978">Этот параметр применяется к номерам SKU Standard_V2 и WAF_V2.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1978">This parameter is applicable for Standard_V2 and WAF_V2 SKU.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="cfa18-1979">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cfa18-1979">Az.OperationalInsights</span></span>
* <span data-ttu-id="cfa18-1980">Обновленная версия по умолчанию для сохраненных операций поиска имеет значение 1.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1980">Updated default version for saved searches to be 1.</span></span>
* <span data-ttu-id="cfa18-1981">Исправлены ошибки при обработке регулярных выражений со значениями NULL в журналах.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1981">Fixed custom log null regex handling</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cfa18-1982">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cfa18-1982">Az.RecoveryServices</span></span>
* <span data-ttu-id="cfa18-1983">Обновлен файл Get-AzRecoveryServicesBackupJob.md.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1983">Update 'Get-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="cfa18-1984">Обновлен файл Get-AzRecoveryServicesBackupContainer.md.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1984">Update 'Get-AzRecoveryServicesBackupContainer.md'</span></span>
* <span data-ttu-id="cfa18-1985">Обновлен файл Get-AzRecoveryServicesVault.md.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1985">Update 'Get-AzRecoveryServicesVault.md'</span></span>
* <span data-ttu-id="cfa18-1986">Обновлен файл Wait-AzRecoveryServicesBackupJob.md.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1986">Update 'Wait-AzRecoveryServicesBackupJob.md'</span></span>
* <span data-ttu-id="cfa18-1987">Обновлен файл Set-AzRecoveryServicesVaultContext.md.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1987">Update 'Set-AzRecoveryServicesVaultContext.md'</span></span>
* <span data-ttu-id="cfa18-1988">Обновлен файл Get-AzRecoveryServicesBackupItem.md.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1988">Update 'Get-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="cfa18-1989">Обновлен файл Get-AzRecoveryServicesBackupRecoveryPoint.md.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1989">Update 'Get-AzRecoveryServicesBackupRecoveryPoint.md'</span></span>
* <span data-ttu-id="cfa18-1990">Обновлен файл Restore-AzRecoveryServicesBackupItem.md.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1990">Update 'Restore-AzRecoveryServicesBackupItem.md'</span></span>
* <span data-ttu-id="cfa18-1991">Обновлен вызов службы для отмены регистрации контейнера в общей папке Azure.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1991">Updated service call for Unregistering container for Azure File Share</span></span>
* <span data-ttu-id="cfa18-1992">Обновлен файл Set-AzRecoveryServicesAsrAlertSetting.md.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1992">Update 'Set-AzRecoveryServicesAsrAlertSetting.md'</span></span>

#### <a name="azresources"></a><span data-ttu-id="cfa18-1993">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cfa18-1993">Az.Resources</span></span>
- <span data-ttu-id="cfa18-1994">Удален отсутствующий командлет, который упоминается в документации по New-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1994">Remove missing cmdlet referenced in 'New-AzResourceGroupDeployment' documentation</span></span>
- <span data-ttu-id="cfa18-1995">Обновлены командлеты политик для использования новой версии API 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1995">Updated policy cmdlets to use new api version 2019-01-01</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="cfa18-1996">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="cfa18-1996">Az.ServiceBus</span></span>
* <span data-ttu-id="cfa18-1997">Добавлен новый командлет для создания маркера SAS: New-AzServiceBusAuthorizationRuleSASToken.</span><span class="sxs-lookup"><span data-stu-id="cfa18-1997">Added new cmmdlet added for generating SAS token : New-AzServiceBusAuthorizationRuleSASToken</span></span>
* <span data-ttu-id="cfa18-1998">Добавлена проверка и сообщение об ошибке в ситуациях, когда для правил авторизации назначаются только права "Управление".</span><span class="sxs-lookup"><span data-stu-id="cfa18-1998">added verification and error message for authorizationrules rights if only 'Manage' is assigned</span></span>

#### <a name="azsql"></a><span data-ttu-id="cfa18-1999">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cfa18-1999">Az.Sql</span></span>
* <span data-ttu-id="cfa18-2000">Исправлены отсутствующие примеры для командлета Set-AzSqlDatabaseSecondary.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2000">Fix missing examples for Set-AzSqlDatabaseSecondary cmdlet</span></span>
* <span data-ttu-id="cfa18-2001">Исправлены заданные повторяющиеся проверки для оценки наличия уязвимостей без указания адресов электронной почты.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2001">Fix set Vulnerability Assessment recurring scans without providing any email addresses</span></span>
* <span data-ttu-id="cfa18-2002">Исправлена незначительная опечатка в сообщении предупреждения.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2002">Fix a small typo in a warining message.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cfa18-2003">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cfa18-2003">Az.Storage</span></span>
* <span data-ttu-id="cfa18-2004">Обновлен пример в справочной документации для использования командлетом Get-AzStorageAccount правильного имени параметра.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2004">Update example in reference documentation for 'Get-AzStorageAccount' to use correct parameter name</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="cfa18-2005">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="cfa18-2005">Az.StorageSync</span></span>
* <span data-ttu-id="cfa18-2006">Добавлен командлет Invoke-AzStorageSyncChangeDetection.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2006">Adding Invoke-AzStorageSyncChangeDetection cmdlet.</span></span>
* <span data-ttu-id="cfa18-2007">Исправлена проблема № 9551, связанная с TierFilesOlderThanDays.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2007">Fix Issue 9551 for honoring TierFilesOlderThanDays</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cfa18-2008">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cfa18-2008">Az.Websites</span></span>
* <span data-ttu-id="cfa18-2009">Исправлена ошибка, при которой некоторые свойства SiteConfig не возвращались Get-AzWebApp и Set-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2009">Fixing a bug where some SiteConfig properties were not returned by Get-AzWebApp and Set-AzWebApp</span></span>
* <span data-ttu-id="cfa18-2010">Добавлен новый параметр Location в Get-AzDeletedWebApp и Restore-AzDeletedWebApp.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2010">Adds a new Location parameter to Get-AzDeletedWebApp and Restore-AzDeletedWebApp</span></span>
* <span data-ttu-id="cfa18-2011">Исправлена ошибка, которая возникала при клонировании слотов веб-приложений с помощью командлета New-AzWebApp-IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2011">Fixes a bug with cloning web app slots using New-AzWebApp -IncludeSourceWebAppSlots</span></span>

## <a name="240---july-2019"></a><span data-ttu-id="cfa18-2012">2.4.0 — июль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2012">2.4.0 - July 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cfa18-2013">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cfa18-2013">Az.Accounts</span></span>
* <span data-ttu-id="cfa18-2014">Добавлена поддержка командлетов профиля.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2014">Add support for profile cmdlets</span></span>
* <span data-ttu-id="cfa18-2015">Добавлена поддержка сред и плоскостей данных в созданных командлетах.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2015">Add support for environments and data planes in generated cmdlets</span></span>
* <span data-ttu-id="cfa18-2016">Исправлена ошибка, когда в командлетах плоскости данных в Windows PowerShell в некоторых случаях использовалась неправильная конечная точка.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2016">Fix bug where incorrect endpoint was being used in some cases for data plane cmdlets in Windows PowerShell</span></span>

#### <a name="azadvisor"></a><span data-ttu-id="cfa18-2017">Az.Advisor</span><span class="sxs-lookup"><span data-stu-id="cfa18-2017">Az.Advisor</span></span>
* <span data-ttu-id="cfa18-2018">Выпущена общедоступная версия Az.Advisor.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2018">GA release of Az.Advisor</span></span>
* <span data-ttu-id="cfa18-2019">Теперь этот модуль входит в сводный модуль `Az`.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2019">This module is now included as a part of the roll-up `Az` module</span></span>

#### <a name="azapimanagement"></a><span data-ttu-id="cfa18-2020">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cfa18-2020">Az.ApiManagement</span></span>
* <span data-ttu-id="cfa18-2021">исправлена проблема https://github.com/Azure/azure-powershell/issues/8671.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2021">Fix for issue https://github.com/Azure/azure-powershell/issues/8671</span></span>
    - <span data-ttu-id="cfa18-2022">**Get-AzApiManagementSubscription**</span><span class="sxs-lookup"><span data-stu-id="cfa18-2022">**Get-AzApiManagementSubscription**</span></span>
        - <span data-ttu-id="cfa18-2023">Добавлена поддержка запрашивания подписок по пользователю и продукту.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2023">Added support for querying subscriptions by User and Product</span></span>
        - <span data-ttu-id="cfa18-2024">Добавлена поддержка создания запросов с использованием области "/", "/apis", "/apis/echo-api".</span><span class="sxs-lookup"><span data-stu-id="cfa18-2024">Added support for querying using Scope '/', '/apis', '/apis/echo-api'</span></span>
* <span data-ttu-id="cfa18-2025">Исправлены проблемы https://github.com/Azure/azure-powershell/issues/9307 и https://github.com/Azure/azure-powershell/issues/8432.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2025">Fix for issue https://github.com/Azure/azure-powershell/issues/9307 and https://github.com/Azure/azure-powershell/issues/8432</span></span>
    - <span data-ttu-id="cfa18-2026">**Import-AzApiManagementApi**</span><span class="sxs-lookup"><span data-stu-id="cfa18-2026">**Import-AzApiManagementApi**</span></span>
        - <span data-ttu-id="cfa18-2027">Добавлена поддержка указания ApiVersion и ApiVersionSetId при импорте API-интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2027">Added support for specifying 'ApiVersion' and 'ApiVersionSetId' when importing Apis</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cfa18-2028">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cfa18-2028">Az.Automation</span></span>
* <span data-ttu-id="cfa18-2029">Исправлена ошибка командлета Set-AzAutomationConnectionFieldValue при обработке строкового значения.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2029">Fixed Set-AzAutomationConnectionFieldValue cmdlet bug to handle string value.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cfa18-2030">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cfa18-2030">Az.Compute</span></span>
* <span data-ttu-id="cfa18-2031">В New AzImageConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2031">Add HyperVGeneration parameter to New-AzImageConfig</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cfa18-2032">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cfa18-2032">Az.DataFactory</span></span>
* <span data-ttu-id="cfa18-2033">Обновление выходных данных командлетов ADF, предназначенных для получения числа выполнений действий, конвейеров и триггеров, для поддержки канала Select-Object.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2033">Updating the output of get activity runs, get pipeline runs, and get trigger runs ADF cmdlets to support Select-Object pipe.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="cfa18-2034">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="cfa18-2034">Az.EventGrid</span></span>
* <span data-ttu-id="cfa18-2035">Исправлена опечатка в документации по командлету New-AzEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2035">Fix typo in 'New-AzEventGridSubscription' documentation</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cfa18-2036">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cfa18-2036">Az.IotHub</span></span>
* <span data-ttu-id="cfa18-2037">Добавлена поддержка повторного создания ключей политики авторизации.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2037">Add support to regenerate authorization policy keys.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cfa18-2038">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cfa18-2038">Az.Network</span></span>
* <span data-ttu-id="cfa18-2039">К тегам общедоступного IP-адреса добавлен тег RoutingPreference.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2039">Added 'RoutingPreference' to public ip tags</span></span>
* <span data-ttu-id="cfa18-2040">Улучшены примеры для справочной документации по командлету Get-AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2040">Improve examples for 'Get-AzNetworkServiceTag' reference documentation</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="cfa18-2041">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="cfa18-2041">Az.PolicyInsights</span></span>
* <span data-ttu-id="cfa18-2042">Исправлена проблема с пустой ссылкой в командлете Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2042">Fix null reference issue in Get-AzPolicyState</span></span>
    - <span data-ttu-id="cfa18-2043">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/9446.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2043">More information here: https://github.com/Azure/azure-powershell/issues/9446</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="cfa18-2044">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cfa18-2044">Az.OperationalInsights</span></span>
* <span data-ttu-id="cfa18-2045">Исправленная модель источника данных CustomLog возвращена в командлет Get-AzOperationalInsightsDataSource.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2045">Fixed CustomLog datasource model returned in Get-AzOperationalInsightsDataSource</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cfa18-2046">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cfa18-2046">Az.RecoveryServices</span></span>
* <span data-ttu-id="cfa18-2047">Выпущено исправление для команды get-policy для виртуальных машин IaaS.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2047">Fix for get-policy command for IaaSVMs</span></span>

#### <a name="azresources"></a><span data-ttu-id="cfa18-2048">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cfa18-2048">Az.Resources</span></span>
    - <span data-ttu-id="cfa18-2049">Исправлен текст справки по параметру Get-AzPolicyState -Top.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2049">Fix help text for Get-AzPolicyState -Top parameter</span></span>
    - <span data-ttu-id="cfa18-2050">Добавлена поддержка разбиения по страницам на стороне клиента для Get-AzPolicyAlias.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2050">Add client-side paging support for Get-AzPolicyAlias</span></span>
    - <span data-ttu-id="cfa18-2051">Добавлены новые параметры для Set-AzPolicyAssignment, -PolicyParameters и -PolicyParametersObject.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2051">Add new parameters for Set-AzPolicyAssignment, -PolicyParameters and -PolicyParametersObject</span></span>
    - <span data-ttu-id="cfa18-2052">Добавлен ряд обновлений документов и примеров для командлетов политик.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2052">Handful of doc and example updates for Policy cmdlets</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="cfa18-2053">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="cfa18-2053">Az.ServiceBus</span></span>
* <span data-ttu-id="cfa18-2054">Исправление ошибки № 4938: командлет New-AzureRmServiceBusQueue возвращает ответ BadRequest (Недопустимый запрос) при задании значения MaxSizeInMegabytes.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2054">Fix for issue #4938 - New-AzureRmServiceBusQueue returns BadRequest when setting MaxSizeInMegabytes</span></span>

#### <a name="azsql"></a><span data-ttu-id="cfa18-2055">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cfa18-2055">Az.Sql</span></span>
* <span data-ttu-id="cfa18-2056">Из выпуска предварительной версии в выпуск общедоступной версии добавлены командлеты группы отработки отказа экземпляра.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2056">Add Instance Failover Group cmdlets from preview release to public release</span></span>
* <span data-ttu-id="cfa18-2057">Поддержка аудита Azure SQL Server и баз данных с помощью новых командлетов:</span><span class="sxs-lookup"><span data-stu-id="cfa18-2057">Support Azure SQL Server\Database Auditing with new cmdlets.</span></span>
    - <span data-ttu-id="cfa18-2058">Set-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="cfa18-2058">Set-AzSqlServerAudit</span></span>
    - <span data-ttu-id="cfa18-2059">Get-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="cfa18-2059">Get-AzSqlServerAudit</span></span>
    - <span data-ttu-id="cfa18-2060">Remove-AzSqlServerAudit</span><span class="sxs-lookup"><span data-stu-id="cfa18-2060">Remove-AzSqlServerAudit</span></span>
    - <span data-ttu-id="cfa18-2061">Set-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="cfa18-2061">Set-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="cfa18-2062">Get-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="cfa18-2062">Get-AzSqlDatabaseAudit</span></span>
    - <span data-ttu-id="cfa18-2063">Remove-AzSqlDatabaseAudit</span><span class="sxs-lookup"><span data-stu-id="cfa18-2063">Remove-AzSqlDatabaseAudit</span></span>
* <span data-ttu-id="cfa18-2064">Из параметров оценки уязвимостей удалены ограничения, касающиеся электронной почты.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2064">Remove email constraints from Vulnerability Assessment settings</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cfa18-2065">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cfa18-2065">Az.Storage</span></span>
* <span data-ttu-id="cfa18-2066">Два параметра в указанном ниже командлете — -IndexDocument и -ErrorDocument404Path, — которые ранее были обязательными, стали необязательными:</span><span class="sxs-lookup"><span data-stu-id="cfa18-2066">Change 2 parameters '-IndexDocument' and '-ErrorDocument404Path' from required to optional  in cmdlet:</span></span>
    -  <span data-ttu-id="cfa18-2067">Enable-AzStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="cfa18-2067">Enable-AzStorageStaticWebsite</span></span>
* <span data-ttu-id="cfa18-2068">Обновлена справка по командлету Get-AzStorageBlobContent: добавлен пример.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2068">Update help of Get-AzStorageBlobContent by add an example</span></span>
* <span data-ttu-id="cfa18-2069">При сбое выполнения командлета с ошибкой StorageException отображаются дополнительные сведения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2069">Show more error information when cmdlet failed with StorageException</span></span>
* <span data-ttu-id="cfa18-2070">Добавлена поддержка создания или обновления учетной записи хранения с использованием проверки подлинности AAD DS для службы "Файлы Azure".</span><span class="sxs-lookup"><span data-stu-id="cfa18-2070">Support create or update Storage account with Azure Files AAD DS Authentication</span></span>
    -  <span data-ttu-id="cfa18-2071">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cfa18-2071">New-AzStorageAccount</span></span>
    -  <span data-ttu-id="cfa18-2072">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cfa18-2072">Set-AzStorageAccount</span></span>
* <span data-ttu-id="cfa18-2073">Добавлена поддержка перечисления или закрытия дескрипторов файлов для общей папки, каталога файлов или файла:</span><span class="sxs-lookup"><span data-stu-id="cfa18-2073">Support list or close file handles of a file share, file directory or a file</span></span>
    - <span data-ttu-id="cfa18-2074">Get-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="cfa18-2074">Get-AzStorageFileHandle</span></span>
    - <span data-ttu-id="cfa18-2075">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="cfa18-2075">Close-AzStorageFileHandle</span></span>

#### <a name="azstoragesync"></a><span data-ttu-id="cfa18-2076">Az.StorageSync</span><span class="sxs-lookup"><span data-stu-id="cfa18-2076">Az.StorageSync</span></span>
* <span data-ttu-id="cfa18-2077">Теперь этот модуль входит в сводный модуль `Az`.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2077">This module is now included as a part of the roll-up `Az` module</span></span>

## <a name="232---june-2019"></a><span data-ttu-id="cfa18-2078">2.3.2 — июнь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2078">2.3.2 - June 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cfa18-2079">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cfa18-2079">Az.Accounts</span></span>
* <span data-ttu-id="cfa18-2080">Исправлена ошибка, связанная с использованием неправильного URL-адреса для вызовов функций.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2080">Fix bug with incorrect URL being used in some cases for Functions calls</span></span>
    - <span data-ttu-id="cfa18-2081">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8983.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2081">More information here: https://github.com/Azure/azure-powershell/issues/8983</span></span>
* <span data-ttu-id="cfa18-2082">Устранена проблема с псевдонимами из AzureRM для командлетов Az.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2082">Fix Issue with aliases from AzureRM to Az cmdlets</span></span>
  - <span data-ttu-id="cfa18-2083">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2083">Set-AzureRmVMBootDiagnostics -> Set-AzVMBootDiagnostic</span></span>
  - <span data-ttu-id="cfa18-2084">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2084">Export-AzureRMLogAnalyticThrottledRequests -> Export-AzLogAnalyticThrottledRequest</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cfa18-2085">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cfa18-2085">Az.Compute</span></span>
* <span data-ttu-id="cfa18-2086">Простые наборы параметров New-AzVm и New-AzVmss теперь принимают параметр ProximityPlacementGroup.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2086">New-AzVm and New-AzVmss simple parameter sets now accept the 'ProximityPlacementGroup' parameter.</span></span>
* <span data-ttu-id="cfa18-2087">Исправлена опечатка в справочной документации по New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2087">Fix typo in 'New-AzVM' reference documentation</span></span>

#### <a name="azdns"></a><span data-ttu-id="cfa18-2088">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="cfa18-2088">Az.Dns</span></span>
* <span data-ttu-id="cfa18-2089">Исправлена опечатка в справочных примерах по использованию Set-AzDnsZone.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2089">Fixed a typo in 'Set-AzDnsZone' help examples.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="cfa18-2090">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="cfa18-2090">Az.EventGrid</span></span>
* <span data-ttu-id="cfa18-2091">Обновлен для использования API версии 2019-06-01.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2091">Updated to use the 2019-06-01 API version.</span></span>
* <span data-ttu-id="cfa18-2092">Новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="cfa18-2092">New cmdlets:</span></span>
    - <span data-ttu-id="cfa18-2093">New-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="cfa18-2093">New-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="cfa18-2094">Создает домен Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2094">Creates a new Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="cfa18-2095">Get-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="cfa18-2095">Get-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="cfa18-2096">Возвращает сведения о домене Сетки событий или список всех доменов Сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2096">Gets the details of an Event Grid Domain, or gets a list of all Event Grid Domains in the current Azure subscription.</span></span>
    - <span data-ttu-id="cfa18-2097">Remove-AzureRmEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="cfa18-2097">Remove-AzureRmEventGridDomain</span></span>
        - <span data-ttu-id="cfa18-2098">Удаляет домен Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2098">Removes an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="cfa18-2099">New-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="cfa18-2099">New-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="cfa18-2100">Повторно создает ключ общего доступа для домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2100">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>
    - <span data-ttu-id="cfa18-2101">Get-AzureRmEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="cfa18-2101">Get-AzureRmEventGridDomainKey</span></span>
        - <span data-ttu-id="cfa18-2102">Возвращает ключи общего доступа, используемые для публикации событий в домене Сетки событий.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2102">Gets the shared access keys used to publish events to an Event Grid Domain.</span></span>
    - <span data-ttu-id="cfa18-2103">New-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="cfa18-2103">New-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="cfa18-2104">Создает раздел домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2104">Creates a new Azure Event Grid Domain Topic.</span></span>
    - <span data-ttu-id="cfa18-2105">Get-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="cfa18-2105">Get-AzureRmEventGridDomainTopic</span></span>
        - <span data-ttu-id="cfa18-2106">Возвращает сведения о разделе домена Сетки событий или список всех разделов определенного домена Сетки событий в текущей подписке Azure.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2106">Gets the details of an Event Grid Domain Topic, or gets a list of all Event Grid Domain Topics under specific Event Grid Domain in the current Azure</span></span>
    - <span data-ttu-id="cfa18-2107">Remove-AzureRmEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="cfa18-2107">Remove-AzureRmEventGridDomainTopic:</span></span>
        - <span data-ttu-id="cfa18-2108">Удаляет раздел домена Сетки событий Azure.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2108">Removes an existing Azure Event Grid Domain Topic.</span></span>
* <span data-ttu-id="cfa18-2109">Обновлены командлеты:</span><span class="sxs-lookup"><span data-stu-id="cfa18-2109">Updated cmdlets:</span></span>
    - <span data-ttu-id="cfa18-2110">New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="cfa18-2110">New-AzureRmEventGridSubscription/Update-AzureRmEventGridSubscription:</span></span>
        - <span data-ttu-id="cfa18-2111">Добавляют новые обязательные параметры, обеспечивающие поддержку передачи по конвейеру для нового домена Сетки событий и раздела домена Сетки событий и позволяющие создавать подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2111">Add new mandatory parameters to support piping for the new Event Grid Domain and Event Grid Domain Topic to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="cfa18-2112">Добавляют новые обязательные параметры для указания имени нового домена Сетки событий и (или) имени раздела домена Сетки событий и позволяют создавать подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2112">Add new mandatory parameters for specifying the new Event Grid Domain name and/or Event Grid Domain Topic name to allow creating new event subscription under these resources.</span></span>
        - <span data-ttu-id="cfa18-2113">Добавляют новые наборы параметров для доменов и разделов домена и позволяют повторно использовать существующие параметры (например, EndPointType, SubjectBeginsWith и т. д.).</span><span class="sxs-lookup"><span data-stu-id="cfa18-2113">Add new Parameter sets for domains and domain topics to allow reusing existing parameters (e.g., EndPointType, SubjectBeginsWith, etc).</span></span>
        - <span data-ttu-id="cfa18-2114">Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="cfa18-2114">Add new optional parameters for specifying:</span></span>
            - <span data-ttu-id="cfa18-2115">срока действия подписки на событие;</span><span class="sxs-lookup"><span data-stu-id="cfa18-2115">Event subscription expiration date,</span></span>
            - <span data-ttu-id="cfa18-2116">параметров расширенной фильтрации.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2116">Advanced filtering parameters.</span></span>
        - <span data-ttu-id="cfa18-2117">Добавляют новое перечисление для ServiceBusQueue в качестве места назначения.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2117">Add new enum for servicebusqueue as destination.</span></span>
        - <span data-ttu-id="cfa18-2118">Запрещают использование значение All в параметре -IncludedEventType и заменяют его следующим:</span><span class="sxs-lookup"><span data-stu-id="cfa18-2118">Disallow usage of 'All' in -IncludedEventType option and replace it with</span></span>
    - <span data-ttu-id="cfa18-2119">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="cfa18-2119">Get-AzEventGridTopic, Get-AzEventGridDomain, Get-AzEventGridDomainTopic, Get-AzEventGridSubscription:</span></span>
        - <span data-ttu-id="cfa18-2120">Добавляют новые необязательные параметры (Top, ODataQuery и NextLink) для поддержки разбиения на страницы и фильтрации результатов.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2120">Add new optional parameters (Top, ODataQuery and NextLink) to support results pagination and filtering.</span></span>
    - <span data-ttu-id="cfa18-2121">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="cfa18-2121">Remove-AzureRmEventGridSubscription</span></span>
        - <span data-ttu-id="cfa18-2122">Добавляют новые обязательные параметры, обеспечивающие поддержку передачи по конвейеру для домена Сетки событий и раздела домена Сетки событий и позволяющие удалять подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2122">Add new mandatory parameters to support piping for Event Grid Domain and Event Grid Domain Topic to allow removing existing event subscription under these resources.</span></span>
        - <span data-ttu-id="cfa18-2123">Добавляют новые обязательные параметры для указания имени домена Сетки событий и (или) имени раздела домена Сетки событий и позволяют удалять подписки на события в этих ресурсах.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2123">Add new mandatory parameters for specifying the Event Grid Domain name and/or Event Grid Domain Topic name to allow removing existing event subscription under these resources.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="cfa18-2124">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="cfa18-2124">Az.FrontDoor</span></span>
* <span data-ttu-id="cfa18-2125">New-AzFrontDoorWafMatchConditionObject</span><span class="sxs-lookup"><span data-stu-id="cfa18-2125">New-AzFrontDoorWafMatchConditionObject</span></span>
    - <span data-ttu-id="cfa18-2126">Добавляет поддержку преобразований и новое значение оператора автозавершения (RegEx).</span><span class="sxs-lookup"><span data-stu-id="cfa18-2126">Add transforms support and new operator auto-complete value (RegEx)</span></span>
* <span data-ttu-id="cfa18-2127">New-AzFrontDoorWafManagedRuleObject</span><span class="sxs-lookup"><span data-stu-id="cfa18-2127">New-AzFrontDoorWafManagedRuleObject</span></span>
    - <span data-ttu-id="cfa18-2128">Добавляет новые значения автозавершения.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2128">Add new auto-complete values</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cfa18-2129">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cfa18-2129">Az.Network</span></span>
* <span data-ttu-id="cfa18-2130">Добавляет поддержку ресурса шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2130">Add support for Virtual Network Gateway Resource</span></span>
    - <span data-ttu-id="cfa18-2131">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="cfa18-2131">New cmdlets</span></span>
        - <span data-ttu-id="cfa18-2132">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span><span class="sxs-lookup"><span data-stu-id="cfa18-2132">Get-AzVirtualNetworkGatewayVpnClientConnectionHealth</span></span>
* <span data-ttu-id="cfa18-2133">Добавляет AvailablePrivateEndpointType.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2133">Add AvailablePrivateEndpointType</span></span>
    - <span data-ttu-id="cfa18-2134">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="cfa18-2134">New cmdlets</span></span>
        - <span data-ttu-id="cfa18-2135">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="cfa18-2135">Get-AzAvailablePrivateEndpointType</span></span>
* <span data-ttu-id="cfa18-2136">Добавляет PrivatePrivateLinkService.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2136">Add PrivatePrivateLinkService</span></span>
    - <span data-ttu-id="cfa18-2137">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="cfa18-2137">New cmdlets</span></span>
        - <span data-ttu-id="cfa18-2138">Get-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="cfa18-2138">Get-AzPrivateLinkService</span></span>
        - <span data-ttu-id="cfa18-2139">New-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="cfa18-2139">New-AzPrivateLinkService</span></span>
        - <span data-ttu-id="cfa18-2140">Remove-AzPrivateLinkService</span><span class="sxs-lookup"><span data-stu-id="cfa18-2140">Remove-AzPrivateLinkService</span></span>
        - <span data-ttu-id="cfa18-2141">New-AzPrivateLinkServiceIpConfig</span><span class="sxs-lookup"><span data-stu-id="cfa18-2141">New-AzPrivateLinkServiceIpConfig</span></span>
        - <span data-ttu-id="cfa18-2142">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="cfa18-2142">Set-AzPrivateEndpointConnection</span></span>
* <span data-ttu-id="cfa18-2143">Добавляет PrivateEndpoint.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2143">Add PrivateEndpoint</span></span>
    - <span data-ttu-id="cfa18-2144">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="cfa18-2144">New cmdlets</span></span>
        - <span data-ttu-id="cfa18-2145">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="cfa18-2145">Get-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="cfa18-2146">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="cfa18-2146">New-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="cfa18-2147">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="cfa18-2147">Remove-AzPrivateEndpoint</span></span>
        - <span data-ttu-id="cfa18-2148">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="cfa18-2148">New-AzPrivateLinkServiceConnection</span></span>
* <span data-ttu-id="cfa18-2149">Обновлены следующие команды для функции: флаг UseLocalAzureIpAddress для VPN-подключения.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2149">Updated below commands for feature: UseLocalAzureIpAddress flag on VpnConnection</span></span>
    - <span data-ttu-id="cfa18-2150">Обновлен командлет New-AzVpnConnection. Добавлен необязательный параметр -UseLocalAzureIpAddress для указания того, что локальный IP-адрес Azure следует использовать в качестве исходного адреса при инициации подключения.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2150">Updated New-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
    - <span data-ttu-id="cfa18-2151">Обновлен командлет Set-AzVpnConnection. Добавлен необязательный параметр -UseLocalAzureIpAddress для указания того, что локальный IP-адрес Azure следует использовать в качестве исходного адреса при инициации подключения.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2151">Updated Set-AzVpnConnection: Added optional parameter -UseLocalAzureIpAddress to indicate that local azure ip address should be used as source address while initiating connection.</span></span>
* <span data-ttu-id="cfa18-2152">В пиринг ExpressRoute добавлено поле только для чтения PeeredConnections.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2152">Added readonly field PeeredConnections in ExpressRoute peering.</span></span>
* <span data-ttu-id="cfa18-2153">В ExpressRoute добавлено поле только для чтения GlobalReachEnabled.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2153">Added readonly field GlobalReachEnabled in ExpressRoute.</span></span>
* <span data-ttu-id="cfa18-2154">Добавлен атрибут в рамках критического изменения, отменяющего статус устаревшего поля AllowGlobalReach в модели ExpressRouteCircuit.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2154">Added breaking change attribute to call out deprecation of AllowGlobalReach field in ExpressRouteCircuit model</span></span>
* <span data-ttu-id="cfa18-2155">Исправлена проблема, связанная с ошибкой 8756, при использовании TargetListenerID с командлетами AzApplicationGatewayRedirectConfiguration.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2155">Fixed Issue 8756 Error using TargetListenerID with AzApplicationGatewayRedirectConfiguration cmdlets</span></span>
* <span data-ttu-id="cfa18-2156">Исправлена ошибка в New-AzApplicationGatewayPathRuleConfig, не позволявшая задавать набор правил повторного создания.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2156">Fixed bug in New-AzApplicationGatewayPathRuleConfig that prevented the rewrite ruleset from being set.</span></span>
* <span data-ttu-id="cfa18-2157">Исправлено отображение VirtualNetworkTaps в NetworkInterfaceIpConfiguration.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2157">Fixed displaying of VirtualNetworkTaps in NetworkInterfaceIpConfiguration</span></span>
* <span data-ttu-id="cfa18-2158">Исправлены командлеты Cortex Get для отображения всех частей.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2158">Fixed Cortex Get cmdlets for list all part</span></span>
* <span data-ttu-id="cfa18-2159">Исправлено создание ссылок VirtualHub для ExpressRouteGateways и VpnGateway.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2159">Fixed VirtualHub reference creation for ExpressRouteGateways, VpnGateway</span></span>
* <span data-ttu-id="cfa18-2160">В AzureFirewall и NatGateway добавлена поддержка Зон доступности.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2160">Added support for Availability Zones in AzureFirewall and NatGateway</span></span>
* <span data-ttu-id="cfa18-2161">Добавлен командлет Get-AzNetworkServiceTag.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2161">Added cmdlet Get-AzNetworkServiceTag</span></span>
* <span data-ttu-id="cfa18-2162">Добавлена поддержка нескольких общедоступных IP-адресов для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2162">Add support for multiple public IP addresses for Azure Firewall</span></span>
    - <span data-ttu-id="cfa18-2163">Обновлен командлет New-AzFirewall:</span><span class="sxs-lookup"><span data-stu-id="cfa18-2163">Updated New-AzFirewall cmdlet:</span></span>
        - <span data-ttu-id="cfa18-2164">Добавлен параметр -PublicIpAddress, который принимает один или несколько объектов общедоступных IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2164">Added parameter -PublicIpAddress which accepts one or more Public IP Address objects</span></span>
        - <span data-ttu-id="cfa18-2165">Добавлен параметр -VirtualNetwork, который принимает объект виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2165">Added parameter -VirtualNetwork which accepts a Virtual Network object</span></span>
        - <span data-ttu-id="cfa18-2166">Добавлены методы AddPublicIpAddress и RemovePublicIpAddress для объекта брандмауэра. Они принимают объект общедоступного IP-адреса в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2166">Added methods AddPublicIpAddress and RemovePublicIpAddress on firewall object - these accept a Public IP Address object as input</span></span>
        - <span data-ttu-id="cfa18-2167">Не рекомендуется использовать параметры -PublicIpName и -VirtualNetworkName.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2167">Deprecated parameters -PublicIpName and -VirtualNetworkName</span></span>
* <span data-ttu-id="cfa18-2168">Обновлены следующие команды для функции: В параметрах проверки подлинности AAD VPN-клиента задан ресурс шлюза виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2168">Updated below commands for feature: Set VpnClient AAD authentication options to Virtual network gateway resource.</span></span>
    - <span data-ttu-id="cfa18-2169">Обновлен командлет New-AzVirtualNetworkGateway: Добавлены необязательные параметры AadTenantUri, AadAudienceId, AadIssuerUri для возможности задавать в шлюзе параметры проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2169">Updated New-AzVirtualNetworkGateway: Added optional parameters AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="cfa18-2170">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлены необязательные параметры AadTenantUri, AadAudienceId, AadIssuerUri для возможности задавать в шлюзе параметры проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2170">Updated Set-AzVirtualNetworkGateway: Added optional parameter AadTenantUri,AadAudienceId,AadIssuerUri to set VpnClient AAD authentication options on Gateway.</span></span>
    - <span data-ttu-id="cfa18-2171">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлен необязательный параметр-переключатель RemoveAadAuthentication для удаления в шлюзе параметров проверки подлинности AAD VPN-клиента.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2171">Updated Set-AzVirtualNetworkGateway: Added optional switch parameter RemoveAadAuthentication to remove VpnClient AAD authentication options from Gateway.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="cfa18-2172">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cfa18-2172">Az.OperationalInsights</span></span>
* <span data-ttu-id="cfa18-2173">Добавлена поддержка SKU **pergb2018** в команде New-AzureRmOperationalInsightsWorkspace.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2173">Enable **pergb2018** pricing tier in 'New-AzureRmOperationalInsightsWorkspace' command</span></span>

#### <a name="azresources"></a><span data-ttu-id="cfa18-2174">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cfa18-2174">Az.Resources</span></span>
* <span data-ttu-id="cfa18-2175">Поддержка дополнительных вариантов экспорта шаблона.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2175">Support for additional Template Export options</span></span>
    - <span data-ttu-id="cfa18-2176">В Export-AzResourceGroup добавлен параметр -SkipResourceNameParameterization.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2176">Add '-SkipResourceNameParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="cfa18-2177">В Export-AzResourceGroup добавлен параметр -SkipAllParameterization.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2177">Add '-SkipAllParameterization' parameter to Export-AzResourceGroup</span></span>
    - <span data-ttu-id="cfa18-2178">В Export-AzResourceGroup добавлен параметр -Resource для фильтрации экспортированных ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2178">Add '-Resource' parameter to Export-AzResourceGroup for exported resource filtering</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="cfa18-2179">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cfa18-2179">Az.ServiceFabric</span></span>
* <span data-ttu-id="cfa18-2180">Исправлена ошибка, связанная с получением иногда неправильных отпечатков при добавлении сертификата ByExistingKeyVault.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2180">Fix add certificate ByExistingKeyVault getting the wrong thumbprint in some cases</span></span>

#### <a name="azsql"></a><span data-ttu-id="cfa18-2181">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cfa18-2181">Az.Sql</span></span>
* <span data-ttu-id="cfa18-2182">Исправлен суффикс конечной точки хранилища службы "Расширенная защита от угроз Azure".</span><span class="sxs-lookup"><span data-stu-id="cfa18-2182">Fix Advanced Threat Protection storage endpoint suffix</span></span>
* <span data-ttu-id="cfa18-2183">Исправлена ошибка, связанная с возможностью пакета "Расширенная защита данных" переопределять политику службы "Расширенная защита от угроз".</span><span class="sxs-lookup"><span data-stu-id="cfa18-2183">Fix Advanced Data Security enable overrides Advanced Threat Protection policy</span></span>
* <span data-ttu-id="cfa18-2184">Новые командлеты для Management.Sql позволяют клиентам добавлять ключи TDE и задавать средство защиты TDE для управляемых экземпляров.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2184">New Cmdlets for Management.Sql to allow customers to add TDE keys and set TDE protector for managed instances</span></span>
   - <span data-ttu-id="cfa18-2185">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="cfa18-2185">Add-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="cfa18-2186">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="cfa18-2186">Get-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="cfa18-2187">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="cfa18-2187">Remove-AzSqlInstanceKeyVaultKey</span></span>
   - <span data-ttu-id="cfa18-2188">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="cfa18-2188">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>
   - <span data-ttu-id="cfa18-2189">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="cfa18-2189">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cfa18-2190">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cfa18-2190">Az.Storage</span></span>
* <span data-ttu-id="cfa18-2191">Поддержка класса Kind в FileStorage и значения Premium_ZRS в SkuName при создании учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2191">Support Kind FileStorage and SkuName Premium_ZRS when create Storage account</span></span>
    - <span data-ttu-id="cfa18-2192">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cfa18-2192">New-AzStorageAccount</span></span>
* <span data-ttu-id="cfa18-2193">Уточнено описание командлета неизменности BLOB-объектов.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2193">Clarified description of blob immutability cmdlet</span></span>
    -  <span data-ttu-id="cfa18-2194">Remove-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="cfa18-2194">Remove-AzRmStorageContainerImmutabilityPolicy</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cfa18-2195">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cfa18-2195">Az.Websites</span></span>
* <span data-ttu-id="cfa18-2196">Оптимизирует Get-AzWebAppCertificate для фильтрации по группе ресурсов на сервере, а не в клиенте.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2196">Optimizes Get-AzWebAppCertificate to filter by resource group on the server instead of the client</span></span>
* <span data-ttu-id="cfa18-2197">Добавляет параметр-переключатель - UseDisasterRecovery в Get AzWebAppSnapshot.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2197">Adds -UseDisasterRecovery switch parameter to Get-AzWebAppSnapshot</span></span>

## <a name="220---june-2019"></a><span data-ttu-id="cfa18-2198">2.2.0 — июнь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2198">2.2.0 - June 2019</span></span>
#### <a name="azcdn"></a><span data-ttu-id="cfa18-2199">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="cfa18-2199">Az.Cdn</span></span>
* <span data-ttu-id="cfa18-2200">Обновлены командлеты для поддержки функции rulesEngine на основе API версии 2019-04-15.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2200">Updated cmdlets to support rulesEngine feature based on API version 2019-04-15.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cfa18-2201">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cfa18-2201">Az.Compute</span></span>
* <span data-ttu-id="cfa18-2202">Добавлен параметр `NoWait`, который запускает операцию и немедленно возвращает значение еще до завершения операции.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2202">Added `NoWait` parameter that starts the operation and returns immediately, before the operation is completed.</span></span>
    - <span data-ttu-id="cfa18-2203">Обновлены командлеты:   Export-AzLogAnalyticRequestRateByInterval; Export-AzLogAnalyticThrottledRequest; Remove-AzVM; Remove-AzVMAccessExtension; Remove-AzVMAEMExtension; Remove-AzVMChefExtension; Remove-AzVMCustomScriptExtension; Remove-AzVMDiagnosticsExtension; Remove-AzVMDiskEncryptionExtension; Remove-AzVMDscExtension; Remove-AzVMSqlServerExtension; Restart-AzVM; Set-AzVM; Set-AzVMAccessExtension; Set-AzVMADDomainExtension; Set-AzVMAEMExtension; Set-AzVMBginfoExtension; Set-AzVMChefExtension; Set-AzVMCustomScriptExtension; Set-AzVMDiagnosticsExtension; Set-AzVMDscExtension; Set-AzVMExtension; Start-AzVM; Stop-AzVM; Update-AzVM.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2203">Updated cmdlets:   Export-AzLogAnalyticRequestRateByInterval   Export-AzLogAnalyticThrottledRequest   Remove-AzVM   Remove-AzVMAccessExtension   Remove-AzVMAEMExtension   Remove-AzVMChefExtension   Remove-AzVMCustomScriptExtension   Remove-AzVMDiagnosticsExtension   Remove-AzVMDiskEncryptionExtension   Remove-AzVMDscExtension   Remove-AzVMSqlServerExtension   Restart-AzVM   Set-AzVM   Set-AzVMAccessExtension   Set-AzVMADDomainExtension   Set-AzVMAEMExtension   Set-AzVMBginfoExtension   Set-AzVMChefExtension   Set-AzVMCustomScriptExtension   Set-AzVMDiagnosticsExtension   Set-AzVMDscExtension   Set-AzVMExtension   Start-AzVM   Stop-AzVM   Update-AzVM</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="cfa18-2204">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="cfa18-2204">Az.EventHub</span></span>
* <span data-ttu-id="cfa18-2205">Исправлена ошибка № 9231. Командлет Get-AzEventHubNamespace не возвращал теги.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2205">Fix for #9231 - Get-AzEventHubNamespace does not return tags</span></span>
* <span data-ttu-id="cfa18-2206">Исправлена ошибка № 9230. Командлет Get-AzEventHubNamespace возвращал значение ResourceGroup вместо ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2206">Fix for #9230 - Get-AzEventHubNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cfa18-2207">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cfa18-2207">Az.Network</span></span>
* <span data-ttu-id="cfa18-2208">Обновлены параметры ResourceId и InputObject для ресурса Шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2208">Update ResourceId and InputObject for Nat Gateway</span></span>
    - <span data-ttu-id="cfa18-2209">Добавлены псевдонимы для параметров ResourceId и InputObject.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2209">Add alias for ResourceId and InputObject</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="cfa18-2210">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="cfa18-2210">Az.PolicyInsights</span></span>
* <span data-ttu-id="cfa18-2211">Исправлена проблема с пустой ссылкой в командлете Get-AzPolicyEvent.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2211">Fix Null reference issue in Get-AzPolicyEvent</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cfa18-2212">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cfa18-2212">Az.RecoveryServices</span></span>
* <span data-ttu-id="cfa18-2213">Минимальный срок хранения политики IaaSVM изменился с 1 до 7 дней.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2213">IaaSVM policy minimum retention in days changed to 7 from 1</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="cfa18-2214">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="cfa18-2214">Az.ServiceBus</span></span>
* <span data-ttu-id="cfa18-2215">Исправлена ошибка № 9182. Командлет Get-AzServiceBusNamespace возвращал ResourceGroup вместо ResourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2215">Fix for issue #9182 - Get-AzServiceBusNamespace returns ResourceGroup instead of ResourceGroupName</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="cfa18-2216">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cfa18-2216">Az.ServiceFabric</span></span>
* <span data-ttu-id="cfa18-2217">Исправлена опечатка в сообщении об ошибке для командлета Update-AzServiceFabricReliability.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2217">Fix typo in error message for 'Update-AzServiceFabricReliability'</span></span>
* <span data-ttu-id="cfa18-2218">Добавлен отсутствующий символ в командных строках Service Fabric.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2218">Fix missing character in Service Fabric cmdlines</span></span>

#### <a name="azsql"></a><span data-ttu-id="cfa18-2219">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cfa18-2219">Az.Sql</span></span>
* <span data-ttu-id="cfa18-2220">Для командлета New-AzureSqlInstance добавлен параметр DnsZonePartner, обеспечивающий поддержку AutoDr для Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2220">Add DnsZonePartner Parameter for New-AzureSqlInstance cmdlet to support AutoDr for Managed Instance.</span></span>
* <span data-ttu-id="cfa18-2221">Командлет Get-AzSqlDatabaseSecureConnectionPolicy объявлен неподдерживаемым.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2221">Deprecating Get-AzSqlDatabaseSecureConnectionPolicy cmdlet</span></span>
* <span data-ttu-id="cfa18-2222">Командлеты обнаружения угроз переименованы в командлеты Расширенной защиты от угроз.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2222">Rename Threat Detection cmdlets to Advanced Threat Protection</span></span>
* <span data-ttu-id="cfa18-2223">Параметры -StorageSizeInGB и -LicenseType командлета New-AzSqlInstance теперь необязательны.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2223">New-AzSqlInstance -StorageSizeInGB and -LicenseType parameters are now optional.</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cfa18-2224">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cfa18-2224">Az.Websites</span></span>
* <span data-ttu-id="cfa18-2225">Исправлены проблемы, когда удалялись теги при использовании Set-AzWebApp и Set-AzWebAppSlot со свойством -WebApp.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2225">fixes the issue where using  Set-AzWebApp and Set-AzWebAppSlot with -WebApp property was removing the tags</span></span>

## <a name="210---may-2019"></a><span data-ttu-id="cfa18-2226">2.1.0 — май 2019 г.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2226">2.1.0 - May 2019</span></span>
#### <a name="azapimanagement"></a><span data-ttu-id="cfa18-2227">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cfa18-2227">Az.ApiManagement</span></span>
* <span data-ttu-id="cfa18-2228">Созданы командлеты для управления диагностикой в глобальной области и в области API.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2228">Created new Cmdlets for managing diagnostics at the global and API Scope</span></span>
    - <span data-ttu-id="cfa18-2229">**Get-AzApiManagementDiagnostic**  — получение диагностики, заданной глобально или на уровне области API.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2229">**Get-AzApiManagementDiagnostic** - Get the diagnostics configured a global or api Scope</span></span>
    - <span data-ttu-id="cfa18-2230">**New-AzApiManagementDiagnostic**  — создание диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2230">**New-AzApiManagementDiagnostic** - Create new diagnostics at the global scope or api Scope</span></span>
    - <span data-ttu-id="cfa18-2231">**New-AzApiManagementHttpMessageDiagnostic**  — создание параметра диагностики, для которого регистрируются заголовки и размер байтов тела.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2231">**New-AzApiManagementHttpMessageDiagnostic** - Create diagnostic setting for which Headers to log and the size of Body Bytes</span></span>
    - <span data-ttu-id="cfa18-2232">**New-AzApiManagementPipelineDiagnosticSetting**  — создание параметров диагностики для сообщений HTTP, поступающих в шлюз или исходящих из него.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2232">**New-AzApiManagementPipelineDiagnosticSetting** - Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>
    - <span data-ttu-id="cfa18-2233">**New-AzApiManagementSamplingSetting**  — создание параметра выборки для запросов и ответов касательно диагностики.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2233">**New-AzApiManagementSamplingSetting** - Create Sampling Setting  for the requests/response for a diagnostic</span></span>
    - <span data-ttu-id="cfa18-2234">**Remove-AzApiManagementDiagnostic**  — удаление объекта диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2234">**Remove-AzApiManagementDiagnostic** - Remove a diagnostic entity at global or api scope</span></span>
    - <span data-ttu-id="cfa18-2235">**Set-AzApiManagementDiagnostic**  — обновление объекта диагностики в глобальной области или в области API.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2235">**Set-AzApiManagementDiagnostic** - Update a diagnostic Entity at global or api scope</span></span>
* <span data-ttu-id="cfa18-2236">Созданы командлеты для управления кэшем в службе ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2236">Created new Cmdlets for managing Cache in ApiManagement service</span></span>
    - <span data-ttu-id="cfa18-2237">**Get-AzApiManagementCache**  — получение сведений о кэше, указанном идентификатором, или обо всех кэшах.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2237">**Get-AzApiManagementCache** - Get the details of the Cache specified by identifier or all caches</span></span>
    - <span data-ttu-id="cfa18-2238">**New-AzApiManagementCache**  — создание кэша по умолчанию или кэша в определенном регионе Azure.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2238">**New-AzApiManagementCache** - Create a new 'default' Cache or Cache in a particular azure 'region'</span></span>
    - <span data-ttu-id="cfa18-2239">**Remove-AzApiManagementCache**  — удаление кэша.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2239">**Remove-AzApiManagementCache** - Remove a cache</span></span>
    - <span data-ttu-id="cfa18-2240">**Update-AzApiManagementCache**  — обновление кэша.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2240">**Update-AzApiManagementCache** - Update a cache</span></span>
* <span data-ttu-id="cfa18-2241">Созданы командлеты для управления схемой API.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2241">Created new Cmdlets for managing API Schema</span></span>
    - <span data-ttu-id="cfa18-2242">**New-AzApiManagementSchema**  — создание схемы для API.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2242">**New-AzApiManagementSchema** - Create a new Schema for an API</span></span>
    - <span data-ttu-id="cfa18-2243">**Get-AzApiManagementSchema**  — получение схем, настроенных в API.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2243">**Get-AzApiManagementSchema** - Get the schemas configured in the API</span></span>
    - <span data-ttu-id="cfa18-2244">**Remove-AzApiManagementSchema**  — удаление схемы, настроенной в API.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2244">**Remove-AzApiManagementSchema** - Remove the schema configured in the API</span></span>
    - <span data-ttu-id="cfa18-2245">**Set-AzApiManagementSchema**  — обновление схемы, настроенной в API.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2245">**Set-AzApiManagementSchema** - Update the schema configured in the API</span></span>
* <span data-ttu-id="cfa18-2246">Создан командлет для создания токена пользователя.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2246">Created new Cmdlet for generating a User Token.</span></span>
    - <span data-ttu-id="cfa18-2247">**New-AzApiManagementUserToken**  — создание токена пользователя, по умолчанию действительного в течение 8 часов. С помощью этого командлета можно создавать токен для пользователя GIT.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2247">**New-AzApiManagementUserToken** - Generate a new User Token valid for 8 hours by default.Token for the 'GIT' user can be generated using this cmdlet./</span></span>
* <span data-ttu-id="cfa18-2248">Создан командлет для получения состояния сети.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2248">Created a new cmdlet to retrieving the Network Status</span></span>
    - <span data-ttu-id="cfa18-2249">**Get-AzApiManagementNetworkStatus**  — получение состояния подключения сети ресурсов, от которых зависит служба "Управление API".</span><span class="sxs-lookup"><span data-stu-id="cfa18-2249">**Get-AzApiManagementNetworkStatus** - Get the Network status connectivity of resources on which API Management service depends on.</span></span> <span data-ttu-id="cfa18-2250">Это полезно при развертывании службы ApiManagement в виртуальной сети и проверке того, не нарушена ли какая-либо из зависимостей.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2250">This is useful when deploying ApiManagement service into a Virtual Network and validing whether any of the dependencies are broken.</span></span>
* <span data-ttu-id="cfa18-2251">Обновлен командлет **New-AzApiManagement** для управления службой ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2251">Updated cmdlet **New-AzApiManagement** to manage ApiManagement service</span></span>
    - <span data-ttu-id="cfa18-2252">Добавлена поддержка нового SKU Consumption.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2252">Added support for the new 'Consumption' SKU</span></span>
    - <span data-ttu-id="cfa18-2253">Добавлена поддержка для включения флага EnableClientCertificate в SKU Consumption.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2253">Added support to turn the 'EnableClientCertificate' flag on for 'Consumption' SKU</span></span>
    - <span data-ttu-id="cfa18-2254">Новый командлет **New-AzApiManagementSslSetting** позволяет настраивать параметр TLS/SSL для сервера (Backend) и внешнего интерфейса (Frontend).</span><span class="sxs-lookup"><span data-stu-id="cfa18-2254">The new cmdlet **New-AzApiManagementSslSetting** allows configuring 'TLS/SSL' setting on the 'Backend' and 'Frontend'.</span></span> <span data-ttu-id="cfa18-2255">Его также можно использовать для настройки Ciphers как 3DES, в ServerProtocols как Http2 для внешнего интерфейса (Frontend) службы ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2255">This can also be used to configure 'Ciphers' like '3DES' and 'ServerProtocols' like 'Http2' on the 'Frontend' of an ApiManagement service.</span></span>
    - <span data-ttu-id="cfa18-2256">Добавлена поддержка настройки имени узла DeveloperPortal в службе ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2256">Added support for configuring the 'DeveloperPortal' hostname on ApiManagement service.</span></span>
* <span data-ttu-id="cfa18-2257">Обновлен командлет **Get-AzApiManagementSsoToken** для извлечения объекта PsApiManagement в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2257">Updated cmdlets **Get-AzApiManagementSsoToken** to take 'PsApiManagement' object as input</span></span>
* <span data-ttu-id="cfa18-2258">Обновлен командлет для отображения встроенных сообщений об ошибках.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2258">Updated the cmdlet to display Error Messages inline</span></span>
     > <span data-ttu-id="cfa18-2259">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Код ошибки: ValidationError. Сообщение об ошибке: "Некоторые поля содержат неправильные значения". Сведения об ошибке: [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span><span class="sxs-lookup"><span data-stu-id="cfa18-2259">PS D:\github\azure-powershell> Set-AzApiManagementPolicy -Context  -PolicyFilePath C:\wrongpolicy.xml -ApiId httpbin Set-AzApiManagementPolicy : Error Code: ValidationError Error Message: One or more fields contain incorrect values: Error Details:    [Code=ValidationError, Message=Error in element 'log-to-eventhub' on line 3, column 10: Logger not found, Target=log-to-eventhub]</span></span>
* <span data-ttu-id="cfa18-2260">Обновлен командлет **Export-AzApiManagementApi** для экспортирования программных интерфейсов в формате OpenApi 3.0.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2260">Updated cmdlet **Export-AzApiManagementApi** to export APIs in 'OpenApi 3.0' format</span></span>
* <span data-ttu-id="cfa18-2261">Обновлен командлет **Import-AzApiManagementApi** :</span><span class="sxs-lookup"><span data-stu-id="cfa18-2261">Updated cmdlet **Import-AzApiManagementApi**</span></span>
    - <span data-ttu-id="cfa18-2262">Для импортирования API из спецификации документа OpenApi 3.0.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2262">To import Api from 'OpenApi 3.0' document specification</span></span>
    - <span data-ttu-id="cfa18-2263">Для переопределения свойства PsApiManagementSchema, указанного в любом документе (Swagger, Wadl, Wsdl, OpenApi).</span><span class="sxs-lookup"><span data-stu-id="cfa18-2263">To override the 'PsApiManagementSchema' property specified in any ('Swagger', 'Wadl', 'Wsdl', 'OpenApi') document.</span></span>
    - <span data-ttu-id="cfa18-2264">Для переопределения свойства ServiceUrl, указанного в любом документе.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2264">To override the 'ServiceUrl' property specified in any document.</span></span>
* <span data-ttu-id="cfa18-2265">Обновлен командлет **Get-AzApiManagementPolicy** для возврата политики в формате, экранированном не для XML, с использованием rawxml.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2265">Updated cmdlet **Get-AzApiManagementPolicy** to return policy in Non-Xml escaped 'format' using 'rawxml'</span></span>
* <span data-ttu-id="cfa18-2266">Обновлен командлет **Set-AzApiManagementPolicy**. Он принимает политику в формате, экранированном не для XML, с использованием rawxml и в формате, экранированном для XML, с использованием XML.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2266">Updated cmdlet **Set-AzApiManagementPolicy** to accept policy in Non-Xml escaped 'format' using 'rawxml' and Xml escaped using 'xml'</span></span>
* <span data-ttu-id="cfa18-2267">Обновлен командлет **New-AzApiManagementApi** :</span><span class="sxs-lookup"><span data-stu-id="cfa18-2267">Updated cmdlet **New-AzApiManagementApi**</span></span>
    - <span data-ttu-id="cfa18-2268">Для настройки API с помощью сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2268">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="cfa18-2269">Для создания API в ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2269">To create an API in an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="cfa18-2270">Для клонирования API с использованием значений SourceApiId и SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2270">To clone an API using 'SourceApiId' and 'SourceApiRevision'.</span></span>
    - <span data-ttu-id="cfa18-2271">Возможность настройки параметра SubscriptionRequired в области API.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2271">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="cfa18-2272">Обновлен командлет **Set-AzApiManagementApi** :</span><span class="sxs-lookup"><span data-stu-id="cfa18-2272">Updated cmdlet **Set-AzApiManagementApi**</span></span>
    - <span data-ttu-id="cfa18-2273">Для настройки API с помощью сервера авторизации OpenId.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2273">To configure API with 'OpenId' authorization server.</span></span>
    - <span data-ttu-id="cfa18-2274">Для обновления API в ApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2274">To updated an API into an 'ApiVersionSet'</span></span>
    - <span data-ttu-id="cfa18-2275">Возможность настройки параметра SubscriptionRequired в области API.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2275">Ability to configure 'SubscriptionRequired' at the Api scope.</span></span>
* <span data-ttu-id="cfa18-2276">Обновлен командлет **New-AzApiManagementRevision** :</span><span class="sxs-lookup"><span data-stu-id="cfa18-2276">Updated cmdlet **New-AzApiManagementRevision**</span></span>
    - <span data-ttu-id="cfa18-2277">Для клонирования (копирования тегов, продуктов, операций и политик) существующей редакции с использованием SourceApiRevision.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2277">To clone (copy tags, products, operations and policies) an existing revision using 'SourceApiRevision'.</span></span> <span data-ttu-id="cfa18-2278">Новая редакция предполагает родительский идентификатор ApiId.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2278">The new Revision assumes the 'ApiId' of the parent.</span></span>
    - <span data-ttu-id="cfa18-2279">Для предоставления ApiRevisionDescription.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2279">To provide an 'ApiRevisionDescription'</span></span>
    - <span data-ttu-id="cfa18-2280">Для переопределения значения ServiceUrl при клонировании API.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2280">To override the 'ServiceUrl' when cloning an API.</span></span>
* <span data-ttu-id="cfa18-2281">Обновлен командлет **New-AzApiManagementIdentityProvider** :</span><span class="sxs-lookup"><span data-stu-id="cfa18-2281">Updated cmdlet **New-AzApiManagementIdentityProvider**</span></span>
    - <span data-ttu-id="cfa18-2282">Для настройки AAD или AADB2C с Authority.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2282">To configure 'AAD' or 'AADB2C' with an 'Authority'</span></span>
    - <span data-ttu-id="cfa18-2283">Для установки политик SignupPolicy, SigninPolicy, ProfileEditingPolicy и PasswordResetPolicy.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2283">To setup 'SignupPolicy', 'SigninPolicy', 'ProfileEditingPolicy' and 'PasswordResetPolicy'</span></span>
* <span data-ttu-id="cfa18-2284">Обновлен командлет **New-AzApiManagementSubscription**.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2284">Updated cmdlet **New-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="cfa18-2285">Для учета новой модели SubscriptonModel с помощью Scope и UserId.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2285">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="cfa18-2286">Для учета прежней модели подписки с помощью ProductId и UserId.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2286">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="cfa18-2287">Добавлена поддержка для включения AllowTracing на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2287">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="cfa18-2288">Обновлен командлет **Set-AzApiManagementSubscription**.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2288">Updated cmdlet **Set-AzApiManagementSubscription**</span></span>
    - <span data-ttu-id="cfa18-2289">Для учета новой модели SubscriptonModel с помощью Scope и UserId.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2289">To account for the new SubscriptonModel using 'Scope' and 'UserId'</span></span>
    - <span data-ttu-id="cfa18-2290">Для учета прежней модели подписки с помощью ProductId и UserId.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2290">To account for the old subscription model using 'ProductId' and 'UserId'</span></span>
    - <span data-ttu-id="cfa18-2291">Добавлена поддержка для включения AllowTracing на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2291">Add support to enable 'AllowTracing' at the subscription level.</span></span>
* <span data-ttu-id="cfa18-2292">Следующие командлеты обновлены, чтобы принимать значение ResourceId в качестве входных данных.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2292">Updated following cmdlets to accept 'ResourceId' as input</span></span>
    - <span data-ttu-id="cfa18-2293">New-AzApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2293">'New-AzApiManagementContext'</span></span>
        > <span data-ttu-id="cfa18-2294">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span><span class="sxs-lookup"><span data-stu-id="cfa18-2294">New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso</span></span>
    - <span data-ttu-id="cfa18-2295">Get-AzApiManagementApiRelease.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2295">'Get-AzApiManagementApiRelease'</span></span>
        > <span data-ttu-id="cfa18-2296">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span><span class="sxs-lookup"><span data-stu-id="cfa18-2296">Get-AzApiManagementApiRelease -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/apis/echo-api/releases/releaseId</span></span>
    - <span data-ttu-id="cfa18-2297">Get-AzApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2297">'Get-AzApiManagementApiVersionSet'</span></span>
        > <span data-ttu-id="cfa18-2298">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span><span class="sxs-lookup"><span data-stu-id="cfa18-2298">Get-AzApiManagementApiVersionSet -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/constoso/apiversionsets/pathversionset</span></span>
    - <span data-ttu-id="cfa18-2299">Get-AzApiManagementAuthorizationServer.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2299">'Get-AzApiManagementAuthorizationServer'</span></span>
    - <span data-ttu-id="cfa18-2300">Get-AzApiManagementBackend.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2300">'Get-AzApiManagementBackend'</span></span>
        > <span data-ttu-id="cfa18-2301">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span><span class="sxs-lookup"><span data-stu-id="cfa18-2301">Get-AzApiManagementBackend -ResourceId /subscriptions/subid/resourceGroups/rgName/providers/Microsoft.ApiManagement/service/contoso/backends/servicefabric</span></span>
    - <span data-ttu-id="cfa18-2302">Get-AzApiManagementCertificate.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2302">'Get-AzApiManagementCertificate'</span></span>
    - <span data-ttu-id="cfa18-2303">Remove-AzApiManagementApiVersionSet.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2303">'Remove-AzApiManagementApiVersionSet'</span></span>
    - <span data-ttu-id="cfa18-2304">Remove-AzApiManagementSubscription.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2304">'Remove-AzApiManagementSubscription'</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cfa18-2305">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cfa18-2305">Az.Automation</span></span>
* <span data-ttu-id="cfa18-2306">Обновлен командлет Get-AzAutomationJobOutputRecord для обработки значений в формате JSON и в виде текстовой записи.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2306">Updated Get-AzAutomationJobOutputRecord to handle JSON and Text record values.</span></span>
    - <span data-ttu-id="cfa18-2307">исправлена проблема https://github.com/Azure/azure-powershell/issues/7977.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2307">Fix for issue https://github.com/Azure/azure-powershell/issues/7977</span></span>
    - <span data-ttu-id="cfa18-2308">исправлена проблема https://github.com/Azure/azure-powershell/issues/8600.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2308">Fix for issue https://github.com/Azure/azure-powershell/issues/8600</span></span>
* <span data-ttu-id="cfa18-2309">Поведение командлета Start-AzAutomationDscCompilationJob изменено так, чтобы сразу же запустить задание, а не ждать его завершения.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2309">Changed behavior for Start-AzAutomationDscCompilationJob to just start the job instead of waiting for its completion.</span></span>
    * <span data-ttu-id="cfa18-2310">исправлена проблема https://github.com/Azure/azure-powershell/issues/8347.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2310">Fix for issue https://github.com/Azure/azure-powershell/issues/8347</span></span>
* <span data-ttu-id="cfa18-2311">Исправлен командлет Get-AzAutomationDscNode, возвращающий все узлы при использовании -Name.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2311">Fix for Get-AzAutomationDscNode when using -Name returns all node.</span></span> <span data-ttu-id="cfa18-2312">Теперь он возвращает только соответствующий узел.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2312">Now it returns matching node only.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cfa18-2313">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cfa18-2313">Az.Compute</span></span>
* <span data-ttu-id="cfa18-2314">Добавлены параметры ProtectFromScaleIn и ProtectFromScaleSetAction для командлета Update-AzVmssVM.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2314">Add ProtectFromScaleIn and ProtectFromScaleSetAction parameters to Update-AzVmssVM cmdlet.</span></span>
* <span data-ttu-id="cfa18-2315">Командлет New-AzVM с простым набором параметров теперь по умолчанию использует доступное расположение, если регион "восточная часть США" не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2315">New-AzVM wimple parameter set now uses by default an available location if 'East US' is not supported</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cfa18-2316">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cfa18-2316">Az.DataLakeStore</span></span>
* <span data-ttu-id="cfa18-2317">Обновлен пакет SDK ADLS для использования httpclient. В инфраструктуру Azure интегрирована проверка плоскости данных.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2317">Update the ADLS sdk to use httpclient, integrate dataplane testing with azure framework</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cfa18-2318">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cfa18-2318">Az.Monitor</span></span>
* <span data-ttu-id="cfa18-2319">Исправлены неправильные имена параметров в справочных примерах.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2319">Fixed incorrect parameter names in help examples</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cfa18-2320">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cfa18-2320">Az.Network</span></span>
* <span data-ttu-id="cfa18-2321">Добавлен флаг DisableBgpRoutePropagation для выходных данных действующей таблицы маршрутов.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2321">Add DisableBgpRoutePropagation flag to Effective Route Table output</span></span>
    - <span data-ttu-id="cfa18-2322">Обновлен командлет:</span><span class="sxs-lookup"><span data-stu-id="cfa18-2322">Updated cmdlet:</span></span>
        - <span data-ttu-id="cfa18-2323">Get-AzEffectiveRouteTable.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2323">Get-AzEffectiveRouteTable</span></span>
* <span data-ttu-id="cfa18-2324">Исправлен двойной дефис в документации New-AzApplicationGatewayTrustedRootCertificate.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2324">Fix double dash in New-AzApplicationGatewayTrustedRootCertificate documentation</span></span>

#### <a name="azresources"></a><span data-ttu-id="cfa18-2325">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cfa18-2325">Az.Resources</span></span>
* <span data-ttu-id="cfa18-2326">Добавлен новый командлет Get-AzureRmDenyAssignment для получения запрещающих назначений.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2326">Add new cmdlet Get-AzureRmDenyAssignment for retrieving deny assignments</span></span>

#### <a name="azsql"></a><span data-ttu-id="cfa18-2327">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cfa18-2327">Az.Sql</span></span>
* <span data-ttu-id="cfa18-2328">Командлеты Расширенной защиты от угроз переименованы на командлеты Расширенной защиты данных, и оценка уязвимости включена по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2328">Rename Advanced Threat Protection cmdlets to Advanced Data Security and enable Vulnerability Assessment by default</span></span>

## <a name="200---may-2019"></a><span data-ttu-id="cfa18-2329">2.0.0 — май 2019 г.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2329">2.0.0 - May 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cfa18-2330">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cfa18-2330">Az.Accounts</span></span>
* <span data-ttu-id="cfa18-2331">Обновлена библиотека аутентификации для устранения проблем с ADFS при использовании аутентификации на основе имени пользователя и пароля.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2331">Update Authentication Library to fix ADFS issues with username/password auth</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cfa18-2332">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cfa18-2332">Az.CognitiveServices</span></span>
* <span data-ttu-id="cfa18-2333">Отображается только заявление об отказе Bing для служб Поиска Bing.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2333">Only display Bing disclaimer for Bing Search Services.</span></span>
* <span data-ttu-id="cfa18-2334">Исправлена проблема с созданием учетной записи.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2334">Improve error when create account failed.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cfa18-2335">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cfa18-2335">Az.Compute</span></span>
* <span data-ttu-id="cfa18-2336">Функция группы размещения близкого взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2336">Proximity placement group feature.</span></span>
    - <span data-ttu-id="cfa18-2337">Добавлены следующие новые командлеты:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span><span class="sxs-lookup"><span data-stu-id="cfa18-2337">The following new cmdlets are added:   New-AzProximityPlacementGroup   Get-AzProximityPlacementGroup   Remove-AzProximityPlacementGroup</span></span>
    - <span data-ttu-id="cfa18-2338">Новый параметр ProximityPlacementGroupId будет добавлен в следующие командлеты:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="cfa18-2338">The new parameter, ProximityPlacementGroupId, is added to the following cmdlets:   New-AzAvailabilitySet   New-AzVMConfig   New-AzVmssConfig</span></span>
* <span data-ttu-id="cfa18-2339">В командлет New-AzGalleryImageVersion добавлен параметр StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2339">StorageAccountType parameter is added to New-AzGalleryImageVersion.</span></span>
* <span data-ttu-id="cfa18-2340">TargetRegion в командлете New-AzGalleryImageVersion может содержать StorageAccountType.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2340">TargetRegion of New-AzGalleryImageVersion can contain StorageAccountType.</span></span>
* <span data-ttu-id="cfa18-2341">Параметр-переключатель SkipShutdown добавлен в командлеты Stop-AzVM и Stop-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2341">SkipShutdown switch parameter is added to Stop-AzVM and Stop-AzVmss</span></span>
* <span data-ttu-id="cfa18-2342">Критические изменения</span><span class="sxs-lookup"><span data-stu-id="cfa18-2342">Breaking changes</span></span>
    - <span data-ttu-id="cfa18-2343">Командлет SET-AzVMBootDiagnostics изменен на Set-AzVMBootDiagnostic.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2343">Set-AzVMBootDiagnostics is changed to Set-AzVMBootDiagnostic.</span></span>
    - <span data-ttu-id="cfa18-2344">Командлет Export-AzLogAnalyticThrottledRequests изменен на Export-AzLogAnalyticThrottledRequests.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2344">Export-AzLogAnalyticThrottledRequests is changed to Export-AzLogAnalyticThrottledRequests.</span></span>

#### <a name="azdeploymentmanager"></a><span data-ttu-id="cfa18-2345">Az.DeploymentManager</span><span class="sxs-lookup"><span data-stu-id="cfa18-2345">Az.DeploymentManager</span></span>
* <span data-ttu-id="cfa18-2346">Первая общедоступная версия командлетов диспетчера развертывания Azure</span><span class="sxs-lookup"><span data-stu-id="cfa18-2346">First Generally Available release of Azure Deployment Manager cmdlets</span></span>

#### <a name="azdns"></a><span data-ttu-id="cfa18-2347">Az.Dns</span><span class="sxs-lookup"><span data-stu-id="cfa18-2347">Az.Dns</span></span>
* <span data-ttu-id="cfa18-2348">Автоматическое делегирование DNS-сервера</span><span class="sxs-lookup"><span data-stu-id="cfa18-2348">Automatic DNS NameServer Delegation</span></span>
    - <span data-ttu-id="cfa18-2349">Командлет для создания зоны DNS принимает имя родительской зоны в качестве дополнительного необязательного параметра.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2349">Create DNS zone cmdlet accepts parent zone name as additional optional parameter.</span></span>
    - <span data-ttu-id="cfa18-2350">Он добавляет записи NS в родительской зоне для созданной дочерней зоны.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2350">Adds NS records in the parent zone for newly created child zone.</span></span>

#### <a name="azfrontdoor"></a><span data-ttu-id="cfa18-2351">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="cfa18-2351">Az.FrontDoor</span></span>
* <span data-ttu-id="cfa18-2352">Первая общедоступная версия командлетов Azure FrontDoor.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2352">First Generally Available Release of Azure FrontDoor cmdlets</span></span>
* <span data-ttu-id="cfa18-2353">Переименованы командлеты WAF для включения Waf.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2353">Rename WAF cmdlets to include 'Waf'</span></span>
    - `Get-AzFrontDoorFireWallPolicy --> Get-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorCustomRuleObject --> New-AzFrontDoorWafCustomRuleObject`
    - `New-AzFrontDoorFireWallPolicy --> New-AzFrontDoorWafPolicy`
    - `New-AzFrontDoorManagedRuleObject --> New-AzFrontDoorWafManagedRuleObject`
    - `New-AzFrontDoorManagedRuleOverrideObject --> New-AzFrontDoorWafManagedRuleOverrideObject`
    - `New-AzFrontDoorMatchConditionObject --> New-AzFrontDoorWafMatchConditionObject`
    - `New-AzFrontDoorRuleGroupOverrideObject --> New-AzFrontDoorWafRuleGroupOverrideObject`
    - `Remove-AzFrontDoorFireWallPolicy --> Remove-AzFrontDoorWafPolicy`
    - `Update-AzFrontDoorFireWallPolicy --> Update-AzFrontDoorWafPolicy`
#### <a name="azhdinsight"></a><span data-ttu-id="cfa18-2354">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cfa18-2354">Az.HDInsight</span></span>
* <span data-ttu-id="cfa18-2355">Удалены два командлета:</span><span class="sxs-lookup"><span data-stu-id="cfa18-2355">Removed two cmdlets:</span></span>
    - <span data-ttu-id="cfa18-2356">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="cfa18-2356">Grant-AzHDInsightHttpServicesAccess</span></span>
    - <span data-ttu-id="cfa18-2357">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="cfa18-2357">Revoke-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="cfa18-2358">Добавлен новый командлет Set-AzHDInsightGatewayCredential для замены Grant-AzHDInsightHttpServicesAccess.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2358">Added a new cmdlet Set-AzHDInsightGatewayCredential to replace Grant-AzHDInsightHttpServicesAccess</span></span>
* <span data-ttu-id="cfa18-2359">Обновлен командлет Get-AzHDInsightJobOutput для различения ролей читателя и оператора HDInsight:</span><span class="sxs-lookup"><span data-stu-id="cfa18-2359">Update cmdlet Get-AzHDInsightJobOutput to distinguish reader role and hdinsight operator role:</span></span>
    - <span data-ttu-id="cfa18-2360">Пользователям с ролью читателя не нужно указывать параметр DefaultStorageAccountKey явным образом, иначе возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2360">Users with reader role need to specify 'DefaultStorageAccountKey' parameter explicitly, otherwise error occurs.</span></span>
    - <span data-ttu-id="cfa18-2361">На пользователей с ролью оператора HDInsight это не повлияет.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2361">Users with hdinsight operator role will not be affected.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cfa18-2362">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cfa18-2362">Az.Monitor</span></span>
* <span data-ttu-id="cfa18-2363">Новые командлеты для API SQR (запланированное правило запросов)</span><span class="sxs-lookup"><span data-stu-id="cfa18-2363">New cmdlets for SQR API (Scheduled Query Rule)</span></span>
    - <span data-ttu-id="cfa18-2364">New-AzScheduledQueryRuleAlertingAction</span><span class="sxs-lookup"><span data-stu-id="cfa18-2364">New-AzScheduledQueryRuleAlertingAction</span></span>
    - <span data-ttu-id="cfa18-2365">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="cfa18-2365">New-AzScheduledQueryRuleAznsActionGroup</span></span>
    - <span data-ttu-id="cfa18-2366">New-AzScheduledQueryRuleLogMetricTrigger</span><span class="sxs-lookup"><span data-stu-id="cfa18-2366">New-AzScheduledQueryRuleLogMetricTrigger</span></span>
    - <span data-ttu-id="cfa18-2367">New-AzScheduledQueryRuleSchedule</span><span class="sxs-lookup"><span data-stu-id="cfa18-2367">New-AzScheduledQueryRuleSchedule</span></span>
    - <span data-ttu-id="cfa18-2368">New-AzScheduledQueryRuleSource</span><span class="sxs-lookup"><span data-stu-id="cfa18-2368">New-AzScheduledQueryRuleSource</span></span>
    - <span data-ttu-id="cfa18-2369">New-AzScheduledQueryRuleTriggerCondition</span><span class="sxs-lookup"><span data-stu-id="cfa18-2369">New-AzScheduledQueryRuleTriggerCondition</span></span>
    - <span data-ttu-id="cfa18-2370">New-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="cfa18-2370">New-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="cfa18-2371">Get-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="cfa18-2371">Get-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="cfa18-2372">Set-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="cfa18-2372">Set-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="cfa18-2373">Update-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="cfa18-2373">Update-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="cfa18-2374">Remove-AzScheduledQueryRule</span><span class="sxs-lookup"><span data-stu-id="cfa18-2374">Remove-AzScheduledQueryRule</span></span>
    - <span data-ttu-id="cfa18-2375">См. подробнее об [API SQR](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules).</span><span class="sxs-lookup"><span data-stu-id="cfa18-2375">[More](https://docs.microsoft.com/rest/api/monitor/scheduledqueryrules) information about SQR API</span></span>
    - <span data-ttu-id="cfa18-2376">Обновлен файл Az.Monitor.md для включения командлетов для правила генерации оповещений на основе метрик GenV2(не классическая версия).</span><span class="sxs-lookup"><span data-stu-id="cfa18-2376">Updated Az.Monitor.md to include cmdlets for GenV2(non classic) metric-based alert rule</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cfa18-2377">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cfa18-2377">Az.Network</span></span>
* <span data-ttu-id="cfa18-2378">Добавлена поддержка для ресурса Шлюза NAT.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2378">Add support for Nat Gateway Resource</span></span>
    - <span data-ttu-id="cfa18-2379">Новые командлеты</span><span class="sxs-lookup"><span data-stu-id="cfa18-2379">New cmdlets</span></span>
        - <span data-ttu-id="cfa18-2380">New-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="cfa18-2380">New-AzNatGateway</span></span>
        - <span data-ttu-id="cfa18-2381">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="cfa18-2381">Get-AzNatGateway</span></span>
        - <span data-ttu-id="cfa18-2382">Set-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="cfa18-2382">Set-AzNatGateway</span></span>
        - <span data-ttu-id="cfa18-2383">Remove-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="cfa18-2383">Remove-AzNatGateway</span></span>
   - <span data-ttu-id="cfa18-2384">Обновлены командлеты</span><span class="sxs-lookup"><span data-stu-id="cfa18-2384">Updated cmdlets</span></span>
        - <span data-ttu-id="cfa18-2385">New-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="cfa18-2385">New-AzureVirtualNetworkSubnetConfigCommand</span></span>
        - <span data-ttu-id="cfa18-2386">Add-AzureVirtualNetworkSubnetConfigCommand</span><span class="sxs-lookup"><span data-stu-id="cfa18-2386">Add-AzureVirtualNetworkSubnetConfigCommand</span></span>
* <span data-ttu-id="cfa18-2387">Обновлены следующие команды для функции: Настройка и удаление пользовательских маршрутов через шлюз в Бруклине.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2387">Updated below commands for feature: Custom routes set/remove on Brooklyn Gateway.</span></span>
    - <span data-ttu-id="cfa18-2388">Обновлен командлет New-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2388">Updated New-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>
    - <span data-ttu-id="cfa18-2389">Обновлен командлет Set-AzVirtualNetworkGateway: Добавлен необязательный параметр -CustomRoute для назначения префиксов адресов в качестве пользовательских маршрутов, указываемых в шлюзе.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2389">Updated Set-AzVirtualNetworkGateway: Added optional parameter -CustomRoute to set the address prefixes as custom routes to set on Gateway.</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="cfa18-2390">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="cfa18-2390">Az.PolicyInsights</span></span>
* <span data-ttu-id="cfa18-2391">Добавлена поддержка сведений об оценке политики запросов.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2391">Support for querying policy evaluation details.</span></span>
    - <span data-ttu-id="cfa18-2392">Добавлен параметр -Expand в командлет Get-AzPolicyState.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2392">Add '-Expand' parameter to Get-AzPolicyState.</span></span> <span data-ttu-id="cfa18-2393">Добавлена поддержка -Expand PolicyEvaluationDetails.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2393">Support '-Expand PolicyEvaluationDetails'.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cfa18-2394">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cfa18-2394">Az.RecoveryServices</span></span>
* <span data-ttu-id="cfa18-2395">Добавлена поддержка перекрестной подписки на Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2395">Support for Cross subscription Azure to Azure site recovery.</span></span>
* <span data-ttu-id="cfa18-2396">Добавлена возможность отмечать предстоящие критически важные изменения для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2396">Marking upcoming breaking changes for Azure Site Recovery.</span></span>
* <span data-ttu-id="cfa18-2397">Исправлены план восстановления и план действий для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2397">Fix for Azure Site Recovery recovery plan end action plan.</span></span>
* <span data-ttu-id="cfa18-2398">Исправлено сетевое сопоставление обновления Azure Site Recovery (Azure — Azure).</span><span class="sxs-lookup"><span data-stu-id="cfa18-2398">Fix for Azure Site Recovery Update network mapping for Azure to Azure.</span></span>
* <span data-ttu-id="cfa18-2399">Исправлено направление защиты обновления Azure Site Recovery для управляемых дисков (Azure — Azure).</span><span class="sxs-lookup"><span data-stu-id="cfa18-2399">Fix for Azure Site Recovery update protection direction for Azure to Azure for managed disk.</span></span>
* <span data-ttu-id="cfa18-2400">Добавлены другие незначительные исправления.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2400">Other minor fixes.</span></span>

#### <a name="azrelay"></a><span data-ttu-id="cfa18-2401">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="cfa18-2401">Az.Relay</span></span>
* <span data-ttu-id="cfa18-2402">Исправлены опечатки в сообщениях для клиентов.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2402">Fix typos in customer-facing messages</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="cfa18-2403">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="cfa18-2403">Az.ServiceBus</span></span>
* <span data-ttu-id="cfa18-2404">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2404">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cfa18-2405">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cfa18-2405">Az.Storage</span></span>
* <span data-ttu-id="cfa18-2406">Выполнено обновление клиентской библиотеки хранилища до версии 10.0.1 (пространство имен всех объектов из этого пакета SDK изменено с Microsoft.WindowsAzure.Storage. *на Microsoft.Azure.Storage* ).</span><span class="sxs-lookup"><span data-stu-id="cfa18-2406">Upgrade to Storage Client Library 10.0.1 (the namespace of all objects from this SDK change from 'Microsoft.WindowsAzure.Storage. *' to 'Microsoft.Azure.Storage.* ')</span></span>
* <span data-ttu-id="cfa18-2407">Выполнено обновление до Microsoft.Azure.Management.Storage версии 11.0.0 для включения поддержки нового API версии 2019-04-01.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2407">Upgrade to Microsoft.Azure.Management.Storage 11.0.0, to support new API version 2019-04-01.</span></span>
* <span data-ttu-id="cfa18-2408">Значение свойства Kind по умолчанию в учетной записи хранения изменено со Storage на StorageV2.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2408">The default Storage account Kind in Create Storage account change from 'Storage' to 'StorageV2'</span></span>
    - <span data-ttu-id="cfa18-2409">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cfa18-2409">New-AzStorageAccount</span></span>
* <span data-ttu-id="cfa18-2410">Изменено значение Sku.Name в выходных данных командлета учетной записи хранения в соответствии со значением Sku.Name во входных данных путем добавления _ (например, StandardLRS изменено на Standard_LRS).</span><span class="sxs-lookup"><span data-stu-id="cfa18-2410">Change the Storage account cmdlet output Sku.Name to be aligned with input SkuName by add '-', like 'StandardLRS' change to 'Standard_LRS'</span></span>
    - <span data-ttu-id="cfa18-2411">New-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cfa18-2411">New-AzStorageAccount</span></span>
    - <span data-ttu-id="cfa18-2412">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cfa18-2412">Get-AzStorageAccount</span></span>
    - <span data-ttu-id="cfa18-2413">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cfa18-2413">Set-AzStorageAccount</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cfa18-2414">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cfa18-2414">Az.Websites</span></span>
* <span data-ttu-id="cfa18-2415">Свойство Kind теперь будет задаваться объектам PSSite, возвращаемым командлетом Get-AzWebApp.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2415">'Kind' property will now be set for PSSite objects returned by Get-AzWebApp</span></span>
* <span data-ttu-id="cfa18-2416">Get-AzWebApp\*Metrics и Get-AzAppServicePlanMetrics считаются нерекомендуемыми.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2416">Get-AzWebApp\*Metrics and Get-AzAppServicePlanMetrics marked deprecated</span></span>

## <a name="180---april-2019"></a><span data-ttu-id="cfa18-2417">1.8.0 — апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2417">1.8.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="cfa18-2418">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="cfa18-2418">Highlights since the last major release</span></span>
* <span data-ttu-id="cfa18-2419">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2419">General availability of `Az` module</span></span>
* <span data-ttu-id="cfa18-2420">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="cfa18-2420">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="cfa18-2421">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="cfa18-2421">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="cfa18-2422">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2422">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="cfa18-2423">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2423">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="cfa18-2424">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2424">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="cfa18-2425">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="cfa18-2425">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="cfa18-2426">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cfa18-2426">Az.Accounts</span></span>
* <span data-ttu-id="cfa18-2427">Обновлен командлет Uninstall-AzureRm для правильного удаления модулей в Mac.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2427">Update Uninstall-AzureRm to correctly delete modules in Mac</span></span>

#### <a name="azbatch"></a><span data-ttu-id="cfa18-2428">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="cfa18-2428">Az.Batch</span></span>
* <span data-ttu-id="cfa18-2429">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2429">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcdn"></a><span data-ttu-id="cfa18-2430">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="cfa18-2430">Az.Cdn</span></span>
* <span data-ttu-id="cfa18-2431">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2431">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cfa18-2432">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cfa18-2432">Az.CognitiveServices</span></span>
* <span data-ttu-id="cfa18-2433">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2433">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cfa18-2434">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cfa18-2434">Az.Compute</span></span>
* <span data-ttu-id="cfa18-2435">Устранена проблема с установкой AEM, если в идентификаторах ресурсов дисков группа ресурсов указана в нижнем регистре.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2435">Fix issue with AEM installation if resource ids of disks had lowercase resourcegroups in resource id</span></span>
* <span data-ttu-id="cfa18-2436">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2436">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="cfa18-2437">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2437">Fix documentation for wildcards</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cfa18-2438">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cfa18-2438">Az.DataFactory</span></span>
* <span data-ttu-id="cfa18-2439">Добавлены свойства SsisProperties, если NodeCount не имеет значения NULL для управляемой среды выполнения интеграции.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2439">Add SsisProperties if NodeCount not null for managed integration runtime.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cfa18-2440">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cfa18-2440">Az.DataLakeStore</span></span>
* <span data-ttu-id="cfa18-2441">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2441">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="cfa18-2442">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="cfa18-2442">Az.EventGrid</span></span>
* <span data-ttu-id="cfa18-2443">Обновлен текст справки для конечной точки, указывающий, что необходимо создать ресурсы, прежде чем использовать командлеты для создания или обновления подписки на события.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2443">Updated the help text for endpoint to indicate that resources should be created before using the create/update event subscription cmdlets.</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="cfa18-2444">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="cfa18-2444">Az.EventHub</span></span>
* <span data-ttu-id="cfa18-2445">Добавлены новые командлеты для NetworkRuleSet пространства имен.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2445">Added new cmdlets for NetworkRuleSet of Namespace</span></span>

#### <a name="azhdinsight"></a><span data-ttu-id="cfa18-2446">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="cfa18-2446">Az.HDInsight</span></span>
* <span data-ttu-id="cfa18-2447">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2447">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cfa18-2448">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cfa18-2448">Az.IotHub</span></span>
* <span data-ttu-id="cfa18-2449">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2449">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cfa18-2450">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cfa18-2450">Az.KeyVault</span></span>
* <span data-ttu-id="cfa18-2451">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2451">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="cfa18-2452">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2452">Fix documentation for wildcards</span></span>

#### <a name="azmachinelearning"></a><span data-ttu-id="cfa18-2453">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="cfa18-2453">Az.MachineLearning</span></span>
* <span data-ttu-id="cfa18-2454">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2454">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmedia"></a><span data-ttu-id="cfa18-2455">Az.Media</span><span class="sxs-lookup"><span data-stu-id="cfa18-2455">Az.Media</span></span>
* <span data-ttu-id="cfa18-2456">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2456">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cfa18-2457">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cfa18-2457">Az.Monitor</span></span>
  * <span data-ttu-id="cfa18-2458">Добавлены новые командлеты для правила генерации оповещений на основе метрик GenV2 (не классических).</span><span class="sxs-lookup"><span data-stu-id="cfa18-2458">New cmdlets for GenV2(non classic) metric-based alert rule</span></span>
      - <span data-ttu-id="cfa18-2459">New-AzMetricAlertRuleV2DimensionSelection</span><span class="sxs-lookup"><span data-stu-id="cfa18-2459">New-AzMetricAlertRuleV2DimensionSelection</span></span>
      - <span data-ttu-id="cfa18-2460">New-AzMetricAlertRuleV2Criteria</span><span class="sxs-lookup"><span data-stu-id="cfa18-2460">New-AzMetricAlertRuleV2Criteria</span></span>
      - <span data-ttu-id="cfa18-2461">Remove-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="cfa18-2461">Remove-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="cfa18-2462">Get-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="cfa18-2462">Get-AzMetricAlertRuleV2</span></span>
      - <span data-ttu-id="cfa18-2463">Add-AzMetricAlertRuleV2</span><span class="sxs-lookup"><span data-stu-id="cfa18-2463">Add-AzMetricAlertRuleV2</span></span>
  * <span data-ttu-id="cfa18-2464">Обновлен пакет SDK Monitor до предварительной версии 0.22.0.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2464">Updated Monitor SDK to version 0.22.0-preview</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cfa18-2465">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cfa18-2465">Az.Network</span></span>
* <span data-ttu-id="cfa18-2466">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2466">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="cfa18-2467">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2467">Fix documentation for wildcards</span></span>

#### <a name="aznotificationhubs"></a><span data-ttu-id="cfa18-2468">Az.NotificationHubs</span><span class="sxs-lookup"><span data-stu-id="cfa18-2468">Az.NotificationHubs</span></span>
* <span data-ttu-id="cfa18-2469">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2469">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="cfa18-2470">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cfa18-2470">Az.OperationalInsights</span></span>
* <span data-ttu-id="cfa18-2471">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2471">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azpowerbiembedded"></a><span data-ttu-id="cfa18-2472">Az.PowerBIEmbedded</span><span class="sxs-lookup"><span data-stu-id="cfa18-2472">Az.PowerBIEmbedded</span></span>
* <span data-ttu-id="cfa18-2473">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2473">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cfa18-2474">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cfa18-2474">Az.RecoveryServices</span></span>
* <span data-ttu-id="cfa18-2475">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2475">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="cfa18-2476">Обновлен табличный формат для SQL на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2476">Updated table format for SQL in azure VM</span></span>
* <span data-ttu-id="cfa18-2477">Добавлен альтернативный метод для получения расположения в Общей папке Azure.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2477">Added alternate method to fetch location in AzureFileShare</span></span>
* <span data-ttu-id="cfa18-2478">Обновлено значение ScheduleRunDays в объекте SchedulePolicy в соответствии с часовым поясом.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2478">Updated ScheduleRunDays in SchedulePolicy object according to timezone</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="cfa18-2479">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="cfa18-2479">Az.RedisCache</span></span>
* <span data-ttu-id="cfa18-2480">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2480">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cfa18-2481">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cfa18-2481">Az.Resources</span></span>
* <span data-ttu-id="cfa18-2482">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2482">Fix documentation for wildcards</span></span>

#### <a name="azsql"></a><span data-ttu-id="cfa18-2483">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cfa18-2483">Az.Sql</span></span>
* <span data-ttu-id="cfa18-2484">Заменена зависимость от пакета SDK монитора на обычный код.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2484">Replace dependency on Monitor SDK with common code</span></span>
* <span data-ttu-id="cfa18-2485">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2485">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="cfa18-2486">Улучшен процесс классификации нескольких столбцов.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2486">Enhanced process of multiple columns classification.</span></span>
* <span data-ttu-id="cfa18-2487">Добавлены свойства SKU (имя, семейство, производительность SKU) в отклике Get-AzSqlServerServiceObjective, а также по умолчанию задан табличный формат.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2487">Include sku properties (sku name, family, capacity) in response from Get-AzSqlServerServiceObjective and format as table by default.</span></span>
* <span data-ttu-id="cfa18-2488">C помощью Get-AzSqlServerServiceObjective теперь можно получать список доступных целевых служб по расположению без необходимости заранее размещать сервер в регионе.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2488">Ability to Get-AzSqlServerServiceObjective by location without needing a preexisting server in the region.</span></span>
* <span data-ttu-id="cfa18-2489">Поддерживается параметр часового пояса при создании Управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2489">Support for time zone parameter in Managed Instance create.</span></span>
* <span data-ttu-id="cfa18-2490">Исправлена документация по подстановочным знакам.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2490">Fix documentation for wildcards</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cfa18-2491">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cfa18-2491">Az.Websites</span></span>
* <span data-ttu-id="cfa18-2492">Исправлены командлеты Set-AzWebApp и Set-AzWebAppSlot, которые теперь не удаляют теги при выполнении.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2492">fixes the Set-AzWebApp and Set-AzWebAppSlot to not remove the tags on execution</span></span>
* <span data-ttu-id="cfa18-2493">Изменены присутствующие в командлетах существительные во множественном числе на существительные в единственном числе, а также устаревшие имена во множественном числе.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2493">Updated cmdlets with plural nouns to singular, and deprecated plural names.</span></span>
* <span data-ttu-id="cfa18-2494">Обновлен пакет SDK веб-узлов.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2494">Updated the WebSites SDK.</span></span>
* <span data-ttu-id="cfa18-2495">Удалено свойство AdminSiteName из PSAppServicePlan.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2495">Removed the AdminSiteName property from PSAppServicePlan.</span></span>

## <a name="170---april-2019"></a><span data-ttu-id="cfa18-2496">1.7.0 —апрель 2019 г.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2496">1.7.0 - April 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="cfa18-2497">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="cfa18-2497">Highlights since the last major release</span></span>
* <span data-ttu-id="cfa18-2498">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2498">General availability of `Az` module</span></span>
* <span data-ttu-id="cfa18-2499">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="cfa18-2499">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="cfa18-2500">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="cfa18-2500">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="cfa18-2501">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2501">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="cfa18-2502">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2502">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="cfa18-2503">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2503">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="cfa18-2504">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="cfa18-2504">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azaccounts"></a><span data-ttu-id="cfa18-2505">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cfa18-2505">Az.Accounts</span></span>
* <span data-ttu-id="cfa18-2506">Обновлены командлеты Add-AzEnvironment и Set-AzEnvironment. Теперь они принимают параметр AzureAnalysisServicesEndpointResourceId.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2506">Updated Add-AzEnvironment and Set-AzEnvironment to accept parameter AzureAnalysisServicesEndpointResourceId</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="cfa18-2507">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="cfa18-2507">Az.AnalysisServices</span></span>
* <span data-ttu-id="cfa18-2508">Использование ServiceClient в командлетах плоскости данных и удаление исходной логики проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2508">Using ServiceClient in dataplane cmdlets and removing the original authentication logic</span></span>
* <span data-ttu-id="cfa18-2509">Add-AzureASAccount используется как оболочка для Connect-AzAccount во избежание критических изменений.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2509">Making Add-AzureASAccount a wrapper of Connect-AzAccount to avoid a breaking change</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cfa18-2510">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cfa18-2510">Az.Automation</span></span>
* <span data-ttu-id="cfa18-2511">Исправлена ошибка командлета New-AzAutomationSoftwareUpdateConfiguration, связанная с включением.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2511">Fixed New-AzAutomationSoftwareUpdateConfiguration cmdlet bug for Inclusions.</span></span> <span data-ttu-id="cfa18-2512">Теперь параметры IncludedKbNumber и IncludedPackageNameMask должны работать нормально.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2512">Now parameter IncludedKbNumber and IncludedPackageNameMask should work.</span></span>
* <span data-ttu-id="cfa18-2513">Исправлена ошибка динамической группы управления обновлениями службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2513">Bug fix for azure automation update management dynamic group</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cfa18-2514">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cfa18-2514">Az.Compute</span></span>
* <span data-ttu-id="cfa18-2515">В командлеты New-AzDiskConfig и New-AzSnapshotConfig добавлен параметр HyperVGeneration.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2515">Add HyperVGeneration parameter to New-AzDiskConfig and New-AzSnapshotConfig</span></span>
* <span data-ttu-id="cfa18-2516">Теперь можно создавать виртуальные машину на основе образов из коллекции от других клиентов.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2516">Allow VM creation with galley image from other tenants.</span></span>

#### <a name="azcontainerinstance"></a><span data-ttu-id="cfa18-2517">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="cfa18-2517">Az.ContainerInstance</span></span>
* <span data-ttu-id="cfa18-2518">Исправлена проблема в параметре -Command командлета New-AzContainerGroup, из-за которой в конце добавлялся пустой аргумент.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2518">Fixed issue in the -Command parameter of New-AzContainerGroup which added a trailing empty argument</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cfa18-2519">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cfa18-2519">Az.DataFactory</span></span>
* <span data-ttu-id="cfa18-2520">Пакет SDK для ADF .NET обновлен до версии 3.0.2.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2520">Updated ADF .Net SDK version to 3.0.2</span></span>
* <span data-ttu-id="cfa18-2521">Командлет Set-AzDataFactoryV2 обновлен с помощью дополнительных параметров для настроек, связанных с RepoConfiguration.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2521">Updated Set-AzDataFactoryV2 cmdlet with extra parameters for RepoConfiguration related settings.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cfa18-2522">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cfa18-2522">Az.Resources</span></span>
* <span data-ttu-id="cfa18-2523">Улучшена обработка поставщиков Get-AzResource при предоставлении параметров -ResourceId или -ResourceGroupName, -Name и -ResourceType.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2523">Improve handling of providers for 'Get-AzResource' when providing '-ResourceId' or '-ResourceGroupName', '-Name' and '-ResourceType' parameters</span></span>
* <span data-ttu-id="cfa18-2524">Улучшена обработка ошибок в командлетах Test-AzDeployment и Test-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2524">Improve error handling for 'Test-AzDeployment' and 'Test-AzResourceGroupDeployment'</span></span>
    - <span data-ttu-id="cfa18-2525">Теперь ошибки, возникающие за пределами проверки развертывания, обрабатываются и включаются в выходные данные команды.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2525">Handle errors thrown outside of deployment validation and include them in output of command instead</span></span>
    - <span data-ttu-id="cfa18-2526">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2526">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>
* <span data-ttu-id="cfa18-2527">Добавлен параметр-переключатель -IgnoreDynamicParameters, с помощью которого можно настроить командлеты развертывания так, чтобы они пропускали запросы в сценариях скриптов и заданий.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2527">Add '-IgnoreDynamicParameters' switch parameter to set of deployment cmdlets to skip prompt in script and job scenarios</span></span>
    - <span data-ttu-id="cfa18-2528">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/6856.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2528">More information here: https://github.com/Azure/azure-powershell/issues/6856</span></span>

#### <a name="azsql"></a><span data-ttu-id="cfa18-2529">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cfa18-2529">Az.Sql</span></span>
* <span data-ttu-id="cfa18-2530">Поддержка классификации данных в базе данных.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2530">Support Database Data Classification.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cfa18-2531">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cfa18-2531">Az.Storage</span></span>
* <span data-ttu-id="cfa18-2532">Подробные сообщения об ошибке передаются при создании контекста хранилища с помощью параметра -UseConnectedAccount, но без входа в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2532">Report detail error when create Storage context with parameter -UseConnectedAccount, but without login Azure account</span></span>
    - <span data-ttu-id="cfa18-2533">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="cfa18-2533">New-AzStorageContext</span></span>
* <span data-ttu-id="cfa18-2534">Поддержка свойств службы управления BLOB-объектов в указанной учетной записи хранения с помощью API плоскости управления.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2534">Support Manage Blob Service Properties of a specified Storage account with Management plane API</span></span>
    - <span data-ttu-id="cfa18-2535">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="cfa18-2535">Update-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="cfa18-2536">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="cfa18-2536">Get-AzStorageBlobServiceProperty</span></span>
    - <span data-ttu-id="cfa18-2537">Enable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="cfa18-2537">Enable-AzStorageBlobDeleteRetentionPolicy</span></span>
    - <span data-ttu-id="cfa18-2538">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="cfa18-2538">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>
* <span data-ttu-id="cfa18-2539">Поддержка параметра -AsJob в командлетах для отправки и скачивания больших двоичных объектов и файлов.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2539">-AsJob support for Blob and file upload and download cmdlets</span></span>
    - <span data-ttu-id="cfa18-2540">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="cfa18-2540">Get-AzStorageBlobContent</span></span>
    - <span data-ttu-id="cfa18-2541">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="cfa18-2541">Set-AzStorageBlobContent</span></span>
    - <span data-ttu-id="cfa18-2542">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="cfa18-2542">Get-AzStorageFileContent</span></span>
    - <span data-ttu-id="cfa18-2543">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="cfa18-2543">Set-AzStorageFileContent</span></span>

## <a name="160---march-2019"></a><span data-ttu-id="cfa18-2544">1.6.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2544">1.6.0 - March 2019</span></span>
### <a name="highlights-since-the-last-major-release"></a><span data-ttu-id="cfa18-2545">Основные возможности с момента последнего основного выпуска</span><span class="sxs-lookup"><span data-stu-id="cfa18-2545">Highlights since the last major release</span></span>
* <span data-ttu-id="cfa18-2546">Общедоступная версия модуля `Az`.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2546">General availability of `Az` module</span></span>
* <span data-ttu-id="cfa18-2547">Дополнительные сведения о модуле `Az` см. по этой ссылке: https://aka.ms/azps-announce</span><span class="sxs-lookup"><span data-stu-id="cfa18-2547">For more information about the `Az` module, please visit the following: https://aka.ms/azps-announce</span></span>
* <span data-ttu-id="cfa18-2548">Добавлены средства заполнения для Location, ResourceGroup и ResourceName: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span><span class="sxs-lookup"><span data-stu-id="cfa18-2548">Added Location, ResourceGroup, and ResourceName completers: https://azure.microsoft.com/blog/completers-in-azure-powershell/</span></span>
* <span data-ttu-id="cfa18-2549">Добавлена поддержка подстановочных знаков в командлетах Get для Az.Compute и Az.Network.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2549">Added wildcard support to Get cmdlets for Az.Compute and Az.Network</span></span>
* <span data-ttu-id="cfa18-2550">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2550">Added interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="cfa18-2551">Добавлена поддержка для модулей runbook Python 2 в Az.Automation.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2551">Added support for Python 2 runbooks in Az.Automation</span></span>
* <span data-ttu-id="cfa18-2552">Az.LogicApp. Новые командлеты для сборок учетных записей интеграции и конфигурации пакета:</span><span class="sxs-lookup"><span data-stu-id="cfa18-2552">Az.LogicApp: New cmdlets for Integration Account Assemblies and Batch Configuration</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cfa18-2553">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cfa18-2553">Az.Automation</span></span>
* <span data-ttu-id="cfa18-2554">В управление обновлениями службы автоматизации Azure внесены изменения для поддержки следующих новых функций:</span><span class="sxs-lookup"><span data-stu-id="cfa18-2554">Azure automation update management change to support the following new features :</span></span>
    * <span data-ttu-id="cfa18-2555">динамическое группирование;</span><span class="sxs-lookup"><span data-stu-id="cfa18-2555">Dynamic grouping</span></span>
    * <span data-ttu-id="cfa18-2556">скрипты предварительного или последующего выполнения;</span><span class="sxs-lookup"><span data-stu-id="cfa18-2556">Pre-Post script</span></span>
    * <span data-ttu-id="cfa18-2557">параметр перезагрузки.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2557">Reboot Setting</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cfa18-2558">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cfa18-2558">Az.Compute</span></span>
* <span data-ttu-id="cfa18-2559">Устранена проблема, связанная с разрешением пути в Get-AzVmBootDiagnosticsData.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2559">Fix issue with path resolution in Get-AzVmBootDiagnosticsData</span></span>
* <span data-ttu-id="cfa18-2560">Обновление клиентской библиотеки вычислений до версии 25.0.0.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2560">Update Compute client library to 25.0.0.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cfa18-2561">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cfa18-2561">Az.KeyVault</span></span>
* <span data-ttu-id="cfa18-2562">Добавлена поддержка подстановочных знаков в командлетах KeyVault.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2562">Added wildcard support to KeyVault cmdlets</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cfa18-2563">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cfa18-2563">Az.Network</span></span>
* <span data-ttu-id="cfa18-2564">Добавлена поддержка анализа угроз для Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2564">Add Threat Intelligence support for Azure Firewall</span></span>
* <span data-ttu-id="cfa18-2565">Добавлены настраиваемые правила и ресурс верхнего уровня для политики брандмауэра Шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2565">Add Application Gateway Firewall Policy top level resource and Custom Rules</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cfa18-2566">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cfa18-2566">Az.RecoveryServices</span></span>
* <span data-ttu-id="cfa18-2567">В политику виртуальной машины Azure добавлен объект SnapshotRetentionInDays для поддержки мгновенного восстановления.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2567">Added SnapshotRetentionInDays in Azure VM policy to support Instant RP</span></span>
* <span data-ttu-id="cfa18-2568">Добавлена поддержка канала для отмены регистрации контейнера.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2568">Added pipe support for unregister container</span></span>

#### <a name="azresources"></a><span data-ttu-id="cfa18-2569">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cfa18-2569">Az.Resources</span></span>
* <span data-ttu-id="cfa18-2570">Обновлена поддержка подстановочных знаков для Get-AzResource и Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2570">Update wildcard support for Get-AzResource and Get-AzResourceGroup</span></span>
* <span data-ttu-id="cfa18-2571">Обновлены учетные данные, используемые при общих вызовах к ARM.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2571">Update credentials used when making generic calls to ARM</span></span>

#### <a name="azsql"></a><span data-ttu-id="cfa18-2572">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cfa18-2572">Az.Sql</span></span>
* <span data-ttu-id="cfa18-2573">Изменен тип параметра (ExcludeDetectionType) командлетов для обнаружения угроз с DetectionTypes на string[] для поддержки актуального состояния при добавлении новых типов обнаружения и для поддержки автозаполнения.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2573">changed Threat Detection's cmdlets param (ExcludeDetectionType) from DetectionType to string[] to make it future proof when new DetectionTypes are added and to support autocomplete as well.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cfa18-2574">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cfa18-2574">Az.Storage</span></span>
* <span data-ttu-id="cfa18-2575">Поддержка получения, настройки и удаления политики управления в учетной записи хранения.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2575">Support Get/Set/Remove Management Policy on a Storage account</span></span>
    - <span data-ttu-id="cfa18-2576">Set-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="cfa18-2576">Set-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="cfa18-2577">Get-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="cfa18-2577">Get-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="cfa18-2578">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="cfa18-2578">Remove-AzStorageAccountManagementPolicy</span></span>
    - <span data-ttu-id="cfa18-2579">Add-AzStorageAccountManagementPolicyAction</span><span class="sxs-lookup"><span data-stu-id="cfa18-2579">Add-AzStorageAccountManagementPolicyAction</span></span>
    - <span data-ttu-id="cfa18-2580">New-AzStorageAccountManagementPolicyFilter</span><span class="sxs-lookup"><span data-stu-id="cfa18-2580">New-AzStorageAccountManagementPolicyFilter</span></span>
    - <span data-ttu-id="cfa18-2581">New-AzStorageAccountManagementPolicyRule</span><span class="sxs-lookup"><span data-stu-id="cfa18-2581">New-AzStorageAccountManagementPolicyRule</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cfa18-2582">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cfa18-2582">Az.Websites</span></span>
* <span data-ttu-id="cfa18-2583">Исправлена ошибка с шаблоном ARM, из-за которой прерывалось клонирование все слотов при использовании New-AzWebApp -IncludeSourceWebAppSlots.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2583">Fix ARM template bug that breaks cloning all slots using 'New-AzWebApp -IncludeSourceWebAppSlots'</span></span>

## <a name="150---march-2019"></a><span data-ttu-id="cfa18-2584">1.5.0 — март 2019 г.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2584">1.5.0 - March 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cfa18-2585">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cfa18-2585">Az.Accounts</span></span>
* <span data-ttu-id="cfa18-2586">Добавлена команда Register-AzModule для поддержки созданных командлетов AutoRest.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2586">Add 'Register-AzModule' command to support AutoRest generated cmdlets</span></span>
* <span data-ttu-id="cfa18-2587">Обновлены примеры для Connect AzAccount.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2587">Update examples for Connect-AzAccount</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cfa18-2588">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cfa18-2588">Az.Automation</span></span>
* <span data-ttu-id="cfa18-2589">Исправлена проблема с получением некоторых ежемесячных расписаний в нескольких командлетах службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2589">Fixed issue when retreiving certain monthly schedules in several Azure Automation cmdlets</span></span>
* <span data-ttu-id="cfa18-2590">Исправлен командлет Get-AzAutomationDscNode, возвращающий только первые 20 узлов.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2590">Fix Get-AzAutomationDscNode returning just top 20 nodes.</span></span> <span data-ttu-id="cfa18-2591">Теперь он возвращает все узлы.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2591">Now it returns all nodes</span></span>

#### <a name="azcdn"></a><span data-ttu-id="cfa18-2592">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="cfa18-2592">Az.Cdn</span></span>
* <span data-ttu-id="cfa18-2593">Добавлены новые командлеты PowerShell для включения и отключения HTTPS для личного домена и отключены устаревшие командлеты.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2593">Added new Powershell cmdlets for Enable/Disable Custom Domain Https and deprecated the old ones</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cfa18-2594">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cfa18-2594">Az.Compute</span></span>
* <span data-ttu-id="cfa18-2595">Добавлена поддержка подстановочных знаков в командлетах Get.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2595">Add wildcard support to Get cmdlets</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cfa18-2596">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cfa18-2596">Az.DataFactory</span></span>
* <span data-ttu-id="cfa18-2597">Обновлен пакет SDK для ADF .NET до версии 3.0.1.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2597">Updated ADF .Net SDK version to 3.0.1</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="cfa18-2598">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="cfa18-2598">Az.LogicApp</span></span>
* <span data-ttu-id="cfa18-2599">Исправлена проблема с получением только первой страницы результатов при выполнении команды ListWorkflows.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2599">Fix for ListWorkflows only retrieving the first page of results</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cfa18-2600">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cfa18-2600">Az.Network</span></span>
* <span data-ttu-id="cfa18-2601">Добавлена поддержка подстановочных знаков в командлетах Network.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2601">Add wildcard support to Network cmdlets</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cfa18-2602">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cfa18-2602">Az.RecoveryServices</span></span>
* <span data-ttu-id="cfa18-2603">Добавлена поддержка SQL Server на виртуальной машине Azure.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2603">Added Sql server in Azure VM support</span></span>
* <span data-ttu-id="cfa18-2604">Обновление пакета SDK</span><span class="sxs-lookup"><span data-stu-id="cfa18-2604">SDK Update</span></span>
* <span data-ttu-id="cfa18-2605">Удалена проверка VMappContainer в Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2605">Removed VMappContainer check in Get-ProtectableItem</span></span>
* <span data-ttu-id="cfa18-2606">Добавлены параметры Name и ServerName для Get-ProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2606">Added Name and ServerName as parameters for Get-ProtectableItem</span></span>

#### <a name="azresources"></a><span data-ttu-id="cfa18-2607">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cfa18-2607">Az.Resources</span></span>
* <span data-ttu-id="cfa18-2608">Добавлен параметр `-TemplateObject` в командлеты для развертывания.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2608">Add `-TemplateObject` parameter to deployment cmdlets</span></span>
    - <span data-ttu-id="cfa18-2609">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2933.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2609">More information here: https://github.com/Azure/azure-powershell/issues/2933</span></span>
* <span data-ttu-id="cfa18-2610">Устранена проблема с передачей в конвейер результата `Get-AzResource` для `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2610">Fix issue when piping the result of `Get-AzResource` to `Set-AzResource`</span></span>
    - <span data-ttu-id="cfa18-2611">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8240.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2611">More information here: https://github.com/Azure/azure-powershell/issues/8240</span></span>
* <span data-ttu-id="cfa18-2612">Устранена проблема с изменением типа данных JSON при выполнении `Set-AzResource`.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2612">Fix issue with JSON data type change when running `Set-AzResource`</span></span>
    - <span data-ttu-id="cfa18-2613">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7930.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2613">More information here: https://github.com/Azure/azure-powershell/issues/7930</span></span>

#### <a name="azsql"></a><span data-ttu-id="cfa18-2614">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cfa18-2614">Az.Sql</span></span>
* <span data-ttu-id="cfa18-2615">Обновление AuditingEndpointsCommunicator.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2615">Updating AuditingEndpointsCommunicator.</span></span>
    - <span data-ttu-id="cfa18-2616">Исправлено поведение для пограничного случая при создании параметров диагностики.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2616">Fixing the behavior of an edge case while creating new diagnostic settings.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cfa18-2617">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cfa18-2617">Az.Storage</span></span>
* <span data-ttu-id="cfa18-2618">Включена поддержка Kind BlockBlobStorage при создании учетной записи хранения для New-AzStorageAccount.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2618">Support Kind BlockBlobStorage when create Storage account      - New-AzStorageAccount</span></span>

## <a name="140---february-2019"></a><span data-ttu-id="cfa18-2619">1.4.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2619">1.4.0 - February 2019</span></span>
#### <a name="azanalysisservices"></a><span data-ttu-id="cfa18-2620">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="cfa18-2620">Az.AnalysisServices</span></span>
* <span data-ttu-id="cfa18-2621">Командлет AddAzureASAccount устарел.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2621">Deprecated AddAzureASAccount cmdlet</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cfa18-2622">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cfa18-2622">Az.Automation</span></span>
* <span data-ttu-id="cfa18-2623">Обновлена справка для командлета Import-AzAutomationDscNodeConfiguration.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2623">Update help for Import-AzAutomationDscNodeConfiguration</span></span>
* <span data-ttu-id="cfa18-2624">Добавлена проверка имени конфигурации для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2624">Added configuration name validation to Import-AzAutomationDscConfiguration cmdlet</span></span>
* <span data-ttu-id="cfa18-2625">Улучшена обработка ошибок для командлета Import-AzAutomationDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2625">Improved error handling for Import-AzAutomationDscConfiguration cmdlet</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cfa18-2626">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cfa18-2626">Az.CognitiveServices</span></span>
* <span data-ttu-id="cfa18-2627">Добавлен параметр CustomSubdomainName — новый необязательный параметр для командлета New-AzCognitiveServicesAccount, который указывает поддомен для ресурса.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2627">Added CustomSubdomainName as a new optional parameter for New-AzCognitiveServicesAccount which is used to specify subdomain for the resource.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cfa18-2628">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cfa18-2628">Az.Compute</span></span>
* <span data-ttu-id="cfa18-2629">Устранена проблема с идентификаторами наборов параметров.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2629">Fix issue with ID parameter sets</span></span>
* <span data-ttu-id="cfa18-2630">Обновлен командлет Get-AzVMExtension для отображения списка всех установленных расширений, если не указан параметр Name.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2630">Update Get-AzVMExtension to list all installed extension if Name parameter is not provided</span></span>
* <span data-ttu-id="cfa18-2631">Для командлета Update-AzImage добавлены параметры Tag и ResourceId.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2631">Add Tag and ResourceId parameters to Update-AzImage cmdlet</span></span>
* <span data-ttu-id="cfa18-2632">Командлет Get-AzVmssVM, который выполняется без указания идентификатора экземпляра и с параметром InstanceView, может выводить виртуальные машины из VMSS с представлением экземпляра.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2632">Get-AzVmssVM without instance ID and with InstanceView can list VMSS VMs with instance view.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cfa18-2633">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cfa18-2633">Az.DataLakeStore</span></span>
* <span data-ttu-id="cfa18-2634">Добавлены командлеты для перечисления и восстановления удаленного элемента ADL.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2634">Add cmdlets for ADL deleted item enumerate and restore</span></span>

#### <a name="azeventhub"></a><span data-ttu-id="cfa18-2635">Az.EventHub</span><span class="sxs-lookup"><span data-stu-id="cfa18-2635">Az.EventHub</span></span>
* <span data-ttu-id="cfa18-2636">Добавлено новое логическое свойство SkipEmptyArchives для пропуска пустых архивов в классе CaptureDescription Eventhub.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2636">Added new boolean property SkipEmptyArchives to Skip Empty Archives in CaptureDescription class of Eventhub</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cfa18-2637">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cfa18-2637">Az.KeyVault</span></span>
* <span data-ttu-id="cfa18-2638">Исправлена расстановка тегов для командлета Set-AzKeyVaultSecret.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2638">Fix tagging on Set-AzKeyVaultSecret</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="cfa18-2639">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="cfa18-2639">Az.LogicApp</span></span>
* <span data-ttu-id="cfa18-2640">Добавлен SKU "Базовый" для учетных записей интеграции.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2640">Add in Basic sku for Integration Accounts</span></span>
* <span data-ttu-id="cfa18-2641">Добавлены типы сопоставлений Liquid, а также XSLT 2.0 и XSLT 3.0.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2641">Add in XSLT 2.0, XSLT 3.0 and Liquid Map Types</span></span>
* <span data-ttu-id="cfa18-2642">Новые командлеты для сборок учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="cfa18-2642">New cmdlets for Integration Account Assemblies</span></span>
    - <span data-ttu-id="cfa18-2643">Get-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="cfa18-2643">Get-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="cfa18-2644">New-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="cfa18-2644">New-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="cfa18-2645">Remove-AzIntegrationAccountAssembly;</span><span class="sxs-lookup"><span data-stu-id="cfa18-2645">Remove-AzIntegrationAccountAssembly</span></span>
    - <span data-ttu-id="cfa18-2646">Set-AzIntegrationAccountAssembly.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2646">Set-AzIntegrationAccountAssembly</span></span>
* <span data-ttu-id="cfa18-2647">Новые командлеты для конфигурации пакета учетных записей интеграции:</span><span class="sxs-lookup"><span data-stu-id="cfa18-2647">New cmdlets for Integration Account Batch Configuration</span></span>
    - <span data-ttu-id="cfa18-2648">Get-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="cfa18-2648">Get-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="cfa18-2649">New-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="cfa18-2649">New-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="cfa18-2650">Remove-AzIntegrationAccountBatchConfiguration;</span><span class="sxs-lookup"><span data-stu-id="cfa18-2650">Remove-AzIntegrationAccountBatchConfiguration</span></span>
    - <span data-ttu-id="cfa18-2651">Set-AzIntegrationAccountBatchConfiguration.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2651">Set-AzIntegrationAccountBatchConfiguration</span></span>
* <span data-ttu-id="cfa18-2652">Обновлен пакет SDK Logic Apps до версии 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2652">Update Logic App SDK to version 4.1.0</span></span>

#### <a name="azmonitor"></a><span data-ttu-id="cfa18-2653">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cfa18-2653">Az.Monitor</span></span>
* <span data-ttu-id="cfa18-2654">Обновлена справка для командлета Get-AzMetric.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2654">Update help for Get-AzMetric</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cfa18-2655">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cfa18-2655">Az.Network</span></span>
* <span data-ttu-id="cfa18-2656">Обновлен пример справки для командлета Add-AzApplicationGatewayCustomError.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2656">Update help example for Add-AzApplicationGatewayCustomError</span></span>

#### <a name="azoperationalinsights"></a><span data-ttu-id="cfa18-2657">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cfa18-2657">Az.OperationalInsights</span></span>
* <span data-ttu-id="cfa18-2658">Дополнительная поддержка создания и получения источников данных ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2658">Additional support for New and Get ApplicationInsights data source.</span></span>
    - <span data-ttu-id="cfa18-2659">Добавлен новый тип ApplicationInsights для получения определенных или всех источников данных ApplicationInsights для указанной рабочей области.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2659">Added new 'ApplicationInsights' kind to support Get specific and Get all ApplicationInsights data sources for given workspace.</span></span>
    - <span data-ttu-id="cfa18-2660">Добавлен командлет New-AzOperationalInsightsApplicationInsightsDataSource для создания источника данных с использованием параметров указанного ресурса Application-Insightss: subscription Id, resourceGroupName и name.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2660">Added New-AzOperationalInsightsApplicationInsightsDataSource cmdlet for creating data source by given Application-Insights resource parameters: subscription Id, resourceGroupName and name.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cfa18-2661">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cfa18-2661">Az.Resources</span></span>
* <span data-ttu-id="cfa18-2662">исправлена проблема https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2662">Fix for issue https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="cfa18-2663">исправлена проблема https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2663">Fix for issue https://github.com/Azure/azure-powershell/issues/8235</span></span>
* <span data-ttu-id="cfa18-2664">исправлена проблема https://github.com/Azure/azure-powershell/issues/6219.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2664">Fix for issue https://github.com/Azure/azure-powershell/issues/6219</span></span>
* <span data-ttu-id="cfa18-2665">Исправлена ошибка, препятствующая повторному созданию KeyCredentials.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2665">Fix bug preventing repeat creation of KeyCredentials</span></span>

#### <a name="azsql"></a><span data-ttu-id="cfa18-2666">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cfa18-2666">Az.Sql</span></span>
* <span data-ttu-id="cfa18-2667">Добавлена поддержка уровня гипермасштабирования в базе данных SQL.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2667">Add support for SQL DB Hyperscale tier</span></span>
* <span data-ttu-id="cfa18-2668">Исправлена ошибка, из-за которой восстановление могло завершиться со сбоем при указании ненужных свойств в запросе на восстановление.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2668">Fixed bug where restore could fail due to setting unnecessary properties in restore request</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cfa18-2669">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cfa18-2669">Az.Websites</span></span>
* <span data-ttu-id="cfa18-2670">Исправлен пример для командлета Get-AzWebAppSlotMetrics.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2670">Correct example in Get-AzWebAppSlotMetrics</span></span>

## <a name="130---february-2019"></a><span data-ttu-id="cfa18-2671">1.3.0 — февраль 2019 г.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2671">1.3.0 - February 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cfa18-2672">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cfa18-2672">Az.Accounts</span></span>
* <span data-ttu-id="cfa18-2673">Обновление до последней версии ClientRuntime</span><span class="sxs-lookup"><span data-stu-id="cfa18-2673">Update to latest version of ClientRuntime</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="cfa18-2674">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="cfa18-2674">Az.AnalysisServices</span></span>
<span data-ttu-id="cfa18-2675">Общедоступная версия модуля Az.AnalysisServices.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2675">General availability for Az.AnalysisServices module.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cfa18-2676">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cfa18-2676">Az.Compute</span></span>
* <span data-ttu-id="cfa18-2677">Расширение AEM: добавлена поддержка дисков UltraSSD, P60, P70 и P80.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2677">AEM extension: Add support for UltraSSD and P60,P70 and P80 disks</span></span>
* <span data-ttu-id="cfa18-2678">Обновлено описание справки для командлета Set-AzVMBootDiagnostics.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2678">Update help description for Set-AzVMBootDiagnostics</span></span>
* <span data-ttu-id="cfa18-2679">Обновлено описание справки и пример для командлета Update-AzImage.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2679">Update help description and example for Update-AzImage</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cfa18-2680">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cfa18-2680">Az.RecoveryServices</span></span>
<span data-ttu-id="cfa18-2681">Общедоступная версия модуля Az.RecoveryServices.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2681">General availability for Az.RecoveryServices module.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cfa18-2682">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cfa18-2682">Az.Resources</span></span>
* <span data-ttu-id="cfa18-2683">Исправлена расстановка тегов для групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2683">Fix tagging for resource groups</span></span>
    - <span data-ttu-id="cfa18-2684">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8166.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2684">More information here: https://github.com/Azure/azure-powershell/issues/8166</span></span>
* <span data-ttu-id="cfa18-2685">Исправлена проблема с игнорированием командлетом `Get-AzureRmRoleAssignment` параметра -ErrorAction.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2685">Fix issue where `Get-AzureRmRoleAssignment` doesn't respect -ErrorAction</span></span>
    - <span data-ttu-id="cfa18-2686">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8235.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2686">More information here: https://github.com/Azure/azure-powershell/issues/8235</span></span>

#### <a name="azsql"></a><span data-ttu-id="cfa18-2687">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cfa18-2687">Az.Sql</span></span>
* <span data-ttu-id="cfa18-2688">Добавлен командлет Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2688">Add Get/Set AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>
* <span data-ttu-id="cfa18-2689">Исправлена проблема с появлением исключения NullRef при выполнении командлетов SQL, если не выполнен вход в учетную запись Azure.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2689">Fix issue where not being logged into Azure account would result in nullref exception when executing SQL cmdlets</span></span>
* <span data-ttu-id="cfa18-2690">Исправлено исключение NullRef в командлете Get-AzSqlCapability.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2690">Fixed null ref exception in Get-AzSqlCapability</span></span>

## <a name="121---january-2019"></a><span data-ttu-id="cfa18-2691">1.2.1 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2691">1.2.1 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cfa18-2692">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cfa18-2692">Az.Accounts</span></span>
* <span data-ttu-id="cfa18-2693">Выпуск с правильной версией службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2693">Release with correct version of Authentication</span></span>

#### <a name="azanalysisservices"></a><span data-ttu-id="cfa18-2694">Az.AnalysisServices</span><span class="sxs-lookup"><span data-stu-id="cfa18-2694">Az.AnalysisServices</span></span>
* <span data-ttu-id="cfa18-2695">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2695">Release with updated Authentication dependency</span></span>

#### <a name="azrecoveryservices"></a><span data-ttu-id="cfa18-2696">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cfa18-2696">Az.RecoveryServices</span></span>
* <span data-ttu-id="cfa18-2697">Выпуск с обновленной зависимостью службы аутентификации.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2697">Release with updated Authentication dependency</span></span>

## <a name="120---january-2019"></a><span data-ttu-id="cfa18-2698">1.2.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2698">1.2.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cfa18-2699">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cfa18-2699">Az.Accounts</span></span>
* <span data-ttu-id="cfa18-2700">Добавлена интерактивная аутентификация и аутентификация по имени пользователя и паролю — только для Windows PowerShell 5.1.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2700">Add interactive and username/password authentication for Windows PowerShell 5.1 only</span></span>
* <span data-ttu-id="cfa18-2701">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2701">Update incorrect online help URLs</span></span>
* <span data-ttu-id="cfa18-2702">Добавлено предупреждающее сообщение в PS Core для модуля Uninstall-AzureRm.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2702">Add warning message in PS Core for Uninstall-AzureRm</span></span>

#### <a name="azaks"></a><span data-ttu-id="cfa18-2703">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="cfa18-2703">Az.Aks</span></span>
* <span data-ttu-id="cfa18-2704">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2704">Update incorrect online help URLs</span></span>

#### <a name="azautomation"></a><span data-ttu-id="cfa18-2705">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cfa18-2705">Az.Automation</span></span>
* <span data-ttu-id="cfa18-2706">Добавлена поддержка для модулей runbook Python 2.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2706">Added support for Python 2 runbooks</span></span>
* <span data-ttu-id="cfa18-2707">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2707">Update incorrect online help URLs</span></span>

#### <a name="azcdn"></a><span data-ttu-id="cfa18-2708">Az.Cdn</span><span class="sxs-lookup"><span data-stu-id="cfa18-2708">Az.Cdn</span></span>
* <span data-ttu-id="cfa18-2709">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2709">Update incorrect online help URLs</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cfa18-2710">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cfa18-2710">Az.Compute</span></span>
* <span data-ttu-id="cfa18-2711">Добавлен командлет Invoke-AzVMReimage.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2711">Add Invoke-AzVMReimage cmdlet</span></span>
* <span data-ttu-id="cfa18-2712">Добавлен параметр TempDisk к командлету Set-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2712">Add TempDisk parameter to Set-AzVmss</span></span>
* <span data-ttu-id="cfa18-2713">Исправлено предупреждающее сообщение командлета New-AzVM.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2713">Fix the warning message of New-AzVM</span></span>

#### <a name="azcontainerregistry"></a><span data-ttu-id="cfa18-2714">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="cfa18-2714">Az.ContainerRegistry</span></span>
* <span data-ttu-id="cfa18-2715">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2715">Update incorrect online help URLs</span></span>

#### <a name="azdatafactory"></a><span data-ttu-id="cfa18-2716">Az.DataFactory</span><span class="sxs-lookup"><span data-stu-id="cfa18-2716">Az.DataFactory</span></span>
* <span data-ttu-id="cfa18-2717">Пакет SDK ADF .Net обновлен до версии 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2717">Updated ADF .Net SDK version to 3.0.0</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cfa18-2718">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cfa18-2718">Az.DataLakeStore</span></span>
* <span data-ttu-id="cfa18-2719">Исправлена проблема с конечной точкой ADLS при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2719">Fix issue with ADLS endpoint when using MSI</span></span>
    - <span data-ttu-id="cfa18-2720">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7462.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2720">More information here: https://github.com/Azure/azure-powershell/issues/7462</span></span>
* <span data-ttu-id="cfa18-2721">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2721">Update incorrect online help URLs</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cfa18-2722">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cfa18-2722">Az.IotHub</span></span>
* <span data-ttu-id="cfa18-2723">Добавлен формат кодирования для командлета Add-IotHubRoutingEndpoint.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2723">Add Encoding format to Add-IotHubRoutingEndpoint cmdlet.</span></span>

#### <a name="azkeyvault"></a><span data-ttu-id="cfa18-2724">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cfa18-2724">Az.KeyVault</span></span>
* <span data-ttu-id="cfa18-2725">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2725">Update incorrect online help URLs</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cfa18-2726">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cfa18-2726">Az.Network</span></span>
* <span data-ttu-id="cfa18-2727">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2727">Update incorrect online help URLs</span></span>

#### <a name="azresources"></a><span data-ttu-id="cfa18-2728">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cfa18-2728">Az.Resources</span></span>
* <span data-ttu-id="cfa18-2729">Исправлены неправильные примеры в справочной документации по командлетам New-AzADAppCredential и New-AzADSpCredential.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2729">Fix incorrect examples in 'New-AzADAppCredential' and 'New-AzADSpCredential' reference documentation</span></span>
* <span data-ttu-id="cfa18-2730">Исправлена проблема, при которой путь для параметра -TemplateFile не удавалось разрешить до выполнения командлетов развертывания групп ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2730">Fix issue where path for '-TemplateFile' parameter was not being resolved before executing resource group deployment cmdlets</span></span>
* <span data-ttu-id="cfa18-2731">Az.Resources: исправлена документация для значения по умолчанию -Mode командлета New-AzureRmPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2731">Az.Resources: Correct documentation for New-AzureRmPolicyDefinition -Mode default value</span></span>
* <span data-ttu-id="cfa18-2732">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/7522.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2732">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/7522</span></span>
* <span data-ttu-id="cfa18-2733">Az.Resources: исправлена проблема https://github.com/Azure/azure-powershell/issues/5747.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2733">Az.Resources: Fix for issue https://github.com/Azure/azure-powershell/issues/5747</span></span>
* <span data-ttu-id="cfa18-2734">Исправлена проблема с форматированием объекта PSResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2734">Fix formatting issue with 'PSResourceGroupDeployment' object</span></span>
    - <span data-ttu-id="cfa18-2735">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/2123.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2735">More information here: https://github.com/Azure/azure-powershell/issues/2123</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="cfa18-2736">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cfa18-2736">Az.ServiceFabric</span></span>
* <span data-ttu-id="cfa18-2737">Исправлена проблема с появлением исключения в процессе отката при добавлении сертификата к модели VMSS: https://github.com/Azure/service-fabric-issues/issues/932.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2737">Rollback when a certificate is added to VMSS model but an exception is thrown this is to fix bug: https://github.com/Azure/service-fabric-issues/issues/932</span></span>
* <span data-ttu-id="cfa18-2738">Исправлены некоторые сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2738">Fix some error messages.</span></span>
* <span data-ttu-id="cfa18-2739">Исправлена проблема с созданием кластера с шаблоном ARM по умолчанию для командлета New-AzServiceFabriCluster, который не работал с операцией миграции в Az.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2739">Fix create cluster with default ARM template for New-AzServiceFabriCluster which was not working with migration to Az.</span></span>
* <span data-ttu-id="cfa18-2740">Исправлена проблема с добавлением сертификата кластера или приложения: теперь они добавляются только в Масштабируемые наборы виртуальных машин, которые сопоставлены с кластером, путем проверки идентификатора кластера в расширении.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2740">Fix add cluster/application certificate to only add to VM Scale Sets that correspond to the cluster by checking cluster id in the extension.</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="cfa18-2741">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="cfa18-2741">Az.SignalR</span></span>
* <span data-ttu-id="cfa18-2742">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2742">Update incorrect online help URLs</span></span>

#### <a name="azsql"></a><span data-ttu-id="cfa18-2743">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cfa18-2743">Az.Sql</span></span>
* <span data-ttu-id="cfa18-2744">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2744">Update incorrect online help URLs</span></span>
* <span data-ttu-id="cfa18-2745">Обновлено описание параметра LicenseType с добавлением возможных значений.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2745">Updated parameter description for LicenseType parameter with possible values</span></span>
* <span data-ttu-id="cfa18-2746">Исправлена проблема с неправильным обновлением удостоверения управляемого экземпляра, если оно было единственным обновляемым свойством.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2746">Fix for updating managed instance identity not working when it is the only updated property</span></span>
* <span data-ttu-id="cfa18-2747">Поддержка пользовательских параметров сортировки в управляемых экземплярах.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2747">Support for custom collation on managed instance</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cfa18-2748">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cfa18-2748">Az.Storage</span></span>
* <span data-ttu-id="cfa18-2749">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2749">Update incorrect online help URLs</span></span>
* <span data-ttu-id="cfa18-2750">Добавлен вывод подробных сообщений об ошибке при получении или установке классических свойств ведения журнала или метрик в учетной записи хранилища класса Premium, так как учетная запись хранилища класса Premium не поддерживает классические функции ведения журнала и метрик.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2750">Give detail error message when get/set classic Logging/Metric on Premium Storage Account, since Premium Storage Account not supoort classic Logging/Metric.</span></span>
    - <span data-ttu-id="cfa18-2751">Get/Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="cfa18-2751">Get/Set-AzStorageServiceLoggingProperty</span></span>
    - <span data-ttu-id="cfa18-2752">Get/Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="cfa18-2752">Get/Set-AzStorageServiceMetricsProperty</span></span>

#### <a name="aztrafficmanager"></a><span data-ttu-id="cfa18-2753">Az.TrafficManager</span><span class="sxs-lookup"><span data-stu-id="cfa18-2753">Az.TrafficManager</span></span>
* <span data-ttu-id="cfa18-2754">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2754">Update incorrect online help URLs</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cfa18-2755">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cfa18-2755">Az.Websites</span></span>
* <span data-ttu-id="cfa18-2756">Исправлены неправильные URL-адреса онлайн-справки.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2756">Update incorrect online help URLs</span></span>
* <span data-ttu-id="cfa18-2757">Исправлена работа командлета New-AzWebAppSSLBinding: сертификат отправляется в правильную группу ресурсов и правильное расположение, если приложение размещено в ASE.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2757">Fixes 'New-AzWebAppSSLBinding' to upload the certificate to the correct resourcegroup+location if the app is hosted on an ASE.</span></span>
* <span data-ttu-id="cfa18-2758">Исправлена работа командлета New-AzWebAppSSLBinding: теги не перезаписываются при привязке SSL-сертификата к приложению.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2758">Fixes 'New-AzWebAppSSLBinding' to not overwrite the tags on binding an SSL certificate to an app</span></span>

## <a name="110---january-2019"></a><span data-ttu-id="cfa18-2759">1.1.0 — январь 2019 г.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2759">1.1.0 - January 2019</span></span>
#### <a name="azaccounts"></a><span data-ttu-id="cfa18-2760">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cfa18-2760">Az.Accounts</span></span>
* <span data-ttu-id="cfa18-2761">Добавление области "Local" в Enable-AzureRmAlias.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2761">Add 'Local' Scope to Enable-AzureRmAlias</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cfa18-2762">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cfa18-2762">Az.Compute</span></span>
* <span data-ttu-id="cfa18-2763">Теперь имя не является обязательным в идентификаторе набора параметров для Restart/Start/Stop/Remove/Set-AzVM и Save-AzVMImage.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2763">Name is now optional in ID parameter set for Restart/Start/Stop/Remove/Set-AzVM and Save-AzVMImage</span></span>
* <span data-ttu-id="cfa18-2764">Обновлено описание идентификатора в файлах справки.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2764">Updated the description of ID in help files</span></span>
* <span data-ttu-id="cfa18-2765">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2765">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cfa18-2766">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cfa18-2766">Az.DataLakeStore</span></span>
* <span data-ttu-id="cfa18-2767">Обновление версии пакета SDK для плоскости данных до 1.1.14 для устранения найденных проблем.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2767">Update the sdk version of dataplane to 1.1.14 for SDK fixes.</span></span>
    - <span data-ttu-id="cfa18-2768">Исправлена обработка отрицательного времени доступа и времени изменения для getfilestatus и liststatus, исправлен токен отмены для асинхронных методов.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2768">Fix handling of negative acesstime and modificationtime for getfilestatus and liststatus, Fix async cancellation token</span></span>

#### <a name="azeventgrid"></a><span data-ttu-id="cfa18-2769">Az.EventGrid</span><span class="sxs-lookup"><span data-stu-id="cfa18-2769">Az.EventGrid</span></span>
* <span data-ttu-id="cfa18-2770">Обновление для использования API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2770">Updated to use the 2019-01-01 API version.</span></span>
* <span data-ttu-id="cfa18-2771">Обновлены указанные ниже командлеты для поддержки нового сценария в API версии 2019-01-01.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2771">Update the following cmdlets to support new scenario in 2019-01-01 API version</span></span>
    - <span data-ttu-id="cfa18-2772">New-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="cfa18-2772">New-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="cfa18-2773">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="cfa18-2773">Event Time-To-Live,</span></span>
        - <span data-ttu-id="cfa18-2774">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="cfa18-2774">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="cfa18-2775">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2775">Dead letter endpoint.</span></span>
    - <span data-ttu-id="cfa18-2776">Update-AzureRmEventGridSubscription. Добавлены новые необязательные параметры для указания:</span><span class="sxs-lookup"><span data-stu-id="cfa18-2776">Update-AzureRmEventGridSubscription: Add new optional parameters for specifying:</span></span>
        - <span data-ttu-id="cfa18-2777">срока жизни события;</span><span class="sxs-lookup"><span data-stu-id="cfa18-2777">Event Time-To-Live,</span></span>
        - <span data-ttu-id="cfa18-2778">максимального числа попыток доставки для событий;</span><span class="sxs-lookup"><span data-stu-id="cfa18-2778">Maximum number of delivery attempts for the events,</span></span>
        - <span data-ttu-id="cfa18-2779">конечной точки недоставленных сообщений.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2779">Dead letter endpoint.</span></span>
* <span data-ttu-id="cfa18-2780">Для параметра EndpointType добавлены новые значения перечисления (storageQueue и hybridConnection) в командлеты New-AzureRmEventGridSubscription и Update-AzureRmEventGridSubscription.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2780">Add new enum values (namely, storageQueue and hybridConnection) for EndpointType option in New-AzureRmEventGridSubscription and Update-AzureRmEventGridSubscription cmdlets.</span></span>
* <span data-ttu-id="cfa18-2781">Если ожидается, что создание или обновление подписки на событие повлечет за собой действия со стороны пользователя, выполняемые вручную, отображается предупреждение при создании или обновлении подписки события.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2781">Show warning message if creating or updating the event subscription is expected to entail manual action from user.</span></span>

#### <a name="aziothub"></a><span data-ttu-id="cfa18-2782">Az.IotHub</span><span class="sxs-lookup"><span data-stu-id="cfa18-2782">Az.IotHub</span></span>
* <span data-ttu-id="cfa18-2783">Пакет SDK Центра Интернета вещей обновлен до последней версии.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2783">Updated to the latest version of the IotHub SDK</span></span>

#### <a name="azlogicapp"></a><span data-ttu-id="cfa18-2784">Az.LogicApp</span><span class="sxs-lookup"><span data-stu-id="cfa18-2784">Az.LogicApp</span></span>
* <span data-ttu-id="cfa18-2785">Get-AzLogicApp позволяет перечислить все параметры без указанного имени.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2785">Get-AzLogicApp lists all without specified Name</span></span>

#### <a name="azresources"></a><span data-ttu-id="cfa18-2786">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cfa18-2786">Az.Resources</span></span>
* <span data-ttu-id="cfa18-2787">Исправлена проблема с набором параметров при предоставлении параметров "-ODataQuery" и "-ResourceId" для "Get-AzResource".</span><span class="sxs-lookup"><span data-stu-id="cfa18-2787">Fix parameter set issue when providing '-ODataQuery' and '-ResourceId' parameters for 'Get-AzResource'</span></span>
    - <span data-ttu-id="cfa18-2788">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/7875.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2788">More information here: https://github.com/Azure/azure-powershell/issues/7875</span></span>
* <span data-ttu-id="cfa18-2789">Исправлена обработка параметра -Custom в New/Set-AzPolicyDefinition.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2789">Fix handling of the -Custom parameter in New/Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="cfa18-2790">Исправлена опечатка в документации по New-AzDeployment.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2790">Fix typo in New-AzDeployment documentation</span></span>
* <span data-ttu-id="cfa18-2791">Параметр "-MailNickname" стал обязательным для "New-AzADUser".</span><span class="sxs-lookup"><span data-stu-id="cfa18-2791">Made '-MailNickname' parameter mandatory for 'New-AzADUser'</span></span>
    - <span data-ttu-id="cfa18-2792">Дополнительные сведения см. здесь: https://github.com/Azure/azure-powershell/issues/8220.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2792">More information here: https://github.com/Azure/azure-powershell/issues/8220</span></span>

#### <a name="azsignalr"></a><span data-ttu-id="cfa18-2793">Az.SignalR</span><span class="sxs-lookup"><span data-stu-id="cfa18-2793">Az.SignalR</span></span>
* <span data-ttu-id="cfa18-2794">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2794">Fix backward compatibility issue with Az.Accounts module</span></span>

#### <a name="azsql"></a><span data-ttu-id="cfa18-2795">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cfa18-2795">Az.Sql</span></span>
* <span data-ttu-id="cfa18-2796">Зависимость клиента управления хранением преобразована для общей реализации в пакете SDK.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2796">Converted the Storage management client dependency to the common SDK implementation.</span></span>

#### <a name="azstorage"></a><span data-ttu-id="cfa18-2797">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cfa18-2797">Az.Storage</span></span>
* <span data-ttu-id="cfa18-2798">Установка параметра StorageAccountName для контекста хранилища в качестве реального имени учетной записи хранения, если она была создана с использованием токена Sas, OAuth или анонимного доступа.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2798">Set the StorageAccountName of Storage context as the real Storage Account Name, when it's created with Sas Token, OAuth or Anonymous</span></span>
    - <span data-ttu-id="cfa18-2799">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="cfa18-2799">New-AzStorageContext</span></span>
* <span data-ttu-id="cfa18-2800">Создание токена Sas большого двоичного объекта моментального снимка с параметром "-FullUri". Возвращаемый URI исправлен на URI моментального снимка.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2800">Create Sas Token of Blob Snapshot Object with '-FullUri' parameter, fix the returned Uri to be the sanpshot Uri</span></span>
    - <span data-ttu-id="cfa18-2801">New-AzStorageBlobSASToken</span><span class="sxs-lookup"><span data-stu-id="cfa18-2801">New-AzStorageBlobSASToken</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cfa18-2802">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cfa18-2802">Az.Websites</span></span>
* <span data-ttu-id="cfa18-2803">Исправлена ошибка синтаксического анализа даты в "Get-AzDeletedWebApp".</span><span class="sxs-lookup"><span data-stu-id="cfa18-2803">Fixed a date parsing bug in 'Get-AzDeletedWebApp'</span></span>
* <span data-ttu-id="cfa18-2804">Устранена проблема обратной совместимости с модулем Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2804">Fix backward compatibility issue with Az.Accounts module</span></span>

## <a name="100---december-2018"></a><span data-ttu-id="cfa18-2805">1.0.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2805">1.0.0 - December 2018</span></span>
### <a name="general"></a><span data-ttu-id="cfa18-2806">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="cfa18-2806">General</span></span>

- <span data-ttu-id="cfa18-2807">Общедоступная версия модуля Az.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2807">General Availability of Az Module</span></span>
- <span data-ttu-id="cfa18-2808">Справка в Интернете для каждого модуля.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2808">Online help for each module</span></span>
- <span data-ttu-id="cfa18-2809">Дополнительные сведения и стратегию развития см. в статье [Announcing New Module 'Az'](https://aka.ms/azps-announce) (Объявление о новом модуле Az)</span><span class="sxs-lookup"><span data-stu-id="cfa18-2809">For more details and a roadmap, see the [Az Announcement page](https://aka.ms/azps-announce)</span></span>
- <span data-ttu-id="cfa18-2810">Сведения о миграции с AzureRM см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="cfa18-2810">See the [Migration Guide](https://aka.ms/azps-migration-guide) for information on migrating from AzureRM</span></span>

### <a name="azaccounts"></a><span data-ttu-id="cfa18-2811">Az.Accounts</span><span class="sxs-lookup"><span data-stu-id="cfa18-2811">Az.Accounts</span></span>
- <span data-ttu-id="cfa18-2812">Изменено с Az.Profile.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2812">Changed from Az.Profile</span></span>
- <span data-ttu-id="cfa18-2813">Исправлены форматы таблиц для типов профиля и контекста.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2813">Fixed table formats for profile and context types</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="cfa18-2814">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cfa18-2814">Az.ApiManagement</span></span>
- <span data-ttu-id="cfa18-2815">Исправления для #7002.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2815">Fixes for #7002</span></span>
- <span data-ttu-id="cfa18-2816">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="cfa18-2816">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbatch"></a><span data-ttu-id="cfa18-2817">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="cfa18-2817">Az.Batch</span></span>
- <span data-ttu-id="cfa18-2818">Добавлена возможность видеть, какая версия агента узла пакетной службы Azure работает в пуле на каждой виртуальной машине, с помощью нового свойства `NodeAgentInformation` в `PSComputeNode`.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2818">Added the ability to see what version of the Azure Batch Node Agent is running on each of the VMs in a pool, via the new `NodeAgentInformation` property on `PSComputeNode`.</span></span>
- <span data-ttu-id="cfa18-2819">Значение `Caching` по умолчанию для `PSDataDisk` теперь `ReadWrite` вместо `None`.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2819">The `Caching` default for `PSDataDisk` is now `ReadWrite` instead of `None`.</span></span>
- <span data-ttu-id="cfa18-2820">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="cfa18-2820">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azbilling"></a><span data-ttu-id="cfa18-2821">Az.Billing</span><span class="sxs-lookup"><span data-stu-id="cfa18-2821">Az.Billing</span></span>
- <span data-ttu-id="cfa18-2822">Объединены командлеты Billing, Consumption и UsageAggregates. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0).</span><span class="sxs-lookup"><span data-stu-id="cfa18-2822">Combines Billing, Consumption, and UsageAggregates cmdlets, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azcognitivservices"></a><span data-ttu-id="cfa18-2823">Az.CognitivServices</span><span class="sxs-lookup"><span data-stu-id="cfa18-2823">Az.CognitivServices</span></span>
- <span data-ttu-id="cfa18-2824">Добавлены средства заполнения для SkuName и Typem, доступные в операции New-AzureRmCognitiveServicesAccount.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2824">Add completers for SkuName and Typem available on New-AzureRmCognitiveServicesAccount operation</span></span>
- <span data-ttu-id="cfa18-2825">Удален набор параметров GetSkusWithAccountParamSetName из Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2825">Removed GetSkusWithAccountParamSetName parameter set from Get-AzCognitiveServicesAccountSkus</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="cfa18-2826">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="cfa18-2826">Az.ContainerInstance</span></span>
- <span data-ttu-id="cfa18-2827">Добавлена поддержка ManagedIdentity.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2827">Added ManagedIdentity support</span></span>

### <a name="azdatalakeanalytics"></a><span data-ttu-id="cfa18-2828">Az.DataLakeAnalytics</span><span class="sxs-lookup"><span data-stu-id="cfa18-2828">Az.DataLakeAnalytics</span></span>
- <span data-ttu-id="cfa18-2829">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="cfa18-2829">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="cfa18-2830">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cfa18-2830">Az.DataLakeStore</span></span>
- <span data-ttu-id="cfa18-2831">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="cfa18-2831">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azmonitor"></a><span data-ttu-id="cfa18-2832">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="cfa18-2832">Az.Monitor</span></span>
- <span data-ttu-id="cfa18-2833">"Az.Insights" переименован в "Az.Monitor" и внесены другие незначительные критические изменения. Дополнительные сведения см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="cfa18-2833">Renamed Az.Insights to Az.Monitor and other minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azkeyvault"></a><span data-ttu-id="cfa18-2834">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="cfa18-2834">Az.KeyVault</span></span>
- <span data-ttu-id="cfa18-2835">Из типов вывода удалено устаревшее свойство PurgeDisabled</span><span class="sxs-lookup"><span data-stu-id="cfa18-2835">Removed the deprecated 'PurgeDisabled' property from output types</span></span>

### <a name="azmachinelearning"></a><span data-ttu-id="cfa18-2836">Az.MachineLearning</span><span class="sxs-lookup"><span data-stu-id="cfa18-2836">Az.MachineLearning</span></span>
- <span data-ttu-id="cfa18-2837">Включены командлеты из модуля Az.MachineLearningCompute</span><span class="sxs-lookup"><span data-stu-id="cfa18-2837">Included cmdlets from Az.MachineLearningCompute module</span></span>

### <a name="azmedia"></a><span data-ttu-id="cfa18-2838">Az.Media</span><span class="sxs-lookup"><span data-stu-id="cfa18-2838">Az.Media</span></span>
- <span data-ttu-id="cfa18-2839">Удаляет устаревший псевдоним Tags из New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="cfa18-2839">Remove deprecated -Tags alias from New-AzMediaService</span></span>

### <a name="aznetwork"></a><span data-ttu-id="cfa18-2840">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cfa18-2840">Az.Network</span></span>
<span data-ttu-id="cfa18-2841">В шлюз приложений добавлена поддержка настройки RewriteRuleSets</span><span class="sxs-lookup"><span data-stu-id="cfa18-2841">Added support for the configuring RewriteRuleSets in the Application Gateway</span></span>
    - <span data-ttu-id="cfa18-2842">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="cfa18-2842">New cmdlets added:</span></span>
        - <span data-ttu-id="cfa18-2843">Add-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cfa18-2843">Add-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="cfa18-2844">Get-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cfa18-2844">Get-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="cfa18-2845">New-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cfa18-2845">New-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="cfa18-2846">Remove-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cfa18-2846">Remove-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="cfa18-2847">Set-AzureRmApplicationGatewayRewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cfa18-2847">Set-AzureRmApplicationGatewayRewriteRuleSet</span></span>
        - <span data-ttu-id="cfa18-2848">New-AzureRmApplicationGatewayRewriteRule</span><span class="sxs-lookup"><span data-stu-id="cfa18-2848">New-AzureRmApplicationGatewayRewriteRule</span></span>
        - <span data-ttu-id="cfa18-2849">New-AzureRmApplicationGatewayRewriteRuleActionSet</span><span class="sxs-lookup"><span data-stu-id="cfa18-2849">New-AzureRmApplicationGatewayRewriteRuleActionSet</span></span>
        - <span data-ttu-id="cfa18-2850">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span><span class="sxs-lookup"><span data-stu-id="cfa18-2850">New-AzureRmApplicationGatewayRewriteRuleHeaderConfiguration</span></span>
    - <span data-ttu-id="cfa18-2851">В следующие командлеты добавлен необязательный параметр -RewriteRuleSet</span><span class="sxs-lookup"><span data-stu-id="cfa18-2851">Cmdlets updated with optional parameter -RewriteRuleSet</span></span>
        - <span data-ttu-id="cfa18-2852">New-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cfa18-2852">New-AzureRmApplicationGateway</span></span>
        - <span data-ttu-id="cfa18-2853">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="cfa18-2853">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="cfa18-2854">Add-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="cfa18-2854">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>
        - <span data-ttu-id="cfa18-2855">New-AzureRmApplicationGatewayPathRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cfa18-2855">New-AzureRmApplicationGatewayPathRuleConfig</span></span>
        - <span data-ttu-id="cfa18-2856">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="cfa18-2856">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>
        - <span data-ttu-id="cfa18-2857">New-AzureRmApplicationGatewayUrlPathMapConfig добавил с помощью идентификатора поддержку KeyVault для шлюза приложений.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2857">New-AzureRmApplicationGatewayUrlPathMapConfig Added KeyVault Support to Application Gateway using Identity.</span></span>
    - <span data-ttu-id="cfa18-2858">В следующие командлеты добавлен необязательный параметр -KeyVaultSecretId, -KeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="cfa18-2858">Cmdlets updated with optonal parameter -KeyVaultSecretId, -KeyVaultSecret</span></span>
        - <span data-ttu-id="cfa18-2859">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="cfa18-2859">Add-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="cfa18-2860">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="cfa18-2860">New-AzApplicationGatewaySslCertificate</span></span>
        - <span data-ttu-id="cfa18-2861">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="cfa18-2861">Set-AzApplicationGatewaySslCertificate</span></span>
    - <span data-ttu-id="cfa18-2862">В командлет New-AzApplicationGateway добавлен необязательный параметр -UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="cfa18-2862">New-AzApplicationGateway cmdlet updated with optional parameter -UserAssignedIdentity</span></span>
- <span data-ttu-id="cfa18-2863">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="cfa18-2863">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azoperationalinsights"></a><span data-ttu-id="cfa18-2864">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="cfa18-2864">Az.OperationalInsights</span></span>
- <span data-ttu-id="cfa18-2865">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="cfa18-2865">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azprofile"></a><span data-ttu-id="cfa18-2866">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="cfa18-2866">Az.Profile</span></span>
- <span data-ttu-id="cfa18-2867">Имя модуля изменено на Az.Accounts.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2867">Changed module name to Az.Accounts</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="cfa18-2868">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cfa18-2868">Az.RecoveryServices</span></span>
- <span data-ttu-id="cfa18-2869">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="cfa18-2869">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azresources"></a><span data-ttu-id="cfa18-2870">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cfa18-2870">Az.Resources</span></span>
- <span data-ttu-id="cfa18-2871">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="cfa18-2871">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="cfa18-2872">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cfa18-2872">Az.ServiceFabric</span></span>
- <span data-ttu-id="cfa18-2873">Поддержка спецификации сертификата по общему имени и отпечатку</span><span class="sxs-lookup"><span data-stu-id="cfa18-2873">Support specfying certificate by common name and thumbprint</span></span>
- <span data-ttu-id="cfa18-2874">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="cfa18-2874">Mnor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azsignalr"></a><span data-ttu-id="cfa18-2875">Az.SIgnalR</span><span class="sxs-lookup"><span data-stu-id="cfa18-2875">Az.SIgnalR</span></span>
- <span data-ttu-id="cfa18-2876">Общедоступная версия командлетов PowerShell для SIgnalR</span><span class="sxs-lookup"><span data-stu-id="cfa18-2876">General Availability for PowerShell cmdlets for SIgnalR</span></span>

### <a name="azsql"></a><span data-ttu-id="cfa18-2877">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cfa18-2877">Az.Sql</span></span>
- <span data-ttu-id="cfa18-2878">Добавлены новые типы обнаружения Data_Exfiltration и Unsafe_Action в командлеты обнаружения угроз</span><span class="sxs-lookup"><span data-stu-id="cfa18-2878">Added new Data_Exfiltration and Unsafe_Action detection types to Threat Detection's cmdlets</span></span>
- <span data-ttu-id="cfa18-2879">Примеры обновленной документации для командлетов аудита Sql</span><span class="sxs-lookup"><span data-stu-id="cfa18-2879">Updated documentation examples for Sql Auditing cmdlets</span></span>
- <span data-ttu-id="cfa18-2880">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="cfa18-2880">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azstorage"></a><span data-ttu-id="cfa18-2881">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cfa18-2881">Az.Storage</span></span>
- <span data-ttu-id="cfa18-2882">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="cfa18-2882">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

### <a name="azwebsites"></a><span data-ttu-id="cfa18-2883">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cfa18-2883">Az.Websites</span></span>
- <span data-ttu-id="cfa18-2884">Дополнительные сведения о незначительных критических изменениях см. в статье [Migration Guide for Az 1.0.0](https://aka.ms/azps-migration-guide) (Руководство по миграции для Az версии 1.0.0)</span><span class="sxs-lookup"><span data-stu-id="cfa18-2884">Minor breaking changes, see the [Migration Guide](https://aka.ms/azps-migration-guide)  for details</span></span>

## <a name="070---december-2018"></a><span data-ttu-id="cfa18-2885">0.7.0 — декабрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2885">0.7.0 - December 2018</span></span>

### <a name="general"></a><span data-ttu-id="cfa18-2886">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="cfa18-2886">General</span></span>

* <span data-ttu-id="cfa18-2887">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="cfa18-2887">Minor changes for upcoming AzureRM to Az transition</span></span>

### <a name="azcompute"></a><span data-ttu-id="cfa18-2888">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cfa18-2888">Az.Compute</span></span>

* <span data-ttu-id="cfa18-2889">Добавлена поддержка UltraSSD и образов коллекции в простых наборах параметров для командлетов `New-AzVm(ss)`.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2889">Add support for UltraSSD and Gallery Images in the simple param sets for `New-AzVm(ss)` cmdlets.</span></span>

### <a name="azdatalakestore"></a><span data-ttu-id="cfa18-2890">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cfa18-2890">Az.DataLakeStore</span></span>

* <span data-ttu-id="cfa18-2891">Исправлено косую черту в конце домена учетной записи ADLS</span><span class="sxs-lookup"><span data-stu-id="cfa18-2891">Fix the trailing slash of the domain of adls account</span></span>

### <a name="azfrontdoor"></a><span data-ttu-id="cfa18-2892">Az.FrontDoor</span><span class="sxs-lookup"><span data-stu-id="cfa18-2892">Az.FrontDoor</span></span>

* <span data-ttu-id="cfa18-2893">Исправлены некоторые неработающие ссылки</span><span class="sxs-lookup"><span data-stu-id="cfa18-2893">Fixed some broken links</span></span>
    - <span data-ttu-id="cfa18-2894">В статьях New-AzureRmFrontDoor и Set-AzureRmFrontDoor исправлена ссылка на статью командлета New-AzureRmFrontDoorHealthProbeSettingObject.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2894">In the New-AzureRmFrontDoor and Set-AzureRmFrontDoor articles, fixed the link to the New-AzureRmFrontDoorHealthProbeSettingObject cmdlet article.</span></span>
    - <span data-ttu-id="cfa18-2895">В статье New-AzureRmFrontDoorManagedRuleObject исправлена ссылка на статью командлета New-AzureRmFrontDoorRuleGroupOverrideObject.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2895">In the New-AzureRmFrontDoorManagedRuleObject article, fixed the link to the New-AzureRmFrontDoorRuleGroupOverrideObject cmdlet article.</span></span>

### <a name="azrecoveryservices"></a><span data-ttu-id="cfa18-2896">Az.RecoveryServices</span><span class="sxs-lookup"><span data-stu-id="cfa18-2896">Az.RecoveryServices</span></span>

* <span data-ttu-id="cfa18-2897">Добавлены проверки на стороне клиента для операций восстановления общей папки Azure.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2897">Added client side validations for Azure File Share restore operations.</span></span>
* <span data-ttu-id="cfa18-2898">StorageAccountName и storageAccountResourceGroupName являются необязательными для восстановления afs.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2898">Made storageAccountName and storageAccountResourceGroupName optional for afs restore.</span></span>

### <a name="azresources"></a><span data-ttu-id="cfa18-2899">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cfa18-2899">Az.Resources</span></span>

* <span data-ttu-id="cfa18-2900">Исправление для https://github.com/Azure/azure-powershell/issues/7679.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2900">Fix for https://github.com/Azure/azure-powershell/issues/7679</span></span>
    - <span data-ttu-id="cfa18-2901">Обновите Get-AzureRmRoleAssignment, чтобы использовать область подписки, если она указана при запросе классических администраторов.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2901">Update Get-AzureRmRoleAssignment to use the subscription scope if it is provided when requesting classic administrators.</span></span>

### <a name="azsql"></a><span data-ttu-id="cfa18-2902">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cfa18-2902">Az.Sql</span></span>

* <span data-ttu-id="cfa18-2903">Незначительные изменения для предстоящего перехода AzureRM на Az</span><span class="sxs-lookup"><span data-stu-id="cfa18-2903">Minor changes for upcoming AzureRM to Az transition</span></span>
* <span data-ttu-id="cfa18-2904">Устранена проблема с использованием Get-AzureRmSqlDatabaseVulnerabilityAssessment с .NET Core.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2904">Fixed issue with using Get-AzureRmSqlDatabaseVulnerabilityAssessment with DotNet core</span></span>
* <span data-ttu-id="cfa18-2905">Изменена документация справочных сообщений, связанных с командлетами аудита SQL.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2905">Modified documentation of help messages related to SQL Auditing cmdlets.</span></span>

### <a name="azstorage"></a><span data-ttu-id="cfa18-2906">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="cfa18-2906">Az.Storage</span></span>

* <span data-ttu-id="cfa18-2907">Добавлено -EnableHierarchicalNamespace к New-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cfa18-2907">Add -EnableHierarchicalNamespace to New-AzureRmStorageAccount</span></span>
* <span data-ttu-id="cfa18-2908">Устранена проблема, из-за которой командлет Copy File не может повторно использовать исходный контекст в пункте назначения, если не введен -DestContext</span><span class="sxs-lookup"><span data-stu-id="cfa18-2908">Fix issue that Copy File cmdlet can't reuse source context in destination when not input -DestContext</span></span>
    - <span data-ttu-id="cfa18-2909">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="cfa18-2909">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="cfa18-2910">Поддержка статической конфигурации сайта</span><span class="sxs-lookup"><span data-stu-id="cfa18-2910">Support Static Website configuration</span></span>
    - <span data-ttu-id="cfa18-2911">Enable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="cfa18-2911">Enable-AzureStorageStaticWebsite</span></span>
    - <span data-ttu-id="cfa18-2912">Disable-AzureStorageStaticWebsite</span><span class="sxs-lookup"><span data-stu-id="cfa18-2912">Disable-AzureStorageStaticWebsite</span></span>

### <a name="azwebsites"></a><span data-ttu-id="cfa18-2913">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cfa18-2913">Az.Websites</span></span>

* <span data-ttu-id="cfa18-2914">Set-AzureRmWebApp и Set-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="cfa18-2914">Set-AzureRmWebApp and Set-AzureRmWebAppSlot</span></span>
    - <span data-ttu-id="cfa18-2915">Добавлен новый параметр (-AzureStoragePath), который указывает путь службы хранилища Azure для подключения в приложениях-контейнерах Windows и Linux.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2915">New parameter (-AzureStoragePath) added to specify Azure Storage paths to be mounted in Windows and Linux container apps.</span></span> <span data-ttu-id="cfa18-2916">Используйте выходные данные нового командлета New-AzureRmWebAppAzureStoragePath в качестве параметра, чтобы задать пути к службе хранилища Azure.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2916">Use the output of the new cmdlet New-AzureRmWebAppAzureStoragePath as a parameter to set the Azure Storage paths.</span></span>

## <a name="061---november-2018"></a><span data-ttu-id="cfa18-2917">0.6.1 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2917">0.6.1 - November 2018</span></span>

### <a name="azapimanagement"></a><span data-ttu-id="cfa18-2918">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="cfa18-2918">Az.ApiManagement</span></span>
* <span data-ttu-id="cfa18-2919">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2919">Update dependencies for type mapping issue</span></span>

### <a name="azautomation"></a><span data-ttu-id="cfa18-2920">Az.Automation</span><span class="sxs-lookup"><span data-stu-id="cfa18-2920">Az.Automation</span></span>
* <span data-ttu-id="cfa18-2921">Командлеты службы автоматизации Azure на базе Swagger.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2921">Swagger based Azure Automation cmdlets</span></span>
* <span data-ttu-id="cfa18-2922">Добавлены командлеты для Управления обновлениями.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2922">Added Update Management cmdlets</span></span>
* <span data-ttu-id="cfa18-2923">Добавлены командлеты для системы управления версиями.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2923">Added Source Control cmdlets</span></span>
* <span data-ttu-id="cfa18-2924">Добавлен командлет Remove-AzureRmAutomationHybridWorkerGroup.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2924">Added Remove-AzureRmAutomationHybridWorkerGroup cmdlet</span></span>
* <span data-ttu-id="cfa18-2925">Исправлена команда DSC для регистрации узла.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2925">Fixed the DSC Register Node command</span></span>

### <a name="azcompute"></a><span data-ttu-id="cfa18-2926">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cfa18-2926">Az.Compute</span></span>
* <span data-ttu-id="cfa18-2927">Исправлена проблема с удостоверением, назначаемым системой.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2927">Fixed identity issue for SystemAssigned identity</span></span>
* <span data-ttu-id="cfa18-2928">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2928">Update dependencies for type mapping issue</span></span>

### <a name="azcontainerinstance"></a><span data-ttu-id="cfa18-2929">Az.ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="cfa18-2929">Az.ContainerInstance</span></span>
* <span data-ttu-id="cfa18-2930">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2930">Update dependencies for type mapping issue</span></span>

### <a name="azmarketplaceordering"></a><span data-ttu-id="cfa18-2931">Az.MarketplaceOrdering</span><span class="sxs-lookup"><span data-stu-id="cfa18-2931">Az.MarketplaceOrdering</span></span>
* <span data-ttu-id="cfa18-2932">Обновлено описание в примерах командлетов для Marketplace.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2932">update the examples description for marketplace cmdlets</span></span>

### <a name="aznetwork"></a><span data-ttu-id="cfa18-2933">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cfa18-2933">Az.Network</span></span>
* <span data-ttu-id="cfa18-2934">Добавлены командлеты New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2934">Added cmdlet New-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayCustomError, Get-AzureRmApplicationGatewayCustomError, Set-AzureRmApplicationGatewayCustomError, Remove-AzureRmApplicationGatewayCustomError, Add-AzureRmApplicationGatewayHttpListenerCustomError, Get-AzureRmApplicationGatewayHttpListenerCustomError, Set-AzureRmApplicationGatewayHttpListenerCustomError, Remove-AzureRmApplicationGatewayHttpListenerCustomError</span></span>
* <span data-ttu-id="cfa18-2935">Протокол ICMP возвращен в список поддерживаемых сетевых протоколов Брандмауэра Azure.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2935">Added ICMP back to supported AzureFirewall Network Protocols</span></span>
* <span data-ttu-id="cfa18-2936">Обновлен командлет Test-AzureRmNetworkWatcherConnectivity, в который добавлена проверка идентификатора, адреса и порта целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2936">Update cmdlet Test-AzureRmNetworkWatcherConnectivity, add validation on destination id, address and port.</span></span>
* <span data-ttu-id="cfa18-2937">Исправлены проблемы с использованием памяти в карте виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2937">Fix issues with memory usage in VirtualNetwork map</span></span>

### <a name="azrecoveryservicesbackup"></a><span data-ttu-id="cfa18-2938">Az.RecoveryServices.Backup</span><span class="sxs-lookup"><span data-stu-id="cfa18-2938">Az.RecoveryServices.Backup</span></span>
* <span data-ttu-id="cfa18-2939">Внесено исправление для изменения политики, применяемой к защищенному общему файловому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2939">Fix for modifying policy for a protected file share.</span></span>
* <span data-ttu-id="cfa18-2940">Параметры часового пояса преобразованы в верхний регистр.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2940">Converted policy timezone to uppercase.</span></span>

### <a name="azrecoveryservicessiterecovery"></a><span data-ttu-id="cfa18-2941">Az.RecoveryServices.SiteRecovery</span><span class="sxs-lookup"><span data-stu-id="cfa18-2941">Az.RecoveryServices.SiteRecovery</span></span>
* <span data-ttu-id="cfa18-2942">Исправлен пример командлета New-AzureRmRecoveryServicesAsrProtectableItem.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2942">Corrected example in New-AzureRmRecoveryServicesAsrProtectableItem</span></span>
* <span data-ttu-id="cfa18-2943">Обновлены зависимости для устранения проблемы сопоставления типов.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2943">Update dependencies for type mapping issue</span></span>

### <a name="azrelay"></a><span data-ttu-id="cfa18-2944">Az.Relay</span><span class="sxs-lookup"><span data-stu-id="cfa18-2944">Az.Relay</span></span>
* <span data-ttu-id="cfa18-2945">Для командлета New-AzureRmRelayKey добавлен необязательный параметр -KeyValue, который позволяет пользователю указать значение ключа.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2945">Added optional Parameter -KeyValue to New-AzureRmRelayKey cmdlet, which enables user to provide KeyValue.</span></span>

### <a name="azresources"></a><span data-ttu-id="cfa18-2946">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cfa18-2946">Az.Resources</span></span>
* <span data-ttu-id="cfa18-2947">Обновлена справочная документация для параметров, связанных с удостоверением ресурса, в `New-AzureRmPolicyAssignment` и `Set-AzureRmPolicyAssignment`.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2947">Update help documentation for resource identity related parameters in `New-AzureRmPolicyAssignment` and `Set-AzureRmPolicyAssignment`</span></span>
* <span data-ttu-id="cfa18-2948">Добавлен пример командлета New-AzureRmPolicyDefinition, в котором используется параметр -Metadata.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2948">Add an example for New-AzureRmPolicyDefinition that uses -Metadata</span></span>
* <span data-ttu-id="cfa18-2949">Реализовано исправление, позволяющее сохранять регистр в ключах тегов NetStandard: #7678, #7703.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2949">Fix to allow case preservation in Tag keys in NetStandard: #7678 #7703</span></span>

### <a name="azservicefabric"></a><span data-ttu-id="cfa18-2950">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cfa18-2950">Az.ServiceFabric</span></span>
* <span data-ttu-id="cfa18-2951">Добавлены сообщения о нерекомендуемых компонентах для предстоящего выпуска критических изменений.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2951">Add deprecation messages for upcoming breaking changes</span></span>

### <a name="azsql"></a><span data-ttu-id="cfa18-2952">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cfa18-2952">Az.Sql</span></span>
* <span data-ttu-id="cfa18-2953">Добавлены новые командлеты для операций создания, просмотра, изменения и удаления в Управляемом экземпляре Базы данных SQL и Управляемой базе данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2953">Added new cmdlets for CRUD operations on Azure Sql Database Managed Instance and Azure Sql Managed Database</span></span>
    - <span data-ttu-id="cfa18-2954">Get-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2954">Get-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="cfa18-2955">New-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2955">New-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="cfa18-2956">Set-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2956">Set-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="cfa18-2957">Remove-AzureRmSqlInstance.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2957">Remove-AzureRmSqlInstance</span></span>
    - <span data-ttu-id="cfa18-2958">Get-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2958">Get-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="cfa18-2959">New-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2959">New-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="cfa18-2960">Restore-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2960">Restore-AzureRmSqlInstanceDatabase</span></span>
    - <span data-ttu-id="cfa18-2961">Remove-AzureRmSqlInstanceDatabase.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2961">Remove-AzureRmSqlInstanceDatabase</span></span>
* <span data-ttu-id="cfa18-2962">Добавлено расширенное управление политиками аудита для сервера или базы данных.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2962">Enabled Extended Auditing Policy management on a server or a database.</span></span>
    - <span data-ttu-id="cfa18-2963">Добавлен новый параметр (PredicateExpression) для фильтрации журналов аудита.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2963">New parameter (PredicateExpression) was added to enable filtering of audit logs.</span></span>
    - <span data-ttu-id="cfa18-2964">Внесены изменения в командлеты для использования клиентов SQL вместо устаревших клиентов.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2964">Cmdlets were modified to use SQL clients instead of Legacy clients.</span></span>
    - <span data-ttu-id="cfa18-2965">Set-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2965">Set-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="cfa18-2966">Get-AzureRmSqlServerAuditing.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2966">Get-AzureRmSqlServerAuditing.</span></span>
    - <span data-ttu-id="cfa18-2967">Set-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2967">Set-AzureRmSqlDatabaseAuditing.</span></span>
    - <span data-ttu-id="cfa18-2968">Get-AzureRmSqlDatabaseAuditing.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2968">Get-AzureRmSqlDatabaseAuditing.</span></span>
* <span data-ttu-id="cfa18-2969">Исправлена проблема с использованием командлета Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings с набором параметров, содержащим имена учетных записей хранения.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2969">Fixed issue with using Update-AzureRmSqlDatabaseVulnerabilityAssessmentSettings with storage account name parameter set</span></span>

## <a name="050---november-2018"></a><span data-ttu-id="cfa18-2970">0.5.0 — ноябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2970">0.5.0 - November 2018</span></span>
#### <a name="general"></a><span data-ttu-id="cfa18-2971">Общие сведения</span><span class="sxs-lookup"><span data-stu-id="cfa18-2971">General</span></span>
* <span data-ttu-id="cfa18-2972">Добавлены средства заполнения ресурсов для многих основных командлетов — они позволяют вам переключать существующие имена ресурсов при вызове командлетов в интерактивном режиме</span><span class="sxs-lookup"><span data-stu-id="cfa18-2972">Added Resource Completers to many core cmdlets - these alloow you to tab through existing resource names when invoking cmdlets interactively</span></span>

#### <a name="azprofile"></a><span data-ttu-id="cfa18-2973">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="cfa18-2973">Az.Profile</span></span>
* <span data-ttu-id="cfa18-2974">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2974">Update common code to use latest version of ClientRuntime</span></span>
* <span data-ttu-id="cfa18-2975">В командлете Connect-AzAccount параметр TenantId переименован в Tenant и добавлен псевдоним для TenantId</span><span class="sxs-lookup"><span data-stu-id="cfa18-2975">Rename param TenantId in cmdlet Connect-AzAccount to Tenant and add an alias for TenantId</span></span>
* <span data-ttu-id="cfa18-2976">Обновлено описание TenantId для командлета Connect-AzAccount</span><span class="sxs-lookup"><span data-stu-id="cfa18-2976">Updated TenantId description for Connect-AzAccount</span></span>
* <span data-ttu-id="cfa18-2977">Исправлено сообщение об ошибке при неудачной попытке входа в процессе предоставления домена клиента.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2977">Fix error message for failed login when providing tenant domain</span></span>
    - https://github.com/Azure/azure-powershell/issues/6936
* <span data-ttu-id="cfa18-2978">Устранена проблема с конфликтом имен контекста в учетных записях без подписок в клиенте.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2978">Fix issue with context name clashing for accounts with no subscriptions in tenant</span></span>
    - https://github.com/Azure/azure-powershell/issues/7453
* <span data-ttu-id="cfa18-2979">Устранена проблема с конечными точками DataLake при использовании MSI.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2979">Fix issue with DataLake endpoints when using MSI</span></span>
    - https://github.com/Azure/azure-powershell/issues/7462
* <span data-ttu-id="cfa18-2980">Устранена проблема, при которой командлет Disconnect-AzAccount вызывал сбой при отсутствии подключения</span><span class="sxs-lookup"><span data-stu-id="cfa18-2980">Fix issue where 'Disconnect-AzAccount' would throw if not connected</span></span>
    - https://github.com/Azure/azure-powershell/issues/7167

#### <a name="azcognitiveservices"></a><span data-ttu-id="cfa18-2981">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cfa18-2981">Az.CognitiveServices</span></span>
* <span data-ttu-id="cfa18-2982">Добавлена операция Get-AzCognitiveServicesAccountSkus.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2982">Add Get-AzCognitiveServicesAccountSkus operation.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cfa18-2983">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cfa18-2983">Az.Compute</span></span>
* <span data-ttu-id="cfa18-2984">Добавлены командлеты Add-AzVmssVMDataDisk и Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="cfa18-2984">Add Add-AzVmssVMDataDisk and Remove-AzVmssVMDataDisk cmdlets</span></span>
* <span data-ttu-id="cfa18-2985">Get-AzVMImage отображает AutomaticOSUpgradeProperties</span><span class="sxs-lookup"><span data-stu-id="cfa18-2985">Get-AzVMImage shows AutomaticOSUpgradeProperties</span></span>
* <span data-ttu-id="cfa18-2986">Устранена проблема, при которой значения параметров SetAzVMChefExtension -BootstrapOptions и -JsonAttribute нельзя было указать в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2986">Fixed SetAzVMChefExtension -BootstrapOptions and -JsonAttribute option values are not setting in json format.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cfa18-2987">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cfa18-2987">Az.DataLakeStore</span></span>
* <span data-ttu-id="cfa18-2988">Обновлен пакет DataLake до версии 1.1.10.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2988">Update the DataLake package to 1.1.10.</span></span>
* <span data-ttu-id="cfa18-2989">Параметр по умолчанию Concurrency добавлен к многопоточным операциям.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2989">Add default Concurrency to multithreaded operations.</span></span>

#### <a name="azinsights"></a><span data-ttu-id="cfa18-2990">Az.Insights</span><span class="sxs-lookup"><span data-stu-id="cfa18-2990">Az.Insights</span></span>
* <span data-ttu-id="cfa18-2991">Исправлена проблема № 7267 (область автомасштабирования).</span><span class="sxs-lookup"><span data-stu-id="cfa18-2991">Fixed issue #7267 (Autoscale area)</span></span>
    - <span data-ttu-id="cfa18-2992">Устранена проблема с созданием правила автомасштабирования, при которой перечисленные параметры не были указаны должным образом (выбор значений по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="cfa18-2992">Issues with creating a new autoscale rule not properly setting enumerated parameters (would always set them to the default value).</span></span>
* <span data-ttu-id="cfa18-2993">Исправлена проблема № 7513 [Insights], при которой для командлета Set-AzDiagnosticSetting требовалось явное указание категорий во время создания параметра</span><span class="sxs-lookup"><span data-stu-id="cfa18-2993">Fixed issue #7513 [Insights] Set-AzDiagnosticSetting requires explicit specification of categories during creation of setting</span></span>
    - <span data-ttu-id="cfa18-2994">Теперь явное указание категорий во время создания не требуется, и командлет выполняется надлежащим образом.</span><span class="sxs-lookup"><span data-stu-id="cfa18-2994">Now the cmdlet does not require explicit indication of the categories to enable during creation, i.e. it works as it is documented</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cfa18-2995">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cfa18-2995">Az.Network</span></span>
* <span data-ttu-id="cfa18-2996">Параметр PeeringType является обязательным для следующих командлетов:</span><span class="sxs-lookup"><span data-stu-id="cfa18-2996">Changed PeeringType to be a mandatory parameter for the following cmdlets:-</span></span>
    - <span data-ttu-id="cfa18-2997">Get-AzExpressRouteCircuitRouteTable</span><span class="sxs-lookup"><span data-stu-id="cfa18-2997">Get-AzExpressRouteCircuitRouteTable</span></span>
    - <span data-ttu-id="cfa18-2998">Get-AzExpressRouteCircuitARPTable</span><span class="sxs-lookup"><span data-stu-id="cfa18-2998">Get-AzExpressRouteCircuitARPTable</span></span>
    - <span data-ttu-id="cfa18-2999">Get-AzExpressRouteCircuitRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="cfa18-2999">Get-AzExpressRouteCircuitRouteTableSummary</span></span>
    - <span data-ttu-id="cfa18-3000">Get-AzExpressRouteCrossConnectionArpTable</span><span class="sxs-lookup"><span data-stu-id="cfa18-3000">Get-AzExpressRouteCrossConnectionArpTable</span></span>
    - <span data-ttu-id="cfa18-3001">Get-AzExpressRouteCrossConnectionRouteTable</span><span class="sxs-lookup"><span data-stu-id="cfa18-3001">Get-AzExpressRouteCrossConnectionRouteTable</span></span>
    - <span data-ttu-id="cfa18-3002">Get-AzExpressRouteCrossConnectionRouteTableSummary</span><span class="sxs-lookup"><span data-stu-id="cfa18-3002">Get-AzExpressRouteCrossConnectionRouteTableSummary</span></span>

#### <a name="azpolicyinsights"></a><span data-ttu-id="cfa18-3003">Az.PolicyInsights</span><span class="sxs-lookup"><span data-stu-id="cfa18-3003">Az.PolicyInsights</span></span>
* <span data-ttu-id="cfa18-3004">Добавлена политика исправления командлетов.</span><span class="sxs-lookup"><span data-stu-id="cfa18-3004">Added policy remediation cmdlets</span></span>

#### <a name="azresources"></a><span data-ttu-id="cfa18-3005">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cfa18-3005">Az.Resources</span></span>
* <span data-ttu-id="cfa18-3006">Исправление для https://github.com/Azure/azure-powershell/issues/7402.</span><span class="sxs-lookup"><span data-stu-id="cfa18-3006">Fix for https://github.com/Azure/azure-powershell/issues/7402</span></span>
    - <span data-ttu-id="cfa18-3007">Разрешено перечисление ресурсов с помощью параметра -ResourceId для командлета Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="cfa18-3007">Allow listing resources using the '-ResourceId' parameter for 'Get-AzResource'</span></span>

#### <a name="azservicebus"></a><span data-ttu-id="cfa18-3008">Az.ServiceBus</span><span class="sxs-lookup"><span data-stu-id="cfa18-3008">Az.ServiceBus</span></span>
* <span data-ttu-id="cfa18-3009">Добавлено свойство только для чтения MigrationState в PSServiceBusMigrationConfigurationAttributes, которое позволяет узнать состояние Migration.</span><span class="sxs-lookup"><span data-stu-id="cfa18-3009">Added MigrationState read-only property to PSServiceBusMigrationConfigurationAttributes which will help to know the Migration state.</span></span>

#### <a name="azservicefabric"></a><span data-ttu-id="cfa18-3010">Az.ServiceFabric</span><span class="sxs-lookup"><span data-stu-id="cfa18-3010">Az.ServiceFabric</span></span>
* <span data-ttu-id="cfa18-3011">Устранена проблема с добавлением сертификата в VMSS Linux.</span><span class="sxs-lookup"><span data-stu-id="cfa18-3011">Fix add certificate to Linux Vmss.</span></span>
* <span data-ttu-id="cfa18-3012">Исправлен командлет Add-AzServiceFabricClusterCertificate</span><span class="sxs-lookup"><span data-stu-id="cfa18-3012">Fix 'Add-AzServiceFabricClusterCertificate'</span></span>
    - <span data-ttu-id="cfa18-3013">Используется правильный отпечаток нового сертификата (Azure/service-fabric-issues#932).</span><span class="sxs-lookup"><span data-stu-id="cfa18-3013">Using correct thumbprint from new certificate (Azure/service-fabric-issues#932).</span></span>
    - <span data-ttu-id="cfa18-3014">Исключение отображается правильно (Azure/service-fabric-issues#1054).</span><span class="sxs-lookup"><span data-stu-id="cfa18-3014">Display exception correctly (Azure/service-fabric-issues#1054).</span></span>
* <span data-ttu-id="cfa18-3015">Исправлен командлет Update-AzServiceFabricDurability для обновления конфигурации кластера перед началом операции CreateOrUpdate для масштабируемого набора виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="cfa18-3015">Fix 'Update-AzServiceFabricDurability' to update cluster configuration before starting Vmss CreateOrUpdate operation.</span></span>

## <a name="040---october-2018"></a><span data-ttu-id="cfa18-3016">0.4.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="cfa18-3016">0.4.0 - October 2018</span></span>
#### <a name="azprofile"></a><span data-ttu-id="cfa18-3017">Az.Profile</span><span class="sxs-lookup"><span data-stu-id="cfa18-3017">Az.Profile</span></span>
* <span data-ttu-id="cfa18-3018">Устранена проблема с Get-AzSubscription в CloudShell</span><span class="sxs-lookup"><span data-stu-id="cfa18-3018">Fix issue with Get-AzSubscription in CloudShell</span></span>
* <span data-ttu-id="cfa18-3019">Обновлен общий код для использования последней версии ClientRuntime.</span><span class="sxs-lookup"><span data-stu-id="cfa18-3019">Update common code to use latest version of ClientRuntime</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cfa18-3020">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cfa18-3020">Az.Compute</span></span>
* <span data-ttu-id="cfa18-3021">В список разрешений добавлены новые размеры виртуальных машин, для которых будет включено ускорение работы в сети при использовании простого набора параметров для New-AzVm</span><span class="sxs-lookup"><span data-stu-id="cfa18-3021">Added new sizes to the whitelist of VM sizes for which accelerated networking will be turned on when using the simple param set for 'New-AzVm'</span></span>
* <span data-ttu-id="cfa18-3022">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="cfa18-3022">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azdatalakestore"></a><span data-ttu-id="cfa18-3023">Az.DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="cfa18-3023">Az.DataLakeStore</span></span>
* <span data-ttu-id="cfa18-3024">Добавлена поддержка правил виртуальной сети:</span><span class="sxs-lookup"><span data-stu-id="cfa18-3024">Adding support for Virtual Network Rules</span></span>
    - <span data-ttu-id="cfa18-3025">Get-AzDataLakeStoreVirtualNetworkRule: получение или отображение правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="cfa18-3025">Get-AzDataLakeStoreVirtualNetworkRule: Gets or Lists Azure Data Lake Store virtual network rule.</span></span>
    - <span data-ttu-id="cfa18-3026">Add-AzDataLakeStoreVirtualNetworkRule: добавление правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="cfa18-3026">Add-AzDataLakeStoreVirtualNetworkRule: Adds a virtual network rule to the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="cfa18-3027">Set-AzDataLakeStoreVirtualNetworkRule: изменение указанного правила виртуальной сети для указанной учетной записи Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="cfa18-3027">Set-AzDataLakeStoreVirtualNetworkRule: Modifies the specified virtual network rule in the specified Data Lake Store account.</span></span>
    - <span data-ttu-id="cfa18-3028">Remove-AzDataLakeStoreVirtualNetworkRule: удаление правила виртуальной сети Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="cfa18-3028">Remove-AzDataLakeStoreVirtualNetworkRule: Deletes an Azure Data Lake Store virtual network rule.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cfa18-3029">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cfa18-3029">Az.Network</span></span>
* <span data-ttu-id="cfa18-3030">Обновлен командлет Test-AzNetworkWatcherConnectivity. Теперь он позволяет передать значение протокола в серверную часть.</span><span class="sxs-lookup"><span data-stu-id="cfa18-3030">Update cmdlet Test-AzNetworkWatcherConnectivity, pass the protocol value to backend.</span></span>
* <span data-ttu-id="cfa18-3031">Во все командлеты добавлено средство заполнения для аргумента ResourceName.</span><span class="sxs-lookup"><span data-stu-id="cfa18-3031">Added ResourceName argument completer to all cmdlets.</span></span>

#### <a name="azresources"></a><span data-ttu-id="cfa18-3032">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cfa18-3032">Az.Resources</span></span>
* <span data-ttu-id="cfa18-3033">Устранена проблема, из-за которой командлет Get-AzRoleDefinition возвращал непонятное исключение (если профиль по умолчанию не содержал подписки и область не была указана), благодаря добавлению понятного исключения в сценарий.</span><span class="sxs-lookup"><span data-stu-id="cfa18-3033">Fix isssue where Get-AzRoleDefinition throws an unintelligible exception (when the default profile has no subscription in it and no scope is specified) by adding a meaningful exception in the scenario.</span></span> <span data-ttu-id="cfa18-3034">Также для набора параметров по умолчанию задано значение RoleDefinitionNameParameterSet.</span><span class="sxs-lookup"><span data-stu-id="cfa18-3034">Also set the default param set to 'RoleDefinitionNameParameterSet'.</span></span>

## <a name="030---october-2018"></a><span data-ttu-id="cfa18-3035">0.3.0 — октябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="cfa18-3035">0.3.0 - October 2018</span></span>
#### <a name="azurestorage"></a><span data-ttu-id="cfa18-3036">Azure.Storage;</span><span class="sxs-lookup"><span data-stu-id="cfa18-3036">Azure.Storage</span></span>
* <span data-ttu-id="cfa18-3037">Исправлена ошибка, из-за которой при копировании файла или большого двоичного объекта метаданные не копировались, если в целевом устройстве имелась проблема с метаданными.</span><span class="sxs-lookup"><span data-stu-id="cfa18-3037">Fix Copy Blob/File won't copy metadata when destination has metadata issue</span></span>
    - <span data-ttu-id="cfa18-3038">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="cfa18-3038">Start-AzureStorageBlobCopy</span></span>
    - <span data-ttu-id="cfa18-3039">Start-AzureStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="cfa18-3039">Start-AzureStorageFileCopy</span></span>
* <span data-ttu-id="cfa18-3040">Добавлена поддержка получения сведения об использовании ресурса хранилища для конкретного расположения. Также добавлено предупреждающее сообщение о том, что функция получения глобальных сведений об использовании ресурса хранилища устарела.</span><span class="sxs-lookup"><span data-stu-id="cfa18-3040">Support get the Storage resource usage of a specific location, and add warning message for get global Storage resource usage is obsolete.</span></span>
    - <span data-ttu-id="cfa18-3041">Get-AzStorageUsage</span><span class="sxs-lookup"><span data-stu-id="cfa18-3041">Get-AzStorageUsage</span></span>

#### <a name="azcognitiveservices"></a><span data-ttu-id="cfa18-3042">Az.CognitiveServices</span><span class="sxs-lookup"><span data-stu-id="cfa18-3042">Az.CognitiveServices</span></span>
* <span data-ttu-id="cfa18-3043">Поддержка Get-AzCognitiveServicesAccountSkus без существующей учетной записи.</span><span class="sxs-lookup"><span data-stu-id="cfa18-3043">Support Get-AzCognitiveServicesAccountSkus without an existing account.</span></span>

#### <a name="azcompute"></a><span data-ttu-id="cfa18-3044">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="cfa18-3044">Az.Compute</span></span>
* <span data-ttu-id="cfa18-3045">Исправлена команда Get-AzVM -ResourceGroupName <rg>, которая теперь может возвращать более 50 результатов</span><span class="sxs-lookup"><span data-stu-id="cfa18-3045">Fix Get-AzVM -ResourceGroupName <rg> to return more than 50 results if needed</span></span>
* <span data-ttu-id="cfa18-3046">Добавлен пример использования SimpleParameterSet в справку командлета New-AzVmss.</span><span class="sxs-lookup"><span data-stu-id="cfa18-3046">Added an example of the 'SimpleParameterSet' to New-AzVmss cmdlet help.</span></span>
* <span data-ttu-id="cfa18-3047">Исправлена ошибка в сообщении о ходе выполнения для шифрования дисков Azure.</span><span class="sxs-lookup"><span data-stu-id="cfa18-3047">Fixed a typo in the Azure Disk Encryption progress message</span></span>

#### <a name="azdatafactoryv2"></a><span data-ttu-id="cfa18-3048">Az.DataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="cfa18-3048">Az.DataFactoryV2</span></span>
* <span data-ttu-id="cfa18-3049">Пакет .NET SDK для ADF обновлен до версии 2.3.0.</span><span class="sxs-lookup"><span data-stu-id="cfa18-3049">Updated the ADF .Net SDK version to 2.3.0.</span></span>

#### <a name="aznetwork"></a><span data-ttu-id="cfa18-3050">Az.Network</span><span class="sxs-lookup"><span data-stu-id="cfa18-3050">Az.Network</span></span>
* <span data-ttu-id="cfa18-3051">Добавлена функциональность NetworkProfile.</span><span class="sxs-lookup"><span data-stu-id="cfa18-3051">Added NetworkProfile functionality.</span></span> <span data-ttu-id="cfa18-3052">Добавлены новые командлеты:</span><span class="sxs-lookup"><span data-stu-id="cfa18-3052">new cmdlets added</span></span>
    - <span data-ttu-id="cfa18-3053">Get-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="cfa18-3053">Get-AzNetworkProfile</span></span>
    - <span data-ttu-id="cfa18-3054">New-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="cfa18-3054">New-AzNetworkProfile</span></span>
    - <span data-ttu-id="cfa18-3055">Remove-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="cfa18-3055">Remove-AzNetworkProfile</span></span>
    - <span data-ttu-id="cfa18-3056">Set-AzNetworkProfile</span><span class="sxs-lookup"><span data-stu-id="cfa18-3056">Set-AzNetworkProfile</span></span>
    - <span data-ttu-id="cfa18-3057">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="cfa18-3057">New-AzContainerNicConfig</span></span>
    - <span data-ttu-id="cfa18-3058">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="cfa18-3058">New-AzContainerNicConfigIpConfig</span></span>
* <span data-ttu-id="cfa18-3059">Добавлен канал связи служб в модель подсети.</span><span class="sxs-lookup"><span data-stu-id="cfa18-3059">Added service association link on Subnet Model</span></span>
* <span data-ttu-id="cfa18-3060">Добавлены командлеты: New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="cfa18-3060">Added cmdlet New-AzVirtualNetworkTap, Get-AzVirtualNetworkTap, Set-AzVirtualNetworkTap, Remove-AzVirtualNetworkTap</span></span>
* <span data-ttu-id="cfa18-3061">Добавлены командлеты: Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="cfa18-3061">Added cmdlet Set-AzNEtworkInterfaceTapConfig, Get-AzNEtworkInterfaceTapConfig, Remove-AzNEtworkInterfaceTapConfig</span></span>

#### <a name="azrediscache"></a><span data-ttu-id="cfa18-3062">Az.RedisCache</span><span class="sxs-lookup"><span data-stu-id="cfa18-3062">Az.RedisCache</span></span>
* <span data-ttu-id="cfa18-3063">С этого момента добавлена поддержка любой строки в качестве параметра Size.</span><span class="sxs-lookup"><span data-stu-id="cfa18-3063">Allow any string as Size parameter going forward.</span></span> <span data-ttu-id="cfa18-3064">Добавлено значение P5 во всплывающее окно PSArgumentCompleter.</span><span class="sxs-lookup"><span data-stu-id="cfa18-3064">Add P5 in PSArgumentCompleter popup</span></span>

#### <a name="azresources"></a><span data-ttu-id="cfa18-3065">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="cfa18-3065">Az.Resources</span></span>
* <span data-ttu-id="cfa18-3066">Добавлен отсутствующий параметр -Mode в командлет Set-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="cfa18-3066">Add missing -Mode parameter to Set-AzPolicyDefinition</span></span>
* <span data-ttu-id="cfa18-3067">Исправлена ошибка командлета Get-AzProviderOperation для операций, когда Origin содержит User</span><span class="sxs-lookup"><span data-stu-id="cfa18-3067">Fix Get-AzProviderOperation commandlet bug for operations with Origin containing User</span></span>

#### <a name="azsql"></a><span data-ttu-id="cfa18-3068">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="cfa18-3068">Az.Sql</span></span>
* <span data-ttu-id="cfa18-3069">Исправлена ошибка, при которой некоторые командлеты резервного копирования не распознавали текущую подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="cfa18-3069">Fixed issue where some backup cmdlets would not recognize the current azure subscription</span></span>

#### <a name="azwebsites"></a><span data-ttu-id="cfa18-3070">Az.Websites</span><span class="sxs-lookup"><span data-stu-id="cfa18-3070">Az.Websites</span></span>
* <span data-ttu-id="cfa18-3071">Новый командлет Get-AzWebAppContainerContinuousDeploymentUrl, который позволяет получить URL-адрес веб-перехватчика для развертывания контейнера</span><span class="sxs-lookup"><span data-stu-id="cfa18-3071">New Cmdlet Get-AzWebAppContainerContinuousDeploymentUrl - Gets the Container Continuous Deployment Webhook URL</span></span>
* <span data-ttu-id="cfa18-3072">Новые командлеты New-AzWebAppContainerPSSession и Enter-WebAppContainerPSSession, которые позволяют инициировать удаленный сеанс PowerShell в приложении-контейнере Windows</span><span class="sxs-lookup"><span data-stu-id="cfa18-3072">New Cmdlets New-AzWebAppContainerPSSession and Enter-WebAppContainerPSSession  - Initiates a PowerShell remote session into a windows container app</span></span>

## <a name="020---september-2018"></a><span data-ttu-id="cfa18-3073">0.2.0 — сентябрь 2018 г.</span><span class="sxs-lookup"><span data-stu-id="cfa18-3073">0.2.0 - September 2018</span></span>
 <span data-ttu-id="cfa18-3074">Начальный выпуск</span><span class="sxs-lookup"><span data-stu-id="cfa18-3074">Initial Release</span></span>
