---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrPlannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrPlannedFailoverJob.md
ms.openlocfilehash: e5864271e96add95624f857357defdea3039c7a8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93912708"
---
# <span data-ttu-id="11985-101">Start-AzRecoveryServicesAsrPlannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="11985-101">Start-AzRecoveryServicesAsrPlannedFailoverJob</span></span>

## <span data-ttu-id="11985-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="11985-102">SYNOPSIS</span></span>
<span data-ttu-id="11985-103">Запускает плановую операцию отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="11985-103">Starts a planned failover operation.</span></span>

## <span data-ttu-id="11985-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="11985-104">SYNTAX</span></span>

### <span data-ttu-id="11985-105">ByRPIObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="11985-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrPlannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-Optimize <String>] [-CreateVmIfNotFound <String>]
 [-ServicesProvider <ASRRecoveryServicesProvider>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="11985-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="11985-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="11985-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="11985-107">DESCRIPTION</span></span>
<span data-ttu-id="11985-108">Командлет **Start-AzRecoveryServicesAsrPlannedFailoverJob** запускает плановую отработку отказа для защищенного элемента или плана восстановления для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="11985-108">The **Start-AzRecoveryServicesAsrPlannedFailoverJob** cmdlet starts a planned failover for an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="11985-109">С помощью командлета Get-AzRecoveryServicesAsrJob можно проверить, успешно ли прошло задание.</span><span class="sxs-lookup"><span data-stu-id="11985-109">You can check whether the job succeeds by using the Get-AzRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="11985-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="11985-110">EXAMPLES</span></span>

### <span data-ttu-id="11985-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="11985-111">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="11985-112">Запускает плановую отработку отказа для указанного плана восстановления ASR и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="11985-112">Starts the planned failover for the specified ASR recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="11985-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="11985-113">PARAMETERS</span></span>

### <span data-ttu-id="11985-114">-CreateVmIfNotFound</span><span class="sxs-lookup"><span data-stu-id="11985-114">-CreateVmIfNotFound</span></span>
<span data-ttu-id="11985-115">Создание виртуальной машины, если она не была найдена при сбое в первичном регионе (используется в восстановлении альтернативных местоположений). Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="11985-115">Create the virtual machine if not found while failing back to the primary region (used in alternate location recovery.) The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="11985-116">Кнопки</span><span class="sxs-lookup"><span data-stu-id="11985-116">Yes</span></span>
- <span data-ttu-id="11985-117">Нет</span><span class="sxs-lookup"><span data-stu-id="11985-117">No</span></span>

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

### <span data-ttu-id="11985-118">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="11985-118">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="11985-119">Задает основной файл сертификата.</span><span class="sxs-lookup"><span data-stu-id="11985-119">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="11985-120">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="11985-120">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="11985-121">Задает вторичный файл сертификата.</span><span class="sxs-lookup"><span data-stu-id="11985-121">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="11985-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11985-122">-DefaultProfile</span></span>
<span data-ttu-id="11985-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="11985-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="11985-124">-Направление</span><span class="sxs-lookup"><span data-stu-id="11985-124">-Direction</span></span>
<span data-ttu-id="11985-125">Указывает направление отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="11985-125">Specifies the direction of the failover.</span></span>
<span data-ttu-id="11985-126">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="11985-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="11985-127">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="11985-127">PrimaryToRecovery</span></span>
- <span data-ttu-id="11985-128">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="11985-128">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="11985-129">-OPTIMIZE</span><span class="sxs-lookup"><span data-stu-id="11985-129">-Optimize</span></span>
<span data-ttu-id="11985-130">Указывает, для чего нужно оптимизировать.</span><span class="sxs-lookup"><span data-stu-id="11985-130">Specifies what to optimize for.</span></span>
<span data-ttu-id="11985-131">Этот параметр применяется в том случае, если отработка отказа выполняется с сайта Azure на локальном сайте, требующем значительную синхронизацию данных.</span><span class="sxs-lookup"><span data-stu-id="11985-131">This parameter applies when failover is done from an Azure site to an on-premise site which requires substantial data synchronization.</span></span>
<span data-ttu-id="11985-132">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="11985-132">Valid values are:</span></span>

- <span data-ttu-id="11985-133">ForDowntime</span><span class="sxs-lookup"><span data-stu-id="11985-133">ForDowntime</span></span>
- <span data-ttu-id="11985-134">ForSynchronization</span><span class="sxs-lookup"><span data-stu-id="11985-134">ForSynchronization</span></span>

<span data-ttu-id="11985-135">Если указан **ForDowntime** , это указывает на то, что данные синхронизируются перед переходом на другой ресурс для минимизации простоев.</span><span class="sxs-lookup"><span data-stu-id="11985-135">When **ForDowntime** is specified, this indicates that data is synchronized before failover to minimize downtime.</span></span>
<span data-ttu-id="11985-136">Синхронизация выполняется без выключения виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="11985-136">Synchronization is performed without shutting down the virtual machine.</span></span>
<span data-ttu-id="11985-137">После завершения синхронизации задание будет приостановлено.</span><span class="sxs-lookup"><span data-stu-id="11985-137">After synchronization is complete, the job is suspended.</span></span>
<span data-ttu-id="11985-138">Возобновите задачу, чтобы выполнить дополнительную операцию синхронизации, которая завершает работу виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="11985-138">Resume the job to do an additional synchronization operation that shuts down the virtual machine.</span></span>

<span data-ttu-id="11985-139">Если указан **ForSynchronization** , это указывает на то, что данные синхронизируются во время отработки отказа, поэтому синхронизация данных свернута.</span><span class="sxs-lookup"><span data-stu-id="11985-139">When **ForSynchronization** is specified, this indicates that data is synchronized during failover only so data synchronization is minimized.</span></span>
<span data-ttu-id="11985-140">Если этот параметр включен, виртуальная машина немедленно завершает работу.</span><span class="sxs-lookup"><span data-stu-id="11985-140">With this setting enabled, the virtual machine is shut down immediately.</span></span>
<span data-ttu-id="11985-141">Синхронизация начинается после завершения работы, чтобы завершить операцию отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="11985-141">Synchronization starts after shutdown to complete the failover operation.</span></span>

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

### <span data-ttu-id="11985-142">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="11985-142">-RecoveryPlan</span></span>
<span data-ttu-id="11985-143">Указывает объект плана восстановления ASR, соответствующий плану восстановления, для которого необходимо выполнить отдействие.</span><span class="sxs-lookup"><span data-stu-id="11985-143">Specifies the ASR Recovery plan object corresponding to the recovery plan to be failed over.</span></span>

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

### <span data-ttu-id="11985-144">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="11985-144">-ReplicationProtectedItem</span></span>
<span data-ttu-id="11985-145">Указывает объект элемента, защищенного репликацией ASR, соответствующий элементу, защищенному репликацией, для которого требуется отдавать отказ.</span><span class="sxs-lookup"><span data-stu-id="11985-145">Specifies the ASR replication protected item object corresponding to the replication protected item to be failed over.</span></span>

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

### <span data-ttu-id="11985-146">-ServicesProvider</span><span class="sxs-lookup"><span data-stu-id="11985-146">-ServicesProvider</span></span>
<span data-ttu-id="11985-147">Определяет узел, на котором будет создаваться виртуальная машина при сбое в другом расположении, указав объект поставщика служб ASR, соответствующий поставщику служб ASR, запущенному на узле.</span><span class="sxs-lookup"><span data-stu-id="11985-147">Identifies the host to on which to create the virtual machine while failing over to an alternate location by specifying the ASR services provider object corresponding to the ASR services provider running on the host.</span></span>

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

### <span data-ttu-id="11985-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="11985-148">-Confirm</span></span>
<span data-ttu-id="11985-149">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="11985-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11985-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11985-150">-WhatIf</span></span>
<span data-ttu-id="11985-151">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="11985-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="11985-152">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="11985-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11985-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11985-153">CommonParameters</span></span>
<span data-ttu-id="11985-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="11985-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11985-155">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="11985-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11985-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="11985-156">INPUTS</span></span>

### <span data-ttu-id="11985-157">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="11985-157">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="11985-158">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="11985-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="11985-159">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="11985-159">OUTPUTS</span></span>

### <span data-ttu-id="11985-160">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="11985-160">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="11985-161">Пуск</span><span class="sxs-lookup"><span data-stu-id="11985-161">NOTES</span></span>

## <span data-ttu-id="11985-162">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="11985-162">RELATED LINKS</span></span>
