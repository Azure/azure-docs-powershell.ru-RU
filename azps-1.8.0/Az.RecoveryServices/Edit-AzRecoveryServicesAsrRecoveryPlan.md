---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/edit-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Edit-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Edit-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: cac83004dc56b8d32acacced0339068a1fd932f4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729752"
---
# <span data-ttu-id="5a51d-101">Edit-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="5a51d-101">Edit-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="5a51d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5a51d-102">SYNOPSIS</span></span>
<span data-ttu-id="5a51d-103">Изменение плана восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="5a51d-103">Edits a Site Recovery plan.</span></span>

## <span data-ttu-id="5a51d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5a51d-104">SYNTAX</span></span>

### <span data-ttu-id="5a51d-105">AppendGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5a51d-105">AppendGroup (Default)</span></span>
```
Edit-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> [-AppendGroup]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a51d-106">RemoveGroup</span><span class="sxs-lookup"><span data-stu-id="5a51d-106">RemoveGroup</span></span>
```
Edit-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -RemoveGroup <ASRRecoveryPlanGroup>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a51d-107">AddReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="5a51d-107">AddReplicationProtectedItems</span></span>
```
Edit-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -AddProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a51d-108">RemoveReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="5a51d-108">RemoveReplicationProtectedItems</span></span>
```
Edit-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -RemoveProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a51d-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5a51d-109">DESCRIPTION</span></span>
<span data-ttu-id="5a51d-110">Командлет **Edit-AzRecoveryServicesAsrRecoveryPlan** редактирует план восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="5a51d-110">The **Edit-AzRecoveryServicesAsrRecoveryPlan** cmdlet edits an Azure Site Recovery plan.</span></span>

## <span data-ttu-id="5a51d-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5a51d-111">EXAMPLES</span></span>

### <span data-ttu-id="5a51d-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5a51d-112">Example 1</span></span>
```
PS C:\> $RP = Edit-AzRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP -AppendGroup
```

<span data-ttu-id="5a51d-113">Добавляет группу в существующий план восстановления Azure Site Recovery и возвращает обновленный план восстановления из памяти.</span><span class="sxs-lookup"><span data-stu-id="5a51d-113">Appends a group to existing Azure Site Recovery recovery plan and returns the in-memory updated recovery plan.</span></span> 

## <span data-ttu-id="5a51d-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5a51d-114">PARAMETERS</span></span>

### <span data-ttu-id="5a51d-115">-AddProtectedItem</span><span class="sxs-lookup"><span data-stu-id="5a51d-115">-AddProtectedItem</span></span>
<span data-ttu-id="5a51d-116">Список элементов, защищенных репликацией ASR, добавляемых в группу плана восстановления в объекте плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="5a51d-116">List of ASR replication protected items to be added to the recovery plan group in the recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: AddReplicationProtectedItems
Aliases: AddProtectedItems

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a51d-117">-AppendGroup</span><span class="sxs-lookup"><span data-stu-id="5a51d-117">-AppendGroup</span></span>
<span data-ttu-id="5a51d-118">Параметр переключить, чтобы добавить группу плана восстановления в объект плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="5a51d-118">Switch parameter to append a recovery plan group to the recovery plan object.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AppendGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a51d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a51d-119">-DefaultProfile</span></span>
<span data-ttu-id="5a51d-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5a51d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="5a51d-121">-Группа</span><span class="sxs-lookup"><span data-stu-id="5a51d-121">-Group</span></span>
<span data-ttu-id="5a51d-122">Указывает группу планов восстановления.</span><span class="sxs-lookup"><span data-stu-id="5a51d-122">Specifies a recovery plan group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlanGroup
Parameter Sets: AddReplicationProtectedItems, RemoveReplicationProtectedItems
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a51d-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a51d-123">-InputObject</span></span>
<span data-ttu-id="5a51d-124">Редактируемый объект плана восстановления ASR (в операции с памятью).</span><span class="sxs-lookup"><span data-stu-id="5a51d-124">The ASR recovery plan object to be edited (In memory operation.</span></span> <span data-ttu-id="5a51d-125">Чтобы обновить Update-AzASRRecoveryPlan выполнения плана восстановления с измененным объектом плана восстановления.)</span><span class="sxs-lookup"><span data-stu-id="5a51d-125">To update the recovery plan run Update-AzASRRecoveryPlan with the edited recovery plan object.)</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: (All)
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a51d-126">-RemoveGroup</span><span class="sxs-lookup"><span data-stu-id="5a51d-126">-RemoveGroup</span></span>
<span data-ttu-id="5a51d-127">Удаляет указанную группу из объекта плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="5a51d-127">Removes the specified group from the recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlanGroup
Parameter Sets: RemoveGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a51d-128">-RemoveProtectedItem</span><span class="sxs-lookup"><span data-stu-id="5a51d-128">-RemoveProtectedItem</span></span>
<span data-ttu-id="5a51d-129">Список защищенных элементов для репликации ASR, которые нужно удалить из группы плана восстановления в объекте плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="5a51d-129">List of ASR replication protected items to be removed from the recovery plan group in the recovery plan object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem[]
Parameter Sets: RemoveReplicationProtectedItems
Aliases: RemoveProtectedItems

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a51d-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5a51d-130">-Confirm</span></span>
<span data-ttu-id="5a51d-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5a51d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a51d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a51d-132">-WhatIf</span></span>
<span data-ttu-id="5a51d-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5a51d-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5a51d-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5a51d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a51d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a51d-135">CommonParameters</span></span>
<span data-ttu-id="5a51d-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5a51d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a51d-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a51d-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a51d-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5a51d-138">INPUTS</span></span>

### <span data-ttu-id="5a51d-139">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="5a51d-139">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="5a51d-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5a51d-140">OUTPUTS</span></span>

### <span data-ttu-id="5a51d-141">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="5a51d-141">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="5a51d-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="5a51d-142">NOTES</span></span>

## <span data-ttu-id="5a51d-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5a51d-143">RELATED LINKS</span></span>

[<span data-ttu-id="5a51d-144">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="5a51d-144">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="5a51d-145">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="5a51d-145">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)
