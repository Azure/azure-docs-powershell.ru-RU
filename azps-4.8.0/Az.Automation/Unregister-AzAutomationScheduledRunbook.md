---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: C7C193CF-4E3A-4275-8289-946C99B1C553
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/unregister-azautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationScheduledRunbook.md
ms.openlocfilehash: 53cfa3ccd708871dfe639b0053cb6ab24946bace
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078501"
---
# <span data-ttu-id="75ad2-101">Unregister-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="75ad2-101">Unregister-AzAutomationScheduledRunbook</span></span>

## <span data-ttu-id="75ad2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="75ad2-102">SYNOPSIS</span></span>
<span data-ttu-id="75ad2-103">Удаляет связь между модулем Runbook и расписанием.</span><span class="sxs-lookup"><span data-stu-id="75ad2-103">Removes an association between a runbook and a schedule.</span></span>

## <span data-ttu-id="75ad2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="75ad2-104">SYNTAX</span></span>

### <span data-ttu-id="75ad2-105">ByJobScheduleId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="75ad2-105">ByJobScheduleId (Default)</span></span>
```
Unregister-AzAutomationScheduledRunbook -JobScheduleId <Guid> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="75ad2-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="75ad2-106">ByRunbookNameAndScheduleName</span></span>
```
Unregister-AzAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75ad2-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="75ad2-107">DESCRIPTION</span></span>
<span data-ttu-id="75ad2-108">Командлет **Unregister-AzAutomationScheduledRunbook** удаляет связь между Runbook и модулем автоматизации Azure и расписанием.</span><span class="sxs-lookup"><span data-stu-id="75ad2-108">The **Unregister-AzAutomationScheduledRunbook** cmdlet removes the association between an Azure Automation runbook and a schedule.</span></span>
<span data-ttu-id="75ad2-109">Расписание больше не запускает Runbook.</span><span class="sxs-lookup"><span data-stu-id="75ad2-109">The schedule no longer starts the runbook.</span></span>

## <span data-ttu-id="75ad2-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="75ad2-110">EXAMPLES</span></span>

### <span data-ttu-id="75ad2-111">Пример 1: Удаление связи между модулем Runbook и расписанием</span><span class="sxs-lookup"><span data-stu-id="75ad2-111">Example 1: Remove the association between a runbook and a schedule</span></span>
```
PS C:\>Unregister-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -ScheduleName "Runbk01Sched"
```

<span data-ttu-id="75ad2-112">Эта команда удаляет связь между модулем Runbook с именем Runbk01 и расписанием под названием Runbk01Sched.</span><span class="sxs-lookup"><span data-stu-id="75ad2-112">This command removes the association between the runbook named Runbk01 and the schedule named Runbk01Sched.</span></span>

## <span data-ttu-id="75ad2-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="75ad2-113">PARAMETERS</span></span>

### <span data-ttu-id="75ad2-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="75ad2-114">-AutomationAccountName</span></span>
<span data-ttu-id="75ad2-115">Указывает учетную запись автоматизации для модуля Runbook, на котором работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="75ad2-115">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75ad2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75ad2-116">-DefaultProfile</span></span>
<span data-ttu-id="75ad2-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="75ad2-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="75ad2-118">-Force</span><span class="sxs-lookup"><span data-stu-id="75ad2-118">-Force</span></span>
<span data-ttu-id="75ad2-119">ps_force</span><span class="sxs-lookup"><span data-stu-id="75ad2-119">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75ad2-120">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="75ad2-120">-JobScheduleId</span></span>
<span data-ttu-id="75ad2-121">Указывает идентификатор запланированного Runbook.</span><span class="sxs-lookup"><span data-stu-id="75ad2-121">Specifies the ID of a scheduled runbook.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: ByJobScheduleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75ad2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75ad2-122">-ResourceGroupName</span></span>
<span data-ttu-id="75ad2-123">Указывает имя группы ресурсов для запланированного Runbook.</span><span class="sxs-lookup"><span data-stu-id="75ad2-123">Specifies the name of a resource group for the scheduled runbook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75ad2-124">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="75ad2-124">-RunbookName</span></span>
<span data-ttu-id="75ad2-125">Указывает имя Runbook, который отменяет этот командлет из расписания.</span><span class="sxs-lookup"><span data-stu-id="75ad2-125">Specifies the name of the runbook that this cmdlet dissociates from a schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75ad2-126">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="75ad2-126">-ScheduleName</span></span>
<span data-ttu-id="75ad2-127">Указывает имя расписания, из которого этот командлет не отменяет Runbook.</span><span class="sxs-lookup"><span data-stu-id="75ad2-127">Specifies the name of the schedule from which this cmdlet dissociates a runbook.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75ad2-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="75ad2-128">-Confirm</span></span>
<span data-ttu-id="75ad2-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="75ad2-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75ad2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75ad2-130">-WhatIf</span></span>
<span data-ttu-id="75ad2-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="75ad2-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75ad2-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="75ad2-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75ad2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75ad2-133">CommonParameters</span></span>
<span data-ttu-id="75ad2-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="75ad2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75ad2-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75ad2-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75ad2-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="75ad2-136">INPUTS</span></span>

### <span data-ttu-id="75ad2-137">System. Nullable "1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, культура = Neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="75ad2-137">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="75ad2-138">System. String</span><span class="sxs-lookup"><span data-stu-id="75ad2-138">System.String</span></span>

## <span data-ttu-id="75ad2-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="75ad2-139">OUTPUTS</span></span>

### <span data-ttu-id="75ad2-140">System. void</span><span class="sxs-lookup"><span data-stu-id="75ad2-140">System.Void</span></span>

## <span data-ttu-id="75ad2-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="75ad2-141">NOTES</span></span>

## <span data-ttu-id="75ad2-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="75ad2-142">RELATED LINKS</span></span>

[<span data-ttu-id="75ad2-143">Get-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="75ad2-143">Get-AzAutomationScheduledRunbook</span></span>](./Get-AzAutomationScheduledRunbook.md)

[<span data-ttu-id="75ad2-144">Регистрация — AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="75ad2-144">Register-AzAutomationScheduledRunbook</span></span>](./Register-AzAutomationScheduledRunbook.md)

