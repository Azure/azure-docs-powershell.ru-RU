---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 5AF6F70F-7137-48E2-96ED-2C509042F127
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationVariable.md
ms.openlocfilehash: ea07e0d0b0c60b35186224d7ea0284df17d1e27b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731554"
---
# <span data-ttu-id="e58a2-101">New-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="e58a2-101">New-AzAutomationVariable</span></span>

## <span data-ttu-id="e58a2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e58a2-102">SYNOPSIS</span></span>
<span data-ttu-id="e58a2-103">Создает переменную автоматизации.</span><span class="sxs-lookup"><span data-stu-id="e58a2-103">Creates an Automation variable.</span></span>

## <span data-ttu-id="e58a2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e58a2-104">SYNTAX</span></span>

```
New-AzAutomationVariable [-Name] <String> -Encrypted <Boolean> [-Description <String>] [-Value <Object>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e58a2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e58a2-105">DESCRIPTION</span></span>
<span data-ttu-id="e58a2-106">Командлет **New-AzAutomationVariable** создает переменную в службе автоматизации Azure.</span><span class="sxs-lookup"><span data-stu-id="e58a2-106">The **New-AzAutomationVariable** cmdlet creates a variable in Azure Automation.</span></span>
<span data-ttu-id="e58a2-107">Чтобы зашифровать переменную, укажите *зашифрованный* параметр.</span><span class="sxs-lookup"><span data-stu-id="e58a2-107">To encrypt the variable, specify the *Encrypted* parameter.</span></span>
<span data-ttu-id="e58a2-108">После создания переменной невозможно изменить зашифрованное состояние.</span><span class="sxs-lookup"><span data-stu-id="e58a2-108">You cannot modify the encrypted state of a variable after creation.</span></span>

## <span data-ttu-id="e58a2-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e58a2-109">EXAMPLES</span></span>

### <span data-ttu-id="e58a2-110">Пример 1: создание переменной с простым значением</span><span class="sxs-lookup"><span data-stu-id="e58a2-110">Example 1: Create a variable with a simple value</span></span>
```
PS C:\>New-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -Encrypted $False -Value "My String" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="e58a2-111">Эта команда создает переменную с именем StringVariable22, которая имеет строковое значение в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="e58a2-111">This command creates a variable named StringVariable22 with a string value in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="e58a2-112">Пример 2: создание переменной со сложным значением</span><span class="sxs-lookup"><span data-stu-id="e58a2-112">Example 2: Create a variable with a complex value</span></span>
```
PS C:\>$VirtualMachine = Get-AzVM -ServiceName "VirtualMachine" -Name "VirtualMachine03"
PS C:\> New-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "ComplexVariable01" -Encrypted $False -Value $VirtualMachine -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="e58a2-113">Первая команда получает виртуальную машину с помощью командлета Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="e58a2-113">The first command gets a virtual machine by using the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="e58a2-114">Команда сохраняет его в переменной $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="e58a2-114">The command stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="e58a2-115">Вторая команда создает переменную с именем ComplexVariable01 в учетной записи автоматизации с именем Contoso17.</span><span class="sxs-lookup"><span data-stu-id="e58a2-115">The second command creates a variable named ComplexVariable01 in the Automation account named Contoso17.</span></span>
<span data-ttu-id="e58a2-116">Эта команда использует сложный объект для его значения (в данном случае — виртуальная машина в $VirtualMachine).</span><span class="sxs-lookup"><span data-stu-id="e58a2-116">This command uses a complex object for its value, in this case, the virtual machine in $VirtualMachine.</span></span>

## <span data-ttu-id="e58a2-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e58a2-117">PARAMETERS</span></span>

### <span data-ttu-id="e58a2-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e58a2-118">-AutomationAccountName</span></span>
<span data-ttu-id="e58a2-119">Указывает имя учетной записи автоматизации, в которой будет храниться переменная.</span><span class="sxs-lookup"><span data-stu-id="e58a2-119">Specifies the name of the Automation account in which to store the variable.</span></span>

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

### <span data-ttu-id="e58a2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e58a2-120">-DefaultProfile</span></span>
<span data-ttu-id="e58a2-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="e58a2-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e58a2-122">-Описание</span><span class="sxs-lookup"><span data-stu-id="e58a2-122">-Description</span></span>
<span data-ttu-id="e58a2-123">Задает описание переменной.</span><span class="sxs-lookup"><span data-stu-id="e58a2-123">Specifies a description for the variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e58a2-124">С шифрованием</span><span class="sxs-lookup"><span data-stu-id="e58a2-124">-Encrypted</span></span>
<span data-ttu-id="e58a2-125">Указывает, шифрует ли этот командлет значение переменной для хранения.</span><span class="sxs-lookup"><span data-stu-id="e58a2-125">Specifies whether this cmdlet encrypts the value of the variable for storage.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e58a2-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e58a2-126">-Name</span></span>
<span data-ttu-id="e58a2-127">Задает имя переменной.</span><span class="sxs-lookup"><span data-stu-id="e58a2-127">Specifies a name for the variable.</span></span>

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

### <span data-ttu-id="e58a2-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e58a2-128">-ResourceGroupName</span></span>
<span data-ttu-id="e58a2-129">Указывает группу ресурсов, для которой этот командлет создает переменную.</span><span class="sxs-lookup"><span data-stu-id="e58a2-129">Specifies the resource group for which this cmdlet creates a variable.</span></span>

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

### <span data-ttu-id="e58a2-130">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="e58a2-130">-Value</span></span>
<span data-ttu-id="e58a2-131">Задает значение переменной.</span><span class="sxs-lookup"><span data-stu-id="e58a2-131">Specifies a value for the variable.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e58a2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e58a2-132">CommonParameters</span></span>
<span data-ttu-id="e58a2-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e58a2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e58a2-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e58a2-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e58a2-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e58a2-135">INPUTS</span></span>

### <span data-ttu-id="e58a2-136">System. String</span><span class="sxs-lookup"><span data-stu-id="e58a2-136">System.String</span></span>

### <span data-ttu-id="e58a2-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e58a2-137">System.Boolean</span></span>

### <span data-ttu-id="e58a2-138">System. Object</span><span class="sxs-lookup"><span data-stu-id="e58a2-138">System.Object</span></span>

## <span data-ttu-id="e58a2-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e58a2-139">OUTPUTS</span></span>

### <span data-ttu-id="e58a2-140">Microsoft. Azure. Commands. Automation. Model. Variable</span><span class="sxs-lookup"><span data-stu-id="e58a2-140">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="e58a2-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="e58a2-141">NOTES</span></span>

## <span data-ttu-id="e58a2-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e58a2-142">RELATED LINKS</span></span>

[<span data-ttu-id="e58a2-143">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="e58a2-143">Get-AzAutomationVariable</span></span>](./Get-AzAutomationVariable.md)

[<span data-ttu-id="e58a2-144">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="e58a2-144">Remove-AzAutomationVariable</span></span>](./Remove-AzAutomationVariable.md)

[<span data-ttu-id="e58a2-145">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="e58a2-145">Set-AzAutomationVariable</span></span>](./Set-AzAutomationVariable.md)


