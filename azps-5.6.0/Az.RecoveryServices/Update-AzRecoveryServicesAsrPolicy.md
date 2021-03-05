---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/update-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 2255a2397c7096ec1a7b5f45dc4fa699649b071a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005816"
---
# <span data-ttu-id="6f41e-101">Update-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="6f41e-101">Update-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="6f41e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f41e-102">SYNOPSIS</span></span>
<span data-ttu-id="6f41e-103">Обновляет политику репликации сайтов Azure.</span><span class="sxs-lookup"><span data-stu-id="6f41e-103">Updates an Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="6f41e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6f41e-104">SYNTAX</span></span>

### <span data-ttu-id="6f41e-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6f41e-105">Default (Default)</span></span>
```
Update-AzRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-RecoveryAzureStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6f41e-106">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="6f41e-106">VMwareToAzure</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-VMwareToAzure] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-RPOWarningThresholdInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f41e-107">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="6f41e-107">AzureToAzure</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-AzureToAzure] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6f41e-108">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="6f41e-108">AzureToVMware</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-AzureToVMware] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-RPOWarningThresholdInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f41e-109">HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="6f41e-109">HyperVToAzure</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-HyperVToAzure] -InputObject <ASRPolicy>
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6f41e-110">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="6f41e-110">EnterpriseToEnterprise</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-VmmToVmm] -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f41e-111">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f41e-111">DESCRIPTION</span></span>
<span data-ttu-id="6f41e-112">Для **обновления-AzRecoveryServicesAsrPolicy** обновляется указанная политика репликации сайтов Azure.</span><span class="sxs-lookup"><span data-stu-id="6f41e-112">The **Update-AzRecoveryServicesAsrPolicy** cmdlet updates the specified Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="6f41e-113">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6f41e-113">EXAMPLES</span></span>

### <span data-ttu-id="6f41e-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6f41e-114">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrPolicy -Policy $Policy -ReplicationFrequencyInSeconds 900
```

<span data-ttu-id="6f41e-115">Запускает операцию репликации обновления с использованием указанных параметров и возвращает задание ASR, используемую для ее отслеживания.</span><span class="sxs-lookup"><span data-stu-id="6f41e-115">Starts the update replication policy operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="6f41e-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="6f41e-116">Example 2</span></span>
```
PS C:\> Update-AzRecoveryServicesAsrPolicy -AzureToAzure -InputObject $Policy -ReplicationFrequencyInSeconds 900
```

<span data-ttu-id="6f41e-117">Запускает операцию обновления azure до политики репликации Azure с использованием указанных параметров и возвращает задание ASR, используемую для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="6f41e-117">Starts the update azure to azure replication policy operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="6f41e-118">Пример 3</span><span class="sxs-lookup"><span data-stu-id="6f41e-118">Example 3</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrPolicy -AzureToAzure -InputObject $Policy -RecoveryPointRetentionInHours 20
```

<span data-ttu-id="6f41e-119">Запускает обновление Azure до политики репликации Azure с использованием указанных параметров и возвращает задание ASR, используемую для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="6f41e-119">Starts the update azure to azure replication policy using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="6f41e-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6f41e-120">PARAMETERS</span></span>

### <span data-ttu-id="6f41e-121">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="6f41e-121">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="6f41e-122">Определяет частоту (в часах), для которой нужно создать согласованные точки восстановления приложения.</span><span class="sxs-lookup"><span data-stu-id="6f41e-122">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

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

### <span data-ttu-id="6f41e-123">-Проверка подлинности</span><span class="sxs-lookup"><span data-stu-id="6f41e-123">-Authentication</span></span>
<span data-ttu-id="6f41e-124">Определяет тип используемой проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="6f41e-124">Specifies the type of authentication used.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Certificate, Kerberos

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f41e-125">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="6f41e-125">-AzureToAzure</span></span>
<span data-ttu-id="6f41e-126">Указывает аварийное восстановление из Azure в Azure.</span><span class="sxs-lookup"><span data-stu-id="6f41e-126">Specifies the Azure to Azure disaster recovery.</span></span>

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

### <span data-ttu-id="6f41e-127">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="6f41e-127">-AzureToVMware</span></span>
<span data-ttu-id="6f41e-128">Указывает аварийное восстановление в Azure для vMWare.</span><span class="sxs-lookup"><span data-stu-id="6f41e-128">Specifies the Azure to vMWare disaster recovery.</span></span>

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

### <span data-ttu-id="6f41e-129">-Compression</span><span class="sxs-lookup"><span data-stu-id="6f41e-129">-Compression</span></span>
<span data-ttu-id="6f41e-130">Указывает, должно ли быть включено сжатие.</span><span class="sxs-lookup"><span data-stu-id="6f41e-130">Specifies if compression should be enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f41e-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f41e-131">-DefaultProfile</span></span>
<span data-ttu-id="6f41e-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6f41e-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="6f41e-133">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="6f41e-133">-HyperVToAzure</span></span>
<span data-ttu-id="6f41e-134">Параметр переключения, указывающий, что указанная политика используется для Hyper-V виртуальных машин в Azure.</span><span class="sxs-lookup"><span data-stu-id="6f41e-134">Switch parameter indicating that the specified policy is used to replicate Hyper-V virtual machines to Azure.</span></span>

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

### <span data-ttu-id="6f41e-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6f41e-135">-InputObject</span></span>
<span data-ttu-id="6f41e-136">Объект ввода для cmdlet: определяет объект политики репликации ASR, соответствующий обновляемой политике репликации.</span><span class="sxs-lookup"><span data-stu-id="6f41e-136">Input object for the cmdlet: Specifies the ASR replication policy object corresponding to the replication policy to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy
Parameter Sets: (All)
Aliases: Policy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6f41e-137">-MultiVmSyncStatus</span><span class="sxs-lookup"><span data-stu-id="6f41e-137">-MultiVmSyncStatus</span></span>
<span data-ttu-id="6f41e-138">Указывает состояние многомерной синхронизации для политики.</span><span class="sxs-lookup"><span data-stu-id="6f41e-138">Specifies multiVm sync status for the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: VMwareToAzure, AzureToAzure, AzureToVMware
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f41e-139">-NumberOfRecoveryPointsToRetain</span><span class="sxs-lookup"><span data-stu-id="6f41e-139">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="6f41e-140">Определяет количество точек восстановления, которые нужно сохранить.</span><span class="sxs-lookup"><span data-stu-id="6f41e-140">Specifies the number recovery points to retain.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Default, HyperVToAzure, EnterpriseToEnterprise
Aliases: RecoveryPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f41e-141">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="6f41e-141">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="6f41e-142">Определяет ИД учетной записи хранения Azure конечного адреса репликации.</span><span class="sxs-lookup"><span data-stu-id="6f41e-142">Specifies the Azure storage account ID of the replication target.</span></span> <span data-ttu-id="6f41e-143">Используется в качестве целевой учетной записи хранения для репликации, если альтернатива не предоставляется, при включая репликацию с помощью New-AzRecoveryServicesASRReplicationProtectedItem-New-AzRecoveryServicesASRReplicationProtectedItem.</span><span class="sxs-lookup"><span data-stu-id="6f41e-143">Used as the target storage account for replication if an alternate is not provided while enabling replication using the New-AzRecoveryServicesASRReplicationProtectedItem cmdlet.</span></span>


```yaml
Type: System.String
Parameter Sets: Default, HyperVToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f41e-144">-RecoveryPointRetentionInHours</span><span class="sxs-lookup"><span data-stu-id="6f41e-144">-RecoveryPointRetentionInHours</span></span>
<span data-ttu-id="6f41e-145">Время в часах для сохранения баллов восстановления после создания.</span><span class="sxs-lookup"><span data-stu-id="6f41e-145">Time in hours to retain recovery points after creation.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VMwareToAzure, AzureToAzure, AzureToVMware
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f41e-146">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="6f41e-146">-ReplicaDeletion</span></span>
<span data-ttu-id="6f41e-147">Указывает, следует ли удалять виртуальную машину при отключке репликации с управляемого VMM-сайта на другом.</span><span class="sxs-lookup"><span data-stu-id="6f41e-147">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Required, NotRequired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f41e-148">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="6f41e-148">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="6f41e-149">Определяет интервал частоты репликации в секундах.</span><span class="sxs-lookup"><span data-stu-id="6f41e-149">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="6f41e-150">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="6f41e-150">Valid values are:</span></span>

- <span data-ttu-id="6f41e-151">30</span><span class="sxs-lookup"><span data-stu-id="6f41e-151">30</span></span>
- <span data-ttu-id="6f41e-152">300</span><span class="sxs-lookup"><span data-stu-id="6f41e-152">300</span></span>
- <span data-ttu-id="6f41e-153">900</span><span class="sxs-lookup"><span data-stu-id="6f41e-153">900</span></span>

```yaml
Type: System.String
Parameter Sets: Default, HyperVToAzure, EnterpriseToEnterprise
Aliases:
Accepted values: 30, 300, 900

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f41e-154">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="6f41e-154">-ReplicationMethod</span></span>
<span data-ttu-id="6f41e-155">Определяет способ репликации.</span><span class="sxs-lookup"><span data-stu-id="6f41e-155">Specifies the replication method.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f41e-156">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="6f41e-156">-ReplicationPort</span></span>
<span data-ttu-id="6f41e-157">Порт, используемый для репликации.</span><span class="sxs-lookup"><span data-stu-id="6f41e-157">Specifies the port used for replication.</span></span>

```yaml
Type: System.UInt16
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f41e-158">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="6f41e-158">-ReplicationStartTime</span></span>
<span data-ttu-id="6f41e-159">Время начала репликации.</span><span class="sxs-lookup"><span data-stu-id="6f41e-159">Specifies the replication start time.</span></span>
<span data-ttu-id="6f41e-160">Оно должно быть не позднее чем через 24 часа с начала задания.</span><span class="sxs-lookup"><span data-stu-id="6f41e-160">It must be no later than 24-hours from the start of the job.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: Default, HyperVToAzure, EnterpriseToEnterprise
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f41e-161">-RPOWarningThresholdInMinutes</span><span class="sxs-lookup"><span data-stu-id="6f41e-161">-RPOWarningThresholdInMinutes</span></span>
<span data-ttu-id="6f41e-162">Пороговое значение RPO в минутах для предупреждения.</span><span class="sxs-lookup"><span data-stu-id="6f41e-162">The RPO threshold value in minutes to warn on.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VMwareToAzure, AzureToVMware
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f41e-163">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="6f41e-163">-VmmToVmm</span></span>
<span data-ttu-id="6f41e-164">Параметр переключения, указывающий, что указанная политика используется для репликации управляемых VMM Hyper-V виртуальных машин между Hyper-V сайтами.</span><span class="sxs-lookup"><span data-stu-id="6f41e-164">Switch parameter indicating that the specified policy is used to replicate VMM managed Hyper-V virtual machines between two Hyper-V sites.</span></span>

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

### <span data-ttu-id="6f41e-165">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="6f41e-165">-VMwareToAzure</span></span>
<span data-ttu-id="6f41e-166">Параметр переключения, указывающий, что указанная политика используется для репликации виртуальных машин VMware в Azure.</span><span class="sxs-lookup"><span data-stu-id="6f41e-166">Switch parameter indicating that the specified policy is used to replicate VMware virtual machines to Azure.</span></span>

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

### <span data-ttu-id="6f41e-167">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6f41e-167">-Confirm</span></span>
<span data-ttu-id="6f41e-168">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="6f41e-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f41e-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f41e-169">-WhatIf</span></span>
<span data-ttu-id="6f41e-170">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f41e-170">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6f41e-171">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6f41e-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f41e-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f41e-172">CommonParameters</span></span>
<span data-ttu-id="6f41e-173">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f41e-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f41e-174">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6f41e-174">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f41e-175">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6f41e-175">INPUTS</span></span>

### <span data-ttu-id="6f41e-176">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="6f41e-176">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="6f41e-177">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6f41e-177">OUTPUTS</span></span>

### <span data-ttu-id="6f41e-178">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="6f41e-178">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="6f41e-179">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6f41e-179">NOTES</span></span>

## <span data-ttu-id="6f41e-180">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6f41e-180">RELATED LINKS</span></span>
