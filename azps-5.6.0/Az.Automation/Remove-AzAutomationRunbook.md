---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 16055879-C001-46E7-B8C3-1FE2A1A67AC4
online version: https://docs.microsoft.com/powershell/module/az.automation/remove-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationRunbook.md
ms.openlocfilehash: a7dc06e4ddbeac224daf9b8a80be40d343514a18
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009891"
---
# <span data-ttu-id="12667-101">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="12667-101">Remove-AzAutomationRunbook</span></span>

## <span data-ttu-id="12667-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12667-102">SYNOPSIS</span></span>
<span data-ttu-id="12667-103">Удаляет книгу.</span><span class="sxs-lookup"><span data-stu-id="12667-103">Removes a runbook.</span></span>

## <span data-ttu-id="12667-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="12667-104">SYNTAX</span></span>

```
Remove-AzAutomationRunbook [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="12667-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="12667-105">DESCRIPTION</span></span>
<span data-ttu-id="12667-106">Для удаления книги из автоматизации Azure удаляется ее **cmdlet Remove-AzAutomationRunbook.**</span><span class="sxs-lookup"><span data-stu-id="12667-106">The **Remove-AzAutomationRunbook** cmdlet removes a runbook from Azure Automation.</span></span>

## <span data-ttu-id="12667-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="12667-107">EXAMPLES</span></span>

### <span data-ttu-id="12667-108">Пример 1. Удаление книги</span><span class="sxs-lookup"><span data-stu-id="12667-108">Example 1: Remove a runbook</span></span>
```
PS C:\>Remove-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook03" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="12667-109">Эта команда удаляет книгу Runbook03 в учетной записи автоматизации Azure с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="12667-109">This command removes the runbook named Runbook03 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="12667-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="12667-110">PARAMETERS</span></span>

### <span data-ttu-id="12667-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="12667-111">-AutomationAccountName</span></span>
<span data-ttu-id="12667-112">Указывает имя учетной записи автоматизации, из которой этот cmdlet удаляет книгу.</span><span class="sxs-lookup"><span data-stu-id="12667-112">Specifies the name of the Automation account in which this cmdlet removes a runbook.</span></span>

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

### <span data-ttu-id="12667-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12667-113">-DefaultProfile</span></span>
<span data-ttu-id="12667-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="12667-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="12667-115">-Force</span><span class="sxs-lookup"><span data-stu-id="12667-115">-Force</span></span>
<span data-ttu-id="12667-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="12667-116">ps_force</span></span>

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

### <span data-ttu-id="12667-117">-Name</span><span class="sxs-lookup"><span data-stu-id="12667-117">-Name</span></span>
<span data-ttu-id="12667-118">Определяет имя книги, которую удаляет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12667-118">Specifies the name of the runbook that this cmdlet removes.</span></span>

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

### <span data-ttu-id="12667-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12667-119">-ResourceGroupName</span></span>
<span data-ttu-id="12667-120">Имя группы ресурсов, для которой этот cmdlet публикует книгу.</span><span class="sxs-lookup"><span data-stu-id="12667-120">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="12667-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="12667-121">-Confirm</span></span>
<span data-ttu-id="12667-122">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12667-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12667-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12667-123">-WhatIf</span></span>
<span data-ttu-id="12667-124">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12667-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12667-125">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="12667-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12667-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12667-126">CommonParameters</span></span>
<span data-ttu-id="12667-127">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12667-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12667-128">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12667-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12667-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="12667-129">INPUTS</span></span>

### <span data-ttu-id="12667-130">System.String</span><span class="sxs-lookup"><span data-stu-id="12667-130">System.String</span></span>

## <span data-ttu-id="12667-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="12667-131">OUTPUTS</span></span>

### <span data-ttu-id="12667-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="12667-132">System.Void</span></span>

## <span data-ttu-id="12667-133">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="12667-133">NOTES</span></span>

## <span data-ttu-id="12667-134">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="12667-134">RELATED LINKS</span></span>

[<span data-ttu-id="12667-135">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="12667-135">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="12667-136">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="12667-136">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="12667-137">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="12667-137">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="12667-138">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="12667-138">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="12667-139">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="12667-139">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="12667-140">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="12667-140">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="12667-141">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="12667-141">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="12667-142">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="12667-142">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


