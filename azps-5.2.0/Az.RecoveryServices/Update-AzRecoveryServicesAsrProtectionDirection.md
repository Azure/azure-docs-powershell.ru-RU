---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrprotectiondirection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionDirection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionDirection.md
ms.openlocfilehash: 326f73e0a056c6d68d0bdd96ddca1aea7c1c6147
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98400295"
---
# <span data-ttu-id="4b0bb-101">Update-AzRecoveryServicesAsrProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="4b0bb-101">Update-AzRecoveryServicesAsrProtectionDirection</span></span>

## <span data-ttu-id="4b0bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b0bb-102">SYNOPSIS</span></span>
<span data-ttu-id="4b0bb-103">Обновляет направление репликации для указанного элемента, защищенного репликацией, или для плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="4b0bb-103">Updates the replication direction for the specified replication protected item or recovery plan.</span></span> <span data-ttu-id="4b0bb-104">Используется для повторной защиты или репликации сбойного по плану репликации или восстановления.</span><span class="sxs-lookup"><span data-stu-id="4b0bb-104">Used to re-protect/reverse replicate a failed over replicated item or recovery plan.</span></span>

## <span data-ttu-id="4b0bb-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4b0bb-105">SYNTAX</span></span>

### <span data-ttu-id="4b0bb-106">ByRPIObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4b0bb-106">ByRPIObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b0bb-107">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="4b0bb-107">AzureToVMware</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToVMware] [-Account <ASRRunAsAccount>]
 -DataStore <ASRDataStore> [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 -RetentionVolume <ASRRetentionVolume> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4b0bb-108">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="4b0bb-108">VMwareToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-VMwareToAzure] -Account <ASRRunAsAccount>
 [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b0bb-109">HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="4b0bb-109">HyperVToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-HyperVToAzure] [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b0bb-110">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="4b0bb-110">EnterpriseToEnterprise</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-VmmToVmm]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b0bb-111">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="4b0bb-111">AzureToAzure</span></span>
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

### <span data-ttu-id="4b0bb-112">AzureToAzureWithMultipleStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4b0bb-112">AzureToAzureWithMultipleStorageAccount</span></span>
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

### <span data-ttu-id="4b0bb-113">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="4b0bb-113">ByRPObject</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b0bb-114">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="4b0bb-114">ByPEObject</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -Direction <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b0bb-115">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4b0bb-115">DESCRIPTION</span></span>
<span data-ttu-id="4b0bb-116">Для **указанного** объекта восстановления сайта Azure после завершения отработки обновления обновляется направление репликации для указанного объекта восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="4b0bb-116">The **Update-AzRecoveryServicesAsrProtectionDirection** cmdlet updates the replication direction for the specified Azure Site Recovery object after the completion of a commit failover operation.</span></span>

## <span data-ttu-id="4b0bb-117">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4b0bb-117">EXAMPLES</span></span>

### <span data-ttu-id="4b0bb-118">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4b0bb-118">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="4b0bb-119">Запуск операции направления обновления для указанного плана восстановления и возврат объекта задания ASR, используемого для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="4b0bb-119">Start the update direction operation for the specified recovery plan and returns the ASR job object used to track the operation.</span></span>

### <span data-ttu-id="4b0bb-120">Пример 2</span><span class="sxs-lookup"><span data-stu-id="4b0bb-120">Example 2</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping -LogStorageAccountId $cacheStorageId `
 -ReplicationProtectedItem $rpi
```

<span data-ttu-id="4b0bb-121">Начните операцию направления обновления для указанного элемента, защищенного репликацией, в целевом регионе Azure, определяемом сопоставлением контейнера защиты и использованием хранилища кэша (в том же регионе, что и VM).</span><span class="sxs-lookup"><span data-stu-id="4b0bb-121">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and using cache storage (in same region as VM).</span></span>

### <span data-ttu-id="4b0bb-122">Пример 3</span><span class="sxs-lookup"><span data-stu-id="4b0bb-122">Example 3</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping `
 -AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -ReplicationProtectedItem  $rpi
```

<span data-ttu-id="4b0bb-123">Начните операцию направления обновления для указанного элемента, защищенного репликацией, в целевом регионе Azure, определяемом сопоставлением контейнера защиты и предоставленной конфигурацией репликации диска.</span><span class="sxs-lookup"><span data-stu-id="4b0bb-123">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and provided disk replication configuration.</span></span>

### <span data-ttu-id="4b0bb-124">Пример 4</span><span class="sxs-lookup"><span data-stu-id="4b0bb-124">Example 4</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping `
 -AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -ReplicationProtectedItem  $rpi `
 -DiskEncryptionVaultId  $DiskEncryptionVaultId -DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
 -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

    
<span data-ttu-id="4b0bb-125">Начните операцию направления обновления для указанного элемента, защищенного зашифрованной репликацией, в целевом регионе Azure, определяемом сопоставлением контейнера защиты и предоставленной конфигурацией репликации диска.</span><span class="sxs-lookup"><span data-stu-id="4b0bb-125">Start the update direction operation for the specified encrypted replication protected item in target azure region defined by protection container mapping and provided disk replication configuration.</span></span>

### <span data-ttu-id="4b0bb-126">Пример 5</span><span class="sxs-lookup"><span data-stu-id="4b0bb-126">Example 5</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping -LogStorageAccountId $cacheStorageId `
 -ReplicationProtectedItem $rpi -RecoveryProximityPlacementGroupId $ppg
```

<span data-ttu-id="4b0bb-127">Начните операцию направления обновления для указанного элемента, защищенного репликацией, в целевом регионе Azure, определяемом сопоставлением контейнера защиты и использованием кэша (в том же регионе, что и VM) и группы расположения.</span><span class="sxs-lookup"><span data-stu-id="4b0bb-127">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and using cache storage (in same region as VM) and proximity placement group.</span></span>


## <span data-ttu-id="4b0bb-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4b0bb-128">PARAMETERS</span></span>

### <span data-ttu-id="4b0bb-129">-Account</span><span class="sxs-lookup"><span data-stu-id="4b0bb-129">-Account</span></span>
<span data-ttu-id="4b0bb-130">Запустите как учетную запись, которая будет использоваться для установки мобильной службы при необходимости.</span><span class="sxs-lookup"><span data-stu-id="4b0bb-130">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="4b0bb-131">Должен быть одним из списков запуска в качестве учетных записей в материале ASR.</span><span class="sxs-lookup"><span data-stu-id="4b0bb-131">Must be one from the list of run as accounts in the ASR fabric.</span></span>

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

### <span data-ttu-id="4b0bb-132">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="4b0bb-132">-AzureToAzure</span></span>
<span data-ttu-id="4b0bb-133">Указывает аварийное восстановление из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="4b0bb-133">Specifies the Azure to Azure disaster recovery.</span></span>

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

### <span data-ttu-id="4b0bb-134">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="4b0bb-134">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="4b0bb-135">Определяет конфигурацию диска для аварийного восстановления.</span><span class="sxs-lookup"><span data-stu-id="4b0bb-135">Specifies the disk configuration for disaster recovery.</span></span>

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

### <span data-ttu-id="4b0bb-136">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="4b0bb-136">-AzureToVMware</span></span>
<span data-ttu-id="4b0bb-137">Указывает сценарий переключения Azure на vMWare.</span><span class="sxs-lookup"><span data-stu-id="4b0bb-137">Specifies the switch azure to vMWare scenario.</span></span>

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

### <span data-ttu-id="4b0bb-138">-DataStore</span><span class="sxs-lookup"><span data-stu-id="4b0bb-138">-DataStore</span></span>
<span data-ttu-id="4b0bb-139">Хранилище данных VMWARE, используемого для vmdisk.</span><span class="sxs-lookup"><span data-stu-id="4b0bb-139">The VMware data-store to be used for the vmdisk's.</span></span>

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

### <span data-ttu-id="4b0bb-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b0bb-140">-DefaultProfile</span></span>
<span data-ttu-id="4b0bb-141">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4b0bb-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="4b0bb-142">-Direction</span><span class="sxs-lookup"><span data-stu-id="4b0bb-142">-Direction</span></span>
<span data-ttu-id="4b0bb-143">Определяет направление, используемого для обновления после отбойного действия.</span><span class="sxs-lookup"><span data-stu-id="4b0bb-143">Specifies the direction to be used for the update operation post a failover.</span></span>
<span data-ttu-id="4b0bb-144">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="4b0bb-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4b0bb-145">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="4b0bb-145">PrimaryToRecovery</span></span>
- <span data-ttu-id="4b0bb-146">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="4b0bb-146">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="4b0bb-147">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="4b0bb-147">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="4b0bb-148">Указывает секретный URL-адрес шифрования диска с версией (шифрованием диска Azure), который будет использоваться для восстановления VM после отбойного канала.</span><span class="sxs-lookup"><span data-stu-id="4b0bb-148">Specifies the disk encryption secret URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="4b0bb-149">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="4b0bb-149">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="4b0bb-150">Определяет код секретного сейфа шифрования диска (шифрование диска Azure), который будет использоваться для восстановления VM после отбойного сбойа.</span><span class="sxs-lookup"><span data-stu-id="4b0bb-150">Specifies the disk encryption secret vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="4b0bb-151">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="4b0bb-151">-HyperVToAzure</span></span>
<span data-ttu-id="4b0bb-152">Переускорение виртуальной машины Hyper-V после срывов.</span><span class="sxs-lookup"><span data-stu-id="4b0bb-152">Reprotect a Hyper-V virtual machine after failback.</span></span>

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

### <span data-ttu-id="4b0bb-153">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="4b0bb-153">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="4b0bb-154">Указывает URL-адрес ключа шифрования диска (шифрование диска Azure), который будет использоваться для восстановления VM-компьютера после отбойного процесса.</span><span class="sxs-lookup"><span data-stu-id="4b0bb-154">Specifies the disk encryption key URL(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="4b0bb-155">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="4b0bb-155">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="4b0bb-156">Определяет код keyVault ключа шифрования диска(шифрование диска Azure), который будет использоваться для восстановления VM после отбоя.</span><span class="sxs-lookup"><span data-stu-id="4b0bb-156">Specifies the disk encryption key keyVault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="4b0bb-157">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="4b0bb-157">-LogStorageAccountId</span></span>
<span data-ttu-id="4b0bb-158">Определяет ИД учетной записи хранения, который будет хранить журнал репликации ВМ-сообщений.</span><span class="sxs-lookup"><span data-stu-id="4b0bb-158">Specifies the storage account ID to store the replication log of VMs.</span></span>

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

### <span data-ttu-id="4b0bb-159">-MasterTarget</span><span class="sxs-lookup"><span data-stu-id="4b0bb-159">-MasterTarget</span></span>
<span data-ttu-id="4b0bb-160">Master Target Server Details (Сведения о целевом сервере).</span><span class="sxs-lookup"><span data-stu-id="4b0bb-160">Master Target Server Details.</span></span>

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

### <span data-ttu-id="4b0bb-161">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="4b0bb-161">-ProcessServer</span></span>
<span data-ttu-id="4b0bb-162">Сервер обработки, используемый для репликации.</span><span class="sxs-lookup"><span data-stu-id="4b0bb-162">Process Server to be used for replication.</span></span>

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

### <span data-ttu-id="4b0bb-163">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="4b0bb-163">-ProtectionContainerMapping</span></span>
<span data-ttu-id="4b0bb-164">Защита containerMapping, используемая для репликации.</span><span class="sxs-lookup"><span data-stu-id="4b0bb-164">Protection containerMapping to be used for replication.</span></span>

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

### <span data-ttu-id="4b0bb-165">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="4b0bb-165">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="4b0bb-166">Набор доступности, в который следует создать виртуальную машину после отбойного доступа</span><span class="sxs-lookup"><span data-stu-id="4b0bb-166">The availability set that the virtual machine should be created in upon failover</span></span>

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

### <span data-ttu-id="4b0bb-167">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="4b0bb-167">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="4b0bb-168">Определяет ИД учетной записи хранения Azure, на который нужно реплицировать.</span><span class="sxs-lookup"><span data-stu-id="4b0bb-168">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="4b0bb-169">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="4b0bb-169">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="4b0bb-170">Указывает учетную запись хранения для диагностики загрузки для восстановления Azure VM.</span><span class="sxs-lookup"><span data-stu-id="4b0bb-170">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

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

### <span data-ttu-id="4b0bb-171">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="4b0bb-171">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="4b0bb-172">ИД ресурса облачной службы восстановления для отохода от сбойной работы этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4b0bb-172">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="4b0bb-173">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4b0bb-173">-RecoveryPlan</span></span>
<span data-ttu-id="4b0bb-174">Указывает объект плана восстановления ASR.</span><span class="sxs-lookup"><span data-stu-id="4b0bb-174">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="4b0bb-175">-RecoveryProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="4b0bb-175">-RecoveryProximityPlacementGroupId</span></span>
<span data-ttu-id="4b0bb-176">ИД ресурса группы расположения расположения близости восстановления для отостановки этой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4b0bb-176">The resource ID of the recovery proximity placement group to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="4b0bb-177">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="4b0bb-177">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="4b0bb-178">ID recovery resourceGroup для защищенного VM-</span><span class="sxs-lookup"><span data-stu-id="4b0bb-178">Recovery resourceGroup id for protected Vm.</span></span>

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

### <span data-ttu-id="4b0bb-179">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="4b0bb-179">-ReplicationProtectedItem</span></span>
<span data-ttu-id="4b0bb-180">Определяет защищенный репликацией asR элемент.</span><span class="sxs-lookup"><span data-stu-id="4b0bb-180">Specifies an ASR replication protected item.</span></span>

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

### <span data-ttu-id="4b0bb-181">-RetentionVolume</span><span class="sxs-lookup"><span data-stu-id="4b0bb-181">-RetentionVolume</span></span>
<span data-ttu-id="4b0bb-182">Громкость хранения на целевом сервере, который используется.</span><span class="sxs-lookup"><span data-stu-id="4b0bb-182">Retention Volume on the master target server to be used.</span></span>

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

### <span data-ttu-id="4b0bb-183">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="4b0bb-183">-VmmToVmm</span></span>
<span data-ttu-id="4b0bb-184">Обновите направление репликации для сбойного с виртуальной машины Hyper-V, которая защищена между двумя сайтами vMM Managed Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="4b0bb-184">Update replication direction for a failed over Hyper-V virtual machine that is protected between two VMM managed Hyper-V sites.</span></span>

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

### <span data-ttu-id="4b0bb-185">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="4b0bb-185">-VMwareToAzure</span></span>
<span data-ttu-id="4b0bb-186">Обновление направления репликации из VMware в Azure.</span><span class="sxs-lookup"><span data-stu-id="4b0bb-186">Update replication direction from VMware to Azure.</span></span>

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

### <span data-ttu-id="4b0bb-187">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4b0bb-187">-Confirm</span></span>
<span data-ttu-id="4b0bb-188">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b0bb-188">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b0bb-189">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b0bb-189">-WhatIf</span></span>
<span data-ttu-id="4b0bb-190">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b0bb-190">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4b0bb-191">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4b0bb-191">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b0bb-192">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b0bb-192">CommonParameters</span></span>
<span data-ttu-id="4b0bb-193">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b0bb-193">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b0bb-194">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4b0bb-194">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b0bb-195">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4b0bb-195">INPUTS</span></span>

### <span data-ttu-id="4b0bb-196">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="4b0bb-196">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="4b0bb-197">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="4b0bb-197">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="4b0bb-198">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4b0bb-198">OUTPUTS</span></span>

### <span data-ttu-id="4b0bb-199">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="4b0bb-199">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="4b0bb-200">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4b0bb-200">NOTES</span></span>

## <span data-ttu-id="4b0bb-201">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4b0bb-201">RELATED LINKS</span></span>
