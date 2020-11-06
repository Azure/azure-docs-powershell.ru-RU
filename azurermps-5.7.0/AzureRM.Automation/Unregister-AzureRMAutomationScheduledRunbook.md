---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: C7C193CF-4E3A-4275-8289-946C99B1C553
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/unregister-azurermautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Unregister-AzureRMAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Unregister-AzureRMAutomationScheduledRunbook.md
ms.openlocfilehash: a8e79dfcd505de6cb1a539f0b194f549835a95f3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567472"
---
# <span data-ttu-id="434ed-101">Unregister-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="434ed-101">Unregister-AzureRmAutomationScheduledRunbook</span></span>

## <span data-ttu-id="434ed-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="434ed-102">SYNOPSIS</span></span>
<span data-ttu-id="434ed-103">Удаляет связь между модулем Runbook и расписанием.</span><span class="sxs-lookup"><span data-stu-id="434ed-103">Removes an association between a runbook and a schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="434ed-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="434ed-104">SYNTAX</span></span>

### <span data-ttu-id="434ed-105">ByJobScheduleId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="434ed-105">ByJobScheduleId (Default)</span></span>
```
Unregister-AzureRmAutomationScheduledRunbook -JobScheduleId <Guid> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="434ed-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="434ed-106">ByRunbookNameAndScheduleName</span></span>
```
Unregister-AzureRmAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="434ed-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="434ed-107">DESCRIPTION</span></span>
<span data-ttu-id="434ed-108">Командлет **Unregister-AzureRmAutomationScheduledRunbook** удаляет связь между Runbook и модулем автоматизации Azure и расписанием.</span><span class="sxs-lookup"><span data-stu-id="434ed-108">The **Unregister-AzureRmAutomationScheduledRunbook** cmdlet removes the association between an Azure Automation runbook and a schedule.</span></span>
<span data-ttu-id="434ed-109">Расписание больше не запускает Runbook.</span><span class="sxs-lookup"><span data-stu-id="434ed-109">The schedule no longer starts the runbook.</span></span>

## <span data-ttu-id="434ed-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="434ed-110">EXAMPLES</span></span>

### <span data-ttu-id="434ed-111">Пример 1: Удаление связи между модулем Runbook и расписанием</span><span class="sxs-lookup"><span data-stu-id="434ed-111">Example 1: Remove the association between a runbook and a schedule</span></span>
```
PS C:\>Unregister-AzureRmAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -ScheduleName "Runbk01Sched"
```

<span data-ttu-id="434ed-112">Эта команда удаляет связь между модулем Runbook с именем Runbk01 и расписанием под названием Runbk01Sched.</span><span class="sxs-lookup"><span data-stu-id="434ed-112">This command removes the association between the runbook named Runbk01 and the schedule named Runbk01Sched.</span></span>

## <span data-ttu-id="434ed-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="434ed-113">PARAMETERS</span></span>

### <span data-ttu-id="434ed-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="434ed-114">-AutomationAccountName</span></span>
<span data-ttu-id="434ed-115">Указывает учетную запись автоматизации для модуля Runbook, на котором работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="434ed-115">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="434ed-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="434ed-116">-DefaultProfile</span></span>
<span data-ttu-id="434ed-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="434ed-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="434ed-118">-Force</span><span class="sxs-lookup"><span data-stu-id="434ed-118">-Force</span></span>
<span data-ttu-id="434ed-119">ps_force</span><span class="sxs-lookup"><span data-stu-id="434ed-119">ps_force</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="434ed-120">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="434ed-120">-JobScheduleId</span></span>
<span data-ttu-id="434ed-121">Указывает идентификатор запланированного Runbook.</span><span class="sxs-lookup"><span data-stu-id="434ed-121">Specifies the ID of a scheduled runbook.</span></span>

```yaml
Type: Guid
Parameter Sets: ByJobScheduleId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="434ed-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="434ed-122">-ResourceGroupName</span></span>
<span data-ttu-id="434ed-123">Указывает имя группы ресурсов для запланированного Runbook.</span><span class="sxs-lookup"><span data-stu-id="434ed-123">Specifies the name of a resource group for the scheduled runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="434ed-124">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="434ed-124">-RunbookName</span></span>
<span data-ttu-id="434ed-125">Указывает имя Runbook, который отменяет этот командлет из расписания.</span><span class="sxs-lookup"><span data-stu-id="434ed-125">Specifies the name of the runbook that this cmdlet dissociates from a schedule.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="434ed-126">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="434ed-126">-ScheduleName</span></span>
<span data-ttu-id="434ed-127">Указывает имя расписания, из которого этот командлет не отменяет Runbook.</span><span class="sxs-lookup"><span data-stu-id="434ed-127">Specifies the name of the schedule from which this cmdlet dissociates a runbook.</span></span>

```yaml
Type: String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="434ed-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="434ed-128">-Confirm</span></span>
<span data-ttu-id="434ed-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="434ed-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="434ed-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="434ed-130">-WhatIf</span></span>
<span data-ttu-id="434ed-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="434ed-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="434ed-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="434ed-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="434ed-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="434ed-133">CommonParameters</span></span>
<span data-ttu-id="434ed-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="434ed-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="434ed-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="434ed-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="434ed-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="434ed-136">INPUTS</span></span>

### <span data-ttu-id="434ed-137">Ничего</span><span class="sxs-lookup"><span data-stu-id="434ed-137">None</span></span>
<span data-ttu-id="434ed-138">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="434ed-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="434ed-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="434ed-139">OUTPUTS</span></span>

## <span data-ttu-id="434ed-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="434ed-140">NOTES</span></span>

## <span data-ttu-id="434ed-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="434ed-141">RELATED LINKS</span></span>

[<span data-ttu-id="434ed-142">Get-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="434ed-142">Get-AzureRmAutomationScheduledRunbook</span></span>](./Get-AzureRMAutomationScheduledRunbook.md)

[<span data-ttu-id="434ed-143">Регистрация — AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="434ed-143">Register-AzureRmAutomationScheduledRunbook</span></span>](./Register-AzureRMAutomationScheduledRunbook.md)


