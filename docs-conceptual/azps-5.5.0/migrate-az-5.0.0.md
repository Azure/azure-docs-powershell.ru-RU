---
title: Руководство по миграции на Az 5.0.0
description: Это руководство по миграции содержит список критических изменений, внесенных в версию Az 5.0.0 в Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/27/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: edfbe14ae3a42bb0b385fe9d6b5fa681a1aa2101
ms.sourcegitcommit: 608289d079b819df2b8d1a2f7935cc500367a312
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "101684922"
---
# <a name="migration-guide-for-az-500"></a><span data-ttu-id="7a4ca-103">Руководство по миграции на Az 5.0.0</span><span class="sxs-lookup"><span data-stu-id="7a4ca-103">Migration Guide for Az 5.0.0</span></span>

<span data-ttu-id="7a4ca-104">В этом документе описаны отличия между версиями Az 4.0.0 и 5.0.0.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-104">This document describes the changes between the 4.0.0 and 5.0.0 versions of Az.</span></span>

- [<span data-ttu-id="7a4ca-105">Руководство по миграции на Az 5.0.0</span><span class="sxs-lookup"><span data-stu-id="7a4ca-105">Migration Guide for Az 5.0.0</span></span>](#migration-guide-for-az-500)
  - [<span data-ttu-id="7a4ca-106">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="7a4ca-106">Az.Aks</span></span>](#azaks)
    - [<span data-ttu-id="7a4ca-107">New-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="7a4ca-107">New-AzAksCluster</span></span>](#new-azakscluster)
    - [<span data-ttu-id="7a4ca-108">Set-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="7a4ca-108">Set-AzAksCluster</span></span>](#set-azakscluster)
  - [<span data-ttu-id="7a4ca-109">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="7a4ca-109">Az.ContainerRegistry</span></span>](#azcontainerregistry)
    - [<span data-ttu-id="7a4ca-110">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="7a4ca-110">New-AzContainerRegistry</span></span>](#new-azcontainerregistry)
  - [<span data-ttu-id="7a4ca-111">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="7a4ca-111">Az.Functions</span></span>](#azfunctions)
    - [<span data-ttu-id="7a4ca-112">Get-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="7a4ca-112">Get-AzFunctionApp</span></span>](#get-azfunctionapp)
    - [<span data-ttu-id="7a4ca-113">New-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="7a4ca-113">New-AzFunctionApp</span></span>](#new-azfunctionapp)
  - [<span data-ttu-id="7a4ca-114">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7a4ca-114">Az.KeyVault</span></span>](#azkeyvault)
    - [<span data-ttu-id="7a4ca-115">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="7a4ca-115">New-AzKeyVault</span></span>](#new-azkeyvault)
    - [<span data-ttu-id="7a4ca-116">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="7a4ca-116">Update-AzKeyVault</span></span>](#update-azkeyvault)
    - [<span data-ttu-id="7a4ca-117">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="7a4ca-117">Get-AzKeyVaultSecret</span></span>](#get-azkeyvaultsecret)
  - [<span data-ttu-id="7a4ca-118">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="7a4ca-118">Az.ManagedServices</span></span>](#azmanagedservices)
    - [<span data-ttu-id="7a4ca-119">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="7a4ca-119">Get-AzManagedServicesDefinition</span></span>](#get-azmanagedservicesdefinition)
    - [<span data-ttu-id="7a4ca-120">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="7a4ca-120">New-AzManagedServicesAssignment</span></span>](#new-azmanagedservicesassignment)
    - [<span data-ttu-id="7a4ca-121">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="7a4ca-121">Remove-AzManagedServicesAssignment</span></span>](#remove-azmanagedservicesassignment)
    - [<span data-ttu-id="7a4ca-122">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="7a4ca-122">Remove-AzManagedServicesDefinition</span></span>](#remove-azmanagedservicesdefinition)
  - [<span data-ttu-id="7a4ca-123">Az.ResourceManager</span><span class="sxs-lookup"><span data-stu-id="7a4ca-123">Az.ResourceManager</span></span>](#azresourcemanager)
    - [<span data-ttu-id="7a4ca-124">Get-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="7a4ca-124">Get-AzManagementGroupDeployment</span></span>](#get-azmanagementgroupdeployment)
    - [<span data-ttu-id="7a4ca-125">Get-AzManagementGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="7a4ca-125">Get-AzManagementGroupDeploymentOperation</span></span>](#get-azmanagementgroupdeploymentoperation)
    - [<span data-ttu-id="7a4ca-126">Get-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="7a4ca-126">Get-AzDeployment</span></span>](#get-azdeployment)
    - [<span data-ttu-id="7a4ca-127">Get-AzDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="7a4ca-127">Get-AzDeploymentOperation</span></span>](#get-azdeploymentoperation)
    - [<span data-ttu-id="7a4ca-128">Get-AzDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="7a4ca-128">Get-AzDeploymentWhatIfResult</span></span>](#get-azdeploymentwhatifresult)
    - [<span data-ttu-id="7a4ca-129">Get-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="7a4ca-129">Get-AzTenantDeployment</span></span>](#get-aztenantdeployment)
    - [<span data-ttu-id="7a4ca-130">Get-AzTenantDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="7a4ca-130">Get-AzTenantDeploymentOperation</span></span>](#get-aztenantdeploymentoperation)
    - [<span data-ttu-id="7a4ca-131">New-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="7a4ca-131">New-AzManagementGroupDeployment</span></span>](#new-azmanagementgroupdeployment)
    - [<span data-ttu-id="7a4ca-132">New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="7a4ca-132">New-AzDeployment</span></span>](#new-azdeployment)
    - [<span data-ttu-id="7a4ca-133">New-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="7a4ca-133">New-AzTenantDeployment</span></span>](#new-aztenantdeployment)
    - [<span data-ttu-id="7a4ca-134">Remove-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="7a4ca-134">Remove-AzManagementGroupDeployment</span></span>](#remove-azmanagementgroupdeployment)
    - [<span data-ttu-id="7a4ca-135">Remove-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="7a4ca-135">Remove-AzDeployment</span></span>](#remove-azdeployment)
    - [<span data-ttu-id="7a4ca-136">Remove-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="7a4ca-136">Remove-AzTenantDeployment</span></span>](#remove-aztenantdeployment)
    - [<span data-ttu-id="7a4ca-137">Save-AzManagementGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="7a4ca-137">Save-AzManagementGroupDeploymentTemplate</span></span>](#save-azmanagementgroupdeploymenttemplate)
    - [<span data-ttu-id="7a4ca-138">Save-AzDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="7a4ca-138">Save-AzDeploymentTemplate</span></span>](#save-azdeploymenttemplate)
    - [<span data-ttu-id="7a4ca-139">Save-AzTenantDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="7a4ca-139">Save-AzTenantDeploymentTemplate</span></span>](#save-aztenantdeploymenttemplate)
    - [<span data-ttu-id="7a4ca-140">Stop-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="7a4ca-140">Stop-AzManagementGroupDeployment</span></span>](#stop-azmanagementgroupdeployment)
    - [<span data-ttu-id="7a4ca-141">Stop-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="7a4ca-141">Stop-AzDeployment</span></span>](#stop-azdeployment)
    - [<span data-ttu-id="7a4ca-142">Stop-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="7a4ca-142">Stop-AzTenantDeployment</span></span>](#stop-aztenantdeployment)
    - [<span data-ttu-id="7a4ca-143">Test-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="7a4ca-143">Test-AzManagementGroupDeployment</span></span>](#test-azmanagementgroupdeployment)
    - [<span data-ttu-id="7a4ca-144">Test-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="7a4ca-144">Test-AzDeployment</span></span>](#test-azdeployment)
    - [<span data-ttu-id="7a4ca-145">Test-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="7a4ca-145">Test-AzTenantDeployment</span></span>](#test-aztenantdeployment)
    - [<span data-ttu-id="7a4ca-146">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="7a4ca-146">Get-AzResourceGroupDeployment</span></span>](#get-azresourcegroupdeployment)
    - [<span data-ttu-id="7a4ca-147">Get-AzResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="7a4ca-147">Get-AzResourceGroupDeploymentOperation</span></span>](#get-azresourcegroupdeploymentoperation)
    - [<span data-ttu-id="7a4ca-148">Get-AzResourceGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="7a4ca-148">Get-AzResourceGroupDeploymentWhatIfResult</span></span>](#get-azresourcegroupdeploymentwhatifresult)
    - [<span data-ttu-id="7a4ca-149">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="7a4ca-149">New-AzResourceGroupDeployment</span></span>](#new-azresourcegroupdeployment)
    - [<span data-ttu-id="7a4ca-150">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="7a4ca-150">Remove-AzResourceGroupDeployment</span></span>](#remove-azresourcegroupdeployment)
    - [<span data-ttu-id="7a4ca-151">Save-AzResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="7a4ca-151">Save-AzResourceGroupDeploymentTemplate</span></span>](#save-azresourcegroupdeploymenttemplate)
    - [<span data-ttu-id="7a4ca-152">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="7a4ca-152">Stop-AzResourceGroupDeployment</span></span>](#stop-azresourcegroupdeployment)
    - [<span data-ttu-id="7a4ca-153">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="7a4ca-153">Test-AzResourceGroupDeployment</span></span>](#test-azresourcegroupdeployment)
    - [<span data-ttu-id="7a4ca-154">Get-AzManagementGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="7a4ca-154">Get-AzManagementGroupDeploymentWhatIfResult</span></span>](#get-azmanagementgroupdeploymentwhatifresult)
    - [<span data-ttu-id="7a4ca-155">Get-AzTenantDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="7a4ca-155">Get-AzTenantDeploymentWhatIfResult</span></span>](#get-aztenantdeploymentwhatifresult)
  - [<span data-ttu-id="7a4ca-156">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7a4ca-156">Az.Sql</span></span>](#azsql)
    - [<span data-ttu-id="7a4ca-157">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="7a4ca-157">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](#set-azsqlserveractivedirectoryadministrator)
  - [<span data-ttu-id="7a4ca-158">Az.Synapse</span><span class="sxs-lookup"><span data-stu-id="7a4ca-158">Az.Synapse</span></span>](#azsynapse)
    - [<span data-ttu-id="7a4ca-159">New-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="7a4ca-159">New-AzSynapseSqlPool</span></span>](#new-azsynapsesqlpool)
    - [<span data-ttu-id="7a4ca-160">Update-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="7a4ca-160">Update-AzSynapseSqlPool</span></span>](#update-azsynapsesqlpool)
  - [<span data-ttu-id="7a4ca-161">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7a4ca-161">Az.Network</span></span>](#aznetwork)
    - [<span data-ttu-id="7a4ca-162">Approve-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-162">Approve-AzPrivateEndpointConnection</span></span>](#approve-azprivateendpointconnection)
    - [<span data-ttu-id="7a4ca-163">Deny-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-163">Deny-AzPrivateEndpointConnection</span></span>](#deny-azprivateendpointconnection)
    - [<span data-ttu-id="7a4ca-164">Get-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-164">Get-AzPrivateEndpointConnection</span></span>](#get-azprivateendpointconnection)
    - [<span data-ttu-id="7a4ca-165">Remove-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-165">Remove-AzPrivateEndpointConnection</span></span>](#remove-azprivateendpointconnection)
    - [<span data-ttu-id="7a4ca-166">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7a4ca-166">Set-AzPrivateEndpointConnection</span></span>](#set-azprivateendpointconnection)
    - [<span data-ttu-id="7a4ca-167">New-AzNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="7a4ca-167">New-AzNetworkWatcherConnectionMonitorEndpointObject</span></span>](#new-aznetworkwatcherconnectionmonitorendpointobject)

## <a name="azaks"></a><span data-ttu-id="7a4ca-168">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="7a4ca-168">Az.Aks</span></span>

### <a name="new-azakscluster"></a><span data-ttu-id="7a4ca-169">New-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="7a4ca-169">New-AzAksCluster</span></span>

- <span data-ttu-id="7a4ca-170">Больше не поддерживает параметр `NodeOsType`; для исходного имени параметра не найден псевдоним (всегда будет `Linux`).</span><span class="sxs-lookup"><span data-stu-id="7a4ca-170">No longer supports the parameter `NodeOsType` and no alias was found for the original parameter name, it will always be `Linux`.</span></span>
- <span data-ttu-id="7a4ca-171">Больше не поддерживает псевдоним `ClientIdAndSecret` для параметра `ServicePrincipalIdAndSecret`.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-171">No longer supports the alias `ClientIdAndSecret` for parameter `ServicePrincipalIdAndSecret`.</span></span>
- <span data-ttu-id="7a4ca-172">Значение по умолчанию `NodeVmSetType` изменено с `AvailabilitySet` на `VirtualMachineScaleSets`.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-172">The default value of `NodeVmSetType` is changed from `AvailabilitySet` to `VirtualMachineScaleSets`.</span></span>
- <span data-ttu-id="7a4ca-173">Значение по умолчанию `NetworkPlugin` изменено с `none` на `azure`.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-173">The default value of `NetworkPlugin` is changed from `none` to `azure`.</span></span>

#### <a name="before"></a><span data-ttu-id="7a4ca-174">До</span><span class="sxs-lookup"><span data-stu-id="7a4ca-174">Before</span></span>

```powershell
New-AzAksCluster -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeOsType Linux -ClientIdAndSecret xxx
```

#### <a name="after"></a><span data-ttu-id="7a4ca-175">После</span><span class="sxs-lookup"><span data-stu-id="7a4ca-175">After</span></span>

```powershell
New-AzAksCluster -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NodeVmSetType AvailabilitySet  -ServicePrincipalIdAndSecret xxx
```

### <a name="set-azakscluster"></a><span data-ttu-id="7a4ca-176">Set-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="7a4ca-176">Set-AzAksCluster</span></span>

<span data-ttu-id="7a4ca-177">Больше не поддерживает псевдоним `ClientIdAndSecret` для параметра `ServicePrincipalIdAndSecret`.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-177">No longer supports the alias `ClientIdAndSecret` for parameter `ServicePrincipalIdAndSecret`.</span></span>

#### <a name="before"></a><span data-ttu-id="7a4ca-178">До</span><span class="sxs-lookup"><span data-stu-id="7a4ca-178">Before</span></span>

```powershell
Get-AzAksCluster -ResourceGroupName xxx -Name xxx | Set-AzAksCluster -ClientIdAndSecret xxx
```

#### <a name="after"></a><span data-ttu-id="7a4ca-179">После</span><span class="sxs-lookup"><span data-stu-id="7a4ca-179">After</span></span>

```powershell
Get-AzAksCluster -ResourceGroupName xxx -Name xxx | Set-AzAksCluster -ServicePrincipalIdAndSecret xxx
```

## <a name="azcontainerregistry"></a><span data-ttu-id="7a4ca-180">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="7a4ca-180">Az.ContainerRegistry</span></span>

### <a name="new-azcontainerregistry"></a><span data-ttu-id="7a4ca-181">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="7a4ca-181">New-AzContainerRegistry</span></span>

<span data-ttu-id="7a4ca-182">Больше не поддерживает параметр `StorageAccountName`, и для исходного имени параметра не найден псевдоним.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-182">No longer supports the parameter `StorageAccountName` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="7a4ca-183">До</span><span class="sxs-lookup"><span data-stu-id="7a4ca-183">Before</span></span>

```powershell
New-AzContainerRegistry -Name $name -ResourceGroupName $rg -Location $location -SKU Classic -StorageAccountName $storage
```

#### <a name="after"></a><span data-ttu-id="7a4ca-184">После</span><span class="sxs-lookup"><span data-stu-id="7a4ca-184">After</span></span>

<span data-ttu-id="7a4ca-185">Параметр `Classic` был устаревшим и параметр `StorageAccountName` был удален, так как он работает только с классическим Реестром контейнеров.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-185">`Classic` was deprecated and `StorageAccountName` was removed since it only works with Classic Container Registry.</span></span>

## <a name="azfunctions"></a><span data-ttu-id="7a4ca-186">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="7a4ca-186">Az.Functions</span></span>

### <a name="get-azfunctionapp"></a><span data-ttu-id="7a4ca-187">Get-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="7a4ca-187">Get-AzFunctionApp</span></span>

<span data-ttu-id="7a4ca-188">Параметр-переключатель `IncludeSlot` был удален из всех наборов параметров `Get-AzFunctionApp`, кроме одного.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-188">Removed `IncludeSlot` switch parameter from all but one parameter set of `Get-AzFunctionApp`.</span></span> <span data-ttu-id="7a4ca-189">Командлет теперь поддерживает получение слотов развертывания в результатах, если указать `-IncludeSlot`.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-189">The cmdlet now supports retrieving deployment slots in the results when `-IncludeSlot` is specified.</span></span>
<span data-ttu-id="7a4ca-190">Эта возможность была нарушена в предыдущей версии командлета,</span><span class="sxs-lookup"><span data-stu-id="7a4ca-190">This functionality was broken in the previous cmdlet version.</span></span> <span data-ttu-id="7a4ca-191">но сейчас она исправлена.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-191">However, this is now fixed.</span></span>

### <a name="new-azfunctionapp"></a><span data-ttu-id="7a4ca-192">New-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="7a4ca-192">New-AzFunctionApp</span></span>

- <span data-ttu-id="7a4ca-193">Исправлена проблема с `-DisableApplicationInsights` в `New-AzFunctionApp`, чтобы при указании этого параметра не создавался проект Application Insights.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-193">Fixed `-DisableApplicationInsights` in `New-AzFunctionApp` so that no application insights project is created when this option is specified.</span></span>
- <span data-ttu-id="7a4ca-194">Отключена возможность создания приложений-функций PowerShell 6.2, так как для поддержка PowerShell 6.2 прекращена.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-194">Removed support to create PowerShell 6.2 function apps since PowerShell 6.2 is EOL.</span></span> <span data-ttu-id="7a4ca-195">Текущая рекомендация для клиентов — создавать приложения-функции PowerShell 7.0.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-195">The current guidance for customers is to create PowerShell 7.0 function apps instead.</span></span>
- <span data-ttu-id="7a4ca-196">Изменена версия среды выполнения по умолчанию (c версии 6.2 на 7.0) в Функциях версии 3 в Windows для приложений-функций PowerShell, если не указать параметр `RuntimeVersion`.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-196">Changed the default runtime version in Functions version 3 on Windows for PowerShell function apps from 6.2 to 7.0 when the `RuntimeVersion` parameter is not specified.</span></span>
- <span data-ttu-id="7a4ca-197">Изменена версия среды выполнения по умолчанию в Функциях версии 3 в Windows и Linux для приложений-функций Node версий 10–12, если не указать параметр `RuntimeVersion`.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-197">Changed the default runtime version in Functions version 3 on Windows and Linux for Node function apps from 10 to 12 when the `RuntimeVersion` parameter is not specified.</span></span> <span data-ttu-id="7a4ca-198">При этом пользователи могут создавать приложения-функции Node 10, указывая `-Runtime Node` и `-RuntimeVersion 10`.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-198">However, users can still create Node 10 function apps by specifying `-Runtime Node` and `-RuntimeVersion 10`.</span></span> <span data-ttu-id="7a4ca-199">Изменена версия среды выполнения по умолчанию (с версии 3.7 на 3.8) в Функциях версии 3 в Linux для приложений-функций Python, если не указать параметр `RuntimeVersion`.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-199">Changed the default runtime version in Functions version 3 on Linux for Python function apps from 3.7 to 3.8 when the `RuntimeVersion` parameter is not specified.</span></span> <span data-ttu-id="7a4ca-200">При этом пользователи могут создавать приложения-функции Python 3.7, указывая `-Runtime Python` и `-RuntimeVersion 3.7`.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-200">However, users can still create Python 3.7 function apps by specifying `-Runtime Python` and `-RuntimeVersion 3.7`.</span></span>

#### <a name="before"></a><span data-ttu-id="7a4ca-201">До</span><span class="sxs-lookup"><span data-stu-id="7a4ca-201">Before</span></span>

```powershell
# Create a Node 10 function app on Linux
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Linux `
                  -Runtime Node

# Create a Node 10 function app on Windows
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Windows `
                  -Runtime Node

# Create a Python 3.7 function app on Linux
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Linux `
                  -Runtime Python
```

#### <a name="after"></a><span data-ttu-id="7a4ca-202">После</span><span class="sxs-lookup"><span data-stu-id="7a4ca-202">After</span></span>

```powershell
# Create a Node 10 function app on Linux
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Linux `
                  -Runtime Node `
                  -RuntimeVersion 10

# Create a Node 10 function app on Windows
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Windows `
                  -Runtime Node

# Create a Python 3.7 function app on Linux
New-AzFunctionApp -ResourceGroupName $rd `
                  -Name $functionAppName `
                  -StorageAccountName $storageAccountName `
                  -Location $location `
                  -OSType Linux `
                  -Runtime Python `
                  -RuntimeVersion 3.7
```

## <a name="azkeyvault"></a><span data-ttu-id="7a4ca-203">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="7a4ca-203">Az.KeyVault</span></span>

### <a name="new-azkeyvault"></a><span data-ttu-id="7a4ca-204">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="7a4ca-204">New-AzKeyVault</span></span>

<span data-ttu-id="7a4ca-205">Больше не поддерживает параметр `DisableSoftDelete`, и для исходного имени параметра не найден псевдоним.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-205">No longer supports the parameter `DisableSoftDelete` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="7a4ca-206">До</span><span class="sxs-lookup"><span data-stu-id="7a4ca-206">Before</span></span>

```powershell
# Opt out soft delete while creating a key vault
New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -DisableSoftDelete
```

#### <a name="after"></a><span data-ttu-id="7a4ca-207">После</span><span class="sxs-lookup"><span data-stu-id="7a4ca-207">After</span></span>

<span data-ttu-id="7a4ca-208">Возможность обновления параметра обратимого удаления является устаревшей в Az.KeyVault 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-208">The ability to update soft-delete setting is deprecated in Az.KeyVault 3.0.0.</span></span> <span data-ttu-id="7a4ca-209">Подробнее: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-209">Read more: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change</span></span>

### <a name="update-azkeyvault"></a><span data-ttu-id="7a4ca-210">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="7a4ca-210">Update-AzKeyVault</span></span>

<span data-ttu-id="7a4ca-211">Больше не поддерживает параметры `EnableSoftDelete` и `SoftDeleteRetentionInDays`; для исходного имени параметра не найден псевдоним.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-211">No longer supports the parameter `EnableSoftDelete`, `SoftDeleteRetentionInDays`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="7a4ca-212">До</span><span class="sxs-lookup"><span data-stu-id="7a4ca-212">Before</span></span>

```powershell
Update-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnableSoftDelete -SoftDeleteRetentionInDays 15
```

#### <a name="after"></a><span data-ttu-id="7a4ca-213">После</span><span class="sxs-lookup"><span data-stu-id="7a4ca-213">After</span></span>

<span data-ttu-id="7a4ca-214">Возможность обновления параметра обратимого удаления является устаревшей в Az.KeyVault 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-214">The ability to update soft-delete setting is deprecated in Az.KeyVault 3.0.0.</span></span> <span data-ttu-id="7a4ca-215">Подробнее: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-215">Read more: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change</span></span>

### <a name="get-azkeyvaultsecret"></a><span data-ttu-id="7a4ca-216">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="7a4ca-216">Get-AzKeyVaultSecret</span></span>

<span data-ttu-id="7a4ca-217">Свойство `SecretValueText` типа `Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret` удалено.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-217">The property `SecretValueText` of type `Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret` has been removed.</span></span> <span data-ttu-id="7a4ca-218">Примените `-AsPlainText` к вызову, чтобы получить секрет в формате обычного текста, или используйте `$secret.SecretValue` с типом `SecureString` в своем скрипте.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-218">Either apply a `-AsPlainText` to the call to get the plain text secret, or use `$secret.SecretValue` of type `SecureString` in your script.</span></span>

#### <a name="before"></a><span data-ttu-id="7a4ca-219">До</span><span class="sxs-lookup"><span data-stu-id="7a4ca-219">Before</span></span>

```powershell
$secret = Get-AzKeyVaultSecret -VaultName myVault -Name mySecret
$secretInPlainText = $secret.SecretValueText
```

#### <a name="after"></a><span data-ttu-id="7a4ca-220">После</span><span class="sxs-lookup"><span data-stu-id="7a4ca-220">After</span></span>

```powershell
$secretInPlainText = Get-AzKeyVaultSecret -VaultName myVault -Name mySecret -AsPlainText
```

## <a name="azmanagedservices"></a><span data-ttu-id="7a4ca-221">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="7a4ca-221">Az.ManagedServices</span></span>

### <a name="get-azmanagedservicesdefinition"></a><span data-ttu-id="7a4ca-222">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="7a4ca-222">Get-AzManagedServicesDefinition</span></span>

<span data-ttu-id="7a4ca-223">Больше не поддерживает параметр `ResourceId`, и для исходного имени параметра не найден псевдоним.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-223">No longer supports the parameter `ResourceId` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="7a4ca-224">До</span><span class="sxs-lookup"><span data-stu-id="7a4ca-224">Before</span></span>

```powershell
Get-AzManagedServicesDefinition -ResourceId xxx
```

#### <a name="after"></a><span data-ttu-id="7a4ca-225">После</span><span class="sxs-lookup"><span data-stu-id="7a4ca-225">After</span></span>

```powershell
Get-AzManagedServicesDefinition -Id xxx
```

### <a name="new-azmanagedservicesassignment"></a><span data-ttu-id="7a4ca-226">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="7a4ca-226">New-AzManagedServicesAssignment</span></span>

<span data-ttu-id="7a4ca-227">Больше не поддерживает параметры `RegistrationDefinitionName` и `RegistrationDefinitionResourceId`; для исходного имени параметра не найден псевдоним.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-227">No longer supports the parameter `RegistrationDefinitionName`, `RegistrationDefinitionResourceId`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="7a4ca-228">До</span><span class="sxs-lookup"><span data-stu-id="7a4ca-228">Before</span></span>

```powershell
New-AzManagedServicesAssignment -RegistrationDefinitionName xxx -Scope xxx
```

#### <a name="after"></a><span data-ttu-id="7a4ca-229">После</span><span class="sxs-lookup"><span data-stu-id="7a4ca-229">After</span></span>

```powershell
New-AzManagedServicesAssignment -Scope xxx -RegistrationDefinition xxx
```

### <a name="remove-azmanagedservicesassignment"></a><span data-ttu-id="7a4ca-230">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="7a4ca-230">Remove-AzManagedServicesAssignment</span></span>

<span data-ttu-id="7a4ca-231">Больше не поддерживает параметры `Id` и `ResourceId`; для исходного имени параметра не найден псевдоним.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-231">No longer supports the parameter `Id`, `ResourceId`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="7a4ca-232">До</span><span class="sxs-lookup"><span data-stu-id="7a4ca-232">Before</span></span>

```powershell
Remove-AzManagedServicesAssignment -ResourceId xxx
```

#### <a name="after"></a><span data-ttu-id="7a4ca-233">После</span><span class="sxs-lookup"><span data-stu-id="7a4ca-233">After</span></span>

```powershell
Get-AzManagedServicesAssignment -Scope xxx | Remove-AzManagedServicesAssignment
```

### <a name="remove-azmanagedservicesdefinition"></a><span data-ttu-id="7a4ca-234">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="7a4ca-234">Remove-AzManagedServicesDefinition</span></span>

<span data-ttu-id="7a4ca-235">Больше не поддерживает параметры `Id` и `ResourceId`; для исходного имени параметра не найден псевдоним.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-235">No longer supports the parameter `Id`, `ResourceId`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="7a4ca-236">До</span><span class="sxs-lookup"><span data-stu-id="7a4ca-236">Before</span></span>

```powershell
Remove-AzManagedServicesDefinition -ResourceId xxx
```

#### <a name="after"></a><span data-ttu-id="7a4ca-237">После</span><span class="sxs-lookup"><span data-stu-id="7a4ca-237">After</span></span>

```powershell
Get-AzManagedServicesDefinition -Scope xxx | Remove-AzManagedServicesDefinition
```

## <a name="azresourcemanager"></a><span data-ttu-id="7a4ca-238">Az.ResourceManager</span><span class="sxs-lookup"><span data-stu-id="7a4ca-238">Az.ResourceManager</span></span>

### <a name="get-azmanagementgroupdeployment"></a><span data-ttu-id="7a4ca-239">Get-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="7a4ca-239">Get-AzManagementGroupDeployment</span></span>

<span data-ttu-id="7a4ca-240">Больше не поддерживает параметр `ApiVersion`, и для исходного имени параметра не найден псевдоним.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-240">No longer supports the parameter `ApiVersion` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="7a4ca-241">До</span><span class="sxs-lookup"><span data-stu-id="7a4ca-241">Before</span></span>

```powershell
Get-AzManagementGroupDeployment -ManagementGroupId xxx -Name xxx -ApiVersion xxx
```

#### <a name="after"></a><span data-ttu-id="7a4ca-242">После</span><span class="sxs-lookup"><span data-stu-id="7a4ca-242">After</span></span>

```powershell
Get-AzManagementGroupDeployment -ManagementGroupId xxx -Name xxx
```

### <a name="get-azmanagementgroupdeploymentoperation"></a><span data-ttu-id="7a4ca-243">Get-AzManagementGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="7a4ca-243">Get-AzManagementGroupDeploymentOperation</span></span>

<span data-ttu-id="7a4ca-244">То же, что и `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-244">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azdeployment"></a><span data-ttu-id="7a4ca-245">Get-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="7a4ca-245">Get-AzDeployment</span></span>

<span data-ttu-id="7a4ca-246">То же, что и `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-246">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azdeploymentoperation"></a><span data-ttu-id="7a4ca-247">Get-AzDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="7a4ca-247">Get-AzDeploymentOperation</span></span>

<span data-ttu-id="7a4ca-248">То же, что и `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-248">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azdeploymentwhatifresult"></a><span data-ttu-id="7a4ca-249">Get-AzDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="7a4ca-249">Get-AzDeploymentWhatIfResult</span></span>

<span data-ttu-id="7a4ca-250">То же, что и `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-250">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-aztenantdeployment"></a><span data-ttu-id="7a4ca-251">Get-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="7a4ca-251">Get-AzTenantDeployment</span></span>

<span data-ttu-id="7a4ca-252">То же, что и `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-252">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-aztenantdeploymentoperation"></a><span data-ttu-id="7a4ca-253">Get-AzTenantDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="7a4ca-253">Get-AzTenantDeploymentOperation</span></span>

<span data-ttu-id="7a4ca-254">То же, что и `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-254">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-azmanagementgroupdeployment"></a><span data-ttu-id="7a4ca-255">New-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="7a4ca-255">New-AzManagementGroupDeployment</span></span>

<span data-ttu-id="7a4ca-256">То же, что и `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-256">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-azdeployment"></a><span data-ttu-id="7a4ca-257">New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="7a4ca-257">New-AzDeployment</span></span>

<span data-ttu-id="7a4ca-258">То же, что и `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-258">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-aztenantdeployment"></a><span data-ttu-id="7a4ca-259">New-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="7a4ca-259">New-AzTenantDeployment</span></span>

<span data-ttu-id="7a4ca-260">То же, что и `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-260">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-azmanagementgroupdeployment"></a><span data-ttu-id="7a4ca-261">Remove-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="7a4ca-261">Remove-AzManagementGroupDeployment</span></span>

<span data-ttu-id="7a4ca-262">То же, что и `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-262">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-azdeployment"></a><span data-ttu-id="7a4ca-263">Remove-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="7a4ca-263">Remove-AzDeployment</span></span>

<span data-ttu-id="7a4ca-264">То же, что и `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-264">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-aztenantdeployment"></a><span data-ttu-id="7a4ca-265">Remove-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="7a4ca-265">Remove-AzTenantDeployment</span></span>

<span data-ttu-id="7a4ca-266">То же, что и `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-266">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-azmanagementgroupdeploymenttemplate"></a><span data-ttu-id="7a4ca-267">Save-AzManagementGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="7a4ca-267">Save-AzManagementGroupDeploymentTemplate</span></span>

<span data-ttu-id="7a4ca-268">То же, что и `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-268">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-azdeploymenttemplate"></a><span data-ttu-id="7a4ca-269">Save-AzDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="7a4ca-269">Save-AzDeploymentTemplate</span></span>

<span data-ttu-id="7a4ca-270">То же, что и `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-270">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-aztenantdeploymenttemplate"></a><span data-ttu-id="7a4ca-271">Save-AzTenantDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="7a4ca-271">Save-AzTenantDeploymentTemplate</span></span>

<span data-ttu-id="7a4ca-272">То же, что и `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-272">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-azmanagementgroupdeployment"></a><span data-ttu-id="7a4ca-273">Stop-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="7a4ca-273">Stop-AzManagementGroupDeployment</span></span>

<span data-ttu-id="7a4ca-274">То же, что и `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-274">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-azdeployment"></a><span data-ttu-id="7a4ca-275">Stop-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="7a4ca-275">Stop-AzDeployment</span></span>

<span data-ttu-id="7a4ca-276">То же, что и `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-276">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-aztenantdeployment"></a><span data-ttu-id="7a4ca-277">Stop-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="7a4ca-277">Stop-AzTenantDeployment</span></span>

<span data-ttu-id="7a4ca-278">То же, что и `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-278">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-azmanagementgroupdeployment"></a><span data-ttu-id="7a4ca-279">Test-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="7a4ca-279">Test-AzManagementGroupDeployment</span></span>

<span data-ttu-id="7a4ca-280">То же, что и `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-280">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-azdeployment"></a><span data-ttu-id="7a4ca-281">Test-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="7a4ca-281">Test-AzDeployment</span></span>

<span data-ttu-id="7a4ca-282">То же, что и `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-282">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-aztenantdeployment"></a><span data-ttu-id="7a4ca-283">Test-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="7a4ca-283">Test-AzTenantDeployment</span></span>

<span data-ttu-id="7a4ca-284">То же, что и `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-284">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azresourcegroupdeployment"></a><span data-ttu-id="7a4ca-285">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="7a4ca-285">Get-AzResourceGroupDeployment</span></span>

<span data-ttu-id="7a4ca-286">То же, что и `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-286">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azresourcegroupdeploymentoperation"></a><span data-ttu-id="7a4ca-287">Get-AzResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="7a4ca-287">Get-AzResourceGroupDeploymentOperation</span></span>

<span data-ttu-id="7a4ca-288">То же, что и `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-288">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azresourcegroupdeploymentwhatifresult"></a><span data-ttu-id="7a4ca-289">Get-AzResourceGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="7a4ca-289">Get-AzResourceGroupDeploymentWhatIfResult</span></span>

<span data-ttu-id="7a4ca-290">То же, что и `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-290">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-azresourcegroupdeployment"></a><span data-ttu-id="7a4ca-291">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="7a4ca-291">New-AzResourceGroupDeployment</span></span>

<span data-ttu-id="7a4ca-292">То же, что и `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-292">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-azresourcegroupdeployment"></a><span data-ttu-id="7a4ca-293">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="7a4ca-293">Remove-AzResourceGroupDeployment</span></span>

<span data-ttu-id="7a4ca-294">То же, что и `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-294">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-azresourcegroupdeploymenttemplate"></a><span data-ttu-id="7a4ca-295">Save-AzResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="7a4ca-295">Save-AzResourceGroupDeploymentTemplate</span></span>

<span data-ttu-id="7a4ca-296">То же, что и `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-296">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-azresourcegroupdeployment"></a><span data-ttu-id="7a4ca-297">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="7a4ca-297">Stop-AzResourceGroupDeployment</span></span>

<span data-ttu-id="7a4ca-298">То же, что и `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-298">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-azresourcegroupdeployment"></a><span data-ttu-id="7a4ca-299">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="7a4ca-299">Test-AzResourceGroupDeployment</span></span>

<span data-ttu-id="7a4ca-300">То же, что и `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-300">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azmanagementgroupdeploymentwhatifresult"></a><span data-ttu-id="7a4ca-301">Get-AzManagementGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="7a4ca-301">Get-AzManagementGroupDeploymentWhatIfResult</span></span>

<span data-ttu-id="7a4ca-302">То же, что и `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-302">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-aztenantdeploymentwhatifresult"></a><span data-ttu-id="7a4ca-303">Get-AzTenantDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="7a4ca-303">Get-AzTenantDeploymentWhatIfResult</span></span>

<span data-ttu-id="7a4ca-304">То же, что и `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-304">Same with `Get-AzManagementGroupDeployment`.</span></span>

## <a name="azsql"></a><span data-ttu-id="7a4ca-305">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="7a4ca-305">Az.Sql</span></span>

### <a name="set-azsqlserveractivedirectoryadministrator"></a><span data-ttu-id="7a4ca-306">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="7a4ca-306">Set-AzSqlServerActiveDirectoryAdministrator</span></span>

<span data-ttu-id="7a4ca-307">Больше не поддерживает параметр `IsAzureADOnlyAuthentication`, и для исходного имени параметра не найден псевдоним.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-307">No longer supports the parameter `IsAzureADOnlyAuthentication` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="7a4ca-308">До</span><span class="sxs-lookup"><span data-stu-id="7a4ca-308">Before</span></span>

```powershell
Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01' -DisplayName 'DBAs' -IsAzureADOnlyAuthentication
```

#### <a name="after"></a><span data-ttu-id="7a4ca-309">После</span><span class="sxs-lookup"><span data-stu-id="7a4ca-309">After</span></span>

```powershell
Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01' -DisplayName 'DBAs'
```

## <a name="azsynapse"></a><span data-ttu-id="7a4ca-310">Az.Synapse</span><span class="sxs-lookup"><span data-stu-id="7a4ca-310">Az.Synapse</span></span>

### <a name="new-azsynapsesqlpool"></a><span data-ttu-id="7a4ca-311">New-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="7a4ca-311">New-AzSynapseSqlPool</span></span>

<span data-ttu-id="7a4ca-312">Больше не поддерживает параметры `FromBackup`, `FromRestorePoint`, `BackupResourceGroupName`, `BackupWorkspaceName`, `BackupSqlPoolName`, `BackupSqlPoolObject`, `BackupResourceId`, `SourceResourceGroupName`, `SourceWorkspaceName`, `SourceSqlPoolName`, `SourceSqlPoolObject`, `SourceResourceId` и `RestorePoint`; для исходного имени параметра не найден псевдоним.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-312">No longer supports the parameter `FromBackup`, `FromRestorePoint`, `BackupResourceGroupName`, `BackupWorkspaceName`, `BackupSqlPoolName`, `BackupSqlPoolObject`, `BackupResourceId`, `SourceResourceGroupName`, `SourceWorkspaceName`, `SourceSqlPoolName`, `SourceSqlPoolObject`, `SourceResourceId`, `RestorePoint`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="7a4ca-313">До</span><span class="sxs-lookup"><span data-stu-id="7a4ca-313">Before</span></span>

```powershell
New-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupWorkspaceName ContosoWorkspace -BackupSqlPoolName ExistingContosoSqlPool
```

#### <a name="after"></a><span data-ttu-id="7a4ca-314">После</span><span class="sxs-lookup"><span data-stu-id="7a4ca-314">After</span></span>

```powershell
PS C:\> New-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c
```

### <a name="update-azsynapsesqlpool"></a><span data-ttu-id="7a4ca-315">Update-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="7a4ca-315">Update-AzSynapseSqlPool</span></span>

<span data-ttu-id="7a4ca-316">Больше не поддерживает параметры `Suspend` и `Resume`; для исходного имени параметра не найден псевдоним.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-316">No longer supports the parameter `Suspend`, `Resume`, and no alias was found for the original parameter name.</span></span>

## <a name="aznetwork"></a><span data-ttu-id="7a4ca-317">Az.Network</span><span class="sxs-lookup"><span data-stu-id="7a4ca-317">Az.Network</span></span>

### <a name="approve-azprivateendpointconnection"></a><span data-ttu-id="7a4ca-318">Approve-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-318">Approve-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="7a4ca-319">Больше не поддерживает параметр `PrivateLinkResourceType`, и для исходного имени параметра не найден псевдоним.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-319">No longer supports the parameter `PrivateLinkResourceType` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="7a4ca-320">До</span><span class="sxs-lookup"><span data-stu-id="7a4ca-320">Before</span></span>

```powershell
Approve-AzPrivateEndpointConnection -ResourceGroupName xxx -ServiceName xxx -Name xxx -PrivateLinkResourceType 'Microsoft.Network/privateLinkServices' -Description xxx
```

#### <a name="after"></a><span data-ttu-id="7a4ca-321">После</span><span class="sxs-lookup"><span data-stu-id="7a4ca-321">After</span></span>

```powershell
Approve-AzPrivateEndpointConnection -ResourceGroupName xxx -ServiceName xxx -Name xxx -Description xxx
```

### <a name="deny-azprivateendpointconnection"></a><span data-ttu-id="7a4ca-322">Deny-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-322">Deny-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="7a4ca-323">То же, что и `Approve-AzPrivateEndpointConnection`.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-323">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="get-azprivateendpointconnection"></a><span data-ttu-id="7a4ca-324">Get-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-324">Get-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="7a4ca-325">То же, что и `Approve-AzPrivateEndpointConnection`.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-325">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="remove-azprivateendpointconnection"></a><span data-ttu-id="7a4ca-326">Remove-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-326">Remove-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="7a4ca-327">То же, что и `Approve-AzPrivateEndpointConnection`.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-327">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="set-azprivateendpointconnection"></a><span data-ttu-id="7a4ca-328">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7a4ca-328">Set-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="7a4ca-329">То же, что и `Approve-AzPrivateEndpointConnection`.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-329">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="new-aznetworkwatcherconnectionmonitorendpointobject"></a><span data-ttu-id="7a4ca-330">New-AzNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="7a4ca-330">New-AzNetworkWatcherConnectionMonitorEndpointObject</span></span>

<span data-ttu-id="7a4ca-331">Больше не поддерживает параметры `FilterType` и `FilterItem`; для исходного имени параметра не найден псевдоним.</span><span class="sxs-lookup"><span data-stu-id="7a4ca-331">No longer supports the parameter `FilterType`, `FilterItem`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="7a4ca-332">До</span><span class="sxs-lookup"><span data-stu-id="7a4ca-332">Before</span></span>

```powershell
$MySrcResourceId1 = '/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace'
$SrcEndpointFilterItem1 =New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject -Type 'AgentAddress' -Address 'WIN-P0HGNDO2S1B'
$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndPointObject -Name 'workspaceEndpoint' -ResourceId $MySrcResourceId1 -FilterType Include -FilterItem $SrcEndpointFilterItem1
```

#### <a name="after"></a><span data-ttu-id="7a4ca-333">После</span><span class="sxs-lookup"><span data-stu-id="7a4ca-333">After</span></span>

```powershell
MySrcResourceId1 = '/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace'
$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndPointObject -Name 'workspaceEndpoint' -ResourceId $MySrcResourceId1
```
