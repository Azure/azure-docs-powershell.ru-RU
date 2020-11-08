---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: d120054a7eef5afd27101d84911a1a57a0b4819a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94242719"
---
# <span data-ttu-id="2ba0e-101">New-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="2ba0e-101">New-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="2ba0e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2ba0e-102">SYNOPSIS</span></span>
<span data-ttu-id="2ba0e-103">Создание политики репликации восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="2ba0e-103">Creates an Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="2ba0e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2ba0e-104">SYNTAX</span></span>

### <span data-ttu-id="2ba0e-105">HyperVToAzure (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2ba0e-105">HyperVToAzure (Default)</span></span>
```
New-AzRecoveryServicesAsrPolicy [-HyperVToAzure] -Name <String> -ReplicationProvider <String>
 -ReplicationFrequencyInSeconds <String> [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2ba0e-106">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="2ba0e-106">VMwareToAzure</span></span>
```
New-AzRecoveryServicesAsrPolicy [-VMwareToAzure] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 -RPOWarningThresholdInMinutes <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2ba0e-107">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="2ba0e-107">AzureToVMware</span></span>
```
New-AzRecoveryServicesAsrPolicy [-AzureToVMware] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 -RPOWarningThresholdInMinutes <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2ba0e-108">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="2ba0e-108">AzureToAzure</span></span>
```
New-AzRecoveryServicesAsrPolicy [-AzureToAzure] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2ba0e-109">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="2ba0e-109">EnterpriseToEnterprise</span></span>
```
New-AzRecoveryServicesAsrPolicy [-VmmToVmm] -Name <String> -ReplicationProvider <String>
 [-ReplicationMethod <String>] -ReplicationFrequencyInSeconds <String>
 [-NumberOfRecoveryPointsToRetain <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-Compression <String>] -ReplicationPort <UInt16> [-Authentication <String>]
 [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ba0e-110">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2ba0e-110">DESCRIPTION</span></span>
<span data-ttu-id="2ba0e-111">Командлет **New-AzRecoveryServicesAsrPolicy** создает политику репликации восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="2ba0e-111">The **New-AzRecoveryServicesAsrPolicy** cmdlet creates an Azure Site Recovery replication policy.</span></span>
<span data-ttu-id="2ba0e-112">Политика репликации используется для указания параметров репликации, таких как частота репликации и количество точек восстановления.</span><span class="sxs-lookup"><span data-stu-id="2ba0e-112">The replication policy is used to specify replication settings such as the replication frequency and number of recovery points.</span></span>

## <span data-ttu-id="2ba0e-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2ba0e-113">EXAMPLES</span></span>

### <span data-ttu-id="2ba0e-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="2ba0e-114">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrPolicy -Name "abc" -ReplicationProvider HyperVReplicaAzure -ReplicationFrequencyInSeconds 30 -NumberOfRecoveryPointsToRetain 10
```

<span data-ttu-id="2ba0e-115">Запускает операцию создания политики репликации с указанными параметрами и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="2ba0e-115">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="2ba0e-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="2ba0e-116">Example 2</span></span>
```
PS C:\> New-AzRecoveryServicesAsrPolicy -Name "abc122" -ReplicationProvider HyperVReplica2012R2 -ReplicationFrequencyInSeconds 300 -ReplicationPort 211

Name             : 1c609a5b-324e-461c-866f-ad58f944df25
ID               : /Subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationJobs/1c609a5b-324e-461c-866f-ad58f944df25
Type             :
JobType          : AddProtectionProfile
DisplayName      : Create replication policy
ClientRequestId  : b10c83ee-fee2-42d4-ad1d-dfc3e166faab ActivityId: 67e8453c-fae0-465f-801c-dfa2e6e6ee23
State            : Succeeded
StateDescription : Completed
StartTime        : 8/29/2017 10:18:10 AM
EndTime          : 8/29/2017 10:18:11 AM
TargetObjectId   : bb8e8c57-221d-5668-9d82-b15a3e19a6a3
TargetObjectType : ProtectionProfile
TargetObjectName : abc122
AllowedActions   :
Tasks            : {Prerequisites check for creating the replication policy, Creating the replication policy}
Errors           : {}
```

<span data-ttu-id="2ba0e-117">Запускает операцию создания политики репликации с указанными параметрами и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="2ba0e-117">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="2ba0e-118">Пример 3</span><span class="sxs-lookup"><span data-stu-id="2ba0e-118">Example 3</span></span>
```
PS C:\> New-AzRecoveryServicesAsrPolicy -Name $policyName1 -ReplicationProvider InMageAzureV2 -RecoveryPoints 40  -RPOWarningThresholdInMinutes 5 -ApplicationConsistentSnapshotFrequencyInMinutes 15
Name             : ed69e451-878b-4f19-9c0f-73184be05eaf
ID               : /Subscriptions/xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxx/replicationJobs/ed69e451-878b-4f19-9c0f-73184be05eaf
Type             :
JobType          :
DisplayName      :
ClientRequestId  : d8922fa2-303c-4eb4-b556-e07969ea6fba ActivityId: 9e946cdf-2351-44c2-9aef-70ef2eab29b4
State            : NotStarted
StateDescription : NotStarted
StartTime        :
EndTime          :
TargetObjectId   :
TargetObjectType :
TargetObjectName :
AllowedActions   :
Tasks            : {}
Errors           : {}
```

### <span data-ttu-id="2ba0e-119">Пример 4</span><span class="sxs-lookup"><span data-stu-id="2ba0e-119">Example 4</span></span>
```
PS C:\>  $Job = New-AzRecoveryServicesAsrPolicy -Name $TestPolicy1 -AzureToAzure -RecoveryPointRetentionInHours 10  -ApplicationConsistentSnapshotFrequencyInHours 5 
PS C:\>  Get-AsrJob -name $Job.id
```

<span data-ttu-id="2ba0e-120">Запускает операцию создания политики репликации с указанными параметрами и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="2ba0e-120">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="2ba0e-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2ba0e-121">PARAMETERS</span></span>

### <span data-ttu-id="2ba0e-122">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="2ba0e-122">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="2ba0e-123">Указывает частоту (в часах) для создания точек восстановления с одинаковым соответствием между приложениями.</span><span class="sxs-lookup"><span data-stu-id="2ba0e-123">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ba0e-124">-Проверка подлинности</span><span class="sxs-lookup"><span data-stu-id="2ba0e-124">-Authentication</span></span>
<span data-ttu-id="2ba0e-125">Указывает тип используемой проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="2ba0e-125">Specifies the type of authentication used.</span></span>
<span data-ttu-id="2ba0e-126">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="2ba0e-126">Valid values are:</span></span>

- <span data-ttu-id="2ba0e-127">См</span><span class="sxs-lookup"><span data-stu-id="2ba0e-127">Certificate</span></span>
-  <span data-ttu-id="2ba0e-128">Использованием</span><span class="sxs-lookup"><span data-stu-id="2ba0e-128">Kerberos</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases:
Accepted values: Certificate, Kerberos

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ba0e-129">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="2ba0e-129">-AzureToAzure</span></span>
<span data-ttu-id="2ba0e-130">Параметр Switch указывает сценарий для создания политики Azure для Azure.</span><span class="sxs-lookup"><span data-stu-id="2ba0e-130">Switch parameter specifies the scenario for azure to azure policy creation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ba0e-131">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="2ba0e-131">-AzureToVMware</span></span>
<span data-ttu-id="2ba0e-132">Параметр Switch указывает сценарий для создания политики Azure для vMWare.</span><span class="sxs-lookup"><span data-stu-id="2ba0e-132">Switch parameter specifies the scenario for azure to vMWare policy creation.</span></span>

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

### <span data-ttu-id="2ba0e-133">-Сжатие</span><span class="sxs-lookup"><span data-stu-id="2ba0e-133">-Compression</span></span>
<span data-ttu-id="2ba0e-134">Указывает, следует ли включить сжатие.</span><span class="sxs-lookup"><span data-stu-id="2ba0e-134">Specifies if compression should be enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ba0e-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ba0e-135">-DefaultProfile</span></span>
<span data-ttu-id="2ba0e-136">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2ba0e-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="2ba0e-137">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="2ba0e-137">-HyperVToAzure</span></span>
<span data-ttu-id="2ba0e-138">Параметр Switch для указания политики используется для репликации виртуальных машин Hyper-V в Azure.</span><span class="sxs-lookup"><span data-stu-id="2ba0e-138">Switch parameter to specify policy is to be used to replicate Hyper-V virtual machines to Azure</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: HyperVToAzure
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ba0e-139">-MultiVmSyncStatus</span><span class="sxs-lookup"><span data-stu-id="2ba0e-139">-MultiVmSyncStatus</span></span>
<span data-ttu-id="2ba0e-140">Задает состояние синхронизации multiVm для политики.</span><span class="sxs-lookup"><span data-stu-id="2ba0e-140">Specifies multiVm sync status for the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, AzureToVMware, AzureToAzure
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ba0e-141">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2ba0e-141">-Name</span></span>
<span data-ttu-id="2ba0e-142">Задает имя политики репликации ASR.</span><span class="sxs-lookup"><span data-stu-id="2ba0e-142">Specifies the name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="2ba0e-143">-NumberOfRecoveryPointsToRetain</span><span class="sxs-lookup"><span data-stu-id="2ba0e-143">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="2ba0e-144">Указывает число точек восстановления, которые нужно сохранить.</span><span class="sxs-lookup"><span data-stu-id="2ba0e-144">Specifies the number recovery points to retain.</span></span>

```yaml
Type: System.Int32
Parameter Sets: HyperVToAzure, EnterpriseToEnterprise
Aliases: RecoveryPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ba0e-145">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="2ba0e-145">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="2ba0e-146">Указывает идентификатор учетной записи хранения Azure, на которую должна выполняться репликация.</span><span class="sxs-lookup"><span data-stu-id="2ba0e-146">Specifies the ID of the Azure storage account to replicate to.</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ba0e-147">-RecoveryPointRetentionInHours</span><span class="sxs-lookup"><span data-stu-id="2ba0e-147">-RecoveryPointRetentionInHours</span></span>
<span data-ttu-id="2ba0e-148">Хранить точки восстановления на заданное время в часах.</span><span class="sxs-lookup"><span data-stu-id="2ba0e-148">Retain the recovery points for given time in hours.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VMwareToAzure, AzureToVMware, AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ba0e-149">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="2ba0e-149">-ReplicaDeletion</span></span>
<span data-ttu-id="2ba0e-150">Указывает, следует ли удалять виртуальную машину реплики при отключении репликации с сайта, управляемого VMM, в другой.</span><span class="sxs-lookup"><span data-stu-id="2ba0e-150">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases:
Accepted values: Required, NotRequired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ba0e-151">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="2ba0e-151">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="2ba0e-152">Указывает периодичность репликации (в секундах).</span><span class="sxs-lookup"><span data-stu-id="2ba0e-152">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="2ba0e-153">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="2ba0e-153">Valid values are:</span></span>

- <span data-ttu-id="2ba0e-154">30</span><span class="sxs-lookup"><span data-stu-id="2ba0e-154">30</span></span>
- <span data-ttu-id="2ba0e-155">300</span><span class="sxs-lookup"><span data-stu-id="2ba0e-155">300</span></span>
- <span data-ttu-id="2ba0e-156">900</span><span class="sxs-lookup"><span data-stu-id="2ba0e-156">900</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVToAzure, EnterpriseToEnterprise
Aliases:
Accepted values: 30, 300, 900

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ba0e-157">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="2ba0e-157">-ReplicationMethod</span></span>
<span data-ttu-id="2ba0e-158">Указывает метод репликации.</span><span class="sxs-lookup"><span data-stu-id="2ba0e-158">Specifies the replication method.</span></span>
<span data-ttu-id="2ba0e-159">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="2ba0e-159">Valid values are:</span></span>

- <span data-ttu-id="2ba0e-160">Онлайн</span><span class="sxs-lookup"><span data-stu-id="2ba0e-160">Online</span></span>
- <span data-ttu-id="2ba0e-161">Доступ</span><span class="sxs-lookup"><span data-stu-id="2ba0e-161">Offline</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToEnterprise
Aliases:
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ba0e-162">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="2ba0e-162">-ReplicationPort</span></span>
<span data-ttu-id="2ba0e-163">Указывает порт, используемый для репликации.</span><span class="sxs-lookup"><span data-stu-id="2ba0e-163">Specifies the port used for replication.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ba0e-164">-ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="2ba0e-164">-ReplicationProvider</span></span>
<span data-ttu-id="2ba0e-165">Указывает поставщика репликации для политики.</span><span class="sxs-lookup"><span data-stu-id="2ba0e-165">Specifies the replication provider for the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: HyperVToAzure, EnterpriseToEnterprise
Aliases:
Accepted values: HyperVReplica2012R2, HyperVReplica2012, HyperVReplicaAzure

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ba0e-166">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="2ba0e-166">-ReplicationStartTime</span></span>
<span data-ttu-id="2ba0e-167">Указывает время начала репликации.</span><span class="sxs-lookup"><span data-stu-id="2ba0e-167">Specifies the replication start time.</span></span>
<span data-ttu-id="2ba0e-168">Оно должно быть не позже, чем 24 часа, начиная с начала задания.</span><span class="sxs-lookup"><span data-stu-id="2ba0e-168">It must be no later than 24-hours from the start of the job.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: HyperVToAzure, EnterpriseToEnterprise
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ba0e-169">-RPOWarningThresholdInMinutes</span><span class="sxs-lookup"><span data-stu-id="2ba0e-169">-RPOWarningThresholdInMinutes</span></span>
<span data-ttu-id="2ba0e-170">Значение порога RPO (в минутах), на которое следует выдать предупреждение.</span><span class="sxs-lookup"><span data-stu-id="2ba0e-170">The RPO threshold value in minutes to warn on.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VMwareToAzure, AzureToVMware
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ba0e-171">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="2ba0e-171">-VmmToVmm</span></span>
<span data-ttu-id="2ba0e-172">Параметр Switch для указания политики используется для репликации между сайтами Hyper-V, управляемыми сервером VMM.</span><span class="sxs-lookup"><span data-stu-id="2ba0e-172">Switch parameter to specify policy is to be used to replicate between Hyper-V sites managed by a VMM server.</span></span>

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

### <span data-ttu-id="2ba0e-173">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="2ba0e-173">-VMwareToAzure</span></span>
<span data-ttu-id="2ba0e-174">Параметр Switch, указывающий на то, что создаваемая политика репликации будет использоваться для репликации виртуальных машин и (или) физических серверов VMware в Azure.</span><span class="sxs-lookup"><span data-stu-id="2ba0e-174">Switch parameter specifying that the replication policy being created will be used to replicate VMware virtual machines and/or Physical servers to Azure.</span></span>

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

### <span data-ttu-id="2ba0e-175">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2ba0e-175">-Confirm</span></span>
<span data-ttu-id="2ba0e-176">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2ba0e-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ba0e-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ba0e-177">-WhatIf</span></span>
<span data-ttu-id="2ba0e-178">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2ba0e-178">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2ba0e-179">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2ba0e-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ba0e-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ba0e-180">CommonParameters</span></span>
<span data-ttu-id="2ba0e-181">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2ba0e-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ba0e-182">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2ba0e-182">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ba0e-183">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2ba0e-183">INPUTS</span></span>

### <span data-ttu-id="2ba0e-184">Ничего</span><span class="sxs-lookup"><span data-stu-id="2ba0e-184">None</span></span>

## <span data-ttu-id="2ba0e-185">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2ba0e-185">OUTPUTS</span></span>

### <span data-ttu-id="2ba0e-186">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="2ba0e-186">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="2ba0e-187">Пуск</span><span class="sxs-lookup"><span data-stu-id="2ba0e-187">NOTES</span></span>

## <span data-ttu-id="2ba0e-188">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2ba0e-188">RELATED LINKS</span></span>

[<span data-ttu-id="2ba0e-189">Get-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="2ba0e-189">Get-AzRecoveryServicesAsrPolicy</span></span>](./Get-AzRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="2ba0e-190">Remove-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="2ba0e-190">Remove-AzRecoveryServicesAsrPolicy</span></span>](./Remove-AzRecoveryServicesAsrPolicy.md)
