---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: EDB918EA-4FF3-44EF-A4CA-5BFBD14340EA
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRunbook.md
ms.openlocfilehash: edae476893de5a64e950902d2de7b31fe53b51ea
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100233721"
---
# <span data-ttu-id="7da32-101">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7da32-101">Get-AzAutomationRunbook</span></span>

## <span data-ttu-id="7da32-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7da32-102">SYNOPSIS</span></span>
<span data-ttu-id="7da32-103">Возвращает книгу запуска.</span><span class="sxs-lookup"><span data-stu-id="7da32-103">Gets a runbook.</span></span>

## <span data-ttu-id="7da32-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7da32-104">SYNTAX</span></span>

### <span data-ttu-id="7da32-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7da32-105">ByAll (Default)</span></span>
```
Get-AzAutomationRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7da32-106">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="7da32-106">ByRunbookName</span></span>
```
Get-AzAutomationRunbook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7da32-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7da32-107">DESCRIPTION</span></span>
<span data-ttu-id="7da32-108">Для получения книг автоматизации Azure возвращается **cmdlet Get-AzAutomationRunbook.**</span><span class="sxs-lookup"><span data-stu-id="7da32-108">The **Get-AzAutomationRunbook** cmdlet gets Azure Automation runbooks.</span></span>
<span data-ttu-id="7da32-109">Чтобы получить определенную книгу, укажите ее имя.</span><span class="sxs-lookup"><span data-stu-id="7da32-109">To get a specific runbook, specify its name.</span></span>

## <span data-ttu-id="7da32-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7da32-110">EXAMPLES</span></span>

### <span data-ttu-id="7da32-111">Пример 1. Получить все книги</span><span class="sxs-lookup"><span data-stu-id="7da32-111">Example 1: Get all runbooks</span></span>
```
PS C:\>Get-AzAutomationRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="7da32-112">Эта команда получает все книги в учетной записи автоматизации Azure с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="7da32-112">This command gets all runbooks in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="7da32-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7da32-113">PARAMETERS</span></span>

### <span data-ttu-id="7da32-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7da32-114">-AutomationAccountName</span></span>
<span data-ttu-id="7da32-115">Указывает имя учетной записи автоматизации, в которой этот cmdlet получает книги.</span><span class="sxs-lookup"><span data-stu-id="7da32-115">Specifies the name of an Automation account in which this cmdlet gets runbooks.</span></span>

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

### <span data-ttu-id="7da32-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7da32-116">-DefaultProfile</span></span>
<span data-ttu-id="7da32-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="7da32-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7da32-118">-Name</span><span class="sxs-lookup"><span data-stu-id="7da32-118">-Name</span></span>
<span data-ttu-id="7da32-119">Определяет имя книги, которая возвращается этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7da32-119">Specifies the name of a runbook that this cmdlet gets.</span></span>

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

### <span data-ttu-id="7da32-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7da32-120">-ResourceGroupName</span></span>
<span data-ttu-id="7da32-121">Имя группы ресурсов, для которой этот cmdlet получает книги.</span><span class="sxs-lookup"><span data-stu-id="7da32-121">Specifies the name of the resource group for which this cmdlet gets runbooks.</span></span>

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

### <span data-ttu-id="7da32-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7da32-122">CommonParameters</span></span>
<span data-ttu-id="7da32-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7da32-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7da32-124">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7da32-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7da32-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7da32-125">INPUTS</span></span>

### <span data-ttu-id="7da32-126">System.String</span><span class="sxs-lookup"><span data-stu-id="7da32-126">System.String</span></span>

## <span data-ttu-id="7da32-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7da32-127">OUTPUTS</span></span>

### <span data-ttu-id="7da32-128">Microsoft.Azure.Commands.Automation.Model.Runbook</span><span class="sxs-lookup"><span data-stu-id="7da32-128">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="7da32-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7da32-129">NOTES</span></span>

## <span data-ttu-id="7da32-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7da32-130">RELATED LINKS</span></span>

[<span data-ttu-id="7da32-131">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7da32-131">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="7da32-132">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7da32-132">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="7da32-133">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7da32-133">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="7da32-134">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7da32-134">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="7da32-135">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7da32-135">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="7da32-136">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7da32-136">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="7da32-137">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7da32-137">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="7da32-138">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7da32-138">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


