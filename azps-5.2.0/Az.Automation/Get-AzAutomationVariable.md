---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 8FB78A4A-8392-44EE-A907-10FDF756071B
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationVariable.md
ms.openlocfilehash: a8238cf9de2b0b20cb347d16bb74623f6469c03c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98418591"
---
# <span data-ttu-id="6f2ff-101">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="6f2ff-101">Get-AzAutomationVariable</span></span>

## <span data-ttu-id="6f2ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f2ff-102">SYNOPSIS</span></span>
<span data-ttu-id="6f2ff-103">Возвращает переменную автоматизации.</span><span class="sxs-lookup"><span data-stu-id="6f2ff-103">Gets an Automation variable.</span></span>

## <span data-ttu-id="6f2ff-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6f2ff-104">SYNTAX</span></span>

### <span data-ttu-id="6f2ff-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6f2ff-105">ByAll (Default)</span></span>
```
Get-AzAutomationVariable [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6f2ff-106">ByName</span><span class="sxs-lookup"><span data-stu-id="6f2ff-106">ByName</span></span>
```
Get-AzAutomationVariable [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f2ff-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6f2ff-107">DESCRIPTION</span></span>
<span data-ttu-id="6f2ff-108">Для **этого возвращается** одна или несколько переменных автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="6f2ff-108">The **Get-AzAutomationVariable** cmdlet gets one or more Azure Automation variables.</span></span>
<span data-ttu-id="6f2ff-109">Чтобы получить определенную переменную, укажите ее имя.</span><span class="sxs-lookup"><span data-stu-id="6f2ff-109">To get a specific variable, specify its name.</span></span>

## <span data-ttu-id="6f2ff-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6f2ff-110">EXAMPLES</span></span>

### <span data-ttu-id="6f2ff-111">Пример 1. Получить переменную</span><span class="sxs-lookup"><span data-stu-id="6f2ff-111">Example 1: Get a variable</span></span>
```
PS C:\>$Variable = Get-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "Variable06" -ResourceGroupName "ResourceGroup01"
PS C:\> $Value = $Variable.value
```

<span data-ttu-id="6f2ff-112">Первая команда получает переменную Автоматизации с именем Variable06 в учетной записи Contoso17.</span><span class="sxs-lookup"><span data-stu-id="6f2ff-112">The first command gets an Automation variable named Variable06 in the account named Contoso17.</span></span>
<span data-ttu-id="6f2ff-113">Эта команда сохраняет объект в переменной $Variable.</span><span class="sxs-lookup"><span data-stu-id="6f2ff-113">The command stores that object in the $Variable variable.</span></span>
<span data-ttu-id="6f2ff-114">Вторая команда использует стандартную точку для ссылки на свойство **значения** $Variable.</span><span class="sxs-lookup"><span data-stu-id="6f2ff-114">The second command uses standard dot notation to refer to the **value** property of $Variable.</span></span>
<span data-ttu-id="6f2ff-115">Команда сохраняет значение в переменной $value.</span><span class="sxs-lookup"><span data-stu-id="6f2ff-115">The command stores the value in the $value variable.</span></span>

## <span data-ttu-id="6f2ff-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6f2ff-116">PARAMETERS</span></span>

### <span data-ttu-id="6f2ff-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6f2ff-117">-AutomationAccountName</span></span>
<span data-ttu-id="6f2ff-118">Указывает имя учетной записи автоматизации, содержаной переменные, которые получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f2ff-118">Specifies the name of the Automation account that contains the variables that this cmdlet gets.</span></span>

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

### <span data-ttu-id="6f2ff-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f2ff-119">-DefaultProfile</span></span>
<span data-ttu-id="6f2ff-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="6f2ff-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6f2ff-121">-Name</span><span class="sxs-lookup"><span data-stu-id="6f2ff-121">-Name</span></span>
<span data-ttu-id="6f2ff-122">Указывает имя переменной, которая получается этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f2ff-122">Specifies the name of a variable that this cmdlet gets.</span></span>

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

### <span data-ttu-id="6f2ff-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f2ff-123">-ResourceGroupName</span></span>
<span data-ttu-id="6f2ff-124">Определяет группу ресурсов, для которой этот cmdlet получает переменные.</span><span class="sxs-lookup"><span data-stu-id="6f2ff-124">Specifies the resource group for which this cmdlet gets variables.</span></span>

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

### <span data-ttu-id="6f2ff-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f2ff-125">CommonParameters</span></span>
<span data-ttu-id="6f2ff-126">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f2ff-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f2ff-127">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f2ff-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f2ff-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6f2ff-128">INPUTS</span></span>

### <span data-ttu-id="6f2ff-129">System.String</span><span class="sxs-lookup"><span data-stu-id="6f2ff-129">System.String</span></span>

## <span data-ttu-id="6f2ff-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6f2ff-130">OUTPUTS</span></span>

### <span data-ttu-id="6f2ff-131">Microsoft.Azure.Commands.Automation.Model.Variable</span><span class="sxs-lookup"><span data-stu-id="6f2ff-131">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="6f2ff-132">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6f2ff-132">NOTES</span></span>

## <span data-ttu-id="6f2ff-133">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6f2ff-133">RELATED LINKS</span></span>

[<span data-ttu-id="6f2ff-134">New-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="6f2ff-134">New-AzAutomationVariable</span></span>](./New-AzAutomationVariable.md)

[<span data-ttu-id="6f2ff-135">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="6f2ff-135">Remove-AzAutomationVariable</span></span>](./Remove-AzAutomationVariable.md)

[<span data-ttu-id="6f2ff-136">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="6f2ff-136">Set-AzAutomationVariable</span></span>](./Set-AzAutomationVariable.md)


