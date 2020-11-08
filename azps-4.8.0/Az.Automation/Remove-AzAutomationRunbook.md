---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 16055879-C001-46E7-B8C3-1FE2A1A67AC4
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationRunbook.md
ms.openlocfilehash: d6ce3a737063763d77ed408072d275c52ee5884c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077918"
---
# <span data-ttu-id="fd24b-101">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="fd24b-101">Remove-AzAutomationRunbook</span></span>

## <span data-ttu-id="fd24b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fd24b-102">SYNOPSIS</span></span>
<span data-ttu-id="fd24b-103">Удаление модуля Runbook.</span><span class="sxs-lookup"><span data-stu-id="fd24b-103">Removes a runbook.</span></span>

## <span data-ttu-id="fd24b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fd24b-104">SYNTAX</span></span>

```
Remove-AzAutomationRunbook [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fd24b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fd24b-105">DESCRIPTION</span></span>
<span data-ttu-id="fd24b-106">Командлет **Remove-AzAutomationRunbook** удаляет Runbook из Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="fd24b-106">The **Remove-AzAutomationRunbook** cmdlet removes a runbook from Azure Automation.</span></span>

## <span data-ttu-id="fd24b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fd24b-107">EXAMPLES</span></span>

### <span data-ttu-id="fd24b-108">Пример 1: удаление Runbook</span><span class="sxs-lookup"><span data-stu-id="fd24b-108">Example 1: Remove a runbook</span></span>
```
PS C:\>Remove-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook03" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="fd24b-109">Эта команда удаляет Runbook с именем Runbook03 в учетной записи службы автоматизации Azure с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="fd24b-109">This command removes the runbook named Runbook03 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="fd24b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fd24b-110">PARAMETERS</span></span>

### <span data-ttu-id="fd24b-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="fd24b-111">-AutomationAccountName</span></span>
<span data-ttu-id="fd24b-112">Указывает имя учетной записи автоматизации, в которой этот командлет удаляет Runbook.</span><span class="sxs-lookup"><span data-stu-id="fd24b-112">Specifies the name of the Automation account in which this cmdlet removes a runbook.</span></span>

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

### <span data-ttu-id="fd24b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd24b-113">-DefaultProfile</span></span>
<span data-ttu-id="fd24b-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="fd24b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fd24b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="fd24b-115">-Force</span></span>
<span data-ttu-id="fd24b-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="fd24b-116">ps_force</span></span>

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

### <span data-ttu-id="fd24b-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fd24b-117">-Name</span></span>
<span data-ttu-id="fd24b-118">Указывает имя Runbook, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="fd24b-118">Specifies the name of the runbook that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd24b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd24b-119">-ResourceGroupName</span></span>
<span data-ttu-id="fd24b-120">Указывает имя группы ресурсов, для которой этот командлет публикует Runbook.</span><span class="sxs-lookup"><span data-stu-id="fd24b-120">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="fd24b-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fd24b-121">-Confirm</span></span>
<span data-ttu-id="fd24b-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fd24b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd24b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd24b-123">-WhatIf</span></span>
<span data-ttu-id="fd24b-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fd24b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd24b-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fd24b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd24b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd24b-126">CommonParameters</span></span>
<span data-ttu-id="fd24b-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fd24b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd24b-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd24b-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd24b-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fd24b-129">INPUTS</span></span>

### <span data-ttu-id="fd24b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="fd24b-130">System.String</span></span>

## <span data-ttu-id="fd24b-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fd24b-131">OUTPUTS</span></span>

### <span data-ttu-id="fd24b-132">System. void</span><span class="sxs-lookup"><span data-stu-id="fd24b-132">System.Void</span></span>

## <span data-ttu-id="fd24b-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="fd24b-133">NOTES</span></span>

## <span data-ttu-id="fd24b-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fd24b-134">RELATED LINKS</span></span>

[<span data-ttu-id="fd24b-135">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="fd24b-135">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="fd24b-136">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="fd24b-136">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="fd24b-137">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="fd24b-137">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="fd24b-138">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="fd24b-138">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="fd24b-139">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="fd24b-139">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="fd24b-140">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="fd24b-140">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="fd24b-141">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="fd24b-141">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="fd24b-142">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="fd24b-142">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)

