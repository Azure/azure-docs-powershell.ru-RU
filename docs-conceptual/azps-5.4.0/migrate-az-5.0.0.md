---
title: Руководство по миграции на Az 5.0.0
description: Это руководство по миграции содержит список критических изменений, внесенных в версию Az 5.0.0 в Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/27/2020
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: 35d562db72e37a630fce8530d715e783412add2e
ms.sourcegitcommit: 12bb1a6d1f89789bf2a78992f9b8ca848691a4d7
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/19/2021
ms.locfileid: "98573923"
---
# <a name="migration-guide-for-az-500"></a><span data-ttu-id="d41d5-103">Руководство по миграции на Az 5.0.0</span><span class="sxs-lookup"><span data-stu-id="d41d5-103">Migration Guide for Az 5.0.0</span></span>

<span data-ttu-id="d41d5-104">В этом документе описаны отличия между версиями Az 4.0.0 и 5.0.0.</span><span class="sxs-lookup"><span data-stu-id="d41d5-104">This document describes the changes between the 4.0.0 and 5.0.0 versions of Az.</span></span>

- [<span data-ttu-id="d41d5-105">Руководство по миграции на Az 5.0.0</span><span class="sxs-lookup"><span data-stu-id="d41d5-105">Migration Guide for Az 5.0.0</span></span>](#migration-guide-for-az-500)
  - [<span data-ttu-id="d41d5-106">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="d41d5-106">Az.Aks</span></span>](#azaks)
    - [<span data-ttu-id="d41d5-107">New-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="d41d5-107">New-AzAksCluster</span></span>](#new-azakscluster)
    - [<span data-ttu-id="d41d5-108">Set-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="d41d5-108">Set-AzAksCluster</span></span>](#set-azakscluster)
  - [<span data-ttu-id="d41d5-109">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d41d5-109">Az.ContainerRegistry</span></span>](#azcontainerregistry)
    - [<span data-ttu-id="d41d5-110">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d41d5-110">New-AzContainerRegistry</span></span>](#new-azcontainerregistry)
  - [<span data-ttu-id="d41d5-111">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="d41d5-111">Az.Functions</span></span>](#azfunctions)
    - [<span data-ttu-id="d41d5-112">Get-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="d41d5-112">Get-AzFunctionApp</span></span>](#get-azfunctionapp)
    - [<span data-ttu-id="d41d5-113">New-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="d41d5-113">New-AzFunctionApp</span></span>](#new-azfunctionapp)
  - [<span data-ttu-id="d41d5-114">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d41d5-114">Az.KeyVault</span></span>](#azkeyvault)
    - [<span data-ttu-id="d41d5-115">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="d41d5-115">New-AzKeyVault</span></span>](#new-azkeyvault)
    - [<span data-ttu-id="d41d5-116">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="d41d5-116">Update-AzKeyVault</span></span>](#update-azkeyvault)
    - [<span data-ttu-id="d41d5-117">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="d41d5-117">Get-AzKeyVaultSecret</span></span>](#get-azkeyvaultsecret)
  - [<span data-ttu-id="d41d5-118">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="d41d5-118">Az.ManagedServices</span></span>](#azmanagedservices)
    - [<span data-ttu-id="d41d5-119">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="d41d5-119">Get-AzManagedServicesDefinition</span></span>](#get-azmanagedservicesdefinition)
    - [<span data-ttu-id="d41d5-120">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="d41d5-120">New-AzManagedServicesAssignment</span></span>](#new-azmanagedservicesassignment)
    - [<span data-ttu-id="d41d5-121">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="d41d5-121">Remove-AzManagedServicesAssignment</span></span>](#remove-azmanagedservicesassignment)
    - [<span data-ttu-id="d41d5-122">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="d41d5-122">Remove-AzManagedServicesDefinition</span></span>](#remove-azmanagedservicesdefinition)
  - [<span data-ttu-id="d41d5-123">Az.ResourceManager</span><span class="sxs-lookup"><span data-stu-id="d41d5-123">Az.ResourceManager</span></span>](#azresourcemanager)
    - [<span data-ttu-id="d41d5-124">Get-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d41d5-124">Get-AzManagementGroupDeployment</span></span>](#get-azmanagementgroupdeployment)
    - [<span data-ttu-id="d41d5-125">Get-AzManagementGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="d41d5-125">Get-AzManagementGroupDeploymentOperation</span></span>](#get-azmanagementgroupdeploymentoperation)
    - [<span data-ttu-id="d41d5-126">Get-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="d41d5-126">Get-AzDeployment</span></span>](#get-azdeployment)
    - [<span data-ttu-id="d41d5-127">Get-AzDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="d41d5-127">Get-AzDeploymentOperation</span></span>](#get-azdeploymentoperation)
    - [<span data-ttu-id="d41d5-128">Get-AzDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="d41d5-128">Get-AzDeploymentWhatIfResult</span></span>](#get-azdeploymentwhatifresult)
    - [<span data-ttu-id="d41d5-129">Get-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="d41d5-129">Get-AzTenantDeployment</span></span>](#get-aztenantdeployment)
    - [<span data-ttu-id="d41d5-130">Get-AzTenantDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="d41d5-130">Get-AzTenantDeploymentOperation</span></span>](#get-aztenantdeploymentoperation)
    - [<span data-ttu-id="d41d5-131">New-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d41d5-131">New-AzManagementGroupDeployment</span></span>](#new-azmanagementgroupdeployment)
    - [<span data-ttu-id="d41d5-132">New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="d41d5-132">New-AzDeployment</span></span>](#new-azdeployment)
    - [<span data-ttu-id="d41d5-133">New-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="d41d5-133">New-AzTenantDeployment</span></span>](#new-aztenantdeployment)
    - [<span data-ttu-id="d41d5-134">Remove-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d41d5-134">Remove-AzManagementGroupDeployment</span></span>](#remove-azmanagementgroupdeployment)
    - [<span data-ttu-id="d41d5-135">Remove-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="d41d5-135">Remove-AzDeployment</span></span>](#remove-azdeployment)
    - [<span data-ttu-id="d41d5-136">Remove-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="d41d5-136">Remove-AzTenantDeployment</span></span>](#remove-aztenantdeployment)
    - [<span data-ttu-id="d41d5-137">Save-AzManagementGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="d41d5-137">Save-AzManagementGroupDeploymentTemplate</span></span>](#save-azmanagementgroupdeploymenttemplate)
    - [<span data-ttu-id="d41d5-138">Save-AzDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="d41d5-138">Save-AzDeploymentTemplate</span></span>](#save-azdeploymenttemplate)
    - [<span data-ttu-id="d41d5-139">Save-AzTenantDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="d41d5-139">Save-AzTenantDeploymentTemplate</span></span>](#save-aztenantdeploymenttemplate)
    - [<span data-ttu-id="d41d5-140">Stop-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d41d5-140">Stop-AzManagementGroupDeployment</span></span>](#stop-azmanagementgroupdeployment)
    - [<span data-ttu-id="d41d5-141">Stop-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="d41d5-141">Stop-AzDeployment</span></span>](#stop-azdeployment)
    - [<span data-ttu-id="d41d5-142">Stop-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="d41d5-142">Stop-AzTenantDeployment</span></span>](#stop-aztenantdeployment)
    - [<span data-ttu-id="d41d5-143">Test-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d41d5-143">Test-AzManagementGroupDeployment</span></span>](#test-azmanagementgroupdeployment)
    - [<span data-ttu-id="d41d5-144">Test-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="d41d5-144">Test-AzDeployment</span></span>](#test-azdeployment)
    - [<span data-ttu-id="d41d5-145">Test-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="d41d5-145">Test-AzTenantDeployment</span></span>](#test-aztenantdeployment)
    - [<span data-ttu-id="d41d5-146">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d41d5-146">Get-AzResourceGroupDeployment</span></span>](#get-azresourcegroupdeployment)
    - [<span data-ttu-id="d41d5-147">Get-AzResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="d41d5-147">Get-AzResourceGroupDeploymentOperation</span></span>](#get-azresourcegroupdeploymentoperation)
    - [<span data-ttu-id="d41d5-148">Get-AzResourceGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="d41d5-148">Get-AzResourceGroupDeploymentWhatIfResult</span></span>](#get-azresourcegroupdeploymentwhatifresult)
    - [<span data-ttu-id="d41d5-149">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d41d5-149">New-AzResourceGroupDeployment</span></span>](#new-azresourcegroupdeployment)
    - [<span data-ttu-id="d41d5-150">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d41d5-150">Remove-AzResourceGroupDeployment</span></span>](#remove-azresourcegroupdeployment)
    - [<span data-ttu-id="d41d5-151">Save-AzResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="d41d5-151">Save-AzResourceGroupDeploymentTemplate</span></span>](#save-azresourcegroupdeploymenttemplate)
    - [<span data-ttu-id="d41d5-152">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d41d5-152">Stop-AzResourceGroupDeployment</span></span>](#stop-azresourcegroupdeployment)
    - [<span data-ttu-id="d41d5-153">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d41d5-153">Test-AzResourceGroupDeployment</span></span>](#test-azresourcegroupdeployment)
    - [<span data-ttu-id="d41d5-154">Get-AzManagementGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="d41d5-154">Get-AzManagementGroupDeploymentWhatIfResult</span></span>](#get-azmanagementgroupdeploymentwhatifresult)
    - [<span data-ttu-id="d41d5-155">Get-AzTenantDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="d41d5-155">Get-AzTenantDeploymentWhatIfResult</span></span>](#get-aztenantdeploymentwhatifresult)
  - [<span data-ttu-id="d41d5-156">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d41d5-156">Az.Sql</span></span>](#azsql)
    - [<span data-ttu-id="d41d5-157">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="d41d5-157">Set-AzSqlServerActiveDirectoryAdministrator</span></span>](#set-azsqlserveractivedirectoryadministrator)
  - [<span data-ttu-id="d41d5-158">Az.Synapse</span><span class="sxs-lookup"><span data-stu-id="d41d5-158">Az.Synapse</span></span>](#azsynapse)
    - [<span data-ttu-id="d41d5-159">New-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="d41d5-159">New-AzSynapseSqlPool</span></span>](#new-azsynapsesqlpool)
    - [<span data-ttu-id="d41d5-160">Update-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="d41d5-160">Update-AzSynapseSqlPool</span></span>](#update-azsynapsesqlpool)
  - [<span data-ttu-id="d41d5-161">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d41d5-161">Az.Network</span></span>](#aznetwork)
    - [<span data-ttu-id="d41d5-162">Approve-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="d41d5-162">Approve-AzPrivateEndpointConnection</span></span>](#approve-azprivateendpointconnection)
    - [<span data-ttu-id="d41d5-163">Deny-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="d41d5-163">Deny-AzPrivateEndpointConnection</span></span>](#deny-azprivateendpointconnection)
    - [<span data-ttu-id="d41d5-164">Get-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="d41d5-164">Get-AzPrivateEndpointConnection</span></span>](#get-azprivateendpointconnection)
    - [<span data-ttu-id="d41d5-165">Remove-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="d41d5-165">Remove-AzPrivateEndpointConnection</span></span>](#remove-azprivateendpointconnection)
    - [<span data-ttu-id="d41d5-166">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d41d5-166">Set-AzPrivateEndpointConnection</span></span>](#set-azprivateendpointconnection)
    - [<span data-ttu-id="d41d5-167">New-AzNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="d41d5-167">New-AzNetworkWatcherConnectionMonitorEndpointObject</span></span>](#new-aznetworkwatcherconnectionmonitorendpointobject)

## <a name="azaks"></a><span data-ttu-id="d41d5-168">Az.Aks</span><span class="sxs-lookup"><span data-stu-id="d41d5-168">Az.Aks</span></span>

### <a name="new-azakscluster"></a><span data-ttu-id="d41d5-169">New-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="d41d5-169">New-AzAksCluster</span></span>

- <span data-ttu-id="d41d5-170">Больше не поддерживает параметр `NodeOsType`; для исходного имени параметра не найден псевдоним (всегда будет `Linux`).</span><span class="sxs-lookup"><span data-stu-id="d41d5-170">No longer supports the parameter `NodeOsType` and no alias was found for the original parameter name, it will always be `Linux`.</span></span>
- <span data-ttu-id="d41d5-171">Больше не поддерживает псевдоним `ClientIdAndSecret` для параметра `ServicePrincipalIdAndSecret`.</span><span class="sxs-lookup"><span data-stu-id="d41d5-171">No longer supports the alias `ClientIdAndSecret` for parameter `ServicePrincipalIdAndSecret`.</span></span>
- <span data-ttu-id="d41d5-172">Значение по умолчанию `NodeVmSetType` изменено с `AvailabilitySet` на `VirtualMachineScaleSets`.</span><span class="sxs-lookup"><span data-stu-id="d41d5-172">The default value of `NodeVmSetType` is changed from `AvailabilitySet` to `VirtualMachineScaleSets`.</span></span>
- <span data-ttu-id="d41d5-173">Значение по умолчанию `NetworkPlugin` изменено с `none` на `azure`.</span><span class="sxs-lookup"><span data-stu-id="d41d5-173">The default value of `NetworkPlugin` is changed from `none` to `azure`.</span></span>

#### <a name="before"></a><span data-ttu-id="d41d5-174">До</span><span class="sxs-lookup"><span data-stu-id="d41d5-174">Before</span></span>

```powershell
New-AzAksCluster -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NetworkPlugin azure -NodeOsType Linux -ClientIdAndSecret xxx
```

#### <a name="after"></a><span data-ttu-id="d41d5-175">После</span><span class="sxs-lookup"><span data-stu-id="d41d5-175">After</span></span>

```powershell
New-AzAksCluster -ResourceGroupName myResourceGroup -Name myCluster -WindowsProfileAdminUserName azureuser -WindowsProfileAdminUserPassword $cred -NodeVmSetType AvailabilitySet  -ServicePrincipalIdAndSecret xxx
```

### <a name="set-azakscluster"></a><span data-ttu-id="d41d5-176">Set-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="d41d5-176">Set-AzAksCluster</span></span>

<span data-ttu-id="d41d5-177">Больше не поддерживает псевдоним `ClientIdAndSecret` для параметра `ServicePrincipalIdAndSecret`.</span><span class="sxs-lookup"><span data-stu-id="d41d5-177">No longer supports the alias `ClientIdAndSecret` for parameter `ServicePrincipalIdAndSecret`.</span></span>

#### <a name="before"></a><span data-ttu-id="d41d5-178">До</span><span class="sxs-lookup"><span data-stu-id="d41d5-178">Before</span></span>

```powershell
Get-AzAksCluster -ResourceGroupName xxx -Name xxx | Set-AzAksCluster -ClientIdAndSecret xxx
```

#### <a name="after"></a><span data-ttu-id="d41d5-179">После</span><span class="sxs-lookup"><span data-stu-id="d41d5-179">After</span></span>

```powershell
Get-AzAksCluster -ResourceGroupName xxx -Name xxx | Set-AzAksCluster -ServicePrincipalIdAndSecret xxx
```

## <a name="azcontainerregistry"></a><span data-ttu-id="d41d5-180">Az.ContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d41d5-180">Az.ContainerRegistry</span></span>

### <a name="new-azcontainerregistry"></a><span data-ttu-id="d41d5-181">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="d41d5-181">New-AzContainerRegistry</span></span>

<span data-ttu-id="d41d5-182">Больше не поддерживает параметр `StorageAccountName`, и для исходного имени параметра не найден псевдоним.</span><span class="sxs-lookup"><span data-stu-id="d41d5-182">No longer supports the parameter `StorageAccountName` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="d41d5-183">До</span><span class="sxs-lookup"><span data-stu-id="d41d5-183">Before</span></span>

```powershell
New-AzContainerRegistry -Name $name -ResourceGroupName $rg -Location $location -SKU Classic -StorageAccountName $storage
```

#### <a name="after"></a><span data-ttu-id="d41d5-184">После</span><span class="sxs-lookup"><span data-stu-id="d41d5-184">After</span></span>

<span data-ttu-id="d41d5-185">Параметр `Classic` был устаревшим и параметр `StorageAccountName` был удален, так как он работает только с классическим Реестром контейнеров.</span><span class="sxs-lookup"><span data-stu-id="d41d5-185">`Classic` was deprecated and `StorageAccountName` was removed since it only works with Classic Container Registry.</span></span>

## <a name="azfunctions"></a><span data-ttu-id="d41d5-186">Az.Functions</span><span class="sxs-lookup"><span data-stu-id="d41d5-186">Az.Functions</span></span>

### <a name="get-azfunctionapp"></a><span data-ttu-id="d41d5-187">Get-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="d41d5-187">Get-AzFunctionApp</span></span>

<span data-ttu-id="d41d5-188">Параметр-переключатель `IncludeSlot` был удален из всех наборов параметров `Get-AzFunctionApp`, кроме одного.</span><span class="sxs-lookup"><span data-stu-id="d41d5-188">Removed `IncludeSlot` switch parameter from all but one parameter set of `Get-AzFunctionApp`.</span></span> <span data-ttu-id="d41d5-189">Командлет теперь поддерживает получение слотов развертывания в результатах, если указать `-IncludeSlot`.</span><span class="sxs-lookup"><span data-stu-id="d41d5-189">The cmdlet now supports retrieving deployment slots in the results when `-IncludeSlot` is specified.</span></span>
<span data-ttu-id="d41d5-190">Эта возможность была нарушена в предыдущей версии командлета,</span><span class="sxs-lookup"><span data-stu-id="d41d5-190">This functionality was broken in the previous cmdlet version.</span></span> <span data-ttu-id="d41d5-191">но сейчас она исправлена.</span><span class="sxs-lookup"><span data-stu-id="d41d5-191">However, this is now fixed.</span></span>

### <a name="new-azfunctionapp"></a><span data-ttu-id="d41d5-192">New-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="d41d5-192">New-AzFunctionApp</span></span>

- <span data-ttu-id="d41d5-193">Исправлена проблема с `-DisableApplicationInsights` в `New-AzFunctionApp`, чтобы при указании этого параметра не создавался проект Application Insights.</span><span class="sxs-lookup"><span data-stu-id="d41d5-193">Fixed `-DisableApplicationInsights` in `New-AzFunctionApp` so that no application insights project is created when this option is specified.</span></span>
- <span data-ttu-id="d41d5-194">Отключена возможность создания приложений-функций PowerShell 6.2, так как для поддержка PowerShell 6.2 прекращена.</span><span class="sxs-lookup"><span data-stu-id="d41d5-194">Removed support to create PowerShell 6.2 function apps since PowerShell 6.2 is EOL.</span></span> <span data-ttu-id="d41d5-195">Текущая рекомендация для клиентов — создавать приложения-функции PowerShell 7.0.</span><span class="sxs-lookup"><span data-stu-id="d41d5-195">The current guidance for customers is to create PowerShell 7.0 function apps instead.</span></span>
- <span data-ttu-id="d41d5-196">Изменена версия среды выполнения по умолчанию (c версии 6.2 на 7.0) в Функциях версии 3 в Windows для приложений-функций PowerShell, если не указать параметр `RuntimeVersion`.</span><span class="sxs-lookup"><span data-stu-id="d41d5-196">Changed the default runtime version in Functions version 3 on Windows for PowerShell function apps from 6.2 to 7.0 when the `RuntimeVersion` parameter is not specified.</span></span>
- <span data-ttu-id="d41d5-197">Изменена версия среды выполнения по умолчанию в Функциях версии 3 в Windows и Linux для приложений-функций Node версий 10–12, если не указать параметр `RuntimeVersion`.</span><span class="sxs-lookup"><span data-stu-id="d41d5-197">Changed the default runtime version in Functions version 3 on Windows and Linux for Node function apps from 10 to 12 when the `RuntimeVersion` parameter is not specified.</span></span> <span data-ttu-id="d41d5-198">При этом пользователи могут создавать приложения-функции Node 10, указывая `-Runtime Node` и `-RuntimeVersion 10`.</span><span class="sxs-lookup"><span data-stu-id="d41d5-198">However, users can still create Node 10 function apps by specifying `-Runtime Node` and `-RuntimeVersion 10`.</span></span> <span data-ttu-id="d41d5-199">Изменена версия среды выполнения по умолчанию (с версии 3.7 на 3.8) в Функциях версии 3 в Linux для приложений-функций Python, если не указать параметр `RuntimeVersion`.</span><span class="sxs-lookup"><span data-stu-id="d41d5-199">Changed the default runtime version in Functions version 3 on Linux for Python function apps from 3.7 to 3.8 when the `RuntimeVersion` parameter is not specified.</span></span> <span data-ttu-id="d41d5-200">При этом пользователи могут создавать приложения-функции Python 3.7, указывая `-Runtime Python` и `-RuntimeVersion 3.7`.</span><span class="sxs-lookup"><span data-stu-id="d41d5-200">However, users can still create Python 3.7 function apps by specifying `-Runtime Python` and `-RuntimeVersion 3.7`.</span></span>

#### <a name="before"></a><span data-ttu-id="d41d5-201">До</span><span class="sxs-lookup"><span data-stu-id="d41d5-201">Before</span></span>

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

#### <a name="after"></a><span data-ttu-id="d41d5-202">После</span><span class="sxs-lookup"><span data-stu-id="d41d5-202">After</span></span>

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

## <a name="azkeyvault"></a><span data-ttu-id="d41d5-203">Az.KeyVault</span><span class="sxs-lookup"><span data-stu-id="d41d5-203">Az.KeyVault</span></span>

### <a name="new-azkeyvault"></a><span data-ttu-id="d41d5-204">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="d41d5-204">New-AzKeyVault</span></span>

<span data-ttu-id="d41d5-205">Больше не поддерживает параметр `DisableSoftDelete`, и для исходного имени параметра не найден псевдоним.</span><span class="sxs-lookup"><span data-stu-id="d41d5-205">No longer supports the parameter `DisableSoftDelete` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="d41d5-206">До</span><span class="sxs-lookup"><span data-stu-id="d41d5-206">Before</span></span>

```powershell
# Opt out soft delete while creating a key vault
New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -DisableSoftDelete
```

#### <a name="after"></a><span data-ttu-id="d41d5-207">После</span><span class="sxs-lookup"><span data-stu-id="d41d5-207">After</span></span>

<span data-ttu-id="d41d5-208">Возможность обновления параметра обратимого удаления является устаревшей в Az.KeyVault 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="d41d5-208">The ability to update soft-delete setting is deprecated in Az.KeyVault 3.0.0.</span></span> <span data-ttu-id="d41d5-209">Подробнее: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change.</span><span class="sxs-lookup"><span data-stu-id="d41d5-209">Read more: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change</span></span>

### <a name="update-azkeyvault"></a><span data-ttu-id="d41d5-210">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="d41d5-210">Update-AzKeyVault</span></span>

<span data-ttu-id="d41d5-211">Больше не поддерживает параметры `EnableSoftDelete` и `SoftDeleteRetentionInDays`; для исходного имени параметра не найден псевдоним.</span><span class="sxs-lookup"><span data-stu-id="d41d5-211">No longer supports the parameter `EnableSoftDelete`, `SoftDeleteRetentionInDays`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="d41d5-212">До</span><span class="sxs-lookup"><span data-stu-id="d41d5-212">Before</span></span>

```powershell
Update-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnableSoftDelete -SoftDeleteRetentionInDays 15
```

#### <a name="after"></a><span data-ttu-id="d41d5-213">После</span><span class="sxs-lookup"><span data-stu-id="d41d5-213">After</span></span>

<span data-ttu-id="d41d5-214">Возможность обновления параметра обратимого удаления является устаревшей в Az.KeyVault 3.0.0.</span><span class="sxs-lookup"><span data-stu-id="d41d5-214">The ability to update soft-delete setting is deprecated in Az.KeyVault 3.0.0.</span></span> <span data-ttu-id="d41d5-215">Подробнее: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change.</span><span class="sxs-lookup"><span data-stu-id="d41d5-215">Read more: https://docs.microsoft.com/azure/key-vault/general/soft-delete-change</span></span>

### <a name="get-azkeyvaultsecret"></a><span data-ttu-id="d41d5-216">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="d41d5-216">Get-AzKeyVaultSecret</span></span>

<span data-ttu-id="d41d5-217">Свойство `SecretValueText` типа `Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret` удалено.</span><span class="sxs-lookup"><span data-stu-id="d41d5-217">The property `SecretValueText` of type `Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret` has been removed.</span></span> <span data-ttu-id="d41d5-218">Свойство `SecretValueText` заменено `SecretValue`.</span><span class="sxs-lookup"><span data-stu-id="d41d5-218">The `SecretValueText` property has been replaced with `SecretValue`.</span></span>

#### <a name="before"></a><span data-ttu-id="d41d5-219">До</span><span class="sxs-lookup"><span data-stu-id="d41d5-219">Before</span></span>

```powershell
$secret = Get-AzKeyVaultSecret -VaultName myVault -Name mySecret
$secretInPlainText = $secret.SecretValueText
```

#### <a name="after"></a><span data-ttu-id="d41d5-220">После</span><span class="sxs-lookup"><span data-stu-id="d41d5-220">After</span></span>

```powershell
# PowerShell 7 or newer
$secret = Get-AzKeyVaultSecret -VaultName myVault -Name mySecret
$secretInPlainText = ConvertFrom-SecureString -SecureString $secret.SecretValue -AsPlainText

# Prior to PowerShell 7, or Windows PowerShell
$secret = Get-AzKeyVaultSecret -VaultName myVault -Name mySecret
$secretInPlainText = [System.Runtime.InteropServices.Marshal]::PtrToStringBSTR([System.Runtime.InteropServices.Marshal]::SecureStringToBSTR($secret.SecretValue))
```

## <a name="azmanagedservices"></a><span data-ttu-id="d41d5-221">Az.ManagedServices</span><span class="sxs-lookup"><span data-stu-id="d41d5-221">Az.ManagedServices</span></span>

### <a name="get-azmanagedservicesdefinition"></a><span data-ttu-id="d41d5-222">Get-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="d41d5-222">Get-AzManagedServicesDefinition</span></span>

<span data-ttu-id="d41d5-223">Больше не поддерживает параметр `ResourceId`, и для исходного имени параметра не найден псевдоним.</span><span class="sxs-lookup"><span data-stu-id="d41d5-223">No longer supports the parameter `ResourceId` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="d41d5-224">До</span><span class="sxs-lookup"><span data-stu-id="d41d5-224">Before</span></span>

```powershell
Get-AzManagedServicesDefinition -ResourceId xxx
```

#### <a name="after"></a><span data-ttu-id="d41d5-225">После</span><span class="sxs-lookup"><span data-stu-id="d41d5-225">After</span></span>

```powershell
Get-AzManagedServicesDefinition -Id xxx
```

### <a name="new-azmanagedservicesassignment"></a><span data-ttu-id="d41d5-226">New-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="d41d5-226">New-AzManagedServicesAssignment</span></span>

<span data-ttu-id="d41d5-227">Больше не поддерживает параметры `RegistrationDefinitionName` и `RegistrationDefinitionResourceId`; для исходного имени параметра не найден псевдоним.</span><span class="sxs-lookup"><span data-stu-id="d41d5-227">No longer supports the parameter `RegistrationDefinitionName`, `RegistrationDefinitionResourceId`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="d41d5-228">До</span><span class="sxs-lookup"><span data-stu-id="d41d5-228">Before</span></span>

```powershell
New-AzManagedServicesAssignment -RegistrationDefinitionName xxx -Scope xxx
```

#### <a name="after"></a><span data-ttu-id="d41d5-229">После</span><span class="sxs-lookup"><span data-stu-id="d41d5-229">After</span></span>

```powershell
New-AzManagedServicesAssignment -Scope xxx -RegistrationDefinition xxx
```

### <a name="remove-azmanagedservicesassignment"></a><span data-ttu-id="d41d5-230">Remove-AzManagedServicesAssignment</span><span class="sxs-lookup"><span data-stu-id="d41d5-230">Remove-AzManagedServicesAssignment</span></span>

<span data-ttu-id="d41d5-231">Больше не поддерживает параметры `Id` и `ResourceId`; для исходного имени параметра не найден псевдоним.</span><span class="sxs-lookup"><span data-stu-id="d41d5-231">No longer supports the parameter `Id`, `ResourceId`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="d41d5-232">До</span><span class="sxs-lookup"><span data-stu-id="d41d5-232">Before</span></span>

```powershell
Remove-AzManagedServicesAssignment -ResourceId xxx
```

#### <a name="after"></a><span data-ttu-id="d41d5-233">После</span><span class="sxs-lookup"><span data-stu-id="d41d5-233">After</span></span>

```powershell
Get-AzManagedServicesAssignment -Scope xxx | Remove-AzManagedServicesAssignment
```

### <a name="remove-azmanagedservicesdefinition"></a><span data-ttu-id="d41d5-234">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="d41d5-234">Remove-AzManagedServicesDefinition</span></span>

<span data-ttu-id="d41d5-235">Больше не поддерживает параметры `Id` и `ResourceId`; для исходного имени параметра не найден псевдоним.</span><span class="sxs-lookup"><span data-stu-id="d41d5-235">No longer supports the parameter `Id`, `ResourceId`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="d41d5-236">До</span><span class="sxs-lookup"><span data-stu-id="d41d5-236">Before</span></span>

```powershell
Remove-AzManagedServicesDefinition -ResourceId xxx
```

#### <a name="after"></a><span data-ttu-id="d41d5-237">После</span><span class="sxs-lookup"><span data-stu-id="d41d5-237">After</span></span>

```powershell
Get-AzManagedServicesDefinition -Scope xxx | Remove-AzManagedServicesDefinition
```

## <a name="azresourcemanager"></a><span data-ttu-id="d41d5-238">Az.ResourceManager</span><span class="sxs-lookup"><span data-stu-id="d41d5-238">Az.ResourceManager</span></span>

### <a name="get-azmanagementgroupdeployment"></a><span data-ttu-id="d41d5-239">Get-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d41d5-239">Get-AzManagementGroupDeployment</span></span>

<span data-ttu-id="d41d5-240">Больше не поддерживает параметр `ApiVersion`, и для исходного имени параметра не найден псевдоним.</span><span class="sxs-lookup"><span data-stu-id="d41d5-240">No longer supports the parameter `ApiVersion` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="d41d5-241">До</span><span class="sxs-lookup"><span data-stu-id="d41d5-241">Before</span></span>

```powershell
Get-AzManagementGroupDeployment -ManagementGroupId xxx -Name xxx -ApiVersion xxx
```

#### <a name="after"></a><span data-ttu-id="d41d5-242">После</span><span class="sxs-lookup"><span data-stu-id="d41d5-242">After</span></span>

```powershell
Get-AzManagementGroupDeployment -ManagementGroupId xxx -Name xxx
```

### <a name="get-azmanagementgroupdeploymentoperation"></a><span data-ttu-id="d41d5-243">Get-AzManagementGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="d41d5-243">Get-AzManagementGroupDeploymentOperation</span></span>

<span data-ttu-id="d41d5-244">То же, что и `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="d41d5-244">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azdeployment"></a><span data-ttu-id="d41d5-245">Get-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="d41d5-245">Get-AzDeployment</span></span>

<span data-ttu-id="d41d5-246">То же, что и `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="d41d5-246">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azdeploymentoperation"></a><span data-ttu-id="d41d5-247">Get-AzDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="d41d5-247">Get-AzDeploymentOperation</span></span>

<span data-ttu-id="d41d5-248">То же, что и `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="d41d5-248">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azdeploymentwhatifresult"></a><span data-ttu-id="d41d5-249">Get-AzDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="d41d5-249">Get-AzDeploymentWhatIfResult</span></span>

<span data-ttu-id="d41d5-250">То же, что и `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="d41d5-250">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-aztenantdeployment"></a><span data-ttu-id="d41d5-251">Get-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="d41d5-251">Get-AzTenantDeployment</span></span>

<span data-ttu-id="d41d5-252">То же, что и `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="d41d5-252">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-aztenantdeploymentoperation"></a><span data-ttu-id="d41d5-253">Get-AzTenantDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="d41d5-253">Get-AzTenantDeploymentOperation</span></span>

<span data-ttu-id="d41d5-254">То же, что и `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="d41d5-254">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-azmanagementgroupdeployment"></a><span data-ttu-id="d41d5-255">New-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d41d5-255">New-AzManagementGroupDeployment</span></span>

<span data-ttu-id="d41d5-256">То же, что и `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="d41d5-256">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-azdeployment"></a><span data-ttu-id="d41d5-257">New-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="d41d5-257">New-AzDeployment</span></span>

<span data-ttu-id="d41d5-258">То же, что и `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="d41d5-258">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-aztenantdeployment"></a><span data-ttu-id="d41d5-259">New-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="d41d5-259">New-AzTenantDeployment</span></span>

<span data-ttu-id="d41d5-260">То же, что и `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="d41d5-260">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-azmanagementgroupdeployment"></a><span data-ttu-id="d41d5-261">Remove-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d41d5-261">Remove-AzManagementGroupDeployment</span></span>

<span data-ttu-id="d41d5-262">То же, что и `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="d41d5-262">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-azdeployment"></a><span data-ttu-id="d41d5-263">Remove-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="d41d5-263">Remove-AzDeployment</span></span>

<span data-ttu-id="d41d5-264">То же, что и `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="d41d5-264">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-aztenantdeployment"></a><span data-ttu-id="d41d5-265">Remove-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="d41d5-265">Remove-AzTenantDeployment</span></span>

<span data-ttu-id="d41d5-266">То же, что и `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="d41d5-266">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-azmanagementgroupdeploymenttemplate"></a><span data-ttu-id="d41d5-267">Save-AzManagementGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="d41d5-267">Save-AzManagementGroupDeploymentTemplate</span></span>

<span data-ttu-id="d41d5-268">То же, что и `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="d41d5-268">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-azdeploymenttemplate"></a><span data-ttu-id="d41d5-269">Save-AzDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="d41d5-269">Save-AzDeploymentTemplate</span></span>

<span data-ttu-id="d41d5-270">То же, что и `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="d41d5-270">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-aztenantdeploymenttemplate"></a><span data-ttu-id="d41d5-271">Save-AzTenantDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="d41d5-271">Save-AzTenantDeploymentTemplate</span></span>

<span data-ttu-id="d41d5-272">То же, что и `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="d41d5-272">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-azmanagementgroupdeployment"></a><span data-ttu-id="d41d5-273">Stop-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d41d5-273">Stop-AzManagementGroupDeployment</span></span>

<span data-ttu-id="d41d5-274">То же, что и `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="d41d5-274">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-azdeployment"></a><span data-ttu-id="d41d5-275">Stop-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="d41d5-275">Stop-AzDeployment</span></span>

<span data-ttu-id="d41d5-276">То же, что и `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="d41d5-276">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-aztenantdeployment"></a><span data-ttu-id="d41d5-277">Stop-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="d41d5-277">Stop-AzTenantDeployment</span></span>

<span data-ttu-id="d41d5-278">То же, что и `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="d41d5-278">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-azmanagementgroupdeployment"></a><span data-ttu-id="d41d5-279">Test-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d41d5-279">Test-AzManagementGroupDeployment</span></span>

<span data-ttu-id="d41d5-280">То же, что и `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="d41d5-280">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-azdeployment"></a><span data-ttu-id="d41d5-281">Test-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="d41d5-281">Test-AzDeployment</span></span>

<span data-ttu-id="d41d5-282">То же, что и `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="d41d5-282">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-aztenantdeployment"></a><span data-ttu-id="d41d5-283">Test-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="d41d5-283">Test-AzTenantDeployment</span></span>

<span data-ttu-id="d41d5-284">То же, что и `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="d41d5-284">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azresourcegroupdeployment"></a><span data-ttu-id="d41d5-285">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d41d5-285">Get-AzResourceGroupDeployment</span></span>

<span data-ttu-id="d41d5-286">То же, что и `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="d41d5-286">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azresourcegroupdeploymentoperation"></a><span data-ttu-id="d41d5-287">Get-AzResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="d41d5-287">Get-AzResourceGroupDeploymentOperation</span></span>

<span data-ttu-id="d41d5-288">То же, что и `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="d41d5-288">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azresourcegroupdeploymentwhatifresult"></a><span data-ttu-id="d41d5-289">Get-AzResourceGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="d41d5-289">Get-AzResourceGroupDeploymentWhatIfResult</span></span>

<span data-ttu-id="d41d5-290">То же, что и `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="d41d5-290">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="new-azresourcegroupdeployment"></a><span data-ttu-id="d41d5-291">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d41d5-291">New-AzResourceGroupDeployment</span></span>

<span data-ttu-id="d41d5-292">То же, что и `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="d41d5-292">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="remove-azresourcegroupdeployment"></a><span data-ttu-id="d41d5-293">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d41d5-293">Remove-AzResourceGroupDeployment</span></span>

<span data-ttu-id="d41d5-294">То же, что и `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="d41d5-294">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="save-azresourcegroupdeploymenttemplate"></a><span data-ttu-id="d41d5-295">Save-AzResourceGroupDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="d41d5-295">Save-AzResourceGroupDeploymentTemplate</span></span>

<span data-ttu-id="d41d5-296">То же, что и `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="d41d5-296">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="stop-azresourcegroupdeployment"></a><span data-ttu-id="d41d5-297">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d41d5-297">Stop-AzResourceGroupDeployment</span></span>

<span data-ttu-id="d41d5-298">То же, что и `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="d41d5-298">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="test-azresourcegroupdeployment"></a><span data-ttu-id="d41d5-299">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d41d5-299">Test-AzResourceGroupDeployment</span></span>

<span data-ttu-id="d41d5-300">То же, что и `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="d41d5-300">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-azmanagementgroupdeploymentwhatifresult"></a><span data-ttu-id="d41d5-301">Get-AzManagementGroupDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="d41d5-301">Get-AzManagementGroupDeploymentWhatIfResult</span></span>

<span data-ttu-id="d41d5-302">То же, что и `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="d41d5-302">Same with `Get-AzManagementGroupDeployment`.</span></span>

### <a name="get-aztenantdeploymentwhatifresult"></a><span data-ttu-id="d41d5-303">Get-AzTenantDeploymentWhatIfResult</span><span class="sxs-lookup"><span data-stu-id="d41d5-303">Get-AzTenantDeploymentWhatIfResult</span></span>

<span data-ttu-id="d41d5-304">То же, что и `Get-AzManagementGroupDeployment`.</span><span class="sxs-lookup"><span data-stu-id="d41d5-304">Same with `Get-AzManagementGroupDeployment`.</span></span>

## <a name="azsql"></a><span data-ttu-id="d41d5-305">Az.Sql</span><span class="sxs-lookup"><span data-stu-id="d41d5-305">Az.Sql</span></span>

### <a name="set-azsqlserveractivedirectoryadministrator"></a><span data-ttu-id="d41d5-306">Set-AzSqlServerActiveDirectoryAdministrator</span><span class="sxs-lookup"><span data-stu-id="d41d5-306">Set-AzSqlServerActiveDirectoryAdministrator</span></span>

<span data-ttu-id="d41d5-307">Больше не поддерживает параметр `IsAzureADOnlyAuthentication`, и для исходного имени параметра не найден псевдоним.</span><span class="sxs-lookup"><span data-stu-id="d41d5-307">No longer supports the parameter `IsAzureADOnlyAuthentication` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="d41d5-308">До</span><span class="sxs-lookup"><span data-stu-id="d41d5-308">Before</span></span>

```powershell
Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01' -DisplayName 'DBAs' -IsAzureADOnlyAuthentication
```

#### <a name="after"></a><span data-ttu-id="d41d5-309">После</span><span class="sxs-lookup"><span data-stu-id="d41d5-309">After</span></span>

```powershell
Set-AzSqlServerActiveDirectoryAdministrator -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01' -DisplayName 'DBAs'
```

## <a name="azsynapse"></a><span data-ttu-id="d41d5-310">Az.Synapse</span><span class="sxs-lookup"><span data-stu-id="d41d5-310">Az.Synapse</span></span>

### <a name="new-azsynapsesqlpool"></a><span data-ttu-id="d41d5-311">New-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="d41d5-311">New-AzSynapseSqlPool</span></span>

<span data-ttu-id="d41d5-312">Больше не поддерживает параметры `FromBackup`, `FromRestorePoint`, `BackupResourceGroupName`, `BackupWorkspaceName`, `BackupSqlPoolName`, `BackupSqlPoolObject`, `BackupResourceId`, `SourceResourceGroupName`, `SourceWorkspaceName`, `SourceSqlPoolName`, `SourceSqlPoolObject`, `SourceResourceId` и `RestorePoint`; для исходного имени параметра не найден псевдоним.</span><span class="sxs-lookup"><span data-stu-id="d41d5-312">No longer supports the parameter `FromBackup`, `FromRestorePoint`, `BackupResourceGroupName`, `BackupWorkspaceName`, `BackupSqlPoolName`, `BackupSqlPoolObject`, `BackupResourceId`, `SourceResourceGroupName`, `SourceWorkspaceName`, `SourceSqlPoolName`, `SourceSqlPoolObject`, `SourceResourceId`, `RestorePoint`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="d41d5-313">До</span><span class="sxs-lookup"><span data-stu-id="d41d5-313">Before</span></span>

```powershell
New-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupWorkspaceName ContosoWorkspace -BackupSqlPoolName ExistingContosoSqlPool
```

#### <a name="after"></a><span data-ttu-id="d41d5-314">После</span><span class="sxs-lookup"><span data-stu-id="d41d5-314">After</span></span>

```powershell
PS C:\> New-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c
```

### <a name="update-azsynapsesqlpool"></a><span data-ttu-id="d41d5-315">Update-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="d41d5-315">Update-AzSynapseSqlPool</span></span>

<span data-ttu-id="d41d5-316">Больше не поддерживает параметры `Suspend` и `Resume`; для исходного имени параметра не найден псевдоним.</span><span class="sxs-lookup"><span data-stu-id="d41d5-316">No longer supports the parameter `Suspend`, `Resume`, and no alias was found for the original parameter name.</span></span>

## <a name="aznetwork"></a><span data-ttu-id="d41d5-317">Az.Network</span><span class="sxs-lookup"><span data-stu-id="d41d5-317">Az.Network</span></span>

### <a name="approve-azprivateendpointconnection"></a><span data-ttu-id="d41d5-318">Approve-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="d41d5-318">Approve-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="d41d5-319">Больше не поддерживает параметр `PrivateLinkResourceType`, и для исходного имени параметра не найден псевдоним.</span><span class="sxs-lookup"><span data-stu-id="d41d5-319">No longer supports the parameter `PrivateLinkResourceType` and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="d41d5-320">До</span><span class="sxs-lookup"><span data-stu-id="d41d5-320">Before</span></span>

```powershell
Approve-AzPrivateEndpointConnection -ResourceGroupName xxx -ServiceName xxx -Name xxx -PrivateLinkResourceType 'Microsoft.Network/privateLinkServices' -Description xxx
```

#### <a name="after"></a><span data-ttu-id="d41d5-321">После</span><span class="sxs-lookup"><span data-stu-id="d41d5-321">After</span></span>

```powershell
Approve-AzPrivateEndpointConnection -ResourceGroupName xxx -ServiceName xxx -Name xxx -Description xxx
```

### <a name="deny-azprivateendpointconnection"></a><span data-ttu-id="d41d5-322">Deny-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="d41d5-322">Deny-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="d41d5-323">То же, что и `Approve-AzPrivateEndpointConnection`.</span><span class="sxs-lookup"><span data-stu-id="d41d5-323">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="get-azprivateendpointconnection"></a><span data-ttu-id="d41d5-324">Get-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="d41d5-324">Get-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="d41d5-325">То же, что и `Approve-AzPrivateEndpointConnection`.</span><span class="sxs-lookup"><span data-stu-id="d41d5-325">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="remove-azprivateendpointconnection"></a><span data-ttu-id="d41d5-326">Remove-AzPrivateEndpointConnection.</span><span class="sxs-lookup"><span data-stu-id="d41d5-326">Remove-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="d41d5-327">То же, что и `Approve-AzPrivateEndpointConnection`.</span><span class="sxs-lookup"><span data-stu-id="d41d5-327">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="set-azprivateendpointconnection"></a><span data-ttu-id="d41d5-328">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="d41d5-328">Set-AzPrivateEndpointConnection</span></span>

<span data-ttu-id="d41d5-329">То же, что и `Approve-AzPrivateEndpointConnection`.</span><span class="sxs-lookup"><span data-stu-id="d41d5-329">Same with `Approve-AzPrivateEndpointConnection`.</span></span>

### <a name="new-aznetworkwatcherconnectionmonitorendpointobject"></a><span data-ttu-id="d41d5-330">New-AzNetworkWatcherConnectionMonitorEndpointObject</span><span class="sxs-lookup"><span data-stu-id="d41d5-330">New-AzNetworkWatcherConnectionMonitorEndpointObject</span></span>

<span data-ttu-id="d41d5-331">Больше не поддерживает параметры `FilterType` и `FilterItem`; для исходного имени параметра не найден псевдоним.</span><span class="sxs-lookup"><span data-stu-id="d41d5-331">No longer supports the parameter `FilterType`, `FilterItem`, and no alias was found for the original parameter name.</span></span>

#### <a name="before"></a><span data-ttu-id="d41d5-332">До</span><span class="sxs-lookup"><span data-stu-id="d41d5-332">Before</span></span>

```powershell
$MySrcResourceId1 = '/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace'
$SrcEndpointFilterItem1 =New-AzNetworkWatcherConnectionMonitorEndpointFilterItemObject -Type 'AgentAddress' -Address 'WIN-P0HGNDO2S1B'
$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndPointObject -Name 'workspaceEndpoint' -ResourceId $MySrcResourceId1 -FilterType Include -FilterItem $SrcEndpointFilterItem1
```

#### <a name="after"></a><span data-ttu-id="d41d5-333">После</span><span class="sxs-lookup"><span data-stu-id="d41d5-333">After</span></span>

```powershell
MySrcResourceId1 = '/subscriptions/00000000-0000-0000-0000-000000000000/resourcegroups/myresourceGroup/providers/Microsoft.OperationalInsights/workspaces/myworkspace'
$SourceEndpointObject1 = New-AzNetworkWatcherConnectionMonitorEndPointObject -Name 'workspaceEndpoint' -ResourceId $MySrcResourceId1
```
