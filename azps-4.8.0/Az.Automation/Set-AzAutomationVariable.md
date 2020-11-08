---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: F344D8D1-5593-4C09-A1CA-37579D2A3A61
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationVariable.md
ms.openlocfilehash: 0ca1e99b68f7cca8d39647357ee81770ea41cefc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078503"
---
# <span data-ttu-id="48054-101">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="48054-101">Set-AzAutomationVariable</span></span>

## <span data-ttu-id="48054-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="48054-102">SYNOPSIS</span></span>
<span data-ttu-id="48054-103">Изменяет переменную автоматизации.</span><span class="sxs-lookup"><span data-stu-id="48054-103">Modifies an Automation variable.</span></span>

## <span data-ttu-id="48054-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="48054-104">SYNTAX</span></span>

### <span data-ttu-id="48054-105">UpdateVariableValue</span><span class="sxs-lookup"><span data-stu-id="48054-105">UpdateVariableValue</span></span>
```
Set-AzAutomationVariable [-Name] <String> -Encrypted <Boolean> -Value <Object> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="48054-106">UpdateVariableDescription</span><span class="sxs-lookup"><span data-stu-id="48054-106">UpdateVariableDescription</span></span>
```
Set-AzAutomationVariable [-Name] <String> -Description <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="48054-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="48054-107">DESCRIPTION</span></span>
<span data-ttu-id="48054-108">Командлет **Set-AzAutomationVariable** изменяет значение или описание переменной в Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="48054-108">The **Set-AzAutomationVariable** cmdlet modifies the value or description of a variable in Azure Automation.</span></span>
<span data-ttu-id="48054-109">Чтобы зашифровать переменную, укажите *зашифрованный* параметр.</span><span class="sxs-lookup"><span data-stu-id="48054-109">To encrypt the variable, specify the *Encrypted* parameter.</span></span>
<span data-ttu-id="48054-110">После создания переменной невозможно изменить зашифрованное состояние.</span><span class="sxs-lookup"><span data-stu-id="48054-110">You cannot modify the encrypted state of a variable after creation.</span></span>
<span data-ttu-id="48054-111">Если задать для существующей, незашифрованной переменной значение *Encrypted* , то переменная не будет выполнена.</span><span class="sxs-lookup"><span data-stu-id="48054-111">Specifying *Encrypted* for an existing, non-encrypted, variable fails.</span></span>

## <span data-ttu-id="48054-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="48054-112">EXAMPLES</span></span>

### <span data-ttu-id="48054-113">Пример 1: Установка значения переменной</span><span class="sxs-lookup"><span data-stu-id="48054-113">Example 1: Set the value of a variable</span></span>
```
PS C:\>Set-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -ResourceGroupName "ResourceGroup01" -Value "New Value" -Encrypted $False
```

<span data-ttu-id="48054-114">Эта команда задает новое значение переменной с именем StringVariable22 в учетной записи службы автоматизации Azure с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="48054-114">This command sets a new value for the variable named StringVariable22 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="48054-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="48054-115">PARAMETERS</span></span>

### <span data-ttu-id="48054-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="48054-116">-AutomationAccountName</span></span>
<span data-ttu-id="48054-117">Указывает имя учетной записи автоматизации, в которой хранится переменная.</span><span class="sxs-lookup"><span data-stu-id="48054-117">Specifies the name of the Automation account in which the variable is stored.</span></span>

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

### <span data-ttu-id="48054-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48054-118">-DefaultProfile</span></span>
<span data-ttu-id="48054-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="48054-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="48054-120">-Описание</span><span class="sxs-lookup"><span data-stu-id="48054-120">-Description</span></span>
<span data-ttu-id="48054-121">Задает описание переменной.</span><span class="sxs-lookup"><span data-stu-id="48054-121">Specifies a description for the variable.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateVariableDescription
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48054-122">С шифрованием</span><span class="sxs-lookup"><span data-stu-id="48054-122">-Encrypted</span></span>
<span data-ttu-id="48054-123">Указывает, шифрует ли командлет значение переменной для хранения.</span><span class="sxs-lookup"><span data-stu-id="48054-123">Specifies whether cmdlet encrypts the value of the variable for storage.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: UpdateVariableValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48054-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="48054-124">-Name</span></span>
<span data-ttu-id="48054-125">Указывает имя переменной, измененной этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="48054-125">Specifies the name of the variable that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48054-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48054-126">-ResourceGroupName</span></span>
<span data-ttu-id="48054-127">Указывает группу ресурсов, для которой этот командлет изменяет переменную.</span><span class="sxs-lookup"><span data-stu-id="48054-127">Specifies the resource group for which this cmdlet modifies a variable.</span></span>

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

### <span data-ttu-id="48054-128">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="48054-128">-Value</span></span>
<span data-ttu-id="48054-129">Задает значение переменной.</span><span class="sxs-lookup"><span data-stu-id="48054-129">Specifies a value for the variable.</span></span>

```yaml
Type: System.Object
Parameter Sets: UpdateVariableValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48054-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48054-130">CommonParameters</span></span>
<span data-ttu-id="48054-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="48054-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48054-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48054-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48054-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="48054-133">INPUTS</span></span>

### <span data-ttu-id="48054-134">System. String</span><span class="sxs-lookup"><span data-stu-id="48054-134">System.String</span></span>

### <span data-ttu-id="48054-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="48054-135">System.Boolean</span></span>

### <span data-ttu-id="48054-136">System. Object</span><span class="sxs-lookup"><span data-stu-id="48054-136">System.Object</span></span>

## <span data-ttu-id="48054-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="48054-137">OUTPUTS</span></span>

### <span data-ttu-id="48054-138">Microsoft. Azure. Commands. Automation. Model. Variable</span><span class="sxs-lookup"><span data-stu-id="48054-138">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="48054-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="48054-139">NOTES</span></span>

## <span data-ttu-id="48054-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="48054-140">RELATED LINKS</span></span>

[<span data-ttu-id="48054-141">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="48054-141">Get-AzAutomationVariable</span></span>](./Get-AzAutomationVariable.md)

[<span data-ttu-id="48054-142">New-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="48054-142">New-AzAutomationVariable</span></span>](./New-AzAutomationVariable.md)

[<span data-ttu-id="48054-143">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="48054-143">Remove-AzAutomationVariable</span></span>](./Remove-AzAutomationVariable.md)


