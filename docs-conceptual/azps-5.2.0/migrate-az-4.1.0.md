---
title: Руководство по переходу на Az версии 4.1.0
description: Это руководство по переходу содержит список критических изменений, внесенных в выпуск Az версии 4.1.0 в Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/23/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: fe4a2a7c2f1b171b530eef41ac072b2029be1026
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "96856773"
---
# <a name="migration-guide-for-az-410"></a><span data-ttu-id="24766-103">Руководство по переходу на Az версии 4.1.0</span><span class="sxs-lookup"><span data-stu-id="24766-103">Migration Guide for Az 4.1.0</span></span>

<span data-ttu-id="24766-104">В этом документе описываются изменения между версиями Az 3.0.0 и 4.1.0.</span><span class="sxs-lookup"><span data-stu-id="24766-104">This document describes the changes between the 3.0.0 and 4.1.0 versions of Az.</span></span>

- [<span data-ttu-id="24766-105">Руководство по переходу на Az версии 4.1.0</span><span class="sxs-lookup"><span data-stu-id="24766-105">Migration Guide for Az 4.1.0</span></span>](#migration-guide-for-az-410)
  - [<span data-ttu-id="24766-106">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="24766-106">Az.ApiManagement</span></span>](#azapimanagement)
    - [`Add-AzApiManagementRegion`](#add-azapimanagementregion)
    - [`New-AzApiManagement`](#new-azapimanagement)
    - [`Set-AzApiManagement`](#set-azapimanagement)
    - [`Get-AzApiManagementProperty`](#get-azapimanagementproperty)
    - [`New-AzApiManagementProperty`](#new-azapimanagementproperty)
    - [`Remove-AzApiManagementProperty`](#remove-azapimanagementproperty)
    - [`Set-AzApiManagementProperty`](#set-azapimanagementproperty)
  - [<span data-ttu-id="24766-107">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="24766-107">Az.Batch</span></span>](#azbatch)
    - [<span data-ttu-id="24766-108">`Get-AzBatchApplication`, `New-AzBatchApplication`</span><span class="sxs-lookup"><span data-stu-id="24766-108">`Get-AzBatchApplication`, `New-AzBatchApplication`</span></span>](#get-azbatchapplication-new-azbatchapplication)
    - [<span data-ttu-id="24766-109">`Get-AzBatchComputeNode`, `New-AzBatchPool`</span><span class="sxs-lookup"><span data-stu-id="24766-109">`Get-AzBatchComputeNode`, `New-AzBatchPool`</span></span>](#get-azbatchcomputenode-new-azbatchpool)
    - [<span data-ttu-id="24766-110">`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`</span><span class="sxs-lookup"><span data-stu-id="24766-110">`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`</span></span>](#get-azbatchapplicationpackage-new-azbatchapplicationpackage)
  - [<span data-ttu-id="24766-111">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="24766-111">Az.Compute</span></span>](#azcompute)
    - [`Remove-AzVmssDiagnosticsExtension`](#remove-azvmssdiagnosticsextension)
    - [`Get-AzVMImage`](#get-azvmimage)
    - [`New-AzVMConfig`](#new-azvmconfig)
    - [`Update-AzVM`](#update-azvm)
    - [`New-AzProximityPlacementGroup`](#new-azproximityplacementgroup)
    - [`Remove-AzProximityPlacementGroup`](#remove-azproximityplacementgroup)
    - [`Get-AzProximityPlacementGroup`](#get-azproximityplacementgroup)
    - [`Add-AzVmssAdditionalUnattendContent`](#add-azvmssadditionalunattendcontent)
    - [`Add-AzVmssDataDisk`](#add-azvmssdatadisk)
    - [`Add-AzVmssExtension`](#add-azvmssextension)
    - [`Add-AzVmssNetworkInterfaceConfiguration`](#add-azvmssnetworkinterfaceconfiguration)
    - [`Add-AzVmssSecret`](#add-azvmsssecret)
    - [`Add-AzVmssSshPublicKey`](#add-azvmsssshpublickey)
    - [`Add-AzVmssWinRMListener`](#add-azvmsswinrmlistener)
    - [`New-AzVmssConfig`](#new-azvmssconfig)
    - [`Remove-AzVmssDataDisk`](#remove-azvmssdatadisk)
    - [`Remove-AzVmssExtension`](#remove-azvmssextension)
    - [`Remove-AzVmssNetworkInterfaceConfiguration`](#remove-azvmssnetworkinterfaceconfiguration)
    - [`Set-AzVmssBootDiagnostic`](#set-azvmssbootdiagnostic)
    - [`Set-AzVmssOsProfile`](#set-azvmssosprofile)
    - [`Set-AzVmssRollingUpgradePolicy`](#set-azvmssrollingupgradepolicy)
    - [`Set-AzVmssStorageProfile`](#set-azvmssstorageprofile)
    - [`New-AzVmss`](#new-azvmss)
    - [`Repair-AzVmssServiceFabricUpdateDomain`](#repair-azvmssservicefabricupdatedomain)
    - [`Get-AzVmss`](#get-azvmss)
    - [`Set-AzVmssOrchestrationServiceState`](#set-azvmssorchestrationservicestate)
    - [`Update-AzVmss`](#update-azvmss)
    - [`Add-AzVmssDiagnosticsExtension`](#add-azvmssdiagnosticsextension)
    - [`Disable-AzVmssDiskEncryption`](#disable-azvmssdiskencryption)
  - [<span data-ttu-id="24766-112">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="24766-112">Az.KeyVault</span></span>](#azkeyvault)
    - [`New-AzKeyVaultCertificateOrganizationDetail`](#new-azkeyvaultcertificateorganizationdetail)
    - [`New-AzKeyVaultCertificateAdministratorDetail`](#new-azkeyvaultcertificateadministratordetail)
    - [`New-AzKeyVault`](#new-azkeyvault)
  - [<span data-ttu-id="24766-113">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="24766-113">Az.Monitor</span></span>](#azmonitor)
    - [`Add-AzLogProfile`](#add-azlogprofile)
    - [`Get-AzLogProfile`](#get-azlogprofile)
    - [`New-AzMetricAlertRuleV2Criteria`](#new-azmetricalertrulev2criteria)
  - [<span data-ttu-id="24766-114">Az.Network</span><span class="sxs-lookup"><span data-stu-id="24766-114">Az.Network</span></span>](#aznetwork)
    - [`Get-AzNetworkWatcherConnectionMonitor`](#get-aznetworkwatcherconnectionmonitor)
    - [`New-AzNetworkWatcherConnectionMonitorTestConfigurationObject`](#new-aznetworkwatcherconnectionmonitortestconfigurationobject)
  - [<span data-ttu-id="24766-115">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="24766-115">Az.OperationalInsights</span></span>](#azoperationalinsights)
    - [`Get-AzOperationalInsightsDataSource`](#get-azoperationalinsightsdatasource)
    - [`New-AzOperationalInsightsApplicationInsightsDataSource`](#new-azoperationalinsightsapplicationinsightsdatasource)
    - [`New-AzOperationalInsightsAzureActivityLogDataSource`](#new-azoperationalinsightsazureactivitylogdatasource)
    - [`New-AzOperationalInsightsCustomLogDataSource`](#new-azoperationalinsightscustomlogdatasource)
    - [`New-AzOperationalInsightsLinuxPerformanceObjectDataSource`](#new-azoperationalinsightslinuxperformanceobjectdatasource)
    - [`New-AzOperationalInsightsLinuxSyslogDataSource`](#new-azoperationalinsightslinuxsyslogdatasource)
    - [`New-AzOperationalInsightsWindowsEventDataSource`](#new-azoperationalinsightswindowseventdatasource)
    - [`New-AzOperationalInsightsWindowsPerformanceCounterDataSource`](#new-azoperationalinsightswindowsperformancecounterdatasource)
    - [`Remove-AzOperationalInsightsDataSource`](#remove-azoperationalinsightsdatasource)
    - [`Disable-AzOperationalInsightsIISLogCollection`](#disable-azoperationalinsightsiislogcollection)
    - [`Disable-AzOperationalInsightsLinuxCustomLogCollection`](#disable-azoperationalinsightslinuxcustomlogcollection)
    - [`Disable-AzOperationalInsightsLinuxPerformanceCollection`](#disable-azoperationalinsightslinuxperformancecollection)
    - [`Disable-AzOperationalInsightsLinuxSyslogCollection`](#disable-azoperationalinsightslinuxsyslogcollection)
    - [`Enable-AzOperationalInsightsIISLogCollection`](#enable-azoperationalinsightsiislogcollection)
    - [`Enable-AzOperationalInsightsLinuxCustomLogCollection`](#enable-azoperationalinsightslinuxcustomlogcollection)
    - [`Enable-AzOperationalInsightsLinuxPerformanceCollection`](#enable-azoperationalinsightslinuxperformancecollection)
    - [`Enable-AzOperationalInsightsLinuxSyslogCollection`](#enable-azoperationalinsightslinuxsyslogcollection)
    - [`Get-AzOperationalInsightsSavedSearch`](#get-azoperationalinsightssavedsearch)
    - [`Get-AzOperationalInsightsSavedSearchResult`](#get-azoperationalinsightssavedsearchresult)
    - [`Get-AzOperationalInsightsSearchResult`](#get-azoperationalinsightssearchresult)
    - [`Get-AzOperationalInsightsStorageInsight`](#get-azoperationalinsightsstorageinsight)
    - [`New-AzOperationalInsightsStorageInsight`](#new-azoperationalinsightsstorageinsight)
    - [`Remove-AzOperationalInsightsStorageInsight`](#remove-azoperationalinsightsstorageinsight)
    - [`Set-AzOperationalInsightsStorageInsight`](#set-azoperationalinsightsstorageinsight)
    - [`Get-AzOperationalInsightsLinkTarget`](#get-azoperationalinsightslinktarget)
    - [`Get-AzOperationalInsightsWorkspace`](#get-azoperationalinsightsworkspace)
    - [`New-AzOperationalInsightsWorkspace`](#new-azoperationalinsightsworkspace)
    - [`Set-AzOperationalInsightsWorkspace`](#set-azoperationalinsightsworkspace)
    - [`Invoke-AzOperationalInsightsQuery`](#invoke-azoperationalinsightsquery)
  - [<span data-ttu-id="24766-116">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="24766-116">Az.Resources</span></span>](#azresources)
    - [`Get-AzDeploymentScript`](#get-azdeploymentscript)
    - [`Get-AzDeploymentScriptLog`](#get-azdeploymentscriptlog)
    - [`Save-AzDeploymentScriptLog`](#save-azdeploymentscriptlog)
    - [`Get-AzResourceLock, New-AzResourceLock, Remove-AzResourceLock, Set-AzResourceLock`](#get-azresourcelock-new-azresourcelock-remove-azresourcelock-set-azresourcelock)
    - [`Get-AzPolicyAlias`](#get-azpolicyalias)
    - [`New-AzPolicyAssignment`](#new-azpolicyassignment)
    - [`Remove-AzDeploymentScript`](#remove-azdeploymentscript)
  - [<span data-ttu-id="24766-117">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="24766-117">Az.Storage</span></span>](#azstorage)
    - [<span data-ttu-id="24766-118">`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`</span><span class="sxs-lookup"><span data-stu-id="24766-118">`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`</span></span>](#update-azstorageaccountnetworkruleset-get-azstorageaccountnetworkruleset)
    - [<span data-ttu-id="24766-119">`New-AzStorageTable`, `Get-AzStorageTable`</span><span class="sxs-lookup"><span data-stu-id="24766-119">`New-AzStorageTable`, `Get-AzStorageTable`</span></span>](#new-azstoragetable-get-azstoragetable)
    - [<span data-ttu-id="24766-120">`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`</span><span class="sxs-lookup"><span data-stu-id="24766-120">`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`</span></span>](#get-azstoragefile-remove-azstoragefile-get-azstoragefilecontent-set-azstoragefilecontent-start-azstoragefilecopy)
    - [<span data-ttu-id="24766-121">`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`</span><span class="sxs-lookup"><span data-stu-id="24766-121">`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`</span></span>](#get-azstoragefile-new-azstoragedirectory-remove-azstoragedirectory)
    - [<span data-ttu-id="24766-122">`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`</span><span class="sxs-lookup"><span data-stu-id="24766-122">`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`</span></span>](#get-azstorageshare-new-azstorageshare-remove-azstorageshare)
    - [`Set-AzStorageShareQuota`](#set-azstoragesharequota)
    - [`Remove-AzStorageDirectory`](#remove-azstoragedirectory)

## <a name="azapimanagement"></a><span data-ttu-id="24766-123">Az.ApiManagement</span><span class="sxs-lookup"><span data-stu-id="24766-123">Az.ApiManagement</span></span>

### `Add-AzApiManagementRegion`

<span data-ttu-id="24766-124">Тип свойства `Type` типа `Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentity` был изменен с `Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentityType` на `System.String`.</span><span class="sxs-lookup"><span data-stu-id="24766-124">The type of property `Type` of type `Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentity` has changed from `Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentityType` to `System.String`.</span></span>

### `New-AzApiManagement`

- <span data-ttu-id="24766-125">Командлет `New-AzApiManagement` больше не поддерживает параметр `AssignIdentity`, и для исходного имени параметра не найден псевдоним.</span><span class="sxs-lookup"><span data-stu-id="24766-125">The cmdlet `New-AzApiManagement` no longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="24766-126">Набор параметров `__AllParameterSets` для командлета `New-AzApiManagement` был удален.</span><span class="sxs-lookup"><span data-stu-id="24766-126">The parameter set `__AllParameterSets` for cmdlet `New-AzApiManagement` has been removed.</span></span>

### `Set-AzApiManagement`

- <span data-ttu-id="24766-127">Командлет `Set-AzApiManagement` больше не поддерживает параметр `AssignIdentity`, и для исходного имени параметра не найден псевдоним.</span><span class="sxs-lookup"><span data-stu-id="24766-127">The cmdlet `Set-AzApiManagement` no longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="24766-128">Набор параметров `__AllParameterSets` для командлета `Set-AzApiManagement` был удален.</span><span class="sxs-lookup"><span data-stu-id="24766-128">The parameter set `__AllParameterSets` for cmdlet `Set-AzApiManagement` has been removed.</span></span>

### `Get-AzApiManagementProperty`

<span data-ttu-id="24766-129">Командлет `Get-AzApiManagementProperty` заменен на `Get-AzApiManagementNamedValue`.</span><span class="sxs-lookup"><span data-stu-id="24766-129">The cmdlet `Get-AzApiManagementProperty` has been replaced by `Get-AzApiManagementNamedValue`.</span></span>

### `New-AzApiManagementProperty`

<span data-ttu-id="24766-130">Командлет `New-AzApiManagementProperty` заменен на `New-AzApiManagementNamedValue`.</span><span class="sxs-lookup"><span data-stu-id="24766-130">The cmdlet `New-AzApiManagementProperty` has been replaced by `New-AzApiManagementNamedValue`.</span></span>

### `Remove-AzApiManagementProperty`

<span data-ttu-id="24766-131">Командлет `Remove-AzApiManagementProperty` заменен на `Remove-AzApiManagementNamedValue`.</span><span class="sxs-lookup"><span data-stu-id="24766-131">The cmdlet `Remove-AzApiManagementProperty` has been replaced by `Remove-AzApiManagementNamedValue`.</span></span>

### `Set-AzApiManagementProperty`

<span data-ttu-id="24766-132">Командлет `Set-AzApiManagementProperty` заменен на `Set-AzApiManagementNamedValue`.</span><span class="sxs-lookup"><span data-stu-id="24766-132">The cmdlet `Set-AzApiManagementProperty` has been replaced by `Set-AzApiManagementNamedValue`.</span></span>

## <a name="azbatch"></a><span data-ttu-id="24766-133">Az.Batch</span><span class="sxs-lookup"><span data-stu-id="24766-133">Az.Batch</span></span>

### <a name="get-azbatchapplication-new-azbatchapplication"></a><span data-ttu-id="24766-134">`Get-AzBatchApplication`, `New-AzBatchApplication`</span><span class="sxs-lookup"><span data-stu-id="24766-134">`Get-AzBatchApplication`, `New-AzBatchApplication`</span></span>

<span data-ttu-id="24766-135">Свойство `ApplicationPackages` типа `Microsoft.Azure.Commands.Batch.Models.PSApplication` удалено.</span><span class="sxs-lookup"><span data-stu-id="24766-135">The property `ApplicationPackages` of type `Microsoft.Azure.Commands.Batch.Models.PSApplication` has been removed.</span></span>

### <a name="get-azbatchcomputenode-new-azbatchpool"></a><span data-ttu-id="24766-136">`Get-AzBatchComputeNode`, `New-AzBatchPool`</span><span class="sxs-lookup"><span data-stu-id="24766-136">`Get-AzBatchComputeNode`, `New-AzBatchPool`</span></span>

<span data-ttu-id="24766-137">Свойство `PublicIPs` типа `Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration` было удалено.</span><span class="sxs-lookup"><span data-stu-id="24766-137">The property `PublicIPs` of type `Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration` has been removed</span></span>

### <a name="get-azbatchapplicationpackage-new-azbatchapplicationpackage"></a><span data-ttu-id="24766-138">`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`</span><span class="sxs-lookup"><span data-stu-id="24766-138">`Get-AzBatchApplicationPackage`, `New-AzBatchApplicationPackage`</span></span>

<span data-ttu-id="24766-139">Тип свойства `StorageUrlExpiry` типа `Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage` был изменен с `System.DateTime` на `System.DateTime?`.</span><span class="sxs-lookup"><span data-stu-id="24766-139">The type of property `StorageUrlExpiry` of type `Microsoft.Azure.Commands.Batch.Models.PSApplicationPackage` has changed from `System.DateTime` to `System.DateTime?`.</span></span>

## <a name="azcompute"></a><span data-ttu-id="24766-140">Az.Compute</span><span class="sxs-lookup"><span data-stu-id="24766-140">Az.Compute</span></span>

### `Remove-AzVmssDiagnosticsExtension`

<span data-ttu-id="24766-141">Тип свойства `AutomaticRepairsPolicy` типа `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` был изменен с `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` на `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="24766-141">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Get-AzVMImage`

- <span data-ttu-id="24766-142">Командлет `Get-AzVMImage` больше не поддерживает параметр `FilterExpression`, и для исходного имени параметра не найден псевдоним.</span><span class="sxs-lookup"><span data-stu-id="24766-142">The cmdlet `Get-AzVMImage` no longer supports the parameter `FilterExpression` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="24766-143">Набор параметров `ListVMImage` для командлета `Get-AzVMImage` был удален.</span><span class="sxs-lookup"><span data-stu-id="24766-143">The parameter set `ListVMImage` for cmdlet `Get-AzVMImage` has been removed.</span></span>

### `New-AzVMConfig`

- <span data-ttu-id="24766-144">Командлет `New-AzVMConfig` больше не поддерживает параметр `AssignIdentity`, и для исходного имени параметра не найден псевдоним.</span><span class="sxs-lookup"><span data-stu-id="24766-144">The cmdlet `New-AzVMConfig` no longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="24766-145">Набор параметров `AssignIdentityParameterSet` для командлета `New-AzVMConfig` был удален.</span><span class="sxs-lookup"><span data-stu-id="24766-145">The parameter set `AssignIdentityParameterSet` for cmdlet `New-AzVMConfig` has been removed.</span></span>

### `Update-AzVM`

- <span data-ttu-id="24766-146">Командлет `Update-AzVM` больше не поддерживает параметр `AssignIdentity`, и для исходного имени параметра не найден псевдоним.</span><span class="sxs-lookup"><span data-stu-id="24766-146">The cmdlet `Update-AzVM` no longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="24766-147">Набор параметров `AssignIdentityParameterSet` для командлета `Update-AzVM` был удален.</span><span class="sxs-lookup"><span data-stu-id="24766-147">The parameter set `AssignIdentityParameterSet` for cmdlet `Update-AzVM` has been removed.</span></span>

### `New-AzProximityPlacementGroup`

- <span data-ttu-id="24766-148">Универсальный тип свойства `VirtualMachines`, `VirtualMachineScaleSets` и `AvailabilitySets` был изменен с `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` на `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.</span><span class="sxs-lookup"><span data-stu-id="24766-148">The generic type for property `VirtualMachines`, `VirtualMachineScaleSets`, and `AvailabilitySets` has been changed from `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` to `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.</span></span>
- <span data-ttu-id="24766-149">Свойство `VirtualMachinesColocationStatus`, `AvailabilitySetsColocationStatus` и `VirtualMachineScaleSetsColocationStatus` типа `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` было удалено.</span><span class="sxs-lookup"><span data-stu-id="24766-149">The property `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus`, and `AvailabilitySetsColocationStatus` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` has been removed.</span></span>

#### <a name="before"></a><span data-ttu-id="24766-150">Перед</span><span class="sxs-lookup"><span data-stu-id="24766-150">Before</span></span>

```powershell
PS C:\> New-AzProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName -Location $location -Tag @{key1 = 'val1'} | Format-List

ResourceGroupName                       : $resourceGroupName
ProximityPlacementGroupType             : Standard
VirtualMachinesColocationStatus         : {}
VirtualMachineScaleSetsColocationStatus : {}
AvailabilitySetsColocationStatus        : {}
ColocationStatus                        :
Id                                      : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/$resourceGroupName/providers/Microsoft.Compute/proximityPlacementGroups/$proximityPlacementGroupName
Name                                    : $proximityPlacementGroupName
Type                                    : Microsoft.Compute/proximityPlacementGroups
Location                                : $location
Tags                                    : {[key1, val1]}
VirtualMachines                         : {}
VirtualMachineScaleSets                 : {}
AvailabilitySets                        : {}
```

#### <a name="after"></a><span data-ttu-id="24766-151">После</span><span class="sxs-lookup"><span data-stu-id="24766-151">After</span></span>

```powershell
PS C:\> New-AzProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName -Location $location -Tag @{key1 = 'val1'} | Format-List

ResourceGroupName                       : $resourceGroupName
ProximityPlacementGroupType             : StandardColocationStatus                        :
Id                                      : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/$resourceGroupName/providers/Microsoft.Compute/proximityPlacementGroups/$proximityPlacementGroupName
Name                                    : $proximityPlacementGroupName
Type                                    : Microsoft.Compute/proximityPlacementGroups
Location                                : $location
Tags                                    : {[key1, val1]}
VirtualMachines                         : {}
VirtualMachineScaleSets                 : {}
AvailabilitySets                        : {}
```

### `Remove-AzProximityPlacementGroup`

- <span data-ttu-id="24766-152">Универсальный тип свойства `VirtualMachines`, `VirtualMachineScaleSets` и `AvailabilitySets` был изменен с `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` на `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.</span><span class="sxs-lookup"><span data-stu-id="24766-152">The generic type for property `VirtualMachines`, `VirtualMachineScaleSets`, and `AvailabilitySets` has been changed from `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` to `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.</span></span>
- <span data-ttu-id="24766-153">Свойство `VirtualMachinesColocationStatus`, `AvailabilitySetsColocationStatus` и `VirtualMachineScaleSetsColocationStatus` типа `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` было удалено.</span><span class="sxs-lookup"><span data-stu-id="24766-153">The property `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus`, and `AvailabilitySetsColocationStatus` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` has been removed.</span></span>

#### <a name="before"></a><span data-ttu-id="24766-154">Перед</span><span class="sxs-lookup"><span data-stu-id="24766-154">Before</span></span>

```powershell
PS C:\> Get-AzProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName | Remove-AzProximityPlacementGroup | Format-List

ResourceGroupName                       : $resourceGroupName
ProximityPlacementGroupType             : Standard
VirtualMachinesColocationStatus         : {}
VirtualMachineScaleSetsColocationStatus : {}
AvailabilitySetsColocationStatus        : {}
ColocationStatus                        :
Id                                      : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/$resourceGroupName/providers/Microsoft.Compute/proximityPlacementGroups/$proximityPlacementGroupName
Name                                    : $proximityPlacementGroupName
Type                                    : Microsoft.Compute/proximityPlacementGroups
Location                                : $location
Tags                                    : {[key1, val1]}
VirtualMachines                         : {}
VirtualMachineScaleSets                 : {}
AvailabilitySets                        : {}
```

#### <a name="after"></a><span data-ttu-id="24766-155">После</span><span class="sxs-lookup"><span data-stu-id="24766-155">After</span></span>

```powershell
PS C:\> Get-AzProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName | Remove-AzProximityPlacementGroup | Format-List

ResourceGroupName                       : $resourceGroupName
ProximityPlacementGroupType             : StandardColocationStatus                        :
Id                                      : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/$resourceGroupName/providers/Microsoft.Compute/proximityPlacementGroups/$proximityPlacementGroupName
Name                                    : $proximityPlacementGroupName
Type                                    : Microsoft.Compute/proximityPlacementGroups
Location                                : $location
Tags                                    : {[key1, val1]}
VirtualMachines                         : {}
VirtualMachineScaleSets                 : {}
AvailabilitySets                        : {}
```

### `Get-AzProximityPlacementGroup`

- <span data-ttu-id="24766-156">Универсальный тип свойства `VirtualMachines`, `VirtualMachineScaleSets` и `AvailabilitySets` был изменен с `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` на `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.</span><span class="sxs-lookup"><span data-stu-id="24766-156">The generic type for property `VirtualMachines`, `VirtualMachineScaleSets`, and `AvailabilitySets` has been changed from `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResource]` to `System.Collections.Generic.IList1[Microsoft.Azure.Management.Compute.Models.SubResourceWithColocationStatus]`.</span></span>
- <span data-ttu-id="24766-157">Свойство `VirtualMachinesColocationStatus`, `AvailabilitySetsColocationStatus` и `VirtualMachineScaleSetsColocationStatus` типа `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` было удалено.</span><span class="sxs-lookup"><span data-stu-id="24766-157">The property `VirtualMachinesColocationStatus`, `VirtualMachineScaleSetsColocationStatus`, and `AvailabilitySetsColocationStatus` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSProximityPlacementGroup` has been removed.</span></span>

#### <a name="before"></a><span data-ttu-id="24766-158">Перед</span><span class="sxs-lookup"><span data-stu-id="24766-158">Before</span></span>

```powershell
PS C:\> Get-AzProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName | Format-List

ResourceGroupName                       : $resourceGroupName
ProximityPlacementGroupType             : Standard
VirtualMachinesColocationStatus         : {}
VirtualMachineScaleSetsColocationStatus : {}
AvailabilitySetsColocationStatus        : {}
ColocationStatus                        :
Id                                      : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/$resourceGroupName/providers/Microsoft.Compute/proximityPlacementGroups/$proximityPlacementGroupName
Name                                    : $proximityPlacementGroupName
Type                                    : Microsoft.Compute/proximityPlacementGroups
Location                                : $location
Tags                                    : {[key1, val1]}
VirtualMachines                         : {}
VirtualMachineScaleSets                 : {}
AvailabilitySets                        : {}
```

#### <a name="after"></a><span data-ttu-id="24766-159">После</span><span class="sxs-lookup"><span data-stu-id="24766-159">After</span></span>

```powershell
PS C:\> Get-AzProximityPlacementGroup -ResourceGroupName $resourceGroupName -Name $proximityPlacementGroupName | Format-List

ResourceGroupName                       : $resourceGroupName
ProximityPlacementGroupType             : StandardColocationStatus                        :
Id                                      : /subscriptions/9e223dbe-3399-4e19-88eb-0975f02ac87f/resourceGroups/$resourceGroupName/providers/Microsoft.Compute/proximityPlacementGroups/$proximityPlacementGroupName
Name                                    : $proximityPlacementGroupName
Type                                    : Microsoft.Compute/proximityPlacementGroups
Location                                : $location
Tags                                    : {[key1, val1]}
VirtualMachines                         : {}
VirtualMachineScaleSets                 : {}
AvailabilitySets                        : {}
```

### `Add-AzVmssAdditionalUnattendContent`

<span data-ttu-id="24766-160">Тип свойства `AutomaticRepairsPolicy` типа `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` был изменен с `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` на `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="24766-160">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssDataDisk`

<span data-ttu-id="24766-161">Тип свойства `AutomaticRepairsPolicy` типа `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` был изменен с `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` на `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="24766-161">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssExtension`

<span data-ttu-id="24766-162">Тип свойства `AutomaticRepairsPolicy` типа `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` был изменен с `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` на `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="24766-162">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssNetworkInterfaceConfiguration`

<span data-ttu-id="24766-163">Тип свойства `AutomaticRepairsPolicy` типа `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` был изменен с `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` на `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="24766-163">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssSecret`

<span data-ttu-id="24766-164">Тип свойства `AutomaticRepairsPolicy` типа `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` был изменен с `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` на `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="24766-164">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssSshPublicKey`

<span data-ttu-id="24766-165">Тип свойства `AutomaticRepairsPolicy` типа `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` был изменен с `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` на `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="24766-165">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Add-AzVmssWinRMListener`

<span data-ttu-id="24766-166">Тип свойства `AutomaticRepairsPolicy` типа `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` был изменен с `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` на `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="24766-166">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `New-AzVmssConfig`

- <span data-ttu-id="24766-167">Тип свойства `AutomaticRepairsPolicy` типа `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` был изменен с `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` на `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="24766-167">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>
- <span data-ttu-id="24766-168">Больше не поддерживает параметр `AutomaticRepairMaxInstanceRepairsPercent`, и для исходного имени параметра не найден псевдоним.</span><span class="sxs-lookup"><span data-stu-id="24766-168">No longer supports the parameter `AutomaticRepairMaxInstanceRepairsPercent` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="24766-169">Больше не поддерживает параметр `AssignIdentity`, и для исходного имени параметра не найден псевдоним.</span><span class="sxs-lookup"><span data-stu-id="24766-169">No longer supports the parameter `AssignIdentity` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="24766-170">Набор параметров `__AllParameterSets` был удален.</span><span class="sxs-lookup"><span data-stu-id="24766-170">The parameter set `__AllParameterSets` has been removed.</span></span>
- <span data-ttu-id="24766-171">Набор параметров `ExplicitIdentityParameterSet` был удален.</span><span class="sxs-lookup"><span data-stu-id="24766-171">The parameter set `ExplicitIdentityParameterSet` has been removed.</span></span>
- <span data-ttu-id="24766-172">Набор параметров `AssignIdentityParameterSet` был удален.</span><span class="sxs-lookup"><span data-stu-id="24766-172">The parameter set `AssignIdentityParameterSet` has been removed.</span></span>

### `Remove-AzVmssDataDisk`

<span data-ttu-id="24766-173">Тип свойства `AutomaticRepairsPolicy` типа `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` был изменен с `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` на `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="24766-173">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Remove-AzVmssExtension`

<span data-ttu-id="24766-174">Тип свойства `AutomaticRepairsPolicy` типа `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` был изменен с `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` на `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="24766-174">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Remove-AzVmssNetworkInterfaceConfiguration`

<span data-ttu-id="24766-175">Тип свойства `AutomaticRepairsPolicy` типа `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` был изменен с `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` на `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="24766-175">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssBootDiagnostic`

<span data-ttu-id="24766-176">Тип свойства `AutomaticRepairsPolicy` типа `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` был изменен с `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` на `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="24766-176">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssOsProfile`

<span data-ttu-id="24766-177">Тип свойства `AutomaticRepairsPolicy` типа `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` был изменен с `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` на `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="24766-177">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssRollingUpgradePolicy`

<span data-ttu-id="24766-178">Тип свойства `AutomaticRepairsPolicy` типа `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` был изменен с `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` на `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="24766-178">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssStorageProfile`

<span data-ttu-id="24766-179">Тип свойства `AutomaticRepairsPolicy` типа `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` был изменен с `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` на `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="24766-179">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `New-AzVmss`

<span data-ttu-id="24766-180">Тип свойства `AutomaticRepairsPolicy` типа `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` был изменен с `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` на `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="24766-180">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Repair-AzVmssServiceFabricUpdateDomain`

<span data-ttu-id="24766-181">Тип свойства `AutomaticRepairsPolicy` типа `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` был изменен с `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` на `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="24766-181">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Get-AzVmss`

<span data-ttu-id="24766-182">Тип свойства `AutomaticRepairsPolicy` типа `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` был изменен с `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` на `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="24766-182">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Set-AzVmssOrchestrationServiceState`

<span data-ttu-id="24766-183">Тип свойства `AutomaticRepairsPolicy` типа `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` был изменен с `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` на `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="24766-183">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Update-AzVmss`

- <span data-ttu-id="24766-184">Тип свойства `AutomaticRepairsPolicy` типа `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` был изменен с `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` на `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="24766-184">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>
- <span data-ttu-id="24766-185">Больше не поддерживает параметр `AutomaticRepairMaxInstanceRepairsPercent`, и для исходного имени параметра не найден псевдоним.</span><span class="sxs-lookup"><span data-stu-id="24766-185">No longer supports the parameter `AutomaticRepairMaxInstanceRepairsPercent` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="24766-186">Набор параметров `__AllParameterSets` был удален.</span><span class="sxs-lookup"><span data-stu-id="24766-186">The parameter set `__AllParameterSets` has been removed.</span></span>
- <span data-ttu-id="24766-187">Набор параметров `ExplicitIdentityParameterSet` был удален.</span><span class="sxs-lookup"><span data-stu-id="24766-187">The parameter set `ExplicitIdentityParameterSet` has been removed.</span></span>

### `Add-AzVmssDiagnosticsExtension`

<span data-ttu-id="24766-188">Тип свойства `AutomaticRepairsPolicy` типа `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` был изменен с `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` на `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="24766-188">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

### `Disable-AzVmssDiskEncryption`

<span data-ttu-id="24766-189">Тип свойства `AutomaticRepairsPolicy` типа `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` был изменен с `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` на `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span><span class="sxs-lookup"><span data-stu-id="24766-189">The type of property `AutomaticRepairsPolicy` of type `Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet` has changed from `Microsoft.Azure.Commands.Compute.Automation.Models.PSAutomaticRepairsPolicy` to `Microsoft.Azure.Management.Compute.Models.AutomaticRepairsPolicy`.</span></span>

## <a name="azkeyvault"></a><span data-ttu-id="24766-190">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="24766-190">Az.KeyVault</span></span>

### `New-AzKeyVaultCertificateOrganizationDetail`

<span data-ttu-id="24766-191">Псевдоним `New-AzKeyVaultCertificateOrganizationDetails` был удален.</span><span class="sxs-lookup"><span data-stu-id="24766-191">The alias `New-AzKeyVaultCertificateOrganizationDetails` is removed.</span></span> <span data-ttu-id="24766-192">Используйте `New-AzKeyVaultCertificateOrganizationDetail`.</span><span class="sxs-lookup"><span data-stu-id="24766-192">Please use `New-AzKeyVaultCertificateOrganizationDetail`.</span></span>

#### <a name="before"></a><span data-ttu-id="24766-193">Перед</span><span class="sxs-lookup"><span data-stu-id="24766-193">Before</span></span>

```powershell
PS C:\> New-AzKeyVaultCertificateOrganizationDetails -AdministratorDetails $AdminDetails
```

#### <a name="after"></a><span data-ttu-id="24766-194">После</span><span class="sxs-lookup"><span data-stu-id="24766-194">After</span></span>

```powershell
PS C:\> New-AzKeyVaultCertificateOrganizationDetail -AdministratorDetails $AdminDetails
```

### `New-AzKeyVaultCertificateAdministratorDetail`

<span data-ttu-id="24766-195">Псевдоним `New-AzKeyVaultCertificateAdministratorDetails` был удален.</span><span class="sxs-lookup"><span data-stu-id="24766-195">The alias `New-AzKeyVaultCertificateAdministratorDetails` is removed.</span></span> <span data-ttu-id="24766-196">Используйте `New-AzKeyVaultCertificateAdministratorDetail`.</span><span class="sxs-lookup"><span data-stu-id="24766-196">Please use `New-AzKeyVaultCertificateAdministratorDetail`.</span></span>

#### <a name="before"></a><span data-ttu-id="24766-197">Перед</span><span class="sxs-lookup"><span data-stu-id="24766-197">Before</span></span>

```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetails -FirstName 'Patti' -LastName 'Fuller' -EmailAddress 'patti.fuller@contoso.com' -PhoneNumber '5553334444'
```

#### <a name="after"></a><span data-ttu-id="24766-198">После</span><span class="sxs-lookup"><span data-stu-id="24766-198">After</span></span>

```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName 'Patti' -LastName 'Fuller' -EmailAddress 'patti.fuller@contoso.com' -PhoneNumber '5553334444'
```

### `New-AzKeyVault`

<span data-ttu-id="24766-199">`-EnableSoftDelete` был удален, так как обратимое удаление включено по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="24766-199">`-EnableSoftDelete` is removed, as soft delete is enabled by default.</span></span> <span data-ttu-id="24766-200">Используйте `-DisableSoftDelete`, если такое поведение не требуется.</span><span class="sxs-lookup"><span data-stu-id="24766-200">Please use `-DisableSoftDelete` if you do not want this behavior.</span></span>

#### <a name="before"></a><span data-ttu-id="24766-201">Перед</span><span class="sxs-lookup"><span data-stu-id="24766-201">Before</span></span>

```powershell
PS C:\> New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -EnableSoftDelete
```

#### <a name="after"></a><span data-ttu-id="24766-202">После</span><span class="sxs-lookup"><span data-stu-id="24766-202">After</span></span>

```powershell
PS C:\> New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US'
```

## <a name="azmonitor"></a><span data-ttu-id="24766-203">Az.Monitor</span><span class="sxs-lookup"><span data-stu-id="24766-203">Az.Monitor</span></span>

### `Add-AzLogProfile`

<span data-ttu-id="24766-204">Тип свойства `RetentionPolicy` типа `Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` был изменен с `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy` на `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy`.</span><span class="sxs-lookup"><span data-stu-id="24766-204">The type of property `RetentionPolicy` of type `Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` has changed from `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy` to `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy`.</span></span>

### `Get-AzLogProfile`

<span data-ttu-id="24766-205">Тип свойства `RetentionPolicy` типа `Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` был изменен с `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy` на `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy`.</span><span class="sxs-lookup"><span data-stu-id="24766-205">The type of property `RetentionPolicy` of type `Microsoft.Azure.Commands.Insights.OutputClasses.PSLogProfile` has changed from `Microsoft.Azure.Management.Monitor.Management.Models.RetentionPolicy` to `Microsoft.Azure.Management.Monitor.Models.RetentionPolicy`.</span></span>

### `New-AzMetricAlertRuleV2Criteria`

<span data-ttu-id="24766-206">Набор параметров `__AllParameterSets` для командлета `New-AzMetricAlertRuleV2Criteria` был удален.</span><span class="sxs-lookup"><span data-stu-id="24766-206">The parameter set `__AllParameterSets` for cmdlet `New-AzMetricAlertRuleV2Criteria` has been removed.</span></span>

## <a name="aznetwork"></a><span data-ttu-id="24766-207">Az.Network</span><span class="sxs-lookup"><span data-stu-id="24766-207">Az.Network</span></span>

### `Get-AzNetworkWatcherConnectionMonitor`

<span data-ttu-id="24766-208">Универсальный тип свойства `RoundTripTimeMs` был изменен с `System.Nullable1[System.Int32]` на `System.Nullable1[System.Double]`.</span><span class="sxs-lookup"><span data-stu-id="24766-208">The generic type for property `RoundTripTimeMs` has been changed from `System.Nullable1[System.Int32]` to `System.Nullable1[System.Double]`.</span></span>

### `New-AzNetworkWatcherConnectionMonitorTestConfigurationObject`

<span data-ttu-id="24766-209">Универсальный тип параметра `SuccessThresholdRoundTripTimeMs` был изменен с `System.Nullable1[System.Int32]` на `System.Nullable1[System.Double]`.</span><span class="sxs-lookup"><span data-stu-id="24766-209">The generic type for parameter `SuccessThresholdRoundTripTimeMs` has been changed from `System.Nullable1[System.Int32]` to `System.Nullable1[System.Double]`.</span></span>

## <a name="azoperationalinsights"></a><span data-ttu-id="24766-210">Az.OperationalInsights</span><span class="sxs-lookup"><span data-stu-id="24766-210">Az.OperationalInsights</span></span>

### `Get-AzOperationalInsightsDataSource`

<span data-ttu-id="24766-211">Свойство `PortalUrl` типа `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` удалено.</span><span class="sxs-lookup"><span data-stu-id="24766-211">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsApplicationInsightsDataSource`

<span data-ttu-id="24766-212">Свойство `PortalUrl` типа `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` удалено.</span><span class="sxs-lookup"><span data-stu-id="24766-212">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsAzureActivityLogDataSource`

<span data-ttu-id="24766-213">Свойство `PortalUrl` типа `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` удалено.</span><span class="sxs-lookup"><span data-stu-id="24766-213">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsCustomLogDataSource`

<span data-ttu-id="24766-214">Свойство `PortalUrl` типа `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` удалено.</span><span class="sxs-lookup"><span data-stu-id="24766-214">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsLinuxPerformanceObjectDataSource`

<span data-ttu-id="24766-215">Свойство `PortalUrl` типа `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` удалено.</span><span class="sxs-lookup"><span data-stu-id="24766-215">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsLinuxSyslogDataSource`

<span data-ttu-id="24766-216">Свойство `PortalUrl` типа `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` удалено.</span><span class="sxs-lookup"><span data-stu-id="24766-216">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsWindowsEventDataSource`

<span data-ttu-id="24766-217">Свойство `PortalUrl` типа `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` удалено.</span><span class="sxs-lookup"><span data-stu-id="24766-217">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsWindowsPerformanceCounterDataSource`

<span data-ttu-id="24766-218">Свойство `PortalUrl` типа `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` удалено.</span><span class="sxs-lookup"><span data-stu-id="24766-218">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Remove-AzOperationalInsightsDataSource`

<span data-ttu-id="24766-219">Свойство `PortalUrl` типа `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` удалено.</span><span class="sxs-lookup"><span data-stu-id="24766-219">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Disable-AzOperationalInsightsIISLogCollection`

<span data-ttu-id="24766-220">Свойство `PortalUrl` типа `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` удалено.</span><span class="sxs-lookup"><span data-stu-id="24766-220">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Disable-AzOperationalInsightsLinuxCustomLogCollection`

<span data-ttu-id="24766-221">Свойство `PortalUrl` типа `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` удалено.</span><span class="sxs-lookup"><span data-stu-id="24766-221">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Disable-AzOperationalInsightsLinuxPerformanceCollection`

<span data-ttu-id="24766-222">Свойство `PortalUrl` типа `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` удалено.</span><span class="sxs-lookup"><span data-stu-id="24766-222">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Disable-AzOperationalInsightsLinuxSyslogCollection`

<span data-ttu-id="24766-223">Свойство `PortalUrl` типа `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` удалено.</span><span class="sxs-lookup"><span data-stu-id="24766-223">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Enable-AzOperationalInsightsIISLogCollection`

<span data-ttu-id="24766-224">Свойство `PortalUrl` типа `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` удалено.</span><span class="sxs-lookup"><span data-stu-id="24766-224">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Enable-AzOperationalInsightsLinuxCustomLogCollection`

<span data-ttu-id="24766-225">Свойство `PortalUrl` типа `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` удалено.</span><span class="sxs-lookup"><span data-stu-id="24766-225">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Enable-AzOperationalInsightsLinuxPerformanceCollection`

<span data-ttu-id="24766-226">Свойство `PortalUrl` типа `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` удалено.</span><span class="sxs-lookup"><span data-stu-id="24766-226">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Enable-AzOperationalInsightsLinuxSyslogCollection`

<span data-ttu-id="24766-227">Свойство `PortalUrl` типа `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` удалено.</span><span class="sxs-lookup"><span data-stu-id="24766-227">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Get-AzOperationalInsightsSavedSearch`

<span data-ttu-id="24766-228">Свойство `Metadata` типа `Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse` удалено.</span><span class="sxs-lookup"><span data-stu-id="24766-228">The property `Metadata` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchListSavedSearchResponse` has been removed.</span></span>

### `Get-AzOperationalInsightsSavedSearchResult`

<span data-ttu-id="24766-229">Командлет `Get-AzOperationalInsightsSavedSearchResult` больше не поддерживался пакетом SDK и был удален.</span><span class="sxs-lookup"><span data-stu-id="24766-229">The cmdlet `Get-AzOperationalInsightsSavedSearchResult` was not supported by SDK anymore and has been removed.</span></span>

### `Get-AzOperationalInsightsSearchResult`

<span data-ttu-id="24766-230">Командлет `Get-AzOperationalInsightsSearchResult` больше не поддерживался пакетом SDK и был удален.</span><span class="sxs-lookup"><span data-stu-id="24766-230">The cmdlet `Get-AzOperationalInsightsSearchResult` was not supported by SDK anymore and has been removed.</span></span>

### `Get-AzOperationalInsightsStorageInsight`

<span data-ttu-id="24766-231">Свойство `PortalUrl` типа `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` удалено.</span><span class="sxs-lookup"><span data-stu-id="24766-231">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsStorageInsight`

<span data-ttu-id="24766-232">Свойство `PortalUrl` типа `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` удалено.</span><span class="sxs-lookup"><span data-stu-id="24766-232">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Remove-AzOperationalInsightsStorageInsight`

<span data-ttu-id="24766-233">Свойство `PortalUrl` типа `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` удалено.</span><span class="sxs-lookup"><span data-stu-id="24766-233">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Set-AzOperationalInsightsStorageInsight`

<span data-ttu-id="24766-234">Свойство `PortalUrl` типа `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` удалено.</span><span class="sxs-lookup"><span data-stu-id="24766-234">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Get-AzOperationalInsightsLinkTarget`

<span data-ttu-id="24766-235">Командлет `Get-AzOperationalInsightsLinkTarget` больше не поддерживался пакетом SDK и был удален.</span><span class="sxs-lookup"><span data-stu-id="24766-235">The cmdlet `Get-AzOperationalInsightsLinkTarget` was not supported by SDK anymore and has been removed.</span></span>

### `Get-AzOperationalInsightsWorkspace`

<span data-ttu-id="24766-236">Свойство `PortalUrl` типа `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` удалено.</span><span class="sxs-lookup"><span data-stu-id="24766-236">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `New-AzOperationalInsightsWorkspace`

- <span data-ttu-id="24766-237">Свойство `PortalUrl` типа `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` удалено.</span><span class="sxs-lookup"><span data-stu-id="24766-237">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>
- <span data-ttu-id="24766-238">Командлет `New-AzOperationalInsightsWorkspace` больше не поддерживает параметр `CustomerId`, и для исходного имени параметра не найден псевдоним.</span><span class="sxs-lookup"><span data-stu-id="24766-238">The cmdlet `New-AzOperationalInsightsWorkspace` no longer supports the parameter `CustomerId` and no alias was found for the original parameter name.</span></span>
- <span data-ttu-id="24766-239">Набор параметров `__AllParameterSets` для командлета `New-AzOperationalInsightsWorkspace` был удален.</span><span class="sxs-lookup"><span data-stu-id="24766-239">The parameter set `__AllParameterSets` for cmdlet `New-AzOperationalInsightsWorkspace` has been removed.</span></span>

### `Set-AzOperationalInsightsWorkspace`

<span data-ttu-id="24766-240">Свойство `PortalUrl` типа `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` удалено.</span><span class="sxs-lookup"><span data-stu-id="24766-240">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

### `Invoke-AzOperationalInsightsQuery`

<span data-ttu-id="24766-241">Свойство `PortalUrl` типа `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` удалено.</span><span class="sxs-lookup"><span data-stu-id="24766-241">The property `PortalUrl` of type `Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace` has been removed.</span></span>

## <a name="azresources"></a><span data-ttu-id="24766-242">Az.Resources</span><span class="sxs-lookup"><span data-stu-id="24766-242">Az.Resources</span></span>

### `Get-AzDeploymentScript`

<span data-ttu-id="24766-243">Тип свойства `Status` типа `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` был изменен с `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` на `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span><span class="sxs-lookup"><span data-stu-id="24766-243">The type of property `Status` of type `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` has changed from `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` to `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span></span>

### `Get-AzDeploymentScriptLog`

<span data-ttu-id="24766-244">Тип свойства `Status` типа `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` был изменен с `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` на `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span><span class="sxs-lookup"><span data-stu-id="24766-244">The type of property `Status` of type `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` has changed from `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` to `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span></span>

### `Save-AzDeploymentScriptLog`

<span data-ttu-id="24766-245">Тип свойства `Status` типа `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` был изменен с `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` на `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span><span class="sxs-lookup"><span data-stu-id="24766-245">The type of property `Status` of type `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` has changed from `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` to `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span></span>

### `Get-AzResourceLock, New-AzResourceLock, Remove-AzResourceLock, Set-AzResourceLock`

<span data-ttu-id="24766-246">Параметр `TenantLevel` был удален.</span><span class="sxs-lookup"><span data-stu-id="24766-246">Parameter `TenantLevel` has been removed.</span></span>

### `Get-AzPolicyAlias`

<span data-ttu-id="24766-247">Универсальный тип свойства `Aliases` был изменен с `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.AliasType]` на `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.Alias]`.</span><span class="sxs-lookup"><span data-stu-id="24766-247">The generic type for property `Aliases` has been changed from `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.AliasType]` to `System.Collections.Generic.IList1[Microsoft.Azure.Management.ResourceManager.Models.Alias]`.</span></span>

### `New-AzPolicyAssignment`

- <span data-ttu-id="24766-248">Командлет `New-AzPolicyAssignment` больше не поддерживает тип `System.Management.Automation.PSObject` параметра `PolicyDefinition`.</span><span class="sxs-lookup"><span data-stu-id="24766-248">The cmdlet `New-AzPolicyAssignment` no longer supports the type `System.Management.Automation.PSObject` for parameter `PolicyDefinition`.</span></span>
- <span data-ttu-id="24766-249">Командлет `New-AzPolicyAssignment` больше не поддерживает тип `System.Management.Automation.PSObject` параметра `PolicySetDefinition`.</span><span class="sxs-lookup"><span data-stu-id="24766-249">The cmdlet `New-AzPolicyAssignment` no longer supports the type `System.Management.Automation.PSObject` for parameter `PolicySetDefinition`.</span></span>

### `Remove-AzDeploymentScript`

<span data-ttu-id="24766-250">Тип свойства `Status` типа `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` был изменен с `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` на `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span><span class="sxs-lookup"><span data-stu-id="24766-250">The type of property `Status` of type `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript` has changed from `Microsoft.Azure.Management.ResourceManager.Models.ScriptStatus` to `Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsScriptStatus`.</span></span>

## <a name="azstorage"></a><span data-ttu-id="24766-251">Az.Storage</span><span class="sxs-lookup"><span data-stu-id="24766-251">Az.Storage</span></span>

### <a name="update-azstorageaccountnetworkruleset-get-azstorageaccountnetworkruleset"></a><span data-ttu-id="24766-252">`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`</span><span class="sxs-lookup"><span data-stu-id="24766-252">`Update-AzStorageAccountNetworkRuleSet`, `Get-AzStorageAccountNetworkRuleSet`</span></span>

<span data-ttu-id="24766-253">Значение NetWorkRule DefaultAction изменено: с Allow = 1 и Deny = 0 на Allow = 0 и Deny = 1.</span><span class="sxs-lookup"><span data-stu-id="24766-253">Changed NetWorkRule DefaultAction value from: Allow = 1, Deny = 0, to: Allow = 0, Deny = 1.</span></span>

### <a name="new-azstoragetable-get-azstoragetable"></a><span data-ttu-id="24766-254">`New-AzStorageTable`, `Get-AzStorageTable`</span><span class="sxs-lookup"><span data-stu-id="24766-254">`New-AzStorageTable`, `Get-AzStorageTable`</span></span>

<span data-ttu-id="24766-255">Для выходного объекта AzureStorageTable.CloudTable.ServiceClient были удалены два свойства: ConnectionPolicy, ConsistencyLevel.</span><span class="sxs-lookup"><span data-stu-id="24766-255">Output object AzureStorageTable.CloudTable.ServiceClient have 2 properties removed: ConnectionPolicy, ConsistencyLevel.</span></span>

### <a name="get-azstoragefile-remove-azstoragefile-get-azstoragefilecontent-set-azstoragefilecontent-start-azstoragefilecopy"></a><span data-ttu-id="24766-256">`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`</span><span class="sxs-lookup"><span data-stu-id="24766-256">`Get-AzStorageFile`, `Remove-AzStorageFile`, `Get-AzStorageFileContent`, `Set-AzStorageFileContent`, `Start-AzStorageFileCopy`</span></span>

<span data-ttu-id="24766-257">Тип выходных данных изменен с CloudFile на AzureStorageFile. Исходные выходные данные теперь становятся дочерним свойством CloudFile нового типа выходных данных.</span><span class="sxs-lookup"><span data-stu-id="24766-257">Change output type from CloudFile to AzureStorageFile, the original output will become child property "CloudFile" of the new output</span></span>

#### <a name="before"></a><span data-ttu-id="24766-258">Перед</span><span class="sxs-lookup"><span data-stu-id="24766-258">Before</span></span>

```powershell
PS C:\> $file = Get-AzStorageFile -ShareName $shareName -Path testfile -Context $ctx

PS C:\> Remove-AzStorageFile -File $file
```

#### <a name="after"></a><span data-ttu-id="24766-259">После</span><span class="sxs-lookup"><span data-stu-id="24766-259">After</span></span>

```powershell
PS C:\> $file = Get-AzStorageFile -ShareName $shareName -Path testfile -Context $ctx

PS C:\> Remove-AzStorageFile -File $file.CloudFile
```

### <a name="get-azstoragefile-new-azstoragedirectory-remove-azstoragedirectory"></a><span data-ttu-id="24766-260">`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`</span><span class="sxs-lookup"><span data-stu-id="24766-260">`Get-AzStorageFile`, `New-AzStorageDirectory`, `Remove-AzStorageDirectory`</span></span>

<span data-ttu-id="24766-261">Тип выходных данных изменен с CloudFileDirectory на AzureStorageFileDirectory. Исходные выходные данные теперь становятся дочерним свойством CloudFileDirectory нового типа выходных данных.</span><span class="sxs-lookup"><span data-stu-id="24766-261">Change output type from CloudFileDirectory to AzureStorageFileDirectory, the original output will become child property "CloudFileDirectory" of the new output</span></span>

#### <a name="before"></a><span data-ttu-id="24766-262">Перед</span><span class="sxs-lookup"><span data-stu-id="24766-262">Before</span></span>

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> Remove-AzStorageDirectory -Directory $dir
```

#### <a name="after"></a><span data-ttu-id="24766-263">После</span><span class="sxs-lookup"><span data-stu-id="24766-263">After</span></span>

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> Remove-AzStorageDirectory -Directory $dir.CloudFileDirectory
```

### <a name="get-azstorageshare-new-azstorageshare-remove-azstorageshare"></a><span data-ttu-id="24766-264">`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`</span><span class="sxs-lookup"><span data-stu-id="24766-264">`Get-AzStorageShare`, `New-AzStorageShare`, `Remove-AzStorageShare`</span></span>

<span data-ttu-id="24766-265">Тип выходных данных изменен с FileShareProperties на AzureStorageFileShare. Исходные выходные данные теперь становятся дочерним свойством CloudFileShare нового типа выходных данных.</span><span class="sxs-lookup"><span data-stu-id="24766-265">Change output type from FileShareProperties to AzureStorageFileShare, the original output will become child property "CloudFileShare" of the new output</span></span>

#### <a name="before"></a><span data-ttu-id="24766-266">Перед</span><span class="sxs-lookup"><span data-stu-id="24766-266">Before</span></span>

```powershell
PS C:\> $share = Get-AzStorageShare -Name $shareName -Context $ctx

PS C:\> Remove-AzStorageShare -Share $share
```

#### <a name="after"></a><span data-ttu-id="24766-267">После</span><span class="sxs-lookup"><span data-stu-id="24766-267">After</span></span>

```powershell
PS C:\> $share = Get-AzStorageShare -Name $shareName -Context $ctx

PS C:\> Remove-AzStorageShare -Share $share.CloudFileShare
```

### `Set-AzStorageShareQuota`

<span data-ttu-id="24766-268">Тип выходных данных изменен с FileShareProperties на AzureStorageFileShare. Исходные выходные данные теперь становятся вложенным дочерним свойством CloudFileShare.Properties нового типа выходных данных.</span><span class="sxs-lookup"><span data-stu-id="24766-268">Change output type from FileShareProperties to AzureStorageFileShare, the original output will become sub child property ""CloudFileShare.Properties"" of the new output</span></span>

#### <a name="before"></a><span data-ttu-id="24766-269">Перед</span><span class="sxs-lookup"><span data-stu-id="24766-269">Before</span></span>

```powershell
PS C:\> $shareProperties = Set-AzStorageShareQuota -Name $shareName -Quota 100 -Context $ctx

PS C:\> $shareProperties

ETag                LastModified                Quota
----                ------------                -----
"0x8D7F5BC7789FC63" 5/11/2020 3:03:30 PM +00:00   100
```

#### <a name="after"></a><span data-ttu-id="24766-270">После</span><span class="sxs-lookup"><span data-stu-id="24766-270">After</span></span>

```powershell
PS C:\> $share = Set-AzStorageShareQuota -Name $shareName -Quota 100 -Context $ctx

PS C:\> $share

   File End Point: https://weiors1.file.core.windows.net/

Name     QuotaGiB LastModified                IsSnapshot SnapshotTime
----     -------- ------------                ---------- ------------
weitest1 100      5/11/2020 3:03:30 PM +00:00 False

PS C:\> $share.CloudFileShare.Properties

ETag                LastModified                Quota
----                ------------                -----
"0x8D7F5BC7789FC63" 5/11/2020 3:03:30 PM +00:00   100
```

### `Remove-AzStorageDirectory`

<span data-ttu-id="24766-271">При удалении вложенных каталогов с родительским объектом каталога и параметром -Path больше не удается использовать параметр -Path из конвейера с сопоставлением типа (строка).</span><span class="sxs-lookup"><span data-stu-id="24766-271">When removing sub File Directories with parent Directory object and -Path, Can't input -Path from pipeline with type (string) match anymore.</span></span>

#### <a name="before"></a><span data-ttu-id="24766-272">Перед</span><span class="sxs-lookup"><span data-stu-id="24766-272">Before</span></span>

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> @('dir1', 'dir2') | Remove-AzStorageDirectory -Directory $dir
```

#### <a name="after"></a><span data-ttu-id="24766-273">После</span><span class="sxs-lookup"><span data-stu-id="24766-273">After</span></span>

```powershell
PS C:\> $dir = Get-AzStorageFile -ShareName $shareName -Path testdir -Context $ctx

PS C:\> $paths = @(
    [PSCustomObject]@{  Path = 'dir1 }
    [PSCustomObject]@{ Path = 'dir2' }
)

PS C:\> $paths | Remove-AzStorageDirectory -Directory $dir.CloudFileDirectory
```
