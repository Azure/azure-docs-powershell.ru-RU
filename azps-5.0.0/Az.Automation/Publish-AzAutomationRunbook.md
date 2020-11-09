---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: E7F31B71-983A-4DB3-BB30-BDC5C0247E74
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/publish-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Publish-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Publish-AzAutomationRunbook.md
ms.openlocfilehash: feca8adfbfe24ce006c2fc5f52618f43591fa0b4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94315266"
---
# <span data-ttu-id="3403f-101">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3403f-101">Publish-AzAutomationRunbook</span></span>

## <span data-ttu-id="3403f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3403f-102">SYNOPSIS</span></span>
<span data-ttu-id="3403f-103">Публикует Runbook.</span><span class="sxs-lookup"><span data-stu-id="3403f-103">Publishes a runbook.</span></span>

## <span data-ttu-id="3403f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3403f-104">SYNTAX</span></span>

```
Publish-AzAutomationRunbook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3403f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3403f-105">DESCRIPTION</span></span>
<span data-ttu-id="3403f-106">Командлет **Publish-AzAutomationRunbook** публикует Runbook для использования в производственной среде службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="3403f-106">The **Publish-AzAutomationRunbook** cmdlet publishes a runbook for use in the production environment of Azure Automation.</span></span>

## <span data-ttu-id="3403f-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3403f-107">EXAMPLES</span></span>

### <span data-ttu-id="3403f-108">Пример 1: публикация Runbook</span><span class="sxs-lookup"><span data-stu-id="3403f-108">Example 1: Publish a runbook</span></span>
```
PS C:\>Publish-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="3403f-109">Эта команда публикует Runbook с именем Runbk01 в учетной записи службы автоматизации Azure с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="3403f-109">This command publishes the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="3403f-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3403f-110">PARAMETERS</span></span>

### <span data-ttu-id="3403f-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3403f-111">-AutomationAccountName</span></span>
<span data-ttu-id="3403f-112">Указывает имя учетной записи автоматизации, в которой этот командлет публикует Runbook.</span><span class="sxs-lookup"><span data-stu-id="3403f-112">Specifies the name of the Automation account in which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="3403f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3403f-113">-DefaultProfile</span></span>
<span data-ttu-id="3403f-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="3403f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3403f-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3403f-115">-Name</span></span>
<span data-ttu-id="3403f-116">Указывает имя Runbook, который публикует этот командлет.</span><span class="sxs-lookup"><span data-stu-id="3403f-116">Specifies the name of the runbook that this cmdlet publishes.</span></span>

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

### <span data-ttu-id="3403f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3403f-117">-ResourceGroupName</span></span>
<span data-ttu-id="3403f-118">Указывает имя группы ресурсов, для которой этот командлет публикует Runbook.</span><span class="sxs-lookup"><span data-stu-id="3403f-118">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="3403f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3403f-119">CommonParameters</span></span>
<span data-ttu-id="3403f-120">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3403f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3403f-121">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3403f-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3403f-122">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3403f-122">INPUTS</span></span>

### <span data-ttu-id="3403f-123">System. String</span><span class="sxs-lookup"><span data-stu-id="3403f-123">System.String</span></span>

## <span data-ttu-id="3403f-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3403f-124">OUTPUTS</span></span>

### <span data-ttu-id="3403f-125">Microsoft. Azure. Commands. Automation. Model. Runbook</span><span class="sxs-lookup"><span data-stu-id="3403f-125">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="3403f-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="3403f-126">NOTES</span></span>

## <span data-ttu-id="3403f-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3403f-127">RELATED LINKS</span></span>

[<span data-ttu-id="3403f-128">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3403f-128">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="3403f-129">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3403f-129">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="3403f-130">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3403f-130">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="3403f-131">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3403f-131">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="3403f-132">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3403f-132">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="3403f-133">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3403f-133">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="3403f-134">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3403f-134">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="3403f-135">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3403f-135">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)

