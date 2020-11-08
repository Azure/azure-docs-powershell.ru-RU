---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 8FB78A4A-8392-44EE-A907-10FDF756071B
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationVariable.md
ms.openlocfilehash: a8238cf9de2b0b20cb347d16bb74623f6469c03c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079217"
---
# <span data-ttu-id="0bd7a-101">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="0bd7a-101">Get-AzAutomationVariable</span></span>

## <span data-ttu-id="0bd7a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0bd7a-102">SYNOPSIS</span></span>
<span data-ttu-id="0bd7a-103">Возвращает переменную автоматизации.</span><span class="sxs-lookup"><span data-stu-id="0bd7a-103">Gets an Automation variable.</span></span>

## <span data-ttu-id="0bd7a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0bd7a-104">SYNTAX</span></span>

### <span data-ttu-id="0bd7a-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0bd7a-105">ByAll (Default)</span></span>
```
Get-AzAutomationVariable [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0bd7a-106">ByName</span><span class="sxs-lookup"><span data-stu-id="0bd7a-106">ByName</span></span>
```
Get-AzAutomationVariable [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0bd7a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0bd7a-107">DESCRIPTION</span></span>
<span data-ttu-id="0bd7a-108">Командлет **Get-AzAutomationVariable** получает одну или несколько переменных службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="0bd7a-108">The **Get-AzAutomationVariable** cmdlet gets one or more Azure Automation variables.</span></span>
<span data-ttu-id="0bd7a-109">Чтобы получить определенную переменную, укажите ее имя.</span><span class="sxs-lookup"><span data-stu-id="0bd7a-109">To get a specific variable, specify its name.</span></span>

## <span data-ttu-id="0bd7a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0bd7a-110">EXAMPLES</span></span>

### <span data-ttu-id="0bd7a-111">Пример 1: получение переменной</span><span class="sxs-lookup"><span data-stu-id="0bd7a-111">Example 1: Get a variable</span></span>
```
PS C:\>$Variable = Get-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "Variable06" -ResourceGroupName "ResourceGroup01"
PS C:\> $Value = $Variable.value
```

<span data-ttu-id="0bd7a-112">Первая команда получает переменную автоматизации с именем Variable06 в учетной записи с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="0bd7a-112">The first command gets an Automation variable named Variable06 in the account named Contoso17.</span></span>
<span data-ttu-id="0bd7a-113">Команда сохраняет этот объект в переменной $Variable.</span><span class="sxs-lookup"><span data-stu-id="0bd7a-113">The command stores that object in the $Variable variable.</span></span>
<span data-ttu-id="0bd7a-114">Во второй команде используется стандартная точечная нотация для ссылки на свойство **value** для $Variable.</span><span class="sxs-lookup"><span data-stu-id="0bd7a-114">The second command uses standard dot notation to refer to the **value** property of $Variable.</span></span>
<span data-ttu-id="0bd7a-115">Команда сохраняет значение в переменной $value.</span><span class="sxs-lookup"><span data-stu-id="0bd7a-115">The command stores the value in the $value variable.</span></span>

## <span data-ttu-id="0bd7a-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0bd7a-116">PARAMETERS</span></span>

### <span data-ttu-id="0bd7a-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0bd7a-117">-AutomationAccountName</span></span>
<span data-ttu-id="0bd7a-118">Указывает имя учетной записи автоматизации, содержащей переменные, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="0bd7a-118">Specifies the name of the Automation account that contains the variables that this cmdlet gets.</span></span>

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

### <span data-ttu-id="0bd7a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bd7a-119">-DefaultProfile</span></span>
<span data-ttu-id="0bd7a-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="0bd7a-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0bd7a-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0bd7a-121">-Name</span></span>
<span data-ttu-id="0bd7a-122">Указывает имя переменной, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="0bd7a-122">Specifies the name of a variable that this cmdlet gets.</span></span>

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

### <span data-ttu-id="0bd7a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bd7a-123">-ResourceGroupName</span></span>
<span data-ttu-id="0bd7a-124">Указывает группу ресурсов, для которой этот командлет получает переменные.</span><span class="sxs-lookup"><span data-stu-id="0bd7a-124">Specifies the resource group for which this cmdlet gets variables.</span></span>

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

### <span data-ttu-id="0bd7a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bd7a-125">CommonParameters</span></span>
<span data-ttu-id="0bd7a-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0bd7a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bd7a-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0bd7a-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bd7a-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0bd7a-128">INPUTS</span></span>

### <span data-ttu-id="0bd7a-129">System. String</span><span class="sxs-lookup"><span data-stu-id="0bd7a-129">System.String</span></span>

## <span data-ttu-id="0bd7a-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0bd7a-130">OUTPUTS</span></span>

### <span data-ttu-id="0bd7a-131">Microsoft. Azure. Commands. Automation. Model. Variable</span><span class="sxs-lookup"><span data-stu-id="0bd7a-131">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="0bd7a-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="0bd7a-132">NOTES</span></span>

## <span data-ttu-id="0bd7a-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0bd7a-133">RELATED LINKS</span></span>

[<span data-ttu-id="0bd7a-134">New-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="0bd7a-134">New-AzAutomationVariable</span></span>](./New-AzAutomationVariable.md)

[<span data-ttu-id="0bd7a-135">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="0bd7a-135">Remove-AzAutomationVariable</span></span>](./Remove-AzAutomationVariable.md)

[<span data-ttu-id="0bd7a-136">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="0bd7a-136">Set-AzAutomationVariable</span></span>](./Set-AzAutomationVariable.md)


