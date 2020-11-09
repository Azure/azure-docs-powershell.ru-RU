---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 31b43930737627a3013f60a82c2ec30626b8518c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246840"
---
# <span data-ttu-id="96cb7-101">Update-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="96cb7-101">Update-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="96cb7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="96cb7-102">SYNOPSIS</span></span>
<span data-ttu-id="96cb7-103">Обновляет политику репликации восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="96cb7-103">Updates an Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="96cb7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="96cb7-104">SYNTAX</span></span>

### <span data-ttu-id="96cb7-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="96cb7-105">Default (Default)</span></span>
```
Update-AzRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-RecoveryAzureStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="96cb7-106">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="96cb7-106">VMwareToAzure</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-VMwareToAzure] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-RPOWarningThresholdInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96cb7-107">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="96cb7-107">AzureToAzure</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-AzureToAzure] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="96cb7-108">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="96cb7-108">AzureToVMware</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-AzureToVMware] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-RPOWarningThresholdInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96cb7-109">HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="96cb7-109">HyperVToAzure</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-HyperVToAzure] -InputObject <ASRPolicy>
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="96cb7-110">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="96cb7-110">EnterpriseToEnterprise</span></span>
```
Update-AzRecoveryServicesAsrPolicy [-VmmToVmm] -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96cb7-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="96cb7-111">DESCRIPTION</span></span>
<span data-ttu-id="96cb7-112">Командлет **Update-AzRecoveryServicesAsrPolicy** обновляет указанную политику репликации восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="96cb7-112">The **Update-AzRecoveryServicesAsrPolicy** cmdlet updates the specified Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="96cb7-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="96cb7-113">EXAMPLES</span></span>

### <span data-ttu-id="96cb7-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="96cb7-114">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrPolicy -Policy $Policy -ReplicationFrequencyInSeconds 900
```

<span data-ttu-id="96cb7-115">Запускает операцию обновления политики репликации с указанными параметрами и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="96cb7-115">Starts the update replication policy operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="96cb7-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="96cb7-116">Example 2</span></span>
```
PS C:\> Update-AzRecoveryServicesAsrPolicy -AzureToAzure -InputObject $Policy -ReplicationFrequencyInSeconds 900
```

<span data-ttu-id="96cb7-117">Запускает операцию изменения политики репликации Azure в Azure с использованием указанных параметров и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="96cb7-117">Starts the update azure to azure replication policy operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="96cb7-118">Пример 3</span><span class="sxs-lookup"><span data-stu-id="96cb7-118">Example 3</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrPolicy -AzureToAzure -InputObject $Policy -RecoveryPointRetentionInHours 20
```

<span data-ttu-id="96cb7-119">Запускает политику репликации Azure для Azure с указанными параметрами и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="96cb7-119">Starts the update azure to azure replication policy using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="96cb7-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="96cb7-120">PARAMETERS</span></span>

### <span data-ttu-id="96cb7-121">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="96cb7-121">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="96cb7-122">Указывает частоту (в часах) для создания точек восстановления с одинаковым соответствием между приложениями.</span><span class="sxs-lookup"><span data-stu-id="96cb7-122">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

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

### <span data-ttu-id="96cb7-123">-Проверка подлинности</span><span class="sxs-lookup"><span data-stu-id="96cb7-123">-Authentication</span></span>
<span data-ttu-id="96cb7-124">Указывает тип используемой проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="96cb7-124">Specifies the type of authentication used.</span></span>

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

### <span data-ttu-id="96cb7-125">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="96cb7-125">-AzureToAzure</span></span>
<span data-ttu-id="96cb7-126">Указывает на аварийное восстановление Azure для Azure.</span><span class="sxs-lookup"><span data-stu-id="96cb7-126">Specifies the Azure to Azure disaster recovery.</span></span>

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

### <span data-ttu-id="96cb7-127">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="96cb7-127">-AzureToVMware</span></span>
<span data-ttu-id="96cb7-128">Указывает на аварийное восстановление Azure для vMWare.</span><span class="sxs-lookup"><span data-stu-id="96cb7-128">Specifies the Azure to vMWare disaster recovery.</span></span>

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

### <span data-ttu-id="96cb7-129">-Сжатие</span><span class="sxs-lookup"><span data-stu-id="96cb7-129">-Compression</span></span>
<span data-ttu-id="96cb7-130">Указывает, следует ли включить сжатие.</span><span class="sxs-lookup"><span data-stu-id="96cb7-130">Specifies if compression should be enabled.</span></span>

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

### <span data-ttu-id="96cb7-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96cb7-131">-DefaultProfile</span></span>
<span data-ttu-id="96cb7-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="96cb7-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="96cb7-133">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="96cb7-133">-HyperVToAzure</span></span>
<span data-ttu-id="96cb7-134">Параметр Switch, указывающий, что указанная политика используется для репликации виртуальных машин Hyper-V в Azure.</span><span class="sxs-lookup"><span data-stu-id="96cb7-134">Switch parameter indicating that the specified policy is used to replicate Hyper-V virtual machines to Azure.</span></span>

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

### <span data-ttu-id="96cb7-135">-InputObject</span><span class="sxs-lookup"><span data-stu-id="96cb7-135">-InputObject</span></span>
<span data-ttu-id="96cb7-136">Входной объект для командлета: определяет объект политики репликации ASR, соответствующий политике репликации, которую нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="96cb7-136">Input object for the cmdlet: Specifies the ASR replication policy object corresponding to the replication policy to be updated.</span></span>

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

### <span data-ttu-id="96cb7-137">-MultiVmSyncStatus</span><span class="sxs-lookup"><span data-stu-id="96cb7-137">-MultiVmSyncStatus</span></span>
<span data-ttu-id="96cb7-138">Задает состояние синхронизации multiVm для политики.</span><span class="sxs-lookup"><span data-stu-id="96cb7-138">Specifies multiVm sync status for the policy.</span></span>

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

### <span data-ttu-id="96cb7-139">-NumberOfRecoveryPointsToRetain</span><span class="sxs-lookup"><span data-stu-id="96cb7-139">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="96cb7-140">Указывает число точек восстановления, которые нужно сохранить.</span><span class="sxs-lookup"><span data-stu-id="96cb7-140">Specifies the number recovery points to retain.</span></span>

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

### <span data-ttu-id="96cb7-141">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="96cb7-141">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="96cb7-142">Указывает идентификатор учетной записи хранилища Azure целевого объекта репликации.</span><span class="sxs-lookup"><span data-stu-id="96cb7-142">Specifies the Azure storage account ID of the replication target.</span></span> <span data-ttu-id="96cb7-143">Используется как Целевая учетная запись хранилища для репликации, если при включении репликации с помощью командлета New-AzRecoveryServicesASRReplicationProtectedItem не предоставлен другой вариант.</span><span class="sxs-lookup"><span data-stu-id="96cb7-143">Used as the target storage account for replication if an alternate is not provided while enabling replication using the New-AzRecoveryServicesASRReplicationProtectedItem cmdlet.</span></span>


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

### <span data-ttu-id="96cb7-144">-RecoveryPointRetentionInHours</span><span class="sxs-lookup"><span data-stu-id="96cb7-144">-RecoveryPointRetentionInHours</span></span>
<span data-ttu-id="96cb7-145">Время в часах, по истечении которого точки восстановления сохраняются после создания.</span><span class="sxs-lookup"><span data-stu-id="96cb7-145">Time in hours to retain recovery points after creation.</span></span>

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

### <span data-ttu-id="96cb7-146">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="96cb7-146">-ReplicaDeletion</span></span>
<span data-ttu-id="96cb7-147">Указывает, следует ли удалять виртуальную машину реплики при отключении репликации с сайта, управляемого VMM, в другой.</span><span class="sxs-lookup"><span data-stu-id="96cb7-147">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

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

### <span data-ttu-id="96cb7-148">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="96cb7-148">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="96cb7-149">Указывает периодичность репликации (в секундах).</span><span class="sxs-lookup"><span data-stu-id="96cb7-149">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="96cb7-150">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="96cb7-150">Valid values are:</span></span>

- <span data-ttu-id="96cb7-151">30</span><span class="sxs-lookup"><span data-stu-id="96cb7-151">30</span></span>
- <span data-ttu-id="96cb7-152">300</span><span class="sxs-lookup"><span data-stu-id="96cb7-152">300</span></span>
- <span data-ttu-id="96cb7-153">900</span><span class="sxs-lookup"><span data-stu-id="96cb7-153">900</span></span>

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

### <span data-ttu-id="96cb7-154">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="96cb7-154">-ReplicationMethod</span></span>
<span data-ttu-id="96cb7-155">Указывает метод репликации.</span><span class="sxs-lookup"><span data-stu-id="96cb7-155">Specifies the replication method.</span></span>

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

### <span data-ttu-id="96cb7-156">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="96cb7-156">-ReplicationPort</span></span>
<span data-ttu-id="96cb7-157">Указывает порт, используемый для репликации.</span><span class="sxs-lookup"><span data-stu-id="96cb7-157">Specifies the port used for replication.</span></span>

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

### <span data-ttu-id="96cb7-158">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="96cb7-158">-ReplicationStartTime</span></span>
<span data-ttu-id="96cb7-159">Указывает время начала репликации.</span><span class="sxs-lookup"><span data-stu-id="96cb7-159">Specifies the replication start time.</span></span>
<span data-ttu-id="96cb7-160">Оно должно быть не позже, чем 24 часа, начиная с начала задания.</span><span class="sxs-lookup"><span data-stu-id="96cb7-160">It must be no later than 24-hours from the start of the job.</span></span>

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

### <span data-ttu-id="96cb7-161">-RPOWarningThresholdInMinutes</span><span class="sxs-lookup"><span data-stu-id="96cb7-161">-RPOWarningThresholdInMinutes</span></span>
<span data-ttu-id="96cb7-162">Значение порога RPO (в минутах), на которое следует выдать предупреждение.</span><span class="sxs-lookup"><span data-stu-id="96cb7-162">The RPO threshold value in minutes to warn on.</span></span>

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

### <span data-ttu-id="96cb7-163">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="96cb7-163">-VmmToVmm</span></span>
<span data-ttu-id="96cb7-164">Параметр Switch, указывающий на то, что указанная политика используется для репликации виртуальных машин Hyper-V, управляемых VMM, между двумя сайтами Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="96cb7-164">Switch parameter indicating that the specified policy is used to replicate VMM managed Hyper-V virtual machines between two Hyper-V sites.</span></span>

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

### <span data-ttu-id="96cb7-165">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="96cb7-165">-VMwareToAzure</span></span>
<span data-ttu-id="96cb7-166">Параметр Switch, указывающий, что указанная политика используется для репликации виртуальных машин VMware в Azure.</span><span class="sxs-lookup"><span data-stu-id="96cb7-166">Switch parameter indicating that the specified policy is used to replicate VMware virtual machines to Azure.</span></span>

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

### <span data-ttu-id="96cb7-167">-Confirm</span><span class="sxs-lookup"><span data-stu-id="96cb7-167">-Confirm</span></span>
<span data-ttu-id="96cb7-168">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="96cb7-168">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96cb7-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96cb7-169">-WhatIf</span></span>
<span data-ttu-id="96cb7-170">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="96cb7-170">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="96cb7-171">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="96cb7-171">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96cb7-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96cb7-172">CommonParameters</span></span>
<span data-ttu-id="96cb7-173">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="96cb7-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96cb7-174">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="96cb7-174">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96cb7-175">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="96cb7-175">INPUTS</span></span>

### <span data-ttu-id="96cb7-176">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="96cb7-176">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="96cb7-177">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="96cb7-177">OUTPUTS</span></span>

### <span data-ttu-id="96cb7-178">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="96cb7-178">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="96cb7-179">Пуск</span><span class="sxs-lookup"><span data-stu-id="96cb7-179">NOTES</span></span>

## <span data-ttu-id="96cb7-180">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="96cb7-180">RELATED LINKS</span></span>