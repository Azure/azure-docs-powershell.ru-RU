---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 16055879-C001-46E7-B8C3-1FE2A1A67AC4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationRunbook.md
ms.openlocfilehash: b84daa4041b8e27351d3b3b63eae4c7599881eae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733184"
---
# <span data-ttu-id="4c1f3-101">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="4c1f3-101">Remove-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="4c1f3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4c1f3-102">SYNOPSIS</span></span>
<span data-ttu-id="4c1f3-103">Удаление модуля Runbook.</span><span class="sxs-lookup"><span data-stu-id="4c1f3-103">Removes a runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c1f3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4c1f3-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationRunbook [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4c1f3-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4c1f3-105">DESCRIPTION</span></span>
<span data-ttu-id="4c1f3-106">Командлет **Remove-AzureRmAutomationRunbook** удаляет Runbook из Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="4c1f3-106">The **Remove-AzureRmAutomationRunbook** cmdlet removes a runbook from Azure Automation.</span></span>

## <span data-ttu-id="4c1f3-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4c1f3-107">EXAMPLES</span></span>

### <span data-ttu-id="4c1f3-108">Пример 1: удаление Runbook</span><span class="sxs-lookup"><span data-stu-id="4c1f3-108">Example 1: Remove a runbook</span></span>
```
PS C:\>Remove-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook03" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="4c1f3-109">Эта команда удаляет Runbook с именем Runbook03 в учетной записи службы автоматизации Azure с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="4c1f3-109">This command removes the runbook named Runbook03 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="4c1f3-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4c1f3-110">PARAMETERS</span></span>

### <span data-ttu-id="4c1f3-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4c1f3-111">-AutomationAccountName</span></span>
<span data-ttu-id="4c1f3-112">Указывает имя учетной записи автоматизации, в которой этот командлет удаляет Runbook.</span><span class="sxs-lookup"><span data-stu-id="4c1f3-112">Specifies the name of the Automation account in which this cmdlet removes a runbook.</span></span>

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

### <span data-ttu-id="4c1f3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c1f3-113">-DefaultProfile</span></span>
<span data-ttu-id="4c1f3-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="4c1f3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4c1f3-115">-Force</span><span class="sxs-lookup"><span data-stu-id="4c1f3-115">-Force</span></span>
<span data-ttu-id="4c1f3-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="4c1f3-116">ps_force</span></span>

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

### <span data-ttu-id="4c1f3-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4c1f3-117">-Name</span></span>
<span data-ttu-id="4c1f3-118">Указывает имя Runbook, который удаляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="4c1f3-118">Specifies the name of the runbook that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4c1f3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c1f3-119">-ResourceGroupName</span></span>
<span data-ttu-id="4c1f3-120">Указывает имя группы ресурсов, для которой этот командлет публикует Runbook.</span><span class="sxs-lookup"><span data-stu-id="4c1f3-120">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="4c1f3-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4c1f3-121">-Confirm</span></span>
<span data-ttu-id="4c1f3-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4c1f3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c1f3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c1f3-123">-WhatIf</span></span>
<span data-ttu-id="4c1f3-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4c1f3-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c1f3-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4c1f3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c1f3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c1f3-126">CommonParameters</span></span>
<span data-ttu-id="4c1f3-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4c1f3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c1f3-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c1f3-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c1f3-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4c1f3-129">INPUTS</span></span>

### <span data-ttu-id="4c1f3-130">System. String</span><span class="sxs-lookup"><span data-stu-id="4c1f3-130">System.String</span></span>

## <span data-ttu-id="4c1f3-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4c1f3-131">OUTPUTS</span></span>

### <span data-ttu-id="4c1f3-132">System. void</span><span class="sxs-lookup"><span data-stu-id="4c1f3-132">System.Void</span></span>

## <span data-ttu-id="4c1f3-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="4c1f3-133">NOTES</span></span>

## <span data-ttu-id="4c1f3-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4c1f3-134">RELATED LINKS</span></span>

[<span data-ttu-id="4c1f3-135">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="4c1f3-135">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="4c1f3-136">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="4c1f3-136">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="4c1f3-137">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="4c1f3-137">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="4c1f3-138">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="4c1f3-138">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="4c1f3-139">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="4c1f3-139">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="4c1f3-140">Publish-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="4c1f3-140">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="4c1f3-141">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="4c1f3-141">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="4c1f3-142">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="4c1f3-142">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)


