---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: EDB918EA-4FF3-44EF-A4CA-5BFBD14340EA
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationRunbook.md
ms.openlocfilehash: 00d6908e244a54fb2dbd501f0d944fc9cfdbdff4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014275"
---
# <span data-ttu-id="b2166-101">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b2166-101">Get-AzAutomationRunbook</span></span>

## <span data-ttu-id="b2166-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2166-102">SYNOPSIS</span></span>
<span data-ttu-id="b2166-103">Возвращает книгу запуска.</span><span class="sxs-lookup"><span data-stu-id="b2166-103">Gets a runbook.</span></span>

## <span data-ttu-id="b2166-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b2166-104">SYNTAX</span></span>

### <span data-ttu-id="b2166-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b2166-105">ByAll (Default)</span></span>
```
Get-AzAutomationRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2166-106">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="b2166-106">ByRunbookName</span></span>
```
Get-AzAutomationRunbook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2166-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b2166-107">DESCRIPTION</span></span>
<span data-ttu-id="b2166-108">Для получения книг автоматизации Azure возвращается **cmdlet Get-AzAutomationRunbook.**</span><span class="sxs-lookup"><span data-stu-id="b2166-108">The **Get-AzAutomationRunbook** cmdlet gets Azure Automation runbooks.</span></span>
<span data-ttu-id="b2166-109">Чтобы получить определенную книгу, укажите ее имя.</span><span class="sxs-lookup"><span data-stu-id="b2166-109">To get a specific runbook, specify its name.</span></span>

## <span data-ttu-id="b2166-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b2166-110">EXAMPLES</span></span>

### <span data-ttu-id="b2166-111">Пример 1. Получить все книги</span><span class="sxs-lookup"><span data-stu-id="b2166-111">Example 1: Get all runbooks</span></span>
```
PS C:\>Get-AzAutomationRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="b2166-112">Эта команда получает все книги в учетной записи автоматизации Azure с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="b2166-112">This command gets all runbooks in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="b2166-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b2166-113">PARAMETERS</span></span>

### <span data-ttu-id="b2166-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b2166-114">-AutomationAccountName</span></span>
<span data-ttu-id="b2166-115">Указывает имя учетной записи автоматизации, в которой этот cmdlet получает книги.</span><span class="sxs-lookup"><span data-stu-id="b2166-115">Specifies the name of an Automation account in which this cmdlet gets runbooks.</span></span>

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

### <span data-ttu-id="b2166-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2166-116">-DefaultProfile</span></span>
<span data-ttu-id="b2166-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b2166-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b2166-118">-Name</span><span class="sxs-lookup"><span data-stu-id="b2166-118">-Name</span></span>
<span data-ttu-id="b2166-119">Определяет имя книги, которая возвращается этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2166-119">Specifies the name of a runbook that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b2166-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2166-120">-ResourceGroupName</span></span>
<span data-ttu-id="b2166-121">Имя группы ресурсов, для которой этот cmdlet получает книги.</span><span class="sxs-lookup"><span data-stu-id="b2166-121">Specifies the name of the resource group for which this cmdlet gets runbooks.</span></span>

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

### <span data-ttu-id="b2166-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2166-122">CommonParameters</span></span>
<span data-ttu-id="b2166-123">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2166-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2166-124">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2166-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2166-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b2166-125">INPUTS</span></span>

### <span data-ttu-id="b2166-126">System.String</span><span class="sxs-lookup"><span data-stu-id="b2166-126">System.String</span></span>

## <span data-ttu-id="b2166-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b2166-127">OUTPUTS</span></span>

### <span data-ttu-id="b2166-128">Microsoft.Azure.Commands.Automation.Model.Runbook</span><span class="sxs-lookup"><span data-stu-id="b2166-128">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="b2166-129">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b2166-129">NOTES</span></span>

## <span data-ttu-id="b2166-130">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b2166-130">RELATED LINKS</span></span>

[<span data-ttu-id="b2166-131">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b2166-131">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="b2166-132">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b2166-132">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="b2166-133">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b2166-133">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="b2166-134">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b2166-134">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="b2166-135">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b2166-135">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="b2166-136">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b2166-136">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="b2166-137">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b2166-137">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="b2166-138">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="b2166-138">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


