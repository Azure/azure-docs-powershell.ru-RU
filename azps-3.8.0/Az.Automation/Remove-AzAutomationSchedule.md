---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: EAD39EE1-C66F-4092-8876-E7F9FA612481
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSchedule.md
ms.openlocfilehash: 0c37c33b60d430bc1782254401033934552f5663
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074923"
---
# <span data-ttu-id="0d60c-101">Remove-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="0d60c-101">Remove-AzAutomationSchedule</span></span>

## <span data-ttu-id="0d60c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0d60c-102">SYNOPSIS</span></span>
<span data-ttu-id="0d60c-103">Удаление расписания автоматизации.</span><span class="sxs-lookup"><span data-stu-id="0d60c-103">Deletes an Automation schedule.</span></span>

## <span data-ttu-id="0d60c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0d60c-104">SYNTAX</span></span>

```
Remove-AzAutomationSchedule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0d60c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d60c-105">DESCRIPTION</span></span>
<span data-ttu-id="0d60c-106">Командлет **Remove-AzAutomationSchedule** Удаляет расписание из Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="0d60c-106">The **Remove-AzAutomationSchedule** cmdlet deletes a schedule from Azure Automation.</span></span>

## <span data-ttu-id="0d60c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0d60c-107">EXAMPLES</span></span>

### <span data-ttu-id="0d60c-108">Пример 1: Удаление расписания</span><span class="sxs-lookup"><span data-stu-id="0d60c-108">Example 1: Remove a schedule</span></span>
```
PS C:\>Remove-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="0d60c-109">Эта команда удаляет расписание с именем Schedule01 в учетной записи автоматизации Contoso17 в группе ресурсов ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="0d60c-109">This command deletes the schedule named Schedule01 in automation account Contoso17 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="0d60c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0d60c-110">PARAMETERS</span></span>

### <span data-ttu-id="0d60c-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0d60c-111">-AutomationAccountName</span></span>
<span data-ttu-id="0d60c-112">Указывает имя учетной записи автоматизации, для которой этот командлет удаляет расписание.</span><span class="sxs-lookup"><span data-stu-id="0d60c-112">Specifies the name of an Automation account for which this cmdlet removes a schedule.</span></span>

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

### <span data-ttu-id="0d60c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d60c-113">-DefaultProfile</span></span>
<span data-ttu-id="0d60c-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="0d60c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0d60c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="0d60c-115">-Force</span></span>
<span data-ttu-id="0d60c-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="0d60c-116">ps_force</span></span>

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

### <span data-ttu-id="0d60c-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0d60c-117">-Name</span></span>
<span data-ttu-id="0d60c-118">Указывает имя расписания, которое удаляет этот командлет.</span><span class="sxs-lookup"><span data-stu-id="0d60c-118">Specifies the name for the schedule that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d60c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d60c-119">-ResourceGroupName</span></span>
<span data-ttu-id="0d60c-120">Указывает имя группы ресурсов, для которой этот командлет удаляет расписание.</span><span class="sxs-lookup"><span data-stu-id="0d60c-120">Specifies the name of a resource group for which this cmdlet removes a schedule.</span></span>

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

### <span data-ttu-id="0d60c-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0d60c-121">-Confirm</span></span>
<span data-ttu-id="0d60c-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0d60c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d60c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d60c-123">-WhatIf</span></span>
<span data-ttu-id="0d60c-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0d60c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d60c-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0d60c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d60c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d60c-126">CommonParameters</span></span>
<span data-ttu-id="0d60c-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0d60c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d60c-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d60c-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d60c-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0d60c-129">INPUTS</span></span>

### <span data-ttu-id="0d60c-130">System. String</span><span class="sxs-lookup"><span data-stu-id="0d60c-130">System.String</span></span>

## <span data-ttu-id="0d60c-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d60c-131">OUTPUTS</span></span>

### <span data-ttu-id="0d60c-132">System. void</span><span class="sxs-lookup"><span data-stu-id="0d60c-132">System.Void</span></span>

## <span data-ttu-id="0d60c-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="0d60c-133">NOTES</span></span>

## <span data-ttu-id="0d60c-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0d60c-134">RELATED LINKS</span></span>

[<span data-ttu-id="0d60c-135">Get-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="0d60c-135">Get-AzAutomationSchedule</span></span>](./Get-AzAutomationSchedule.md)

[<span data-ttu-id="0d60c-136">New-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="0d60c-136">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)

[<span data-ttu-id="0d60c-137">Set-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="0d60c-137">Set-AzAutomationSchedule</span></span>](./Set-AzAutomationSchedule.md)


