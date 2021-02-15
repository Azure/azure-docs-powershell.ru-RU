---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrPlannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrPlannedFailoverJob.md
ms.openlocfilehash: e5864271e96add95624f857357defdea3039c7a8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100225316"
---
# <span data-ttu-id="efaf9-101">Start-AzRecoveryServicesAsrPlannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="efaf9-101">Start-AzRecoveryServicesAsrPlannedFailoverJob</span></span>

## <span data-ttu-id="efaf9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efaf9-102">SYNOPSIS</span></span>
<span data-ttu-id="efaf9-103">Начало запланированной отбойной операции.</span><span class="sxs-lookup"><span data-stu-id="efaf9-103">Starts a planned failover operation.</span></span>

## <span data-ttu-id="efaf9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="efaf9-104">SYNTAX</span></span>

### <span data-ttu-id="efaf9-105">ByRPIObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="efaf9-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrPlannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-Optimize <String>] [-CreateVmIfNotFound <String>]
 [-ServicesProvider <ASRRecoveryServicesProvider>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="efaf9-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="efaf9-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-Optimize <String>] [-CreateVmIfNotFound <String>] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="efaf9-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="efaf9-107">DESCRIPTION</span></span>
<span data-ttu-id="efaf9-108">Для защищенного элемента или плана восстановления сайта Azure запускается запланированный отбой для **start-AzRecoveryServicesAsrPlannedFailoverJob.**</span><span class="sxs-lookup"><span data-stu-id="efaf9-108">The **Start-AzRecoveryServicesAsrPlannedFailoverJob** cmdlet starts a planned failover for an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="efaf9-109">Вы можете проверить, успешно ли задание, с помощью Get-AzRecoveryServicesAsrJob управления.</span><span class="sxs-lookup"><span data-stu-id="efaf9-109">You can check whether the job succeeds by using the Get-AzRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="efaf9-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="efaf9-110">EXAMPLES</span></span>

### <span data-ttu-id="efaf9-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="efaf9-111">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzRecoveryServicesAsrPlannedFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="efaf9-112">Запускает запланированный отбой для указанного плана восстановления ASR и возвращает задание ASR, используемую для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="efaf9-112">Starts the planned failover for the specified ASR recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="efaf9-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="efaf9-113">PARAMETERS</span></span>

### <span data-ttu-id="efaf9-114">-CreateVmIfNotFound</span><span class="sxs-lookup"><span data-stu-id="efaf9-114">-CreateVmIfNotFound</span></span>
<span data-ttu-id="efaf9-115">Создайте виртуальную машину, если она не найдена при сбое обратно в основной регион (используется при альтернативном восстановлении расположения). Допустимые значения этого параметра:</span><span class="sxs-lookup"><span data-stu-id="efaf9-115">Create the virtual machine if not found while failing back to the primary region (used in alternate location recovery.) The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="efaf9-116">Да</span><span class="sxs-lookup"><span data-stu-id="efaf9-116">Yes</span></span>
- <span data-ttu-id="efaf9-117">Нет</span><span class="sxs-lookup"><span data-stu-id="efaf9-117">No</span></span>

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

### <span data-ttu-id="efaf9-118">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="efaf9-118">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="efaf9-119">Указывает основной файл сертификата.</span><span class="sxs-lookup"><span data-stu-id="efaf9-119">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="efaf9-120">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="efaf9-120">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="efaf9-121">Определяет дополнительный файл сертификата.</span><span class="sxs-lookup"><span data-stu-id="efaf9-121">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="efaf9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efaf9-122">-DefaultProfile</span></span>
<span data-ttu-id="efaf9-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="efaf9-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="efaf9-124">-Direction</span><span class="sxs-lookup"><span data-stu-id="efaf9-124">-Direction</span></span>
<span data-ttu-id="efaf9-125">Определяет направление отбойного пути.</span><span class="sxs-lookup"><span data-stu-id="efaf9-125">Specifies the direction of the failover.</span></span>
<span data-ttu-id="efaf9-126">Допустимыми значениями для этого параметра являются:</span><span class="sxs-lookup"><span data-stu-id="efaf9-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="efaf9-127">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="efaf9-127">PrimaryToRecovery</span></span>
- <span data-ttu-id="efaf9-128">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="efaf9-128">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="efaf9-129">-Optimize</span><span class="sxs-lookup"><span data-stu-id="efaf9-129">-Optimize</span></span>
<span data-ttu-id="efaf9-130">Определяет, для чего нужно оптимизировать.</span><span class="sxs-lookup"><span data-stu-id="efaf9-130">Specifies what to optimize for.</span></span>
<span data-ttu-id="efaf9-131">Этот параметр применяется, если от с сайта Azure к локальному сайту требуется существенный синхронизированный доступ к данным.</span><span class="sxs-lookup"><span data-stu-id="efaf9-131">This parameter applies when failover is done from an Azure site to an on-premise site which requires substantial data synchronization.</span></span>
<span data-ttu-id="efaf9-132">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="efaf9-132">Valid values are:</span></span>

- <span data-ttu-id="efaf9-133">ForDowntime</span><span class="sxs-lookup"><span data-stu-id="efaf9-133">ForDowntime</span></span>
- <span data-ttu-id="efaf9-134">ForSynchronization</span><span class="sxs-lookup"><span data-stu-id="efaf9-134">ForSynchronization</span></span>

<span data-ttu-id="efaf9-135">Если **задан forDowntime,** это означает, что данные синхронизируются до отключения, чтобы свести к минимуму простои.</span><span class="sxs-lookup"><span data-stu-id="efaf9-135">When **ForDowntime** is specified, this indicates that data is synchronized before failover to minimize downtime.</span></span>
<span data-ttu-id="efaf9-136">Синхронизация выполняется без выключения виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="efaf9-136">Synchronization is performed without shutting down the virtual machine.</span></span>
<span data-ttu-id="efaf9-137">После завершения синхронизации задание приостанавлизируется.</span><span class="sxs-lookup"><span data-stu-id="efaf9-137">After synchronization is complete, the job is suspended.</span></span>
<span data-ttu-id="efaf9-138">Возобновление работы для дополнительной операции синхронизации, которая закрывает виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="efaf9-138">Resume the job to do an additional synchronization operation that shuts down the virtual machine.</span></span>

<span data-ttu-id="efaf9-139">Если **задана синхронизация ForSynchronization,** это означает, что данные синхронизируются только во время отбойной передачи, чтобы свернуть синхронизацию данных.</span><span class="sxs-lookup"><span data-stu-id="efaf9-139">When **ForSynchronization** is specified, this indicates that data is synchronized during failover only so data synchronization is minimized.</span></span>
<span data-ttu-id="efaf9-140">Если этот параметр включен, виртуальная машины сразу же отключится.</span><span class="sxs-lookup"><span data-stu-id="efaf9-140">With this setting enabled, the virtual machine is shut down immediately.</span></span>
<span data-ttu-id="efaf9-141">Синхронизация начинается после завершения отключения.</span><span class="sxs-lookup"><span data-stu-id="efaf9-141">Synchronization starts after shutdown to complete the failover operation.</span></span>

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

### <span data-ttu-id="efaf9-142">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="efaf9-142">-RecoveryPlan</span></span>
<span data-ttu-id="efaf9-143">Указывает объект для плана восстановления ASR, соответствующий плану восстановления, для который нужно сбой.</span><span class="sxs-lookup"><span data-stu-id="efaf9-143">Specifies the ASR Recovery plan object corresponding to the recovery plan to be failed over.</span></span>

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

### <span data-ttu-id="efaf9-144">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="efaf9-144">-ReplicationProtectedItem</span></span>
<span data-ttu-id="efaf9-145">Определяет объект, защищенный репликацией ASR, соответствующий элементу, защищенного репликацией.</span><span class="sxs-lookup"><span data-stu-id="efaf9-145">Specifies the ASR replication protected item object corresponding to the replication protected item to be failed over.</span></span>

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

### <span data-ttu-id="efaf9-146">-ServicesProvider</span><span class="sxs-lookup"><span data-stu-id="efaf9-146">-ServicesProvider</span></span>
<span data-ttu-id="efaf9-147">Определяет хост, на котором нужно создать виртуальную машину, при сбое перенастройки в альтернативное расположение, указав объект поставщика служб ASR, соответствующий поставщику служб ASR, запущенного на этом хосте.</span><span class="sxs-lookup"><span data-stu-id="efaf9-147">Identifies the host to on which to create the virtual machine while failing over to an alternate location by specifying the ASR services provider object corresponding to the ASR services provider running on the host.</span></span>

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

### <span data-ttu-id="efaf9-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="efaf9-148">-Confirm</span></span>
<span data-ttu-id="efaf9-149">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="efaf9-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="efaf9-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="efaf9-150">-WhatIf</span></span>
<span data-ttu-id="efaf9-151">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="efaf9-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="efaf9-152">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="efaf9-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="efaf9-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efaf9-153">CommonParameters</span></span>
<span data-ttu-id="efaf9-154">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efaf9-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efaf9-155">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="efaf9-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efaf9-156">INPUTS</span><span class="sxs-lookup"><span data-stu-id="efaf9-156">INPUTS</span></span>

### <span data-ttu-id="efaf9-157">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="efaf9-157">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="efaf9-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="efaf9-158">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="efaf9-159">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="efaf9-159">OUTPUTS</span></span>

### <span data-ttu-id="efaf9-160">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="efaf9-160">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="efaf9-161">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="efaf9-161">NOTES</span></span>

## <span data-ttu-id="efaf9-162">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="efaf9-162">RELATED LINKS</span></span>
