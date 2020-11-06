---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Edit-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Edit-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 68e06f8a4d9c88b57fa88ee8044ca2e5d04d9ce9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568314"
---
# <span data-ttu-id="9028e-101">Edit-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9028e-101">Edit-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="9028e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9028e-102">SYNOPSIS</span></span>
<span data-ttu-id="9028e-103">Изменение плана восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="9028e-103">Edits a Site Recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9028e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9028e-104">SYNTAX</span></span>

### <span data-ttu-id="9028e-105">AppendGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9028e-105">AppendGroup (Default)</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> [-AppendGroup] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9028e-106">RemoveGroup</span><span class="sxs-lookup"><span data-stu-id="9028e-106">RemoveGroup</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -RemoveGroup <ASRRecoveryPlanGroup>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9028e-107">AddReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="9028e-107">AddReplicationProtectedItems</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -AddProtectedItem <ASRReplicationProtectedItem[]> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9028e-108">RemoveReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="9028e-108">RemoveReplicationProtectedItems</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -RemoveProtectedItem <ASRReplicationProtectedItem[]> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9028e-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9028e-109">DESCRIPTION</span></span>
<span data-ttu-id="9028e-110">Командлет **Edit-AzureRmRecoveryServicesAsrRecoveryPlan** редактирует план восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="9028e-110">The **Edit-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet edits an Azure Site Recovery plan.</span></span>

## <span data-ttu-id="9028e-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9028e-111">EXAMPLES</span></span>

### <span data-ttu-id="9028e-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9028e-112">Example 1</span></span>
```
PS C:\> $RP = Edit-AzureRmRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP -AppendGroup
```

<span data-ttu-id="9028e-113">Добавляет группу в существующий план восстановления Azure Site Recovery и возвращает обновленный план восстановления из памяти.</span><span class="sxs-lookup"><span data-stu-id="9028e-113">Appends a group to existing Azure Site Recovery recovery plan and returns the in-memory updated recovery plan.</span></span> 

## <span data-ttu-id="9028e-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9028e-114">PARAMETERS</span></span>

### <span data-ttu-id="9028e-115">-AddProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9028e-115">-AddProtectedItem</span></span>
<span data-ttu-id="9028e-116">Список элементов, защищенных репликацией ASR, добавляемых в группу плана восстановления в объекте плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="9028e-116">List of ASR replication protected items to be added to the recovery plan group in the recovery plan object.</span></span>

```yaml
Type: ASRReplicationProtectedItem[]
Parameter Sets: AddReplicationProtectedItems
Aliases: AddProtectedItems

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9028e-117">-AppendGroup</span><span class="sxs-lookup"><span data-stu-id="9028e-117">-AppendGroup</span></span>
<span data-ttu-id="9028e-118">Параметр переключить, чтобы добавить группу плана восстановления в объект плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="9028e-118">Switch parameter to append a recovery plan group to the recovery plan object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AppendGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9028e-119">-Группа</span><span class="sxs-lookup"><span data-stu-id="9028e-119">-Group</span></span>
<span data-ttu-id="9028e-120">Указывает группу планов восстановления.</span><span class="sxs-lookup"><span data-stu-id="9028e-120">Specifies a recovery plan group.</span></span>

```yaml
Type: ASRRecoveryPlanGroup
Parameter Sets: AddReplicationProtectedItems, RemoveReplicationProtectedItems
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9028e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9028e-121">-InputObject</span></span>
<span data-ttu-id="9028e-122">Редактируемый объект плана восстановления ASR (в операции с памятью).</span><span class="sxs-lookup"><span data-stu-id="9028e-122">The ASR recovery plan object to be edited (In memory operation.</span></span> <span data-ttu-id="9028e-123">Чтобы обновить Update-AzureRmASRRecoveryPlan выполнения плана восстановления с измененным объектом плана восстановления.)</span><span class="sxs-lookup"><span data-stu-id="9028e-123">To update the recovery plan run Update-AzureRmASRRecoveryPlan with the edited recovery plan object.)</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: (All)
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9028e-124">-RemoveGroup</span><span class="sxs-lookup"><span data-stu-id="9028e-124">-RemoveGroup</span></span>
<span data-ttu-id="9028e-125">Удаляет указанную группу из объекта плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="9028e-125">Removes the specified group from the recovery plan object.</span></span>

```yaml
Type: ASRRecoveryPlanGroup
Parameter Sets: RemoveGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9028e-126">-RemoveProtectedItem</span><span class="sxs-lookup"><span data-stu-id="9028e-126">-RemoveProtectedItem</span></span>
<span data-ttu-id="9028e-127">Список защищенных элементов для репликации ASR, которые нужно удалить из группы плана восстановления в объекте плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="9028e-127">List of ASR replication protected items to be removed from the recovery plan group in the recovery plan object.</span></span>

```yaml
Type: ASRReplicationProtectedItem[]
Parameter Sets: RemoveReplicationProtectedItems
Aliases: RemoveProtectedItems

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9028e-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9028e-128">-Confirm</span></span>
<span data-ttu-id="9028e-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9028e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9028e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9028e-130">-WhatIf</span></span>
<span data-ttu-id="9028e-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9028e-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9028e-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9028e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9028e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9028e-133">CommonParameters</span></span>
<span data-ttu-id="9028e-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9028e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9028e-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9028e-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9028e-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9028e-136">INPUTS</span></span>

### <span data-ttu-id="9028e-137">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9028e-137">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="9028e-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9028e-138">OUTPUTS</span></span>

### <span data-ttu-id="9028e-139">System. Object</span><span class="sxs-lookup"><span data-stu-id="9028e-139">System.Object</span></span>

## <span data-ttu-id="9028e-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="9028e-140">NOTES</span></span>

## <span data-ttu-id="9028e-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9028e-141">RELATED LINKS</span></span>

[<span data-ttu-id="9028e-142">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9028e-142">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="9028e-143">New-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9028e-143">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)
