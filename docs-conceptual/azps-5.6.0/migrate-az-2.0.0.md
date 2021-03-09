---
title: Руководство по переходу на Az версии 2.0.0
description: Это руководство по переходу содержит список критических изменений, внесенных в выпуск Az версии 2.0 в Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/24/2019
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: d6dac1514fffa140f6d785be9a1a0e8be58476eb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101872488"
---
# <a name="migration-guide-for-az-200"></a><span data-ttu-id="99ec1-103">Руководство по переходу на Az версии 2.0.0</span><span class="sxs-lookup"><span data-stu-id="99ec1-103">Migration Guide for Az 2.0.0</span></span>

<span data-ttu-id="99ec1-104">Этот документ описывает изменения между Az версии 1.0.0 и Az версии 2.0.0.</span><span class="sxs-lookup"><span data-stu-id="99ec1-104">This document describes the changes between the 1.0.0 and 2.0.0 versions of Az</span></span> 

## <a name="table-of-contents"></a><span data-ttu-id="99ec1-105">Оглавление</span><span class="sxs-lookup"><span data-stu-id="99ec1-105">Table of Contents</span></span>
- [<span data-ttu-id="99ec1-106">Критические изменения модуля</span><span class="sxs-lookup"><span data-stu-id="99ec1-106">Module breaking changes</span></span>](#module-breaking-changes)
  - [<span data-ttu-id="99ec1-107">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="99ec1-107">Az.Compute</span></span>](#azcompute)
  - [<span data-ttu-id="99ec1-108">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="99ec1-108">Az.HDInsight</span></span>](#azhdinsight)
  - [<span data-ttu-id="99ec1-109">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="99ec1-109">Az.Storage</span></span>](#azstorage)

## <a name="module-breaking-changes"></a><span data-ttu-id="99ec1-110">Критические изменения модуля</span><span class="sxs-lookup"><span data-stu-id="99ec1-110">Module breaking changes</span></span>

### <a name="azcompute"></a><span data-ttu-id="99ec1-111">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="99ec1-111">Az.Compute</span></span>

- <span data-ttu-id="99ec1-112">Параметр `Managed` удален из командлетов `New-AzAvailabilitySet` и `Update-AzAvailabilitySet`. Теперь используется ```Sku = Aligned```.</span><span class="sxs-lookup"><span data-stu-id="99ec1-112">Removed `Managed` Parameter from `New-AzAvailabilitySet` and `Update-AzAvailabilitySet` cmdlets in favor of using ```Sku = Aligned```</span></span>

  #### <a name="before"></a><span data-ttu-id="99ec1-113">До</span><span class="sxs-lookup"><span data-stu-id="99ec1-113">Before</span></span>

  ```powershell
  Update-AzAvailabilitySet -Managed
  ```

  #### <a name="after"></a><span data-ttu-id="99ec1-114">После</span><span class="sxs-lookup"><span data-stu-id="99ec1-114">After</span></span>

  ```powershell
  Update-AzAvailabilitySet -Sku Aligned
  ```
- <span data-ttu-id="99ec1-115">Для согласованности параметр `Image` удален из наборов параметров ByName и ByResourceId в `Update-AzImage`.</span><span class="sxs-lookup"><span data-stu-id="99ec1-115">For consistency, removed `Image` parameter from 'ByName' and 'ByResourceId' parameter sets in `Update-AzImage`</span></span> 
  
  #### <a name="before"></a><span data-ttu-id="99ec1-116">До</span><span class="sxs-lookup"><span data-stu-id="99ec1-116">Before</span></span>

  <span data-ttu-id="99ec1-117">Обратите внимание, что приведенный ниже код работает, но переданный параметр ImageName не используется, поэтому удаление этого параметра не влияет на функциональность.</span><span class="sxs-lookup"><span data-stu-id="99ec1-117">Note that the below code is functional, but the passed-in ImageName is not used, so removing this parameter has no functional impact.</span></span>

  ```powershell
  Update-AzImage -ResourceGroupName $Rg -ImageName $Name -Image $Image -Tag $tags

  Update-AzImage -ResourceId $Id -Image $Image -Tag $tags
  ```

  #### <a name="after"></a><span data-ttu-id="99ec1-118">После</span><span class="sxs-lookup"><span data-stu-id="99ec1-118">After</span></span>

  ```powershell
  Update-AzImage -ResourceGroupName $Rg -ImageName $Name -Tag $tags

  Update-AzImage -ResourceId $Id -Tag $tags
  ```

- <span data-ttu-id="99ec1-119">Для согласованности параметр `Name` удален из наборов параметров ByObject и ByResourceId в `Restart-AzVM`.</span><span class="sxs-lookup"><span data-stu-id="99ec1-119">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Restart-AzVM`</span></span>
  
  #### <a name="before"></a><span data-ttu-id="99ec1-120">До</span><span class="sxs-lookup"><span data-stu-id="99ec1-120">Before</span></span>

  <span data-ttu-id="99ec1-121">Обратите внимание, что приведенный ниже код работает, но переданный параметр Name не используется, поэтому удаление этого параметра не влияет на функциональность.</span><span class="sxs-lookup"><span data-stu-id="99ec1-121">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>
  ```powershell
  Restart-AzVM -InputObject $VM -Name $Name 

  Restart-AzVM -ResourceId $Id -Name $Name
  ```

  #### <a name="after"></a><span data-ttu-id="99ec1-122">После</span><span class="sxs-lookup"><span data-stu-id="99ec1-122">After</span></span>

  ```powershell
  Restart-AzVM -InputObject $VM

  Restart-AzVM -ResourceId $Id
  ```

- <span data-ttu-id="99ec1-123">Для согласованности параметр `Name` удален из наборов параметров ByObject и ByResourceId в `Start-AzVM`.</span><span class="sxs-lookup"><span data-stu-id="99ec1-123">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Start-AzVM`</span></span>
  
  #### <a name="before"></a><span data-ttu-id="99ec1-124">До</span><span class="sxs-lookup"><span data-stu-id="99ec1-124">Before</span></span>

  <span data-ttu-id="99ec1-125">Обратите внимание, что приведенный ниже код работает, но переданный параметр Name не используется, поэтому удаление этого параметра не влияет на функциональность.</span><span class="sxs-lookup"><span data-stu-id="99ec1-125">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>

  ```powershell
  Start-AzVM -InputObject $VM -Name $Name 

  Start-AzVM -ResourceId $Id -Name $Name
  ```

  #### <a name="after"></a><span data-ttu-id="99ec1-126">После</span><span class="sxs-lookup"><span data-stu-id="99ec1-126">After</span></span>

  ```powershell
  Start-AzVM -InputObject $VM

  Start-AzVM -ResourceId $Id
  ```

- <span data-ttu-id="99ec1-127">Для согласованности параметр `Name` удален из наборов параметров ByObject и ByResourceId в `Stop-AzVM`.</span><span class="sxs-lookup"><span data-stu-id="99ec1-127">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Stop-AzVM`</span></span>
  
  #### <a name="before"></a><span data-ttu-id="99ec1-128">До</span><span class="sxs-lookup"><span data-stu-id="99ec1-128">Before</span></span>

  <span data-ttu-id="99ec1-129">Обратите внимание, что приведенный ниже код работает, но переданный параметр Name не используется, поэтому удаление этого параметра не влияет на функциональность.</span><span class="sxs-lookup"><span data-stu-id="99ec1-129">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>

  ```powershell
  Stop-AzVM -InputObject $VM -Name $Name 

  Stop-AzVM -ResourceId $Id -Name $Name
  ```

  #### <a name="after"></a><span data-ttu-id="99ec1-130">После</span><span class="sxs-lookup"><span data-stu-id="99ec1-130">After</span></span>

  ```powershell
  Stop-AzVM -InputObject $VM

  Stop-AzVM -ResourceId $Id
  ```

- <span data-ttu-id="99ec1-131">Для согласованности параметр `Name` удален из наборов параметров ByObject и ByResourceId в `Remove-AzVM`.</span><span class="sxs-lookup"><span data-stu-id="99ec1-131">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Remove-AzVM`</span></span>
  
  #### <a name="before"></a><span data-ttu-id="99ec1-132">До</span><span class="sxs-lookup"><span data-stu-id="99ec1-132">Before</span></span>

  <span data-ttu-id="99ec1-133">Обратите внимание, что приведенный ниже код работает, но переданный параметр Name не используется, поэтому удаление этого параметра не влияет на функциональность.</span><span class="sxs-lookup"><span data-stu-id="99ec1-133">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>

  ```powershell
  Remove-AzVM -InputObject $VM -Name $Name

  Remove-AzVM -ResourceId $Id -Name $Name 
  ```

  #### <a name="after"></a><span data-ttu-id="99ec1-134">После</span><span class="sxs-lookup"><span data-stu-id="99ec1-134">After</span></span>

  ```powershell
  Remove-AzVM -InputObject $VM 

  Remove-AzVM -ResourceId $Id 
  ```

- <span data-ttu-id="99ec1-135">Для согласованности параметр `Name` удален из наборов параметров ByObject и ByResourceId в `Set-AzVM`.</span><span class="sxs-lookup"><span data-stu-id="99ec1-135">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Set-AzVM`</span></span>
  
  #### <a name="before"></a><span data-ttu-id="99ec1-136">До</span><span class="sxs-lookup"><span data-stu-id="99ec1-136">Before</span></span>

  <span data-ttu-id="99ec1-137">Обратите внимание, что приведенный ниже код работает, но переданный параметр Name не используется, поэтому удаление этого параметра не влияет на функциональность.</span><span class="sxs-lookup"><span data-stu-id="99ec1-137">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>

  ```powershell
  Set-AzVM -InputObject $VM -Name $Name ...

  Set-AzVM -ResourceId $Id -Name $Name ...
  ```

  #### <a name="after"></a><span data-ttu-id="99ec1-138">После</span><span class="sxs-lookup"><span data-stu-id="99ec1-138">After</span></span>

  ```powershell
  Set-AzVM -InputObject $VM ...

  Set-AzVM -ResourceId $Id ...
  ```

- <span data-ttu-id="99ec1-139">Для согласованности параметр `Name` удален из наборов параметров ByObject и ByResourceId в `Save-AzVMImage`.</span><span class="sxs-lookup"><span data-stu-id="99ec1-139">For consistency, removed `Name` parameter from 'ByObject' and 'ByResourceId' parameter sets in `Save-AzVMImage`</span></span> 
  
  #### <a name="before"></a><span data-ttu-id="99ec1-140">До</span><span class="sxs-lookup"><span data-stu-id="99ec1-140">Before</span></span>
  <span data-ttu-id="99ec1-141">Обратите внимание, что приведенный ниже код работает, но переданный параметр Name не используется, поэтому удаление этого параметра не влияет на функциональность.</span><span class="sxs-lookup"><span data-stu-id="99ec1-141">Note that the below code is functional, but the passed-in Name is not used, so removing this parameter has no functional impact.</span></span>
  ```powershell
  Save-AzVMImage -InputObject $VM -Name $Name ...

  Save-AzVMImage -ResourceId $Id -Name $Name ...
  ```
  #### <a name="after"></a><span data-ttu-id="99ec1-142">После</span><span class="sxs-lookup"><span data-stu-id="99ec1-142">After</span></span>
  ```powershell
  Save-AzVMImage -InputObject $VM ...

  Save-AzVMImage -ResourceId $Id ...
  ```

- <span data-ttu-id="99ec1-143">Добавлено свойство ProtectionPolicy для инкапсуляции свойства `ProtectFromScaleIn` в классе `PSVirtualMachineScaleSetVM`.</span><span class="sxs-lookup"><span data-stu-id="99ec1-143">Added ProtectionPolicy property to encapsulate `ProtectFromScaleIn` property in `PSVirtualMachineScaleSetVM`</span></span>

  #### <a name="before"></a><span data-ttu-id="99ec1-144">До</span><span class="sxs-lookup"><span data-stu-id="99ec1-144">Before</span></span>

  ```powershell
  $vmss = Get-AzVMssVM ...
  $vmss.ProtectFromScaleIn = $true

  $vmss = Update-AzVMssVM ...
  $vmss.ProtectFromScaleIn = $true

  $vmss = Remove-AzVMssVMDataDisk ...
  $vmss.ProtectFromScaleIn = $true
  ```

  #### <a name="after"></a><span data-ttu-id="99ec1-145">После</span><span class="sxs-lookup"><span data-stu-id="99ec1-145">After</span></span>

  ```powershell
  $vmss = Get-AzVMssVM ...
  $vmss.ProtectionPolicy.ProtectFromScaleIn = $true

  $vmss = Update-AzVMssVM ...
  $vmss.ProtectionPolicy.ProtectFromScaleIn = $true

  $vmss = Remove-AzVMssVMDataDisk ...
  $vmss.ProtectionPolicy.ProtectFromScaleIn = $true

  ```

- <span data-ttu-id="99ec1-146">Добавлено свойство ```EncryptionSettingsCollection``` для заключения свойства `EncryptionSettings` в классе `PSDisk`.</span><span class="sxs-lookup"><span data-stu-id="99ec1-146">Added ```EncryptionSettingsCollection``` Property to enclose `EncryptionSettings` property in `PSDisk`</span></span>

  #### <a name="before"></a><span data-ttu-id="99ec1-147">До</span><span class="sxs-lookup"><span data-stu-id="99ec1-147">Before</span></span>

  ```powershell
  $disk = New-AzDisk ... | Set-AzDiskDiskEncrytionKey ...
  $disk.EncryptionSettings

  $disk = New-AzDisk ... | Set-AzDiskKeyEncrytionKey ...
  $disk.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateDiskEncryptionKey ...
  $update.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateKeyEncryptionKey ...
  $update.EncryptionSettings
  ```

  #### <a name="after"></a><span data-ttu-id="99ec1-148">После</span><span class="sxs-lookup"><span data-stu-id="99ec1-148">After</span></span>

  ```powershell
  $disk = New-AzDisk ... | Set-AzDiskDiskEncrytionKey ...
  $disk.EncryptionSettingsCollection.EncryptionSettings

  $disk = New-AzDisk ... | Set-AzDiskKeyEncrytionKey ...
  $disk.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateDiskEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzDiskUpdateConfig | Set-AzDiskUpdateKeyEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings
  ```

- <span data-ttu-id="99ec1-149">Добавлено свойство ```EncryptionSettingsCollection``` для заключения свойства `EncryptionSettings` в классе `PSSnapshot`.</span><span class="sxs-lookup"><span data-stu-id="99ec1-149">Added ```EncryptionSettingsCollection``` Property to enclose `EncryptionSettings` property in `PSSnapshot`</span></span>

  #### <a name="before"></a><span data-ttu-id="99ec1-150">До</span><span class="sxs-lookup"><span data-stu-id="99ec1-150">Before</span></span>

  ```powershell
  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotDiskEncryptionKey ...
  $snap.EncryptionSettings

  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotKeyEncryptionKey ...
  $snap.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateDiskEncryptionKey ...
  $update.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateKeyEncryptionKey ...
  $update.EncryptionSettings
  ```

  #### <a name="after"></a><span data-ttu-id="99ec1-151">После</span><span class="sxs-lookup"><span data-stu-id="99ec1-151">After</span></span>

  ```powershell
  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotDiskEncryptionKey ...
  $snap.EncryptionSettingsCollection.EncryptionSettings

  $snap = New-AzSnapshotConfig ... | Set-AzSnapshotKeyEncryptionKey ...
  $snap.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateDiskEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings

  $update = New-AzSnapshotUpdateConfig ... | Set-AzSnapshotUpdateKeyEncryptionKey ...
  $update.EncryptionSettingsCollection.EncryptionSettings
  ```

- <span data-ttu-id="99ec1-152">Удалено свойство `VirtualMachineProfile` из класса `PSVirtualMachineScaleSet`.</span><span class="sxs-lookup"><span data-stu-id="99ec1-152">Removed `VirtualMachineProfile` property from `PSVirtualMachineScaleSet`</span></span>

  #### <a name="before"></a><span data-ttu-id="99ec1-153">До</span><span class="sxs-lookup"><span data-stu-id="99ec1-153">Before</span></span>

  ```powershell
  $vmss = New-AzVMSSConfig ...
  $vmss.VirtualMachineProfile.AdditionalCapabilities.UltraSSDEnabled = $true
  ```

  #### <a name="after"></a><span data-ttu-id="99ec1-154">После</span><span class="sxs-lookup"><span data-stu-id="99ec1-154">After</span></span>

  ```powershell
  $vmss = New-AzVMSSConfig ...
  $vmss.AdditionalCapabilities.UltraSSDEnabled = $true
  ```

- <span data-ttu-id="99ec1-155">Для командлета `Set-AzVMBootDiagnostic` удален устаревший псевдоним (ранее — `Set-AzVMBootDiagnostics`).</span><span class="sxs-lookup"><span data-stu-id="99ec1-155">Cmdlet `Set-AzVMBootDiagnostic` removed alias to `Set-AzVMBootDiagnostics`</span></span>

  #### <a name="before"></a><span data-ttu-id="99ec1-156">До</span><span class="sxs-lookup"><span data-stu-id="99ec1-156">Before</span></span>

  <span data-ttu-id="99ec1-157">Использование устаревшего псевдонима</span><span class="sxs-lookup"><span data-stu-id="99ec1-157">Using deprecated alias</span></span>

  ```powershell
  Set-AzVMBootDiagnostics
  ```

  #### <a name="after"></a><span data-ttu-id="99ec1-158">После</span><span class="sxs-lookup"><span data-stu-id="99ec1-158">After</span></span>

  ```powershell
  Set-AzVMBootDIagnostic
  ```

- <span data-ttu-id="99ec1-159">Для командлета `Export-AzLogAnalyticThrottledRequest` удален устаревший псевдоним (ранее — `Export-AzLogAnalyticThrottledRequests`).</span><span class="sxs-lookup"><span data-stu-id="99ec1-159">Cmdlet `Export-AzLogAnalyticThrottledRequest` removed alias to `Export-AzLogAnalyticThrottledRequests`</span></span>

  #### <a name="before"></a><span data-ttu-id="99ec1-160">До</span><span class="sxs-lookup"><span data-stu-id="99ec1-160">Before</span></span>

  <span data-ttu-id="99ec1-161">Использование устаревшего псевдонима</span><span class="sxs-lookup"><span data-stu-id="99ec1-161">Using deprectaed alias</span></span>

  ```powershell
  Export-AzLogAnalyticThrottledRequests
  ```

  #### <a name="after"></a><span data-ttu-id="99ec1-162">После</span><span class="sxs-lookup"><span data-stu-id="99ec1-162">After</span></span>

  ```powershell
  Export-AzLogAnalyticThrottledRequest
  ```

### <a name="azhdinsight"></a><span data-ttu-id="99ec1-163">Az.HDInsight</span><span class="sxs-lookup"><span data-stu-id="99ec1-163">Az.HDInsight</span></span>

- <span data-ttu-id="99ec1-164">Удалены командлеты `Grant-AzHDInsightHttpServicesAccess` и `Revoke-AzHDInsightHttpServicesAccess`.</span><span class="sxs-lookup"><span data-stu-id="99ec1-164">Removed the `Grant-AzHDInsightHttpServicesAccess` and `Revoke-AzHDInsightHttpServicesAccess` cmdlets.</span></span> <span data-ttu-id="99ec1-165">Они больше не требуются, потому что доступ по протоколу HTTP всегда включен во всех кластерах HDInsight.</span><span class="sxs-lookup"><span data-stu-id="99ec1-165">These are no longer necessary because HTTP access is always enabled on all HDInsight clusters.</span></span>
- <span data-ttu-id="99ec1-166">Добавлен новый командлет `Set-AzHDInsightGatewayCredential`.</span><span class="sxs-lookup"><span data-stu-id="99ec1-166">Added a new `Set-AzHDInsightGatewayCredential`  cmdlet.</span></span> <span data-ttu-id="99ec1-167">С помощью этого командлета можно изменить имя пользователя и пароль HTTP шлюза (заменяет `Grant-AzHDInsightHttpServicesAccess`).</span><span class="sxs-lookup"><span data-stu-id="99ec1-167">Use this cmdlet to change the gateway HTTP username and password (replaces `Grant-AzHDInsightHttpServicesAccess`).</span></span>
- <span data-ttu-id="99ec1-168">Обновлен командлет `Get-AzHDInsightJobOutput` для поддержки детализированного доступа на основе ролей к ключу к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="99ec1-168">Updated the `Get-AzHDInsightJobOutput` cmdlet to support granular role-based access to the storage key.</span></span>
    - <span data-ttu-id="99ec1-169">На пользователей с ролями оператора, участника или владельца кластера HDInsight это не повлияет.</span><span class="sxs-lookup"><span data-stu-id="99ec1-169">Users with HDInsight Cluster Operator, Contributor, or Owner roles will not be affected.</span></span>
    - <span data-ttu-id="99ec1-170">Только пользователям с ролью читателя нужно указывать параметр `DefaultStorageAccountKey` явным образом.</span><span class="sxs-lookup"><span data-stu-id="99ec1-170">Users with only the Reader role will need to specify `DefaultStorageAccountKey` parameter explicitly.</span></span>

<span data-ttu-id="99ec1-171">Дополнительные сведения об этих изменениях доступа на основе ролей см. по адресу [aka.ms/hdi-config-update](/azure/hdinsight/hdinsight-migrate-granular-access-cluster-configurations).</span><span class="sxs-lookup"><span data-stu-id="99ec1-171">For more information about these role-based access changes, see [aka.ms/hdi-config-update](/azure/hdinsight/hdinsight-migrate-granular-access-cluster-configurations)</span></span>

  #### <a name="before"></a><span data-ttu-id="99ec1-172">До</span><span class="sxs-lookup"><span data-stu-id="99ec1-172">Before</span></span>

  ```powershell
  Grant-AzHDInsightHttpServicesAccess -ClusterName $cluster -HttpCredential $credential
  ```

  #### <a name="after"></a><span data-ttu-id="99ec1-173">После</span><span class="sxs-lookup"><span data-stu-id="99ec1-173">After</span></span>

  ```powershell
  Set-AzHDInsightGatewayCredential -ClusterName $cluster -HttpCredential $credential
  ```

###  <a name="users-with-only-reader-role-for-cmdlet-get-azhdinsightjoboutput"></a><span data-ttu-id="99ec1-174">Пользователи только с ролью читателя для командлета Get-AzHDInsightJobOutput</span><span class="sxs-lookup"><span data-stu-id="99ec1-174">Users with only Reader role for cmdlet Get-AzHDInsightJobOutput</span></span>

  ####  <a name="before"></a><span data-ttu-id="99ec1-175">До</span><span class="sxs-lookup"><span data-stu-id="99ec1-175">Before</span></span>

  ```powershell
  Get-AzHDInsightJobOutput  -ClusterName $clusterName -JobId $jobId
  ```

  #### <a name="after"></a><span data-ttu-id="99ec1-176">После</span><span class="sxs-lookup"><span data-stu-id="99ec1-176">After</span></span>

  ```powershell
  Get-AzHDInsightJobOutput  -ClusterName $clusterName -JobId $jobId -DefaultStorageAccountKey $storageAccountKey
  ```

### <a name="azstorage"></a><span data-ttu-id="99ec1-177">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="99ec1-177">Az.Storage</span></span>

- <span data-ttu-id="99ec1-178">Пространства имен для типов, возвращаемых командлетами, выполняющими действия с большими двоичными объектами, очередями и файлами, были изменены с `Microsoft.WindowsAzure.Storage` на `Microsoft.Azure.Storage`.</span><span class="sxs-lookup"><span data-stu-id="99ec1-178">Namespaces for types returned from Blob, Queue, and File cmdlets have changed their namespace from `Microsoft.WindowsAzure.Storage` to `Microsoft.Azure.Storage`.</span></span>  <span data-ttu-id="99ec1-179">Хотя согласно политике критических изменений технически это не является критическим изменением, для взаимодействия с объектами, возвращаемыми этими командлетами, может потребоваться внести некоторые изменения в код, использующий методы из пакета SDK .NET для службы хранилища.</span><span class="sxs-lookup"><span data-stu-id="99ec1-179">While this is not technically a breaking change according to the breaking change policy, it may require some changes in code that uses the methods from the Storage .Net SDK to interact with the objects returned from these cmdlets.</span></span>

  #### <a name="example-1--add-a-message-to-a-queue-change-cloudqueuemessage-object-namespace"></a><span data-ttu-id="99ec1-180">Пример 1. Добавление сообщения в очередь (изменение пространства имен объекта CloudQueueMessage)</span><span class="sxs-lookup"><span data-stu-id="99ec1-180">Example 1:  Add a message to a Queue (change CloudQueueMessage object namespace)</span></span>

  <span data-ttu-id="99ec1-181">Перед следующей операцией.</span><span class="sxs-lookup"><span data-stu-id="99ec1-181">Before:</span></span> 

  ```powershell
  $queue = Get-AzStorageQueue –Name $queueName –Context $ctx
  $queueMessage = New-Object -TypeName "Microsoft.WindowsAzure.Storage.Queue.CloudQueueMessage,$($queue.CloudQueue.GetType().Assembly.FullName)" -ArgumentList "This is message 1"
  $queue.CloudQueue.AddMessageAsync($QueueMessage)
  ```

  <span data-ttu-id="99ec1-182">После следующих операций.</span><span class="sxs-lookup"><span data-stu-id="99ec1-182">After:</span></span>

  ```powershell
  $queue = Get-AzStorageQueue –Name $queueName –Context $ctx
  $queueMessage = New-Object -TypeName "Microsoft.Azure.Storage.Queue.CloudQueueMessage,$($queue.CloudQueue.GetType().Assembly.FullName)"  -ArgumentList "This is message 1"
  $queue.CloudQueue.AddMessageAsync($QueueMessage)
  ```

  #### <a name="example-2--fetch-blobfile-attributes-with-accesscondition-change-accesscondition-object-namespace"></a><span data-ttu-id="99ec1-183">Пример 2. Получение атрибутов файла или большого двоичного объекта с условием AccessCondition (изменение пространства имен объекта AccessCondition)</span><span class="sxs-lookup"><span data-stu-id="99ec1-183">Example 2:  Fetch Blob/File Attributes with AccessCondition (change AccessCondition object namespace)</span></span>

  <span data-ttu-id="99ec1-184">Перед следующей операцией.</span><span class="sxs-lookup"><span data-stu-id="99ec1-184">Before:</span></span> 

  ```powershell
  $accessCondition= New-Object Microsoft.WindowsAzure.Storage.AccessCondition

  $blob = Get-AzureStorageBlob -Container $containerName -Blob $blobName
  $blob.ICloudBlob.FetchAttributes($accessCondition)

  $file = Get-AzureStorageFile -ShareName $shareName -Path $filepath
  $file.FetchAttributes($accessCondition)
  ```

  <span data-ttu-id="99ec1-185">После следующих операций.</span><span class="sxs-lookup"><span data-stu-id="99ec1-185">After:</span></span>

  ```powershell
  $accessCondition= New-Object Microsoft.Azure.Storage.AccessCondition

  $blob = Get-AzureStorageBlob -Container $containerName -Blob $blobName
  $blob.ICloudBlob.FetchAttributes($accessCondition)

  $file = Get-AzureStorageFile -ShareName $shareName -Path $filepath
  $file.FetchAttributes($accessCondition)
  ```

- <span data-ttu-id="99ec1-186">Хотя технически это не является критическим изменением, вы обнаружите различия в значениях свойства SKU.Name учетных записей хранения в выходных данных, возвращенных из `New/Get/Set-AzStorageAccount`. Ниже приведены эти изменения.</span><span class="sxs-lookup"><span data-stu-id="99ec1-186">While not technically a breaking change, you will notice output differences in the Sku.Name property of Storage Accounts returned from  `New/Get/Set-AzStorageAccount` changes are as follows.</span></span> <span data-ttu-id="99ec1-187">(После изменения значения SkuName в выходных и входных данных согласовываются.)</span><span class="sxs-lookup"><span data-stu-id="99ec1-187">(After the change, output and input SkuName are aligned.)</span></span>
  - <span data-ttu-id="99ec1-188">"StandardLRS" -> "Standard_LRS".</span><span class="sxs-lookup"><span data-stu-id="99ec1-188">"StandardLRS" -> "Standard_LRS";</span></span>
  - <span data-ttu-id="99ec1-189">"StandardGRS" -> "Standard_GRS".</span><span class="sxs-lookup"><span data-stu-id="99ec1-189">"StandardGRS" -> "Standard_GRS";</span></span>
  - <span data-ttu-id="99ec1-190">"StandardRAGRS" -> "Standard_RAGRS".</span><span class="sxs-lookup"><span data-stu-id="99ec1-190">"StandardRAGRS" -> "Standard_RAGRS";</span></span>
  - <span data-ttu-id="99ec1-191">"StandardZRS" -> "Standard_ZRS".</span><span class="sxs-lookup"><span data-stu-id="99ec1-191">"StandardZRS" -> "Standard_ZRS";</span></span>
  - <span data-ttu-id="99ec1-192">"PremiumLRS" -> "Premium_LRS".</span><span class="sxs-lookup"><span data-stu-id="99ec1-192">"PremiumLRS" -> "Premium_LRS";</span></span>

- <span data-ttu-id="99ec1-193">Изменено поведение службы по умолчанию при создании учетной записи хранения без указания параметра Kind.</span><span class="sxs-lookup"><span data-stu-id="99ec1-193">The default service behavior when creating a storage account withous specifying a Kind has changed.</span></span>  <span data-ttu-id="99ec1-194">В предыдущих версиях при создании учетной записи хранения без указания параметра `Kind` использовался тип `Storage`. В новой версии значением параметра `Kind` по умолчанию является `StorageV2`.</span><span class="sxs-lookup"><span data-stu-id="99ec1-194">In previous versions, when a storage account was created with no `Kind` specified, the Storage account Kind of `Storage` was used, in the new version `StorageV2` is the default `Kind` value.</span></span> <span data-ttu-id="99ec1-195">Если вам нужно создать учетную запись хранения версии 1 с параметром Kind со значением Storage, добавьте параметр -Kind Storage.</span><span class="sxs-lookup"><span data-stu-id="99ec1-195">If you need to create a V1 Storage account with Kind 'Storage', add parameter '-Kind Storage'</span></span>

  #### <a name="example--create-a-storage-account-default-kind-change"></a><span data-ttu-id="99ec1-196">Пример. Создание учетной записи хранения (изменение вида по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="99ec1-196">Example : Create a storage Account (Default Kind change)</span></span>  

  <span data-ttu-id="99ec1-197">Перед следующей операцией.</span><span class="sxs-lookup"><span data-stu-id="99ec1-197">Before:</span></span>

  ```powershell
  PS c:\> New-AzStorageAccount -ResourceGroupName groupname -Name accountname -SkuName Standard_LRS -Location "westus"

  StorageAccountName ResourceGroupName Location SkuName     Kind      AccessTier CreationTime          ProvisioningState EnableHttpsTrafficOnly
  ------------------ ----------------- -------- -------     ----      ---------- ------------          ----------------- ----------------------
  accountname        groupname         westus   StandardLRS Storage   Hot        4/17/2018 10:34:32 AM Succeeded         False
  ```

  <span data-ttu-id="99ec1-198">После следующих операций.</span><span class="sxs-lookup"><span data-stu-id="99ec1-198">After:</span></span>

  ```powershell
  PS c:\> New-AzStorageAccount -ResourceGroupName groupname -Name accountname -SkuName Standard_LRS -Location "westus"

  StorageAccountName ResourceGroupName Location SkuName      Kind      AccessTier CreationTime          ProvisioningState EnableHttpsTrafficOnly
  ------------------ ----------------- -------- -------      ----      ----------  ------------          ----------------- ----------------------
  accountname        groupname         westus   Standard_LRS StorageV2 Hot        4/17/2018 10:34:32 AM Succeeded         False
  ```