---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/start-azrecoveryservicesasrunplannedfailoverjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrUnplannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Start-AzRecoveryServicesAsrUnplannedFailoverJob.md
ms.openlocfilehash: a3b2f428f4738a354abfcc006a4e2b7b5ff29514
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94066086"
---
# <span data-ttu-id="8d04d-101">Start-AzRecoveryServicesAsrUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="8d04d-101">Start-AzRecoveryServicesAsrUnplannedFailoverJob</span></span>

## <span data-ttu-id="8d04d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8d04d-102">SYNOPSIS</span></span>
<span data-ttu-id="8d04d-103">Запускает внеплановую операцию отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="8d04d-103">Starts an unplanned failover operation.</span></span>

## <span data-ttu-id="8d04d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8d04d-104">SYNTAX</span></span>

### <span data-ttu-id="8d04d-105">ByRPIObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8d04d-105">ByRPIObject (Default)</span></span>
```
Start-AzRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryPoint <ASRRecoveryPoint>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d04d-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="8d04d-106">ByRPObject</span></span>
```
Start-AzRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-RecoveryTag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d04d-107">ByRPIObjectWithRecoveryTag</span><span class="sxs-lookup"><span data-stu-id="8d04d-107">ByRPIObjectWithRecoveryTag</span></span>
```
Start-AzRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] -RecoveryTag <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d04d-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8d04d-108">DESCRIPTION</span></span>
<span data-ttu-id="8d04d-109">Командлет **Start-AzRecoveryServicesAsrUnplannedFailoverJob** запускает внеплановая отработка отказа защищенного элемента или плана восстановления для Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="8d04d-109">The **Start-AzRecoveryServicesAsrUnplannedFailoverJob** cmdlet starts unplanned failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="8d04d-110">Вы можете проверить, завершилось ли задание успешно с помощью командлета Get-AzRecoveryServicesAsrJob.</span><span class="sxs-lookup"><span data-stu-id="8d04d-110">You can check whether the job succeeded by using the Get-AzRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="8d04d-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8d04d-111">EXAMPLES</span></span>

### <span data-ttu-id="8d04d-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8d04d-112">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery -VMNetwork $RecoveryNetwork
```

<span data-ttu-id="8d04d-113">Запускает незапланированную операцию отработки отказа для плана восстановления с указанными параметрами и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="8d04d-113">Starts the unplanned failover operation for the recovery plan with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="8d04d-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8d04d-114">PARAMETERS</span></span>

### <span data-ttu-id="8d04d-115">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="8d04d-115">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="8d04d-116">Задает путь к файлу основного сертификата для шифрования данных для отработки отказа защищенного элемента.</span><span class="sxs-lookup"><span data-stu-id="8d04d-116">Specifies the data encryption primary certificate file path for failover of Protected Item.</span></span>

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

### <span data-ttu-id="8d04d-117">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="8d04d-117">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="8d04d-118">Указывает путь к вторичному сертификату шифрования данных для отработки отказа защищенного элемента.</span><span class="sxs-lookup"><span data-stu-id="8d04d-118">Specifies the data encryption secondary certificate file path for failover of Protected Item.</span></span>

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

### <span data-ttu-id="8d04d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d04d-119">-DefaultProfile</span></span>
<span data-ttu-id="8d04d-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8d04d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="8d04d-121">-Направление</span><span class="sxs-lookup"><span data-stu-id="8d04d-121">-Direction</span></span>
<span data-ttu-id="8d04d-122">Указывает направление перехода на другой ресурс.</span><span class="sxs-lookup"><span data-stu-id="8d04d-122">Specifies the failover direction.</span></span>
<span data-ttu-id="8d04d-123">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="8d04d-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8d04d-124">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="8d04d-124">PrimaryToRecovery</span></span>
- <span data-ttu-id="8d04d-125">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="8d04d-125">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="8d04d-126">-PerformSourceSideAction</span><span class="sxs-lookup"><span data-stu-id="8d04d-126">-PerformSourceSideAction</span></span>
<span data-ttu-id="8d04d-127">Выполнение операции на стороне источника перед началом внеплановой отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="8d04d-127">Perform operation in source side before starting unplanned failover.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: PerformSourceSideActions

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d04d-128">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="8d04d-128">-RecoveryPlan</span></span>
<span data-ttu-id="8d04d-129">Указывает объект плана восстановления ASR.</span><span class="sxs-lookup"><span data-stu-id="8d04d-129">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="8d04d-130">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="8d04d-130">-RecoveryPoint</span></span>
<span data-ttu-id="8d04d-131">Задает настраиваемую точку восстановления для отработки отказа защищенного компьютера.</span><span class="sxs-lookup"><span data-stu-id="8d04d-131">Specifies a custom recovery point to failover the protected machine to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPoint
Parameter Sets: ByRPIObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d04d-132">-RecoveryTag</span><span class="sxs-lookup"><span data-stu-id="8d04d-132">-RecoveryTag</span></span>
<span data-ttu-id="8d04d-133">Указывает тег восстановления для перехода на другой ресурс.</span><span class="sxs-lookup"><span data-stu-id="8d04d-133">Specifies the recovery tag to failover to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPObject
Aliases:
Accepted values: Latest, LatestAvailable, LatestAvailableApplicationConsistent, LatestAvailableCrashConsistent

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByRPIObjectWithRecoveryTag
Aliases:
Accepted values: Latest, LatestAvailable, LatestAvailableApplicationConsistent, LatestAvailableCrashConsistent

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d04d-134">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8d04d-134">-ReplicationProtectedItem</span></span>
<span data-ttu-id="8d04d-135">Указывает защищенный элемент репликации Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="8d04d-135">Specifies an azure site recovery replication protected item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject, ByRPIObjectWithRecoveryTag
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8d04d-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8d04d-136">-Confirm</span></span>
<span data-ttu-id="8d04d-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8d04d-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d04d-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d04d-138">-WhatIf</span></span>
<span data-ttu-id="8d04d-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8d04d-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8d04d-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8d04d-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d04d-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d04d-141">CommonParameters</span></span>
<span data-ttu-id="8d04d-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8d04d-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d04d-143">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8d04d-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d04d-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8d04d-144">INPUTS</span></span>

### <span data-ttu-id="8d04d-145">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="8d04d-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

### <span data-ttu-id="8d04d-146">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="8d04d-146">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="8d04d-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8d04d-147">OUTPUTS</span></span>

### <span data-ttu-id="8d04d-148">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="8d04d-148">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="8d04d-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="8d04d-149">NOTES</span></span>

## <span data-ttu-id="8d04d-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8d04d-150">RELATED LINKS</span></span>

[<span data-ttu-id="8d04d-151">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="8d04d-151">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)
