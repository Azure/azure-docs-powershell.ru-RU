---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrPlannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrPlannedFailoverJob.md
ms.openlocfilehash: e5864271e96add95624f857357defdea3039c7a8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327981"
---
# <span data-ttu-id="b1335-101">Start-AzRecoveryServicesAsrPlannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="b1335-101">Start-AzRecoveryServicesAsrPlannedFailoverJob</span></span>

## <span data-ttu-id="b1335-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1335-102">SYNOPSIS</span></span>
<span data-ttu-id="b1335-103">Начало запланированной отбойной операции.</span><span class="sxs-lookup"><span data-stu-id="b1335-103">Starts a planned failover operation.</span></span>

## <span data-ttu-id="b1335-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b1335-104">SYNTAX</span></span>

### <span data-ttu-id="b1335-105">ByRPIObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b1335-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrPlannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-Optimize <String>] [-CreateVmIfNotFound <String>]
 [-ServicesProvider <ASRRecoveryServicesProvider>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b1335-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="b1335-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b1335-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b1335-107">DESCRIPTION</span></span>
<span data-ttu-id="b1335-108">Для защищенного элемента или плана восстановления сайта Azure запускается запланированный отбой для **start-AzRecoveryServicesAsrPlannedFailoverJob.**</span><span class="sxs-lookup"><span data-stu-id="b1335-108">The **Start-AzRecoveryServicesAsrPlannedFailoverJob** cmdlet starts a planned failover for an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="b1335-109">Вы можете проверить, успешно ли задание, с помощью Get-AzRecoveryServicesAsrJob управления.</span><span class="sxs-lookup"><span data-stu-id="b1335-109">You can check whether the job succeeds by using the Get-AzRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="b1335-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b1335-110">EXAMPLES</span></span>

### <span data-ttu-id="b1335-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b1335-111">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="b1335-112">Запускает запланированный отбой для указанного плана восстановления ASR и возвращает задание ASR, используемую для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="b1335-112">Starts the planned failover for the specified ASR recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="b1335-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b1335-113">PARAMETERS</span></span>

### <span data-ttu-id="b1335-114">-CreateVmIfNotFound</span><span class="sxs-lookup"><span data-stu-id="b1335-114">-CreateVmIfNotFound</span></span>
<span data-ttu-id="b1335-115">Создайте виртуальную машину, если она не найдена при сбое обратно в основной регион (используется при альтернативном восстановлении расположения). Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="b1335-115">Create the virtual machine if not found while failing back to the primary region (used in alternate location recovery.) The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b1335-116">Да</span><span class="sxs-lookup"><span data-stu-id="b1335-116">Yes</span></span>
- <span data-ttu-id="b1335-117">Нет</span><span class="sxs-lookup"><span data-stu-id="b1335-117">No</span></span>

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

### <span data-ttu-id="b1335-118">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="b1335-118">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="b1335-119">Указывает основной файл сертификата.</span><span class="sxs-lookup"><span data-stu-id="b1335-119">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="b1335-120">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="b1335-120">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="b1335-121">Определяет дополнительный файл сертификата.</span><span class="sxs-lookup"><span data-stu-id="b1335-121">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="b1335-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1335-122">-DefaultProfile</span></span>
<span data-ttu-id="b1335-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b1335-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="b1335-124">-Direction</span><span class="sxs-lookup"><span data-stu-id="b1335-124">-Direction</span></span>
<span data-ttu-id="b1335-125">Определяет направление отбойного пути.</span><span class="sxs-lookup"><span data-stu-id="b1335-125">Specifies the direction of the failover.</span></span>
<span data-ttu-id="b1335-126">Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="b1335-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b1335-127">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="b1335-127">PrimaryToRecovery</span></span>
- <span data-ttu-id="b1335-128">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="b1335-128">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="b1335-129">-Optimize</span><span class="sxs-lookup"><span data-stu-id="b1335-129">-Optimize</span></span>
<span data-ttu-id="b1335-130">Определяет, для чего нужно оптимизировать.</span><span class="sxs-lookup"><span data-stu-id="b1335-130">Specifies what to optimize for.</span></span>
<span data-ttu-id="b1335-131">Этот параметр применяется, если от с сайта Azure к локальному сайту требуется существенный синхронизированный доступ к данным.</span><span class="sxs-lookup"><span data-stu-id="b1335-131">This parameter applies when failover is done from an Azure site to an on-premise site which requires substantial data synchronization.</span></span>
<span data-ttu-id="b1335-132">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="b1335-132">Valid values are:</span></span>

- <span data-ttu-id="b1335-133">ForDowntime</span><span class="sxs-lookup"><span data-stu-id="b1335-133">ForDowntime</span></span>
- <span data-ttu-id="b1335-134">ForSynchronization</span><span class="sxs-lookup"><span data-stu-id="b1335-134">ForSynchronization</span></span>

<span data-ttu-id="b1335-135">Если **задан forDowntime,** это означает, что данные синхронизируются до отключения, чтобы свести к минимуму простои.</span><span class="sxs-lookup"><span data-stu-id="b1335-135">When **ForDowntime** is specified, this indicates that data is synchronized before failover to minimize downtime.</span></span>
<span data-ttu-id="b1335-136">Синхронизация выполняется без выключения виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="b1335-136">Synchronization is performed without shutting down the virtual machine.</span></span>
<span data-ttu-id="b1335-137">После завершения синхронизации задание приостанавлизируется.</span><span class="sxs-lookup"><span data-stu-id="b1335-137">After synchronization is complete, the job is suspended.</span></span>
<span data-ttu-id="b1335-138">Возобновить задание, чтобы еще раз синхронизировать виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="b1335-138">Resume the job to do an additional synchronization operation that shuts down the virtual machine.</span></span>

<span data-ttu-id="b1335-139">Если **задана синхронизация ForSynchronization,** это означает, что данные синхронизируются только во время отбойной передачи, чтобы свернуть синхронизацию данных.</span><span class="sxs-lookup"><span data-stu-id="b1335-139">When **ForSynchronization** is specified, this indicates that data is synchronized during failover only so data synchronization is minimized.</span></span>
<span data-ttu-id="b1335-140">Если этот параметр включен, виртуальная машины сразу же отключится.</span><span class="sxs-lookup"><span data-stu-id="b1335-140">With this setting enabled, the virtual machine is shut down immediately.</span></span>
<span data-ttu-id="b1335-141">Синхронизация начинается после завершения отключения.</span><span class="sxs-lookup"><span data-stu-id="b1335-141">Synchronization starts after shutdown to complete the failover operation.</span></span>

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

### <span data-ttu-id="b1335-142">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b1335-142">-RecoveryPlan</span></span>
<span data-ttu-id="b1335-143">Указывает объект для плана восстановления ASR, соответствующий плану восстановления, для который нужно сбой.</span><span class="sxs-lookup"><span data-stu-id="b1335-143">Specifies the ASR Recovery plan object corresponding to the recovery plan to be failed over.</span></span>

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

### <span data-ttu-id="b1335-144">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="b1335-144">-ReplicationProtectedItem</span></span>
<span data-ttu-id="b1335-145">Определяет объект, защищенный репликацией ASR, соответствующий элементу, защищенного репликацией.</span><span class="sxs-lookup"><span data-stu-id="b1335-145">Specifies the ASR replication protected item object corresponding to the replication protected item to be failed over.</span></span>

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

### <span data-ttu-id="b1335-146">-ServicesProvider</span><span class="sxs-lookup"><span data-stu-id="b1335-146">-ServicesProvider</span></span>
<span data-ttu-id="b1335-147">Определяет хост, на котором нужно создать виртуальную машину, при сбое перенастройки в альтернативное расположение, указав объект поставщика служб ASR, соответствующий поставщику служб ASR, запущенного на этом хосте.</span><span class="sxs-lookup"><span data-stu-id="b1335-147">Identifies the host to on which to create the virtual machine while failing over to an alternate location by specifying the ASR services provider object corresponding to the ASR services provider running on the host.</span></span>

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

### <span data-ttu-id="b1335-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b1335-148">-Confirm</span></span>
<span data-ttu-id="b1335-149">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1335-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1335-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1335-150">-WhatIf</span></span>
<span data-ttu-id="b1335-151">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1335-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b1335-152">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b1335-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1335-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1335-153">CommonParameters</span></span>
<span data-ttu-id="b1335-154">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1335-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1335-155">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b1335-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1335-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b1335-156">INPUTS</span></span>

### <span data-ttu-id="b1335-157">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="b1335-157">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="b1335-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="b1335-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="b1335-159">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b1335-159">OUTPUTS</span></span>

### <span data-ttu-id="b1335-160">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="b1335-160">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="b1335-161">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b1335-161">NOTES</span></span>

## <span data-ttu-id="b1335-162">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b1335-162">RELATED LINKS</span></span>
