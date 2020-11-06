---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrPlannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrPlannedFailoverJob.md
ms.openlocfilehash: e96a57a00d6314015d1d13f4f540d3f763c96c23
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562252"
---
# <span data-ttu-id="63019-101">Start-AzureRmRecoveryServicesAsrPlannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="63019-101">Start-AzureRmRecoveryServicesAsrPlannedFailoverJob</span></span>

## <span data-ttu-id="63019-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="63019-102">SYNOPSIS</span></span>
<span data-ttu-id="63019-103">Запускает плановую операцию отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="63019-103">Starts a planned failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63019-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="63019-104">SYNTAX</span></span>

### <span data-ttu-id="63019-105">ByRPIObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="63019-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrPlannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-Optimize <String>] [-CreateVmIfNotFound <String>]
 [-ServicesProvider <ASRRecoveryServicesProvider>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63019-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="63019-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63019-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="63019-107">DESCRIPTION</span></span>
<span data-ttu-id="63019-108">Командлет **Start-AzureRmRecoveryServicesAsrPlannedFailoverJob** запускает плановую отработку отказа для защищенного элемента или плана восстановления для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="63019-108">The **Start-AzureRmRecoveryServicesAsrPlannedFailoverJob** cmdlet starts a planned failover for an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="63019-109">С помощью командлета Get-AzureRmRecoveryServicesAsrJob можно проверить, успешно ли прошло задание.</span><span class="sxs-lookup"><span data-stu-id="63019-109">You can check whether the job succeeds by using the Get-AzureRmRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="63019-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="63019-110">EXAMPLES</span></span>

### <span data-ttu-id="63019-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="63019-111">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="63019-112">Запускает плановую отработку отказа для указанного плана восстановления ASR и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="63019-112">Starts the planned failover for the specified ASR recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="63019-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="63019-113">PARAMETERS</span></span>

### <span data-ttu-id="63019-114">-CreateVmIfNotFound</span><span class="sxs-lookup"><span data-stu-id="63019-114">-CreateVmIfNotFound</span></span>
<span data-ttu-id="63019-115">Создание виртуальной машины, если она не была найдена при сбое в первичном регионе (используется в восстановлении альтернативных местоположений). Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="63019-115">Create the virtual machine if not found while failing back to the primary region (used in alternate location recovery.) The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="63019-116">Кнопки</span><span class="sxs-lookup"><span data-stu-id="63019-116">Yes</span></span>
- <span data-ttu-id="63019-117">Нет</span><span class="sxs-lookup"><span data-stu-id="63019-117">No</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Yes, No

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63019-118">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="63019-118">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="63019-119">Задает основной файл сертификата.</span><span class="sxs-lookup"><span data-stu-id="63019-119">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="63019-120">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="63019-120">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="63019-121">Задает вторичный файл сертификата.</span><span class="sxs-lookup"><span data-stu-id="63019-121">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="63019-122">-Направление</span><span class="sxs-lookup"><span data-stu-id="63019-122">-Direction</span></span>
<span data-ttu-id="63019-123">Указывает направление отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="63019-123">Specifies the direction of the failover.</span></span>
<span data-ttu-id="63019-124">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="63019-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="63019-125">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="63019-125">PrimaryToRecovery</span></span>
- <span data-ttu-id="63019-126">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="63019-126">RecoveryToPrimary</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63019-127">-OPTIMIZE</span><span class="sxs-lookup"><span data-stu-id="63019-127">-Optimize</span></span>
<span data-ttu-id="63019-128">Указывает, для чего нужно оптимизировать.</span><span class="sxs-lookup"><span data-stu-id="63019-128">Specifies what to optimize for.</span></span>
<span data-ttu-id="63019-129">Этот параметр применяется в том случае, если отработка отказа выполняется с сайта Azure на локальном сайте, для которого требуется значительная синхронизация данных.</span><span class="sxs-lookup"><span data-stu-id="63019-129">This parameter applies when failover is done from an Azure site to an on-premise site which requires a substantial data synchronization.</span></span>
<span data-ttu-id="63019-130">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="63019-130">Valid values are:</span></span>

- <span data-ttu-id="63019-131">ForDowntime</span><span class="sxs-lookup"><span data-stu-id="63019-131">ForDowntime</span></span>
- <span data-ttu-id="63019-132">ForSynchronization</span><span class="sxs-lookup"><span data-stu-id="63019-132">ForSynchronization</span></span>

<span data-ttu-id="63019-133">Если указан **ForDowntime** , это указывает на то, что данные синхронизируются перед переходом на другой ресурс для минимизации простоев.</span><span class="sxs-lookup"><span data-stu-id="63019-133">When **ForDowntime** is specified, this indicates that data is synchronized before failover to minimize downtime.</span></span>
<span data-ttu-id="63019-134">Синхронизация выполняется без выключения виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="63019-134">Synchronization is performed without shutting down the virtual machine.</span></span>
<span data-ttu-id="63019-135">После завершения синхронизации задание будет приостановлено.</span><span class="sxs-lookup"><span data-stu-id="63019-135">After synchronization is complete, the job is suspended.</span></span>
<span data-ttu-id="63019-136">Возобновите задачу, чтобы выполнить дополнительную операцию синхронизации, которая завершает работу виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="63019-136">Resume the job to do an additional synchronization operation that shuts down the virtual machine.</span></span>

<span data-ttu-id="63019-137">Если указан **ForSynchronization** , это указывает на то, что данные синхронизируются во время отработки отказа, поэтому синхронизация данных свернута.</span><span class="sxs-lookup"><span data-stu-id="63019-137">When **ForSynchronization** is specified, this indicates that data is synchronized during failover only so data synchronization is minimized.</span></span>
<span data-ttu-id="63019-138">Если этот параметр включен, виртуальная машина немедленно завершает работу.</span><span class="sxs-lookup"><span data-stu-id="63019-138">With this setting enabled, the virtual machine is shut down immediately.</span></span>
<span data-ttu-id="63019-139">Синхронизация начинается после завершения работы, чтобы завершить операцию отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="63019-139">Synchronization starts after shutdown to complete the failover operation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: ForDownTime, ForSynchronization

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63019-140">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="63019-140">-RecoveryPlan</span></span>
<span data-ttu-id="63019-141">Указывает объект плана восстановления ASR, соответствующий плану восстановления, для которого необходимо выполнить отдействие.</span><span class="sxs-lookup"><span data-stu-id="63019-141">Specifies the ASR Recovery plan object corresponding to the recovery plan to be failed over.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63019-142">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="63019-142">-ReplicationProtectedItem</span></span>
<span data-ttu-id="63019-143">Указывает объект элемента, защищенного репликацией ASR, соответствующий элементу, защищенному репликацией, для которого требуется отдавать отказ.</span><span class="sxs-lookup"><span data-stu-id="63019-143">Specifies the ASR replication protected item object corresponding to the replication protected item to be failed over.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63019-144">-ServicesProvider</span><span class="sxs-lookup"><span data-stu-id="63019-144">-ServicesProvider</span></span>
<span data-ttu-id="63019-145">Определяет узел, на котором будет создаваться виртуальная машина при сбое в другом расположении, указав объект поставщика служб ASR, соответствующий поставщику служб ASR, запущенному на узле.</span><span class="sxs-lookup"><span data-stu-id="63019-145">Identifies the host to on which to create the virtual machine while failing over to an alternate location by specifying the ASR services provider object corresponding to the ASR services provider running on the host.</span></span> 

```yaml
Type: ASRRecoveryServicesProvider
Parameter Sets: ByRPIObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63019-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="63019-146">-Confirm</span></span>
<span data-ttu-id="63019-147">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="63019-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63019-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63019-148">-WhatIf</span></span>
<span data-ttu-id="63019-149">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="63019-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="63019-150">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="63019-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63019-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63019-151">CommonParameters</span></span>
<span data-ttu-id="63019-152">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="63019-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63019-153">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63019-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63019-154">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="63019-154">INPUTS</span></span>

### <span data-ttu-id="63019-155">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="63019-155">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="63019-156">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="63019-156">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="63019-157">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="63019-157">OUTPUTS</span></span>

### <span data-ttu-id="63019-158">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="63019-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="63019-159">Пуск</span><span class="sxs-lookup"><span data-stu-id="63019-159">NOTES</span></span>

## <span data-ttu-id="63019-160">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="63019-160">RELATED LINKS</span></span>

