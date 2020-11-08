---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrprotectiondirection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionDirection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionDirection.md
ms.openlocfilehash: 326f73e0a056c6d68d0bdd96ddca1aea7c1c6147
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244243"
---
# <span data-ttu-id="8cce8-101">Update-AzRecoveryServicesAsrProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="8cce8-101">Update-AzRecoveryServicesAsrProtectionDirection</span></span>

## <span data-ttu-id="8cce8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8cce8-102">SYNOPSIS</span></span>
<span data-ttu-id="8cce8-103">Обновляет направление репликации для указанного защищенного элемента или плана восстановления для репликации.</span><span class="sxs-lookup"><span data-stu-id="8cce8-103">Updates the replication direction for the specified replication protected item or recovery plan.</span></span> <span data-ttu-id="8cce8-104">Используется для повторной защиты или обратной репликации, которая переносит отказ на реплицируемый элемент или план восстановления.</span><span class="sxs-lookup"><span data-stu-id="8cce8-104">Used to re-protect/reverse replicate a failed over replicated item or recovery plan.</span></span>

## <span data-ttu-id="8cce8-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8cce8-105">SYNTAX</span></span>

### <span data-ttu-id="8cce8-106">ByRPIObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8cce8-106">ByRPIObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cce8-107">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="8cce8-107">AzureToVMware</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToVMware] [-Account <ASRRunAsAccount>]
 -DataStore <ASRDataStore> [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 -RetentionVolume <ASRRetentionVolume> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8cce8-108">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="8cce8-108">VMwareToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-VMwareToAzure] -Account <ASRRunAsAccount>
 [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cce8-109">HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="8cce8-109">HyperVToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-HyperVToAzure] [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cce8-110">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="8cce8-110">EnterpriseToEnterprise</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-VmmToVmm]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cce8-111">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="8cce8-111">AzureToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToAzure]
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -LogStorageAccountId <String>
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-RecoveryResourceGroupId <String>] [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryProximityPlacementGroupId <String>] [-RecoveryBootDiagStorageAccountId <String>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8cce8-112">AzureToAzureWithMultipleStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8cce8-112">AzureToAzureWithMultipleStorageAccount</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToAzure]
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-RecoveryResourceGroupId <String>]
 [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryProximityPlacementGroupId <String>] [-RecoveryBootDiagStorageAccountId <String>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8cce8-113">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="8cce8-113">ByRPObject</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cce8-114">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="8cce8-114">ByPEObject</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -Direction <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8cce8-115">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8cce8-115">DESCRIPTION</span></span>
<span data-ttu-id="8cce8-116">Командлет **Update-AzRecoveryServicesAsrProtectionDirection** обновляет направление репликации для указанного объекта Azure Site Recovery после завершения операции фиксации отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="8cce8-116">The **Update-AzRecoveryServicesAsrProtectionDirection** cmdlet updates the replication direction for the specified Azure Site Recovery object after the completion of a commit failover operation.</span></span>

## <span data-ttu-id="8cce8-117">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8cce8-117">EXAMPLES</span></span>

### <span data-ttu-id="8cce8-118">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8cce8-118">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="8cce8-119">Начните операцию направления обновления для указанного плана восстановления и возвращает объект задания ASR, который используется для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="8cce8-119">Start the update direction operation for the specified recovery plan and returns the ASR job object used to track the operation.</span></span>

### <span data-ttu-id="8cce8-120">Пример 2</span><span class="sxs-lookup"><span data-stu-id="8cce8-120">Example 2</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping -LogStorageAccountId $cacheStorageId `
 -ReplicationProtectedItem $rpi
```

<span data-ttu-id="8cce8-121">Начните операцию направления обновления для указанного элемента, защищенного репликацией, в целевом регионе Azure, определяемом сопоставлением контейнера защиты, и с помощью хранилища кэша (в том же регионе, что и VM).</span><span class="sxs-lookup"><span data-stu-id="8cce8-121">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and using cache storage (in same region as VM).</span></span>

### <span data-ttu-id="8cce8-122">Пример 3</span><span class="sxs-lookup"><span data-stu-id="8cce8-122">Example 3</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping `
 -AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -ReplicationProtectedItem  $rpi
```

<span data-ttu-id="8cce8-123">Начните операцию направления обновления для указанного элемента, защищенного репликацией, в целевом регионе Azure, определяемом сопоставлением контейнеров защиты и указанной конфигурацией репликации дисков.</span><span class="sxs-lookup"><span data-stu-id="8cce8-123">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and provided disk replication configuration.</span></span>

### <span data-ttu-id="8cce8-124">Пример 4</span><span class="sxs-lookup"><span data-stu-id="8cce8-124">Example 4</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping `
 -AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -ReplicationProtectedItem  $rpi `
 -DiskEncryptionVaultId  $DiskEncryptionVaultId -DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
 -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

    
<span data-ttu-id="8cce8-125">Начните операцию направления обновления для указанного защищенного элемента с шифрованием в целевом регионе Azure, определяемом сопоставлением контейнеров защиты и указанной конфигурацией репликации дисков.</span><span class="sxs-lookup"><span data-stu-id="8cce8-125">Start the update direction operation for the specified encrypted replication protected item in target azure region defined by protection container mapping and provided disk replication configuration.</span></span>

### <span data-ttu-id="8cce8-126">Пример 5</span><span class="sxs-lookup"><span data-stu-id="8cce8-126">Example 5</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping -LogStorageAccountId $cacheStorageId `
 -ReplicationProtectedItem $rpi -RecoveryProximityPlacementGroupId $ppg
```

<span data-ttu-id="8cce8-127">Начните операцию направления обновления для указанного элемента, защищенного репликацией, в целевом регионе Azure, определяемом сопоставлением контейнеров защиты, и с помощью хранилища кэша (в том же регионе, что и VM) и группы размещения близкого взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="8cce8-127">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and using cache storage (in same region as VM) and proximity placement group.</span></span>


## <span data-ttu-id="8cce8-128">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8cce8-128">PARAMETERS</span></span>

### <span data-ttu-id="8cce8-129">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="8cce8-129">-Account</span></span>
<span data-ttu-id="8cce8-130">Учетная запись запуска от имени, которая будет использоваться для принудительной установки службы Mobility Service при необходимости.</span><span class="sxs-lookup"><span data-stu-id="8cce8-130">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="8cce8-131">Должен быть один из списка учетных записей запуска от имени в структуре ASR.</span><span class="sxs-lookup"><span data-stu-id="8cce8-131">Must be one from the list of run as accounts in the ASR fabric.</span></span>

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

### <span data-ttu-id="8cce8-132">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="8cce8-132">-AzureToAzure</span></span>
<span data-ttu-id="8cce8-133">Указывает на аварийное восстановление Azure для Azure.</span><span class="sxs-lookup"><span data-stu-id="8cce8-133">Specifies the Azure to Azure disaster recovery.</span></span>

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

### <span data-ttu-id="8cce8-134">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="8cce8-134">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="8cce8-135">Указывает конфигурацию диска для аварийного восстановления.</span><span class="sxs-lookup"><span data-stu-id="8cce8-135">Specifies the disk configuration for disaster recovery.</span></span>

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

### <span data-ttu-id="8cce8-136">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="8cce8-136">-AzureToVMware</span></span>
<span data-ttu-id="8cce8-137">Указывает сценарий переключения с Azure на vMWare.</span><span class="sxs-lookup"><span data-stu-id="8cce8-137">Specifies the switch azure to vMWare scenario.</span></span>

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

### <span data-ttu-id="8cce8-138">-DataStore</span><span class="sxs-lookup"><span data-stu-id="8cce8-138">-DataStore</span></span>
<span data-ttu-id="8cce8-139">Хранилище данных VMware, используемое для vmdisk.</span><span class="sxs-lookup"><span data-stu-id="8cce8-139">The VMware data-store to be used for the vmdisk's.</span></span>

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

### <span data-ttu-id="8cce8-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cce8-140">-DefaultProfile</span></span>
<span data-ttu-id="8cce8-141">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8cce8-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="8cce8-142">-Направление</span><span class="sxs-lookup"><span data-stu-id="8cce8-142">-Direction</span></span>
<span data-ttu-id="8cce8-143">Указывает направление, которое будет использоваться для операции обновления. Опубликуйте отработку отказа.</span><span class="sxs-lookup"><span data-stu-id="8cce8-143">Specifies the direction to be used for the update operation post a failover.</span></span>
<span data-ttu-id="8cce8-144">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="8cce8-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8cce8-145">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="8cce8-145">PrimaryToRecovery</span></span>
- <span data-ttu-id="8cce8-146">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="8cce8-146">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="8cce8-147">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="8cce8-147">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="8cce8-148">Указывает секретный URL-адрес шифрования диска, который будет использоваться в качестве виртуальной машины для восстановления после отработки отказа (шифрование диска Azure).</span><span class="sxs-lookup"><span data-stu-id="8cce8-148">Specifies the disk encryption secret URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="8cce8-149">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="8cce8-149">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="8cce8-150">Задает секретный код (шифрование диска Azure), который будет использоваться для восстановления виртуальной машины после отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="8cce8-150">Specifies the disk encryption secret vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="8cce8-151">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="8cce8-151">-HyperVToAzure</span></span>
<span data-ttu-id="8cce8-152">Повторно включите защиту виртуальной машины Hyper-V после восстановления после сбоя.</span><span class="sxs-lookup"><span data-stu-id="8cce8-152">Reprotect a Hyper-V virtual machine after failback.</span></span>

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

### <span data-ttu-id="8cce8-153">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="8cce8-153">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="8cce8-154">Указывает, что URL-адрес ключа шифрования диска (шифрование диска Azure) будет использоваться для восстановления виртуальной машины после перехода на другой ресурс.</span><span class="sxs-lookup"><span data-stu-id="8cce8-154">Specifies the disk encryption key URL(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="8cce8-155">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="8cce8-155">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="8cce8-156">Указывает, что при переходе на другой ресурс keyVault ключ шифрования диска (шифрование диска Azure) будет использоваться для восстановления виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="8cce8-156">Specifies the disk encryption key keyVault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="8cce8-157">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="8cce8-157">-LogStorageAccountId</span></span>
<span data-ttu-id="8cce8-158">Указывает идентификатор учетной записи хранения для хранения журнала репликации виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="8cce8-158">Specifies the storage account ID to store the replication log of VMs.</span></span>

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

### <span data-ttu-id="8cce8-159">-MasterTarget</span><span class="sxs-lookup"><span data-stu-id="8cce8-159">-MasterTarget</span></span>
<span data-ttu-id="8cce8-160">Сведения о главном целевом сервере.</span><span class="sxs-lookup"><span data-stu-id="8cce8-160">Master Target Server Details.</span></span>

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

### <span data-ttu-id="8cce8-161">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="8cce8-161">-ProcessServer</span></span>
<span data-ttu-id="8cce8-162">Сервер обработки, который будет использоваться для репликации.</span><span class="sxs-lookup"><span data-stu-id="8cce8-162">Process Server to be used for replication.</span></span>

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

### <span data-ttu-id="8cce8-163">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="8cce8-163">-ProtectionContainerMapping</span></span>
<span data-ttu-id="8cce8-164">ContainerMapping защиты, которую необходимо использовать для репликации.</span><span class="sxs-lookup"><span data-stu-id="8cce8-164">Protection containerMapping to be used for replication.</span></span>

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

### <span data-ttu-id="8cce8-165">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="8cce8-165">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="8cce8-166">Группа доступности, на которой должна быть создана виртуальная машина при переходе на другой ресурс</span><span class="sxs-lookup"><span data-stu-id="8cce8-166">The availability set that the virtual machine should be created in upon failover</span></span>

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

### <span data-ttu-id="8cce8-167">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="8cce8-167">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="8cce8-168">Указывает идентификатор учетной записи хранения Azure, на которую должна выполняться репликация.</span><span class="sxs-lookup"><span data-stu-id="8cce8-168">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="8cce8-169">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="8cce8-169">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="8cce8-170">Указывает учетную запись хранения для диагностики загрузки для восстановления ВМ Azure.</span><span class="sxs-lookup"><span data-stu-id="8cce8-170">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

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

### <span data-ttu-id="8cce8-171">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="8cce8-171">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="8cce8-172">Идентификатор ресурса облачной службы восстановления, на которую следует отработка отказа виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="8cce8-172">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="8cce8-173">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="8cce8-173">-RecoveryPlan</span></span>
<span data-ttu-id="8cce8-174">Указывает объект плана восстановления ASR.</span><span class="sxs-lookup"><span data-stu-id="8cce8-174">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="8cce8-175">-RecoveryProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="8cce8-175">-RecoveryProximityPlacementGroupId</span></span>
<span data-ttu-id="8cce8-176">Идентификатор ресурса группы размещения близкого взаимодействия для восстановления, на которую следует отработка отказа виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="8cce8-176">The resource ID of the recovery proximity placement group to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="8cce8-177">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="8cce8-177">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="8cce8-178">Идентификатор resourceGroup восстановления для защищенной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="8cce8-178">Recovery resourceGroup id for protected Vm.</span></span>

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

### <span data-ttu-id="8cce8-179">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8cce8-179">-ReplicationProtectedItem</span></span>
<span data-ttu-id="8cce8-180">Задает защищенный элемент репликации ASR.</span><span class="sxs-lookup"><span data-stu-id="8cce8-180">Specifies an ASR replication protected item.</span></span>

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

### <span data-ttu-id="8cce8-181">-RetentionVolume</span><span class="sxs-lookup"><span data-stu-id="8cce8-181">-RetentionVolume</span></span>
<span data-ttu-id="8cce8-182">Том хранения на главном целевом сервере, который нужно использовать.</span><span class="sxs-lookup"><span data-stu-id="8cce8-182">Retention Volume on the master target server to be used.</span></span>

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

### <span data-ttu-id="8cce8-183">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="8cce8-183">-VmmToVmm</span></span>
<span data-ttu-id="8cce8-184">Изменение направления репликации для сбоя на виртуальной машине Hyper-V, защищенной между двумя сайтами Hyper-V, управляемыми VMM.</span><span class="sxs-lookup"><span data-stu-id="8cce8-184">Update replication direction for a failed over Hyper-V virtual machine that is protected between two VMM managed Hyper-V sites.</span></span>

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

### <span data-ttu-id="8cce8-185">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="8cce8-185">-VMwareToAzure</span></span>
<span data-ttu-id="8cce8-186">Обновите направление репликации с VMware на Azure.</span><span class="sxs-lookup"><span data-stu-id="8cce8-186">Update replication direction from VMware to Azure.</span></span>

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

### <span data-ttu-id="8cce8-187">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8cce8-187">-Confirm</span></span>
<span data-ttu-id="8cce8-188">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8cce8-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8cce8-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cce8-189">-WhatIf</span></span>
<span data-ttu-id="8cce8-190">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8cce8-190">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8cce8-191">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8cce8-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8cce8-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cce8-192">CommonParameters</span></span>
<span data-ttu-id="8cce8-193">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8cce8-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cce8-194">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8cce8-194">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cce8-195">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8cce8-195">INPUTS</span></span>

### <span data-ttu-id="8cce8-196">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="8cce8-196">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="8cce8-197">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8cce8-197">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="8cce8-198">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8cce8-198">OUTPUTS</span></span>

### <span data-ttu-id="8cce8-199">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="8cce8-199">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="8cce8-200">Пуск</span><span class="sxs-lookup"><span data-stu-id="8cce8-200">NOTES</span></span>

## <span data-ttu-id="8cce8-201">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8cce8-201">RELATED LINKS</span></span>
