---
title: Руководство по переходу на Az версии 3.0.0
description: Это руководство по переходу содержит список критических изменений, внесенных в выпуск Az версии 3.0 в Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 11/04/2019
ms.openlocfilehash: 06be35bc3573d00d90a8cf2d822ac051ab72f6bb
ms.sourcegitcommit: 7839b82f47ef8dd522eff900081c22de0d089cfc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "83387672"
---
# <a name="migration-guide-for-az-300"></a><span data-ttu-id="e85f3-103">Руководство по переходу на Az версии 3.0.0</span><span class="sxs-lookup"><span data-stu-id="e85f3-103">Migration Guide for Az 3.0.0</span></span>

<span data-ttu-id="e85f3-104">В этом документе описываются изменения между Az версии 2.0.0 и Az версии 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="e85f3-104">This document describes the changes between the 2.0.0 and 3.0.0 versions of Az</span></span>

<!-- TOC -->

- [<span data-ttu-id="e85f3-105">Руководство по переходу на Az версии 3.0.0</span><span class="sxs-lookup"><span data-stu-id="e85f3-105">Migration Guide for Az 3.0.0</span></span>](#migration-guide-for-az-300)
  - [<span data-ttu-id="e85f3-106">Пакетная служба</span><span class="sxs-lookup"><span data-stu-id="e85f3-106">Batch</span></span>](#batch)
    - [`Get-AzBatchNodeAgentSku`](#get-azbatchnodeagentsku)
    - [<span data-ttu-id="e85f3-107">Несовместимость с предыдущими версиями `Az.Resources`</span><span class="sxs-lookup"><span data-stu-id="e85f3-107">Incompatibility with previous versions of `Az.Resources`</span></span>](#previous-version-incompatibility-with-azresources-module)
  - [<span data-ttu-id="e85f3-108">Среда выполнения приложений</span><span class="sxs-lookup"><span data-stu-id="e85f3-108">Compute</span></span>](#compute)
    - [`New-AzDiskConfig`](#new-azdiskconfig)
  - [<span data-ttu-id="e85f3-109">HDInsight</span><span class="sxs-lookup"><span data-stu-id="e85f3-109">HDInsight</span></span>](#hdinsight)
    - [`Get-AzHDInsightJobOutput`](#get-azhdinsightjoboutput)
    - [`Add-AzHDInsightConfigValues`](#add-azhdinsightconfigvalues)
    - [`Disable-AzHDInsightMonitoring`](#disable-azhdinsightmonitoring)
    - [`Enable-AzHDInsightMonitoring`](#enable-azhdinsightmonitoring)
    - [`Get-AzHDInsightMonitoring`](#get-azhdinsightmonitoring)
    - [`Get-AzHDInsightProperty`](#get-azhdinsightproperty)
    - [`Grant-AzHDInsightRdpServicesAccess`](#grant-azhdinsightrdpservicesaccess)
    - [`Remove-AzHDInsightCluster`](#remove-azhdinsightcluster)
    - [`Revoke-AzHDInsightRdpServicesAccess`](#revoke-azhdinsightrdpservicesaccess)
    - [`Set-AzHDInsightGatewayCredential`](#set-azhdinsightgatewaycredential)
  - [<span data-ttu-id="e85f3-110">Центр Интернета вещей</span><span class="sxs-lookup"><span data-stu-id="e85f3-110">IotHub</span></span>](#iothub)
    - [`New-AzIotHubImportDevices`](#new-aziothubimportdevices)
    - [`New-AzIotHubExportDevices`](#new-aziothubexportdevices)
    - [`Add-AzIotHubEventHubConsumerGroup`](#add-aziothubeventhubconsumergroup)
    - [`Get-AzIotHubEventHubConsumerGroup`](#get-aziothubeventhubconsumergroup)
    - [`Remove-AzIotHubEventHubConsumerGroup`](#remove-aziothubeventhubconsumergroup)
    - [`Set-AzIotHub`](#set-aziothub)
  - [<span data-ttu-id="e85f3-111">Службы восстановления</span><span class="sxs-lookup"><span data-stu-id="e85f3-111">RecoveryServices</span></span>](#recoveryservices)
    - [`Edit-AzRecoveryServicesAsrRecoveryPlan`](#edit-azrecoveryservicesasrrecoveryplan)
    - [`Get-AzRecoveryServicesAsrRecoveryPlan`](#get-azrecoveryservicesasrrecoveryplan)
    - [`New-AzRecoveryServicesAsrReplicationProtectedItem`](#new-azrecoveryservicesasrreplicationprotecteditem)
  - [<span data-ttu-id="e85f3-112">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="e85f3-112">Resources</span></span>](#resources)
    - [<span data-ttu-id="e85f3-113">Несовместимость с предыдущими версиями `Az.Batch`</span><span class="sxs-lookup"><span data-stu-id="e85f3-113">Incompatibility with previous versions of `Az.Batch`</span></span>](#previous-version-incompatibility-with-azbatch-module)
  - [<span data-ttu-id="e85f3-114">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="e85f3-114">ServiceFabric</span></span>](#servicefabric)
    - [`Add-ServiceFabricApplicationCertificate`](#add-servicefabricapplicationcertificate)
  - [<span data-ttu-id="e85f3-115">SQL</span><span class="sxs-lookup"><span data-stu-id="e85f3-115">Sql</span></span>](#sql)
    - [`Get-AzSqlDatabaseSecureConnectionPolicy`](#get-azsqldatabasesecureconnectionpolicy)
    - [`Get-AzSqlDatabaseIndexRecommendations`](#get-azsqldatabaseindexrecommendations)
    - [`Get-AzSqlDatabaseRestorePoints`](#get-azsqldatabaserestorepoints)
    - [`Get-AzSqlDatabaseAuditing`](#get-azsqldatabaseauditing)
    - [`Set-AzSqlDatabaseAuditing`](#set-azsqldatabaseauditing)
    - [`Get-AzSqlServerAuditing`](#get-azsqlserverauditing)
    - [`Set-AzSqlServerAuditing`](#set-azsqlserverauditing)
    - [`Get-AzSqlServerAdvancedThreatProtectionSettings`](#get-azsqlserveradvancedthreatprotectionsettings)
    - [`Clear-AzSqlServerAdvancedThreatProtectionSettings`](#clear-azsqlserveradvancedthreatprotectionsettings)
    - [`Update-AzSqlServerAdvancedThreatProtectionSettings`](#update-azsqlserveradvancedthreatprotectionsettings)
    - [`Get-AzSqlDatabaseAdvancedThreatProtectionSettings`](#get-azsqldatabaseadvancedthreatprotectionsettings)
    - [`Update-AzSqlDatabaseAdvancedThreatProtectionSettings`](#update-azsqldatabaseadvancedthreatprotectionsettings)
    - [`Clear-AzSqlDatabaseAdvancedThreatProtectionSettings`](#clear-azsqldatabaseadvancedthreatprotectionsettings)
    - [`Update-AzSqlDatabaseVulnerabilityAssessmentSettings`](#update-azsqldatabasevulnerabilityassessmentsettings)
    - [`Get-AzSqlDatabaseVulnerabilityAssessmentSettings`](#get-azsqldatabasevulnerabilityassessmentsettings)
    - [`Clear-AzSqlDatabaseVulnerabilityAssessmentSettings`](#clear-azsqldatabasevulnerabilityassessmentsettings)
    - [`Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`](#update-azsqlinstancedatabasevulnerabilityassessmentsettings)
    - [`Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`](#get-azsqlinstancedatabasevulnerabilityassessmentsettings)
    - [`Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`](#clear-azsqlinstancedatabasevulnerabilityassessmentsettings)
    - [`Update-AzSqlInstanceVulnerabilityAssessmentSettings`](#update-azsqlinstancevulnerabilityassessmentsettings)
    - [`Get-AzSqlInstanceVulnerabilityAssessmentSettings`](#get-azsqlinstancevulnerabilityassessmentsettings)
    - [`Clear-AzSqlInstanceVulnerabilityAssessmentSettings`](#clear-azsqlinstancevulnerabilityassessmentsettings)
    - [`Update-AzSqlServerVulnerabilityAssessmentSettings`](#update-azsqlservervulnerabilityassessmentsettings)
    - [`Get-AzSqlServerVulnerabilityAssessmentSettings`](#get-azsqlservervulnerabilityassessmentsettings)
    - [`Clear-AzSqlServerVulnerabilityAssessmentSettings`](#clear-azsqlservervulnerabilityassessmentsettings)
    - [`Get-AzSqlServerAdvancedThreatProtectionPolicy`](#get-azsqlserveradvancedthreatprotectionpolicy)
    - [`Get-AzSqlServerThreatDetectionPolicy`](#get-azsqlserverthreatdetectionpolicy)
    - [`Remove-AzSqlServerThreatDetectionPolicy`](#remove-azsqlserverthreatdetectionpolicy)
    - [`Set-AzSqlServerThreatDetectionPolicy`](#set-azsqlserverthreatdetectionpolicy)
    - [`Get-AzSqlDatabaseThreatDetectionPolicy`](#get-azsqldatabasethreatdetectionpolicy)
    - [`Set-AzSqlDatabaseThreatDetectionPolicy`](#set-azsqldatabasethreatdetectionpolicy)
    - [`Remove-AzSqlDatabaseThreatDetectionPolicy`](#remove-azsqldatabasethreatdetectionpolicy)

<!-- /TOC -->


## <a name="batch"></a><span data-ttu-id="e85f3-116">Пакетная служба Azure</span><span class="sxs-lookup"><span data-stu-id="e85f3-116">Batch</span></span>

### `Get-AzBatchNodeAgentSku`
- <span data-ttu-id="e85f3-117">Параметр `Get-AzBatchNodeAgentSku` удален и заменен на `Get-AzBatchSupportedImage`.</span><span class="sxs-lookup"><span data-stu-id="e85f3-117">Removed `Get-AzBatchNodeAgentSku` and replaced it with  `Get-AzBatchSupportedImage`.</span></span>
- <span data-ttu-id="e85f3-118">`Get-AzBatchSupportedImage` возвращает те же данные, что и `Get-AzBatchNodeAgentSku`, но в более понятном формате.</span><span class="sxs-lookup"><span data-stu-id="e85f3-118">`Get-AzBatchSupportedImage` returns the same data as `Get-AzBatchNodeAgentSku` but in a more friendly format.</span></span>
- <span data-ttu-id="e85f3-119">Также возвращаются новые непроверенные образы.</span><span class="sxs-lookup"><span data-stu-id="e85f3-119">New non-verified images are also now returned.</span></span> <span data-ttu-id="e85f3-120">Включается и дополнительная информация о `Capabilities` и `BatchSupportEndOfLife` для каждого образа.</span><span class="sxs-lookup"><span data-stu-id="e85f3-120">Additional information about `Capabilities` and `BatchSupportEndOfLife` for each image is also included.</span></span>

#### <a name="before"></a><span data-ttu-id="e85f3-121">Перед</span><span class="sxs-lookup"><span data-stu-id="e85f3-121">Before</span></span>
```powershell
$Context = Get-AzBatchAccountKeys -AccountName "ContosoBatchAccount"
Get-AzBatchNodeAgentSku -BatchContext $Context
```

#### <a name="after"></a><span data-ttu-id="e85f3-122">После</span><span class="sxs-lookup"><span data-stu-id="e85f3-122">After</span></span>
```powershell
$Context = Get-AzBatchAccountKey -AccountName "ContosoBatchAccount"
Get-AzBatchSupportedImage -BatchContext $Context
```
### <a name="previous-version-incompatibility-with-azresources-module"></a><span data-ttu-id="e85f3-123">Совместимость предыдущих версий с модулем Az.Resources</span><span class="sxs-lookup"><span data-stu-id="e85f3-123">Previous Version Incompatibility with Az.Resources Module</span></span>
<span data-ttu-id="e85f3-124">Версия 2.0.1 модуля Az.Batch несовместима с более ранними версиями (1.7.0 или более ранними) модуля Az.Resources.</span><span class="sxs-lookup"><span data-stu-id="e85f3-124">Version 2.0.1 of the ‘Az.Batch’ module is incompatible with earlier versions (version 1.7.0 or earlier) of the ‘Az.Resources’ module.</span></span>  <span data-ttu-id="e85f3-125">Из-за этого невозможно импортировать версию 1.7.0 модуля Az.Resources, если импортирована версия 2.0.1 модуля Az.Batch.</span><span class="sxs-lookup"><span data-stu-id="e85f3-125">This will result in being unable to import  version 1.7.0 of the ‘Az.Resources’ module when version 2.0.1 of the ‘Az.Batch’ module is imported.</span></span>  <span data-ttu-id="e85f3-126">Чтобы исправить эту проблему, просто обновите модуль Az.Resources до версии 1.7.1 или более поздней либо установите последнюю версию модуля Az.</span><span class="sxs-lookup"><span data-stu-id="e85f3-126">To fix this issue, simply update the ‘Az.Resources’ module to version 1.7.1 or greater, or simply install the latest version of the ‘Az’ module.</span></span>

## <a name="compute"></a><span data-ttu-id="e85f3-127">Службы вычислений</span><span class="sxs-lookup"><span data-stu-id="e85f3-127">Compute</span></span>

### `New-AzDiskConfig`
<span data-ttu-id="e85f3-128">Параметр `UploadSizeInBytes` используется вместо `DiskSizeGB` для `New-AzDiskConfig`, если для CreateOption указано Upload.</span><span class="sxs-lookup"><span data-stu-id="e85f3-128">`UploadSizeInBytes` parameter is used instead of `DiskSizeGB` for `New-AzDiskConfig` when CreateOption is Upload</span></span>

#### <a name="before"></a><span data-ttu-id="e85f3-129">Перед</span><span class="sxs-lookup"><span data-stu-id="e85f3-129">Before</span></span>
```powershell
$diskconfig = New-AzDiskConfig -Location 'Central US' -DiskSizeGB 1023 -SkuName Standard_LRS -OsType Windows -CreateOption Upload -DiskIOPSReadWrite 500 -DiskMBpsReadWrite 8
```

#### <a name="after"></a><span data-ttu-id="e85f3-130">После</span><span class="sxs-lookup"><span data-stu-id="e85f3-130">After</span></span>
```powershell
$diskconfig = New-AzDiskConfig -Location 'Central US' -UploadSizeInBytes 1023 * 1024 * 1024 * 1024 -SkuName Standard_LRS -OsType Windows -CreateOption Upload -DiskIOPSReadWrite 500 -DiskMBpsReadWrite 8
```

## <a name="hdinsight"></a><span data-ttu-id="e85f3-131">HDInsight</span><span class="sxs-lookup"><span data-stu-id="e85f3-131">HDInsight</span></span>

### `Get-AzHDInsightJobOutput`
- <span data-ttu-id="e85f3-132">Обновлен командлет `Get-AzHDInsightJobOutput` для поддержки детализированного доступа на основе ролей к ключу к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="e85f3-132">Updated the `Get-AzHDInsightJobOutput` cmdlet to support granular role-based access to the storage key.</span></span>
- <span data-ttu-id="e85f3-133">На пользователей с ролями оператора, участника или владельца кластера HDInsight это не повлияет.</span><span class="sxs-lookup"><span data-stu-id="e85f3-133">Users with HDInsight Cluster Operator, Contributor, or Owner roles will not be affected.</span></span>
- <span data-ttu-id="e85f3-134">Только пользователям с ролью читателя нужно указывать параметр `DefaultStorageAccountKey` явным образом.</span><span class="sxs-lookup"><span data-stu-id="e85f3-134">Users with only the Reader role will need to specify `DefaultStorageAccountKey` parameter explicitly.</span></span>

#### <a name="before"></a><span data-ttu-id="e85f3-135">Перед</span><span class="sxs-lookup"><span data-stu-id="e85f3-135">Before</span></span>
```powershell
Get-AzHDInsightJobOutput  -ClusterName $clusterName -JobId $jobId
```

#### <a name="after"></a><span data-ttu-id="e85f3-136">После</span><span class="sxs-lookup"><span data-stu-id="e85f3-136">After</span></span>
```powershell
Get-AzHDInsightJobOutput -ClusterName $clusterName -JobId $jobId -DefaultStorageAccountKey $storageAccountKey
```

### `Add-AzHDInsightConfigValues`
<span data-ttu-id="e85f3-137">Для командлета `Add-AzHDInsightConfigValue` удален устаревший псевдоним (ранее — `Add-AzHDInsightConfigValues`).</span><span class="sxs-lookup"><span data-stu-id="e85f3-137">Cmdlet `Add-AzHDInsightConfigValue` removed alias to `Add-AzHDInsightConfigValues`.</span></span>

#### <a name="before"></a><span data-ttu-id="e85f3-138">Перед</span><span class="sxs-lookup"><span data-stu-id="e85f3-138">Before</span></span>
<span data-ttu-id="e85f3-139">Использование устаревшего псевдонима</span><span class="sxs-lookup"><span data-stu-id="e85f3-139">Using deprecated alias</span></span>
```powershell
Add-AzHDInsightConfigValues
```

#### <a name="after"></a><span data-ttu-id="e85f3-140">После</span><span class="sxs-lookup"><span data-stu-id="e85f3-140">After</span></span>
```powershell
Add-AzHDInsightConfigValue
```


### `Disable-AzHDInsightMonitoring`
<span data-ttu-id="e85f3-141">Добавлен новый командлет `Disable-AzHDInsightMonitoring`.</span><span class="sxs-lookup"><span data-stu-id="e85f3-141">Added a new `Disable-AzHDInsightMonitoring` cmdlet.</span></span> <span data-ttu-id="e85f3-142">Используйте этот командлет, чтобы отключить мониторинг в кластере HDInsight (заменяет `Disable-AzHDInsightOperationsManagementSuite` и `Disable-AzHDInsightOMS`).</span><span class="sxs-lookup"><span data-stu-id="e85f3-142">Use this cmdlet to disable monitoring in a HDInsight cluster (replaces `Disable-AzHDInsightOperationsManagementSuite` and `Disable-AzHDInsightOMS`).</span></span>

#### <a name="before"></a><span data-ttu-id="e85f3-143">Перед</span><span class="sxs-lookup"><span data-stu-id="e85f3-143">Before</span></span>
```powershell
Disable-AzHDInsightOMS -Name testcluster
```
```powershell
Disable-AzHDInsightOperationsManagementSuite -Name testcluster
```

#### <a name="after"></a><span data-ttu-id="e85f3-144">После</span><span class="sxs-lookup"><span data-stu-id="e85f3-144">After</span></span>
```powershell
Disable-AzHDInsightMonitoring -Name testcluster
```


### `Enable-AzHDInsightMonitoring`
<span data-ttu-id="e85f3-145">Добавлен новый командлет `Enable-AzHDInsightMonitoring`.</span><span class="sxs-lookup"><span data-stu-id="e85f3-145">Added a new `Enable-AzHDInsightMonitoring` cmdlet.</span></span> <span data-ttu-id="e85f3-146">Используйте этот командлет, чтобы включить мониторинг в кластере HDInsight (заменяет `Enable-AzHDInsightOperationsManagementSuite` и `Enable-AzHDInsightOMS`).</span><span class="sxs-lookup"><span data-stu-id="e85f3-146">Use this cmdlet to enable monitoring in a HDInsight cluster (replaces `Enable-AzHDInsightOperationsManagementSuite` and `Enable-AzHDInsightOMS`).</span></span>

#### <a name="before"></a><span data-ttu-id="e85f3-147">Перед</span><span class="sxs-lookup"><span data-stu-id="e85f3-147">Before</span></span>
```powershell
Enable-AzHDInsightOMS Enable-AzHDInsightMonitoring -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>
```
```powershell
Enable-AzHDInsightOperationsManagementSuite Enable-AzHDInsightMonitoring -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>
```

#### <a name="after"></a><span data-ttu-id="e85f3-148">После</span><span class="sxs-lookup"><span data-stu-id="e85f3-148">After</span></span>
```powershell
Enable-AzHDInsightMonitoring Enable-AzHDInsightMonitoring -Name testcluster -WorkspaceId 1d364e89-bb71-4503-aa3d-a23535aea7bd -PrimaryKey <key for workspace 1d364e89-bb71-4503-aa3d-a23535aea7bd>
```

### `Get-AzHDInsightMonitoring`
<span data-ttu-id="e85f3-149">Добавлен новый командлет `Get-AzHDInsightMonitoring`.</span><span class="sxs-lookup"><span data-stu-id="e85f3-149">Added a new `Get-AzHDInsightMonitoring` cmdlet.</span></span> <span data-ttu-id="e85f3-150">Используйте этот командлет, чтобы узнать состояние установки средства мониторинга в кластере Azure HDInsight (заменяет `Get-AzHDInsightOperationsManagementSuite` и `Get-AzHDInsightOMS`).</span><span class="sxs-lookup"><span data-stu-id="e85f3-150">Use this cmdlet to get the status of monitoring installation in an Azure HDInsight cluster (replaces `Get-AzHDInsightOperationsManagementSuite` and `Get-AzHDInsightOMS`).</span></span>

#### <a name="before"></a><span data-ttu-id="e85f3-151">Перед</span><span class="sxs-lookup"><span data-stu-id="e85f3-151">Before</span></span>
```powershell
Get-AzHDInsightOMS -Name testcluster
```
```powershell
Get-AzHDInsightOperationsManagementSuite -Name testcluster
```

#### <a name="after"></a><span data-ttu-id="e85f3-152">После</span><span class="sxs-lookup"><span data-stu-id="e85f3-152">After</span></span>
```powershell
Get-AzHDInsightMonitoring -Name testcluster
```

### `Get-AzHDInsightProperty`
<span data-ttu-id="e85f3-153">Для командлета `Get-HDInsightProperty` удален устаревший псевдоним (ранее — `Get-AzHDInsightProperties`).</span><span class="sxs-lookup"><span data-stu-id="e85f3-153">Cmdlet `Get-HDInsightProperty` removed alias to `Get-AzHDInsightProperties`.</span></span>

#### <a name="before"></a><span data-ttu-id="e85f3-154">Перед</span><span class="sxs-lookup"><span data-stu-id="e85f3-154">Before</span></span>
<span data-ttu-id="e85f3-155">Использование устаревшего псевдонима</span><span class="sxs-lookup"><span data-stu-id="e85f3-155">Using deprecated alias</span></span>
```powershell
Get-AzHDInsightProperties -Location "East US 2"
```

#### <a name="after"></a><span data-ttu-id="e85f3-156">После</span><span class="sxs-lookup"><span data-stu-id="e85f3-156">After</span></span>
```powershell
Get-AzHDInsightProperty -Location "East US 2"
```

### `Grant-AzHDInsightRdpServicesAccess`
<span data-ttu-id="e85f3-157">Удалены командлеты `Grant-AzHDInsightRdpServicesAccess` и `Revoke-AzHDInsightRdpServicesAccess`.</span><span class="sxs-lookup"><span data-stu-id="e85f3-157">Removed the `Grant-AzHDInsightRdpServicesAccess` and `Revoke-AzHDInsightRdpServicesAccess` cmdlets.</span></span> <span data-ttu-id="e85f3-158">Эти командлеты больше не нужны, так как кластеры, использующие ОС Windows, не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="e85f3-158">These are no longer necessary because clusters using Windows OS type are not supported.</span></span> <span data-ttu-id="e85f3-159">Вместо этого создайте кластер с ОС Linux.</span><span class="sxs-lookup"><span data-stu-id="e85f3-159">Please create a cluster using Linux OS type instead.</span></span>

### `Remove-AzHDInsightCluster`
<span data-ttu-id="e85f3-160">Тип выходных данных `Remove-AzHDInsightCluster` изменен с `Microsoft.Azure.Management.HDInsight.Models.ClusterGetResponse` на `bool`.</span><span class="sxs-lookup"><span data-stu-id="e85f3-160">The output type of `Remove-AzHDInsightCluster` changed from `Microsoft.Azure.Management.HDInsight.Models.ClusterGetResponse` to `bool`.</span></span>

#### <a name="before"></a><span data-ttu-id="e85f3-161">Перед</span><span class="sxs-lookup"><span data-stu-id="e85f3-161">Before</span></span>
```powershell
$cluster = Remove-AzHDInsightCluster -ClusterName "your-hadoop-001"
```

#### <a name="after"></a><span data-ttu-id="e85f3-162">После</span><span class="sxs-lookup"><span data-stu-id="e85f3-162">After</span></span>
```powershell
Remove-AzHDInsightCluster -ClusterName "your-hadoop-001" -PassThru
True
```

### `Revoke-AzHDInsightRdpServicesAccess`
<span data-ttu-id="e85f3-163">Командлет считается устаревшим.</span><span class="sxs-lookup"><span data-stu-id="e85f3-163">The cmdlet is deprecated.</span></span> <span data-ttu-id="e85f3-164">Для него не существует замены.</span><span class="sxs-lookup"><span data-stu-id="e85f3-164">There is no replacement for it.</span></span>

### `Set-AzHDInsightGatewayCredential`
<span data-ttu-id="e85f3-165">Тип выходных данных `Set-AzHDInsightGatewayCredential` изменен с `HttpConnectivitySettings` на `AzureHDInsightGatewaySettings`.</span><span class="sxs-lookup"><span data-stu-id="e85f3-165">The output type of `Set-AzHDInsightGatewayCredential` changed from `HttpConnectivitySettings` to `AzureHDInsightGatewaySettings`.</span></span>



## <a name="iothub"></a><span data-ttu-id="e85f3-166">Центр Интернета вещей:</span><span class="sxs-lookup"><span data-stu-id="e85f3-166">IotHub</span></span>

### `New-AzIotHubImportDevices`
<span data-ttu-id="e85f3-167">Этот псевдоним удален. Вместо него следует использовать `New-AzIotHubImportDevice`.</span><span class="sxs-lookup"><span data-stu-id="e85f3-167">This alias is removed, please use `New-AzIotHubImportDevice` instead.</span></span>

#### <a name="before"></a><span data-ttu-id="e85f3-168">Перед</span><span class="sxs-lookup"><span data-stu-id="e85f3-168">Before</span></span>
```powershell
New-AzIotHubImportDevices -ResourceGroupName "myresourcegroup" -Name "myiothub" -InputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -OutputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D"
```

#### <a name="after"></a><span data-ttu-id="e85f3-169">После</span><span class="sxs-lookup"><span data-stu-id="e85f3-169">After</span></span>
```powershell
New-AzIotHubImportDevice -ResourceGroupName "myresourcegroup" -Name "myiothub" -InputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -OutputBlobContainerUri "https://mystorageaccount.blob.core.windows.net/?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D"
```

### `New-AzIotHubExportDevices`
<span data-ttu-id="e85f3-170">Этот псевдоним удален. Вместо него следует использовать `New-AzIotHubExportDevice`.</span><span class="sxs-lookup"><span data-stu-id="e85f3-170">This alias is removed, please use `New-AzIotHubExportDevice` instead.</span></span>

#### <a name="before"></a><span data-ttu-id="e85f3-171">Перед</span><span class="sxs-lookup"><span data-stu-id="e85f3-171">Before</span></span>
```powershell
New-AzIotHubExportDevices -ResourceGroupName "myresourcegroup" -Name "myiothub" -ExportBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -ExcludeKeys
```

#### <a name="after"></a><span data-ttu-id="e85f3-172">После</span><span class="sxs-lookup"><span data-stu-id="e85f3-172">After</span></span>
```powershell
New-AzIotHubExportDevice -ResourceGroupName "myresourcegroup" -Name "myiothub" -ExportBlobContainerUri "https://mystorageaccount.blob.core.windows.net/mystoragecontainer?sv=2015-04-05&ss=bfqt&sr=c&srt=sco&sp=rwdl&se=2016-10-27T04:01:48Z&st=2016-10-26T20:01:48Z&spr=https&sig=QqpIhHsIMF8hNuFO%3D" -ExcludeKeys
```

### `Add-AzIotHubEventHubConsumerGroup`
<span data-ttu-id="e85f3-173">Параметр `EventHubEndPointName` считается устаревшим, и для него нет замены. Это связано с тем, что для Центра Интернета вещей предусмотрена только одна встроенная конечная точка (events), на которую можно отправлять сообщения системы и устройства.</span><span class="sxs-lookup"><span data-stu-id="e85f3-173">Parameter `EventHubEndPointName` is deprecated without being replaced as IotHub comes with only one built-in endpoint("events") which could handle system and device messages.</span></span>

#### <a name="before"></a><span data-ttu-id="e85f3-174">Перед</span><span class="sxs-lookup"><span data-stu-id="e85f3-174">Before</span></span>
```powershell
Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName "myconsumergroup" -EventHubEndpointName "/EventHubEndpointName"
```

#### <a name="after"></a><span data-ttu-id="e85f3-175">После</span><span class="sxs-lookup"><span data-stu-id="e85f3-175">After</span></span>
```powershell
Add-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName "myconsumergroup"
```

### `Get-AzIotHubEventHubConsumerGroup`
<span data-ttu-id="e85f3-176">Параметр `EventHubEndPointName` считается устаревшим, и для него нет замены. Это связано с тем, что для Центра Интернета вещей предусмотрена только одна встроенная конечная точка (events), на которую можно отправлять сообщения системы и устройства.</span><span class="sxs-lookup"><span data-stu-id="e85f3-176">Parameter `EventHubEndPointName` is deprecated without being replaced as IotHub comes with only one built-in endpoint("events") which could handle system and device messages.</span></span>

#### <a name="before"></a><span data-ttu-id="e85f3-177">Перед</span><span class="sxs-lookup"><span data-stu-id="e85f3-177">Before</span></span>
```powershell
Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubEndpointName "/EventHubEndpointName"
```

#### <a name="after"></a><span data-ttu-id="e85f3-178">После</span><span class="sxs-lookup"><span data-stu-id="e85f3-178">After</span></span>
```powershell
Get-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

### `Remove-AzIotHubEventHubConsumerGroup`
<span data-ttu-id="e85f3-179">Параметр `EventHubEndPointName` считается устаревшим, и для него нет замены. Это связано с тем, что для Центра Интернета вещей предусмотрена только одна встроенная конечная точка (events), на которую можно отправлять сообщения системы и устройства.</span><span class="sxs-lookup"><span data-stu-id="e85f3-179">Parameter `EventHubEndPointName` is deprecated without being replaced as IotHub comes with only one built-in endpoint("events") which could handle system and device messages.</span></span>

#### <a name="before"></a><span data-ttu-id="e85f3-180">Перед</span><span class="sxs-lookup"><span data-stu-id="e85f3-180">Before</span></span>
```powershell
Remove-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName myconsumergroup -EventHubEndpointName "/EventHubEndpointName"
```

#### <a name="after"></a><span data-ttu-id="e85f3-181">После</span><span class="sxs-lookup"><span data-stu-id="e85f3-181">After</span></span>
```powershell
Remove-AzIotHubEventHubConsumerGroup -ResourceGroupName "myresourcegroup" -Name "myiothub" -EventHubConsumerGroupName myconsumergroup
```

### `Set-AzIotHub`
<span data-ttu-id="e85f3-182">Параметр `OperationsMonitoringProperties` является устаревшим, и для него нет замены. Это связано с тем, что для Центра Интернета вещей больше не используется встроенная конечная точка operationsMonitoringEvents.</span><span class="sxs-lookup"><span data-stu-id="e85f3-182">Parameter `OperationsMonitoringProperties` is deprecated without being replaced as IotHub is no longer using built-in endpoint("operationsMonitoringEvents").</span></span>



## <a name="recoveryservices"></a><span data-ttu-id="e85f3-183">Службы восстановления</span><span class="sxs-lookup"><span data-stu-id="e85f3-183">RecoveryServices</span></span>

### `Edit-AzRecoveryServicesAsrRecoveryPlan`
<span data-ttu-id="e85f3-184">`ASRRecoveryPlanGroup.ReplicationProtectedItems`, `ASRRecoveryPlanGroup.StartGroupActions` и `ASRRecoveryPlanGroup.EndGroupActions` удалены из выходных данных.</span><span class="sxs-lookup"><span data-stu-id="e85f3-184">`ASRRecoveryPlanGroup.ReplicationProtectedItems`, `ASRRecoveryPlanGroup.StartGroupActions` and `ASRRecoveryPlanGroup.EndGroupActions` is removed from output.</span></span>

### `Get-AzRecoveryServicesAsrRecoveryPlan`
<span data-ttu-id="e85f3-185">`ASRRecoveryPlanGroup.ReplicationProtectedItems`, `ASRRecoveryPlanGroup.StartGroupActions` и `ASRRecoveryPlanGroup.EndGroupActions` удалены из выходных данных.</span><span class="sxs-lookup"><span data-stu-id="e85f3-185">`ASRRecoveryPlanGroup.ReplicationProtectedItems`, `ASRRecoveryPlanGroup.StartGroupActions` and `ASRRecoveryPlanGroup.EndGroupActions` is removed from output.</span></span>

### `New-AzRecoveryServicesAsrReplicationProtectedItem`
<span data-ttu-id="e85f3-186">Параметр IncludeDiskId изменен для поддержки непосредственной записи на управляемый диск в Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="e85f3-186">Parameter IncludeDiskId is changed to support directly writing to a managed disk in Azure Site Recovery.</span></span>

#### <a name="before"></a><span data-ttu-id="e85f3-187">Перед</span><span class="sxs-lookup"><span data-stu-id="e85f3-187">Before</span></span>
```powershell
$job = New-AzRecoveryServicesAsrReplicationProtectedItem -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId -IncludeDiskId $includeDiskId -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId -RecoveryAzureNetworkId $RecoveryAzureNetworkId -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem -ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName -LogStorageAccountId $LogStorageAccountId
```

#### <a name="after"></a><span data-ttu-id="e85f3-188">После</span><span class="sxs-lookup"><span data-stu-id="e85f3-188">After</span></span>
```powershell
$disk1 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId -LogStorageAccountId $logStorageAccountId -DiskType $diskType
$disk2 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId2 -LogStorageAccountId $logStorageAccountId -DiskType $diskType2
$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId -RecoveryAzureNetworkId $RecoveryAzureNetworkId -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem -ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName -LogStorageAccountId $LogStorageAccountId -InMageAzureV2DiskInput $disk1,$disk2
```

## <a name="resources"></a><span data-ttu-id="e85f3-189">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="e85f3-189">Resources</span></span>

### <a name="previous-version-incompatibility-with-azbatch-module"></a><span data-ttu-id="e85f3-190">Несовместимость предыдущих версий с модулем Az.Batch</span><span class="sxs-lookup"><span data-stu-id="e85f3-190">Previous Version Incompatibility with Az.Batch Module</span></span>
<span data-ttu-id="e85f3-191">Версия 1.7.1 модуля Az.Resources несовместима с более ранними версиями (1.1.2 или ниже) модуля Az.Batch.</span><span class="sxs-lookup"><span data-stu-id="e85f3-191">Version 1.7.1 of the ‘Az.Resources’ module is incompatible with earlier versions (version 1.1.2 or earlier) of the ‘Az.Batch’ module.</span></span>  <span data-ttu-id="e85f3-192">Из-за этого невозможно импортировать версию 1.1.2 модуля Az.Batch, если импортирована версия 1.7.1 модуля Az.Resources.</span><span class="sxs-lookup"><span data-stu-id="e85f3-192">This will result in being unable to import  version 1.1.2 of the ‘Az.Batch’ module when version 1.7.1 of the ‘Az.Resources’ module is imported.</span></span>  <span data-ttu-id="e85f3-193">Чтобы исправить эту проблему, обновите модуль Az.Batch до версии 2.0.1 или более поздней либо просто установите последнюю версию модуля Az.</span><span class="sxs-lookup"><span data-stu-id="e85f3-193">To fix this issue, update the ‘Az.Batch’ module to version 2.0.1 or greater, or simply install the latest version of the ‘Az’ module.</span></span>

## <a name="servicefabric"></a><span data-ttu-id="e85f3-194">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="e85f3-194">ServiceFabric</span></span>

### `Add-ServiceFabricApplicationCertificate`
<span data-ttu-id="e85f3-195">Удален командлет `Add-ServiceFabricApplicationCertificate`, так как этот сценарий выполняется командлетом `Add-AzVmssSecret`.</span><span class="sxs-lookup"><span data-stu-id="e85f3-195">Removed `Add-ServiceFabricApplicationCertificate` as this scenario is covered by `Add-AzVmssSecret`.</span></span>

#### <a name="before"></a><span data-ttu-id="e85f3-196">Перед</span><span class="sxs-lookup"><span data-stu-id="e85f3-196">Before</span></span>
```powershell
Add-AzServiceFabricApplicationCertificate -ResourceGroupName "Group1" -Name "Contoso01SFCluster" -SecretIdentifier "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion"
```

#### <a name="after"></a><span data-ttu-id="e85f3-197">После</span><span class="sxs-lookup"><span data-stu-id="e85f3-197">After</span></span>
```powershell
$Vault = Get-AzKeyVault -VaultName "ContosoVault"
$CertConfig = New-AzVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "Certificates"
$VMSS = New-AzVmssConfig
Add-AzVmssSecret -VirtualMachineScaleSet $VMSS -SourceVaultId $Vault.ResourceId -VaultCertificate $CertConfig
```


## <a name="sql"></a><span data-ttu-id="e85f3-198">SQL</span><span class="sxs-lookup"><span data-stu-id="e85f3-198">Sql</span></span>

### `Get-AzSqlDatabaseSecureConnectionPolicy`
<span data-ttu-id="e85f3-199">Обратите внимание, что функция безопасного подключения считается устаревшей, поэтому команда удалена.</span><span class="sxs-lookup"><span data-stu-id="e85f3-199">Note that secure connection is deprecated and so command is removed.</span></span> <span data-ttu-id="e85f3-200">Чтобы просмотреть строки подключения, используйте колонку базы данных SQL на портале Azure.</span><span class="sxs-lookup"><span data-stu-id="e85f3-200">Please use the SQL database blade in the Azure portal to view the connection strings</span></span>

### `Get-AzSqlDatabaseIndexRecommendations`
<span data-ttu-id="e85f3-201">Псевдоним `Get-AzSqlDatabaseIndexRecommendations` удален.</span><span class="sxs-lookup"><span data-stu-id="e85f3-201">`Get-AzSqlDatabaseIndexRecommendations` alias is removed.</span></span> <span data-ttu-id="e85f3-202">Используйте вместо этого `Get-AzSqlDatabaseIndexRecommendation`.</span><span class="sxs-lookup"><span data-stu-id="e85f3-202">Use `Get-AzSqlDatabaseIndexRecommendation` instead.</span></span>

### `Get-AzSqlDatabaseRestorePoints`
<span data-ttu-id="e85f3-203">Псевдоним `Get-AzSqlDatabaseRestorePoints` удален.</span><span class="sxs-lookup"><span data-stu-id="e85f3-203">`Get-AzSqlDatabaseRestorePoints` alias is removed.</span></span> <span data-ttu-id="e85f3-204">Используйте вместо этого `Get-AzSqlDatabaseRestorePoint`.</span><span class="sxs-lookup"><span data-stu-id="e85f3-204">Use `Get-AzSqlDatabaseRestorePoint` instead.</span></span>

### `Get-AzSqlDatabaseAuditing`
- <span data-ttu-id="e85f3-205">Этот командлет заменен командлетом `Get-AzSqlDatabaseAudit`.</span><span class="sxs-lookup"><span data-stu-id="e85f3-205">The cmdlet `Get-AzSqlDatabaseAudit` is replacing this cmdlet.</span></span>
- <span data-ttu-id="e85f3-206">Существующий тип выходных данных Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel заменяется новым типом Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseAuditingSettingsModel и удаляются свойства `AuditState`, `StorageAccountName`</span><span class="sxs-lookup"><span data-stu-id="e85f3-206">The output type is changing from the existing type :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' to the new type :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseAuditingSettingsModel', removing properties `AuditState` and `StorageAccountName`.</span></span> <span data-ttu-id="e85f3-207">и `StorageAccountSubscriptionId`.</span><span class="sxs-lookup"><span data-stu-id="e85f3-207">and `StorageAccountSubscriptionId`.</span></span>  <span data-ttu-id="e85f3-208">Скрипты могут получать сведения об учетной записи хранения с помощью нового свойства `StorageAccountResourceId`.</span><span class="sxs-lookup"><span data-stu-id="e85f3-208">Scripts can retrieve storage account information from the new `StorageAccountResourceId` property.</span></span>

#### <a name="before"></a><span data-ttu-id="e85f3-209">Перед</span><span class="sxs-lookup"><span data-stu-id="e85f3-209">Before</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseAuditing -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName                 : database01
AuditAction                  : {}
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

#### <a name="after"></a><span data-ttu-id="e85f3-210">После</span><span class="sxs-lookup"><span data-stu-id="e85f3-210">After</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
ServerName                          : server01
DatabaseName                        : database01
AuditAction                         : {}
ResourceGroupName                   : resourcegroup01
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP,
                                       BATCH_COMPLETED_GROUP, ...}
PredicateExpression                 : statement <> 'select 1'
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
StorageKeyType                      : Primary
RetentionInDays                     : 0
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Enabled
WorkspaceResourceId                 : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### `Set-AzSqlDatabaseAuditing`
- <span data-ttu-id="e85f3-211">Этот командлет заменен командлетом `Set-AzSqlDatabaseAudit`.</span><span class="sxs-lookup"><span data-stu-id="e85f3-211">The cmdlet `Set-AzSqlDatabaseAudit` is replacing this cmdlet.</span></span>
- <span data-ttu-id="e85f3-212">Существующий тип выходных данных Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel заменяется новым типом: bool.</span><span class="sxs-lookup"><span data-stu-id="e85f3-212">The output type is changing from the existing type :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' to the new type :'bool'</span></span>

#### <a name="before"></a><span data-ttu-id="e85f3-213">Перед</span><span class="sxs-lookup"><span data-stu-id="e85f3-213">Before</span></span>
```powershell
Set-AzSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="e85f3-214">После</span><span class="sxs-lookup"><span data-stu-id="e85f3-214">After</span></span>
```powershell
Set-AzSqlDatabaseAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### `Get-AzSqlServerAuditing`
- <span data-ttu-id="e85f3-215">Этот командлет заменен командлетом `Get-AzSqlServerAudit`.</span><span class="sxs-lookup"><span data-stu-id="e85f3-215">The cmdlet `Get-AzSqlServerAudit` is replacing this cmdlet.</span></span>
- <span data-ttu-id="e85f3-216">Существующий тип выходных данных Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel заменяется новым типом Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseAuditingSettingsModel.</span><span class="sxs-lookup"><span data-stu-id="e85f3-216">The output type is changing from the existing type :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' to the new type :'Microsoft.Azure.Commands.Sql.Auditing.Model.ServerAuditingSettingsModel'.</span></span>  <span data-ttu-id="e85f3-217">Свойства `AuditState`, `StorageAccountName` и `StorageAccountSubscriptionId` удалены.</span><span class="sxs-lookup"><span data-stu-id="e85f3-217">Properties `AuditState`, `StorageAccountName`, and `StorageAccountSubscriptionId` are removed.</span></span>  <span data-ttu-id="e85f3-218">Скрипты, использующие свойство `StorageAccountName` и `StorageAccountSubscriptionId`, могут получить эту информацию с помощью нового свойства `StorageAccountResourceId`.</span><span class="sxs-lookup"><span data-stu-id="e85f3-218">Scripts that use `StorageAccountName` and `StorageAccountSubscriptionId` proeprties can retrieve this information from the new `StorageAccountResourceId` property.</span></span>

#### <a name="before"></a><span data-ttu-id="e85f3-219">Перед</span><span class="sxs-lookup"><span data-stu-id="e85f3-219">Before</span></span>
```powershell
PS C:\> Get-AzSqlServerAuditing -ResourceGroupName "resourcegroup01" -ServerName "server01"
AuditActionGroup             : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, BATCH_COMPLETED_GROUP, ...}
ResourceGroupName            : resourcegroup01
ServerName                   : server01
AuditState                   : Enabled
StorageAccountName           : mystorage
StorageKeyType               : Primary
RetentionInDays              : 0
StorageAccountSubscriptionId : 7fe3301d-31d3-4668-af5e-211a890ba6e3
PredicateExpression          : statement <> 'select 1'
```

#### <a name="after"></a><span data-ttu-id="e85f3-220">После</span><span class="sxs-lookup"><span data-stu-id="e85f3-220">After</span></span>
```powershell
PS C:\> Get-AzSqlServerAudit -ResourceGroupName "resourcegroup01" -ServerName "server01"
ServerName                          : server01
ResourceGroupName                   : resourcegroup01
AuditActionGroup                    : {SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, BATCH_COMPLETED_GROUP, ...}
PredicateExpression                 : statement <> 'select 1'
BlobStorageTargetState              : Enabled
StorageAccountResourceId            : /subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage
StorageKeyType                      : Primary
RetentionInDays                     : 0
EventHubTargetState                 : Enabled
EventHubName                        : eventHubName
EventHubAuthorizationRuleResourceId : EventHubAuthorizationRuleResourceId
LogAnalyticsTargetState             : Enabled
WorkspaceResourceId                 : "/subscriptions/4b9e8510-67ab-4e9a-95a9-e2f1e570ea9c/resourceGroups/insights-integration/providers/Microsoft.OperationalInsights/workspaces/viruela2"
```

### `Set-AzSqlServerAuditing`
- <span data-ttu-id="e85f3-221">Этот командлет заменен командлетом `Set-AzSqlServerAudit`.</span><span class="sxs-lookup"><span data-stu-id="e85f3-221">The cmdlet `Set-AzSqlServerAudit` is replacing this cmdlet.</span></span>
- <span data-ttu-id="e85f3-222">Существующий тип выходных данных Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel заменяется новым типом: bool.</span><span class="sxs-lookup"><span data-stu-id="e85f3-222">The output type is changing from the existing type :'Microsoft.Azure.Commands.Sql.Auditing.Model.DatabaseBlobAuditingSettingsModel' to the new type :'bool'</span></span>

#### <a name="before"></a><span data-ttu-id="e85f3-223">Перед</span><span class="sxs-lookup"><span data-stu-id="e85f3-223">Before</span></span>
```powershell
Set-AzSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22"
```

#### <a name="after"></a><span data-ttu-id="e85f3-224">После</span><span class="sxs-lookup"><span data-stu-id="e85f3-224">After</span></span>
```powershell
PS C:\> Set-AzSqlServerAudit -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage"
```

### `Get-AzSqlServerAdvancedThreatProtectionSettings`
<span data-ttu-id="e85f3-225">Командлет `Get-AzSqlServerAdvancedThreatProtectionSettings` заменен командлетом `Get-AzSqlServerAdvancedThreatProtectionSetting`.</span><span class="sxs-lookup"><span data-stu-id="e85f3-225">Cmdlet `Get-AzSqlServerAdvancedThreatProtectionSettings` is replaced by `Get-AzSqlServerAdvancedThreatProtectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="e85f3-226">Перед</span><span class="sxs-lookup"><span data-stu-id="e85f3-226">Before</span></span>
```powershell
Get-AzSqlServerAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

#### <a name="after"></a><span data-ttu-id="e85f3-227">После</span><span class="sxs-lookup"><span data-stu-id="e85f3-227">After</span></span>
```powershell
Get-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

### `Clear-AzSqlServerAdvancedThreatProtectionSettings`
<span data-ttu-id="e85f3-228">Командлет `Clear-AzSqlServerAdvancedThreatProtectionSettings` заменен командлетом `Clear-AzSqlServerAdvancedThreatProtectionSetting`.</span><span class="sxs-lookup"><span data-stu-id="e85f3-228">Cmdlet `Clear-AzSqlServerAdvancedThreatProtectionSettings` is replaced by `Clear-AzSqlServerAdvancedThreatProtectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="e85f3-229">Перед</span><span class="sxs-lookup"><span data-stu-id="e85f3-229">Before</span></span>
```powershell
Clear-AzSqlServerAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

#### <a name="after"></a><span data-ttu-id="e85f3-230">После</span><span class="sxs-lookup"><span data-stu-id="e85f3-230">After</span></span>
```powershell
Clear-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

### `Update-AzSqlServerAdvancedThreatProtectionSettings`
<span data-ttu-id="e85f3-231">Командлет `Update-AzSqlServerAdvancedThreatProtectionSettings` заменен командлетом `Update-AzSqlServerAdvancedThreatProtectionSetting`.</span><span class="sxs-lookup"><span data-stu-id="e85f3-231">Cmdlet `Update-AzSqlServerAdvancedThreatProtectionSettings` is replaced by `Update-AzSqlServerAdvancedThreatProtectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="e85f3-232">Перед</span><span class="sxs-lookup"><span data-stu-id="e85f3-232">Before</span></span>
```powershell
Update-AzSqlServerAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

#### <a name="after"></a><span data-ttu-id="e85f3-233">После</span><span class="sxs-lookup"><span data-stu-id="e85f3-233">After</span></span>
```powershell
Update-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

### `Get-AzSqlDatabaseAdvancedThreatProtectionSettings`
<span data-ttu-id="e85f3-234">Командлет `Get-AzSqlDatabaseAdvancedThreatProtectionSettings` заменен командлетом `Get-AzSqlDatabaseAdvancedThreatProtectionSetting`.</span><span class="sxs-lookup"><span data-stu-id="e85f3-234">Cmdlet `Get-AzSqlDatabaseAdvancedThreatProtectionSettings` is replaced by `Get-AzSqlDatabaseAdvancedThreatProtectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="e85f3-235">Перед</span><span class="sxs-lookup"><span data-stu-id="e85f3-235">Before</span></span>
```powershell
Get-AzSqlDatabaseAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="e85f3-236">После</span><span class="sxs-lookup"><span data-stu-id="e85f3-236">After</span></span>
```powershell
Get-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

### `Update-AzSqlDatabaseAdvancedThreatProtectionSettings`
<span data-ttu-id="e85f3-237">Командлет `Update-AzSqlDatabaseAdvancedThreatProtectionSettings` заменен командлетом `Update-AzSqlDatabaseAdvancedThreatProtectionSetting`.</span><span class="sxs-lookup"><span data-stu-id="e85f3-237">Cmdlet `Update-AzSqlDatabaseAdvancedThreatProtectionSettings` is repleaced by `Update-AzSqlDatabaseAdvancedThreatProtectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="e85f3-238">Перед</span><span class="sxs-lookup"><span data-stu-id="e85f3-238">Before</span></span>
```powershell
Update-AzSqlDatabaseAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

#### <a name="after"></a><span data-ttu-id="e85f3-239">После</span><span class="sxs-lookup"><span data-stu-id="e85f3-239">After</span></span>
```powershell
Update-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

### `Clear-AzSqlDatabaseAdvancedThreatProtectionSettings`
<span data-ttu-id="e85f3-240">Командлет `Clear-AzSqlDatabaseAdvancedThreatProtectionSettings` заменен командлетом `Clear-AzSqlDatabaseAdvancedThreatProtectionSetting`.</span><span class="sxs-lookup"><span data-stu-id="e85f3-240">Cmdlet `Clear-AzSqlDatabaseAdvancedThreatProtectionSettings` is repleaced by `Clear-AzSqlDatabaseAdvancedThreatProtectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="e85f3-241">Перед</span><span class="sxs-lookup"><span data-stu-id="e85f3-241">Before</span></span>
```powershell
Clear-AzSqlDatabaseAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="e85f3-242">После</span><span class="sxs-lookup"><span data-stu-id="e85f3-242">After</span></span>
```powershell
Clear-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

### `Update-AzSqlDatabaseVulnerabilityAssessmentSettings`
<span data-ttu-id="e85f3-243">Командлет `Update-AzSqlDatabaseVulnerabilityAssessmentSettings` заменен командлетом `Update-AzSqlDatabaseVulnerabilityAssessmentSetting`.</span><span class="sxs-lookup"><span data-stu-id="e85f3-243">Cmdlet `Update-AzSqlDatabaseVulnerabilityAssessmentSettings` is repleaced by `Update-AzSqlDatabaseVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="e85f3-244">Перед</span><span class="sxs-lookup"><span data-stu-id="e85f3-244">Before</span></span>
```powershell
Update-AzSqlDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01"`
    -ServerName "Server01"`
    -DatabaseName "Database01" `
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

#### <a name="after"></a><span data-ttu-id="e85f3-245">После</span><span class="sxs-lookup"><span data-stu-id="e85f3-245">After</span></span>
```powershell
Update-AzSqlDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01"`
    -ServerName "Server01"`
    -DatabaseName "Database01" `
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```


### `Get-AzSqlDatabaseVulnerabilityAssessmentSettings`
<span data-ttu-id="e85f3-246">Командлет `Get-AzSqlDatabaseVulnerabilityAssessmentSettings` заменен командлетом `Get-AzSqlDatabaseVulnerabilityAssessmentSetting`.</span><span class="sxs-lookup"><span data-stu-id="e85f3-246">Cmdlet `Get-AzSqlDatabaseVulnerabilityAssessmentSettings` is repleaced by `Get-AzSqlDatabaseVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="e85f3-247">Перед</span><span class="sxs-lookup"><span data-stu-id="e85f3-247">Before</span></span>
```powershell
Get-AzSqlDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="e85f3-248">После</span><span class="sxs-lookup"><span data-stu-id="e85f3-248">After</span></span>
```powershell
Get-AzSqlDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Clear-AzSqlDatabaseVulnerabilityAssessmentSettings`
<span data-ttu-id="e85f3-249">Командлет `Clear-AzSqlDatabaseVulnerabilityAssessmentSettings` заменен командлетом `Clear-AzSqlDatabaseVulnerabilityAssessmentSetting`.</span><span class="sxs-lookup"><span data-stu-id="e85f3-249">Cmdlet `Clear-AzSqlDatabaseVulnerabilityAssessmentSettings` is repleaced by `Clear-AzSqlDatabaseVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="e85f3-250">Перед</span><span class="sxs-lookup"><span data-stu-id="e85f3-250">Before</span></span>
```powershell
Clear-AzSqlDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="e85f3-251">После</span><span class="sxs-lookup"><span data-stu-id="e85f3-251">After</span></span>
```powershell
Clear-AzSqlDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`
<span data-ttu-id="e85f3-252">Командлет `Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` заменен командлетом `Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting`.</span><span class="sxs-lookup"><span data-stu-id="e85f3-252">Cmdlet `Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` is repleaced by `Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="e85f3-253">Перед</span><span class="sxs-lookup"><span data-stu-id="e85f3-253">Before</span></span>
```powershell
Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -InstanceName "ManagedInstance01" `
    -DatabaseName "Database01" `
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

#### <a name="after"></a><span data-ttu-id="e85f3-254">После</span><span class="sxs-lookup"><span data-stu-id="e85f3-254">After</span></span>
```powershell
Update-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -InstanceName "ManagedInstance01" `
    -DatabaseName "Database01" `
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

### `Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`
<span data-ttu-id="e85f3-255">Командлет `Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` заменен командлетом `Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting`.</span><span class="sxs-lookup"><span data-stu-id="e85f3-255">Cmdlet `Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` is repleaced by `Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="e85f3-256">Перед</span><span class="sxs-lookup"><span data-stu-id="e85f3-256">Before</span></span>
```powershell
Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="e85f3-257">После</span><span class="sxs-lookup"><span data-stu-id="e85f3-257">After</span></span>
```powershell
Get-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings`
<span data-ttu-id="e85f3-258">Командлет `Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` заменен командлетом `Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting`.</span><span class="sxs-lookup"><span data-stu-id="e85f3-258">Cmdlet `Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings` is repleaced by `Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="e85f3-259">Перед</span><span class="sxs-lookup"><span data-stu-id="e85f3-259">Before</span></span>
```powershell
Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="e85f3-260">После</span><span class="sxs-lookup"><span data-stu-id="e85f3-260">After</span></span>
```powershell
Clear-AzSqlInstanceDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Update-AzSqlInstanceVulnerabilityAssessmentSettings`
<span data-ttu-id="e85f3-261">Командлет `Update-AzSqlInstanceVulnerabilityAssessmentSettings` заменен командлетом `Update-AzSqlInstanceVulnerabilityAssessmentSetting`.</span><span class="sxs-lookup"><span data-stu-id="e85f3-261">Cmdlet `Update-AzSqlInstanceVulnerabilityAssessmentSettings` is repleaced by `Update-AzSqlInstanceVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="e85f3-262">Перед</span><span class="sxs-lookup"><span data-stu-id="e85f3-262">Before</span></span>
```powershell
Update-AzSqlInstanceVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -InstanceName "ManagedInstance01" `
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

#### <a name="after"></a><span data-ttu-id="e85f3-263">После</span><span class="sxs-lookup"><span data-stu-id="e85f3-263">After</span></span>
```powershell
Update-AzSqlInstanceVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -InstanceName "ManagedInstance01" `
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

### `Get-AzSqlInstanceVulnerabilityAssessmentSettings`
<span data-ttu-id="e85f3-264">Командлет `Get-AzSqlInstanceVulnerabilityAssessmentSettings` заменен командлетом `Get-AzSqlInstanceVulnerabilityAssessmentSetting`.</span><span class="sxs-lookup"><span data-stu-id="e85f3-264">Cmdlet `Get-AzSqlInstanceVulnerabilityAssessmentSettings` is repleaced by `Get-AzSqlInstanceVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="e85f3-265">Перед</span><span class="sxs-lookup"><span data-stu-id="e85f3-265">Before</span></span>
```powershell
Get-AzSqlInstanceVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="e85f3-266">После</span><span class="sxs-lookup"><span data-stu-id="e85f3-266">After</span></span>
```powershell
Get-AzSqlInstanceVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Clear-AzSqlInstanceVulnerabilityAssessmentSettings`
<span data-ttu-id="e85f3-267">Командлет `Clear-AzSqlInstanceVulnerabilityAssessmentSettings` заменен командлетом `Clear-AzSqlInstanceVulnerabilityAssessmentSetting`.</span><span class="sxs-lookup"><span data-stu-id="e85f3-267">Cmdlet `Clear-AzSqlInstanceVulnerabilityAssessmentSettings` is repleaced by `Clear-AzSqlInstanceVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="e85f3-268">Перед</span><span class="sxs-lookup"><span data-stu-id="e85f3-268">Before</span></span>
```powershell
Clear-AzSqlInstanceVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="e85f3-269">После</span><span class="sxs-lookup"><span data-stu-id="e85f3-269">After</span></span>
```powershell
Clear-AzSqlInstanceVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Update-AzSqlServerVulnerabilityAssessmentSettings`
<span data-ttu-id="e85f3-270">Командлет `Update-AzSqlServerVulnerabilityAssessmentSettings` заменен командлетом `Update-AzSqlServerVulnerabilityAssessmentSetting`.</span><span class="sxs-lookup"><span data-stu-id="e85f3-270">Cmdlet `Update-AzSqlServerVulnerabilityAssessmentSettings` is repleaced by `Update-AzSqlServerVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="e85f3-271">Перед</span><span class="sxs-lookup"><span data-stu-id="e85f3-271">Before</span></span>
```powershell
Update-AzSqlServerVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01"`
    -ServerName "Server01"`
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

#### <a name="after"></a><span data-ttu-id="e85f3-272">После</span><span class="sxs-lookup"><span data-stu-id="e85f3-272">After</span></span>
```powershell
Update-AzSqlServerVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01"`
    -ServerName "Server01"`
    -StorageAccountName "mystorage" `
    -ScanResultsContainerName "vulnerability-assessment" `
    -RecurringScansInterval Weekly `
    -EmailSubscriptionAdmins $true `
    -NotificationEmail @("mail1@mail.com" , "mail2@mail.com")
```

### `Get-AzSqlServerVulnerabilityAssessmentSettings`
<span data-ttu-id="e85f3-273">Командлет `Get-AzSqlServerVulnerabilityAssessmentSettings` заменен командлетом `Get-AzSqlServerVulnerabilityAssessmentSetting`.</span><span class="sxs-lookup"><span data-stu-id="e85f3-273">Cmdlet `Get-AzSqlServerVulnerabilityAssessmentSettings` is repleaced by `Get-AzSqlServerVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="e85f3-274">Перед</span><span class="sxs-lookup"><span data-stu-id="e85f3-274">Before</span></span>
```powershell
Get-AzSqlServerVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="e85f3-275">После</span><span class="sxs-lookup"><span data-stu-id="e85f3-275">After</span></span>
```powershell
Get-AzSqlServerVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Clear-AzSqlServerVulnerabilityAssessmentSettings`
<span data-ttu-id="e85f3-276">Командлет `Clear-AzSqlServerVulnerabilityAssessmentSettings` заменен командлетом `Clear-AzSqlServerVulnerabilityAssessmentSetting`.</span><span class="sxs-lookup"><span data-stu-id="e85f3-276">Cmdlet `Clear-AzSqlServerVulnerabilityAssessmentSettings` is repleaced by `Clear-AzSqlServerVulnerabilityAssessmentSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="e85f3-277">Перед</span><span class="sxs-lookup"><span data-stu-id="e85f3-277">Before</span></span>
```powershell
Clear-AzSqlServerVulnerabilityAssessmentSettings `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="e85f3-278">После</span><span class="sxs-lookup"><span data-stu-id="e85f3-278">After</span></span>
```powershell
Clear-AzSqlDatabaseVulnerabilityAssessmentSetting `
    -ResourceGroupName "ResourceGroup01" `
    -ServerName "Server01" `
    -DatabaseName "Database01"
```

### `Get-AzSqlServerAdvancedThreatProtectionPolicy`
<span data-ttu-id="e85f3-279">Командлет `Get-AzSqlServerAdvancedThreatProtectionPolicy` удален. Для него нет замены.</span><span class="sxs-lookup"><span data-stu-id="e85f3-279">Cmdlet `Get-AzSqlServerAdvancedThreatProtectionPolicy` is deleted and no cmdlet is repleaced it</span></span>

### `Get-AzSqlServerThreatDetectionPolicy`
<span data-ttu-id="e85f3-280">Командлет `Get-AzSqlServerThreatDetectionPolicy` заменен командлетом `Get-AzSqlServerThreatDetectionSetting`.</span><span class="sxs-lookup"><span data-stu-id="e85f3-280">Cmdlet `Get-AzSqlServerThreatDetectionPolicy` is repleaced by `Get-AzSqlServerThreatDetectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="e85f3-281">Перед</span><span class="sxs-lookup"><span data-stu-id="e85f3-281">Before</span></span>
```powershell
PS C:\> Get-AzSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

#### <a name="after"></a><span data-ttu-id="e85f3-282">После</span><span class="sxs-lookup"><span data-stu-id="e85f3-282">After</span></span>
```powershell
PS C:\> Get-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

### `Remove-AzSqlServerThreatDetectionPolicy`
<span data-ttu-id="e85f3-283">Командлет `Remove-AzSqlServerThreatDetectionPolicy` заменен командлетом `Clear-AzSqlServerThreatDetectionSetting`.</span><span class="sxs-lookup"><span data-stu-id="e85f3-283">Cmdlet `Remove-AzSqlServerThreatDetectionPolicy` is repleaced by `Clear-AzSqlServerThreatDetectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="e85f3-284">Перед</span><span class="sxs-lookup"><span data-stu-id="e85f3-284">Before</span></span>
```powershell
Remove-AzSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

#### <a name="after"></a><span data-ttu-id="e85f3-285">После</span><span class="sxs-lookup"><span data-stu-id="e85f3-285">After</span></span>
```powershell
Clear-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"
```

### `Set-AzSqlServerThreatDetectionPolicy`
<span data-ttu-id="e85f3-286">Командлет `Set-AzSqlServerThreatDetectionPolicy` заменен командлетом `Update-AzSqlServerThreatDetectionSetting`.</span><span class="sxs-lookup"><span data-stu-id="e85f3-286">Cmdlet `Set-AzSqlServerThreatDetectionPolicy` is repleaced by `Update-AzSqlServerThreatDetectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="e85f3-287">Перед</span><span class="sxs-lookup"><span data-stu-id="e85f3-287">Before</span></span>
```powershell
Set-AzSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

#### <a name="after"></a><span data-ttu-id="e85f3-288">После</span><span class="sxs-lookup"><span data-stu-id="e85f3-288">After</span></span>
```powershell
Update-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

### `Get-AzSqlDatabaseThreatDetectionPolicy`
<span data-ttu-id="e85f3-289">Командлет `Get-AzSqlDatabaseThreatDetectionPolicy` заменен командлетом `Get-AzSqlDatabaseThreatDetectionSetting`.</span><span class="sxs-lookup"><span data-stu-id="e85f3-289">Cmdlet `Get-AzSqlDatabaseThreatDetectionPolicy` is repleaced by `Get-AzSqlDatabaseThreatDetectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="e85f3-290">Перед</span><span class="sxs-lookup"><span data-stu-id="e85f3-290">Before</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName   "Database01"
DatabaseName                 : Database01
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

#### <a name="after"></a><span data-ttu-id="e85f3-291">После</span><span class="sxs-lookup"><span data-stu-id="e85f3-291">After</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01"   -DatabaseName "Database01"
DatabaseName                 : Database01
ResourceGroupName            : ResourceGroup11
ServerName                   : Server01
ThreatDetectionState         : Enabled
NotificationRecipientsEmails : admin@myCompany.com
StorageAccountName           : mystorage
EmailAdmins                  : True
ExcludedDetectionTypes       : {}
RetentionInDays              : 0
```

### `Set-AzSqlDatabaseThreatDetectionPolicy`
<span data-ttu-id="e85f3-292">Командлет `Set-AzSqlDatabaseThreatDetectionPolicy` заменен командлетом `Update-AzSqlDatabaseThreatDetectionSetting`.</span><span class="sxs-lookup"><span data-stu-id="e85f3-292">Cmdlet `Set-AzSqlDatabaseThreatDetectionPolicy` is repleaced by `Update-AzSqlDatabaseThreatDetectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="e85f3-293">Перед</span><span class="sxs-lookup"><span data-stu-id="e85f3-293">Before</span></span>
```powershell
Set-AzSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

#### <a name="after"></a><span data-ttu-id="e85f3-294">После</span><span class="sxs-lookup"><span data-stu-id="e85f3-294">After</span></span>
```powershell
Update-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

### `Remove-AzSqlDatabaseThreatDetectionPolicy`
<span data-ttu-id="e85f3-295">Командлет `Remove-AzSqlDatabaseThreatDetectionPolicy` заменен командлетом `Clear-AzSqlDatabaseThreatDetectionSetting`.</span><span class="sxs-lookup"><span data-stu-id="e85f3-295">Cmdlet `Remove-AzSqlDatabaseThreatDetectionPolicy` is repleaced by `Clear-AzSqlDatabaseThreatDetectionSetting`</span></span>

#### <a name="before"></a><span data-ttu-id="e85f3-296">Перед</span><span class="sxs-lookup"><span data-stu-id="e85f3-296">Before</span></span>
```powershell
Remove-AzSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```

#### <a name="after"></a><span data-ttu-id="e85f3-297">После</span><span class="sxs-lookup"><span data-stu-id="e85f3-297">After</span></span>
```powershell
Clear-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01"
```
