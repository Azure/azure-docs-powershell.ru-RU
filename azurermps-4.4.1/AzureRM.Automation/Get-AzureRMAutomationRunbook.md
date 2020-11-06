---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: EDB918EA-4FF3-44EF-A4CA-5BFBD14340EA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationRunbook.md
ms.openlocfilehash: e543a7da3ce5502e0f78619ca4fbb455b29b82d0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559972"
---
# <span data-ttu-id="ba8ea-101">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ba8ea-101">Get-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="ba8ea-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ba8ea-102">SYNOPSIS</span></span>
<span data-ttu-id="ba8ea-103">Получает Runbook.</span><span class="sxs-lookup"><span data-stu-id="ba8ea-103">Gets a runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba8ea-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ba8ea-104">SYNTAX</span></span>

### <span data-ttu-id="ba8ea-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ba8ea-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba8ea-106">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="ba8ea-106">ByRunbookName</span></span>
```
Get-AzureRmAutomationRunbook [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba8ea-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ba8ea-107">DESCRIPTION</span></span>
<span data-ttu-id="ba8ea-108">Командлет **Get-AzureRmAutomationRunbook** получает Runbook службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="ba8ea-108">The **Get-AzureRmAutomationRunbook** cmdlet gets Azure Automation runbooks.</span></span>
<span data-ttu-id="ba8ea-109">Чтобы получить определенный Runbook, укажите его имя.</span><span class="sxs-lookup"><span data-stu-id="ba8ea-109">To get a specific runbook, specify its name.</span></span>

## <span data-ttu-id="ba8ea-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ba8ea-110">EXAMPLES</span></span>

### <span data-ttu-id="ba8ea-111">Пример 1: получение всех модулей Runbook</span><span class="sxs-lookup"><span data-stu-id="ba8ea-111">Example 1: Get all runbooks</span></span>
```
PS C:\>Get-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="ba8ea-112">Эта команда получает все runbooks в учетной записи службы автоматизации Azure с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="ba8ea-112">This command gets all runbooks in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="ba8ea-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ba8ea-113">PARAMETERS</span></span>

### <span data-ttu-id="ba8ea-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ba8ea-114">-AutomationAccountName</span></span>
<span data-ttu-id="ba8ea-115">Указывает имя учетной записи автоматизации, в которой этот командлет получает runbooks.</span><span class="sxs-lookup"><span data-stu-id="ba8ea-115">Specifies the name of an Automation account in which this cmdlet gets runbooks.</span></span>

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

### <span data-ttu-id="ba8ea-116">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ba8ea-116">-Name</span></span>
<span data-ttu-id="ba8ea-117">Указывает имя Runbook, который получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="ba8ea-117">Specifies the name of a runbook that this cmdlet gets.</span></span>

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

### <span data-ttu-id="ba8ea-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba8ea-118">-ResourceGroupName</span></span>
<span data-ttu-id="ba8ea-119">Указывает имя группы ресурсов, для которой этот командлет получает runbooks.</span><span class="sxs-lookup"><span data-stu-id="ba8ea-119">Specifies the name of the resource group for which this cmdlet gets runbooks.</span></span>

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

### <span data-ttu-id="ba8ea-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba8ea-120">-DefaultProfile</span></span>
<span data-ttu-id="ba8ea-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ba8ea-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba8ea-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba8ea-122">CommonParameters</span></span>
<span data-ttu-id="ba8ea-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ba8ea-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba8ea-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba8ea-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba8ea-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ba8ea-125">INPUTS</span></span>

## <span data-ttu-id="ba8ea-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ba8ea-126">OUTPUTS</span></span>

### <span data-ttu-id="ba8ea-127">Microsoft. Azure. Commands. Automation. Model. Runbook</span><span class="sxs-lookup"><span data-stu-id="ba8ea-127">Microsoft.Azure.Commands.Automation.Model.Runbook</span></span>

## <span data-ttu-id="ba8ea-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="ba8ea-128">NOTES</span></span>

## <span data-ttu-id="ba8ea-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ba8ea-129">RELATED LINKS</span></span>

[<span data-ttu-id="ba8ea-130">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ba8ea-130">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="ba8ea-131">Import-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ba8ea-131">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="ba8ea-132">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ba8ea-132">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="ba8ea-133">New-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ba8ea-133">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="ba8ea-134">Publish-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ba8ea-134">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="ba8ea-135">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ba8ea-135">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="ba8ea-136">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ba8ea-136">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="ba8ea-137">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="ba8ea-137">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)


