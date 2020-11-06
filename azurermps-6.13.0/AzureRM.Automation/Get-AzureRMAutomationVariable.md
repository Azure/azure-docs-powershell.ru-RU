---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 8FB78A4A-8392-44EE-A907-10FDF756071B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationVariable.md
ms.openlocfilehash: 7bd28149de46faa06420e87be8b83e7749ea248e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566855"
---
# <span data-ttu-id="d5865-101">Get-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="d5865-101">Get-AzureRmAutomationVariable</span></span>

## <span data-ttu-id="d5865-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d5865-102">SYNOPSIS</span></span>
<span data-ttu-id="d5865-103">Возвращает переменную автоматизации.</span><span class="sxs-lookup"><span data-stu-id="d5865-103">Gets an Automation variable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d5865-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d5865-104">SYNTAX</span></span>

### <span data-ttu-id="d5865-105">ByAll (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d5865-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationVariable [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5865-106">ByName</span><span class="sxs-lookup"><span data-stu-id="d5865-106">ByName</span></span>
```
Get-AzureRmAutomationVariable [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5865-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d5865-107">DESCRIPTION</span></span>
<span data-ttu-id="d5865-108">Командлет **Get-AzureRmAutomationVariable** получает одну или несколько переменных службы автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="d5865-108">The **Get-AzureRmAutomationVariable** cmdlet gets one or more Azure Automation variables.</span></span>
<span data-ttu-id="d5865-109">Чтобы получить определенную переменную, укажите ее имя.</span><span class="sxs-lookup"><span data-stu-id="d5865-109">To get a specific variable, specify its name.</span></span>

## <span data-ttu-id="d5865-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d5865-110">EXAMPLES</span></span>

### <span data-ttu-id="d5865-111">Пример 1: получение переменной</span><span class="sxs-lookup"><span data-stu-id="d5865-111">Example 1: Get a variable</span></span>
```
PS C:\>$Variable = Get-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "Variable06" -ResourceGroupName "ResourceGroup01"
PS C:\> $Value = $Variable.value
```

<span data-ttu-id="d5865-112">Первая команда получает переменную автоматизации с именем Variable06 в учетной записи с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="d5865-112">The first command gets an Automation variable named Variable06 in the account named Contoso17.</span></span>
<span data-ttu-id="d5865-113">Команда сохраняет этот объект в переменной $Variable.</span><span class="sxs-lookup"><span data-stu-id="d5865-113">The command stores that object in the $Variable variable.</span></span>
<span data-ttu-id="d5865-114">Во второй команде используется стандартная точечная нотация для ссылки на свойство **value** для $Variable.</span><span class="sxs-lookup"><span data-stu-id="d5865-114">The second command uses standard dot notation to refer to the **value** property of $Variable.</span></span>
<span data-ttu-id="d5865-115">Команда сохраняет значение в переменной $value.</span><span class="sxs-lookup"><span data-stu-id="d5865-115">The command stores the value in the $value variable.</span></span>

## <span data-ttu-id="d5865-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d5865-116">PARAMETERS</span></span>

### <span data-ttu-id="d5865-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d5865-117">-AutomationAccountName</span></span>
<span data-ttu-id="d5865-118">Указывает имя учетной записи автоматизации, содержащей переменные, которые получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="d5865-118">Specifies the name of the Automation account that contains the variables that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d5865-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5865-119">-DefaultProfile</span></span>
<span data-ttu-id="d5865-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="d5865-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d5865-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d5865-121">-Name</span></span>
<span data-ttu-id="d5865-122">Указывает имя переменной, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="d5865-122">Specifies the name of a variable that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d5865-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5865-123">-ResourceGroupName</span></span>
<span data-ttu-id="d5865-124">Указывает группу ресурсов, для которой этот командлет получает переменные.</span><span class="sxs-lookup"><span data-stu-id="d5865-124">Specifies the resource group for which this cmdlet gets variables.</span></span>

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

### <span data-ttu-id="d5865-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5865-125">CommonParameters</span></span>
<span data-ttu-id="d5865-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d5865-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5865-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5865-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5865-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d5865-128">INPUTS</span></span>

### <span data-ttu-id="d5865-129">System. String</span><span class="sxs-lookup"><span data-stu-id="d5865-129">System.String</span></span>

## <span data-ttu-id="d5865-130">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d5865-130">OUTPUTS</span></span>

### <span data-ttu-id="d5865-131">Microsoft. Azure. Commands. Automation. Model. Variable</span><span class="sxs-lookup"><span data-stu-id="d5865-131">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="d5865-132">Пуск</span><span class="sxs-lookup"><span data-stu-id="d5865-132">NOTES</span></span>

## <span data-ttu-id="d5865-133">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d5865-133">RELATED LINKS</span></span>

[<span data-ttu-id="d5865-134">New-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="d5865-134">New-AzureRmAutomationVariable</span></span>](./New-AzureRMAutomationVariable.md)

[<span data-ttu-id="d5865-135">Remove-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="d5865-135">Remove-AzureRmAutomationVariable</span></span>](./Remove-AzureRMAutomationVariable.md)

[<span data-ttu-id="d5865-136">Set-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="d5865-136">Set-AzureRmAutomationVariable</span></span>](./Set-AzureRMAutomationVariable.md)


