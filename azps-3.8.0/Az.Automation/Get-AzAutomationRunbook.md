---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: EDB918EA-4FF3-44EF-A4CA-5BFBD14340EA
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRunbook.md
ms.openlocfilehash: edae476893de5a64e950902d2de7b31fe53b51ea
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94072753"
---
# <span data-ttu-id="d8116-101">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d8116-101">Get-AzAutomationRunbook</span></span>

## <span data-ttu-id="d8116-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d8116-102">SYNOPSIS</span></span>
<span data-ttu-id="d8116-103">Получает Runbook.</span><span class="sxs-lookup"><span data-stu-id="d8116-103">Gets a runbook.</span></span>

## <span data-ttu-id="d8116-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d8116-104">SYNTAX</span></span>

### <span data-ttu-id="d8116-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d8116-105">ByAll (Default)</span></span>
```
Get-AzAutomationRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d8116-106">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="d8116-106">ByRunbookName</span></span>
```
Get-AzAutomationRunbook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8116-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8116-107">DESCRIPTION</span></span>
<span data-ttu-id="d8116-108">Командлет **Get-AzAutomationRunbook** получает Runbook службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="d8116-108">The **Get-AzAutomationRunbook** cmdlet gets Azure Automation runbooks.</span></span>
<span data-ttu-id="d8116-109">Чтобы получить определенный Runbook, укажите его имя.</span><span class="sxs-lookup"><span data-stu-id="d8116-109">To get a specific runbook, specify its name.</span></span>

## <span data-ttu-id="d8116-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d8116-110">EXAMPLES</span></span>

### <span data-ttu-id="d8116-111">Пример 1: получение всех модулей Runbook</span><span class="sxs-lookup"><span data-stu-id="d8116-111">Example 1: Get all runbooks</span></span>
```
PS C:\>Get-AzAutomationRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="d8116-112">Эта команда получает все runbooks в учетной записи службы автоматизации Azure с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="d8116-112">This command gets all runbooks in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="d8116-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d8116-113">PARAMETERS</span></span>

### <span data-ttu-id="d8116-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d8116-114">-AutomationAccountName</span></span>
<span data-ttu-id="d8116-115">Указывает имя учетной записи автоматизации, в которой этот командлет получает runbooks.</span><span class="sxs-lookup"><span data-stu-id="d8116-115">Specifies the name of an Automation account in which this cmdlet gets runbooks.</span></span>

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

### <span data-ttu-id="d8116-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8116-116">-DefaultProfile</span></span>
<span data-ttu-id="d8116-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d8116-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d8116-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d8116-118">-Name</span></span>
<span data-ttu-id="d8116-119">Указывает имя Runbook, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="d8116-119">Specifies the name of a runbook that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookName
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8116-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8116-120">-ResourceGroupName</span></span>
<span data-ttu-id="d8116-121">Указывает имя группы ресурсов, для которой этот командлет получает runbooks.</span><span class="sxs-lookup"><span data-stu-id="d8116-121">Specifies the name of the resource group for which this cmdlet gets runbooks.</span></span>

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

### <span data-ttu-id="d8116-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8116-122">CommonParameters</span></span>
<span data-ttu-id="d8116-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d8116-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8116-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8116-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8116-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d8116-125">INPUTS</span></span>

### <span data-ttu-id="d8116-126">System. String</span><span class="sxs-lookup"><span data-stu-id="d8116-126">System.String</span></span>

## <span data-ttu-id="d8116-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8116-127">OUTPUTS</span></span>

### <span data-ttu-id="d8116-128">Microsoft. Azure. Commands. Automation. Model. Runbook</span><span class="sxs-lookup"><span data-stu-id="d8116-128">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="d8116-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="d8116-129">NOTES</span></span>

## <span data-ttu-id="d8116-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d8116-130">RELATED LINKS</span></span>

[<span data-ttu-id="d8116-131">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d8116-131">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="d8116-132">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d8116-132">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="d8116-133">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d8116-133">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="d8116-134">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d8116-134">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="d8116-135">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d8116-135">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="d8116-136">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d8116-136">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="d8116-137">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d8116-137">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="d8116-138">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="d8116-138">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


