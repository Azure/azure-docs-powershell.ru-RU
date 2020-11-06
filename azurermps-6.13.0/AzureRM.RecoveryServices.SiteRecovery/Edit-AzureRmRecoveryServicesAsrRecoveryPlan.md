---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/edit-azurermrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Edit-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Edit-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: f60da52bffcc78e563863c79971beea8d45e398e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566429"
---
# <span data-ttu-id="f7d5e-101">Edit-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f7d5e-101">Edit-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="f7d5e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f7d5e-102">SYNOPSIS</span></span>
<span data-ttu-id="f7d5e-103">Изменение плана восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="f7d5e-103">Edits a Site Recovery plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7d5e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f7d5e-104">SYNTAX</span></span>

### <span data-ttu-id="f7d5e-105">AppendGroup (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f7d5e-105">AppendGroup (Default)</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> [-AppendGroup]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7d5e-106">RemoveGroup</span><span class="sxs-lookup"><span data-stu-id="f7d5e-106">RemoveGroup</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -RemoveGroup <ASRRecoveryPlanGroup>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7d5e-107">AddReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="f7d5e-107">AddReplicationProtectedItems</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -AddProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7d5e-108">RemoveReplicationProtectedItems</span><span class="sxs-lookup"><span data-stu-id="f7d5e-108">RemoveReplicationProtectedItems</span></span>
```
Edit-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> -Group <ASRRecoveryPlanGroup>
 -RemoveProtectedItem <ASRReplicationProtectedItem[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7d5e-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7d5e-109">DESCRIPTION</span></span>
<span data-ttu-id="f7d5e-110">Командлет **Edit-AzureRmRecoveryServicesAsrRecoveryPlan** редактирует план восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="f7d5e-110">The **Edit-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet edits an Azure Site Recovery plan.</span></span>

## <span data-ttu-id="f7d5e-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f7d5e-111">EXAMPLES</span></span>

### <span data-ttu-id="f7d5e-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f7d5e-112">Example 1</span></span>
```
PS C:\> $RP = Edit-AzureRmRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP -AppendGroup
```

<span data-ttu-id="f7d5e-113">Добавляет группу в существующий план восстановления Azure Site Recovery и возвращает обновленный план восстановления из памяти.</span><span class="sxs-lookup"><span data-stu-id="f7d5e-113">Appends a group to existing Azure Site Recovery recovery plan and returns the in-memory updated recovery plan.</span></span> 

## <span data-ttu-id="f7d5e-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f7d5e-114">PARAMETERS</span></span>

### <span data-ttu-id="f7d5e-115">-AddProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f7d5e-115">-AddProtectedItem</span></span>
<span data-ttu-id="f7d5e-116">Список элементов, защищенных репликацией ASR, добавляемых в группу плана восстановления в объекте плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="f7d5e-116">List of ASR replication protected items to be added to the recovery plan group in the recovery plan object.</span></span>

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

### <span data-ttu-id="f7d5e-117">-AppendGroup</span><span class="sxs-lookup"><span data-stu-id="f7d5e-117">-AppendGroup</span></span>
<span data-ttu-id="f7d5e-118">Параметр переключить, чтобы добавить группу плана восстановления в объект плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="f7d5e-118">Switch parameter to append a recovery plan group to the recovery plan object.</span></span>

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

### <span data-ttu-id="f7d5e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7d5e-119">-DefaultProfile</span></span>
<span data-ttu-id="f7d5e-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f7d5e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7d5e-121">-Группа</span><span class="sxs-lookup"><span data-stu-id="f7d5e-121">-Group</span></span>
<span data-ttu-id="f7d5e-122">Указывает группу планов восстановления.</span><span class="sxs-lookup"><span data-stu-id="f7d5e-122">Specifies a recovery plan group.</span></span>

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

### <span data-ttu-id="f7d5e-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f7d5e-123">-InputObject</span></span>
<span data-ttu-id="f7d5e-124">Редактируемый объект плана восстановления ASR (в операции с памятью).</span><span class="sxs-lookup"><span data-stu-id="f7d5e-124">The ASR recovery plan object to be edited (In memory operation.</span></span> <span data-ttu-id="f7d5e-125">Чтобы обновить Update-AzureRmASRRecoveryPlan выполнения плана восстановления с измененным объектом плана восстановления.)</span><span class="sxs-lookup"><span data-stu-id="f7d5e-125">To update the recovery plan run Update-AzureRmASRRecoveryPlan with the edited recovery plan object.)</span></span>

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

### <span data-ttu-id="f7d5e-126">-RemoveGroup</span><span class="sxs-lookup"><span data-stu-id="f7d5e-126">-RemoveGroup</span></span>
<span data-ttu-id="f7d5e-127">Удаляет указанную группу из объекта плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="f7d5e-127">Removes the specified group from the recovery plan object.</span></span>

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

### <span data-ttu-id="f7d5e-128">-RemoveProtectedItem</span><span class="sxs-lookup"><span data-stu-id="f7d5e-128">-RemoveProtectedItem</span></span>
<span data-ttu-id="f7d5e-129">Список защищенных элементов для репликации ASR, которые нужно удалить из группы плана восстановления в объекте плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="f7d5e-129">List of ASR replication protected items to be removed from the recovery plan group in the recovery plan object.</span></span>

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

### <span data-ttu-id="f7d5e-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f7d5e-130">-Confirm</span></span>
<span data-ttu-id="f7d5e-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f7d5e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7d5e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7d5e-132">-WhatIf</span></span>
<span data-ttu-id="f7d5e-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f7d5e-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f7d5e-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f7d5e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7d5e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7d5e-135">CommonParameters</span></span>
<span data-ttu-id="f7d5e-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f7d5e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7d5e-137">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7d5e-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7d5e-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f7d5e-138">INPUTS</span></span>

### <span data-ttu-id="f7d5e-139">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f7d5e-139">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="f7d5e-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f7d5e-140">OUTPUTS</span></span>

### <span data-ttu-id="f7d5e-141">System. Object</span><span class="sxs-lookup"><span data-stu-id="f7d5e-141">System.Object</span></span>

## <span data-ttu-id="f7d5e-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="f7d5e-142">NOTES</span></span>

## <span data-ttu-id="f7d5e-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f7d5e-143">RELATED LINKS</span></span>

[<span data-ttu-id="f7d5e-144">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f7d5e-144">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="f7d5e-145">New-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f7d5e-145">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)
