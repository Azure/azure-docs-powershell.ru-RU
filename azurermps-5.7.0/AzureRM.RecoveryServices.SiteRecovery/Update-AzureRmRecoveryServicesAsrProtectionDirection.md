---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/update-azurermrecoveryservicesasrprotectiondirection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrProtectionDirection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrProtectionDirection.md
ms.openlocfilehash: 13d1829326695e2860caf99bf002dcf5da31caac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558867"
---
# <span data-ttu-id="20034-101">Update-AzureRmRecoveryServicesAsrProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="20034-101">Update-AzureRmRecoveryServicesAsrProtectionDirection</span></span>

## <span data-ttu-id="20034-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="20034-102">SYNOPSIS</span></span>
<span data-ttu-id="20034-103">Обновляет направление репликации для указанного защищенного элемента или плана восстановления для репликации.</span><span class="sxs-lookup"><span data-stu-id="20034-103">Updates the replication direction for the specified replication protected item or recovery plan.</span></span> <span data-ttu-id="20034-104">Используется для повторной защиты или обратной репликации, которая переносит отказ на реплицируемый элемент или план восстановления.</span><span class="sxs-lookup"><span data-stu-id="20034-104">Used to re-protect/reverse replicate a failed over replicated item or recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20034-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="20034-105">SYNTAX</span></span>

### <span data-ttu-id="20034-106">ByRPIObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="20034-106">ByRPIObject (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20034-107">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="20034-107">AzureToVMware</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection [-AzureToVMware] [-Account <ASRRunAsAccount>]
 -DataStore <ASRDataStore> [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 -RetentionVolume <ASRRetentionVolume> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="20034-108">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="20034-108">VMwareToAzure</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection [-VMwareToAzure] -Account <ASRRunAsAccount>
 [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20034-109">HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="20034-109">HyperVToAzure</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection [-HyperVToAzure] [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20034-110">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="20034-110">EnterpriseToEnterprise</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection [-VmmToVmm]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20034-111">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="20034-111">AzureToAzure</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection [-AzureToAzure]
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -LogStorageAccountId <String>
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-RecoveryResourceGroupId <String>] [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20034-112">AzureToAzureWithMultipleStorageAccount</span><span class="sxs-lookup"><span data-stu-id="20034-112">AzureToAzureWithMultipleStorageAccount</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection [-AzureToAzure]
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-RecoveryResourceGroupId <String>]
 [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20034-113">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="20034-113">ByRPObject</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20034-114">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="20034-114">ByPEObject</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20034-115">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="20034-115">DESCRIPTION</span></span>
<span data-ttu-id="20034-116">Командлет **Update-AzureRmRecoveryServicesAsrProtectionDirection** обновляет направление репликации для указанного объекта Azure Site Recovery после завершения операции фиксации отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="20034-116">The **Update-AzureRmRecoveryServicesAsrProtectionDirection** cmdlet updates the replication direction for the specified Azure Site Recovery object after the completion of a commit failover operation.</span></span>

## <span data-ttu-id="20034-117">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="20034-117">EXAMPLES</span></span>

### <span data-ttu-id="20034-118">Пример 1</span><span class="sxs-lookup"><span data-stu-id="20034-118">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrProtectionDirection -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="20034-119">Начните операцию направления обновления для указанного плана восстановления и возвращает объект задания ASR, который используется для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="20034-119">Start the update direction operation for the specified recovery plan and returns the ASR job object used to track the operation.</span></span>

### <span data-ttu-id="20034-120">Пример 2</span><span class="sxs-lookup"><span data-stu-id="20034-120">Example 2</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping -LogStorageAccountId $cacheStorageId `
 -ReplicationProtectedItem $rpi
```

<span data-ttu-id="20034-121">Начните операцию направления обновления для указанного элемента, защищенного репликацией, в целевом регионе Azure, определяемом сопоставлением контейнера защиты, и с помощью хранилища кэша (в том же регионе, что и VM).</span><span class="sxs-lookup"><span data-stu-id="20034-121">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and using cache storage (in same region as VM).</span></span>

### <span data-ttu-id="20034-122">Пример 3</span><span class="sxs-lookup"><span data-stu-id="20034-122">Example 3</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping `
 -AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -ReplicationProtectedItem  $rpi
```

<span data-ttu-id="20034-123">Начните операцию направления обновления для указанного элемента, защищенного репликацией, в целевом регионе Azure, определяемом сопоставлением контейнеров защиты и указанной конфигурацией репликации дисков.</span><span class="sxs-lookup"><span data-stu-id="20034-123">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and provided disk replication configuration.</span></span>

## <span data-ttu-id="20034-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="20034-124">PARAMETERS</span></span>

### <span data-ttu-id="20034-125">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="20034-125">-Account</span></span>
<span data-ttu-id="20034-126">Учетная запись запуска от имени, которая будет использоваться для принудительной установки службы Mobility Service при необходимости.</span><span class="sxs-lookup"><span data-stu-id="20034-126">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="20034-127">Должен быть один из списка учетных записей запуска от имени в структуре ASR.</span><span class="sxs-lookup"><span data-stu-id="20034-127">Must be one from the list of run as accounts in the ASR fabric.</span></span>

```yaml
Type: ASRRunAsAccount
Parameter Sets: AzureToVMware
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: ASRRunAsAccount
Parameter Sets: VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20034-128">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="20034-128">-AzureToAzure</span></span>
<span data-ttu-id="20034-129">Параметр Switch, указывающий, что направление репликации обновляется для реплицированных виртуальных машин Azure между двумя областями Azure.</span><span class="sxs-lookup"><span data-stu-id="20034-129">Switch parameter specifying that the replication direction being updated for replicated Azure virtual machines between two Azure regions.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20034-130">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="20034-130">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="20034-131">Указывает список реплицированных виртуальных машин и учетной записи хранилища кэша и хранилища для восстановления, которые будут использоваться для репликации диска.</span><span class="sxs-lookup"><span data-stu-id="20034-131">Specifies the list of virtual machine disks to replicated and the cache storage account and recovery storage account to be used to replicate the disk.</span></span>

```yaml
Type: ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20034-132">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="20034-132">-AzureToVMware</span></span>
<span data-ttu-id="20034-133">Обновите направление репликации с Azure на VMware.</span><span class="sxs-lookup"><span data-stu-id="20034-133">Update replication direction from Azure to Vmware.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AzureToVMware
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20034-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="20034-134">-Confirm</span></span>
<span data-ttu-id="20034-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="20034-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20034-136">-DataStore</span><span class="sxs-lookup"><span data-stu-id="20034-136">-DataStore</span></span>
<span data-ttu-id="20034-137">Хранилище DataStore VMware, используемое для vmdisk.</span><span class="sxs-lookup"><span data-stu-id="20034-137">The VMware datastore to be used for the vmdisk's.</span></span>

```yaml
Type: ASRDataStore
Parameter Sets: AzureToVMware
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20034-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20034-138">-DefaultProfile</span></span>
<span data-ttu-id="20034-139">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="20034-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20034-140">-Направление</span><span class="sxs-lookup"><span data-stu-id="20034-140">-Direction</span></span>
<span data-ttu-id="20034-141">Указывает направление, которое будет использоваться для операции обновления. Опубликуйте отработку отказа.</span><span class="sxs-lookup"><span data-stu-id="20034-141">Specifies the direction to be used for the update operation post a failover.</span></span>
<span data-ttu-id="20034-142">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="20034-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="20034-143">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="20034-143">PrimaryToRecovery</span></span>
- <span data-ttu-id="20034-144">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="20034-144">RecoveryToPrimary</span></span>

```yaml
Type: String
Parameter Sets: ByRPIObject, AzureToVMware, VMwareToAzure, HyperVToAzure, EnterpriseToEnterprise, ByRPObject, ByPEObject
Aliases:
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20034-145">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="20034-145">-HyperVToAzure</span></span>
<span data-ttu-id="20034-146">Повторно включите защиту виртуальной машины Hyper-V после восстановления после сбоя.</span><span class="sxs-lookup"><span data-stu-id="20034-146">Reprotect a Hyper-V virtual machine after failback.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: HyperVToAzure
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20034-147">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="20034-147">-LogStorageAccountId</span></span>
<span data-ttu-id="20034-148">Указывает идентификатор учетной записи хранения для хранения журнала репликации виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="20034-148">Specifies the storage account ID to store the replication log of VMs.</span></span>

```yaml
Type: String
Parameter Sets: VMwareToAzure, HyperVToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20034-149">-MasterTarget</span><span class="sxs-lookup"><span data-stu-id="20034-149">-MasterTarget</span></span>
<span data-ttu-id="20034-150">Сведения о главном целевом сервере.</span><span class="sxs-lookup"><span data-stu-id="20034-150">Master Target Server Details.</span></span>

```yaml
Type: ASRMasterTargetServer
Parameter Sets: AzureToVMware, VMwareToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20034-151">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="20034-151">-ProcessServer</span></span>
<span data-ttu-id="20034-152">Сервер обработки, который будет использоваться для репликации.</span><span class="sxs-lookup"><span data-stu-id="20034-152">Process Server to be used for replication.</span></span>

```yaml
Type: ASRProcessServer
Parameter Sets: AzureToVMware, VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20034-153">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="20034-153">-ProtectionContainerMapping</span></span>
<span data-ttu-id="20034-154">ContainerMapping защиты, которую необходимо использовать для репликации.</span><span class="sxs-lookup"><span data-stu-id="20034-154">Protection containerMapping to be used for replication.</span></span>

```yaml
Type: ASRProtectionContainerMapping
Parameter Sets: AzureToVMware, VMwareToAzure, AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20034-155">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="20034-155">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="20034-156">Группа доступности, на которой должна быть создана виртуальная машина при переходе на другой ресурс</span><span class="sxs-lookup"><span data-stu-id="20034-156">The availability set that the virtual machine should be created in upon failover</span></span>

```yaml
Type: String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20034-157">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="20034-157">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="20034-158">Указывает идентификатор учетной записи хранения Azure, на которую должна выполняться репликация.</span><span class="sxs-lookup"><span data-stu-id="20034-158">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: String
Parameter Sets: VMwareToAzure, HyperVToAzure, AzureToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20034-159">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="20034-159">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="20034-160">Идентификатор ресурса облачной службы восстановления, на которую следует отработка отказа виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="20034-160">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

```yaml
Type: String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20034-161">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="20034-161">-RecoveryPlan</span></span>
<span data-ttu-id="20034-162">Указывает объект плана восстановления ASR.</span><span class="sxs-lookup"><span data-stu-id="20034-162">Specifies an ASR recovery plan object.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20034-163">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="20034-163">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="20034-164">Идентификатор resourceGroup восстановления для защищенной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="20034-164">Recovery resourceGroup id for protected Vm.</span></span>

```yaml
Type: String
Parameter Sets: AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20034-165">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="20034-165">-ReplicationProtectedItem</span></span>
<span data-ttu-id="20034-166">Задает защищенный элемент репликации ASR.</span><span class="sxs-lookup"><span data-stu-id="20034-166">Specifies an ASR replication protected item.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, AzureToVMware, VMwareToAzure, HyperVToAzure, EnterpriseToEnterprise, AzureToAzure, AzureToAzureWithMultipleStorageAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20034-167">-RetentionVolume</span><span class="sxs-lookup"><span data-stu-id="20034-167">-RetentionVolume</span></span>
<span data-ttu-id="20034-168">Том хранения на главном целевом сервере, который нужно использовать.</span><span class="sxs-lookup"><span data-stu-id="20034-168">Retention Volume on the master target server to be used.</span></span>

```yaml
Type: ASRRetentionVolume
Parameter Sets: AzureToVMware
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20034-169">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="20034-169">-VMwareToAzure</span></span>
<span data-ttu-id="20034-170">Обновите направление репликации с VMware на Azure.</span><span class="sxs-lookup"><span data-stu-id="20034-170">Update replication direction from VMware to Azure.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: VMwareToAzure
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20034-171">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="20034-171">-VmmToVmm</span></span>
<span data-ttu-id="20034-172">Изменение направления репликации для сбоя на виртуальной машине Hyper-V, защищенной между двумя сайтами Hyper-V, управляемыми VMM.</span><span class="sxs-lookup"><span data-stu-id="20034-172">Update replication direction for a failed over Hyper-V virtual machine that is protected between two VMM managed Hyper-V sites.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20034-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20034-173">-WhatIf</span></span>
<span data-ttu-id="20034-174">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="20034-174">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="20034-175">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="20034-175">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20034-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20034-176">CommonParameters</span></span>
<span data-ttu-id="20034-177">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="20034-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20034-178">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20034-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20034-179">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="20034-179">INPUTS</span></span>

### <span data-ttu-id="20034-180">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="20034-180">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="20034-181">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="20034-181">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="20034-182">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="20034-182">OUTPUTS</span></span>

### <span data-ttu-id="20034-183">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="20034-183">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="20034-184">Пуск</span><span class="sxs-lookup"><span data-stu-id="20034-184">NOTES</span></span>

## <span data-ttu-id="20034-185">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="20034-185">RELATED LINKS</span></span>
