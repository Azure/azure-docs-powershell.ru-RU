---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: d120054a7eef5afd27101d84911a1a57a0b4819a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506797"
---
# <span data-ttu-id="68a14-101">New-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="68a14-101">New-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="68a14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68a14-102">SYNOPSIS</span></span>
<span data-ttu-id="68a14-103">Создает политику репликации сайтов Azure.</span><span class="sxs-lookup"><span data-stu-id="68a14-103">Creates an Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="68a14-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="68a14-104">SYNTAX</span></span>

### <span data-ttu-id="68a14-105">HyperVToAzure (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="68a14-105">HyperVToAzure (Default)</span></span>
```
New-AzRecoveryServicesAsrPolicy [-HyperVToAzure] -Name <String> -ReplicationProvider <String>
 -ReplicationFrequencyInSeconds <String> [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="68a14-106">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="68a14-106">VMwareToAzure</span></span>
```
New-AzRecoveryServicesAsrPolicy [-VMwareToAzure] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 -RPOWarningThresholdInMinutes <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="68a14-107">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="68a14-107">AzureToVMware</span></span>
```
New-AzRecoveryServicesAsrPolicy [-AzureToVMware] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 -RPOWarningThresholdInMinutes <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="68a14-108">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="68a14-108">AzureToAzure</span></span>
```
New-AzRecoveryServicesAsrPolicy [-AzureToAzure] -Name <String> -RecoveryPointRetentionInHours <Int32>
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-MultiVmSyncStatus <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68a14-109">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="68a14-109">EnterpriseToEnterprise</span></span>
```
New-AzRecoveryServicesAsrPolicy [-VmmToVmm] -Name <String> -ReplicationProvider <String>
 [-ReplicationMethod <String>] -ReplicationFrequencyInSeconds <String>
 [-NumberOfRecoveryPointsToRetain <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-Compression <String>] -ReplicationPort <UInt16> [-Authentication <String>]
 [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68a14-110">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="68a14-110">DESCRIPTION</span></span>
<span data-ttu-id="68a14-111">Для создания политики репликации сайтов **Azure создается cmdlet New-AzRecoveryServicesAsrPolicy.**</span><span class="sxs-lookup"><span data-stu-id="68a14-111">The **New-AzRecoveryServicesAsrPolicy** cmdlet creates an Azure Site Recovery replication policy.</span></span>
<span data-ttu-id="68a14-112">Политика репликации используется для настройки параметров репликации, таких как частота репликации и количество точек восстановления.</span><span class="sxs-lookup"><span data-stu-id="68a14-112">The replication policy is used to specify replication settings such as the replication frequency and number of recovery points.</span></span>

## <span data-ttu-id="68a14-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="68a14-113">EXAMPLES</span></span>

### <span data-ttu-id="68a14-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="68a14-114">Example 1</span></span>
```
PS C:\> New-AzRecoveryServicesAsrPolicy -Name "abc" -ReplicationProvider HyperVReplicaAzure -ReplicationFrequencyInSeconds 30 -NumberOfRecoveryPointsToRetain 10
```

<span data-ttu-id="68a14-115">Запускает операцию создания политики репликации с использованием указанных параметров и возвращает задание ASR, используемую для ее отслеживания.</span><span class="sxs-lookup"><span data-stu-id="68a14-115">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="68a14-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="68a14-116">Example 2</span></span>
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

<span data-ttu-id="68a14-117">Запускает операцию создания политики репликации с использованием указанных параметров и возвращает задание ASR, используемую для ее отслеживания.</span><span class="sxs-lookup"><span data-stu-id="68a14-117">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="68a14-118">Пример 3</span><span class="sxs-lookup"><span data-stu-id="68a14-118">Example 3</span></span>
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

### <span data-ttu-id="68a14-119">Пример 4</span><span class="sxs-lookup"><span data-stu-id="68a14-119">Example 4</span></span>
```
PS C:\>  $Job = New-AzRecoveryServicesAsrPolicy -Name $TestPolicy1 -AzureToAzure -RecoveryPointRetentionInHours 10  -ApplicationConsistentSnapshotFrequencyInHours 5 
PS C:\>  Get-AsrJob -name $Job.id
```

<span data-ttu-id="68a14-120">Запускает операцию создания политики репликации с использованием указанных параметров и возвращает задание ASR, используемую для ее отслеживания.</span><span class="sxs-lookup"><span data-stu-id="68a14-120">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="68a14-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="68a14-121">PARAMETERS</span></span>

### <span data-ttu-id="68a14-122">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="68a14-122">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="68a14-123">Определяет частоту (в часах) для создания согласованных точек восстановления приложения.</span><span class="sxs-lookup"><span data-stu-id="68a14-123">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

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

### <span data-ttu-id="68a14-124">-Проверка подлинности</span><span class="sxs-lookup"><span data-stu-id="68a14-124">-Authentication</span></span>
<span data-ttu-id="68a14-125">Определяет тип используемой проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="68a14-125">Specifies the type of authentication used.</span></span>
<span data-ttu-id="68a14-126">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="68a14-126">Valid values are:</span></span>

- <span data-ttu-id="68a14-127">Сертификат</span><span class="sxs-lookup"><span data-stu-id="68a14-127">Certificate</span></span>
-  <span data-ttu-id="68a14-128">Kerberos</span><span class="sxs-lookup"><span data-stu-id="68a14-128">Kerberos</span></span>

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

### <span data-ttu-id="68a14-129">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="68a14-129">-AzureToAzure</span></span>
<span data-ttu-id="68a14-130">Параметр переключения определяет сценарий создания политики Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="68a14-130">Switch parameter specifies the scenario for azure to azure policy creation.</span></span>

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

### <span data-ttu-id="68a14-131">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="68a14-131">-AzureToVMware</span></span>
<span data-ttu-id="68a14-132">Параметр переключения определяет сценарий создания политики Azure в vMWare.</span><span class="sxs-lookup"><span data-stu-id="68a14-132">Switch parameter specifies the scenario for azure to vMWare policy creation.</span></span>

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

### <span data-ttu-id="68a14-133">-Сжатие</span><span class="sxs-lookup"><span data-stu-id="68a14-133">-Compression</span></span>
<span data-ttu-id="68a14-134">Указывает, должно ли быть включено сжатие.</span><span class="sxs-lookup"><span data-stu-id="68a14-134">Specifies if compression should be enabled.</span></span>

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

### <span data-ttu-id="68a14-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68a14-135">-DefaultProfile</span></span>
<span data-ttu-id="68a14-136">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="68a14-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="68a14-137">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="68a14-137">-HyperVToAzure</span></span>
<span data-ttu-id="68a14-138">Параметр переключения для указания политики будет использоваться для репликации виртуальных машин Hyper-V в Azure</span><span class="sxs-lookup"><span data-stu-id="68a14-138">Switch parameter to specify policy is to be used to replicate Hyper-V virtual machines to Azure</span></span>

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

### <span data-ttu-id="68a14-139">-MultiVmSyncStatus</span><span class="sxs-lookup"><span data-stu-id="68a14-139">-MultiVmSyncStatus</span></span>
<span data-ttu-id="68a14-140">Указывает состояние многомерной синхронизации для политики.</span><span class="sxs-lookup"><span data-stu-id="68a14-140">Specifies multiVm sync status for the policy.</span></span>

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

### <span data-ttu-id="68a14-141">-Name</span><span class="sxs-lookup"><span data-stu-id="68a14-141">-Name</span></span>
<span data-ttu-id="68a14-142">Указывает имя политики репликации ASR.</span><span class="sxs-lookup"><span data-stu-id="68a14-142">Specifies the name of the ASR replication policy.</span></span>

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

### <span data-ttu-id="68a14-143">-NumberOfRecoveryPointsToRetain</span><span class="sxs-lookup"><span data-stu-id="68a14-143">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="68a14-144">Определяет количество точек восстановления, которые нужно сохранить.</span><span class="sxs-lookup"><span data-stu-id="68a14-144">Specifies the number recovery points to retain.</span></span>

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

### <span data-ttu-id="68a14-145">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="68a14-145">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="68a14-146">Определяет ИД учетной записи хранения Azure, к которая будет реплицироваться.</span><span class="sxs-lookup"><span data-stu-id="68a14-146">Specifies the ID of the Azure storage account to replicate to.</span></span>

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

### <span data-ttu-id="68a14-147">-RecoveryPointRetentionInHours</span><span class="sxs-lookup"><span data-stu-id="68a14-147">-RecoveryPointRetentionInHours</span></span>
<span data-ttu-id="68a14-148">Сохраните баллы восстановления за заданный период времени в часах.</span><span class="sxs-lookup"><span data-stu-id="68a14-148">Retain the recovery points for given time in hours.</span></span>

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

### <span data-ttu-id="68a14-149">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="68a14-149">-ReplicaDeletion</span></span>
<span data-ttu-id="68a14-150">Указывает, следует ли удалять виртуальную машину при отключке репликации с управляемого VMM-сайта на другом.</span><span class="sxs-lookup"><span data-stu-id="68a14-150">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

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

### <span data-ttu-id="68a14-151">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="68a14-151">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="68a14-152">Определяет интервал частоты репликации в секундах.</span><span class="sxs-lookup"><span data-stu-id="68a14-152">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="68a14-153">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="68a14-153">Valid values are:</span></span>

- <span data-ttu-id="68a14-154">30</span><span class="sxs-lookup"><span data-stu-id="68a14-154">30</span></span>
- <span data-ttu-id="68a14-155">300</span><span class="sxs-lookup"><span data-stu-id="68a14-155">300</span></span>
- <span data-ttu-id="68a14-156">900</span><span class="sxs-lookup"><span data-stu-id="68a14-156">900</span></span>

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

### <span data-ttu-id="68a14-157">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="68a14-157">-ReplicationMethod</span></span>
<span data-ttu-id="68a14-158">Определяет способ репликации.</span><span class="sxs-lookup"><span data-stu-id="68a14-158">Specifies the replication method.</span></span>
<span data-ttu-id="68a14-159">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="68a14-159">Valid values are:</span></span>

- <span data-ttu-id="68a14-160">Онлайн</span><span class="sxs-lookup"><span data-stu-id="68a14-160">Online</span></span>
- <span data-ttu-id="68a14-161">Автономный режим</span><span class="sxs-lookup"><span data-stu-id="68a14-161">Offline</span></span>

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

### <span data-ttu-id="68a14-162">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="68a14-162">-ReplicationPort</span></span>
<span data-ttu-id="68a14-163">Порт, используемый для репликации.</span><span class="sxs-lookup"><span data-stu-id="68a14-163">Specifies the port used for replication.</span></span>

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

### <span data-ttu-id="68a14-164">-ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="68a14-164">-ReplicationProvider</span></span>
<span data-ttu-id="68a14-165">Указывает поставщика репликации для политики.</span><span class="sxs-lookup"><span data-stu-id="68a14-165">Specifies the replication provider for the policy.</span></span>

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

### <span data-ttu-id="68a14-166">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="68a14-166">-ReplicationStartTime</span></span>
<span data-ttu-id="68a14-167">Время начала репликации.</span><span class="sxs-lookup"><span data-stu-id="68a14-167">Specifies the replication start time.</span></span>
<span data-ttu-id="68a14-168">Оно должно быть не позднее чем через 24 часа с начала задания.</span><span class="sxs-lookup"><span data-stu-id="68a14-168">It must be no later than 24-hours from the start of the job.</span></span>

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

### <span data-ttu-id="68a14-169">-RPOWarningThresholdInMinutes</span><span class="sxs-lookup"><span data-stu-id="68a14-169">-RPOWarningThresholdInMinutes</span></span>
<span data-ttu-id="68a14-170">Пороговое значение RPO в минутах для предупреждения.</span><span class="sxs-lookup"><span data-stu-id="68a14-170">The RPO threshold value in minutes to warn on.</span></span>

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

### <span data-ttu-id="68a14-171">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="68a14-171">-VmmToVmm</span></span>
<span data-ttu-id="68a14-172">Параметр переключения для указания политики будет использоваться для репликации между сайтами Hyper-V, управляемыми VMM-сервером.</span><span class="sxs-lookup"><span data-stu-id="68a14-172">Switch parameter to specify policy is to be used to replicate between Hyper-V sites managed by a VMM server.</span></span>

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

### <span data-ttu-id="68a14-173">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="68a14-173">-VMwareToAzure</span></span>
<span data-ttu-id="68a14-174">Параметр переключения, определяющий, что создаемая политика репликации будет использоваться для репликации виртуальных машин VMware и физических серверов в Azure.</span><span class="sxs-lookup"><span data-stu-id="68a14-174">Switch parameter specifying that the replication policy being created will be used to replicate VMware virtual machines and/or Physical servers to Azure.</span></span>

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

### <span data-ttu-id="68a14-175">-Confirm</span><span class="sxs-lookup"><span data-stu-id="68a14-175">-Confirm</span></span>
<span data-ttu-id="68a14-176">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68a14-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68a14-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68a14-177">-WhatIf</span></span>
<span data-ttu-id="68a14-178">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68a14-178">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="68a14-179">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="68a14-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68a14-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68a14-180">CommonParameters</span></span>
<span data-ttu-id="68a14-181">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68a14-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68a14-182">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="68a14-182">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68a14-183">INPUTS</span><span class="sxs-lookup"><span data-stu-id="68a14-183">INPUTS</span></span>

### <span data-ttu-id="68a14-184">Нет</span><span class="sxs-lookup"><span data-stu-id="68a14-184">None</span></span>

## <span data-ttu-id="68a14-185">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="68a14-185">OUTPUTS</span></span>

### <span data-ttu-id="68a14-186">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="68a14-186">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="68a14-187">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="68a14-187">NOTES</span></span>

## <span data-ttu-id="68a14-188">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="68a14-188">RELATED LINKS</span></span>

[<span data-ttu-id="68a14-189">Get-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="68a14-189">Get-AzRecoveryServicesAsrPolicy</span></span>](./Get-AzRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="68a14-190">Remove-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="68a14-190">Remove-AzRecoveryServicesAsrPolicy</span></span>](./Remove-AzRecoveryServicesAsrPolicy.md)
