---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/update-azurermrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: bf049e18d75867f7dd9904e8d2ab2223dffdb0bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557220"
---
# <span data-ttu-id="a2441-101">Update-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="a2441-101">Update-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="a2441-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a2441-102">SYNOPSIS</span></span>
<span data-ttu-id="a2441-103">Обновляет политику репликации восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="a2441-103">Updates an Azure Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2441-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a2441-104">SYNTAX</span></span>

### <span data-ttu-id="a2441-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a2441-105">Default (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2441-106">VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="a2441-106">VMwareToAzure</span></span>
```
Update-AzureRmRecoveryServicesAsrPolicy [-VMwareToAzure] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-RPOWarningThresholdInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2441-107">AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="a2441-107">AzureToAzure</span></span>
```
Update-AzureRmRecoveryServicesAsrPolicy [-AzureToAzure] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a2441-108">AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="a2441-108">AzureToVMware</span></span>
```
Update-AzureRmRecoveryServicesAsrPolicy [-AzureToVMware] -InputObject <ASRPolicy>
 [-RecoveryPointRetentionInHours <Int32>] [-ApplicationConsistentSnapshotFrequencyInHours <Int32>]
 [-MultiVmSyncStatus <String>] [-RPOWarningThresholdInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2441-109">HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="a2441-109">HyperVToAzure</span></span>
```
Update-AzureRmRecoveryServicesAsrPolicy [-HyperVToAzure] -InputObject <ASRPolicy>
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2441-110">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="a2441-110">EnterpriseToEnterprise</span></span>
```
Update-AzureRmRecoveryServicesAsrPolicy [-VmmToVmm] -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2441-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a2441-111">DESCRIPTION</span></span>
<span data-ttu-id="a2441-112">Командлет **Update-AzureRmRecoveryServicesAsrPolicy** обновляет указанную политику репликации восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="a2441-112">The **Update-AzureRmRecoveryServicesAsrPolicy** cmdlet updates the specified Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="a2441-113">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a2441-113">EXAMPLES</span></span>

### <span data-ttu-id="a2441-114">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a2441-114">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrPolicy -Policy $Policy -ReplicationFrequencyInSeconds 900
```

<span data-ttu-id="a2441-115">Запускает операцию обновления политики репликации с указанными параметрами и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="a2441-115">Starts the update replication policy operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="a2441-116">Пример 2</span><span class="sxs-lookup"><span data-stu-id="a2441-116">Example 2</span></span>
```
PS C:\> Update-AzureRmRecoveryServicesAsrPolicy -AzureToAzure -InputObject $Policy -ReplicationFrequencyInSeconds 900
```

<span data-ttu-id="a2441-117">Запускает операцию изменения политики репликации Azure в Azure с использованием указанных параметров и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="a2441-117">Starts the update azure to azure replication policy operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

### <span data-ttu-id="a2441-118">Пример 3</span><span class="sxs-lookup"><span data-stu-id="a2441-118">Example 3</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrPolicy -AzureToAzure -InputObject $Policy -RecoveryPointRetentionInHours 20
```

<span data-ttu-id="a2441-119">Запускает политику репликации Azure для Azure с указанными параметрами и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="a2441-119">Starts the update azure to azure replication policy using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="a2441-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a2441-120">PARAMETERS</span></span>

### <span data-ttu-id="a2441-121">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="a2441-121">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="a2441-122">Указывает частоту (в часах) для создания точек восстановления с одинаковым соответствием между приложениями.</span><span class="sxs-lookup"><span data-stu-id="a2441-122">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2441-123">-Проверка подлинности</span><span class="sxs-lookup"><span data-stu-id="a2441-123">-Authentication</span></span>
<span data-ttu-id="a2441-124">Указывает тип используемой проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="a2441-124">Specifies the type of authentication used.</span></span>

```yaml
Type: String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Certificate, Kerberos

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2441-125">-AzureToAzure</span><span class="sxs-lookup"><span data-stu-id="a2441-125">-AzureToAzure</span></span>
<span data-ttu-id="a2441-126">Параметр Switch, указывающий на то, что политика репликации, используемая для репликации виртуальных машин Azure между двумя областями Azure, будет обновлена.</span><span class="sxs-lookup"><span data-stu-id="a2441-126">Switch parameter specifying that the replication policy used to replicate Azure virtual machines between two Azure regions will be updated.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2441-127">-AzureToVMware</span><span class="sxs-lookup"><span data-stu-id="a2441-127">-AzureToVMware</span></span>
<span data-ttu-id="a2441-128">Параметр Switch, указывающий на то, что политика specfied используется для репликации отказов на виртуальные машины, запущенные в Azure, обратно на локальный сайт VMware.</span><span class="sxs-lookup"><span data-stu-id="a2441-128">Switch parameter indicating that the specfied policy is used to replicate failed over virtual machines running in Azure back to an on-premises VMware site.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AzureToVMware
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2441-129">-Сжатие</span><span class="sxs-lookup"><span data-stu-id="a2441-129">-Compression</span></span>
<span data-ttu-id="a2441-130">Указывает, следует ли включить сжатие.</span><span class="sxs-lookup"><span data-stu-id="a2441-130">Specifies if compression should be enabled.</span></span>

```yaml
Type: String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2441-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a2441-131">-Confirm</span></span>
<span data-ttu-id="a2441-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a2441-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2441-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2441-133">-DefaultProfile</span></span>
<span data-ttu-id="a2441-134">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a2441-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2441-135">-Шифрование</span><span class="sxs-lookup"><span data-stu-id="a2441-135">-Encryption</span></span>
<span data-ttu-id="a2441-136">Указывает, следует ли включать или отключать шифрование.</span><span class="sxs-lookup"><span data-stu-id="a2441-136">Specifies if encryption should be enabled or disabled.</span></span>

```yaml
Type: String
Parameter Sets: Default, HyperVToAzure
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2441-137">-HyperVToAzure</span><span class="sxs-lookup"><span data-stu-id="a2441-137">-HyperVToAzure</span></span>
<span data-ttu-id="a2441-138">Параметр Switch, указывающий на то, что для репликации виртуальных машин Hyper-V в Azure используется политика specfied.</span><span class="sxs-lookup"><span data-stu-id="a2441-138">Switch parameter indicating that the specfied policy is used to replicate Hyper-V virtual machines to Azure.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: HyperVToAzure
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2441-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a2441-139">-InputObject</span></span>
<span data-ttu-id="a2441-140">Входной объект для командлета: определяет объект политики репликации ASR, соответствующий политике репликации, которую нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="a2441-140">Input object for the cmdlet: Specifies the ASR replication policy object corresponding to the replication policy to be updated.</span></span>

```yaml
Type: ASRPolicy
Parameter Sets: (All)
Aliases: Policy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a2441-141">-MultiVmSyncStatus</span><span class="sxs-lookup"><span data-stu-id="a2441-141">-MultiVmSyncStatus</span></span>
<span data-ttu-id="a2441-142">Задает состояние синхронизации multiVm для политики.</span><span class="sxs-lookup"><span data-stu-id="a2441-142">Specifies multiVm sync status for the policy.</span></span>

```yaml
Type: String
Parameter Sets: VMwareToAzure, AzureToAzure, AzureToVMware
Aliases:
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2441-143">-NumberOfRecoveryPointsToRetain</span><span class="sxs-lookup"><span data-stu-id="a2441-143">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="a2441-144">Указывает число точек восстановления, которые нужно сохранить.</span><span class="sxs-lookup"><span data-stu-id="a2441-144">Specifies the number recovery points to retain.</span></span>

```yaml
Type: Int32
Parameter Sets: Default, HyperVToAzure, EnterpriseToEnterprise
Aliases: RecoveryPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2441-145">-RPOWarningThresholdInMinutes</span><span class="sxs-lookup"><span data-stu-id="a2441-145">-RPOWarningThresholdInMinutes</span></span>
<span data-ttu-id="a2441-146">Значение порога RPO (в минутах), на которое следует выдать предупреждение.</span><span class="sxs-lookup"><span data-stu-id="a2441-146">The RPO threshold value in minutes to warn on.</span></span>

```yaml
Type: Int32
Parameter Sets: VMwareToAzure, AzureToVMware
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2441-147">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="a2441-147">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="a2441-148">Указывает идентификатор учетной записи хранилища Azure целевого объекта репликации.</span><span class="sxs-lookup"><span data-stu-id="a2441-148">Specifies the Azure storage account ID of the replication target.</span></span> <span data-ttu-id="a2441-149">Используется как Целевая учетная запись хранилища для репликации, если при включении репликации с помощью командлета New-AzureRmRecoveryServicesASRReplicationProtectedItem не предоставлен другой вариант.</span><span class="sxs-lookup"><span data-stu-id="a2441-149">Used as the target storage account for replication if an alternate is not provided while enabling replication using the New-AzureRmRecoveryServicesASRReplicationProtectedItem cmdlet.</span></span>


```yaml
Type: String
Parameter Sets: Default, HyperVToAzure
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2441-150">-RecoveryPointRetentionInHours</span><span class="sxs-lookup"><span data-stu-id="a2441-150">-RecoveryPointRetentionInHours</span></span>
<span data-ttu-id="a2441-151">Время в часах, по истечении которого точки восстановления сохраняются после создания.</span><span class="sxs-lookup"><span data-stu-id="a2441-151">Time in hours to retain recovery points after creation.</span></span>

```yaml
Type: Int32
Parameter Sets: VMwareToAzure, AzureToAzure, AzureToVMware
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2441-152">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="a2441-152">-ReplicaDeletion</span></span>
<span data-ttu-id="a2441-153">Указывает, следует ли удалять виртуальную машину реплики при отключении репликации с сайта, управляемого VMM, в другой.</span><span class="sxs-lookup"><span data-stu-id="a2441-153">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

```yaml
Type: String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Required, NotRequired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2441-154">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="a2441-154">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="a2441-155">Указывает периодичность репликации (в секундах).</span><span class="sxs-lookup"><span data-stu-id="a2441-155">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="a2441-156">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="a2441-156">Valid values are:</span></span>

- <span data-ttu-id="a2441-157">30</span><span class="sxs-lookup"><span data-stu-id="a2441-157">30</span></span>
- <span data-ttu-id="a2441-158">300</span><span class="sxs-lookup"><span data-stu-id="a2441-158">300</span></span>
- <span data-ttu-id="a2441-159">900</span><span class="sxs-lookup"><span data-stu-id="a2441-159">900</span></span>

```yaml
Type: String
Parameter Sets: Default, HyperVToAzure, EnterpriseToEnterprise
Aliases:
Accepted values: 30, 300, 900

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2441-160">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="a2441-160">-ReplicationMethod</span></span>
<span data-ttu-id="a2441-161">Указывает метод репликации.</span><span class="sxs-lookup"><span data-stu-id="a2441-161">Specifies the replication method.</span></span>

```yaml
Type: String
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2441-162">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="a2441-162">-ReplicationPort</span></span>
<span data-ttu-id="a2441-163">Указывает порт, используемый для репликации.</span><span class="sxs-lookup"><span data-stu-id="a2441-163">Specifies the port used for replication.</span></span>

```yaml
Type: UInt16
Parameter Sets: Default, EnterpriseToEnterprise
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2441-164">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="a2441-164">-ReplicationStartTime</span></span>
<span data-ttu-id="a2441-165">Указывает время начала репликации.</span><span class="sxs-lookup"><span data-stu-id="a2441-165">Specifies the replication start time.</span></span>
<span data-ttu-id="a2441-166">Оно должно быть не позже, чем 24 часа, начиная с начала задания.</span><span class="sxs-lookup"><span data-stu-id="a2441-166">It must be no later than 24-hours from the start of the job.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: Default, HyperVToAzure, EnterpriseToEnterprise
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2441-167">-VMwareToAzure</span><span class="sxs-lookup"><span data-stu-id="a2441-167">-VMwareToAzure</span></span>
<span data-ttu-id="a2441-168">Параметр Switch, указывающий на то, что для репликации виртуальных машин VMware в Azure используется политика specfied.</span><span class="sxs-lookup"><span data-stu-id="a2441-168">Switch parameter indicating that the specfied policy is used to replicate VMware virtual machines to Azure.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: VMwareToAzure
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2441-169">-VmmToVmm</span><span class="sxs-lookup"><span data-stu-id="a2441-169">-VmmToVmm</span></span>
<span data-ttu-id="a2441-170">Параметр Switch, указывающий, что политика specfied используется для репликации виртуальных машин Hyper-V, управляемых VMM, между двумя сайтами Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="a2441-170">Switch parameter indicating that the specfied policy is used to replicate VMM managed Hyper-V virtual machines between two Hyper-V sites.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnterpriseToEnterprise
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2441-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2441-171">-WhatIf</span></span>
<span data-ttu-id="a2441-172">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a2441-172">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a2441-173">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a2441-173">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2441-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2441-174">CommonParameters</span></span>
<span data-ttu-id="a2441-175">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a2441-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2441-176">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2441-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2441-177">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a2441-177">INPUTS</span></span>

### <span data-ttu-id="a2441-178">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="a2441-178">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="a2441-179">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a2441-179">OUTPUTS</span></span>

### <span data-ttu-id="a2441-180">System. Object</span><span class="sxs-lookup"><span data-stu-id="a2441-180">System.Object</span></span>

## <span data-ttu-id="a2441-181">Пуск</span><span class="sxs-lookup"><span data-stu-id="a2441-181">NOTES</span></span>

## <span data-ttu-id="a2441-182">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a2441-182">RELATED LINKS</span></span>
