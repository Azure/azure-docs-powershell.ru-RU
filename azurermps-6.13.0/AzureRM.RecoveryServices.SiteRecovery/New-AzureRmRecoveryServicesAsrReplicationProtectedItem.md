---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrReplicationProtectedItem.md
ms.openlocfilehash: 6a35620b7a4d8952b10973f181c2ab50f5d958b7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556543"
---
# <span data-ttu-id="d8b2a-101">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d8b2a-101">New-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>

## <span data-ttu-id="d8b2a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d8b2a-102">SYNOPSIS</span></span>
<span data-ttu-id="d8b2a-103">Включает репликацию для защищенного элемента ASR путем создания элемента, защищенного репликацией.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-103">Enables replication for an ASR protectable item by creating a replication protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8b2a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d8b2a-104">SYNTAX</span></span>

### <span data-ttu-id="d8b2a-105">EnterpriseToEnterprise (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d8b2a-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-VmmToVmm] -ProtectableItem <ASRProtectableItem>
 -Name <String> -ProtectionContainerMapping <ASRProtectionContainerMapping> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8b2a-106">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="d8b2a-106">VMwareToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-VMwareToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -Account <ASRRunAsAccount> [-LogStorageAccountId <String>]
 [-IncludeDiskId <String[]>] -ProcessServer <ASRProcessServer> [-RecoveryAzureNetworkId <String>]
 [-RecoveryAzureSubnetName <String>] -RecoveryResourceGroupId <String> [-ReplicationGroupName <String>]
 [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8b2a-107">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="d8b2a-107">EnterpriseToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -RecoveryResourceGroupId <String> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8b2a-108">HyperVSiteToAzure</span><span class="sxs-lookup"><span data-stu-id="d8b2a-108">HyperVSiteToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-HyperVToAzure] -ProtectableItem <ASRProtectableItem>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryAzureStorageAccountId <String> -OSDiskName <String> -OS <String> [-LogStorageAccountId <String>]
 [-IncludeDiskId <String[]>] [-RecoveryAzureNetworkId <String>] [-RecoveryAzureSubnetName <String>]
 -RecoveryResourceGroupId <String> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8b2a-109">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="d8b2a-109">AzureToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-AzureToAzure]
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]> -AzureVmId <String>
 -Name <String> [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 -RecoveryResourceGroupId <String> [-RecoveryCloudServiceId <String>] [-RecoveryAvailabilitySetId <String>]
 [-RecoveryBootDiagStorageAccountId <String>] [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8b2a-110">AzureToAzureWithoutDiskDetails</span><span class="sxs-lookup"><span data-stu-id="d8b2a-110">AzureToAzureWithoutDiskDetails</span></span>
```
New-AzureRmRecoveryServicesAsrReplicationProtectedItem [-AzureToAzure] -AzureVmId <String> -Name <String>
 [-RecoveryVmName <String>] -ProtectionContainerMapping <ASRProtectionContainerMapping>
 [-RecoveryAzureStorageAccountId <String>] -LogStorageAccountId <String> -RecoveryResourceGroupId <String>
 [-RecoveryAvailabilitySetId <String>] [-RecoveryBootDiagStorageAccountId <String>] [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8b2a-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8b2a-111">DESCRIPTION</span></span>
<span data-ttu-id="d8b2a-112">Командлет **New-AzureRmRecoveryServicesAsrReplicationProtectedItem** создает новый элемент, защищенный репликацией.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-112">The **New-AzureRmRecoveryServicesAsrReplicationProtectedItem** cmdlet creates a new replication protected item.</span></span>
<span data-ttu-id="d8b2a-113">Используйте этот командлет, чтобы включить репликацию для защищенного элемента ASR.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-113">Use this cmdlet to enable replication for an ASR protectable item.</span></span>

## <span data-ttu-id="d8b2a-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d8b2a-114">EXAMPLES</span></span>

### <span data-ttu-id="d8b2a-115">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d8b2a-115">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem $VM -Name $VM.Name -ProtectionContainerMapping $ProtectionContainerMapping
```

<span data-ttu-id="d8b2a-116">Запускает операцию создания защищенного элемента репликации для указанного защищенного элемента ASR и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-116">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="d8b2a-117">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d8b2a-117">Example 2</span></span>
```
PS C:\>$job = New-AzureRmRecoveryServicesAsrReplicationProtectedItem -ProtectableItem $pi -Name $rpiName -ProtectionContainerMapping $pcm `
-RecoveryAzureStorageAccountId $RecoveryAzureStorageAccountId -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-ProcessServer $fabric.fabricSpecificDetails.ProcessServers[0] -Account $fabric.fabricSpecificDetails.RunAsAccounts[0]
```

<span data-ttu-id="d8b2a-118">Запускает операцию создания защищенного элемента репликации для указанного защищенного элемента ASR и возвращает задание ASR, используемое для отслеживания операции (vmWare — сценарий Azure).</span><span class="sxs-lookup"><span data-stu-id="d8b2a-118">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation(vmWare to Azure scenario).</span></span>

### <span data-ttu-id="d8b2a-119">Пример 3</span><span class="sxs-lookup"><span data-stu-id="d8b2a-119">Example 3</span></span>
```
PS C:>$job = New-AzureRmRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureToAzureDiskReplicationConfig disk1,disk2 -AzureVmId $vmId `
-Name "a2aprotectedItem" -RecoveryVmName "vmName" -ProtectionContainerMapping $pcmMapping -RecoveryResourceGroupId $recoveryResourceGroup
```

<span data-ttu-id="d8b2a-120">Запускает операцию создания защищенного элемента репликации для указанного защищенного элемента ASR и возвращает задание ASR, используемое для отслеживания операции (в сценарии Azure to Azure).</span><span class="sxs-lookup"><span data-stu-id="d8b2a-120">Starts the replication protected item creation operation for the specified ASR protectable item and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

### <span data-ttu-id="d8b2a-121">Пример 4</span><span class="sxs-lookup"><span data-stu-id="d8b2a-121">Example 4</span></span>
```
PS C:\> $disk1 = new-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri1 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $disk2 = new-AzureToAzureDiskReplicationConfiguration -vhdUri  $diskUri2 -RecoveryAzureStorageAccountId $recoveryAzureStorageAccountId `
-LogStorageAccountId $logStorageAccountId  
PS C:\> $enableDRjob = New-AzureRmRecoveryServicesAsrReplicationProtectedItem -AzureToAzure -AzureVmId $vmId -Name $rpiName `
-RecoveryCloudServiceId  $recoveryCloudServiceId -ProtectionContainerMapping $pcm -RecoveryResourceGroupId  $RecoveryResourceGroupId `
-AzureToAzureDiskReplicationConfiguration $disk1,$disk2
```

<span data-ttu-id="d8b2a-122">Запускает операцию создания защищенного элемента для репликации для указанного ИД VmId и возвращает задание ASR, используемое для отслеживания операции (в сценарии Azure to Azure).</span><span class="sxs-lookup"><span data-stu-id="d8b2a-122">Starts the replication protected item creation operation for the specified VmId and returns the ASR job used to track the operation (Azure to Azure scenario).</span></span>

## <span data-ttu-id="d8b2a-123">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d8b2a-123">PARAMETERS</span></span>

### <span data-ttu-id="d8b2a-124">-Account (учетная запись)</span><span class="sxs-lookup"><span data-stu-id="d8b2a-124">-Account</span></span>
<span data-ttu-id="d8b2a-125">Учетная запись запуска от имени, которая будет использоваться для принудительной установки службы Mobility Service при необходимости.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-125">The run as account to be used to push install the Mobility service if needed.</span></span> <span data-ttu-id="d8b2a-126">Должен быть один из списка учетных записей запуска от имени в структуре ASR.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-126">Must be one from the list of run as accounts in the ASR fabric.</span></span>

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

### <span data-ttu-id="d8b2a-127">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="d8b2a-127">-AzureToAzure</span></span>
<span data-ttu-id="d8b2a-128">Параметр Switch, указывающий, что реплицированный элемент является виртуальной машиной Azure, которая реплицируется в регион восстановления Azure.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-128">Switch parameter to specify that the replicated item is an Azure virtual machine replicating to a recovery Azure region.</span></span>

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

### <span data-ttu-id="d8b2a-129">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="d8b2a-129">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="d8b2a-130">Указывает список реплицированных виртуальных машин и учетной записи хранилища кэша и хранилища для восстановления, которые будут использоваться для репликации диска.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-130">Specifies the list of virtual machine disks to replicated and the cache storage account and recovery storage account to be used to replicate the disk.</span></span>

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

### <span data-ttu-id="d8b2a-131">-AzureVmId</span><span class="sxs-lookup"><span data-stu-id="d8b2a-131">-AzureVmId</span></span>
<span data-ttu-id="d8b2a-132">Указывает ИД виртуальной машины Azure для репликации.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-132">Specifies the azure vm id to be replicated.</span></span>

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

### <span data-ttu-id="d8b2a-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8b2a-133">-DefaultProfile</span></span>
<span data-ttu-id="d8b2a-134">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8b2a-135">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="d8b2a-135">-HyperVToAzure</span></span>
<span data-ttu-id="d8b2a-136">Параметр Switch, указывающий, что реплицируемый элемент — это виртуальная машина Hyper-V, реплицируемая в Azure.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-136">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated to Azure.</span></span>

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

### <span data-ttu-id="d8b2a-137">-IncludeDiskId</span><span class="sxs-lookup"><span data-stu-id="d8b2a-137">-IncludeDiskId</span></span>
<span data-ttu-id="d8b2a-138">Список дисков, которые нужно включить в репликацию.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-138">The list of disks to include for replication.</span></span> <span data-ttu-id="d8b2a-139">По умолчанию включаются все диски.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-139">By default all disks are included.</span></span>

```yaml
Type: System.String[]
Parameter Sets: VMwareToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8b2a-140">-LogStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="d8b2a-140">-LogStorageAccountId</span></span>
<span data-ttu-id="d8b2a-141">Указывает идентификатор журнала или учетной записи для хранения кэша, который будет использоваться для хранения журналов репликации.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-141">Specifies the log or cache storage account Id to be used to store replication logs.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, HyperVSiteToAzure
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

### <span data-ttu-id="d8b2a-142">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d8b2a-142">-Name</span></span>
<span data-ttu-id="d8b2a-143">Задает имя для элемента, защищенного репликацией ASR.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-143">Specifies a name for the ASR replication protected item.</span></span> <span data-ttu-id="d8b2a-144">Имя должно быть уникальным в пределах хранилища.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-144">The name must be unique within the vault.</span></span>

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

### <span data-ttu-id="d8b2a-145">-OS</span><span class="sxs-lookup"><span data-stu-id="d8b2a-145">-OS</span></span>
<span data-ttu-id="d8b2a-146">Указывает семейство операционной системы.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-146">Specifies the operating system family.</span></span>
<span data-ttu-id="d8b2a-147">Допустимые значения этого параметра: Windows или Linux.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-147">The acceptable values for this parameter are: Windows or Linux.</span></span>

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

### <span data-ttu-id="d8b2a-148">-OSDiskName</span><span class="sxs-lookup"><span data-stu-id="d8b2a-148">-OSDiskName</span></span>
<span data-ttu-id="d8b2a-149">Указывает имя диска операционной системы.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-149">Specifies the name of the operating system disk.</span></span>

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

### <span data-ttu-id="d8b2a-150">-ProcessServer</span><span class="sxs-lookup"><span data-stu-id="d8b2a-150">-ProcessServer</span></span>
<span data-ttu-id="d8b2a-151">Сервер обработки, который будет использоваться для репликации этого компьютера.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-151">The Process Server to use to replicate this machine.</span></span> <span data-ttu-id="d8b2a-152">С помощью списка серверов обработки в структуре ASR, соответствующей серверу конфигурации, укажите один из них.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-152">Use the list of process servers in the ASR fabric corresponding to the Configuration server to specify one.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProcessServer
Parameter Sets: VMwareToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8b2a-153">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="d8b2a-153">-ProtectableItem</span></span>
<span data-ttu-id="d8b2a-154">Указывает объект защищенного элемента ASR, для которого включена репликация.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-154">Specifies the ASR protectable item object for which replication is being enabled.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem
Parameter Sets: EnterpriseToEnterprise, VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8b2a-155">-ProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="d8b2a-155">-ProtectionContainerMapping</span></span>
<span data-ttu-id="d8b2a-156">Указывает объект сопоставления контейнера защиты ASR, соответствующий политике репликации, которая должна использоваться для репликации.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-156">Specifies the ASR protection container mapping object corresponding to the replication policy to be used for replication.</span></span>

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

### <span data-ttu-id="d8b2a-157">-RecoveryAvailabilitySetId</span><span class="sxs-lookup"><span data-stu-id="d8b2a-157">-RecoveryAvailabilitySetId</span></span>
<span data-ttu-id="d8b2a-158">Идентификатор набора доступности для восстановления компьютера в случае отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-158">The ID of the AvailabilitySet to recover the machine to in the event of a failover.</span></span>

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

### <span data-ttu-id="d8b2a-159">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="d8b2a-159">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="d8b2a-160">ИДЕНТИФИКАТОР виртуальной сети Azure для восстановления компьютера в случае отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-160">The ID of the Azure virtual network to recover the machine to in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8b2a-161">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="d8b2a-161">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="d8b2a-162">Указывает идентификатор учетной записи хранения Azure, на которую должна выполняться репликация.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-162">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure
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

### <span data-ttu-id="d8b2a-163">-RecoveryAzureSubnetName</span><span class="sxs-lookup"><span data-stu-id="d8b2a-163">-RecoveryAzureSubnetName</span></span>
<span data-ttu-id="d8b2a-164">Подсеть в виртуальной сети восстановления Azure, к которой следует прикрепить сбой виртуальной машины в случае отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-164">The subnet within the recovery Azure virtual network to which the failed over virtual machine should be attached in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, HyperVSiteToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8b2a-165">-RecoveryBootDiagStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="d8b2a-165">-RecoveryBootDiagStorageAccountId</span></span>
<span data-ttu-id="d8b2a-166">Указывает учетную запись хранения для диагностики загрузки для восстановления ВМ Azure.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-166">Specifies the storage account for boot diagnostics for recovery azure VM.</span></span>

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

### <span data-ttu-id="d8b2a-167">-RecoveryCloudServiceId</span><span class="sxs-lookup"><span data-stu-id="d8b2a-167">-RecoveryCloudServiceId</span></span>
<span data-ttu-id="d8b2a-168">Указывает идентификатор ресурса облачной службы восстановления, на которую следует отработка отказа виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-168">Specifies the resource ID of the recovery cloud service to failover this virtual machine to.</span></span>

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

### <span data-ttu-id="d8b2a-169">-RecoveryResourceGroupId</span><span class="sxs-lookup"><span data-stu-id="d8b2a-169">-RecoveryResourceGroupId</span></span>
<span data-ttu-id="d8b2a-170">Указывает идентификатор ARM для группы ресурсов, в которой виртуальная машина будет создана в случае отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-170">Specifies the ARM identifier of the resource group in which the virtual machine will be created in the event of a failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8b2a-171">-RecoveryVmName</span><span class="sxs-lookup"><span data-stu-id="d8b2a-171">-RecoveryVmName</span></span>
<span data-ttu-id="d8b2a-172">Имя виртуальной машины восстановления, созданной после перехода на другой ресурс.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-172">Name of the recovery Vm created after failover.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, EnterpriseToAzure, HyperVSiteToAzure, AzureToAzure, AzureToAzureWithoutDiskDetails
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8b2a-173">-ReplicationGroupName</span><span class="sxs-lookup"><span data-stu-id="d8b2a-173">-ReplicationGroupName</span></span>
<span data-ttu-id="d8b2a-174">Указывает имя группы репликации, которое будет использоваться для создания точек восстановления с несколькими виртуальными машинами.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-174">Specifies the replication group name to use to create multi-VM consistent recovery points.</span></span> <span data-ttu-id="d8b2a-175">По умолчанию каждый элемент, защищенный репликацией, создается в группе собственной и постоянной точки восстановления из-за множественной виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-175">By default each replication protected item is created in a group of its own and multi-VM consistent recovery points are not generated.</span></span> <span data-ttu-id="d8b2a-176">Используйте этот параметр только в том случае, если вам нужно создать точки восстановления с несколькими виртуальными машинами в группе компьютеров, защищая все компьютеры к одной группе репликации.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-176">Use this option only if you need to create multi-VM consistent recovery points across a group of machines by protecting all machines to the same replication group.</span></span> 

```yaml
Type: System.String
Parameter Sets: VMwareToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8b2a-177">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="d8b2a-177">-VmmToVmm</span></span>
<span data-ttu-id="d8b2a-178">Параметр Switch, указывающий, что реплицируемый элемент — это виртуальная машина Hyper-V, реплицируемая между сайтами Hyper-V, управляемыми VMM.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-178">Switch parameter to specify the replicated item is a Hyper-V virtual machine that is being replicated between VMM managed Hyper-V sites.</span></span>

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

### <span data-ttu-id="d8b2a-179">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="d8b2a-179">-VMwareToAzure</span></span>
<span data-ttu-id="d8b2a-180">Параметр Switch, указывающий, что реплицированный элемент является виртуальной машиной VMware или физическим сервером, который будет реплицирован в Azure.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-180">Switch parameter to specify the replicated item is a VMware virtual machine or physical server that will be replicate to Azure.</span></span>

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

### <span data-ttu-id="d8b2a-181">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="d8b2a-181">-WaitForCompletion</span></span>
<span data-ttu-id="d8b2a-182">Указывает, что перед возвратом командлет должен дождаться завершения операции.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-182">Specifies that the cmdlet should wait for completion of the operation before returning.</span></span>

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

### <span data-ttu-id="d8b2a-183">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d8b2a-183">-Confirm</span></span>
<span data-ttu-id="d8b2a-184">Запрашивает подтверждение перед запуском операции.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-184">Prompts  for confirmation before starting the operation.</span></span>

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

### <span data-ttu-id="d8b2a-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8b2a-185">-WhatIf</span></span>
<span data-ttu-id="d8b2a-186">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-186">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8b2a-187">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-187">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8b2a-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8b2a-188">CommonParameters</span></span>
<span data-ttu-id="d8b2a-189">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d8b2a-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8b2a-190">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8b2a-190">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8b2a-191">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d8b2a-191">INPUTS</span></span>

### <span data-ttu-id="d8b2a-192">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="d8b2a-192">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectableItem</span></span>

## <span data-ttu-id="d8b2a-193">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8b2a-193">OUTPUTS</span></span>

### <span data-ttu-id="d8b2a-194">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="d8b2a-194">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d8b2a-195">Пуск</span><span class="sxs-lookup"><span data-stu-id="d8b2a-195">NOTES</span></span>

## <span data-ttu-id="d8b2a-196">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d8b2a-196">RELATED LINKS</span></span>

[<span data-ttu-id="d8b2a-197">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d8b2a-197">Get-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Get-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="d8b2a-198">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d8b2a-198">Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Remove-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)

[<span data-ttu-id="d8b2a-199">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d8b2a-199">Set-AzureRmRecoveryServicesAsrReplicationProtectedItem</span></span>](./Set-AzureRmRecoveryServicesAsrReplicationProtectedItem.md)
