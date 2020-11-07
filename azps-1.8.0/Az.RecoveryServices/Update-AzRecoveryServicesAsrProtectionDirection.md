---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrprotectiondirection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionDirection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionDirection.md
ms.openlocfilehash: 9dd28cd3a05db15cef64a1e6023b1684909fdc13
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729575"
---
# <span data-ttu-id="bdbd9-101">Update-AzRecoveryServicesAsrProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="bdbd9-101">Update-AzRecoveryServicesAsrProtectionDirection</span></span>

## <span data-ttu-id="bdbd9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bdbd9-102">SYNOPSIS</span></span>
<span data-ttu-id="bdbd9-103">Обновляет направление репликации для указанного защищенного элемента или плана восстановления для репликации.</span><span class="sxs-lookup"><span data-stu-id="bdbd9-103">Updates the replication direction for the specified replication protected item or recovery plan.</span></span> <span data-ttu-id="bdbd9-104">Используется для повторной защиты или обратной репликации, которая переносит отказ на реплицируемый элемент или план восстановления.</span><span class="sxs-lookup"><span data-stu-id="bdbd9-104">Used to re-protect/reverse replicate a failed over replicated item or recovery plan.</span></span>

## <span data-ttu-id="bdbd9-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bdbd9-105">SYNTAX</span></span>

### <span data-ttu-id="bdbd9-106">ByRPIObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bdbd9-106">ByRPIObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdbd9-107">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="bdbd9-107">AzureToVMware</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToVMware] [-Account <ASRRunAsAccount>]
 -DataStore <ASRDataStore> [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 -RetentionVolume <ASRRetentionVolume> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bdbd9-108">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="bdbd9-108">VMwareToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-VMwareToAzure] -Account <ASRRunAsAccount>
 [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdbd9-109">HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="bdbd9-109">HyperVToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-HyperVToAzure] [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdbd9-110">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="bdbd9-110">EnterpriseToEnterprise</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-VmmToVmm]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdbd9-111">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="bdbd9-111">AzureToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToAzure]
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -LogStorageAccountId <String>
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-RecoveryResourceGroupId <String>] [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryBootDiagStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bdbd9-112">AzureToAzureWithMultipleStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bdbd9-112">AzureToAzureWithMultipleStorageAccount</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToAzure]
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-RecoveryResourceGroupId <String>]
 [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryBootDiagStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bdbd9-113">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="bdbd9-113">ByRPObject</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdbd9-114">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="bdbd9-114">ByPEObject</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -Direction <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bdbd9-115">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bdbd9-115">DESCRIPTION</span></span>
<span data-ttu-id="bdbd9-116">Командлет **Update-AzRecoveryServicesAsrProtectionDirection** обновляет направление репликации для указанного объекта Azure Site Recovery после завершения операции фиксации отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="bdbd9-116">The **Update-AzRecoveryServicesAsrProtectionDirection** cmdlet updates the replication direction for the specified Azure Site Recovery object after the completion of a commit failover operation.</span></span>

## <span data-ttu-id="bdbd9-117">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bdbd9-117">EXAMPLES</span></span>

### <span data-ttu-id="bdbd9-118">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bdbd9-118">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="bdbd9-119">Начните операцию направления обновления для указанного плана восстановления и возвращает объект задания ASR, который используется для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="bdbd9-119">Start the update direction operation for the specified recovery plan and returns the ASR job object used to track the operation.</span></span>

### <span data-ttu-id="bdbd9-120">Пример 2</span><span class="sxs-lookup"><span data-stu-id="bdbd9-120">Example 2</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzToAzure -ProtectionContainerMapping $B2ApcmMapping -LogStorageAccountId $cacheStorageId `
 -ReplicationProtectedItem $rpi
```

<span data-ttu-id="bdbd9-121">Начните операцию направления обновления для указанного элемента, защищенного репликацией, в целевом регионе Azure, определяемом сопоставлением контейнера защиты, и с помощью хранилища кэша (в том же регионе, что и VM).</span><span class="sxs-lookup"><span data-stu-id="bdbd9-121">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and using cache storage (in same region as VM).</span></span>

### <span data-ttu-id="bdbd9-122">Пример 3</span><span class="sxs-lookup"><span data-stu-id="bdbd9-122">Example 3</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzToAzure -ProtectionContainerMapping $B2ApcmMapping `
 -AzToAzureDiskReplicationConfiguration $disk1,$disk2 -ReplicationProtectedItem  $rpi
```

<span data-ttu-id="bdbd9-123">Начните операцию направления обновления для указанного элемента, защищенного репликацией, в целевом регионе Azure, определяемом сопоставлением контейнеров защиты и указанной конфигурацией репликации дисков.</span><span class="sxs-lookup"><span data-stu-id="bdbd9-123">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and provided disk replication configuration.</span></span>

## <span data-ttu-id="bdbd9-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bdbd9-124">PARAMETERS</span></span>

### <span data-ttu-id="bdbd9-125">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="bdbd9-125">-Account</span></span>
<span data-ttu-id="bdbd9-126">Учетная запись запуска от имени, которая будет использоваться для принудительной установки службы Mobility Service при необходимости.</span><span class="sxs-lookup"><span data-stu-id="bdbd9-126">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="bdbd9-127">Должен быть один из списка учетных записей запуска от имени в структуре ASR.</span><span class="sxs-lookup"><span data-stu-id="bdbd9-127">Must be one from the list of run as accounts in the ASR fabric.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: AzureToVMware
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdbd9-128">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="bdbd9-128">-AzureToAzure</span></span>
<span data-ttu-id="bdbd9-129">{{Fill AzureToAzure Description}}</span><span class="sxs-lookup"><span data-stu-id="bdbd9-129">{{Fill AzureToAzure Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdbd9-130">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="bdbd9-130">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="bdbd9-131">{{Fill AzureToAzureDiskReplicationConfiguration Description}}</span><span class="sxs-lookup"><span data-stu-id="bdbd9-131">{{Fill AzureToAzureDiskReplicationConfiguration Description}}</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdbd9-132">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="bdbd9-132">-AzureToVMware</span></span>
<span data-ttu-id="bdbd9-133">{{Fill AzureToVMware Description}}</span><span class="sxs-lookup"><span data-stu-id="bdbd9-133">{{Fill AzureToVMware Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToVMware
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdbd9-134">-DataStore</span><span class="sxs-lookup"><span data-stu-id="bdbd9-134">-DataStore</span></span>
<span data-ttu-id="bdbd9-135">Хранилище DataStore VMware, используемое для vmdisk.</span><span class="sxs-lookup"><span data-stu-id="bdbd9-135">The VMware datastore to be used for the vmdisk's.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRDataStore
Parameter Sets: AzureToVMware
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdbd9-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdbd9-136">-DefaultProfile</span></span>
<span data-ttu-id="bdbd9-137">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bdbd9-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdbd9-138">-Направление</span><span class="sxs-lookup"><span data-stu-id="bdbd9-138">-Direction</span></span>
<span data-ttu-id="bdbd9-139">Указывает направление, которое будет использоваться для операции обновления. Опубликуйте отработку отказа.</span><span class="sxs-lookup"><span data-stu-id="bdbd9-139">Specifies the direction to be used for the update operation post a failover.</span></span>
<span data-ttu-id="bdbd9-140">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="bdbd9-140">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bdbd9-141">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="bdbd9-141">PrimaryToRecovery</span></span>
- <span data-ttu-id="bdbd9-142">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="bdbd9-142">RecoveryToPrimary</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPIObject, AzureToVMware, VMwareToAzure, HyperVToAzure, EnterpriseToEnterprise, ByRPObject, ByPEObject
Aliases:
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdbd9-143">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="bdbd9-143">-HyperVToAzure</span></span>
<span data-ttu-id="bdbd9-144">Повторно включите защиту виртуальной машины Hyper-V после восстановления после сбоя.</span><span class="sxs-lookup"><span data-stu-id="bdbd9-144">Reprotect a Hyper-V virtual machine after failback.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: HyperVToAzure
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdbd9-145">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="bdbd9-145">-LogStorageAccountId</span></span>
<span data-ttu-id="bdbd9-146">Указывает идентификатор учетной записи хранения для хранения журнала репликации виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="bdbd9-146">Specifies the storage account ID to store the replication log of VMs.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, HyperVToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdbd9-147">-MasterTarget</span><span class="sxs-lookup"><span data-stu-id="bdbd9-147">-MasterTarget</span></span>
<span data-ttu-id="bdbd9-148">Сведения о главном целевом сервере.</span><span class="sxs-lookup"><span data-stu-id="bdbd9-148">Master Target Server Details.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRMasterTargetServer
Parameter Sets: AzureToVMware, VMwareToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdbd9-149">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="bdbd9-149">-ProcessServer</span></span>
<span data-ttu-id="bdbd9-150">Сервер обработки, который будет использоваться для репликации.</span><span class="sxs-lookup"><span data-stu-id="bdbd9-150">Process Server to be used for replication.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProcessServer
Parameter Sets: AzureToVMware, VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdbd9-151">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="bdbd9-151">-ProtectionContainerMapping</span></span>
<span data-ttu-id="bdbd9-152">ContainerMapping защиты, которую необходимо использовать для репликации.</span><span class="sxs-lookup"><span data-stu-id="bdbd9-152">Protection containerMapping to be used for replication.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping
Parameter Sets: AzureToVMware, VMwareToAzure, AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdbd9-153">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="bdbd9-153">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="bdbd9-154">Группа доступности, на которой должна быть создана виртуальная машина при переходе на другой ресурс</span><span class="sxs-lookup"><span data-stu-id="bdbd9-154">The availability set that the virtual machine should be created in upon failover</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdbd9-155">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="bdbd9-155">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="bdbd9-156">Указывает идентификатор учетной записи хранения Azure, на которую должна выполняться репликация.</span><span class="sxs-lookup"><span data-stu-id="bdbd9-156">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, HyperVToAzure, AzureToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdbd9-157">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="bdbd9-157">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="bdbd9-158">Указывает учетную запись хранения для диагностики загрузки для восстановления ВМ Azure.</span><span class="sxs-lookup"><span data-stu-id="bdbd9-158">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdbd9-159">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="bdbd9-159">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="bdbd9-160">Идентификатор ресурса облачной службы восстановления, на которую следует отработка отказа виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="bdbd9-160">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdbd9-161">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="bdbd9-161">-RecoveryPlan</span></span>
<span data-ttu-id="bdbd9-162">Указывает объект плана восстановления ASR.</span><span class="sxs-lookup"><span data-stu-id="bdbd9-162">Specifies an ASR recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bdbd9-163">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="bdbd9-163">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="bdbd9-164">Идентификатор resourceGroup восстановления для защищенной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="bdbd9-164">Recovery resourceGroup id for protected Vm.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdbd9-165">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="bdbd9-165">-ReplicationProtectedItem</span></span>
<span data-ttu-id="bdbd9-166">Задает защищенный элемент репликации ASR.</span><span class="sxs-lookup"><span data-stu-id="bdbd9-166">Specifies an ASR replication protected item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, AzureToVMware, VMwareToAzure, HyperVToAzure, EnterpriseToEnterprise, AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bdbd9-167">-RetentionVolume</span><span class="sxs-lookup"><span data-stu-id="bdbd9-167">-RetentionVolume</span></span>
<span data-ttu-id="bdbd9-168">Том хранения на главном целевом сервере, который нужно использовать.</span><span class="sxs-lookup"><span data-stu-id="bdbd9-168">Retention Volume on the master target server to be used.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRetentionVolume
Parameter Sets: AzureToVMware
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdbd9-169">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="bdbd9-169">-VmmToVmm</span></span>
<span data-ttu-id="bdbd9-170">Изменение направления репликации для сбоя на виртуальной машине Hyper-V, защищенной между двумя сайтами Hyper-V, управляемыми VMM.</span><span class="sxs-lookup"><span data-stu-id="bdbd9-170">Update replication direction for a failed over Hyper-V virtual machine that is protected between two VMM managed Hyper-V sites.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdbd9-171">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="bdbd9-171">-VMwareToAzure</span></span>
<span data-ttu-id="bdbd9-172">Обновите направление репликации с VMware на Azure.</span><span class="sxs-lookup"><span data-stu-id="bdbd9-172">Update replication direction from VMware to Azure.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VMwareToAzure
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdbd9-173">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bdbd9-173">-Confirm</span></span>
<span data-ttu-id="bdbd9-174">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bdbd9-174">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdbd9-175">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdbd9-175">-WhatIf</span></span>
<span data-ttu-id="bdbd9-176">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bdbd9-176">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bdbd9-177">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bdbd9-177">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdbd9-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdbd9-178">CommonParameters</span></span>
<span data-ttu-id="bdbd9-179">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bdbd9-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdbd9-180">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdbd9-180">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdbd9-181">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bdbd9-181">INPUTS</span></span>

### <span data-ttu-id="bdbd9-182">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="bdbd9-182">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="bdbd9-183">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="bdbd9-183">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="bdbd9-184">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bdbd9-184">OUTPUTS</span></span>

### <span data-ttu-id="bdbd9-185">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="bdbd9-185">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="bdbd9-186">Пуск</span><span class="sxs-lookup"><span data-stu-id="bdbd9-186">NOTES</span></span>

## <span data-ttu-id="bdbd9-187">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bdbd9-187">RELATED LINKS</span></span>
