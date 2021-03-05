---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 920C028B-0471-43EB-9123-C444289FD845
online version: https://docs.microsoft.com/powershell/module/az.automation/set-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationRunbook.md
ms.openlocfilehash: 26a84b381e3193f9f95f21135f40489f0cacb754
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004723"
---
# <span data-ttu-id="e0117-101">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e0117-101">Set-AzAutomationRunbook</span></span>

## <span data-ttu-id="e0117-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0117-102">SYNOPSIS</span></span>
<span data-ttu-id="e0117-103">Изменяет книгу.</span><span class="sxs-lookup"><span data-stu-id="e0117-103">Modifies a runbook.</span></span>

## <span data-ttu-id="e0117-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e0117-104">SYNTAX</span></span>

```
Set-AzAutomationRunbook [-Name] <String> [-Description <String>] [-Tag <IDictionary>] [-LogProgress <Boolean>]
 [-LogVerbose <Boolean>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e0117-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e0117-105">DESCRIPTION</span></span>
<span data-ttu-id="e0117-106">**Cmdlet Set-AzAutomationRunbook** изменяет конфигурацию книги автоматизации Azure в APS.</span><span class="sxs-lookup"><span data-stu-id="e0117-106">The **Set-AzAutomationRunbook** cmdlet modifies the configuration of an Azure Automation runbook in APS.</span></span>

## <span data-ttu-id="e0117-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e0117-107">EXAMPLES</span></span>

### <span data-ttu-id="e0117-108">Пример 1. Включить подробное ведение журнала для книги</span><span class="sxs-lookup"><span data-stu-id="e0117-108">Example 1: Enable verbose logging for a runbook</span></span>
```
PS C:\>Set-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook02" -LogVerbose $True -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="e0117-109">Эта команда позволяет подробно вести журнал для заданий указанной книги в учетной записи автоматизации Azure Contoso17.</span><span class="sxs-lookup"><span data-stu-id="e0117-109">This command enables verbose logging for the jobs of the specified runbook in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="e0117-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e0117-110">PARAMETERS</span></span>

### <span data-ttu-id="e0117-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e0117-111">-AutomationAccountName</span></span>
<span data-ttu-id="e0117-112">Указывает имя учетной записи автоматизации, в которой этот cmdlet изменяет книгу.</span><span class="sxs-lookup"><span data-stu-id="e0117-112">Specifies the name of the Automation account in which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="e0117-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0117-113">-DefaultProfile</span></span>
<span data-ttu-id="e0117-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e0117-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e0117-115">-Description</span><span class="sxs-lookup"><span data-stu-id="e0117-115">-Description</span></span>
<span data-ttu-id="e0117-116">Описание книги.</span><span class="sxs-lookup"><span data-stu-id="e0117-116">Specifies a description for the runbook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0117-117">-LogProgress</span><span class="sxs-lookup"><span data-stu-id="e0117-117">-LogProgress</span></span>
<span data-ttu-id="e0117-118">Указывает, регистрирует ли журнал выполнения.</span><span class="sxs-lookup"><span data-stu-id="e0117-118">Specifies whether the runbook logs progress.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0117-119">-LogVerbose</span><span class="sxs-lookup"><span data-stu-id="e0117-119">-LogVerbose</span></span>
<span data-ttu-id="e0117-120">Указывает, включает ли ведение журнала подробные сведения.</span><span class="sxs-lookup"><span data-stu-id="e0117-120">Specifies whether logging includes detailed information.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0117-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e0117-121">-Name</span></span>
<span data-ttu-id="e0117-122">Указывает имя книги, которую изменяет этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0117-122">Specifies the name of the runbook that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="e0117-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0117-123">-ResourceGroupName</span></span>
<span data-ttu-id="e0117-124">Имя группы ресурсов, для которой этот cmdlet изменяет книгу.</span><span class="sxs-lookup"><span data-stu-id="e0117-124">Specifies the name of the resource group for which this cmdlet modifies a runbook.</span></span>

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

### <span data-ttu-id="e0117-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="e0117-125">-Tag</span></span>
<span data-ttu-id="e0117-126">Теги книги запуска.</span><span class="sxs-lookup"><span data-stu-id="e0117-126">The runbook tags.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0117-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0117-127">CommonParameters</span></span>
<span data-ttu-id="e0117-128">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0117-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0117-129">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0117-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0117-130">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e0117-130">INPUTS</span></span>

### <span data-ttu-id="e0117-131">System.String</span><span class="sxs-lookup"><span data-stu-id="e0117-131">System.String</span></span>

### <span data-ttu-id="e0117-132">System.Collections.IDictionary</span><span class="sxs-lookup"><span data-stu-id="e0117-132">System.Collections.IDictionary</span></span>

### <span data-ttu-id="e0117-133">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e0117-133">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="e0117-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e0117-134">OUTPUTS</span></span>

### <span data-ttu-id="e0117-135">Microsoft.Azure.Commands.Automation.Model.Runbook</span><span class="sxs-lookup"><span data-stu-id="e0117-135">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="e0117-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e0117-136">NOTES</span></span>

## <span data-ttu-id="e0117-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e0117-137">RELATED LINKS</span></span>

[<span data-ttu-id="e0117-138">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e0117-138">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="e0117-139">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e0117-139">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="e0117-140">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e0117-140">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="e0117-141">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e0117-141">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="e0117-142">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e0117-142">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="e0117-143">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e0117-143">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="e0117-144">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e0117-144">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="e0117-145">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="e0117-145">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


