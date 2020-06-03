---
title: Критические изменения для Microsoft Azure PowerShell 4.0.0
description: Это руководство по миграции содержит список критических изменений, внесенных в выпуск Azure PowerShell версии 4.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/01/2018
ms.openlocfilehash: 47d7ab67a6b1d092bb07405e7dc925d844cac5ab
ms.sourcegitcommit: 7839b82f47ef8dd522eff900081c22de0d089cfc
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "83386720"
---
# <a name="breaking-changes-for-microsoft-azure-powershell-400"></a><span data-ttu-id="64ded-103">Критические изменения для Microsoft Azure PowerShell 4.0.0</span><span class="sxs-lookup"><span data-stu-id="64ded-103">Breaking changes for Microsoft Azure PowerShell 4.0.0</span></span>

[!INCLUDE [migrate-to-az](../includes/migrate-to-az.md)]

<span data-ttu-id="64ded-104">Этот документ предназначен для уведомления о критических изменениях и является руководством по миграции для пользователей командлетов Microsoft Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="64ded-104">This document serves as both a breaking change notification and migration guide for consumers of the Microsoft Azure PowerShell cmdlets.</span></span> <span data-ttu-id="64ded-105">В каждом разделе описана причина критического изменения и самый простой путь миграции.</span><span class="sxs-lookup"><span data-stu-id="64ded-105">Each section describes both the impetus for the breaking change and the migration path of least resistance.</span></span> <span data-ttu-id="64ded-106">Подробное описание см. в запросах на вытягивание для каждого изменения.</span><span class="sxs-lookup"><span data-stu-id="64ded-106">For in-depth context, please refer to the pull request associated with each change.</span></span>

## <a name="table-of-contents"></a><span data-ttu-id="64ded-107">Оглавление</span><span class="sxs-lookup"><span data-stu-id="64ded-107">Table of Contents</span></span>

- [<span data-ttu-id="64ded-108">Критические изменения в командлетах Compute</span><span class="sxs-lookup"><span data-stu-id="64ded-108">Breaking changes to Compute cmdlets</span></span>](#breaking-changes-to-compute-cmdlets)
- [<span data-ttu-id="64ded-109">Критические изменения в командлетах EventHub</span><span class="sxs-lookup"><span data-stu-id="64ded-109">Breaking changes to EventHub cmdlets</span></span>](#breaking-changes-to-eventhub-cmdlets)
- [<span data-ttu-id="64ded-110">Критические изменения в командлетах Insights</span><span class="sxs-lookup"><span data-stu-id="64ded-110">Breaking changes to Insights cmdlets</span></span>](#breaking-changes-to-insights-cmdlets)
- [<span data-ttu-id="64ded-111">Критические изменения в командлетах Network</span><span class="sxs-lookup"><span data-stu-id="64ded-111">Breaking changes to Network cmdlets</span></span>](#breaking-changes-to-network-cmdlets)
- [<span data-ttu-id="64ded-112">Критические изменения в командлетах ServiceBus</span><span class="sxs-lookup"><span data-stu-id="64ded-112">Breaking changes to ServiceBus cmdlets</span></span>](#breaking-changes-to-servicebus-cmdlets)
- [<span data-ttu-id="64ded-113">Критические изменения в командлетах Sql</span><span class="sxs-lookup"><span data-stu-id="64ded-113">Breaking changes to Sql cmdlets</span></span>](#breaking-changes-to-sql-cmdlets)
- [<span data-ttu-id="64ded-114">Критические изменения в командлетах Storage</span><span class="sxs-lookup"><span data-stu-id="64ded-114">Breaking changes to Storage cmdlets</span></span>](#breaking-changes-to-storage-cmdlets)
- [<span data-ttu-id="64ded-115">Критические изменения в командлетах Profile</span><span class="sxs-lookup"><span data-stu-id="64ded-115">Breaking Changes to Profile Cmdlets</span></span>](#breaking-changes-to-profile-cmdlets)
  ## <a name="breaking-changes-to-compute-cmdlets"></a><span data-ttu-id="64ded-116">Критические изменения в командлетах Compute</span><span class="sxs-lookup"><span data-stu-id="64ded-116">Breaking changes to Compute cmdlets</span></span>

<span data-ttu-id="64ded-117">В этом выпуске затронуты следующие типы выходных данных:</span><span class="sxs-lookup"><span data-stu-id="64ded-117">The following output types were affected this release:</span></span>

### <a name="psvirtualmachine"></a><span data-ttu-id="64ded-118">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="64ded-118">PSVirtualMachine</span></span>
- <span data-ttu-id="64ded-119">Свойства верхнего уровня `DataDiskNames` и `NetworkInterfaceIDs` объекта `PSVirtualMachine` удалены из типа выходных данных.</span><span class="sxs-lookup"><span data-stu-id="64ded-119">Top level properties `DataDiskNames` and `NetworkInterfaceIDs` of nthe `PSVirtualMachine` object have been removed from the output type.</span></span> <span data-ttu-id="64ded-120">Эти свойства всегда были доступны в свойствах `StorageProfile` и `NetworkProfile` объекта `PSVirtualMachine`. Там их можно будет найти и в дальнейшем.</span><span class="sxs-lookup"><span data-stu-id="64ded-120">These properties have always been available in the `StorageProfile` and `NetworkProfile` properties of the `PSVirtualMachine` object and will be the way they will need to be accessed going forward.</span></span>
- <span data-ttu-id="64ded-121">Это изменение затрагивает следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="64ded-121">This change affects the following cmdlets:</span></span>
    - `Add-AzureRmVMDataDisk`
    - `Add-AzureRmVMNetworkInterface`
    - `Get-AzureRmVM`
    - `Remove-AzureRmVMDataDisk`
    - `Remove-AzureRmVMNetworkInterface`
    - `Set-AzureRmVMDataDisk`

```powershell-interactive
# Old
$vm.DataDiskNames
$vm.NetworkInterfaceIDs

# New
$vm.StorageProfile.DataDisks | Select -Property Name
$vm.NetworkProfile.NetworkInterfaces | Select -Property Id
```

## <a name="breaking-changes-to-eventhub-cmdlets"></a><span data-ttu-id="64ded-122">Критические изменения в командлетах EventHub</span><span class="sxs-lookup"><span data-stu-id="64ded-122">Breaking changes to EventHub cmdlets</span></span>

<span data-ttu-id="64ded-123">В этом выпуске затронуты следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="64ded-123">The following cmdlets were affected this release:</span></span>

### <a name="get-azurermeventhubnamespace"></a><span data-ttu-id="64ded-124">Get-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="64ded-124">Get-AzureRmEventHubNamespace</span></span>
- <span data-ttu-id="64ded-125">Свойство `ResourceGroupName` удалено из типа выходных данных `NamespaceAttributes`.</span><span class="sxs-lookup"><span data-stu-id="64ded-125">The property `ResourceGroupName` has been removed from the output type `NamespaceAttributes`</span></span>

### <a name="new-azurermeventhubnamespace"></a><span data-ttu-id="64ded-126">New-AzureRmEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="64ded-126">New-AzureRmEventHubNamespace</span></span>
- <span data-ttu-id="64ded-127">Свойство `ResourceGroupName` удалено из типа выходных данных `NamespaceAttributes`.</span><span class="sxs-lookup"><span data-stu-id="64ded-127">The property `ResourceGroupName` has been removed from the output type `NamespaceAttributes`</span></span>

## <a name="breaking-changes-to-insights-cmdlets"></a><span data-ttu-id="64ded-128">Критические изменения в командлетах Insights</span><span class="sxs-lookup"><span data-stu-id="64ded-128">Breaking changes to Insights cmdlets</span></span>

<span data-ttu-id="64ded-129">В этом выпуске затронуты следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="64ded-129">The following cmdlets were affected this release:</span></span>
    
### <a name="get-azurermusage"></a><span data-ttu-id="64ded-130">Get-AzureRmUsage</span><span class="sxs-lookup"><span data-stu-id="64ded-130">Get-AzureRmUsage</span></span>
- <span data-ttu-id="64ded-131">Этот командлет отмечен как нерекомендуемый.</span><span class="sxs-lookup"><span data-stu-id="64ded-131">This cmdlet has been deprecated.</span></span>

### <a name="remove-azurermalertrule"></a><span data-ttu-id="64ded-132">Remove-AzureRmAlertRule:</span><span class="sxs-lookup"><span data-stu-id="64ded-132">Remove-AzureRmAlertRule</span></span>
- <span data-ttu-id="64ded-133">Выходные данные этого командлета изменились со списка с одним объектом на один объект. Этот объект включает идентификатор запроса и код состояния.</span><span class="sxs-lookup"><span data-stu-id="64ded-133">The output of this cmdlet has changed from a list with a single object to a single object; this object includes the requestId, and status code.</span></span>
    
```powershell-interactive
# Old  
$s1 = Remove-AzureRmAlertRule -ResourceGroup $resourceGroup -name chiricutin
if ($s1 -ne $null)
{
    $r = $s1(0).RequestId
    $s = $s1(0).StatusCode
}

# New
$s1 = Remove-AzureRmAlertRule -ResourceGroup $resourceGroup -name chiricutin
$r = $s1.RequestId
$s = $s1.StatusCode
```
    
### <a name="add-azurermlogalertrule"></a><span data-ttu-id="64ded-134">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="64ded-134">Add-AzureRmLogAlertRule</span></span>
- <span data-ttu-id="64ded-135">Этот командлет отмечен как нерекомендуемый.</span><span class="sxs-lookup"><span data-stu-id="64ded-135">This cmdlet has been deprecated.</span></span>
    
### <a name="get-azurermalertrule"></a><span data-ttu-id="64ded-136">Get-AzureRmAlertRule:</span><span class="sxs-lookup"><span data-stu-id="64ded-136">Get-AzureRmAlertRule</span></span>
- <span data-ttu-id="64ded-137">Каждый элемент выходных данных (список объектов) этого командлета преобразован в плоскую структуру, т. е. вместо возвращения объектов со структурой `{ Id, Location, Name, Tags, Properties }` он будет возвращать объекты со структурой `{ Id, Location, Name, Tags, Type, Description, IsEnabled, Condition, Actions, LastUpdatedTime, ...}`. Она представляет собой все атрибуты Resource в Azure, а также все атрибуты AlertRuleResource верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="64ded-137">Each element of the output (a list of objects) of this cmdlet is flattened, i.e. instead of returning objects with the structure `{ Id, Location, Name, Tags, Properties }` it will return objects with the structure `{ Id, Location, Name, Tags, Type, Description, IsEnabled, Condition, Actions, LastUpdatedTime, ...}`, which is all of the attributes of an Azure Resource plus all of the attributes of an AlertRuleResource at the top level.</span></span>
    
```powershell-interactive
# Old
$rules = Get-AzureRmAlertRule -ResourceGroup $resourceGroup
if ($rules -and $rules.count -ge 1)
{
    Write-Host -fore red "Error updating alert rule"
      
    Write-Host $rules(0).Id
    Write-Host $rules(0).Properties.IsEnabled
    Write-Host $rules(0).Properties.Condition
}

# New
$rules = Get-AzureRmAlertRule -ResourceGroup $resourceGroup
if ($rules -and $rules.count -ge 1)
{
    Write-Host -fore red "Error updating alert rule"
 
    Write-Host $rules(0).Id
      
    # Properties will remain for a while
    Write-Host $rules(0).Properties.IsEnabled
      
    # But the properties will be at the top level too. Later Properties will be removed
    Write-Host $rules(0).IsEnabled
    Write-Host $rules(0).Condition
}
```
    
### <a name="get-azurermautoscalesetting"></a><span data-ttu-id="64ded-138">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="64ded-138">Get-AzureRmAutoscaleSetting</span></span>
- <span data-ttu-id="64ded-139">Поле `AutoscaleSettingResourceName` отмечено как нерекомендуемое, так как его значение всегда совпадало со значением поля `Name`.</span><span class="sxs-lookup"><span data-stu-id="64ded-139">The `AutoscaleSettingResourceName` field is deprecated since it always has the same value as the `Name` field.</span></span>

```powershell-interactive
# Old  
$s1 = Get-AzureRmAutoscaleSetting -ResourceGroup $resourceGroup -Name MySetting
if ($s1.AutoscaleSettingResourceName -ne $s1.Name)
{
    Write-Host "There is something wrong with the name"
}

# New
$s1 = Get-AzureRmAutoscaleSetting -ResourceGroup $resourceGroup -Name MySetting
    
# There won't be a AutoscaleSettingResourceName
Write-Host $s1.Name
```
    
### <a name="remove-azurermlogprofile"></a><span data-ttu-id="64ded-140">Remove-AzureRmLogProfile:</span><span class="sxs-lookup"><span data-stu-id="64ded-140">Remove-AzureRmLogProfile</span></span>
- <span data-ttu-id="64ded-141">Выходные данные командлета изменятся с `Boolean` на объект, содержащий `RequestId` и `StatusCode`.</span><span class="sxs-lookup"><span data-stu-id="64ded-141">The output of this cmdlet will change from `Boolean` to and object containing `RequestId` and `StatusCode`</span></span>

```powershell-interactive
# Old  
$s1 = Remove-AzureRmLogProfile -Name myLogProfile
if ($s1 -eq $true)
{
    Write-Host "Removed"
}
else
{
    Write-Host "Failed"
}

# New
$s1 = Remove-AzureRmLogProfile -Name myLogProfile
$r = $s1.RequestId
$s = $s1.StatusCode
```
    
### <a name="add-azurermlogprofile"></a><span data-ttu-id="64ded-142">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="64ded-142">Add-AzureRmLogProfile</span></span>
- <span data-ttu-id="64ded-143">Выходные данные командлета изменятся с объекта, содержащего идентификатор запроса, код состояния и данные обновленного или только что созданного ресурса.</span><span class="sxs-lookup"><span data-stu-id="64ded-143">The output of this cmdlet will change from an object that includes the requestId, status code, and the updated or newly created resource</span></span>
    
```powershell-interactive
# Old  
$s1 = Add-AzureRmLogProfile -Name default -StorageAccountId /subscriptions/df602c9c-7aa0-407d-a6fb-eb20c8bd1192/resourceGroups/JohnKemTest/providers/Microsoft.Storage/storageAccounts/johnkemtest8162 -Locations Global -categ Delete, Write, Action -retention 3
$r = $s1.ServiceBusRuleId

# New
$s1 = Add-AzureRmLogProfile -Name default -StorageAccountId /subscriptions/df602c9c-7aa0-407d-a6fb-eb20c8bd1192/resourceGroups/JohnKemTest/providers/Microsoft.Storage/storageAccounts/johnkemtest8162 -Locations Global -categ Delete, Write, Action -retention 3
$r = $s1.RequestId
$s = $s1.StatusCode
$a = $s1.NewResource.ServiceBusRuleId
    
```
    
### <a name="set-azurermdiagnosticsettings"></a><span data-ttu-id="64ded-144">Set-AzureRmDiagnosticSettings</span><span class="sxs-lookup"><span data-stu-id="64ded-144">Set-AzureRmDiagnosticSettings</span></span>
- <span data-ttu-id="64ded-145">Команда будет переименована в `Update-AzureRmDiagnosticSettings`.</span><span class="sxs-lookup"><span data-stu-id="64ded-145">The command is going to be renamed to `Update-AzureRmDiagnosticSettings`</span></span>

```powershell-interactive
# Old
Set-AzureRmDiagnosticSettings

# New
Update-AzureRmDiagnosticSettings
```

## <a name="breaking-changes-to-network-cmdlets"></a><span data-ttu-id="64ded-146">Критические изменения в командлетах Network</span><span class="sxs-lookup"><span data-stu-id="64ded-146">Breaking changes to Network cmdlets</span></span>

<span data-ttu-id="64ded-147">В этом выпуске затронуты следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="64ded-147">The following cmdlets were affected this release:</span></span>

### <a name="new-azurermvirtualnetworkgatewayconnection"></a><span data-ttu-id="64ded-148">New-AzureRmVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="64ded-148">New-AzureRmVirtualNetworkGatewayConnection</span></span>
- <span data-ttu-id="64ded-149">Параметр `EnableBgp` изменен. Теперь он принимает `boolean` вместо `string`.</span><span class="sxs-lookup"><span data-stu-id="64ded-149">`EnableBgp` parameter has been changed to take a `boolean` instead of a `string`</span></span>

```powershell-interactive
# Old
New-AzureRmVirtualNetworkGatewayConnection -ResourceGroupName "RG" -name "conn1" -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -SharedKey "key" -EnableBgp "true"

# New
New-AzureRmVirtualNetworkGatewayConnection -ResourceGroupName "RG" -name "conn1" -VirtualNetworkGateway1 $vnetGateway -LocalNetworkGateway2 $localnetGateway -ConnectionType IPsec -SharedKey "key" -EnableBgp $true
```

## <a name="breaking-changes-to-servicebus-cmdlets"></a><span data-ttu-id="64ded-150">Критические изменения в командлетах ServiceBus</span><span class="sxs-lookup"><span data-stu-id="64ded-150">Breaking changes to ServiceBus cmdlets</span></span>

<span data-ttu-id="64ded-151">В этом выпуске затронуты следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="64ded-151">The following cmdlets were affected this release:</span></span>

### <a name="get-azurermservicebusnamespace"></a><span data-ttu-id="64ded-152">Get-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="64ded-152">Get-AzureRmServiceBusNamespace</span></span>
- <span data-ttu-id="64ded-153">Свойство `ResourceGroupName` удалено из типа выходных данных `NamespaceAttributes`.</span><span class="sxs-lookup"><span data-stu-id="64ded-153">The property `ResourceGroupName` has been removed from the output type `NamespaceAttributes`</span></span>

### <a name="new-azurermservicebusnamespace"></a><span data-ttu-id="64ded-154">New-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="64ded-154">New-AzureRmServiceBusNamespace</span></span>

- <span data-ttu-id="64ded-155">Свойство `ResourceGroupName` удалено из типа выходных данных `NamespaceAttributes`.</span><span class="sxs-lookup"><span data-stu-id="64ded-155">The property `ResourceGroupName` has been removed from the output type `NamespaceAttributes`</span></span>

## <a name="breaking-changes-to-sql-cmdlets"></a><span data-ttu-id="64ded-156">Критические изменения в командлетах Sql</span><span class="sxs-lookup"><span data-stu-id="64ded-156">Breaking changes to Sql cmdlets</span></span>

<span data-ttu-id="64ded-157">В этом выпуске затронуты следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="64ded-157">The following cmdlets were affected this release:</span></span>

### <a name="new-azurermsqldatabasefailovergroup"></a><span data-ttu-id="64ded-158">New-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="64ded-158">New-AzureRmSqlDatabaseFailoverGroup</span></span>
- <span data-ttu-id="64ded-159">Параметр `Tag` удален.</span><span class="sxs-lookup"><span data-stu-id="64ded-159">`Tag` parameter has been removed</span></span>
- <span data-ttu-id="64ded-160">Параметр `GracePeriodWithDataLossHour` переименован в `GracePeriodWithDataLossHours`.</span><span class="sxs-lookup"><span data-stu-id="64ded-160">`GracePeriodWithDataLossHour` parameter has been renamed to `GracePeriodWithDataLossHours`</span></span>

```powershell-interactive
# Old
New-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -FailoverPolicy Automatic -GracePeriodWithDataLossHour 1 -Tag @{ Environment="Test" }

# New
New-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

### <a name="set-azurermsqldatabasefailovergroup"></a><span data-ttu-id="64ded-161">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="64ded-161">Set-AzureRmSqlDatabaseFailoverGroup</span></span>
- <span data-ttu-id="64ded-162">Параметр `Tag` удален.</span><span class="sxs-lookup"><span data-stu-id="64ded-162">`Tag` parameter has been removed</span></span>
- <span data-ttu-id="64ded-163">Параметр `GracePeriodWithDataLossHour` переименован в `GracePeriodWithDataLossHours`.</span><span class="sxs-lookup"><span data-stu-id="64ded-163">`GracePeriodWithDataLossHour` parameter has been renamed to `GracePeriodWithDataLossHours`</span></span>

```powershell-interactive
# Old
Set-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHour 1 -Tag @{ Environment="Test" }

# New
Set-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

### <a name="add-azurermsqldatabasetofailovergroup"></a><span data-ttu-id="64ded-164">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="64ded-164">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>
- <span data-ttu-id="64ded-165">Параметр `Tag` удален.</span><span class="sxs-lookup"><span data-stu-id="64ded-165">`Tag` parameter has been removed</span></span>

```powershell-interactive
# Old
Add-AzureRmSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1 -Tag @{ Environment="Test" }

# New
Add-AzureRmSqlDatabaseToFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1
```

###  <a name="remove-azurermsqldatabasefromfailovergroup"></a><span data-ttu-id="64ded-166">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="64ded-166">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>
- <span data-ttu-id="64ded-167">Параметр `Tag` удален.</span><span class="sxs-lookup"><span data-stu-id="64ded-167">`Tag` parameter has been removed</span></span>

```powershell-interactive
# Old
Remove-AzureRmSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1 -Tag @{ Environment="Test" }

# New
Remove-AzureRmSqlDatabaseFromFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -Database $db1
```

### <a name="remove-azurermsqldatabasefailovergroup"></a><span data-ttu-id="64ded-168">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="64ded-168">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>
- <span data-ttu-id="64ded-169">Параметр `PartnerResourceGroupName` удален.</span><span class="sxs-lookup"><span data-stu-id="64ded-169">`PartnerResourceGroupName` parameter has been removed</span></span>
- <span data-ttu-id="64ded-170">Параметр `PartnerServerName` удален.</span><span class="sxs-lookup"><span data-stu-id="64ded-170">`PartnerServerName` parameter has been removed</span></span>

```powershell-interactive
# Old
Remove-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg -PartnerServerName server2 -PartnerResourceGroupName rg

# New
Remove-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server1 -FailoverGroupName fg
```

### <a name="set-azurermsqldatabasethreatdetectionpolicy"></a><span data-ttu-id="64ded-171">Set-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="64ded-171">Set-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>
- <span data-ttu-id="64ded-172">Значение `Usage_Anomaly` больше не является допустимым для параметра `ExcludedDetectionType`.</span><span class="sxs-lookup"><span data-stu-id="64ded-172">The value `Usage_Anomaly` is no longer valid for the parameter `ExcludedDetectionType`</span></span>

### <a name="set-azurermsqlserverthreatdetectionpolicy"></a><span data-ttu-id="64ded-173">Set-AzureRmSqlServerThreatDetectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="64ded-173">Set-AzureRmSqlServerThreatDetectionPolicy</span></span>
- <span data-ttu-id="64ded-174">Значение `Usage_Anomaly` больше не является допустимым для параметра `ExcludedDetectionType`.</span><span class="sxs-lookup"><span data-stu-id="64ded-174">The value `Usage_Anomaly` is no longer valid for the parameter `ExcludedDetectionType`</span></span>

## <a name="breaking-changes-to-storage-cmdlets"></a><span data-ttu-id="64ded-175">Критические изменения в командлетах Storage</span><span class="sxs-lookup"><span data-stu-id="64ded-175">Breaking changes to Storage cmdlets</span></span>

<span data-ttu-id="64ded-176">В этом выпуске затронуты следующие свойства типов выходных данных:</span><span class="sxs-lookup"><span data-stu-id="64ded-176">The following output type properties were affected this release:</span></span>

### <a name="azurestorageblobicloudblobserviceclient"></a><span data-ttu-id="64ded-177">AzureStorageBlob.ICloudBlob.ServiceClient</span><span class="sxs-lookup"><span data-stu-id="64ded-177">AzureStorageBlob.ICloudBlob.ServiceClient</span></span>
- <span data-ttu-id="64ded-178">Из этого типа удалены следующие свойства (_примечание:_ они по-прежнему находятся в свойстве `DefaultRequestOptions`):</span><span class="sxs-lookup"><span data-stu-id="64ded-178">The following properties were removed from this type (_note_: they can still be found in `DefaultRequestOptions` property):</span></span>
    - `LocationMode`
    - `MaximumExecutionTime`
    - `ServerTimeout`
    - `ParallelOperationThreadCount`
    - `SingleBlobUploadThresholdInBytes`
- <span data-ttu-id="64ded-179">Это изменение затрагивает следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="64ded-179">This change affects the following cmdlets:</span></span>
    - `Get-AzureStorageBlob`
    - `Get-AzureStorageBlobContent`
    - `Get-AzureStorageBlobCopyState`
    - `Set-AzureStorageBlobContent`
    - `Start-AzureStorageBlobCopy`
    - `Stop-AzureStorageBlobCopy`
    
### <a name="azurestoragecontainercloudblobcontainerserviceclient"></a><span data-ttu-id="64ded-180">AzureStorageContainer.CloudBlobContainer.ServiceClient</span><span class="sxs-lookup"><span data-stu-id="64ded-180">AzureStorageContainer.CloudBlobContainer.ServiceClient</span></span>
- <span data-ttu-id="64ded-181">Из этого типа удалены следующие свойства (_примечание:_ они по-прежнему находятся в свойстве `DefaultRequestOptions`):</span><span class="sxs-lookup"><span data-stu-id="64ded-181">The following properties were removed from this type (_note_: they can still be found in the `DefaultRequestOptions` property):</span></span>
    - `LocationMode`
    - `MaximumExecutionTime`
    - `ServerTimeout`
    - `ParallelOperationThreadCount`
    - `SingleBlobUploadThresholdInBytes`
- <span data-ttu-id="64ded-182">Это изменение затрагивает следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="64ded-182">This change affects the following cmdlets:</span></span>
    - `Get-AzureStorageContainer`
    - `New-AzureStorageContainer`
    - `Set-AzureStorageContainerAcl`
    
### <a name="azurestoragequeuecloudqueueserviceclient"></a><span data-ttu-id="64ded-183">AzureStorageQueue.CloudQueue.ServiceClient</span><span class="sxs-lookup"><span data-stu-id="64ded-183">AzureStorageQueue.CloudQueue.ServiceClient</span></span>
- <span data-ttu-id="64ded-184">Из этого типа удалены следующие свойства (_примечание:_ они по-прежнему находятся в свойстве `DefaultRequestOptions`):</span><span class="sxs-lookup"><span data-stu-id="64ded-184">The following properties were removed from this type (_note_: they can still be found in the `DefaultRequestOptions` property):</span></span>
    - `LocationMode`
    - `MaximumExecutionTime`
    - `RetryPolicy`
    - `ServerTimeout`
- <span data-ttu-id="64ded-185">Это изменение затрагивает следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="64ded-185">This change affects the following cmdlets:</span></span>
    - `Get-AzureStorageQueue`
    - `New-AzureStorageQueue`
    
### <a name="azurestoragetablecloudtableserviceclient"></a><span data-ttu-id="64ded-186">AzureStorageTable.CloudTable.ServiceClient</span><span class="sxs-lookup"><span data-stu-id="64ded-186">AzureStorageTable.CloudTable.ServiceClient</span></span>
- <span data-ttu-id="64ded-187">Из этого типа удалены следующие свойства (_примечание:_ они по-прежнему находятся в свойстве `DefaultRequestOptions`):</span><span class="sxs-lookup"><span data-stu-id="64ded-187">The following properties were removed from this type (_note_: they can still be found in the `DefaultRequestOptions` property):</span></span>
    - `LocationMode`
    - `MaximumExecutionTime`
    - `PayloadFormat`
    - `RetryPolicy`
    - `ServerTimeout`
- <span data-ttu-id="64ded-188">Это изменение затрагивает следующие командлеты:</span><span class="sxs-lookup"><span data-stu-id="64ded-188">This change affects the following cmdlets:</span></span>
    - `Get-AzureStorageTable`
    - `New-AzureStorageTable`
    
```powershell-interactive
# Old
$LocationMode = (Get-AzureStorageBlob -Container $containername)[0].ICloudBlob.ServiceClient.LocationMode       
$ParallelOperationThreadCount = (Get-AzureStorageContainer -Container $containername).CloudBlobContainer.ServiceClient.ParallelOperationThreadCount
$PayloadFormat = (Get-AzureStorageTable -Name $tablename).CloudTable.ServiceClient.PayloadFormat
$RetryPolicy = (Get-AzureStorageQueue -Name $queuename).CloudQueue.ServiceClient.RetryPolicy

# New
$LocationMode = (Get-AzureStorageBlob -Container $containername)[0].ICloudBlob.ServiceClient.DefaultRequestOptions.LocationMode     
$ParallelOperationThreadCount = (Get-AzureStorageContainer -Container $containername).CloudBlobContainer.ServiceClient.DefaultRequestOptions.ParallelOperationThreadCount
$PayloadFormat = (Get-AzureStorageTable -Name $tablename).CloudTable.ServiceClient.DefaultRequestOptions.PayloadFormat
$RetryPolicy = (Get-AzureStorageQueue -Name $queuename).CloudQueue.ServiceClient.DefaultRequestOptions.RetryPolicy
```

## <a name="breaking-changes-to-profile-cmdlets"></a><span data-ttu-id="64ded-189">Критические изменения в командлетах Profile</span><span class="sxs-lookup"><span data-stu-id="64ded-189">Breaking Changes to Profile Cmdlets</span></span>

<span data-ttu-id="64ded-190">В этом выпуске изменены указанные ниже командлеты и типы выходных данных командлетов.</span><span class="sxs-lookup"><span data-stu-id="64ded-190">The following cmdlets and cmdlet output types were changed in this release.</span></span>

### <a name="add-azurermaccount-breaking-changes"></a><span data-ttu-id="64ded-191">Критические изменения в AzureRmAccount</span><span class="sxs-lookup"><span data-stu-id="64ded-191">Add-AzureRmAccount breaking changes</span></span>

- <span data-ttu-id="64ded-192">Параметр ```EnvironmentName``` удален и заменен на ```Environment```. ```Environment``` теперь принимает строку, а не объект ```AzureEnvironment```.</span><span class="sxs-lookup"><span data-stu-id="64ded-192">```EnvironmentName``` parameter has been removed and replaced with ```Environment```, the ```Environment``` now takes a string and not an ```AzureEnvironment``` object</span></span>

```powershell-interactive
# Old
Add-AzureRmAccount -EnvironmentName AzureChinaCloud

# New
Add-AzureRmAccount -Environment AzureChinaCloud
```

### <a name="select-azurermprofile-was-renamed-to-import-azurermcontext"></a><span data-ttu-id="64ded-193">Параметр Select-AzureRmProfile переименован в Import-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="64ded-193">Select-AzureRmProfile was renamed to Import-AzureRmContext</span></span>

<span data-ttu-id="64ded-194">Параметр ```Select-AzureRmProfile``` переименован в ```Import-AzureRmContext```.</span><span class="sxs-lookup"><span data-stu-id="64ded-194">```Select-AzureRmProfile``` was renamed to ```Import-AzureRmContext```</span></span>

```powershell-interactive
# Old
Select-AzureRmProfile -Path c:\mydir\myprofile.json

# New
Import-AzureRmContext -Path c:\mydir\myprofile.json
```

### <a name="save-azurermprofile-was-renamed-to-save-azurermcontext"></a><span data-ttu-id="64ded-195">Параметр Save-AzureRmProfile переименован в Save-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="64ded-195">Save-AzureRmProfile was renamed to Save-AzureRmContext</span></span>

<span data-ttu-id="64ded-196">Параметр ```Save-AzureRmProfile``` переименован в ```Save-AzureRmContext```.</span><span class="sxs-lookup"><span data-stu-id="64ded-196">```Save-AzureRmProfile``` was renamed to ```Save-AzureRmContext```</span></span>

```powershell-interactive
# Old
Save-AzureRmProfile -Path c:\mydir\myprofile.json

# New
Save-AzureRmContext -Path c:\mydir\myprofile.json
```
### <a name="breaking-changes-to-output-psazurecontext-type"></a><span data-ttu-id="64ded-197">Критические изменения в типе выходных данных PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="64ded-197">Breaking Changes to output PSAzureContext Type</span></span>

- <span data-ttu-id="64ded-198">Свойство ```TokenCache``` изменено на тип, реализующий ```IAzureTokenCache``` вместо ```byte[]```.</span><span class="sxs-lookup"><span data-stu-id="64ded-198">The ```TokenCache``` property changed to a type that implements ```IAzureTokenCache``` instead of a ```byte[]```</span></span>

```powershell-interactive
# Old
$bytes = (Get-AzureRmContext).TokenCache
$bytes = (Set-AzureRmContext -SubscriptionId xxx-xxx-xxx-xxx).TokenCache
$bytes = (Add-AzureRmAccount).Context.TokenCache

# New
$bytes = (Get-AzureRmContext).TokenCache.CacheData
$bytes = (Set-AzureRmContext -SubscriptionId xxx-xxx-xxx-xxx).TokenCache.CacheData
$bytes = (Add-AzureRmAccount).Context.TokenCache.CacheData
```

### <a name="breaking-changes-to-the-output-psazureaccount-type"></a><span data-ttu-id="64ded-199">Критические изменения в типе выходных данных PSAzureAccount</span><span class="sxs-lookup"><span data-stu-id="64ded-199">Breaking Changes to the output PSAzureAccount Type</span></span>

- <span data-ttu-id="64ded-200">Свойство ```AccountType``` изменено на ```Type```.</span><span class="sxs-lookup"><span data-stu-id="64ded-200">The ```AccountType``` property was changed to ```Type```</span></span>

```powershell-interactive
# Old
$type = (Get-AzureRmContext).Account.AccountType
$type = (Set-AzureRmContext -SubscriptionId xxx-xxx-xxx-xxx).Account.AccountType
$type = (Add-AzureRmAccount).Context.Account.AccountType

# New 
$type = (Get-AzureRmContext).Account.Type
$type = (Set-AzureRmContext -SubscriptionId xxx-xxx-xxx-xxx).Account.Type
$type = (Add-AzureRmAccount).Context.Account.Type
```

### <a name="breaking-changes-to-the-output-psazuresubscription-type"></a><span data-ttu-id="64ded-201">Критические изменения в типе выходных данных PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="64ded-201">Breaking Changes to the output PSAzureSubscription Type</span></span>
- <span data-ttu-id="64ded-202">Свойство ```SubscriptionId``` изменено на ```Id```.</span><span class="sxs-lookup"><span data-stu-id="64ded-202">The ```SubscriptionId``` property was changed to ```Id```</span></span>

```powershell-interactive
# Old
$id =(Get-AzureRmSubscription -SubscriptionId xxxx-xxxx-xxxx-xxxx).SubscriptionId
$id =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Subscription.SubscriptionId
$id =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.SubscriptionId
$id =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.SubscriptionId

# New
$id =(Get-AzureRmSubscription -SubscriptionId xxxx-xxxx-xxxx-xxxx).Id
$id =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Subscription.Id
$id =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.Id
$id =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.Id
```

- <span data-ttu-id="64ded-203">Свойство ```SubscriptionName``` изменено на ```Name```.</span><span class="sxs-lookup"><span data-stu-id="64ded-203">The ```SubscriptionName``` property was changed to ```Name```</span></span>

```powershell-interactive
# Old
$name =(Get-AzureRmSubscription -SubscriptionId xxxx-xxxx-xxxx-xxxx).SubscriptionName
$name =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Subscription.SubscriptionName
$name =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.SubscriptionName
$name =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.SubscriptionName

# New
$name =(Get-AzureRmSubscription -SubscriptionId xxxx-xxxx-xxxx-xxxx).Name
$name =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Subscription.Name
$name =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.Name
$name =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Subscription.Name
```

### <a name="breaking-changes-to-the-output-psazuretenant-type"></a><span data-ttu-id="64ded-204">Критические изменения в типе выходных данных PSAzureTenant</span><span class="sxs-lookup"><span data-stu-id="64ded-204">Breaking Changes to the output PSAzureTenant Type</span></span>

- <span data-ttu-id="64ded-205">Свойство ```TenantId``` изменено на ```Id```.</span><span class="sxs-lookup"><span data-stu-id="64ded-205">The ```TenantId``` property was changed to ```Id```</span></span>

```powershell-interactive
# Old
$id =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).TenantId
$id =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Tenant.TenantId
$id =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Tenant.TenantId
$id =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Tenant.TenantId

# New
$id =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).Id
$id =(Add-AzureRmAccount -SubscriptionId xxxx-xxxx-xxxx-xxxx).Context.Tenant.Id
$id =(Get-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Tenant.Id
$id =(Set-AzureRmContext -SubscriptionId xxxx-xxxx-xxxx-xxxx).Tenant.Id
```

- <span data-ttu-id="64ded-206">Свойство ```Domain``` изменено на ```Directory```.</span><span class="sxs-lookup"><span data-stu-id="64ded-206">The ```Domain``` property was changed to ```Directory```</span></span>

```powershell-interactive
# Old
$tenantName =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).Domain

# New
$tenantName =(Get-AzureRmTenant -TenantId xxxx-xxxx-xxxx-xxxx).Directory
```
