---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: bde840903c53dae9ba47b9eb30634ce90f80ee9e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245918"
---
# <span data-ttu-id="fe9db-101">New-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="fe9db-101">New-AzRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="fe9db-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fe9db-102">SYNOPSIS</span></span>
<span data-ttu-id="fe9db-103">Включает репликацию для защищенного элемента ASR путем создания элемента, защищенного репликацией.</span><span class="sxs-lookup"><span data-stu-id="fe9db-103">Enables replication for an ASR protectable item by creating a replication protected item.</span></span>

## <span data-ttu-id="fe9db-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fe9db-104">SYNTAX</span></span>

### <span data-ttu-id="fe9db-105">EnterpriseToEnterprise (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fe9db-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VmmToVmm] -ProtectableItem <ASRProtectableItem>
 -Name <String> -ProtectionContainerMapping <ASRProtectionContainerMapping> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe9db-106">VMwareToAzureWithDiskType</span><span class="sxs-lookup"><span data-stu-id="fe9db-106">VMwareToAzureWithDiskType</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VMwareToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -Account <ASRRunAsAccount> [-LogStorageAccountId <String>] -ProcessServer <ASRProcessServer>
 [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String>
 [-ReplicationGroupName <String>] [-WaitForCompletion] -DiskType <String> [-DiskEncryptionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe9db-107">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="fe9db-107">VMwareToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-VMwareToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -Account <ASRRunAsAccount> [-LogStorageAccountId <String>]
 [-InMageAzureV2DiskInput <AsrInMageAzureV2DiskInput[]>] -ProcessServer <ASRProcessServer>
 [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String>
 [-ReplicationGroupName <String>] [-WaitForCompletion] [-DiskEncryptionSetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe9db-108">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="fe9db-108">EnterpriseToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -RecoveryResourceGroupId <String> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe9db-109">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="fe9db-109">HyperVSiteToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -OSDiskName <String> -OS <String> [-LogStorageAccountId <String>]
 [-IncludeDiskId <String[]>] [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>]
 -RecoveryResourceGroupId <String> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe9db-110">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="fe9db-110">AzureToAzure</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-AzureToAzure]
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]> -AzureVmId <String>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String>
 [-ReplicationGroupName <String>] [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilityZone <String>]
 [-RecoveryProximityPlacementGroupId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryBootDiagStorageAccountId <String>] [-DiskEncryptionVaultId <String>]
 [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>] [-KeyEncryptionVaultId <String>]
 [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe9db-111">AzureToAzureWithoutDiskDetails</span><span class="sxs-lookup"><span data-stu-id="fe9db-111">AzureToAzureWithoutDiskDetails</span></span>
```
New-AzRecoveryServicesAsrReplicationProtectedItem [-AzureToAzure] -AzureVmId <String> -Name <String>
 [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 [-RecoveryAzureStorageAccountId <String>] -LogStorageAccountId <String> [-RecoveryAzureNetworkId <String>]
 [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String> [-ReplicationGroupName <String>]
 [-RecoveryAvailabilityZone <String>] [-RecoveryProximityPlacementGroupId <String>]
 [-RecoveryAvailabilitySetId <String>] [-RecoveryBootDiagStorageAccountId <String>]
 [-DiskEncryptionVaultId <String>] [-DiskEncryptionSecretUrl <String>] [-KeyEncryptionKeyUrl <String>]
 [-KeyEncryptionVaultId <String>] [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe9db-112">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fe9db-112">DESCRIPTION</span></span>
<span data-ttu-id="fe9db-113">Командлет **New-AzRecoveryServicesAsrReplicationProtectedItem** создает новый элемент, защищенный репликацией.</span><span class="sxs-lookup"><span data-stu-id="fe9db-113">The **New-AzRecoveryServicesAsrReplicationProtectedItem** cmdlet creates a new replication protected item.</span></span>
<span data-ttu-id="fe9db-114">Используйте этот командлет, чтобы включить репликацию для защищенного элемента ASR.</span><span class="sxs-lookup"><span data-stu-id="fe9db-114">Use this cmdlet to enable replication for an ASR protectable item.</span></span>

## <span data-ttu-id="fe9db-115">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fe9db-115">EXAMPLES</span></span>

### <span data-ttu-id="fe9db-116">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fe9db-116">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrReplicationProtectedItem -ProtectableItem $VM -Name $VM.Name -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="fe9db-117">Запускает операцию создания защищенного элемента репликации для указанного защищенного элемента ASR и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="fe9db-117">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="fe9db-118">Пример 2</span><span class="sxs-lookup"><span data-stu-id="fe9db-118">Example 2</span></span>
```
PS C:\>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] `
-RecoveryResourceGroupId $RecoveryResourceGroupId -RecoveryAzureNetworkId $RecoveryAzureNetworkId  -name $name `
-ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem -ProtectionContainerMapping $pcm `
-RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName -LogStorageAccountId $LogStorageAccountId
```

<span data-ttu-id="fe9db-119">Запускает операцию создания защищенного элемента репликации для указанного защищенного элемента ASR и возвращает задание ASR, используемое для отслеживания операции (vmWare — сценарий Azure).</span><span class="sxs-lookup"><span data-stu-id="fe9db-119">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation(vmWare to Azure scenario).</span></span>

### <span data-ttu-id="fe9db-120">Пример 3</span><span class="sxs-lookup"><span data-stu-id="fe9db-120">Example 3</span></span>
```
PS C:>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureToAzureDiskReplicationConfig disk1,disk2 -AzVmId $vmId `
-Name "a2aprotectedItem" -RecoveryVmName "vmName" -ProtectionContainerMapping $pcmMapping -RecoveryResourceGroupId $recoveryResourceGroup
```

<span data-ttu-id="fe9db-121">Запускает операцию создания защищенного элемента репликации для указанного защищенного элемента ASR и возвращает задание ASR, используемое для отслеживания операции (в сценарии Azure to Azure).</span><span class="sxs-lookup"><span data-stu-id="fe9db-121">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

### <span data-ttu-id="fe9db-122">Пример 4</span><span class="sxs-lookup"><span data-stu-id="fe9db-122">Example 4</span></span>
```
PS C:\> $disk1 = New-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri1 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $disk2 = New-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri2 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $enableDRjob = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureVmId $vmId -Name $rpiName `
-RecoveryCloudServiceId  $recoveryCloudServiceId -ProtectionContainerMapping $pcm -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -RecoveryAzureNetworkId $RecoveryAzureNetworkId -RecoveryAzureSubnetName $RecoveryAzureSubnetName
```

<span data-ttu-id="fe9db-123">Запускает операцию создания защищенного элемента для репликации для указанного ИД VmId и возвращает задание ASR, используемое для отслеживания операции (в сценарии Azure to Azure).</span><span class="sxs-lookup"><span data-stu-id="fe9db-123">Starts the replication protected item creation operation for the specified VmId and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

### <span data-ttu-id="fe9db-124">Пример 5</span><span class="sxs-lookup"><span data-stu-id="fe9db-124">Example 5</span></span>
```
PS C:\>$disk1 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId -LogStorageAccountId $logStorageAccountId -DiskType $diskType
PS C:\>$disk2 = New-AzRecoveryServicesAsrInMageAzureV2DiskInput -DiskId $diskId2 -LogStorageAccountId $logStorageAccountId -DiskType $diskType2

PS C:\>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryAzureNetworkId $RecoveryAzureNetworkId  -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem  `
-ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName `
-LogStorageAccountId $LogStorageAccountId -InMageAzureV2DiskInput $disk1,$disk2
```

<span data-ttu-id="fe9db-125">Запускает операцию создания защищенного элемента для репликации для указанного защищенного элемента ASR, включая выборочные диски, и возвращает задание ASR, используемое для отслеживания операции (в сценарии vmWare — Azure) с выбранными дисками.</span><span class="sxs-lookup"><span data-stu-id="fe9db-125">Starts the replication protected item creation operation for the specified ASR protectable item including selective disks and returns the ASR job used to track the operation(vmWare to Azure scenario) with selected disks.</span></span>

### <span data-ttu-id="fe9db-126">Пример 6</span><span class="sxs-lookup"><span data-stu-id="fe9db-126">Example 6</span></span>
```
PS C:\>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -VMwareToAzure -Account $fabric.FabricSpecificDetails.RunAsAccounts[0] -RecoveryResourceGroupId $RecoveryResourceGroupId `
-RecoveryAzureNetworkId $RecoveryAzureNetworkId  -name $name -ProcessServer $fabric.FabricSpecificDetails.ProcessServers[0] -ProtectableItem $protectableItem  `
-ProtectionContainerMapping $pcm -RecoveryAzureSubnetName $RecoveryAzureSubnetName -RecoveryVmName $RecoveryVmName `
-LogStorageAccountId $LogStorageAccountId -DiskType Standard_LRS

Starts the replication protected item creation operation for the specified ASR protectable item with default disk type and returns the ASR job used to track the operation(vmWare to Azure scenario).
```

### <span data-ttu-id="fe9db-127">Пример 7</span><span class="sxs-lookup"><span data-stu-id="fe9db-127">Example 7</span></span>
```
PS C:\> $disk1 = New-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri1 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId -LogStorageAccountId $logStorageAccountId  
PS C:\> $disk2 = new-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri2 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId -LogStorageAccountId $logStorageAccountId  
PS C:\> $enableDRjob = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzVmId $vmId -Name $rpiName `
-RecoveryCloudServiceId  $recoveryCloudServiceId -ProtectionContainerMapping $pcm -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-AzureToAzureDiskReplicationConfiguration $disk1,$disk2 -DiskEncryptionVaultId  $DiskEncryptionVaultId -DiskEncryptionSecertUrl $DiskEncryptionSecertUrl `
 -KeyEncryptionVaultId $KeyEncryptionVaultId  -KeyEncryptionKeyUrl $KeyEncryptionKeyUrl
```

<span data-ttu-id="fe9db-128">Запускает операцию создания защищенного элемента для репликации для указанного ИД VmId и возвращает задание ASR, используемое для отслеживания операции (в сценарии Azure to Azure). Для данных, передаваемых в командлете для шифрования, будет использоваться информация для отказоустойчивой виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="fe9db-128">Starts the replication protected item creation operation for the specified VmId and returns the ASR job used to track the operation (Azure to Azure scenario).For the failover VM details passed in cmdlet for encryption will be used .</span></span>

### <span data-ttu-id="fe9db-129">Пример 8</span><span class="sxs-lookup"><span data-stu-id="fe9db-129">Example 8</span></span>
```
PS C:>$job = New-AzRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureToAzureDiskReplicationConfig disk1,disk2 -AzVmId $vmId `
-Name "a2aprotectedItem" -RecoveryVmName "vmName" -ProtectionContainerMapping $pcmMapping -RecoveryResourceGroupId $recoveryResourceGroup -RecoveryProximityPlacementGroupId $ppg
```

<span data-ttu-id="fe9db-130">Запускает операцию создания элемента, защищенную репликацией, для виртуальной машины в группе размещения близких и возвращает задание ASR, используемое для отслеживания операции (в сценарии Azure to Azure).</span><span class="sxs-lookup"><span data-stu-id="fe9db-130">Starts the replication protected item creation operation for a Virtual Machine inside Proximity placement group and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

## <span data-ttu-id="fe9db-131">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fe9db-131">PARAMETERS</span></span>

### <span data-ttu-id="fe9db-132">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="fe9db-132">-Account</span></span>
<span data-ttu-id="fe9db-133">Учетная запись запуска от имени, которая будет использоваться для принудительной установки службы Mobility Service при необходимости.</span><span class="sxs-lookup"><span data-stu-id="fe9db-133">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="fe9db-134">Должен быть один из списка учетных записей запуска от имени в структуре ASR.</span><span class="sxs-lookup"><span data-stu-id="fe9db-134">Must be one from the list of run as accounts in the ASR fabric.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe9db-135">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="fe9db-135">-AzureToAzure</span></span>
<span data-ttu-id="fe9db-136">Параметр Switch указывает на необходимость создания реплицируемого элемента в Azure to Azure.</span><span class="sxs-lookup"><span data-stu-id="fe9db-136">Switch parameter specifies creating the replicated item in azure to azure scenario.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe9db-137">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="fe9db-137">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="fe9db-138">Указывает конфигурацию диска для использования в сценарии аварийного восстановления Azure to Azure.</span><span class="sxs-lookup"><span data-stu-id="fe9db-138">Specifies the disk configuration to used Vm for Azure to Azure disaster recovery scenario.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe9db-139">-AzureVmId</span><span class="sxs-lookup"><span data-stu-id="fe9db-139">-AzureVmId</span></span>
<span data-ttu-id="fe9db-140">Указывает идентификатор виртуальной машины Azure для защиты аварийного восстановления в области восстановления.</span><span class="sxs-lookup"><span data-stu-id="fe9db-140">Specifies the Azure VM id for disaster recovery protection in recovery region.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe9db-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe9db-141">-DefaultProfile</span></span>
<span data-ttu-id="fe9db-142">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fe9db-142">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="fe9db-143">-DiskEncryptionSecretUrl</span><span class="sxs-lookup"><span data-stu-id="fe9db-143">-DiskEncryptionSecretUrl</span></span>
<span data-ttu-id="fe9db-144">Указывает секретный URL-адрес шифрования диска, который будет использоваться в качестве виртуальной машины для восстановления после отработки отказа (шифрование диска Azure).</span><span class="sxs-lookup"><span data-stu-id="fe9db-144">Specifies the disk encryption secret URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe9db-145">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="fe9db-145">-DiskEncryptionSetId</span></span>
<span data-ttu-id="fe9db-146">Указывает идентификатор ресурса набора шифрования диска, который будет использоваться для шифрования управляемых дисков.</span><span class="sxs-lookup"><span data-stu-id="fe9db-146">Specifies the resource Id of the disk encryption set, to be used for the encryption of the managed disks.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe9db-147">-DiskEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="fe9db-147">-DiskEncryptionVaultId</span></span>
<span data-ttu-id="fe9db-148">Задает секретный код (шифрование диска Azure), который будет использоваться для восстановления виртуальной машины после отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="fe9db-148">Specifies the disk encryption secret vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe9db-149">-DiskType</span><span class="sxs-lookup"><span data-stu-id="fe9db-149">-DiskType</span></span>
<span data-ttu-id="fe9db-150">Указывает тип диска, управляемого восстановлением для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="fe9db-150">Specifies the Recovery VM managed disk type.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe9db-151">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="fe9db-151">-HyperVToAzure</span></span>
<span data-ttu-id="fe9db-152">Параметр Switch, указывающий, что реплицируемый элемент — это виртуальная машина Hyper-V, реплицируемая в Azure.</span><span class="sxs-lookup"><span data-stu-id="fe9db-152">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated to Azure.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe9db-153">-IncludeDiskId</span><span class="sxs-lookup"><span data-stu-id="fe9db-153">-IncludeDiskId</span></span>
<span data-ttu-id="fe9db-154">Список дисков, которые нужно включить в репликацию.</span><span class="sxs-lookup"><span data-stu-id="fe9db-154">The list of disks to include for replication.</span></span> <span data-ttu-id="fe9db-155">По умолчанию включаются все диски.</span><span class="sxs-lookup"><span data-stu-id="fe9db-155">By default all disks are included.</span></span>

```yaml
Type: System.String[]
Parameter Sets: HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe9db-156">-InMageAzureV2DiskInput</span><span class="sxs-lookup"><span data-stu-id="fe9db-156">-InMageAzureV2DiskInput</span></span>
<span data-ttu-id="fe9db-157">Задает входную конфигурацию диска для идентификатора диска vMWare для защиты от указанного защищенного элемента.</span><span class="sxs-lookup"><span data-stu-id="fe9db-157">Specifies the disk configuration input for vMWare disk id to protect from specified protectable item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.AsrInMageAzureV2DiskInput[]
Parameter Sets: VMwareToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe9db-158">-KeyEncryptionKeyUrl</span><span class="sxs-lookup"><span data-stu-id="fe9db-158">-KeyEncryptionKeyUrl</span></span>
<span data-ttu-id="fe9db-159">Задает URL-адрес ключа шифрования диска с версией (шифрованием с помощью Azure) для восстановления виртуальной машины после отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="fe9db-159">Specifies the disk encryption key URL with version(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe9db-160">-KeyEncryptionVaultId</span><span class="sxs-lookup"><span data-stu-id="fe9db-160">-KeyEncryptionVaultId</span></span>
<span data-ttu-id="fe9db-161">Указывает, что при переходе на другой ресурс в качестве виртуальной машины для восстановления используется ИД ключа шифрования диска (шифрование диска Azure).</span><span class="sxs-lookup"><span data-stu-id="fe9db-161">Specifies the disk encryption key key-vault ID(Azure disk encryption) to be used be recovery VM after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe9db-162">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="fe9db-162">-LogStorageAccountId</span></span>
<span data-ttu-id="fe9db-163">Указывает идентификатор журнала или учетной записи для хранения кэша, который будет использоваться для хранения журналов репликации.</span><span class="sxs-lookup"><span data-stu-id="fe9db-163">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AzureToAzureWithoutDiskDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe9db-164">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fe9db-164">-Name</span></span>
<span data-ttu-id="fe9db-165">Задает имя для элемента, защищенного репликацией ASR.</span><span class="sxs-lookup"><span data-stu-id="fe9db-165">Specifies a name for the ASR replication protected item.</span></span> <span data-ttu-id="fe9db-166">Имя должно быть уникальным в пределах хранилища.</span><span class="sxs-lookup"><span data-stu-id="fe9db-166">The name must be unique within the vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe9db-167">-OS</span><span class="sxs-lookup"><span data-stu-id="fe9db-167">-OS</span></span>
<span data-ttu-id="fe9db-168">Указывает семейство операционной системы.</span><span class="sxs-lookup"><span data-stu-id="fe9db-168">Specifies the operating system family.</span></span>
<span data-ttu-id="fe9db-169">Допустимые значения этого параметра: Windows или Linux.</span><span class="sxs-lookup"><span data-stu-id="fe9db-169">The acceptable values for this parameter are: Windows or Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVSiteToAzure
Aliases:
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe9db-170">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="fe9db-170">-OSDiskName</span></span>
<span data-ttu-id="fe9db-171">Указывает имя диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="fe9db-171">Specifies the name of the operating system disk.</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVSiteToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe9db-172">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="fe9db-172">-ProcessServer</span></span>
<span data-ttu-id="fe9db-173">Сервер обработки, который будет использоваться для репликации этого компьютера.</span><span class="sxs-lookup"><span data-stu-id="fe9db-173">The Process Server to use to replicate this machine.</span></span> <span data-ttu-id="fe9db-174">С помощью списка серверов обработки в структуре ASR, соответствующей серверу конфигурации, укажите один из них.</span><span class="sxs-lookup"><span data-stu-id="fe9db-174">Use the list of process servers in the ASR fabric corresponding to the Configuration server to specify one.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProcessServer
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe9db-175">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="fe9db-175">-ProtectableItem</span></span>
<span data-ttu-id="fe9db-176">Указывает объект защищенного элемента ASR, для которого включена репликация.</span><span class="sxs-lookup"><span data-stu-id="fe9db-176">Specifies the ASR protectable item object for which replication is being enabled.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem
Parameter Sets: EnterpriseToEnterprise, VMwareToAzureWithDiskType, VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe9db-177">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="fe9db-177">-ProtectionContainerMapping</span></span>
<span data-ttu-id="fe9db-178">Указывает объект сопоставления контейнера защиты ASR, соответствующий политике репликации, которая должна использоваться для репликации.</span><span class="sxs-lookup"><span data-stu-id="fe9db-178">Specifies the ASR protection container mapping object corresponding to the replication policy to be used for replication.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe9db-179">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="fe9db-179">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="fe9db-180">Идентификатор набора доступности для восстановления компьютера в случае отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="fe9db-180">The ID of the AvailabilitySet to recover the machine to in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe9db-181">-RecoveryAvailabilityZone</span><span class="sxs-lookup"><span data-stu-id="fe9db-181">-RecoveryAvailabilityZone</span></span>
<span data-ttu-id="fe9db-182">Указывает зону доступности виртуальной машины для восстановления после перехода на другой ресурс.</span><span class="sxs-lookup"><span data-stu-id="fe9db-182">Specifies the recovery VM availability zone after failover.</span></span>


```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe9db-183">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="fe9db-183">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="fe9db-184">ИДЕНТИФИКАТОР виртуальной сети Azure для восстановления компьютера в случае отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="fe9db-184">The ID of the Azure virtual network to recover the machine to in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe9db-185">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="fe9db-185">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="fe9db-186">Указывает идентификатор учетной записи хранения Azure, на которую должна выполняться репликация.</span><span class="sxs-lookup"><span data-stu-id="fe9db-186">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure, HyperVSiteToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe9db-187">-RecoveryAzureSubnetName</span><span class="sxs-lookup"><span data-stu-id="fe9db-187">-RecoveryAzureSubnetName</span></span>
<span data-ttu-id="fe9db-188">Подсеть в виртуальной сети восстановления Azure, к которой следует прикрепить сбой виртуальной машины в случае отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="fe9db-188">The subnet within the recovery Azure virtual network to which the failed over virtual machine should be attached in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe9db-189">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="fe9db-189">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="fe9db-190">Указывает учетную запись хранения для диагностики загрузки для восстановления ВМ Azure.</span><span class="sxs-lookup"><span data-stu-id="fe9db-190">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe9db-191">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="fe9db-191">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="fe9db-192">Указывает идентификатор ресурса облачной службы восстановления, на которую следует отработка отказа виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="fe9db-192">Specifies the resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe9db-193">-RecoveryProximityPlacementGroupId</span><span class="sxs-lookup"><span data-stu-id="fe9db-193">-RecoveryProximityPlacementGroupId</span></span>
<span data-ttu-id="fe9db-194">Укажите идентификатор группы размещения близкого взаимодействия, который будет использоваться при отработке отказа виртуальной машины в целевом регионе восстановления.</span><span class="sxs-lookup"><span data-stu-id="fe9db-194">Specify the proximity placement group Id to used by the failover Vm in target recovery region.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe9db-195">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="fe9db-195">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="fe9db-196">Указывает идентификатор ARM для группы ресурсов, в которой виртуальная машина будет создана в случае отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="fe9db-196">Specifies the ARM identifier of the resource group in which the virtual machine will be created in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe9db-197">-RecoveryVmName</span><span class="sxs-lookup"><span data-stu-id="fe9db-197">-RecoveryVmName</span></span>
<span data-ttu-id="fe9db-198">Имя виртуальной машины восстановления, созданной после перехода на другой ресурс.</span><span class="sxs-lookup"><span data-stu-id="fe9db-198">Name of the recovery Vm created after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe9db-199">-ReplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="fe9db-199">-ReplicationGroupName</span></span>
<span data-ttu-id="fe9db-200">Указывает имя группы репликации, которое будет использоваться для создания точек восстановления с несколькими виртуальными машинами.</span><span class="sxs-lookup"><span data-stu-id="fe9db-200">Specifies the replication group name to use to create multi-VM consistent recovery points.</span></span> <span data-ttu-id="fe9db-201">По умолчанию каждый элемент, защищенный репликацией, создается в группе собственной и постоянной точки восстановления из-за множественной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="fe9db-201">By default each replication protected item is created in a group of its own and multi-VM consistent recovery points are not generated.</span></span> <span data-ttu-id="fe9db-202">Используйте этот параметр только в том случае, если вам нужно создать точки восстановления с несколькими виртуальными машинами в группе компьютеров, защищая все компьютеры к одной группе репликации.</span><span class="sxs-lookup"><span data-stu-id="fe9db-202">Use this option only if you need to create multi-VM consistent recovery points across a group of machines by protecting all machines to the same replication group.</span></span> 

```yaml
Type: System.String
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe9db-203">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="fe9db-203">-VmmToVmm</span></span>
<span data-ttu-id="fe9db-204">Параметр Switch, указывающий, что реплицируемый элемент — это виртуальная машина Hyper-V, реплицируемая между сайтами Hyper-V, управляемыми VMM.</span><span class="sxs-lookup"><span data-stu-id="fe9db-204">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated between VMM managed Hyper-V sites.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe9db-205">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="fe9db-205">-VMwareToAzure</span></span>
<span data-ttu-id="fe9db-206">Параметр Switch, указывающий, что реплицированный элемент является виртуальной машиной VMware или физическим сервером, который будет реплицирован в Azure.</span><span class="sxs-lookup"><span data-stu-id="fe9db-206">Switch parameter to specify the replicated item is a VMware virtual machine or physical server that will be replicate to Azure.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: VMwareToAzureWithDiskType, VMwareToAzure
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe9db-207">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="fe9db-207">-WaitForCompletion</span></span>
<span data-ttu-id="fe9db-208">Указывает, что перед возвратом командлет должен дождаться завершения операции.</span><span class="sxs-lookup"><span data-stu-id="fe9db-208">Specifies that the cmdlet should wait for completion of the operation before returning.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe9db-209">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fe9db-209">-Confirm</span></span>
<span data-ttu-id="fe9db-210">Запрашивает подтверждение перед запуском операции.</span><span class="sxs-lookup"><span data-stu-id="fe9db-210">Prompts  for confirmation before starting the operation.</span></span>

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

### <span data-ttu-id="fe9db-211">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe9db-211">-WhatIf</span></span>
<span data-ttu-id="fe9db-212">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fe9db-212">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe9db-213">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fe9db-213">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe9db-214">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe9db-214">CommonParameters</span></span>
<span data-ttu-id="fe9db-215">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fe9db-215">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe9db-216">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fe9db-216">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe9db-217">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fe9db-217">INPUTS</span></span>

### <span data-ttu-id="fe9db-218">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="fe9db-218">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="fe9db-219">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fe9db-219">OUTPUTS</span></span>

### <span data-ttu-id="fe9db-220">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="fe9db-220">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="fe9db-221">Пуск</span><span class="sxs-lookup"><span data-stu-id="fe9db-221">NOTES</span></span>

## <span data-ttu-id="fe9db-222">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fe9db-222">RELATED LINKS</span></span>

[<span data-ttu-id="fe9db-223">Get-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="fe9db-223">Get-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="fe9db-224">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="fe9db-224">Remove-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="fe9db-225">Set-AzRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="fe9db-225">Set-AzRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzRecoveryServicesAsrReplicationProtectedItem.md)
