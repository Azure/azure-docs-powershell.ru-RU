---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/update-azrecoveryservicesasrprotectiondirection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionDirection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionDirection.md
ms.openlocfilehash: c6e25b9b8ec7fe22f76ccec954312914af8dd53e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990842"
---
# <span data-ttu-id="033bf-101">Update-AzRecoveryServicesAsrProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="033bf-101">Update-AzRecoveryServicesAsrProtectionDirection</span></span>

## <span data-ttu-id="033bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="033bf-102">SYNOPSIS</span></span>
<span data-ttu-id="033bf-103">Обновляет направление репликации для указанного элемента, защищенного репликацией, или для плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="033bf-103">Updates the replication direction for the specified replication protected item or recovery plan.</span></span> <span data-ttu-id="033bf-104">Используется для повторной защиты или репликации сбойного по плану репликации или восстановления.</span><span class="sxs-lookup"><span data-stu-id="033bf-104">Used to re-protect/reverse replicate a failed over replicated item or recovery plan.</span></span>

## <span data-ttu-id="033bf-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="033bf-105">SYNTAX</span></span>

### <span data-ttu-id="033bf-106">ByRPIObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="033bf-106">ByRPIObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="033bf-107">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="033bf-107">AzureToVMware</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToVMware] [-Account <ASRRunAsAccount>]
 -DataStore <ASRDataStore> [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 -RetentionVolume <ASRRetentionVolume> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="033bf-108">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="033bf-108">VMwareToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-VMwareToAzure] -Account <ASRRunAsAccount>
 [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="033bf-109">HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="033bf-109">HyperVToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-HyperVToAzure] [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="033bf-110">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="033bf-110">EnterpriseToEnterprise</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-VmmToVmm]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="033bf-111">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="033bf-111">AzureToAzure</span></span>
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

### <span data-ttu-id="033bf-112">AzureToAzureWithMultipleStorageAccount</span><span class="sxs-lookup"><span data-stu-id="033bf-112">AzureToAzureWithMultipleStorageAccount</span></span>
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

### <span data-ttu-id="033bf-113">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="033bf-113">ByRPObject</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="033bf-114">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="033bf-114">ByPEObject</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -Direction <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="033bf-115">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="033bf-115">DESCRIPTION</span></span>
<span data-ttu-id="033bf-116">Для **указанного** объекта восстановления сайта Azure после завершения отработки будет обновлено направление репликации для указанного объекта восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="033bf-116">The **Update-AzRecoveryServicesAsrProtectionDirection** cmdlet updates the replication direction for the specified Azure Site Recovery object after the completion of a commit failover operation.</span></span>

## <span data-ttu-id="033bf-117">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="033bf-117">EXAMPLES</span></span>

### <span data-ttu-id="033bf-118">Пример 1</span><span class="sxs-lookup"><span data-stu-id="033bf-118">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="033bf-119">Запуск операции направления обновления для указанного плана восстановления и возврат объекта задания ASR, используемого для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="033bf-119">Start the update direction operation for the specified recovery plan and returns the ASR job object used to track the operation.</span></span>

### <span data-ttu-id="033bf-120">Пример 2</span><span class="sxs-lookup"><span data-stu-id="033bf-120">Example 2</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping -LogStorageAccountId $cacheStorageId `
 -ReplicationProtectedItem $rpi
```

<span data-ttu-id="033bf-121">Начните операцию направления обновления для указанного элемента, защищенного репликацией, в целевом регионе Azure, определяемом сопоставлением контейнера защиты и использованием хранилища кэша (в том же регионе, что и VM).</span><span class="sxs-lookup"><span data-stu-id="033bf-121">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and using cache storage (in same region as VM).</span></span>

### <span data-ttu-id="033bf-122">Пример 3</span><span class="sxs-lookup"><span data-stu-id="033bf-122">Example 3</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping `
 -AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -ReplicationProtectedItem  $rpi
```

<span data-ttu-id="033bf-123">Начните операцию направления обновления для указанного элемента, защищенного репликацией, в целевом регионе Azure, определяемом сопоставлением контейнера защиты и предоставленной конфигурацией репликации диска.</span><span class="sxs-lookup"><span data-stu-id="033bf-123">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and provided disk replication configuration.</span></span>

### <span data-ttu-id="033bf-124">Пример 4</span><span class="sxs-lookup"><span data-stu-id="033bf-124">Example 4</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping `
 -AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -ReplicationProtectedItem  $rpi `
 -DiskEncryptionVaultId  $DiskEncryptionVaultId -DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
 -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

    
<span data-ttu-id="033bf-125">Начните операцию направления обновления для указанного элемента, защищенного зашифрованной репликацией, в целевом регионе Azure, определяемом сопоставлением контейнера защиты и предоставленной конфигурацией репликации диска.</span><span class="sxs-lookup"><span data-stu-id="033bf-125">Start the update direction operation for the specified encrypted replication protected item in target azure region defined by protection container mapping and provided disk replication configuration.</span></span>

### <span data-ttu-id="033bf-126">Пример 5</span><span class="sxs-lookup"><span data-stu-id="033bf-126">Example 5</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping -LogStorageAccountId $cacheStorageId `
 -ReplicationProtectedItem $rpi -RecoveryProximityPlacementGroupId $ppg
```

<span data-ttu-id="033bf-127">Начните операцию направления обновления для указанного элемента, защищенного репликацией, в целевом регионе Azure, определяемом сопоставлением контейнера защиты и использованием кэша (в том же регионе, что и VM) и группы расположения.</span><span class="sxs-lookup"><span data-stu-id="033bf-127">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and using cache storage (in same region as VM) and proximity placement group.</span></span>


## <span data-ttu-id="033bf-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="033bf-128">PARAMETERS</span></span>

### <span data-ttu-id="033bf-129">-Account</span><span class="sxs-lookup"><span data-stu-id="033bf-129">-Account</span></span>
<span data-ttu-id="033bf-130">Запустите как учетную запись, которая будет использоваться для push-установки службы мобильной установки при необходимости.</span><span class="sxs-lookup"><span data-stu-id="033bf-130">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="033bf-131">Должен быть одним из списков запуска в качестве учетных записей в материале ASR.</span><span class="sxs-lookup"><span data-stu-id="033bf-131">Must be one from the list of run as accounts in the ASR fabric.</span></span>

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

### <span data-ttu-id="033bf-132">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="033bf-132">-AzureToAzure</span></span>
<span data-ttu-id="033bf-133">Указывает аварийное восстановление из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="033bf-133">Specifies the Azure to Azure disaster recovery.</span></span>

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

### <span data-ttu-id="033bf-134">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="033bf-134">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="033bf-135">Определяет конфигурацию диска для аварийного восстановления.</span><span class="sxs-lookup"><span data-stu-id="033bf-135">Specifies the disk configuration for disaster recovery.</span></span>

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

### <span data-ttu-id="033bf-136">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="033bf-136">-AzureToVMware</span></span>
<span data-ttu-id="033bf-137">Указывает сценарий переключения Azure на vMWare.</span><span class="sxs-lookup"><span data-stu-id="033bf-137">Specifies the switch azure to vMWare scenario.</span></span>

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

### <span data-ttu-id="033bf-138">-DataStore</span><span class="sxs-lookup"><span data-stu-id="033bf-138">-DataStore</span></span>
<span data-ttu-id="033bf-139">Хранилище данных VMWARE, используемого для vmdisk.</span><span class="sxs-lookup"><span data-stu-id="033bf-139">The VMware data-store to be used for the vmdisk's.</span></span>

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

### <span data-ttu-id="033bf-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="033bf-140">-DefaultProfile</span></span>
<span data-ttu-id="033bf-141">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="033bf-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="033bf-142">-Direction</span><span class="sxs-lookup"><span data-stu-id="033bf-142">-Direction</span></span>
<span data-ttu-id="033bf-143">Определяет направление, используемого для обновления после отбойного обновления.</span><span class="sxs-lookup"><span data-stu-id="033bf-143">Specifies the direction to be used for the update operation post a failover.</span></span>
<span data-ttu-id="033bf-144">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="033bf-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="033bf-145">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="033bf-145">PrimaryToRecovery</span></span>
- <span data-ttu-id="033bf-146">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="033bf-146">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="033bf-147">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="033bf-147">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="033bf-148">Указывает секретный URL-адрес шифрования диска с версией (шифрованием диска Azure), который будет использоваться для восстановления VM после отбойного канала.</span><span class="sxs-lookup"><span data-stu-id="033bf-148">Specifies the disk encryption secret URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="033bf-149">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="033bf-149">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="033bf-150">Определяет код секретного сейфа шифрования диска (шифрование диска Azure), который будет использоваться для восстановления VM после отбойного сбойа.</span><span class="sxs-lookup"><span data-stu-id="033bf-150">Specifies the disk encryption secret vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="033bf-151">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="033bf-151">-HyperVToAzure</span></span>
<span data-ttu-id="033bf-152">После сбойной Hyper-V переускорение виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="033bf-152">Reprotect a Hyper-V virtual machine after failback.</span></span>

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

### <span data-ttu-id="033bf-153">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="033bf-153">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="033bf-154">Определяет URL-адрес ключа шифрования диска (шифрование диска Azure), который будет использоваться для восстановления VM-файлов после отбойного процесса.</span><span class="sxs-lookup"><span data-stu-id="033bf-154">Specifies the disk encryption key URL(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="033bf-155">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="033bf-155">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="033bf-156">Определяет, что ключ ключа шифрования диска ( шифрование диска Azure) будет использоваться для восстановления VM после отбоя.</span><span class="sxs-lookup"><span data-stu-id="033bf-156">Specifies the disk encryption key keyVault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="033bf-157">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="033bf-157">-LogStorageAccountId</span></span>
<span data-ttu-id="033bf-158">Определяет ИД учетной записи хранения, который будет хранить журнал репликации ВМ-сообщений.</span><span class="sxs-lookup"><span data-stu-id="033bf-158">Specifies the storage account ID to store the replication log of VMs.</span></span>

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

### <span data-ttu-id="033bf-159">-MasterTarget</span><span class="sxs-lookup"><span data-stu-id="033bf-159">-MasterTarget</span></span>
<span data-ttu-id="033bf-160">Master Target Server Details (Сведения о целевом сервере).</span><span class="sxs-lookup"><span data-stu-id="033bf-160">Master Target Server Details.</span></span>

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

### <span data-ttu-id="033bf-161">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="033bf-161">-ProcessServer</span></span>
<span data-ttu-id="033bf-162">Сервер обработки, используемый для репликации.</span><span class="sxs-lookup"><span data-stu-id="033bf-162">Process Server to be used for replication.</span></span>

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

### <span data-ttu-id="033bf-163">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="033bf-163">-ProtectionContainerMapping</span></span>
<span data-ttu-id="033bf-164">Защита containerMapping, используемая для репликации.</span><span class="sxs-lookup"><span data-stu-id="033bf-164">Protection containerMapping to be used for replication.</span></span>

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

### <span data-ttu-id="033bf-165">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="033bf-165">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="033bf-166">Набор доступности, в который следует создать виртуальную машину после отбойного доступа</span><span class="sxs-lookup"><span data-stu-id="033bf-166">The availability set that the virtual machine should be created in upon failover</span></span>

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

### <span data-ttu-id="033bf-167">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="033bf-167">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="033bf-168">Определяет ИД учетной записи хранения Azure, на который нужно реплицировать.</span><span class="sxs-lookup"><span data-stu-id="033bf-168">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="033bf-169">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="033bf-169">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="033bf-170">Указывает учетную запись хранения для диагностики загрузки для восстановления Azure VM.</span><span class="sxs-lookup"><span data-stu-id="033bf-170">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

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

### <span data-ttu-id="033bf-171">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="033bf-171">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="033bf-172">ИД ресурса облачной службы восстановления для отохода от сбойной работы этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="033bf-172">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="033bf-173">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="033bf-173">-RecoveryPlan</span></span>
<span data-ttu-id="033bf-174">Указывает объект плана восстановления ASR.</span><span class="sxs-lookup"><span data-stu-id="033bf-174">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="033bf-175">-RecoveryProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="033bf-175">-RecoveryProximityPlacementGroupId</span></span>
<span data-ttu-id="033bf-176">ИД ресурса группы расположения расположения близости восстановления для отостановки отостановки этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="033bf-176">The resource ID of the recovery proximity placement group to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="033bf-177">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="033bf-177">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="033bf-178">ID recovery resourceGroup для защищенного VM-</span><span class="sxs-lookup"><span data-stu-id="033bf-178">Recovery resourceGroup id for protected Vm.</span></span>

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

### <span data-ttu-id="033bf-179">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="033bf-179">-ReplicationProtectedItem</span></span>
<span data-ttu-id="033bf-180">Определяет защищенный репликацией asR элемент.</span><span class="sxs-lookup"><span data-stu-id="033bf-180">Specifies an ASR replication protected item.</span></span>

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

### <span data-ttu-id="033bf-181">-RetentionVolume</span><span class="sxs-lookup"><span data-stu-id="033bf-181">-RetentionVolume</span></span>
<span data-ttu-id="033bf-182">Громкость хранения на целевом сервере,который используется.</span><span class="sxs-lookup"><span data-stu-id="033bf-182">Retention Volume on the master target server to be used.</span></span>

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

### <span data-ttu-id="033bf-183">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="033bf-183">-VmmToVmm</span></span>
<span data-ttu-id="033bf-184">Обновите направление репликации для сбойного Hyper-V виртуальной машине, которая защищена между двумя управляемыми VMM Hyper-V сайтов.</span><span class="sxs-lookup"><span data-stu-id="033bf-184">Update replication direction for a failed over Hyper-V virtual machine that is protected between two VMM managed Hyper-V sites.</span></span>

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

### <span data-ttu-id="033bf-185">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="033bf-185">-VMwareToAzure</span></span>
<span data-ttu-id="033bf-186">Обновление направления репликации из VMware в Azure.</span><span class="sxs-lookup"><span data-stu-id="033bf-186">Update replication direction from VMware to Azure.</span></span>

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

### <span data-ttu-id="033bf-187">-Confirm</span><span class="sxs-lookup"><span data-stu-id="033bf-187">-Confirm</span></span>
<span data-ttu-id="033bf-188">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="033bf-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="033bf-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="033bf-189">-WhatIf</span></span>
<span data-ttu-id="033bf-190">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="033bf-190">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="033bf-191">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="033bf-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="033bf-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="033bf-192">CommonParameters</span></span>
<span data-ttu-id="033bf-193">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="033bf-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="033bf-194">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="033bf-194">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="033bf-195">INPUTS</span><span class="sxs-lookup"><span data-stu-id="033bf-195">INPUTS</span></span>

### <span data-ttu-id="033bf-196">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="033bf-196">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="033bf-197">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="033bf-197">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="033bf-198">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="033bf-198">OUTPUTS</span></span>

### <span data-ttu-id="033bf-199">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="033bf-199">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="033bf-200">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="033bf-200">NOTES</span></span>

## <span data-ttu-id="033bf-201">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="033bf-201">RELATED LINKS</span></span>
