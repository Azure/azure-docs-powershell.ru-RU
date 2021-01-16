---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A73B388A-E859-40D3-BA63-0E231CF1E81D
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationModule.md
ms.openlocfilehash: d0ff86b21b96e5aa133f61d0682aa89ed3fea225
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98418679"
---
# <span data-ttu-id="4ace5-101">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="4ace5-101">Get-AzAutomationModule</span></span>

## <span data-ttu-id="4ace5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ace5-102">SYNOPSIS</span></span>
<span data-ttu-id="4ace5-103">Получает метаданные модулей от автоматизации.</span><span class="sxs-lookup"><span data-stu-id="4ace5-103">Gets metadata for modules from Automation.</span></span>

## <span data-ttu-id="4ace5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4ace5-104">SYNTAX</span></span>

### <span data-ttu-id="4ace5-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4ace5-105">ByAll (Default)</span></span>
```
Get-AzAutomationModule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ace5-106">ByName</span><span class="sxs-lookup"><span data-stu-id="4ace5-106">ByName</span></span>
```
Get-AzAutomationModule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ace5-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ace5-107">DESCRIPTION</span></span>
<span data-ttu-id="4ace5-108">Командлет **Get-AzAutomationModule** получает метаданные модулей из автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="4ace5-108">The **Get-AzAutomationModule** cmdlet gets metadata for modules from Azure Automation.</span></span>

## <span data-ttu-id="4ace5-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4ace5-109">EXAMPLES</span></span>

### <span data-ttu-id="4ace5-110">Пример 1. Получить все модули</span><span class="sxs-lookup"><span data-stu-id="4ace5-110">Example 1: Get all modules</span></span>
```
PS C:\>Get-AzAutomationModule -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="4ace5-111">Эта команда получает все модули в учетной записи автоматизации Contoso17.</span><span class="sxs-lookup"><span data-stu-id="4ace5-111">This command gets all modules in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="4ace5-112">Пример 2. Получить модуль</span><span class="sxs-lookup"><span data-stu-id="4ace5-112">Example 2: Get a module</span></span>
```
PS C:\>Get-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="4ace5-113">Эта команда получает модуль ContosoModule в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="4ace5-113">This command gets a module named ContosoModule in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="4ace5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4ace5-114">PARAMETERS</span></span>

### <span data-ttu-id="4ace5-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4ace5-115">-AutomationAccountName</span></span>
<span data-ttu-id="4ace5-116">Указывает имя учетной записи автоматизации, для которой этот командлет получает метаданные модуля.</span><span class="sxs-lookup"><span data-stu-id="4ace5-116">Specifies the name of the Automation account for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="4ace5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ace5-117">-DefaultProfile</span></span>
<span data-ttu-id="4ace5-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="4ace5-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4ace5-119">-Name</span><span class="sxs-lookup"><span data-stu-id="4ace5-119">-Name</span></span>
<span data-ttu-id="4ace5-120">Имя модуля, для которого этот командлет получает метаданные.</span><span class="sxs-lookup"><span data-stu-id="4ace5-120">Specifies the name of the module for which this cmdlet gets metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ace5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ace5-121">-ResourceGroupName</span></span>
<span data-ttu-id="4ace5-122">Имя группы ресурсов, для которой этот командлет получает метаданные модуля.</span><span class="sxs-lookup"><span data-stu-id="4ace5-122">Specifies the name of a resource group for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="4ace5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ace5-123">CommonParameters</span></span>
<span data-ttu-id="4ace5-124">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ace5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ace5-125">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ace5-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ace5-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4ace5-126">INPUTS</span></span>

### <span data-ttu-id="4ace5-127">System.String</span><span class="sxs-lookup"><span data-stu-id="4ace5-127">System.String</span></span>

## <span data-ttu-id="4ace5-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4ace5-128">OUTPUTS</span></span>

### <span data-ttu-id="4ace5-129">Microsoft.Azure.Commands.Automation.Model.Module</span><span class="sxs-lookup"><span data-stu-id="4ace5-129">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="4ace5-130">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4ace5-130">NOTES</span></span>

## <span data-ttu-id="4ace5-131">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4ace5-131">RELATED LINKS</span></span>

[<span data-ttu-id="4ace5-132">New-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="4ace5-132">New-AzAutomationModule</span></span>](./New-AzAutomationModule.md)

[<span data-ttu-id="4ace5-133">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="4ace5-133">Remove-AzAutomationModule</span></span>](./Remove-AzAutomationModule.md)

[<span data-ttu-id="4ace5-134">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="4ace5-134">Set-AzAutomationModule</span></span>](./Set-AzAutomationModule.md)


