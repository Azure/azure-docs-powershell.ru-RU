---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrProtectionDirection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrProtectionDirection.md
ms.openlocfilehash: afa5da5a34954c1e1a610ce9153172934069c2a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733646"
---
# <span data-ttu-id="889df-101">Update-AzureRmRecoveryServicesAsrProtectionDirection</span><span class="sxs-lookup"><span data-stu-id="889df-101">Update-AzureRmRecoveryServicesAsrProtectionDirection</span></span>

## <span data-ttu-id="889df-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="889df-102">SYNOPSIS</span></span>
<span data-ttu-id="889df-103">Обновляет направление репликации для указанного защищенного элемента или плана восстановления для репликации.</span><span class="sxs-lookup"><span data-stu-id="889df-103">Updates the replication direction for the specified replication protected item or recovery plan.</span></span> <span data-ttu-id="889df-104">Используется для повторной защиты или обратной репликации, которая переносит отказ на реплицируемый элемент или план восстановления.</span><span class="sxs-lookup"><span data-stu-id="889df-104">Used to re-protect/reverse replicate a failed over replicated item or recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="889df-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="889df-105">SYNTAX</span></span>

### <span data-ttu-id="889df-106">ByRPIObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="889df-106">ByRPIObject (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="889df-107">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="889df-107">ByRPObject</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="889df-108">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="889df-108">ByPEObject</span></span>
```
Update-AzureRmRecoveryServicesAsrProtectionDirection -Direction <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="889df-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="889df-109">DESCRIPTION</span></span>
<span data-ttu-id="889df-110">Командлет **Update-AzureRmRecoveryServicesAsrProtectionDirection** обновляет направление репликации для указанного объекта Azure Site Recovery после завершения операции фиксации отработки отказа.</span><span class="sxs-lookup"><span data-stu-id="889df-110">The **Update-AzureRmRecoveryServicesAsrProtectionDirection** cmdlet updates the replication direction for the specified Azure Site Recovery object after the completion of a commit failover operation.</span></span>

## <span data-ttu-id="889df-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="889df-111">EXAMPLES</span></span>

### <span data-ttu-id="889df-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="889df-112">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrProtectionDirection -RecoveryPlan $RP -Direction PrimaryToRecovery
```

<span data-ttu-id="889df-113">Начните операцию направления обновления для указанного плана recoveyr и возвращает объект задания ASR, который используется для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="889df-113">Start the update direction operation for the specified recoveyr plan and returns the ASR job object used to track the operation.</span></span>

## <span data-ttu-id="889df-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="889df-114">PARAMETERS</span></span>

### <span data-ttu-id="889df-115">-Направление</span><span class="sxs-lookup"><span data-stu-id="889df-115">-Direction</span></span>
<span data-ttu-id="889df-116">Указывает направление, которое будет использоваться для операции обновления. Опубликуйте отработку отказа.</span><span class="sxs-lookup"><span data-stu-id="889df-116">Specifies the direction to be used for the update operation post a failover.</span></span>  
<span data-ttu-id="889df-117">Для этого параметра допустимы следующие значения:</span><span class="sxs-lookup"><span data-stu-id="889df-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="889df-118">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="889df-118">PrimaryToRecovery</span></span>
- <span data-ttu-id="889df-119">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="889df-119">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="889df-120">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="889df-120">-RecoveryPlan</span></span>
<span data-ttu-id="889df-121">Указывает объект плана восстановления ASR.</span><span class="sxs-lookup"><span data-stu-id="889df-121">Specifies an ASR recovery plan object.</span></span>

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

### <span data-ttu-id="889df-122">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="889df-122">-ReplicationProtectedItem</span></span>
<span data-ttu-id="889df-123">Указывает элемент, защищенный репликацией ASR</span><span class="sxs-lookup"><span data-stu-id="889df-123">Specifies an ASR replication protected item</span></span>

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

### <span data-ttu-id="889df-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="889df-124">-Confirm</span></span>
<span data-ttu-id="889df-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="889df-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="889df-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="889df-126">-WhatIf</span></span>
<span data-ttu-id="889df-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="889df-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="889df-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="889df-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="889df-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="889df-129">CommonParameters</span></span>
<span data-ttu-id="889df-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="889df-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="889df-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="889df-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="889df-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="889df-132">INPUTS</span></span>

### <span data-ttu-id="889df-133">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="889df-133">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>
<span data-ttu-id="889df-134">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="889df-134">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="889df-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="889df-135">OUTPUTS</span></span>

### <span data-ttu-id="889df-136">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="889df-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="889df-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="889df-137">NOTES</span></span>

## <span data-ttu-id="889df-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="889df-138">RELATED LINKS</span></span>

