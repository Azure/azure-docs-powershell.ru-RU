---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob.md
ms.openlocfilehash: 0d619084f62f4cad9b5bd7a9295987681994e53e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733652"
---
# <span data-ttu-id="371b1-101">Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="371b1-101">Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob</span></span>

## <span data-ttu-id="371b1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="371b1-102">SYNOPSIS</span></span>
<span data-ttu-id="371b1-103">Запускает внеплановую операцию отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="371b1-103">Starts an unplanned failover operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="371b1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="371b1-104">SYNTAX</span></span>

### <span data-ttu-id="371b1-105">ByRPIObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="371b1-105">ByRPIObject (Default)</span></span>
```
Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="371b1-106">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="371b1-106">ByRPObject</span></span>
```
Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-PerformSourceSideAction] [-DataEncryptionPrimaryCertFile <String>]
 [-DataEncryptionSecondaryCertFile <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="371b1-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="371b1-107">DESCRIPTION</span></span>
<span data-ttu-id="371b1-108">Командлет **Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob** запускает внеплановую отработку отказа для защищенного элемента или плана восстановления Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="371b1-108">The **Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob** cmdlet starts the unplanned failover of an Azure Site Recovery replication protected item or recovery plan.</span></span>
<span data-ttu-id="371b1-109">С помощью командлета Get-AzureRmRecoveryServicesAsrJob можно проверить, успешно ли прошло задание.</span><span class="sxs-lookup"><span data-stu-id="371b1-109">You can check whether the job succeeds by using the Get-AzureRmRecoveryServicesAsrJob cmdlet.</span></span>

## <span data-ttu-id="371b1-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="371b1-110">EXAMPLES</span></span>

### <span data-ttu-id="371b1-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="371b1-111">Example 1</span></span>
```
PS C:\> $currentJob = Start-AzureRmRecoveryServicesAsrUnplannedFailoverJob -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="371b1-112">Запускает незапланированную операцию отработки отказа для указанного плана восстановления с использованием указанных параметров и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="371b1-112">Starts the unplanned failover operation for the specified recovery plan using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="371b1-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="371b1-113">PARAMETERS</span></span>

### <span data-ttu-id="371b1-114">-DataEncryptionPrimaryCertFile</span><span class="sxs-lookup"><span data-stu-id="371b1-114">-DataEncryptionPrimaryCertFile</span></span>
<span data-ttu-id="371b1-115">Задает основной файл сертификата.</span><span class="sxs-lookup"><span data-stu-id="371b1-115">Specifies the primary certificate file.</span></span>

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

### <span data-ttu-id="371b1-116">-DataEncryptionSecondaryCertFile</span><span class="sxs-lookup"><span data-stu-id="371b1-116">-DataEncryptionSecondaryCertFile</span></span>
<span data-ttu-id="371b1-117">Задает вторичный файл сертификата.</span><span class="sxs-lookup"><span data-stu-id="371b1-117">Specifies the secondary certificate file.</span></span>

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

### <span data-ttu-id="371b1-118">-Направление</span><span class="sxs-lookup"><span data-stu-id="371b1-118">-Direction</span></span>
<span data-ttu-id="371b1-119">Указывает направление отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="371b1-119">Specifies the direction of the failover.</span></span>
<span data-ttu-id="371b1-120">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="371b1-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="371b1-121">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="371b1-121">PrimaryToRecovery</span></span>
- <span data-ttu-id="371b1-122">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="371b1-122">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="371b1-123">-PerformSourceSideAction</span><span class="sxs-lookup"><span data-stu-id="371b1-123">-PerformSourceSideAction</span></span>
<span data-ttu-id="371b1-124">Указывает на то, что при переходе должна выполняться попытка выполнить любые операции сайта, указанные в плане восстановления.</span><span class="sxs-lookup"><span data-stu-id="371b1-124">Indicates that any source site operations specified in the recovery plan must be attempted to be performed as part of the fail over.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: PerformSourceSideActions

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="371b1-125">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="371b1-125">-RecoveryPlan</span></span>
<span data-ttu-id="371b1-126">Указывает объект плана восстановления ASR, соответствующий плану восстановления, на котором необходимо выполнить операцию отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="371b1-126">Specifies an ASR recovery plan object corresponding to the recovery plan on which the failover operation is to be performed.</span></span>

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

### <span data-ttu-id="371b1-127">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="371b1-127">-ReplicationProtectedItem</span></span>
<span data-ttu-id="371b1-128">Указывает объект элемента, защищенного репликацией ASR, соответствующий элементу, защищенному репликацией, для которого требуется выполнить операцию отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="371b1-128">Specifies the ASR replication protected item object corresponding to the replication protected item on which the failover operation is to be performed.</span></span>

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

### <span data-ttu-id="371b1-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="371b1-129">-Confirm</span></span>
<span data-ttu-id="371b1-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="371b1-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="371b1-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="371b1-131">-WhatIf</span></span>
<span data-ttu-id="371b1-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="371b1-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="371b1-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="371b1-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="371b1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="371b1-134">CommonParameters</span></span>
<span data-ttu-id="371b1-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="371b1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="371b1-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="371b1-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="371b1-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="371b1-137">INPUTS</span></span>

### <span data-ttu-id="371b1-138">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="371b1-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="371b1-139">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="371b1-139">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="371b1-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="371b1-140">OUTPUTS</span></span>

### <span data-ttu-id="371b1-141">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="371b1-141">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="371b1-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="371b1-142">NOTES</span></span>

## <span data-ttu-id="371b1-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="371b1-143">RELATED LINKS</span></span>

[<span data-ttu-id="371b1-144">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="371b1-144">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)


