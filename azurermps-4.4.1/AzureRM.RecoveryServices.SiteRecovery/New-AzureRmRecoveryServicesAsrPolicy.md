---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: a0a55ad071a21f7924eb5a4115a7699fc6690060
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562284"
---
# <span data-ttu-id="be920-101">New-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="be920-101">New-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="be920-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="be920-102">SYNOPSIS</span></span>
<span data-ttu-id="be920-103">Создание политики репликации восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="be920-103">Creates an Azure Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be920-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="be920-104">SYNTAX</span></span>

### <span data-ttu-id="be920-105">EnterpriseToAzure (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="be920-105">EnterpriseToAzure (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrPolicy -Name <String> -ReplicationProvider <String>
 -ReplicationFrequencyInSeconds <String> [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-ReplicationStartTime <TimeSpan>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be920-106">EnterpriseToEnterprise</span><span class="sxs-lookup"><span data-stu-id="be920-106">EnterpriseToEnterprise</span></span>
```
New-AzureRmRecoveryServicesAsrPolicy -Name <String> -ReplicationProvider <String> [-ReplicationMethod <String>]
 -ReplicationFrequencyInSeconds <String> [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] -ReplicationPort <UInt16>
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="be920-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="be920-107">DESCRIPTION</span></span>
<span data-ttu-id="be920-108">Командлет **New-AzureRmRecoveryServicesAsrPolicy** создает политику репликации восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="be920-108">The **New-AzureRmRecoveryServicesAsrPolicy** cmdlet creates an Azure Site Recovery replication policy.</span></span>
<span data-ttu-id="be920-109">Политика репликации используется для указания параметров репликации, таких как частота репликации и количество точек восстановления.</span><span class="sxs-lookup"><span data-stu-id="be920-109">The replication policy is used to specify replication settings such as the replication frequency and number of recovery points.</span></span>

## <span data-ttu-id="be920-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="be920-110">EXAMPLES</span></span>

### <span data-ttu-id="be920-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="be920-111">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name $PolicyName -Policy $ProtectionProfile -PrimaryProtectionContainer $PrimaryContainer -RecoveryProtectionContainer $RecoveryContainer
```

<span data-ttu-id="be920-112">Запускает операцию создания политики репликации с указанными параметрами и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="be920-112">Starts the replication policy creation operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="be920-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="be920-113">PARAMETERS</span></span>

### <span data-ttu-id="be920-114">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="be920-114">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="be920-115">Указывает частоту (в часах) для создания точек восстановления с одинаковым соответствием между приложениями.</span><span class="sxs-lookup"><span data-stu-id="be920-115">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

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

### <span data-ttu-id="be920-116">-Проверка подлинности</span><span class="sxs-lookup"><span data-stu-id="be920-116">-Authentication</span></span>
<span data-ttu-id="be920-117">Указывает тип используемой проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="be920-117">Specifies the type of authentication used.</span></span>
<span data-ttu-id="be920-118">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="be920-118">Valid values are:</span></span>

- <span data-ttu-id="be920-119">См</span><span class="sxs-lookup"><span data-stu-id="be920-119">Certificate</span></span>
-  <span data-ttu-id="be920-120">Использованием</span><span class="sxs-lookup"><span data-stu-id="be920-120">Kerberos</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Certificate, Kerberos

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be920-121">-Сжатие</span><span class="sxs-lookup"><span data-stu-id="be920-121">-Compression</span></span>
<span data-ttu-id="be920-122">Указывает, следует ли включить сжатие.</span><span class="sxs-lookup"><span data-stu-id="be920-122">Specifies if compression should be enabled.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be920-123">-Шифрование</span><span class="sxs-lookup"><span data-stu-id="be920-123">-Encryption</span></span>
<span data-ttu-id="be920-124">Указывает, следует ли включать или отключать шифрование.</span><span class="sxs-lookup"><span data-stu-id="be920-124">Specifies if encryption should be enabled or disabled.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be920-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="be920-125">-Name</span></span>
<span data-ttu-id="be920-126">Задает имя политики репликации ASR.</span><span class="sxs-lookup"><span data-stu-id="be920-126">Specifies the name of the ASR replication policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be920-127">-NumberOfRecoveryPointsToRetain</span><span class="sxs-lookup"><span data-stu-id="be920-127">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="be920-128">Указывает число точек восстановления, которые нужно сохранить.</span><span class="sxs-lookup"><span data-stu-id="be920-128">Specifies the number recovery points to retain.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: RecoveryPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be920-129">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="be920-129">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="be920-130">Указывает идентификатор учетной записи хранилища Azure целевого объекта репликации.</span><span class="sxs-lookup"><span data-stu-id="be920-130">Specifies the Azure storage account ID of the replication target.</span></span> <span data-ttu-id="be920-131">Используется как Целевая учетная запись хранилища для репликации, если при включении репликации с помощью командлета New-AzureRmRecoveryServicesASRReplicationProtectedItem не предоставлен другой вариант.</span><span class="sxs-lookup"><span data-stu-id="be920-131">Used as the target storage account for replication if an alternate is not provided while enabling replication using the New-AzureRmRecoveryServicesASRReplicationProtectedItem cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be920-132">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="be920-132">-ReplicaDeletion</span></span>
<span data-ttu-id="be920-133">Указывает, следует ли удалять виртуальную машину реплики при отключении репликации с сайта, управляемого VMM, в другой.</span><span class="sxs-lookup"><span data-stu-id="be920-133">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Required, NotRequired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be920-134">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="be920-134">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="be920-135">Указывает периодичность репликации (в секундах).</span><span class="sxs-lookup"><span data-stu-id="be920-135">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="be920-136">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="be920-136">Valid values are:</span></span>

- <span data-ttu-id="be920-137">30</span><span class="sxs-lookup"><span data-stu-id="be920-137">30</span></span>
- <span data-ttu-id="be920-138">300</span><span class="sxs-lookup"><span data-stu-id="be920-138">300</span></span>
- <span data-ttu-id="be920-139">900</span><span class="sxs-lookup"><span data-stu-id="be920-139">900</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: 30, 300, 900

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be920-140">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="be920-140">-ReplicationMethod</span></span>
<span data-ttu-id="be920-141">Указывает метод репликации.</span><span class="sxs-lookup"><span data-stu-id="be920-141">Specifies the replication method.</span></span>
<span data-ttu-id="be920-142">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="be920-142">Valid values are:</span></span>

- <span data-ttu-id="be920-143">Онлайн</span><span class="sxs-lookup"><span data-stu-id="be920-143">Online</span></span>
- <span data-ttu-id="be920-144">Доступ</span><span class="sxs-lookup"><span data-stu-id="be920-144">Offline</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToEnterprise
Aliases: 
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be920-145">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="be920-145">-ReplicationPort</span></span>
<span data-ttu-id="be920-146">Указывает порт, используемый для репликации.</span><span class="sxs-lookup"><span data-stu-id="be920-146">Specifies the port used for replication.</span></span>

```yaml
Type: UInt16
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be920-147">-ReplicationProvider</span><span class="sxs-lookup"><span data-stu-id="be920-147">-ReplicationProvider</span></span>
<span data-ttu-id="be920-148">Указывает поставщика репликации.</span><span class="sxs-lookup"><span data-stu-id="be920-148">Specifies the replication provider.</span></span>
<span data-ttu-id="be920-149">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="be920-149">Valid values are:</span></span>

- <span data-ttu-id="be920-150">HyperVReplica2012R2</span><span class="sxs-lookup"><span data-stu-id="be920-150">HyperVReplica2012R2</span></span>
- <span data-ttu-id="be920-151">HyperVReplica2012</span><span class="sxs-lookup"><span data-stu-id="be920-151">HyperVReplica2012</span></span>
- <span data-ttu-id="be920-152">HyperVReplicaAzure</span><span class="sxs-lookup"><span data-stu-id="be920-152">HyperVReplicaAzure</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: HyperVReplica2012R2, HyperVReplica2012, HyperVReplicaAzure

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be920-153">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="be920-153">-ReplicationStartTime</span></span>
<span data-ttu-id="be920-154">Указывает время начала репликации.</span><span class="sxs-lookup"><span data-stu-id="be920-154">Specifies the replication start time.</span></span>
<span data-ttu-id="be920-155">Оно должно быть не позже, чем 24 часа, начиная с начала задания.</span><span class="sxs-lookup"><span data-stu-id="be920-155">It must be no later than 24-hours from the start of the job.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be920-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="be920-156">-Confirm</span></span>
<span data-ttu-id="be920-157">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="be920-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be920-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be920-158">-WhatIf</span></span>
<span data-ttu-id="be920-159">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="be920-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="be920-160">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="be920-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be920-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be920-161">CommonParameters</span></span>
<span data-ttu-id="be920-162">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="be920-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be920-163">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be920-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be920-164">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="be920-164">INPUTS</span></span>

### <span data-ttu-id="be920-165">Ничего</span><span class="sxs-lookup"><span data-stu-id="be920-165">None</span></span>

## <span data-ttu-id="be920-166">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="be920-166">OUTPUTS</span></span>

### <span data-ttu-id="be920-167">System. Object</span><span class="sxs-lookup"><span data-stu-id="be920-167">System.Object</span></span>

## <span data-ttu-id="be920-168">Пуск</span><span class="sxs-lookup"><span data-stu-id="be920-168">NOTES</span></span>

## <span data-ttu-id="be920-169">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="be920-169">RELATED LINKS</span></span>

[<span data-ttu-id="be920-170">Get-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="be920-170">Get-AzureRmRecoveryServicesAsrPolicy</span></span>](./Get-AzureRmRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="be920-171">Remove-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="be920-171">Remove-AzureRmRecoveryServicesAsrPolicy</span></span>](./Remove-AzureRmRecoveryServicesAsrPolicy.md)
