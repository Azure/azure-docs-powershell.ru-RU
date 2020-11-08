---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrprotectiondirection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionDirection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrProtectionDirection.md
ms.openlocfilehash: 32218fdb966a17cedcb51a2838acae1ae79d9f54
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073516"
---
# <span data-ttu-id="729ba-101">Update-AzRecoveryServicesAsrProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="729ba-101">Update-AzRecoveryServicesAsrProtectionDirection</span></span>

## <span data-ttu-id="729ba-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="729ba-102">SYNOPSIS</span></span>
<span data-ttu-id="729ba-103">Обновляет направление репликации для указанного защищенного элемента или плана восстановления для репликации.</span><span class="sxs-lookup"><span data-stu-id="729ba-103">Updates the replication direction for the specified replication protected item or recovery plan.</span></span> <span data-ttu-id="729ba-104">Используется для повторной защиты или обратной репликации, которая переносит отказ на реплицируемый элемент или план восстановления.</span><span class="sxs-lookup"><span data-stu-id="729ba-104">Used to re-protect/reverse replicate a failed over replicated item or recovery plan.</span></span>

## <span data-ttu-id="729ba-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="729ba-105">SYNTAX</span></span>

### <span data-ttu-id="729ba-106">ByRPIObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="729ba-106">ByRPIObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="729ba-107">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="729ba-107">AzureToVMware</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToVMware] [-Account <ASRRunAsAccount>]
 -DataStore <ASRDataStore> [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 -RetentionVolume <ASRRetentionVolume> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="729ba-108">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="729ba-108">VMwareToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-VMwareToAzure] -Account <ASRRunAsAccount>
 [-MasterTarget <ASRMasterTargetServer>] -ProcessServer <ASRProcessServer>
 -ProtectionContainerMapping <ASRProtectionContainerMapping> [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="729ba-109">HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="729ba-109">HyperVToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-HyperVToAzure] [-LogStorageAccountId <String>]
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="729ba-110">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="729ba-110">EnterpriseToEnterprise</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-VmmToVmm]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="729ba-111">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="729ba-111">AzureToAzure</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToAzure]
 -ProtectionContainerMapping <ASRProtectionContainerMapping> -LogStorageAccountId <String>
 [-RecoveryAzureStorageAccountId <String>] -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-RecoveryResourceGroupId <String>] [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryBootDiagStorageAccountId <String>] [-DiskEncryptionVaultId <String>]
 [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>] [-KeyEncryptionVaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="729ba-112">AzureToAzureWithMultipleStorageAccount</span><span class="sxs-lookup"><span data-stu-id="729ba-112">AzureToAzureWithMultipleStorageAccount</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection [-AzureToAzure]
 -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]>
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-RecoveryResourceGroupId <String>]
 [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryBootDiagStorageAccountId <String>] [-DiskEncryptionVaultId <String>]
 [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>] [-KeyEncryptionVaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="729ba-113">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="729ba-113">ByRPObject</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="729ba-114">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="729ba-114">ByPEObject</span></span>
```
Update-AzRecoveryServicesAsrProtectionDirection -Direction <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="729ba-115">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="729ba-115">DESCRIPTION</span></span>
<span data-ttu-id="729ba-116">Командлет **Update-AzRecoveryServicesAsrProtectionDirection** обновляет направление репликации для указанного объекта Azure Site Recovery после завершения операции фиксации отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="729ba-116">The **Update-AzRecoveryServicesAsrProtectionDirection** cmdlet updates the replication direction for the specified Azure Site Recovery object after the completion of a commit failover operation.</span></span>

## <span data-ttu-id="729ba-117">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="729ba-117">EXAMPLES</span></span>

### <span data-ttu-id="729ba-118">Пример 1</span><span class="sxs-lookup"><span data-stu-id="729ba-118">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="729ba-119">Начните операцию направления обновления для указанного плана восстановления и возвращает объект задания ASR, который используется для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="729ba-119">Start the update direction operation for the specified recovery plan and returns the ASR job object used to track the operation.</span></span>

### <span data-ttu-id="729ba-120">Пример 2</span><span class="sxs-lookup"><span data-stu-id="729ba-120">Example 2</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping -LogStorageAccountId $cacheStorageId `
 -ReplicationProtectedItem $rpi
```

<span data-ttu-id="729ba-121">Начните операцию направления обновления для указанного элемента, защищенного репликацией, в целевом регионе Azure, определяемом сопоставлением контейнера защиты, и с помощью хранилища кэша (в том же регионе, что и VM).</span><span class="sxs-lookup"><span data-stu-id="729ba-121">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and using cache storage (in same region as VM).</span></span>

### <span data-ttu-id="729ba-122">Пример 3</span><span class="sxs-lookup"><span data-stu-id="729ba-122">Example 3</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping `
 -AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -ReplicationProtectedItem  $rpi
```

<span data-ttu-id="729ba-123">Начните операцию направления обновления для указанного элемента, защищенного репликацией, в целевом регионе Azure, определяемом сопоставлением контейнеров защиты и указанной конфигурацией репликации дисков.</span><span class="sxs-lookup"><span data-stu-id="729ba-123">Start the update direction operation for the specified replication protected item in target azure region defined by protection container mapping and provided disk replication configuration.</span></span>

### <span data-ttu-id="729ba-124">Пример 4</span><span class="sxs-lookup"><span data-stu-id="729ba-124">Example 4</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrProtectionDirection -AzureToAzure -ProtectionContainerMapping $B2ApcmMapping `
 -AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -ReplicationProtectedItem  $rpi `
 -DiskEncryptionVaultId  $DiskEncryptionVaultId -DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
 -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

    
<span data-ttu-id="729ba-125">Начните операцию направления обновления для указанного защищенного элемента с шифрованием в целевом регионе Azure, определяемом сопоставлением контейнеров защиты и указанной конфигурацией репликации дисков.</span><span class="sxs-lookup"><span data-stu-id="729ba-125">Start the update direction operation for the specified encrypted replication protected item in target azure region defined by protection container mapping and provided disk replication configuration.</span></span>

## <span data-ttu-id="729ba-126">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="729ba-126">PARAMETERS</span></span>

### <span data-ttu-id="729ba-127">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="729ba-127">-Account</span></span>
<span data-ttu-id="729ba-128">Учетная запись запуска от имени, которая будет использоваться для принудительной установки службы Mobility Service при необходимости.</span><span class="sxs-lookup"><span data-stu-id="729ba-128">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="729ba-129">Должен быть один из списка учетных записей запуска от имени в структуре ASR.</span><span class="sxs-lookup"><span data-stu-id="729ba-129">Must be one from the list of run as accounts in the ASR fabric.</span></span>

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

### <span data-ttu-id="729ba-130">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="729ba-130">-AzureToAzure</span></span>
<span data-ttu-id="729ba-131">Указывает на аварийное восстановление Azure для Azure.</span><span class="sxs-lookup"><span data-stu-id="729ba-131">Specifies the Azure to Azure disaster recovery.</span></span>

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

### <span data-ttu-id="729ba-132">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="729ba-132">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="729ba-133">Указывает конфигурацию диска для аварийного восстановления.</span><span class="sxs-lookup"><span data-stu-id="729ba-133">Specifies the disk configuration for disaster recovery.</span></span>

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

### <span data-ttu-id="729ba-134">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="729ba-134">-AzureToVMware</span></span>
<span data-ttu-id="729ba-135">Указывает сценарий переключения с Azure на vMWare.</span><span class="sxs-lookup"><span data-stu-id="729ba-135">Specifies the switch azure to vMWare scenario.</span></span>

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

### <span data-ttu-id="729ba-136">-DataStore</span><span class="sxs-lookup"><span data-stu-id="729ba-136">-DataStore</span></span>
<span data-ttu-id="729ba-137">Хранилище данных VMware, используемое для vmdisk.</span><span class="sxs-lookup"><span data-stu-id="729ba-137">The VMware data-store to be used for the vmdisk's.</span></span>

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

### <span data-ttu-id="729ba-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="729ba-138">-DefaultProfile</span></span>
<span data-ttu-id="729ba-139">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="729ba-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="729ba-140">-Направление</span><span class="sxs-lookup"><span data-stu-id="729ba-140">-Direction</span></span>
<span data-ttu-id="729ba-141">Указывает направление, которое будет использоваться для операции обновления. Опубликуйте отработку отказа.</span><span class="sxs-lookup"><span data-stu-id="729ba-141">Specifies the direction to be used for the update operation post a failover.</span></span>
<span data-ttu-id="729ba-142">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="729ba-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="729ba-143">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="729ba-143">PrimaryToRecovery</span></span>
- <span data-ttu-id="729ba-144">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="729ba-144">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="729ba-145">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="729ba-145">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="729ba-146">Указывает секретный URL-адрес шифрования диска, который будет использоваться в качестве виртуальной машины для восстановления после отработки отказа (шифрование диска Azure).</span><span class="sxs-lookup"><span data-stu-id="729ba-146">Specifies the disk encryption secret URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="729ba-147">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="729ba-147">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="729ba-148">Задает секретный код (шифрование диска Azure), который будет использоваться для восстановления виртуальной машины после отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="729ba-148">Specifies the disk encryption secret vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="729ba-149">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="729ba-149">-HyperVToAzure</span></span>
<span data-ttu-id="729ba-150">Повторно включите защиту виртуальной машины Hyper-V после восстановления после сбоя.</span><span class="sxs-lookup"><span data-stu-id="729ba-150">Reprotect a Hyper-V virtual machine after failback.</span></span>

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

### <span data-ttu-id="729ba-151">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="729ba-151">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="729ba-152">Указывает, что URL-адрес ключа шифрования диска (шифрование диска Azure) будет использоваться для восстановления виртуальной машины после перехода на другой ресурс.</span><span class="sxs-lookup"><span data-stu-id="729ba-152">Specifies the disk encryption key URL(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="729ba-153">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="729ba-153">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="729ba-154">Указывает, что при переходе на другой ресурс keyVault ключ шифрования диска (шифрование диска Azure) будет использоваться для восстановления виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="729ba-154">Specifies the disk encryption key keyVault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

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

### <span data-ttu-id="729ba-155">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="729ba-155">-LogStorageAccountId</span></span>
<span data-ttu-id="729ba-156">Указывает идентификатор учетной записи хранения для хранения журнала репликации виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="729ba-156">Specifies the storage account ID to store the replication log of VMs.</span></span>

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

### <span data-ttu-id="729ba-157">-MasterTarget</span><span class="sxs-lookup"><span data-stu-id="729ba-157">-MasterTarget</span></span>
<span data-ttu-id="729ba-158">Сведения о главном целевом сервере.</span><span class="sxs-lookup"><span data-stu-id="729ba-158">Master Target Server Details.</span></span>

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

### <span data-ttu-id="729ba-159">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="729ba-159">-ProcessServer</span></span>
<span data-ttu-id="729ba-160">Сервер обработки, который будет использоваться для репликации.</span><span class="sxs-lookup"><span data-stu-id="729ba-160">Process Server to be used for replication.</span></span>

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

### <span data-ttu-id="729ba-161">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="729ba-161">-ProtectionContainerMapping</span></span>
<span data-ttu-id="729ba-162">ContainerMapping защиты, которую необходимо использовать для репликации.</span><span class="sxs-lookup"><span data-stu-id="729ba-162">Protection containerMapping to be used for replication.</span></span>

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

### <span data-ttu-id="729ba-163">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="729ba-163">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="729ba-164">Группа доступности, на которой должна быть создана виртуальная машина при переходе на другой ресурс</span><span class="sxs-lookup"><span data-stu-id="729ba-164">The availability set that the virtual machine should be created in upon failover</span></span>

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

### <span data-ttu-id="729ba-165">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="729ba-165">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="729ba-166">Указывает идентификатор учетной записи хранения Azure, на которую должна выполняться репликация.</span><span class="sxs-lookup"><span data-stu-id="729ba-166">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="729ba-167">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="729ba-167">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="729ba-168">Указывает учетную запись хранения для диагностики загрузки для восстановления ВМ Azure.</span><span class="sxs-lookup"><span data-stu-id="729ba-168">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

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

### <span data-ttu-id="729ba-169">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="729ba-169">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="729ba-170">Идентификатор ресурса облачной службы восстановления, на которую следует отработка отказа виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="729ba-170">The resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="729ba-171">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="729ba-171">-RecoveryPlan</span></span>
<span data-ttu-id="729ba-172">Указывает объект плана восстановления ASR.</span><span class="sxs-lookup"><span data-stu-id="729ba-172">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="729ba-173">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="729ba-173">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="729ba-174">Идентификатор resourceGroup восстановления для защищенной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="729ba-174">Recovery resourceGroup id for protected Vm.</span></span>

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

### <span data-ttu-id="729ba-175">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="729ba-175">-ReplicationProtectedItem</span></span>
<span data-ttu-id="729ba-176">Задает защищенный элемент репликации ASR.</span><span class="sxs-lookup"><span data-stu-id="729ba-176">Specifies an ASR replication protected item.</span></span>

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

### <span data-ttu-id="729ba-177">-RetentionVolume</span><span class="sxs-lookup"><span data-stu-id="729ba-177">-RetentionVolume</span></span>
<span data-ttu-id="729ba-178">Том хранения на главном целевом сервере, который нужно использовать.</span><span class="sxs-lookup"><span data-stu-id="729ba-178">Retention Volume on the master target server to be used.</span></span>

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

### <span data-ttu-id="729ba-179">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="729ba-179">-VmmToVmm</span></span>
<span data-ttu-id="729ba-180">Изменение направления репликации для сбоя на виртуальной машине Hyper-V, защищенной между двумя сайтами Hyper-V, управляемыми VMM.</span><span class="sxs-lookup"><span data-stu-id="729ba-180">Update replication direction for a failed over Hyper-V virtual machine that is protected between two VMM managed Hyper-V sites.</span></span>

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

### <span data-ttu-id="729ba-181">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="729ba-181">-VMwareToAzure</span></span>
<span data-ttu-id="729ba-182">Обновите направление репликации с VMware на Azure.</span><span class="sxs-lookup"><span data-stu-id="729ba-182">Update replication direction from VMware to Azure.</span></span>

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

### <span data-ttu-id="729ba-183">-Confirm</span><span class="sxs-lookup"><span data-stu-id="729ba-183">-Confirm</span></span>
<span data-ttu-id="729ba-184">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="729ba-184">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="729ba-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="729ba-185">-WhatIf</span></span>
<span data-ttu-id="729ba-186">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="729ba-186">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="729ba-187">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="729ba-187">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="729ba-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="729ba-188">CommonParameters</span></span>
<span data-ttu-id="729ba-189">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="729ba-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="729ba-190">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="729ba-190">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="729ba-191">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="729ba-191">INPUTS</span></span>

### <span data-ttu-id="729ba-192">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="729ba-192">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="729ba-193">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="729ba-193">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="729ba-194">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="729ba-194">OUTPUTS</span></span>

### <span data-ttu-id="729ba-195">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="729ba-195">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="729ba-196">Пуск</span><span class="sxs-lookup"><span data-stu-id="729ba-196">NOTES</span></span>

## <span data-ttu-id="729ba-197">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="729ba-197">RELATED LINKS</span></span>
