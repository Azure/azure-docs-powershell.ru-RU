---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 8FB78A4A-8392-44EE-A907-10FDF756071B
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationVariable.md
ms.openlocfilehash: c30e78b21c8f0dbc59e12c0fbecad14cfc93781a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014131"
---
# <span data-ttu-id="5f2ac-101">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="5f2ac-101">Get-AzAutomationVariable</span></span>

## <span data-ttu-id="5f2ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f2ac-102">SYNOPSIS</span></span>
<span data-ttu-id="5f2ac-103">Возвращает переменную автоматизации.</span><span class="sxs-lookup"><span data-stu-id="5f2ac-103">Gets an Automation variable.</span></span>

## <span data-ttu-id="5f2ac-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5f2ac-104">SYNTAX</span></span>

### <span data-ttu-id="5f2ac-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5f2ac-105">ByAll (Default)</span></span>
```
Get-AzAutomationVariable [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5f2ac-106">ByName</span><span class="sxs-lookup"><span data-stu-id="5f2ac-106">ByName</span></span>
```
Get-AzAutomationVariable [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f2ac-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5f2ac-107">DESCRIPTION</span></span>
<span data-ttu-id="5f2ac-108">Для **этого возвращается** одна или несколько переменных автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="5f2ac-108">The **Get-AzAutomationVariable** cmdlet gets one or more Azure Automation variables.</span></span>
<span data-ttu-id="5f2ac-109">Чтобы получить определенную переменную, укажите ее имя.</span><span class="sxs-lookup"><span data-stu-id="5f2ac-109">To get a specific variable, specify its name.</span></span>

## <span data-ttu-id="5f2ac-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5f2ac-110">EXAMPLES</span></span>

### <span data-ttu-id="5f2ac-111">Пример 1. Получить переменную</span><span class="sxs-lookup"><span data-stu-id="5f2ac-111">Example 1: Get a variable</span></span>
```
PS C:\>$Variable = Get-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "Variable06" -ResourceGroupName "ResourceGroup01"
PS C:\> $Value = $Variable.value
```

<span data-ttu-id="5f2ac-112">Первая команда получает переменную Автоматизации с именем Variable06 в учетной записи Contoso17.</span><span class="sxs-lookup"><span data-stu-id="5f2ac-112">The first command gets an Automation variable named Variable06 in the account named Contoso17.</span></span>
<span data-ttu-id="5f2ac-113">Эта команда сохраняет этот объект в $Variable переменной.</span><span class="sxs-lookup"><span data-stu-id="5f2ac-113">The command stores that object in the $Variable variable.</span></span>
<span data-ttu-id="5f2ac-114">Вторая команда использует стандартную точку для ссылки на свойство **значения** $Variable.</span><span class="sxs-lookup"><span data-stu-id="5f2ac-114">The second command uses standard dot notation to refer to the **value** property of $Variable.</span></span>
<span data-ttu-id="5f2ac-115">Команда сохраняет значение в переменной $value.</span><span class="sxs-lookup"><span data-stu-id="5f2ac-115">The command stores the value in the $value variable.</span></span>

## <span data-ttu-id="5f2ac-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5f2ac-116">PARAMETERS</span></span>

### <span data-ttu-id="5f2ac-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5f2ac-117">-AutomationAccountName</span></span>
<span data-ttu-id="5f2ac-118">Указывает имя учетной записи автоматизации, содержаной переменные, которые получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f2ac-118">Specifies the name of the Automation account that contains the variables that this cmdlet gets.</span></span>

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

### <span data-ttu-id="5f2ac-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f2ac-119">-DefaultProfile</span></span>
<span data-ttu-id="5f2ac-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="5f2ac-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5f2ac-121">-Name</span><span class="sxs-lookup"><span data-stu-id="5f2ac-121">-Name</span></span>
<span data-ttu-id="5f2ac-122">Указывает имя переменной, которая получается этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f2ac-122">Specifies the name of a variable that this cmdlet gets.</span></span>

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

### <span data-ttu-id="5f2ac-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f2ac-123">-ResourceGroupName</span></span>
<span data-ttu-id="5f2ac-124">Определяет группу ресурсов, для которой этот cmdlet получает переменные.</span><span class="sxs-lookup"><span data-stu-id="5f2ac-124">Specifies the resource group for which this cmdlet gets variables.</span></span>

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

### <span data-ttu-id="5f2ac-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f2ac-125">CommonParameters</span></span>
<span data-ttu-id="5f2ac-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f2ac-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f2ac-127">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f2ac-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f2ac-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5f2ac-128">INPUTS</span></span>

### <span data-ttu-id="5f2ac-129">System.String</span><span class="sxs-lookup"><span data-stu-id="5f2ac-129">System.String</span></span>

## <span data-ttu-id="5f2ac-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5f2ac-130">OUTPUTS</span></span>

### <span data-ttu-id="5f2ac-131">Microsoft.Azure.Commands.Automation.Model.Variable</span><span class="sxs-lookup"><span data-stu-id="5f2ac-131">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="5f2ac-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5f2ac-132">NOTES</span></span>

## <span data-ttu-id="5f2ac-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5f2ac-133">RELATED LINKS</span></span>

[<span data-ttu-id="5f2ac-134">New-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="5f2ac-134">New-AzAutomationVariable</span></span>](./New-AzAutomationVariable.md)

[<span data-ttu-id="5f2ac-135">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="5f2ac-135">Remove-AzAutomationVariable</span></span>](./Remove-AzAutomationVariable.md)

[<span data-ttu-id="5f2ac-136">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="5f2ac-136">Set-AzAutomationVariable</span></span>](./Set-AzAutomationVariable.md)


