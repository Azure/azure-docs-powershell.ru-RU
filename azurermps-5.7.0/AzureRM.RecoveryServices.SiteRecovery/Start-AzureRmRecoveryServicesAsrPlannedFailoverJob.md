---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/start-azurermrecoveryservicesasrplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrPlannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrPlannedFailoverJob.md
ms.openlocfilehash: df52a9b690060903affa666d66bfbd2a3afb7aea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558872"
---
# <span data-ttu-id="c242e-101">Start-AzureRmRecoveryServicesAsrPlannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="c242e-101">Start-AzureRmRecoveryServicesAsrPlannedFailoverJob</span></span>

## <span data-ttu-id="c242e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c242e-102">SYNOPSIS</span></span>
<span data-ttu-id="c242e-103">Запускает плановую операцию отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="c242e-103">Starts a planned failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c242e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c242e-104">SYNTAX</span></span>

### <span data-ttu-id="c242e-105">ByRPIObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c242e-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrPlannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-Optimize <String>] [-CreateVmIfNotFound <String>]
 [-ServicesProvider <ASRRecoveryServicesProvider>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c242e-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="c242e-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c242e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c242e-107">DESCRIPTION</span></span>
<span data-ttu-id="c242e-108">Командлет **Start-AzureRmRecoveryServicesAsrPlannedFailoverJob** запускает плановую отработку отказа для защищенного элемента или плана восстановления для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="c242e-108">The **Start-AzureRmRecoveryServicesAsrPlannedFailoverJob** cmdlet starts a planned failover for an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="c242e-109">С помощью командлета Get-AzureRmRecoveryServicesAsrJob можно проверить, успешно ли прошло задание.</span><span class="sxs-lookup"><span data-stu-id="c242e-109">You can check whether the job succeeds by using the Get-AzureRmRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="c242e-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c242e-110">EXAMPLES</span></span>

### <span data-ttu-id="c242e-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c242e-111">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="c242e-112">Запускает плановую отработку отказа для указанного плана восстановления ASR и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="c242e-112">Starts the planned failover for the specified ASR recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="c242e-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c242e-113">PARAMETERS</span></span>

### <span data-ttu-id="c242e-114">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c242e-114">-Confirm</span></span>
<span data-ttu-id="c242e-115">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c242e-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c242e-116">-CreateVmIfNotFound</span><span class="sxs-lookup"><span data-stu-id="c242e-116">-CreateVmIfNotFound</span></span>
<span data-ttu-id="c242e-117">Создание виртуальной машины, если она не была найдена при сбое в первичном регионе (используется в восстановлении альтернативных местоположений). Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c242e-117">Create the virtual machine if not found while failing back to the primary region (used in alternate location recovery.) The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c242e-118">Кнопки</span><span class="sxs-lookup"><span data-stu-id="c242e-118">Yes</span></span>
- <span data-ttu-id="c242e-119">Нет</span><span class="sxs-lookup"><span data-stu-id="c242e-119">No</span></span>

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

### <span data-ttu-id="c242e-120">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="c242e-120">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="c242e-121">Задает основной файл сертификата.</span><span class="sxs-lookup"><span data-stu-id="c242e-121">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="c242e-122">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="c242e-122">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="c242e-123">Задает вторичный файл сертификата.</span><span class="sxs-lookup"><span data-stu-id="c242e-123">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="c242e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c242e-124">-DefaultProfile</span></span>
<span data-ttu-id="c242e-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c242e-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="c242e-126">-Направление</span><span class="sxs-lookup"><span data-stu-id="c242e-126">-Direction</span></span>
<span data-ttu-id="c242e-127">Указывает направление отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="c242e-127">Specifies the direction of the failover.</span></span>
<span data-ttu-id="c242e-128">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="c242e-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c242e-129">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="c242e-129">PrimaryToRecovery</span></span>
- <span data-ttu-id="c242e-130">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="c242e-130">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="c242e-131">-OPTIMIZE</span><span class="sxs-lookup"><span data-stu-id="c242e-131">-Optimize</span></span>
<span data-ttu-id="c242e-132">Указывает, для чего нужно оптимизировать.</span><span class="sxs-lookup"><span data-stu-id="c242e-132">Specifies what to optimize for.</span></span>
<span data-ttu-id="c242e-133">Этот параметр применяется в том случае, если отработка отказа выполняется с сайта Azure на локальном сайте, требующем значительную синхронизацию данных.</span><span class="sxs-lookup"><span data-stu-id="c242e-133">This parameter applies when failover is done from an Azure site to an on-premise site which requires substantial data synchronization.</span></span>
<span data-ttu-id="c242e-134">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="c242e-134">Valid values are:</span></span>

- <span data-ttu-id="c242e-135">ForDowntime</span><span class="sxs-lookup"><span data-stu-id="c242e-135">ForDowntime</span></span>
- <span data-ttu-id="c242e-136">ForSynchronization</span><span class="sxs-lookup"><span data-stu-id="c242e-136">ForSynchronization</span></span>

<span data-ttu-id="c242e-137">Если указан **ForDowntime** , это указывает на то, что данные синхронизируются перед переходом на другой ресурс для минимизации простоев.</span><span class="sxs-lookup"><span data-stu-id="c242e-137">When **ForDowntime** is specified, this indicates that data is synchronized before failover to minimize downtime.</span></span>
<span data-ttu-id="c242e-138">Синхронизация выполняется без выключения виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c242e-138">Synchronization is performed without shutting down the virtual machine.</span></span>
<span data-ttu-id="c242e-139">После завершения синхронизации задание будет приостановлено.</span><span class="sxs-lookup"><span data-stu-id="c242e-139">After synchronization is complete, the job is suspended.</span></span>
<span data-ttu-id="c242e-140">Возобновите задачу, чтобы выполнить дополнительную операцию синхронизации, которая завершает работу виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="c242e-140">Resume the job to do an additional synchronization operation that shuts down the virtual machine.</span></span>

<span data-ttu-id="c242e-141">Если указан **ForSynchronization** , это указывает на то, что данные синхронизируются во время отработки отказа, поэтому синхронизация данных свернута.</span><span class="sxs-lookup"><span data-stu-id="c242e-141">When **ForSynchronization** is specified, this indicates that data is synchronized during failover only so data synchronization is minimized.</span></span>
<span data-ttu-id="c242e-142">Если этот параметр включен, виртуальная машина немедленно завершает работу.</span><span class="sxs-lookup"><span data-stu-id="c242e-142">With this setting enabled, the virtual machine is shut down immediately.</span></span>
<span data-ttu-id="c242e-143">Синхронизация начинается после завершения работы, чтобы завершить операцию отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="c242e-143">Synchronization starts after shutdown to complete the failover operation.</span></span>

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

### <span data-ttu-id="c242e-144">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c242e-144">-RecoveryPlan</span></span>
<span data-ttu-id="c242e-145">Указывает объект плана восстановления ASR, соответствующий плану восстановления, для которого необходимо выполнить отдействие.</span><span class="sxs-lookup"><span data-stu-id="c242e-145">Specifies the ASR Recovery plan object corresponding to the recovery plan to be failed over.</span></span>

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

### <span data-ttu-id="c242e-146">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c242e-146">-ReplicationProtectedItem</span></span>
<span data-ttu-id="c242e-147">Указывает объект элемента, защищенного репликацией ASR, соответствующий элементу, защищенному репликацией, для которого требуется отдавать отказ.</span><span class="sxs-lookup"><span data-stu-id="c242e-147">Specifies the ASR replication protected item object corresponding to the replication protected item to be failed over.</span></span>

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

### <span data-ttu-id="c242e-148">-ServicesProvider</span><span class="sxs-lookup"><span data-stu-id="c242e-148">-ServicesProvider</span></span>
<span data-ttu-id="c242e-149">Определяет узел, на котором будет создаваться виртуальная машина при сбое в другом расположении, указав объект поставщика служб ASR, соответствующий поставщику служб ASR, запущенному на узле.</span><span class="sxs-lookup"><span data-stu-id="c242e-149">Identifies the host to on which to create the virtual machine while failing over to an alternate location by specifying the ASR services provider object corresponding to the ASR services provider running on the host.</span></span>

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

### <span data-ttu-id="c242e-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c242e-150">-WhatIf</span></span>
<span data-ttu-id="c242e-151">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c242e-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c242e-152">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c242e-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c242e-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c242e-153">CommonParameters</span></span>
<span data-ttu-id="c242e-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c242e-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c242e-155">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c242e-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c242e-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c242e-156">INPUTS</span></span>

### <span data-ttu-id="c242e-157">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="c242e-157">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="c242e-158">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="c242e-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="c242e-159">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c242e-159">OUTPUTS</span></span>

### <span data-ttu-id="c242e-160">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="c242e-160">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c242e-161">Пуск</span><span class="sxs-lookup"><span data-stu-id="c242e-161">NOTES</span></span>

## <span data-ttu-id="c242e-162">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c242e-162">RELATED LINKS</span></span>
