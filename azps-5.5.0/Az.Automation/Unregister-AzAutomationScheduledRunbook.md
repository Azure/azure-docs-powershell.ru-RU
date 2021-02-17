---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: C7C193CF-4E3A-4275-8289-946C99B1C553
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/unregister-azautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationScheduledRunbook.md
ms.openlocfilehash: 53cfa3ccd708871dfe639b0053cb6ab24946bace
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239488"
---
# <span data-ttu-id="2478c-101">Unregister-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="2478c-101">Unregister-AzAutomationScheduledRunbook</span></span>

## <span data-ttu-id="2478c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2478c-102">SYNOPSIS</span></span>
<span data-ttu-id="2478c-103">Удаляет связь между книгой и расписанием.</span><span class="sxs-lookup"><span data-stu-id="2478c-103">Removes an association between a runbook and a schedule.</span></span>

## <span data-ttu-id="2478c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2478c-104">SYNTAX</span></span>

### <span data-ttu-id="2478c-105">ByJobScheduleId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2478c-105">ByJobScheduleId (Default)</span></span>
```
Unregister-AzAutomationScheduledRunbook -JobScheduleId <Guid> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2478c-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="2478c-106">ByRunbookNameAndScheduleName</span></span>
```
Unregister-AzAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2478c-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2478c-107">DESCRIPTION</span></span>
<span data-ttu-id="2478c-108">Командалет **Unregister-AzAutomationScheduledRunbook** удаляет связь между книгой автоматизации Azure и расписанием.</span><span class="sxs-lookup"><span data-stu-id="2478c-108">The **Unregister-AzAutomationScheduledRunbook** cmdlet removes the association between an Azure Automation runbook and a schedule.</span></span>
<span data-ttu-id="2478c-109">В расписании запуск книги больше не запускается.</span><span class="sxs-lookup"><span data-stu-id="2478c-109">The schedule no longer starts the runbook.</span></span>

## <span data-ttu-id="2478c-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2478c-110">EXAMPLES</span></span>

### <span data-ttu-id="2478c-111">Пример 1. Удаление связи между книгой и расписанием</span><span class="sxs-lookup"><span data-stu-id="2478c-111">Example 1: Remove the association between a runbook and a schedule</span></span>
```
PS C:\>Unregister-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -ScheduleName "Runbk01Sched"
```

<span data-ttu-id="2478c-112">Эта команда удаляет связь между книгой Runbk01 и расписанием Runbk01Sched.</span><span class="sxs-lookup"><span data-stu-id="2478c-112">This command removes the association between the runbook named Runbk01 and the schedule named Runbk01Sched.</span></span>

## <span data-ttu-id="2478c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2478c-113">PARAMETERS</span></span>

### <span data-ttu-id="2478c-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2478c-114">-AutomationAccountName</span></span>
<span data-ttu-id="2478c-115">Указывает учетную запись автоматизации для книги, с которой работает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2478c-115">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="2478c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2478c-116">-DefaultProfile</span></span>
<span data-ttu-id="2478c-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="2478c-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2478c-118">-Force</span><span class="sxs-lookup"><span data-stu-id="2478c-118">-Force</span></span>
<span data-ttu-id="2478c-119">ps_force</span><span class="sxs-lookup"><span data-stu-id="2478c-119">ps_force</span></span>

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

### <span data-ttu-id="2478c-120">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="2478c-120">-JobScheduleId</span></span>
<span data-ttu-id="2478c-121">Определяет ИД запланированной книги запуска.</span><span class="sxs-lookup"><span data-stu-id="2478c-121">Specifies the ID of a scheduled runbook.</span></span>

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

### <span data-ttu-id="2478c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2478c-122">-ResourceGroupName</span></span>
<span data-ttu-id="2478c-123">Имя группы ресурсов для запланированной книги.</span><span class="sxs-lookup"><span data-stu-id="2478c-123">Specifies the name of a resource group for the scheduled runbook.</span></span>

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

### <span data-ttu-id="2478c-124">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="2478c-124">-RunbookName</span></span>
<span data-ttu-id="2478c-125">Указывает имя книги, которую этот cmdlet отсоединит от расписания.</span><span class="sxs-lookup"><span data-stu-id="2478c-125">Specifies the name of the runbook that this cmdlet dissociates from a schedule.</span></span>

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

### <span data-ttu-id="2478c-126">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="2478c-126">-ScheduleName</span></span>
<span data-ttu-id="2478c-127">Определяет название расписания, из которого этот cmdlet дисошиацией книги.</span><span class="sxs-lookup"><span data-stu-id="2478c-127">Specifies the name of the schedule from which this cmdlet dissociates a runbook.</span></span>

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

### <span data-ttu-id="2478c-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2478c-128">-Confirm</span></span>
<span data-ttu-id="2478c-129">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="2478c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2478c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2478c-130">-WhatIf</span></span>
<span data-ttu-id="2478c-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2478c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2478c-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2478c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2478c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2478c-133">CommonParameters</span></span>
<span data-ttu-id="2478c-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2478c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2478c-135">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2478c-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2478c-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2478c-136">INPUTS</span></span>

### <span data-ttu-id="2478c-137">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="2478c-137">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="2478c-138">System.String</span><span class="sxs-lookup"><span data-stu-id="2478c-138">System.String</span></span>

## <span data-ttu-id="2478c-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2478c-139">OUTPUTS</span></span>

### <span data-ttu-id="2478c-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="2478c-140">System.Void</span></span>

## <span data-ttu-id="2478c-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2478c-141">NOTES</span></span>

## <span data-ttu-id="2478c-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2478c-142">RELATED LINKS</span></span>

[<span data-ttu-id="2478c-143">Get-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="2478c-143">Get-AzAutomationScheduledRunbook</span></span>](./Get-AzAutomationScheduledRunbook.md)

[<span data-ttu-id="2478c-144">Register-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="2478c-144">Register-AzAutomationScheduledRunbook</span></span>](./Register-AzAutomationScheduledRunbook.md)


