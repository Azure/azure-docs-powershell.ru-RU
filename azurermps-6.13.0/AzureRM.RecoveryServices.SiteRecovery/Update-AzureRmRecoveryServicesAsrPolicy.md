---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/update-azurermrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 805e421aedbb06b6f9a821b3f575b8a5035c86d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558335"
---
# <span data-ttu-id="299bc-101">Update-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="299bc-101">Update-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="299bc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="299bc-102">SYNOPSIS</span></span>
<span data-ttu-id="299bc-103">Обновляет политику репликации восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="299bc-103">Updates an Azure Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="299bc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="299bc-104">SYNTAX</span></span>

### <span data-ttu-id="299bc-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="299bc-105">Default (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="299bc-106">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="299bc-106">VMwareToAzure</span></span>
```
Update-AzureRmRecoveryServicesAsrPolicy [-VMwareToAzure] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-RPOWarningThresholdInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="299bc-107">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="299bc-107">AzureToAzure</span></span>
```
Update-AzureRmRecoveryServicesAsrPolicy [-AzureToAzure] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="299bc-108">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="299bc-108">AzureToVMware</span></span>
```
Update-AzureRmRecoveryServicesAsrPolicy [-AzureToVMware] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-RPOWarningThresholdInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="299bc-109">HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="299bc-109">HyperVToAzure</span></span>
```
Update-AzureRmRecoveryServicesAsrPolicy [-HyperVToAzure] -InputObject <ASRPolicy>
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="299bc-110">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="299bc-110">EnterpriseToEnterprise</span></span>
```
Update-AzureRmRecoveryServicesAsrPolicy [-VmmToVmm] -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="299bc-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="299bc-111">DESCRIPTION</span></span>
<span data-ttu-id="299bc-112">Командлет **Update-AzureRmRecoveryServicesAsrPolicy** обновляет указанную политику репликации восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="299bc-112">The **Update-AzureRmRecoveryServicesAsrPolicy** cmdlet updates the specified Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="299bc-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="299bc-113">EXAMPLES</span></span>

### <span data-ttu-id="299bc-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="299bc-114">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrPolicy -Policy $Policy -ReplicationFrequencyInSeconds 900
```

<span data-ttu-id="299bc-115">Запускает операцию обновления политики репликации с указанными параметрами и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="299bc-115">Starts the update replication policy operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="299bc-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="299bc-116">Example 2</span></span>
```
PS C:\> Update-AzureRmRecoveryServicesAsrPolicy -AzureToAzure -InputObject $Policy -ReplicationFrequencyInSeconds 900
```

<span data-ttu-id="299bc-117">Запускает операцию изменения политики репликации Azure в Azure с использованием указанных параметров и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="299bc-117">Starts the update azure to azure replication policy operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="299bc-118">Пример 3</span><span class="sxs-lookup"><span data-stu-id="299bc-118">Example 3</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrPolicy -AzureToAzure -InputObject $Policy -RecoveryPointRetentionInHours 20
```

<span data-ttu-id="299bc-119">Запускает политику репликации Azure для Azure с указанными параметрами и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="299bc-119">Starts the update azure to azure replication policy using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="299bc-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="299bc-120">PARAMETERS</span></span>

### <span data-ttu-id="299bc-121">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="299bc-121">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="299bc-122">Указывает частоту (в часах) для создания точек восстановления с одинаковым соответствием между приложениями.</span><span class="sxs-lookup"><span data-stu-id="299bc-122">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

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

### <span data-ttu-id="299bc-123">-Проверка подлинности</span><span class="sxs-lookup"><span data-stu-id="299bc-123">-Authentication</span></span>
<span data-ttu-id="299bc-124">Указывает тип используемой проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="299bc-124">Specifies the type of authentication used.</span></span>

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

### <span data-ttu-id="299bc-125">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="299bc-125">-AzureToAzure</span></span>
<span data-ttu-id="299bc-126">Параметр Switch, указывающий на то, что политика репликации, используемая для репликации виртуальных машин Azure между двумя областями Azure, будет обновлена.</span><span class="sxs-lookup"><span data-stu-id="299bc-126">Switch parameter specifying that the replication policy used to replicate Azure virtual machines between two Azure regions will be updated.</span></span>

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

### <span data-ttu-id="299bc-127">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="299bc-127">-AzureToVMware</span></span>
<span data-ttu-id="299bc-128">Параметр Switch, указывающий на то, что политика specfied используется для репликации отказов на виртуальные машины, запущенные в Azure, обратно на локальный сайт VMware.</span><span class="sxs-lookup"><span data-stu-id="299bc-128">Switch parameter indicating that the specfied policy is used to replicate failed over virtual machines running in Azure back to an on-premises VMware site.</span></span>

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

### <span data-ttu-id="299bc-129">-Сжатие</span><span class="sxs-lookup"><span data-stu-id="299bc-129">-Compression</span></span>
<span data-ttu-id="299bc-130">Указывает, следует ли включить сжатие.</span><span class="sxs-lookup"><span data-stu-id="299bc-130">Specifies if compression should be enabled.</span></span>

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

### <span data-ttu-id="299bc-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="299bc-131">-DefaultProfile</span></span>
<span data-ttu-id="299bc-132">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="299bc-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="299bc-133">-Шифрование</span><span class="sxs-lookup"><span data-stu-id="299bc-133">-Encryption</span></span>
<span data-ttu-id="299bc-134">{{Fill описание шифрования}}</span><span class="sxs-lookup"><span data-stu-id="299bc-134">{{Fill Encryption Description}}</span></span>

```yaml
Type: System.String
Parameter Sets: Default, HyperVToAzure
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="299bc-135">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="299bc-135">-HyperVToAzure</span></span>
<span data-ttu-id="299bc-136">Параметр Switch, указывающий на то, что для репликации виртуальных машин Hyper-V в Azure используется политика specfied.</span><span class="sxs-lookup"><span data-stu-id="299bc-136">Switch parameter indicating that the specfied policy is used to replicate Hyper-V virtual machines to Azure.</span></span>

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

### <span data-ttu-id="299bc-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="299bc-137">-InputObject</span></span>
<span data-ttu-id="299bc-138">Входной объект для командлета: определяет объект политики репликации ASR, соответствующий политике репликации, которую нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="299bc-138">Input object for the cmdlet: Specifies the ASR replication policy object corresponding to the replication policy to be updated.</span></span>

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

### <span data-ttu-id="299bc-139">-MultiVmSyncStatus</span><span class="sxs-lookup"><span data-stu-id="299bc-139">-MultiVmSyncStatus</span></span>
<span data-ttu-id="299bc-140">Задает состояние синхронизации multiVm для политики.</span><span class="sxs-lookup"><span data-stu-id="299bc-140">Specifies multiVm sync status for the policy.</span></span>

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

### <span data-ttu-id="299bc-141">-NumberOfRecoveryPointsToRetain</span><span class="sxs-lookup"><span data-stu-id="299bc-141">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="299bc-142">Указывает число точек восстановления, которые нужно сохранить.</span><span class="sxs-lookup"><span data-stu-id="299bc-142">Specifies the number recovery points to retain.</span></span>

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

### <span data-ttu-id="299bc-143">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="299bc-143">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="299bc-144">Указывает идентификатор учетной записи хранилища Azure целевого объекта репликации.</span><span class="sxs-lookup"><span data-stu-id="299bc-144">Specifies the Azure storage account ID of the replication target.</span></span> <span data-ttu-id="299bc-145">Используется как Целевая учетная запись хранилища для репликации, если при включении репликации с помощью командлета New-AzureRmRecoveryServicesASRReplicationProtectedItem не предоставлен другой вариант.</span><span class="sxs-lookup"><span data-stu-id="299bc-145">Used as the target storage account for replication if an alternate is not provided while enabling replication using the New-AzureRmRecoveryServicesASRReplicationProtectedItem cmdlet.</span></span>


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

### <span data-ttu-id="299bc-146">-RecoveryPointRetentionInHours</span><span class="sxs-lookup"><span data-stu-id="299bc-146">-RecoveryPointRetentionInHours</span></span>
<span data-ttu-id="299bc-147">Время в часах, по истечении которого точки восстановления сохраняются после создания.</span><span class="sxs-lookup"><span data-stu-id="299bc-147">Time in hours to retain recovery points after creation.</span></span>

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

### <span data-ttu-id="299bc-148">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="299bc-148">-ReplicaDeletion</span></span>
<span data-ttu-id="299bc-149">Указывает, следует ли удалять виртуальную машину реплики при отключении репликации с сайта, управляемого VMM, в другой.</span><span class="sxs-lookup"><span data-stu-id="299bc-149">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

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

### <span data-ttu-id="299bc-150">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="299bc-150">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="299bc-151">Указывает периодичность репликации (в секундах).</span><span class="sxs-lookup"><span data-stu-id="299bc-151">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="299bc-152">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="299bc-152">Valid values are:</span></span>

- <span data-ttu-id="299bc-153">30</span><span class="sxs-lookup"><span data-stu-id="299bc-153">30</span></span>
- <span data-ttu-id="299bc-154">300</span><span class="sxs-lookup"><span data-stu-id="299bc-154">300</span></span>
- <span data-ttu-id="299bc-155">900</span><span class="sxs-lookup"><span data-stu-id="299bc-155">900</span></span>

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

### <span data-ttu-id="299bc-156">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="299bc-156">-ReplicationMethod</span></span>
<span data-ttu-id="299bc-157">Указывает метод репликации.</span><span class="sxs-lookup"><span data-stu-id="299bc-157">Specifies the replication method.</span></span>

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

### <span data-ttu-id="299bc-158">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="299bc-158">-ReplicationPort</span></span>
<span data-ttu-id="299bc-159">Указывает порт, используемый для репликации.</span><span class="sxs-lookup"><span data-stu-id="299bc-159">Specifies the port used for replication.</span></span>

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

### <span data-ttu-id="299bc-160">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="299bc-160">-ReplicationStartTime</span></span>
<span data-ttu-id="299bc-161">Указывает время начала репликации.</span><span class="sxs-lookup"><span data-stu-id="299bc-161">Specifies the replication start time.</span></span>
<span data-ttu-id="299bc-162">Оно должно быть не позже, чем 24 часа, начиная с начала задания.</span><span class="sxs-lookup"><span data-stu-id="299bc-162">It must be no later than 24-hours from the start of the job.</span></span>

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

### <span data-ttu-id="299bc-163">-RPOWarningThresholdInMinutes</span><span class="sxs-lookup"><span data-stu-id="299bc-163">-RPOWarningThresholdInMinutes</span></span>
<span data-ttu-id="299bc-164">Значение порога RPO (в минутах), на которое следует выдать предупреждение.</span><span class="sxs-lookup"><span data-stu-id="299bc-164">The RPO threshold value in minutes to warn on.</span></span>

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

### <span data-ttu-id="299bc-165">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="299bc-165">-VmmToVmm</span></span>
<span data-ttu-id="299bc-166">Параметр Switch, указывающий, что политика specfied используется для репликации виртуальных машин Hyper-V, управляемых VMM, между двумя сайтами Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="299bc-166">Switch parameter indicating that the specfied policy is used to replicate VMM managed Hyper-V virtual machines between two Hyper-V sites.</span></span>

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

### <span data-ttu-id="299bc-167">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="299bc-167">-VMwareToAzure</span></span>
<span data-ttu-id="299bc-168">Параметр Switch, указывающий на то, что для репликации виртуальных машин VMware в Azure используется политика specfied.</span><span class="sxs-lookup"><span data-stu-id="299bc-168">Switch parameter indicating that the specfied policy is used to replicate VMware virtual machines to Azure.</span></span>

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

### <span data-ttu-id="299bc-169">-Confirm</span><span class="sxs-lookup"><span data-stu-id="299bc-169">-Confirm</span></span>
<span data-ttu-id="299bc-170">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="299bc-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="299bc-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="299bc-171">-WhatIf</span></span>
<span data-ttu-id="299bc-172">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="299bc-172">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="299bc-173">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="299bc-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="299bc-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="299bc-174">CommonParameters</span></span>
<span data-ttu-id="299bc-175">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="299bc-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="299bc-176">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="299bc-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="299bc-177">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="299bc-177">INPUTS</span></span>

### <span data-ttu-id="299bc-178">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="299bc-178">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="299bc-179">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="299bc-179">OUTPUTS</span></span>

### <span data-ttu-id="299bc-180">System. Object</span><span class="sxs-lookup"><span data-stu-id="299bc-180">System.Object</span></span>

## <span data-ttu-id="299bc-181">Пуск</span><span class="sxs-lookup"><span data-stu-id="299bc-181">NOTES</span></span>

## <span data-ttu-id="299bc-182">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="299bc-182">RELATED LINKS</span></span>
