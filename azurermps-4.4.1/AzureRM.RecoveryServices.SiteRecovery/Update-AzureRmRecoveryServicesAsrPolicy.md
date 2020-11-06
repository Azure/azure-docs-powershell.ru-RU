---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 302b781ee6af68cb960ab01668147edc56e04284
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567537"
---
# <span data-ttu-id="f3b1e-101">Update-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="f3b1e-101">Update-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="f3b1e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f3b1e-102">SYNOPSIS</span></span>
<span data-ttu-id="f3b1e-103">Обновляет политику репликации восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="f3b1e-103">Updates an Azure Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3b1e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f3b1e-104">SYNTAX</span></span>

```
Update-AzureRmRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-ReplicationMethod <String>]
 [-ReplicationFrequencyInSeconds <String>] [-NumberOfRecoveryPointsToRetain <Int32>]
 [-ApplicationConsistentSnapshotFrequencyInHours <Int32>] [-Compression <String>] [-ReplicationPort <UInt16>]
 [-Authentication <String>] [-ReplicationStartTime <TimeSpan>] [-ReplicaDeletion <String>]
 [-RecoveryAzureStorageAccountId <String>] [-Encryption <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3b1e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3b1e-105">DESCRIPTION</span></span>
<span data-ttu-id="f3b1e-106">Командлет **Update-AzureRmRecoveryServicesAsrPolicy** обновляет указанную политику репликации восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="f3b1e-106">The **Update-AzureRmRecoveryServicesAsrPolicy** cmdlet updates the specified Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="f3b1e-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f3b1e-107">EXAMPLES</span></span>

### <span data-ttu-id="f3b1e-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f3b1e-108">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrPolicy -Policy $Policy -ReplicationFrequencyInSeconds 900
```

<span data-ttu-id="f3b1e-109">Запускает операцию обновления политики репликации с указанными параметрами и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="f3b1e-109">Starts the update replication policy operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="f3b1e-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f3b1e-110">PARAMETERS</span></span>

### <span data-ttu-id="f3b1e-111">-ApplicationConsistentSnapshotFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="f3b1e-111">-ApplicationConsistentSnapshotFrequencyInHours</span></span>
<span data-ttu-id="f3b1e-112">Указывает частоту (в часах) для создания точек восстановления с одинаковым соответствием между приложениями.</span><span class="sxs-lookup"><span data-stu-id="f3b1e-112">Specifies the frequency(in hours) at which to create application consistent recovery points.</span></span>

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

### <span data-ttu-id="f3b1e-113">-Проверка подлинности</span><span class="sxs-lookup"><span data-stu-id="f3b1e-113">-Authentication</span></span>
<span data-ttu-id="f3b1e-114">Указывает тип используемой проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="f3b1e-114">Specifies the type of authentication used.</span></span>
<span data-ttu-id="f3b1e-115">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="f3b1e-115">Valid values are:</span></span>

- <span data-ttu-id="f3b1e-116">См</span><span class="sxs-lookup"><span data-stu-id="f3b1e-116">Certificate</span></span>
-  <span data-ttu-id="f3b1e-117">Использованием</span><span class="sxs-lookup"><span data-stu-id="f3b1e-117">Kerberos</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Certificate, Kerberos

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3b1e-118">-Сжатие</span><span class="sxs-lookup"><span data-stu-id="f3b1e-118">-Compression</span></span>
<span data-ttu-id="f3b1e-119">Указывает, следует ли включить сжатие.</span><span class="sxs-lookup"><span data-stu-id="f3b1e-119">Specifies if compression should be enabled.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3b1e-120">-Шифрование</span><span class="sxs-lookup"><span data-stu-id="f3b1e-120">-Encryption</span></span>
<span data-ttu-id="f3b1e-121">Указывает, следует ли включать или отключать шифрование.</span><span class="sxs-lookup"><span data-stu-id="f3b1e-121">Specifies if encryption should be enabled or disabled.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enable, Disable

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3b1e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f3b1e-122">-InputObject</span></span>
<span data-ttu-id="f3b1e-123">Входной объект для командлета: определяет объект политики репликации ASR, соответствующий политике репликации, которую нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="f3b1e-123">Input object for the cmdlet: Specifies the ASR replication policy object corresponding to the replication policy to be updated.</span></span>

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

### <span data-ttu-id="f3b1e-124">-NumberOfRecoveryPointsToRetain</span><span class="sxs-lookup"><span data-stu-id="f3b1e-124">-NumberOfRecoveryPointsToRetain</span></span>
<span data-ttu-id="f3b1e-125">Указывает число точек восстановления, которые нужно сохранить.</span><span class="sxs-lookup"><span data-stu-id="f3b1e-125">Specifies the number recovery points to retain.</span></span>

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

### <span data-ttu-id="f3b1e-126">-RecoveryAzureStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="f3b1e-126">-RecoveryAzureStorageAccountId</span></span>
<span data-ttu-id="f3b1e-127">Указывает идентификатор учетной записи хранилища Azure целевого объекта репликации.</span><span class="sxs-lookup"><span data-stu-id="f3b1e-127">Specifies the Azure storage account ID of the replication target.</span></span> <span data-ttu-id="f3b1e-128">Используется как Целевая учетная запись хранилища для репликации, если при включении репликации с помощью командлета New-AzureRmRecoveryServicesASRReplicationProtectedItem не предоставлен другой вариант.</span><span class="sxs-lookup"><span data-stu-id="f3b1e-128">Used as the target storage account for replication if an alternate is not provided while enabling replication using the New-AzureRmRecoveryServicesASRReplicationProtectedItem cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3b1e-129">-ReplicaDeletion</span><span class="sxs-lookup"><span data-stu-id="f3b1e-129">-ReplicaDeletion</span></span>
<span data-ttu-id="f3b1e-130">Указывает, следует ли удалять виртуальную машину реплики при отключении репликации с сайта, управляемого VMM, в другой.</span><span class="sxs-lookup"><span data-stu-id="f3b1e-130">Specifies if the replica virtual machine should be deleted on disabling replication from a VMM managed site to another.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Required, NotRequired

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3b1e-131">-ReplicationFrequencyInSeconds</span><span class="sxs-lookup"><span data-stu-id="f3b1e-131">-ReplicationFrequencyInSeconds</span></span>
<span data-ttu-id="f3b1e-132">Указывает периодичность репликации (в секундах).</span><span class="sxs-lookup"><span data-stu-id="f3b1e-132">Specifies the replication frequency interval in seconds.</span></span>
<span data-ttu-id="f3b1e-133">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="f3b1e-133">Valid values are:</span></span>

- <span data-ttu-id="f3b1e-134">30</span><span class="sxs-lookup"><span data-stu-id="f3b1e-134">30</span></span>
- <span data-ttu-id="f3b1e-135">300</span><span class="sxs-lookup"><span data-stu-id="f3b1e-135">300</span></span>
- <span data-ttu-id="f3b1e-136">900</span><span class="sxs-lookup"><span data-stu-id="f3b1e-136">900</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: 30, 300, 900

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3b1e-137">-ReplicationMethod</span><span class="sxs-lookup"><span data-stu-id="f3b1e-137">-ReplicationMethod</span></span>
<span data-ttu-id="f3b1e-138">Указывает метод репликации.</span><span class="sxs-lookup"><span data-stu-id="f3b1e-138">Specifies the replication method.</span></span>
<span data-ttu-id="f3b1e-139">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="f3b1e-139">Valid values are:</span></span>

- <span data-ttu-id="f3b1e-140">Онлайн</span><span class="sxs-lookup"><span data-stu-id="f3b1e-140">Online</span></span>
- <span data-ttu-id="f3b1e-141">Доступ</span><span class="sxs-lookup"><span data-stu-id="f3b1e-141">Offline</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3b1e-142">-ReplicationPort</span><span class="sxs-lookup"><span data-stu-id="f3b1e-142">-ReplicationPort</span></span>
<span data-ttu-id="f3b1e-143">Указывает порт, используемый для репликации.</span><span class="sxs-lookup"><span data-stu-id="f3b1e-143">Specifies the port used for replication.</span></span>

```yaml
Type: UInt16
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3b1e-144">-ReplicationStartTime</span><span class="sxs-lookup"><span data-stu-id="f3b1e-144">-ReplicationStartTime</span></span>
<span data-ttu-id="f3b1e-145">Указывает время начала репликации.</span><span class="sxs-lookup"><span data-stu-id="f3b1e-145">Specifies the replication start time.</span></span>
<span data-ttu-id="f3b1e-146">Оно должно быть не позже, чем 24 часа, начиная с начала задания.</span><span class="sxs-lookup"><span data-stu-id="f3b1e-146">It must be no later than 24-hours from the start of the job.</span></span>

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

### <span data-ttu-id="f3b1e-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f3b1e-147">-Confirm</span></span>
<span data-ttu-id="f3b1e-148">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f3b1e-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3b1e-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3b1e-149">-WhatIf</span></span>
<span data-ttu-id="f3b1e-150">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f3b1e-150">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f3b1e-151">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f3b1e-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3b1e-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3b1e-152">CommonParameters</span></span>
<span data-ttu-id="f3b1e-153">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f3b1e-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3b1e-154">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3b1e-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3b1e-155">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f3b1e-155">INPUTS</span></span>

### <span data-ttu-id="f3b1e-156">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="f3b1e-156">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="f3b1e-157">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3b1e-157">OUTPUTS</span></span>

### <span data-ttu-id="f3b1e-158">System. Object</span><span class="sxs-lookup"><span data-stu-id="f3b1e-158">System.Object</span></span>

## <span data-ttu-id="f3b1e-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="f3b1e-159">NOTES</span></span>

## <span data-ttu-id="f3b1e-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f3b1e-160">RELATED LINKS</span></span>

