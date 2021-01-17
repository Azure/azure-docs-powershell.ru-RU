---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: EAD39EE1-C66F-4092-8876-E7F9FA612481
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSchedule.md
ms.openlocfilehash: 0c37c33b60d430bc1782254401033934552f5663
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98418335"
---
# <span data-ttu-id="f736c-101">Remove-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="f736c-101">Remove-AzAutomationSchedule</span></span>

## <span data-ttu-id="f736c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f736c-102">SYNOPSIS</span></span>
<span data-ttu-id="f736c-103">Удаляет расписание автоматизации.</span><span class="sxs-lookup"><span data-stu-id="f736c-103">Deletes an Automation schedule.</span></span>

## <span data-ttu-id="f736c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="f736c-104">SYNTAX</span></span>

```
Remove-AzAutomationSchedule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f736c-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f736c-105">DESCRIPTION</span></span>
<span data-ttu-id="f736c-106">Из автоматизации Azure календарный план удаляется с использованием **cmdlet Remove-AzAutomationSchedule.**</span><span class="sxs-lookup"><span data-stu-id="f736c-106">The **Remove-AzAutomationSchedule** cmdlet deletes a schedule from Azure Automation.</span></span>

## <span data-ttu-id="f736c-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="f736c-107">EXAMPLES</span></span>

### <span data-ttu-id="f736c-108">Пример 1. Удаление расписания</span><span class="sxs-lookup"><span data-stu-id="f736c-108">Example 1: Remove a schedule</span></span>
```
PS C:\>Remove-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="f736c-109">Эта команда удаляет расписание с именем Schedule01 в учетной записи автоматизации Contoso17 в группе ресурсов ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="f736c-109">This command deletes the schedule named Schedule01 in automation account Contoso17 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="f736c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f736c-110">PARAMETERS</span></span>

### <span data-ttu-id="f736c-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f736c-111">-AutomationAccountName</span></span>
<span data-ttu-id="f736c-112">Указывает имя учетной записи автоматизации, для которой этот cmdlet удаляет расписание.</span><span class="sxs-lookup"><span data-stu-id="f736c-112">Specifies the name of an Automation account for which this cmdlet removes a schedule.</span></span>

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

### <span data-ttu-id="f736c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f736c-113">-DefaultProfile</span></span>
<span data-ttu-id="f736c-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f736c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f736c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f736c-115">-Force</span></span>
<span data-ttu-id="f736c-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="f736c-116">ps_force</span></span>

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

### <span data-ttu-id="f736c-117">-Name</span><span class="sxs-lookup"><span data-stu-id="f736c-117">-Name</span></span>
<span data-ttu-id="f736c-118">Определяет имя расписания, которое удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f736c-118">Specifies the name for the schedule that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f736c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f736c-119">-ResourceGroupName</span></span>
<span data-ttu-id="f736c-120">Указывает имя группы ресурсов, для которой этот cmdlet удаляет расписание.</span><span class="sxs-lookup"><span data-stu-id="f736c-120">Specifies the name of a resource group for which this cmdlet removes a schedule.</span></span>

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

### <span data-ttu-id="f736c-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f736c-121">-Confirm</span></span>
<span data-ttu-id="f736c-122">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="f736c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f736c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f736c-123">-WhatIf</span></span>
<span data-ttu-id="f736c-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f736c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f736c-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="f736c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f736c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f736c-126">CommonParameters</span></span>
<span data-ttu-id="f736c-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f736c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f736c-128">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f736c-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f736c-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f736c-129">INPUTS</span></span>

### <span data-ttu-id="f736c-130">System.String</span><span class="sxs-lookup"><span data-stu-id="f736c-130">System.String</span></span>

## <span data-ttu-id="f736c-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f736c-131">OUTPUTS</span></span>

### <span data-ttu-id="f736c-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="f736c-132">System.Void</span></span>

## <span data-ttu-id="f736c-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="f736c-133">NOTES</span></span>

## <span data-ttu-id="f736c-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f736c-134">RELATED LINKS</span></span>

[<span data-ttu-id="f736c-135">Get-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="f736c-135">Get-AzAutomationSchedule</span></span>](./Get-AzAutomationSchedule.md)

[<span data-ttu-id="f736c-136">New-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="f736c-136">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)

[<span data-ttu-id="f736c-137">Set-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="f736c-137">Set-AzAutomationSchedule</span></span>](./Set-AzAutomationSchedule.md)


