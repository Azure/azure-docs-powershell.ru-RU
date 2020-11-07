---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrPlannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrPlannedFailoverJob.md
ms.openlocfilehash: ee39fdfcb40c394bfbd7f1d804d8d9785a63f7c3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729600"
---
# <span data-ttu-id="fb072-101">Start-AzRecoveryServicesAsrPlannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="fb072-101">Start-AzRecoveryServicesAsrPlannedFailoverJob</span></span>

## <span data-ttu-id="fb072-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fb072-102">SYNOPSIS</span></span>
<span data-ttu-id="fb072-103">Запускает плановую операцию отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="fb072-103">Starts a planned failover operation.</span></span>

## <span data-ttu-id="fb072-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fb072-104">SYNTAX</span></span>

### <span data-ttu-id="fb072-105">ByRPIObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fb072-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrPlannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-Optimize <String>] [-CreateVmIfNotFound <String>]
 [-ServicesProvider <ASRRecoveryServicesProvider>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fb072-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="fb072-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fb072-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fb072-107">DESCRIPTION</span></span>
<span data-ttu-id="fb072-108">Командлет **Start-AzRecoveryServicesAsrPlannedFailoverJob** запускает плановую отработку отказа для защищенного элемента или плана восстановления для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="fb072-108">The **Start-AzRecoveryServicesAsrPlannedFailoverJob** cmdlet starts a planned failover for an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="fb072-109">С помощью командлета Get-AzRecoveryServicesAsrJob можно проверить, успешно ли прошло задание.</span><span class="sxs-lookup"><span data-stu-id="fb072-109">You can check whether the job succeeds by using the Get-AzRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="fb072-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fb072-110">EXAMPLES</span></span>

### <span data-ttu-id="fb072-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fb072-111">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="fb072-112">Запускает плановую отработку отказа для указанного плана восстановления ASR и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="fb072-112">Starts the planned failover for the specified ASR recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="fb072-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fb072-113">PARAMETERS</span></span>

### <span data-ttu-id="fb072-114">-CreateVmIfNotFound</span><span class="sxs-lookup"><span data-stu-id="fb072-114">-CreateVmIfNotFound</span></span>
<span data-ttu-id="fb072-115">Создание виртуальной машины, если она не была найдена при сбое в первичном регионе (используется в восстановлении альтернативных местоположений). Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="fb072-115">Create the virtual machine if not found while failing back to the primary region (used in alternate location recovery.) The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fb072-116">Кнопки</span><span class="sxs-lookup"><span data-stu-id="fb072-116">Yes</span></span>
- <span data-ttu-id="fb072-117">Нет</span><span class="sxs-lookup"><span data-stu-id="fb072-117">No</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Yes, No

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb072-118">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="fb072-118">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="fb072-119">Задает основной файл сертификата.</span><span class="sxs-lookup"><span data-stu-id="fb072-119">Specifies the primary certificate file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb072-120">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="fb072-120">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="fb072-121">Задает вторичный файл сертификата.</span><span class="sxs-lookup"><span data-stu-id="fb072-121">Specifies the secondary certificate file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb072-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb072-122">-DefaultProfile</span></span>
<span data-ttu-id="fb072-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fb072-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="fb072-124">-Направление</span><span class="sxs-lookup"><span data-stu-id="fb072-124">-Direction</span></span>
<span data-ttu-id="fb072-125">Указывает направление отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="fb072-125">Specifies the direction of the failover.</span></span>
<span data-ttu-id="fb072-126">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="fb072-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fb072-127">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="fb072-127">PrimaryToRecovery</span></span>
- <span data-ttu-id="fb072-128">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="fb072-128">RecoveryToPrimary</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb072-129">-OPTIMIZE</span><span class="sxs-lookup"><span data-stu-id="fb072-129">-Optimize</span></span>
<span data-ttu-id="fb072-130">Указывает, для чего нужно оптимизировать.</span><span class="sxs-lookup"><span data-stu-id="fb072-130">Specifies what to optimize for.</span></span>
<span data-ttu-id="fb072-131">Этот параметр применяется в том случае, если отработка отказа выполняется с сайта Azure на локальном сайте, требующем значительную синхронизацию данных.</span><span class="sxs-lookup"><span data-stu-id="fb072-131">This parameter applies when failover is done from an Azure site to an on-premise site which requires substantial data synchronization.</span></span>
<span data-ttu-id="fb072-132">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="fb072-132">Valid values are:</span></span>

- <span data-ttu-id="fb072-133">ForDowntime</span><span class="sxs-lookup"><span data-stu-id="fb072-133">ForDowntime</span></span>
- <span data-ttu-id="fb072-134">ForSynchronization</span><span class="sxs-lookup"><span data-stu-id="fb072-134">ForSynchronization</span></span>

<span data-ttu-id="fb072-135">Если указан **ForDowntime** , это указывает на то, что данные синхронизируются перед переходом на другой ресурс для минимизации простоев.</span><span class="sxs-lookup"><span data-stu-id="fb072-135">When **ForDowntime** is specified, this indicates that data is synchronized before failover to minimize downtime.</span></span>
<span data-ttu-id="fb072-136">Синхронизация выполняется без выключения виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="fb072-136">Synchronization is performed without shutting down the virtual machine.</span></span>
<span data-ttu-id="fb072-137">После завершения синхронизации задание будет приостановлено.</span><span class="sxs-lookup"><span data-stu-id="fb072-137">After synchronization is complete, the job is suspended.</span></span>
<span data-ttu-id="fb072-138">Возобновите задачу, чтобы выполнить дополнительную операцию синхронизации, которая завершает работу виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="fb072-138">Resume the job to do an additional synchronization operation that shuts down the virtual machine.</span></span>

<span data-ttu-id="fb072-139">Если указан **ForSynchronization** , это указывает на то, что данные синхронизируются во время отработки отказа, поэтому синхронизация данных свернута.</span><span class="sxs-lookup"><span data-stu-id="fb072-139">When **ForSynchronization** is specified, this indicates that data is synchronized during failover only so data synchronization is minimized.</span></span>
<span data-ttu-id="fb072-140">Если этот параметр включен, виртуальная машина немедленно завершает работу.</span><span class="sxs-lookup"><span data-stu-id="fb072-140">With this setting enabled, the virtual machine is shut down immediately.</span></span>
<span data-ttu-id="fb072-141">Синхронизация начинается после завершения работы, чтобы завершить операцию отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="fb072-141">Synchronization starts after shutdown to complete the failover operation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ForDownTime, ForSynchronization

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb072-142">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="fb072-142">-RecoveryPlan</span></span>
<span data-ttu-id="fb072-143">Указывает объект плана восстановления ASR, соответствующий плану восстановления, для которого необходимо выполнить отдействие.</span><span class="sxs-lookup"><span data-stu-id="fb072-143">Specifies the ASR Recovery plan object corresponding to the recovery plan to be failed over.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb072-144">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="fb072-144">-ReplicationProtectedItem</span></span>
<span data-ttu-id="fb072-145">Указывает объект элемента, защищенного репликацией ASR, соответствующий элементу, защищенному репликацией, для которого требуется отдавать отказ.</span><span class="sxs-lookup"><span data-stu-id="fb072-145">Specifies the ASR replication protected item object corresponding to the replication protected item to be failed over.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fb072-146">-ServicesProvider</span><span class="sxs-lookup"><span data-stu-id="fb072-146">-ServicesProvider</span></span>
<span data-ttu-id="fb072-147">Определяет узел, на котором будет создаваться виртуальная машина при сбое в другом расположении, указав объект поставщика служб ASR, соответствующий поставщику служб ASR, запущенному на узле.</span><span class="sxs-lookup"><span data-stu-id="fb072-147">Identifies the host to on which to create the virtual machine while failing over to an alternate location by specifying the ASR services provider object corresponding to the ASR services provider running on the host.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider
Parameter Sets: ByRPIObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb072-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fb072-148">-Confirm</span></span>
<span data-ttu-id="fb072-149">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fb072-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb072-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb072-150">-WhatIf</span></span>
<span data-ttu-id="fb072-151">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fb072-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fb072-152">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fb072-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb072-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb072-153">CommonParameters</span></span>
<span data-ttu-id="fb072-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fb072-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb072-155">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb072-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb072-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fb072-156">INPUTS</span></span>

### <span data-ttu-id="fb072-157">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="fb072-157">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="fb072-158">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="fb072-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="fb072-159">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fb072-159">OUTPUTS</span></span>

### <span data-ttu-id="fb072-160">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="fb072-160">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="fb072-161">Пуск</span><span class="sxs-lookup"><span data-stu-id="fb072-161">NOTES</span></span>

## <span data-ttu-id="fb072-162">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fb072-162">RELATED LINKS</span></span>
